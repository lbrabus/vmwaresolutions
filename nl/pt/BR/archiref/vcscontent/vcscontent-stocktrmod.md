---

copyright:

  years:  2016, 2018

lastupdated: "2018-11-15"

---

{:tip: .tip}
{:note: .note}
{:important: .important}

# Transformar o Stock Trader do WebSphere Application Server em Stock Trader em contêineres

A próxima etapa na jornada de modernização do Stock Trader é transformar a carga de trabalho de execução em máquinas virtuais (VMs) para execução em contêineres.

Para continuar, Todd e Jane executam o Transformation Advisor para analisar a carga de trabalho do Stock Trader, identificar qualquer complexidade de migração e recomendar mudanças. Quando pronto, eles usam o Transformation Advisor para implementar o Stock Trader em contêineres do Liberty que são executados no {{site.data.keyword.cloud}} Private (ICP).

## Preparar o IBM Cloud Private

Primeiro, Todd precisa instalar o ICP. Como Todd tem seu VMware no ambiente do {{site.data.keyword.cloud_notm}}, ele decide usar a oferta {{site.data.keyword.cloud_notm}} Privada Hosted que fornece a ele uma instância completa do ICP que é executada em VMs VMware no {{site.data.keyword.cloud_notm}}.

O painel padrão fornece uma interface com o usuário abrangente para gerenciar o cluster do Kubernetes, segurança, armazenamento e implementação por meio do catálogo.

### Preparar o armazenamento

O {{site.data.keyword.cloud_notm}} Private Hosted está configurado pronto para utilização com o GlusterFS e fornece armazenamento de arquivo entre VMs como nós dedicados do GlusterFS. O valor de GlusterFS é que ele permite o fornecimento dinâmico. Se Todd desejar, ele poderá configurar VMs extras como servidores NFS.

Como Todd desejava um servidor NFS disponível para ele, ele identificou uma VM chamada ‘toddnfs’ e executou estas
[etapas](https://help.ubuntu.com/community/SettingUpNFSHowTo).

Todd executa os comandos a seguir para criar um novo servidor NFS:

`ssh root@toodnfs.acme.com`

`apt-get install nfs-kernel-server`

`mkdir -p /shared`

`chown nobody:nogroup /shared`

`vi /etc/exports`

Em seguida, Todd inclui a linha a seguir:

`/shared \*(rw,no_subtree_check,async,insecure,no_root_squash)`

`systemctl restart nfs-kernel-server`

Em seguida, Todd executa o comando a seguir em cada VM para instalar o NFS em cada VM do trabalhador do ICP:

`sudo apt-get update`

`sudo apt-get install nfs-common`

Todd executa o comando a seguir para confirmar a versão instalada:

`apt-cache policy nfs-common`

Sempre que um novo volume NFS for necessário, Todd executa o comando a seguir para criar um novo volume NFS, quando necessário:

`cd /shared`

`mkdir -p <foldername>`

`chmod 777 <foldername>`

### Preparar a segurança de imagem

No ICP V3.1, a segurança é aprimorada requerendo uma política de imagem adequada antes que qualquer imagem seja puxada para uma instância do ICP. O aprimoramento requer que você inclua uma política de imagem onde as imagens da IBM residem, *dockerhub/ibmcom*, e no armazenamento do docker.

O ibmcloud-default-cluster-image-policy é fornecido por padrão e abrange quaisquer imagens da IBM em docker.io/ibmcom/\*, mas como o Db2 e outros conteúdos da IBM estão localizados no Docker Store, outra política de imagem para o armazenamento do docker, *docker.io/store/ibmcorp/*, é necessária.

Além disso, alguns conteúdos requerem um conjunto de políticas de segurança de pod para permitir acesso específico para o pod. Por exemplo, o Db2 requer uma política para clientes que desejam executar o Db2 em um namespace diferente de 'default'.

Saiba mais no [IBM Knowledge
Center](https://www.ibm.com/support/knowledgecenter/SSBS6K_3.1.0/manage_cluster/enable_pod_security.html).

## Implementar o Transformation Advisor e o Microclimate

Depois que Todd tiver o ICP em execução, ele instalará o Transformation Advisor junto com o Microclimate. Todd abre o [catálogo](https://www.ibm.com/cloud/private/developer) e visualiza todo o conteúdo disponível.

Todd procura o Transformation Advisor e o Microclimate e os instala usando as instruções do arquivo leia-me fornecido quando ele clica no gráfico helm.

### Executar o Transformation Advisor

Para executar o Transformation Advisor, Jane incluiu o coletor de dados na VM que executa o Stock Trader no WebSphere e abre a interface com o usuário [Transformation
Advisor](https://developer.ibm.com/recipes/tutorials/using-the-transformation-advisor-on-ibm-cloud-private/) para visualizar os resultados.

Jane clicou em Stock Trader e vê a recomendação de executar cada arquivo war no Liberty e que a maioria da migração seria simples com uma migração moderada. Jane clica em Detalhes da migração e vê que o Transformation Advisor fornece arquivos de implementação que ela pode usar para concluir a migração. Depois que Jane faz upload dos arquivos binários para o Transformation Advisor, ela usa as APIs fornecidas pelo Microclimate para implementar os contêineres do liberty.

No final, as opções de layout resultantes do Stock Trader são:
* Único contêiner do Liberty - se Jane implementa um tempo de execução do Liberty e inclui seu app Stock Trader nesse único contêiner.
* Múltiplos contêineres do Liberty - um para cada arquivo .war como o Transformation Advisor recomenda para o Stock Trader.

Todd não alterou a origem de dados durante a etapa de transformação. O Transformation Advisor toma a configuração de origem de dados do WebSphere Application Server Network Deployment e a inclui no server.xml do contêiner do Liberty.
{:important}

### Links relacionados

* [Visão geral do vCenter Server on {{site.data.keyword.cloud_notm}} with Hybridity Bundle](../vcs/vcs-hybridity-intro.html)
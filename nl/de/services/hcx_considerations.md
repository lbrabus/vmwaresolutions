---

copyright:

  years:  2016, 2018

lastupdated: "2018-06-07"

---

# Überblick zu VMware HCX on IBM Cloud

Der Service "HCX on {{site.data.keyword.cloud}}" kann die Netze von lokalen Rechenzentren nahtlos in die {{site.data.keyword.cloud_notm}} erweitern. Dies ermöglicht die Migration von virtuellen Maschinen in die und aus der {{site.data.keyword.cloud_notm}}, ohne dass hierzu eine Konvertierung oder Änderung erforderlich ist.

**Verfügbarkeit**: Dieser Service ist nur für Instanzen von VMware vCenter Server on IBM Cloud with Hybridity Bundle verfügbar, die in V2.3 und höheren Releases bereitgestellt werden.

Sie können für Ihre vorhandene vCenter Server-Instanz ein Upgrade auf eine vCenter Server with Hybridity Bundle-Instanz durchführen. Weitere Informationen zum Upgrade Ihrer Instanz und zur Bereitstellung des Service "HCX on {{site.data.keyword.cloud_notm}}" finden Sie unter [Upgrade auf vCenter Server with Hybridity Bundle-Instanz durchführen](../vcenter/vc_applyingupdates.html#applying-updates-to-vcenter-server-instances.html#upgrading-to-the-vcenter-server-with-hybridity-bundle-instance).

**Hinweis:** Eine vCenter Server-Instanz mit HCX on {{site.data.keyword.cloud_notm}} ist auf drei simultane Verbindungen von lokalen Standorten begrenzt.

## Hinweise zur Installation von HCX on IBM Cloud

Lesen Sie die folgenden Hinweise, bevor Sie versuchen, HCX on {{site.data.keyword.cloud_notm}} zu installieren.

### Anforderungen an die Anzahl der ESXi-Server

Der Service "HCX on {{site.data.keyword.cloud_notm}}" kann nicht in einer Instanz installiert werden, für die der Standardcluster mehr als 51 ESXi-Server umfasst. Da HCX on {{site.data.keyword.cloud_notm}} acht IP-Adressen im vMotion-Teilnetz aus dem Standardcluster benötigt, sind keine IP-Adressen im vMotion-Teilnetz für HCX on {{site.data.keyword.cloud_notm}} verfügbar, wenn die Anzahl der ESXi-Server 51 überschreitet.

### Anforderungen an Firewallregeln

Bevor Sie den Service "HCX on {{site.data.keyword.cloud_notm}}" installieren, müssen Sie eine Firewallregel zu vorhandenen Firewalls hinzufügen, um den gesamten abgehenden HTTPS-Datenverkehr zuzulassen, damit die virtuelle Appliance für den HCX-Manager sich selbst registrieren kann. Nachdem die Installation des HCX-Managers abgeschlossen ist, können Sie die Firewallregel entfernen. Darüber hinaus müssen Sie Firewallregeln konfigurieren, damit HCX ordnungsgemäß funktionieren kann. Weitere Informationen finden Sie in *Anhang A - Portzugriffsvoraussetzungen* unter der [Architektur von HCX on {{site.data.keyword.cloud_notm}}](https://www.ibm.com/cloud/garage/files/HCX_Architecture_Design.pdf).

## Hinweise zum Entfernen von HCX on IBM Cloud

Lesen Sie die folgenden Hinweise, bevor Sie den Service "HCX on {{site.data.keyword.cloud_notm}}" entfernen:
* Stellen Sie sicher, dass die Verbindungen und erweiterten Netze zwischen dem lokalen Quellenstandort und den {{site.data.keyword.cloud_notm}}-Zielstandorten entfernt wurden. Verwenden Sie zum Entfernen der Verbindungen und erweiterten Netze die HCX-Benutzerschnittstelle in der lokalen Instanz von VMware vSphere Web Client.
* Stellen Sie sicher, dass die Standortpaarungen zwischen dem lokalen Quellenstandort und den {{site.data.keyword.cloud_notm}}-Zielstandorten entfernt wurden. Verwenden Sie zum Entfernen der Standortpaarungen die HCX-Benutzerschnittstelle in der lokalen Instanz von VMware vSphere Web Client.
* Das Entfernen von HCX on {{site.data.keyword.cloud_notm}} ist nicht automatisiert. Die folgenden Prozeduren müssen für das erfolgreiche Entfernen dieses Service durchgeführt werden:
   * Inaktivieren Sie die für den cloudseitigen HCX-Manager bestellte HCX-Lizenz.
   * Löschen Sie den HCX-Manager.
   * Geben Sie die vMotion-IP-Adressen frei, die für HCX reserviert wurden.
   * Entfernen Sie die HCX-bezogenen Ressourcenpools, wenn diese leer sind.
   * Entfernen Sie die HCX-bezogenen Ordner, wenn diese leer sind.
   * Löschen Sie die Appliances für das HCX-Management-Edge.

## Zugehörige Links

* [HCX on {{site.data.keyword.cloud_notm}} bestellen](hcx_ordering.html)
* [HCX on {{site.data.keyword.cloud_notm}} verwalten](managinghcx.html)
* [Glossar der HCX-Begriffe](hcx_glossary.html)
* [Kontaktaufnahme mit dem IBM Support](../vmonic/trbl_support.html)
* [VMware Hybrid Cloud Extension overview](https://cloud.vmware.com/vmware-hcx)
* [VMware Hybrid Cloud Extension documentation](https://hcx.vmware.com/#vm-documentation)
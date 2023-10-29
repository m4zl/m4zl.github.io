# Microsoft Office — Guides

***
## C2R Installationen
***


### Download Source Files

1. Download des Office Customization Tool (ODT) in einen Ordner der Wahl (z.B. "C:\\office2019-pro-plus")
2. Erstellen oder bearbeiten der Konfigurations-Datei (siehe Beispiel "configuration.xml" ) 
3. 

``` { .xml }
<Configuration>
  <Add SourcePath="C:\office2019-pro-plus"     
    OfficeClientEdition="64"
    Channel="PerpetualVL2021" >
    <Product ID="ProPlus2021Volume">
    <Language ID="de-de" />
    <Language ID="en-us" />
    </Product>
  </Add>
  <Display Level="Full" AcceptEULA="TRUE" />  
</Configuration>
```
configuration.xml



***
## Outlook
***

### Deaktivieren von Office 365 Autodiscover in Outlook

 > Wenn Sie ein Nicht-Office365-Postfach oder ein lokales Exchange-Postfach verwenden, versucht Outlook, Ihr Microsoft-Konto zu erkennen, auch wenn die AutoErmittlung nicht auf Microsoft 365 verweist. 
 > Sie können diese Prüfung für einen lokalen Exchange Server deaktivieren. Gehen Sie zum Registrierungsschlüssel `HKEY_CURRENT_USER\Software \Microsoft\Office\16.0\Outlook\AutoDiscover` und erstellen Sie einen neuen DWORD-Parameter mit dem Namen `ExcludeExplicitO365Endpoint` und dem Wert `1`. Starten Sie Outlook neu.


Mit dem folgenden Befehl können Sie Änderungen an der Registry vornehmen:

```batch
reg add HKEY_CURRENT_USER\Software\Microsoft\Office\x.0\Outlook\AutoDiscover /t REG_DWORD /v ExcludeExplicitO365Endpoint /d 1
```

oder mit dem Powershell cmdlet:

```powershell
Set-ItemProperty -Path "HKCU:\Software\Microsoft\Office\16.0\Outlook\AutoDiscover" -Name 'ExcludeExplicitO365Endpoint' -Value 1 -Type DWORD –Force
```
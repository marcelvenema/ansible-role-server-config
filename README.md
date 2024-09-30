# VM Config

<table border="0">
  <tr>
    <td width="160px" valign="top"><img src="media/icon_vm_config.png" align="left" height="128" width="128" /></td>
    <td>Ansible playbooks voor configuratie van een server.<br/>
        <br/>
        <br/>
        Wordt mogelijk in de toekomst vervangen door Ansile role os-settings.<br/>
    </td>
  </tr>
</table>

# Diensten:

action: **first_config**<br/>
Initiele configuratie van server, o.a. set hostname, timezone, install apps, etc. <br/>
variabelen:<br/>
<kbd>server_hostname</kbd> : naam van de server.<br/>
<kbd>timezone</kbd> (optioneel) : Voorbeeld: 'Europe/Amsterdam'.

action: **configure_server**<br/>
Configuratie van server, o.a. aanmaken admin user.<br/>
variabelen:<br/>
<kbd>admin_username</kbd> (optioneel) : Gebruikersnaam admin user, standaard is 'admin'.<br/>
<kbd>admin_password</kbd> (optioneel) : Wachtwoord van admin user, standaard is automatisch gegenereerd.<br/>

action: **configure_vault**<br/>
Configuratie van server gegevens in Hashicorp Vault.<br/>
variabelen:<br/>
<kbd>vault_address</kbd> : URL naar vault adres voor toegang vault, bijvoorbeeld `http://localhost:8081`. <br/>
<kbd>vault_token</kbd> : token voor toegang tot vault.<br/>
<kbd>admin_username</kbd> (optioneel) : Gebruikersnaam admin user, standaard is 'admin'.<br/>
<kbd>admin_password</kbd> (optioneel) : Wachtwoord van admin user, standaard is automatisch gegenereerd.<br/>
<kbd>automation_username</kbd> (optioneel) : Gebruikersnaam automation user, standaard is 'ansible'.<br/>
<kbd>automation_password</kbd> (optioneel) : Wachtwoord van automation user, standaard is automatisch gegenereerd.<br/>
<kbd>automation_email</kbd> (optioneel) : "email@mindef.nl"<br/>

action: **initialize**<br/>
Initialiseer omgeving, test Vault verbinding.<br/>
variabelen:<br/>
<kbd>vault_address</kbd> : URL naar vault adres voor toegang vault, bijvoorbeeld `http://localhost:8081`.<br/>
<kbd>vault_token</kbd> : token voor toegang tot vault.<br/>

***

- **changelog**<br/>
  Wijzigingen logboek.<br/>
  Zie [changelog](CHANGELOG.md)<br/>

- **roadmap**<br/>
  Visie en toekomstige ontwikkelingen.<br/>
  Zie [roadmap](ROADMAP.md)<br/>

***

## Voorbereidingen
(geen)<br/>

## Afhankelijkheden
Afhankelijkheden zijn benoemd in het **requirements.yml** bestand. Gebruik `ansible-galaxy install -r requirements.yml --force` voor installatie.<br/>

Indien deze role in andere playbooks of Ansible projecten wordt gebruikt, dient de URL van deze rol te worden toegevoegd aan het `requirements.yml` bestand. Via bovenstaand command wordt de rol dan in de juiste folderstructuur geplaatst.<br/>
Let op! Vergewis u dat de inhoud van `requirements.yml` verwijst naar de juiste repositories.<br/>
<br/>


## Installatie
Geen installatie benodigd.<br/>


## Configuratie
(geen).<br/>


## Overige informatie
(geen).<br/>


## Licentie
MIT


## Auteur
Marcel Venema

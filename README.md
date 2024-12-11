# VM Config

<table border="0">
  <tr>
    <td width="160px" valign="top"><img src="media/icon_vm_config.png" align="left" height="128" width="128" /></td>
    <td>Ansible playbooks for server configuration.<br/>
        <br/>
        <br/>
        May be replaced by Ansile role os-settings in the future.<br/>
    </td>
  </tr>
</table>

# Services:

action: **first_config**<br/>
Initial server configuration, e.g., set hostname, timezone, install apps, etc. <br/>
variables:<br/>
<kbd>server_hostname</kbd> : name of the server.<br/>
<kbd>timezone</kbd> (optional) : Example: 'Europe/Amsterdam'.

action: **configure_server**<br/>
Server configuration, e.g., create admin user.<br/>
variables:<br/>
<kbd>admin_username</kbd> (optional) : Username of admin user, default is 'admin'.<br/>
<kbd>admin_password</kbd> (optional) : Password of admin user, default is automatically generated.<br/>

action: **configure_vault**<br/>
Server configuration in Hashicorp Vault.<br/>
variables:<br/>
<kbd>vault_address</kbd> : URL to vault address for vault access, e.g., `http://localhost:8081`. <br/>
<kbd>vault_token</kbd> : token for vault access.<br/>
<kbd>admin_username</kbd> (optional) : Username of admin user, default is 'admin'.<br/>
<kbd>admin_password</kbd> (optional) : Password of admin user, default is automatically generated.<br/>
<kbd>automation_username</kbd> (optional) : Username of automation user, default is 'ansible'.<br/>
<kbd>automation_password</kbd> (optional) : Password of automation user, default is automatically generated.<br/>
<kbd>automation_email</kbd> (optional) : Email address of automation user.<br/>

action: **initialize**<br/>
Initialize environment, test Vault connection.<br/>
variables:<br/>
<kbd>vault_address</kbd> : URL to vault address for vault access, e.g., `http://localhost:8081`.<br/>
<kbd>vault_token</kbd> : token for vault access.<br/>

***

- **changelog**<br/>
  Change log.<br/>
  See [changelog](CHANGELOG.md)<br/>

- **roadmap**<br/>
  Vision and future developments.<br/>
  See [roadmap](ROADMAP.md)<br/>

***

## Preparations
(none)<br/>

## Dependencies
Dependencies are listed in the **requirements.yml** file. Use `ansible-galaxy install -r requirements.yml --force` for installation.<br/>

If this role is used in other playbooks or Ansible projects, the URL of this role should be added to the `requirements.yml` file. Using the above command, the role will be placed in the correct folder structure.<br/>
Note! Ensure that the content of `requirements.yml` refers to the correct repositories.<br/>
<br/>

## Installation
No installation required.<br/>

## Configuration
(none).<br/>

## Other information
(none).<br/>

## License
MIT

## Author
Marcel Venema

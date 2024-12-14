# If you have n8n installed: Install custom nodes module

Install it to the n8n root folder. This is the node_modules folder on the same level of n8n and n8n-core. This differs when you used the -g flag on n8n initial installation. From there do:

```
npm install @digital-boss/n8n-nodes-suitecrm
```

# Fresh install n8n

Navigate to desired folder, create a package json and install n8n like so:

```
cd /var/www/vhosts/

mkdir my-n8n && cd my-n8n

npm init --yes

npm install n8n

npm install @digital-boss/n8n-nodes-suitecrm
```

# Start n8n

Directly:

```
n8n
```

Plesk or C-Panel:

```
node /var/www/vhosts/n8n/bin/n8n
```

# Ensure your SuiteCRM v8 has keys

Keys must be placed in /suitecrm-root/SuiteCRM-8.2.4/public/legacy/Api/V8/OAuth2/

```bash
cd /suitecrm-root/SuiteCRM-8.2.4/public/legacy/Api/V8/OAuth2/
openssl genrsa -out private.key 2048
openssl rsa -in private.key -pubout -out public.key
sudo chmod 600 private.key public.key
sudo chown www-data:www-data p*.key
```

# Latest functionality

Suite Crm n8n node includes REST API endpoints via "data" implementation.

# Contribution

To make this node even better, please let us know, [how you use it](mailto:info@digital-north-consulting.com). Commits are always welcome.

# Issues

If you have any issues, please [let us know on GitHub](https://github.com/quansenB/n8n-nodes-suitecrm/issues).

# About

Special thanks to [N8n nodemation](https://n8n.io) workflow automation by Jan Oberhauser.

Nodes by [digital-north-consulting.com](https://digital-north-consulting.com). For productive use and consulting on this, [contact us please](mailto:info@digital-north-consulting.com).

This node was programmed with :heart: by Iñaki Breinbauer [quansenB](https://github.com/quansenB)

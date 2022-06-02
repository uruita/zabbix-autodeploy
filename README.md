# Autodeploy do Zabbix Agent

Este módulo permite a autoconfiguração das máquinas que devem ser monitoradas pelo servidor Zabbix. A partir deste, o zabbix-agent é instalado, configurado de forma ativada e são adicionadas as regras de Firewall iptables.

## Pré-Install - Clientes

> Ter o python versão 2.7 ou superior instalado no cliente.

> Ter o usuário 'x', devidamente padronizado, no cliente e no grupo sudo.

> Ter firewall liberado para a vm 'que roda o playbook' na porta 22.

## Como usar

Os servidores que devem ser monitorados estão na presente no arquivo [inventory.an](). Portanto, para adicionar um novo servidor a ser monitorado, deve-se adicionar o nome do servidor ao final do arquivo, de forma que, ao ser feito o push no gitlab, o script irá checar se todos os servidores presentes neste arquivo estão configurados de forma correta. Caso não estejam, serão configurados.

e.g Pretende-se monitorar um novo servidor chamado foo.com a partir do servidor zabbix

A partir do [gitlab](), 
1. Edite o arquivo chamado [inventory.an](); 
2. Adicione ao final do grupo virtual_hosts o nome "foo", para versões 10, 9 e 8 do Debian;
3. Para instalar em uma porta específica como a 2222, utilize a variável 'ansible_ssh_port=2222' após "foo"
4. Salve as alterações.

# Mantenedor

Nome            | E-mail          | Lattes     | Linkedin
--------------- | --------------- | ---------- | ----------
Uruita          | xxxxx@gmail.com | [link]()   | [link]()


# Ansible Playbook para Configuração de Servidor Minecraft

Este repositório contém um playbook Ansible e roles associadas para configurar um servidor Minecraft em uma máquina Oracle Linux.

## Pré-requisitos

- Ansible instalado na máquina de controle.
- Conexão SSH configurada entre a máquina de controle e o servidor alvo.
- Java Development Kit (JDK) instalado no servidor alvo.

## Como usar

1. Clone este repositório para a máquina de controle:

    ```bash
    git clone https://github.com/alexandercsq/minecraft_server.git
    ```

2. Edite o arquivo `inventory.yml` e substitua `server1.example.com` pelo endereço IP ou nome de host do seu servidor Minecraft.

3. Execute o playbook principal `minecraft_server.yml`:

    ```bash
    ansible-playbook -i inventory.yml minecraft_server.yml
    ```

Isso configurará o servidor Minecraft na máquina remota com as configurações padrão.

## Estrutura do Projeto

- `minecraft_server.yml`: O playbook principal que chama as roles necessárias.
- `inventory.yml`: O arquivo de inventário contendo o(s) servidor(es) alvo.
- `roles/`:
  - `java/`: Role responsável por instalar o JDK.
  - `minecraft/`: Role responsável por instalar o Minecraft.
  - `firewall/`: Role para configurar o firewall.
  - `configure_minecraft/`: Role para configurar o servidor Minecraft.
  
## Contribuindo

Se encontrar algum problema ou tiver sugestões de melhorias, sinta-se à vontade para abrir uma issue ou enviar um pull request.


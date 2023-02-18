# Magento2 Ansible PlayBook

Este es un playbook de Ansible para Magento 2. Se utiliza para configurar un entorno de desarrollo rápido en un servidor.

Este playbook se probó en Ubuntu 20.04.

## Preinstalación

Para configurar el PPA en su máquina e instalar Ansible, ejecute estos comandos:

```
sudo apt-get update
sudo apt-get install software-properties-common
sudo apt-add-repository ppa:ansible/ansible
sudo apt-get update
sudo apt-get install ansible -y
```

## Instalación

Actualice los valores en:

* hosts
* group_vars/all.yml

Then after editing, run:

```
ansible-playbook -c local -i localhost,tienda playbook.yml
```

## Desarrollo

### Verificar sintaxis

Comprobar sintaxis básica del rol.

```
ansible-playbook -c local -i localhost,tienda playbook.yml --syntax-check
```

### Verificar Lint

Ejecutar herramienta de Lint para verificar las mejores prácticas.

```
ansible-lint
```

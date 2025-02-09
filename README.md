# Projeto Vagrant Ubuntu

## Descrição
Este projeto configura uma máquina virtual Ubuntu 20.04 utilizando Vagrant. A máquina virtual é provisionada com 1 GB de RAM e 1 núcleo de CPU, e possui uma pasta sincronizada para facilitar o compartilhamento de arquivos entre o host e a VM.

## Passos para Subir a VM
Siga os passos abaixo para iniciar a máquina virtual:

1. Certifique-se de ter o Vagrant e o VMware Desktop instalados no seu sistema.
2. Clone este repositório para o seu diretório local.
   ```sh
   git clone https://github.com/Eliezer-Nogueira/vagrant-ubuntu
   cd seu-repositorio
   ```
3. Inicie a máquina virtual com o comando:
   ```sh
   vagrant up
   ```

## Acessar a Máquina Virtual
Para acessar a máquina virtual via SSH, utilize o comando abaixo:
```sh
vagrant ssh
```

## Sincronização de Pastas
A pasta `root` no diretório local está sincronizada com a pasta `/home/vagrant/root` na máquina virtual. Isso permite que você compartilhe arquivos entre o host e a VM facilmente. Qualquer arquivo colocado na pasta local será acessível na VM, e vice-versa.

## Links
[Repositório no GitHub](https://github.com/Eliezer-Nogueira/vagrant-ubuntu)

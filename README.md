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

## Configuração para Usuários do VMware Workstation

Se você está utilizando o **VMware Workstation** como provedor no Vagrant, siga os passos abaixo para garantir que a máquina virtual funcione corretamente:

1. **Instalar o Plugin do Vagrant para VMware**:
   O Vagrant necessita de um plugin específico para funcionar com o VMware Workstation. Instale o plugin executando o seguinte comando no terminal:

   ```sh
   vagrant plugin install vagrant-vmware-desktop
   ```

2. **Alterar a Box no Vagrantfile**:
   O Vagrant precisa de uma box que seja compatível com o VMware. No seu `Vagrantfile`, substitua a configuração da box para usar uma box compatível, como `generic/ubuntu2004`:

     config.vm.box = "generic/ubuntu2004"  # Box para VMware Workstation

3. **Iniciar a Máquina Virtual**:
   Agora, execute o comando abaixo para subir a máquina virtual com o **VMware Workstation** como provedor:

   ```sh
   vagrant up --provider=vmware_desktop
   ```

Após esses ajustes, você pode acessar a máquina virtual da mesma maneira utilizando o comando ```vagrant ssh```.

Se encontrar algum erro, verifique se o VMware Workstation está instalado corretamente, e que o plugin [vagrant-vmware-desktop](https://developer.hashicorp.com/vagrant/install/vmware) está funcionando corretamente.


## Links
[Repositório no GitHub](https://github.com/Eliezer-Nogueira/vagrant-ubuntu)

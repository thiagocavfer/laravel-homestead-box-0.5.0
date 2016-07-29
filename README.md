##  Laravel-Homestead-box-0.5.0
Configuração e instalação de Laravel Homestead adicionando a box **"virtualbox.box"** manualmente.

> *Este tutorial é direcionado à pessoas que tenham problemas de link com o servidor **Atlas**, onde residem as boxes utilizadas pelo Laravel/Homestead.*

**OBS**: Subentende-se que o usuário, ao executar esse tutorial já esteja com o **VAGRANT** e **VIRTUALBOX** instalados e funcionando em sua máquina.

#### 1º Passo
Baixe a box **"0.5.0.virtualbox.box"** através deste link: https://drive.google.com/open?id=0B0bskwK6X6GnQlRyX0ZGTkRCT2M

#### 2º Passo
Coloque a box dentro do diretório "Homestead", o mesmo que você clonou a partir das recomendações do site **Laravel Homestead** (https://laravel.com/docs/5.2/homestead)

#### 3º Passo
Copie o arquivo **metadata.json** também para o diretório **"Homestead"**.

#### 4º Passo
Usando um terminal, digite o comando:
```
vagrant box add metadata.json
```
Verifique a versão da box adicionada com o comando `vagrant box list`. O retorno deverá ser o descrito abaixo:
```
laravel/homestead (virtualbox, 0.5.0)
```

#### 5º Passo (Só se o seu S.O. for Linux)
Pode ser que haja problemas de permissão ao diretório **"~Homestead/.vagrant/machines/default/virtualbox"**. Caso isso ocorra, coloque o seu usuário e grupo como donos do diretório:
```
sudo chown *seu-usuario*:*seu-grupo* -R /home/*seu-usuario*/Homestead/.vagrant/machines/default/virtualbox/
```

#### 6º Passo
Inicie sua VM Homestead e seja feliz.
```
vagrant up
```








zsh és Powerline
===
`1.`)   Forrás és magyarázat:
>
>ZSH_használata_LINUX-2018-5_SajatJegyzet.pdf  
>
`2.`)   Szükséges programok:  
`2.1.`) git  
`2.2.`) zsh  
`2.3.`) zsh-syntax-highlighting  
`2.4.`) Oh My ZSH  
`2.5.`) powerline   
`2.6.`) fonts-powerline  
`2.7.`) psutils  
`2.8.`) ruby-albino  
`2.9.`) neofetch  

`3.`)   Telepítés:  

`3.1.`) Programok telepítése:
```
sudo apt install git zsh zsh-syntax-highlighting powerline fonts-powerline psutils ruby-albino neofetch
```  

`3.2.`) Oh-My-ZSH telepítése:

```
sudo sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
```
`3.3.`)    Konfig fájlok letöltése:
```
git clone https://github.com/psalan/linux-basics-zsh-config.git Letöltések/linux-basics-zsh-config
```
vagy
```
wget -cO Letöltések/linux-basics-zsh-config.zip https://github.com/psalan/linux-basics-zsh-config/archive/master.zip

unzip Letöltések/linux-basics-zsh-config.zip -d Letöltések/

mv Letöltések/linux-basics-zsh-config-master/ Letöltések/linux-basics-zsh-config
```
`3.4.`) A konfig fájlok másolása:  
`3.4.1.`)   Powerline shell beállító Json fájlok másolása
```
cp -vr Letöltések/linux-basics-zsh-config/powerline .config
```
`3.4.2.`)   Backup készítés:  
```
cat .zshrc > .zshrc_old
```
`3.4.3.`)   ZSH konfig fájl másolása:
```
cp Letöltések/linux-basics-zsh-config/.zshrc .zshrc
```
`3.4.4.`)   Automatikus ajánlatok plugin letöltése:
```
sudo git clone https://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions
```
`3.4.5.`)   Kiegészítések plugin letöltése:
```
sudo git clone https://github.com/zsh-users/zsh-completions $ZSH_CUSTOM/plugins/zsh-completions
```
`3.5.`) ZSH az alapértelmezett parancsértelmező:
```
chsh -s $(which zsh)
```
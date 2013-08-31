所為何來
=
於 Ubuntu 上安裝 Git 版本管理系統，並方便使用 Git 之資源。


使用環境
=
Ubuntu 12.04 Server  
Git 1.8.3.4


推薦安裝方式
=
於終端機中，先輸入以下指令，以安裝 Git 所需的相關套件：
```bash
sudo aptitude install libcurl4-gnutls-dev libexpat1-dev gettext libz-dev libssl-dev build-essential
```
接著，輸入以下指令，以將 Git 下載並安裝：  
(Git 的版本可至 [Git 官網](https://code.google.com/p/git-core/downloads/list) 查看與選擇，本文以 1.8.3.4 做為示範)
```bash
wget https://git-core.googlecode.com/files/git-1.8.4.tar.gz && 
tar -zxf git-1.8.4.tar.gz && mv git-1.8.4 git && cd git && 
make prefix=/usr/local all && sudo make prefix=/usr/local install && 
cd && rm -rf git git-1.8.4.tar.gz
```
最後，請設定帳號名稱及 Email：  
(本文以 git.user 做為帳號、git＠email.com 做為 Email)
```git
git config --global user.name "git.user" && 
git config --global user.email git@email.com
```
欲修改時，請再次輸入以上帳號或 Email 之指令，即可覆蓋原設定。  

DONE.
<br>
<br>

補充說明
=
日後需更新 Git 時，可使用 Git 的指令來進行：
```bash
git clone git://git.kernel.org/pub/scm/git/git.git && 
cd git && make prefix=/usr/local all && sudo make prefix=/usr/local install &&
cd && rm -rf git
```
欲查看帳號及 Email 設定時，可輸入：
```git
git config --list
```
若要直接編輯的話，可使用：
```bash
sudo nano ~/.gitconfig
```

參考資源
=
* [Git](http://git-scm.com/download/linux)
* [How to Install Git on Ubuntu 12.04 | DigitalOcean](https://www.digitalocean.com/community/articles/how-to-install-git-on-ubuntu-12-04)
* [Git - Community Ubuntu Documentation](https://help.ubuntu.com/community/Git)
* [Downloads - git-core - Git - the stupid content tracker - Google Project Hosting](https://code.google.com/p/git-core/downloads/list)

所為何來
=
於 Ubuntu 上安裝 Git 命令列工具，以便使用 git 指令來下載套件，或運作分散式的版本管理系統。


使用環境
=
Ubuntu 12.04 Server  
Git 1.7.9.5


推薦安裝方式
=
於終端機中，輸入以下指令來安裝 Git：
```bash
sudo aptitude install git-core &&
```
接著，請使用更新 Git 來更新自己：
```bash
git clone https://github.com/git/git && 
cd git
make prefix=/usr/local all && 
sudo make prefix=/usr/local install

```
DONE.
<br>
<br>

補充說明
=
* 未選擇從 Git 網站下載最新版本，而使用 aptitude 來安裝的原因在，能把 Git 所需的相關套件一併安裝 (如：libcurl4-gnutls-dev libexpat1-dev gettext libz-dev libssl-dev build-essential... 等)。
* 更新時，需使用 Make 及 cURL 工具，請先行安裝：<code>sudo aptitude install make</code> 

參考資源
=
* [Git](http://git-scm.com/download/linux)
* [How to Install Git on Ubuntu 12.04 | DigitalOcean](https://www.digitalocean.com/community/articles/how-to-install-git-on-ubuntu-12-04)
* [Git - Community Ubuntu Documentation](https://help.ubuntu.com/community/Git)
* [Downloads - git-core - Git - the stupid content tracker - Google Project Hosting](https://code.google.com/p/git-core/downloads/list)

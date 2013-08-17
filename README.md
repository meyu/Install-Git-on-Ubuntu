所為何來
=
於 Ubuntu 上安裝 Git 命令列工具，以便使用 git 指令來下載套件，或運作分散式的版本管理系統。


使用環境
=
Ubuntu 12.04 Server  
Drush 5.9


推薦安裝方式
=
於終端機中，輸入以下指令來安裝並更新 Git：
```bash
sudo aptitude install git-core &&
git clone git://git.kernel.org/pub/scm/git/git.git
```
DONE.
<br>
<br>

補充說明
=
* Ubuntu 12.04 預設是安裝 Drush 4.5，但官方建議使用 5.6 以上的版本，故請務必進行更新。
* 欲查詢所安裝的 Drush 版本，可使用：<code>drush --version</code>

參考資源
=
* [Drush | drupal.org](https://drupal.org/project/drush)
* [Drush.org](http://www.drush.org/)
* [Installing/Upgrading Drush on Ubuntu | drupal.org](https://drupal.org/node/1248790)

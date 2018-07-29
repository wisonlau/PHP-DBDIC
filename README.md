# PHP-DBDIC
PHP脚本生成MySQL的数据字典

## 用法

```
include('./DBdic.php');

//浏览器显示
DBdic::ini('localhost', 'db_name', 'username', 'password')->outForBrowser();

//浏览器显示, 带左侧菜单
DBdic::ini('localhost', 'db_name', 'username', 'password')->outForBrowserWithMenu();

//下载word文档
DBdic::ini('localhost', 'db_name', 'username', 'password')->outForWord();

//只导出一个表
DBdic::ini('localhost', 'db_name', 'username', 'password')->setExportTable('user')->outForBrowser();

//导出部分表, 支持正则
DBdic::ini('localhost', 'db_name', 'username', 'password')->setExportTableArray(['user', 'goods_.*', 'product_\d{4}'])->outForBrowser();

```

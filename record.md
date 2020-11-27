# linux 
-  find / -name  "*default*.log"
-  grep 
	1> grep -r searchName dir/  查出所有符合的字符串包含searchName的行信息
	2> grep -rw searchWord dir/ 查出所有字符串中 等于(而不是包含)searchWord的行信息
-  2>&1 & 
-  vim全选，全部复制，全部删除
	全选（高亮显示）：按esc后，然后ggvG或者ggVG
	全部复制：按esc后，然后ggyG
	全部删除：按esc后，然后dG
	跳转到第一行: gg
	跳转到最后一行: shift+g
- wget downurl 安装软件
# git  
-  删除远端分支   git push origin --delete originBranch
-  删除本地分支   git branch -d Branch
-  fetch的含义
 

# php
- usort(a, fucntion(a,b){
	return 1 #交换a b 
	return -1#不交换 a b
})
- is_numm和empty的区别
- arr = array_flip(array);
- 字符串替换str_replace strtr


# mysql
- 分区、分表(水平分割、垂直分割)



# laravel
- 生成model并且生成迁移文件
 php artisan make:model Models/Tags -m

- belongsToMany(Blogs::class, 'blog_tags', 'tag_id', 'blog_id') 
参数1 ： 关联表名称    
参数2 ： 中间表名称  
参数3 ： 中间表中关联的当前表id名称
参数4 ： 中间表中关联的关联表id名称 

- 引入前端第三方库 并合并到app.min.js或者app.min.css
	1. npm官网找到需要下载包名
    2. 对应项目下用npm下载对应包npm install xxx.js
    3. 然后在resoureces/js/app.js require包含上在node_modules对应路径下下载的包中的js文件
	4. 合并压缩js

- 生成迁移文件
    1. php artisan make:migration create_table_note
	2. php artisan migrate:status 
	3. php artisan migrate

- elquent 判断是否为空   ->isEmpty()
- 重置迁移文件  php artisan migrate:refresh (会将已有表和数据全删)

# mysql
- 备份 && 恢复
  - 备份
	1. cd /var/lib/mysql
	2. mysqldump -uroot -p 数据库名称 > /var/www/mysql_backup/自定义名称.sql
	3. 验证：备份完成可以vim查看 /var/www/mysql_backup/自定义名称.sql的内容  是否和数据相一致
  - 恢复
	1. 连接mysql create  database 数据库名称
	2. ctrl+z
    3. cd /var/www/mysql_backup/
	4. mysql -uroot  -p  前面新建的数据库的名字  <  自定义名称.sql
	5. 验证：进入mysql，  use刚才创建的数据库中， show tables； 查看表是否生成  并检查数据

- binlog 开启 
	- log_bin                        = /var/log/mysql/mysql-bin.log
	- server-id=1234




----------------------------------------------------------------------------------------------------------------
													公司业务
----------------------------------------------------------------------------------------------------------------
-  中间层可执行文件更新到开发环境：
执行目录：……go/src/bszhihui.com/v2_hcloud
rsync -av --chown=root:root eduinterface/bin/eduMysqlServer root@192.168.0.32:/data/service_hcloud/eduMysql

ssh root@192.168.0.32 /data/service_hcloud/eduMysql/start.sh restart


-  在sim服务器查线上log

目录 /srv

搜索脚本grepLog.sh，后面跟着查找内容、查找路径。

示例：./grepLog.sh getPaveMainById.*61.66 /data/web/hcloud//web/log/interface/20200902.log
-  重启nginx   sudo /usr/local/openresty/nginx/sbin/nginx -s reload

-  sit - solr  ---- 1> mstsc 
				   2> 121.36.46.191




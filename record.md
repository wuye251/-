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

# git  
-  删除远端分支   git push origin --delete originBranch
-  删除本地分支   git branch -d Branch

# php
- usort(a, fucntion(a,b){
	return 1 #交换a b 
	return -1#不交换 a b
})















----------------------------------------------------------------------------------------------------------------
													公司业务
----------------------------------------------------------------------------------------------------------------
-  中间层可执行文件更新到开发环境：
执行目录：……go/src/bszhihui.com/v2_hcloud
rsync -av --chown=root:root eduinterface/bin/eduMysqlServer root@192.168.0.32:/data/service_hcloud/eduMysql

ssh root@192.168.0.32 /data/service_hcloud/eduMysql/start.sh restart


2.在sim服务器查线上log

目录 /srv

搜索脚本grepLog.sh，后面跟着查找内容、查找路径。

示例：./grepLog.sh getPaveMainById.*61.66 /data/web/hcloud//web/log/interface/20200902.log


3. 重启nginx   sudo /usr/local/openresty/nginx/sbin/nginx -s reload

4.sit - solr  ---- 1> mstsc 
				   2> 121.36.46.191





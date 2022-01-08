gal-theme问题
	1.新本版node的npm版本太高，sass不能支持，最高只能使用版本7的npm。可以下载v16.10的node。
		版本太高可以尝试一下命令回退
			npm install npm@7.20.0 -g
			
	2.国内网络会导致下载各种依赖出问题通过一下命令修改源
	    下载国外的资源众所周知的慢，常用设置镜像，平时多用yarn
		yarn全局安装及设置镜像
			npm install -g yarn
			yarn config set registry http://registry.npm.taobao.org/ -g
			yarn config set sass_binary_site http://cdn.npm.taobao.org/dist/node-sass -g
			npm config set registry https://registry.npm.taobao.org
			npm config get registry // 查看是否配置成功
			npm config list  // 查看npm当前配置
			npm cache clear --force // 强制清除缓存
        然后再安装gal-theme的依赖
			yarn add hexo-renderer-sass
			yarn add hexo-renderer-scss
			cnpm install hexo-generator-json-content --save
		如果 hexo g 后 sass 还是报错可以改用 cnpm 安装
		    cnpm install node-sass
			
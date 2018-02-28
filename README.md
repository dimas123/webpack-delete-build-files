# 1.插件说明
	1.删除webpack预打包时产生的带有hash值的js文件
	2.带有文件排除功能
# 2.使用说明
	2.1:安装插件
		npm install webpack-delete-build-files --save-dev
	2.2:配置方法(修改webpack.conf.js)
		const removeFiles = require('webpack-delete-build-files');
		const perBuildDir = './static/js/';//要删除的文件目录(根据实际情况配置)
		const excludeFiles = ['html2canvas.js','jsPdf.debug.min.js'];//要排除的文件 避免误删
		......
		new removeFiles(perBuildDir,excludeFiles)

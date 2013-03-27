技术要求:
	前期前台样式可以不修边幅，但该有的内容必须都要显示出来
	采用Smarty作为模板引擎（前台+后台）
	后台编辑器

前期功能：
	栏目的增删改查
		无限级分类
		栏目模板设置
	文章的增删改查
		文章可上传附件/图片
		文章分类
		静态页面生成
		回收站功能
	管理员的增删改查
		权限管理
		日志功能
	用户的增删改查
		用户注册模块
		用户密码修改
	系统设置
		站点SEO信息
		模板设置
		全局模板（用于添加站点统计脚本）
		全局模板变量
		SQL语句执行
		数据库备份/恢复

编码规范:
	参考Discuz的编码规范http://dev.discuz.org/wiki/index.php?title=%E7%BC%96%E7%A0%81%E8%A7%84%E8%8C%83
	几个特别注意的事项
	文件编码统一为UTF-8
	书写代码缩进必须明确，层次必须分明，用tab键缩进，不得使用空格方式缩进
	编码风格统一为:
		php:
			php文件声明
				<?php
				/*your code*/
				?>
			函数声明
				function test($user,$key='tester'){
					/*有默认值的参数需要放到参数后部*/
				}
		
		css:
			body{
				margin:0;
				padding:0;
			}
			
		html:
			<html>
				<head>
					<title>HTML文件声明</title>
					<body>
						<div id="test">
							id、class等属性必须使用双引号标注
						</div>
					</body>
				</head>
			</html>
		
		Javascript:
			function test(){
				/*每句后面都要使用分号分开*/
				/*变量的声明必须使用var*/
				var tester="Hello World";
				alert(tester);
			}
	
	
	不得出现<?php =$var; ?>类似的不规范的编码
	数据库操作使用MySQLi方式
	SQL语句规范字符串必须使用单引号标注起来
	代码如果觉得代码不够简单，比较不易理解，请加以注释
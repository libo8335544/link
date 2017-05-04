

# links
这是一个可以进行模板选择的自动化工具

# 安装依赖
```
npm install links -g
```
或者
```
git clone https://github.com/libo8335544/link.git

cd link && npm install

npm link
```

# 使用
```
  Usage: links <command>


  Commands:

    add|a      Add a new template
    list|l     List all the templates
    init|i     Generate a new project
    delete|d   Delete a template

  Options:

    -h, --help     output usage information
    -V, --version  output the version number
```

# 命令大全
### add | a
添加一个新的模板 成功后添加到本地的`templates.json`
```
$ links add 
```
```
 /*  Template name：模板名称 */
Template name: my-tpl

 /*https link： git https 链接*/
Git https link:  https://xxx.git 

 /* Branch:模板的分支 */
Branch: master 
```
添加模板成功后，您将看到:
```
The last template list is:

{ tpl:
   { 'my-tpl-name':
      { url: 'https://xxx.git',
        branch: 'master' } } }
```

### list | l
查看模板列表.
```
$ link list

{ tpl:
   { 'my-tpl-name':
      { url: 'https://xxxx.git',
        branch: 'master' } } }
```

### init | i
初始化 link配置 ，可以根据选择项配置出项目模板列表中的项目
```
$ links init|i

/* Template name：输入一个模板名称 */
Template name: my-tpl-name

/* Project name：输入本地的要创建的项目名称 */
Project name: my-new-project
```
创建成功后您将看到一下：
```
Start generating...

 √ Generation completed!

 cd my-new-project && npm install
```
It's easy, right?

### delete | d
删除模板:
```
$ links delete
```
Template name：输入要删除的模板名称
```
Template name: my-tpl-name
```
删除成功后您将看到:
```
Template deleted!
The last template list is:

{ tpl:
   { 'my-tpl-name': undefined } }
```















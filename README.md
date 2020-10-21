# development-norms

仓库创建 REMEAD 模板按照以下仓库信息进行规范

### 仓库信息

仓库名：development-norms（单词小写，单词间用横线隔开）

项目名：校易班学生工作站技术部开发规范

创建人：林洁彬

创建时间：2020-10-18

参与人：
- 林洁彬
- 喻嘉兴

### 命名类型

大驼峰命名法：所有单词首字母大写，如`MyFirstClass`

小驼峰命名法：第一个单词之外，其他单词首字母大写，如`myName`,`getMyFirstName`

下划线命名法：用单词和下划线组合命名，如`user_name`

脊柱命名法：单词小写命名，多个单词用`-`符号隔开

### 文件命名

普通文件和文件夹命名一律采用小写，用完整的单词描述文件，多个单词用下划线分开。

代码文件划分根据不同类型使用不同符号：

- SQL 文件：使用`_`下划线分开
- HTML 文件：使用`_`下划线分开
- 样式文件：使用`-`横线分开
- JavaScript 文件：使用`-`横线分开单词和数字版本，用`.`来分开标识版本
- Java 文件：使用小驼峰命名法
- Python 文件：使用`_`下划线分开
- Go 文件：使用`_`下划线分开

```Text
project_dir
    - README.md
    - data_file.sql
    - descript.word
    - code_files
        - html_file.html
        - style-file.css
        - filename-1.2.10.js
        - filename.min.js
        - javaFile.java
        - python_file.python
        - go_file.python
```

### HTML 与样式

class 和 id 命名：采用脊柱命名法，如下

```HTML
<div class="wrap" id="user">
    <div class="user-id"> 用户ID </div>
    <div class="user-name"> 用户姓名 </div>
</div>
```

样式文件变量命名（css/sass/less/stylus...）: 与 class/id 的命名一样，如下在 Stylus 中

```Stylus
font-default-color = #666

.wrap
    color font-default-color
```

### JavaScript

类命名：使用大驼峰命名法，如`JavaScriptClass`

函数命名：使用小驼峰命名法，如`myFunction`

变量命名：使用下划线命名法，如`user_name`

### Java

包名：使用大写开头的功能概括单词或全部大写的单词缩写进行命名

类命名：使用大驼峰命名法

函数 / 变量命名：使用小驼峰命名法

```Java
package com.csxyyiban.data_objects;
// or
package com.csxyyiban.DO;

class NewUser{
    private int userId = 001;
    private String userName = "name";

    public getUserId(){
        return this.userId;
    }

    public changeUserName(String name){
        this.userName = name;
    }
}
```

### Python

类名：使用大驼峰命名法，如`PythonClass`

功能函数 / 变量命名：使用下划线命名法

```Python
class UserClass:
    user_id = 000
    user_name = "name"

    def get_user_id(self):
        id = self.user_id
        return id
```

### 易班相关变量命名

采用易班开放平台接口文档中相关字段的命名，其它额外的命名采用`yb`作为前缀，如下所示：

在 Java 中

```Java
int ybId = 000001;

String ybName = "name";

String ybOtherName = "other name";
```

在 Python 中

``` Python

yb_id = 000001

yb_other_name = "other name"
```

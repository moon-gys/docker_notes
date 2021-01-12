## 程序常用的配置文件格式

通过从配置文件中读取信息，可以进程程序初始化和改变运行时的状态。

<https://dablelv.blog.csdn.net/article/details/102626144?utm_medium=distribute.pc_relevant.none-task-blog-BlogCommendFromBaidu-3.control&depth_1-utm_source=distribute.pc_relevant.none-task-blog-BlogCommendFromBaidu-3.control>

1. 键值对
2. JSON
  - 语法、实例、解析
3. XML
  - 语法、实例、解析
4. YAML
5. TOML
6. 配置文件格式的选择

### 键值对

#### 1. 语法：

- 每个键值对表示一项配置，键值对的分隔符一般使用等号或冒号。
- 解析时，#开头视为注释

以键值对为表现形式的配置文件常用的格式： window下的.ini和java中的.properties

#### 2. 实例

  ```
    # This is a comment
    name=UserProfileServer
    maxconns=1000
    queuecap=10000
    queuetimeout=300
    loglevel=ERROR
    logsize=10M
    lognum=10
    logpath=/usr/local/app/log
  ```
  
### JSON
  
(javascript object notation) 轻量级的文本数据交换格式，独立于语言，具有自我描述性。但是比XML更小、更快、更易解析。

#### 1.语法
 
JavaScript对象表示语法的子集
- 数据在名称/值对中
- 数据由逗号分隔
- 花括号保存对象
- 方括号保存数组

#### 2.实例

  ```
    {
      "employees": [
        { "firstName":"John" , "lastName":"Doe" },
        { "firstName":"Anna" , "lastName":"Smith" },
        { "firstName":"Peter" , "lastName":"Jones" }
      ]
    }
  ```

### XML

Extensible Markup Language 是可扩展标记语言，用来传输和存储数据，因为其允许用户自定义标记名称，具有自我描述性，可以灵活地用于存储服务配置信息。

#### 1.语法
 
XML语法是一种树结构，从根部开始，然后扩展到枝叶。XML文档必须有一个唯一的根节点，根节点包含所有其他结点。所有结点均可拥有文本内容和属性（名称/值的对）。XML结点也叫做XML元素。

编写XML文档时，需要注意：
1. 所有的XML元素都有关闭标签
2. XML标签对大小写敏感
3. XML属性值需加引号
4. 5个预定义的实体引用
  - &lt <
  - &gt >
  - &amp &
  - &apos '
  - &quot "

#### 2.实例

  ```
    <?xml version="1.0" encoding="UTF-8"?>
    <server name="UserProfileServer">
      <maxconns>1000</maxconns>
      <queuecap>10000</queuecap>
      <queuetimeout>300</queuetimeout>
      <loginfo>
        <loglevel>ERROR</loglevel>
        <logsize>10M</logsize>
        <lognum>10</lognum>
        <logpath>/usr/local/app/log</logpath>
      </loginfo>
    </server>
  ```





 



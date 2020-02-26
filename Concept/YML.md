# YML

Created: Feb 25, 2020 12:10 PM

### 一、YML是什么

YAML (YAML Aint Markup Language)是一种标记语言，通常以.yml为后缀的文件，是一种直观的能够被电脑识别的数据序列化格式，并且容易被人类阅读，容易和脚本语言交互的，可以被支持YAML库的不同的编程语言程序导入，一种专门用来写配置文件的语言。可用于如： Java，C/C++, Ruby, Python, Perl, C#, PHP等。

### 二、YML的优点

1. YAML易于人们阅读。
2. YAML数据在编程语言之间是可移植的。
3. YAML匹配敏捷语言的本机数据结构。
4. YAML具有一致的模型来支持通用工具。
5. YAML支持单程处理。
6. YAML具有表现力和可扩展性。
7. YAML易于实现和使用。

作者：张家界的雪链接：https://www.jianshu.com/p/cea930923f3d来源：简书著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。

# 编写规则

- **大小写敏感**

json 里也是大小写敏感的，这点二者一样。

- **使用缩进表示层级关系**

json 中使用 `{}` 的嵌套表示层级，而 yaml 使用缩进，后者更方便一些。

- **`#` 表示注释**

json 文件中不允许写注释，对于很长配置文件全靠字面意思猜挺痛快的，yaml 可以写注释，:100:

# 数据结构

配置文件理应十分简洁，与 json 相比，不用频繁的写 `{}` 和 `[]`，毕竟换行和 `-` 符号更加简洁，字符串也不需要频繁的加引号（无论是单引号还是双引号）。

## 对象

`# conf.yml
animal: pets
hash: { name: Steve, foo: bar }`

转换为 json 为：

`{ { "animal": "pets" }, { "hash": { "name": "Steve", "foo": "bar" } }
}`

## 数组

`# conf.yml
Animal: - Cat - Dog - Goldfish`

转换为 json 为：

`{ "Animal": [ "Cat", "Dog", "Goldfish" ] }`

## 字符串

`# conf.yml
# 正常情况下字符串不用写引号
str: 这是一行字符串
# 字符串内有空格或者特殊字符时需要加引号
str: '内容： 字符串'`

## null

`# conf.yml
parent: ~`

.yml 中 ~ 表示 null，转换为 json 为：

`{ "parent": null }`

作者：dkvirus链接：https://www.jianshu.com/p/a8252bf2a63d来源：简书著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。
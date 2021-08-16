# JS对象
## 对象object
### 定义：
* 无序的数组集合
* 键值对的集合
* 写法
````
    let obj = { 'name':'frank','age':18 }
    let obj = new Object({'name':'frank'})
    console.log({'name':'frank', 'age':18})
````
* 细节
1. 键名是字符串，不是标识符，可以包含任意字符。
2. 引号可省略，省略之后就只能写标识符。
3. 就算引号省略了，键名也还是字符串（重要）

## 属性名
* 每个key都有对象的属性名（property）
## 属性值
* 每个value都是对象的属性值

## 对象的隐藏属性
* JS中每个对象都有一个隐藏属性。
* 这个隐藏属性存储着其共有属性组成的对象的地址。
* 这个共有属性组成的对象叫做原型。
* 也就是说，隐藏属性存储着原型的地址。

# 增删改查
## 删除属性
````
    delete obj.xxx或者delete obj['xxx']
````

## 查看所有属性（读属性）
* 查看自身所有属性
````
    Object.keys(obj)
````
* 查看自身+共有属性
````
    console.dir(obj)
````
* 判断一个属性是自身的还是共有的
````
    obj.hasOwnProperty('toString')
````

## 原型
* 每个对象都有原型
1. 原型里存着对象的共有属性
2. 比如obj的原型就是一个对象
3. obj.__proto__存着这个对象的地址
4. 这个对象里有toString/constructor/valueOf等属性
* 对象的原型也是对象
1. 所有对象的原型也是对象
2. obj={}的原型即为所有对象的原型
3. 这个原型包含所有对象的共有属性，是对象的根
4. 这个原型也有原型，是null
## 查看属性
* 两种方法
1. 中括号语法：obj['key']
2. 点语法：obj.key
#### 优先使用中括号语法

## 修改或增加属性
* 直接赋值
````
    let obj = {name:'frank'}//name是字符串
    obj.name ='frank' //name是字符串
    obj['name'] = 'frank'
````
* 批量复制
````
    Object.assign(obj,{age: 18,gender: 'man'})
````
## 'name' in obj和obj.hasOwnProperty('name') 的区别
* 都是两种查看属性是不是在对象里的方法
前者自身属性和共有属性都返回true，后者仅仅是自身属性才返回true









































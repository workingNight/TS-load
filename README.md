## TS-load
学习ts，准备nest.js开发后台做准备

### 优秀学习资料
[入门教程](https://github.com/xcatliu/typescript-tutorial/blob/master/README.md)
[掘金-一篇朴实的文章带你入门](https://juejin.im/post/5d53a8895188257fad671cbc)
[掘金-ts安利指北](https://juejin.im/post/5d8efeace51d45782b0c1bd6)


### ts浅看
清晰的函数参数/接口属性，增加了代码可读性和可维护性
静态检查
代码提示
是什么类型就要赋值给什么类型 :   
let isDone: boolean = false;  
让函数接收参数和输出的类型有一个稳定的把控，

### 基本知识点
1. 几大类型
    boolean、number、string、null、undefined 
2. 联合类型
    表示取值可以为多种类型的一种 string | number
3. 断言<>
    <string>something 把这个数据断言成stirng类型，--即表示你认同这个数据是这个类型
4. type 创建类型别名常用于联合类型
    type NameOrResolver = Name | NameResolver
5. 枚举
    把取值限定在一定范围内，enum Days {Sun, Mon, Tue, Wed, Thu, Fri, Sat}
6. 泛型<T>
解决类型判断冗余，比如一个方法可能会被种类型调用，没有必要重复调用，用泛型可以让其根据具体的调用类型来决定
```
function getData<T>(value:T):T{
  return value;
}
getData<number>(123);       //调用时指定number类型
getData<string>('1214231'); //调用时指定string类型
```

### 大杂烩
1. 外部声明 declare 外部引入一些文件的时候要进行声明    
常用做法： 把声明写在.d.ts文件里  再在需要的时候通过///<reference path...>引
2. 函数类型  method: (p1: type, p2: type) => type      此箭头非箭头函数，而是声明这个函数的输出类型
3. 命名空间 namespace ns { exprot let a:number = 1 }
4. 类型查询语法
```
let a: number
let b: typeof a    //也就等同于a的类型
```
5. 元组类型[T0 , T1, T2]
6. 泛型<T>   泛型约束<T as ...>
7. null undefined所有类型的子类
8. 类型断言 as
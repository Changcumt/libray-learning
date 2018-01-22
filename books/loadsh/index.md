**lodash** 是现在javascript开发中最常使用的一个库之一，其封装的函数方法极大的便利了js开发效率。先就列出其常用的方法，并用简单代码说明其实现原理。

- Array
  - chunk(array,size)  根据size 把array分块
  - compact(array) 把数组中的可以转为false的值过滤出去，如null,'',false,NaN,0,undefined等
  - concat(array,values) 封装的原生的concat
  - difference(array,[values]) 返回与第一个数组不同的项组成的数组
  - differenceBy(array, [values], [iteratee=_.identity]) iteratee可以是一个方法或者属性，根据对比改方法或者属性的结果，返回与第一个数组不同项组成的数组。
  - differenceWith(array, [values], [comparator])comparator是一个比较方法，根据返回true或者false来判断元素是否一致，将与第一个数组不同的项组成数组返回
  - drop(array,[n=1]) 从开始数移除n个元素后并 返回新数组
  - dropRight(array,[n=1]) 从结尾开始移除n个元素后返回新数组
  - dropRightWhile(array, [predicate=_.identity]) 传入一个断言，从结尾开始直到匹配不成功，则返回剩下的数组
  - dropWhile(array, [predicate=_.identity]) 传入一个断言，从起始位置直到匹配不成功，返回剩下的元素组成的数组。断言可以是一个函数 可以是一个对象(lodash.matches),一个数组(lodash.matchesProperty),或者是一个字符串(lodash.property),根据返回的结果转化的boolean来判断是否应该drop


其他的陆续整理中。。。

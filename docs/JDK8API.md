# JDK 8 API

## [Collection 接口](jdk8/conllection.md)

>   `Collection` 是 `java.util` 包下的的一个接口类，所有实现了该接口的类都将具有它的方法与属性。目前官方实现的有：`Set`，`List`，`Map`等。开发人员可以根据需求自定义几个类并实现它。
  
``` java 
    /**
     *    The root interface in the <i>collection hierarchy</i>.  A collection
     * represents a group of objects, known as its <i>elements</i>.  Some
     * collections allow duplicate elements and others do not.  Some are ordered
     * and others unordered.  The JDK does not provide any <i>direct</i>
     * implementations of this interface: it provides implementations of more
     * specific subinterfaces like <tt>Set</tt> and <tt>List</tt>.  This interface
     * is typically used to pass collections around and manipulate them where
     * maximum generality is desired.
     */
 
 ```
   [`Collection`的重要方法](jdk8/conllection.md) 


## [Objects 类](jdk8/objects.md)

>	`Objects` 是一个工具类，由一些有用的操作对象的方法组成，这些方法通常都是很有用的。例如判断 `user` 对象是否为空，`Objects.isNull(user)`等方法。 

``` java
	/**
	 * This class consists of {@code static} utility methods for operating
	 * on objects.  These utilities include {@code null}-safe or {@code
	 * null}-tolerant methods for computing the hash code of an object,
	 * returning a string for an object, and comparing two objects.
	 *
	 * @since 1.7
	 */

```
[`Objects`的重要方法](jdk8/objects.md) 
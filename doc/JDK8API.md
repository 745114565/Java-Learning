# JDK 8 API

## Collection

>   `Collection` 是 `java.util` 包下的的一个接口类，所有实现了该接口的类都将具有它的方法与属性。目前官方实现的有：`Set`，`List`，`Map`等。开发人员可以根据需求自定义几个类并实现它。

>   `Collection` 的重要方法如下：

>>   
``` java 
   int size()
```

``` java 
   boolean isEmpty()
``` 

``` java 
   boolean contains(Object o)
``` 
>>    _Returns <tt>true</tt> if this collection contains the specified element._
      

>>    `Iterator<E> iterator()` :   Returns an iterator over the elements in this collection.

>>    `Object[] toArray()` : Returns an array containing all of the elements in this collection.

>>    `<T> T[] toArray(T[] a)` : Returns an array containing all of the elements in this collection; the runtime type of the returned array is that of the specified array.

>>    `boolean add(E e)` : Ensures that this collection contains the specified element (optional operation).  Returns <tt>true</tt> if this collection changed as a result of the call.  (Returns <tt>false</tt> if this collection does not permit duplicates and already contains the specified element.)<p>

>>    `boolean remove(Object o)` : Removes a single instance of the specified element from this collection, if it is present (optional operation).

>>    `boolean containsAll(Collection<?> c)` : Returns <tt>true</tt> if this collection contains all of the elements in the specified collection.

>>    `boolean addAll(Collection<? extends E> c)` : Adds all of the elements in the specified collection to this collection (optional operation).

>>    `boolean removeAll(Collection<?> c)` : Removes all of this collection's elements that are also contained in the specified collection (optional operation).  After this call returns, this collection will contain no elements in common with the specified collection.

>>    `default boolean removeIf`: Removes all of the elements of this collection that satisfy the given predicate.  Errors or runtime exceptions thrown during iteration or by the predicate are relayed to the caller.
``` java
    default boolean removeIf(Predicate<? super E> filter) {
        Objects.requireNonNull(filter);
        boolean removed = false;
        final Iterator<E> each = iterator();
        while (each.hasNext()) {
            if (filter.test(each.next())) {
                each.remove();
                removed = true;
            }
        }
        return removed;
    }
``` 

>>    `` : 

>>    `` : 

>>    `` : 

>>    `` : 

>>    `` : 

>>    `` : 

>>

>>

>>

## Objects

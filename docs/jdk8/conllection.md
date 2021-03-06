   
``` java 
   int size()
```

``` java 
   boolean isEmpty()
``` 

``` java 
   /**
      Returns <tt>true</tt> if this collection contains the specified element.
    */
   boolean contains(Object o)
```   

``` java 
   /**
      Returns an iterator over the elements in this collection.
    */
   Iterator<E> iterator()
``` 

 ``` java 
/**
 *    Returns an array containing all of the elements in this collection.
 */
   Object[] toArray()
 ``` 

 ``` java 
   /**
	      Returns an array containing all of the elements in this collection; the runtime type of the returned array 
	   is that of the specified array.
   */
   <T> T[] toArray(T[] a)
   
 ``` 
 ``` java 
   /**
	    Ensures that this collection contains the specified element (optional operation).  Returns <tt>true</tt> if 
	  this collection changed as a result of the call.  (Returns <tt>false</tt> if this collection does not permit 
	  duplicates and already contains the specified element.)
   */
   boolean add(E e)
   
 ``` 
  ``` java 
   
   /**
     Removes a single instance of the specified element from this collection, if it is 
   present (optional operation).
   */
   boolean remove(Object o)
   
 ``` 
 ``` java 
   /**
   Returns <tt>true</tt> if this collection contains all of the elements in the specified collection.
   */
   boolean containsAll(Collection<?> c)
   
 ``` 
``` java 
/**
   Adds all of the elements in the specified collection to this collection (optional operation).
*/
   boolean addAll(Collection<? extends E> c)
   
``` 
``` java 
/**
   Removes all of this collection's elements that are also contained in the specified 
 collection (optional operation).  After this call returns, this collection will contain no elements 
 in common with the specified collection.
*/
   boolean removeAll(Collection<?> c)
```
``` java 
/**
   Removes all of the elements of this collection that satisfy the given predicate.  Errors or runtime 
 exceptions thrown during iteration or by the predicate are relayed to the caller.
*/
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
``` java  
  /**
   *    Retains only the elements in this collection that are contained in the
   * specified collection (optional operation).  In other words, removes from
   * this collection all of its elements that are not contained in the
   * specified collection.
   */
   boolean retainAll(Collection<?> c)
```
``` java 
  /**
     * Removes all of the elements from this collection (optional operation).
     * The collection will be empty after this method returns.
     *
     * @throws UnsupportedOperationException if the <tt>clear</tt> operation
     *         is not supported by this collection
     */
    void clear();
   
```
``` java 
   
    /**
     * Creates a {@link Spliterator} over the elements in this collection.
     */
   @Override
    default Spliterator<E> spliterator() {
        return Spliterators.spliterator(this, 0);
    }
   
```
[Spliterator 参考文档](http://blog.csdn.net/lh513828570/article/details/56673804)
``` java 
    /**
     * Returns a sequential {@code Stream} with this collection as its source.
     */
    default Stream<E> stream() {
        return StreamSupport.stream(spliterator(), false);
    }
   
```
[Stream 参考文档](https://www.ibm.com/developerworks/cn/java/j-lo-java8streamapi/ "IBM 之 Java 8 中的 Streams API 详解")
``` java 
    /**
     * Returns a possibly parallel {@code Stream} with this collection as its
     * source.  It is allowable for this method to return a sequential stream.
     * @since 1.8
     */
    default Stream<E> parallelStream() {
        return StreamSupport.stream(spliterator(), true);
    }
   
```
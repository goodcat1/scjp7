Abstract Classes and Interfaces
====================

<table>
<tr>
    <td><strong>Iterable</strong></td>  
    <td>A class implementing this interface can be used for iterating with a for each statement.</td>
</tr>
<tr>
<tr>
    <td>*Collection*</td>
    <td>Common base interface for classes in the collection hierarchy. When you want to write 
methods that are very general, you can pass the Collection interface.
For example, max() method in java.util.Collections takes a Collection and
returns an object.
    </td>
</tr>
<tr>
    <td>*List*</td>
    <td>Base interface for containers that store a sequence of elements. You can access the
elements using an index, and retrieve the same element later (so that it maintains
the insertion order). You can store duplicate elements in a List.
    </td>
</tr>
<tr>
    <td>*Set, SortedSet,
NavigableSet
Queue, Deque*
    </td>
    <td>Interfaces for containers that don’t allow duplicate elements. SortedSet maintains
the set elements in a sorted order. NavigableSet allows searching the set for the
closest matches.
Queue is a base interface for containers that holds a sequence of elements for
processing. For example, the classes implementing Queue can be LIFO (last in,
first out— as in stack data structure) or FIFO (first in, first out—as in queue data
structure). In a Deque you can insert or remove elements from both the ends.
    </td>
</tr>
<tr>
    <td>*Map, SortedMap, NavigableMap*</td>
    <td>Base class for containers that map keys to values. In SortedMap, the keys are in a
sorted order. A NavigableMap allows you to search and return the closest match
for given search criteria. Note that Map hierarchy does not extend the Collection
interface.</td>
</tr>
<tr>
    <td>*Iterator, ListIterator*</td>
    <td>You can traverse over the container in the forward direction if a class implements
the Iterator interface. You can traverse in both forward and reverse directions if a
class implements the ListIterator interface.
    </td>
</tr>
</table>

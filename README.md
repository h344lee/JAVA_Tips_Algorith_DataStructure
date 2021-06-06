# JAVA_Tips_Algorithm_DataStructure

## Tips

### String
    String.parseInt(decimalString);
    String.parseInt(binaryString,2);
    String.substring(startIndex, endIndex+1);
    String.charAt(stringIndex);

### Integer
    Integer.toBinaryString(binaryInteger);

## Algorithm

### Binary Search

 
    while (low <= high) {
      int mid = (low + high) / 2;
      if ( answer condition) return mid;
      else if ( mid > x ) {
          high = mid - 1;
      } else {
          low = mid + 1;
      }
    }

## Data Structure

### Collection

#### List
Data can be duplicated, Order 
- LinkedList
- Stack
- Vector
- ArrayList

#### Set 
Data cannot be duplicated, Order-less
- HashSet
- SortedSet (TreeSet)

### MAP
each entry consists of (key, value) pair
#### Hashtable
#### HashMap
#### SortedMap (TreeMap)

#### Queue
- LinkedList
- PriorityQueue




# JAVA_Tips_Algorithm_DataStructure

## Tips


### Array
    Arrays.sort(arrayVariable);
    System.arraycopy(originalArrayVariable, startIndex, destArrayVariable, startIndex, copyLength);

### String
    String.parseInt(decimalString);
    String.parseInt(binaryString,2);
    String.substring(startIndex, endIndex+1);  // the second parameter is the starting point of the remaining string
    String.charAt(stringIndex);
    StringVariable.split(" ");    // it requires double quotes

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

#### List Interface
Data can be duplicated, Order 
- LinkedList
- Stack
- Vector
- ArrayList

#### Set Interface
Data cannot be duplicated, Order-less
- HashSet
- SortedSet (TreeSet)

#### MAP Interface
each entry consists of (key, value) pair
- Hashtable
- HashMap
- SortedMap (TreeMap)

      TreeMap<Integer, Integer> map = new TreeMap<>();   // automatically ordered by red-black tree 
      map.put(arr[size-1], size-1);            // put(key_variable , value_variable)
      for (int i = size-2; i >= 0; i--) {
          Map.Entry high_key_value_pair = map.ceilingEntry(arr[i]);  // get an entry which has equal or the smallest large value of arr[i]
          Map.Entry low_key_value_pair = map.floorEntry(arr[i]);     // variable is Map.Entry type
          if (high_key_value_pair != null) higher[i] = lower[(int)high_key_value_pair.getValue()];   // getValue() method 
          if (low_key_value_pair != null) lower[i] = higher[(int)low_key_value_pair.getValue()]; 
      }

#### Queue Interface
- LinkedList
- PriorityQueue




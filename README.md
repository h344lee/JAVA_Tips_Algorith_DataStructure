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

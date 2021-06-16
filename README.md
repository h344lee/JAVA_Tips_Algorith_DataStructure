# JAVA_Tips_Algorithm_DataStructure

## Tips

### Collections
    Collections.sort(arrayVariable);    // Merge Sort : stable, O(nlogn) guaranteed, double memory space
    Collections.sort(arrayVariable, Collections.reverseOrder())

### Arrays
    Arrays.sort(arrayVariable);    // Double Pivot Quick Sort : unstable, O(n^2) ~ O(nlogn), in-place sorting
    Arrays.sort(arrayVariable, Collections.reverseOrder())
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
Each entry consists of (key, value) pair
- Hashtable
- HashMap (put, get, remove, containsKey, containsValue)

      HashMap<Integer, Integer> hashMap = new HashMap<>();
      HashMap<Integer, Integer> valIndex = new HashMap<>();

      for (int i = 0 ; i < nums.length; i++){
          if(hashMap.containsKey(nums[i])) {
              hashMap.put(nums[i], hashMap.get(nums[i])+1);
          } else {
              hashMap.put(nums[i], 1);
          }
          valIndex.put(nums[i], i);
      }
      // hashMap.remove(1);  // remove by key

- TreeMap (put, getKey, getValue, containsKey, containsValue, ceilingEntry, floorEntry)

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

## Graph

### Adjacency List
An array of lists is used. The size of the array is equal to the number of vertices. Let the array be an array[]. An entry array[i] represents the list of vertices adjacent to the ith vertex. 

    // Creating a graph with 5 vertices
    int V = 5;
    ArrayList<ArrayList<Integer> > adj = new ArrayList<ArrayList<Integer> >();
         
    for (int i = 0; i < V; i++)
        adj.add(new ArrayList<Integer>());

    // Adding edges one by one
    addEdge(adj, 0, 1);
    addEdge(adj, 0, 4);
    addEdge(adj, 1, 2);
    addEdge(adj, 1, 3);
    addEdge(adj, 1, 4);
    addEdge(adj, 2, 3);
    addEdge(adj, 3, 4);


    static void addEdge(ArrayList<ArrayList<Integer> > adj, int u, int v){
       adj.get(u).add(v);
           adj.get(v).add(u);
    }


### BFS

Queue + While

    Queue<Integer> q = new LinkedList<Integer>();
    check[1] = true; 
    q.add(1);

    while (!q.empty()) {
      int x = q.poll();   // peek & remove
      for (int i = 0; i < a[x].size(); i++) {
        int y = a[x][i];
        if (check[y] == false) {
          check[y] = true;
          q.add(y);
         }
      }
    }

### DFS

Stack is replaced by recursive function

    void dfs (int x) {
      check[x] = true;
      for (int i = 0; i < a[x].size(); i++) {
        int y = a[x][i];
        if (check[y] == false) {
        dfs(y);
        }
      }
    }


### Dijkstra


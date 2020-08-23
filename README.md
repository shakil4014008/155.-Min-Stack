# 155.-Min-Stack

```C#
   public class MinStack {

   Stack<int> st;
    
    /** initialize your data structure here. */
    public MinStack() {
          st = new Stack<int>();
    }
    
    public void Push(int x) {
        st.Push(x);
    }
    
    public void Pop() {
        st.Pop();
    }
    
    public int Top() {
        return st.Peek();  
    }
    
    public int GetMin() {
        int val = Int32.MaxValue;
        foreach(int elem in st){
            if(elem<val)
                val = elem;
        }
        return val;
    }
}
```

## Complexity Analysis 

* Time Complexity: O(N)  ??????
* Space Complexity: O(N) ??????

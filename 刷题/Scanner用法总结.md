## Scanner用法总结

### 1 scanner.nextLine()

### 2 scanner.nextInt()

> 只读取有效数字，遇到空格会停下：所以可以巧妙应用

##### 输入描述：

先输入键值对的个数n（1 <= n <= 500）
然后输入成对的index和value值，以空格隔开

##### 输出描述：

输出合并后的键值对（多行）

``` java
import java.util.*;
 
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        while (sc.hasNext()) {
            Map<Integer, Integer> map = new TreeMap<Integer, Integer>();
            int n = sc.nextInt();
            for (int i = 0; i < n; i++) {
                int s=sc.nextInt(); //遇到空格停止读入
                int value=sc.nextInt(); //遇到空格停止读入，key，value其实属于同一行输入
                if (map.containsKey(s)) {
                    map.put(s, map.get(s) + value);
                } else
                    map.put(s, value);
            }
            for (Integer key : map.keySet()) {
                System.out.println(key + " " + map.get(key));
            }
        }
    }
}
```


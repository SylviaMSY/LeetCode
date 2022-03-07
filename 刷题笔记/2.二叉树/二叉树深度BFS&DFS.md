## 二叉树深度计算：BFS、DFS算法

#### 1 深度优先搜索 DFS

##### 递归实现：

``` java
class Solution {
    public int maxDepth(TreeNode root) {
        if(root == null){
            return 0;
        }
        // 深度遍历左右节点，取最大的值
        return Math.max(maxDepth(root.left),maxDepth(root.right)) + 1;

    }
}
```

##### 迭代实现：栈

```java
public static void dfsWithStack(Node root) {
    if (root == null) {
        return;
    }
    Stack<Node> stack = new Stack<>();
    // 先把根节点压栈
    stack.push(root);
    while (!stack.isEmpty()) {
        Node treeNode = stack.pop();
        // 遍历节点操作
        process(treeNode)
        // 先压右节点
        if (treeNode.right != null) {
            stack.push(treeNode.right);
        }
        // 再压左节点
        if (treeNode.left != null) {
            stack.push(treeNode.left);
        }
    }
}
```



#### 2 广度优先搜索 BFS：FIFO，所以队列实现

``` java
class Solution {
    public int maxDepth(TreeNode root) {
        if (root == null) {
            return 0;
        }
        Queue<TreeNode> queue = new LinkedList<TreeNode>();//队列
        queue.offer(root);//放入root
        int ans = 0;
        while (!queue.isEmpty()) {
            int size = queue.size();
            while (size > 0) {
                TreeNode node = queue.poll();//取出节点
                if (node.left != null) {
                    queue.offer(node.left);//放入节点
                }
                if (node.right != null) {
                    queue.offer(node.right);//放入节点
                }
                size--;
            }
            ans++;
        }
        return ans;
    }
}
```




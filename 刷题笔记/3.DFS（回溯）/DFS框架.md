### 1 回溯算法

``` java
List<List<Integer>> res = new LinkedList<>();
/* 主函数，输⼊⼀组不重复的数字，返回它们的全排列 */
List<List<Integer>> permute(int[] nums) {
     // 记录「路径」
     LinkedList<Integer> track = new LinkedList<>();
     backtrack(nums, track);
     return res;
}

// 路径：记录在 track 中
// 选择列表：nums 中不存在于 track 的那些元素
// 结束条件：nums 中的元素全都在 track 中出现
void backtrack(int[] nums, LinkedList<Integer> track) {
     if (track.size() == nums.length) { // 触发结束条件
     	res.add(new LinkedList(track));
     	return;
     }

     for (int i = 0; i < nums.length; i++) {
     	if (track.contains(nums[i])) { // 排除不合法的选择
     	continue;
     }
     track.add(nums[i]); // 做选择
     backtrack(nums, track); // 进⼊下⼀层决策树
     track.removeLast(); // 取消选择
     }
}
```


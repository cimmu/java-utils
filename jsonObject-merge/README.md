## 需求背景

现在有两个JSONArray，每个JSONArray中都有多个JSONObject，每个JSONObject中都有一个name属性。java如何使用fastjson将两个JSONArray中的name相同的JSONObject的其他属性合并成一个新的JSONObject然后存放在新的JSONArray中

## 代码解释

合并所有的代码会遍历array2中的所有JSONObject，并查找名字相同的JSONObject。如果找到了，就将它们合并到一起，然后将合并后的JSONObject添加到结果JSONArray中。

这段代码的时间复杂度是O(n)的，其中n是输入JSONArray中JSONObject的总数。因此，这段代码速度要快得多，比使用嵌套循环的方法快得多。


合并指定属性的代码，代码会遍历array2中的所有JSONObject，并查找名字相同的JSONObject。如果找到了，就将它们的指定的多个属性合并到一起，然后将合并后的JSONObject添加到结果JSONArray中。

你可以在`mergedObject.put`语句中设置你希望合并的属性。例如，你可以使用`mergedObject.put("prop1", object1.get("prop1"))`来将两个`JSONObject`的`prop1`

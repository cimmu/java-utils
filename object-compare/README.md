## 调用示例

### 在实体类上使用注解

```java
public class Entity {
    @NeedCompare
    private String field1;
    private String field2;
    // ...
}
```

### 调用方法进行比对

```java
Entity entity1 = new Entity();
entity1.setField1("value1");
entity1.setField2("value2");

Entity entity2 = new Entity();
entity2.setField1("value3");
entity2.setField2("value2");

Map<String, Object> differences = EntityComparer.compare(entity1, entity2);
// differences = {field1=value3}
```

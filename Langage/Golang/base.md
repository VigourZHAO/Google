

---

## Array

append：

1. head

   ```go
   var b = []int{1, 2, 3}	// result [1 2 3]           
   b = append([]int{0}, b...)	// result [0 1 2 3]
   b = append([]int{-3, -2, -1}, b...)	// result [-3 -2 -1 0 1 2 3]
   ```

   

2. inner

   ```go
   var c = []int{1, 2, 3}	// result [1 2 3]
   c = append(c[:1], append([]int{7}, c[1:]...)...)	// result [1 7 2 3]
   c = append(c[:3], append([]int{8, 9}, c[3:]...)...)	// result [1 7 2 8 9 3]
   ```

   

3. end

   ```go
   var a []int	// result []
   a = append(a, 1)	// result [1]
   a = append(a, 1, 2, 3)	// result [1 1 2 3]
   a = append(a, []int{1, 2, 3}...)	// result [1 1 2 3 1 2 3]
   ```

delete：

1. head

   ```go
   slice
   ```

2. inner

   ```go
   append
   copy
   append + slice
   ```

3. end

   ```go
   slice
   ```

   

copy：

1. 对原数组复制

ref：

1. 对原数组的引用，原数组改变，引用数组随动。

---

## Map

1. 可使用 make() 构造 map，但不可使用 new() 构造 map。

delete：

1. delete(map_obj, key)

concurrent：

1. sync

   ```go
   import "sync"	// 线程安全
   
   var sence sync.Map
   
   sence.Store("key", "value")	// 存储
   sence.Load("key")	// 获取
   sence.Delete("key")	//删除
   
   // 回调函数遍历
   scene.Range(func(k, v interface{}) bool {
   	fmt.Println("iterate:", k, v)
       return true
   })
   ```

   

---

## Linked list

init：

1. container/list 包
   1. 如： linked_list := list.New()
   2. 如： var linked_list list.List

Insert：

1. Front：
   1. linked_list.PushFront("pre")
2. Back：
   1. linked_list.PushBack("back")
3. inner：
   1. Front：
      1. linked_list.InsertBefore("item", des_item)
   2. Back：
      1. linked_list.InsertAfter("item", des_item)

delete：

1. linked_list.Remove(item)

Iter：

1. ```go
   for i := linked_list.Front(); i != nil; i = i.Next() {
   	fmt.Println(i.Value)
   }
   ```

---


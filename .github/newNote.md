# **Kotlin Notes**

常數/變數宣告
-
    變數    var x=5;
    常數    val x=0;    //自動推定為Int

但不一定要賦值:
```kotlin=
val x:int;  //代表x尚未賦值
```

When
-
類似C的switch，不過可以做更多活用
```kotlin=
when (x) {
    0,1 -> print("x == 0 or x == 1")        //特定值
    in 1..10 -> print("x is in the range")  //在特定範圍內
    is String -> x.startsWith("prefix")     //特定型別
    x.isOdd() -> print("x is odd")          //使用函數
    else -> print("otherwise")              //其他
}
```

函式宣告
-
**fun 函式名稱(傳入參數:參數型別):傳回值型別{函式內容}**
```kotlin=
fun sum(a: Int, b: Int): Int {
    return a + b
}
```
    
也可以用表達式寫成:
```kotlin=
fun sum(a: Int, b: Int) = a + b
```

* Unit: 返回無意義的值(理解成Void)
    **當返回型別為Unit，可省略不寫**
```kotlin=
fun sum(a: Int, b: Int): Unit {
    Log.e("a+b",(a+b).toString());
}
```
* **並無規定傳入的值--->使用型別Any**
```kotlin=
fun sum(a: Any){
    if (a ! is String) return null
    return a.length
}
```
字串模板
-
```kotlin=
var a=1;
var str1="a is $a"; //="a is "+a.toString();
print(str1);
```
    output: a is 1

List
-
使用listOf建立
```kotlin=
val fruits = listOf("banana", "avocado", "apple")
```
Lambda
-



scanf = python 的 input  
在scanf裡面的& = 取址 儲存到我想要的位置  
```c  
int main(){
int i
scanf("%d", &i)  
}
```  
這段 = python的  
```python  
i = int(input(""))  
```  
c語言的if判斷式必須加()  

```C
if(a>=0)  
```  
 然後在加{想做的動作} 就會變成  
 ```c  
 if(a>=0){
 printf("Y");
}
```  
其他的elif 與 else 的用法相似於python  
switch相似if  且switch只會用在數值或字元  
```c  
switch (變數名稱){  
    case: 符合的條件;//有等於的意思  
        運行  
        break//break是結束, 跳出switch涵式的一意思  
    default://像是if 涵式的elas  
}
```
# for迴圈

for(執行式1;判斷式1;執行式3);
    執行式2;

                                                                                                                                               \/-------------------------------------------------<-
                            |                                                  |
其過程: 執行執行式1--> 判斷判斷式1是否為正確 --> 正確:執行執行式2 --> 執行執行式3  
                                           --> 不正確:結束迴圈



# while迴圈    
while(判斷式){  
    執行式;    
}    

順序為:判斷判斷式 如果正確 -->執行執行式  
(且無限執行)  
```c  
int main(){
    int i=1;
    while (i<10)
    {
        i++;
        printf("%i", i);
    }
}    
```

# break  
簡單來說就是用來跳出迴圈  
舉例如下:  
```c
int i;
for(i = 0;i < 10;i++){
    if(i == 5) {
        break;

    }
    printf("%i",i)
}
```

# continue  
跳過迴圈的意思  
(是跳過不是跳出)  
```c  
int i;
for(i = 0;i < 10;i++){
    if(i == 5) {
        continue;
    }
    printf("%i",i)
}
```  
會輸出:1 2 3 4 6 7 8 9  


# 陣列  
簡單來說就是同個元素的集合  
要定義一個陣列時 要先定義他的類型(就是int等等) 還有元素的數量 如下  
```c  
int a[大小];
``` 
在陣列中每個元素都是一個整數 (注意:排序是由零開始) 所以第一個元素
為0 第二個為1 第三個為2以此類推 我們可以把這些陣列裡面的每個數字  
賦予一個新的數 如下:  
```c
a[0] = 10;
a[3] = 30;
```  
這串代碼的意思是把a陣列裡面的第一項數字賦值為10 第四項賦值為30
同樣的要賦值也可以使用這種方法:
```c
int a[] = {12, 23, 45,};  
```
這串程式碼的意思是建立一個有三個元素的陣列a 並把第一項賦值為12  
第二項為23 第三項為45
陣列除了一維陣列 還有多維陣列 如下;
```c
int a[列][行];
```  

# 字串  
跟陣列的用法雷同 只是輸入的是字元 不是數字  
以下是字串的例子  
```c
char st[10]; //st字串有十的長度  
    scanf("%s", st);//要求輸入字串的內容 並以字元的形式儲存在字串st裡  
    printf("%s",st);//輸出字串內容  
```
需要注意的是在字串要存入多個字元時必須要留一個空字元給空格  
如下  
```c
char st[] = {'h', 'e', 'l', 'l', 'o', '\0'};
```
# 結構(struct)    
可以創建一個結構來概括多個變量
例如 整數 字符 浮點數等等

舉例來說要創建一個名為student的結構  
裡面包含了需要的變量 像班級 座號 學號 名字  
```c
struct student{
    int class; //班級  
    int number;//座號  
    int id;    //學號  
    char name[10];  
}  
```
當需要這個結構時 可以創建他的名字  
```c  
struct studen my_student;  
```  
如此一來我們就可以將這些變量賦值  
```c
my_student.class = 104;  
my_student.number = 7;
my_student.id = 119045;
strcpy(my_student.name, "Ricky");
```  
當要輸出這些變量時
```c  
printf("class: %d\n", my_student.class);    
printf("number: %d\n", my_student.number);  
printf("id: %d\n", my_student.id);  
printf("name: %s\n", my_student.name);  
```
如此一來就可以印出 my_student 結構中的變量值了  
  
總之結構是c語言中非常有用的 可以讓我們創建數據類型 方便的儲存和操作多個變量  
# 列舉    
列舉是一種用於定義一組值的資料類型  
如下  
```c  
enum Weekday {
    Monday,
    Tuesday,
    Wednesday,
    Thursday,
    Friday,
    Saturday,
    Sunday
};  
```  
在這個例子中，定義了一個名為 Weekday的列舉
包含了七個值 同時也可以使用typedef為列舉定義名子
```c
typedef enum {
    Red,
    Green,
    Blue
} Color;
```
在這個例子中定義了一個名為 Color 的列舉
 也可以用下列方式初始化列舉的其中一個值  
```c
enum Weekday today = Monday;
```
也可以使用 switch 對列舉進行比較  
```c
switch(today){
    case Monday:
        printf("Today is Monday");
        break;
    case Tuesday:
        printf("Today is Tuesday");
        break;
    // 其他列舉值的情況
}
```  
# 指標  
在C語言中我們可以透過在一個變量錢加上(*)來  
宣告他指項指標變量 如下:
```C
int *num;
```  
我們可以在指標內取址來初始化指標  
如下:  
```c  
int i = 10;
int *num = &i;
``` 
這裡將num的指標變量賦值 其內容為從i取的址






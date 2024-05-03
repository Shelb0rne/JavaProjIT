# JavaProjIT
![](https://github.com/Shelb0rne/JavaProjIT/actions/workflows/Maven.yml/badge.svg)

## Описание работы кода 
Код ```/src/main/TZ_2.java ``` принимает файл и считывает находящиеся в нем числа, далее он переписывает данные числа в динамический массив ```nums``` после чего вызываются методы ```_max ```, ```_min ```, ```_sum ```, ```_mult ```, которые находят максимум и минимум среди всех входных чисел, а также сумму и произведение всех чисел.
## Методы ```_max``` и ```_min```
```
 public static long _max(){
       List<Long> copy = nums;
       Collections.sort(copy);
       return copy.getLast();
    }
    public static long _min(){
        List<Long> copy = nums;
        Collections.sort(copy);
        return copy.getFirst();
    }
```
Оба метотда сортируют по возрастанию массив ```nums```, таким образом максимумом будет число отсортированного массива с индесом ```nums.size()-1```, то есть последнее число массива, а минимумом будет число с индексом 0, то есть первое число массива. 

## Метод ```_sum```
```
public static long _sum(){
        long ans=0;
        for (int i =0; i< nums.size(); i++){
            ans+= nums.get(i);
        }
        return ans;
    }
```
Данный метод создает переменную ```ans```, и пробегаясь по 'ktvtynfv массива, с помощью цикла прибавляет все значения к ```ans```.

## Метод ```_mult``` 
```
public static BigInteger _mult(){
        BigInteger ans = new BigInteger("1");
        for (int i = 0; i< nums.size(); i++){
            ans = ans.multiply(BigInteger.valueOf(nums.get(i)));
        }
        return ans;
    }
```
Данный метод создает переменную ```ans```, но уже данная переменная имеет тип BigInteger, для хранения большого числа, которое легко привышает максимальное значение типа Long. Локига кода такая же как и у метода ```_sum```, код пробегается по массиву и умножает ```ans``` на каждый элемент.

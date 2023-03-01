# MirMaxFun 

```java
package ru.mirmaxfun.javalesson;

import java.util.Scanner;

public class HomeWorkSix
{
    public static void main(String[] args) {
        /*
                                Домашнее задание. Вебинар 6.
        Сделать из произвольной строки, введённой пользователем, массив символов. (DONE)
        Сделать каждый чётный символ в строке заглавным, если это возможно. (DONE)
        Пользователь вводит строку. С помощью методов StringBuilder найти и удалить в ней все пробелы. (DONE)
        */


        Scanner scanner = new Scanner(System.in);
        String str = scanner.nextLine();


        char[] chars = str.toCharArray();
        for (int i = 0; i < chars.length; i++)
        {
            System.out.print(chars[i]);
        }
        System.out.println();
        for (int i = 0; i < chars.length; i++)
        {
            if (i%2 == 0){
                chars[i] = Character.toUpperCase(chars[i]);

            }
            System.out.print(chars[i]);
        }
        System.out.println();
        System.out.println("Enter text: ");
        String str2 = scanner.nextLine();
        StringBuilder builder = new StringBuilder(str2);
        for (int i = 0; i < builder.length(); i++)
        {
            if (builder.charAt(i) == ' '){
                builder.deleteCharAt(i);
                i--;
            }

        }
        System.out.print(builder);

    }
}
```
# 58ͬ�ǹ�˾2018У԰��Ƹ�㷨������

<!-- TOC -->
* [��һ��](#��һ��)
* [�ڶ���](#�ڶ���)
<!-- TOC -->


## ��һ��

### ��Ŀ����
>����һ������metrix��������ֻ����1��0���������е�1�������ڣ�����һ����n�����ܷ��ڽ�������n��0�������1���ƻ�1�������ڵ�������

**��������:**
>��һ��ΪN����ʾ����Ԫ�ظ���
�ڶ���ΪM����ʾ��Ҫ�滻�ĸ���
������Ϊ�����N��Ԫ��


**�������:**
>�滻���ܷ��ƻ�����������

**������**
```
����
5
1
1 0 0 0 1

���
true

����
5
2
1 0 0 0 1

���
false
```

### �ο�����
```java
import java.util.Scanner;
public class Main{
    public static void main(String[] args){
        Scanner in = new Scanner(System.in);
        int N = in.nextInt();
        int M = in.nextInt();
        int[] arr = new int[N];
        for(int i=0;i<N;i++){
            arr[i]=in.nextInt();
        }
        //̰�ķ�
        int max = 0;
        for(int i=0;i<N;i++){
            if(arr[i]==0){
                boolean left = i-1>=0 ? arr[i-1]==0:true;
                boolean right = i+1<N ? arr[i+1]==0:true;
                if(left && right){
                    max++;
                    arr[i]=1;
                }
            }
        }
        System.out.println(max>=M);
    }
}
```

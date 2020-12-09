# Java4
第五次实验
一 实验目的
掌握字符串String及其方法的使用
掌握文件的读取/写入方法
掌握异常处理结构

二 实验要求
在某课上,学生要提交实验结果，该结果存储在一个文本文件A中。
文件A包括两部分内容：
一是学生的基本信息；
二是学生处理后的作业信息，该作业的业务逻辑内容是：利用已学的字符串处理知识编程完成《长恨歌》古诗的整理对齐工作，写出功能方法，实现如下功能：
1.每7个汉字加入一个标点符号，奇数时加“，”，偶数时加“。”
2.允许提供输入参数，统计古诗中某个字或词出现的次数
3.输入的文本来源于文本文件B读取，把处理好的结果写入到文本文件A
4.考虑操作中可能出现的异常，在程序中设计异常处理程序

三 实验过程
1设计学生类
2实例化某学生
3读取学生作业
4利用字符串的一些方法实现对古诗的格式化，以及添加字符奇数句子加“，”偶数句子加“。\n”实现换行以及分割。  
5将处理完的作业写入并保存
6设计主函数，输出学生信息和作业处理情况

四主要代码
class Homework{
    public static StringBuffer HW(StringBuffer str1){
        StringBuffer str2 = new StringBuffer(str1);
        int j=0;int z;
        for(int i = 7;i < str2.length()-45;i= i+7){
            z = i +j;
            if(i%2 == 0){
                str2.insert(z,"。\n");
                j = j+2;
            }
            else{
                str2.insert(z,"，");
                j= j+1;
            }
        }
        System.out.println(str2);
        return str2;
    }
    
五实验结果
![image](https://github.com/Dark-less/Java4/blob/main/f130408064b18314f3b62242405b72f.png)

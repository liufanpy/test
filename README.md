# test
//为什么需要抽象接口？为什么Collections.sort()方法需要传入Comparator这个抽象接口？
接口是对不同类通用方法的抽象，解决了重复创建同一类型方法的问题，也是解决不同类的同一方法的存在不同形态问题的方式，因为在接口用抽象方法只规定要做什么，具体怎么做不同类通过实现接口，重写方法即可；
例如，Collections.sort (List<T> list, Comparator<? super T> c)中传入Comparator接口，因为需要的不同比较方法不同，所以规定要比较，具体怎么比较重写其中的抽象方法compareTo()即可；

图片为接口作用的具体体现
public class Test {
  public static void main(String[] args) {
    ChinesePeople cp1 = new ChinesePeople("张三",18);
    cp1.country="中国";
    System.out.println("姓名:"+cp1.name+",年龄:"+cp1.age+",国家:"+cp1.country);
    System.out.println("-------------------------");
    ChinesePeople cp2 = new ChinesePeople();
    //应为country被所有类的对象共享，所以被定义的country一旦定义，其他的类也能获取该值。
    System.out.println("姓名:"+cp2.name+",年龄:"+cp2.age+",国家:"+cp2.country);
    ChinesePeople.country="大中国";
    ChinesePeople cp3 = new ChinesePeople("李四",22);
    System.out.println("姓名:"+cp1.name+",年龄:"+cp1.age+",国家:"+cp1.country);
    System.out.println("姓名:"+cp2.name+",年龄:"+cp2.age+",国家:"+cp2.country);
    System.out.println("姓名:"+cp3.name+",年龄:"+cp3.age+",国家:"+cp3.country);
  }

# This is an <h1> tag
## This is an <h2> tag
###### This is an <h6> tag}
  
  *This text will be italic*
_This will also be italic_

**This text will be bold**
__This will also be bold__

_You **can** combine them_


class Utils{
    public static int getSum(int num1,int num2) {
		return num1+num2;
    }
}

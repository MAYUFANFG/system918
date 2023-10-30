Q：
請新增一個CShape的子類別CTriangle，其constructor 共有三個double的參數 a,b,c (為直角三角形的三個邊長)，其面積為0.5*a*b，請寫出CTriangle的類別程式與產生其物件的main 程式(顏色為紅色，a=3, b=4, c=5) 程式碼請

A：
```java
public abstract class CShape {
    protected String color;
    public abstract void setColor(String str);
    public abstract double getArea();
}

public class CTriangle extends CShape {
    protected double a, b, c;

    public CTriangle(double a, double b, double c) {
        this.a = a;
        this.b = b;
        this.c = c;
    }

    public void setColor(String str) {
        color = str;
    }

    public double getArea() {
        return 0.5 * a * b;
    }

    public void show() {
        System.out.println("color=" + color + ", area=" + getArea());
    }
}

public class Main {
    public static void main(String[] args) {
        CTriangle tri = new CTriangle(3, 4, 5);
        tri.setColor("Red");
        tri.show();
    }
}
```
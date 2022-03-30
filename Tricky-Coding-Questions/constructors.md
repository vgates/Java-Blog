#### 1. What is the output?
```
class Parent {
    private int number;
    public Parent(int number) {
        this.number = number;
    }
}

public class Child extends Parent {
    public static void main(String[] args) {
        System.out.println("Hello World");
    }
}
```


### Answers
### 1. Will not compile
Since the Child class does not have Java compiler will try to add a default no-argument constructor and also it will insert ```super()``` in its constructor body. Since the Parent class has a constructor defined, the compiler will not add a default no-argument constructor. Hence super() call in the Child class does not compile. Adding a no-argument constructor in the Parent class will solve the issue.

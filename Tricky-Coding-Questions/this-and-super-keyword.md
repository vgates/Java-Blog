### Questions 
**Answers provided at the bottom**
1. What will be the output of the following?
  ```
  public class Main {
      private int number = 1;
      public Main(int number) {
          number = number;
      }
      public static void main(String[] args) {
          Main m = new Main(2);
          System.out.println(m.number);
      }
  }
  ```

2. What will the output of the following
  ```
  class Parent {
    protected int number = 2;
    String name = "ParentName";
  }

  public class Main extends Parent {
    protected int number = 4;
    int code = 1000;
    public void printMe() {
        System.out.println(this.number); 
        System.out.println(super.number);
        System.out.println(this.name);
        System.out.println(super.name);
        System.out.println(this.code);
    }
    public static void main(String[] args) {
        Main m = new Main();
        m.printMe();
    }
  }
  ```

### Answers
1. Output will be: **1**
  
    Explanation:  the constructor we are assigning the method value parameter to itself. If we need to change the value of the instance variable as 2 then we need to edit the constructor as  ```this.number = number;```
    
    Whenever we have a local variable with the same name as an instance variable, we need to use **this** keyword. 
    
    If the local variable has a different name as shown below then **this** is not necessary. See the change we made as below. In that case output would be **2**
    ```
    ...
    public Main(int num) {
        number = num;
    }
    ...
    ```

2. Output will be
    ```
    4
    2
    ParentName
    ParentName
    1000
    ```
    We cannot access code using super keyword because the variable code is only defined in the Main class.
    


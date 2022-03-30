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
  

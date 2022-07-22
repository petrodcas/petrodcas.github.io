---
layout: post
title: Syntax comparison between languages
date: 2022-07-21 04:12:00 +0200
categories: tests
excerpt_separator: <!--excerpt-end-->
---

This time we are going to compare several languages' syntax and see which one is the
most comfortable to use in order to create large applications with low writing efforts.

Want to come along?
<!--excerpt-end-->
### Basic syntax on different languages

**Java**
```java
//single line comment

/*
 * Multiline comment
 */

/**
 * Here it is... Some javadoc.
 * 
 * @param args Arguments that are never used.
 */
public static void main(String[] args) {
  Car myCar = new Car("Mercedes", 32);
  System.out.println(String.format("Brand: %s%nColor: %d", myCar.getBrand(), myCar.getColor()));
}


public class Car {
  
  private String brand;
  private int color;

  public Car(String brand, int color) {
    setBrand(brand);
    setColor(color);
  }

  public void setColor(int color) {
    this.color = color;
  }

  public int getColor() {
    return this.color;
  }

  public void setBrand(String brand) {
    this.brand = brand;
  }

  public String getBrand() {
    return this.brand;
  }
}
```

**Kotlin**
```kotlin
//single line comment

/*
 * Multiline comment
 */

/**
 * some Kdoc
 */
fun main() {
  val myCar = Car(color = 32, brand = "Mercedes")
  println("Brand: ${myCar.brand}\nColor: ${myCar.color}")
}

data class Car(var color: Int, var brand: String)
```

**Python**
```python
# markdown codeblock
def main():
  """ docstring """
  myCar = Car(color=32, brand='Mercedes')
  print("Brand: %s\nColor: %d"%(myCar.brand, myCar.color))


class Car:
  def __init__(self, brand, color):
    self.color = int(color)
    self.brand = str(brand)


if __name__ == "__main__":
  main()


```
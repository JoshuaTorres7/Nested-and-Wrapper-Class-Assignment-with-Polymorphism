# Nested-and-Wrapper-Class-Assignment-with-Polymorphism

In the provided code, I began by creating an Automobile class with instance variables using Wrapper classes: Integer for year, Double for price, String for slogan, and Character for type. I defined getter and setter methods for each of these variables. Next, I developed a Toyota class that extends Automobile, initializing its properties with specific values: year 1937, price 0, slogan "Let's Go Places", and type 'na'. The Corolla, Tundra, and Highlander classes further extend Toyota, each with their own specific attributes while inheriting the slogan from Toyota and defining unique type values. The Highlander class also includes a nested class, allowing users to select between configurations of 8 seats or 7 seats. Additionally, I introduced an extra method in Corolla does not present in the other classes. Each class, including Automobile, Toyota, Corolla, Tundra, and Highlander, implements a sound method, which prints distinct sounds for each class. In the Main class, I created instances of all these classes to demonstrate polymorphism, static and dynamic binding, the use of Wrapper classes, and the nested class feature.

class Automobile {
private Integer year;
private Double price;
private String slogan;
private Character type;
public Integer getYear() {
return year;
}
public void setYear(Integer year) {
this.year = year;
}
public Double getPrice() {
return price;
}
public void setPrice(Double price) {
this.price = price;
}
public String getSlogan() {
return slogan;
}
public void setSlogan(String slogan) {
this.slogan = slogan;
}
public Character getType() {
return type;
}
public void setType(Character type) {
this.type = type;
}
public void sound() {
System.out.println("Generic automobile sound");
}
}
class Toyota extends Automobile {
public Toyota() {
setYear(1937);
setPrice(0.0);
setSlogan("Let's Go Places");
setType('n');
}
@Override
public void sound() {
System.out.println("MMMMMMMMMMM's sound");
}
}
class Corolla extends Toyota {
public Corolla() {
setYear(2023);
setPrice(21700.0);
setType('c');
}
public void additionalMethod() {
System.out.println("Corolla specific method");
}
@Override
public void sound() {
System.out.println("RRRRRRRRR's sound");
}
}
class Tundra extends Toyota {
public Tundra() {
setYear(2023);
setPrice(38965.0);
setType('t');
}
@Override
public void sound() {
System.out.println("NNNNNNN's sound");
}
}
class Highlander extends Toyota {
public Highlander() {
setYear(2023);
setPrice(36620.0);
setType('s');
}
@Override
public void sound() {
System.out.println("HHHHHHHHH's sound");
}
public class HighlanderConfiguration {
private int seats;
public HighlanderConfiguration(int seats) {
this.seats = seats;
}
public void displayConfiguration() {
System.out.println("Highlander Configuration: " + seats + " seats");
}
}
}
public class Main {
public static void main(String[] args) {
Automobile genericCar = new Automobile();
Toyota toyotaCar = new Toyota();
Corolla corollaCar = new Corolla();
Highlander highlanderCar = new Highlander();
Tundra tundraCar = new Tundra();
genericCar.sound();
toyotaCar.sound();
corollaCar.sound();
highlanderCar.sound();
tundraCar.sound();
Integer integerWrapper = 42;
Double doubleWrapper = 3.14;
System.out.println("Integer Wrapper: " + integerWrapper);
System.out.println("Double Wrapper: " + doubleWrapper);
Highlander highlander = new Highlander();
Highlander.HighlanderConfiguration config1 = highlander.new
HighlanderConfiguration(8);
Highlander.HighlanderConfiguration config2 = highlander.new
HighlanderConfiguration(7);
config1.displayConfiguration();
config2.displayConfiguration();
Corolla corolla = new Corolla();  
corolla.additionalMethod();
}
}Corolla corollaCar = new Corolla();
Highlander highlanderCar = new Highlander();
Tundra tundraCar = new Tundra();
genericCar.sound();
toyotaCar.sound();
corollaCar.sound();
highlanderCar.sound();
tundraCar.sound();
Integer integerWrapper = 42;
Double doubleWrapper = 3.14;
System.out.println("Integer Wrapper: " + integerWrapper);
System.out.println("Double Wrapper: " + doubleWrapper);
Highlander highlander = new Highlander();
Highlander.HighlanderConfiguration config1 = highlander.new
HighlanderConfiguration(8);
Highlander.HighlanderConfiguration config2 = highlander.new
HighlanderConfiguration(7);
config1.displayConfiguration();

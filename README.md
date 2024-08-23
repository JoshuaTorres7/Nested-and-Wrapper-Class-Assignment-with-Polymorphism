# Nested-and-Wrapper-Class-Assignment-with-Polymorphism
In the provided code, I began by creating an Automobile class with instance variables using Wrapper classes: Integer for year, Double for price, String for slogan, and Character for type. I defined getter and setter methods for each of these variables. Next, I developed a Toyota class that extends Automobile, initializing its properties with specific values: year 1937, price 0, slogan "Let's Go Places", and type 'na'. The Corolla, Tundra, and Highlander classes further extend Toyota, each with their own specific attributes while inheriting the slogan from Toyota and defining unique type values. The Highlander class also includes a nested class, allowing users to select between configurations of 8 seats or 7 seats. Additionally, I introduced an extra method in Corolla does not present in the other classes. Each class, including Automobile, Toyota, Corolla, Tundra, and Highlander, implements a sound method, which prints distinct sounds for each class. In the Main class, I created instances of all these classes to demonstrate polymorphism, static and dynamic binding, the use of Wrapper classes, and the nested class feature.

# -Shape-Inheritance-
// Abstract base class
abstract class Shape {
    // Abstract method to calculate the area
    public abstract double calculateArea();
}

// Circle class
class Circle extends Shape {
    private double radius;
    // Constructor to initialize radius
    public Circle(double radius) {
        this.radius = radius;
    }

    // Implementation of calculateArea for Circle
    @Override
    public double calculateArea() {
        return Math.PI * radius * radius;
    }
}

// Rectangle class
class Rectangle extends Shape {
    private double length, width;
    // Constructor to initialize length and width
    public Rectangle(double length, double width) {
        this.length = length;
        this.width = width;
    }

    // Implementation of calculateArea for Rectangle
    @Override
    public double calculateArea() {
        return length * width;
    }
}

// Square class
class Square extends Shape {
    private double side;
    // Constructor to initialize side
    public Square(double side) {
        this.side = side;
    }

    // Implementation of calculateArea for Square
    @Override
    public double calculateArea() {
        return side * side;
    }
}

// Triangle class
class Triangle extends Shape {
    private double base, height;
    // Constructor to initialize base and height
    public Triangle(double base, double height) {
        this.base = base;
        this.height = height;
    }

    // Implementation of calculateArea for Triangle
    @Override
    public double calculateArea() {
        return 0.5 * base * height;
    }
}

// Main class
public class ShapeInheritanceExample {
    public static void main(String[] args) {
        // Creating shape objects
        Shape circle = new Circle(5);
        Shape rectangle = new Rectangle(4, 6);
        Shape square = new Square(4);
        Shape triangle = new Triangle(3, 5);

        // Calculating and displaying areas
        System.out.println("Circle Area: " + circle.calculateArea());
        System.out.println("Rectangle Area: " + rectangle.calculateArea());
        System.out.println("Square Area: " + square.calculateArea());
        System.out.println("Triangle Area: " + triangle.calculateArea());
    }
}

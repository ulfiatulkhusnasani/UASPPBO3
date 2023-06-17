// File: Main.java

// Kelas Calculator untuk mengatur operasi kalkulator
class Calculator {
    private double operand1;
    private double operand2;
    
    public Calculator(double operand1, double operand2) {
        this.operand1 = operand1;
        this.operand2 = operand2;
    }
    
    public double add() {
        return operand1 + operand2;
    }
    
    public double subtract() {
        return operand1 - operand2;
    }
    
    public double multiply() {
        return operand1 * operand2;
    }
    
    public double divide() {
        if (operand2 != 0) {
            return operand1 / operand2;
        } else {
            throw new ArithmeticException("Error: Division by zero!");
        }
    }
}

// Kelas Main untuk menjalankan program
public class Main {
    public static void Main(String[] args) {
        double num1 = 10.5;
        double num2 = 5.5;
        
        Calculator calculator = new Calculator(num1, num2);
        
        double resultAdd = calculator.add();
        System.out.println(num1 + " + " + num2 + " = " + resultAdd);
        
        double resultSubtract = calculator.subtract();
        System.out.println(num1 + " - " + num2 + " = " + resultSubtract);
        
        double resultMultiply = calculator.multiply();
        System.out.println(num1 + " * " + num2 + " = " + resultMultiply);
        
        double resultDivide = calculator.divide();
        System.out.println(num1 + " / " + num2 + " = " + resultDivide);
    }
}

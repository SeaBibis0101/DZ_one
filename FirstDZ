public class SimpleStack {
    private int[] elements;  // массив для хранения элементов
    private int top;         // индекс вершины стека
    private int capacity;    // максимальный размер стека
    
    // Конструктор: создаем стек определенного размера
    public SimpleStack(int size) {
        elements = new int[size];
        capacity = size;
        top = -1;  // -1 означает, что стек пуст
    }
    
    // Добавление элемента в стек
    public void push(int value) {
        if (top == capacity - 1) {
            System.out.println("Стек переполнен!");
            return;
        }
        elements[++top] = value;
        System.out.println("В стек добавлено число: " + value);
    }
    
    // Удаление элемента из стека
    public int pop() {
        if (isEmpty()) {
            System.out.println("Стек пуст!");
            return -1;
        }
        return elements[top--];
    }
    
    // Просмотр верхнего элемента без удаления
    public int peek() {
        if (isEmpty()) {
            System.out.println("Стек пуст!");
            return -1;
        }
        return elements[top];
    }
    
    // Проверка на пустоту
    public boolean isEmpty() {
        return top == -1;
    }
    
    // Текущий размер стека
    public int size() {
        return top + 1;
    }
    
    // Вывод всех элементов стека
    public void display() {
        if (isEmpty()) {
            System.out.println("Стек пуст");
            return;
        }
        System.out.print("Стек (с конца): ");
        for (int i = top; i >= 0; i--) {
            System.out.print(elements[i] + " ");
        }
        System.out.println();
    }
    
    //Точка входа, тестирование
    public static void main(String[] args) {
        SimpleStack stack = new SimpleStack(5);
        
        // Добавление элементов
        stack.push(10);
        stack.push(20);
        stack.push(30);
        stack.push(100);
        
        System.out.println();
        stack.display();  // Стек (сверху вниз): 30 20 10
        System.out.println();

        System.out.println("Верхний элемент: " + stack.peek());  // просмотр верхнего элемента
        System.out.println("Удаляем: " + stack.pop());           // удаление
        System.out.println("Удаляем: " + stack.pop());           // просмотр второго верхнего элемента
        
        stack.display();  // Стек (сверху вниз): 10
    }
}

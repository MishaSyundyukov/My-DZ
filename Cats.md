public class Cats {
    public int food;
    public Cats(int food) {
        this.food = food;
    }


    boolean decreaseFood(int n) {
        int diff = food - n;
        if (diff < 0) return false;

        food -= n;
        return true;
    }
    void addFood(int food) {
        this.food += food;
    }

    void info() {
        System.out.println("plate: " + food);
    }
}
class Cat {
    private String name;
    private int appetite;
    private boolean hungry;

    Cat(String name, int appetite) {
        this.name = name;
        this.appetite = appetite;
        this.hungry = true;
    }

    void info() {
        String isHungry = !hungry ? "сыт" : "голоден";
        System.out.println(name + ": " + isHungry);
    }

    void eat(Cats plate) {
        if (hungry && plate.decreaseFood(appetite))
            hungry = false;
    }
}
    class Main {
    public static
    void main(String[] args) {
        Cat[] cats = {new Cat("Сережа", 20), new Cat("Матвей", 11), new Cat("Скот", 6), new Cat("Мусик", 50)};
        Cats plate = new Cats( 50);

        for (Cat cat : cats) {
            cat.eat(plate);
            cat.info();
        }
    }
}

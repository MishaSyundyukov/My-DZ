class Animal { public String name; public int run;

    public Animal() {
    }

    public Animal(String name) {
        this.name = name;
    }

    public void animalInfo() {
        System.out.println();

    }

    public static class Main {
        public static void main(String[] args) {

            Animal animal = new Animal("CatsCategory");
            Cat cat = new Cat("Серега", 200, false, 2);
            animal.animalInfo();
            cat.animalInfo();
            cat.catInfo();

            Animal danimal = new Animal("Dogs");
            Dog dog = new Dog("Шера", 500, 10, 0.5);
            danimal.animalInfo();
            dog.animalInfo();
            dog.dogInfo();

        }
    }
}

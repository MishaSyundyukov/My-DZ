public class Job { private String fullName; private String position; private String email; private String number; private int pay; private int age;

public Job(String fullName, String position, String email, String number, int pay, int age) {
    this.fullName = fullName;
    this.position = position;
    this.email = email;
    this.number = number;
    this.pay = pay;
    this.age = age;
}
public int getAge() {
    return age;
}
public String toString() {
    return (fullName + "\n-"
            + position + "\n-"
            + email + "\n-"
            + number + "\n-"
            + number + "\n-"
            + age);
}
public static void main(String[] args) {
    Job[] person = new Job[5];
    person[0] = new Job("Иванов А.И", "Специалист", "ivivan@mailbox.com", "89334567311",25000,33);
    person[1] = new Job("Семенова Е.В", "Бугалтер", "semyka1973@mailbox.com", "89777552065",50000,49);
    person[2] = new Job("Антонов Е.А", "Стажер", "anton2000@mailbox.com", "89176985510",10000,21);
    person[3] = new Job("Карина А.А", "Секретарь", "carinaanna@mailbox.com", "89098527631",55000,41);
    person[4] = new Job("Астаров В.И", "Заместитель директора", "astor@mailbox.com", "89175284931",90000,44);
    for (Job employee : person)
        if (employee.getAge()>40)
            System.out.println(employee);

}
}

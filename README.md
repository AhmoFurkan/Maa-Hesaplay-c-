![image](https://github.com/user-attachments/assets/8c6bd47a-4510-4cbd-8034-a1ffee7fe2ca)# Maa-Hesaplay-c-
![image](https://github.com/user-attachments/assets/70f63a58-031a-4319-8092-de5896105c16)
![image](https://github.com/user-attachments/assets/b69482b4-dc8d-4659-97cb-91a1949b7327)
![image](https://github.com/user-attachments/assets/d3fbc99e-b9e3-4b88-9ae0-e023c7901a6b)



public class Main {

    public static void main(String[] args) {
        Employee calisan1 = new Employee("Ahmet Furkan",200,45,2010);
        calisan1.tax();
        calisan1.bonus();
        calisan1.raiseSalar();
        calisan1.ekranCıktı();

        Employee calisan2 = new Employee("Ahmet Furkan",5000,30,2000);

    }

}



==========================================================
public class Employee {
    String name;
    int salary;
    int workHours;
    int hireYear;
    double vergi;
    double fazlaUcret;
    double zam;

    Employee(String name, int salary, int workHours, int hireYear) {
        this.name = name;
        this.salary = salary;
        this.workHours = workHours;
        this.hireYear = hireYear;

    }

    void tax() {
        if (this.salary < 1000) {


        } else {
            vergi = this.salary * 0.03;
        }
    }

    void bonus() {

        if (this.workHours > 40) {
            fazlaUcret = ((this.workHours - 40) * 30);
        }
    }


    void raiseSalar() {
        if ((2025 - this.hireYear) < 10) {
            zam = (this.salary * 0.05);
        }
        if ((((2025 - this.hireYear) > 9) && ((2025 - this.hireYear)) < 20)) {
            zam = (this.salary * 0.10);
        }
        if ((2025 - this.hireYear) > 19) {
            zam = (this.salary * 0.15);
        }
    }

    void ekranCıktı() {
        System.out.println(" Adı : " + this.name);
        System.out.println(" Maaşı : " + this.salary);
        System.out.println(" Haftalık Çalışma Saati : " + this.workHours);
        System.out.println(" İşe giriş Tarihi : " + this.hireYear);
        System.out.println(" Vergi  : " + vergi);
        System.out.println(" Bonus (Fazla Mesai) : " + fazlaUcret);
        System.out.println(" Maaş Artışı (zam) : " + zam);
        System.out.println(" Vergi ve Bonuslar ile birlikte maaş : " + ((fazlaUcret + this.salary) - vergi));
        System.out.println(" Toplam Maaş : " + ((fazlaUcret + this.salary + zam) - vergi));

    }
}



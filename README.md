
import java.util.*;

public class Car {

     Attributes{color,
     fuelCapacity,electric,automatic,voicecommand,AC,numberOfDoor}
    private String CarName;
    private String Color;
    private int fuelCapacity;
    private boolean isElectric;
    private boolean isAutomatic;
    private boolean hasVoiceCommand;
    private int numberOfDoors;
    private boolean hasAC;
    private Door leftDoor;
    private Door rightDoor;

    public static int NUMBER_OF_CARS = 0;

     
    public Car() {
        NUMBER_OF_CARS++;
    }

    // Const. with parameters 
    public Car(String name, String color, int capacity, int doors) {
        this.CarName = name;
        this.Color = color;
        this.fuelCapacity = capacity;
        this.numberOfDoors = doors;
        NUMBER_OF_CARS++;
    }

     //eg Car mycar = new Car("Red",50,2,true);
    public Car(String name, String color, int capacity, int doors, boolean electic) {
        this.CarName = name;
        this.Color = color;
        this.fuelCapacity = capacity;
        this.numberOfDoors = doors;
        this.isElectric = electic;
        NUMBER_OF_CARS++;
    }

    public Car(String name, String color, int capacity, boolean electic, boolean automatic, boolean voiceCommand,
            int doors, boolean hasAC) {
        this.CarName = name;
        this.Color = color;
        this.fuelCapacity = capacity;
        this.numberOfDoors = doors;
        this.isElectric = electic;
        this.isAutomatic = automatic;
        this.hasVoiceCommand = voiceCommand;
        this.hasAC = hasAC;
        NUMBER_OF_CARS++;
    }

   

    public void setCarName(String _name) {
        this.Color = _name;
    }

    public String getCarName() {
        return this.CarName;
    }

    public void setColor(String _color) {
        this.Color = _color;
    }

    public String getColor() {
        return this.Color;
    }

    public void setFuelCapacity(int _capacity) {
        this.fuelCapacity = _capacity;
    }

    public int getFuelCapacity() {
        return this.fuelCapacity;
    }

    public void setisAutomatic(boolean _automatic) {
        this.isAutomatic = _automatic;
    }

    public boolean getisAutomatic() {
        return this.isAutomatic;
    }

    // Functions

    // 1. Return all manual cars
    public static List<Car> getAllManualCar(Car[] inputCars) {

        List<Car> manualCars = new ArrayList<>();

        for (int i = 0; i < inputCars.length; i++) {

            if (!inputCars[i].isAutomatic) {
                manualCars.add(inputCars[i]);
            }
        }
        return manualCars;
    }

    public void driveCar() {
        System.out.println(this.CarName + " has started driving");
    }

}














public class Human {
   
    private String Name;
    private int Age;
    private String DOB;

    
    public Human() {

    }

    public Human(String name, int age, String dob) {
        Name = name;
        Age = age;
        DOB = dob;
    }



    public void setName(String _name) {
        Name = _name;
    }

    public String getName() {
        return Name;
    }
    

    public void sayYourName() {
        System.out.println("I am " + Name);
    }

    public void eat(String food) {
        System.out.println(Name + " is eating " + food);
    }

    public void sing(String _songName) {
        System.out.println(Name + " sings " + _songName);
    }
}












import java.util.*;

public class APPLE {

    public static void main(String[] args) throws InterruptedException {

        Human sulaiman = new Human("sulaiman", 24, "01/06/1996");
        Human Tim= new Human("Tim", 20, "01/08/1990");
        Human zainab = new Human("zainab", 10, "01/06/1999");
        Human Kell= new Human("Kell", 11, "01/03/1999");

        sulaiman.eat("Rice");
      

        Tim.sing("Hello");
        

        Human[] humans = { sulaiman, Tim, zainab, Kell};

        for (int i = 0; i < humans.length; i++) {
            System.out.println(humans[i].getName());
        }

         data type, variable name
         Car firstCar = new Car("move", 50, 3, true);
         Car firstCar = new Car();
         firstCar.setCarName("Altima");
          firstCar.setColor("black");
         firstCar.setFuelCapacity(70);
         firstCar.setisAutomatic(true);

         Car secondCar = new Car("Second Car", "Yelow", 60, false, false, true, 2,
         true);
         Car thirdCar = new Car("Third Car", "Red", 50, true, true, true, 4, true);
         Car fourthCar = new Car("Fourth Car", "Pink", 100, true, false, true, 4,
         true);
         Car fifthCar = new Car("Fifth Car", "Green", 40, false, false, true, 2,
        true);

         fourthCar.setColor("Dark blue");
         Car[] carArray = { firstCar, secondCar, thirdCar, fourthCar, fifthCar };

         secondCar.driveCar();

         Thread.sleep(8000);

         thirdCar.driveCar();

         List<Car> ourManualCars = Car.getAllManualCar(carArray);

         for (int j = 0; j < ourManualCars.size(); j++) {
         System.out.println(ourManualCars.get(j).getCarName());
         System.out.println(ourManualCars.get(j).getColor());
         System.out.println(ourManualCars.get(j).getFuelCapacity());
         System.out.println(ourManualCars.get(j).getisAutomatic());
         System.out.println("\n");
         }

         System.out.println(Car.NUMBER_OF_CARS);

         
         firstCar.setColor("grey");
         firstCar.setFuelCapacity(89);

         int capacity = firstCar.getFuelCapacity();
         String color = firstCar.getColor();

         System.out.println(" The Color of the car is: " + color);
         System.out.println(" It Fuel capacity is: " + capacity);

    }
}

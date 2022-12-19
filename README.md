# Assignment-4-

<html>
    <head>

    </head>
    <body>
    <div class="container">
        <div id="name_Input">
            <Label>Name:</Label>
            <input type="text" placeholder="Name" class="input">
        </div>
        <div id="Id_num_Input">
            <Label>ID Number:</Label>
            <input type="text" placeholder="ID Number" class="input">
        </div>
        <div id="Shift_num_Input">
            <Label>Shift Number:</Label>
            <input type="text" placeholder="Shift Number" class="input">
        </div>
        <div id="Hourly_rate_Input">
            <Label>Hourly Pay:</Label>
            <input type="text" placeholder="Hourly Pay" class="input">
        </div>
        <button id="btn" type="button" onclick="doInputOutput()">Submit</button>
    </div>
    <br/>
    <br/>
    <br/>
    <div class="container">
        <div id="name">
            <Label>Name:</Label>
        </div>
        <div id="Id_num">
            <Label>ID Number:</Label>
        </div>
        <div id="Shift_num">
            <Label>Shift Number:</Label>
        </div>
        <div id="Hourly_rate">
            <Label>Hourly Pay:</Label>
        </div>
    </div>
    </body>
     <!--test class--> 
    <script>
class Employee {
    constructor(name,Id_num) {
        this.name = name;
        this.Id_num = Id_num;
    }
    get_Id_num() {
        return this.Id_num
    }
    get_Emp_name() {
        return this.name
    }
}
/*write a class named “ProudctionWorker” that is a subclass of the “Employee” class.  
The “ProductionWorker” class will keep data for the following information:
1. Shift number (an integer)
2. Hourly Pay Rate*/
class productionWorker extends Employee{
    constructor(name,Id_num,Shift_num,Hourly_rate) {
        super(name,Id_num);
        this.Shift_num = Shift_num;
        this.Hourly_rate = Hourly_rate;
    }
    get_Shift_num() {
        return this.Shift_num
    }
    get_Hourly_rate() {
        return this.Hourly_rate
    }
}
//const Jeff = new Employee("Jeff", "3023");
const Jefff = new productionWorker("Jeff", "3023",3,5);

console.log(Jefff.name)
console.log(Jefff.Id_num)
console.log(Jefff.Shift_num)
console.log(Jefff.Hourly_rate)
function doInputOutput(name,Id_num,Shift_num,Hourly_rate) {
document.getElementById("name").innerHTML = Jefff.get_Emp_name()
document.getElementById("Id_num").innerHTML = Jefff.get_Id_num()
document.getElementById("Shift_num").innerHTML = Jefff.get_Shift_num()
document.getElementById("Hourly_rate").innerHTML = Jefff.get_Hourly_rate()
}
    </script>
</html>

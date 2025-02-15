# Unit 2 Exercise

## Exercise 1
### 01_Renta.CPP

### DESCRIPTION


<pre>The tax brackets for the income statement in a given country are the following:

Income tax rate
Less than $10,000 5%
Between $10,000 and $20,000 15%
Between $20,000 and $35,000 20%
Between $35,000 and $60,000 30%
More than $60,000 45%

Write a program that asks the user for their annual income and displays by
display the corresponding tax rate.
</pre>


### PROGRAM

```C++

    #include <iostream>

    using namespace std;

    int main(){
        int rentaCasa;
        float impuestoCasa;
        float impuestoCasaTotal;
        float montoCasas;
        float montoCasasTotal;

        //ask for rental price
        cout << "Enter the rent of your house";
        cin >> rentaCasa;

        //line break
        cout << "\n";

            // house rent to know percentage
            if (rentaCasa >0 && rentaCasa <= 10000 )
                impuestoCasa = 0.05;
            else if (rentaCasa>=10000 && rentaCasa <= 20000 )
                impuestoCasa = 0.15;
            else if (rentaCasa>=20000 && rentaCasa <= 35000 )
                impuestoCasa = 0.20;
            else if (rentaCasa>=35000 && rentaCasa <= 60000 )
                impuestoCasa = 0.30;
            else if (rentaCasa > 60000 )
                impuestoCasa = 0.45;


        //house tax in percent
        impuestoCasaTotal=impuestoCasa*100;
        cout << "The tax is from" << impuestoCasaTotal << "% \n" << endl;
        //amount of percentage envaced to rent
        montoCasas=(rentaCasa*impuestoCasa);
        cout << "Rent amount with percentage: $" << montoCasas << "\n" << endl;
        // rent plus percentage 
        montoCasasTotal=(montoCasas+rentaCasa);
        cout << "Rent amount with percentage: $" << montoCasasTotal << "\n" << endl;
    }
```

### EXPlANATION

<pre>
What this program does is first request the rent of a house after evaluating in what
range is the price given by the user and thus with some nested ifs to be able to determine
What will be their respective percentage?

As a result, it gives the rent, percentage, percentage of the rent and sum of the rent and the percentage of rent.
</pre>

### TESTS

#### Entry with $7000
![7000](/imagenes/7000.png "imagen de 7000")

#### Entry with $15000
![15000](/imagenes/15000.png "imagen de 15000")

#### Entry with $25000
![25000](/imagenes/25000.png "imagen de 25000")

#### Entry with $45000
![45000](/imagenes/45000.png "imagen de 45000")

#### Entry with $65000
![65000](/imagenes/65000.png "imagen de 65000")


<br>
<br>
<br>

## Exercise 2
### 02_Benefios.CPP

### DESCRIPTION

<pre>In a certain company, its employees are evaluated at the end of each year.
The points that can be obtained in the evaluation start at 0.0 and can go up,
translating into better benefits. The points you can get
employees can be 0.0, 0.4, 0.6 or more, but not intermediate values
between the figures mentioned. Below is a table with the
levels corresponding to each score. The amount of money earned
on each level is $2,400 multiplied by the level score.

Level Score
Unacceptable 0.0
Acceptable 0.4
Merit 0.6 or more
Write a program that reads the user's score and indicates their level of performance,
as well as the amount of money the user will receive.
</pre>

### PROGRAM


```C++
    #include <iostream>

using namespace std;

int main()
{

  double puntuacion;
  float pago;
  double beneficio;

  pago = 2400;

  // preguntar por la puntuacion
  cout << "Enter your score obtained 0.0,0.4 or 0.6 or more ";
  cin >> puntuacion;

  // salto de linea
  cout << "\n";

  // validates user values ​​and determines
  if (puntuacion == 0.0)
  {
    cout << "The score is unacceptable" << endl;
  }
  else if (puntuacion == 0.4)
  {
    cout << "The score is acceptable" << endl;
  }
  else if (puntuacion >= 0.6 && puntuacion <= 1)
  {
    cout << "The score is Merit" << endl;
  }

  // line break
  cout << "\n";

  // makes payment score
  if ((puntuacion == 0.0) || (puntuacion == 0.4) || (puntuacion >= 0.6))
  {
    beneficio = pago * puntuacion;
    cout << "The amount you will receive is: $" << beneficio << endl;
  }

  // Exercise: use the different comparisons ==, !=, <, >, <=, >=

  // line break
  cout << "\n";

  return 0;
}
```
### EXPLANATION

<pre>Receiving a bonus for the work done depending on the percentage obtained, which are 0.0, 0.4 and 0.6 up to 1 and 
the money is 2400 and the money will be collected according to the bonus</pre>

### TESTS

#### Entry with 0.0
![0](/imagenes/0.0.png "image of 0.0")
#### Entry with 0.4
![6](/imagenes/0.4.png "image of 0.0")
#### Entry with 0.6 to 1
![8](/imagenes/0.8.png "image of 0.8")



## Exercise 3
### 02_Edades.CPP

### DESCRIPTION

<pre>
Exercise 3. Write a program for a company that has game rooms for all ages and wants to automatically calculate the price to charge its customers to enter. 
The program must ask the user for the customer's age and display the price of the ticket. 
Yes the client is under 4 years old can enter for free
if they are between 4 and 18 years old they must pay $5 
if they are over 18 years old, $10.
</pre>

### PROGRAM
```C++
#include <iostream>

using namespace std;

int main(){

    int age;
    
    //ask about age 
    cout << "how old are you ?";
    cin >> age;

    //salto de linea
    cout << "\n";

  // valid the number ang give a result
  if (age <= 3){
    cout << "Your ticket is free " << endl;
   }   
   else if (age >= 4 && age <=18  ){
    cout << "Your ticket is 5 pesos" << endl;
   }
    else if (age >= 19 ){
    cout << "Your ticket is 10 pesos" << endl;
   }
    // line break
    cout << "\n";
    
    return 0;
}
```
### EXPLANATION

<pre>
what this program does is that with the variable it does the whole program,
first it asks what the age is, then it puts it in the if and it already validates all the situations that you can do.
In this case it is better than 4 years they enter for free, older than 4 years and under 18 its cost is 5 pesos and over 18 the entrance is 10 pesos
</pre>

### TESTS

#### Entry with less 4
![3](/imagenes/3.png "image of 3")
#### Entry between 4 and 18
![12](/imagenes/12.png "image of 12")
#### Entry with vegetarian pizza with 
![20](/imagenes/20.png "image of 20")


## Exercise 4
### 02_Pizeria.CPP

### DESCRIPTION

<pre>
Exercise 4. The Bella Napoli pizzeria offers vegetarian and non-vegetarian pizzas to its customers. The ingredients for each type of pizza appear below.
- Vegetarian ingredients: Pepper and tofu.
- Non-vegetarian ingredients: Pepperoni, Ham and Salmon.
Write a program that asks the user if he wants a vegetarian pizza or not
based on his answer shows him a menu with the ingredients available for him to choose from.
You can only choose one ingredient besides the mozzarella and tomato that are in all the pizzas.
At the end it should be shown on the screen if the chosen pizza is vegetarian or not and all the
ingredients it contains.
</pre>

### PROGRAM
```C++
#include <iostream>

using namespace std;

int main()
{

    int typePizza;
    int ingredientVegetal;
    int ingredientNoVegetal;

    cout << "MENU" << endl;
    // salto de linea
    cout << "\n";

    cout << "Vegetarian ingredients: Pepper and tofu." << endl;
    cout << "Non-vegetarian ingredients: Pepperoni, Ham and Salmon." << endl;

    cout << "\n";

    // ask about Pizza
    cout << "Do you want vegetarian pizza?" << endl;
    cout << "1.- vegetarian pizza " << endl;
    cout << "2.- No vegetarian pizza " << endl;

    cout << "\n";
    //keep the variable in typepizza
    cout << "select the type of pizza" << endl;
    cin >> typePizza;

    // line break
    cout << "\n";

    cout << "Note choose only one ingredient" << endl;
    
    // salto de linea
    cout << "\n";

    //validate variable if 1 or 2
    if (typePizza == 1)
    {
        cout << "Vegetarian ingredients: Pepper and tofu." << endl;
        cout << "3.-Pepper" << endl;
        cout << "4.-tofu" << endl;
        cin >> ingredientVegetal;
    }
    else if (typePizza == 2)
    {
        cout << "Non-vegetarian ingredients: Pepperoni, Ham and Salmon." << endl;
        cout << "5.-Peperoni" << endl;
        cout << "6.-Ham and Salmon" << endl;
        cin >> ingredientNoVegetal;
    }
    else
    {
        cout << "ERROR" << endl;
    }
    //line break
    cout << "\n";

    // validate variable if 3 or 4
    if (ingredientVegetal == 3)
    {
        cout << "Your pizza is vegetarian with Mozzarella, Tomato and Peper" << endl;
    }
    else if (ingredientVegetal == 4)
    {
        cout << "Your pizza is vegetarian with Mozzarella, Tomato and Tofu" << endl;
    }
    
    // validate variable if 5 or 6
    if (ingredientNoVegetal == 5)
    {
        cout << "Your pizza is non-vegetarian Mozzarella, Tomato with pepperoni" << endl;
    }
    else if (ingredientNoVegetal == 6)
    {
        cout << "Your pizza is not vegetarian Mozzarella, Tomato with Ham and Salmon" << endl;
    }
    cout << "\n";

    return 0;
}

```
### EXPLANATION

<pre>
First declare 3 variables one to see if you want a vegetarian pizza or not, and the other 2 is to know what to choose from that they want the pizza
1 is to choose vegetarian pizza
2 is to choose non-vegetarian pizza
3 is for the Pepper ingredient
4 is for the Tofu ingredient
5 is for the Pepperoni ingredient
6 is for the Ham and Salmon ingredient
These numbers are for validation in each of the if to know what it is to know what the user wants
</pre>

### TESTS

#### Entry with vegetarian pizza with Peper
![Tofu](/imagenes/pepepepeep.png "image of tofu")
#### Entry with vegetarian pizza with Tofu
![Tofu](/imagenes/Tofu.png "image of tofu")
#### Entry with NO vegetarian pizza with Pepperoni 
![pepperoni](/imagenes/pepperoni.png "image of pepperoni")
#### Entry with NO vegetarian pizza with Ham and Salmon
![Ham and Salmon](/imagenes/Ham.png "image of Ham")


## Exercise 5
### 05_Averge.CPP

### DESCRIPTION


<pre>
Make a program in which you enter 6 temperatures and determine the average. 
The lowest and the highest,and the highest.</pre>


### PROGRAM

```C++
#include<iostream>

using namespace std;

int main()
{
    int contador = 1;
    float temperatura;
    float tempAcum = 0;
    float temMax = 0;
    float temMin = 9999;
    do
    {
        //Ask for the temperature
        cout << "give me the temperature: ";
        //keep the valor of temperature
        cin >> temperatura;
        //save the value 
        tempAcum += temperatura;
        //count down 
        contador ++;

        if (temperatura <= temMin )
            temMin = temperatura;
        if (temperatura >= temMax )
            temMax = temperatura;
    } while (contador <= 6);

    cout << "\n";
    cout << "Today's average temperature is: " << tempAcum/6 << endl;
    cout << "\n";
    cout << "The avergange of temperature maximum today is : " << temMax << endl;
    cout << "\n";
    cout << "The avergange of temperature minimal today is : " << temMin << endl;
    cout << "\n";
return 0;
    
}
```

### EXPlANATION

<pre>
we first realized that this work had to be done with a do while.
we declare a counter variable for the counter
temperature to save user temperature
Tempacum to accumulate temperatures
temMax for maximum temperature
temMin for minimum temperature
Enter the temperature to cycle for 6 times
It saves it in the accumulator and this accumulator validates it with maximum temperature and equals it to 0 and minimum temperature and equals it to 9999 to determine which temperature is higher or lower
</pre>

### TESTS
#### Temperature program example
![Temp](/imagenes/tem.png "example")

<br>
<br>
<br>

## Exercise 6
### 06_factura.CPP

### DESCRIPTION

<pre>
Make a program that reads indefinitely quantities of products and their price
At the end indicate the total of the invoice.
To know that the purchase has been completed, you must
enter a 0 in the amount.
</pre>

### PROGRAM
```C++

#include<iostream>

using namespace std;

int main()
{
    //we declare the variables
    int contador = 1;
    float cantidadVendida;
    float precioArticulo;
    float factura;
    float facAcum = 0;

    do
    {
        //we ask how many products you sold
        cout << "Enter the amount sold = ";
        cin >> cantidadVendida;
        //we ask how much the product costs
        cout << "Enter the price of the item = ";
        cin >> precioArticulo;

        //does the multiplication of product by price
        facAcum =  cantidadVendida* precioArticulo;
        //each operation that the facAcum is doing is saved and so on until it puts a zero but this is with all the products
        factura = facAcum + factura ;
        contador ++;

    } while ( cantidadVendida != 0 );

    cout << "\n";
    cout << "INVOICE" << endl;
    cout << "\n";
    cout << "Total of the invoice $ " << factura << endl;
    cout << "\n";
return 0;   
}
```
### EXPLANATION

<pre>
The user is first asked how many products they have
then, what is the price of those products
It will multiply and save doing this a cycle
until the user puts zero items this cycle closes
and at the end of gives the sum of all products.
</pre>

### TESTS

#### Invoice example
![invoice example](/imagenes/factura.png "image of invoice example")

<br>
<br>
<br>

## Exercise 7
### 07_Decimalabinario.CPP

### DESCRIPTION

<pre>
Write a program that converts decimal numbers to binary.
</pre>

### PROGRAM
```C++

#include <iostream>

using namespace std;

int main()
{
    int number;
    string result;

    cout << "Entry a number decimal ";
    cin >> number;
    do
    {
        if (number > 0)
        {
            while (number != 0)
            {
                // if en una linea con un else
                //The number divided by 2 and the remainder is the one that is going to be put with a cout a "0", "1" and so on until the number is no longer divisible
                result = (number % 2 == 0) ? "0" + result : "1" + result;

                number /= 2;
            }
        }
        else if (number == 0)
        {
            cout << "Mayor a cero";
        }

        // salto de linea
        cout << "\n";
    } while (number < 0);

    cout << "The number in binary is: " << result << endl;

    // salto de linea
    cout << "\n";

    return 0;
}
```
### EXPLANATION

<pre>
The program divides the decimal number by 2 until the number is decomposed
with two do while loops that these determine their end
</pre>

### TESTS

#### Example with number 50
![number example](/imagenes/numero.png "example")

<br>
<br>
<br>


## Exercise 8
### 08_TablaMultiplicar.CPP

### DESCRIPTION

<pre>
Ask what number you want to multiply and by how many times you want to multiply 
it with this form a table.    
</pre>

### PROGRAM
```C++
#include <iostream>

using namespace std;

int main()
{

    int contador, i;
    float numMult, multiplicacion, contador2;

    // first it asks what number you want to multiply and saves it in the variable numMult
    cout << "What number do you want to multiply : ";
    cin >> numMult;
    // salto de linea
    cout << "\n";
    // Then they ask how many times you want to multiply that number and save it in the variable counter 2
    cout << "Up to what number do you want to multiply it: ";
    cin >> contador2;

    cout << "\n";
    cout << "\n";
    // this is for is for the accountant
    for (contador = 1; contador <= contador2; contador++)
    {
        // this line does all the multiplication of each of the numbers and saves them in multiplication
        multiplicacion = contador * numMult;

        // this line is to do the construction of the table and make jumps in each step of the block
        cout << "|";
        for (i = 1, i = 0; i < 47; i++)
        {
            cout << "-";
        }
        cout << "|";
        cout << "\n";
        // this line does the printing of the table so that it is not out of date
        cout << "|"
             << "\t" << contador << "\t"
             << "x"
             << "\t" << numMult << "\t"
             << "="
             << "\t" << multiplicacion << "\t"
             << "|" << endl;
    }
    // FOR to close the table
    for (i = 1, i = 0; i < 49; i++)
    {
        cout << "-";
    }
    cout << "\n";
    cout << "\n";

    // Wait for the user to press a key to end the program
    cout << "Presiona enter para terminar.";
    int c = getchar();

    // Being a function, it must return a value, in this case 0
    return 0;
}
```
### EXPLANATION

<pre>
What this program does is that it makes a multiplication table based on the numbers that the user wants and the times he wants to multiply them
</pre>

### TESTS

#### Example of multiplication with 5 to 12
![multi](/imagenes/multi.png "example")

<br>
<br>
<br>

## Exercise 9
### 09_Biseccion.CPP

### DESCRIPTION

<pre>
Ask what number you want to multiply and by how many times you want to multiply 
it with this form a table.    
</pre>

### PROGRAM
```C++
#include <iostream>
#include <cmath>
#include <iomanip>

using namespace std;

double solveEquation(float worth)
{
    return pow(worth, 2) - worth - 12;
}
int main()
{
    double a;
    double b;
    double c = (a + b) / 2;
    double ya = solveEquation(a);
    double yb = solveEquation(b);
    double yc = solveEquation(c);
    float error = 0.01;
    float noRoot = 0;

    cout << "Enter the value of (a): ";
    cin >> a;
    cout << endl;
    cout << "Enter the value of (b): ";
    cin >> b;
    cout << endl;
        cout << "\t" << "a" << "\t"
        << "\t" << "b" << "\t"
        << "\t" << "c" << "\t"
        << "\t" << "ya" << "\t"
        << "\t" << "yb" << "\t"
        << "\t" << "yc" << "\t" << endl;
    cout << "________________________________________________________________________________________________" << endl;
    cout << endl;

    do
    {
        c = (a + b) / 2;
        ya = solveEquation(a);
        yb = solveEquation(b);
        yc = solveEquation(c);
        if (ya * yc < 0)
        {
            b = c;
        }
        else if (yc * yb < 0)
        {
            a = c;
        }
        else
        {
            noRoot = 1;
        }
        if (noRoot == 0)
        {
            cout << fixed;
            cout << setprecision(3) << "\t" << a << "\t"
            << "\t" << b << "\t"
            << "\t" << c << "\t"
            << "\t" << ya << "\t"
            << "\t" << yb << "\t"
            << "\t" << yc << "\t" << endl;
        }
        else
        {
            cout << "\t" << "No root."
            << "\t" << "No root."
            << "\t" << "No root."
            << "\t" << "No root."
            << "\t" << "No root."
            << "\t" << "No root." << endl;
        }
        
    } while ((abs(yc) >= error) && (noRoot != 1));

    cout << endl;

    return 0;
}
```
### EXPLANATION

<pre>

The program uses 8 variables:

solverEquation: declared as double to save a math operation.
worth: is declared for the number of the mathematical operation.
a: saves the first number to enter whose root you want to know.
b: save the second number to enter whose root you want to know.
c: saves the result of the operation performed.
ya: saves the result of the operation performed with the first number entered by the user.
yb: saves the result of the operation performed with the second number entered by the user.
yc: saves the final result that determines if there is a root and what it is.
error: determines when the program stops.\
noRoot: determine if there is no root.
</pre>

### TESTS


1.![multi](/imagenes/1_10.png "example")

2.![multi](/imagenes/2-3.png "example")

<br>
<br>
<br>
# Zoo Management System
______________________________________________________________________
# Overview:
The Zoo Management System is a Java application designed to manage a virtual zoo. This
system allows administrators to add, modify, and remove attractions, set up visitor discounts,
manage visitor information, and purchase tickets for zoo attractions. It also includes features like
special deals and membership options that visitors can use while buying tickets.
______________________________________________________________________
# Project Structure:
The project consists of the following key classes and interfaces:
1. `Admin` - The `Admin` class manages administrative functions such as adding,
modifying, and removing zoo attractions, setting up visitor discounts, and managing special
deal.
2. `Visitor` - The `Visitor` class represents a visitor to the zoo and stores information about them,
including their name, age, phone number, balance, email, and password.
3. `Attractions` - The `Attractions` class is part of the Zoo's structure, storing information about
each attraction, such as the attraction name, description, status, price, and visitor count.
4. `Zoo` - The `Zoo` class represents the overall zoo and contains the data related to
attractions.
5. `Membership` - The `Membership` class manages visitor memberships and allows visitors to
purchase memberships with or without applying discounts.
6.`Main` - The `Main` class serves as the entry point for the program and contains the main
method that initializes the system and manages user interaction.
______________________________________________________________________
# Functionality:
Administrative Functions
1.`Add Attraction`: Administrators can add new attractions to the zoo by providing a name,
description, and initial status (usually set as "closed").
2.`Modify Attraction`: Attractions can be modified by specifying the attraction's member ID and
providing updated information.
3.`Remove Attraction`: Attractions can be removed from the zoo by specifying the attraction ID.
4.`Set Discounts`: Administrators can set up discounts for visitors based on categories like
"SENIOR" and "MINOR."
5.`Modify Discounts`: Discounts can be modified by specifying the discount code and updating
the discount percentage.
6.`Remove Discounts`: Discounts can be removed by specifying the discount code.
7.`Set Special Deals`: Special deals can be set for visitors based on the number of tickets they
purchase.
8.`Modify Special Deals`: Special deals can be modified by specifying the number of tickets and
updating the discount percentage.
9.`Remove Special Deals`: Special deals can be removed by specifying the number of tickets.
______________________________________________________________________
# Assumptions for ADMIN part:
1. There is only 1 valid username and password for admin i.e admin, admin123
2. There are respective ID’s for each animal, deals, discounts, visitor, attractions
3. All the details for the attractions like name, description, price, setting status have to be
entered by the admin.
4. When adding the animals, the type has to be correctly typed in as “reptiles”, “amphibians”,
“mammals”, otherwise the animal will not be added.
5. When modifying the animal, all the details like name, description, sound have to be entered
again.
6. In order to modify the status of the event you have to use the schedule event option.
7. In order to make the segregation of discounts easier, they only be of 2 types MINOR or
SENIOR
8. Special deals take only 2 things into input, number of attractions and the percentage discount
on them.
9. Visitor stats will show the total revenue, total visitors, most popular attractions.
10. The event is said to be open if schedule is true, and closed if false.
11. By default all attractions are taken to be closed, the admin can schedule an event and
change the status of the attraction to open.
12.Attractions can be opened by admin.
13. While modification of a deal, if it is not yet present, it is created by the admin.
14.Open events are considered as attractions.
15. For logical considerations, it is assumed that the visitor balance is minimum 300
16. While scheduling event, I am displaying the different attributes of one attraction, ignore if
difficulty in interpreting
17.Animal type can’t be modified once declared.
18.Status entered while scheduling of an event can be open/ closed.
19.While modification of special deal if there is no deal set corresponding to the no of tickets
then it is added.
20.Admin can’t remove an animal if the total no of animals are less than 6.
21.In modify discount method, only the discount percentage can be updated.
22.If none of the attractions have been visited currently, and if the admin tries to print the most popular attraction in the visitor stats, the output will be “all equal currently” which is the value that must be present i.e 0 for all.
23.`One email ID` is assumed to be present for a single visitor
24.Important - - !!
It is assumed that after displaying the entire menu, the user enters the correct input ( i.e. 1 or 2 )
and not some arbitrary value such as string as input.
______________________________________________________
# Assumptions for the visitor part:
1.If the visitor doesn’t have membership, it would take him/ her to the visitor menu again where
the user can buy membership .
2. The user can only view the animals and attractions if they have not purchased the
membership, they also cannot purchase any tickets.
3. If the member has purchased the basic membership, they cannot purchase it again, if they
have purchased the premium membership they cannot purchase both the memberships again.
4. An option to apply discount coupons has also been provided, the user has to answer in.
Yes/No if they have to use discounts, they have to enter the ID of the discount code displayed
above.
5. The users have to first enter the ID of the animal only then they will be either allowed to feed or read about the animal.
6. Premium members don’t have to buy tickets.
7. Basic members can choose if they want to use some special deal, if they want to, they enter
the number of attractions.
8. Similarly for discounts, however every time they will be allowed to purchase 1 ticket only, if
they decide to use the discounts, their age will be checked with the age given in the discount.
9. When the user decides to visit the attractions they will be shown the attractions for which they have purchased the tickets, they will have to enter the ID of that attractions, the corresponding descriptions of the attractions will be given and the ticket will be removed from the user.
10.In the given assignment instructions, there was no option to renew the balance of the user
hence no provision for that has been made.
11.Visitor can visit the animals of the zoo without a ticket.
12.Attractions can be visited only after buying a membership.
13.Visitors must register before purchasing memberships or tickets.
14.Discounts can be modified by administrators.
15.If the visitor is buying the membership, it is assumed that the visitor would enter the correct
discount coupon code, another method for eligibility of coupon code has been made, but not
implement for “buy membership option”.
16.If a visitor doesn’t have tickets he/she can’t visit the attractions.
17.Important - - !!
It is assumed that after displaying the entire menu, the user enters the correct input ( i.e. 1 or 2
or 3 ) and not some arbitrary value such as string as input
______________________________________________________________________
# Extra Considerations Used:
1.6 objects of the animal class(declared type) with different subclasses as the actual data type
have been added. These are hardcoded at the start.
______________________________________________________________________
OOPS Concepts used:
1. `Polymorphism`: Polymorphism is achieved through the use of the Animal superclass. One can
create objects of Mammal, Reptile, and Amphibian classes and use them as Animal objects,
which simplifies code and makes it more flexible.
2. `Inheritance`: Mammals, Amphibians, and Reptiles inherit the Animal class and modify it in
their own way. Inheritance allows to create a new class (e.g., Membership) that inherits
properties and behaviors from an existing class (e.g., Admin).
3. `Interface`: An attraction interface has been made, which contains the various types of
methods that can be implemented in Attraction used in Zootopia.
4. `Abstraction`: The Animal class represents an abstract concept of an animal with properties
like name, sound, description, and type. It provides a blueprint for creating specific animal types
like mammals, reptiles, and amphibians.
5.`Method Overriding`: Each subclass (Mammal, Reptile, Amphibian) overrides the constructor of
the Animal class to provide their own initialization logic. This allows each type of animal to have
its unique properties and behaviors.
6.`Object Comparison `(equals and hashCode): The equals and hashCode methods are
overridden in the Animal class to provide custom logic for comparing and hashing objects of the
class. This allows you to compare and hash Animal objects based on the sound attribute.
7.`Class Hierarchy`: The code uses a class hierarchy where Admin is a standalone class that
interacts with other classes like Visitor and Zoo. This hierarchy models the relationships
between different components of the application.
8.`Access Control`: The class specifies private fields and uses getter and setter methods to
control access to those fields. This demonstrates access control principles and encapsulation.
9.`Object class implementation`:toString method in the Admin class to provide a custom
representation of the object's state. This demonstrates the use of the Object class's toString
method, allowing to present visitor statistics and information about the Admin object in a more
human-readable format.
10.`Encapsulation`: The class encapsulates private fields, including map, discount_map,
visitor_map, discount_code, and special_deals. These fields are accessed and modified through
getter and setter methods, which provides control over data access
____________________________________________________________________
Procedure to run:
All the commands mentioned below should be executed in the terminal within the
HOME_FOLDER unless otherwise specified.
1. *Download Code*: Download the 2022591_YashovardhanSinghal code folder from
Classroom and unzip it.
2. *Clean*: Run mvn clean to clean the project.
3. *Compile*: Run mvn compile to compile the project.
4. *Package*: Run mvn package to package the project.
5. *Run the Application*: Execute java -jar target\A2_2022344-1.0-SNAPSHOT.jar to run the
application. Optionally, you can replace this command with java -jar <path to jar file> Main,
where the jar file is A2_2022344-1.0-SNAPSHOT.jar.
Alternatively:
1. *Navigate to the Target Folder*: Run cd target.
2. *Run the Application*: Execute java -jar A2_2022344-1.0-SNAPSHOT.jar Main to run the
application.


EXTRA CONSIDERATIONS WHILE RUNNING THE CODE
In case of an abrupt new line character, press enter and the extra space should go away, this is
largely machine-dependent,
New line consumption character has been done to avoid this
Extra Extras
PROCEDURE:
Add attraction status
In case of a blank line coming, add an additional enter character so that the code functions
smoothly
The new line character is consumed but there is a possibility that on running it may appear - like
attached in the images above,
Else please re-run, it isn’t one of the potential problems of the code itself
____________________________________________________________________
CONTRIBUTORS:
Palak Bhardwaj (2022344)

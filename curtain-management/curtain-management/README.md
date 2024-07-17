Spring JPA:
Description
Implement the JPQL statement to fetch the list of curtains whose price is greater than the given 
price and the list of curtains whose brand is equal to the given brand name.
The Curtain Model is as follows:
id : the unique id of the curtain (int)
brand : the brand name of the curtain (String)
material : the material used in curtain (String)
color : the color of the curtain (String)
price : the price of the curtain (int)
File in which you need to write the code:
● src/main/java/com/example/curtainmodel/repository/CurtainRepository.java
The task is to write the JPQL statement in the CurtainRepository file under the repository 
folder:
● Task 1: Create a function called "getIdByPrice" that returns a list of curtains with a price 
greater than the given price. You need to use query annotation to execute the function 
based on the GET query.
● Task 2: Create a " getIdByBrand " function that returns the list of curtains with a brand 
equal to the given brand name. You need to use query annotation to execute the 
function based on the GET query

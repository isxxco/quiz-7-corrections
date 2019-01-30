# Quiz 7 corrections

1. I need to keep a list of students who have registered to take AP Computer Science A next year. All I need to store are the students' names. To do this, I've decided to use an array. The maximum enrollment for the course is 50 students.

Which of the following represents a correct declaration and initialization of my ArrayList?

Correct Answers:
ArrayList<String> registeredStudents = new ArrayList<String>(50);
ArrayList<String> registeredStudents = new ArrayList<String>();

Why these answers are correct: The declaration of the first arraylist has the array list, the data type, the name, and the amount of elements that will be in it. The second arraylist declaration has the same parts of the first statement, except the amount of elements. Both are valid because for an arraylist declaration you need ArrayList<datatype> name = newArrayList<datatype>, with or without the number of elements.
  

5.
String[] data = new String[] {
    "New York", "Boston", "Philadelphia", "Washington, D.C.", "Chicago", "Los Angeles"
};
ArrayList<String> cities = new ArrayList<String>();

for (String city : data) {
   cities.add(city);
}
System.out.println(cities.get(1));

Correct Answer: Boston

Why this answer is correct: THe first statement is the declaration and initialization of an arraylist called data. The second statement is the creation of a new arraylist cities. The for loop essentially adds all the elements of the data arraylist to the cities array list. In the last statement, it asks for the 1st index in the arraylist, or the second elemenet (since it is 0 indexed), hence the answer is Boston as it is the second element in the data ArrayList.

6.
Although their behaviors are identical, length is a _______ of an array whereas size is a _________  of the ArrayList class. Syntactically, this difference is shown by either the presence of absence of ________________ .

Correct Answer: property, method, parantheses. 

Why this is correct: Arrays are special objects in java, which have a simple attribute called length and it returns the capacity of the ArrayList. The size method actually provides how many objects are in the arrayList, making it more than an attribute, so it is a method. The length property does not have a parentheses following it, but the size method does (size()). 

7. 
Which method(s) of the ArrayList class is being called in the code segment below?

ArrayList<String> names = new ArrayList<String>();

names.add("Paul");
names.remove(0);

System.out.println("There are " + names.size() + " elements in the ArrayList.");

Correct Answer: the size method, the add method, the remove method  

Why these answers are correct: The add method is called when the ArrayList adds Paul to the end of the ArrayList. The remove method is called when the ArrayList deletes its first element. The size method is called in the printstatement for the amount of objects in the ArrayList.


13.
Consider the following code segment.

ArrayList<Integer> numbers = new ArrayList<Integer>();
System.out.println(numbers.get(0));
What is printed to the console as a result of executing this code?
  
Correct Answer: An IndexOutOfBoundsException will be thrown.

Why this answer is correct: There are no elements added to the ArrayList, so the get method called will not be able to retrieve any values.



15.
Consider the following code segment, which is designed to print only those values in an array that are multiples of 5.

for (int i = 0; i < numbers.size(); i++) {
    if (numbers.get(i) % 5 == 0) {
        System.out.println(numbers.get(i));
    }
}
Which of the following code snippets represents the equivalent behavior? You may assume (in both the question and answer options) that numbers is properly declared and initialized. Select all that apply.

Correct Answers:
for (int number : numbers) {
    if (number % 5 == 0) {
        System.out.println(number);
    }
}

numbers.forEach((number) -> System.out.println(number));

Why these answers are correct: In the first answer choice, the for loop goes through each element in the array, and checks whether each element is divisible by 5, and if it is, it pritns it out.  The second answer uses a for each method, and prints every number that is divisible by 5 beecause number is initialized.


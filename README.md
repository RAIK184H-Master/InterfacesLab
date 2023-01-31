# INSTRUCTIONS
Working in your assigned pairs, perform the following tasks.

## PART 1: SETUP 
1.	Download the code and import the project into Eclipse. 

## PART 2: ANALYZING INTERFACES 
2.	Read the source code for the HolidayAccount class and Driver.

3.	Compile and execute Driver.

4.	ANSWER IN A TEXT FILE IN YOUR REPOSITORY: What output was generated?

5.	Add the following to the end of the main() method in Driver:
```
	// Sort the accounts
	Arrays.sort(accounts);


	// Print the accounts in the sorted order
	for (i=0; i < accounts.length; i++)
	{
	    System.out.println(accounts[i].getAccountID()+"\t"+
			       accounts[i].getHolder());
	}
```
6.	Compile and execute Driver.

7.	ANSWER IN A TEXT FILE IN YOUR REPOSITORY: What error message was generated?

8.	Read the documentation for the `Arrays.sort(java.lang.Object[])` method.

9.	ANSWER IN A TEXT FILE IN YOUR REPOSITORY: What interface must all elements in the Object array implement?

10.	ANSWER IN A TEXT FILE IN YOUR REPOSITORY: Why was the error message from Question 9 generated?

11.	ANSWER IN A TEXT FILE IN YOUR REPOSITORY: Does the HolidayAccount class contain a `compareTo()` method?

12.	ANSWER IN A TEXT FILE IN YOUR REPOSITORY: Given the answer to the previous questions, it seems like this defect can be corrected by declaring that the HolidayAccount class fulfills the promises made in the the Comparable interface. What change do you need to make to accomplish this?

13.	Make this change and compile HolidayAccount.

14.	ANSWER IN A TEXT FILE IN YOUR REPOSITORY: What error message was generated?

15.	ANSWER IN A TEXT FILE IN YOUR REPOSITORY: Why was this error message generated? In other words, why does the HolidayAccount class not actually implement the Comparable interface?

16.	Fix this error by either:
    1. adding a type paramater to the Comparable interface in the class declaration (`implements Comparable<HolidayAccount>`), or
    2. changing the parameter accepted by the `compareTo` method to `Object`, then casting the object to a HolidayAccount inside the function.

17.	ANSWER IN A TEXT FILE IN YOUR REPOSITORY: What does your compareTo method look like now?

18.	Compile and execute Driver.

19.	ANSWER IN A TEXT FILE IN YOUR REPOSITORY: What output was generated?

PART 2: GETTING MORE SOPHISTOCATED 
20.	“Undo” the changes you just made to the class declaration or the `compareTo(HolidayAccount other)` method. 

21.	Add the following method to the HolidayAccount class:
```
	/**
     	  * Compare the account number on this account to the
     		* account number on a given account (required by Comparable)
    		*
     		* @param other The given account
     		* @return -1/1 if this account is before/after the given account
     		*/
   	public int compareTo(Object other){
       		return compareTo(other);       
    	}
```
22.	ANSWER IN A TEXT FILE IN YOUR REPOSITORY: Does this class now implement the Comparable interface?

23.	Compile HolidayAccount.

24.	ANSWER IN A TEXT FILE IN YOUR REPOSITORY: Does HolidayAccount contain any syntax errors?

25.	Compile Driver.

26.	ANSWER IN A TEXT FILE IN YOUR REPOSITORY: Does Driver contain any syntax errors?

27.	Execute Driver.

28.	ANSWER IN A TEXT FILE IN YOUR REPOSITORY: What runtime error message was generated?

29.	ANSWER IN A TEXT FILE IN YOUR REPOSITORY: Why was this error message generated?

30.	Fix this problem by typecasting other in such a way that the compareTo(Object) method calls the appropriate implementation.

31.	ANSWER IN A TEXT FILE IN YOUR REPOSITORY: What change(s) did you make? (copy any relevant code)

32.	Compile HolidayAccount. Compile and execute Driver.

33.	ANSWER IN A TEXT FILE IN YOUR REPOSITORY: What output was generated?

34.	ANSWER IN A TEXT FILE IN YOUR REPOSITORY: Which working implementation of the HolidayAccount class do you prefer, the one with just the compareTo(Object) method, or the one with both a compareTo(HolidayAccount) method and compareTo(Object) method? Why?

COMMIT, PUSH, DONE!

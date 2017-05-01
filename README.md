
![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png)

# Training: JavaScript Data Types

*Use the JavaScript console in your browser to solve the challenges. Press `command + option + J` to open the console in Chrome. Feel free to also record your responses in a file, but make sure you test them in the console!*

### Strings

1. Store your first name in a variable.
2. Concatenate your first name with your last name, and store the result in another variable.
3. Use the `String` <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split" target="_blank">`split`</a> method to turn your string variable from challenge #2 into an array.

### Arrays

1. An array called `foods` holds the names of my top 20 favorite foods, starting with the best food. How can you find my fifth favorite food?

	  <details>
	    <summary>answer</summary>  
	    	` foods[4] `
	  </details>


2. Starting from the existing `friends` variable below, change the element that is currently "Elizabeth" to "Liz".


	  ```js
	  var friends = [
	    "Moe",
	    "Jane",
	    "Emma",
	    "Elizabeth",
	    "Abanov",
	    "Lycia"
	  ];
	  ```

	  <details>
	    <summary>answer</summary>
	    ```js
	    friends[3] = "Liz";
	    ```
	  </details>

3. Using array methods, add your name to the end of the `friends` array, and add another name to beginning.

	  <details>
	    <summary>hint</summary>
	    Look up array methods `push` and `unshift`.
	  </details>

	  <details>
	    <summary>answer</summary>
	    ```js
	    friends.push("Me!");
	    friends.unshift("Someone else!");
	    ```
	  </details>

4. Stretch: We have two lists of friends below. Use array methods to combine them into one alphabetically-sorted list.

	  ```js
	  var myFriends = [
	    "Rickon",
	    "Meera",
	    "Hodor",
	    "Jojen",
	    "Osha",
	    "Rickard",
	    "Maester"
	  ];

	  var yourFriends = [
	    "Bilbo",
	    "Boromir",
	    "Elrond",
	    "Faramir",
	    "Frodo",
	    "Gandalf",
	    "Legolas",
	    "Pippin"
	  ];
	  ```

	  <details>
	    <summary>hint</summary>
	    Look up array methods `concat` and `sort`.
	  </details>

	  <details>
	    <summary>answer</summary>
	    ```js
	    var allFriends = myFriends.concat(yourFriends);
	    allFriends.sort();
	    ```
	  </details>



**Start from the `clubs` variable.**

1. Find and `console.log` the following:  
	* the array that contains all the student club data
	    <details>
	      <summary>answer</summary>
	      `console.log(clubs);`
	    </details>

	* the number of clubs  
	    <details>
	      <summary>answer</summary>
	      `console.log(clubs.length);`
	    </details>


	* the object that contains all of the information for the jazz band
	    <details>
	      <summary>answer</summary>
	      `console.log(clubs[1]);`
	    </details>


	* the teacher of the first club  
	    <details>
	      <summary>answer</summary>
	      ```js
	      console.log(clubs[0]['teacher']); // bracket notation, or
	      console.log(clubs[0].teacher);    // dot notation
	      ```
	    </details>


	* the array of students in the jazz band
	    <details>
	      <summary>answer</summary>
	      ```js
	      console.log(clubs[1]['students']);
	      console.log(clubs[1].students);
	      ```
	    </details>


	* the last name of the second student on the swim team  
	    <details>
	      <summary>answer</summary>
	      ```js
	      console.log(clubs[2]['students'][1]['last']);
	      console.log(clubs[2].students[1].last);
	      ```
	    </details>



1. Create an object literal representing a student with your name, and assign it to a variable.
	  <details>
	    <summary>answer</summary>
	    `var me = { first: 'Bob', last: 'Loblaw' };`
	  </details>



1. Add yourself to one of the clubs as a student member.
	  <details>
	    <summary>answer</summary>
	    ```js
	    // joining the swim team
	    clubs[2]['students'].push(me); // or
	    clubs[2].students.push(me);  
	    ```
	  </details>



1. Create an object literal representing a new club, and assign it to a variable. Make sure it has values for name, students, and teacher.
	  <details>
	    <summary>answer</summary>
	    ```js
	    var lawClub = {
		name: 'Legal Eagles',
		students: [],
		teacher: 'Abby Fuentes'
	    };
	    ```
	  </details>



	* Use an array method to add your new club to the array of clubs.  
	    <details>
	      <summary>answer</summary>
	      ```js
	      clubs.push(lawClub);
	      ```
	    </details>


	* Add yourself as a student in the new club.
	    <details>
	      <summary>answer</summary>
	      ```js
	      clubs[3]['students'].push(me); // or
	      clubs[3].students.push(me);
	      ```
	    </details>



1. Update Samuel Black's first name to Sam everywhere it occurs. Hint: there is not a great shortcut to do this.

	  <details>
	    <summary>answer</summary>
	    ```js
	    clubs[0]['students'][2]['first'] = 'Sam';
	    clubs[2]['students'][1]['first'] = 'Sam';
	    clubs[0].students[2].first = 'Sam';
	    clubs[2].students[1].first = 'Sam';
	    ```
	  </details>



1. Oops, the school is losing extracurricular funding.  Use an array method to remove one of the clubs from the array.
	  <details>
	    <summary>answer</summary>
	    `clubs.shift(); // goodbye yearbook!`
	  </details>

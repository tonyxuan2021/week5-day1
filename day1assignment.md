# Problem1: In 3-4 sentences, please explain what Big O Notation is.

Big O Notation is the measuring tool to analyze the complexity of your code. Big O Notation analyze code using two approaches, which are time complexity and space complexity. Time complexity is the approach of using 5 ranks of O indicator to measure the code run time, inlcuding O(n!), O(n^2), O(n), O(logn), O(1), with O(1) being the most efficient run time, and O(n!) the worst efficent runtime. Space complexity measures the memory sapce used by a code/algorithum, and uses O(1), O(log n), and O(n) to measure the code efficiency according to the memory space used, which are O(1) takes the same amount of space regardless of the input size, and O(log n), with space memory propotional to the log of input size, and O(n), with space memory used proportional to the input size. 

# Problem 2: For each of the time complexities shown below:

Complexity name:
O(1) - constant, code runtime not affect by the input size, example would be add an element to the end of an array
O(logn) - logarithmic, code runtime affected by more input size, the efficient the code run time, example would be a binary search method
O(n) - linear: code runtime is proportional of the input size, example would be a for loop, which loops of each item in an array
O(n^2) - Quadratic: more code input size, the less efficient of the quatratic times \* input size, example would be a 2D array
O(n!) Factorial: worst of worst runtime, run time is the factorial of the input size, which is slow, example would be to get permutation of a string
Rank: constant is the best, and Factorial is the worst

# Problem 3: Name 3 reasons why we care about Big O and we care about code performance.

1. it is essential for developers to know how their code scales based on the input size, especially it is important to use Big O to measure the run time efficiency
2. Better run times means reduced latency when user uses the appliction, which has a direct effect to the company's revenue
3. Better space complexity means the code uses less space of the company's resoureces, which saves cost of the company too from using less computer memory

# Problem 4: What is the problem of using a time method such as performance.now() to measure how “fast” a code runs on our machines.

The problem with performance.now() is that it is not a accurate way to measure the code performance beacause every computer that has different hardware setup will result in run time difference, and even with the same compmuter the runtime is still different every time the code is ran. Big O is a much better and accurate way to measure code runtime at the big picture

# Problem 5: Given the following piece of code:

const someFunction = (arr1) => { 
arr1.push(1).pop() //O(1)
for (let i = 0; i < arr1.length; i++) { //O(n)
    console.log('do something 2')
}
for (let i = 0; i < arr1.length; i++) { //O(n)
    console.log('do something 3')
}
for (let i = 0; i < arr1.length; i++) { //O(n)
    for (let i = 0; i < arr1.length; i++) {
console.log('do something 3') }
} }

# Total time complexity: O(1) + 3*O(n) = O(n)

# Problem 6: Given the following piece of code:
const someFunction1 = (arr1) => {
  let sum = arr1[1] + arr[2]; // O(1)
  while (condition) { // O(n)
    sum = arr[5] + arr[7]; 
  }
  for (let i = 0; i < arr1.length; i++) {
    for (let i = 0; i < arr1.length; i++) {
      for (let i = 0; i < arr1.length; i++) {
        console.log("do something 3"); // O(n^3)
      }
    }
  }
};

# Total time complexity: O(1) + O(n) + O(n^3) = O(n^3)

# Problem 7: Please explain in 3-5 sentences why we can ignore constants and consolidate our time complexities.
We ingore constants and consolidate our time complexities beacuse what Big O measures is the worst case senario of run time of a algorithum. Therefore, if the time complexity is combined with O(1) and O(n^2), the O(1) is way too small, in order word, it is small enough and can be neglected because the effect brought by O(n^2) is much more significant to the whole algorithum. 

# Problem 8: In 2-3 sentences, please explain what space complexity is and why we care.
Space complexity measures the memory sapce used by a code/algorithum, and uses O(1), O(log n), and O(n) to measure the code efficiency according to the memory space used, which are O(1) takes the same amount of space regardless of the input size, and O(log n), with space memory propotional to the log of input size, and O(n), with space memory used proportional to the input size. We care about the space compexity because it directly affect the memory space of the computer the company uses. It means more space used will be equivalent to the cost incurred by the company, think about if you use AWS to host, you will need to pay more for more memory space used. 

# Problem 9: Given the following data TYPES, label what the space complexity is for each one:
- Boolean // O(n)
- Undefined // O(1)
- Null // O(1)
- Numbers // O(n)
- String // O(n)
- Array // O(n)
- Object // O(n)

explaination: since undefined and null will not take only 1 unit of space, they have time complexity of O(1), all other data types will have a time complexity of O(n) because they are proportional based on the input size. 

# Problem 10: Give two reasons when you should use a array and when you should use a object.
we use array when we want to store same data types, and also the order matters
we use object when we want to store more complex data in key/value pairs, the order usually does not matter

# Problem 11: Given the following object methods, label what the TIME complexity is for each one:

const obj = { name: "tony" };
//inserting
obj.age = 44; // O(1)
//removing
delete obj.age; // O(1)
//searching 1
obj.hasOwnProperty["name"]; // O(n)
//searching 2
for (const prop in obj) {
  console.log(obj[prop]); // O(n)
}
//accessing 
obj.age //44 // O(1)
//retrieving keys 
Object.keys(obj); // O(1)
//retrieving values
Object.values(obj); // O(1)

# Problem 12: Given the following array methods, label what the TIME complexity is for each one:

const arr2 = [1, 2, 3, 4, 5, 6, 7]; 
//inserting 1 
arr2.push(8); // O(1)
//inserting 2 
arr2.unshift(0); // O(n)
//removing 1 
arr2.pop(); // O(1)
//removing 2 
arr2.shift(); // O(n)
//searching 1 
const findNumber = arr2.find((num) => num === 2); // O(n)
//searching 2
for (let i = 0; i < arr2.length; i++) {
  if (arr2[i] === 2) {
    return arr2[i]; // O(n)
  }
}
//retrieving
const getNumber = arr2[3]; // O(1)
//method 1
const double = arr2.map((num) => num * 2); // O(n)
//method 2
const removeAndAddNewNumber = arr2.splice(1, 1, 5); // O(n)
//method 3
const getSum = arr2.reduce((total, num) => total + num, 0); // O(n)
//method 4
for (const num of nums) {
  console.log(num * 2); // O(n)
}
//method 5
const convertToString = arr2.join(" "); // O(n)
//method 6
const reversed = arr2.reverse(); // O(n)

# Problem 13: For each one of these code blocks, please identify the time & space complexity and explanation of why it is.

# problem 1
function findFirstIndexOfNumber(number, array) {
  for (let i = 0; i < array.length; i++) {
    if (array[i] === number) {
      return i;
    }
  }
  return -1;
}

# time complexity: O(n), becuase this s a for loop, iterate every item in an array.
# space complexity: O(n), because space used is proportional to its input size

# problem 2
function findEachIndexOfNumber(number, array) {
  let arrayOfIndexes = [];
  array.forEach(function (element, index) { // O(n)
    if (element === number) {
      arrayOfIndexes.push(index); // O(1)
    }
  });
  return arrayOfIndexes; // O(1)
}

# time complexity: O(n), becuase the consolidated time complexity is O(n)
# space complexity: O(n), because space used is proportional to its input size

# problem 3
const array = [36, 14, 1, 7, 21];

function higherOrLower(array) {
  if (array[array.length - 1] > array[0]) { 
    return "Higher"; // O(1)
  } else if (array[array.length - 1] < array[0]) {
    return "Lower"; // O(1)
  } else {
    return "Neither"; // O(1)
  }
}

# time complexity: O(1), becuase the consolidated time complexity is 3*O(n), which is O(1)
# space complexity: O(1), because more data size will not impact the space complexity

# problem 4
const array = [1, 2, 3, 4, 5, 6, 7, 8];
function determineSumOfSequentialArray(array) {
  let sum = 0;
  for (let i = 0; i < array.length; i++) {
    sum += array[i]; // O(n)
  }
  return sum;
}

# time complexity: O(n), becuase this s a for loop, iterate every item in an array.
# space complexity: O(n), because space used is proportional to its input size

# problem 5
const array = [1, 2, 3, 4, 5, 6, 7, 8];
function determineSumOfSequentialArray(array) {
  return (array.length * (array.length + 1)) / 2; // O(1)
}

# time complexity: O(1), becuase the the returning value just a simple math calculation
# space complexity: O(1), because more data size will not impact the space complexity

# problem 6
function searchSortedArray(
  number,
  array,
  beginIndex = 0,
  endIndex = array.length - 1
) {
  let middleIndex = Math.floor((beginIndex + endIndex) / 2); // O(1)
  if (array[middleIndex] === number) {
    return middleIndex; // O(1)
  } else if (beginIndex >= endIndex) {
    return -1; // O(1)
  } else if (array[middleIndex] < number) {
    beginIndex = middleIndex + 1; // O(1)
    return recursiveBinarySearch(number, array, beginIndex, endIndex); // O(n)
  } else if (array[middleIndex] > number) {
    endIndex = middleIndex - 1;
    return recursiveBinarySearch(number, array, beginIndex, endIndex); // O(n)
  }
}

# time complexity: O(n), becuase the consolidated run time is O(n)
# space complexity: O(n), because space used is proportional to its input size

# problem 7
const array1 = [3, 7, 9, 12, 15, 18, 32];
const array2 = [3, 3, 7, 41, 76];
function compareArrays(array1, array2) {
  let arrayOfPairs = [];
  array1.forEach(function (e, i) { 
    array2.forEach(function (e2, i2) {
      if (e === e2) {
        arrayOfPairs.push([i, i2]); // O(n^2)
      }
    });
  });
  return arrayOfPairs; // O(1)
}

# time complexity: O(n^2), becuase 2D array is a O(n^2)
# space complexity: O(n^2), because space used is the n^2

# problem 8
function sortByValue(array) {
  function swap(array, index1, index2) {
    let temporaryValue = array[index1];
    array[index1] = array[index2]; // O(1)
    array[index2] = temporaryValue; // O(1)
  }
  let count = 1;
  while (count < array.length) { // O(n)
    let swapCount = 0;
    for (let i = 0; i < array.length - count; i++) { // O(n)
      if (array[i] > array[i + 1]) { 
        swap(array, i, i + 1); // O(1)
        swapCount++; // O(1)
      }
    }
    count++; // O(1)
  }
  return array;
}

# time complexity: O(n), becuase consolidated time complexity is O(n)
# space complexity: O(n), because space used is proportional to its input size

# problem 9
function returnDupes(array, array2) {
  let dupeArray = [];
  array.forEach(function (element) { 
    if (array2.includes(element)) { 
      dupeArray.push(element); // O(n^2)
    }
  });
  return dupeArray; O(1)
}

# time complexity: O(n^2), because forEach and includes array methods makes this operation a 2D array operation, which has run time of O(n^2)
# space complexity: O(n^2), because space used is the n^2

# problem 10
function sumFilteredData(array) {
  return array
    .filter(function (element) {
      return element > 5 && element < 20; // O(n)
    })
    .reduce(function (valueToAdd, currentValue) {
      return valueToAdd + currentValue; // O(n)
    }, 0);
}

# time complexity: O(n), because consolidated time complexity is O(n), the chain of 2 array method does not make this operation a 2D array.
# space complexity: O(n), because space used is proportional to its input size
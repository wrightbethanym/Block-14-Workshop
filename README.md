# Block-14-Workshop

// Only odds

// Function to filter out only odd numbers from an array
function onlyOdds(numbers) {
    // Initialize an empty array to store odd numbers
    const oddNumbers = [];

    // Loop through each number in the input array
    for (let i = 0; i < numbers.length; i++) {
        // Check if the number is odd
        if (numbers[i] % 2 !== 0) {
            // If it is odd, push it into the new array
            oddNumbers.push(numbers[i]);
        }
    }

    // Return the new array
    return oddNumbers;
}

// Test
console.log(onlyOdds([2, 4, 6, 8, 11, 20, 15, 22]));
console.log(onlyOdds([1, 2, 3, 4, 5, 6, 7, 8, 9, 10]));
console.log(onlyOdds([70, 42, 55, 81, 21, 91, 34]));
console.log(onlyOdds([2, 4, 6, 8, 10, 11, 12]));

// Vowel versus Consonant

// Function to count consonants and vowels in a string
function countConsonantsAndVowels(word) {
    // Initialize variables to keep track of consonant and vowel counts
    let consonantCount = 0;
    let vowelCount = 0;

    // Loop through each character in the input string
    for (let i = 0; i < word.length; i++) {
        // Check if the character is a vowel
        if ('aeiou'.includes(word[i])) {
            // If it is a vowel, increment the vowel count
            vowelCount++;
        } else {
            // If it is not a vowel, increment the consonant count
            consonantCount++;
        }
    }

    // Print the original word and the counts of the consonants and vowels
    console.log(`${word} has ${consonantCount} consonants and ${vowelCount} vowels`);
}

// Test Cases
countConsonantsAndVowels("hello"); //Expected: "hello has 3 consonants and 2 vowels"
countConsonantsAndVowels("ukelele"); //Expected: "ukelele has 3 consonants and 4 vowels"
countConsonantsAndVowels("awesome"); //Expected: "awesome has 3 consonants and 4 vowels"
countConsonantsAndVowels("onomonopia"); //Expected: "onomonopia has 4 consonants and 6 vowels"
countConsonantsAndVowels("textbook"); //Expected: "textbook has 5 consonants and 3 vowels"


//Reverse Array

//Function to reverse an array
function reverseArray(inputArray) {
    //initialize an empty array to store reversed elements
    const reversedArray = [];

    //Use a for loop to iterate over the input array in reverse order
    for (let i = inputArray.length - 1; i >= 0; i--) {
        //Push each element into the new array
        reversedArray.push(inputArray[i]);
    }

    //Return the new array
    return reversedArray;
}

//Testing
console.log(reverseArray([1, 2, 3])); //Expected array: [3, 2, 1]
console.log(reverseArray([1, 3, 5, 7, 9, 11])); // Expected array: [11, 9, 7, 5, 3, 1]
console.log(reverseArray([20, 50, 30, 60, 200]));
console.log(reverseArray([1, -1, 2, -3, 5, -8, 13]));


//Fizz Buzz

//Loop through numbers from 1 to 100
for (let i = 1; i <= 100; i++) {
    //Check if the number is a multiple of both 3 and 5
    if (i % 3 === 0 && i % 5 === 0) {
        console.log("FizzBuzz");
    } else if ( i % 3 === 0) {
        //Check if the number is a multiple of 3
        console.log ("Fizz");
    } else if (i % 5 === 0) {
        //Check if the number is a multiple of 5
        console.log("Buzz");
    } else {
        // If not a multiple of 3 or 5, print the number 
        console.log(i);
    }
}

// Test the functions with example customers
const timmyRefillTotal = calculateRefillTotal(timmy);
const timmyWithSubscription = applySubscriptionDiscount(timmyRefillTotal, timmy.hasSubscription);
const timmyWithCoupon = applyCouponDiscount(timmyWithSubscription, timmy.hasCoupon);
console.log(generateFinalAmountString(timmyWithCoupon)); //Expected "Your grand total is $65.00"

const sarahRefillTotal =calculateRefillTotal(sarah);
const sarahWithSubscription = applySubscriptionDiscount(sarahRefillTotal, sarah.hasSubscription);
const sarahWithCoupon = applyCouponDiscount(sarahWithSubscription, sarah.hasCoupon);
console.log(generateFinalAmountString(sarahWithCoupon)); //Expected: "Your grand total is $37.50"

const rockyRefillTotal = calculateRefillTotal(rocky);
const rockyWithSubscription = applySubscriptionDiscount(rockyRefillTotal, rocky.hasSubscription);
const rockyWithCoupon = applyCouponDiscount(rockyWithSubscription, rocky.hasCoupon);
console.log(generateFinalAmountString(rockyWithCoupon)); //Expected: "Your grand total is $102.50"

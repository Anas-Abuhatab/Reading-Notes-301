# React Docs - lists and keys

* What does .map() return?
a new arr with changes in value we make for each item .

* If I want to loop through an array and display each value in JSX, how do I do that in React?
array.map(item)
* Each list item needs a unique Key.
* What is the purpose of a key?
Keys only make sense in the context of the surrounding array.


# The Spread Operator

What is the spread operator?
The spread operator is a useful and quick syntax for adding items to arrays, combining arrays or objects, and spreading an array out into a functionβs arguments.

List 4 things that the spread operator can do.
1-Copying an array
2-Concatenating or combining arrays
3-Using Math functions
4-Using an array as arguments

Give an example of using the spread operator to combine two arrays.
`const fruits = ['π','π','π','π','π']
const moreFruits = [...fruits];
console.log(moreFruits) // Array(5) [ "π", "π", "π", "π", "π" ]
fruits[0] = 'π'
console.log(...[...fruits,'...',...moreFruits]) //  π π π π π ... π π π π π`


Give an example of using the spread operator to add a new item to an array.

`const fruitStand = ['π','π','π']
const sellFruit = (f1, f2, f3) => { console.log(`Fruits for sale: ${f1}, ${f2}, ${f3}`) }
sellFruit(...fruitStand) // Fruits for sale: π, π, π
fruitStand.pop()
fruitStand.pop()
fruitStand.push('π')
fruitStand.push('π')
sellFruit(...fruitStand) // Fruits for sale: π, π, π
fruitStand.pop()
fruitStand.pop()
sellFruit(...fruitStand,'π') // Fruits for sale: π, π, undefined`

Give an example of using the spread operator to combine two objects into one.

`const objectOne = {hello: "π€ͺ"}
const objectTwo = {world: "π»"}
const objectThree = {...objectOne, ...objectTwo, laugh: "π"}
console.log(objectThree) // Object { hello: "π€ͺ", world: "π»", laugh: "π" }
const objectFour = {...objectOne, ...objectTwo, laugh: () => {console.log("π".repeat(5))}}
objectFour.laugh() // πππππ`
# Algorithm Exploration Activity

## Instructions

The purpose of this activity is to see how each of these algorithms scales as the size of input grows.

There are four separate algorithms implemented below:

1. `appendRandom`
2. `loop`
3. `binarSearch`
4. `nestedLoop`

You will invoke each function multiple times with an increasingly large lists. **You will update this [README.md](http://readme.md/) by replacing the emoji in the last column of each table with the corresponding number of operations that take place with each invocation**. You can make commits to this file directly. We have given you a little help by console logging inside of each function so that all you have to do is **count the number of times, each function console.logs a value**.

Finally, after you have observed the number of operations for each function call, **you will plot them on [this graph](https://www.desmos.com/calculator/rlh5wglbky) to better visualize how they scale.**

**Last but not least, you must answer all 4 essential questions in the README file!**



## 1. Append Random

```
function appendRandom(list) {
    let rand = Math.floor(Math.random() * 100);
    list.push(rand);
    console.log(`New List is ${list}`);
}

```

| Append | Length of Input | # of Operations |
| --- | --- | --- |
| appendRandom([]) | 0 | 😴 |
| appendRandom(['a']) | 1 | 🤔 |
| appendRandom(['a', 'b']) | 2 | 🤔 |
| appendRandom(['a', 'b', 'c', 'd']) | 4 | 🤔 |
| appendRandom(['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h']) | 8 | 🧐 |
| appendRandom(['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p']) | 16 | 😕 |
| appendRandom(['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z', 'za', 'zb', 'zc', 'zd', 'ze', 'zf']) | 32 | 🤯 |

## 2. Loop

```
function loop(arr) {
    for (let el in arr) {
        console.log(el);
    }
}

```

| Loop | Length of Input | # of Operations |
| --- | --- | --- |
| loop(['a']) | 1 | 🤔 |
| loop(['a', 'b']) | 2 | 🤔 |
| loop(['a', 'b', 'c', 'd']) | 4 | 🤔 |
| loop(['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h']) | 8 | 🧐 |
| loop(['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p']) | 16 | 😕 |
| loop(['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z','za', 'zb', 'zc', 'zd', 'ze', 'zf']) | 32 | 🤯 |

## 3. Binary Search

```
function binarySearch(list, el) {
    let low = 0;
    let high = list.length - 1;
    while (low <= high) {
        let mid = Math.floor((high + low) / 2 );
        let guess = list[mid];
        console.log(guess);
        if (guess === el) {
            return `Found at index ${mid}`;
        } else if (guess > el) {
            high = mid - 1;
        } else {
            low = mid + 1;
        }
    }
    return null;
}

```

| Binary Search | Length of Input | # of Operations |
| --- | --- | --- |
| binarySearch(['a'], 'a') | 1 | 😴 |
| binarySearch(['a', 'b'], 'b') | 2 | 🤔 |
| binarySearch(['a', 'b', 'c', 'd'], 'c') | 4 | 🤔 |
| binarySearch(['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h'], 'g') | 8 | 🧐 |
| binarySearch(['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p'], 'b') | 16 | 😕 |
| binarySearch(['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z','za', 'zb', 'zc', 'zd', 'ze', 'zf'], 'zf') | 32 | 🤯 |

## 4. Nested Loop

```
function nestedLoop(list){
    for (let first in list) {
        for (let second in list) {
            console.log(first, second);
        }
    }
}

```

| Nested Loop | Length of Input | #  of Operations |
| --- | --- | --- |
| nestedLoop(['a']) | 1 | 😴 |
| nestedLoop(['a', 'b']) | 2 | 🤔 |
| nestedLoop(['a', 'b', 'c']) | 3 | 🤔 |
| nestedLoop(['a', 'b', 'c', 'd']) | 4 | 🧐 |
| nestedLoop(['a', 'b', 'c', 'd', 'e']) | 5 | 🤯 |

# Essential Questions

1. What is Big O? What is it used for?
2. What does the `n` in O(n) mean?
3. Why is it important to analyze the worst-case scenarios when analyzing the efficiency of an algorithm?
4. What are common algorithm runtimes and how do they describe how and which algorithms are associated with them?

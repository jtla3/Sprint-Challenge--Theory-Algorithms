# Anaalysis of Algorithms

### Exercise I. Give an analysis of the running time with respect to the input size n of each of the following program fragmenst below:

a) a = 0
while (a < n * n * n)
    a = a + n * n;

Solution: a: O(n)


b) // input array is of length n
i = array.length - 1;
while (array[i] > x && i >= 0)
    i = i / 2;

Solution b: O(log n) 

c) sum = 0
for (i = 0; i < Math.sqrt(n) / 2: i++)
    for (j = i; j < 8 + i; j++)
        for (k = j; k < 8 + j; k++)
            sum++;

Solution c: O(sqrt(n))

d) sum = 0
    for (i = 1; i < n; i *= 2)
        for (j = 0; j < n; j++)
            summ++;

Solution d: O(n log n)

e) sum = 0
for (i = 0; i < n / 2: i++)
    for (j = i; j < n + i; j++)
        for (k = j + 1; k < n;; k++)
            for ( l = k + 1; l < 10 + k; l++)
            sum++;

Solution e: O(n^3)

f) bunnyEars = functions (bunnies) {// here bunnies === n
    if (bunnies === 0) return 0;;
    return 2 + bunnyEars(bunnies-1;)
    }

Solution f: O(n)

g) search = functions (array, arraySize, target) {// here arraySize === n
    if (arraySize > 0)
        if (array[arraySize - 1] === target) return true;
        else return search(array, arraySize-1, target);
        }
            return false;
        }

Solution g: O(n)

### Exercies II

a) Given an array a of n numbers, design a linear running time algorithm to find the maximum value of a[j] - a[i], where j >= i.

int maxIndexDiff(int arr[], int n) // found solution on Google and not sure if it is right
{
    int maxDiff = -1;
    int i, j;
 
    for (i = 0; i < n; ++i)
    {
        for (j = n-1; j > i; --j)
        {
            if(arr[j] > arr[i] && maxDiff < (j - i))
                maxDiff = j - i;
        }
    }
 
    return maxDiff;

b) Egg Dropping problem

The first thing to do is start at the lower half of the building, on floor f and drop and egg from there and record if it breaks or not. If it breaks then move to lower floor and continue the process until it doesn not break. If it did not break on floor f then you have found the floor you want.

### Exercise 3

function quicksort(array)
    if length(array) <= 1
        return array
    select and remove a pivot element pivot from array
    create empty lists less and greater
    for each x in array
        if x <= pivot then append x to less
        else append x to greater
    return concatenate(quicksort(less), list(pivot), quicksort(greater))

    a) The run time on the algorithm above would be O(n^2). After every interation the first array is empty and second array is of size (n-1), (n-2),...

    b) The run time will be O(n log n). After at every step the array is split into 2 almost equal sized arrays. Hence there will be (log n) number of steps, and each step has linear O(n) time complexity.



# Exercise I

### A
  * linear O(n)

### B
  * log O(log n)

### C
  * linear O(n)

### D
  * log linear O(n log n)

### E
  * cubic O(n^3)

### F
  * linear O(n)

### G
  * linear O(n)


# Exercise II:

### A
```
function linearMaxDifference(nums) {
  let maxDiff = 0;
  let smallestElement = nums[0];
  let temp;
  for(let i = 1; i < nums.length; i++) {
    temp = nums[i] - smallestElement;
    if(temp > maxDiff){
    	maxDiff = temp;
    }
    if(nums[i] < smallestElement) {
    	smallestElement = nums[i];
    }
  }
  return maxDiff;
}
```
### B 
Algorithm:
Each round consists of dropping an egg off of the middle of the remaining floors (floor n / 2 for the first round). If the egg breaks, only consider floors below the middle floor in future rounds. If the egg does not break, only consider floors above the middle floor in future rounds. Continue until there is only 1 remaining floor. Each round reduces the number of floors to check by half, so the run time will be O(log(n)).

 # Exercise III:
 
 ### A 
 * O(n^2) because it supports the array and has to re-sort it.

 ### B 
  * O(n log n) because you split it in half and divide up the work.
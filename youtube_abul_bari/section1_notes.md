# Algorithms

## Algorithm

  - written at design time
  - Domain knowledge
  - can use any language
  - H/W and OS independent
  - can be analyzed

## Program

  - Implementation time
  - programmer ( can also have domain knowledge)
  - written only in a programming language
  - H/W & OS dependent
  - Testing

## Prior Analysis vs Posteriori Testing

### Priori Analysis (done on algorithms)

1. Algorithm
2. Independent of Language
3. hardware Independent
4. Time and Space Function

### Posteriori Testing (done on programs)

1. Program
2. Language dependent
3. Hardware dependent
4. watch time & bytes

## Characteristics of Algorithm

1. Input - 0 or more
2. Output - 1 or more
3. Definiteness - clear statements 
4. Finiteness - stops at some point
5. Effectiveness - should serve some purpose (avoid unnecessary statements)

## How to Write and Analyze an Algorithm

swap(a, b) {
  temp = a;
  a = b;
  b = temp;
}

### Analyzing

1. Time
2. Space
3. Network Consumption (how data transfer is done)
4. Power Consumption
5. CPU Registers (low level programming)


### Time

each simple statement is 1 unit of time
f(n) = 3 (constant time) O(1)
x = 5*a + 6*b ==> 1 unit of time regardless of the multiple steps of machine code required for this calculation

### Space

a ==> 1
b ==> 1
temp ==> 1
s(n) = 3 (constant time) O(1)
s(n) = 3 words

### Frequency Count Method

A [8, 3, 9, 7 2]
i {0, 1, 2, 3, 4}
n = 5

Algorithm sum(A, n) {
  s = 0;
  for (i = 0; i < n;  i++) {
    s = s + A[i];
  }
  return s;
}

s = 0 => 1 unit time
i = 0 => 1 unit time
i < n => n + 1 units time
i++ => n unit time
s = S + A[i]; => n units time
return s => 1 unit time
overall => f(n) = 2n + 3 ==> simplifies to O(n)

space complexity

A => n words
n => 1
s => 1
i => 1

s(n) = n + 3 => simplifies to O(n)

Algorithm Add(A,B,n) {
  for (i = 0; i < n; i++) { // ==> n + 1
    for (j = 0; j < n; j++) { // ==> n x (n + 1)
      c[i, j] = A[i, j] +  B[i,j];  // ==> n x n
    }
  }
}

#### Time Complexity
f(n) = 2n^2 + 2n + 1 ==> O(n^2) 

#### Space

A => n^2
B => n^2
C => n^2
n => 1
i => 1
j => 1

s(n) = 3n^2 + 3

### For a triple nested loop

#### Time Complexity
f(n) = 2n^3 + 3n^2 + 2n + 1 ==> overall O(n^3) time complexity
#### Space Complexity
A => n^2
B => n^2
C => n^2
n => 1
i => 1
j => 1
k => 1
s(n) = 3n^2 + 4 ==> overall O(n^2) space complexity



# **Vector Dot-Product Implementation**

## **Introduction**
>This repository contains the implementation of the **vector dot-product** operation in C++. The dot-product is a fundamental operation in ***linear algebra***, widely used in fields like computer graphics, **machine learning**, and scientific `computing`.
For more information visit [dot product](https://byjus.com/maths/dot-product-of-two-vectors/).

![dot product showing image](https://cdn1.byjus.com/wp-content/uploads/2022/09/Dot-Product-Of-Two-Vectors-1.png)
## **Mathematical Expression**
The dot-product of two vectors **A** and **B** is defined as:

**A = [a₁, a₂, ..., aₙ]**

**B = [b₁, b₂, ..., bₙ]**

The dot-product is calculated as:

$\mathbf{A} \cdot \mathbf{B} = \sum_{i=1}^{n} a_i \cdot b_i$

## **Example Code Snippet**
Here is a simple implementation of the vector dot-product in C++:

```cpp
#include <iostream>
#include <vector>
using namespace std;
double dotProduct(vector<double>& vec1, vector<double>& vec2) {
    double result = 0.0;
    for (int  i = 0; i < vec1.size(); ++i) {
        result += vec1[i] * vec2[i];
    }
    return result;
}

int main() {
    vector<double> vec1 = {1.0, 2.0, 3.0};
    vector<double> vec2 = {4.0, 5.0, 6.0};
    if(vec1.size()!=vec2.size())
    {
         cout<<"for dot product vector must in equal size"<<endl;
    }
    else
    {
        cout << "Dot Product: " << dotProduct(vec1, vec2) << endl;
    } 
    return 0;
}
```
# LISTS
### two type of product exist
* dot product
* cross product
### output of two type of product
+ dot give scalar
+ cross product give vector

1. first 
   - dot 
   - cross
# Task list
- [x] tw work
- [ ] ooad work
- [ ] ooad learn
- [x] fol topic
# footnote
Here is a simple footnote[^1].
A footnote can also have multiple lines[^2].

[^1]: My reference.
[^2]: To add line breaks within a footnote, prefix new lines with 2 spaces.
  This is a second line.
# Alerts 
> [!NOTE]
> note note note.!!!

> [!TIP]
> practice daily.!!!
# Tables 

|Version|Approach|Complexity|Memory Usage|Performance|
|----|----|----|----|----|
|Naive|	Basic for-loop|	𝑂(𝑛)|minimal|moderate|
|Parallelized|	Multithreading|O(n/p)|	Moderate|	High|
SIMD Optimized|	Vectorized operations|O(n/k)|	High	|Very High|
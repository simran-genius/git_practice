# **Vector Dot-Product Implementation**

## **Introduction**
This repository contains the implementation of the **vector dot-product** operation in C++. The dot-product is a fundamental operation in linear algebra, widely used in fields like computer graphics, machine learning, and scientific computing.

## **Mathematical Expression**
The dot-product of two vectors \( \mathbf{A} = [a_1, a_2, \ldots, a_n] \) and \( \mathbf{B} = [b_1, b_2, \ldots, b_n] \) is defined as:

\[
\mathbf{A} \cdot \mathbf{B} = \sum_{i=1}^{n} a_i \cdot b_i
\]

## **Example Code Snippet**
Here is a simple implementation of the vector dot-product in C++:

```cpp
#include <iostream>
#include <vector>

double dotProduct(const std::vector<double>& vecA, const std::vector<double>& vecB) {
    if (vecA.size() != vecB.size()) {
        throw std::invalid_argument("Vectors must have the same size.");
    }

    double result = 0.0;
    for (size_t i = 0; i < vecA.size(); ++i) {
        result += vecA[i] * vecB[i];
    }
    return result;
}

int main() {
    std::vector<double> vecA = {1.0, 2.0, 3.0};
    std::vector<double> vecB = {4.0, 5.0, 6.0};
    try {
        std::cout << "Dot Product: " << dotProduct(vecA, vecB) << std::endl;
    } catch (const std::exception& e) {
        std::cerr << e.what() << std::endl;
    }
    return 0;
}

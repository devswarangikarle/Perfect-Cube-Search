# Perfect-Cube-Search

#include <iostream>
#include <cmath>

int main() {
    // Input
    int n;
    std::cin >> n;

    // Find the integer cube root of n
    int cubeRoot = static_cast<int>(std::cbrt(n));

    // Handle the case where cube root is rounded down
    if (std::pow(cubeRoot, 3) > n) {
        cubeRoot--;
    }

    // Compute the largest perfect cube less than or equal to n
    int result = std::pow(cubeRoot, 3);

    // Output the result
    std::cout << result << std::endl;

    return 0;
}

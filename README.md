# labit1
#include <iostream>

int main() {
    int sum_of_primes = 0;

    for (int number = 2; number <= 1000; number++) {
        bool is_prime = true;

        for (int current = 2; current < number; current++) {
            if (number / current == 0) {
                is_prime = false;
                break;
            }
        }

        if (is_prime) {
            sum_of_primes += number;
        }
    }

    std::cout << "Сума всіх простих чисел від 2 до 1000: " << sum_of_primes << std::endl;

    return 0;
}


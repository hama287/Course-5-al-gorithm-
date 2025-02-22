# Course-5-al-gorithm-
#include <iostream>
#include <string>

using namespace std;

int readPositiveNumber(string messages)
{
    int number = 0;

    do
    {
        cout << messages << endl;
        cin >> number;

    } while (number < 0);

    return number;
};

bool IsPerfectNumber(int number)
{
    int sum = 0;

    for (int i = 1; i < number; i++)
    {
        if (number % i == 0)

            sum += i;
        ;
    };
    return number == sum;
};

void printNumberIsperfect(int number)
{
    if (IsPerfectNumber(number))
    {
        cout << " number is perfect  " << number << endl;
    }

    else
    {
        cout << "number is no perfect  " << number << endl;
    }
};

int main()
{
    printNumberIsperfect(readPositiveNumber("please enter a positive number :"));

    return 0;
};

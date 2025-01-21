#include <iostream>
#include <string.h>
#include<unistd.h>
using namespace std;
void format(int n, int arr[3])
{
    char tenwale[10][10] = {"ten", "eleven", "twelve", "thirteen", "fourteen", "fifteen", "sixteen", "seventeen", "eighteen", "nineteen"};
    char suffix[8][10] = {"twenty", "thirty", "forty", "fifty", "sixty", "seventy", "eighty", "ninety"};
    char initial[9][10] = {"one", "two", "three", "four", "five", "six", "seven", "eight", "nine"};
    if (arr[n] == 0)
    {
        if (arr[n + 1] == 0)
        {
            for (int a = 1; a < 10; a++)
            {
                if (arr[n + 2] == a)
                {
                    cout << initial[a - 1] << " ";
                }
            }
        }

        else if (arr[n + 1] == 1)
        {
            for (int a = 0; a < 10; a++)
            {
                if (arr[n + 2] == a)
                {
                    cout << tenwale[a] << " ";
                }
            }
        }
        else
        {
            if (arr[n + 2] != 0)
            {
                for (int a = 2; a < 10; a++)
                {
                    for (int b = 1; b < 10; b++)
                    {
                        if (arr[n + 1] == a && arr[n + 2] == b)
                        {
                            cout << suffix[a - 2] << " " << initial[b - 1] << " ";
                        }
                    }
                }
            }
            else
            {
                for (int a = 2; a < 10; a++)
                {
                    if (arr[n + 1] == a)
                    {
                        cout << suffix[a - 2] << " ";
                    }
                }
            }
        }
    }

    else
    {
        for (int c = 1; c < 10; c++)
        {
            if (arr[n] == c)
            {
                if (arr[n + 1] == 1)
                {
                    for (int a = 0; a < 10; a++)
                    {
                        if (arr[n + 2] == a)
                        {
                            cout << initial[c - 1] << " hundred " << tenwale[a] << " ";
                        }
                    }
                }
                else if (arr[n + 1] == 0)
                {
                    if (arr[n + 2] != 0)
                    {
                        for (int a = 1; a < 10; a++)
                        {
                            if (arr[n + 2] == a)
                            {
                                cout << initial[c - 1] << " hundred " << initial[a - 1] << " ";
                            }
                        }
                    }
                    else if (arr[n + 2] == 0)
                    {
                        cout << initial[c - 1] << " hundred ";
                    }
                }
                else
                {
                    if (arr[n + 2] != 0)
                    {
                        for (int a = 2; a < 10; a++)
                        {
                            for (int b = 1; b < 10; b++)
                            {
                                if (arr[n] == c && arr[n + 1] == a && arr[n + 2] == b)
                                {
                                    cout << initial[c - 1] << " hundred " << suffix[a - 2] << " " << initial[b - 1] << " ";
                                }
                            }
                        }
                    }
                    else if (arr[n + 2] == 0)
                    {
                        for (int a = 2; a < 10; a++)
                        {
                            if (arr[n + 1] == a)
                            {
                                cout << initial[c - 1] << " hundred " << suffix[a - 2] << " ";
                            }
                        }
                    }
                }
            }
        }
    }
}
int main()
{
    cout << "Enter Number:";
    char input[20];
    cin >> input;
    int a = strlen(input); // tells me total numbers
    int number = stoi(input);
    if (number == 0)
    {
        cout << "zero";
    }
    int b;
    if (a % 3 == 0)
    {
        b = a;
    }
    else
    {
        b = a + (3 - (a % 3));
    }
    int arr1[b];
    for (int a = 0; a < b; a++)
    {
        arr1[0] = 0;
    }
    for (int t = b; t >= 0; t--)
    {
        arr1[t - 1] = number % 10;
        number = number / 10;
    }

    if (a >= 1 && a <= 3)
    {
        format(0, arr1);
    }
    else if (a >= 4 && a <= 6)
    {
        if (arr1[0] == 0 && arr1[1] == 0 && arr1[2] == 0)
        {
            cout << "";
        }
        else
        {
            format(0, arr1);
            cout << "thousand ";
        }
        format(3, arr1);
    }
    else if (a >= 7 && a <= 9)
    {
        if (arr1[0] == 0 && arr1[1] == 0 && arr1[2] == 0)
        {
            cout << "";
        }
        else
        {
            format(0, arr1);
            cout << "million ";
        }
        if (arr1[3] == 0 && arr1[4] == 0 && arr1[5] == 0)
        {
            cout << "";
        }
        else
        {
            format(3, arr1);
            cout << "thousand ";
        }

        format(6, arr1);
    }
    else if (a >= 10 && a <= 12)
    {
        if (arr1[0] == 0 && arr1[1] == 0 && arr1[2] == 0)
        {
            cout << "";
        }
        else
        {
            format(0, arr1);
            cout << "billion ";
        }
        if (arr1[3] == 0 && arr1[4] == 0 && arr1[5] == 0)
        {
            cout << "";
        }
        else
        {
            format(3, arr1);
            cout << "million ";
        }
        if (arr1[6] == 0 && arr1[7] == 0 && arr1[8] == 0)
        {
            cout << "";
        }
        else
        {
            format(6, arr1);
            cout << "thousand ";
        }

        format(9, arr1);
    }
    sleep(5);
}

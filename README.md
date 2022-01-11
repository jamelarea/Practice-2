# Practice-2

    #include <iostream>
    #include <string>
    #include <math.h>
    using namespace std;

    void factorial(double num)
    {
        for (int i = 1; i <= 10; i++) {
            num = num * i;
        }
        cout << "\nFactorial: " << num << endl;
    }

    void table(double num) {
        double result = 0;
        int Negative = 0;
        int Positive = 0;

        cout << "\nTable:" << endl;
        for (int i = -5; i <= 10; i++) {
            result = num * i;
            cout << num << " x " << i << " = " << result << endl;

            if (result < 0)
            {
                Negative++;
            }
            else {
                Positive++;
            }
        }

        cout << "\nTotal of Negative outputs: " << Negative << endl;
        cout << "Total of Positive outputs: " << Positive << endl;
    }

        int main()
        {
            string name;
            double num;

            cout << "Enter your full name: ";
            getline(cin, name);

            cout << "Enter a number from 1 to 10: ";
            cin >> num;

            while (cin.fail() || num > 1 && num <= 10)
            {
                if (num > 1 && num <= 10)
                {
                    factorial(num);
                    break;
                }
                else {
                    cin.clear();
                    cin.ignore(1000, '\n');
                    cout << "\nInvalid input. Enter a number again: ";
                    cin >> num;
                }
            }

            table(num);
            return 0;
        }

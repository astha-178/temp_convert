#include <iostream>
#include <iomanip>
#include <string>
#include <algorithm>

using namespace std;

double celsiusToFahrenheit(double c) {
    return (c * 9.0 / 5.0) + 32.0;
}

double celsiusToKelvin(double c) {
    return c + 273.15;
}

double fahrenheitToCelsius(double f) {
    return (f - 32.0) * 5.0 / 9.0;
}

double fahrenheitToKelvin(double f) {
    return (f - 32.0) * 5.0 / 9.0 + 273.15;
}

double kelvinToCelsius(double k) {
    return k - 273.15;
}

double kelvinToFahrenheit(double k) {
    return (k - 273.15) * 9.0 / 5.0 + 32.0;
}

int main() {
    double value;
    string fromScale, toScale;

    cout << "Temperature Converter\n";
    cout << "Available scales: Celsius, Fahrenheit, Kelvin\n";

    cout << "Enter the temperature value: ";
    cin >> value;

    cout << "Convert from (Celsius/Fahrenheit/Kelvin): ";
    cin >> fromScale;
    cout << "Convert to (Celsius/Fahrenheit/Kelvin): ";
    cin >> toScale;

    // Convert input to lowercase for easy comparison
    transform(fromScale.begin(), fromScale.end(), fromScale.begin(), ::tolower);
    transform(toScale.begin(), toScale.end(), toScale.begin(), ::tolower);

    double result;

    if (fromScale == toScale) {
        result = value;
    } else if (fromScale == "celsius") {
        if (toScale == "fahrenheit")
            result = celsiusToFahrenheit(value);
        else if (toScale == "kelvin")
            result = celsiusToKelvin(value);
        else {
            cout << "Invalid target scale.\n";
            return 1;
        }
    } else if (fromScale == "fahrenheit") {
        if (toScale == "celsius")
            result = fahrenheitToCelsius(value);
        else if (toScale == "kelvin")
            result = fahrenheitToKelvin(value);
        else {
            cout << "Invalid target scale.\n";
            return 1;
        }
    } else if (fromScale == "kelvin") {
        if (toScale == "celsius")
            result = kelvinToCelsius(value);
        else if (toScale == "fahrenheit")
            result = kelvinToFahrenheit(value);
        else {
            cout << "Invalid target scale.\n";
            return 1;
        }
    } else {
        cout << "Invalid input scale.\n";
        return 1;
    }

    cout << fixed << setprecision(2);
    cout << "\n" << value << " degrees " << fromScale << " = " << result << " degrees " << toScale << endl;

    return 0;
}

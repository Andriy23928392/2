// Задача 1: Виведення символу та його ASCII-кодів
#include <iostream>
#include <iomanip>
using namespace std;

int main() {
    char symbol;
    cout << "Введіть символ: ";
    cin >> symbol;
    cout << "Символ: " << symbol << endl;
    cout << "ASCII (десятковий): " << int(symbol) << endl;
    cout << "ASCII (шістнадцятковий): " << hex << int(symbol) << endl;
    return 0;
}

// Задача 2: Арифметичні операції з точністю до 12 знаків
#include <iostream>
#include <iomanip>
using namespace std;

int main() {
    double a, b;
    cout << "Введіть два числа: ";
    cin >> a >> b;
    cout << fixed << setprecision(12);
    cout << "Сума: " << a + b << endl;
    cout << "Різниця: " << a - b << endl;
    cout << "Добуток: " << a * b << endl;
    if (b != 0) {
        cout << "Частка: " << a / b << endl;
    } else {
        cout << "Ділення на нуль неможливе!" << endl;
    }
    return 0;
}

// Задача 3: Перевірка подільності числа
#include <iostream>
#include <iomanip>
using namespace std;

int main() {
    int number;
    cout << "Введіть ціле число: ";
    cin >> number;
    cout << "Парне: " << (number % 2 == 0 ? "ТАК" : "НІ") << endl;
    cout << "Ділиться на 8: " << (number % 8 == 0 ? "ТАК" : "НІ") << endl;
    cout << "Ділиться на 16: " << (number % 16 == 0 ? "ТАК" : "НІ") << endl;
    cout << "Вісімковий формат: " << oct << number << endl;
    cout << "Шістнадцятковий формат: " << hex << number << endl;
    return 0;
}

// Задача 4: Перетворення температур
#include <iostream>
#include <iomanip>
using namespace std;

int main() {
    int option;
    double temperature;
    cout << "Введіть варіант (1 - Цельсій у Фаренгейт, 2 - Фаренгейт у Цельсій): ";
    cin >> option;
    cout << "Введіть температуру: ";
    cin >> temperature;
    if ((option == 1 && temperature < -273.15) || (option == 2 && temperature < -459.67)) {
        cout << "Занадто холодно для підрахунку!" << endl;
    } else {
        cout << fixed << setprecision(2);
        if (option == 1) {
            cout << "Температура у Фаренгейтах: " << (temperature * 9 / 5 + 32) << endl;
        } else if (option == 2) {
            cout << "Температура у Цельсіях: " << ((temperature - 32) * 5 / 9) << endl;
        } else {
            cout << "Невірний вибір!" << endl;
        }
    }
    return 0;
}

// Задача 5: Переведення балів у оцінки
#include <iostream>
using namespace std;

int main() {
    double points;
    cout << "Введіть кількість балів (0.0 - 9.0): ";
    cin >> points;
    if (points >= 0.0 && points <= 4.4) {
        cout << "Незадовільна оцінка (2.0)" << endl;
    } else if (points >= 4.5 && points <= 5.2) {
        cout << "Задовільний (3.0)" << endl;
    } else if (points >= 5.3 && points <= 6.2) {
        cout << "Оцінка вище задовільно (3.5)" << endl;
    } else if (points >= 6.3 && points <= 7.2) {
        cout << "Хороша оцінка (4.0)" << endl;
    } else if (points >= 7.3 && points <= 8.2) {
        cout << "Оцінка вище добре (4.5)" << endl;
    } else if (points >= 8.3 && points <= 9.0) {
        cout << "Дуже добре (5.0)" << endl;
    } else {
        cout << "Неправильна кількість пунктів!" << endl;
    }
    return 0;
}

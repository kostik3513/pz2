# 🥨 Практична робота №2

## ⚓ Тема: Реалізація списків. Однозв’язний список.

## ✨ Мета: ознайомитися з принципами організації однозв’язного списку та контейнером std::forward_list у C++, сформувати навички створення, перегляду, пошуку, вставки та видалення елементів списку з використанням ітераторів.

## Варіант 1

### Завдання 1. Ініціалізація та виведення елементів.

# <img width="503" height="228" alt="pz2_sec1" src="https://github.com/user-attachments/assets/50c4f0a1-23a1-4ff5-a5c5-0fade11e04da" />

```
#include <iostream>
#include <forward_list>
#include <string>

using namespace std;

int main() {
    forward_list<string> professions = { "Програміст", "Дизайнер", "Тестувальник", "Аналітик", "DevOps" };

    cout << "Список ІТ-професій:" << endl;

    for (auto it = professions.begin(); it != professions.end(); ++it) {
        cout << *it << endl;
    }

    return 0;
}
```

### Завдання 2. Додавання та видалення елементів.

# <img width="495" height="243" alt="pz2_sec2" src="https://github.com/user-attachments/assets/d6a5ccf4-5844-4a72-bd94-be2eca2c6bc9" />
# <img width="1647" height="167" alt="image" src="https://github.com/user-attachments/assets/4e1ce1be-5e7a-44f0-8e3e-0a1f8234fcec" />

```
#include <iostream>
#include <forward_list>
#include <string>

using namespace std;

int main() {
    
    forward_list<string> professions = { "Програміст" };

    professions.push_front("Data Scientist");
    professions.push_front("Архитектор");

    cout << "Список після додавання елементів:" << endl;
    for (auto it = professions.begin(); it != professions.end(); ++it) {
        cout << *it << endl;
    }

    professions.pop_front();

    cout << "\nПісля видалення першого елемента:" << endl;
    for (auto it = professions.begin(); it != professions.end(); ++it) {
        cout << *it << endl;
    }

    return 0;
}
```

### Завдання 3. Знаходження та перевірка наявності елемента

# <img width="1072" height="296" alt="image" src="https://github.com/user-attachments/assets/58b525e1-1dcc-4c44-bdb1-ee5180a3a516" />

```
#include <iostream>
#include <forward_list>
#include <string>

using namespace std;

int main() {
    
    forward_list<string> professions = { "Програміст", "Дизайнер", "Тестувальник", "Аналітик", "DevOps" };
    
    string searchElement = "Аналітик";

    auto it = professions.begin();
    while (it != professions.end()) {
        if (*it == searchElement) {
            break;
        }
        ++it;
    }

    if (it != professions.end()) {
        cout << "Елемент знайдено" << endl;
    } else {
        cout << "Елемент не знайдено" << endl;
    }

    return 0;
}
```

### Завдання 4. Підрахунок кількості символів

# <img width="1150" height="295" alt="image" src="https://github.com/user-attachments/assets/54fc7c0f-585f-4693-9f0d-d0b22e6e8f09" />

```
#include <iostream>
#include <forward_list>
#include <string>

using namespace std;

int main() {
    
    forward_list<string> professions = { "Програміст", "Дизайнер", "Тестувальник", "Аналітик", "DevOps" };

    int totalChars = 0;

    for (auto it = professions.begin(); it != professions.end(); ++it) {
        totalChars += it->length();
    }

    cout << "Загальна кількість символів у назвах елементів: " << totalChars << endl;

    return 0;
}
```

### Завдання 5. Вставка елемента у список

# <img width="1095" height="475" alt="image" src="https://github.com/user-attachments/assets/6e2ec21c-2704-4634-a300-b0a253a252e5" />

```
#include <iostream>
#include <forward_list>
#include <string>

using namespace std;

int main() {
    forward_list<string> professions = { "Програміст", "Дизайнер", "Тестувальник", "Аналітик", "DevOps" };

    string searchElement = "Аналітик";
    string newElement = "Проєктувальник";

    auto it = professions.begin();
    bool found = false;

    while (it != professions.end()) {
        if (*it == searchElement) {
            professions.insert_after(it, newElement);
            found = true;
            break;
        }
        ++it;
    }

    if (!found) {
        cout << "Елемент \"" << searchElement << "\" відсутній у списку." << endl;
    }

    cout << "Оновлений список професій:" << endl;
    for (auto i = professions.begin(); i != professions.end(); ++i) {
        cout << *i << endl;
    }

    return 0;
}
```

## Висновок

Під час виконання Практичної роботи №2 я ознайомився з принципами організації однозв'язного списку та контейнером `std::forward_list` у C++. Набув практичних навичок створення, ініціалізації та перегляду списку за допомогою ітераторів. Опрацював базові операції з елементами: додавання на початок (`push_front`), видалення (`pop_front`), пошук і вставку після знайденого елемента (`insert_after`). Усі завдання виконано в повному обсязі, програми працюють коректно.

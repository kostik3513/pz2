# Практична робота № 2

## Тема: Реалізація списків. Однозв’язний список.

## Мета: ознайомитися з принципами організації однозв’язного списку та контейнером std::forward_list у C++, сформувати навички створення, перегляду, пошуку, вставки та видалення елементів списку з використанням ітераторів.

## Варіант 1

### Завдання 1. Ініціалізація та виведення елементів.

# <img width="503" height="228" alt="pz2_sec1" src="https://github.com/user-attachments/assets/50c4f0a1-23a1-4ff5-a5c5-0fade11e04da" />

```
#include <iostream>
#include <forward_list>
#include <string>

using namespace std;

int main() {
    // 1. Створення однозв'язного списку відповідно до варіанта №3
    forward_list<string> professions = { "Програміст", "Дизайнер", "Тестувальник", "Аналітик", "DevOps" };

    cout << "Список ІТ-професій:" << endl;

    // 2. Виведення всіх елементів списку за допомогою ітератора
    for (auto it = professions.begin(); it != professions.end(); ++it) {
        cout << *it << endl;
    }

    return 0;
}
```

### Завдання 2. Додавання та видалення елементів.

# <img width="495" height="243" alt="pz2_sec2" src="https://github.com/user-attachments/assets/d6a5ccf4-5844-4a72-bd94-be2eca2c6bc9" />

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

#

```

```

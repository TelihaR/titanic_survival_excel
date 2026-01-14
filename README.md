# Прогноз виживання пасажирів «Титаніка» в Excel
Метою проєкту було спробувати побудувати модель прогнозування виживання пасажирів «Титаніка» в Excel, щоб на практиці зрозуміти, як працюють різні підходи до моделювання і з якими труднощами можна зіткнутися без спеціалізованих бібліотек.

---

## Дані
- Відкритий набір даних **Titanic (Kaggle)**
- Цільова змінна: `Survived` (0 — не вижив, 1 — вижив)

## Підготовка:
- Перетворення не числових зміних в числові, для цього ChatGPT радить One-Hot Encoding.
  Тобито наші дані по типу Embarked, що містять  "S", "С", "Q" - запишемо у вигляді 3 стовців Embarked_S, Embarked_C,	Embarked_Q. Вони матимуть вигляд:
  
<img width="323" height="121" alt="image" src="https://github.com/user-attachments/assets/44580677-a1ae-43c0-a56d-a2303472d445" />

- Зі ствопця Name виокремлюємо титул, вибираємо рідкісні титули записуємо в колонку Rare:
<img width="243" height="141" alt="image" src="https://github.com/user-attachments/assets/19c7aabc-c3c0-4a94-8707-f38933dcfccb" />

Використовуючи  One-Hot Encoding, записуємо у вигляді :

<img width="270" height="81" alt="image" src="https://github.com/user-attachments/assets/c3eb336a-26f0-467d-8d53-8fd0c5f55df4" />

- Заповнюємо пропущенні занчення в Аge:

<img width="223" height="81" alt="image" src="https://github.com/user-attachments/assets/de871ed9-f483-4c7e-8edf-08ae30dcd4a2" />

Маємо 202 пропущених значення. Заповнюємо їх середнім значенням для кожного Title.
  
---

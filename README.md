# 🧪 TDD Live Demo — Лекція «XP та TDD»
### Дисципліна: Розроблення програмного забезпечення | 3 курс | КН

---

## 📋 Опис проєкту

Цей проєкт демонструє повний цикл **Test-Driven Development (TDD)**
на прикладі **String Calculator Kata** (Roy Osherove).

**Задача:** реалізувати функцію `add(text)`, яка:
- приймає рядок чисел через кому або `\n`
- повертає їх суму
- підтримує кастомні роздільники
- кидає виняток для від'ємних чисел

---

## 🗂️ Структура кроків

```
tdd_lecture_demo/
│
├── step1_red/          ← 🔴 RED: перший тест, що падає
├── step2_green/        ← 🟢 GREEN: мінімальна реалізація
├── step3_refactor/     ← 🔵 REFACTOR: очищення коду
├── step4_extended/     ← 🔴🟢 Додаємо нові тести (новини вимоги)
├── step5_refactor_final/ ← 🔵 Фінальний рефакторинг
│
├── conftest.py         ← Спільна конфігурація pytest
├── requirements.txt    ← Залежності
└── README.md           ← Цей файл
```

---

## ⚡ Швидкий старт

```bash
# 1. Встановити залежності
pip install -r requirements.txt

# 2. Запустити тести конкретного кроку
cd step1_red
pytest test_calculator.py -v

# 3. Запустити всі тести
pytest . -v --tb=short
```

---

## 🎓 Сценарій

| Крок | Дія викладача |
|------|---------------|
| step1_red | Показати тест → запустити → побачити RED |
| step2_green | Написати мінімальний код → GREEN |
| step3_refactor | Рефакторинг → тести залишаються GREEN |
| step4_extended | Нові вимоги → нові тести → RED знову |
| step5_refactor_final | Фінальний дизайн коду |

---

## 💡 Команди для PyCharm Terminal (Alt+F12)

```bash
# Запуск з детальним виводом + зупинка на першому падінні
pytest step1_red/ -v -x

# Показати покриття коду
pytest step3_refactor/ -v --cov=calculator --cov-report=term-missing

# Запустити і стежити за змінами (live reloading)
ptw step4_extended/ -- -v
```

---

## 📖 Ресурси
- [String Calculator Kata — Roy Osherove](https://osherove.com/tdd-kata-1)
- [pytest документація](https://docs.pytest.org)
- [Refactoring Guru](https://refactoring.guru/uk)

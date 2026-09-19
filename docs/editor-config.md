# Shared editor settings

## .editorconfig

`.editorconfig` задає спільні правила форматування для всіх учасників команди.

### Global settings

- `charset = utf-8` — використовуємо UTF-8 для однакового кодування файлів.
- `end_of_line = lf` — однакові переноси рядків незалежно від ОС.
- `insert_final_newline = true` — файл закінчується порожнім переносом рядка.
- `trim_trailing_whitespace = true` — видаляються зайві пробіли в кінці рядків.

### C/C++

Для C і C++ використовуємо:

```ini
indent_style = space
indent_size = 4
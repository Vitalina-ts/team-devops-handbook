# Branching and Commit Conventions

## Branch naming

Формат:

type/short-description

Типи:

- feature — нова функціональність
- fix — виправлення помилки
- docs — зміни документації
- chore — технічні зміни

Приклади:

docs/add-readme-template
fix/gitignore-rules
chore/update-editorconfig

## Commit messages

Формат:

type: short description

Приклади:

docs: add branching conventions
fix: ignore environment files
chore: update editor settings

Повідомлення має бути коротким і описувати одну логічну зміну.

## Before merging

Перед злиттям робочі коміти типу:

fix typo
fix again
temp
test

мають бути об'єднані через squash або впорядковані через rebase.

У main повинна потрапляти зрозуміла історія змін.

## Локальні Git Hooks

Для перевірки відсутності зайвих пробілів перед комітом встановіть хук локально.
Каталог `.git/hooks` є локальним і не версіонується Git, тому після кожного clone хук потрібно встановити заново.

Створіть файл `.git/hooks/pre-commit` і вставте код:

```sh
#!/bin/sh
if git diff --cached --check; then
exit 0
else
echo "Помилка: Знайдено зайві пробіли в кінці рядків!"
exit 1
fi
```

Для Linux/WSL зробіть файл виконуваним:

```sh
chmod +x .git/hooks/pre-commit
```

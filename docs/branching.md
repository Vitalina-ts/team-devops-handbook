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
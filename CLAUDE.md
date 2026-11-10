# ai-routine-audit

Публичный лид-магнит: скил Claude + промпт ChatGPT, которые аудитят чаты пользователя (повторяемые задачи, переделки, часы потерь), выдают quick win и ведут на автовеб «ИИ-сотрудники».

- Репо: https://github.com/AIDimani/ai-routine-audit (публичный — сюда не класть ничего личного: отчёты по реальным чатам, ID, ключи).
- `ai-routine-audit/` — сам скил (SKILL.md + references). `chatgpt/prompt.md` — версия для ChatGPT.
- Zip для загрузки в Claude собирается из `ai-routine-audit/` и лежит в релизе GitHub (`releases/latest/download/ai-routine-audit.zip`, на него ссылается README).
- Ссылки: только по `~/.claude/reference/links-standard.md`. `utm_source=gh_skill`, `utm_medium=social`, `utm_campaign=aw_ai_workers`, `utm_content` = `claude-skill` / `chatgpt-prompt` / `readme`. ID получателя нет: это вход для новых.

## Выпуск новой версии

1. Правка файлов, коммит, push.
2. Упаковать: `uv run --with pyyaml python ~/.claude/skills/skill-creator/scripts/package_skill.py ai-routine-audit dist && cp dist/ai-routine-audit.skill dist/ai-routine-audit.zip`
3. `gh release create vX.Y dist/ai-routine-audit.zip --title "vX.Y" --notes "..."` — ссылка `latest/download` подхватит новый релиз сама.
4. Запись в `changelog.md`.

## Не проверено
- Работа скила в веб-Claude и ChatGPT со встроенным поиском по истории (тест был только на сессиях Claude Code).
- Точные названия пунктов настроек в README.

Етап/задача: P0.0 — узгодження документів за ADR-0001.

Зроблено:
- Перенесено Р1–Р16 у правила, архітектуру, інваріанти, перевірки та UI.
- Додано P0.0 й оновлено [план P0](/Users/openclow/workspace/Lead Keeper/docs/04-roadmap.md): реєстри — P0.3, ролі БД — P0.4, setup/e2e — P0.5, специфікація — P0.6, заготовки інваріантів і повне приймання — P0.7.
- Оновлено Makefile, CI та контракти імпортів.
- Додано [README KeyCRM](/Users/openclow/workspace/Lead Keeper/docs/keycrm/README.md), [known issues](/Users/openclow/workspace/Lead Keeper/docs/keycrm/known-issues.md) і порожній список overrides. Код застосунку не створював.
Файли: 13 оновлених, 3 нових. Ключові: [AGENTS.md](/Users/openclow/workspace/Lead Keeper/AGENTS.md), [інваріанти](/Users/openclow/workspace/Lead Keeper/docs/03-safety-invariants.md), [перевірки](/Users/openclow/workspace/Lead Keeper/docs/05-verification.md), [Makefile](/Users/openclow/workspace/Lead Keeper/Makefile), [.importlinter](/Users/openclow/workspace/Lead Keeper/backend/.importlinter).

Перевірки:
- 25 синтетичних перевірок контрактів — OK.
- Звірка перенесення Р1–Р16, YAML/INI, dry-run Makefile — OK.
- api.yaml і прийнятий ADR побайтово незмінні.
- make check — FAIL: ruff: command not found, make: [lint] Error 127.
- Eval — н/з: каркас ще не реалізований.
Інваріанти зачеплено: INV-01, INV-05–06, INV-08, INV-10, INV-12–13, INV-15, INV-18, INV-21–23; правила обліку етапів стосуються всіх 24.

Не зроблено / не перевірено: реєстри та скрипти лише заплановані; повний прогін Python 3.12/Postgres/frontend, setup, e2e та CI не виконаний. Залежностей застосунку не додано.

Ризики і питання до людини: нових конфліктів рішень не виявлено. Дата первинного завантаження специфікації невідома — позначено для P0.6. Читання примітки потребує перевірки на P2; append_note за правилами залишається вимкненим.

Наступний крок: окреме рев’ю P0.0, потім P0.1.

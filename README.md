# approval-policy

Политика подписи узлов governance-бандла (§I12 devtools). Единственный
источник значения `AUTHORIZED_APPROVER_ACCOUNTS`.

- Меняет: владелец, PR в `main`. Соавторов у репозитория нет намеренно:
  исполнитель (агент `ai-prosto`) писать сюда не может.
- Читает: devtools — `governance/approval_facts.policy_snapshot` и
  `human-merge.sh` — по SHA последнего коммита, тронувшего
  `policy/approvers.env`; версия закрепляется в заявке на одобрение узла,
  смена версии при живой заявке терминализирует её (`policy_changed`).
- Координаты источника у потребителя: devtools
  `contracts/approval-policy-source/v1/source.env` (authority-root).
- Правило флота: `prograph-vault/authored/rules/approver-policy.md`.

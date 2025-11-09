# Подюков Илья. ФИТ-2-2024 НМ. Методы и инструменты DevOps. ЛР по лекции 6
- копирую файлы из репозитория github.com/vparanoid/devops_lab6_roles
- активирую ci-пайплайны
<img width="2002" height="729" alt="изображение" src="https://github.com/user-attachments/assets/9f925476-8b9f-4801-a5be-f8235bdceff6" />

- добавляю тестовый сценарий и проверяю его работу со стороны github
<img width="1159" height="1172" alt="изображение" src="https://github.com/user-attachments/assets/76864ff9-d86c-4b38-8a1d-58ead1564ce7" />

- добавляю боевой сценарий и проверяю его работу со стороны github

сталкиваюсь с ошибками:
<img width="897" height="568" alt="изображение" src="https://github.com/user-attachments/assets/bea360e6-22b9-4ff6-981a-86368058e3b3" />
```
Error: 'become_method' must be one of the currently available values: ansible.builtin.runas, ansible.builtin.su, ansible.builtin.sudo
Error: Truthy value should be one of [false, true]
Error: Wrong indentation: expected 6 but found 4
Error: Wrong indentation: expected 4 but found 2
Error: All names should start with an uppercase letter.
Error: Use FQCN for builtin module actions (systemd).
Error: Too many blank lines (1 > 0)
Error: File permissions unset or incorrect.
Error: Use FQCN for builtin module actions (template).
Error: File permissions unset or incorrect.
Error: Use FQCN for builtin module actions (file).
Error: Use FQCN for builtin module actions (template).
```

- пытаюсь фиксить, снова получаю ошибки
```
Error: Truthy value should be one of [false, true]
Error: Wrong indentation: expected 6 but found 4
Error: Wrong indentation: expected 4 but found 2
Error: Too many blank lines (1 > 0)
Error: File permissions unset or incorrect.
Error: File permissions unset or incorrect.
```

- исправляю, снова ошибки
```
Error: Trailing spaces
Error: No new line character at the end of file
Error: No new line character at the end of file
```

- после исправления ещё ошибки
```
Run exit_code=0
WARNING  Listing 1 violation(s) that are fatal
Error: Trailing spaces
Read documentation for instructions on how to ignore specific rule violations.

# Rule Violation Summary

  1 yaml profile:basic tags:formatting,yaml

Failed: 1 failure(s), 0 warning(s) in 8 files processed of 11 encountered. Last profile that met the validation criteria was 'min'.
yaml[trailing-spaces]: Trailing spaces
playbook.yml:11

Command failed: got '2', expected '0'
Error: Process completed with exit code 1.
```

- исправляю, и.. вуаля! теперь валидация кода прошла успешно
<img width="873" height="564" alt="изображение" src="https://github.com/user-attachments/assets/1f735f2b-c17a-4eef-b0f6-c77e4598fc1b" />

# Python Banking System

A command-line banking system written in Python, built as a project challenge for the [DIO](https://www.dio.me/) Python Developer track.

## Features

- **Deposit:** accepts only positive values.
- **Withdrawal:** up to 3 withdrawals, each limited to R$ 500.00, only when there is enough balance.
- **Statement:** lists every deposit and withdrawal and shows the current balance in the `R$ 1500.45` format.
- **Input validation:** typing letters instead of a number no longer crashes the program. Values with a comma, like `150,50`, are accepted.

## How to run

You need Python 3 installed.

```bash
git clone https://github.com/Isgroi/python-banking-system.git
cd python-banking-system
python desafio.py
```

## Menu

```text
[d] Depositar
[s] Sacar
[e] Extrato
[q] Sair
```

## Concepts used

- `while True` loop to keep the menu running
- `if` / `elif` / `else` for each operation and validation rule
- Assignment operators (`+=`, `-=`)
- f-strings with `:.2f` to format money values
- A function with `try` / `except ValueError` to read numbers safely
- One function per operation (`depositar`, `sacar`, `exibir_extrato`), with positional-only (`/`) and keyword-only (`*`) parameters
- Functions returning several values as a tuple
- A `main()` function guarded by `if __name__ == "__main__":`

## Melhorias em relação ao desafio original (PT-BR)

- Validação de entrada: o programa não fecha com `ValueError` quando a pessoa digita letras.
- Aceita valores com vírgula, no formato brasileiro.
- Código separado em funções, uma para cada operação, com mensagens de confirmação de depósito e saque.

## Próximos passos

- Suportar vários usuários e contas.
- Adicionar testes automatizados com `pytest`.

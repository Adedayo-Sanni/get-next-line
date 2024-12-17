# Get Next Line

## Sumário
- [Introdução](#introdução)
- [Descrição](#descrição)
- [Regras](#regras)
- [Compilação](#compilação)

---

## Introdução
O projeto **Get Next Line** tem como objetivo desenvolver uma função em C que leia e retorne uma linha de um arquivo ou entrada padrão (stdin) a cada chamada. É uma função essencial que pode ser usada como base para futuros projetos que lidam com leitura de arquivos ou entradas dinâmicas.

---

### Descrição
A função `get_next_line` deve:
- Ler e retornar uma linha de um arquivo, uma chamada por vez.
- Incluir o caractere `\n` no final de cada linha retornada, exceto na última linha do arquivo se esta não terminar com `\n`.
- Retornar `NULL` quando não houver mais nada para ler ou em caso de erro.

### Regras
1. **Leitura incremental**: Não leia o arquivo inteiro de uma vez. A função deve retornar cada linha assim que um `\n` for encontrado.
2. **Compilação**: Use o parâmetro `-D BUFFER_SIZE=n` para definir o tamanho do buffer usado pelo `read()`.
3. **Comportamento indefinido**:
   - Se o arquivo apontado pelo file descriptor mudar entre chamadas.
   - Ao ler arquivos binários, embora você possa implementar uma lógica para tratá-los.

### Compilação
O código deve ser compilado com as seguintes flags:
```cc -Wall -Wextra -Werror -D BUFFER_SIZE=42 <files>.c```


Você deve garantir que o código funcione corretamente para diferentes valores de BUFFER_SIZE, como 1, 42, 9999, ou até 10000000.

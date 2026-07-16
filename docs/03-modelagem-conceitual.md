# Modelagem Conceitual do Traça

## Entidades do MVP

### Usuário
- id
- nome
- email
- senha

### Livro
- id
- titulo
- autor
- numeroPaginas
- capa
- sinopse
- genero
- isbn

### Leitura
- id
- usuario
- livro
- paginaAtual
- status
- dataInicio
- dataFim

## Relacionamentos

Usuário (1) ---- (N) Leitura
Livro (1) ------ (N) Leitura

## Regras de Negócio

1. A página atual não pode ultrapassar o número de páginas do livro.
2. O usuário pode corrigir a página atual para um valor menor.
3. Ao atingir a última página, o status muda automaticamente para Concluído.
4. Um usuário pode ter várias leituras ativas de livros diferentes.
5. Não é permitido ter duas leituras ativas do mesmo livro para o mesmo usuário.
6. Ao adicionar um livro, a leitura é criada com status Quero Ler e página atual 0.
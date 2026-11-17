# 1. Introdução
Esta atividade define e testa em JavaScript as regras de um Sudoku Binário de 6 × 6 casas. Os testes automatizados verificam o formato do tabuleiro, a distribuição dos zeros e uns, a ausência de sequências de três símbolos iguais e a unicidade de linhas e colunas.
# 2. Regras de negócio
# RN01 — Dimensões. O tabuleiro deve ter exatamente 6 linhas e 6 colunas.
# RN02 — Símbolos. Cada casa contém 0, 1 ou fica vazia durante o preenchimento.
# RN03 — Equilíbrio das linhas. Cada linha completa deve conter exatamente três zeros e três uns.
# RN04 — Equilíbrio das colunas. Cada coluna completa deve conter exatamente três zeros e três uns.
# RN05 — Sem trincas horizontais. Não pode haver três zeros ou três uns consecutivos numa linha.
# RN06 — Sem trincas verticais. Não pode haver três zeros ou três uns consecutivos numa coluna.
# RN07 — Linhas únicas. Linhas completas não podem ser iguais entre si.
# RN08 — Colunas únicas. Colunas completas não podem ser iguais entre si.
# RN09 — Solução completa. Para validar uma solução final, todas as casas devem estar preenchidas e as regras acima devem ser respeitadas.
# RN10 — Estado parcial. Durante o preenchimento, casas vazias são permitidas, mas conflitos já presentes — como excesso de um símbolo ou três iguais consecutivos — devem ser rejeitados.
# 3. Casos de teste

# CT01
Criar um tabuleiro vazio
Seis linhas e seis colunas, com casas inicialmente vazias
# CT02
Validar uma solução correta
Aceitar a grade completa
# CT03
Verificar equilíbrio de uma linha
Rejeitar linha com sequência de três símbolos iguais
# CT04
Verificar equilíbrio de uma coluna
Rejeitar coluna que exceda a quantidade permitida
# CT05
Inserir três símbolos iguais consecutivos numa linha
Rejeitar o tabuleiro
# CT06
Inserir três símbolos iguais consecutivos numa coluna
Rejeitar o tabuleiro
# CT07
Duplicar uma linha completa
Rejeitar o tabuleiro
# CT08
Duplicar uma coluna completa
Rejeitar o tabuleiro
# CT09
Inserir um símbolo inválido
Rejeitar valor diferente de 0, 1 ou casa vazia
# CT10
Criar tabuleiro com dimensão incorreta
Rejeitar o tabuleiro
# CT11
Validar solução ainda incompleta
Rejeitar como solução final
# CT12
Validar tabuleiro parcial sem conflitos
Aceitar como estado parcial
# CT13
Exceder zeros ou uns numa linha parcial
Rejeitar o estado parcial
# CT14
Criar tabuleiros independentes
Garantir que alterar um não modifica o outro
# 4. Execução dos testes
Os testes usam o runner integrado ao Node.js, sem dependências externas. Execute node --test test/*.test.js na pasta do projeto. Os 14 testes passaram.

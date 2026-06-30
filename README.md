# SISTEMA-DE-SORTEIO-DE-AMIGO-SECRETO

Este projeto consiste em uma aplicação interativa para a realização de 
sorteios de Amigo Secreto. A aplicação permite a inserção dinâmica de 
nomes, valida a duplicidade e campos vazios, gerencia a listagem visual, 
e realiza o sorteio de forma aleatória e circular (garantindo que todos 
tiram e sejam tirados por alguém sem repetições ou auto-sorteio), com a 
opção de reiniciar o fluxo completamente.

------------------------------------------------------------------------
1. FUNCIONALIDADES PRINCIPAIS
------------------------------------------------------------------------
* Validação de Entrada: Impede a inserção de strings vazias ou nomes que 
  já foram adicionados anteriormente na lista.
* Listagem em Tempo Real: Atualiza dinamicamente a exibição dos nomes no 
  HTML conforme são inseridos, limpando o campo de texto automaticamente.
* Sorteio Circular Aleatório: Utiliza o algoritmo de Fisher-Yates para 
  embaralhar o array de participantes e monta a estrutura de pares onde 
  o último participante fecha o ciclo tirando o primeiro.
* Trava de Segurança: Exige um quórum mínimo de pelo menos 4 amigos para 
  permitir a execução estável do sorteio.
* Reinicialização de Estado: Limpa o array interno e limpa as listas de 
  exibição e de resultados no DOM, retornando ao estado inicial.

------------------------------------------------------------------------
2. ESTRUTURA DO CÓDIGO JAVASCRIPT
------------------------------------------------------------------------
* `amigos` (Variável Global): Array que armazena as strings dos nomes.
* `adicionar()`: Captura o valor do input, executa validações, adiciona 
  o nome ao array e atualiza o texto do elemento HTML.
* `embaralha(lista)`: Função utilitária que implementa o embaralhamento 
  de arrays usando atribuição via destructuring.
* `sortear()`: Valida o número mínimo de elementos, embaralha a lista, 
  percorre o array montando as strings de correspondência e injeta o 
  resultado formatado no HTML.
* `reiniciar()`: Reseta o array `amigos` e limpa o conteúdo interno (`innerHTML`) 
  dos containers de exibição.

------------------------------------------------------------------------
3. TECNOLOGIAS UTILIZADAS
------------------------------------------------------------------------
* 🟡 JavaScript (ES6+) - Lógica de validação, embaralhamento e manipulação do DOM.
* 🌐 HTML5 - Estruturação dos elementos de input, botões e containers de exibição.
* 🎨 CSS3 - Estilização e layout da interface de sorteio.

------------------------------------------------------------------------
4. REFERÊNCIA DO PROJETO
------------------------------------------------------------------------
Este projeto foi desenvolvido com base no seguinte treinamento:
* Instituição: Alura
* Curso: Lógica de programação: Praticando com desafios


# Criado para fins educacionais e consolidação de lógica e manipulação de DOM.

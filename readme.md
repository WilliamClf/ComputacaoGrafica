# DVD Bounce — Simulação de Colisão com Pygame

## Descrição

Este projeto implementa uma simulação gráfica em Python utilizando a biblioteca Pygame. Dois textos são exibidos em uma janela e se movimentam continuamente pela tela, reagindo a colisões com as bordas e entre si.

A proposta é demonstrar conceitos básicos de movimentação, detecção de colisão e organização modular de código.

---

## Objetivos do Projeto

- Simular movimentação bidimensional com velocidade inicial aleatória  
- Detectar colisão com os limites da janela  
- Detectar colisão entre dois objetos  
- Alterar dinamicamente direção, velocidade e cor após colisões  
- Estruturar o código de forma modular e reutilizável  

---

## Funcionamento

Ao executar o programa, é aberta uma janela de 800x600 pixels contendo dois textos.

Cada texto:

- Recebe uma velocidade inicial aleatória (nunca nula)  
- Move-se continuamente na tela  
- Altera sua direção ao atingir qualquer borda  
- Muda de cor quando ocorre colisão  
- Troca sua velocidade com o outro texto ao colidir  

A troca de velocidades cria um efeito simples de impacto, simulando a transferência de movimento entre dois corpos.

---

## Estrutura do Código

O código foi organizado em funções com responsabilidades bem definidas:

### 1. Geração de Velocidade

Função responsável por criar velocidades aleatórias válidas, garantindo que o objeto nunca permaneça parado.

### 2. Geração de Cor

Retorna valores RGB aleatórios utilizados para atualizar a aparência dos textos após colisões.

### 3. Criação dos Objetos de Texto

Encapsula:

- Renderização do texto  
- Definição da posição inicial  
- Criação da área de colisão (`rect`)  

### 4. Tratamento de Colisão com Bordas

Verifica se o objeto ultrapassou os limites da janela e, quando necessário:

- Ajusta a direção do movimento  
- Gera uma nova cor  

### 5. Loop Principal

Responsável por:

- Inicializar o Pygame  
- Criar a janela  
- Controlar o ciclo de atualização  
- Atualizar posições  
- Detectar colisões  
- Renderizar os elementos na tela  

---

## Conceitos Demonstrados

- Manipulação de retângulos para colisão (`colliderect`)  
- Controle de frame rate  
- Atualização contínua de estado em loop principal  
- Separação de responsabilidades em funções  
- Uso prático da biblioteca Pygame  

---

## Como Executar

1. Instale a biblioteca necessária:

pip install pygame

2. Execute o arquivo principal:

python main.py

## Finalidade

Este projeto serve como base introdutória para desenvolvimento de jogos e simulações interativas, podendo ser expandido para incluir múltiplos objetos, física mais elaborada ou controle por entrada do usuário.
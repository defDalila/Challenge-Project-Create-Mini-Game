<link rel="stylesheet" type='text/css' href="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/devicon.min.css" />
          
 ### ![Static Badge](https://img.shields.io/badge/status-em_desenvolvimento-cyan)         

# :dart: Desafio de Projeto: Criar um Mini Game


> Este repositório contém um projeto desenvolvido no módulo de treinamento de introdução ao C# da [Microsoft Learn](https://learn.microsoft.com/). Este projeto está dentro dos requisitos de qualificação para o Exame de Certificação `Foundational C#`.
>
> Objetivos de Aprendizagem:
>> - Use o Visual Studio Code para desenvolver um aplicativo de console em C# que use métodos para implementar fluxos de trabalho lógicos.
>> - Entenda o código existente e faça alterações de design fundamentadas em dados.
>> - Crie valores retornados, bem como parâmetros obrigatórios e opcionais em métodos.

         
          
<br>

## :beginner: Contexto

Você deverá desenvolver um mini-jogo pequeno. Seu aplicativo deve estabelecer as noções básicas do jogo, incluindo atualizar o estado do jogador, manipular o movimento do jogador e consumir e regenerar um objeto de alimento.

<br>

## :gear: Especificação do Projeto

O [Projeto de Código Starter](https://github.com/MicrosoftLearning/Challenge-project-Create-methods-in-CSharp/archive/refs/heads/main.zip) contém os seguintes recursos:

<br>

:hash:&emsp;**O código declara as seguintes variáveis:**
- Variáveis para determinar o tamanho da janela do Terminal.
- Variáveis para rastrear as localizações do jogador e da comida.
- Arrays `states` e `foods` para fornecer as aparências disponíveis do jogador e da comida.
- Variáveis para rastrear a aparência atual do jogador e da comida.

<br>

:hash:&emsp;**O código fornece os seguintes métodos:**
- Um método para determinar se a janela do Terminal foi redimensionada.
- Um método para exibir uma aparência de comida aleatória em uma localização aleatória.
- Um método que altera a aparência do jogador para combinar com a comida consumida.
- Um método que congela temporariamente o movimento do jogador.
- Um método que move o jogador de acordo com a entrada direcional.
- Um método que configura o estado inicial do jogo.

<br>

:hash:&emsp;**O código não chama os métodos corretamente para tornar o jogo jogável. As seguintes funcionalidades estão faltando:**
- Código para determinar se o jogador consumiu a comida exibida.
- Código para determinar se a comida consumida deve congelar o movimento do jogador.
- Código para determinar se a comida consumida deve aumentar o movimento do jogador.
- Código para aumentar a velocidade de movimento.
- Código para redisplay a comida após ser consumida pelo jogador.
- Código para terminar a execução se uma tecla não suportada for pressionada.
- Código para terminar a execução se o terminal foi redimensionado.

<br>

## :computer: Implementações

### :hammer_and_wrench: ***Adicionar código para encerrar o jogo***

Atualizar o código existente para dar suporte a uma opção para encerrar a jogabilidade se um caractere não direcional for inserido. O jogo deve ser encerrado se a janela do terminal foi redimensionada. É necessário localizar os métodos corretos para utilizar no código.

:bookmark_tabs:&emsp;**Este recurso deve:**

- Determinar se o terminal foi redimensionado antes de permitir que o jogo continue
- Limpar o Console e encerrar o jogo se o terminal tiver sido redimensionado
- Exibir a seguinte mensagem antes de encerrar o programa: `Console was resized. Program exiting.`
- Modificar o método `Move` existente para dar suporte a um parâmetro opcional
- Se habilitado, o parâmetro opcional deverá detectar a entrada de uma chave não direcional
- Se uma entrada não direcional for detectada, faça com que o jogo seja encerrado

<br>

:white_check_mark:&emsp;**Para validar se o código atende aos requisitos especificados, deve-se executar as seguintes etapas:**

1. Habilite o parâmetro opcional.
1. No prompt de comando do Terminal, redimensione a janela.
1. Insira uma tecla direcional.
1. Verifique se o programa termina depois de exibir a seguinte mensagem: `Console was resized. Program exiting.`
1. Execute o aplicativo novamente.
1. No prompt de comando do terminal, pressione as teclas direcionais para mover o jogador.
1. Pressione uma tecla não direcional.
1. Verifique se o programa é encerrado.
1. Desabilite o parâmetro opcional, depois compile e execute o aplicativo.
1. No prompt de comando do terminal, pressione as teclas direcionais para mover o jogador.
1. Pressione uma tecla não direcional.
1. Verifique se o programa continua.
1. Redimensione a janela do Terminal.
1. Verifique se o programa é encerrado.

<br>

### :hammer_and_wrench: ***Adicionar código que faz jogador consumir alimentos***

Criar um método que determine se o jogador consumiu os alimentos que foram exibidos. Se o alimento foi consumido, a aparência do jogador deve ser atualizada e reexibir o alimento.

:bookmark_tabs:&emsp;**Para este recurso é necessário:**

- Criar um método que usa as variáveis existentes de posicionamento do player e do alimento
- O método deve retornar um valor
- Depois que o usuário mover o personagem, chame seu método para determinar o seguinte:
    - Se deve ou não usar o método existente que altera a aparência do jogador
    - Se deve ou não usar o método existente para reexibir o alimento

<br>

:white_check_mark:&emsp;**Para validar se o código atende aos requisitos especificados, deve-se executar as seguintes etapas:**

1. No prompt de comando do terminal, pressione as teclas direcionais para mover o jogador.
1. Mova o jogador pela cadeia de caracteres de comida exibida.
1. Verifique se uma nova cadeia de caracteres de alimentos é exibida.
1. Verifique se a aparência do jogador muda dependendo de qual cadeia de caracteres de alimentos foi consumida.

<br>

### :hammer_and_wrench: ***Adicionar código para modificar a movimentaçao***

Criar um método que determine se o jogador consumiu os alimentos que afetam a movimentação dele. Quando o jogador consome a cadeia de caracteres de alimentos com valor `#####`, a aparência é atualizada para `(X_X)`. Você adicionará um recurso para detectar se a aparência do jogador é `(X_X)` e, em caso afirmativo, impedirá temporariamente a movimentação do jogador.

Adicionar um recurso opcional que detecte se a aparência do jogador é `(^-^)` e, em caso afirmativo, aumente ou diminua as velocidades de movimento direita e esquerda em `3` unidades enquanto essa aparência estiver ativa. Quando o estado do jogador for `('-')`, a velocidade deve voltar ao normal. Você deve tornar esse recurso opcional, pois consumir alimentos nesse estado requer mais detecção de colisão do que você pretende desenvolver nesse momento.

<br>

:bookmark_tabs:&emsp;**Para este recurso é necessário:**

- Criar um método que verifica se a aparência atual do jogador é `(X_X)`
- O método deve retornar um valor
- Antes de permitir que o usuário mova o personagem, chame o método para determinar o seguinte:
- Se deve ou não usar o método existente que congela o movimento do personagem
- Verificar se o personagem está congelado apenas temporariamente e se ainda consegue se mover posteriormente
- Modificar o método Move existente para dar suporte a um parâmetro opcional de velocidade do movimento
- Use o parâmetro para aumentar ou diminuir a velocidade de movimento à direita e à esquerda em 3 unidades
- Criar um método que verifica se a aparência atual do jogador é `(^-^)`
- O método deve retornar um valor
- Chame seu método para determinar se Move deve usar o parâmetro de velocidade de movimentação

<br>

:white_check_mark:&emsp;**Para validar se o código atende aos requisitos especificados, deve-se executar as seguintes etapas:**

1. Habilite os parâmetros opcionais.
1. No prompt de comando do terminal, pressione as teclas direcionais para mover o jogador.
1. Mova o jogador pela cadeia de caracteres de comida exibida.
1. Verifique se uma nova cadeia de caracteres de alimentos é exibida.
1. Verifique se a aparência do jogador muda dependendo de qual cadeia de caracteres de alimento foi consumida.
1. Verifique se a movimentação é temporariamente interrompida quando a aparência do jogador é `(X_X)`.
1. Verifique se o movimento à esquerda e à direita é mais rápido nas direções corretas quando a aparência do jogador é `(^-^)`.
1. Pressione uma tecla não direcional para encerrar o programa.
1. Desabilite o parâmetro de velocidade de movimentação opcional e execute novamente o aplicativo.
1. Verifique se o movimento é normal quando a aparência do jogador é `(^-^)`.

<br>

## <p align="center"><i class="devicon-csharp-plain-wordmark colored"></i> <i class="devicon-vscode-plain colored"></i> <i class="devicon-git-plain colored"></i>  <i class="devicon-github-original colored"></i></p>
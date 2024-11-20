# Desafio de Projeto: Criar um Mini Game :dart:

> Este repositório contém um projeto desenvolvido no módulo de treinamento de introdução ao C# da [Microsoft Learn](https://learn.microsoft.com/). Este projeto está dentro dos requisitos necessários de qualificação para o Exame de Certificação `Foundational C#`.
>
> Objetivos de Aprendizagem:
>> - Use o Visual Studio Code para desenvolver um aplicativo de console em C# que use métodos para implementar fluxos de trabalho lógicos.
>> - Entenda o código existente e faça alterações de design fundamentadas em dados.
>> - Crie valores retornados, bem como parâmetros obrigatórios e opcionais em métodos.

<br>

## :beginner: Contexto

Você deverá desenvolver um mini-jogo pequeno. Seu aplicativo deve estabelecer as noções básicas do jogo, incluindo atualizar o estado do jogador, manipular o movimento do jogador e consumir e regenerar um objeto de alimento.

<br>

## :wrench: Especificação do Projeto

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

- Adicionar código para encerrar o jogo;
- Adicionar código que faz jogador consumir alimentos
- Adicionar código para modificar a movimentaçao;
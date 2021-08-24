---
title: Animações do Microsoft Agent para o caractere Dey
description: Animações do Microsoft Agent para o caractere Dey
ms.assetid: 05baf1ab-3217-4da4-9562-6719c58cd744
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ef6cf0fc3d44f9783fe3d22f9f0d2b291e6acc51bd5bb72890af793ffe55156
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609096"
---
# <a name="microsoft-agent-animations-for-robby-character"></a>Animações do Microsoft Agent para o caractere Dey

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O [Caractere DeIay do Microsoft Agent](https://www.microsoft.com/downloads/details.aspx?FamilyID=fa36d1d5-d828-494a-ad0a-7b571db5bd2e) é um trabalho protegido por direitos autorais Microsoft Corporation.

Ela dá suporte às animações listadas na tabela a seguir. Consulte [Programando a Interface do Servidor do Microsoft Agent](/windows/desktop/lwef/programming-the-microsoft-agent-server-interface) e [Programando o Controle do Microsoft Agent](programming-the-microsoft-agent-control.md) para obter informações sobre como chamar animações do caractere.

Se você estiver acessando essas animações de caractere usando o [](/windows/desktop/lwef/iagentcharacter--prepare) protocolo HTTP e o método [**Get**](get-method.md) ou Prepare do servidor do controle, considere como baixá-las. Em vez de baixar todas as animações de  uma  só vez, talvez você queira recuperar as animações de estado Mostrando e Falando primeiro. Isso permitirá que você exibir o caractere rapidamente e fazer com que ele fale, ao mesmo tempo que baixa outras animações de forma assíncrona. Além disso, para garantir que os dados de animação e caracteres carreguem com êxito, use [**o evento RequestComplete.**](requestcomplete-event.md) Se uma solicitação de carga falhar, você poderá tentar carregar novamente os dados ou exibir uma mensagem apropriada.

Se a animação **Return** de uma animação for definida usando branches exit, você não precisará chamá-la explicitamente; O Agent reproduz automaticamente a **animação Return** antes da próxima animação. No entanto, se uma **animação** Return estiver listada, você deverá chamar a animação usando o método [**Play**](play-method.md) antes de outra animação para fornecer uma transição suave. Se nenhuma **animação** return for listada, a animação normalmente terminará sem a necessidade de uma animação de transição.

O arquivo de caracteres inclui efeitos de som para algumas animações, conforme notado na tabela a seguir. Os efeitos de som só reproduzirão se essa opção estiver habilitada na folha de propriedades do Microsoft Agent. Você também pode desabilitar efeitos de som em seu aplicativo.



| Animação                 | Animação de retorno         | Dá suporte à fala | Efeitos de som | Atribuído ao Estado                            | Descrição                                                |
|---------------------------|--------------------------|-------------------|---------------|----------------------------------------------|------------------------------------------------------------|
| **Reconhecer**           | Nenhum                     | Não                | **Não**        | Nenhum                                         | Nods head                                                  |
| **Alerta**                 | Sim, usando branches exit | Sim               | **Não**        | **Ouvir**                                | Endireita                                                |
| **Anunciar**              | Sim, usando branches exit | Sim               | **Sim**       | Nenhum                                         | Imprime papel e relatórios                               |
| **Blink**                 | Nenhum                     | Não                | **Não**        | **IdlingLevel1** **IdlingLevel2**<br/> | Pisca os olhos                                                |
| **Confuso**              | Sim, usando branches exit | Sim               | **Não**        | Nenhum                                         | Cabeça de rascunhos                                             |
| **Felicitar**          | Sim, usando branches exit | Sim               | **Não**        | Nenhum                                         | Em seguida, eleva as mãos e, em seguida, a mão dele                             |
| **Recusar**               | Sim, usando branches exit | Sim               | **Não**        | Nenhum                                         | Eleva a mão e treme a cabeça                                |
| **DoMagic1**              | Nenhum                     | Sim               | **Não**        | Nenhum                                         | Remove o dispositivo                                             |
| **DoMagic2**              | Sim, usando branches exit | Não                | **Sim**       | Nenhum                                         | Pressiona o botão e o botão é exibido                            |
| **DontRecognize**         | Sim, usando branches exit | Sim               | **Não**        | Nenhum                                         | Mantém a mão para o ouvido                                          |
| **Explicar**               | Sim, usando branches exit | Sim               | **Não**        | Nenhum                                         | Gestos com os braços                                         |
| **GestureDown**           | Sim, usando branches exit | Sim               | **Não**        | **GesturingDown**                            | Gestos para baixo                                              |
| **GestureLeft**           | Sim, usando branches exit | Sim               | **Não**        | **GesturingLeft**                            | Gestos à esquerda                                              |
| **GestureRight**          | Sim, usando branches exit | Sim               | **Não**        | **GesturingRight**                           | Gestos à direita                                             |
| **GestureUp**             | Sim, usando branches exit | Sim               | **Não**        | **GesturingUp**                              | Gestos para cima                                                |
| **GetAttention**          | **GetAttentionReturn**   | Sim               | **Não**        | Nenhum                                         | Mãos de ondas                                                 |
| **GetAttentionContinued** | **GetAttentionReturn**   | Sim               | **Não**        | Nenhum                                         | Mãos de ondas novamente                                           |
| **GetAttentionReturn**    | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                                |
| **Saudar**                 | Sim, usando branches exit | Sim               | **Não**        | Nenhum                                         | Mantém a mão                                              |
| **Escuta \_ 1**            | Sim, usando branches exit | Não                | **Não**        | **Audição**                                  | Inclina a cabeça para a direita \* (animação em loop)                     |
| **Escuta \_ 2**            | Sim, usando branches exit | Não                | **Não**        | **Audição**                                  | Inclina a cabeça para a esquerda \* (animação em loop)                      |
| **Escuta \_ 3**            | Sim, usando branches exit | Não                | **Não**        | **Audição**                                  | Cabecinha à esquerda \* (animação em loop)                      |
| **Escuta \_ 4**            | Sim, usando branches exit | Não                | **Não**        | **Audição**                                  | Inclina a cabeça para baixo \* (animação em loop)                      |
| **Ocultar**                  | Nenhum                     | Não                | **Sim**       | **Escondendo**                                   | Desaparece por meio da porta                                    |
| **Idle1 \_ 1**              | Nenhum                     | Não                | **Não**        | **IdlingLevel1** **IdlingLevel2**<br/> | Relances para a direita                                              |
| **Idle1 \_ 2**              | Nenhum                     | Não                | **Não**        | **IdlingLevel1** **IdlingLevel2**<br/> | Relance e pisque                                      |
| **Idle1 \_ 3**              | Nenhum                     | Não                | **Não**        | **IdlingLevel1** **IdlingLevel2**<br/> | Relance para baixo e pisca                                    |
| **Idle1 \_ 4**              | Nenhum                     | Não                | **Não**        | **IdlingLevel1** **IdlingLevel2**<br/> | Relance à esquerda e pisca                                    |
| **Idle2 \_ 1**              | Nenhum                     | Não                | **Não**        | **IdlingLevel2**                             | Dobra os braços                                                 |
| **Idle2 \_ 2**              | Nenhum                     | Não                | **Sim**       | **IdlingLevel2**                             | Remove a cabeça e faz o ajuste                          |
| **Idle3 \_ 1**              | Nenhum                     | Não                | **Não**        | **IdlingLevel3**                             | Bocejos                                                      |
| **Idle3 \_ 2**              | Nenhum                     | Não                | **Sim**       | **IdlingLevel3**                             | Desliga                                                 |
| **LookDown**              | **LookDownReturn**       | Não                | **Não**        | Nenhum                                         | Procura para baixo                                                 |
| **LookDownReturn**        | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                                |
| **LookLeft**              | **LookLeftReturn**       | Não                | **Não**        | Nenhum                                         | Parece à esquerda                                                 |
| **LookLeftReturn**        | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                                |
| **LookRight**             | **LookRightReturn**      | Não                | **Não**        | Nenhum                                         | Parece à direita                                                |
| **LookRightReturn**       | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                                |
| **Pesquisa**                | **LookUpReturn**         | Não                | **Não**        | Nenhum                                         | Procura                                                   |
| **LookUpReturn**          | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                                |
| **Movedown**              | Sim, usando branches exit | Não                | **Sim**       | **MovingDown**                               | Reba de 1000                                                 |
| **Moveleft**              | Sim, usando branches exit | Não                | **Sim**       | **MovingLeft**                               | Solão esquerda                                                 |
| **Moveright**             | Sim, usando branches exit | Não                | **Sim**       | **MovingRight**                              | Direito do mundo                                                |
| **MoveUp**                | Sim, usando branches exit | Não                | **Sim**       | **MovingUp**                                 | Up up                                                   |
| **Satisfeito**               | Sim, usando branches exit | Sim               | **Sim**       | Nenhum                                         | Sorrisos e sorrisos                                  |
| **Processo**               | Não                       | Não                | **Sim**       | Nenhum                                         | Pressiona botões, imprime, lê e, em seguida, lança a impressão       |
| **Processing**            | Sim, usando branches exit | Não                | **Sim**       | Nenhum                                         | Pressiona botões, imprime, lê e, em seguida, lança a impressão       |
| **Ler**                  | **ReadReturn**           | Sim               | **Sim**       | Nenhum                                         | Imprime, lê e procura                                |
| **ReadContinued**         | **ReadReturn**           | Sim               | **Sim**       | Nenhum                                         | Lê e procura                                         |
| **ReadReturn**            | Nenhum                     | Não                | **Sim**       | Nenhum                                         | Retorna para a posição neutra                                |
| **Lendo**               | Sim, usando branches exit | Não                | **Sim**       | Nenhum                                         | Imprime, lê e procura \* (animação em loop)          |
| **RestPose**              | Nenhum                     | Sim               | **Não**        | **Falando**                                 | Posição neutra                                           |
| **Triste**                   | Sim, usando branches exit | Sim               | **Não**        | Nenhum                                         | Expressão triste                                             |
| **Pesquisar**                | Não                       | Não                | **Sim**       | Nenhum                                         | Revela a caixa de ferramentas e remove a ferramenta                           |
| **Procurando**             | Sim, usando branches exit | Não                | **Sim**       | Nenhum                                         | Revela a caixa de ferramentas e remove ferramentas \* (animação em loop)    |
| **Mostrar**                  | Nenhum                     | Não                | **Sim**       | **Mostrando**                                  | Aparece por meio da porta                                    |
| **Startlistening**        | Sim, usando branches exit | Sim               | **Não**        | Nenhum                                         | Coloca a mão no ouvido                                           |
| **Stoplistening**         | Sim, usando branches exit | Sim               | **Não**        | Nenhum                                         | Coloca as mãos sobre os olhos                                       |
| **Sugerir**               | Sim, usando branches exit | Sim               | **Sim**       | Nenhum                                         | Exibe a lâmpada                                         |
| **Surpreso**             | Sim, usando branches exit | Sim               | **Não**        | Nenhum                                         | Parece estar surpresa                                            |
| **Pensar**                 | Sim, usando branches exit | Sim               | **Sim**       | Nenhum                                         | Cabeça de rascunhos                                             |
| **Processando dados**              | Não                       | Não                | **Sim**       | Nenhum                                         | Cabeça de rascunho \* (animação em loop)                       |
| **Incerto**             | Sim, usando branches exit | Sim               | **Não**        | Nenhum                                         | Shrugs                                                     |
| **Onda**                  | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Ondas                                                      |
| **Gravar**                 | **WriteReturn**          | Sim               | **Sim**       | Nenhum                                         | Revela lápis e área de transferência, gravações e pesquisa          |
| **WriteContinued**        | **WriteReturn**          | Sim               | **Sim**       | Nenhum                                         | Gravações e pesquisa                                        |
| **WriteReturn**           | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                                |
| **Gravando**               | Sim, usando branches de saída | Não                | **Sim**       | Nenhum                                         | Revela lápis e área de transferência, gravações ( \* animação em loop) |



 

\* Se você reproduzir uma animação de looping, deverá usar [**parar**](stop-method.md) para limpá-la antes que outras animações na fila do caractere sejam reproduzidas.

 


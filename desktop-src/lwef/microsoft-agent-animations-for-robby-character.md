---
title: Animações do Microsoft Agent para o caractere Robby
description: Animações do Microsoft Agent para o caractere Robby
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
# <a name="microsoft-agent-animations-for-robby-character"></a>Animações do Microsoft Agent para o caractere Robby

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O [Microsoft Agent Robby Character](https://www.microsoft.com/downloads/details.aspx?FamilyID=fa36d1d5-d828-494a-ad0a-7b571db5bd2e) é um trabalho com direitos autorais da Microsoft Corporation.

O Robby dá suporte às animações listadas na tabela a seguir. Consulte [programando a interface do servidor do Microsoft Agent](/windows/desktop/lwef/programming-the-microsoft-agent-server-interface) e [programando o controle do Microsoft Agent](programming-the-microsoft-agent-control.md) para obter informações sobre como chamar as animações do caractere.

Se estiver acessando essas animações de caracteres usando o protocolo HTTP e o método de [**preparação**](/windows/desktop/lwef/iagentcharacter--prepare) do servidor [**Get**](get-method.md) ou do controle, considere como você os baixará. Em vez de baixar todas as animações de uma só vez, talvez você queira recuperar as animações de **estado de apresentação e de** **fala** primeiro. Isso permitirá que você exiba o caractere rapidamente e o leia enquanto estiver desativando as outras animações de forma assíncrona. Além disso, para garantir que os dados de caractere e animação sejam carregados com êxito, use o evento [**RequestComplete**](requestcomplete-event.md) . Se uma solicitação de carregamento falhar, você poderá tentar carregar os dados novamente ou exibir uma mensagem apropriada.

Se a animação de **retorno** de uma animação for definida usando ramificações de saída, você não precisará chamá-la explicitamente; O agente reproduz automaticamente a animação de **retorno** antes da próxima animação. No entanto, se uma animação de **retorno** for listada, você deverá chamar a animação usando o método [**Play**](play-method.md) antes de outra animação para fornecer uma transição suave. Se nenhuma animação de **retorno** for listada, a animação normalmente terminará sem a necessidade de uma animação de transição.

O arquivo de caractere inclui efeitos sonoros para algumas animações, conforme observado na tabela a seguir. Os efeitos sonoros só serão executados se essa opção estiver habilitada na folha de propriedades do Microsoft Agent. Você também pode desabilitar efeitos de som em seu aplicativo.



| Animação                 | Retornar animação         | Dá suporte à fala | Efeitos de som | Atribuído ao estado                            | Descrição                                                |
|---------------------------|--------------------------|-------------------|---------------|----------------------------------------------|------------------------------------------------------------|
| **Reconhecer**           | Nenhum                     | Não                | **Não**        | Nenhum                                         | Cabeçalho do nós nesta                                                  |
| **Alerta**                 | Sim, usando branches de saída | Sim               | **Não**        | **Detecta**                                | Retificações                                                |
| **Nascimento**              | Sim, usando branches de saída | Sim               | **Sim**       | Nenhum                                         | Imprime papel e relatórios                               |
| **Blink**                 | Nenhum                     | Não                | **Não**        | **IdlingLevel1** **IdlingLevel2**<br/> | Olhos pisca                                                |
| **Confuso**              | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Cabeça de rascunhos                                             |
| **Parabenizar**          | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Levanta mãos claspss                             |
| **Recusar**               | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Cabeça levantada e agita                                |
| **DoMagic1**              | Nenhum                     | Sim               | **Não**        | Nenhum                                         | Remove o dispositivo                                             |
| **DoMagic2**              | Sim, usando branches de saída | Não                | **Sim**       | Nenhum                                         | O botão e o feixe são exibidos                            |
| **DontRecognize**         | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Contém mão para Ear                                          |
| **Explicar**               | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Gestos com braços                                         |
| **GestureDown**           | Sim, usando branches de saída | Sim               | **Não**        | **GesturingDown**                            | Gestos para baixo                                              |
| **GestureLeft**           | Sim, usando branches de saída | Sim               | **Não**        | **GesturingLeft**                            | Gestos restantes                                              |
| **GestureRight**          | Sim, usando branches de saída | Sim               | **Não**        | **GesturingRight**                           | Gestos para a direita                                             |
| **GestureUp**             | Sim, usando branches de saída | Sim               | **Não**        | **GesturingUp**                              | Gestos para cima                                                |
| **Getatenção**          | **GetAttentionReturn**   | Sim               | **Não**        | Nenhum                                         | Braços de ondas                                                 |
| **GetAttentionContinued** | **GetAttentionReturn**   | Sim               | **Não**        | Nenhum                                         | Braços de ondas novamente                                           |
| **GetAttentionReturn**    | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                                |
| **Saudar**                 | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Tem a mão                                              |
| **Audição \_ 1**            | Sim, usando branches de saída | Não                | **Não**        | **Audição**                                  | Cabeça de inclinação para a direita ( \* animação em loop)                     |
| **Audição \_ 2**            | Sim, usando branches de saída | Não                | **Não**        | **Audição**                                  | Cabeça inclinada para a esquerda ( \* animação em loop)                      |
| **Audição \_ 3**            | Sim, usando branches de saída | Não                | **Não**        | **Audição**                                  | Cocks do cabeçalho esquerdo ( \* animação em loop)                      |
| **Audição \_ 4**            | Sim, usando branches de saída | Não                | **Não**        | **Audição**                                  | Inclinação da cabeça para baixo ( \* animação em loop)                      |
| **Ocultar**                  | Nenhum                     | Não                | **Sim**       | **Ocultar**                                   | Desaparece por meio da porta                                    |
| **Idle1 \_ 1**              | Nenhum                     | Não                | **Não**        | **IdlingLevel1** **IdlingLevel2**<br/> | Resumos à direita                                              |
| **Idle1 \_ 2**              | Nenhum                     | Não                | **Não**        | **IdlingLevel1** **IdlingLevel2**<br/> | Visão geral e intermitências                                      |
| **Idle1 \_ 3**              | Nenhum                     | Não                | **Não**        | **IdlingLevel1** **IdlingLevel2**<br/> | Visão geral e intermitências                                    |
| **Idle1 \_ 4**              | Nenhum                     | Não                | **Não**        | **IdlingLevel1** **IdlingLevel2**<br/> | Resumos à esquerda e piscar                                    |
| **Idle2 \_ 1**              | Nenhum                     | Não                | **Não**        | **IdlingLevel2**                             | Braços de dobra                                                 |
| **Idle2 \_ 2**              | Nenhum                     | Não                | **Sim**       | **IdlingLevel2**                             | Remove o cabeçalho e faz o ajuste                          |
| **Idle3 \_ 1**              | Nenhum                     | Não                | **Não**        | **IdlingLevel3**                             | Bocejos                                                      |
| **Idle3 \_ 2**              | Nenhum                     | Não                | **Sim**       | **IdlingLevel3**                             | Desliga                                                 |
| **LookDown**              | **LookDownReturn**       | Não                | **Não**        | Nenhum                                         | Pesquisa                                                 |
| **LookDownReturn**        | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                                |
| **LookLeft**              | **LookLeftReturn**       | Não                | **Não**        | Nenhum                                         | Parece com a esquerda                                                 |
| **LookLeftReturn**        | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                                |
| **LookRight**             | **LookRightReturn**      | Não                | **Não**        | Nenhum                                         | Parece com a direita                                                |
| **LookRightReturn**       | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                                |
| **Busca**                | **LookUpReturn**         | Não                | **Não**        | Nenhum                                         | Pesquisa                                                   |
| **LookUpReturn**          | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                                |
| **MoveDown**              | Sim, usando branches de saída | Não                | **Sim**       | **MovingDown**                               | Voa para baixo                                                 |
| **MoveLeft**              | Sim, usando branches de saída | Não                | **Sim**       | **MovingLeft**                               | Surge à esquerda                                                 |
| **MoveRight**             | Sim, usando branches de saída | Não                | **Sim**       | **MovingRight**                              | Voa para a direita                                                |
| **MoveUp**                | Sim, usando branches de saída | Não                | **Sim**       | **MovingUp**                                 | Voa                                                   |
| **Satisfeito**               | Sim, usando branches de saída | Sim               | **Sim**       | Nenhum                                         | Sorrisos e se retifica                                  |
| **Processo**               | Não                       | Não                | **Sim**       | Nenhum                                         | Pressiona botões, imprime, lê e, em seguida, envia a impressão       |
| **Processing**            | Sim, usando branches de saída | Não                | **Sim**       | Nenhum                                         | Pressiona botões, imprime, lê e, em seguida, envia a impressão       |
| **Ler**                  | **ReadReturn**           | Sim               | **Sim**       | Nenhum                                         | Impressões, leituras e pesquisa                                |
| **ReadContinued**         | **ReadReturn**           | Sim               | **Sim**       | Nenhum                                         | Lê e pesquisa                                         |
| **ReadReturn**            | Nenhum                     | Não                | **Sim**       | Nenhum                                         | Retorna para a posição neutra                                |
| **Lendo**               | Sim, usando branches de saída | Não                | **Sim**       | Nenhum                                         | Impressões, leituras e pesquisa (animação em \* loop)          |
| **RestPose**              | Nenhum                     | Sim               | **Não**        | **Língua**                                 | Posição neutra                                           |
| **Triste**                   | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Expressão triste                                             |
| **Pesquisar**                | Não                       | Não                | **Sim**       | Nenhum                                         | Revela caixa de ferramentas e remove a ferramenta                           |
| **Procurar**             | Sim, usando branches de saída | Não                | **Sim**       | Nenhum                                         | Revela a caixa de ferramentas e remove ferramentas ( \* animação em loop)    |
| **Mostrar**                  | Nenhum                     | Não                | **Sim**       | **Mostrando**                                  | Aparece por meio de porta                                    |
| **StartListening**        | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Coloca mão em Ear                                           |
| **StopListening**         | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Coloca a mão sobre ouvidos                                       |
| **Sugerir**               | Sim, usando branches de saída | Sim               | **Sim**       | Nenhum                                         | Exibe lâmpada                                         |
| **Ficamos**             | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Parece surpreso                                            |
| **Pensar**                 | Sim, usando branches de saída | Sim               | **Sim**       | Nenhum                                         | Cabeça de rascunhos                                             |
| **Processando dados**              | Não                       | Não                | **Sim**       | Nenhum                                         | Cabeça de arranhões ( \* animação de looping)                       |
| **Certeza**             | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Shrugs                                                     |
| **Onda**                  | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Ondas                                                      |
| **Gravar**                 | **WriteReturn**          | Sim               | **Sim**       | Nenhum                                         | Revela lápis e área de transferência, gravações e pesquisa          |
| **WriteContinued**        | **WriteReturn**          | Sim               | **Sim**       | Nenhum                                         | Gravações e pesquisa                                        |
| **WriteReturn**           | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                                |
| **Gravando**               | Sim, usando branches de saída | Não                | **Sim**       | Nenhum                                         | Revela lápis e área de transferência, gravações ( \* animação em loop) |



 

\* Se você reproduzir uma animação de looping, deverá usar [**parar**](stop-method.md) para limpá-la antes que outras animações na fila do caractere sejam reproduzidas.

 


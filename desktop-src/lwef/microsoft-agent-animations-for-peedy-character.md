---
title: Animações do Microsoft Agent para o caractere Peedy
description: Animações do Microsoft Agent para o caractere Peedy
ms.assetid: 335d915c-9cae-4850-a6bf-66ad78d533ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8e064063b322bc6549d91b5fce35bdbc491a5a3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103641033"
---
# <a name="microsoft-agent-animations-for-peedy-character"></a>Animações do Microsoft Agent para o caractere Peedy

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O [personagem Microsoft Agent Peedy](https://www.microsoft.com/downloads/details.aspx?FamilyID=bd3c4655-79e4-4791-ab9d-abc7bbd133ef) é um trabalho protegido pela Microsoft Corporation.

Peedy oferece suporte às animações listadas na tabela a seguir. Consulte [programando a interface do servidor do Microsoft Agent](/windows/desktop/lwef/programming-the-microsoft-agent-server-interface) e [programando o controle do Microsoft Agent](programming-the-microsoft-agent-control.md) para obter informações sobre como chamar as animações do caractere.

Se estiver acessando essas animações de caracteres usando o protocolo HTTP e o método de [**preparação**](/windows/desktop/lwef/iagentcharacter--prepare) do servidor [**Get**](get-method.md) ou do controle, considere como você os baixará. Em vez de baixar todas as animações de uma só vez, talvez você queira recuperar as animações de **estado de apresentação e de** **fala** primeiro. Isso permitirá que você exiba o caractere rapidamente e o leia enquanto estiver desativando as outras animações de forma assíncrona. Além disso, para garantir que os dados de caractere e animação sejam carregados com êxito, use o evento [**RequestComplete**](requestcomplete-event.md) . Se uma solicitação de carregamento falhar, você poderá tentar carregar os dados novamente ou exibir uma mensagem apropriada.

Se a animação de **retorno** de uma animação for definida usando ramificações de saída, você não precisará chamá-la explicitamente; O agente reproduz automaticamente a animação de **retorno** antes da próxima animação. No entanto, se uma animação de **retorno** for listada, você deverá chamar a animação usando o método [**Play**](play-method.md) antes de outra animação para fornecer uma transição suave. Se nenhuma animação de **retorno** for listada, a animação normalmente terminará sem a necessidade de uma animação de transição.

Se estiver acessando essas animações de caracteres usando o protocolo HTTP e o método de [**preparação**](/windows/desktop/lwef/iagentcharacter--prepare) do servidor [**Get**](get-method.md) ou do controle, considere como você os baixará. Em vez de baixar todas as animações de uma só vez, talvez você queira recuperar as animações de **estado de apresentação e de** **fala** primeiro. Isso permitirá que você exiba o caractere rapidamente e o leia enquanto estiver desativando as outras animações de forma assíncrona. Além disso, para garantir que os dados de caractere e animação sejam carregados com êxito, use o evento [**RequestComplete**](requestcomplete-event.md) . Se uma solicitação de carregamento falhar, você poderá tentar carregar os dados novamente ou exibir uma mensagem apropriada.

O arquivo de caractere inclui efeitos sonoros para algumas animações, conforme observado na tabela a seguir. Os efeitos sonoros só serão executados se essa opção estiver habilitada na folha de propriedades do Microsoft Agent. Você também pode desabilitar efeitos de som em seu aplicativo.



| Animação                  | Retornar animação         | Dá suporte à fala | Efeitos de som | Atribuído ao estado                            | Descrição                                            |
|----------------------------|--------------------------|-------------------|---------------|----------------------------------------------|--------------------------------------------------------|
| **Reconhecer**            | Nenhum                     | Não                | **Não**        | Nenhum                                         | Cabeçalho do nós nesta                                              |
| **Alerta**                  | Sim, usando branches de saída | Sim               | **Não**        | **Detecta**                                | Retifica e levanta os meus eyebrows                        |
| **Nascimento**               | Sim, usando branches de saída | Sim               | **Sim**       | Nenhum                                         | O avião de papel surge e não dobra                    |
| **Blink**                  | Nenhum                     | Não                | **Não**        | **IdlingLevel1** **IdlingLevel2**<br/> | Olhos pisca                                            |
| **Confuso**               | Sim, usando branches de saída | Sim               | **Sim**       | Nenhum                                         | Olhos girando                                       |
| **Parabenizar**           | Sim, usando branches de saída | Sim               | **Sim**       | Nenhum                                         | Exibe a faixa de especificações azul                                   |
| **Recusar**                | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Cabeça de agitações                                            |
| **DoMagic1**               | Nenhum                     | Sim               | **Sim**       | Nenhum                                         | Levanta a varinha mágica                                      |
| **DoMagic2**               | Sim, usando branches de saída | Não                | **Sim**       | Nenhum                                         | Abaixa a varinha, as nuvens aparecem                             |
| **DontRecognize**          | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Agita cabeça e contém asa para Ear                      |
| **Explicar**                | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Estende os braços para o lado                                   |
| **GestureDown**            | Sim, usando branches de saída | Sim               | **Não**        | **GesturingDown**                            | Gestos para baixo                                          |
| **GestureLeft**            | Sim, usando branches de saída | Sim               | **Não**        | **GesturingLeft**                            | Gestos restantes                                          |
| **GestureRight**           | Sim, usando branches de saída | Sim               | **Não**        | **GesturingRight**                           | Gestos para a direita                                         |
| **GestureUp**              | Sim, usando branches de saída | Sim               | **Não**        | **GesturingUp**                              | Gestos para cima                                            |
| **Getatenção**           | **GetAttentionReturn**   | Sim               | **Sim**       | Nenhum                                         | Vai para cima com asas superalongadas                       |
| **GetAttentionContinued**  | **GetAttentionReturn**   | Sim               | **Sim**       | Nenhum                                         | Vai para cima com asas superalongadas                 |
| **GetAttentionReturn**     | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                            |
| **Saudar**                  | Sim, usando branches de saída | Sim               | **Sim**       | Nenhum                                         | Bows                                                   |
| **Audição \_ 1**             | Nenhum                     | Não                | **Não**        | **Audição**                                  | Cabeça de inclinação para a direita ( \* animação em loop)                 |
| **Audição \_ 2**             | Nenhum                     | Não                | **Não**        | **Audição**                                  | Cabeça inclinada para a esquerda ( \* animação em loop)                  |
| **Audição \_ 3**             | Nenhum                     | Não                | **Não**        | **Audição**                                  | Transforma o cabeçalho à direita e à esquerda ( \* animação em loop)       |
| **Ocultar**                   | Nenhum                     | Não                | **Sim**       | **Ocultar**                                   | Voa para fora                                             |
| **Idle1 \_ 1**               | Nenhum                     | Não                | **Não**        | **IdlingLevel1** **IdlingLevel2**<br/> | Leva respire                                           |
| **Idle1 \_ 2**               | Nenhum                     | Não                | **Não**        | **IdlingLevel1** **IdlingLevel2**<br/> | Resumos à direita e piscar                               |
| **Idle1 \_ 3**               | Nenhum                     | Não                | **Não**        | **IdlingLevel1** **IdlingLevel2**<br/> | Resumos à esquerda e piscar                                |
| **Idle1 \_ 4**               | Nenhum                     | Não                | **Não**        | **IdlingLevel1** **IdlingLevel2**<br/> | Visão geral e intermitências                                  |
| **Idle1 \_ 5**               | Nenhum                     | Não                | **Não**        | **IdlingLevel1** **IdlingLevel2**<br/> | Visão geral e intermitências                                |
| **Idle2 \_ 1**               | Sim, usando branches de saída | Não                | **Não**        | **IdlingLevel2**                             | Coloca em óculos                                     |
| **Idle2 \_ 2**               | Nenhum                     | Não                | **Sim**       | **IdlingLevel2**                             | Consome um decifrador                                         |
| **Idle3 \_ 1**               | Nenhum                     | Não                | **Sim**       | **IdlingLevel3**                             | Bocejos                                                  |
| **Idle3 \_ 2**               | Sim, usando branches de saída | Não                | **Sim**       | **IdlingLevel3**                             | Cai em suspensão ( \* animação em loop)                     |
| **Idle3 \_ 3**               | Sim, usando branches de saída | Não                | **Não**        | **IdlingLevel3**                             | Escuta música (animação em \* loop)                 |
| **LookDownLookDownReturn** |                          | Não                | **Não**        | Nenhum                                         | Pesquisa                                             |
| **LookDownBlink**          | **LookDownReturn**       | Não                | **Sim**       | Nenhum                                         | Piscando em busca                                    |
| **LookDownReturn**         | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                            |
| **LookDownLeft**           | **LookDownLeftReturn**   | Não                | **Não**        | Nenhum                                         | Procura à esquerda                                        |
| **LookDownLeftBlink**      | **LookDownLeftReturn**   | Não                | **Sim**       | Nenhum                                         | Piscar para a esquerda                               |
| **LookDownLeftReturn**     | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                            |
| **LookDownRight**          | **LookDownRightReturn**  | Não                | **Não**        | Nenhum                                         | Pesquisa à direita                                       |
| **LookDownRightBlink**     | **LookDownRightReturn**  | Não                | **Sim**       | Nenhum                                         | Piscar à direita                              |
| **LookDownRightReturn**    | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                            |
| **LookLeft**               | **LookLeftReturn**       | Sim               | **Não**        | Nenhum                                         | Parece com a esquerda                                             |
| **LookLeftBlink**          | **LookLeftReturn**       | Sim               | **Sim**       | Nenhum                                         | Piscando à esquerda                                    |
| **LookLeftReturn**         | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                            |
| **LookRight**              | **LookRightReturn**      | Sim               | **Não**        | Nenhum                                         | Parece com a direita                                            |
| **LookRightBlink**         | **LookRightReturn**      | Sim               | **Sim**       | Nenhum                                         | Piscando à direita                                   |
| **LookRightReturn**        | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                            |
| **Busca**                 | **LookUpReturn**         | Não                | **Não**        | Nenhum                                         | Pesquisa                                               |
| **LookUpBlink**            | **LookUpReturn**         | Não                | **Sim**       | Nenhum                                         | Piscar de procurar                                      |
| **LookUpReturn**           | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                            |
| **LookUpLeft**             | **LookUpLeftReturn**     | Não                | **Não**        | Nenhum                                         | Pesquisa à esquerda                                          |
| **LookUpLeftBlink**        | **LookUpLeftReturn**     | Não                | **Sim**       | Nenhum                                         | Piscar de olhar para a esquerda                                 |
| **LookUpLeftReturn**       | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                            |
| **LookUpRight**            | **LookUpRightReturn**    | Não                | **Não**        | Nenhum                                         | Pesquisa à direita                                         |
| **LookUpRightBlink**       | **LookUpRightReturn**    | Não                | **Sim**       | Nenhum                                         | Piscando à direita                                |
| **LookUpRightReturn**      | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                            |
| **MoveDown**               | Sim, usando branches de saída | Não                | **Sim**       | **MovingDown**                               | Voa para baixo                                             |
| **MoveLeft**               | Sim, usando branches de saída | Não                | **Sim**       | **MovingLeft**                               | Surge à esquerda                                             |
| **MoveRight**              | Sim, usando branches de saída | Não                | **Sim**       | **MovingRight**                              | Voa para a direita                                            |
| **MoveUp**                 | Sim, usando branches de saída | Não                | **Sim**       | **MovingUp**                                 | Voa                                               |
| **Satisfeito**                | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Sorrisos                                                 |
| **Processo**                | Nenhum                     | Não                | **Sim**       | Nenhum                                         | Usa a calculadora                                        |
| **Processing**             | Sim, usando branches de saída | Não                | **Sim**       | Nenhum                                         | Usa a calculadora ( \* animação em loop)                  |
| **Ler**                   | **ReadReturn**           | Sim               | **Sim**       | Nenhum                                         | Abre a revista, lê e pesquisa                     |
| **ReadContinued**          | **ReadReturn**           | Sim               | **Sim**       | Nenhum                                         | Lê e pesquisa                                     |
| **ReadReturn**             | Nenhum                     | Não                | **Sim**       | Nenhum                                         | Retorna para a posição neutra                            |
| **Lendo**                | Sim, usando branches de saída | Não                | **Sim**       | Nenhum                                         | Leituras ( \* animação em loop)                            |
| **RestPose**               | Nenhum                     | Sim               | **Não**        | **Língua**                                 | Posição neutra                                       |
| **Triste**                    | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Expressão triste                                         |
| **Pesquisa**                 | Nenhum                     | Não                | **Sim**       | Nenhum                                         | Revela Telescope e gira                          |
| **Procurar**              | Sim, usando branches de saída | Não                | **Sim**       | Nenhum                                         | Revela Telescope e gira ( \* animação em loop)    |
| **Mostrar**                   | Nenhum                     | Não                | **Sim**       | **Mostrando**                                  | Surge em                                               |
| **StartListening**         | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Coloca mão em Ear                                       |
| **StopListening**          | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Coloca as mãos em ouvidos                                     |
| **Sugerir**                | Sim, usando branches de saída | Sim               | **Sim**       | Nenhum                                         | Exibe a lâmpada                                    |
| **Ficamos**              | Sim, usando branches de saída | Sim               | **Sim**       | Nenhum                                         | Parece surpreso                                        |
| **Pensar**                  | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Pesquisa com asa no rosto                             |
| **Pensando**               | Nenhum                     | Não                | **Não**        | Nenhum                                         | Pesquisa com asa no rosto ( \* animação em loop)       |
| **Certeza**              | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Baixo para a direita e Shrugs                              |
| **Onda**                   | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Ondas                                                  |
| **Gravar**                  | **WriteReturn**          | Sim               | **Sim**       | Nenhum                                         | Retira o lápis e o teclado, grava e pesquisa          |
| **WriteContinued**         | **WriteReturn**          | Sim               | **Sim**       | Nenhum                                         | Gravações e pesquisa                                    |
| **WriteReturn**            | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                            |
| **Gravando**                | Sim, usando branches de saída | Não                | **Sim**       | Nenhum                                         | Retira lápis e pad, escreve ( \* animação em loop) |



 

\* Se você reproduzir uma animação de looping, deverá usar [**parar**](stop-method.md) para limpá-la antes que outras animações na fila do caractere sejam reproduzidas.

 


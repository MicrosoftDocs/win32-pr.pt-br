---
title: Animações do Microsoft Agent para o caractere gênio
description: Animações do Microsoft Agent para o caractere gênio
ms.assetid: 56c42d7a-32af-47cb-8578-0a89507a41ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4f583fc6540b5fe13cc157542d69352a8ea5b31
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104366012"
---
# <a name="microsoft-agent-animations-for-genie-character"></a>Animações do Microsoft Agent para o caractere gênio

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O [Microsoft Agent gênio Character](https://www.microsoft.com/downloads/details.aspx?FamilyID=da86ba4e-bc2d-4c1d-b5a0-3183fe206414) é um trabalho com direitos autorais da Microsoft Corporation.

O gênio dá suporte às animações listadas na tabela a seguir. Consulte [programando a interface do servidor do Microsoft Agent](/windows/desktop/lwef/programming-the-microsoft-agent-server-interface) e [programando o controle do Microsoft Agent](programming-the-microsoft-agent-control.md) para obter informações sobre como chamar as animações do caractere.

Se estiver acessando essas animações de caracteres usando o protocolo HTTP e o método de [**preparação**](/windows/desktop/lwef/iagentcharacter--prepare) do servidor [**Get**](get-method.md) ou do controle, considere como você os baixará. Em vez de baixar todas as animações de uma só vez, talvez você queira recuperar as animações de **estado de apresentação e de** **fala** primeiro. Isso permitirá que você exiba o caractere rapidamente e o leia enquanto estiver desativando as outras animações de forma assíncrona. Além disso, para garantir que os dados de caractere e animação sejam carregados com êxito, use o evento [**RequestComplete**](requestcomplete-event.md) . Se uma solicitação de carregamento falhar, você poderá tentar carregar os dados novamente ou exibir uma mensagem apropriada.

Se as animações de **retorno** de uma animação forem definidas usando branches de saída, você não precisará chamá-las explicitamente; O agente reproduz automaticamente a animação de **retorno** antes da próxima animação. No entanto, se uma animação de **retorno** for listada, você deverá chamar a animação usando o método [**Play**](play-method.md) antes de outra animação para fornecer uma transição suave. Se nenhuma animação de **retorno** for listada, a animação normalmente terminará sem a necessidade de uma animação de transição.

O arquivo de caractere inclui efeitos sonoros para algumas animações, conforme observado na tabela a seguir. Os efeitos sonoros só serão executados se essa opção estiver habilitada na folha de propriedades do Microsoft Agent. Você também pode desabilitar efeitos de som em seu aplicativo.



| Animação                 | Retornar animação         | Dá suporte à fala | Efeitos de som | Atribuído ao estado                            | Descrição                                                    |
|---------------------------|--------------------------|-------------------|---------------|----------------------------------------------|----------------------------------------------------------------|
| **Reconhecer**           | Nenhum                     | Não                | **Não**        | Nenhum                                         | Cabeçalho do nós nesta                                                      |
| **Alerta**                 | Sim, usando branches de saída | Sim               | **Não**        | **Detecta**                                | Retifica e levanta os meus eyebrows                                |
| **Nascimento**              | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Mão levantada                                                    |
| **Blink**                 | Nenhum                     | Não                | **Não**        | **IdlingLevel1** **IdlingLevel2**<br/> | Olhos pisca                                                    |
| **Confuso**              | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Cabeça de rascunhos                                                 |
| **Parabenizar**          | Sim, usando branches de saída | Sim               | **Sim**       | Nenhum                                         | Applauds                                                       |
| **Parabenizar \_ 2**       | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Dá gestos para cima                                        |
| **Recusar**               | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Levanta o cabeçalho das mãos e as agitas                                   |
| **DoMagic1**              | Nenhum                     | Sim               | **Não**        | Nenhum                                         | Vira para o lado e levanta as mãos                                 |
| **DoMagic2**              | Sim, usando branches de saída | Não                | **Sim**       | Nenhum                                         | Diminui as mãos, as nuvens são exibidas                                    |
| **DontRecognize**         | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Contém mão para Ear                                              |
| **Explicar**               | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Estende os braços para o lado                                           |
| **GestureDown**           | Sim, usando branches de saída | Sim               | **Não**        | **GesturingDown**                            | Gestos para baixo                                                  |
| **GestureLeft**           | Sim, usando branches de saída | Sim               | **Não**        | **GesturingLeft**                            | Gestos restantes                                                  |
| **GestureRight**          | Sim, usando branches de saída | Sim               | **Não**        | **GesturingRight**                           | Gestos para a direita                                                 |
| **GestureUp**             | Sim, usando branches de saída | Sim               | **Não**        | **GesturingUp**                              | Gestos para cima                                                    |
| **Getatenção**          | **GetAttentionReturn**   | Sim               | **Não**        | Nenhum                                         | Braços de ondas                                                     |
| **GetAttentionContinued** | **GetAttentionReturn**   | Sim               | **Não**        | Nenhum                                         | Braços de ondas novamente                                               |
| **GetAttentionReturn**    | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                                    |
| **Saudar**                 | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Bows                                                           |
| **Audição \_ 1**            | Nenhum                     | Não                | **Não**        | **Audição**                                  | Estender ouvidos ( \* animação em loop)                              |
| **Audição \_ 2**            | Nenhum                     | Não                | **Não**        | **Audição**                                  | Cabeça inclinada para a esquerda ( \* animação em loop)                          |
| **Audição \_ 3**            | Nenhum                     | Não                | **Não**        | **Audição**                                  | Transforma o cabeçalho à esquerda ( \* animação em loop)                          |
| **Audição \_ 4**            | Nenhum                     | Não                | **Não**        | **Audição**                                  | Transforma o cabeçalho à direita ( \* animação em loop)                         |
| **Ocultar**                  | Nenhum                     | Não                | **Sim**       | **Ocultar**                                   | Desaparece em fumaça                                          |
| **Idle1 \_ 1**              | Nenhum                     | Não                | **Não**        | **IdlingLevel1** IdlingLevel2                | Leva respire                                                   |
| **Idle1 \_ 2**              | Nenhum                     | Não                | **Não**        | **IdlingLevel1** **IdlingLevel2**<br/> | Resumos à direita e piscar                                       |
| **Idle1 \_ 3**              | Sim, usando branches de saída | Não                | **Não**        | **IdlingLevel1** **IdlingLevel2**<br/> | Resumos à esquerda e piscar                                        |
| **Idle1 \_ 4**              | Nenhum                     | Não                | **Não**        | **IdlingLevel1** **IdlingLevel2**<br/> | É resumido à direita e pisca                             |
| **Idle1 \_ 5**              | Sim, usando branches de saída | Não                | **Não**        | **IdlingLevel1** **IdlingLevel2**<br/> | Visão geral e intermitências                                        |
| **Idle1 \_ 6**              | Nenhum                     | Não                | **Não**        | **IdlingLevel1** **IdlingLevel2**<br/> | Visão geral e intermitências                                          |
| **Idle2 \_ 1**              | Nenhum                     | Não                | **Não**        | **IdlingLevel2**                             | Snakes de WISP                                                    |
| **Idle2 \_ 2**              | Sim, usando branches de saída | Não                | **Não**        | **IdlingLevel2**                             | Revela rolagem e leituras                                       |
| **Idle2 \_ 3**              | Sim, usando branches de saída | Não                | **Não**        | **IdlingLevel2**                             | Revela rolagem e gravações                                      |
| **Idle3 \_ 1**              | Nenhum                     | Não                | **Sim**       | **IdlingLevel3**                             | Bocejos                                                          |
| **Idle3 \_ 2**              | Sim, usando branches de saída | Não                | **Sim**       | **IdlingLevel3**                             | Cai em suspensão ( \* animação em loop)                             |
| **LookDown**              | **LookDownReturn**       | Não                | **Não**        | Nenhum                                         | Pesquisa                                                     |
| **LookDownBlink**         | **LookDownReturn**       | Não                | **Não**        | Nenhum                                         | Piscando em busca                                            |
| **LookDownReturn**        | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                                    |
| **LookLeft**              | **LookLeftReturn**       | Não                | **Não**        | Nenhum                                         | Parece com a esquerda                                                     |
| **LookLeftBlink**         | **LookLeftReturn**       | Não                | **Não**        | Nenhum                                         | Piscando à esquerda                                            |
| **LookLeftReturn**        | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                                    |
| **LookRight**             | **LookRightReturn**      | Não                | **Não**        | Nenhum                                         | Parece com a direita                                                    |
| **LookRightBlink**        | **LookRightReturn**      | Não                | **Não**        | Nenhum                                         | Piscando à direita                                           |
| **LookRightReturn**       | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                                    |
| **Busca**                | **LookUpReturn**         | Não                | **Não**        | Nenhum                                         | Pesquisa                                                       |
| **LookUpBlink**           | **LookUpReturn**         | Não                | **Não**        | Nenhum                                         | Piscar de procurar                                              |
| **LookUpReturn**          | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                                    |
| **MoveDown**              | Sim, usando branches de saída | Não                | **Sim**       | **MovingDown**                               | Voa para baixo                                                     |
| **MoveLeft**              | Sim, usando branches de saída | Não                | **Sim**       | **MovingLeft**                               | Surge à esquerda                                                     |
| **MoveRight**             | Sim, usando branches de saída | Não                | **Sim**       | **MovingRight**                              | Voa para a direita                                                    |
| **MoveUp**                | Sim, usando branches de saída | Não                | **Sim**       | **MovingUp**                                 | Voa                                                       |
| **Satisfeito**               | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Sorrisos e suspensões juntas                                |
| **Processo**               | Não                       | Não                | **Não**        | Nenhum                                         | Gira em uma nuvem                                             |
| **Processing**            | Sim, usando branches de saída | Não                | **Não**        | Nenhum                                         | Gira em uma nuvem ( \* animação em loop)                       |
| **Ler**                  | **ReadReturn**           | Sim               | **Sim**       | Nenhum                                         | Revela rolagem, leituras e pesquisa                             |
| **ReadContinued**         | **ReadReturn**           | Sim               | **Não**        | Nenhum                                         | Lê e pesquisa                                             |
| **ReadReturn**            | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                                    |
| **Lendo**               | Sim, usando branches de saída | Não                | **Sim**       | Nenhum                                         | Revelar rolagem e leituras ( \* animação em loop)                  |
| **RestPose**              | Nenhum                     | Sim               | **Não**        | **Língua**                                 | Posição neutra                                               |
| **Triste**                   | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Expressão triste                                                 |
| **Pesquisa**                | Não                       | Não                | **Não**        | Nenhum                                         | Revela binóculos e ativações                                   |
| **Procurar**             | Sim, usando branches de saída | Não                | **Não**        | Nenhum                                         | Revela binóculos e ativações ( \* animação em loop)             |
| **Mostrar**                  | Nenhum                     | Não                | **Sim**       | **Mostrando**                                  | Parece sem fumaça                                           |
| **StartListening**        | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Coloca mão em Ear                                               |
| **StopListening**         | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Coloca a mão sobre ouvidos                                           |
| **Sugerir**               | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Exibe lâmpada                                             |
| **Ficamos**             | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Parece surpreso                                                |
| **Pensar**                 | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Pesquisa com mão em Chin                                     |
| **Pensando**              | Não                       | Não                | **Não**        | Nenhum                                         | Pesquisa com mão no Chin ( \* animação em loop)               |
| **Certeza**             | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Move uma mão para Chin, outra para hip e levanta a direita eyebrow |
| **Onda**                  | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Ondas                                                          |
| **Gravar**                 | **WriteReturn**          | Sim               | **Sim**       | Nenhum                                         | Revela rolagem, gravações e pesquisa                            |
| **WriteContinued**        | **WriteReturn**          | Sim               | **Sim**       | Nenhum                                         | Gravações e pesquisa                                            |
| **WriteReturn**           | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                                    |
| **Gravando**               | Sim, usando branches de saída | Não                | **Sim**       | Nenhum                                         | Revelar rolagem, gravações ( \* animação em loop)                   |



 

\* Se você reproduzir uma animação de looping, deverá usar [**parar**](stop-method.md) para limpá-la antes que outras animações na fila do caractere sejam reproduzidas.

 


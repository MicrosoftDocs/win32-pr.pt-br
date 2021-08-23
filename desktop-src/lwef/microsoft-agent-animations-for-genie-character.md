---
title: Animações do Microsoft Agent para caracteres de mágico
description: Animações do Microsoft Agent para caracteres de mágico
ms.assetid: 56c42d7a-32af-47cb-8578-0a89507a41ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 204da244b74e96e239d540662dabf73af82001748b395da8e660f53fe4cf85e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976096"
---
# <a name="microsoft-agent-animations-for-genie-character"></a>Animações do Microsoft Agent para caracteres de mágico

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O [Caractere de Mágico do Microsoft Agent](https://www.microsoft.com/downloads/details.aspx?FamilyID=da86ba4e-bc2d-4c1d-b5a0-3183fe206414) é um trabalho protegido por direitos autorais Microsoft Corporation.

O Supports dá suporte às animações listadas na tabela a seguir. Consulte [Programando a Interface do Servidor do Microsoft Agent](/windows/desktop/lwef/programming-the-microsoft-agent-server-interface) e [Programando o Controle do Microsoft Agent](programming-the-microsoft-agent-control.md) para obter informações sobre como chamar animações do caractere.

Se você estiver acessando essas animações de caractere usando o [](/windows/desktop/lwef/iagentcharacter--prepare) protocolo HTTP e o método [**Get**](get-method.md) ou Prepare do servidor do controle, considere como baixá-las. Em vez de baixar todas as animações de  uma  só vez, talvez você queira recuperar as animações de estado Mostrando e Falando primeiro. Isso permitirá que você exibir o caractere rapidamente e fazer com que ele fale, ao mesmo tempo que baixa outras animações de forma assíncrona. Além disso, para garantir que os dados de animação e caracteres carreguem com êxito, use [**o evento RequestComplete.**](requestcomplete-event.md) Se uma solicitação de carga falhar, você poderá tentar carregar novamente os dados ou exibir uma mensagem apropriada.

Se as animações return **de** uma animação são definidas usando branches exit, você não precisa chamá-la explicitamente; O Agent reproduz automaticamente a **animação Return** antes da próxima animação. No entanto, se uma **animação** Return estiver listada, você deverá chamar a animação usando o método [**Play**](play-method.md) antes de outra animação para fornecer uma transição suave. Se nenhuma **animação** return for listada, a animação normalmente terminará sem a necessidade de uma animação de transição.

O arquivo de caracteres inclui efeitos de som para alguma animação, conforme notado na tabela a seguir. Os efeitos de som só reproduzirão se essa opção estiver habilitada na folha de propriedades do Microsoft Agent. Você também pode desabilitar efeitos de som em seu aplicativo.



| Animação                 | Animação de retorno         | Dá suporte à fala | Efeitos de som | Atribuído ao Estado                            | Descrição                                                    |
|---------------------------|--------------------------|-------------------|---------------|----------------------------------------------|----------------------------------------------------------------|
| **Reconhecer**           | Nenhum                     | Não                | **Não**        | Nenhum                                         | Nods head                                                      |
| **Alerta**                 | Sim, usando branches exit | Sim               | **Não**        | **Ouvir**                                | Cria e gera reações                                |
| **Anunciar**              | Sim, usando branches exit | Sim               | **Não**        | Nenhum                                         | Gera a mão                                                    |
| **Blink**                 | Nenhum                     | Não                | **Não**        | **IdlingLevel1** **IdlingLevel2**<br/> | Pisca os olhos                                                    |
| **Confuso**              | Sim, usando branches exit | Sim               | **Não**        | Nenhum                                         | Cabeça de rascunhos                                                 |
| **Felicitar**          | Sim, usando branches exit | Sim               | **Sim**       | Nenhum                                         | Aplaude                                                       |
| **\_2º dia**       | Sim, usando branches exit | Sim               | **Não**        | Nenhum                                         | Dá um gesto de miniaturas                                        |
| **Recusar**               | Sim, usando branches exit | Sim               | **Não**        | Nenhum                                         | Eleva as mãos e treme a cabeça                                   |
| **DoMagic1**              | Nenhum                     | Sim               | **Não**        | Nenhum                                         | Volta para o lado e ativas as mãos                                 |
| **DoMagic2**              | Sim, usando branches exit | Não                | **Sim**       | Nenhum                                         | Mãos inferiores, nuvens são exibidas                                    |
| **DontRecognize**         | Sim, usando branches exit | Sim               | **Não**        | Nenhum                                         | Mantém a mão para o ouvido                                              |
| **Explicar**               | Sim, usando branches exit | Sim               | **Não**        | Nenhum                                         | Estende os braços para o lado                                           |
| **GestureDown**           | Sim, usando branches exit | Sim               | **Não**        | **GesturingDown**                            | Gestos para baixo                                                  |
| **GestureLeft**           | Sim, usando branches exit | Sim               | **Não**        | **GesturingLeft**                            | Gestos à esquerda                                                  |
| **GestureRight**          | Sim, usando branches exit | Sim               | **Não**        | **GesturingRight**                           | Gestos à direita                                                 |
| **GestureUp**             | Sim, usando branches exit | Sim               | **Não**        | **GesturingUp**                              | Gestos para cima                                                    |
| **GetAttention**          | **GetAttentionReturn**   | Sim               | **Não**        | Nenhum                                         | Mãos de ondas                                                     |
| **GetAttentionContinued** | **GetAttentionReturn**   | Sim               | **Não**        | Nenhum                                         | Mãos de ondas novamente                                               |
| **GetAttentionReturn**    | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                                    |
| **Saudar**                 | Sim, usando branches exit | Sim               | **Não**        | Nenhum                                         | Arcos                                                           |
| **Escuta \_ 1**            | Nenhum                     | Não                | **Não**        | **Audição**                                  | Estendendo os olhos \* (animação em loop)                              |
| **Escuta \_ 2**            | Nenhum                     | Não                | **Não**        | **Audição**                                  | Inclina a cabeça para a esquerda \* (animação em loop)                          |
| **Escuta \_ 3**            | Nenhum                     | Não                | **Não**        | **Audição**                                  | Gira a cabeça para a esquerda \* (animação de loop)                          |
| **Escuta \_ 4**            | Nenhum                     | Não                | **Não**        | **Audição**                                  | Gira a cabeça para a direita \* (animação de loop)                         |
| **Ocultar**                  | Nenhum                     | Não                | **Sim**       | **Escondendo**                                   | Desaparece no smoke                                          |
| **Idle1 \_ 1**              | Nenhum                     | Não                | **Não**        | **IdlingLevel1** IdlingLevel2                | Leva um tempo                                                   |
| **Idle1 \_ 2**              | Nenhum                     | Não                | **Não**        | **IdlingLevel1** **IdlingLevel2**<br/> | Relance para a direita e pisca                                       |
| **Idle1 \_ 3**              | Sim, usando branches exit | Não                | **Não**        | **IdlingLevel1** **IdlingLevel2**<br/> | Relance à esquerda e pisca                                        |
| **Idle1 \_ 4**              | Nenhum                     | Não                | **Não**        | **IdlingLevel1** **IdlingLevel2**<br/> | Relance para a direita e pisca                             |
| **Idle1 \_ 5**              | Sim, usando branches exit | Não                | **Não**        | **IdlingLevel1** **IdlingLevel2**<br/> | Relance para baixo e pisca                                        |
| **Idle1 \_ 6**              | Nenhum                     | Não                | **Não**        | **IdlingLevel1** **IdlingLevel2**<br/> | Relance e pisque                                          |
| **Idle2 \_ 1**              | Nenhum                     | Não                | **Não**        | **IdlingLevel2**                             | Wisp                                                    |
| **Idle2 \_ 2**              | Sim, usando branches exit | Não                | **Não**        | **IdlingLevel2**                             | Revelações rolam e leem                                       |
| **Idle2 \_ 3**              | Sim, usando branches exit | Não                | **Não**        | **IdlingLevel2**                             | Rolagem e gravações de revelações                                      |
| **Idle3 \_ 1**              | Nenhum                     | Não                | **Sim**       | **IdlingLevel3**                             | Bocejos                                                          |
| **Idle3 \_ 2**              | Sim, usando branches exit | Não                | **Sim**       | **IdlingLevel3**                             | Adormeça \* (animação em loop)                             |
| **LookDown**              | **LookDownReturn**       | Não                | **Não**        | Nenhum                                         | Procura para baixo                                                     |
| **LookDownBlink**         | **LookDownReturn**       | Não                | **Não**        | Nenhum                                         | Pisca olhando para baixo                                            |
| **LookDownReturn**        | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                                    |
| **LookLeft**              | **LookLeftReturn**       | Não                | **Não**        | Nenhum                                         | Parece à esquerda                                                     |
| **LookLeftBlink**         | **LookLeftReturn**       | Não                | **Não**        | Nenhum                                         | Piscar olhando para a esquerda                                            |
| **LookLeftReturn**        | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                                    |
| **LookRight**             | **LookRightReturn**      | Não                | **Não**        | Nenhum                                         | Parece à direita                                                    |
| **LookRightBlink**        | **LookRightReturn**      | Não                | **Não**        | Nenhum                                         | Piscar olhando para a direita                                           |
| **LookRightReturn**       | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                                    |
| **Pesquisa**                | **LookUpReturn**         | Não                | **Não**        | Nenhum                                         | Procura                                                       |
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
| **Pesquisar**                | Não                       | Não                | **Não**        | Nenhum                                         | Revela binóculos e ativações                                   |
| **Procurar**             | Sim, usando branches de saída | Não                | **Não**        | Nenhum                                         | Revela binóculos e ativações ( \* animação em loop)             |
| **Mostrar**                  | Nenhum                     | Não                | **Sim**       | **Mostrando**                                  | Parece sem fumaça                                           |
| **StartListening**        | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Coloca mão em Ear                                               |
| **StopListening**         | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Coloca a mão sobre ouvidos                                           |
| **Sugerir**               | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Exibe lâmpada                                             |
| **Ficamos**             | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Parece surpreso                                                |
| **Pensar**                 | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Pesquisa com mão em Chin                                     |
| **Processando dados**              | Não                       | Não                | **Não**        | Nenhum                                         | Pesquisa com mão no Chin ( \* animação em loop)               |
| **Certeza**             | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Move uma mão para Chin, outra para hip e levanta a direita eyebrow |
| **Onda**                  | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Ondas                                                          |
| **Gravar**                 | **WriteReturn**          | Sim               | **Sim**       | Nenhum                                         | Revela rolagem, gravações e pesquisa                            |
| **WriteContinued**        | **WriteReturn**          | Sim               | **Sim**       | Nenhum                                         | Gravações e pesquisa                                            |
| **WriteReturn**           | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                                    |
| **Gravando**               | Sim, usando branches de saída | Não                | **Sim**       | Nenhum                                         | Revelar rolagem, gravações ( \* animação em loop)                   |



 

\* Se você reproduzir uma animação de looping, deverá usar [**parar**](stop-method.md) para limpá-la antes que outras animações na fila do caractere sejam reproduzidas.

 


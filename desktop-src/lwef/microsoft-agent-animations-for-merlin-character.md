---
title: Animações do Microsoft Agent para caracteres DeIa
description: Animações do Microsoft Agent para caracteres DeIa
ms.assetid: 4563a464-2c1a-4928-a471-e3f0fdfe85c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 797002897f0e3bdb7efb309de8b73a33df8bdf399279895be8daa2b47d8ec084
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247469"
---
# <a name="microsoft-agent-animations-for-merlin-character"></a>Animações do Microsoft Agent para caracteres DeIa

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O [Caractere DeIa do Microsoft Agent](https://www.microsoft.com/downloads/details.aspx?FamilyID=fee1dadd-2f23-41d0-8a81-2affd74c0aa5) é um trabalho protegido por direitos autorais Microsoft Corporation.

Ele dá suporte às animações listadas na tabela a seguir. Consulte [Programando a Interface do Servidor do Microsoft Agent](/windows/desktop/lwef/programming-the-microsoft-agent-server-interface) e [Programando o Controle do Microsoft Agent](programming-the-microsoft-agent-control.md) para obter informações sobre como chamar animações do caractere.

Se você estiver acessando essas animações de caractere usando o [](/windows/desktop/lwef/iagentcharacter--prepare) protocolo HTTP e o método [**Get**](get-method.md) ou Prepare do servidor do controle, considere como baixá-las. Em vez de baixar todas as animações de  uma  só vez, talvez você queira recuperar as animações de estado Mostrando e Falando primeiro. Isso permitirá que você exibir o caractere rapidamente e fazer com que ele fale, ao mesmo tempo que baixa outras animações de forma assíncrona. Além disso, para garantir que os dados de animação e caracteres carreguem com êxito, use [**o evento RequestComplete.**](requestcomplete-event.md) Se uma solicitação de carga falhar, você poderá tentar carregar novamente os dados ou exibir uma mensagem apropriada.

Se a animação **Return** de uma animação for definida usando branches exit, você não precisará chamá-la explicitamente; O Agent reproduz automaticamente a **animação Return** antes da próxima animação. No entanto, se uma **animação** Return estiver listada, você deverá chamar a animação usando o método [**Play**](play-method.md) antes de outra animação para fornecer uma transição suave. Se nenhuma **animação** return for listada, a animação normalmente terminará sem a necessidade de uma animação de transição.

O arquivo de caracteres inclui efeitos de som para algumas animações, conforme notado na tabela a seguir. Os efeitos de som só reproduzirão se essa opção estiver habilitada na folha de propriedades do Microsoft Agent. Você também pode desabilitar efeitos de som em seu aplicativo.



| Animação                 | Animação de retorno         | Dá suporte à fala | Efeitos de som | Atribuído ao Estado                            | Descrição                                      |
|---------------------------|--------------------------|-------------------|---------------|----------------------------------------------|--------------------------------------------------|
| **Reconhecer**           | Nenhum                     | Não                | **Não**        | Nenhum                                         | Nods head                                        |
| **Alerta**                 | Sim, usando branches exit | Sim               | **Não**        | **Ouvir**                                | Cria e gera reações                  |
| **Anunciar**              | Sim, usando branches exit | Sim               | **Sim**       | Nenhum                                         | Gera jogos e jogos                         |
| **Blink**                 | Nenhum                     | Não                | **Não**        | **IdlingLevel1** **IdlingLevel2**<br/> | Pisca os olhos                                      |
| **Confuso**              | Sim, usando branches exit | Sim               | **Sim**       | Nenhum                                         | Cabeça de rascunhos                                   |
| **Felicitar**          | Sim, usando branches exit | Sim               | **Sim**       | Nenhum                                         | Exibe o troféu                                  |
| **\_2º dia**       | Sim, usando branches exit | Sim               | **Sim**       | Nenhum                                         | Aplaude                                         |
| **Recusar**               | Sim, usando branches exit | Sim               | **Não**        | Nenhum                                         | Eleva as mãos e treme a cabeça                     |
| **DoMagic1**              | Nenhum                     | Sim               | **Não**        | Nenhum                                         | Gera magic magic magic                                |
| **DoMagic2**              | Sim, usando branches exit | Não                | **Sim**       | Nenhum                                         | Diminui a renda, as nuvens aparecem                       |
| **DontRecognize**         | Sim, usando branches exit | Sim               | **Não**        | Nenhum                                         | Mantém a mão para o ouvido                                |
| **Explicar**               | Sim, usando branches exit | Sim               | **Não**        | Nenhum                                         | Estende os braços para o lado                             |
| **GestureDown**           | Sim, usando branches exit | Sim               | **Não**        | **GesturingDown**                            | Gestos para baixo                                    |
| **GestureLeft**           | Sim, usando branches de saída | Sim               | **Não**        | **GesturingLeft**                            | Gestos restantes                                    |
| **GestureRight**          | Sim, usando branches de saída | Sim               | **Não**        | **GesturingRight**                           | Gestos para a direita                                   |
| **GestureUp**             | Sim, usando branches de saída | Sim               | **Não**        | **GesturingUp**                              | Gestos para cima                                      |
| **Getatenção**          | **GetAttentionReturn**   | Sim               | **Sim**       | Nenhum                                         | Rebatidas progressivos e vazados                         |
| **GetAttentionContinued** | **GetAttentionReturn**   | Sim               | **Sim**       | Nenhum                                         | Encaminhar, rebatidas                    |
| **GetAttentionReturn**    | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                      |
| **Saudar**                 | Sim, usando branches de saída | Sim               | **Sim**       | Nenhum                                         | Bows                                             |
| **Audição \_ 1**            | Nenhum                     | Não                | **Não**        | **Audição**                                  | Estender ouvidos ( \* animação em loop)                |
| **Audição \_ 2**            | Nenhum                     | Não                | **Não**        | **Audição**                                  | Cabeça inclinada para a esquerda ( \* animação em loop)            |
| **Audição \_ 3**            | Nenhum                     | Não                | **Não**        | **Audição**                                  | Transforma o cabeçalho à esquerda ( \* animação em loop)            |
| **Audição \_ 4**            | Nenhum                     | Não                | **Não**        | **Audição**                                  | Transforma o cabeçalho à direita ( \* animação em loop)           |
| **Ocultar**                  | Nenhum                     | Não                | **Sim**       | **Ocultar**                                   | Desaparece abaixo da Cap                             |
| **Idle1 \_ 1**              | Sim, usando branches de saída | Não                | **Não**        | **IdlingLevel1** **IdlingLevel2**<br/> | Leva respire                                     |
| **Idle1 \_ 2**              | Sim, usando branches de saída | Não                | **Não**        | **IdlingLevel1** **IdlingLevel2**<br/> | Resumos à esquerda e piscar                          |
| **Idle1 \_ 3**              | Sim, usando branches de saída | Não                | **Não**        | **IdlingLevel1** **IdlingLevel2**<br/> | Resumos à direita                                    |
| **Idle1 \_ 4**              | Sim, usando branches de saída | Não                | **Não**        | **IdlingLevel1** **IdlingLevel2**<br/> | É resumido à direita e pisca               |
| **Idle2 \_ 1**              | Nenhum                     | Não                | **Não**        | **IdlingLevel2**                             | Analisa a luz e pisca                         |
| **Idle2 \_ 2**              | Nenhum                     | Não                | **Não**        | **IdlingLevel2**                             | Mantém as mãos e piscar                           |
| **Idle3 \_ 1**              | Nenhum                     | Não                | **Sim**       | **IdlingLevel3**                             | Bocejos                                            |
| **Idle3 \_ 2**              | Sim, usando branches exit | Não                | **Sim**       | **IdlingLevel3**                             | Adormeça \* (animação em loop)               |
| **LookDown**              | **LookDownReturn**       | Não                | **Não**        | Nenhum                                         | Procura para baixo                                       |
| **LookDownBlink**         | **LookDownReturn**       | Não                | **Não**        | Nenhum                                         | Pisca olhando para baixo                              |
| **LookDownReturn**        | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                      |
| **LookLeft**              | **LookLeftReturn**       | Não                | **Não**        | Nenhum                                         | Parece à esquerda                                       |
| **LookLeftBlink**         | **LookLeftReturn**       | Não                | **Não**        | Nenhum                                         | Piscar olhando para a esquerda                              |
| **LookLeftReturn**        | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                      |
| **LookRight**             | **LookRightReturn**      | Não                | **Não**        | Nenhum                                         | Parece à direita                                      |
| **LookRightBlink**        | **LookRightReturn**      | Não                | **Não**        | Nenhum                                         | Piscar olhando para a direita                             |
| **LookRightReturn**       | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                      |
| **Pesquisa**                | **LookUpReturn**         | Não                | **Não**        | Nenhum                                         | Procura                                         |
| **LookUpBlink**           | **LookUpReturn**         | Não                | **Não**        | Nenhum                                         | Piscar olhando para cima                                |
| **LookUpReturn**          | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                      |
| **Movedown**              | Sim, usando branches exit | Não                | **Sim**       | **MovingDown**                               | Reba de 1000                                       |
| **MoveLeft**              | Sim, usando branches de saída | Não                | **Sim**       | **MovingLeft**                               | Surge à esquerda                                       |
| **MoveRight**             | Sim, usando branches de saída | Não                | **Sim**       | **MovingRight**                              | Voa para a direita                                      |
| **MoveUp**                | Sim, usando branches de saída | Não                | **Sim**       | **MovingUp**                                 | Voa                                         |
| **Satisfeito**               | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Sorrisos e suspensões juntas                  |
| **Processo**               | Não                       | Não                | **Sim**       | Nenhum                                         | Stirs caldron                                    |
| **Processing**            | Sim, usando branches de saída | Não                | **Sim**       | Nenhum                                         | Stirs caldron ( \* animação em looping)              |
| **Ler**                  | **ReadReturn**           | Sim               | **Sim**       | Nenhum                                         | Abre o livro, lê e pesquisa                   |
| **ReadContinued**         | **ReadReturn**           | Sim               | **Sim**       | Nenhum                                         | Lê e pesquisa                               |
| **ReadReturn**            | Nenhum                     | Não                | **Sim**       | Nenhum                                         | Retorna para a posição neutra                      |
| **Lendo**               | Sim, usando branches de saída | Não                | **Sim**       | Nenhum                                         | Leituras ( \* animação em loop)                      |
| **RestPose**              | Nenhum                     | Sim               | **Não**        | **Língua**                                 | Posição neutra                                 |
| **Triste**                   | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Expressão triste                                   |
| **Pesquisar**                | Não                       | Não                | **Sim**       | Nenhum                                         | Procura no indicador de cristal                          |
| **Procurar**             | Sim, usando branches de saída | Não                | **Sim**       | Nenhum                                         | Procura no indicador de cristal ( \* animação em loop)    |
| **Mostrar**                  | Nenhum                     | Não                | **Sim**       | **Mostrando**                                  | Aparece fora do limite                               |
| **StartListening**        | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Coloca mão em Ear                                 |
| **StopListening**         | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Coloca a mão sobre ouvidos                             |
| **Sugerir**               | Sim, usando branches de saída | Sim               | **Sim**       | Nenhum                                         | Exibe lâmpada                               |
| **Ficamos**             | Sim, usando branches de saída | Sim               | **Sim**       | Nenhum                                         | Parece surpreso                                  |
| **Pensar**                 | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Pesquisa com mão em Chin                       |
| **Processando dados**              | Não                       | Não                | **Não**        | Nenhum                                         | Pesquisa com mão no Chin ( \* animação em loop) |
| **Certeza**             | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Encaminhar e gerar eyebrow                 |
| **Onda**                  | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Ondas                                            |
| **Gravar**                 | **WriteReturn**          | Sim               | **Sim**       | Nenhum                                         | Abre o livro, grava e pesquisa                  |
| **WriteContinued**        | **WriteReturn**          | Sim               | **Sim**       | Nenhum                                         | Gravações e pesquisa                              |
| **WriteReturn**           | Nenhum                     | Não                | **Sim**       | Nenhum                                         | Retorna para a posição neutra                      |
| **Gravando**               | Sim, usando branches de saída | Não                | **Sim**       | Nenhum                                         | Gravações ( \* animação em loop)                     |



 

\* Se você reproduzir uma animação de looping, deverá usar [**parar**](stop-method.md) para limpá-la antes que outras animações na fila do caractere sejam reproduzidas.

 


---
title: Animações do Microsoft Agent para o caractere Merlin
description: Animações do Microsoft Agent para o caractere Merlin
ms.assetid: 4563a464-2c1a-4928-a471-e3f0fdfe85c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5138dab8b3a4d411226cfe03b9341a73f301c037
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104294028"
---
# <a name="microsoft-agent-animations-for-merlin-character"></a>Animações do Microsoft Agent para o caractere Merlin

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O [caractere Merlin do Microsoft Agent](https://www.microsoft.com/downloads/details.aspx?FamilyID=fee1dadd-2f23-41d0-8a81-2affd74c0aa5) é um trabalho com direitos autorais da Microsoft Corporation.

Merlin dá suporte às animações listadas na tabela a seguir. Consulte [programando a interface do servidor do Microsoft Agent](/windows/desktop/lwef/programming-the-microsoft-agent-server-interface) e [programando o controle do Microsoft Agent](programming-the-microsoft-agent-control.md) para obter informações sobre como chamar as animações do caractere.

Se estiver acessando essas animações de caracteres usando o protocolo HTTP e o método de [**preparação**](/windows/desktop/lwef/iagentcharacter--prepare) do servidor [**Get**](get-method.md) ou do controle, considere como você os baixará. Em vez de baixar todas as animações de uma só vez, talvez você queira recuperar as animações de **estado de apresentação e de** **fala** primeiro. Isso permitirá que você exiba o caractere rapidamente e o leia enquanto estiver desativando as outras animações de forma assíncrona. Além disso, para garantir que os dados de caractere e animação sejam carregados com êxito, use o evento [**RequestComplete**](requestcomplete-event.md) . Se uma solicitação de carregamento falhar, você poderá tentar carregar os dados novamente ou exibir uma mensagem apropriada.

Se a animação de **retorno** de uma animação for definida usando ramificações de saída, você não precisará chamá-la explicitamente; O agente reproduz automaticamente a animação de **retorno** antes da próxima animação. No entanto, se uma animação de **retorno** for listada, você deverá chamar a animação usando o método [**Play**](play-method.md) antes de outra animação para fornecer uma transição suave. Se nenhuma animação de **retorno** for listada, a animação normalmente terminará sem a necessidade de uma animação de transição.

O arquivo de caractere inclui efeitos sonoros para algumas animações, conforme observado na tabela a seguir. Os efeitos sonoros só serão executados se essa opção estiver habilitada na folha de propriedades do Microsoft Agent. Você também pode desabilitar efeitos de som em seu aplicativo.



| Animação                 | Retornar animação         | Dá suporte à fala | Efeitos de som | Atribuído ao estado                            | Descrição                                      |
|---------------------------|--------------------------|-------------------|---------------|----------------------------------------------|--------------------------------------------------|
| **Reconhecer**           | Nenhum                     | Não                | **Não**        | Nenhum                                         | Cabeçalho do nós nesta                                        |
| **Alerta**                 | Sim, usando branches de saída | Sim               | **Não**        | **Detecta**                                | Retifica e levanta os meus eyebrows                  |
| **Nascimento**              | Sim, usando branches de saída | Sim               | **Sim**       | Nenhum                                         | Gera trompete e joga                         |
| **Blink**                 | Nenhum                     | Não                | **Não**        | **IdlingLevel1** **IdlingLevel2**<br/> | Olhos pisca                                      |
| **Confuso**              | Sim, usando branches de saída | Sim               | **Sim**       | Nenhum                                         | Cabeça de rascunhos                                   |
| **Parabenizar**          | Sim, usando branches de saída | Sim               | **Sim**       | Nenhum                                         | Exibe Trophy                                  |
| **Parabenizar \_ 2**       | Sim, usando branches de saída | Sim               | **Sim**       | Nenhum                                         | Applauds                                         |
| **Recusar**               | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Levanta o cabeçalho das mãos e as agitas                     |
| **DoMagic1**              | Nenhum                     | Sim               | **Não**        | Nenhum                                         | Levanta a varinha mágica                                |
| **DoMagic2**              | Sim, usando branches de saída | Não                | **Sim**       | Nenhum                                         | Abaixa a varinha, as nuvens aparecem                       |
| **DontRecognize**         | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Contém mão para Ear                                |
| **Explicar**               | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Estende os braços para o lado                             |
| **GestureDown**           | Sim, usando branches de saída | Sim               | **Não**        | **GesturingDown**                            | Gestos para baixo                                    |
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
| **Idle2 \_ 1**              | Nenhum                     | Não                | **Não**        | **IdlingLevel2**                             | Procura na varinha e pisca                         |
| **Idle2 \_ 2**              | Nenhum                     | Não                | **Não**        | **IdlingLevel2**                             | Mantém as mãos e pisca                           |
| **Idle3 \_ 1**              | Nenhum                     | Não                | **Sim**       | **IdlingLevel3**                             | Bocejos                                            |
| **Idle3 \_ 2**              | Sim, usando branches de saída | Não                | **Sim**       | **IdlingLevel3**                             | Cai em suspensão ( \* animação em loop)               |
| **LookDown**              | **LookDownReturn**       | Não                | **Não**        | Nenhum                                         | Pesquisa                                       |
| **LookDownBlink**         | **LookDownReturn**       | Não                | **Não**        | Nenhum                                         | Piscando em busca                              |
| **LookDownReturn**        | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                      |
| **LookLeft**              | **LookLeftReturn**       | Não                | **Não**        | Nenhum                                         | Parece com a esquerda                                       |
| **LookLeftBlink**         | **LookLeftReturn**       | Não                | **Não**        | Nenhum                                         | Piscando à esquerda                              |
| **LookLeftReturn**        | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                      |
| **LookRight**             | **LookRightReturn**      | Não                | **Não**        | Nenhum                                         | Parece com a direita                                      |
| **LookRightBlink**        | **LookRightReturn**      | Não                | **Não**        | Nenhum                                         | Piscando à direita                             |
| **LookRightReturn**       | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                      |
| **Busca**                | **LookUpReturn**         | Não                | **Não**        | Nenhum                                         | Pesquisa                                         |
| **LookUpBlink**           | **LookUpReturn**         | Não                | **Não**        | Nenhum                                         | Piscar de procurar                                |
| **LookUpReturn**          | Nenhum                     | Não                | **Não**        | Nenhum                                         | Retorna para a posição neutra                      |
| **MoveDown**              | Sim, usando branches de saída | Não                | **Sim**       | **MovingDown**                               | Voa para baixo                                       |
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
| **Pesquisa**                | Não                       | Não                | **Sim**       | Nenhum                                         | Procura no indicador de cristal                          |
| **Procurar**             | Sim, usando branches de saída | Não                | **Sim**       | Nenhum                                         | Procura no indicador de cristal ( \* animação em loop)    |
| **Mostrar**                  | Nenhum                     | Não                | **Sim**       | **Mostrando**                                  | Aparece fora do limite                               |
| **StartListening**        | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Coloca mão em Ear                                 |
| **StopListening**         | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Coloca a mão sobre ouvidos                             |
| **Sugerir**               | Sim, usando branches de saída | Sim               | **Sim**       | Nenhum                                         | Exibe lâmpada                               |
| **Ficamos**             | Sim, usando branches de saída | Sim               | **Sim**       | Nenhum                                         | Parece surpreso                                  |
| **Pensar**                 | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Pesquisa com mão em Chin                       |
| **Pensando**              | Não                       | Não                | **Não**        | Nenhum                                         | Pesquisa com mão no Chin ( \* animação em loop) |
| **Certeza**             | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Encaminhar e gerar eyebrow                 |
| **Onda**                  | Sim, usando branches de saída | Sim               | **Não**        | Nenhum                                         | Ondas                                            |
| **Gravar**                 | **WriteReturn**          | Sim               | **Sim**       | Nenhum                                         | Abre o livro, grava e pesquisa                  |
| **WriteContinued**        | **WriteReturn**          | Sim               | **Sim**       | Nenhum                                         | Gravações e pesquisa                              |
| **WriteReturn**           | Nenhum                     | Não                | **Sim**       | Nenhum                                         | Retorna para a posição neutra                      |
| **Gravando**               | Sim, usando branches de saída | Não                | **Sim**       | Nenhum                                         | Gravações ( \* animação em loop)                     |



 

\* Se você reproduzir uma animação de looping, deverá usar [**parar**](stop-method.md) para limpá-la antes que outras animações na fila do caractere sejam reproduzidas.

 


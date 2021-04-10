---
description: Uma cadeia de troca é uma coleção de buffers que são usados para exibir quadros para o usuário.
ms.assetid: aefc0680-cbe6-42eb-8c00-eaa343eee469
title: O que é uma cadeia de permuta? (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8fc1fd2d313c70a680d9b276a3aabedc6d8cff
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163732"
---
# <a name="what-is-a-swap-chain-direct3d-9"></a>O que é uma cadeia de permuta? (Direct3D 9)

Uma cadeia de troca é uma coleção de buffers que são usados para exibir quadros para o usuário. Cada vez que um aplicativo apresenta um novo quadro para exibição, o primeiro buffer da cadeia de troca assume o lugar do buffer exibido. Esse processo é chamado troca ou inversão.

Um adaptador gráfico contém um ponteiro para uma superfície que representa a imagem que está sendo exibida no monitor, chamado de um buffer frontal. Como o monitor é atualizado, a placa gráfica envia o conteúdo do buffer frontal para o monitor para ser exibido. No entanto, isso leva a um problema ao renderizar gráficos em tempo real. O coração do problema é que as taxas de atualização do monitor são muito lentas em comparação com o restante do computador. As taxas de atualização comuns variam de 60 Hz (60 vezes por segundo) a 100 Hz. Se seu aplicativo está atualizando o buffer frontal enquanto o monitor está no meio de uma atualização, a imagem exibida será recortada na metade com a metade superior da tela que contém a imagem anterior e a metade inferior que contém a nova imagem. Esse problema é conhecido como desmembramento.

O Direct3D implementa duas opções para evitar a divisão:

-   Uma opção para permitir somente as atualizações de monitor na operação de retorno vertical (ou sincronização vertical). Um monitor normalmente atualiza sua imagem, movendo um marcador de luz horizontalmente, fazendo um movimento em zigue-zague na parte superior esquerda do monitor e terminando na parte inferior direita. Quando o marcador de luz atinge a parte inferior, o monitor calibra novamente o marcador de luz, movendo-o novamente para o canto superior esquerdo para que o processo possa iniciar novamente. Essa recalibração é denominada sincronização vertical. Durante uma sincronização vertical, nada é desenhado no monitor, portanto, qualquer atualização para o buffer frontal não será vista até o monitor comece a desenhar novamente. A sincronização vertical é relativamente lenta, no entanto, não lenta o suficiente para renderizar uma cena complexa durante o tempo de espera. O que é necessário para evitar o desmembramento e ser capaz de renderizar cenas complexas é um processo chamado de armazenamento em buffer de fundo.
-   Uma opção para usar uma técnica chamada de armazenamento em buffer de fundo. O armazenamento em buffer de trás é o processo de desenhar uma cena em uma superfície fora da tela, chamada de buffer de fundo. Observe que qualquer superfície diferente do buffer frontal é chamada de superfície fora da tela porque nunca é exibida diretamente pelo monitor. Usando um buffer de fundo, um aplicativo tem a liberdade de renderizar uma cena sempre que o sistema estiver ocioso (ou seja, não há mensagens do Windows esperando) sem precisar considerar a taxa de atualização do monitor. O armazenamento em buffer de fundo traz uma complicação adicional sobre como e quando mover o buffer de fundo para o buffer frontal.

O processo de mover o buffer de fundo para o buffer frontal é chamado de inversão de superfície. Como a placa gráfica simplesmente usa um ponteiro para uma superfície para representar o buffer frontal, uma simples alteração no ponteiro é tudo o que é necessário para definir o buffer de fundo no buffer frontal. Quando um aplicativo solicita ao Direct3D para apresentar o buffer de fundo no buffer frontal, o Direct3D simplesmente "vira" os dois ponteiros de superfície. O resultado é que o buffer de fundo agora é o novo buffer frontal e o buffer frontal antigo é o novo buffer de fundo. A inversão de superfície é invocada sempre que um aplicativo solicita ao dispositivo Direct3D para apresentar o buffer de fundo, no entanto, você pode configurar o Direct3D para enfileirar as solicitações até que uma sincronização vertical ocorra. Essa opção é conhecida como intervalo de apresentação do dispositivo Direct3D. Observe que os dados no novo buffer de fundo podem não ser reutilizáveis, dependendo de como um aplicativo especifica como o Direct3D deve lidar com a inversão da superfície. A inversão de superfície é fundamental para multimídia, animação e software de jogo; ela é equivalente à maneira como você faz animações usando uma folha de papel. Em cada página, o artista muda as figuras ligeiramente, para que ao navegar rapidamente entre as folhas, o desenho pareça animado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Superfícies de Direct3D](direct3d-surfaces.md)
</dt> <dt>

[Invertendo superfícies (Direct3D 9)](flipping-surfaces.md)
</dt> </dl>

 

 




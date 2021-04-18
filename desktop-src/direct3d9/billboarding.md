---
description: Ao criar cenas 3D, um aplicativo pode, às vezes, obter vantagens de desempenho renderizando objetos 2D de forma que eles pareçam ser objetos 3D. Essa é a ideia básica por trás da técnica de mural.
ms.assetid: 6637a9ce-6731-4f60-8b76-854e86b10bdd
title: Mural (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e287624ef8800f0b66941e826e211d044b7bf27
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788972"
---
# <a name="billboarding-direct3d-9"></a>Mural (Direct3D 9)

Ao criar cenas 3D, um aplicativo pode, às vezes, obter vantagens de desempenho renderizando objetos 2D de forma que eles pareçam ser objetos 3D. Essa é a ideia básica por trás da técnica de mural.

Um mural no sentido normal da palavra é um sinal ao longo de um Roadway. Os aplicativos Microsoft Direct3D podem criar e renderizar esse tipo de mensagem definindo um sólido retangular e aplicando uma textura a ele. A mensagem de erro no aspecto mais especializado de gráficos 3D é uma extensão disso. O objetivo é fazer com que objetos 2D pareçam ser 3D. A técnica é aplicar uma textura que contenha a imagem do objeto a um primitivo retangular. O primitivo é girado para que ele sempre gire o usuário. Não importa se a imagem do objeto não é retangular. Partes do mural podem se tornar transparentes, portanto, as partes da imagem do mural que você não deseja ver não são visíveis.

Muitos jogos empregam a mensagem para sprites animados. Por exemplo, quando o usuário está passando por um labirinto 3D, ele pode ver armas ou recompensas que podem ser coletadas. Normalmente, elas são imagens 2D texturizadas em um primitivo retangular. A mensagem é geralmente usada em jogos para renderizar imagens de árvores, bushes e nuvens.

Quando uma imagem é aplicada a um mural, o primitivo retangular deve primeiro ser girado para que a imagem resultante gire o usuário. Seu aplicativo deve então convertê-lo em posição. Em seguida, o aplicativo pode aplicar uma textura à primitiva.

O mural funciona melhor para objetos simétricos, especialmente objetos que são simétricos ao longo do eixo vertical. Ele também exige que a altitude do ponto de vista não aumente muito. Se o usuário tiver permissão para exibir o exibido a partir de acima, será imediatamente aparente que o objeto é 2D em vez de 3D.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos alfa](alpha-examples.md)
</dt> </dl>

 

 




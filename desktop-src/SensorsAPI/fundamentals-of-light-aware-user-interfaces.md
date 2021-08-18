---
description: Conceitos básicos de Light-Aware interfaces de usuário
ms.assetid: 7ea391cb-f72b-4ac1-99be-c957d4ccc8af
title: Conceitos básicos de Light-Aware interfaces de usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8955180dfc57219d3b640c6463f2ee2025f22500d3d29b688bc4b0c154895f66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890176"
---
# <a name="fundamentals-of-light-aware-user-interfaces"></a>Conceitos básicos de Light-Aware interfaces de usuário

O termo *interface do usuário com reconhecimento claro* refere-se a um programa que usa dados de sensor claro para otimizar seu conteúdo, controles e outros gráficos para uma experiência de usuário ideal em muitas condições de iluminação, desde a escuridão até a luz solar. Talvez as otimizações mais importantes sejam legibilidade, legibilidade e interações na luz do sol direta, pois as telas normalmente não têm um bom desempenho nessas condições. Nesta seção, nos concentramos em três propriedades de interface do usuário: escala, contraste e cor. Essas propriedades podem ser alteradas para otimizar a experiência do usuário visual.

## <a name="scale-and-brightness"></a>Escala e brilho

Em geral, os objetos maiores são mais fáceis de ver. Quando o computador está em condições de iluminação negativa (como na luz do sol direta), tornar o conteúdo maior pode ajudar a melhorar a legibilidade e a interativação desse conteúdo.

As fotografias a seguir comparam um laptop no Oriente direto com um brilho de tela típico e níveis de zoom para um laptop nas mesmas condições de iluminação com a interface do usuário com reconhecimento claro. A primeira fotografia mostra a exibição definida como 40% de brilho com níveis de zoom normais. A segunda fotografia mostra a exibição definida como 100% de brilho com níveis de zoom maiores.

![exibição de laptop em 40% de brilho com níveis de zoom normais](images/laptop-40.png)![exibição de laptop em 100% de brilho com níveis de zoom maiores](images/laptop-100.png)

### <a name="varying-font-size"></a>Tamanho de fonte variável

Se você aumentar o tamanho da fonte usada para exibir texto, o texto será mais legível em condições de iluminação negativa. Estilo de fonte, face de fonte e outras características também podem ser variados para otimizar a legibilidade e legibilidade. Por exemplo, as fontes de Sans Serif geralmente são mais fáceis de ler do que as fontes Serif.

![fonte sans serif comparada à fonte serif](images/fonts.png)

### <a name="zooming-content"></a>Ampliando o conteúdo

Se o seu programa implementar o zoom, ele poderá ser usado para dimensionar o conteúdo. O zoom no aumenta a legibilidade enquanto o zoom permite que o programa exiba mais conteúdo.

### <a name="altering-vector-graphic-rendering-properties"></a>Alterando propriedades de renderização de gráfico de vetor

Se o seu programa renderizar primitivos gráficos vetoriais (como linhas, círculos e assim por diante), as características da renderização poderão ser alteradas para otimizar a legibilidade. Por exemplo, se seu programa renderizar retângulos, a largura das linhas usadas para renderizar os retângulos pode ser dimensionada (mais largo para áreas externas e mais estreitas para inportações) para otimizar a aparência e a legibilidade do conteúdo gráfico vetorial.

## <a name="contrast"></a>Contraste

Quando as telas de LCD são usadas em condições de iluminação brilhante, o contraste geral da tela é reduzido. Quando a tela é inundada com luz (do sol, por exemplo), a percepção do usuário de áreas escuras na tela é reduzida. Em geral, isso torna importante aumentar o contraste do conteúdo e da interface do usuário quando a luz ambiente é brilhante. Pode ser desejável usar um esquema de cores monocromático para maximizar o contraste nessas condições de iluminação. Outra maneira de aumentar o contraste é substituir o conteúdo de baixo contraste (como um modo de foto aérea em um programa de mapeamento) por elementos de alto contraste (como o modo gráfico de vetor de ruas preto-em-branco).

## <a name="color"></a>Color

As cores que um programa usa para exibir seu conteúdo podem ter um efeito drástico sobre a experiência geral do usuário e a legibilidade do conteúdo renderizado. Alterando o contraste de cores com base na luz ambiente, você pode tornar o conteúdo mais legível em condições de iluminação negativa, como luz externa brilhante ou luz interior escura.

Uma maneira de aumentar o contraste de cor é por meio da saturação de cor. Outra maneira é usar cores complementares em vez de cores adjacentes para melhorar a legibilidade. Cores complementares são pares de cores que são de matiz oposto, como azul e amarelo. O exemplo lado a lado a seguir mostra como o uso de cores complementares pode ajudar a melhorar o contraste de cores.

![exemplo dos efeitos da cor do texto na legibilidade.](images/color.png)

 

 




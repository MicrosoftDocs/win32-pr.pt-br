---
description: Embora um aplicativo possa usar cores sem considerar as funcionalidades de cor do dispositivo, a saída resultante pode não ser tão informativa e agradável quanto a saída para a qual a cor é cuidadosamente escolhida.
ms.assetid: 008c8a8e-3456-4727-9b27-00b20ae880a2
title: Aproximações de cores e dithering
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af9733259aff787856ac9c6fed68f708c3b580c6200b65652424264eef3c73d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761963"
---
# <a name="color-approximations-and-dithering"></a>Aproximações de cores e dithering

Embora um aplicativo possa usar cores sem considerar as funcionalidades de cor do dispositivo, a saída resultante pode não ser tão informativa e agradável quanto a saída para a qual a cor é cuidadosamente escolhida. Alguns, se algum, os dispositivos garantem uma combinação exata para cada valor de cor possível; portanto, se um aplicativo solicitar uma cor que o dispositivo não pode gerar, o sistema aproximará essa cor usando uma cor que o dispositivo pode gerar. Por exemplo, se um aplicativo tentar criar uma caneta vermelha para uma impressora preta e branca, ele receberá uma caneta preta, em vez disso, o sistema usará preto como a aproximação para vermelho.

Um aplicativo pode descobrir se o sistema aproximará uma determinada cor usando a [**função GetNe approximateColor.**](/windows/desktop/api/Wingdi/nf-wingdi-getnearestcolor) A função recebe um valor de cor e retorna o valor de cor da cor correspondente mais próxima que o dispositivo pode gerar. O método usado pelo sistema para determinar essa aproximação depende do driver do dispositivo e de suas funcionalidades de cor. Na maioria dos casos, a intensidade geral da cor aproximada é mais próxima da cor solicitada.

Quando um aplicativo cria uma caneta ou define a cor do texto, o sistema sempre aproxima uma cor se não houver nenhuma combinação exata. Quando um aplicativo cria um pincel sólido, o sistema pode tentar simular a cor solicitada dithering. *A dithering* simula uma cor alternando duas ou mais cores em um padrão. Por exemplo, diferentes tons de rosa podem ser simulados alternando combinações diferentes de vermelho e branco. Dependendo das cores e do padrão, a dithering pode produzir simulações razoáveis. Ele é mais útil para dispositivos monocromáticos, pois expande o número de "cores" disponíveis bem além do simples preto e branco.

O método usado para criar cores dithered depende do driver do dispositivo. A maioria dos drivers de dispositivo usa um algoritmo de dithering padrão, que gera um padrão com base nos valores de intensidade das cores vermelha, verde e azul solicitadas. Em geral, qualquer cor solicitada que não possa ser gerada pelo dispositivo está sujeita à simulação, mas um aplicativo não é notificado quando o sistema simula uma cor. Além disso, um aplicativo não pode modificar ou alterar o algoritmo de dithering do driver de dispositivo. No entanto, um aplicativo pode ignorar o algoritmo criando e usando pincéis de padrão. Dessa forma, o aplicativo cria suas próprias cores dithered combinando cores sólidas no bitmap que ele usa para criar o pincel.

 

 




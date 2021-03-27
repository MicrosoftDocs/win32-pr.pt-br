---
description: Embora um aplicativo possa usar cores sem considerar os recursos de cores do dispositivo, a saída resultante pode não ser informativa e agradável como saída para a qual a cor é escolhida cuidadosamente.
ms.assetid: 008c8a8e-3456-4727-9b27-00b20ae880a2
title: Aproximações de cores e pontilhamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a72e28dbc3ce20a42b53b5ff060d950719e2d861
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091208"
---
# <a name="color-approximations-and-dithering"></a>Aproximações de cores e pontilhamento

Embora um aplicativo possa usar cores sem considerar os recursos de cores do dispositivo, a saída resultante pode não ser informativa e agradável como saída para a qual a cor é escolhida cuidadosamente. Alguns dispositivos, se houver, garantem uma correspondência exata para cada valor de cor possível; Portanto, se um aplicativo solicitar uma cor que o dispositivo não pode gerar, o sistema aproxima essa cor usando uma cor que o dispositivo pode gerar. Por exemplo, se um aplicativo tentar criar uma caneta vermelha para uma impressora preta e branca, ele receberá uma caneta preta, em vez disso, o sistema usará preto como a aproximação para vermelho.

Um aplicativo pode descobrir se o sistema irá aproximar uma determinada cor usando a função [**GetNearestColor**](/windows/desktop/api/Wingdi/nf-wingdi-getnearestcolor) . A função usa um valor de cor e retorna o valor de cor da cor correspondente mais próxima que o dispositivo pode gerar. O método usado pelo sistema para determinar essa aproximação depende do driver de dispositivo e de seus recursos de cores. Na maioria dos casos, a intensidade geral da cor aproximada está mais próxima da cor solicitada.

Quando um aplicativo cria uma caneta ou define a cor do texto, o sistema sempre aproxima uma cor se não existir nenhuma correspondência exata. Quando um aplicativo cria um pincel sólido, o sistema pode tentar simular a cor solicitada ao pontilhar. O *pontilhamento* simula uma cor alternando duas ou mais cores em um padrão. Por exemplo, diferentes tons de rosa podem ser simulados alternando diferentes combinações de vermelho e branco. Dependendo das cores e do padrão, o pontilhamento pode produzir simulações razoáveis. Ele é mais útil para dispositivos monocromáticos, pois expande o número de "cores" disponíveis, bem além do preto simples e branco.

O método usado para criar cores diquerdas depende do driver de dispositivo. A maioria dos drivers de dispositivo usa um algoritmo de pontilhamento padrão, que gera um padrão com base nos valores de intensidade das cores de vermelho, verde e azul solicitadas. Em geral, qualquer cor solicitada que não possa ser gerada pelo dispositivo está sujeita à simulação, mas um aplicativo não é notificado quando o sistema simula uma cor. Além disso, um aplicativo não pode modificar ou alterar o algoritmo de pontilhamento do driver de dispositivo. Um aplicativo, no entanto, pode ignorar o algoritmo criando e usando pincéis de padrão. Dessa forma, o aplicativo cria suas próprias cores dilaterais combinando cores sólidas no bitmap que ele usa para criar o pincel.

 

 




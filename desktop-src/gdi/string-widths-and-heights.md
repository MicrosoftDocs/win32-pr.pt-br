---
description: Além de recuperar dados de largura de caractere para caracteres individuais, os aplicativos também precisam calcular a largura e a altura de cadeias de caracteres inteiras.
ms.assetid: 0c1d9142-258a-447f-8950-8d684645383b
title: Larguras e alturas da cadeia de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d5a9ee485cbc163cc7cbb9dbd296f15db0e9e622f4be6ad8dcb251b583099f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778816"
---
# <a name="string-widths-and-heights"></a>Larguras e alturas da cadeia de caracteres

Além de recuperar dados de largura de caractere para caracteres individuais, os aplicativos também precisam calcular a largura e a altura de cadeias de caracteres inteiras. Duas funções recuperam medidas de largura e altura de cadeia de caracteres: [**GetTextExtentPoint32**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a)e [**GetTabbedTextExtent**](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta). Se a cadeia de caracteres não contém caracteres de tabulação, um aplicativo pode usar a função **GetTextExtentPoint32** para recuperar a largura e a altura de uma cadeia de caracteres especificada. Se a cadeia de caracteres contiver caracteres de tabulação, um aplicativo deverá chamar a função GetTabbedTextExtent.

Os aplicativos podem usar [**a função GetTextExtentExPoint**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa) para operações de quebra de texto. Essa função retorna o número de caracteres de uma cadeia de caracteres especificada que se ajustam a um espaço especificado.

## <a name="font-ascenders-and-descenders"></a>Ascendentes e descendentes de fontes

Alguns aplicativos determinam o espaçamento de linha entre linhas de texto de tamanhos diferentes usando o máximo ascendente e descendente de uma fonte. Um aplicativo pode recuperar esses valores chamando a [**função GetTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) e, em seguida, verificando os membros **tmAscent** e **tmDescent** do [**TEXTMETRIC.**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)

A ascent e descendente máximas são diferentes da ascente tipográfica e descendente. Em fontes TrueType e OpenType, a ascent e descendente tipográficas normalmente são a parte superior do glifo f e a parte inferior do glifo. Um aplicativo pode recuperar o ascendente tipográfico e o descendente para uma fonte TrueType ou OpenType chamando a função [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) e verificando os valores nos membros **otmMacAscent** e **otmMacDescent** da estrutura [**OUTLINETEXTMETRIC.**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica)

A figura a seguir mostra a diferença entre os valores de métrica de texto vertical retornados nas estruturas [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) e [**OUTLINETEXTMETRIC.**](/windows/win32/api/wingdi/ns-wingdi-outlinetextmetrica) (Os nomes que começam com otm são membros da estrutura **OUTLINETEXTMETRIC.)**

![ilustração que mostra como os valores de métrica de texto contrastam com os valores de métricas de texto de contorno](images/csftx-03.png)

## <a name="font-dimensions"></a>Dimensões de fonte

Um aplicativo pode recuperar as dimensões físicas de uma fonte TrueType ou OpenType chamando a [**função GetOutlineTextMetrics.**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) Um aplicativo pode recuperar as dimensões físicas de qualquer outra fonte chamando a [**função GetTextMetrics.**](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) Para determinar as dimensões de um dispositivo de saída, um aplicativo pode chamar a [**função GetDeviceCaps.**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) **GetDeviceCaps** retorna dimensões físicas e lógicas.

Uma polegada lógica é uma medida que o sistema usa para apresentar fontes legíveis na tela e é aproximadamente de 30 a 40% maior do que uma polegada física. O uso de polegadas lógicas impede uma combinação exata entre a saída da tela e da impressora. Os desenvolvedores devem estar cientes de que o texto em uma tela não é simplesmente uma versão dimensionada do texto que aparecerá na página, especialmente se os gráficos são incorporados ao texto.

 

 

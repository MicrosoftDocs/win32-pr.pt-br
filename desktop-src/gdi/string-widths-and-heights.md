---
description: Além de recuperar dados de largura de caractere para caracteres individuais, os aplicativos também precisam calcular a largura e a altura de cadeias inteiras.
ms.assetid: 0c1d9142-258a-447f-8950-8d684645383b
title: Larguras e alturas da cadeia de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f57846d0588c518f445523361ae186e4b966bf93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827993"
---
# <a name="string-widths-and-heights"></a>Larguras e alturas da cadeia de caracteres

Além de recuperar dados de largura de caractere para caracteres individuais, os aplicativos também precisam calcular a largura e a altura de cadeias inteiras. Duas funções recuperam medidas de largura de cadeia de caracteres e altura: [**GetTextExtentPoint32**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a)e [**GetTabbedTextExtent**](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta). Se a cadeia não contiver caracteres de tabulação, um aplicativo poderá usar a função **GetTextExtentPoint32** para recuperar a largura e a altura de uma cadeia de caracteres especificada. Se a cadeia contiver caracteres de tabulação, um aplicativo deverá chamar a função GetTabbedTextExtent.

Os aplicativos podem usar a função [**GetTextExtentExPoint**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa) para operações de quebra automática de palavras. Essa função retorna o número de caracteres de uma cadeia de caracteres especificada que se ajusta em um espaço especificado.

## <a name="font-ascenders-and-descenders"></a>Fontes ascendentes e descendentes

Alguns aplicativos determinam o espaçamento de linha entre as linhas de texto de tamanhos diferentes usando o máximo de uma fonte ascendente e descendente. Um aplicativo pode recuperar esses valores chamando a função [**GetTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) e, em seguida, verificando os membros **tmAscent** e **tmDescent** do [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica).

O máximo de ascento e descendente são diferentes dos ascendentes tipográficos e descendente. Nas fontes TrueType e OpenType, as descendente tipográficas e as demarcadoras são normalmente a parte superior do glifo f e da parte inferior do glifo g. Um aplicativo pode recuperar o ascendente tipográfico e descendente para uma fonte TrueType ou OpenType chamando a função [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) e verificando os valores nos membros **otmMacAscent** e **otmMacDescent** da estrutura [**OUTLINETEXTMETRIC**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) .

A figura a seguir mostra a diferença entre os valores de métrica de texto vertical retornados nas estruturas [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) e [**OUTLINETEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-outlinetextmetrica) . (Os nomes que começam com OTM são membros da estrutura **OUTLINETEXTMETRIC** .)

![ilustração que mostra como os valores de métrica de texto contrastam com valores de métricas de texto de estrutura de tópicos](images/csftx-03.png)

## <a name="font-dimensions"></a>Dimensões da fonte

Um aplicativo pode recuperar as dimensões físicas de uma fonte TrueType ou OpenType chamando a função [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) . Um aplicativo pode recuperar as dimensões físicas de qualquer outra fonte chamando a função [**GetTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) . Para determinar as dimensões de um dispositivo de saída, um aplicativo pode chamar a função [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) . **GetDeviceCaps** retorna dimensões físicas e lógicas.

Uma polegada lógica é uma medida que o sistema usa para apresentar fontes legíveis na tela e é de aproximadamente 30 a 40 por cento maior do que uma polegada física. O uso de polegadas lógicas impede uma correspondência exata entre a saída da tela e da impressora. Os desenvolvedores devem estar cientes de que o texto em uma tela não é simplesmente uma versão dimensionada do texto que aparecerá na página, especialmente se os elementos gráficos forem incorporados ao texto.

 

 

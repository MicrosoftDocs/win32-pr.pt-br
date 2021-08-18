---
description: Os aplicativos precisam recuperar dados de largura de caractere quando executam tarefas como ajustar cadeias de caracteres de texto para larguras de página ou coluna.
ms.assetid: 0c84f5f9-71cd-4077-bc99-f23a393c1c4d
title: Larguras de caractere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 822ae01ea1ccd5a2a7ec118cb1b93211b1c2e5c0a215737a600d9450b8996117
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117888091"
---
# <a name="character-widths"></a>Larguras de caractere

Os aplicativos precisam recuperar dados de largura de caractere quando executam tarefas como ajustar cadeias de caracteres de texto para larguras de página ou coluna. Há quatro funções que um aplicativo pode usar para recuperar dados de largura de caractere. Duas dessas funções recuperam a largura de avanço de caractere e duas dessas funções recuperam dados reais de largura de caractere.

Um aplicativo pode usar as funções [GetCharWidth32](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a) e [GetCharWidthFloat](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidthfloata) para recuperar a largura avançada para caracteres individuais ou símbolos em uma cadeia de caracteres de texto. A largura de avanço é a distância que o cursor em uma exibição de vídeo ou a cabeça de impressão em uma impressora deve avançar antes de imprimir o próximo caractere em uma cadeia de caracteres de texto. A [**função GetCharWidth32**](/windows/win32/api/wingdi/nf-wingdi-getcharwidth32a) retorna a largura avançada como um valor inteiro. Se uma precisão maior for necessária, um aplicativo poderá usar a [**função GetCharWidthFloat**](/windows/win32/api/wingdi/nf-wingdi-getcharwidthfloata) para recuperar valores fracionais de largura avançada.

Um aplicativo pode recuperar dados reais de largura de caractere usando as funções [GetCharABCWidths](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa) e [**GetCharABCWidthsFloat.**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsfloata) A **função GetCharABCWidthsFloat** funciona com todas as fontes. A [**função GetCharABCWidths**](/windows/win32/api/wingdi/nf-wingdi-getcharabcwidthsa) só funciona com fontes TrueType e OpenType. Para obter mais informações sobre fontes TrueType e OpenType, consulte [Fontes Raster, Vector, TrueType e OpenType](raster--vector--truetype--and-opentype-fonts.md).

A ilustração a seguir mostra os três componentes de uma largura de caractere:

![ilustração mostrando o espaçamento a, espaçamento b e espaçamento c de dois caracteres adjacentes](images/csftx-02.png)

O espaçamento A é a largura a ser acrescentada à posição atual antes de colocar o caractere. O espaçamento B é a largura do próprio caractere. O espaçamento C é o espaço em branco à direita do caractere. A largura de avanço total é determinada calculando a soma de A+B+C. A célula de caractere é um retângulo imaginário que envolve cada caractere ou símbolo em uma fonte. Como os caracteres podem sobrecarr ou subajustar a célula de caracteres, ou ambos os incrementos A e C podem ser um número negativo.

 

 

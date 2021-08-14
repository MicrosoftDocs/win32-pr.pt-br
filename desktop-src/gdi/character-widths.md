---
description: Os aplicativos precisam recuperar dados de largura de caractere quando executam tarefas como ajustar cadeias de caracteres de texto para larguras de página ou coluna.
ms.assetid: 0c84f5f9-71cd-4077-bc99-f23a393c1c4d
title: Larguras de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 822ae01ea1ccd5a2a7ec118cb1b93211b1c2e5c0a215737a600d9450b8996117
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117888091"
---
# <a name="character-widths"></a>Larguras de caracteres

Os aplicativos precisam recuperar dados de largura de caractere quando executam tarefas como ajustar cadeias de caracteres de texto para larguras de página ou coluna. Há quatro funções que um aplicativo pode usar para recuperar dados de largura de caracteres. Duas dessas funções recuperam a largura de avanço de caractere e duas dessas funções recuperam dados reais de largura de caractere.

Um aplicativo pode usar as funções [GetCharWidth32](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a) e [GetCharWidthFloat](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidthfloata) para recuperar a largura antecipada de caracteres ou símbolos individuais em uma cadeia de texto. A largura antecipada é a distância em que o cursor em um vídeo é exibido ou o cabeçote de impressão em uma impressora deve avançar antes de imprimir o próximo caractere em uma cadeia de texto. A função [**GetCharWidth32**](/windows/win32/api/wingdi/nf-wingdi-getcharwidth32a) retorna a largura antecipada como um valor inteiro. Se for necessária uma precisão maior, um aplicativo poderá usar a função [**GetCharWidthFloat**](/windows/win32/api/wingdi/nf-wingdi-getcharwidthfloata) para recuperar valores de largura de avanço fracionário.

Um aplicativo pode recuperar dados de largura de caractere reais usando as funções [GetCharABCWidths](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa) e [**GetCharABCWidthsFloat**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsfloata) . A função **GetCharABCWidthsFloat** funciona com todas as fontes. A função [**GetCharABCWidths**](/windows/win32/api/wingdi/nf-wingdi-getcharabcwidthsa) só funciona com fontes TrueType e OpenType. Para obter mais informações sobre fontes TrueType e OpenType, veja [fontes rasterizadas, vetoriais, TrueType e OpenType](raster--vector--truetype--and-opentype-fonts.md).

A ilustração a seguir mostra os três componentes da largura de um caractere:

![ilustração que mostra o espaçamento entre o espaçamento, o espaçamento b e o c de dois caracteres adjacentes](images/csftx-02.png)

O espaçamento é a largura a ser adicionada à posição atual antes de colocar o caractere. O espaçamento B é a largura do próprio caractere. O espaçamento C é o espaço em branco à direita do caractere. A largura total de avanço é determinada pelo cálculo da soma de A + B + C. A célula Character é um retângulo imaginário que circunda cada caractere ou símbolo em uma fonte. Como os caracteres podem ter folgado ou afetar a célula de caractere, um ou ambos os incrementos de A e C podem ser um número negativo.

 

 

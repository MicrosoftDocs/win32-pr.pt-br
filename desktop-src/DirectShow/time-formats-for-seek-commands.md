---
description: Formatos de hora para comandos de busca
ms.assetid: d9c1b860-f75f-4886-95d6-c62e9e5b69eb
title: Formatos de hora para comandos de busca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8217873a9443c2b56c60523f95a6fe599ee045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506285"
---
# <a name="time-formats-for-seek-commands"></a>Formatos de hora para comandos de busca

Muitos dos métodos na interface **IMediaSeeking** têm parâmetros que expressam valores de posição, como posição atual ou posição de parada. Por padrão, esses parâmetros são expressos em unidades de 100 nanossegundos, também chamados de tempo de referência. Qualquer filtro que possa buscar deve dar suporte à busca por tempo de referência. Alguns filtros também podem buscar usando outras unidades de tempo, como procurar um número de quadro específico ou procurar um determinado deslocamento de byte dentro de um fluxo. Cada uma dessas unidades de tempo é chamada de formato de hora e é definida por um GUID (identificador global exclusivo). Para obter uma lista dos formatos de hora definidos pelo DirectShow, consulte [**GUIDs de formato de tempo**](time-format-guids.md). Terceiros também podem definir GUIDs para formatos de hora personalizados.

Para determinar se os filtros atualmente no grafo de filtro dão suporte a um formato de hora específico, chame o método [**IMediaSeeking:: IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) . O método retornará S \_ OK se o formato tiver suporte. Caso contrário, retornará S \_ false ou um código de erro. Se houver suporte para um formato, você poderá alternar para esse formato chamando o método [**IMediaSeeking:: SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) . Se o método **SetTimeFormat** for executado com sucesso, os comandos de busca subsequentes serão expressos usando o novo formato de hora.

O exemplo a seguir verifica se o grafo dá suporte à busca por número de quadro. Nesse caso, ele procura o número de quadro 20:


```C++
hr = pSeek->IsFormatSupported(&TIME_FORMAT_FRAME);
if (hr == S_OK)
{
    hr = pSeek->SetTimeFormat(&TIME_FORMAT_FRAME);
    if (SUCCEEDED(hr))
    {
        // Seek to frame number 20.
        LONGLONG rtNow = 20;
        hr = pSeek->SetPositions(
            &rtNow, AM_SEEKING_AbsolutePositioning, 
            0, AM_SEEKING_NoPositioning);
    }
}
```



Observe que os formatos de hora se aplicam apenas aos comandos de busca. Eles não afetam a reprodução do grafo ou outras ações.

 

 




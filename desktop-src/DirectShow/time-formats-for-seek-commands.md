---
description: Formatos de tempo para comandos seek
ms.assetid: d9c1b860-f75f-4886-95d6-c62e9e5b69eb
title: Formatos de tempo para comandos seek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e585a7dda12b40e7f501e51aff6ffed50d647066f03804c82e5ffa236f8623a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078716"
---
# <a name="time-formats-for-seek-commands"></a>Formatos de tempo para comandos seek

Muitos dos métodos na interface **IMediaSeeking** têm parâmetros que expressam valores de posição, como posição atual ou posição de parada. Por padrão, esses parâmetros são expressos em unidades de 100 nanossegundos, também chamado de tempo de referência. Qualquer filtro que possa buscar deve dar suporte à busca por tempo de referência. Alguns filtros também podem buscar o uso de outras unidades de tempo, como a busca de um número de quadro específico ou a busca de um determinado deslocamento de byte dentro de um fluxo. Cada uma dessas unidades de tempo é chamada de formato de hora e é definida por um GUID (identificador global exclusivo). Para ver uma lista dos formatos de hora definidos por DirectShow, consulte [**GUIDs de formato de hora**](time-format-guids.md). Terceiros também podem definir GUIDs para formatos de hora personalizados.

Para determinar se os filtros atualmente no grafo de filtro são compatíveis com um formato de tempo específico, chame o [**método IMediaSeeking::IsFormatSupported.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) O método retornará S \_ OK se o formato tiver suporte. Caso contrário, ele retornará S \_ FALSE ou um código de erro. Se um formato tiver suporte, você poderá alternar para esse formato chamando o [**método IMediaSeeking::SetTimeFormat.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) Se o **método SetTimeFormat** for bem-sucedido, os comandos de busca subsequentes serão expressos usando o novo formato de hora.

O exemplo a seguir verifica se o grafo dá suporte à busca por número de quadro. Se sim, ele busca enquadrar o número 20:


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



Observe que os formatos de hora se aplicam somente aos comandos seek. Eles não afetam a reprodução de grafo ou outras ações.

 

 




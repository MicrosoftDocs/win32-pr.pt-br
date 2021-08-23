---
description: Consultando recursos de busca
ms.assetid: d1d8c708-75f2-4dc7-a33a-8dd2cea0ee00
title: Consultando recursos de busca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d1d4389d9e5fcf1466a039ae48bbffb2c26a41c29281101984f6a7a291789f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747446"
---
# <a name="querying-for-seeking-capabilities"></a>Consultando recursos de busca

o Microsoft® DirectShow® oferece suporte à busca pela interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) . o filtro Graph Manager expõe essa interface, mas a funcionalidade de busca sempre é implementada por filtros no grafo.

Alguns dados não podem ser procurados. Por exemplo, você não pode buscar um fluxo de vídeo ao vivo de uma câmera. No entanto, se um fluxo é pesquisável, há vários tipos de busca que ele pode dar suporte. Elas incluem:

-   Buscando uma posição arbitrária no fluxo.
-   Recuperando a duração do fluxo.
-   Recuperando a posição atual dentro do fluxo.
-   Tocando em ordem inversa.

A interface **IMediaSeeking** define um conjunto de sinalizadores, [**está \_ buscando \_ \_ recursos de busca**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities), que descrevem os possíveis recursos de busca. Para recuperar os recursos do Stream, chame o método [**IMediaSeeking:: GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) . O método retorna uma combinação de bits de bit que não é possível. O aplicativo pode testá-los usando o operador de & ( **and** and). Por exemplo, o código a seguir verifica se o grafo pode buscar uma posição arbitrária:


```C++
DWORD dwCap = 0;
HRESULT hr = pSeek->GetCapabilities(&dwCap);
if (AM_SEEKING_CanSeekAbsolute & dwCap)
{
    // Graph can seek to absolute positions.
}
```



 

 




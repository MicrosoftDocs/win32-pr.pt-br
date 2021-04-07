---
description: Consultando recursos de busca
ms.assetid: d1d8c708-75f2-4dc7-a33a-8dd2cea0ee00
title: Consultando recursos de busca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa763ab11267da0a9a13a920285491d83273a8d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825907"
---
# <a name="querying-for-seeking-capabilities"></a>Consultando recursos de busca

O Microsoft® DirectShow® oferece suporte à busca pela interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) . O Gerenciador de gráfico de filtro expõe essa interface, mas a funcionalidade de busca sempre é implementada por filtros no grafo.

Alguns dados não podem ser procurados. Por exemplo, você não pode buscar um fluxo de vídeo ao vivo de uma câmera. No entanto, se um fluxo é pesquisável, há vários tipos de busca que ele pode dar suporte. Estão incluídos:

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



 

 




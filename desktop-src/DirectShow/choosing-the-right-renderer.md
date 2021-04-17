---
description: Escolhendo o processador de vídeo correto
ms.assetid: c57c4c68-ea1c-4198-94b4-e9b6e53bb625
title: Escolhendo o processador de vídeo correto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38a334fec59f6e3631217d48df7f0e8c83d87462
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105812850"
---
# <a name="choosing-the-right-video-renderer"></a>Escolhendo o processador de vídeo correto

O DirectShow fornece vários filtros de processador de vídeo, resumidos na tabela a seguir.



| Filtrar                                                                  | Comentários                                           |
|-------------------------------------------------------------------------|---------------------------------------------------|
| [**Processador de vídeo avançado**](enhanced-video-renderer-filter.md) (EVR) | Usa o Direct3D 9. Requer o Windows Vista ou posterior. |
| [Processador de mixagem de vídeo 9](video-mixing-renderer-filter-9.md) (VMR-9)   | Usa o Direct3D 9. Requer o Windows XP ou posterior.    |
| [Filtro de mixagem de vídeo 7](video-mixing-renderer-filter-7.md) (VMR-7)     | Usa o DirectDraw. Requer o Windows XP ou posterior.    |
| [Mixer de sobreposição](using-the-overlay-mixer-in-video-capture.md)           | Dá suporte a sobreposições de hardware por meio do DirectDraw.    |
| Filtro de [renderização de vídeo](video-renderer-filter.md) herdado.              | Usa o DirectDraw ou o GDI (raramente)                   |



 

O renderizador a ser usado depende em grande parte das versões do Windows às quais você precisa dar suporte.

-   No Windows Vista e posterior, os aplicativos devem usar o EVR se o hardware der suporte a ele. Caso contrário, retorne para o VMR-9 ou o VMR-7. O EVR oferece melhor desempenho e melhor qualidade de vídeo do que os renderizadores anteriores. Além disso, ele foi projetado para trabalhar com o Gerenciador de Janelas da Área de Trabalho (DWM).
-   Antes do Windows Vista, use o VMR-9 se o hardware der suporte à funcionalidade de porta de vídeo e a ela não for necessária. Caso contrário, use o VMR-7.
-   Em sistemas mais antigos, talvez seja necessário usar o mixer de sobreposição (para porta de vídeo ou suporte à sobreposição de hardware) ou o filtro de renderização de vídeo herdado.

Os métodos [**IGraphBuilder:: render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) e [**RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) usam o VMR-7 por padrão. Se o hardware não oferecer suporte ao VMR-7, esses métodos retornarão ao filtro de renderização de vídeo herdado. O EVR e o VMR-9 nunca são os renderizadores padrão.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderização de vídeo](video-rendering.md)
</dt> </dl>

 

 




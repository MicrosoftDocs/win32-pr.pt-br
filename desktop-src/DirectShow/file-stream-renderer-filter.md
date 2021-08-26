---
description: Filtro de renderizador de fluxo de arquivo
ms.assetid: e26462bb-e67f-4522-bec2-88378c4ff442
title: Filtro de renderizador de fluxo de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3da8651d61559a9b22b722f91563426cb067f7a3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470561"
---
# <a name="file-stream-renderer-filter"></a>Filtro de renderizador de fluxo de arquivo

O filtro de renderizador de fluxo de arquivo processa nomes de arquivo analisados pelo filtro [analisador de vários arquivos](multi-file-parser-filter.md) . Para obter mais informações, consulte a documentação para esse filtro.

O uso desse filtro foi preterido. Para renderizar vários arquivos dentro do mesmo grafo de filtro, o aplicativo deve simplesmente chamar **ProcessFile** ou **AddSourceFilter** várias vezes.




| | | Filtrar interfaces | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | | Tipos de mídia de pino de entrada | <ul><li>Tipo principal: MEDIATYPE_File</li><li>Subtipo: GUID_NULL</li><li>Tipo de formato: MEDIATYPE_File</li></ul> | | Interfaces de pino de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Tipos de mídia de pino de saída | Nenhum | | Interfaces de pino de saída | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-istreambuilder"><strong>IStreamBuilder</strong></a> | | CLSID de filtro | CLSID_FileRend | | Executável | Quartz.dll | | <a href="merit.md">Mérito</a> | MERIT_UNLIKELY | | <a href="filter-categories.md">Categoria do filtro</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Comentários

O CLSID do filtro não está definido em UUIDs. h. Use esta macro em seu próprio arquivo de cabeçalho:


```C++
// {D51BD5A5-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_FileRend,
0xd51bd5A5, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filter](directshow-filters.md)
</dt> </dl>

 

 




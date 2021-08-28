---
description: Filtro do renderdor de fluxo de arquivos
ms.assetid: e26462bb-e67f-4522-bec2-88378c4ff442
title: Filtro do renderdor de fluxo de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d438d77b4f402cefed2e80f2c32d061d1652710f
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987859"
---
# <a name="file-stream-renderer-filter"></a>Filtro do renderdor de fluxo de arquivos

O filtro Renderização de Fluxo de Arquivos renderiza os nomes de arquivo que são analisados pelo filtro [Analisador de](multi-file-parser-filter.md) Vários Arquivos. Para obter mais informações, consulte a documentação desse filtro.

O uso desse filtro foi preterido. Para renderizar vários arquivos no mesmo grafo de filtro, o aplicativo deve simplesmente chamar **RenderFile** ou **AddSourceFilter** várias vezes.




| Rótulo | Valor |
|--------|-------|
| Interfaces de filtro | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ibasefilter</strong></a> | 
| Tipos de mídia de pino de entrada | <ul><li>Tipo principal: MEDIATYPE_File</li><li>Subtipo: GUID_NULL</li><li>Tipo de formato: MEDIATYPE_File</li></ul> | 
| Interfaces de pino de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a> | 
| Tipos de mídia de pino de saída | Nenhum | 
| Interfaces de pino de saída | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-istreambuilder"><strong>IStreamBuilder</strong></a> | 
| Filtrar CLSID | CLSID_FileRend | 
| Executável | Quartz.dll | 
| <a href="merit.md">Mérito</a> | MERIT_UNLIKELY | 
| <a href="filter-categories.md">Categoria de filtro</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Comentários

O CLSID do filtro não está definido em Uuids.h. Use essa macro em seu próprio arquivo de header:


```C++
// {D51BD5A5-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_FileRend,
0xd51bd5A5, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 




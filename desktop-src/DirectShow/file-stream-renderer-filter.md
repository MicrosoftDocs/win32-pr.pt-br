---
description: Filtro de renderizador de fluxo de arquivo
ms.assetid: e26462bb-e67f-4522-bec2-88378c4ff442
title: Filtro de renderizador de fluxo de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64c8d8a0c87dab3aa811c8246be24ded8ee04dc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500616"
---
# <a name="file-stream-renderer-filter"></a>Filtro de renderizador de fluxo de arquivo

O filtro de renderizador de fluxo de arquivo processa nomes de arquivo analisados pelo filtro [analisador de vários arquivos](multi-file-parser-filter.md) . Para obter mais informações, consulte a documentação para esse filtro.

O uso desse filtro foi preterido. Para renderizar vários arquivos dentro do mesmo grafo de filtro, o aplicativo deve simplesmente chamar **ProcessFile** ou **AddSourceFilter** várias vezes.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filtrar interfaces</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de mídia de pino de entrada</td>
<td><ul>
<li>Tipo principal: MEDIATYPE_File</li>
<li>Subtipo: GUID_NULL</li>
<li>Tipo de formato: MEDIATYPE_File</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces de pino de entrada</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de mídia do pino de saída</td>
<td>Nenhum</td>
</tr>
<tr class="odd">
<td>Interfaces de pino de saída</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-istreambuilder"><strong>IStreamBuilder</strong></a></td>
</tr>
<tr class="even">
<td>CLSID do filtro</td>
<td>CLSID_FileRend</td>
</tr>
<tr class="odd">
<td>Executável</td>
<td>Quartz.dll</td>
</tr>
<tr class="even">
<td><a href="merit.md">Núcleo</a></td>
<td>MERIT_UNLIKELY</td>
</tr>
<tr class="odd">
<td><a href="filter-categories.md">Categoria do filtro</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentários

O CLSID do filtro não está definido em UUIDs. h. Use esta macro em seu próprio arquivo de cabeçalho:


```C++
// {D51BD5A5-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_FileRend,
0xd51bd5A5, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> </dl>

 

 




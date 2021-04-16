---
description: Filtro do analisador de vários arquivos
ms.assetid: 8ef06f49-fda4-49e2-9b07-70453a2e897c
title: Filtro do analisador de vários arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44fc83a56bb12c307b85be875a3a2e7e73b744d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105779324"
---
# <a name="multi-file-parser-filter"></a>Filtro do analisador de vários arquivos

O filtro analisador de vários arquivos analisa um formato de arquivo simples que permite que vários nomes de arquivo sejam especificados como se fossem um arquivo. Esses arquivos têm o formato mostrado no exemplo a seguir:


```C++
;MULTI
https://server/share/video.mpg
https://server/share/captions.smi
```



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
<li>Tipo principal: MEDIATYPE_Stream</li>
<li>Subtipo: CLSID_MultFile</li>
<li>Tipo de formato: GUID_NULL</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces de pino de entrada</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de mídia do pino de saída</td>
<td><ul>
<li>Tipo principal: MEDIATYPE_File</li>
<li>Subtipo: GUID_NULL</li>
<li>Tipo de formato: MEDIATYPE_File</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces de pino de saída</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>CLSID do filtro</td>
<td>CLSID_MultFile</td>
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

O filtro cria um PIN de saída para cada arquivo listado no arquivo de origem. O tipo de saída é \_ arquivo de MediaType e o bloco de formato para o tipo de saída é uma cadeia de caracteres largos que contém o nome do arquivo. Cada PIN se conecta a uma instância do filtro de [renderizador de fluxo de arquivo](file-stream-renderer-filter.md) . O filtro de renderizador de fluxo de arquivo cria um PIN de saída, que expõe a interface [**IStreamBuilder**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder) . O PIN de saída renderiza o arquivo especificado. Nenhum dado de mídia é transmitido entre o analisador de vários arquivos e o renderizador de fluxo de arquivo.

O CLSID do filtro não está definido em UUIDs. h. Use esta macro em seu próprio arquivo de cabeçalho:


```C++
// {D51BD5A3-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_MultFile,
0xd51bd5a3, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> </dl>

 

 




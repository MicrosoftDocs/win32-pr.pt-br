---
description: Filtro de desenho AVI
ms.assetid: 86cd8e48-7cfa-46e4-b8f4-609b4d09fe80
title: Filtro de desenho AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b6d6b318b7a1f7e762fc0806186114fb9256f5c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087326"
---
# <a name="avi-draw-filter"></a>Filtro de desenho AVI

O filtro de desenho AVI é puxado automaticamente para um grafo de reprodução em vez do [descompactador AVI](avi-decompressor-filter.md) quando o vídeo está sendo impresso em um monitor de televisão NTSC externo.



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
<td>Tipo principal: MEDIATYPE_VideoSubtypes:<br/>
<ul>
<li>MEDIASUBTYPE_MJPG</li>
<li>MEDIASUBTYPE_TVMJ</li>
<li>MEDIASUBTYPE_WAKE</li>
<li>MEDIASUBTYPE_CFCC</li>
<li>MEDIASUBTYPE_IJPG</li>
<li>MEDIASUBTYPE_Plum</li>
<li>MEDIASUBTYPE_DVCS</li>
<li>MEDIASUBTYPE_DVSD</li>
<li>MEDIASUBTYPE_MDVF</li>
<li>Tipo de formato: FORMAT_VideoInfo</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces de pino de entrada</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de mídia do pino de saída</td>
<td>MEDIATYPE_Video, MEDIASUBTYPE_NULL</td>
</tr>
<tr class="odd">
<td>Interfaces de pino de saída</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify"><strong>IOverlayNotify</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>CLSID do filtro</td>
<td>CLSID_AVIDraw</td>
</tr>
<tr class="odd">
<td>CLSID de página de propriedades</td>
<td>Nenhuma página de propriedades.</td>
</tr>
<tr class="even">
<td>Executável</td>
<td>quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Núcleo</a></td>
<td>MERIT_NORMAL + 100</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoria do filtro</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentários

Como o filtro de desenho do AVI e o [filtro de captura do VFW](vfw-capture-filter.md) se conectam ao mesmo hardware, eles não podem estar no mesmo grafo de filtro.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> </dl>

 

 





---
description: Filtro de decodificador de vídeo MPEG-1
ms.assetid: 272d2f31-6e57-4ce5-ac86-b4d47f661fea
title: Filtro de decodificador de vídeo MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e72e575baf6761a34078ee4413b6dd095871a646d9539d08c9357ffd8af5efd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051016"
---
# <a name="mpeg-1-video-decoder-filter"></a>Filtro de decodificador de vídeo MPEG-1

Decodifica o vídeo MPEG-1.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaces de filtro</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a> <strong>ISpecifyPropertyPages</strong></td>
</tr>
<tr class="even">
<td>Tipos de mídia de pino de entrada</td>
<td>MEDIATYPE_Video, FORMAT_MPEGVideo<br/> Os seguintes subtipos são válidos:<br/>
<ul>
<li><strong>MEDIASUBTYPE_MPEG1Packet</strong></li>
<li><strong>MEDIASUBTYPE_MPEG1Payload</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces de pino de entrada</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"> <strong>IMemInputPin</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de mídia de pino de saída</td>
<td>Tipo principal: <strong>MEDIATYPE_Video</strong>,<br/> Tipo de formato: <strong>FORMAT_VideoInfo</strong> ou <strong>FORMAT_VideoInfo2</strong><br/> Subtipos:<br/>
<ul>
<li><strong>MEDIASUBTYPE_RGB24</strong></li>
<li><strong>MEDIASUBTYPE_RGB32</strong></li>
<li><strong>MEDIASUBTYPE_RGB8</strong></li>
<li><strong>MEDIASUBTYPE_RGB555</strong></li>
<li><strong>MEDIASUBTYPE_RGB565</strong></li>
<li><strong>MEDIASUBTYPE_UYVY</strong></li>
<li><strong>MEDIASUBTYPE_Y41P</strong></li>
<li><strong>MEDIASUBTYPE_YUY2</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces de pino de saída</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Filtrar CLSID</td>
<td><strong>CLSID_CMpegVideoCodec</strong></td>
</tr>
<tr class="odd">
<td>CLSID da página de propriedades</td>
<td><strong>CLSID_MpegVideoDecodePropertyPage</strong></td>
</tr>
<tr class="even">
<td>Executável</td>
<td>quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Mérito</a></td>
<td>0x40000001</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoria de filtro</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentários

Esse filtro pode decodificar em uma Superfície directDraw. O filtro usará MMX se o computador for compatível com MMX.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 





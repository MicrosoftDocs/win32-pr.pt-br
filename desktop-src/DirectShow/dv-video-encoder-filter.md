---
description: Filtro de codificador de vídeo DV
ms.assetid: ac57bd11-de16-4a58-9f4b-da270a57ad08
title: Filtro de codificador de vídeo DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73b91da15fda0597e9b943c78fd5a6716021a3ae
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103919743"
---
# <a name="dv-video-encoder-filter"></a>Filtro de codificador de vídeo DV

Esse filtro codifica um fluxo de vídeo descompactado em vídeo digital (DV). Ele fornece uma interface personalizada, [**IDVEnc**](/windows/desktop/api/Strmif/nn-strmif-idvenc), para definir a resolução e o formato da codificação.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filtrar interfaces</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamvideocompression"><strong>IAMVideoCompression</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvenc"><strong>IDVEnc</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>, <strong>IPersistStream</strong>, <strong>ISpecifyPropertyPages</strong></td>
</tr>
<tr class="even">
<td>Tipos de mídia de pino de entrada</td>
<td><ul>
<li>Tipo principal: MEDIATYPE_VideoThe seguintes subtipos são válidos:<br/>
<ul>
<li>MEDIASUBTYPE_RGB24</li>
<li>MEDIASUBTYPE_RGB565</li>
<li>MEDIASUBTYPE_RGB555</li>
</ul></li>
<li>Tipo de formato: FORMAT_VideoInfo</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces de pino de entrada</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de mídia do pino de saída</td>
<td><ul>
<li>Tipo principal: MEDIATYPE_Video</li>
<li>Subtipo: MEDIASUBTYPE_dvsd</li>
<li>Tipo de formato: FORMAT_VideoInfo</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces de pino de saída</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>CLSID do filtro</td>
<td>CLSID_DVVideoEnc</td>
</tr>
<tr class="odd">
<td>CLSID de página de propriedades</td>
<td>CLSID_DVEncPropertiesPage</td>
</tr>
<tr class="even">
<td>Executável</td>
<td>qdv.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Núcleo</a></td>
<td>MERIT_DO_NOT_USE</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoria do filtro</a></td>
<td>CLSID_VideoCompressorCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentários

Para vídeo de 16 bits (MEDIASUBTYPE \_ RGB555 ou MEDIASUBTYPE \_ RGB565), a entrada deve ter 720 x 480 pixels para NTSC ou 720 x 576 pixels para PAL. Para vídeo de 24 bits, não há restrições de tamanho na entrada.

A saída é sempre 720 x 480 para NTSC ou 720 x 576 para PAL; o vídeo de 24 bits é dimensionado para se ajustar a essas dimensões.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> <dt>

[Vídeo digital no DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 





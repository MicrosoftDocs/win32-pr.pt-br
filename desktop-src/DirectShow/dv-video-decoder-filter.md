---
description: Filtro de decodificador de vídeo DV
ms.assetid: aa47010e-8510-475d-836a-cb63deeb3a7b
title: Filtro de decodificador de vídeo DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6baab43d4a369cb16d92974a0e6e469c914961bb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500153"
---
# <a name="dv-video-decoder-filter"></a>Filtro de decodificador de vídeo DV

Esse filtro decodifica um fluxo de vídeo digital (DV) em vídeo descompactado.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filtrar interfaces</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iipdvdec"><strong>IIPDVDec</strong></a>, <strong>IPersistStream</strong>, <strong>ISpecifyPropertyPages</strong></td>
</tr>
<tr class="even">
<td>Tipos de mídia de pino de entrada</td>
<td><ul>
<li>MEDIATYPE_Video</li>
<li>MEDIASUBTYPE_dvsd</li>
<li>FORMAT_VideoInfo, FORMAT_DvInfo</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces de pino de entrada</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de mídia do pino de saída</td>
<td><strong>Tipo principal</strong>: MEDIATYPE_Video<strong>subtipos</strong>:<br/>
<ul>
<li>MEDIASUBTYPE_YUY2</li>
<li>MEDIASUBTYPE_UYVY</li>
<li>MEDIASUBTYPE_RGB24</li>
<li>MEDIASUBTYPE_RGB32</li>
<li>MEDIASUBTYPE_ARGB32</li>
<li>MEDIASUBTYPE_RGB565</li>
<li>MEDIASUBTYPE_RGB555</li>
<li>MEDIASUBTYPE_RGB8</li>
<li>MEDIASUBTYPE_Y41P</li>
</ul>
<strong>Tipos de formato</strong>:<br/> Format_VideoInfo, Format_VideoInfo2<br/></td>
</tr>
<tr class="odd">
<td>Interfaces de pino de saída</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>CLSID do filtro</td>
<td>CLSID_DVVideoCodec</td>
</tr>
<tr class="odd">
<td>CLSID de página de propriedades</td>
<td>CLSID_DVDecPropertiesPage</td>
</tr>
<tr class="even">
<td>Executável</td>
<td>qdv.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Núcleo</a></td>
<td>MERIT_NORMAL</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoria do filtro</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentários

Use a interface [**IIPDVDec**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec) para definir a resolução de decodificação como Full, meia-size, tamanho de trimestre ou um oitavo tamanho.

**Entrelaçamento**: as versões anteriores do decodificador sempre desentrelaçam o vídeo. A partir do DirectX 9,0, o decodificador de vídeo DV pode preservar o entrelaçamento. Isso permite que o vídeo entrelaçado seja desentrelaçado pelo VMR (Video Misturation Renderer), para melhor qualidade de renderização. Para usar esse recurso, o filtro downstream deve dar suporte a formatos [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , indicados pelo formato de valor \_ VideoInfo2 no membro **formatType** da estrutura do [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . Na saída de resolução completa, os sinalizadores de desentrelaçamento (**dwInterlace**) na estrutura **VIDEOINFOHEADER2** são definidos como `AMINTERLACE_IsInterlaced | AMINTERLACE_DisplayModeBobOrWeave` , indicando campos entrelaçados. Na metade da resolução ou inferior, **dwInterlace** é definido como zero, indicando quadros progressivos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> <dt>

[Vídeo digital no DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 





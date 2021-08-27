---
description: Filtro de decodificador de vídeo DV
ms.assetid: aa47010e-8510-475d-836a-cb63deeb3a7b
title: Filtro de decodificador de vídeo DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12131aa09f8e3f7dbef56504ad55410af11ffcbe
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466043"
---
# <a name="dv-video-decoder-filter"></a>Filtro de decodificador de vídeo DV

Esse filtro decodifica um fluxo de vídeo digital (DV) em um vídeo descompactado.




| | | Interfaces de filtro | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iipdvdec"><strong>IIPDVDec,</strong></a> <strong>IPersistStream,</strong> <strong>ISpecifyPropertyPages</strong> | | Tipos de mídia de pino de entrada | <ul><li>MEDIATYPE_Video</li><li>MEDIASUBTYPE_dvsd</li><li>FORMAT_VideoInfo, FORMAT_DvInfo</li></ul> | | Interfaces de pino de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Tipos de mídia de pino de | <strong>Tipo principal:</strong>MEDIATYPE_Video<strong>subtipos</strong>:<br /><ul><li>MEDIASUBTYPE_YUY2</li><li>MEDIASUBTYPE_UYVY</li><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB32</li><li>MEDIASUBTYPE_ARGB32</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB555</li><li>MEDIASUBTYPE_RGB8</li><li>MEDIASUBTYPE_Y41P</li></ul><strong>Tipos de formato:</strong><br /> Format_VideoInfo, Format_VideoInfo2<br /> | | Interfaces de pino de | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Filtrar CLSID | CLSID_DVVideoCodec | | ClSID da página de propriedades | CLSID_DVDecPropertiesPage | | Arquivo executável | qdv.dll | | <a href="merit.md">|</a> MERIT_NORMAL | | <a href="filter-categories.md">Categoria de</a> filtro | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Comentários

Use a interface [**IIPDVDec**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec) para definir a resolução de decodificação como tamanho completo, meio tamanho, tamanho de trimestre ou um oitavo tamanho.

**Entrelaçamento:** versões anteriores do decodificador sempre desinteressam o vídeo. A partir do DirectX 9.0, o Decodificador de Vídeo DV pode preservar o entrelaçamento. Isso permite que o vídeo entrelaçado seja desintercalado pela VMR (Video Mixing Renderer), para melhorar a qualidade de renderização. Para usar esse recurso, o filtro downstream deve dar suporte aos formatos [**VIDEOINFOHEADER2,**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) indicados por esse valor Format VideoInfo2 no membro formattype da estrutura \_ AM MEDIA [**\_ \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type)  Na saída de resolução completa, os sinalizadores de desintercalação (**dwIntercto**) na estrutura **VIDEOINFOHEADER2** são definidos como , indicando campos `AMINTERLACE_IsInterlaced | AMINTERLACE_DisplayModeBobOrWeave` entrelaçados. Na metade da resolução ou inferior, **dwInter frames** é definido como zero, indicando quadros progressivos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[Vídeo digital no DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 





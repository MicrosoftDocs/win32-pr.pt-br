---
description: Filtro de codificador de vídeo DV
ms.assetid: ac57bd11-de16-4a58-9f4b-da270a57ad08
title: Filtro de codificador de vídeo DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e14928c937313d056549a348bd255f251354c0ab
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482632"
---
# <a name="dv-video-encoder-filter"></a>Filtro de codificador de vídeo DV

Esse filtro codifica um fluxo de vídeo descompactado em vídeo digital (DV). Ele fornece uma interface personalizada, [**IDVEnc**](/windows/desktop/api/Strmif/nn-strmif-idvenc), para definir a resolução e o formato da codificação.




| | | Filtrar interfaces | <a href="/windows/desktop/api/Strmif/nn-strmif-iamvideocompression"><strong>IAMVideoCompression</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvenc"><strong>IDVEnc</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>, <strong>IPersistStream</strong>, <strong>ISpecifyPropertyPages</strong> | | Tipos de mídia de pino de entrada | <ul><li>Tipo principal: MEDIATYPE_VideoThe seguintes subtipos são válidos:<br /><ul><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB555</li></ul></li><li>Tipo de formato: FORMAT_VideoInfo</li></ul> | | Interfaces de pino de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Tipos de mídia de pino de saída | <ul><li>Tipo principal: MEDIATYPE_Video</li><li>Subtipo: MEDIASUBTYPE_dvsd</li><li>Tipo de formato: FORMAT_VideoInfo</li></ul> | | Interfaces de pino de saída | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | CLSID de filtro | CLSID_DVVideoEnc | | CLSID da página de propriedades | CLSID_DVEncPropertiesPage | | Executável | qdv.dll | | <a href="merit.md">Mérito</a> | MERIT_DO_NOT_USE | | <a href="filter-categories.md">Categoria do filtro</a> | CLSID_VideoCompressorCategory | 




 

## <a name="remarks"></a>Comentários

Para vídeo de 16 bits (MEDIASUBTYPE \_ RGB555 ou MEDIASUBTYPE \_ RGB565), a entrada deve ter 720 x 480 pixels para NTSC ou 720 x 576 pixels para PAL. Para vídeo de 24 bits, não há restrições de tamanho na entrada.

A saída é sempre 720 x 480 para NTSC ou 720 x 576 para PAL; o vídeo de 24 bits é dimensionado para se ajustar a essas dimensões.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filter](directshow-filters.md)
</dt> <dt>

[Vídeo digital no DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 





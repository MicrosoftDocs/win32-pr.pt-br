---
description: Filtro do analisador de som WAVE
ms.assetid: 53a9538d-7a79-40bb-9468-d710eb238925
title: Filtro do analisador de som WAVE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d91508500b02743f7cac8b4ed5cff718d12e3b03
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987849"
---
# <a name="wave-parser-filter"></a>Filtro do analisador de som WAVE

O filtro WAVE Parser analisa dados de áudio de formato WAV de arquivos. wav,. au ou. aif. O filtro upstream deve ser o filtro de [origem de arquivo assíncrono](file-source--async--filter.md) , o filtro de [origem de arquivo de URL](file-source--url--filter.md) ou um filtro de origem assíncrono de terceiros compatível que contenha dados de áudio WAV. O fluxo de saída são dados de áudio, que você pode conectar diretamente a um filtro de renderização de áudio ou a um filtro de transformação de áudio intermediário.




| Rótulo | Valor |
|--------|-------|
| Filtrar interfaces | <a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a> | 
| Tipos de mídia de pino de entrada | Tipo principal: MEDIATYPE_StreamThe seguintes subtipos são válidos:<br /><ul><li>MEDIASUBTYPE_AIFF</li><li>MEDIASUBTYPE_AU</li><li>MEDIASUBTYPE_WAVE</li></ul> | 
| Interfaces de pino de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a> | 
| Tipos de mídia do pino de saída | Tipo principal: MEDIATYPE_AudioSubtype: MEDIASUBTYPE_PCM ou outro tipo de compactação. (Consulte <a href="audio-subtypes.md"><strong>subtipos de áudio</strong></a>.)<br /> Tipo de formato: FORMAT_WaveFormatEx<br /> | 
| Interfaces de pino de saída | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a> | 
| CLSID do filtro | {D51BD5A1-7548-11cf-A520-0080C77EF58A} | 
| CLSID de página de propriedades | Nenhuma página de propriedades. | 
| Executável | quartz.dll | 
| <a href="merit.md">Núcleo</a> | MERIT_UNLIKELY | 
| <a href="filter-categories.md">Categoria do filtro</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Comentários

Este filtro dá suporte aos seguintes tipos de arquivo:

-   ONDA (. wav)
-   AIFF e AIFF-C (. aif)
-   AU (. au)

No entanto, ele tem as seguintes limitações no formato de áudio:

-   O áudio deve ser um PCM linear de 8 bits ou 16 bits.
-   Para arquivos AIFF-C, o áudio deve ser descompactado, em ordem de byte big endian (tipo de compactação ' NONE ').

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filter](directshow-filters.md)
</dt> </dl>

 

 





---
description: Filtro de decodificador de áudio MPEG-1
ms.assetid: 2f695ac6-7d4b-41a8-b4c5-83fb9d20ab9d
title: Filtro de decodificador de áudio MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c3c014497d8b3db5aaf3031250e78edd8b59cb2
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983819"
---
# <a name="mpeg-1-audio-decoder-filter"></a>Filtro de decodificador de áudio MPEG-1

Decodifica o áudio de camada I e camada II MPEG-1 para PCM.




| Rótulo | Valor |
|--------|-------|
| Filtrar interfaces | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong> | 
| Tipos de mídia de pino de entrada | MEDIATYPE_Audio, FORMAT_WaveFormatEx<br /> Os seguintes subtipos são válidos:<br /><ul><li>MEDIASUBTYPE_MPEG1Packet</li><li>MEDIASUBTYPE_MPEG1Payload</li><li>MEDIASUBTYPE_MPEG1AudioPayload</li><li>GUID_NULL</li></ul> | 
| Interfaces de pino de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Tipos de mídia do pino de saída | MEDIATYPE_Audio, MEDIASUBTYPE_PCM | 
| Interfaces de pino de saída | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| CLSID do filtro | CLSID_CMpegAudioCodec | 
| CLSID de página de propriedades | CLSID_MpegAudioDecoderPropertyPage | 
| Executável | quartz.dll | 
| <a href="merit.md">Núcleo</a> | 0x03680001 | 
| <a href="filter-categories.md">Categoria do filtro</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filter](directshow-filters.md)
</dt> </dl>

 

 





---
description: O filtro de codificador MPEG-2 da Microsoft codificará áudio e vídeo MPEG-2 e multiplexa os fluxos para gerar um fluxo de programa MPEG-2 ou fluxo de transporte.
ms.assetid: 61e8918b-7f5a-4720-bb3b-df9ac7614894
title: Codificador MPEG-2 da Microsoft (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef5fad3b316db9ac4e47efcb9de761227cdd3279
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645766"
---
# <a name="microsoft-mpeg-2-encoder"></a>Codificador MPEG-2 da Microsoft

O filtro de codificador MPEG-2 da Microsoft codificará áudio e vídeo MPEG-2 e multiplexa os fluxos para gerar um fluxo de programa MPEG-2 ou fluxo de transporte.

> [!Note]  
> Não há suporte para esse filtro em plataformas baseadas em IA-64.

 



Informações de filtro

Filtrar interfaces

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> **IEncoderAPI**<br/> [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IVideoEncoder**](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

Tipos de mídia de pino de entrada

Ver comentários

Interfaces de pino de entrada

[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Tipos de mídia do pino de saída

Ver comentários

Interfaces de pino de saída

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

CLSID do filtro

**CLSID \_ do CMPEG2EncoderDS** (declarado em wmcodecdsp. h)

Executável

msmpeg2enc.dll

[Núcleo](merit.md)

**MÉRITO \_ \_ não \_ use**

[Categoria do filtro](filter-categories.md)

**\_LEGACYAMFILTERCATEGORY CLSID**



 

## <a name="remarks"></a>Comentários

Esse filtro combina a funcionalidade de codificação de dois outros filtros:

-   [**Codificador de áudio Microsoft MPEG-2**](microsoft-mpeg-2-audio-encoder.md)
-   [**Codificador de vídeo MPEG-2 da Microsoft**](microsoft-mpeg-2-video-encoder.md)

Exceto como observado, esse filtro oferece suporte aos mesmos recursos de codificação que os dois codificadores.

Inicialmente, o filtro tem um pino de entrada, que pode aceitar entrada de áudio ou vídeo. Quando esse PIN é conectado, o filtro cria um segundo PIN de entrada. Se o primeiro PIN de entrada receber áudio, o segundo PIN de entrada aceitará apenas o vídeo e vice-versa. Cada PIN de entrada dá suporte aos mesmos tipos de mídia que o filtro de codificador correspondente.

Se apenas um PIN de entrada estiver conectado, o filtro dará suporte aos mesmos tipos de saída que o codificador de áudio ou vídeo correspondente. Se ambos os Pins estiverem conectados, o filtro dará suporte aos seguintes tipos de saída:

-   Áudio-visual em um fluxo de programa MPEG-2
-   Áudio-visual em um fluxo de transporte MPEG-2

Eles correspondem aos seguintes tipos de saída:

-   **MediaType \_ Fluxo**, **\_ \_ programa MEDIASUBTYPE MPEG2**
-   **MediaType \_ Fluxo**, **\_ \_ transporte MEDIASUBTYPE MPEG2**

Esse filtro não pode multiplexar fluxos que foram codificados anteriormente. Os fluxos de entrada devem ser áudio/vídeo descompactado, que o filtro codifica antes da multiplexação. O fluxo multiplexado é limitado a um programa, contendo até um áudio e um fluxo de vídeo.

### <a name="codec-properties"></a>Propriedades do codec

O filtro dá suporte às propriedades combinadas do [**codificador de áudio MPEG-2**](microsoft-mpeg-2-audio-encoder.md) e dos filtros de [**codificador de vídeo MPEG-2**](microsoft-mpeg-2-video-encoder.md) , com a seguinte diferença:

-   A propriedade [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md) define a taxa média de bits para o fluxo de vídeo.
-   A propriedade [**AVEncAudioMeanBitRate**](avencaudiomeanbitrate.md) define a taxa média de bits para o fluxo de áudio.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop apps\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                                                                                     |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> </dl>

 

 

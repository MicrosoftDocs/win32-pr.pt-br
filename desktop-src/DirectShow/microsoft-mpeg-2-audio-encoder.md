---
description: O filtro Microsoft MPEG-2 Audio Encoder codifica as camadas de áudio MPEG-1 I e II, incluindo suporte para as extensões MPEG-2 Low amostragem Frequency (LSF).
ms.assetid: a36e838b-8b11-4851-9dd2-efd9fe070770
title: Codificador de áudio Microsoft MPEG-2 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43d055acd379d9e966f43eac284e38a10c05a86c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105759494"
---
# <a name="microsoft-mpeg-2-audio-encoder"></a>Codificador de áudio Microsoft MPEG-2

O filtro Microsoft MPEG-2 Audio Encoder codifica as camadas de áudio MPEG-1 I e II, incluindo suporte para as extensões MPEG-2 Low amostragem Frequency (LSF).

Para codificar e multiplexar fluxos de áudio/vídeo, use o filtro de [**codificador MPEG-2 da Microsoft**](microsoft-mpeg-2-encoder.md) , que encapsula as funções desse filtro e do filtro de [**codificador de vídeo MPEG-2 da Microsoft**](microsoft-mpeg-2-video-encoder.md) .

> [!Note]  
> Não há suporte para esse filtro em plataformas baseadas em IA-64.

 



Informações de filtro

Filtrar interfaces

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> **IEncoderAPI**<br/> [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IVideoEncoder**](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

Tipos de mídia de pino de entrada

**MediaType \_ Áudio**, **MEDIASUBTYPE \_ PCM**

Interfaces de pino de entrada

[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Tipos de mídia do pino de saída

**MediaType \_ Áudio**, **\_ \_ áudio MEDIASUBTYPE MPEG2**<br/> **MediaType \_ Fluxo**, **\_ \_ áudio MEDIASUBTYPE MPEG2**<br/> **MediaType \_ Fluxo**, **\_ \_ programa MEDIASUBTYPE MPEG2**<br/> **MediaType \_ Fluxo**, **\_ \_ transporte MEDIASUBTYPE MPEG2**<br/>

Interfaces de pino de saída

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

CLSID do filtro

**CLSID \_ do CMPEG2EncoderAudioDS** (declarado em wmcodecdsp. h)

Executável

msmpeg2enc.dll

[Núcleo](merit.md)

**MÉRITO \_ \_ não \_ use**

[Categoria do filtro](filter-categories.md)

**\_LEGACYAMFILTERCATEGORY CLSID**



 

## <a name="remarks"></a>Comentários

O codificador de áudio MPEG-2 pode produzir os seguintes tipos de saída:

-   Fluxo elementar áudio
-   Áudio em um fluxo de programa MPEG-2
-   Áudio em um fluxo de transporte MPEG-2

Ele dá suporte a camadas MPEG-1 I e II e extensões LSF (baixa amostragem Frequency) de MPEG-2

Os exemplos de entrada devem ter 16 bits por amostra, com uma taxa de amostragem de áudio de 48, 44,1, 32, 22, 5 ou 16 KHz. O codificador não pode reamostrar o fluxo de áudio; o áudio codificado tem a mesma taxa de amostragem que a entrada.

Os exemplos de entrada devem ser mono ou estéreo. O áudio codificado tem o número de canais como entrada.

### <a name="limitations"></a>Limitações

O codificador não oferece suporte ao seguinte:

-   Áudio MPEG Layer III fragmentado.
-   Extensão de vários canais MPEG-2 fragmentado.
-   MPEG-4 AAC fragmentado.
-   Fragmentado (NBC) compatível com MPEG-2 sem versões anteriores.
-   Geração de pacotes de pacote de fluxo elementar (PES).
-   Codificação digital Dolby.

### <a name="codec-properties"></a>Propriedades do codec

O filtro oferece suporte às seguintes propriedades por meio de [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):

-   [**AVAudioChannelCount**](avaudiochannelcount-property.md)
-   [**AVAudioSampleRate**](avaudiosamplerate-property.md)
-   [**AVEncAudioIntervalToEncode**](avencaudiointervaltoencode-property.md)
-   [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)
-   [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md)
-   [**AVEncMPACodingMode**](avencmpacodingmode-property.md)
-   [**AVEncMPACopyright**](avencmpacopyright-property.md)
-   [**AVEncMPAEmphasisType**](avencmpaemphasistype-property.md)
-   [**AVEncMPAEnableRedundancyProtection**](avencmpaenableredundancyprotection-property.md)
-   [**AVEncMPALayer**](avencmpalayer-property.md)
-   [**AVEncMPAOriginalBitstream**](avencmpaoriginalbitstream-property.md)
-   [**AVEncMPAPrivateUserBit**](avencmpaprivateuserbit-property.md)

> [!Note]  
> Uma versão anterior da documentação listava incorretamente algumas propriedades adicionais que não têm suporte.

 

Para compatibilidade com versões anteriores, o filtro oferece suporte à seguinte propriedade por meio da interface **IEncoderAPI** :



| Propriedade                 | Descrição                                                                      |
|--------------------------|----------------------------------------------------------------------------------|
| **\_taxa de bits ENCAPIPARAM** | Equivalente a [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md). |



 

É recomendável definir as propriedades na seguinte ordem:

1.  [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)
2.  [**AVEncMPALayer**](avencmpalayer-property.md)
3.  [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md)
4.  [**AVEncMPACodingMode**](avencmpacodingmode-property.md)

Defina as propriedades restantes em qualquer ordem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop apps\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                                                                                     |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> <dt>

[**Tipos de mídia de Desmultiplexador MPEG-2**](mpeg-2-demultiplexer-media-types.md)
</dt> </dl>

 

 

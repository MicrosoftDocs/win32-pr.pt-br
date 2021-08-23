---
description: O filtro Microsoft MPEG-2 Audio Encoder codifica as camadas de áudio MPEG-1 I e II, incluindo suporte para as extensões de LSF (Baixa Frequência de Amostragem) MPEG-2.
ms.assetid: a36e838b-8b11-4851-9dd2-efd9fe070770
title: Codificador de Áudio Microsoft MPEG-2 (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 030821905862a9698ee24c3227f2846cd8c892e20c501d2776cdf2f9bb88f3e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584116"
---
# <a name="microsoft-mpeg-2-audio-encoder"></a>Codificador de áudio do Microsoft MPEG-2

O filtro Microsoft MPEG-2 Audio Encoder codifica as camadas de áudio MPEG-1 I e II, incluindo suporte para as extensões de LSF (Baixa Frequência de Amostragem) MPEG-2.

Para codificar e multiplexar fluxos de áudio/vídeo, use o filtro [**codificador Microsoft MPEG-2,**](microsoft-mpeg-2-encoder.md) que encapsula as funções desse filtro e do filtro do Codificador de Vídeo [**do Microsoft MPEG-2.**](microsoft-mpeg-2-video-encoder.md)

> [!Note]  
> Não há suporte para esse filtro em plataformas baseadas em IA-64.

 



Informações de filtro

Interfaces de filtro

[**Ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> **IEncoderAPI**<br/> [**Imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IVideoEncoder**](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

Tipos de mídia de pino de entrada

**MEDIATYPE \_ ÁUDIO**, **MEDIASUBTYPE \_ PCM**

Interfaces de pino de entrada

[**Imeminputpin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**Iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Tipos de mídia de pino de saída

**MEDIATYPE \_ Áudio**, **MEDIASUBTYPE \_ MPEG2 \_ AUDIO**<br/> **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ MPEG2 \_ AUDIO**<br/> **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ MPEG2 \_ PROGRAM**<br/> **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT**<br/>

Interfaces de pino de saída

[**Imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**Iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Filtrar CLSID

**CLSID \_ CMPEG2EncoderAudioDS** (declarado em wmcodecdsp.h)

Executável

msmpeg2enc.dll

[Mérito](merit.md)

**NÃO USE O NÃO \_ \_ USO \_ DE LIMITED**

[Categoria de filtro](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

## <a name="remarks"></a>Comentários

O Codificador de Áudio MPEG-2 pode produzir os seguintes tipos de saída:

-   Fluxo elementar de áudio
-   Áudio em um fluxo de programa MPEG-2
-   Áudio em um fluxo de transporte MPEG-2

Ele dá suporte a extensões de LSF (frequência de amostragem baixa) mpEG-1 e II e MPEG-2

As amostras de entrada devem ter 16 bits por amostra, com uma taxa de amostragem de áudio de 48, 44,1, 32, 22,05 ou 16 KHz. O codificador não pode resamplor o fluxo de áudio; o áudio codificado tem a mesma taxa de exemplo que a entrada.

As amostras de entrada devem ser mono ou estéreo. O áudio codificado tem o número de canais como entrada.

### <a name="limitations"></a>Limitações

O codificador não dá suporte ao seguinte:

-   Bitstreams de áudio da camada III da MPEG.
-   Bitstreams de extensão multi channel MPEG-2.
-   Fluxos de bits do AAC MPEG-4.
-   Fluxos de bits compatíveis com MPEG-2 não compatíveis com versões anteriores (LTD).
-   Geração de pacotes PES (fluxo elementar) em pacotes.
-   Codificação Dolby Digital.

### <a name="codec-properties"></a>Propriedades do Codec

O filtro dá suporte às seguintes propriedades por [**meio de ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):

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
> Uma versão anterior da documentação listava incorretamente algumas propriedades adicionais sem suporte.

 

Para compatibilidade com backward, o filtro dá suporte à seguinte propriedade por meio da interface **IEncoderAPI:**



| Propriedade                 | Descrição                                                                      |
|--------------------------|----------------------------------------------------------------------------------|
| **TAXA DE BITS ENCAPIPARAM \_** | Equivalente a [**AVEncCommonMeanBitRate.**](avenccommonmeanbitrate-property.md) |



 

É recomendável definir propriedades na seguinte ordem:

1.  [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)
2.  [**AVEncMPALayer**](avencmpalayer-property.md)
3.  [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md)
4.  [**AVEncMPACodingMode**](avencmpacodingmode-property.md)

De definir as propriedades restantes em qualquer ordem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Aplicativos de área de trabalho \[ ultimate\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[**Tipos de mídia de demultiplexer MPEG-2**](mpeg-2-demultiplexer-media-types.md)
</dt> </dl>

 

 

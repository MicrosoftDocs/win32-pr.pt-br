---
description: O reamostrador de áudio executa uma ou ambas as ações a seguir em um fluxo de áudio. Altere a taxa de amostragem. Altere o número de canais.
ms.assetid: bee755c4-0585-40fb-aa4d-4e964f5144a3
title: DSP do reamostrador de áudio (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fb173fa4f8d964bec1102c4cfeefa4bf83f1ffe
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105763155"
---
# <a name="audio-resampler-dsp"></a>DSP de reamostragem de áudio

O reamostrador de áudio executa uma ou ambas as ações a seguir em um fluxo de áudio.

-   Altere a taxa de amostragem.
-   Altere o número de canais.

## <a name="clsid"></a>CLSID

\_CRESAMPLERMEDIAOBJECT CLSID

## <a name="interfaces"></a>Interfaces

-   [**IMediaObject**](/previous-versions/ms785953(v=vs.85))
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [**IWMResamplerProps**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresamplerprops)

## <a name="formats"></a>Formatos

PCM ou ponto flutuante de IEEE

O tipo de mídia deve especificar um formato de áudio PCM ou de ponto flutuante não compactado.

-   Para a interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) , inicialize o tipo de mídia conforme descrito em [tipos de mídia de áudio descompactados](uncompressed-audio-media-types.md).
-   Para a interface [**IMediaObject**](/previous-versions/ms785953%28v%3dvs.85%29) , o tipo de mídia deve ser um tipo de **\_ WaveFormatEx de formato** . Para obter mais informações, consulte [**DMO \_ Media \_ Type**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type).

## <a name="properties"></a>Propriedades

-   [MFPKEY \_ WMRESAMP \_ FILTERQUALITY](mfpkey-wmresamp-filterquality.md)
-   [MFPKEY \_ WMRESAMP \_ CHANNELMTX](mfpkey-wmresamp-channelmtx.md)
-   [MFPKEY \_ WMRESAMP \_ LOWPASS \_ largura de banda](mfpkey-wmresamp-lowpass-bandwidth.md)

## <a name="required-attributes"></a>Atributos necessários.

O reamostrador requer que os seguintes atributos sejam definidos nele:

-   [\_máscara de \_ canal de áudio MF MT \_ \_](mf-mt-audio-channel-mask-attribute.md)
-   [áudio do MF \_ MT \_ média de \_ \_ bytes \_ por \_ segundo](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [\_alinhamento de \_ bloco de áudio MF MT \_ \_](mf-mt-audio-block-alignment-attribute.md)

## <a name="custom-channel-mapping"></a>Mapeamento de canal personalizado

O reamostrador de áudio mapeia os canais de áudio de entrada para os canais de áudio de saída, com base nas seguintes informações:

-   O número de canais. Isso é fornecido no atributo [de \_ \_ \_ \_ canais de áudio MF MT](mf-mt-audio-num-channels-attribute.md) do tipo de mídia ou no membro **nChannels** da estrutura [WAVEFORMATEX](mf-mt-audio-prefer-waveformatex-attribute.md) .
-   A máscara de canal, que atribui canais à posição do orador. A máscara de canal é fornecida no \_ \_ \_ \_ atributo de máscara de canal de áudio MF MT do tipo de mídia ou no membro **dwChannelMask** da estrutura [**WAVEFORMATEXTENSIBLE**](/windows/desktop/api/mmreg/ns-mmreg-waveformatextensible) .
-   Uma matriz de pesos de mapeamento.

A matriz contém uma série de pesos, de modo que cada canal de saída é uma média ponderada dos canais de entrada.

Você pode especificar uma matriz personalizada para o mapeamento de canal chamando [**IWMResamplerProps:: SetUserChannelMtx**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmresamplerprops-setuserchannelmtx) ou definindo a propriedade [**MFPKEY \_ WMRESAMP \_ CHANNELMTX**](mfpkey-wmresamp-channelmtx.md) . Se uma matriz personalizada não for fornecida, o reamostrador de áudio usará um conjunto de matrizes padrão.

## <a name="default-channel-mapping"></a>Mapeamento de canal padrão

Se você não especificar uma matriz personalizada, o DSP do reamostrador de áudio usará valores padrão para o mapeamento de canal.

Nas tabelas a seguir, os canais são abreviados:

-   L: esquerda
-   R: à direita
-   C: central
-   LFE: efeitos de frequência baixa
-   BL: voltar à esquerda
-   BR: voltar à direita
-   SL: surround esquerdo
-   SR: surround direito

A tabela a seguir mostra os coeficientes padrão para mapeamento de 6 canais (Mask 0x3F) para 2 canais.



|     | L     | R     | C     | LFE   | BL    | BR    |
|-----|-------|-------|-------|-------|-------|-------|
| L   | 0.314 | 0     | 0,222 | 0, 31 | 0,268 | 0,164 |
| R   | 0     | 0.314 | 0,222 | 0, 31 | 0,164 | 0,268 |



 

A tabela a seguir mostra os coeficientes padrão para mapeamento de 6 canais (Mask 0x60F) para 2 canais.



|     | L     | R     | C     | LFE   | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|
| L   | 0,320 | 0     | 0,226 | 0, 32 | 0,292 | 0,130 |
| R   | 0     | 0,320 | 0,226 | 0, 32 | 0,130 | 0,292 |



 

A tabela a seguir mostra os coeficientes padrão para mapear os canais 6 (Mask 0x3F ou 0x60F) para 1 canal.



|     | L     | R     | C     | LFE   | BL (SL) | BR (SR) |
|-----|-------|-------|-------|-------|--------|--------|
| C   | 0,192 | 0,192 | 0,192 | 0, 38 | 0,192  | 0,192  |



 

A tabela a seguir mostra os coeficientes padrão para mapeamento de 8 canais (Mask 0x63F) para 2 canais.



|     | L     | R     | C     | LFE   | BL    | BR    | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| L   | 0,222 | 0     | 0,157 | 0, 22 | 0,189 | 0,116 | 0,203 | 0, 90 |
| R   | 0     | 0,222 | 0,157 | 0, 22 | 0,116 | 0,189 | 0, 90 | 0,203 |



 

A tabela a seguir mostra os coeficientes padrão para mapeamento de 8 canais (Mask 0x63F) para 1 canal.



|     | L     | R     | C     | LFE   | BL    | BR    | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| C   | 0,139 | 0,139 | 0,139 | 0, 28 | 0,139 | 0,139 | 0,139 | 0,139 |



 

A tabela a seguir mostra os coeficientes padrão para mapeamento de 8 canais (Mask 0x63F) para 6 canais (Mask 0x3F).



|     | L     | R     | C     | LFE   | BL    | BR    | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| L   | 0,518 | 0     | 0     | 0     | 0     | 0     | 0,189 | 0     |
| R   | 0     | 0,518 | 0     | 0     | 0     | 0     | 0     | 0,189 |
| C   | 0     | 0     | 0,518 | 0     | 0     | 0     | 0     | 0     |
| LFE | 0     | 0     | 0     | 0,518 | 0     | 0     | 0     | 0     |
| BL  | 0     | 0     | 0     | 0     | 0,518 | 0     | 0,482 | 0     |
| BR  | 0     | 0     | 0     | 0     | 0     | 0,518 | 0     | 0,482 |



 

A tabela a seguir mostra os coeficientes padrão para mapeamento de 8 canais (Mask 0x63F) para 6 canais (Mask 0x60F).



|     | L     | R     | C     | LFE   | BL    | BR    | SL    | SR    |
|-----|-------|-------|-------|-------|-------|-------|-------|-------|
| L   | 0,447 | 0     | 0     | 0     | 0     | 0     | 0     | 0     |
| R   | 0     | 0,447 | 0     | 0     | 0     | 0     | 0     | 0     |
| C   | 0     | 0     | 0,447 | 0     | 0     | 0     | 0     | 0     |
| LFE | 0     | 0     | 0     | 0,447 | 0     | 0     | 0     | 0     |
| SL  | 0     | 0     | 0     | 0     | 0,429 | 0,124 | 0,447 | 0     |
| SR  | 0     | 0     | 0     | 0     | 0,124 | 0,429 | 0     | 0,447 |



 

Para entender como interpretar as tabelas de coeficientes, considere a primeira tabela, que mapeia 6 canais para 2. A primeira linha da tabela (0,314, 0, 0,222, 0, 31, 0,268, 0,164) é um vetor de pesos que especifica o grau de contribuição de cada canal de entrada para o canal esquerdo da saída. A segunda linha da tabela (0, 0,314, 0,222, 0, 31, 0,164, 0,268) é um vetor de pesos que especifica o grau de contribuição de cada canal de entrada para o canal correto da saída.

As fórmulas a seguir mostram como os canais de saída são calculados.

``` syntax
L_out = L*0.314 + C*0.222 + LFE*0.031 + BL*0.268 + BR*0.164 
R_out = R*0.314 + C*0.222 + LFE*0.031 + BL*0.164 + BR*0.268
```

> [!Note]  
> Se você usar o DSP reamostrador de áudio para aumentar o número de canais, os canais adicionados serão atribuídos aos valores 0.

 

## <a name="output-quality"></a>Qualidade de saída

Você pode especificar a qualidade de saída do DSP do reamostrador de áudio chamando [**IWMResamplerProps:: SetHalfFilterLength**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmresamplerprops-sethalffilterlength) ou definindo a propriedade [**MFPKEY \_ WMRESAMP \_ FILTERQUALITY**](mfpkey-wmresamp-filterquality.md) . Se você não especificar a qualidade de saída, o DSP do reamostrador de áudio usará um valor de qualidade padrão de 30.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Resampledmo.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

[Processadores de sinais digitais](windowsmediadigitalsignalprocessors.md)

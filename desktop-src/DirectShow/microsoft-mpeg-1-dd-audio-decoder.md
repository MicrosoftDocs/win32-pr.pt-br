---
description: 'Esse filtro decodifica os seguintes formatos de áudio:'
ms.assetid: 2fd14296-9eed-4e25-b140-6281c707fdb7
title: Decodificador de áudio do Microsoft MPEG-1/DD/AAC (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dd20bfc2ad8a366b46ac0c0600d8cc7a8bca5abacae621e8ea7d02f5f1cb4d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051246"
---
# <a name="microsoft-mpeg-1ddaac-audio-decoder"></a>Decodificador de áudio do Microsoft MPEG-1/DD/AAC

Esse filtro decodifica os seguintes formatos de áudio:

-   Camadas de áudio MPEG-1 I e II.
-   Áudio MPEG-2 compatível com versões anteriores, camadas I e II (ISO/IEC 13818-3), mono e estéreo somente.
-   Perfil de LC (codificação de áudio avançado) (AAC) de baixa complexidade.
-   High-Efficiency AAC (HE-AAC) versão 1 e versão 2.
-   DTS (Digital Theater Systems) de passagem para saída digital.
-   Somente LPCM, mono e estéreo, com ou sem cabeçalhos do PES.
-   Dolby Digital.
-   Dolby Digital Plus, incluindo conversão de Dolby Digital Plus para Dolby Digital para saída digital.

> [!Note]  
> A implementação da tecnologia Dolby Digital da Microsoft é restrita em termos do programa de licenciamento do Dolby Digital para uso pelos aplicativos da Microsoft.

 

> [!Note]  
> Não há suporte para esse filtro em plataformas baseadas em IA-64.

 

a decodificação dos formatos Dolby Digital Plus, AAC e HE-AAC requer o Windows 7. não há suporte para a decodificação de dolby digital ou dolby digital Plus no Windows 7 Home Basic ou Windows 7 starter.

No registro, o nome amigável desse filtro é "decodificador de áudio do Microsoft DTV-DVD".



Informações de filtro

Filtrar interfaces

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/>

Tipos de mídia de pino de entrada

no Windows Vista e posterior, o filtro oferece suporte aos seguintes tipos de entrada:<br/>

-   **MediaType \_ Áudio**, **MEDIASUBTYPE \_ Dolby \_ AC3** (veja a observação 1).
-   **MediaType \_ Áudio**, **MEDIASUBTYPE \_ MPEG1Audio**
-   **MediaType \_ Áudio**, **MEDIASUBTYPE \_ MPEG1Payload**
-   **MediaType \_ Áudio**, **\_ \_ áudio MEDIASUBTYPE MPEG2**
-   **MediaType \_ DVD \_ ENCRYPTED \_ Pack**, **MEDIASUBTYPE \_ Dolby \_ AC3** (veja a observação 1).
-   **MediaType \_ \_ \_ Pacote de DVD criptografado**, **MEDIASUBTYPE \_ DTS** (consulte a observação 2.)
-   **MediaType \_ DVD \_ ENCRYPTED \_ Pack**, **\_ \_ \_ áudio MEDIASUBTYPE DVD LPCM**
-   **MediaType \_ DVD \_ ENCRYPTED \_ Pack**, **\_ \_ áudio MEDIASUBTYPE MPEG2**
-   **MediaType \_ MPEG2 \_ PES**, **MEDIASUBTYPE \_ Dolby \_ AC3** (consulte a observação 1.)
-   **MediaType \_ MPEG2 \_ PES**, **MEDIASUBTYPE \_ DTS** (consulte a observação 2.)
-   **MediaType \_ MPEG2 \_ PES**, **MEDIASUBTYPE \_ DVD \_ LPCM \_ Audio**
-   **MediaType \_ MPEG2 \_ PES**, **\_ \_ áudio MEDIASUBTYPE MPEG2**
-   **MediaType \_ Stream**, **MEDIASUBTYPE \_ Dolby \_ AC3** (consulte a observação 1.)
-   **MediaType \_ Stream**, **MEDIASUBTYPE \_ MPEG1Audio**
-   **MediaType \_ Fluxo**, **\_ \_ áudio MEDIASUBTYPE MPEG2**

a partir do Windows 7, o filtro também oferece suporte aos seguintes tipos de entrada:<br/>

-   **MediaType \_ Áudio**, **MEDIASUBTYPE \_ Dolby \_ DDPLUS** (veja a observação 1).
-   **MediaType \_ Áudio**, **MEDIASUBTYPE \_ DTS2** (consulte a observação 2.)
-   **MediaType \_ Áudio**, **MEDIASUBTYPE \_ DVD \_ LPCM \_ Audio**
-   **MediaType \_ Áudio**, **MEDIASUBTYPE \_ DVM** (consulte a observação 1).
-   **MediaType \_ Áudio**, **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC**
-   **MediaType \_ Áudio**, **MEDIASUBTYPE \_ MPEG \_ loas**
-   **MediaType \_ Áudio**, **MEDIASUBTYPE \_ MPEG1AudioPayload**
-   **MediaType \_ Áudio**, **MEDIASUBTYPE \_ RAW \_ AAC1**
-   **MediaType \_ Stream**, **MEDIASUBTYPE \_ Dolby \_ DDPLUS** (consulte a observação 1.)
-   **MediaType \_ Stream**, **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC**
-   **MediaType \_ Stream**, **MEDIASUBTYPE \_ MPEG \_ loas**

O tipo de entrada pode ser alterado dinamicamente durante o streaming.<br/> Para obter mais informações sobre esses tipos de mídia, consulte [**subtipos de áudio**](audio-subtypes.md).<br/>

> [!Note]  
> 1. A implementação da tecnologia Dolby Digital da Microsoft é restrita em termos do programa de licenciamento do Dolby Digital para uso pelos aplicativos da Microsoft.

<br/>

> [!Note]  
> 2. Para a entrada de DTS (Digital Theater Systems), somente a saída de S/PDIF é suportada (DTS over S/PDIF). Não há suporte para a decodificação de áudio.

<br/>

Interfaces de pino de entrada

[**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> [**IKsPropertySet**](ikspropertyset.md)<br/> [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Tipos de mídia do pino de saída

no Windows Vista e posterior, o filtro dá suporte aos seguintes tipos de saída:<br/>

-   **MediaType \_ Áudio**, **MEDIASUBTYPE \_ Dolby \_ AC3 \_ SPDIF** (igual ao **KSDATAFORMAT \_ subtipo \_ IEC61937 \_ Dolby \_ digital**)
-   **MediaType \_ Áudio**, **MEDIASUBTYPE \_ PCM**

a partir do Windows 7, o filtro também oferece suporte aos seguintes tipos de saída:<br/>

-   **MediaType \_ Áudio**, **KSDATAFORMAT \_ subtipo \_ IEC61937 \_ DTS**
-   **MediaType \_ Áudio**, **MEDIASUBTYPE \_ IEEE \_ float**

Interfaces de pino de saída

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

CLSID do filtro

**CLSID \_ do CMPEG2AudDecoderDS** (declarado em wmcodecdsp. h)

Executável

msmpeg2adec.dll

[Núcleo](merit.md)

**Mérito \_ NORMAL** -1

[Categoria do filtro](filter-categories.md)

**\_LEGACYAMFILTERCATEGORY CLSID**



 

> [!Note]  
> Uma versão anterior da documentação declarava que esse filtro pode decodificar "áudio MPEG-2". O filtro decodifica apenas áudio MPEG-2 compatível com versões anteriores.

 

## <a name="remarks"></a>Comentários

Os fluxos mono sempre são decodificados para estéreo.

Para fluxos com uma configuração de canal de dois ou mais alto-falantes, o decodificador faz um dos seguintes:

-   Combina até seis canais, usando a configuração de alto-falante 5,1 comum.
-   Downmixes para estéreo.

Para selecionar entre essas duas opções, use a interface [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) para definir a propriedade [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) , antes de conectar os Pins. Como alternativa, quando o aplicativo cria o grafo de filtro, ele pode definir o tipo de mídia desejado no pino de saída.

### <a name="aac-decoding"></a>Decodificação AAC

Para o AAC, o decodificador tem determinadas restrições de formato na entrada AAC compactada. Essas restrições de formato são as mesmas que o [**decodificador AAC**](../medfound/aac-decoder.md)Media Foundation e estão documentadas na seção "[**restrições de formato**](../medfound/aac-decoder.md)".

o decodificador DirectShow também aceita tipos de entrada diferentes do decodificador Media Foundation. o decodificador DirectShow dá suporte aos seguintes tipos de entrada AAC:

-   **MEDIASUBTYPE \_ \_AAC1 bruto**: AAC bruto, normalmente encontrado em AVI ou Matroska (. MKV) arquivos.
-   **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC**: AAC em um fluxo de transporte de dados de áudio (ADTS) para streaming.
-   **MEDIASUBTYPE \_ MPEG \_ loas**: fluxo de transporte com uma camada de sincronização (loas) e uma camada de MULTIPLEX (LATM).

O decodificador Media Foundation dá suporte aos seguintes tipos de entrada AAC:

-   MFAudioFormat \_ AAC (igual a **MEDIASUBTYPE \_ MPEG \_ HEAAC**) para reprodução de arquivo MP4.
-   **MEDIASUBTYPE \_ \_AAC1 brutos**.

### <a name="property-sets"></a>Conjuntos de propriedades

O PIN de entrada do decodificador dá suporte aos seguintes conjuntos de propriedades por meio de [**IKsPropertySet**](ikspropertyset.md):

-   [**Conjunto de propriedades da proteção contra cópia de DVD**](dvd-copy-protection-property-set.md)
-   [**Taxa-alteração de propriedade definida**](rate-change-property-set.md).

> [!Note]  
> a partir do Windows 7, o decodificador dá suporte ao modo de truque por meio do conjunto de propriedades de alteração de taxa. Ele dá suporte a taxas de reprodução no intervalo de \[ 0,501 a 2,0 \] , em que 1,0 é taxa de reprodução normal e 2,0 é o dobro da taxa normal.

 

### <a name="codec-properties"></a>Propriedades do codec

O PIN de entrada do decodificador dá suporte às seguintes propriedades por meio de [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):



| Propriedade                                                          | Exige                                                 |
|-------------------------------------------------------------------|----------------------------------------------------------|
| [**AVAudioChannelConfig**](avaudiochannelconfig-property.md)     | Windows Vista                                            |
| [**AVAudioChannelCount**](avaudiochannelcount-property.md)       | Windows Vista                                            |
| [**AVAudioSampleRate**](avaudiosamplerate-property.md)           | Windows Vista                                            |
| [**AVDDSurroundMode**](avddsurroundmode-property.md)             | Windows Somente vista; sem suporte no Windows 7 ou posterior. |
| [**AVDecAudioDualMono**](avdecaudiodualmono-property.md)         | Windows Vista                                            |
| [**AVDecCommonInputFormat**](avdeccommoninputformat-property.md) | Windows Vista                                            |
| [**AVDecCommonMeanBitRate**](avdeccommonmeanbitrate.md)          | Windows 7                                                |



 

O filtro oferece suporte às seguintes propriedades por meio de [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):



| Propriedade                                                                          | Exige      |
|-----------------------------------------------------------------------------------|---------------|
| [**AVDecAACDownmixMode**](avdecaacdownmixmode-property.md)                       | Windows 7     |
| [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md)       | Windows Vista |
| [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) (veja a observação 3.) | Windows Vista |
| [**AVDecDDDynamicRangeScaleHigh**](avdecdddynamicrangescalehigh-property.md)     | Windows Vista |
| [**AVDecDDDynamicRangeScaleLow**](avdecdddynamicrangescalelow-property.md)       | Windows Vista |
| [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md)                 | Windows Vista |
| [**AVDecMmcssClass**](avdecmmcss-property.md)                                    | Windows Vista |
| [**AVDSPLoudnessEqualization**](avdsploudnessequalization-property.md)           | Windows 7     |
| [**AVDSPSpeakerFill**](avdspspeakerfill-property.md)                             | Windows 7     |



 

> [!Note]  
> 3. A propriedade [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) deve ser definida antes do pino de saída do decodificador ser conectado. Caso contrário, a alteração não terá efeito.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows vista Home Premium, Windows vista Ultimate, \[ somente aplicativos de área de trabalho do Windows 7\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl>        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Subtipos de áudio**](audio-subtypes.md)
</dt> <dt>

[DirectShow Filter](directshow-filters.md)
</dt> <dt>

[**Tipos de mídia de DVD**](dvd-media-types.md)
</dt> </dl>

 

 

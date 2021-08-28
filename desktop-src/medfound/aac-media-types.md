---
description: Este tópico descreve como especificar o formato de um fluxo AAC (codificação de áudio avançado) no Media Foundation.
ms.assetid: 82218bc5-6660-4253-b50c-b6d9f30be3d5
title: Tipos de mídia AAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae70661478ad0d2267c951c80fc4a63d98c15267
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479882"
---
# <a name="aac-media-types"></a>Tipos de mídia AAC

Este tópico descreve como especificar o formato de um fluxo AAC (codificação de áudio avançado) no Media Foundation.

Dois subtipos são definidos para áudio AAC:



| Subtype                     | Descrição          | Cabeçalho       |
|-----------------------------|----------------------|--------------|
| **\_AAC MFAudioFormat**      | AAC bruto ou ADTS. | mfapi. h      |
| **\_AAC1 bruto \_ MEDIASUBTYPE** | AAC bruto.             | wmcodecdsp. h |



 

<dl> <dt>

<span id="MFAudioFormat_AAC"></span><span id="mfaudioformat_aac"></span><span id="MFAUDIOFORMAT_AAC"></span>\_AAC MFAudioFormat
</dt> <dd>

Para esse subtipo, o tipo de mídia fornece a taxa de amostra e o número de canais antes da aplicação de ferramentas de Spectral Band Replication (SBR) e de estéreo paramétrica (PS), se presente. O efeito da ferramenta SBR é dobrar a taxa de amostragem decodificada em relação à taxa de amostra AAC-LC principal. O efeito da ferramenta PS é decodificar o estéreo de um fluxo básico AAC-LC do canal mono.

Esse subtipo é equivalente a **MEDIASUBTYPE \_ MPEG \_ HEAAC**, definido em wmcodecdsp. h. Consulte [GUIDs de subtipo de áudio](audio-subtype-guids.md).

</dd> <dt>

<span id="MEDIASUBTYPE_RAW_AAC1"></span><span id="mediasubtype_raw_aac1"></span>\_AAC1 bruto \_ MEDIASUBTYPE
</dt> <dd>

Esse subtipo é usado para AAC contido em um arquivo AVI com a marca de formato de áudio igual ao \_ formato Wave \_ \_ AAC1 RAW (0x00FF).

Para esse subtipo, o tipo de mídia fornece a taxa de amostra e o número de canais depois que as ferramentas SBR e PS são aplicadas, se presentes.

</dd> </dl>

Os seguintes atributos de tipo de mídia se aplicam ao áudio AAC.




| Atributo | Descrição | 
|-----------|-------------|
| <a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a> | Tipo principal. Deve ser <strong>MFMediaType_Audio</strong>. | 
| <a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a> | Subtipo de áudio. Consulte a descrição anterior para obter detalhes. | 
| <a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a> | Perfil de áudio e nível. <br /> O valor desse atributo é o campo <strong>audioProfileLevelIndication</strong> , conforme definido por ISO/IEC 14496-3.<br /> Se for desconhecido, defina como zero ou 0xFE ("nenhum perfil de áudio especificado").<br /> | 
| <a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a> | Taxa de bits do fluxo AAC codificado, em bytes por segundo. | 
| <a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> | Tipo de carga.<br /> Aplica-se somente a <strong>MFAudioFormat_AAC</strong>.<br /><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> é opcional. Se esse atributo não for especificado, o valor padrão 0 será usado, o que especificará que o fluxo contém apenas elementos de raw_data_block.<br /> | 
| <a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a> | Profundidade de bits do áudio PCM decodificado. | 
| <a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a> | Atribuição de canais de áudio a posições do orador. | 
| <a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a> | Número de canais, incluindo o canal de baixa frequência (LFE), se presente.<br /> A interpretação desse valor depende do subtipo de mídia, conforme descrito anteriormente.<br /> | 
| <a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a> | Taxa de amostragem, em amostras por segundo.<br /> A interpretação desse valor depende do subtipo de mídia, conforme descrito anteriormente.<br /> | 
| <a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a> | O valor desse atributo depende do subtipo:<br /><ul><li><strong>MFAudioFormat_AAC</strong>: contém a parte da estrutura <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> que aparece após a estrutura <strong>WAVEFORMATEX</strong> (ou seja, após o membro <strong>WFX</strong> ). Isso é seguido pelos dados de AudioSpecificConfig (), conforme definido por ISO/IEC 14496-3.</li><li><strong>MEDIASUBTYPE_RAW_AAC1</strong>: contém os dados de AudioSpecificConfig ().</li></ul> | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de mídia de áudio](audio-media-types.md)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> <dt>

[Suporte a MPEG-4 no Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> </dl>

 


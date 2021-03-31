---
description: O decodificador de áudio MPEG da Microsoft é uma Media Foundation de transformação síncrona que permite decodificar formatos de fluxo elementares de áudio MPEG usando o pipeline de Media Foundation (MF).
ms.assetid: 29A0491D-CA0D-4909-96F0-5640D5EE77F9
title: Decodificador de áudio MPEG
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a98106ce4610c7c89a5e6212c225fd8eca3e4526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921216"
---
# <a name="mpeg-audio-decoder"></a>Decodificador de áudio MPEG

O decodificador de áudio MPEG da Microsoft é uma [Media Foundation de transformação](media-foundation-transforms.md) síncrona que permite decodificar formatos de fluxo elementares de áudio MPEG usando o pipeline de Media Foundation (MF).

O decodificador dá suporte aos seguintes formatos de fluxo de do MPEG elementar.

-   Camadas de áudio MPEG-1 I e II (ISO/IEC 11172-3). 2. MPEG-2 retroativa-Compatible, camadas I e II (ISO

-   MPEG-2 retroativa-Compatible, camadas I e II (ISO/IEC 13818-3), mono e estéreo somente

## <a name="class-identifier"></a>Identificador de classe

O CLSID (identificador de classe) do decodificador de áudio MPEG é **CLSID \_ MSMPEGAudDecMFT**, definido no arquivo de cabeçalho wmcodecdsp. h.

## <a name="input-media-types"></a>Tipos de mídia de entrada

O decodificador de áudio MPEG dá suporte aos seguintes atributos de tipo de mídia de entrada.



| Atributo                                                                               | Valor                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ tipo principal MF \_ MT**](mf-mt-major-type-attribute.md)                               | **\_Áudio MFMediaType**                                                                                                                                                                                                                                                |
| [**subtipo MF \_ MT \_**](mf-mt-subtype-attribute.md)                                      | **MFAudioFormat \_ MPEG**                                                                                                                                                                                                                                               |
| [**\_canais de \_ número de áudio MF MT \_ \_**](mf-mt-audio-num-channels-attribute.md)              | Adicional Geralmente 1 para mono ou 2 para estéreo, mas pode ter até 6 canais.<br/>                                                                                                                                                                                |
| [**\_máscara de \_ canal de áudio MF MT \_ \_**](mf-mt-audio-channel-mask-attribute.md)              | Adicional Normalmente 0x4 para mono ou 0x3 para estéreo, mas também pode ser qualquer uma das máscaras de canal associadas a até 6 canais (3/2/1, 3/2, 3/1, 2/2, 2/1). Se presente, a máscara de canal deve ser consistente com o número de entrada especificado de canais.<br/> |
| [**\_amostras de áudio MF MT \_ \_ \_ por \_ segundo**](mf-mt-audio-samples-per-second-attribute.md) | Adicional Um dos seguintes: 16000, 22050, 24000, 32000, 44100, 48000. Se especificado, a taxa de amostragem de entrada deve ser uma das taxas de amostragem de MPEG válidas.<br/>                                                                                             |



 

## <a name="output-media-types"></a>Tipos de mídia de saída

O decodificador de áudio MPEG dará suporte a até quatro subtipos de mídia de saída, na seguinte ordem.

<dl> 1. Estéreo, ponto flutuante.  
2. Estéreo de 16 bits.  
3. Mono, ponto flutuante (somente se a entrada for mono ou dual-mono).  
4. Mono, PCM de 16 bits (somente se a entrada for mono ou dual-mono).  
</dl>

O decodificador sempre dá suporte à saída de estéreo e é enumerado como o primeiro tipo de mídia de saída.

O decodificador dá suporte aos seguintes atributos de tipo de mídia de saída.



| Atributo                                                                           | Valor                                                                      |
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [\_ \_ tipo principal MF \_ MT](mf-mt-major-type-attribute.md)                               | **\_Áudio MFMediaType**                                                     |
| [subtipo MF \_ MT \_](mf-mt-subtype-attribute.md)                                      | **MFAudioFormat \_ PCM** ou **MFAudioFormat \_ float**                  |
| [\_bits de áudio MF MT \_ \_ \_ por \_ amostra](mf-mt-audio-bits-per-sample-attribute.md)       | 16 ou 32                                                                   |
| [\_canais de \_ número de áudio MF MT \_ \_](mf-mt-audio-num-channels-attribute.md)              | 1 ou 2                                                                     |
| [\_máscara de \_ canal de áudio MF MT \_ \_](mf-mt-audio-channel-mask-attribute.md)              | 0x4 para mono ou 0x3 para estéreo                                             |
| [\_amostras de áudio MF MT \_ \_ \_ por \_ segundo](mf-mt-audio-samples-per-second-attribute.md) | Um dos seguintes: 16000, 22050, 24000, 32000, 44100, 48000.<br/> |



 

## <a name="transform-attributes"></a>Atributos de transformação

O decodificador de áudio MPEG implementa o método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) . Os aplicativos podem usar esse método para obter ou definir os atributos a seguir.



| Atributo                                                                               | Descrição                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CODECAPI \_ AVDecAudioDualMono**](../directshow/avdecaudiodualmono-property.md)                   | Especifica se o áudio de 2 canais que está sendo decodificado é dual mono ou não. Somente leitura. Definido pelo MFT. Para obter mais informações, consulte [**eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).                                                                                                                               |
| [**CODECAPI \_ AVDecAudioDualMonoReproMode**](../directshow/avdecaudiodualmonorepromode-property.md) | Especifica como o decodificador Reproduz áudio mono duplo. O valor padrão é **eAVDecAudioDualMonoReproMode \_ esquerdo \_ mono**.<br/> Leitura/gravação. Os aplicativos podem definir essa propriedade para alterar o comportamento padrão. Para obter mais informações, consulte [**eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).<br/> |
| [**CODECAPI \_ AVEncCommonMeanBitRate**](../directshow/avenccommonmeanbitrate-property.md)           | Especifica a taxa de bits do fluxo compactado. Somente leitura. Definido pelo MFT.                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de codec](codecobjects.md)
</dt> </dl>

 

 

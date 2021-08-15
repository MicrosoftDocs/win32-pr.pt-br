---
description: Definindo um tipo de saída para um codificador WMA
ms.assetid: 0a1a22bb-460f-4ac2-be76-4249997441de
title: Definindo um tipo de saída para um codificador WMA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48f2731a081138bda30ab3e81f01d353e0348f4d3586fd4c02878b62a7f04393
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880567"
---
# <a name="setting-an-output-type-for-a-wma-encoder"></a>Definindo um tipo de saída para um codificador WMA

Para criar um tipo de saída válido para um codificador WMA (Windows Media Audio), você deve ter as seguintes informações:

-   O subtipo de áudio que repessa o formato WMA codificado. Consulte [GUIDs de subtipo de áudio.](audio-subtype-guids.md)
-   As propriedades de configuração a definir no codificador.

    As propriedades de configuração estão documentadas na documentação Windows Codec de Áudio e Vídeo de Mídia e APIs do DSP. Para obter mais informações, consulte "Propriedades de fluxo de áudio" [em Propriedades de codificação](configuring-the-encoder.md).

### <a name="windows-vista-or-later"></a>Windows Vista ou Posterior

Para obter um tipo de saída válido para o codificador, execute as etapas a seguir.

1.  Use a [**função MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) ou [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) para criar uma instância do codificador.
2.  Consulte o codificador para a interface **IPropertyStore.**
3.  Use a interface **IPropertyStore** para configurar o codificador.
4.  Recupere os tipos de saída com suporte chamando [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) em um loop até que o codificador retorne **MF \_ E NO MORE \_ \_ \_ TYPES** e você escolha o tipo de mídia de destino. I
5.  Chame [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) para definir o tipo de mídia de compactação no codificador.

### <a name="windows-7"></a>Windows 7

Para obter um tipo de saída válido para o codificador no Windows 7, Media Foundation fornece a função [**MFTranscodeGetAudioOutputAvailableTypes.**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) Um aplicativo deve passar o subtipo de áudio necessário que repessa o WMA codificado e as propriedades de codificação. As propriedades são necessárias porque o codificador altera os tipos de saída com suporte, dependendo do conjunto de modos.

> [!Note]  
> [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes)só tem suporte para codificação de taxa [de bits constante.](constant-bit-rate-encoding.md)

 

Se a chamada for bem-sucedida, o aplicativo receberá uma lista de ponteiros IUnknown dos tipos de mídia de saída com suporte em [**um objeto IMFCollection.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) Para definir o tipo de mídia de saída, encontre aquele que corresponde ao tipo de destino e chame [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) para definir o tipo de mídia de compactação no codificador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Inciando um MFT codificador](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Codificadores de mídia](windows-media-encoders.md)
</dt> </dl>

 

 




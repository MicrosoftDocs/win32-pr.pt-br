---
description: Configurando um tipo de saída para um codificador WMA
ms.assetid: 0a1a22bb-460f-4ac2-be76-4249997441de
title: Configurando um tipo de saída para um codificador WMA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c6b078dc2426b062a90f706c5d113960f54ce32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089777"
---
# <a name="setting-an-output-type-for-a-wma-encoder"></a>Configurando um tipo de saída para um codificador WMA

Para criar um tipo de saída válido para um codificador de áudio do Windows Media (WMA), você deve ter as seguintes informações:

-   O subtipo de áudio que repesents o formato WMA codificado. Consulte [GUIDs de subtipo de áudio](audio-subtype-guids.md).
-   As propriedades de configuração a serem definidas no codificador.

    As propriedades de configuração estão documentadas na documentação do codec de áudio e vídeo do Windows Media e das APIs do DSP. Para obter mais informações, consulte "Propriedades do fluxo de áudio" em [Propriedades de codificação](configuring-the-encoder.md).

### <a name="windows-vista-or-later"></a>Windows Vista ou posterior

Para obter um tipo de saída válido para o codificador, execute as etapas a seguir.

1.  Use a função [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) ou [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) para criar uma instância do codificador.
2.  Consulte o codificador para a interface **IPropertyStore** .
3.  Use a interface **IPropertyStore** para configurar o codificador.
4.  Recupere os tipos de saída com suporte chamando [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) em um loop até que o codificador retorne o **MF \_ e \_ não \_ mais \_ tipos** e você escolha o tipo de mídia de destino. I
5.  Chame [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) para definir o tipo de mídia de compactação no codificador.

### <a name="windows-7"></a>Windows 7

Para obter um tipo de saída válido para o codificador no Windows 7, Media Foundation fornece a função [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) . Um aplicativo deve passar pelo subtipo de áudio necessário que repesents as propriedades de codificação e WMA codificadas. As propriedades são necessárias porque o codificador altera os tipos de saída com suporte, dependendo do conjunto de modos.

> [!Note]  
> Só há suporte para [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes)para [codificação de taxa de bits constante](constant-bit-rate-encoding.md).

 

Se a chamada for realizada com sucesso, o aplicativo receberá uma lista de ponteiros IUnknown dos tipos de mídia de saída com suporte em um objeto [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) . Para definir o tipo de mídia de saída, localize aquele que corresponde ao tipo de destino e chame [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) para definir o tipo de mídia de compactação no codificador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando uma instância de um MFT do codificador](instantiating-the-encoder-mft.md)
</dt> <dt>

[Codificadores de mídia do Windows](windows-media-encoders.md)
</dt> </dl>

 

 




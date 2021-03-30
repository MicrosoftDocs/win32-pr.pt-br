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
# <a name="setting-an-output-type-for-a-wma-encoder"></a><span data-ttu-id="af3df-103">Configurando um tipo de saída para um codificador WMA</span><span class="sxs-lookup"><span data-stu-id="af3df-103">Setting an Output Type for a WMA Encoder</span></span>

<span data-ttu-id="af3df-104">Para criar um tipo de saída válido para um codificador de áudio do Windows Media (WMA), você deve ter as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="af3df-104">To create a valid output type for a Windows Media Audio (WMA) encoder, you must have the following information:</span></span>

-   <span data-ttu-id="af3df-105">O subtipo de áudio que repesents o formato WMA codificado.</span><span class="sxs-lookup"><span data-stu-id="af3df-105">The audio subtype that repesents the encoded WMA format.</span></span> <span data-ttu-id="af3df-106">Consulte [GUIDs de subtipo de áudio](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="af3df-106">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span>
-   <span data-ttu-id="af3df-107">As propriedades de configuração a serem definidas no codificador.</span><span class="sxs-lookup"><span data-stu-id="af3df-107">The configuration properties to set on the encoder.</span></span>

    <span data-ttu-id="af3df-108">As propriedades de configuração estão documentadas na documentação do codec de áudio e vídeo do Windows Media e das APIs do DSP.</span><span class="sxs-lookup"><span data-stu-id="af3df-108">The configuration properties are documented in the Windows Media Audio and Video Codec and DSP APIs documentation.</span></span> <span data-ttu-id="af3df-109">Para obter mais informações, consulte "Propriedades do fluxo de áudio" em [Propriedades de codificação](configuring-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="af3df-109">For more information, see "Audio Stream Properties" in [Encoding Properties](configuring-the-encoder.md).</span></span>

### <a name="windows-vista-or-later"></a><span data-ttu-id="af3df-110">Windows Vista ou posterior</span><span class="sxs-lookup"><span data-stu-id="af3df-110">Windows Vista or Later</span></span>

<span data-ttu-id="af3df-111">Para obter um tipo de saída válido para o codificador, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="af3df-111">To get a valid output type for the encoder, perform the following steps.</span></span>

1.  <span data-ttu-id="af3df-112">Use a função [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) ou [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) para criar uma instância do codificador.</span><span class="sxs-lookup"><span data-stu-id="af3df-112">Use the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) or [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function to create an instance of the encoder.</span></span>
2.  <span data-ttu-id="af3df-113">Consulte o codificador para a interface **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="af3df-113">Query the encoder for the **IPropertyStore** interface.</span></span>
3.  <span data-ttu-id="af3df-114">Use a interface **IPropertyStore** para configurar o codificador.</span><span class="sxs-lookup"><span data-stu-id="af3df-114">Use the **IPropertyStore** interface to configure the encoder.</span></span>
4.  <span data-ttu-id="af3df-115">Recupere os tipos de saída com suporte chamando [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) em um loop até que o codificador retorne o **MF \_ e \_ não \_ mais \_ tipos** e você escolha o tipo de mídia de destino.</span><span class="sxs-lookup"><span data-stu-id="af3df-115">Retrieve the supported output types by calling [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) in a loop until the encoder returns **MF\_E\_NO\_MORE\_TYPES** and you choose the target media type.</span></span> <span data-ttu-id="af3df-116">I</span><span class="sxs-lookup"><span data-stu-id="af3df-116">I</span></span>
5.  <span data-ttu-id="af3df-117">Chame [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) para definir o tipo de mídia de compactação no codificador.</span><span class="sxs-lookup"><span data-stu-id="af3df-117">Call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) to set the compression media type on the encoder.</span></span>

### <a name="windows-7"></a><span data-ttu-id="af3df-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="af3df-118">Windows 7</span></span>

<span data-ttu-id="af3df-119">Para obter um tipo de saída válido para o codificador no Windows 7, Media Foundation fornece a função [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) .</span><span class="sxs-lookup"><span data-stu-id="af3df-119">To get a valid output type for the encoder in Windows 7, Media Foundation provides the [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) function.</span></span> <span data-ttu-id="af3df-120">Um aplicativo deve passar pelo subtipo de áudio necessário que repesents as propriedades de codificação e WMA codificadas.</span><span class="sxs-lookup"><span data-stu-id="af3df-120">An application must pass required the audio subtype that repesents the encoded WMA and the encoding properties.</span></span> <span data-ttu-id="af3df-121">As propriedades são necessárias porque o codificador altera os tipos de saída com suporte, dependendo do conjunto de modos.</span><span class="sxs-lookup"><span data-stu-id="af3df-121">The properties are required because the encoder changes the supported output types depending upon the mode set.</span></span>

> [!Note]  
> <span data-ttu-id="af3df-122">Só há suporte para [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes)para [codificação de taxa de bits constante](constant-bit-rate-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="af3df-122">[**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes)is only supported for [Constant Bit Rate Encoding](constant-bit-rate-encoding.md).</span></span>

 

<span data-ttu-id="af3df-123">Se a chamada for realizada com sucesso, o aplicativo receberá uma lista de ponteiros IUnknown dos tipos de mídia de saída com suporte em um objeto [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) .</span><span class="sxs-lookup"><span data-stu-id="af3df-123">If the call succeeds, the application receives a list of IUnknown pointers of the supported output media types in an [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) object.</span></span> <span data-ttu-id="af3df-124">Para definir o tipo de mídia de saída, localize aquele que corresponde ao tipo de destino e chame [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) para definir o tipo de mídia de compactação no codificador.</span><span class="sxs-lookup"><span data-stu-id="af3df-124">To set the output media type, find the one that matches your target type and call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) to set the compression media type on the encoder.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af3df-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="af3df-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af3df-126">Criando uma instância de um MFT do codificador</span><span class="sxs-lookup"><span data-stu-id="af3df-126">Instantiating an Encoder MFT</span></span>](instantiating-the-encoder-mft.md)
</dt> <dt>

[<span data-ttu-id="af3df-127">Codificadores de mídia do Windows</span><span class="sxs-lookup"><span data-stu-id="af3df-127">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 




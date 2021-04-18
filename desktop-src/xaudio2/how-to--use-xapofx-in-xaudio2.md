---
description: Este tópico mostra como usar um dos efeitos incluídos no XAPOFX em uma cadeia de efeitos de XAudio2.
ms.assetid: dc325584-13f7-231a-e0c7-17f38d54ae11
title: 'Como: Usar um XAPOFX no XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b0bb4cbeabb38f408d9102a2534634e8eed7cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810754"
---
# <a name="how-to-use-xapofx-in-xaudio2"></a><span data-ttu-id="4c642-103">Como: Usar um XAPOFX no XAudio2</span><span class="sxs-lookup"><span data-stu-id="4c642-103">How to: Use XAPOFX in XAudio2</span></span>

<span data-ttu-id="4c642-104">Este tópico mostra como usar um dos efeitos incluídos no XAPOFX em uma cadeia de efeitos de XAudio2.</span><span class="sxs-lookup"><span data-stu-id="4c642-104">This topic shows you how to use one of the effects included in XAPOFX in an XAudio2 effect chain.</span></span>

## <a name="to-use-an-effect-from-xapofx-in-an-xaudio2-effect-chain"></a><span data-ttu-id="4c642-105">Para usar um efeito de XAPOFX em uma cadeia de efeito de XAudio2</span><span class="sxs-lookup"><span data-stu-id="4c642-105">To use an effect from XAPOFX in an XAudio2 effect chain</span></span>

1.  <span data-ttu-id="4c642-106">Crie o efeito passando o CLSID de um efeito de XAPOFX para a função [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) .</span><span class="sxs-lookup"><span data-stu-id="4c642-106">Create the effect by passing the CLSID of an XAPOFX effect to the [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) function.</span></span>

    <span data-ttu-id="4c642-107">Nesse caso, o efeito de reverbose simplificado FXReverb está sendo criado.</span><span class="sxs-lookup"><span data-stu-id="4c642-107">In this case, the simplified reverb effect FXReverb is being created.</span></span>

    ```
    IUnknown * pXAPO;
    CreateFX(__uuidof(FXReverb),&pXAPO);
    ```

    

2.  <span data-ttu-id="4c642-108">Popular uma estrutura de [**\_ \_ descritor de efeito XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) com dados.</span><span class="sxs-lookup"><span data-stu-id="4c642-108">Populate an [**XAUDIO2\_EFFECT\_DESCRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) structure with data.</span></span>

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

3.  <span data-ttu-id="4c642-109">Preencha uma estrutura de [**\_ \_ cadeia de efeito de XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) com dados.</span><span class="sxs-lookup"><span data-stu-id="4c642-109">Populate an [**XAUDIO2\_EFFECT\_CHAIN**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) structure with data.</span></span>

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

4.  <span data-ttu-id="4c642-110">Aplique a cadeia de efeito a uma voz XAudio2 com a função [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) .</span><span class="sxs-lookup"><span data-stu-id="4c642-110">Apply the effect chain to an XAudio2 voice with the [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) function.</span></span>

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

    > [!Note]  
    > <span data-ttu-id="4c642-111">Você também pode aplicar uma cadeia de efeito a uma voz ao criar a voz passando a cadeia como um parâmetro para [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2:: CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice)ou [**IXAudio2:: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).</span><span class="sxs-lookup"><span data-stu-id="4c642-111">You can also apply an effect chain to a voice when you create the voice by passing the chain as a parameter to [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2::CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice), or [**IXAudio2::CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).</span></span>

     

5.  <span data-ttu-id="4c642-112">Libere o efeito com IUnknown:: Release.</span><span class="sxs-lookup"><span data-stu-id="4c642-112">Release the effect with IUnknown::Release.</span></span> <span data-ttu-id="4c642-113">Quando você cria um XAPO, ele terá uma contagem de referência de 1.</span><span class="sxs-lookup"><span data-stu-id="4c642-113">When you create an XAPO, it will have a reference count of 1.</span></span> <span data-ttu-id="4c642-114">Quando XAPO é passado para XAudio2 com [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 incrementa a contagem de referência no XAPO.</span><span class="sxs-lookup"><span data-stu-id="4c642-114">When the XAPO is passed to XAudio2 with [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 increments the reference count on the XAPO.</span></span> <span data-ttu-id="4c642-115">Liberar a referência do cliente para o XAPO permite que o XAudio2 assuma a propriedade do XAPO.</span><span class="sxs-lookup"><span data-stu-id="4c642-115">Releasing the client's reference to the XAPO allows XAudio2 to take ownership of the XAPO.</span></span> <span data-ttu-id="4c642-116">Se XAudio2 tiver a única referência para o XAPO, essa referência será descartada quando não estiver mais sendo usada pelo XAudio2.</span><span class="sxs-lookup"><span data-stu-id="4c642-116">If XAudio2 has the only reference to the XAPO, this reference is disposed of when it is no longer being used by XAudio2.</span></span> <span data-ttu-id="4c642-117">Se o código do cliente precisar manter uma referência para o XAPO — por exemplo, para reutilização posterior — você poderá ignorar esta etapa.</span><span class="sxs-lookup"><span data-stu-id="4c642-117">If the client code needs to maintain a reference to the XAPO—for example, for reuse later—you can skip this step.</span></span>

    ```
    pXAPO->Release();
    ```

    

6.  <span data-ttu-id="4c642-118">Preencha a estrutura do parâmetro, se houver, associada ao efeito.</span><span class="sxs-lookup"><span data-stu-id="4c642-118">Populate the parameter structure, if any, associated with the effect.</span></span>

    <span data-ttu-id="4c642-119">Nesse caso, a estrutura [**de \_ parâmetros FXREVERB**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters) é usada para definir o tamanho de difusão e sala que o efeito de reverberação deve usar.</span><span class="sxs-lookup"><span data-stu-id="4c642-119">In this case, the [**FXREVERB\_PARAMETERS**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters) structure is used to set the diffusion and room size that the reverb effect should use.</span></span>

    ```
    FXREVERB_PARAMETERS XAPOParameters;
    XAPOParameters.Diffusion = FXREVERB_DEFAULT_DIFFUSION;
    XAPOParameters.RoomSize = FXREVERB_DEFAULT_ROOMSIZE;
    ```

    

7.  <span data-ttu-id="4c642-120">Passe a estrutura do parâmetro de efeito para o efeito chamando a função [**Seteffectparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) na voz à qual o efeito está anexado.</span><span class="sxs-lookup"><span data-stu-id="4c642-120">Pass the effect parameter structure to the effect by calling the [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) function on the voice to which the effect is attached.</span></span>

    ```
    hr = pVoice->SetEffectParameters( 0, &XAPOParameters, sizeof( FXREVERB_PARAMETERS ) );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="4c642-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4c642-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c642-122">Efeitos de áudio</span><span class="sxs-lookup"><span data-stu-id="4c642-122">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="4c642-123">Guia de Programação em XAudio2</span><span class="sxs-lookup"><span data-stu-id="4c642-123">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 

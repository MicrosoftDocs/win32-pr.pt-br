---
description: Este tópico mostra como você pode aplicar uma cadeia de efeito a uma voz para permitir o processamento personalizado dos dados de áudio para essa voz. Este tópico descreve como usar o efeito de reverberação, que é um dos efeitos XAudio2 internos.
ms.assetid: 4c33bd83-2654-cd6f-ea6c-bbc0d5872638
title: 'Como: Criar uma cadeia de efeitos'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85d58186b623dca04da99001a29e54cf3ecc39fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090681"
---
# <a name="how-to-create-an-effect-chain"></a><span data-ttu-id="a63be-104">Como: Criar uma cadeia de efeitos</span><span class="sxs-lookup"><span data-stu-id="a63be-104">How to: Create an Effect Chain</span></span>

<span data-ttu-id="a63be-105">Este tópico mostra como você pode aplicar uma cadeia de efeito a uma voz para permitir o processamento personalizado dos dados de áudio para essa voz.</span><span class="sxs-lookup"><span data-stu-id="a63be-105">This topic shows you how you can apply an effect chain to a voice to allow custom processing of the audio data for that voice.</span></span> <span data-ttu-id="a63be-106">Este tópico descreve como usar o efeito de reverberação, que é um dos efeitos XAudio2 internos.</span><span class="sxs-lookup"><span data-stu-id="a63be-106">This topic describes how to use the reverb effect, which is one of the built-in XAudio2 effects.</span></span>

## <a name="to-create-a-basic-effect-chain-that-applies-an-effect-to-a-voice"></a><span data-ttu-id="a63be-107">Para criar uma cadeia de efeito básica que aplica um efeito a uma voz</span><span class="sxs-lookup"><span data-stu-id="a63be-107">To create a basic effect chain that applies an effect to a voice</span></span>

1.  <span data-ttu-id="a63be-108">Crie o efeito.</span><span class="sxs-lookup"><span data-stu-id="a63be-108">Create the effect.</span></span>

    <span data-ttu-id="a63be-109">Neste exemplo, a função [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) cria um efeito de reverberação.</span><span class="sxs-lookup"><span data-stu-id="a63be-109">In this example, the [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) function creates a reverb effect.</span></span> <span data-ttu-id="a63be-110">Consulte [XAudio2 Audio Effects](xaudio2-audio-effects.md) para obter uma lista de possíveis fontes de efeitos para uso com o XAudio2.</span><span class="sxs-lookup"><span data-stu-id="a63be-110">See [XAudio2 Audio Effects](xaudio2-audio-effects.md) for a list of possible sources of effects for use with XAudio2.</span></span>

    ```
    IUnknown * pXAPO;
    hr = XAudio2CreateReverb(&pXAPO);
    ```

    

2.  <span data-ttu-id="a63be-111">Popular uma estrutura de [**\_ \_ descritor de efeito XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) com dados.</span><span class="sxs-lookup"><span data-stu-id="a63be-111">Populate an [**XAUDIO2\_EFFECT\_DESCRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) structure with data.</span></span>

    <span data-ttu-id="a63be-112">Se houver vários efeitos na cadeia, cada efeito precisará de uma estrutura [**de \_ \_ descritor de efeito XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="a63be-112">If there are multiple effects in the chain, each effect will need a [**XAUDIO2\_EFFECT\_DESCRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) structure.</span></span>

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

3.  <span data-ttu-id="a63be-113">Preencha uma estrutura de [**\_ \_ cadeia de efeito de XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) com dados.</span><span class="sxs-lookup"><span data-stu-id="a63be-113">Populate an [**XAUDIO2\_EFFECT\_CHAIN**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) structure with data.</span></span> <span data-ttu-id="a63be-114">Nesse caso, a cadeia tem apenas um efeito.</span><span class="sxs-lookup"><span data-stu-id="a63be-114">In this case, the chain only has one effect.</span></span> <span data-ttu-id="a63be-115">Se a cadeia tiver mais de um efeito, o membro EffectCount conterá a contagem de efeitos e o membro pEffectDescriptors apontará para uma matriz de estruturas de \_ descritor de efeito XAudio2 \_ .</span><span class="sxs-lookup"><span data-stu-id="a63be-115">If the chain has more than one effect, the EffectCount member will contain the count of effects, and the pEffectDescriptors member will point to an array of XAUDIO2\_EFFECT\_DESCRIPTOR structures.</span></span>

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

4.  <span data-ttu-id="a63be-116">Aplique a cadeia de efeito a uma voz com a função [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) .</span><span class="sxs-lookup"><span data-stu-id="a63be-116">Apply the effect chain to a voice with the [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) function.</span></span>

    <span data-ttu-id="a63be-117">Você pode aplicar cadeias de efeito a vozes mestre, vozes de origem e vozes submix.</span><span class="sxs-lookup"><span data-stu-id="a63be-117">You can apply effect chains to master voices, source voices, and submix voices.</span></span>

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

5.  <span data-ttu-id="a63be-118">Libere o efeito com IUnknown:: Release.</span><span class="sxs-lookup"><span data-stu-id="a63be-118">Release the effect with IUnknown::Release.</span></span>

    <span data-ttu-id="a63be-119">Quando você cria um XAPO, ele terá uma contagem de referência de 1.</span><span class="sxs-lookup"><span data-stu-id="a63be-119">When you create an XAPO, it will have a reference count of 1.</span></span> <span data-ttu-id="a63be-120">Quando XAPO é passado para XAudio2 com [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 incrementa a contagem de referência no XAPO.</span><span class="sxs-lookup"><span data-stu-id="a63be-120">When the XAPO is passed to XAudio2 with [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 increments the reference count on the XAPO.</span></span> <span data-ttu-id="a63be-121">Liberar a referência do cliente para o XAPO permite que o XAudio2 assuma a propriedade do XAPO.</span><span class="sxs-lookup"><span data-stu-id="a63be-121">Releasing the client's reference to the XAPO allows XAudio2 to take ownership of the XAPO.</span></span> <span data-ttu-id="a63be-122">Se XAudio2 tiver a única referência para o XAPO, ele será Descartado quando não estiver mais sendo usado pelo XAudio2.</span><span class="sxs-lookup"><span data-stu-id="a63be-122">If XAudio2 has the only reference to the XAPO, it will be disposed of when it is no longer being used by XAudio2.</span></span> <span data-ttu-id="a63be-123">Se o código do cliente precisar manter uma referência para o XAPO — por exemplo, para reutilização posterior — você deve ignorar esta etapa.</span><span class="sxs-lookup"><span data-stu-id="a63be-123">If the client code needs to maintain a reference to the XAPO—for example for later reuse—you should skip this step.</span></span>

    ```
    pXAPO->Release();
    ```

    

6.  <span data-ttu-id="a63be-124">Preencha a estrutura do parâmetro, se houver, associada ao efeito.</span><span class="sxs-lookup"><span data-stu-id="a63be-124">Populate the parameter structure, if any, associated with the effect.</span></span> <span data-ttu-id="a63be-125">O efeito de reverberação usa uma estrutura de [**\_ \_ parâmetros de reverberação XAUDIO2FX**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters) .</span><span class="sxs-lookup"><span data-stu-id="a63be-125">The reverb effect uses an [**XAUDIO2FX\_REVERB\_PARAMETERS**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters) structure.</span></span>

    ```
    XAUDIO2FX_REVERB_PARAMETERS reverbParameters;
    reverbParameters.ReflectionsDelay = XAUDIO2FX_REVERB_DEFAULT_REFLECTIONS_DELAY;
    reverbParameters.ReverbDelay = XAUDIO2FX_REVERB_DEFAULT_REVERB_DELAY;
    reverbParameters.RearDelay = XAUDIO2FX_REVERB_DEFAULT_REAR_DELAY;
    reverbParameters.PositionLeft = XAUDIO2FX_REVERB_DEFAULT_POSITION;
    reverbParameters.PositionRight = XAUDIO2FX_REVERB_DEFAULT_POSITION;
    reverbParameters.PositionMatrixLeft = XAUDIO2FX_REVERB_DEFAULT_POSITION_MATRIX;
    reverbParameters.PositionMatrixRight = XAUDIO2FX_REVERB_DEFAULT_POSITION_MATRIX;
    reverbParameters.EarlyDiffusion = XAUDIO2FX_REVERB_DEFAULT_EARLY_DIFFUSION;
    reverbParameters.LateDiffusion = XAUDIO2FX_REVERB_DEFAULT_LATE_DIFFUSION;
    reverbParameters.LowEQGain = XAUDIO2FX_REVERB_DEFAULT_LOW_EQ_GAIN;
    reverbParameters.LowEQCutoff = XAUDIO2FX_REVERB_DEFAULT_LOW_EQ_CUTOFF;
    reverbParameters.HighEQGain = XAUDIO2FX_REVERB_DEFAULT_HIGH_EQ_GAIN;
    reverbParameters.HighEQCutoff = XAUDIO2FX_REVERB_DEFAULT_HIGH_EQ_CUTOFF;
    reverbParameters.RoomFilterFreq = XAUDIO2FX_REVERB_DEFAULT_ROOM_FILTER_FREQ;
    reverbParameters.RoomFilterMain = XAUDIO2FX_REVERB_DEFAULT_ROOM_FILTER_MAIN;
    reverbParameters.RoomFilterHF = XAUDIO2FX_REVERB_DEFAULT_ROOM_FILTER_HF;
    reverbParameters.ReflectionsGain = XAUDIO2FX_REVERB_DEFAULT_REFLECTIONS_GAIN;
    reverbParameters.ReverbGain = XAUDIO2FX_REVERB_DEFAULT_REVERB_GAIN;
    reverbParameters.DecayTime = XAUDIO2FX_REVERB_DEFAULT_DECAY_TIME;
    reverbParameters.Density = XAUDIO2FX_REVERB_DEFAULT_DENSITY;
    reverbParameters.RoomSize = XAUDIO2FX_REVERB_DEFAULT_ROOM_SIZE;
    reverbParameters.WetDryMix = XAUDIO2FX_REVERB_DEFAULT_WET_DRY_MIX;
    ```

    

7.  <span data-ttu-id="a63be-126">Passe a estrutura do parâmetro de efeito para o efeito chamando a função [**Seteffectparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) na voz à qual o efeito está anexado.</span><span class="sxs-lookup"><span data-stu-id="a63be-126">Pass the effect parameter structure to the effect by calling the [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) function on the voice to which the effect is attached.</span></span>

    ```
    hr = pVoice->SetEffectParameters( 0, &reverbParameters, sizeof( reverbParameters ) );
    ```

    

8.  <span data-ttu-id="a63be-127">Desabilite ou habilite o efeito, sempre que apropriado.</span><span class="sxs-lookup"><span data-stu-id="a63be-127">Disable or enable the effect, whenever appropriate.</span></span>

    <span data-ttu-id="a63be-128">Você pode usar o [**DisableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) a qualquer momento para desativar um efeito.</span><span class="sxs-lookup"><span data-stu-id="a63be-128">You can use [**DisableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) at any time to turn an effect off.</span></span>

    ```
    pVoice->DisableEffect(0);
    ```

    

    <span data-ttu-id="a63be-129">Você pode ativar um efeito novamente com [**EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect).</span><span class="sxs-lookup"><span data-stu-id="a63be-129">You can turn on an effect again with [**EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect).</span></span>

    ```
    pVoice->EnableEffect(0);
    ```

    

    <span data-ttu-id="a63be-130">Os parâmetros para [**DisableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) e [**EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect) especificam qual efeito na cadeia habilitar ou desabilitar.</span><span class="sxs-lookup"><span data-stu-id="a63be-130">The parameters for [**DisableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) and [**EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect) specify which effect in the chain to enable or disable.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a63be-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a63be-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a63be-132">Efeitos de áudio</span><span class="sxs-lookup"><span data-stu-id="a63be-132">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="a63be-133">Guia de Programação em XAudio2</span><span class="sxs-lookup"><span data-stu-id="a63be-133">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="a63be-134">Como: Compilar um gráfico de processamento de áudio básico</span><span class="sxs-lookup"><span data-stu-id="a63be-134">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="a63be-135">Visão geral do XAPO</span><span class="sxs-lookup"><span data-stu-id="a63be-135">XAPO Overview</span></span>](xapo-overview.md)
</dt> <dt>

[<span data-ttu-id="a63be-136">Como: usar XAOPFX no XAudio2</span><span class="sxs-lookup"><span data-stu-id="a63be-136">How to: Use XAOPFX in XAudio2</span></span>](how-to--use-xapofx-in-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="a63be-137">Como: usar um XAOP no XAudio2</span><span class="sxs-lookup"><span data-stu-id="a63be-137">How to: Use an XAOP in XAudio2</span></span>](how-to--use-an-xapo-in-xaudio2.md)
</dt> </dl>

 

 

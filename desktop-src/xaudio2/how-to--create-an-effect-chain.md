---
description: Este tópico mostra como você pode aplicar uma cadeia de efeito a uma voz para permitir o processamento personalizado dos dados de áudio para essa voz. Este tópico descreve como usar o efeito de reverberação, que é um dos efeitos XAudio2 internos.
ms.assetid: 4c33bd83-2654-cd6f-ea6c-bbc0d5872638
title: 'Como: Criar uma cadeia de efeitos'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46abd6372fe07f71d75a4963f6617cdeda15ecf8390e3142fcf110029bd8f6dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119838408"
---
# <a name="how-to-create-an-effect-chain"></a>Como: Criar uma cadeia de efeitos

Este tópico mostra como você pode aplicar uma cadeia de efeito a uma voz para permitir o processamento personalizado dos dados de áudio para essa voz. Este tópico descreve como usar o efeito de reverberação, que é um dos efeitos XAudio2 internos.

## <a name="to-create-a-basic-effect-chain-that-applies-an-effect-to-a-voice"></a>Para criar uma cadeia de efeito básica que aplica um efeito a uma voz

1.  Crie o efeito.

    Neste exemplo, a função [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) cria um efeito de reverberação. Consulte [XAudio2 Audio Effects](xaudio2-audio-effects.md) para obter uma lista de possíveis fontes de efeitos para uso com o XAudio2.

    ```
    IUnknown * pXAPO;
    hr = XAudio2CreateReverb(&pXAPO);
    ```

    

2.  Popular uma estrutura de [**\_ \_ descritor de efeito XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) com dados.

    Se houver vários efeitos na cadeia, cada efeito precisará de uma estrutura [**de \_ \_ descritor de efeito XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) .

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

3.  Preencha uma estrutura de [**\_ \_ cadeia de efeito de XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) com dados. Nesse caso, a cadeia tem apenas um efeito. Se a cadeia tiver mais de um efeito, o membro EffectCount conterá a contagem de efeitos e o membro pEffectDescriptors apontará para uma matriz de estruturas de \_ descritor de efeito XAudio2 \_ .

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

4.  Aplique a cadeia de efeito a uma voz com a função [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) .

    Você pode aplicar cadeias de efeito a vozes mestre, vozes de origem e vozes submix.

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

5.  Libere o efeito com IUnknown:: Release.

    Quando você cria um XAPO, ele terá uma contagem de referência de 1. Quando XAPO é passado para XAudio2 com [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 incrementa a contagem de referência no XAPO. Liberar a referência do cliente para o XAPO permite que o XAudio2 assuma a propriedade do XAPO. Se XAudio2 tiver a única referência para o XAPO, ele será Descartado quando não estiver mais sendo usado pelo XAudio2. Se o código do cliente precisar manter uma referência para o XAPO — por exemplo, para reutilização posterior — você deve ignorar esta etapa.

    ```
    pXAPO->Release();
    ```

    

6.  Preencha a estrutura do parâmetro, se houver, associada ao efeito. O efeito de reverberação usa uma estrutura de [**\_ \_ parâmetros de reverberação XAUDIO2FX**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters) .

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

    

7.  Passe a estrutura do parâmetro de efeito para o efeito chamando a função [**Seteffectparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) na voz à qual o efeito está anexado.

    ```
    hr = pVoice->SetEffectParameters( 0, &reverbParameters, sizeof( reverbParameters ) );
    ```

    

8.  Desabilite ou habilite o efeito, sempre que apropriado.

    Você pode usar o [**DisableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) a qualquer momento para desativar um efeito.

    ```
    pVoice->DisableEffect(0);
    ```

    

    Você pode ativar um efeito novamente com [**EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect).

    ```
    pVoice->EnableEffect(0);
    ```

    

    Os parâmetros para [**DisableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) e [**EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect) especificam qual efeito na cadeia habilitar ou desabilitar.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Efeitos de áudio](audio-effects.md)
</dt> <dt>

[Guia de Programação em XAudio2](programming-guide.md)
</dt> <dt>

[Como: Compilar um gráfico de processamento de áudio básico](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Visão geral do XAPO](xapo-overview.md)
</dt> <dt>

[Como: usar XAOPFX no XAudio2](how-to--use-xapofx-in-xaudio2.md)
</dt> <dt>

[Como: usar um XAOP no XAudio2](how-to--use-an-xapo-in-xaudio2.md)
</dt> </dl>

 

 

---
description: Este tópico mostra como usar um dos efeitos incluídos no XAPOFX em uma cadeia de efeitos de XAudio2.
ms.assetid: dc325584-13f7-231a-e0c7-17f38d54ae11
title: 'Como: Usar um XAPOFX no XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 618e508d5e023c29c373193aa38da9d0e7f9f76c94a57f63e50df0c346426b6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118696147"
---
# <a name="how-to-use-xapofx-in-xaudio2"></a>Como: Usar um XAPOFX no XAudio2

Este tópico mostra como usar um dos efeitos incluídos no XAPOFX em uma cadeia de efeitos de XAudio2.

## <a name="to-use-an-effect-from-xapofx-in-an-xaudio2-effect-chain"></a>Para usar um efeito de XAPOFX em uma cadeia de efeito de XAudio2

1.  Crie o efeito passando o CLSID de um efeito de XAPOFX para a função [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) .

    Nesse caso, o efeito de reverbose simplificado FXReverb está sendo criado.

    ```
    IUnknown * pXAPO;
    CreateFX(__uuidof(FXReverb),&pXAPO);
    ```

    

2.  Popular uma estrutura de [**\_ \_ descritor de efeito XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) com dados.

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

3.  Preencha uma estrutura de [**\_ \_ cadeia de efeito de XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) com dados.

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

4.  Aplique a cadeia de efeito a uma voz XAudio2 com a função [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) .

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

    > [!Note]  
    > Você também pode aplicar uma cadeia de efeito a uma voz ao criar a voz passando a cadeia como um parâmetro para [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2:: CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice)ou [**IXAudio2:: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).

     

5.  Libere o efeito com IUnknown:: Release. Quando você cria um XAPO, ele terá uma contagem de referência de 1. Quando XAPO é passado para XAudio2 com [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 incrementa a contagem de referência no XAPO. Liberar a referência do cliente para o XAPO permite que o XAudio2 assuma a propriedade do XAPO. Se XAudio2 tiver a única referência para o XAPO, essa referência será descartada quando não estiver mais sendo usada pelo XAudio2. Se o código do cliente precisar manter uma referência para o XAPO — por exemplo, para reutilização posterior — você poderá ignorar esta etapa.

    ```
    pXAPO->Release();
    ```

    

6.  Preencha a estrutura do parâmetro, se houver, associada ao efeito.

    Nesse caso, a estrutura [**de \_ parâmetros FXREVERB**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters) é usada para definir o tamanho de difusão e sala que o efeito de reverberação deve usar.

    ```
    FXREVERB_PARAMETERS XAPOParameters;
    XAPOParameters.Diffusion = FXREVERB_DEFAULT_DIFFUSION;
    XAPOParameters.RoomSize = FXREVERB_DEFAULT_ROOMSIZE;
    ```

    

7.  Passe a estrutura do parâmetro de efeito para o efeito chamando a função [**Seteffectparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) na voz à qual o efeito está anexado.

    ```
    hr = pVoice->SetEffectParameters( 0, &XAPOParameters, sizeof( FXREVERB_PARAMETERS ) );
    ```

    

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Efeitos de áudio](audio-effects.md)
</dt> <dt>

[Guia de Programação em XAudio2](programming-guide.md)
</dt> </dl>

 

 

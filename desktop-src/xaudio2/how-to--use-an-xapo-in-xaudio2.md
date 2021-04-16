---
description: Este tópico mostra como usar um efeito criado com a API XAPO em uma cadeia de efeitos XAudio2.
ms.assetid: d4d24177-25eb-13ca-0e38-0c876a273e0d
title: 'Como: Usar um XAPO no XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 780e0ba59b5032ddc01b2709f1f3e9c5a0fcce1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779248"
---
# <a name="how-to-use-an-xapo-in-xaudio2"></a>Como: Usar um XAPO no XAudio2

Este tópico mostra como usar um efeito criado com a API XAPO em uma cadeia de efeitos XAudio2.

1.  Crie o XAPO conforme descrito em [como: criar um XAPO](how-to--create-an-xapo.md).

    Você também pode implementar a funcionalidade de parâmetro de tempo de execução conforme descrito em [como adicionar suporte a parâmetros de tempo de execução a um XAPO](how-to--add-run-time-parameter-support-to-an-xapo.md).

2.  Crie uma instância do XAPO.

    ```
    IUnknown * pXAPO;
    pXAPO = new SimpleXAPO();
    ```

    

3.  Popular uma estrutura de [**\_ \_ descritor de efeito XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) com dados.

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

4.  Preencha uma estrutura de [**\_ \_ cadeia de efeito de XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) com dados.

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

5.  Aplique a cadeia de efeito a uma voz XAudio2 com a função [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) .

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

    > [!Note]  
    > Uma cadeia de efeitos também pode ser aplicada a uma voz quando a voz é criada passando a cadeia como um parâmetro para [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2:: CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice)ou [**IXAudio2:: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).

     

6.  Libere o efeito com IUnknown:: Release.

    Quando você cria um XAPO, ele terá uma contagem de referência de 1. Quando XAPO é passado para XAudio2 com [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 incrementa a contagem de referência no XAPO. Liberar a referência do cliente para o XAPO permite que o XAudio2 assuma a propriedade do XAPO. Se XAudio2 tiver a única referência para o XAPO, ele será Descartado quando não estiver mais sendo usado pelo XAudio2. Se o código do cliente precisar manter uma referência para o XAPO para reutilização posterior, por exemplo, você deve ignorar esta etapa.

    ```
    pXAPO->Release();
    ```

    

7.  Preencha a estrutura do parâmetro, se houver, associada ao efeito. Nesse caso, a porcentagem de força total na qual o efeito deve ser aplicado.

    ```
    XAPO_PARAMETERS XAPOParameters;
    XAPOParameters.Level = 0.75;
    ```

    

8.  Passe a estrutura do parâmetro de efeito para o efeito chamando a função [**Seteffectparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) na voz à qual o efeito está anexado.

    ```
    hr = pVoice->SetEffectParameters( 0, &XAPOParameters, sizeof( XAPO_PARAMETERS ) );
    ```

    

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Efeitos de áudio](audio-effects.md)
</dt> <dt>

[Visão geral do XAPO](xapo-overview.md)
</dt> <dt>

[Guia de Programação em XAudio2](programming-guide.md)
</dt> </dl>

 

 

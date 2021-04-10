---
description: Este tópico mostra como você pode definir grupos de vozes para enviar sua saída para a mesma voz submix. Isso permite que uma única alteração em uma voz submix afete um grupo inteiro de vozes.
ms.assetid: 76c1c138-4846-9c4f-7875-446867436ee9
title: 'Como: Usar vozes de submixagem'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7152c3224d6528ac52651f2ca2f433631b347c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170278"
---
# <a name="how-to-use-submix-voices"></a>Como: Usar vozes de submixagem

Este tópico mostra como você pode definir grupos de vozes para enviar sua saída para a mesma voz submix. Isso permite que uma única alteração em uma voz submix afete um grupo inteiro de vozes.

1.  Crie uma [**voz submix**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) à qual todas as vozes de efeito de som do jogo serão enviadas.
    ```
    IXAudio2SubmixVoice * pSFXSubmixVoice;
    pXAudio2->CreateSubmixVoice(&pSFXSubmixVoice,1,44100,0,0,0,0);
    ```

    

2.  Criar uma [**XAudio2 \_ Voice \_ envia**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) uma estrutura que contém uma referência à voz submix.
    ```
    XAUDIO2_SEND_DESCRIPTOR SFXSend = {0, pSFXSubmixVoice};
    XAUDIO2_VOICE_SENDS SFXSendList = {1, &SFXSend};
    ```

    

3.  Passar a [**XAudio2 \_ Voice \_ envia**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) a estrutura para as novas vozes de origem à medida que elas são criadas.
    ```
    IXAudio2SourceVoice* pSFXSourceVoice;
    if( FAILED(hr = pXaudio2->CreateSourceVoice( &pSFXSourceVoice, (WAVEFORMATEX*)&wfx,
        0, XAUDIO2_DEFAULT_FREQ_RATIO, pCallback, pSFXSendList, NULL ) ) )
        return hr;
    ```

    

4.  Aplique as alterações a todas as vozes de efeito de som ajustando a voz submix.

    Neste exemplo, alterar o volume da voz submix com a função [**SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) altera efetivamente o volume de todas as vozes que a saída para ela.

    ```
    pSFXSubmixVoice->SetVolume(0.1);
    ```

    

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vozes](voices.md)
</dt> <dt>

[Guia de Programação em XAudio2](programming-guide.md)
</dt> <dt>

[Como: Compilar um gráfico de processamento de áudio básico](how-to--build-a-basic-audio-processing-graph.md)
</dt> </dl>

 

 

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
# <a name="how-to-use-submix-voices"></a><span data-ttu-id="bf6b5-104">Como: Usar vozes de submixagem</span><span class="sxs-lookup"><span data-stu-id="bf6b5-104">How to: Use Submix Voices</span></span>

<span data-ttu-id="bf6b5-105">Este tópico mostra como você pode definir grupos de vozes para enviar sua saída para a mesma voz submix.</span><span class="sxs-lookup"><span data-stu-id="bf6b5-105">This topic shows you how you can set groups of voices to send their output to the same submix voice.</span></span> <span data-ttu-id="bf6b5-106">Isso permite que uma única alteração em uma voz submix afete um grupo inteiro de vozes.</span><span class="sxs-lookup"><span data-stu-id="bf6b5-106">This enables a single change to a submix voice to affect a whole group of voices.</span></span>

1.  <span data-ttu-id="bf6b5-107">Crie uma [**voz submix**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) à qual todas as vozes de efeito de som do jogo serão enviadas.</span><span class="sxs-lookup"><span data-stu-id="bf6b5-107">Create a [**submix voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) to which all of the game's sound effect voices will send.</span></span>
    ```
    IXAudio2SubmixVoice * pSFXSubmixVoice;
    pXAudio2->CreateSubmixVoice(&pSFXSubmixVoice,1,44100,0,0,0,0);
    ```

    

2.  <span data-ttu-id="bf6b5-108">Criar uma [**XAudio2 \_ Voice \_ envia**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) uma estrutura que contém uma referência à voz submix.</span><span class="sxs-lookup"><span data-stu-id="bf6b5-108">Create an [**XAUDIO2\_VOICE\_SENDS**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) structure that contains a reference to the submix voice.</span></span>
    ```
    XAUDIO2_SEND_DESCRIPTOR SFXSend = {0, pSFXSubmixVoice};
    XAUDIO2_VOICE_SENDS SFXSendList = {1, &SFXSend};
    ```

    

3.  <span data-ttu-id="bf6b5-109">Passar a [**XAudio2 \_ Voice \_ envia**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) a estrutura para as novas vozes de origem à medida que elas são criadas.</span><span class="sxs-lookup"><span data-stu-id="bf6b5-109">Pass the [**XAUDIO2\_VOICE\_SENDS**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) structure to new source voices as they are created.</span></span>
    ```
    IXAudio2SourceVoice* pSFXSourceVoice;
    if( FAILED(hr = pXaudio2->CreateSourceVoice( &pSFXSourceVoice, (WAVEFORMATEX*)&wfx,
        0, XAUDIO2_DEFAULT_FREQ_RATIO, pCallback, pSFXSendList, NULL ) ) )
        return hr;
    ```

    

4.  <span data-ttu-id="bf6b5-110">Aplique as alterações a todas as vozes de efeito de som ajustando a voz submix.</span><span class="sxs-lookup"><span data-stu-id="bf6b5-110">Apply changes to all sound effect voices by adjusting the submix voice.</span></span>

    <span data-ttu-id="bf6b5-111">Neste exemplo, alterar o volume da voz submix com a função [**SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) altera efetivamente o volume de todas as vozes que a saída para ela.</span><span class="sxs-lookup"><span data-stu-id="bf6b5-111">In this example, changing the volume of the submix voice with the [**SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) function effectively changes the volume of all voices that output to it.</span></span>

    ```
    pSFXSubmixVoice->SetVolume(0.1);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="bf6b5-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bf6b5-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf6b5-113">Vozes</span><span class="sxs-lookup"><span data-stu-id="bf6b5-113">Voices</span></span>](voices.md)
</dt> <dt>

[<span data-ttu-id="bf6b5-114">Guia de Programação em XAudio2</span><span class="sxs-lookup"><span data-stu-id="bf6b5-114">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="bf6b5-115">Como: Compilar um gráfico de processamento de áudio básico</span><span class="sxs-lookup"><span data-stu-id="bf6b5-115">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> </dl>

 

 

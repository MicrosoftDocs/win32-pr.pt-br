---
description: Este tópico mostra como você pode aumentar ou diminuir a densidade dos dados de áudio alterando sua taxa de reprodução usando a função SetFrequencyRatio em uma voz de origem.
ms.assetid: 93408116-1c1f-307f-7e1f-090f2663ff0b
title: 'Como: alterar a densidade da voz'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7143dda30eae48bd8ed966c4170da2884d2633ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090682"
---
# <a name="how-to-change-voice-pitch"></a><span data-ttu-id="986ae-103">Como: alterar a densidade da voz</span><span class="sxs-lookup"><span data-stu-id="986ae-103">How to: Change Voice Pitch</span></span>

<span data-ttu-id="986ae-104">Este tópico mostra como você pode aumentar ou diminuir a densidade dos dados de áudio alterando sua taxa de reprodução usando a função [**SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) em uma voz de origem.</span><span class="sxs-lookup"><span data-stu-id="986ae-104">This topic shows you how you can raise or lower the pitch of audio data by changing its rate of playback using the [**SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) function on a source voice.</span></span>

## <a name="to-change-the-pitch-of-a-source-voice"></a><span data-ttu-id="986ae-105">Para alterar a inclinação de uma voz de origem</span><span class="sxs-lookup"><span data-stu-id="986ae-105">To change the pitch of a source voice</span></span>

1.  <span data-ttu-id="986ae-106">Determine a taxa de frequência desejada para a [**voz de origem**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice).</span><span class="sxs-lookup"><span data-stu-id="986ae-106">Determine the desired frequency ratio for the [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice).</span></span>

    <span data-ttu-id="986ae-107">Consulte [controle de volume e densidade de XAudio2](xaudio2-volume-and-pitch-control.md) para obter mais informações sobre como calcular a taxa de frequência.</span><span class="sxs-lookup"><span data-stu-id="986ae-107">See [XAudio2 Volume and Pitch Control](xaudio2-volume-and-pitch-control.md) for more information about calculating the frequency ratio.</span></span>

    ```
    float frequencyRatio = sourceRate / targetRate;
    ```

    

2.  <span data-ttu-id="986ae-108">Use a função [**SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) para definir a taxa de frequência da voz de origem.</span><span class="sxs-lookup"><span data-stu-id="986ae-108">Use the [**SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) function to set the frequency ratio of the source voice.</span></span>

    ```
    pSourceVoice->SetFrequencyRatio(frequencyRatio);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="986ae-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="986ae-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="986ae-110">Guia de Programação em XAudio2</span><span class="sxs-lookup"><span data-stu-id="986ae-110">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="986ae-111">Como: Compilar um gráfico de processamento de áudio básico</span><span class="sxs-lookup"><span data-stu-id="986ae-111">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="986ae-112">Controle de volume e densidade XAudio2</span><span class="sxs-lookup"><span data-stu-id="986ae-112">XAudio2 Volume and Pitch Control</span></span>](volume-and-pitch-control.md)
</dt> </dl>

 

 

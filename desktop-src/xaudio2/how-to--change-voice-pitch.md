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
# <a name="how-to-change-voice-pitch"></a>Como: alterar a densidade da voz

Este tópico mostra como você pode aumentar ou diminuir a densidade dos dados de áudio alterando sua taxa de reprodução usando a função [**SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) em uma voz de origem.

## <a name="to-change-the-pitch-of-a-source-voice"></a>Para alterar a inclinação de uma voz de origem

1.  Determine a taxa de frequência desejada para a [**voz de origem**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice).

    Consulte [controle de volume e densidade de XAudio2](xaudio2-volume-and-pitch-control.md) para obter mais informações sobre como calcular a taxa de frequência.

    ```
    float frequencyRatio = sourceRate / targetRate;
    ```

    

2.  Use a função [**SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) para definir a taxa de frequência da voz de origem.

    ```
    pSourceVoice->SetFrequencyRatio(frequencyRatio);
    ```

    

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de Programação em XAudio2](programming-guide.md)
</dt> <dt>

[Como: Compilar um gráfico de processamento de áudio básico](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Controle de volume e densidade XAudio2](volume-and-pitch-control.md)
</dt> </dl>

 

 

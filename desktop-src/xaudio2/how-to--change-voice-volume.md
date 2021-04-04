---
description: Este tópico mostra como você pode alterar o volume de uma voz em um nível geral, em cada canal de saída ou entre cada canal de uma voz e outra voz em sua caixa de envio.
ms.assetid: 40004128-4abb-4bcd-fe76-91276be8abec
title: 'Como: alterar o volume de voz'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a307c5585e56fb6dc4dbdc40386c6844607498ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662553"
---
# <a name="how-to-change-voice-volume"></a>Como: alterar o volume de voz

Este tópico mostra como você pode alterar o volume de uma voz em um nível geral, em cada canal de saída ou entre cada canal de uma voz e outra voz em sua caixa de [**envio**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends).

## <a name="to-set-an-overall-volume-level-for-the-voices-input"></a>Para definir um nível de volume geral para a entrada da voz

-   Use a função [**SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) .

    ```
    pSourceVoice->SetVolume(1.0);
    ```

    

## <a name="to-set-the-volume-of-the-voices-output-channels"></a>Para definir o volume dos canais de saída da voz

1.  Crie uma matriz de números de ponto flutuante que contenham os volumes desejados de todos os canais de saída na voz.

    A matriz terá uma entrada para cada canal na voz.

    ```
    float SourceVoiceChannelVolumes[1] = {1.0};
    ```

    

2.  Use a função [**SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes) para definir o volume dos canais de saída.

    ```
    hr = pSourceVoice->SetChannelVolumes(1,SourceVoiceChannelVolumes);
    ```

    

## <a name="to-set-the-volume-of-connections"></a>Para definir o volume de conexões

Defina o volume de conexão entre a voz e uma voz em sua caixa de [**envio**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends).

1.  Crie uma matriz de números de ponto flutuante que define uma matriz de saída se a voz enviar para outra voz.

    > [!Note]  
    > A matriz deve ter um número de entradas iguais a canais de voz de origem × canais de voz de destino. Neste exemplo, o mapeamento é de uma voz com um canal para uma voz com dois canais.

     

    ```
    float outputMatrix[2] = {1.0f,0.05f};
    ```

    

2.  Use a função [**SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) para definir a matriz de saída.

    ```
    pSourceVoice->SetOutputMatrix(pSubmixVoice,1,2,outputMatrix);
    ```

    

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de Programação em XAudio2](programming-guide.md)
</dt> <dt>

[Como: Compilar um gráfico de processamento de áudio básico](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Controle de volume e densidade XAudio2](volume-and-pitch-control.md)
</dt> </dl>

 

 

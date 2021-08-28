---
description: Este tópico mostra como você pode definir a matriz de saída de uma voz de origem mono que gera uma voz de mestre de estéreo para obter movimento panorâmico entre os alto-falantes esquerdo e direito.
ms.assetid: d87db173-6de0-09eb-7767-df619c88acfd
title: 'Como: deslocar um som'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e91ff27dfe7c951f95c37fed194a83dac09de8ccec7e37ebc5ad35ca548199
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118696265"
---
# <a name="how-to-pan-a-sound"></a>Como: deslocar um som

Este tópico mostra como você pode definir a matriz de saída de uma voz de origem mono que gera uma voz de mestre de estéreo para obter movimento panorâmico entre os alto-falantes esquerdo e direito.

## <a name="to-setup-panning"></a>Para configurar o movimento panorâmico

1.  Recupere a configuração do alto-falante usando [**IXAudio2MasteringVoice:: GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask).

    ```
    DWORD dwChannelMask;       
    pMasteringVoice->GetChannelMask( &dwChannelMask );       
    ```

    

2.  Crie uma matriz para manter a matriz de saída. O tamanho mínimo da matriz de saída é o número de canais na voz de origem, o número de canais na voz de saída. Nesse caso, uma matriz de oito elementos tratará uma saída de voz mono para qualquer formato de saída de até 7,1 surround sound.

    ```
    float outputMatrix[ 8 ];
    for (int i=0; i<8; i++) outputMatrix[i] = 0;
    ```

    

3.  Calcule os níveis de envio com base no movimento panorâmico desejado entre os alto-falantes esquerdo e direito. Neste exemplo, os valores de Pan vão de-1 a 1 com-1, indicando todo o som para o palestrante esquerdo e 1 indicando todo o som ao alto-falante direito.

    ```
    // pan of -1.0 indicates all left speaker, 
    // 1.0 is all right speaker, 0.0 is split between left and right
    float left = 0.5f - pan / 2;
    float right = 0.5f + pan / 2; 
    ```

    

4.  Defina os índices de matriz de saída correspondentes aos alto-falantes esquerdo e direito com os valores calculados na etapa anterior. Os alto-falantes esquerdo e direito são determinados examinando a máscara de canal retornada por [**IXAudio2MasteringVoice:: GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask). Como os canais sempre devem ser codificados na ordem especificada na página de referência do [**WAVEFORMATEXTENSIBLE**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-waveformatextensible) , é possível determinar o índice de matriz correspondente a um orador individual.

    ```
    switch (dwChannelMask)
    {
    case SPEAKER_MONO:
        outputMatrix[0] = 1.0;
        break;
    case SPEAKER_STEREO:
    case SPEAKER_2POINT1:
    case SPEAKER_SURROUND:
        outputMatrix[0] = left;
        outputMatrix[1] = right;
        break;
    case SPEAKER_QUAD:
        outputMatrix[0] = outputMatrix[2] = left;
        outputMatrix[1] = outputMatrix[3] = right;
        break;
    case SPEAKER_4POINT1:
        outputMatrix[ 0 ] = outputMatrix[ 3 ] = left;
        outputMatrix[ 1 ] = outputMatrix[ 4 ] = right;
        break;
    case SPEAKER_5POINT1:
    case SPEAKER_7POINT1:
    case SPEAKER_5POINT1_SURROUND:
        outputMatrix[ 0 ] = outputMatrix[ 4 ] = left;
        outputMatrix[ 1 ] = outputMatrix[ 5 ] = right;
        break;
    case SPEAKER_7POINT1_SURROUND:
        outputMatrix[ 0 ] = outputMatrix[ 4 ] = outputMatrix[ 6 ] = left;
        outputMatrix[ 1 ] = outputMatrix[ 5 ] = outputMatrix[ 7 ] = right;
        break;
    }
    ```

    

5.  Aplique a matriz de saída à voz de origem usando [**IXAudio2Voice:: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix). A voz de origem será uma voz de origem ou uma voz submix enviando para uma voz submix ou uma voz de mestre. Você pode obter informações sobre as vozes de origem e de destino, como o número de canais, usando [**IXAudio2Voice:: GetVoiceDetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails).

    ```
    // Assuming pVoice sends to pMasteringVoice

    XAUDIO2_VOICE_DETAILS VoiceDetails;
    pVoice->GetVoiceDetails(&VoiceDetails);

    XAUDIO2_VOICE_DETAILS MasterVoiceDetails;
    pMasteringVoice->GetVoiceDetails(&MasterVoiceDetails);

    pVoice->SetOutputMatrix( NULL, VoiceDetails.InputChannels, MasterVoiceDetails.InputChannels, outputMatrix );
    ```

    

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de Programação em XAudio2](programming-guide.md)
</dt> <dt>

[Como: Compilar um gráfico de processamento de áudio básico](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Controle de volume e densidade XAudio2](volume-and-pitch-control.md)
</dt> </dl>

 

 

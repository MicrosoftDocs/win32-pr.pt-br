---
description: O requisito mínimo para permitir que o XAudio2 reproduza dados de áudio é um grafo de processamento de áudio, que é construído a partir de uma única voz de mestre e uma única voz de origem.
ms.assetid: 40f79959-23c9-4513-363b-2f2fc85e4c0a
title: 'Como: Compilar um gráfico de processamento de áudio básico'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43a11601514e3bcad5536ed1a8599178bcc52aa0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768374"
---
# <a name="how-to-build-a-basic-audio-processing-graph"></a>Como: Compilar um gráfico de processamento de áudio básico

O requisito mínimo para permitir que o XAudio2 reproduza dados de áudio é um grafo de processamento de áudio, que é construído a partir de uma única voz de mestre e uma única voz de origem.

## <a name="to-build-a-basic-audio-processing-graph"></a>Para criar um grafo básico de processamento de áudio

1.  Inicialize o mecanismo XAudio2 seguindo as etapas descritas em [como: inicializar o XAudio2](how-to--initialize-xaudio2.md).
2.  Preencha uma estrutura de [**\_ buffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) **WAVEFORMATEX** e XAudio2 seguindo as etapas descritas em [como carregar arquivos de dados de áudio no XAudio2](how-to--load-audio-data-files-in-xaudio2.md).
3.  Crie uma voz de origem usando a função [**CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) .

    Quando você especifica NULL para o argumento pSendList de [**CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), a saída da voz de origem vai para a voz de mestre criada na etapa 1.

    ```
    IXAudio2SourceVoice* pSourceVoice;
    if( FAILED(hr = pXAudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx,
                  0, XAUDIO2_DEFAULT_FREQ_RATIO, NULL, NULL, NULL ) ) ) return hr;
    ```

    

    Depois de concluir esta etapa, há um gráfico de áudio simples que consiste na voz de origem, na voz de mestre e no dispositivo de áudio. As etapas restantes neste tópico de instruções mostram como iniciar os dados de áudio que fluem pelo grafo.

    Um grafo de áudio simples

    ![um gráfico de áudio simples.](images/xaudio2-audio-graph.png)

4.  Use a função [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) para enviar um [**\_ buffer XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) para a voz de origem.

    ```
    if( FAILED(hr = pSourceVoice->SubmitSourceBuffer( &buffer ) ) )
        return hr;
    ```

    

5.  Use a função [**Iniciar**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) para iniciar a voz de origem.

    ```
    if ( FAILED(hr = pSourceVoice->Start( 0, XAUDIO2_COMMIT_NOW ) ) )
        return hr;
    ```

    

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gráficos de áudio](audio-graphs.md)
</dt> <dt>

[Guia de Programação em XAudio2](programming-guide.md)
</dt> </dl>

 

 

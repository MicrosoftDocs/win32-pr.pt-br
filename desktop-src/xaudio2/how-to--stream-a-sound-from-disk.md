---
description: Você pode transmitir dados de áudio no XAudio2 criando um thread separado e executando leituras de buffer dos dados de áudio no thread de streaming e, em seguida, usar retornos de chamada para controlar esse thread.
ms.assetid: 48b80a66-91c1-973f-069b-6f63422d7154
title: 'Como: Fazer o streaming de um som do disco'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ee06866427a8efcdd3e132740d595ec547f55a592182ebfbdced0feefca793
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707096"
---
# <a name="how-to-stream-a-sound-from-disk"></a>Como: Fazer o streaming de um som do disco

> [!Note]  
> Esse conteúdo se aplica somente a aplicativos da área de trabalho e exigirá revisão para funcionar em um aplicativo Windows Store. Consulte a documentação para **CreateFile2,** [CreateEventEx,](/windows/win32/api/synchapi/nf-synchapi-createeventexa) [WaitForSingleObjectEx,](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) [SetFilePointerEx](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex)e **GetOverlappedResultEx.** Consulte o exemplo de Windows 8 StreamEffect na [Galeria de Exemplos Windows SDK.](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20stream%20effect%20sample%20(Windows%208))

 

Você pode transmitir dados de áudio no XAudio2 criando um thread separado e executando leituras de buffer dos dados de áudio no thread de streaming e, em seguida, usar retornos de chamada para controlar esse thread.

-   [Executando leituras de buffer no thread de streaming](#performing-buffer-reads-in-the-streaming-thread)
-   [Criando a classe de retorno de chamada](#creating-the-callback-class)

## <a name="performing-buffer-reads-in-the-streaming-thread"></a>Executando leituras de buffer no thread de streaming

Para executar leituras de buffer no thread de streaming, siga estas etapas:

1.  Crie uma matriz de buffers de leitura.

    ```
    #define STREAMING_BUFFER_SIZE 65536
    #define MAX_BUFFER_COUNT 3
    BYTE buffers[MAX_BUFFER_COUNT][STREAMING_BUFFER_SIZE];
    ```

    

2.  Inicializar uma estrutura OVERLAPPED.

    A estrutura é usada para verificar quando uma leitura de disco assíncrona é concluída.

    ```
    OVERLAPPED Overlapped = {0};
    Overlapped.hEvent = CreateEvent( NULL, TRUE, FALSE, NULL );
    ```

    

3.  Chame a [**função Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) na voz [**de origem**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) que tocará o áudio de streaming.

    ```
    hr = pSourceVoice->Start( 0, 0 );
    ```

    

4.  Loop enquanto a posição de leitura atual não é passada no final do arquivo de áudio.

    ```
    CurrentDiskReadBuffer = 0;
    CurrentPosition = 0;
    while ( CurrentPosition < cbWaveSize )
    {
        ...
    }
    ```

    

    No loop, faça o seguinte:

    1.  Leia uma parte dos dados do disco no buffer de leitura atual.

        ```
        DWORD dwRead;
        if( SUCCEEDED(hr) && 0 == ReadFile( hFile, pData, dwDataSize, &dwRead, pOverlapped ) )
            hr = HRESULT_FROM_WIN32( GetLastError() );
            DWORD cbValid = min( STREAMING_BUFFER_SIZE, cbWaveSize - CurrentPosition );
            DWORD dwRead;
            if( 0 == ReadFile( hFile, buffers[CurrentDiskReadBuffer], STREAMING_BUFFER_SIZE, &dwRead, &Overlapped ) )
                hr = HRESULT_FROM_WIN32( GetLastError() );
            Overlapped.Offset += cbValid;

            //update the file position to where it will be once the read finishes
            CurrentPosition += cbValid;
        ```

        

    2.  Use a **função GetOverlappedResult** para aguardar o evento que sinaliza que a leitura foi concluída.

        ```
        DWORD NumberBytesTransferred;
        ::GetOverlappedResult(hFile,&Overlapped,&NumberBytesTransferred, TRUE);
        ```

        

    3.  Aguarde até que o número de [](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) buffers na fila na voz de origem seja menor que o número de buffers de leitura.

        O estado da voz [**de origem**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) é verificado com a [**função GetState.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate)

        ```
        XAUDIO2_VOICE_STATE state;
        while( pSourceVoice->GetState( &state ), state.BuffersQueued >= MAX_BUFFER_COUNT - 1)
        {
            WaitForSingleObject( Context.hBufferEndEvent, INFINITE );
        }
        ```

        

    4.  Envie o buffer de leitura atual para a [**voz de origem**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) usando [**a função SubmitSourceBuffer.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer)

        ```
        XAUDIO2_BUFFER buf = {0};
        buf.AudioBytes = cbValid;
        buf.pAudioData = buffers[CurrentDiskReadBuffer];
        if( CurrentPosition >= cbWaveSize )
        {
            buf.Flags = XAUDIO2_END_OF_STREAM;
        }
        pSourceVoice->SubmitSourceBuffer( &buf );
        ```

        

    5.  De definir o índice de buffer de leitura atual para o próximo buffer.

        ```
        CurrentDiskReadBuffer++;
        CurrentDiskReadBuffer %= MAX_BUFFER_COUNT;
        ```

        

5.  Depois que o loop for concluído, aguarde até que os buffers em fila restantes terminem a reprodução.

    Quando os buffers restantes terminarem de tocar, o som será interrompido e o thread poderá sair ou ser reutilizado para transmitir outro som.

    ```
    XAUDIO2_VOICE_STATE state;
    while( pSourceVoice->GetState( &state ), state.BuffersQueued > 0 )
    {
        WaitForSingleObjectEx( Context.hBufferEndEvent, INFINITE, TRUE );
    }
    ```

    

## <a name="creating-the-callback-class"></a>Criando a classe de retorno de chamada

Para criar a classe de retorno de chamada, crie uma classe que herda da interface [**IXAudio2VoiceCallback.**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback)

A classe deve definir um evento em [**seu método OnBufferEnd.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onbufferend) Isso permite que o thread de streaming coloque-se em sleep até que o evento sinaliza que o XAudio2 concluiu a leitura de um buffer de áudio. Para obter mais informações sobre como usar retornos de chamada com XAudio2, consulte Como usar retornos de chamada [de voz de origem.](how-to--use-source-voice-callbacks.md)


```
struct StreamingVoiceContext : public IXAudio2VoiceCallback
{
    HANDLE hBufferEndEvent;
    StreamingVoiceContext(): hBufferEndEvent( CreateEvent( NULL, FALSE, FALSE, NULL ) ){}
    ~StreamingVoiceContext(){ CloseHandle( hBufferEndEvent ); }
    void OnBufferEnd( void* ){ SetEvent( hBufferEndEvent ); }
    ...
};
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Streaming de dados de áudio](streaming-audio-data.md)
</dt> <dt>

[Retorno de chamadas XAudio2](callbacks.md)
</dt> <dt>

[Guia de Programação em XAudio2](programming-guide.md)
</dt> <dt>

[Como: Compilar um gráfico de processamento de áudio básico](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Como: Usar retornos de chamadas de voz de origem](how-to--use-source-voice-callbacks.md)
</dt> </dl>

 

 

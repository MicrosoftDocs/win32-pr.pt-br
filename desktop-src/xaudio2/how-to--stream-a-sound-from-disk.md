---
description: Você pode transmitir dados de áudio no XAudio2 criando um thread separado e executar leituras de buffer dos dados de áudio no thread de streaming e, em seguida, usar retornos de chamada para controlar esse thread.
ms.assetid: 48b80a66-91c1-973f-069b-6f63422d7154
title: 'Como: Fazer o streaming de um som do disco'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c5598e8913514d6b0bf81b55bab5b481dbc43b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662551"
---
# <a name="how-to-stream-a-sound-from-disk"></a><span data-ttu-id="7184b-103">Como: Fazer o streaming de um som do disco</span><span class="sxs-lookup"><span data-stu-id="7184b-103">How to: Stream a Sound from Disk</span></span>

> [!Note]  
> <span data-ttu-id="7184b-104">Esse conteúdo se aplica somente a aplicativos da área de trabalho e exigirá revisão para funcionar em um aplicativo da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="7184b-104">This content applies only to desktop apps and will require revision to function in a Windows Store app.</span></span> <span data-ttu-id="7184b-105">Veja a documentação de **createfile2**, [CreateEventEx](/windows/win32/api/synchapi/nf-synchapi-createeventexa), [WaitForSingleObjectEx](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex), [SetFilePointerEx](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex)e **GetOverlappedResultEx**.</span><span class="sxs-lookup"><span data-stu-id="7184b-105">Please refer to the documentation for **CreateFile2**, [CreateEventEx](/windows/win32/api/synchapi/nf-synchapi-createeventexa), [WaitForSingleObjectEx](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex), [SetFilePointerEx](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex), and **GetOverlappedResultEx**.</span></span> <span data-ttu-id="7184b-106">Consulte o exemplo do Windows 8 do StreamEffect na [Galeria de exemplos SDK do Windows](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20stream%20effect%20sample%20(Windows%208)).</span><span class="sxs-lookup"><span data-stu-id="7184b-106">See the StreamEffect Windows 8 sample from the [Windows SDK Samples Gallery](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20stream%20effect%20sample%20(Windows%208)).</span></span>

 

<span data-ttu-id="7184b-107">Você pode transmitir dados de áudio no XAudio2 criando um thread separado e executar leituras de buffer dos dados de áudio no thread de streaming e, em seguida, usar retornos de chamada para controlar esse thread.</span><span class="sxs-lookup"><span data-stu-id="7184b-107">You can stream audio data in XAudio2 by creating a separate thread and perform buffer reads of the audio data in the streaming thread, and then use callbacks to control that thread.</span></span>

-   [<span data-ttu-id="7184b-108">Executando leituras de buffer no thread de streaming</span><span class="sxs-lookup"><span data-stu-id="7184b-108">Performing buffer reads in the streaming thread</span></span>](#performing-buffer-reads-in-the-streaming-thread)
-   [<span data-ttu-id="7184b-109">Criando a classe de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="7184b-109">Creating the callback class</span></span>](#creating-the-callback-class)

## <a name="performing-buffer-reads-in-the-streaming-thread"></a><span data-ttu-id="7184b-110">Executando leituras de buffer no thread de streaming</span><span class="sxs-lookup"><span data-stu-id="7184b-110">Performing buffer reads in the streaming thread</span></span>

<span data-ttu-id="7184b-111">Para executar leituras de buffer no thread de streaming, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="7184b-111">To perform buffer reads in the streaming thread follow these steps:</span></span>

1.  <span data-ttu-id="7184b-112">Crie uma matriz de buffers de leitura.</span><span class="sxs-lookup"><span data-stu-id="7184b-112">Create an array of read buffers.</span></span>

    ```
    #define STREAMING_BUFFER_SIZE 65536
    #define MAX_BUFFER_COUNT 3
    BYTE buffers[MAX_BUFFER_COUNT][STREAMING_BUFFER_SIZE];
    ```

    

2.  <span data-ttu-id="7184b-113">Inicializar uma estrutura SOBREPOSTA.</span><span class="sxs-lookup"><span data-stu-id="7184b-113">Initialize an OVERLAPPED structure.</span></span>

    <span data-ttu-id="7184b-114">A estrutura é usada para verificar quando uma leitura de disco assíncrono foi concluída.</span><span class="sxs-lookup"><span data-stu-id="7184b-114">The structure is used to check when an asynchronous disk read has finished.</span></span>

    ```
    OVERLAPPED Overlapped = {0};
    Overlapped.hEvent = CreateEvent( NULL, TRUE, FALSE, NULL );
    ```

    

3.  <span data-ttu-id="7184b-115">Chame a função [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) na [**voz de origem**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) que executará o áudio de streaming.</span><span class="sxs-lookup"><span data-stu-id="7184b-115">Call the [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) function on the [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) that will be playing the streaming audio.</span></span>

    ```
    hr = pSourceVoice->Start( 0, 0 );
    ```

    

4.  <span data-ttu-id="7184b-116">Loop enquanto a posição de leitura atual não é passada ao final do arquivo de áudio.</span><span class="sxs-lookup"><span data-stu-id="7184b-116">Loop while the current read position is not passed the end of the audio file.</span></span>

    ```
    CurrentDiskReadBuffer = 0;
    CurrentPosition = 0;
    while ( CurrentPosition < cbWaveSize )
    {
        ...
    }
    ```

    

    <span data-ttu-id="7184b-117">No loop, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="7184b-117">In the loop, do the following:</span></span>

    1.  <span data-ttu-id="7184b-118">Ler um bloco de dados do disco para o buffer de leitura atual.</span><span class="sxs-lookup"><span data-stu-id="7184b-118">Read a chunk of data from the disk into the current read buffer.</span></span>

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

        

    2.  <span data-ttu-id="7184b-119">Use a função **GetOverlappedResult** para aguardar o evento que sinaliza que a leitura foi concluída.</span><span class="sxs-lookup"><span data-stu-id="7184b-119">Use the **GetOverlappedResult** function to wait for the event that signals the read has finished.</span></span>

        ```
        DWORD NumberBytesTransferred;
        ::GetOverlappedResult(hFile,&Overlapped,&NumberBytesTransferred, TRUE);
        ```

        

    3.  <span data-ttu-id="7184b-120">Aguarde até que o número de buffers enfileirados na [**voz de origem**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) seja menor que o número de buffers de leitura.</span><span class="sxs-lookup"><span data-stu-id="7184b-120">Wait for the number of buffers queued on the [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) to be less than the number of read buffers.</span></span>

        <span data-ttu-id="7184b-121">O estado da [**voz de origem**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) é verificado com a função [**GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) .</span><span class="sxs-lookup"><span data-stu-id="7184b-121">The state of the [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) is checked with the [**GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) function.</span></span>

        ```
        XAUDIO2_VOICE_STATE state;
        while( pSourceVoice->GetState( &state ), state.BuffersQueued >= MAX_BUFFER_COUNT - 1)
        {
            WaitForSingleObject( Context.hBufferEndEvent, INFINITE );
        }
        ```

        

    4.  <span data-ttu-id="7184b-122">Envie o buffer de leitura atual para a [**voz de origem**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) usando a função [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) .</span><span class="sxs-lookup"><span data-stu-id="7184b-122">Submit the current read buffer to the [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) using the [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) function.</span></span>

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

        

    5.  <span data-ttu-id="7184b-123">Defina o índice do buffer de leitura atual para o próximo buffer.</span><span class="sxs-lookup"><span data-stu-id="7184b-123">Set the current read buffer index to the next buffer.</span></span>

        ```
        CurrentDiskReadBuffer++;
        CurrentDiskReadBuffer %= MAX_BUFFER_COUNT;
        ```

        

5.  <span data-ttu-id="7184b-124">Após a conclusão do loop, aguarde até que os buffers restantes da fila terminem de ser executados.</span><span class="sxs-lookup"><span data-stu-id="7184b-124">After the loop has finished, wait for the remaining queued buffers to finish playing.</span></span>

    <span data-ttu-id="7184b-125">Quando os buffers restantes terminaram de ser executados, o som é interrompido e o thread pode sair ou ser reutilizado para transmitir outro som.</span><span class="sxs-lookup"><span data-stu-id="7184b-125">When the remaining buffers have finished playing, the sound stops, and the thread can exit or be reused to stream another sound.</span></span>

    ```
    XAUDIO2_VOICE_STATE state;
    while( pSourceVoice->GetState( &state ), state.BuffersQueued > 0 )
    {
        WaitForSingleObjectEx( Context.hBufferEndEvent, INFINITE, TRUE );
    }
    ```

    

## <a name="creating-the-callback-class"></a><span data-ttu-id="7184b-126">Criando a classe de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="7184b-126">Creating the callback class</span></span>

<span data-ttu-id="7184b-127">Para criar a classe de retorno de chamada, crie uma classe que herda da interface [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) .</span><span class="sxs-lookup"><span data-stu-id="7184b-127">To create the callback class, create a class that inherits from the [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) interface.</span></span>

<span data-ttu-id="7184b-128">A classe deve definir um evento em seu método [**OnBufferEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onbufferend) .</span><span class="sxs-lookup"><span data-stu-id="7184b-128">The class should set an event in its [**OnBufferEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onbufferend) method.</span></span> <span data-ttu-id="7184b-129">Isso permite que o thread de streaming se coloque em suspensão até que o evento sinalize que o XAudio2 concluiu a leitura de um buffer de áudio.</span><span class="sxs-lookup"><span data-stu-id="7184b-129">This allows the streaming thread to put itself to sleep until the event signals it that XAudio2 has finished reading from an audio buffer.</span></span> <span data-ttu-id="7184b-130">Para obter mais informações sobre como usar retornos de chamada com XAudio2, consulte [como usar retornos de chamada de voz de origem](how-to--use-source-voice-callbacks.md).</span><span class="sxs-lookup"><span data-stu-id="7184b-130">For more information about using callbacks with XAudio2, see [How to: Use Source Voice Callbacks](how-to--use-source-voice-callbacks.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="7184b-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7184b-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7184b-132">Transmitindo dados de áudio</span><span class="sxs-lookup"><span data-stu-id="7184b-132">Streaming Audio Data</span></span>](streaming-audio-data.md)
</dt> <dt>

[<span data-ttu-id="7184b-133">Retorno de chamadas XAudio2</span><span class="sxs-lookup"><span data-stu-id="7184b-133">XAudio2 Callbacks</span></span>](callbacks.md)
</dt> <dt>

[<span data-ttu-id="7184b-134">Guia de Programação em XAudio2</span><span class="sxs-lookup"><span data-stu-id="7184b-134">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="7184b-135">Como: Compilar um gráfico de processamento de áudio básico</span><span class="sxs-lookup"><span data-stu-id="7184b-135">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="7184b-136">Como: Usar retornos de chamadas de voz de origem</span><span class="sxs-lookup"><span data-stu-id="7184b-136">How to: Use Source Voice Callbacks</span></span>](how-to--use-source-voice-callbacks.md)
</dt> </dl>

 

 

---
description: Ao criar uma voz de origem, você pode passar uma estrutura para ela que define os retornos de chamada para determinados eventos de áudio. Você pode usar esses retornos de chamada para executar ações ou para sinalizar outro código.
ms.assetid: 0bace0c5-9171-efd8-9a38-2c2b3452f73f
title: 'Como: Usar retornos de chamadas de voz de origem'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c10005ed838a22ea0dfce59312d6f293c213c39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647380"
---
# <a name="how-to-use-source-voice-callbacks"></a><span data-ttu-id="7db4d-104">Como: Usar retornos de chamadas de voz de origem</span><span class="sxs-lookup"><span data-stu-id="7db4d-104">How to: Use Source Voice Callbacks</span></span>

<span data-ttu-id="7db4d-105">Ao criar uma voz de origem, você pode passar uma estrutura para ela que define os retornos de chamada para determinados eventos de áudio.</span><span class="sxs-lookup"><span data-stu-id="7db4d-105">When you create a source voice, you can pass a structure to it that defines callbacks for certain audio events.</span></span> <span data-ttu-id="7db4d-106">Você pode usar esses retornos de chamada para executar ações ou para sinalizar outro código.</span><span class="sxs-lookup"><span data-stu-id="7db4d-106">You can use these callbacks to perform actions or to signal other code.</span></span>

1.  <span data-ttu-id="7db4d-107">Crie uma classe que herda da interface [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) .</span><span class="sxs-lookup"><span data-stu-id="7db4d-107">Create a class that inherits from the [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) interface.</span></span> <span data-ttu-id="7db4d-108">Todas as funções de membro de **IXAudio2VoiceCallback** são puramente virtuais e devem ser definidas.</span><span class="sxs-lookup"><span data-stu-id="7db4d-108">All member functions of **IXAudio2VoiceCallback** are purely virtual, and must be defined.</span></span> <span data-ttu-id="7db4d-109">A única função de interesse neste exemplo é [**OnStreamEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onstreamend).</span><span class="sxs-lookup"><span data-stu-id="7db4d-109">The only function of interest in this example is [**OnStreamEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onstreamend).</span></span> <span data-ttu-id="7db4d-110">Portanto, o restante das funções são os stubs.</span><span class="sxs-lookup"><span data-stu-id="7db4d-110">Therefore, the rest of the functions are stubs.</span></span> <span data-ttu-id="7db4d-111">A função **OnStreamEnd** aciona um evento que indica que o som é executado.</span><span class="sxs-lookup"><span data-stu-id="7db4d-111">The **OnStreamEnd** function triggers an event that indicates the sound is done playing.</span></span>

    ```
    class VoiceCallback : public IXAudio2VoiceCallback
    {
    public:
        HANDLE hBufferEndEvent;
        VoiceCallback(): hBufferEndEvent( CreateEvent( NULL, FALSE, FALSE, NULL ) ){}
        ~VoiceCallback(){ CloseHandle( hBufferEndEvent ); }

        //Called when the voice has just finished playing a contiguous audio stream.
        void OnStreamEnd() { SetEvent( hBufferEndEvent ); }

        //Unused methods are stubs
        void OnVoiceProcessingPassEnd() { }
        void OnVoiceProcessingPassStart(UINT32 SamplesRequired) {    }
        void OnBufferEnd(void * pBufferContext)    { }
        void OnBufferStart(void * pBufferContext) {    }
        void OnLoopEnd(void * pBufferContext) {    }
        void OnVoiceError(void * pBufferContext, HRESULT Error) { }
    };
    ```

    

2.  <span data-ttu-id="7db4d-112">Crie uma [**voz de origem**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) com [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) usando uma instância da classe de retorno de chamada criada anteriormente como o parâmetro pCallback.</span><span class="sxs-lookup"><span data-stu-id="7db4d-112">Create a [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) with [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) using an instance of the callback class created previously as the pCallback parameter.</span></span>

    ```
    VoiceCallback voiceCallback;
    if( FAILED(hr = pXaudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx,
                                 0, XAUDIO2_DEFAULT_FREQ_RATIO, &voiceCallback, NULL, NULL ) ) ) return;
    ```

    

3.  <span data-ttu-id="7db4d-113">Depois de iniciar a voz, use o método [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) para aguardar o evento ser disparado.</span><span class="sxs-lookup"><span data-stu-id="7db4d-113">After starting the voice, use the [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) method to wait for the event to be triggered.</span></span>

    ```
    WaitForSingleObjectEx( voiceCallback.hBufferEndEvent, INFINITE, TRUE );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="7db4d-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7db4d-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7db4d-115">Retornos de chamada</span><span class="sxs-lookup"><span data-stu-id="7db4d-115">Callbacks</span></span>](callbacks.md)
</dt> <dt>

[<span data-ttu-id="7db4d-116">Retorno de chamadas XAudio2</span><span class="sxs-lookup"><span data-stu-id="7db4d-116">XAudio2 Callbacks</span></span>](xaudio2-callbacks.md)
</dt> <dt>

[<span data-ttu-id="7db4d-117">Guia de Programação em XAudio2</span><span class="sxs-lookup"><span data-stu-id="7db4d-117">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="7db4d-118">Como: Compilar um gráfico de processamento de áudio básico</span><span class="sxs-lookup"><span data-stu-id="7db4d-118">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="7db4d-119">Como: Fazer o streaming de um som do disco</span><span class="sxs-lookup"><span data-stu-id="7db4d-119">How to: Stream a Sound from Disk</span></span>](how-to--stream-a-sound-from-disk.md)
</dt> </dl>

 

 

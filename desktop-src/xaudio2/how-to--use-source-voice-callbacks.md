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
# <a name="how-to-use-source-voice-callbacks"></a>Como: Usar retornos de chamadas de voz de origem

Ao criar uma voz de origem, você pode passar uma estrutura para ela que define os retornos de chamada para determinados eventos de áudio. Você pode usar esses retornos de chamada para executar ações ou para sinalizar outro código.

1.  Crie uma classe que herda da interface [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) . Todas as funções de membro de **IXAudio2VoiceCallback** são puramente virtuais e devem ser definidas. A única função de interesse neste exemplo é [**OnStreamEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onstreamend). Portanto, o restante das funções são os stubs. A função **OnStreamEnd** aciona um evento que indica que o som é executado.

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

    

2.  Crie uma [**voz de origem**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) com [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) usando uma instância da classe de retorno de chamada criada anteriormente como o parâmetro pCallback.

    ```
    VoiceCallback voiceCallback;
    if( FAILED(hr = pXaudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx,
                                 0, XAUDIO2_DEFAULT_FREQ_RATIO, &voiceCallback, NULL, NULL ) ) ) return;
    ```

    

3.  Depois de iniciar a voz, use o método [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) para aguardar o evento ser disparado.

    ```
    WaitForSingleObjectEx( voiceCallback.hBufferEndEvent, INFINITE, TRUE );
    ```

    

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Retornos de chamada](callbacks.md)
</dt> <dt>

[Retorno de chamadas XAudio2](xaudio2-callbacks.md)
</dt> <dt>

[Guia de Programação em XAudio2](programming-guide.md)
</dt> <dt>

[Como: Compilar um gráfico de processamento de áudio básico](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Como: Fazer o streaming de um som do disco](how-to--stream-a-sound-from-disk.md)
</dt> </dl>

 

 

---
description: Você pode notificar o código do cliente XAudio2 de eventos do mecanismo registrando uma instância de uma classe que implementa a interface IXAudio2EngineCallback com o mecanismo XAudio2.
ms.assetid: 006a8cb6-c24c-f7d1-9e8b-9cb2baa046c0
title: 'Como: Usar retornos de chamadas de dispositivo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04adec0efd0625157740488d70be7896688d1176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104370763"
---
# <a name="how-to-use-engine-callbacks"></a>Como: Usar retornos de chamadas de dispositivo

Você pode notificar o código do cliente XAudio2 de eventos do mecanismo registrando uma instância de uma classe que implementa a interface [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) com o mecanismo XAudio2. Isso permite que o código do cliente XAudio2 acompanhe quando o processamento de áudio está ocorrendo e quando reiniciar o mecanismo no caso de um erro crítico.

## <a name="to-use-an-engine-callback"></a>Para usar um retorno de chamada do mecanismo

As etapas a seguir registram um objeto para manipular eventos do mecanismo.

1.  Crie uma classe que herda da interface [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) .

    Todos os métodos de [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) são puramente virtuais e devem ser definidos. O método de interesse neste exemplo é [**IXAudio2EngineCallback:: OnCriticalError**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror), que define um sinalizador para sinalizar o loop principal do jogo que ocorreu um erro crítico. Os métodos restantes, [**IXAudio2EngineCallback:: OnProcessingPassStart**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassstart) e [**IXAudio2EngineCallback:: OnProcessingPassEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassend), são stubs neste exemplo.

    ```
    class EngineCallback : public IXAudio2EngineCallback
    {
        void OnProcessingPassEnd () {}
        void OnProcessingPassStart() {}
        void OnCriticalError (HRESULT Error) {}
    };
    ```

    

2.  Use [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) para criar uma instância do mecanismo XAudio2.

    ```
    if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
        return hr;
    ```

    

3.  Use [**IXAudio2:: RegisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) para registrar o retorno de chamada do mecanismo.

    ```
    pXAudio2->RegisterForCallbacks( &engineCallback );
    ```

    

4.  Se você não precisar mais do retorno de chamada do mecanismo, chame [**IXAudio2:: UnregisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-unregisterforcallbacks).

    ```
    pXAudio2->UnregisterForCallbacks( &engineCallback );
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

 

 

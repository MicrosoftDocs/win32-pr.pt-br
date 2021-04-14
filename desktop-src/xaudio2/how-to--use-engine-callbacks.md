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
# <a name="how-to-use-engine-callbacks"></a><span data-ttu-id="5aeb1-103">Como: Usar retornos de chamadas de dispositivo</span><span class="sxs-lookup"><span data-stu-id="5aeb1-103">How to: Use Engine Callbacks</span></span>

<span data-ttu-id="5aeb1-104">Você pode notificar o código do cliente XAudio2 de eventos do mecanismo registrando uma instância de uma classe que implementa a interface [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) com o mecanismo XAudio2.</span><span class="sxs-lookup"><span data-stu-id="5aeb1-104">You can notify the XAudio2 client code of engine events by registering an instance of a class implementing the [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) interface with the XAudio2 engine.</span></span> <span data-ttu-id="5aeb1-105">Isso permite que o código do cliente XAudio2 acompanhe quando o processamento de áudio está ocorrendo e quando reiniciar o mecanismo no caso de um erro crítico.</span><span class="sxs-lookup"><span data-stu-id="5aeb1-105">This allows the XAudio2 client code to keep track of when audio processing is occurring, and when to restart the engine in the event of a critical error.</span></span>

## <a name="to-use-an-engine-callback"></a><span data-ttu-id="5aeb1-106">Para usar um retorno de chamada do mecanismo</span><span class="sxs-lookup"><span data-stu-id="5aeb1-106">To use an engine callback</span></span>

<span data-ttu-id="5aeb1-107">As etapas a seguir registram um objeto para manipular eventos do mecanismo.</span><span class="sxs-lookup"><span data-stu-id="5aeb1-107">The following steps register an object to handle engine events.</span></span>

1.  <span data-ttu-id="5aeb1-108">Crie uma classe que herda da interface [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) .</span><span class="sxs-lookup"><span data-stu-id="5aeb1-108">Create a class that inherits from the [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) interface.</span></span>

    <span data-ttu-id="5aeb1-109">Todos os métodos de [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) são puramente virtuais e devem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="5aeb1-109">All methods of [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) are purely virtual and must be defined.</span></span> <span data-ttu-id="5aeb1-110">O método de interesse neste exemplo é [**IXAudio2EngineCallback:: OnCriticalError**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror), que define um sinalizador para sinalizar o loop principal do jogo que ocorreu um erro crítico.</span><span class="sxs-lookup"><span data-stu-id="5aeb1-110">The method of interest in this example is [**IXAudio2EngineCallback::OnCriticalError**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror), which sets a flag to signal the main game loop that a critical error has occurred.</span></span> <span data-ttu-id="5aeb1-111">Os métodos restantes, [**IXAudio2EngineCallback:: OnProcessingPassStart**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassstart) e [**IXAudio2EngineCallback:: OnProcessingPassEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassend), são stubs neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="5aeb1-111">The remaining methods, [**IXAudio2EngineCallback::OnProcessingPassStart**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassstart) and [**IXAudio2EngineCallback::OnProcessingPassEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassend), are stubs in this example.</span></span>

    ```
    class EngineCallback : public IXAudio2EngineCallback
    {
        void OnProcessingPassEnd () {}
        void OnProcessingPassStart() {}
        void OnCriticalError (HRESULT Error) {}
    };
    ```

    

2.  <span data-ttu-id="5aeb1-112">Use [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) para criar uma instância do mecanismo XAudio2.</span><span class="sxs-lookup"><span data-stu-id="5aeb1-112">Use [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) to create an instance of the XAudio2 engine.</span></span>

    ```
    if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
        return hr;
    ```

    

3.  <span data-ttu-id="5aeb1-113">Use [**IXAudio2:: RegisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) para registrar o retorno de chamada do mecanismo.</span><span class="sxs-lookup"><span data-stu-id="5aeb1-113">Use [**IXAudio2::RegisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) to register the engine callback.</span></span>

    ```
    pXAudio2->RegisterForCallbacks( &engineCallback );
    ```

    

4.  <span data-ttu-id="5aeb1-114">Se você não precisar mais do retorno de chamada do mecanismo, chame [**IXAudio2:: UnregisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-unregisterforcallbacks).</span><span class="sxs-lookup"><span data-stu-id="5aeb1-114">If you don't need the engine callback any more, call [**IXAudio2::UnregisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-unregisterforcallbacks).</span></span>

    ```
    pXAudio2->UnregisterForCallbacks( &engineCallback );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="5aeb1-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5aeb1-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5aeb1-116">Retornos de chamada</span><span class="sxs-lookup"><span data-stu-id="5aeb1-116">Callbacks</span></span>](callbacks.md)
</dt> <dt>

[<span data-ttu-id="5aeb1-117">Retorno de chamadas XAudio2</span><span class="sxs-lookup"><span data-stu-id="5aeb1-117">XAudio2 Callbacks</span></span>](xaudio2-callbacks.md)
</dt> <dt>

[<span data-ttu-id="5aeb1-118">Guia de Programação em XAudio2</span><span class="sxs-lookup"><span data-stu-id="5aeb1-118">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="5aeb1-119">Como: Compilar um gráfico de processamento de áudio básico</span><span class="sxs-lookup"><span data-stu-id="5aeb1-119">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="5aeb1-120">Como: Fazer o streaming de um som do disco</span><span class="sxs-lookup"><span data-stu-id="5aeb1-120">How to: Stream a Sound from Disk</span></span>](how-to--stream-a-sound-from-disk.md)
</dt> </dl>

 

 

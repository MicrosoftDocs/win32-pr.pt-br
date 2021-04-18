---
description: Geradores de eventos de mídia
ms.assetid: 2e003ad4-9fcb-4834-a335-e4969ffd3a00
title: Geradores de eventos de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 125bf165740b0260f9131e0df8af420c8a669d97
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105802140"
---
# <a name="media-event-generators"></a><span data-ttu-id="c9b28-103">Geradores de eventos de mídia</span><span class="sxs-lookup"><span data-stu-id="c9b28-103">Media Event Generators</span></span>

<span data-ttu-id="c9b28-104">Media Foundation fornece uma maneira consistente para os objetos enviarem eventos.</span><span class="sxs-lookup"><span data-stu-id="c9b28-104">Media Foundation provides a consistent way for objects to send events.</span></span> <span data-ttu-id="c9b28-105">Um objeto pode usar eventos para sinalizar a conclusão de um método assíncrono ou notificar o aplicativo sobre uma alteração no estado do objeto.</span><span class="sxs-lookup"><span data-stu-id="c9b28-105">An object can use events to signal the completion of an asynchronous method, or to notify the application about a change in the object's state.</span></span>

<span data-ttu-id="c9b28-106">Se um objeto enviar eventos, ele exporá a interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="c9b28-106">If an object sends events, it exposes the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="c9b28-107">Sempre que o objeto envia um novo evento, o evento é colocado em uma fila.</span><span class="sxs-lookup"><span data-stu-id="c9b28-107">Whenever the object sends a new event, the event is placed in a queue.</span></span> <span data-ttu-id="c9b28-108">O aplicativo pode solicitar o próximo evento da fila chamando um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="c9b28-108">The application can request the next event from the queue by calling one of the following methods:</span></span>

-   [<span data-ttu-id="c9b28-109">**IMFMediaEventGenerator:: GetEvent**</span><span class="sxs-lookup"><span data-stu-id="c9b28-109">**IMFMediaEventGenerator::GetEvent**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent)

-   [<span data-ttu-id="c9b28-110">**IMFMediaEventGenerator::BeginGetEvent**</span><span class="sxs-lookup"><span data-stu-id="c9b28-110">**IMFMediaEventGenerator::BeginGetEvent**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent)

<span data-ttu-id="c9b28-111">O método [**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) é síncrono.</span><span class="sxs-lookup"><span data-stu-id="c9b28-111">The [**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) method is synchronous.</span></span> <span data-ttu-id="c9b28-112">Se um evento já estiver na fila, o método retornará imediatamente.</span><span class="sxs-lookup"><span data-stu-id="c9b28-112">If an event is already in the queue, the method returns immediately.</span></span> <span data-ttu-id="c9b28-113">Se não houver nenhum evento na fila, o método falhará imediatamente ou bloqueará até que o próximo evento seja enfileirado, dependendo de qual sinalizador você passa em **GetEvent**.</span><span class="sxs-lookup"><span data-stu-id="c9b28-113">If there is no event in the queue, the method either fails immediately, or blocks until the next event is queued, depending on which flag you pass into **GetEvent**.</span></span>

<span data-ttu-id="c9b28-114">O método [**BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) é assíncrono e, portanto, nunca é bloqueado.</span><span class="sxs-lookup"><span data-stu-id="c9b28-114">The [**BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) method is asynchronous, so it never blocks.</span></span> <span data-ttu-id="c9b28-115">Esse método usa um ponteiro para a interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) , que o aplicativo deve implementar.</span><span class="sxs-lookup"><span data-stu-id="c9b28-115">This method takes a pointer to the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface, which the application must implement.</span></span> <span data-ttu-id="c9b28-116">Quando o retorno de chamada é invocado, o aplicativo chama [**IMFMediaEventGenerator:: EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) para obter o evento da fila.</span><span class="sxs-lookup"><span data-stu-id="c9b28-116">When the callback is invoked, the application calls [**IMFMediaEventGenerator::EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) to get the event from the queue.</span></span> <span data-ttu-id="c9b28-117">Para obter mais informações sobre **IMFAsyncCallback**, consulte [métodos de retorno de chamada assíncrono](asynchronous-callback-methods.md).</span><span class="sxs-lookup"><span data-stu-id="c9b28-117">For more information about **IMFAsyncCallback**, see [Asynchronous Callback Methods](asynchronous-callback-methods.md).</span></span>

<span data-ttu-id="c9b28-118">Os eventos são representados pela interface [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) .</span><span class="sxs-lookup"><span data-stu-id="c9b28-118">Events are represented by the [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) interface.</span></span> <span data-ttu-id="c9b28-119">Essa interface tem os seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="c9b28-119">This interface has the following methods:</span></span>

-   <span data-ttu-id="c9b28-120">[**GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype): recupera o tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="c9b28-120">[**GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype): Retrieves the event type.</span></span> <span data-ttu-id="c9b28-121">O tipo de evento indica o que aconteceu para disparar o evento.</span><span class="sxs-lookup"><span data-stu-id="c9b28-121">The event type indicates what happened to trigger the event.</span></span>

-   <span data-ttu-id="c9b28-122">[**GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus): recupera um valor **HRESULT** , indicando se a operação que disparou o evento foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c9b28-122">[**GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus): Retrieves an **HRESULT** value, indicating whether the operation that triggered the event was successful.</span></span> <span data-ttu-id="c9b28-123">Se uma operação falhar de forma assíncrona, **GetStatus** retornará um código de falha.</span><span class="sxs-lookup"><span data-stu-id="c9b28-123">If an operation fails asynchronously, **GetStatus** returns a failure code.</span></span>

-   <span data-ttu-id="c9b28-124">[**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue): recupera um **PROPVARIANT** que contém dados de evento.</span><span class="sxs-lookup"><span data-stu-id="c9b28-124">[**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue): Retrieves a **PROPVARIANT** that contains event data.</span></span> <span data-ttu-id="c9b28-125">Os dados do evento dependem do tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="c9b28-125">The event data depends on the event type.</span></span> <span data-ttu-id="c9b28-126">Alguns eventos não têm nenhum dado.</span><span class="sxs-lookup"><span data-stu-id="c9b28-126">Some events do not have any data.</span></span>

-   <span data-ttu-id="c9b28-127">[**Getextendedattribute**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype): recupera um **GUID**.</span><span class="sxs-lookup"><span data-stu-id="c9b28-127">[**GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype): Retrieves a **GUID**.</span></span> <span data-ttu-id="c9b28-128">Esse método se aplica ao [evento MEExtendedType](meextendedtype.md)e fornece uma maneira de definir eventos personalizados.</span><span class="sxs-lookup"><span data-stu-id="c9b28-128">This method applies to the [MEExtendedType Event](meextendedtype.md), and provides a way to define custom events.</span></span>

<span data-ttu-id="c9b28-129">A interface [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) também herda a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="c9b28-129">The [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) interface also inherits the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="c9b28-130">Alguns eventos contêm informações adicionais como atributos.</span><span class="sxs-lookup"><span data-stu-id="c9b28-130">Some events carry additional information as attributes.</span></span>

<span data-ttu-id="c9b28-131">Para obter uma lista de tipos de eventos e seus dados e atributos associados, consulte [Media Foundation eventos](media-foundation-events.md).</span><span class="sxs-lookup"><span data-stu-id="c9b28-131">For a list of event types and their associated data and attributes, see [Media Foundation Events](media-foundation-events.md).</span></span>

## <a name="implementing-imfmediaeventgenerator"></a><span data-ttu-id="c9b28-132">Implementando IMFMediaEventGenerator</span><span class="sxs-lookup"><span data-stu-id="c9b28-132">Implementing IMFMediaEventGenerator</span></span>

<span data-ttu-id="c9b28-133">Se você estiver escrevendo um componente de plug-in para Media Foundation, como uma origem de mídia personalizada ou um coletor de mídia, talvez seja necessário implementar [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator).</span><span class="sxs-lookup"><span data-stu-id="c9b28-133">If you are writing a plug-in component for Media Foundation, such as a custom media source or media sink, you might need to implement [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator).</span></span> <span data-ttu-id="c9b28-134">Para tornar isso mais fácil, Media Foundation fornece um objeto auxiliar que implementa uma fila de eventos.</span><span class="sxs-lookup"><span data-stu-id="c9b28-134">To make this easier, Media Foundation provides a helper object that implements an event queue.</span></span> <span data-ttu-id="c9b28-135">Crie a fila de eventos chamando a função [**MFCreateEventQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateeventqueue) .</span><span class="sxs-lookup"><span data-stu-id="c9b28-135">Create the event queue by calling the [**MFCreateEventQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateeventqueue) function.</span></span> <span data-ttu-id="c9b28-136">A fila de eventos expõe a interface [**IMFMediaEventQueue**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventqueue) .</span><span class="sxs-lookup"><span data-stu-id="c9b28-136">The event queue exposes the [**IMFMediaEventQueue**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventqueue) interface.</span></span> <span data-ttu-id="c9b28-137">Na implementação do objeto dos métodos **IMFMediaEventGenerator** , chame o método correspondente na fila de eventos.</span><span class="sxs-lookup"><span data-stu-id="c9b28-137">In your object's implementation of the **IMFMediaEventGenerator** methods, call the corresponding method on the event queue.</span></span>

<span data-ttu-id="c9b28-138">O objeto fila de eventos é thread-safe.</span><span class="sxs-lookup"><span data-stu-id="c9b28-138">The event queue object is thread safe.</span></span> <span data-ttu-id="c9b28-139">Nunca mantenha o mesmo objeto de seção crítica ao chamar [**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-getevent) e [**QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-queueevent), pois **GetEvent** pode bloquear indefinidamente aguardando [**QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent).</span><span class="sxs-lookup"><span data-stu-id="c9b28-139">Never hold the same critical section object when calling [**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-getevent) and [**QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-queueevent), because **GetEvent** might block indefinitely waiting for [**QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent).</span></span> <span data-ttu-id="c9b28-140">Se você mantiver a mesma seção crítica para ambos os métodos, isso causará um deadlock.</span><span class="sxs-lookup"><span data-stu-id="c9b28-140">If you hold the same critical section for both methods, it will cause a deadlock.</span></span>

<span data-ttu-id="c9b28-141">Antes de liberar a fila de eventos, chame [**IMFMediaEventQueue:: Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) para liberar os recursos que o objeto mantém.</span><span class="sxs-lookup"><span data-stu-id="c9b28-141">Before releasing the event queue, call [**IMFMediaEventQueue::Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) to release the resources that the object holds.</span></span>

<span data-ttu-id="c9b28-142">Quando o objeto precisar gerar um evento, chame um dos seguintes métodos na fila de eventos:</span><span class="sxs-lookup"><span data-stu-id="c9b28-142">When your object needs to raise an event, call one of the following methods on the event queue:</span></span>

-   [<span data-ttu-id="c9b28-143">**IMFMediaEventQueue::QueueEvent**</span><span class="sxs-lookup"><span data-stu-id="c9b28-143">**IMFMediaEventQueue::QueueEvent**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent)

-   [<span data-ttu-id="c9b28-144">**IMFMediaEventQueue::QueueEventParamVar**</span><span class="sxs-lookup"><span data-stu-id="c9b28-144">**IMFMediaEventQueue::QueueEventParamVar**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueeventparamvar)

-   [<span data-ttu-id="c9b28-145">**IMFMediaEventQueue::QueueEventParamUnk**</span><span class="sxs-lookup"><span data-stu-id="c9b28-145">**IMFMediaEventQueue::QueueEventParamUnk**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueeventparamunk)

<span data-ttu-id="c9b28-146">Esses métodos colocam um novo evento na fila e sinalizam qualquer chamador que esteja aguardando o próximo evento.</span><span class="sxs-lookup"><span data-stu-id="c9b28-146">These methods put a new event on the queue and signal any caller that is waiting for the next event.</span></span>

<span data-ttu-id="c9b28-147">O código a seguir mostra uma classe que implementa [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) usando esse objeto auxiliar.</span><span class="sxs-lookup"><span data-stu-id="c9b28-147">The following code shows a class that implements [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) using this helper object.</span></span> <span data-ttu-id="c9b28-148">Essa classe define um método de **desligamento** público que desliga a fila de eventos e libera o ponteiro de fila de eventos.</span><span class="sxs-lookup"><span data-stu-id="c9b28-148">This class defines a public **Shutdown** method that shuts down the event queue and releases the event queue pointer.</span></span> <span data-ttu-id="c9b28-149">Esse comportamento seria típico para fontes de mídia e coletores de mídia, que sempre têm um método de **desligamento** .</span><span class="sxs-lookup"><span data-stu-id="c9b28-149">This behavior would be typical for media sources and media sinks, which always have a **Shutdown** method.</span></span>


```C++
class MyObject : public IMFMediaEventGenerator
{
private:
    long                m_nRefCount;    // Reference count.
    CRITICAL_SECTION    m_critSec;      // Critical section.
    IMFMediaEventQueue *m_pQueue;       // Event queue.
    BOOL                m_bShutdown;    // Is the object shut down?

    // CheckShutdown: Returns MF_E_SHUTDOWN if the object was shut down.
    HRESULT CheckShutdown() const 
    {
        return (m_bShutdown? MF_E_SHUTDOWN : S_OK);
    }

public:
    MyObject(HRESULT &hr) : m_nRefCount(0), m_pQueue(NULL), m_bShutdown(FALSE)
    {
        InitializeCriticalSection(&m_critSec);
        
        // Create the event queue.
        hr = MFCreateEventQueue(&m_pQueue);
    }

    // Shutdown: Shuts down this object.
    HRESULT Shutdown()
    {
        EnterCriticalSection(&m_critSec);

        HRESULT hr = CheckShutdown();
        if (SUCCEEDED(hr))
        {
            // Shut down the event queue.
            if (m_pQueue)
            {
                hr = m_pQueue->Shutdown();
            }

            // Release the event queue.
            SAFE_RELEASE(m_pQueue);
            // Release any other objects owned by the class (not shown).

            // Set the shutdown flag.
            m_bShutdown = TRUE;
        }

        LeaveCriticalSection(&m_critSec);
        return hr;
    }

    // TODO: Implement IUnknown (not shown).
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);

    // IMFMediaEventGenerator::BeginGetEvent
    STDMETHODIMP BeginGetEvent(IMFAsyncCallback* pCallback, IUnknown* pState)
    {
        EnterCriticalSection(&m_critSec);

        HRESULT hr = CheckShutdown();
        if (SUCCEEDED(hr))
        {
            hr = m_pQueue->BeginGetEvent(pCallback, pState);
        }

        LeaveCriticalSection(&m_critSec);
        return hr;    
    }

    // IMFMediaEventGenerator::EndGetEvent
    STDMETHODIMP EndGetEvent(IMFAsyncResult* pResult, IMFMediaEvent** ppEvent)
    {
        EnterCriticalSection(&m_critSec);

        HRESULT hr = CheckShutdown();
        if (SUCCEEDED(hr))
        {
            hr = m_pQueue->EndGetEvent(pResult, ppEvent);
        }

        LeaveCriticalSection(&m_critSec);
        return hr;    
    }

    // IMFMediaEventGenerator::GetEvent
    STDMETHODIMP GetEvent(DWORD dwFlags, IMFMediaEvent** ppEvent)
    {
        // Because GetEvent can block indefinitely, it requires
        // a slightly different locking strategy.
        IMFMediaEventQueue *pQueue = NULL;

        // Hold lock.
        EnterCriticalSection(&m_critSec);

        // Check shutdown
        HRESULT hr = CheckShutdown();

        // Store the pointer in a local variable, so that another thread
        // does not release it after we leave the critical section.
        if (SUCCEEDED(hr))
        {
            pQueue = m_pQueue;
            pQueue->AddRef();
        }

        // Release the lock.
        LeaveCriticalSection(&m_critSec);

        if (SUCCEEDED(hr))
        {
            hr = pQueue->GetEvent(dwFlags, ppEvent);
        }

        SAFE_RELEASE(pQueue);
        return hr;
    }

    // IMFMediaEventGenerator::QueueEvent
    STDMETHODIMP QueueEvent(
        MediaEventType met, REFGUID extendedType, 
        HRESULT hrStatus, const PROPVARIANT* pvValue)
    {
        EnterCriticalSection(&m_critSec);

        HRESULT hr = CheckShutdown();
        if (SUCCEEDED(hr))
        {
            hr = m_pQueue->QueueEventParamVar(
                met, extendedType, hrStatus, pvValue);
        }

        LeaveCriticalSection(&m_critSec);
        return hr;
    }

private:

    // The destructor is private. The caller must call Release.
    virtual ~MyObject()
    {
        assert(m_bShutdown);
        assert(m_nRefCount == 0);
    }
};
```



## <a name="related-topics"></a><span data-ttu-id="c9b28-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c9b28-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9b28-151">APIs da plataforma Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c9b28-151">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 




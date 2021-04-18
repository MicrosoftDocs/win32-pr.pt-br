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
# <a name="media-event-generators"></a>Geradores de eventos de mídia

Media Foundation fornece uma maneira consistente para os objetos enviarem eventos. Um objeto pode usar eventos para sinalizar a conclusão de um método assíncrono ou notificar o aplicativo sobre uma alteração no estado do objeto.

Se um objeto enviar eventos, ele exporá a interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . Sempre que o objeto envia um novo evento, o evento é colocado em uma fila. O aplicativo pode solicitar o próximo evento da fila chamando um dos seguintes métodos:

-   [**IMFMediaEventGenerator:: GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent)

-   [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent)

O método [**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) é síncrono. Se um evento já estiver na fila, o método retornará imediatamente. Se não houver nenhum evento na fila, o método falhará imediatamente ou bloqueará até que o próximo evento seja enfileirado, dependendo de qual sinalizador você passa em **GetEvent**.

O método [**BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) é assíncrono e, portanto, nunca é bloqueado. Esse método usa um ponteiro para a interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) , que o aplicativo deve implementar. Quando o retorno de chamada é invocado, o aplicativo chama [**IMFMediaEventGenerator:: EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) para obter o evento da fila. Para obter mais informações sobre **IMFAsyncCallback**, consulte [métodos de retorno de chamada assíncrono](asynchronous-callback-methods.md).

Os eventos são representados pela interface [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) . Essa interface tem os seguintes métodos:

-   [**GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype): recupera o tipo de evento. O tipo de evento indica o que aconteceu para disparar o evento.

-   [**GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus): recupera um valor **HRESULT** , indicando se a operação que disparou o evento foi bem-sucedida. Se uma operação falhar de forma assíncrona, **GetStatus** retornará um código de falha.

-   [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue): recupera um **PROPVARIANT** que contém dados de evento. Os dados do evento dependem do tipo de evento. Alguns eventos não têm nenhum dado.

-   [**Getextendedattribute**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype): recupera um **GUID**. Esse método se aplica ao [evento MEExtendedType](meextendedtype.md)e fornece uma maneira de definir eventos personalizados.

A interface [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) também herda a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Alguns eventos contêm informações adicionais como atributos.

Para obter uma lista de tipos de eventos e seus dados e atributos associados, consulte [Media Foundation eventos](media-foundation-events.md).

## <a name="implementing-imfmediaeventgenerator"></a>Implementando IMFMediaEventGenerator

Se você estiver escrevendo um componente de plug-in para Media Foundation, como uma origem de mídia personalizada ou um coletor de mídia, talvez seja necessário implementar [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator). Para tornar isso mais fácil, Media Foundation fornece um objeto auxiliar que implementa uma fila de eventos. Crie a fila de eventos chamando a função [**MFCreateEventQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateeventqueue) . A fila de eventos expõe a interface [**IMFMediaEventQueue**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventqueue) . Na implementação do objeto dos métodos **IMFMediaEventGenerator** , chame o método correspondente na fila de eventos.

O objeto fila de eventos é thread-safe. Nunca mantenha o mesmo objeto de seção crítica ao chamar [**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-getevent) e [**QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-queueevent), pois **GetEvent** pode bloquear indefinidamente aguardando [**QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent). Se você mantiver a mesma seção crítica para ambos os métodos, isso causará um deadlock.

Antes de liberar a fila de eventos, chame [**IMFMediaEventQueue:: Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) para liberar os recursos que o objeto mantém.

Quando o objeto precisar gerar um evento, chame um dos seguintes métodos na fila de eventos:

-   [**IMFMediaEventQueue::QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent)

-   [**IMFMediaEventQueue::QueueEventParamVar**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueeventparamvar)

-   [**IMFMediaEventQueue::QueueEventParamUnk**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueeventparamunk)

Esses métodos colocam um novo evento na fila e sinalizam qualquer chamador que esteja aguardando o próximo evento.

O código a seguir mostra uma classe que implementa [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) usando esse objeto auxiliar. Essa classe define um método de **desligamento** público que desliga a fila de eventos e libera o ponteiro de fila de eventos. Esse comportamento seria típico para fontes de mídia e coletores de mídia, que sempre têm um método de **desligamento** .


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[APIs da plataforma Media Foundation](media-foundation-platform-apis.md)
</dt> </dl>

 

 




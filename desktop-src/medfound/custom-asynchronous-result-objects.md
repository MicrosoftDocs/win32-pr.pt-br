---
description: Objetos de resultados assíncronos personalizados
ms.assetid: 78cef367-b007-46d5-bb7f-2b3f7eed9926
title: Objetos de resultados assíncronos personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7212152de737a0af8e290b2c837b40cd4ad68840a49df79db148b4691068678b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742922"
---
# <a name="custom-asynchronous-result-objects"></a>Objetos de resultados assíncronos personalizados

Este tópico descreve como implementar a interface [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) .

É raro que você precise escrever uma implementação personalizada da interface [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) . Em quase todos os casos, a implementação de Media Foundation padrão é suficiente. (Essa implementação é retornada pela função [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) .) No entanto, se você escrever uma implementação personalizada, haverá alguns problemas que você deve conhecer.

Primeiro, sua implementação deve herdar a estrutura [**MFASYNCRESULT**](/windows/win32/api/mfapi/ns-mfapi-mfasyncresult) . O Media Foundation filas de trabalho usam essa estrutura internamente para distribuir a operação. Inicialize todos os membros da estrutura para zero, exceto para o membro **pCallback** , que contém um ponteiro para a interface de retorno de chamada do chamador.

Em segundo lugar, o objeto deve chamar [**MFLockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mflockplatform) em seu construtor para bloquear a plataforma Media Foundation. Chame [**MFUnlockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockplatform) para desbloquear a plataforma. Essas funções ajudam a impedir que a plataforma seja desligada antes que o objeto seja destruído. Para obter mais informações, consulte [filas de trabalho](work-queues.md).

O código a seguir mostra uma implementação básica da interface [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) . Como mostrado, esse código não fornece recursos adicionais além da implementação de Media Foundation padrão.


```C++
///////////////////////////////////////////////////////////////////////////////
//  CMyAsyncResult
//
//  Custom implementation of IMFAsyncResult. All implementations of this 
//  interface must inherit the MFASYNCRESULT structure.
// 
///////////////////////////////////////////////////////////////////////////////

class CMyAsyncResult : public MFASYNCRESULT
{
protected:
    LONG        m_cRef;             // Reference count.
    BOOL        m_bLockPlatform;    // Locked the Media Foundation platform?
    IUnknown*   m_pState;           // Caller's state object. 
    IUnknown*   m_pObject;  // Optional object. See IMFAsyncResult::GetObject.

    // Constructor. 
    CMyAsyncResult(IMFAsyncCallback *pCallback, IUnknown *pState, HRESULT *phr) :
        m_cRef(1),
        m_bLockPlatform(FALSE),
        m_pObject(NULL),
        m_pState(pState)
    {
        *phr = MFLockPlatform();

        m_bLockPlatform = TRUE;

        // Initialize the MFASYNCRESULT members.
        ZeroMemory(&this->overlapped, sizeof(OVERLAPPED));
        hrStatusResult = S_OK;
        dwBytesTransferred = 0;
        hEvent = NULL;

        this->pCallback = pCallback;
        if (pCallback)
        {
            this->pCallback->AddRef();
        }

        if (m_pState)
        {
            m_pState->AddRef();
        }
    }

    virtual ~CMyAsyncResult()
    {
        SafeRelease(&pCallback);
        SafeRelease(&m_pState);
        SafeRelease(&m_pObject);

        if (m_bLockPlatform)
        {
            MFUnlockPlatform();
        }
    }

public:
    // Static method to create an instance of this object.
    static HRESULT CreateInstance(
        IMFAsyncCallback *pCallback,    // Callback to invoke.
        IUnknown *pState,               // Optional state object.
        CMyAsyncResult **ppResult       // Receives a pointer to the object.
        )
    {
        HRESULT hr = S_OK;

        *ppResult = NULL;

        CMyAsyncResult *pResult = 
            new (std::nothrow) CMyAsyncResult(pCallback, pState, &hr);

        if (pResult == NULL)
        {
            return E_OUTOFMEMORY;
        }
        if (FAILED(hr))
        {
            delete pResult;
            return hr;
        }

        // If the callback is NULL, create an event that will be signaled.
        if (pCallback == NULL)
        {
            pResult->hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
            if (pResult->hEvent == NULL)
            {
                hr = HRESULT_FROM_WIN32(GetLastError());
            }
        }

        if (SUCCEEDED(hr))
        {
            *ppResult = pResult;  // Return the pointer to the caller.
        }
        else
        {
            pResult->Release();
        }
        return hr;
    }

    // SetObject: Sets the optional result object. 
    // (This method is not part of the interface.)
    HRESULT SetObject(IUnknown *pObject)
    {
        SafeRelease(&m_pObject);
        m_pObject = pObject;
        if (pObject)
        {
            m_pObject->AddRef();
        }
        return S_OK;
    }

    // IUnknown methods.
    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CMyAsyncResult, IMFAsyncResult),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }
    
    // IMFAsyncResult methods.
    STDMETHODIMP GetState(IUnknown** ppunkState)
    {
        if (ppunkState == NULL)
        {
            return E_POINTER;
        }

        *ppunkState = m_pState;
        if (m_pState)
        {
            (*ppunkState)->AddRef();
        }

        return S_OK;
    }

    STDMETHODIMP GetStatus( void)
    {
        return hrStatusResult;
    }

    STDMETHODIMP STDMETHODCALLTYPE SetStatus(HRESULT hrStatus)
    {
        hrStatusResult = hrStatus;
        return S_OK;
    }

    STDMETHODIMP GetObject(IUnknown **ppObject)
    {
        if (ppObject == NULL)
        {
            return E_POINTER;
        }

        *ppObject = m_pObject;
        if (m_pObject)
        {
            (*ppObject)->AddRef();
        }
        return S_OK;
    }

    IUnknown* STDMETHODCALLTYPE GetStateNoAddRef()
    {
        return m_pState;  // Warning! Can be NULL. 
    }
};
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filas de trabalho](work-queues.md)
</dt> <dt>

[Métodos de retorno de chamada assíncrono](asynchronous-callback-methods.md)
</dt> </dl>

 

 




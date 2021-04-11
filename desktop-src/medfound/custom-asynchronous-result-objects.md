---
description: Objetos de resultados assíncronos personalizados
ms.assetid: 78cef367-b007-46d5-bb7f-2b3f7eed9926
title: Objetos de resultados assíncronos personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de5a0109b47255bc14fcccafbbb09c419848b5a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164206"
---
# <a name="custom-asynchronous-result-objects"></a><span data-ttu-id="ba8db-103">Objetos de resultados assíncronos personalizados</span><span class="sxs-lookup"><span data-stu-id="ba8db-103">Custom Asynchronous Result Objects</span></span>

<span data-ttu-id="ba8db-104">Este tópico descreve como implementar a interface [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) .</span><span class="sxs-lookup"><span data-stu-id="ba8db-104">This topic describes how to implement the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) interface.</span></span>

<span data-ttu-id="ba8db-105">É raro que você precise escrever uma implementação personalizada da interface [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) .</span><span class="sxs-lookup"><span data-stu-id="ba8db-105">It is rare that you will need to write a custom implementation of the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) interface.</span></span> <span data-ttu-id="ba8db-106">Em quase todos os casos, a implementação de Media Foundation padrão é suficiente.</span><span class="sxs-lookup"><span data-stu-id="ba8db-106">In almost all cases, the standard Media Foundation implementation is sufficient.</span></span> <span data-ttu-id="ba8db-107">(Essa implementação é retornada pela função [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) .) No entanto, se você escrever uma implementação personalizada, haverá alguns problemas que você deve conhecer.</span><span class="sxs-lookup"><span data-stu-id="ba8db-107">(This implementation is returned by the [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) function.) However, if you do write a custom implementation, there are some issues to be aware of.</span></span>

<span data-ttu-id="ba8db-108">Primeiro, sua implementação deve herdar a estrutura [**MFASYNCRESULT**](/windows/win32/api/mfapi/ns-mfapi-mfasyncresult) .</span><span class="sxs-lookup"><span data-stu-id="ba8db-108">First, your implementation must inherit the [**MFASYNCRESULT**](/windows/win32/api/mfapi/ns-mfapi-mfasyncresult) structure.</span></span> <span data-ttu-id="ba8db-109">O Media Foundation filas de trabalho usam essa estrutura internamente para distribuir a operação.</span><span class="sxs-lookup"><span data-stu-id="ba8db-109">The Media Foundation work queues use this structure internally to dispatch the operation.</span></span> <span data-ttu-id="ba8db-110">Inicialize todos os membros da estrutura para zero, exceto para o membro **pCallback** , que contém um ponteiro para a interface de retorno de chamada do chamador.</span><span class="sxs-lookup"><span data-stu-id="ba8db-110">Initialize all of the structure members to zero, except for the **pCallback** member, which contains a pointer to the caller's callback interface.</span></span>

<span data-ttu-id="ba8db-111">Em segundo lugar, o objeto deve chamar [**MFLockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mflockplatform) em seu construtor para bloquear a plataforma Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="ba8db-111">Second, your object should call [**MFLockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mflockplatform) in its constructor, to lock the Media Foundation platform.</span></span> <span data-ttu-id="ba8db-112">Chame [**MFUnlockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockplatform) para desbloquear a plataforma.</span><span class="sxs-lookup"><span data-stu-id="ba8db-112">Call [**MFUnlockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockplatform) to unlock the platform.</span></span> <span data-ttu-id="ba8db-113">Essas funções ajudam a impedir que a plataforma seja desligada antes que o objeto seja destruído.</span><span class="sxs-lookup"><span data-stu-id="ba8db-113">These functions help to prevent the platform from shutting down before the object is destroyed.</span></span> <span data-ttu-id="ba8db-114">Para obter mais informações, consulte [filas de trabalho](work-queues.md).</span><span class="sxs-lookup"><span data-stu-id="ba8db-114">For more information, see [Work Queues](work-queues.md).</span></span>

<span data-ttu-id="ba8db-115">O código a seguir mostra uma implementação básica da interface [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) .</span><span class="sxs-lookup"><span data-stu-id="ba8db-115">The following code shows a basic implementation of the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) interface.</span></span> <span data-ttu-id="ba8db-116">Como mostrado, esse código não fornece recursos adicionais além da implementação de Media Foundation padrão.</span><span class="sxs-lookup"><span data-stu-id="ba8db-116">As shown, this code provides no additional features beyond the standard Media Foundation implementation.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="ba8db-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ba8db-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba8db-118">Filas de trabalho</span><span class="sxs-lookup"><span data-stu-id="ba8db-118">Work Queues</span></span>](work-queues.md)
</dt> <dt>

[<span data-ttu-id="ba8db-119">Métodos de retorno de chamada assíncrono</span><span class="sxs-lookup"><span data-stu-id="ba8db-119">Asynchronous Callback Methods</span></span>](asynchronous-callback-methods.md)
</dt> </dl>

 

 




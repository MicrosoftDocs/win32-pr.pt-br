---
description: Dando suporte a vários retornos de chamada
ms.assetid: d57544cc-f16c-4415-9411-d06d6c16cb2f
title: Dando suporte a vários retornos de chamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b77a15899488e44ea3c1499b11af65894d47483c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661822"
---
# <a name="supporting-multiple-callbacks"></a><span data-ttu-id="73d5b-103">Dando suporte a vários retornos de chamada</span><span class="sxs-lookup"><span data-stu-id="73d5b-103">Supporting Multiple Callbacks</span></span>

<span data-ttu-id="73d5b-104">Se você chamar mais de um método assíncrono, cada um deles exigirá uma implementação separada de [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span><span class="sxs-lookup"><span data-stu-id="73d5b-104">If you call more than one asynchronous method, each one requires a separate implementation of [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span></span> <span data-ttu-id="73d5b-105">No entanto, talvez você queira implementar os retornos de chamada dentro de uma única classe C++.</span><span class="sxs-lookup"><span data-stu-id="73d5b-105">However, you might want to implement the callbacks inside a single C++ class.</span></span> <span data-ttu-id="73d5b-106">A classe pode ter apenas um método **Invoke** , portanto, uma solução é fornecer uma classe auxiliar **que delega chamadas** a outro método em uma classe de contêiner.</span><span class="sxs-lookup"><span data-stu-id="73d5b-106">The class can have only one **Invoke** method, so one solution is to provide a helper class that delegates **Invoke** calls to another method on a container class.</span></span>

<span data-ttu-id="73d5b-107">O código a seguir mostra um modelo de classe chamado `AsyncCallback` , que demonstra essa abordagem.</span><span class="sxs-lookup"><span data-stu-id="73d5b-107">The following code shows a class template named `AsyncCallback`, which demonstrates this approach.</span></span>


```C++
//////////////////////////////////////////////////////////////////////////
//  AsyncCallback [template]
//
//  Description:
//  Helper class that routes IMFAsyncCallback::Invoke calls to a class
//  method on the parent class.
//
//  Usage:
//  Add this class as a member variable. In the parent class constructor,
//  initialize the AsyncCallback class like this:
//      m_cb(this, &CYourClass::OnInvoke)
//  where
//      m_cb       = AsyncCallback object
//      CYourClass = parent class
//      OnInvoke   = Method in the parent class to receive Invoke calls.
//
//  The parent's OnInvoke method (you can name it anything you like) must
//  have a signature that matches the InvokeFn typedef below.
//////////////////////////////////////////////////////////////////////////

// T: Type of the parent object
template<class T>
class AsyncCallback : public IMFAsyncCallback
{
public:
    typedef HRESULT (T::*InvokeFn)(IMFAsyncResult *pAsyncResult);

    AsyncCallback(T *pParent, InvokeFn fn) : m_pParent(pParent), m_pInvokeFn(fn)
    {
    }

    // IUnknown
    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] =
        {
            QITABENT(AsyncCallback, IMFAsyncCallback),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }
    STDMETHODIMP_(ULONG) AddRef() {
        // Delegate to parent class.
        return m_pParent->AddRef();
    }
    STDMETHODIMP_(ULONG) Release() {
        // Delegate to parent class.
        return m_pParent->Release();
    }

    // IMFAsyncCallback methods
    STDMETHODIMP GetParameters(DWORD*, DWORD*)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }

    STDMETHODIMP Invoke(IMFAsyncResult* pAsyncResult)
    {
        return (m_pParent->*m_pInvokeFn)(pAsyncResult);
    }

    T *m_pParent;
    InvokeFn m_pInvokeFn;
};
```



<span data-ttu-id="73d5b-108">O parâmetro de modelo é o nome da classe de contêiner.</span><span class="sxs-lookup"><span data-stu-id="73d5b-108">The template parameter is the name of container class.</span></span> <span data-ttu-id="73d5b-109">O `AsyncCallback` Construtor tem dois parâmetros: um ponteiro para a classe de contêiner e o endereço de um método de retorno de chamada na classe de contêiner.</span><span class="sxs-lookup"><span data-stu-id="73d5b-109">The `AsyncCallback` constructor has two parameters: a pointer to the container class, and the address of a callback method on the container class.</span></span> <span data-ttu-id="73d5b-110">A classe de contêiner pode ter várias instâncias da `AsyncCallback` classe como variáveis de membro, uma para cada método assíncrono.</span><span class="sxs-lookup"><span data-stu-id="73d5b-110">The container class can have multiple instances of the `AsyncCallback` class as member variables, one for each asynchronous method.</span></span> <span data-ttu-id="73d5b-111">Quando a classe de contêiner chama um método assíncrono, ela usa a interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) do `AsyncCallback` objeto apropriado.</span><span class="sxs-lookup"><span data-stu-id="73d5b-111">When the container class calls an asynchronous method, it use the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface of the appropriate `AsyncCallback` object.</span></span> <span data-ttu-id="73d5b-112">Quando o `AsyncCallback` método [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) do objeto é chamado, a chamada é delegada para o método correto na classe de contêiner.</span><span class="sxs-lookup"><span data-stu-id="73d5b-112">When the `AsyncCallback` object's [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method is called, the call is delegated to the correct method on the container class.</span></span>

<span data-ttu-id="73d5b-113">O `AsyncCallback` objeto também Delega chamadas **AddRef** e **Release** para a classe de contêiner, de modo que a classe de contêiner gerencia o tempo de vida do `AsyncCallback` objeto.</span><span class="sxs-lookup"><span data-stu-id="73d5b-113">The `AsyncCallback` object also delegates **AddRef** and **Release** calls to the container class, so the container class manages the lifetime of the `AsyncCallback` object.</span></span> <span data-ttu-id="73d5b-114">Isso garante que o `AsyncCallback` objeto não será excluído até que o próprio objeto de contêiner seja excluído.</span><span class="sxs-lookup"><span data-stu-id="73d5b-114">This guarantees that the `AsyncCallback` object will not be deleted until the container object itself is deleted.</span></span>

<span data-ttu-id="73d5b-115">O código a seguir mostra como usar este modelo:</span><span class="sxs-lookup"><span data-stu-id="73d5b-115">The following code shows how to use this template:</span></span>


```C++
#pragma warning( push )
#pragma warning( disable : 4355 )  // 'this' used in base member initializer list

class CMyObject : public IUnknown
{
public:

    CMyObject() : m_CB(this, &CMyObject::OnInvoke)
    {
        // Other initialization here.
    }

    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);


private:

    AsyncCallback<CMyObject>   m_CB;

    HRESULT OnInvoke(IMFAsyncResult *pAsyncResult);
};

#pragma warning( pop )
```



<span data-ttu-id="73d5b-116">Neste exemplo, a classe de contêiner é nomeada `CMyObject` .</span><span class="sxs-lookup"><span data-stu-id="73d5b-116">In this example, the container class is named `CMyObject`.</span></span> <span data-ttu-id="73d5b-117">A variável de membro de *\_ CB m* é um `AsyncCallback` objeto.</span><span class="sxs-lookup"><span data-stu-id="73d5b-117">The *m\_CB* member variable is a `AsyncCallback` object.</span></span> <span data-ttu-id="73d5b-118">No `CMyObject` Construtor, a variável de membro de *\_ CB m* é inicializada com o endereço do `CMyObject::OnInvoke` método.</span><span class="sxs-lookup"><span data-stu-id="73d5b-118">In the `CMyObject` constructor, the *m\_CB* member variable is initialized with the address of the `CMyObject::OnInvoke` method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73d5b-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="73d5b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73d5b-120">Métodos de retorno de chamada assíncrono</span><span class="sxs-lookup"><span data-stu-id="73d5b-120">Asynchronous Callback Methods</span></span>](asynchronous-callback-methods.md)
</dt> </dl>

 

 




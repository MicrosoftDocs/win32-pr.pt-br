---
description: Este tópico descreve como implementar o log de erros nos serviços de edição do DirectShow.
ms.assetid: c0b3b25c-ed03-4f78-9c53-0c0bcff1c60c
title: Criando uma classe de log de erros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db08971c7bf1a0024669935079b7a9403c429327
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105752081"
---
# <a name="creating-an-error-logging-class"></a><span data-ttu-id="6dec9-103">Criando uma classe de log de erros</span><span class="sxs-lookup"><span data-stu-id="6dec9-103">Creating an Error Logging Class</span></span>

<span data-ttu-id="6dec9-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="6dec9-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="6dec9-105">Este tópico descreve como implementar o log de erros nos [serviços de edição do DirectShow](directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="6dec9-105">This topic describes how to implement error logging in [DirectShow Editing Services](directshow-editing-services.md).</span></span>

<span data-ttu-id="6dec9-106">Primeiro, declare uma classe que irá implementar o log de erros.</span><span class="sxs-lookup"><span data-stu-id="6dec9-106">First, declare a class that will implement error logging.</span></span> <span data-ttu-id="6dec9-107">A classe herda a interface [**IAMErrorLog**](iamerrorlog.md) .</span><span class="sxs-lookup"><span data-stu-id="6dec9-107">The class inherits the [**IAMErrorLog**](iamerrorlog.md) interface.</span></span> <span data-ttu-id="6dec9-108">Ele contém declarações para os três métodos **IUnknown** e para o método único em [IAMErrorLog](implementing-iamerrorlog.md).</span><span class="sxs-lookup"><span data-stu-id="6dec9-108">It contains declarations for the three **IUnknown** methods, and for the single method in [IAMErrorLog](implementing-iamerrorlog.md).</span></span> <span data-ttu-id="6dec9-109">A declaração de classe é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="6dec9-109">The class declaration is as follows:</span></span>


```C++
class CErrReporter : public IAMErrorLog
{
protected:
    long    m_lRef; // Reference count.

public:
    CErrReporter() { m_lRef = 0; }

    // IUnknown
    STDMETHOD(QueryInterface(REFIID, void**));
    STDMETHOD_(ULONG, AddRef());
    STDMETHOD_(ULONG, Release());

    // IAMErrorLog
    STDMETHOD(LogError(LONG, BSTR, LONG, HRESULT, VARIANT*));
};
```



<span data-ttu-id="6dec9-110">A única variável de membro na classe é m \_ lRef, que contém a contagem de referência do objeto.</span><span class="sxs-lookup"><span data-stu-id="6dec9-110">The only member variable in the class is m\_lRef, which holds the object's reference count.</span></span>

<span data-ttu-id="6dec9-111">Em seguida, defina os métodos em **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="6dec9-111">Next, define the methods in **IUnknown**.</span></span> <span data-ttu-id="6dec9-112">O exemplo a seguir mostra uma implementação padrão para esses métodos:</span><span class="sxs-lookup"><span data-stu-id="6dec9-112">The following example shows a standard implementation for these methods:</span></span>


```C++
STDMETHODIMP CErrReporter::QueryInterface(REFIID riid, void **ppv)
{
    if (ppv == NULL) return E_POINTER;

    *ppv = NULL;
    if (riid == IID_IUnknown)
        *ppv = static_cast<IUnknown*>(this);
    else if (riid == IID_IAMErrorLog)
        *ppv = static_cast<IAMErrorLog*>(this);
        
    else 
    return E_NOINTERFACE;

    AddRef();
    return S_OK;
}

STDMETHODIMP_(ULONG) CErrReporter::AddRef()
{
    return InterlockedIncrement(&m_lRef);
}

STDMETHODIMP_(ULONG) CErrReporter::Release()
{
    // Store the decremented count in a temporary
    // variable. 
    ULONG uCount = InterlockedDecrement(&m_lRef);
    if (uCount == 0)
    {
        delete this;
    }
    // Return the temporary variable, not the member
    // variable, for thread safety.
    return uCount;
}
```



<span data-ttu-id="6dec9-113">Com a estrutura COM em vigor, agora você pode implementar a interface **IAMErrorLog** .</span><span class="sxs-lookup"><span data-stu-id="6dec9-113">With the COM framework in place, you can now implement the **IAMErrorLog** interface.</span></span> <span data-ttu-id="6dec9-114">A próxima seção descreve como fazer isso.</span><span class="sxs-lookup"><span data-stu-id="6dec9-114">The next section describes how to do this.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6dec9-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6dec9-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6dec9-116">Erros de log</span><span class="sxs-lookup"><span data-stu-id="6dec9-116">Logging Errors</span></span>](logging-errors.md)
</dt> </dl>

 

 




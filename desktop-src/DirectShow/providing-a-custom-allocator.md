---
description: Fornecendo um alocador personalizado
ms.assetid: 4ce2db4b-c901-43a5-b905-7d6d923c940b
title: Fornecendo um alocador personalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e85a8d133ee5b686e25bc0d7d4a3e2444cb2791
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370151"
---
# <a name="providing-a-custom-allocator"></a><span data-ttu-id="7b724-103">Fornecendo um alocador personalizado</span><span class="sxs-lookup"><span data-stu-id="7b724-103">Providing a Custom Allocator</span></span>

<span data-ttu-id="7b724-104">Esta seção descreve como fornecer um alocador personalizado para um filtro.</span><span class="sxs-lookup"><span data-stu-id="7b724-104">This section describes how to provide a custom allocator for a filter.</span></span> <span data-ttu-id="7b724-105">Somente as conexões [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) são descritas, mas as etapas para uma conexão [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) são semelhantes.</span><span class="sxs-lookup"><span data-stu-id="7b724-105">Only [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) connections are described, but the steps for an [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) connection are similar.</span></span>

<span data-ttu-id="7b724-106">Primeiro, defina uma classe C++ para o alocador.</span><span class="sxs-lookup"><span data-stu-id="7b724-106">First, define a C++ class for the allocator.</span></span> <span data-ttu-id="7b724-107">Seu alocador pode derivar de uma das classes de alocador padrão, [**CBaseAllocator**](cbaseallocator.md) ou [**CMemAllocator**](cmemallocator.md), ou você pode criar uma classe de alocador totalmente nova.</span><span class="sxs-lookup"><span data-stu-id="7b724-107">Your allocator can derive from one of the standard allocator classes, [**CBaseAllocator**](cbaseallocator.md) or [**CMemAllocator**](cmemallocator.md), or you can create an entirely new allocator class.</span></span> <span data-ttu-id="7b724-108">Se você criar uma nova classe, ela deverá expor a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .</span><span class="sxs-lookup"><span data-stu-id="7b724-108">If you create a new class, it must expose the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

<span data-ttu-id="7b724-109">As etapas restantes dependem se o alocador pertence a um PIN de entrada ou a um pino de saída no filtro.</span><span class="sxs-lookup"><span data-stu-id="7b724-109">The remaining steps depend on whether your allocator belongs to an input pin or an output pin on your filter.</span></span> <span data-ttu-id="7b724-110">Os Pins de entrada desempenham uma função diferente dos Pins de saída durante a fase de negociação de alocador, pois o PIN de saída seleciona o alocador.</span><span class="sxs-lookup"><span data-stu-id="7b724-110">Input pins play a different role than output pins during the allocator negotiation phase, because the output pin ultimately selects the allocator.</span></span>

<span data-ttu-id="7b724-111">**Fornecendo um alocador personalizado para um PIN de entrada**</span><span class="sxs-lookup"><span data-stu-id="7b724-111">**Providing a Custom Allocator for an Input Pin**</span></span>

<span data-ttu-id="7b724-112">Para fornecer um alocador para um PIN de entrada, substitua o método [**CBaseInputPin:: Getalocador**](cbaseinputpin-getallocator.md) de entrada do PIN.</span><span class="sxs-lookup"><span data-stu-id="7b724-112">To provide an allocator for an input pin, override the input pin's [**CBaseInputPin::GetAllocator**](cbaseinputpin-getallocator.md) method.</span></span> <span data-ttu-id="7b724-113">Dentro desse método, verifique a variável de membro **m \_ pAllocator** .</span><span class="sxs-lookup"><span data-stu-id="7b724-113">Within this method, check the **m\_pAllocator** member variable.</span></span> <span data-ttu-id="7b724-114">Se essa variável for não **nula**, significa que o alocador já foi selecionado para essa conexão, portanto, o método **getalocador** deve retornar um ponteiro para esse alocador.</span><span class="sxs-lookup"><span data-stu-id="7b724-114">If this variable is non-**NULL**, it means the allocator has already been selected for this connection, so the **GetAllocator** method must return a pointer to that allocator.</span></span> <span data-ttu-id="7b724-115">Se **m \_ PAllocator** for **nulo**, isso significará que o alocador não foi selecionado, portanto, o método **getalocador** deve retornar um ponteiro para o alocador preferencial do pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="7b724-115">If **m\_pAllocator** is **NULL**, it means the allocator has not been selected, so the **GetAllocator** method should return a pointer to the input pin's preferred allocator.</span></span> <span data-ttu-id="7b724-116">Nesse caso, crie uma instância do seu alocador personalizado e retorne seu ponteiro [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .</span><span class="sxs-lookup"><span data-stu-id="7b724-116">In that case, create an instance of your custom allocator and return its [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) pointer.</span></span> <span data-ttu-id="7b724-117">O código a seguir mostra como implementar o método **Getalocador** :</span><span class="sxs-lookup"><span data-stu-id="7b724-117">The following code shows how to implement the **GetAllocator** method:</span></span>


```C++
STDMETHODIMP CMyInputPin::GetAllocator(IMemAllocator **ppAllocator)
{
    CheckPointer(ppAllocator, E_POINTER);
    if (m_pAllocator)  
    {
        // We already have an allocator, so return that one.
        *ppAllocator = m_pAllocator;
        (*ppAllocator)->AddRef();
        return S_OK;
    }

    // No allocator yet, so propose our custom allocator. The exact code
    // here will depend on your custom allocator class definition.
    HRESULT hr = S_OK;
    CMyAllocator *pAlloc = new CMyAllocator(&hr);
    if (!pAlloc)
    {
        return E_OUTOFMEMORY;
    }
    if (FAILED(hr))
    {
        delete pAlloc;
        return hr;
    }

    // Return the IMemAllocator interface to the caller.
    return pAlloc->QueryInterface(IID_IMemAllocator, (void**)ppAllocator);
}
```



<span data-ttu-id="7b724-118">Quando o filtro upstream seleciona um alocador, ele chama o método [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) do pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="7b724-118">When the upstream filter selects an allocator, it calls the input pin's [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) method.</span></span> <span data-ttu-id="7b724-119">Substitua o método [**CBaseInputPin:: NotifyAllocator**](cbaseinputpin-notifyallocator.md) para verificar as propriedades do alocador.</span><span class="sxs-lookup"><span data-stu-id="7b724-119">Override the [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md) method to check the allocator properties.</span></span> <span data-ttu-id="7b724-120">Em alguns casos, o PIN de entrada poderá rejeitar o alocador se ele não for seu alocador personalizado, embora isso possa causar uma falha na conexão inteira do PIN.</span><span class="sxs-lookup"><span data-stu-id="7b724-120">In some cases, the input pin might reject the allocator if it is not your custom allocator, although this may cause the entire pin connection to fail.</span></span>

<span data-ttu-id="7b724-121">**Fornecendo um alocador personalizado para um pino de saída**</span><span class="sxs-lookup"><span data-stu-id="7b724-121">**Providing a Custom Allocator for an Output Pin**</span></span>

<span data-ttu-id="7b724-122">Para fornecer um alocador para um pino de saída, substitua o método [**CBaseOutputPin:: InitAllocator**](cbaseoutputpin-initallocator.md) para criar uma instância do seu alocador:</span><span class="sxs-lookup"><span data-stu-id="7b724-122">To provide an allocator for an output pin, override the [**CBaseOutputPin::InitAllocator**](cbaseoutputpin-initallocator.md) method to create an instance of your allocator:</span></span>


```C++
HRESULT MyOutputPin::InitAllocator(IMemAllocator **ppAllocator)
{
    HRESULT hr = S_OK;
    CMyAllocator *pAlloc = new CMyAllocator(&hr);
    if (!pAlloc)
    {
        return E_OUTOFMEMORY;
    }

    if (FAILED(hr))
    {
        delete pAlloc;
        return hr;
    }

    // Return the IMemAllocator interface.
    return pAlloc->QueryInterface(IID_IMemAllocator, (void**)ppAllocator);
}
```



<span data-ttu-id="7b724-123">Por padrão, a classe [**CBaseOutputPin**](cbaseoutputpin.md) solicita um alocador do PIN de entrada primeiro.</span><span class="sxs-lookup"><span data-stu-id="7b724-123">By default, the [**CBaseOutputPin**](cbaseoutputpin.md) class requests an allocator from the input pin first.</span></span> <span data-ttu-id="7b724-124">Se esse alocador não for adequado, o pino de saída criará seu próprio alocador.</span><span class="sxs-lookup"><span data-stu-id="7b724-124">If that allocator is not suitable, the output pin creates its own allocator.</span></span> <span data-ttu-id="7b724-125">Para forçar a conexão a usar seu alocador personalizado, substitua o método [**CBaseOutputPin::D ecideallocator**](cbaseoutputpin-decideallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="7b724-125">To force the connection to use your custom allocator, override the [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md) method.</span></span> <span data-ttu-id="7b724-126">No entanto, lembre-se de que isso pode impedir que o PIN de saída se conecte a determinados filtros, porque o outro filtro também pode exigir seu próprio alocador personalizado.</span><span class="sxs-lookup"><span data-stu-id="7b724-126">However, be aware that this can prevent your output pin from connecting with certain filters, because the other filter may also require its own custom allocator.</span></span> <span data-ttu-id="7b724-127">Uma terceira opção é alternar a ordem: Tente o seu alocador personalizado primeiro e, em seguida, volte para o alocador do outro filtro.</span><span class="sxs-lookup"><span data-stu-id="7b724-127">A third option is to switch the order: Try your custom allocator first, and then fall back to the other filter's allocator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b724-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7b724-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b724-129">Negociando alocadores</span><span class="sxs-lookup"><span data-stu-id="7b724-129">Negotiating Allocators</span></span>](negotiating-allocators.md)
</dt> </dl>

 

 




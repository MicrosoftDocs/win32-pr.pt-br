---
title: Regras para implementação de QueryInterface
description: Regras para implementação de QueryInterface
ms.assetid: 6db17ed8-06e4-4bae-bc26-113176cc7e0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e40c743d5306e7dae79bd55ec2c43c01afe742
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105793301"
---
# <a name="rules-for-implementing-queryinterface"></a><span data-ttu-id="67b94-103">Regras para implementação de QueryInterface</span><span class="sxs-lookup"><span data-stu-id="67b94-103">Rules for Implementing QueryInterface</span></span>

<span data-ttu-id="67b94-104">Há três regras principais que regem a implementação do método [**IUnknown:: QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) em um objeto com:</span><span class="sxs-lookup"><span data-stu-id="67b94-104">There are three main rules that govern implementing the [**IUnknown::QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) method on a COM object:</span></span>

-   <span data-ttu-id="67b94-105">Os objetos devem ter identidade.</span><span class="sxs-lookup"><span data-stu-id="67b94-105">Objects must have identity.</span></span>
-   <span data-ttu-id="67b94-106">O conjunto de interfaces em uma instância de objeto deve ser estático.</span><span class="sxs-lookup"><span data-stu-id="67b94-106">The set of interfaces on an object instance must be static.</span></span>
-   <span data-ttu-id="67b94-107">Deve ser possível consultar com êxito qualquer interface em um objeto de qualquer outra interface.</span><span class="sxs-lookup"><span data-stu-id="67b94-107">It must be possible to query successfully for any interface on an object from any other interface.</span></span>

## <a name="objects-must-have-identity"></a><span data-ttu-id="67b94-108">Os objetos devem ter identidade</span><span class="sxs-lookup"><span data-stu-id="67b94-108">Objects Must Have Identity</span></span>

<span data-ttu-id="67b94-109">Para qualquer instância de objeto, uma chamada para [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) com a IID \_ IUnknown sempre deve retornar o mesmo valor de ponteiro físico.</span><span class="sxs-lookup"><span data-stu-id="67b94-109">For any given object instance, a call to [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) with IID\_IUnknown must always return the same physical pointer value.</span></span> <span data-ttu-id="67b94-110">Isso permite que você chame **QueryInterface** em duas interfaces e compare os resultados para determinar se eles apontam para a mesma instância de um objeto.</span><span class="sxs-lookup"><span data-stu-id="67b94-110">This allows you to call **QueryInterface** on any two interfaces and compare the results to determine whether they point to the same instance of an object.</span></span>

## <a name="the-set-of-interfaces-on-an-object-instance-must-be-static"></a><span data-ttu-id="67b94-111">O conjunto de interfaces em uma instância de objeto deve ser estático</span><span class="sxs-lookup"><span data-stu-id="67b94-111">The Set of Interfaces on an Object Instance Must Be Static</span></span>

<span data-ttu-id="67b94-112">O conjunto de interfaces acessíveis em um objeto por meio de [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) deve ser estático, não dinâmico.</span><span class="sxs-lookup"><span data-stu-id="67b94-112">The set of interfaces accessible on an object through [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) must be static, not dynamic.</span></span> <span data-ttu-id="67b94-113">Especificamente, se **QueryInterface** retornar S \_ OK para um determinado IID uma vez, ele nunca deve retornar e \_ nointerface em chamadas subsequentes no mesmo objeto; E se **QueryInterface** retornar e \_ nointerface para um determinado IID, as chamadas subsequentes para a mesma IID no mesmo objeto nunca deverão retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="67b94-113">Specifically, if **QueryInterface** returns S\_OK for a given IID once, it must never return E\_NOINTERFACE on subsequent calls on the same object; and if **QueryInterface** returns E\_NOINTERFACE for a given IID, subsequent calls for the same IID on the same object must never return S\_OK.</span></span>

## <a name="it-must-be-possible-to-query-successfully-for-any-interface-on-an-object-from-any-other-interface"></a><span data-ttu-id="67b94-114">Deve ser possível consultar com êxito qualquer interface em um objeto de qualquer outra interface</span><span class="sxs-lookup"><span data-stu-id="67b94-114">It Must Be Possible to Query Successfully for Any Interface on an Object from Any Other Interface</span></span>

<span data-ttu-id="67b94-115">Ou seja, dado o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="67b94-115">That is, given the following code:</span></span>

``` syntax
IA * pA = (some function returning an IA *); 
IB * pB = NULL; 
HRESULT   hr; 
hr = pA->QueryInterface(IID_IB, &pB); 
 
```

<span data-ttu-id="67b94-116">as seguintes regras se aplicam:</span><span class="sxs-lookup"><span data-stu-id="67b94-116">the following rules apply:</span></span>

-   <span data-ttu-id="67b94-117">Se você tiver um ponteiro para uma interface em um objeto, uma chamada como a seguinte para [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) para a mesma interface deverá ter sucesso:</span><span class="sxs-lookup"><span data-stu-id="67b94-117">If you have a pointer to an interface on an object, a call like the following to [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) for that same interface must succeed:</span></span>

    ``` syntax
    pA->QueryInterface(IID_IA, ...) 
     
    ```

-   <span data-ttu-id="67b94-118">Se uma chamada para [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) para um segundo ponteiro de interface for bem sucedido, uma chamada para **QueryInterface** desse ponteiro para a primeira interface também deverá ser bem sucedido.</span><span class="sxs-lookup"><span data-stu-id="67b94-118">If a call to [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) for a second interface pointer succeeds, a call to **QueryInterface** from that pointer for the first interface must also succeed.</span></span> <span data-ttu-id="67b94-119">Se o pB foi obtido com êxito, o seguinte também deve ter êxito:</span><span class="sxs-lookup"><span data-stu-id="67b94-119">If pB was successfully obtained, the following must also succeed:</span></span>

    ``` syntax
    pB->QueryInterface(IID_IA, ...) 
     
    ```

-   <span data-ttu-id="67b94-120">Qualquer interface deve ser capaz de consultar qualquer outra interface em um objeto.</span><span class="sxs-lookup"><span data-stu-id="67b94-120">Any interface must be able to query for any other interface on an object.</span></span> <span data-ttu-id="67b94-121">Se pB obtiver êxito e você consultar com êxito uma terceira interface (IC) usando esse ponteiro, você também deverá ser capaz de consultar com êxito para IC usando o primeiro ponteiro, pA.</span><span class="sxs-lookup"><span data-stu-id="67b94-121">If pB was successfully obtained and you successfully query for a third interface (IC) using that pointer, you must also be able to query successfully for IC using the first pointer, pA.</span></span> <span data-ttu-id="67b94-122">Nesse caso, a sequência a seguir deve ter sucesso:</span><span class="sxs-lookup"><span data-stu-id="67b94-122">In this case, the following sequence must succeed:</span></span>

    ``` syntax
    IC * pC = NULL; 
    hr = pB->QueryInterface(IID_IC, &pC); 
    pA->QueryInterface(IID_IC, ...) 
     
    ```

<span data-ttu-id="67b94-123">Implementações de interface devem manter um contador de referências de ponteiros pendentes para todas as interfaces em um determinado objeto.</span><span class="sxs-lookup"><span data-stu-id="67b94-123">Interface implementations must maintain a counter of outstanding pointer references to all the interfaces on a given object.</span></span> <span data-ttu-id="67b94-124">Você deve usar um **inteiro sem sinal** para o contador.</span><span class="sxs-lookup"><span data-stu-id="67b94-124">You should use an **unsigned integer** for the counter.</span></span>

<span data-ttu-id="67b94-125">Se um cliente precisar saber que os recursos foram liberados, ele deverá usar um método em alguma interface no objeto com semânticas de nível superior antes de chamar [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="67b94-125">If a client needs to know that resources have been freed, it must use a method in some interface on the object with higher-level semantics before calling [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span>

## <a name="related-topics"></a><span data-ttu-id="67b94-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="67b94-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67b94-127">Usando e implementando IUnknown</span><span class="sxs-lookup"><span data-stu-id="67b94-127">Using and Implementing IUnknown</span></span>](using-and-implementing-iunknown.md)
</dt> </dl>

 

 
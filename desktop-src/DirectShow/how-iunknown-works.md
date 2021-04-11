---
description: Como o IUnknown funciona
ms.assetid: 926778a5-e941-4424-8bc0-b50c925fd08b
title: Como o IUnknown funciona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a7549ce892e9c0dd3c82f1229a2440f1b930190
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087251"
---
# <a name="how-iunknown-works"></a><span data-ttu-id="77796-103">Como o IUnknown funciona</span><span class="sxs-lookup"><span data-stu-id="77796-103">How IUnknown Works</span></span>

<span data-ttu-id="77796-104">Os métodos em **IUnknown** permitem que um aplicativo consulte interfaces no componente e gerencie a contagem de referência do componente.</span><span class="sxs-lookup"><span data-stu-id="77796-104">The methods in **IUnknown** enable an application to query for interfaces on the component and manage the component's reference count.</span></span>

<span data-ttu-id="77796-105">**Contagem de referência**</span><span class="sxs-lookup"><span data-stu-id="77796-105">**Reference Count**</span></span>

<span data-ttu-id="77796-106">A contagem de referência é uma variável interna, incrementada no método **AddRef** e decrementada no método **Release** .</span><span class="sxs-lookup"><span data-stu-id="77796-106">The reference count is an internal variable, incremented in the **AddRef** method and decremented in the **Release** method.</span></span> <span data-ttu-id="77796-107">As classes base gerenciam a contagem de referência e sincronizam o acesso à contagem de referência entre vários threads.</span><span class="sxs-lookup"><span data-stu-id="77796-107">The base classes manage the reference count and synchronize access to the reference count among multiple threads.</span></span>

<span data-ttu-id="77796-108">**Consultas de interface**</span><span class="sxs-lookup"><span data-stu-id="77796-108">**Interface Queries**</span></span>

<span data-ttu-id="77796-109">Consultar uma interface também é simples.</span><span class="sxs-lookup"><span data-stu-id="77796-109">Querying for an interface is also straightforward.</span></span> <span data-ttu-id="77796-110">O chamador passa dois parâmetros: um IID (identificador de interface) e o endereço de um ponteiro.</span><span class="sxs-lookup"><span data-stu-id="77796-110">The caller passes two parameters: an interface identifier (IID), and the address of a pointer.</span></span> <span data-ttu-id="77796-111">Se o componente oferecer suporte à interface solicitada, ele definirá o ponteiro para a interface, incrementará sua própria contagem de referência e retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="77796-111">If the component supports the requested interface, it sets the pointer to the interface, increments its own reference count, and returns S\_OK.</span></span> <span data-ttu-id="77796-112">Caso contrário, ele define o ponteiro como **NULL** E retorna e \_ nointerface.</span><span class="sxs-lookup"><span data-stu-id="77796-112">Otherwise, it sets the pointer to **NULL** and returns E\_NOINTERFACE.</span></span> <span data-ttu-id="77796-113">O pseudocódigo a seguir mostra o contorno geral do método **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="77796-113">The following pseudocode shows the general outline of the **QueryInterface** method.</span></span> <span data-ttu-id="77796-114">A agregação de componentes, descrita na próxima seção, apresenta alguma complexidade adicional.</span><span class="sxs-lookup"><span data-stu-id="77796-114">Component aggregation, described in the next section, introduces some additional complexity.</span></span>


```C++
if (IID == IID_IUnknown)
    set pointer to (IUnknown *)this
    AddRef
    return S_OK

else if (IID == IID_ISomeInterface)
    set pointer to (ISomeInterface *)this
    AddRef
    return S_OK

else if ... 

else
    set pointer to NULL
    return E_NOINTERFACE
```



<span data-ttu-id="77796-115">A única diferença entre o método **QueryInterface** de um componente e o método **QueryInterface** de outro é a lista de IIDs que cada componente testa.</span><span class="sxs-lookup"><span data-stu-id="77796-115">The only difference between the **QueryInterface** method of one component and the **QueryInterface** method of another is the list of IIDs that each component tests.</span></span> <span data-ttu-id="77796-116">Para cada interface compatível com o componente, o componente deve testar a IID dessa interface.</span><span class="sxs-lookup"><span data-stu-id="77796-116">For every interface that the component supports, the component must test for the IID of that interface.</span></span>

<span data-ttu-id="77796-117">**Agregação e delegação**</span><span class="sxs-lookup"><span data-stu-id="77796-117">**Aggregation and Delegation**</span></span>

<span data-ttu-id="77796-118">A agregação de componentes deve ser transparente para o chamador.</span><span class="sxs-lookup"><span data-stu-id="77796-118">Component aggregation must be transparent to the caller.</span></span> <span data-ttu-id="77796-119">Portanto, a agregação deve expor uma interface **IUnknown** única, com o componente agregado, desferindo-se à implementação do componente externo.</span><span class="sxs-lookup"><span data-stu-id="77796-119">Therefore, the aggregate must expose a single **IUnknown** interface, with the aggregated component deferring to the outer component's implementation.</span></span> <span data-ttu-id="77796-120">Caso contrário, o chamador veria duas interfaces **IUnknown** diferentes na mesma agregação.</span><span class="sxs-lookup"><span data-stu-id="77796-120">Otherwise, the caller would see two different **IUnknown** interfaces in the same aggregate.</span></span> <span data-ttu-id="77796-121">Se o componente não for agregado, ele usará sua própria implementação.</span><span class="sxs-lookup"><span data-stu-id="77796-121">If the component is not aggregated, it uses its own implementation.</span></span>

<span data-ttu-id="77796-122">Para dar suporte a esse comportamento, o componente deve adicionar um nível de indireção.</span><span class="sxs-lookup"><span data-stu-id="77796-122">To support this behavior, the component must add a level of indirection.</span></span> <span data-ttu-id="77796-123">Um *IUnknown de delegação* delega o trabalho para o local apropriado: para o componente externo, se houver um, ou para a versão interna do componente.</span><span class="sxs-lookup"><span data-stu-id="77796-123">A *delegating IUnknown* delegates the work to the appropriate place: to the outer component, if there is one, or to the component's internal version.</span></span> <span data-ttu-id="77796-124">Um *IUnknown não delegante* faz o trabalho, conforme descrito na seção anterior.</span><span class="sxs-lookup"><span data-stu-id="77796-124">A *nondelegating IUnknown* does the work, as described in the previous section.</span></span>

<span data-ttu-id="77796-125">A versão de delegação é pública e mantém o nome **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="77796-125">The delegating version is public and keeps the name **IUnknown**.</span></span> <span data-ttu-id="77796-126">A versão sem delegação é renomeada como [**INonDelegatingUnknown**](inondelegatingunknown.md).</span><span class="sxs-lookup"><span data-stu-id="77796-126">The nondelegating version is renamed [**INonDelegatingUnknown**](inondelegatingunknown.md).</span></span> <span data-ttu-id="77796-127">Esse nome não faz parte da especificação COM, pois não é uma interface pública.</span><span class="sxs-lookup"><span data-stu-id="77796-127">This name is not part of the COM specification, because it is not a public interface.</span></span>

<span data-ttu-id="77796-128">Quando o cliente cria uma instância do componente, ele chama o método **IClassFactory:: CreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="77796-128">When the client creates an instance of the component, it calls the **IClassFactory::CreateInstance** method.</span></span> <span data-ttu-id="77796-129">Um parâmetro é um ponteiro para a interface **IUnknown** do componente de agregação, ou **NULL** se a nova instância não for agregada.</span><span class="sxs-lookup"><span data-stu-id="77796-129">One parameter is a pointer to the aggregating component's **IUnknown** interface, or **NULL** if the new instance is not aggregated.</span></span> <span data-ttu-id="77796-130">O componente usa esse parâmetro para armazenar uma variável de membro que indica qual interface **IUnknown** usar, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="77796-130">The component uses this parameter to store a member variable indicating which **IUnknown** interface to use, as shown in the following example:</span></span>


```C++
CMyComponent::CMyComponent(IUnknown *pOuterUnkown)
{
    if (pOuterUnknown == NULL)
        m_pUnknown = (IUnknown *)(INonDelegatingUnknown *)this;
    else
        m_pUnknown = pOuterUnknown;

    [ ... more constructor code ... ]
}
```



<span data-ttu-id="77796-131">Cada método na delegação de **IUnknown** chama seu equivalente de não delegação, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="77796-131">Each method in the delegating **IUnknown** calls its nondelegating counterpart, as shown in the following example:</span></span>


```C++
HRESULT QueryInterface(REFIID iid, void **ppv) 
{
    return m_pUnknown->QueryInterface(iid, ppv);
}
```



<span data-ttu-id="77796-132">Pela natureza da delegação, os métodos de delegação parecem idênticos em todos os componentes.</span><span class="sxs-lookup"><span data-stu-id="77796-132">By the nature of delegation, the delegating methods look identical in every component.</span></span> <span data-ttu-id="77796-133">Somente as versões que não são de delegação são alteradas.</span><span class="sxs-lookup"><span data-stu-id="77796-133">Only the nondelegating versions change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="77796-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="77796-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77796-135">Como implementar IUnknown</span><span class="sxs-lookup"><span data-stu-id="77796-135">How to Implement IUnknown</span></span>](how-to-implement-iunknown.md)
</dt> </dl>

 

 




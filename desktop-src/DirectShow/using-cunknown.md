---
description: O DirectShow implementa IUnknown em uma classe base chamada CUnknown.
ms.assetid: 1fc74db6-c23a-464f-b9fa-b19d7e8672b7
title: Usando CUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c1758065e8d618bf6ca74b37d98b0a8b5425919
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755133"
---
# <a name="using-cunknown"></a><span data-ttu-id="cc2c3-103">Usando CUnknown</span><span class="sxs-lookup"><span data-stu-id="cc2c3-103">Using CUnknown</span></span>

<span data-ttu-id="cc2c3-104">O DirectShow implementa [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) em uma classe base chamada [**CUnknown**](cunknown.md).</span><span class="sxs-lookup"><span data-stu-id="cc2c3-104">DirectShow implements [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) in a base class called [**CUnknown**](cunknown.md).</span></span> <span data-ttu-id="cc2c3-105">Você pode usar **CUnknown** para derivar outras classes, substituindo somente os métodos que mudam entre os componentes.</span><span class="sxs-lookup"><span data-stu-id="cc2c3-105">You can use **CUnknown** to derive other classes, overriding only the methods that change across components.</span></span> <span data-ttu-id="cc2c3-106">A maioria das outras classes base no DirectShow deriva de **CUnknown**, de modo que seu componente pode herdar diretamente do **CUnknown** ou de outra classe base.</span><span class="sxs-lookup"><span data-stu-id="cc2c3-106">Most of the other base classes in DirectShow derive from **CUnknown**, so your component can inherit directly from **CUnknown** or from another base class.</span></span>

## <a name="inondelegatingunknown"></a><span data-ttu-id="cc2c3-107">INonDelegatingUnknown</span><span class="sxs-lookup"><span data-stu-id="cc2c3-107">INonDelegatingUnknown</span></span>

<span data-ttu-id="cc2c3-108">[**CUnknown**](cunknown.md) implementa [**INonDelegatingUnknown**](inondelegatingunknown.md).</span><span class="sxs-lookup"><span data-stu-id="cc2c3-108">[**CUnknown**](cunknown.md) implements [**INonDelegatingUnknown**](inondelegatingunknown.md).</span></span> <span data-ttu-id="cc2c3-109">Ele gerencia contagens de referência internamente e, na maioria das situações, sua classe derivada pode herdar os dois métodos de contagem de referência sem alteração.</span><span class="sxs-lookup"><span data-stu-id="cc2c3-109">It manages reference counts internally, and in most situations your derived class can inherit the two reference-counting methods with no change.</span></span> <span data-ttu-id="cc2c3-110">Lembre-se de que o **CUnknown** se exclui quando a contagem de referência cai para zero.</span><span class="sxs-lookup"><span data-stu-id="cc2c3-110">Be aware that **CUnknown** deletes itself when the reference count drops to zero.</span></span> <span data-ttu-id="cc2c3-111">Por outro lado, você deve substituir [**CUnknown:: NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md), porque o método na classe base retorna E \_ nointerface se receber qualquer IID diferente de IID \_ IUnknown.</span><span class="sxs-lookup"><span data-stu-id="cc2c3-111">On the other hand, you must override [**CUnknown::NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md), because the method in the base class returns E\_NOINTERFACE if it receives any IID other than IID\_IUnknown.</span></span> <span data-ttu-id="cc2c3-112">Em sua classe derivada, teste para o IIDs de interfaces que você dá suporte, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="cc2c3-112">In your derived class, test for the IIDs of interfaces that you support, as shown in the following example:</span></span>


```C++
STDMETHODIMP NonDelegatingQueryInterface(REFIID riid, void **ppv)
{
    if (riid == IID_ISomeInterface)
    {
        return GetInterface((ISomeInterface*)this, ppv);
    }
    // Default: Call parent class method. 
    // The CUnknown class must be in the inheritance chain.
    return CParentClass::NonDelegatingQueryInterface(riid, ppv);
}
```



<span data-ttu-id="cc2c3-113">A função do utilitário [**GetInterface**](getinterface.md) (consulte [**funções auxiliares com**](com-helper-functions.md)) define o ponteiro, incrementa a contagem de referência de forma segura para thread e retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cc2c3-113">The utility function [**GetInterface**](getinterface.md) (see [**COM Helper Functions**](com-helper-functions.md)) sets the pointer, increments the reference count in a thread-safe way, and returns S\_OK.</span></span> <span data-ttu-id="cc2c3-114">No caso padrão, chame o método da classe base e retorne o resultado.</span><span class="sxs-lookup"><span data-stu-id="cc2c3-114">In the default case, call the base class method and return the result.</span></span> <span data-ttu-id="cc2c3-115">Se você derivar de outra classe base, chame seu método [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="cc2c3-115">If you derive from another base class, call its [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method instead.</span></span> <span data-ttu-id="cc2c3-116">Isso permite que você dê suporte a todas as interfaces às quais a classe pai dá suporte.</span><span class="sxs-lookup"><span data-stu-id="cc2c3-116">This enables you to support all the interfaces that the parent class supports.</span></span>

## <a name="iunknown"></a><span data-ttu-id="cc2c3-117">IUnknown</span><span class="sxs-lookup"><span data-stu-id="cc2c3-117">IUnknown</span></span>

<span data-ttu-id="cc2c3-118">Como mencionado anteriormente, a versão de delegação de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) é a mesma para cada componente, porque não faz nada mais do que invocar a instância correta da versão que não é de delegação.</span><span class="sxs-lookup"><span data-stu-id="cc2c3-118">As mentioned earlier, the delegating version of [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) is the same for every component, because it does nothing more than invoke the correct instance of the nondelegating version.</span></span> <span data-ttu-id="cc2c3-119">Para sua conveniência, o arquivo de cabeçalho combase. h contém uma macro, [**Declare \_ IUnknown**](declare-iunknown.md), que declara os três métodos de delegação como métodos embutidos.</span><span class="sxs-lookup"><span data-stu-id="cc2c3-119">For convenience, the header file Combase.h contains a macro, [**DECLARE\_IUNKNOWN**](declare-iunknown.md), which declares the three delegating methods as inline methods.</span></span> <span data-ttu-id="cc2c3-120">Ele se expande para o código a seguir:</span><span class="sxs-lookup"><span data-stu-id="cc2c3-120">It expands to the following code:</span></span>


```C++
STDMETHODIMP QueryInterface(REFIID riid, void **ppv) {      
    return GetOwner()->QueryInterface(riid,ppv);            
};                                                          
STDMETHODIMP_(ULONG) AddRef() {                             
    return GetOwner()->AddRef();                            
};                                                          
STDMETHODIMP_(ULONG) Release() {                            
    return GetOwner()->Release();                           
};
```



<span data-ttu-id="cc2c3-121">A função do utilitário [**CUnknown:: GetOwner**](cunknown-getowner.md) recupera um ponteiro para a interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) do componente que possui esse componente.</span><span class="sxs-lookup"><span data-stu-id="cc2c3-121">The utility function [**CUnknown::GetOwner**](cunknown-getowner.md) retrieves a pointer to the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the component that owns this component.</span></span> <span data-ttu-id="cc2c3-122">Para um componente agregado, o proprietário é o componente externo.</span><span class="sxs-lookup"><span data-stu-id="cc2c3-122">For an aggregated component, the owner is the outer component.</span></span> <span data-ttu-id="cc2c3-123">Caso contrário, o componente pertence a si mesmo.</span><span class="sxs-lookup"><span data-stu-id="cc2c3-123">Otherwise, the component owns itself.</span></span> <span data-ttu-id="cc2c3-124">Inclua a \_ macro declare IUnknown na seção pública de sua definição de classe.</span><span class="sxs-lookup"><span data-stu-id="cc2c3-124">Include the DECLARE\_IUNKNOWN macro in the public section of your class definition.</span></span>

## <a name="class-constructor"></a><span data-ttu-id="cc2c3-125">Construtor de classe</span><span class="sxs-lookup"><span data-stu-id="cc2c3-125">Class Constructor</span></span>

<span data-ttu-id="cc2c3-126">Seu construtor de classe deve invocar o método de construtor para a classe pai, além de qualquer coisa que ele faça, seja específico para sua classe.</span><span class="sxs-lookup"><span data-stu-id="cc2c3-126">Your class constructor should invoke the constructor method for the parent class, in addition to anything it does that is specific to your class.</span></span> <span data-ttu-id="cc2c3-127">O exemplo a seguir é um método de Construtor típico:</span><span class="sxs-lookup"><span data-stu-id="cc2c3-127">The following example is a typical constructor method:</span></span>


```C++
CMyComponent(TCHAR *tszName, LPUNKNOWN pUnk, HRESULT *phr) 
    : CUnknown(tszName, pUnk, phr)
{ 
    /* Other initializations */ 
};
```



<span data-ttu-id="cc2c3-128">O método usa os parâmetros a seguir, que passa diretamente para o método de construtor [**CUnknown**](cunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="cc2c3-128">The method takes the following parameters, which it passes directly to the [**CUnknown**](cunknown.md) constructor method.</span></span>

-   <span data-ttu-id="cc2c3-129">*tszName* especifica um nome para o componente.</span><span class="sxs-lookup"><span data-stu-id="cc2c3-129">*tszName* specifies a name for the component.</span></span>
-   <span data-ttu-id="cc2c3-130">*punk* é um ponteiro para o [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)de agregação.</span><span class="sxs-lookup"><span data-stu-id="cc2c3-130">*pUnk* is a pointer to the aggregating [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span>
-   <span data-ttu-id="cc2c3-131">*PHR* é um ponteiro para um valor HRESULT, indicando o êxito ou a falha do método.</span><span class="sxs-lookup"><span data-stu-id="cc2c3-131">*pHr* is a pointer to an HRESULT value, indicating the success or failure of the method.</span></span>

## <a name="summary"></a><span data-ttu-id="cc2c3-132">Resumo</span><span class="sxs-lookup"><span data-stu-id="cc2c3-132">Summary</span></span>

<span data-ttu-id="cc2c3-133">O exemplo a seguir mostra uma classe derivada que dá suporte a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e a uma interface hipotética chamada ISomeInterface:</span><span class="sxs-lookup"><span data-stu-id="cc2c3-133">The following example shows a derived class that supports [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) and a hypothetical interface named ISomeInterface:</span></span>


```C++
class CMyComponent : public CUnknown, public ISomeInterface
{
public:

    DECLARE_IUNKNOWN;

    STDMETHODIMP NonDelegatingQueryInterface(REFIID riid, void **ppv)
    {
        if( riid == IID_ISomeInterface )
        {
            return GetInterface((ISomeInterface*)this, ppv);
        }
        return CUnknown::NonDelegatingQueryInterface(riid, ppv);
    }

    CMyComponent(TCHAR *tszName, LPUNKNOWN pUnk, HRESULT *phr) 
        : CUnknown(tszName, pUnk, phr)
    { 
        /* Other initializations */ 
    };

    // More declarations will be added later.
};
```



<span data-ttu-id="cc2c3-134">Este exemplo ilustra os seguintes pontos:</span><span class="sxs-lookup"><span data-stu-id="cc2c3-134">This example illustrates the following points:</span></span>

-   <span data-ttu-id="cc2c3-135">A classe [**CUnknown**](cunknown.md) implementa a interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="cc2c3-135">The [**CUnknown**](cunknown.md) class implements the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="cc2c3-136">O novo componente herda de **CUnknown** e de quaisquer interfaces às quais o componente dá suporte.</span><span class="sxs-lookup"><span data-stu-id="cc2c3-136">The new component inherits from **CUnknown** and from any interfaces that the component supports.</span></span> <span data-ttu-id="cc2c3-137">O componente pode derivar em vez de outra classe base que herda de **CUnknown**.</span><span class="sxs-lookup"><span data-stu-id="cc2c3-137">The component could derive instead from another base class that inherits from **CUnknown**.</span></span>
-   <span data-ttu-id="cc2c3-138">A macro [**Declare \_ IUnknown**](declare-iunknown.md) declara a delegação de métodos [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) como métodos embutidos.</span><span class="sxs-lookup"><span data-stu-id="cc2c3-138">The [**DECLARE\_IUNKNOWN**](declare-iunknown.md) macro declares the delegating [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) methods as inline methods.</span></span>
-   <span data-ttu-id="cc2c3-139">A classe [**CUnknown**](cunknown.md) fornece a implementação para [**INonDelegatingUnknown**](inondelegatingunknown.md).</span><span class="sxs-lookup"><span data-stu-id="cc2c3-139">The [**CUnknown**](cunknown.md) class provides the implementation for [**INonDelegatingUnknown**](inondelegatingunknown.md).</span></span>
-   <span data-ttu-id="cc2c3-140">Para dar suporte a uma interface diferente de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), a classe derivada deve substituir o método [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) e testar o IID da nova interface.</span><span class="sxs-lookup"><span data-stu-id="cc2c3-140">To support an interface other than [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), the derived class must override the [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method and test for the IID of the new interface.</span></span>
-   <span data-ttu-id="cc2c3-141">O construtor de classe invoca o método de construtor para [**CUnknown**](cunknown.md).</span><span class="sxs-lookup"><span data-stu-id="cc2c3-141">The class constructor invokes the constructor method for [**CUnknown**](cunknown.md).</span></span>

<span data-ttu-id="cc2c3-142">A próxima etapa na escrita de um filtro é habilitar um aplicativo para criar novas instâncias do componente.</span><span class="sxs-lookup"><span data-stu-id="cc2c3-142">The next step in writing a filter is to enable an application to create new instances of the component.</span></span> <span data-ttu-id="cc2c3-143">Isso requer uma compreensão das DLLs e de sua relação com as fábricas de classes e métodos de construtor de classes.</span><span class="sxs-lookup"><span data-stu-id="cc2c3-143">This requires an understanding of DLLs and their relation to class factories and class constructor methods.</span></span> <span data-ttu-id="cc2c3-144">Para obter mais informações, consulte [como criar uma DLL de filtro do DirectShow](how-to-create-a-dll.md).</span><span class="sxs-lookup"><span data-stu-id="cc2c3-144">For more information, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc2c3-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cc2c3-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc2c3-146">Como implementar IUnknown</span><span class="sxs-lookup"><span data-stu-id="cc2c3-146">How to Implement IUnknown</span></span>](how-to-implement-iunknown.md)
</dt> </dl>

 

 

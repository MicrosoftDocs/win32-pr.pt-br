---
title: Exemplo para resolver conflitos de nome de função
description: Este tópico descreve como resolver conflitos de nome de função ao criar uma extensão para ADSI.
ms.assetid: 8121f037-3845-44ba-a2cd-8d7f15e0beb2
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, código de exemplo Visual Basic, resolvendo conflitos de nome de função
- resolvendo conflitos de nome de função ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 049f9ce6447bf6d6ead783db3e34f74374333f10
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104294503"
---
# <a name="example-for-resolving-function-name-conflicts"></a><span data-ttu-id="34e6c-105">Exemplo para resolver conflitos de nome de função</span><span class="sxs-lookup"><span data-stu-id="34e6c-105">Example for Resolving Function Name Conflicts</span></span>

<span data-ttu-id="34e6c-106">Considere o seguinte:</span><span class="sxs-lookup"><span data-stu-id="34e6c-106">Consider the following:</span></span>

-   <span data-ttu-id="34e6c-107">IADs0 não dá suporte a Func0.</span><span class="sxs-lookup"><span data-stu-id="34e6c-107">IADs0 does not support Func0.</span></span>
-   <span data-ttu-id="34e6c-108">IADs1 dá suporte a func1 e Func0.</span><span class="sxs-lookup"><span data-stu-id="34e6c-108">IADs1 supports Func1 and Func0.</span></span>
-   <span data-ttu-id="34e6c-109">IADs2 dá suporte a func2 e Func0.</span><span class="sxs-lookup"><span data-stu-id="34e6c-109">IADs2 supports Func2 and Func0.</span></span>

<span data-ttu-id="34e6c-110">Todas as três interfaces são interfaces duplas.</span><span class="sxs-lookup"><span data-stu-id="34e6c-110">All three interfaces are dual interfaces.</span></span>


```C++
IADs0 : IDispatch
{
    OtherFunc();
}

IADs1 : IDispatch
{
    Func0() 
    Func1();
}

IADs2 : IDispatch
{
    Func0()
    Func2();
}
```




```VB
Dim myInf1 as IADs1
 
myInf1.Func1  ' IADs1::Func1 is invoked using direct vtable access 
 
myInf1.Func2  ' IADs2::Func2 is invoked using GetIDsOfNames/Invoke
```



<span data-ttu-id="34e6c-111">Lembre-se de que, embora IADs1 não ofereça suporte a func2, um cliente ADSI reconhece um [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que dá suporte a todas as interfaces duplas e de expedição no modelo.</span><span class="sxs-lookup"><span data-stu-id="34e6c-111">Be aware that even though IADs1 does not support Func2, an ADSI client recognizes one [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that supports all the dual and dispatch interfaces in the model.</span></span> <span data-ttu-id="34e6c-112">Assim, o cliente ADSI pode chamar diretamente func2 usando myInf1. func2 sem resolver qual interface dá suporte a Func2.</span><span class="sxs-lookup"><span data-stu-id="34e6c-112">Thus, the ADSI client can directly call Func2 using myInf1.Func2 without resolving which interface supports Func2.</span></span>


```VB
myInf1.Func2
```



<span data-ttu-id="34e6c-113">IADs1 e IADs2 têm uma função chamada Func0, mas IADs1:: Func0 é invocado diretamente usando o acesso vtable, porque os dois itens a seguir se aplicam ao cliente:</span><span class="sxs-lookup"><span data-stu-id="34e6c-113">Both IADs1 and IADs2 have a function called Func0, but IADs1::Func0 is invoked directly using vtable access, because both of following apply to the client:</span></span>

-   <span data-ttu-id="34e6c-114">O cliente tem um ponteiro para o objeto IADs1 de interface dupla, que tem uma função chamada Func0.</span><span class="sxs-lookup"><span data-stu-id="34e6c-114">The client has a pointer to dual interface IADs1 object, which has a function called Func0.</span></span>
-   <span data-ttu-id="34e6c-115">O Visual Basic dá suporte ao acesso Direct vtable, supondo que esse tipo de dados esteja disponível por meio da biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="34e6c-115">Visual Basic supports direct vtable access, assuming that type of data is available through the type library.</span></span>

<span data-ttu-id="34e6c-116">No próximo exemplo de código, o cliente tem um ponteiro de interface dupla para IADs2 em vez de IADs1.</span><span class="sxs-lookup"><span data-stu-id="34e6c-116">In the next code example, the client has a dual interface pointer to IADs2 instead of IADs1.</span></span> <span data-ttu-id="34e6c-117">Portanto, IADs2:: Func0 é invocado usando o acesso Direct vtable.</span><span class="sxs-lookup"><span data-stu-id="34e6c-117">Therefore, IADs2::Func0 is invoked using direct vtable access.</span></span>


```VB
Dim myInf2 as IADs2
Set myInf2 = myInf1 ' Query for pointer to IADs2 
myInf2.Func0
```



<span data-ttu-id="34e6c-118">Novamente, no próximo exemplo de código, IADs1 e IADs2 têm uma função chamada Func0, mas, aqui, o cliente tem um ponteiro para uma interface dupla, IADs0, que não tem uma função chamada Func0.</span><span class="sxs-lookup"><span data-stu-id="34e6c-118">Again, in the next code example, both IADs1 and IADs2 have a function called Func0, but, here, the client has a pointer to a dual interface, IADs0, which does not have a function called Func0.</span></span> <span data-ttu-id="34e6c-119">Portanto, nenhum acesso Direct vtable pode ser executado.</span><span class="sxs-lookup"><span data-stu-id="34e6c-119">Therefore, no direct vtable access can be performed.</span></span> <span data-ttu-id="34e6c-120">Em vez disso, [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) e [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) são chamados para invocar Func0.</span><span class="sxs-lookup"><span data-stu-id="34e6c-120">Instead, [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) and [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) are called to invoke Func0.</span></span>


```VB
Dim myInfNone as IADs0
Set myInfNone = myInf1    ' The aggregated object that 
   ' supports IADs1 and IADs2.
myInfNone.Func0
```



<span data-ttu-id="34e6c-121">Considere estes dois casos:</span><span class="sxs-lookup"><span data-stu-id="34e6c-121">Consider these two cases:</span></span>

-   <span data-ttu-id="34e6c-122">IADs1 e IADs2 são implementados por dois componentes COM, Ext1 e ext2, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="34e6c-122">IADs1 and IADs2 are implemented by two COM components, Ext1 and Ext2, respectively.</span></span> <span data-ttu-id="34e6c-123">Se Ext1 vier antes de ext2 no registro, IADs1:: Func0 será invocado.</span><span class="sxs-lookup"><span data-stu-id="34e6c-123">If Ext1 comes before Ext2 in the registry, IADs1::Func0 is invoked.</span></span> <span data-ttu-id="34e6c-124">No entanto, se o ext2 vier primeiro no registro, IADs2:: Func0 será invocado.</span><span class="sxs-lookup"><span data-stu-id="34e6c-124">However, if Ext2 comes first in the registry, IADs2::Func0 is invoked.</span></span>
-   <span data-ttu-id="34e6c-125">Se IADs1 e ADs2 forem implementados pelo mesmo objeto de extensão, Func0 será sempre invocado pelos métodos [**IADsExtension::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) e [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) da extensão.</span><span class="sxs-lookup"><span data-stu-id="34e6c-125">If IADs1 and ADs2 are implemented by the same extension object, Func0 is always invoked by the extension's [**IADsExtension::PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) and [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) methods.</span></span>

<span data-ttu-id="34e6c-126">O desenvolvedor de extensão deve determinar como resolver conflitos de funções, ou propriedades, de diferentes interfaces duplas de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que têm o mesmo nome em uma extensão.</span><span class="sxs-lookup"><span data-stu-id="34e6c-126">The extension developer must determine how to resolve conflicts of functions, or properties, of different dual [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interfaces that have the same name in an extension.</span></span> <span data-ttu-id="34e6c-127">A implementação dos métodos [**IADsExtension::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) e [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) deve resolver esse conflito.</span><span class="sxs-lookup"><span data-stu-id="34e6c-127">The implementation of [**IADsExtension::PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) and [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) methods should resolve this conflict.</span></span> <span data-ttu-id="34e6c-128">Por exemplo, se você usar IMyInterface1:: func1 e IMyInterface2:: func1, em que IMyInterface1 e IMyInterface2 são interfaces duplas **IDispatch** com suporte no mesmo objeto de extensão.</span><span class="sxs-lookup"><span data-stu-id="34e6c-128">For example, if you use IMyInterface1::Func1 and IMyInterface2::Func1, where IMyInterface1 and IMyInterface2 are dual **IDispatch** interfaces supported by the same extension object.</span></span> <span data-ttu-id="34e6c-129">Os métodos **PrivateGetIDsOfNames** e **PrivateInvoke** devem determinar qual func1 deve ser sempre chamado.</span><span class="sxs-lookup"><span data-stu-id="34e6c-129">The **PrivateGetIDsOfNames** and **PrivateInvoke** methods must determine which Func1 should always be called.</span></span>

<span data-ttu-id="34e6c-130">O mesmo se aplica a DISPIDs conflitantes em diferentes interfaces dual ou [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="34e6c-130">The same applies to conflicting DISPIDs in different dual or [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interfaces.</span></span>

<span data-ttu-id="34e6c-131">Por exemplo, o DISPID de IMyInterface1:: Y é 2 no arquivo IMyInterface1. odl ou IMyInterface1. idl.</span><span class="sxs-lookup"><span data-stu-id="34e6c-131">For example, the DISPID of IMyInterface1::Y is 2 in the file imyinterface1.odl, or imyinterface1.idl.</span></span> <span data-ttu-id="34e6c-132">O DISPID de IMyInterface2:: X também é 2 em iMyInterface2. odl.</span><span class="sxs-lookup"><span data-stu-id="34e6c-132">The DISPID of IMyInterface2::X is also 2 in iMyInterface2.odl.</span></span> <span data-ttu-id="34e6c-133">[**IADsExtension::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) deve retornar um DispId exclusivo, dentro da própria extensão, para cada, em vez de retornar o mesmo DISPID para ambos.</span><span class="sxs-lookup"><span data-stu-id="34e6c-133">[**IADsExtension::PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) must return a unique DISPID, within the extension itself, for each, instead of returning the same DISPID for both.</span></span>

<span data-ttu-id="34e6c-134">A ADSI resolve o primeiro problema não dá suporte a várias interfaces com nomes de função ou Propriedade conflitantes.</span><span class="sxs-lookup"><span data-stu-id="34e6c-134">ADSI resolves the first problem by not supporting multiple interfaces with conflicting function or property names.</span></span> <span data-ttu-id="34e6c-135">Ele resolve o segundo problema adicionando um exclusivo, que está dentro do mesmo objeto de extensão, o número de interface para os bits não utilizados do DISPID.</span><span class="sxs-lookup"><span data-stu-id="34e6c-135">It resolves the second problem by adding a unique, that is within the same extension object, interface number to the unused bits of the DISPID.</span></span>

 

 
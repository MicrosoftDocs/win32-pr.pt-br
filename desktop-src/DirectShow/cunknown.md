---
description: A classe CUnknown implementa a interface IUnknown. A maioria dos objetos COM Component Object Model (COM) no DirectShow deriva de CUnknown.
ms.assetid: 9711d36b-6987-4fb0-a8df-eba94348dc7b
title: Classe CUnknown (combase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4818a088119f7cba25ce8a470f63cab722998c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759505"
---
# <a name="cunknown-class"></a><span data-ttu-id="61917-104">Classe CUnknown</span><span class="sxs-lookup"><span data-stu-id="61917-104">CUnknown class</span></span>

![hierarquia de classe CUnknown](images/cbase01.png)

<span data-ttu-id="61917-106">A classe **CUnknown** implementa a interface **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="61917-106">The **CUnknown** class implements the **IUnknown** interface.</span></span> <span data-ttu-id="61917-107">A maioria dos objetos COM Component Object Model (COM) no DirectShow deriva de **CUnknown**.</span><span class="sxs-lookup"><span data-stu-id="61917-107">Most Component Object Model (COM) objects in DirectShow derive from **CUnknown**.</span></span>

<span data-ttu-id="61917-108">Se você implementar um objeto COM, talvez queira derivá-lo de **CUnknown**.</span><span class="sxs-lookup"><span data-stu-id="61917-108">If you implement a COM object, you might want to derive it from **CUnknown**.</span></span> <span data-ttu-id="61917-109">A derivação de **CUnknown** fornece uma implementação thread-safe e economiza o problema de implementação de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="61917-109">Deriving from **CUnknown** provides a thread-safe implementation, and saves you the trouble of implementing **IUnknown**.</span></span>

<span data-ttu-id="61917-110">Para obter uma discussão detalhada sobre como usar essa classe base, consulte [como implementar IUnknown](how-to-implement-iunknown.md).</span><span class="sxs-lookup"><span data-stu-id="61917-110">For a detailed discussion of how to use this base class, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span> <span data-ttu-id="61917-111">O seguinte é um breve resumo:</span><span class="sxs-lookup"><span data-stu-id="61917-111">What follows is a brief summary:</span></span>

-   <span data-ttu-id="61917-112">Inclua a macro [**Declare \_ IUnknown**](declare-iunknown.md) na seção pública de sua definição de classe.</span><span class="sxs-lookup"><span data-stu-id="61917-112">Include the [**DECLARE\_IUNKNOWN**](declare-iunknown.md) macro in the public section of your class definition.</span></span> <span data-ttu-id="61917-113">Essa macro declara os três métodos da interface **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="61917-113">This macro declares the three methods of the **IUnknown** interface.</span></span>
-   <span data-ttu-id="61917-114">Substitua o método [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) para dar suporte a interfaces diferentes de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="61917-114">Override the [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method to support interfaces other than **IUnknown**.</span></span> <span data-ttu-id="61917-115">Dentro desse método, chame a função [**GetInterface**](getinterface.md) para recuperar ponteiros de interface.</span><span class="sxs-lookup"><span data-stu-id="61917-115">Within this method, call the [**GetInterface**](getinterface.md) function to retrieve interface pointers.</span></span>
-   <span data-ttu-id="61917-116">Em seu construtor de classe, invoque o método do construtor **CUnknown** .</span><span class="sxs-lookup"><span data-stu-id="61917-116">In your class constructor, invoke the **CUnknown** constructor method.</span></span>



| <span data-ttu-id="61917-117">Variáveis de membro protegido</span><span class="sxs-lookup"><span data-stu-id="61917-117">Protected Member Variables</span></span>                                                  | <span data-ttu-id="61917-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="61917-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="61917-119">**\_cRef m**</span><span class="sxs-lookup"><span data-stu-id="61917-119">**m\_cRef**</span></span>](cunknown-m-cref.md)                                          | <span data-ttu-id="61917-120">Contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="61917-120">Reference count.</span></span>                                                   |
| <span data-ttu-id="61917-121">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="61917-121">Public Methods</span></span>                                                              | <span data-ttu-id="61917-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="61917-122">Description</span></span>                                                        |
| [<span data-ttu-id="61917-123">**CUnknown**</span><span class="sxs-lookup"><span data-stu-id="61917-123">**CUnknown**</span></span>](cunknown-cunknown.md)                                       | <span data-ttu-id="61917-124">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="61917-124">Constructor method.</span></span>                                                |
| [<span data-ttu-id="61917-125">**~ CUnknown**</span><span class="sxs-lookup"><span data-stu-id="61917-125">**~ CUnknown**</span></span>](cunknown--cunknown.md)                                    | <span data-ttu-id="61917-126">Método destruidor.</span><span class="sxs-lookup"><span data-stu-id="61917-126">Destructor method.</span></span> <span data-ttu-id="61917-127">VirtuaisLUNs.</span><span class="sxs-lookup"><span data-stu-id="61917-127">Virtual.</span></span>                                        |
| [<span data-ttu-id="61917-128">**GetOwner**</span><span class="sxs-lookup"><span data-stu-id="61917-128">**GetOwner**</span></span>](cunknown-getowner.md)                                       | <span data-ttu-id="61917-129">Obtém um ponteiro para o **IUnknown** de controle.</span><span class="sxs-lookup"><span data-stu-id="61917-129">Gets a pointer to the controlling **IUnknown**.</span></span>                    |
| <span data-ttu-id="61917-130">Métodos INonDelegatingUnknown</span><span class="sxs-lookup"><span data-stu-id="61917-130">INonDelegatingUnknown Methods</span></span>                                               | <span data-ttu-id="61917-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="61917-131">Description</span></span>                                                        |
| [<span data-ttu-id="61917-132">**NonDelegatingAddRef**</span><span class="sxs-lookup"><span data-stu-id="61917-132">**NonDelegatingAddRef**</span></span>](cunknown-nondelegatingaddref.md)                 | <span data-ttu-id="61917-133">Incrementa a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="61917-133">Increments the reference count.</span></span>                                    |
| [<span data-ttu-id="61917-134">**NonDelegatingQueryInterface**</span><span class="sxs-lookup"><span data-stu-id="61917-134">**NonDelegatingQueryInterface**</span></span>](cunknown-nondelegatingqueryinterface.md) | <span data-ttu-id="61917-135">Recupera um ponteiro de interface e incrementa a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="61917-135">Retrieves an interface pointer and increments the reference count.</span></span> |
| [<span data-ttu-id="61917-136">**NonDelegatingRelease**</span><span class="sxs-lookup"><span data-stu-id="61917-136">**NonDelegatingRelease**</span></span>](cunknown-nondelegatingrelease.md)               | <span data-ttu-id="61917-137">Decrementa a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="61917-137">Decrements the reference count.</span></span>                                    |



 

## <a name="requirements"></a><span data-ttu-id="61917-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61917-138">Requirements</span></span>



| <span data-ttu-id="61917-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="61917-139">Requirement</span></span> | <span data-ttu-id="61917-140">Valor</span><span class="sxs-lookup"><span data-stu-id="61917-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61917-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="61917-141">Header</span></span><br/>  | <dl> <span data-ttu-id="61917-142"><dt>Combase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="61917-142"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="61917-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="61917-143">Library</span></span><br/> | <dl> <span data-ttu-id="61917-144"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="61917-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61917-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="61917-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61917-146">Classes base do DirectShow</span><span class="sxs-lookup"><span data-stu-id="61917-146">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> </dl>

 

 





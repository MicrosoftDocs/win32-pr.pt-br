---
description: O modelo de classe CGenericList que implementa uma lista específica de tipo. Para obter mais informações, consulte CBaseList.
ms.assetid: 69067530-3a7d-4731-8ac6-9d02dbba8440
title: Classe CGenericList (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6de3a2dde8d4549221ef4f13decab167fcf6d560
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752289"
---
# <a name="cgenericlist-class"></a><span data-ttu-id="4b0e5-104">Classe CGenericList</span><span class="sxs-lookup"><span data-stu-id="4b0e5-104">CGenericList class</span></span>

![hierarquia de classe CGenericList](images/list01.png)

<span data-ttu-id="4b0e5-106">O `CGenericList` modelo de classe que implementa uma lista específica de tipo.</span><span class="sxs-lookup"><span data-stu-id="4b0e5-106">The `CGenericList` class template that implements a type-specific list.</span></span> <span data-ttu-id="4b0e5-107">Para obter mais informações, consulte [**CBaseList**](cbaselist.md).</span><span class="sxs-lookup"><span data-stu-id="4b0e5-107">For more information, see [**CBaseList**](cbaselist.md).</span></span>

<span data-ttu-id="4b0e5-108">Para usar este modelo, declare uma variável do tipo `CGenericList` com um argumento de modelo que define o tipo de objeto na lista.</span><span class="sxs-lookup"><span data-stu-id="4b0e5-108">To use this template, declare a variable of type `CGenericList` with a template argument that defines the type of object in the list.</span></span> <span data-ttu-id="4b0e5-109">Por exemplo, a instrução a seguir declara uma lista de objetos [**CBaseFilter**](cbasefilter.md) :</span><span class="sxs-lookup"><span data-stu-id="4b0e5-109">For example, the following statement declares a list of [**CBaseFilter**](cbasefilter.md) objects:</span></span>


```
CGenericList<CBaseFilter> myFilterList("Filters"); 
```



<span data-ttu-id="4b0e5-110">Para sua conveniência, Wxlist. h define os seguintes tipos de lista:</span><span class="sxs-lookup"><span data-stu-id="4b0e5-110">For convenience, Wxlist.h defines the following list types:</span></span>

``` syntax
typedef CGenericList<CBaseObject> CBaseObjectList;
typedef CGenericList<IUnknown> CBaseInterfaceList;
```



| <span data-ttu-id="4b0e5-111">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="4b0e5-111">Public Methods</span></span>                                          | <span data-ttu-id="4b0e5-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="4b0e5-112">Description</span></span>                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="4b0e5-113">**CGenericList**</span><span class="sxs-lookup"><span data-stu-id="4b0e5-113">**CGenericList**</span></span>](cgenericlist-cgenericlist.md)       | <span data-ttu-id="4b0e5-114">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="4b0e5-114">Constructor method.</span></span>                                                      |
| [<span data-ttu-id="4b0e5-115">**~ CGenericList**</span><span class="sxs-lookup"><span data-stu-id="4b0e5-115">**~CGenericList**</span></span>](cgenericlist--cgenericlist.md)     | <span data-ttu-id="4b0e5-116">Método destruidor.</span><span class="sxs-lookup"><span data-stu-id="4b0e5-116">Destructor method.</span></span>                                                       |
| [<span data-ttu-id="4b0e5-117">**GetHeadPosition**</span><span class="sxs-lookup"><span data-stu-id="4b0e5-117">**GetHeadPosition**</span></span>](cgenericlist-getheadposition.md) | <span data-ttu-id="4b0e5-118">Recupera a posição do primeiro item na lista.</span><span class="sxs-lookup"><span data-stu-id="4b0e5-118">Retrieves the position of the first item in the list.</span></span>                    |
| [<span data-ttu-id="4b0e5-119">**GetTailPosition**</span><span class="sxs-lookup"><span data-stu-id="4b0e5-119">**GetTailPosition**</span></span>](cgenericlist-gettailposition.md) | <span data-ttu-id="4b0e5-120">Recupera a posição do último item da lista.</span><span class="sxs-lookup"><span data-stu-id="4b0e5-120">Retrieves the position of the last item of the list.</span></span>                     |
| [<span data-ttu-id="4b0e5-121">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="4b0e5-121">**GetCount**</span></span>](cgenericlist-getcount.md)               | <span data-ttu-id="4b0e5-122">Recupera o número de itens na lista.</span><span class="sxs-lookup"><span data-stu-id="4b0e5-122">Retrieves the number of items in the list.</span></span>                               |
| [<span data-ttu-id="4b0e5-123">**GetNext**</span><span class="sxs-lookup"><span data-stu-id="4b0e5-123">**GetNext**</span></span>](cgenericlist-getnext.md)                 | <span data-ttu-id="4b0e5-124">Recupera o item na posição especificada e avança a posição.</span><span class="sxs-lookup"><span data-stu-id="4b0e5-124">Retrieves the item at the specified position, and advances the position.</span></span> |
| [<span data-ttu-id="4b0e5-125">**Obter**</span><span class="sxs-lookup"><span data-stu-id="4b0e5-125">**Get**</span></span>](cgenericlist-get.md)                         | <span data-ttu-id="4b0e5-126">Recupera o item na posição especificada.</span><span class="sxs-lookup"><span data-stu-id="4b0e5-126">Retrieves the item at the specified position.</span></span>                            |
| [<span data-ttu-id="4b0e5-127">**GetHead**</span><span class="sxs-lookup"><span data-stu-id="4b0e5-127">**GetHead**</span></span>](cgenericlist-gethead.md)                 | <span data-ttu-id="4b0e5-128">Recupera o item no cabeçalho da lista.</span><span class="sxs-lookup"><span data-stu-id="4b0e5-128">Retrieves the item at the head of the list.</span></span>                              |
| [<span data-ttu-id="4b0e5-129">**RemoveHead**</span><span class="sxs-lookup"><span data-stu-id="4b0e5-129">**RemoveHead**</span></span>](cgenericlist-removehead.md)           | <span data-ttu-id="4b0e5-130">Remove o primeiro item da lista.</span><span class="sxs-lookup"><span data-stu-id="4b0e5-130">Removes the first item in the list.</span></span>                                      |
| [<span data-ttu-id="4b0e5-131">**RemoveTail**</span><span class="sxs-lookup"><span data-stu-id="4b0e5-131">**RemoveTail**</span></span>](cgenericlist-removetail.md)           | <span data-ttu-id="4b0e5-132">Remove o último item da lista.</span><span class="sxs-lookup"><span data-stu-id="4b0e5-132">Removes the last item in the list.</span></span>                                       |
| [<span data-ttu-id="4b0e5-133">**Remover**</span><span class="sxs-lookup"><span data-stu-id="4b0e5-133">**Remove**</span></span>](cgenericlist-remove.md)                   | <span data-ttu-id="4b0e5-134">Remove o item na posição especificada.</span><span class="sxs-lookup"><span data-stu-id="4b0e5-134">Removes the item at the specified position.</span></span>                              |
| [<span data-ttu-id="4b0e5-135">**Addantes**</span><span class="sxs-lookup"><span data-stu-id="4b0e5-135">**AddBefore**</span></span>](cgenericlist-addbefore.md)             | <span data-ttu-id="4b0e5-136">Insere um item ou uma lista antes da posição especificada.</span><span class="sxs-lookup"><span data-stu-id="4b0e5-136">Inserts an item or list before the specified position.</span></span>                   |
| [<span data-ttu-id="4b0e5-137">**AddAfter**</span><span class="sxs-lookup"><span data-stu-id="4b0e5-137">**AddAfter**</span></span>](cgenericlist-addafter.md)               | <span data-ttu-id="4b0e5-138">Insere um item ou uma lista após a posição especificada.</span><span class="sxs-lookup"><span data-stu-id="4b0e5-138">Inserts an item or list after the specified position.</span></span>                    |
| [<span data-ttu-id="4b0e5-139">**AddHead**</span><span class="sxs-lookup"><span data-stu-id="4b0e5-139">**AddHead**</span></span>](cgenericlist-addhead.md)                 | <span data-ttu-id="4b0e5-140">Adiciona um item ou lista à frente da lista.</span><span class="sxs-lookup"><span data-stu-id="4b0e5-140">Adds an item or list to the front of the list.</span></span>                           |
| [<span data-ttu-id="4b0e5-141">**Addcaudal**</span><span class="sxs-lookup"><span data-stu-id="4b0e5-141">**AddTail**</span></span>](cgenericlist-addtail.md)                 | <span data-ttu-id="4b0e5-142">Anexa um item ou uma lista ao final da lista.</span><span class="sxs-lookup"><span data-stu-id="4b0e5-142">Appends an item or list to the end of the list.</span></span>                          |
| [<span data-ttu-id="4b0e5-143">**Localizar**</span><span class="sxs-lookup"><span data-stu-id="4b0e5-143">**Find**</span></span>](cgenericlist-find.md)                       | <span data-ttu-id="4b0e5-144">Recupera a primeira posição que contém o item especificado.</span><span class="sxs-lookup"><span data-stu-id="4b0e5-144">Retrieves the first position that holds the specified item.</span></span>              |



 

## <a name="requirements"></a><span data-ttu-id="4b0e5-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b0e5-145">Requirements</span></span>



| <span data-ttu-id="4b0e5-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b0e5-146">Requirement</span></span> | <span data-ttu-id="4b0e5-147">Valor</span><span class="sxs-lookup"><span data-stu-id="4b0e5-147">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b0e5-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4b0e5-148">Header</span></span><br/>  | <dl> <span data-ttu-id="4b0e5-149"><dt>Wxlist. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4b0e5-149"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="4b0e5-150">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4b0e5-150">Library</span></span><br/> | <dl> <span data-ttu-id="4b0e5-151"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="4b0e5-151"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





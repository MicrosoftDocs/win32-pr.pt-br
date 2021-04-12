---
description: Saiba mais sobre o método de construtor para CGenericList. CGenericList (Wxlist. h). Este método usa os parâmetros ' pName ' e ' iItems '.
ms.assetid: 2258ecd6-7594-4ff8-961b-9e5e1ae9ff82
title: Construtor CGenericList. CGenericList (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.CGenericList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 77a3dd932872b9d96c754ac5b1db184dcf99cf03
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104298889"
---
# <a name="cgenericlistcgenericlist-constructor-wxlisth---pname-iitems-parameters"></a><span data-ttu-id="5921a-104">Construtor CGenericList. CGenericList (Wxlist. h)-pName, iItems parâmetros</span><span class="sxs-lookup"><span data-stu-id="5921a-104">CGenericList.CGenericList constructor (Wxlist.h) - pName, iItems parameters</span></span>

<span data-ttu-id="5921a-105">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="5921a-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5921a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5921a-106">Syntax</span></span>


```C++
CGenericList(
   TCHAR *pName,
   INT   iItems,
   BOOL  bLock,
   BOOL  bAlert
);
```



## <a name="parameters"></a><span data-ttu-id="5921a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5921a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5921a-108">*pName*</span><span class="sxs-lookup"><span data-stu-id="5921a-108">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="5921a-109">Ponteiro para o nome da lista.</span><span class="sxs-lookup"><span data-stu-id="5921a-109">Pointer to the name of the list.</span></span>

</dd> <dt>

<span data-ttu-id="5921a-110">*iItems*</span><span class="sxs-lookup"><span data-stu-id="5921a-110">*iItems*</span></span> 
</dt> <dd>

<span data-ttu-id="5921a-111">Tamanho do cache do nó.</span><span class="sxs-lookup"><span data-stu-id="5921a-111">Size of the node cache.</span></span>

</dd> <dt>

<span data-ttu-id="5921a-112">*Impeça*</span><span class="sxs-lookup"><span data-stu-id="5921a-112">*bLock*</span></span> 
</dt> <dd>

<span data-ttu-id="5921a-113">Não usado.</span><span class="sxs-lookup"><span data-stu-id="5921a-113">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="5921a-114">*bAlert*</span><span class="sxs-lookup"><span data-stu-id="5921a-114">*bAlert*</span></span> 
</dt> <dd>

<span data-ttu-id="5921a-115">Não usado.</span><span class="sxs-lookup"><span data-stu-id="5921a-115">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5921a-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="5921a-116">Remarks</span></span>

<span data-ttu-id="5921a-117">Para eficiência, a `CGenericList` classe mantém um cache de nós de lista.</span><span class="sxs-lookup"><span data-stu-id="5921a-117">For efficiency, the `CGenericList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="5921a-118">Se você souber aproximadamente quantos itens a lista manterá, use esta versão do construtor.</span><span class="sxs-lookup"><span data-stu-id="5921a-118">If you know approximately how many items the list will hold, use this version of the constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="5921a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5921a-119">Requirements</span></span>

| <span data-ttu-id="5921a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5921a-120">Requirement</span></span> | <span data-ttu-id="5921a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="5921a-121">Value</span></span> |
|-|-|
| <span data-ttu-id="5921a-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5921a-122">Header</span></span> | <span data-ttu-id="5921a-123">Wxlist. h (incluir fluxos. h)</span><span class="sxs-lookup"><span data-stu-id="5921a-123">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="5921a-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5921a-124">Library</span></span>| <span data-ttu-id="5921a-125">Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração)</span><span class="sxs-lookup"><span data-stu-id="5921a-125">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="5921a-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="5921a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5921a-127">**Classe CGenericList**</span><span class="sxs-lookup"><span data-stu-id="5921a-127">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 





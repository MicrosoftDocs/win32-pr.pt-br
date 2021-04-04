---
description: Saiba mais sobre o método de construtor para CGenericList. CGenericList (Wxlist. h). Esse método usa o parâmetro ' pName '.
ms.assetid: 6311d84d-1723-4607-87f8-7cd2ad2582f3
title: Construtor CGenericList. CGenericList (Wxlist. h)-pName parâmetro
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
ms.openlocfilehash: 4a2aa2347e963839c18d904f2819d50de8d6d9c3
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "103837988"
---
# <a name="cgenericlistcgenericlist-constructor-wxlisth---pname-parameter"></a><span data-ttu-id="16b02-104">Construtor CGenericList. CGenericList (Wxlist. h)-pName parâmetro</span><span class="sxs-lookup"><span data-stu-id="16b02-104">CGenericList.CGenericList constructor (Wxlist.h) - pName parameter</span></span>

<span data-ttu-id="16b02-105">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="16b02-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="16b02-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16b02-106">Syntax</span></span>


```C++
CGenericList(
   TCHAR *pName
);
```



## <a name="parameters"></a><span data-ttu-id="16b02-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="16b02-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16b02-108">*pName*</span><span class="sxs-lookup"><span data-stu-id="16b02-108">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="16b02-109">Ponteiro para o nome da lista.</span><span class="sxs-lookup"><span data-stu-id="16b02-109">Pointer to the name of the list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="16b02-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="16b02-110">Remarks</span></span>

<span data-ttu-id="16b02-111">Para eficiência, a `CGenericList` classe mantém um cache de nós de lista.</span><span class="sxs-lookup"><span data-stu-id="16b02-111">For efficiency, the `CGenericList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="16b02-112">Esta versão do construtor usa um tamanho de cache padrão.</span><span class="sxs-lookup"><span data-stu-id="16b02-112">This version of the constructor uses a default cache size.</span></span>

## <a name="requirements"></a><span data-ttu-id="16b02-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16b02-113">Requirements</span></span>

| <span data-ttu-id="16b02-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="16b02-114">Requirement</span></span> | <span data-ttu-id="16b02-115">Valor</span><span class="sxs-lookup"><span data-stu-id="16b02-115">Value</span></span> |
|-|-|
| <span data-ttu-id="16b02-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="16b02-116">Header</span></span> | <span data-ttu-id="16b02-117">Wxlist. h (incluir fluxos. h)</span><span class="sxs-lookup"><span data-stu-id="16b02-117">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="16b02-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="16b02-118">Library</span></span>| <span data-ttu-id="16b02-119">Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração)</span><span class="sxs-lookup"><span data-stu-id="16b02-119">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="16b02-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="16b02-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16b02-121">**Classe CGenericList**</span><span class="sxs-lookup"><span data-stu-id="16b02-121">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 





---
description: O método addcauda acrescenta uma lista ao final da lista.
ms.assetid: 006cccc5-4fb2-4e3f-9481-5d10c090d24e
title: Método CGenericList. addcauda (Wxlist. h)-parâmetro pList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6695df796e54e85ba32dcd63cce2940e00a0199c
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "105747593"
---
# <a name="cgenericlistaddtail-method-wxlisth---plist-parameter"></a><span data-ttu-id="ad23f-103">Método CGenericList. addcauda (Wxlist. h)-parâmetro pList</span><span class="sxs-lookup"><span data-stu-id="ad23f-103">CGenericList.AddTail method (Wxlist.h) - pList parameter</span></span>

<span data-ttu-id="ad23f-104">O `AddTail` método anexa uma lista ao final da lista.</span><span class="sxs-lookup"><span data-stu-id="ad23f-104">The `AddTail` method appends a list to the end of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad23f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ad23f-105">Syntax</span></span>


```C++
BOOL AddTail(
   CGenericList<OBJECT> pList
);
```



## <a name="parameters"></a><span data-ttu-id="ad23f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ad23f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad23f-107">*pList*</span><span class="sxs-lookup"><span data-stu-id="ad23f-107">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="ad23f-108">Ponteiro para a lista a ser acrescentada.</span><span class="sxs-lookup"><span data-stu-id="ad23f-108">Pointer to the list to append.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad23f-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ad23f-109">Return value</span></span>

<span data-ttu-id="ad23f-110">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="ad23f-110">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad23f-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad23f-111">Requirements</span></span>

| <span data-ttu-id="ad23f-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad23f-112">Requirement</span></span> | <span data-ttu-id="ad23f-113">Valor</span><span class="sxs-lookup"><span data-stu-id="ad23f-113">Value</span></span> |
|-|-|
| <span data-ttu-id="ad23f-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ad23f-114">Header</span></span> | <span data-ttu-id="ad23f-115">Wxlist. h (incluir fluxos. h)</span><span class="sxs-lookup"><span data-stu-id="ad23f-115">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="ad23f-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ad23f-116">Library</span></span>| <span data-ttu-id="ad23f-117">Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração)</span><span class="sxs-lookup"><span data-stu-id="ad23f-117">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="ad23f-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="ad23f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad23f-119">**Classe CGenericList**</span><span class="sxs-lookup"><span data-stu-id="ad23f-119">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 





---
description: O método AddHeadI adiciona um item à frente da lista.
ms.assetid: d83b3c5e-2c6d-4369-a74d-18bf19cfd34d
title: Método CBaseList. AddHeadI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddHeadI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6104b6acae0f22c028f3bad050567f4da34ff0f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754566"
---
# <a name="cbaselistaddheadi-method"></a><span data-ttu-id="640ad-103">Método CBaseList. AddHeadI</span><span class="sxs-lookup"><span data-stu-id="640ad-103">CBaseList.AddHeadI method</span></span>

<span data-ttu-id="640ad-104">O `AddHeadI` método adiciona um item à frente da lista.</span><span class="sxs-lookup"><span data-stu-id="640ad-104">The `AddHeadI` method adds an item to the front of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="640ad-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="640ad-105">Syntax</span></span>


```C++
POSITION AddHeadI(
   void *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="640ad-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="640ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="640ad-107">*pObj*</span><span class="sxs-lookup"><span data-stu-id="640ad-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="640ad-108">Ponteiro para o item.</span><span class="sxs-lookup"><span data-stu-id="640ad-108">Pointer to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="640ad-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="640ad-109">Return value</span></span>

<span data-ttu-id="640ad-110">Retorna um valor de posição que indica a nova posição de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="640ad-110">Returns a POSITION value indicating the new head position.</span></span>

## <a name="remarks"></a><span data-ttu-id="640ad-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="640ad-111">Remarks</span></span>

<span data-ttu-id="640ad-112">Se o método falhar, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="640ad-112">If the method fails, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="640ad-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="640ad-113">Requirements</span></span>



| <span data-ttu-id="640ad-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="640ad-114">Requirement</span></span> | <span data-ttu-id="640ad-115">Valor</span><span class="sxs-lookup"><span data-stu-id="640ad-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="640ad-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="640ad-116">Header</span></span><br/>  | <dl> <span data-ttu-id="640ad-117"><dt>Wxlist. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="640ad-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="640ad-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="640ad-118">Library</span></span><br/> | <dl> <span data-ttu-id="640ad-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="640ad-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="640ad-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="640ad-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="640ad-121">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="640ad-121">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 





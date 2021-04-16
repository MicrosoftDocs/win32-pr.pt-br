---
description: O método GetI recupera o item na posição especificada.
ms.assetid: fc775230-491a-49b6-b631-e7d5b8c82d8c
title: Método CBaseList. GetI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.GetI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2473401aeaee201456b4eede39ffb492f40ee2b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751271"
---
# <a name="cbaselistgeti-method"></a><span data-ttu-id="8caec-103">Método CBaseList. GetI</span><span class="sxs-lookup"><span data-stu-id="8caec-103">CBaseList.GetI method</span></span>

<span data-ttu-id="8caec-104">O `GetI` método recupera o item na posição especificada.</span><span class="sxs-lookup"><span data-stu-id="8caec-104">The `GetI` method retrieves the item at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="8caec-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8caec-105">Syntax</span></span>


```C++
void* GetI(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="8caec-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8caec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8caec-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="8caec-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="8caec-108">Indicador de posição do item a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="8caec-108">Position indicator for the item to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8caec-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8caec-109">Return value</span></span>

<span data-ttu-id="8caec-110">Retorna um ponteiro para o item.</span><span class="sxs-lookup"><span data-stu-id="8caec-110">Returns a pointer to the item.</span></span>

## <a name="remarks"></a><span data-ttu-id="8caec-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="8caec-111">Remarks</span></span>

<span data-ttu-id="8caec-112">Se o *PDV* for **nulo**, o método retornará **NULL**.</span><span class="sxs-lookup"><span data-stu-id="8caec-112">If *pos* is **NULL**, the method returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8caec-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8caec-113">Requirements</span></span>



| <span data-ttu-id="8caec-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8caec-114">Requirement</span></span> | <span data-ttu-id="8caec-115">Valor</span><span class="sxs-lookup"><span data-stu-id="8caec-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8caec-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8caec-116">Header</span></span><br/>  | <dl> <span data-ttu-id="8caec-117"><dt>Wxlist. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8caec-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="8caec-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8caec-118">Library</span></span><br/> | <dl> <span data-ttu-id="8caec-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="8caec-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8caec-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="8caec-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8caec-121">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="8caec-121">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 





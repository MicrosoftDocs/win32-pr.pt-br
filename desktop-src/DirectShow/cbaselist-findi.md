---
description: O método findi recupera a primeira posição que contém o item especificado.
ms.assetid: a95fac19-0f93-4bb4-8e76-0da82745a1d2
title: Método CBaseList. findi (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.FindI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2366f8c4c117b8550d91c84bffafb03393801088
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756647"
---
# <a name="cbaselistfindi-method"></a><span data-ttu-id="61299-103">Método CBaseList. findi</span><span class="sxs-lookup"><span data-stu-id="61299-103">CBaseList.FindI method</span></span>

<span data-ttu-id="61299-104">O `FindI` método recupera a primeira posição que contém o item especificado.</span><span class="sxs-lookup"><span data-stu-id="61299-104">The `FindI` method retrieves the first position that holds the specified item.</span></span>

## <a name="syntax"></a><span data-ttu-id="61299-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61299-105">Syntax</span></span>


```C++
POSITION FindI(
   void *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="61299-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="61299-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61299-107">*pObj*</span><span class="sxs-lookup"><span data-stu-id="61299-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="61299-108">Ponteiro para o item.</span><span class="sxs-lookup"><span data-stu-id="61299-108">Pointer to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61299-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="61299-109">Return value</span></span>

<span data-ttu-id="61299-110">Retorna um valor de posição ou **NULL** se o item não estiver na lista.</span><span class="sxs-lookup"><span data-stu-id="61299-110">Returns a POSITION value, or **NULL** if the item is not in the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="61299-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61299-111">Requirements</span></span>



| <span data-ttu-id="61299-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="61299-112">Requirement</span></span> | <span data-ttu-id="61299-113">Valor</span><span class="sxs-lookup"><span data-stu-id="61299-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61299-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="61299-114">Header</span></span><br/>  | <dl> <span data-ttu-id="61299-115"><dt>Wxlist. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="61299-115"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="61299-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="61299-116">Library</span></span><br/> | <dl> <span data-ttu-id="61299-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="61299-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61299-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="61299-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61299-119">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="61299-119">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 





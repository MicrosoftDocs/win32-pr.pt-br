---
description: O método Find recupera a primeira posição que contém o item especificado.
ms.assetid: 8e2a3e5d-96e6-4f40-8e2a-4dc8c21088cd
title: Método CGenericList. Find (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Find
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a21f16e25d8a2ebba4494a850bc456a7b579f2a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749018"
---
# <a name="cgenericlistfind-method"></a><span data-ttu-id="e81d8-103">Método CGenericList. Find</span><span class="sxs-lookup"><span data-stu-id="e81d8-103">CGenericList.Find method</span></span>

<span data-ttu-id="e81d8-104">O `Find` método recupera a primeira posição que contém o item especificado.</span><span class="sxs-lookup"><span data-stu-id="e81d8-104">The `Find` method retrieves the first position that holds the specified item.</span></span>

## <a name="syntax"></a><span data-ttu-id="e81d8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e81d8-105">Syntax</span></span>


```C++
POSITION Find(
   OBJECT *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="e81d8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e81d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e81d8-107">*pObj*</span><span class="sxs-lookup"><span data-stu-id="e81d8-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="e81d8-108">Ponteiro para um objeto do tipo **Object** (o tipo de modelo).</span><span class="sxs-lookup"><span data-stu-id="e81d8-108">Pointer to an object of type **OBJECT** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e81d8-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e81d8-109">Return value</span></span>

<span data-ttu-id="e81d8-110">Retorna um valor de posição ou **NULL** se o item não estiver na lista.</span><span class="sxs-lookup"><span data-stu-id="e81d8-110">Returns a POSITION value, or **NULL** if the item is not in the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="e81d8-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e81d8-111">Requirements</span></span>



| <span data-ttu-id="e81d8-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="e81d8-112">Requirement</span></span> | <span data-ttu-id="e81d8-113">Valor</span><span class="sxs-lookup"><span data-stu-id="e81d8-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e81d8-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e81d8-114">Header</span></span><br/>  | <dl> <span data-ttu-id="e81d8-115"><dt>Wxlist. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e81d8-115"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="e81d8-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e81d8-116">Library</span></span><br/> | <dl> <span data-ttu-id="e81d8-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e81d8-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e81d8-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="e81d8-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e81d8-119">**Classe CGenericList**</span><span class="sxs-lookup"><span data-stu-id="e81d8-119">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 





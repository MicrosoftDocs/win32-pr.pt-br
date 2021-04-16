---
description: O método Get recupera o item na posição especificada.
ms.assetid: cafa4083-96e6-4ed3-afbc-5828b7f1c5be
title: Método CGenericList. Get (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Get
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 02af7d57d2219e6eb0506a8ab11521b4cf3570eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750481"
---
# <a name="cgenericlistget-method"></a><span data-ttu-id="468b4-103">Método CGenericList. Get</span><span class="sxs-lookup"><span data-stu-id="468b4-103">CGenericList.Get method</span></span>

<span data-ttu-id="468b4-104">O `Get` método recupera o item na posição especificada.</span><span class="sxs-lookup"><span data-stu-id="468b4-104">The `Get` method retrieves the item at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="468b4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="468b4-105">Syntax</span></span>


```C++
OBJECT* Get(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="468b4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="468b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="468b4-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="468b4-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="468b4-108">Indicador de posição do item a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="468b4-108">Position indicator for the item to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="468b4-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="468b4-109">Return value</span></span>

<span data-ttu-id="468b4-110">Retorna um ponteiro para um objeto do tipo **Object** (o tipo de modelo).</span><span class="sxs-lookup"><span data-stu-id="468b4-110">Returns a pointer to an object of type **OBJECT** (the template type).</span></span>

## <a name="remarks"></a><span data-ttu-id="468b4-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="468b4-111">Remarks</span></span>

<span data-ttu-id="468b4-112">Se o *PDV* for **nulo**, o método retornará **NULL**.</span><span class="sxs-lookup"><span data-stu-id="468b4-112">If *pos* is **NULL**, the method returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="468b4-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="468b4-113">Requirements</span></span>



| <span data-ttu-id="468b4-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="468b4-114">Requirement</span></span> | <span data-ttu-id="468b4-115">Valor</span><span class="sxs-lookup"><span data-stu-id="468b4-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="468b4-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="468b4-116">Header</span></span><br/>  | <dl> <span data-ttu-id="468b4-117"><dt>Wxlist. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="468b4-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="468b4-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="468b4-118">Library</span></span><br/> | <dl> <span data-ttu-id="468b4-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="468b4-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="468b4-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="468b4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="468b4-121">**Classe CGenericList**</span><span class="sxs-lookup"><span data-stu-id="468b4-121">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 





---
description: O método anterior recupera a posição anterior na lista.
ms.assetid: 537c3019-373a-4974-a42e-72150da72767
title: Método CBaseList. anterior (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.Prev
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 03c35a89754b27aa67a5bba33ee694433d74c0fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749846"
---
# <a name="cbaselistprev-method"></a><span data-ttu-id="b17bb-103">Método CBaseList. anterior</span><span class="sxs-lookup"><span data-stu-id="b17bb-103">CBaseList.Prev method</span></span>

<span data-ttu-id="b17bb-104">O `Prev` método recupera a posição anterior na lista.</span><span class="sxs-lookup"><span data-stu-id="b17bb-104">The `Prev` method retrieves the previous position in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="b17bb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b17bb-105">Syntax</span></span>


```C++
POSITION Prev(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="b17bb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b17bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b17bb-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="b17bb-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="b17bb-108">Valor da posição.</span><span class="sxs-lookup"><span data-stu-id="b17bb-108">POSITION value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b17bb-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b17bb-109">Return value</span></span>

<span data-ttu-id="b17bb-110">Retorna o indicador de posição anterior à posição especificada no *PDV*.</span><span class="sxs-lookup"><span data-stu-id="b17bb-110">Returns the position indicator that is previous to the position specified in *pos*.</span></span>

## <a name="remarks"></a><span data-ttu-id="b17bb-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b17bb-111">Remarks</span></span>

<span data-ttu-id="b17bb-112">Se *pos* for a primeira posição na lista, o método retornará **NULL**.</span><span class="sxs-lookup"><span data-stu-id="b17bb-112">If *pos* is the first position in the list, the method returns **NULL**.</span></span> <span data-ttu-id="b17bb-113">Se o *PDV* for **nulo**, o método retornará a última posição na lista.</span><span class="sxs-lookup"><span data-stu-id="b17bb-113">If *pos* is **NULL**, the method returns the last position in the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="b17bb-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b17bb-114">Requirements</span></span>



| <span data-ttu-id="b17bb-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b17bb-115">Requirement</span></span> | <span data-ttu-id="b17bb-116">Valor</span><span class="sxs-lookup"><span data-stu-id="b17bb-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b17bb-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b17bb-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b17bb-118"><dt>Wxlist. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b17bb-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b17bb-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b17bb-119">Library</span></span><br/> | <dl> <span data-ttu-id="b17bb-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b17bb-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b17bb-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="b17bb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b17bb-122">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="b17bb-122">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 





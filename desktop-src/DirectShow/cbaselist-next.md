---
description: O próximo método recupera a próxima posição na lista.
ms.assetid: ba9753b0-c82e-4772-84a7-e9982de3b8ad
title: Método CBaseList. Next (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f8a09ec91191437fbfb851ce92824b118a5440ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769248"
---
# <a name="cbaselistnext-method"></a><span data-ttu-id="3e274-103">Método CBaseList. Next</span><span class="sxs-lookup"><span data-stu-id="3e274-103">CBaseList.Next method</span></span>

<span data-ttu-id="3e274-104">O `Next` método recupera a próxima posição na lista.</span><span class="sxs-lookup"><span data-stu-id="3e274-104">The `Next` method retrieves the next position in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e274-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e274-105">Syntax</span></span>


```C++
POSITION Next(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="3e274-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e274-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e274-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="3e274-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="3e274-108">Valor da posição.</span><span class="sxs-lookup"><span data-stu-id="3e274-108">POSITION value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e274-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3e274-109">Return value</span></span>

<span data-ttu-id="3e274-110">Retorna o indicador de posição que segue a posição especificada pelo *PDV*.</span><span class="sxs-lookup"><span data-stu-id="3e274-110">Returns the position indicator that follows the position specified by *pos*.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e274-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e274-111">Remarks</span></span>

<span data-ttu-id="3e274-112">Se *pos* for a última posição na lista, o método retornará **NULL**.</span><span class="sxs-lookup"><span data-stu-id="3e274-112">If *pos* is the last position in the list, the method returns **NULL**.</span></span> <span data-ttu-id="3e274-113">Se o *PDV* for **nulo**, o método retornará a primeira posição na lista.</span><span class="sxs-lookup"><span data-stu-id="3e274-113">If *pos* is **NULL**, the method returns the first position in the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e274-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e274-114">Requirements</span></span>



| <span data-ttu-id="3e274-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e274-115">Requirement</span></span> | <span data-ttu-id="3e274-116">Valor</span><span class="sxs-lookup"><span data-stu-id="3e274-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e274-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3e274-117">Header</span></span><br/>  | <dl> <span data-ttu-id="3e274-118"><dt>Wxlist. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3e274-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="3e274-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3e274-119">Library</span></span><br/> | <dl> <span data-ttu-id="3e274-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="3e274-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e274-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e274-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e274-122">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="3e274-122">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 





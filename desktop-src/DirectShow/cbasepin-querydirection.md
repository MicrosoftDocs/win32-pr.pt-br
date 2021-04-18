---
description: 'O método QueryDirection recupera a direção do PIN (entrada ou saída). Esse método implementa o método IPin:: QueryDirection.'
ms.assetid: c28332dc-5ac4-4c89-98b4-281424f36ba9
title: Método CBasePin. QueryDirection (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryDirection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7e2ebfaa3d12b5f582b4b67014280fa0a0d5299d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780888"
---
# <a name="cbasepinquerydirection-method"></a><span data-ttu-id="f0f5a-104">Método CBasePin. QueryDirection</span><span class="sxs-lookup"><span data-stu-id="f0f5a-104">CBasePin.QueryDirection method</span></span>

<span data-ttu-id="f0f5a-105">O `QueryDirection` método recupera a direção do PIN (entrada ou saída).</span><span class="sxs-lookup"><span data-stu-id="f0f5a-105">The `QueryDirection` method retrieves the direction of the pin (input or output).</span></span> <span data-ttu-id="f0f5a-106">Esse método implementa o método [**IPin:: QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) .</span><span class="sxs-lookup"><span data-stu-id="f0f5a-106">This method implements the [**IPin::QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0f5a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f0f5a-107">Syntax</span></span>


```C++
HRESULT QueryDirection(
   PIN_DIRECTION *pPinDir
);
```



## <a name="parameters"></a><span data-ttu-id="f0f5a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0f5a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0f5a-109">*pPinDir*</span><span class="sxs-lookup"><span data-stu-id="f0f5a-109">*pPinDir*</span></span> 
</dt> <dd>

<span data-ttu-id="f0f5a-110">Ponteiro para uma variável que recebe um membro do tipo enumerado de [**\_ direção de PIN**](/windows/win32/api/strmif/ne-strmif-pin_direction) .</span><span class="sxs-lookup"><span data-stu-id="f0f5a-110">Pointer to a variable that receives a member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0f5a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f0f5a-111">Return value</span></span>

<span data-ttu-id="f0f5a-112">Retorna S \_ OK ou o \_ ponteiro.</span><span class="sxs-lookup"><span data-stu-id="f0f5a-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0f5a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0f5a-113">Requirements</span></span>



| <span data-ttu-id="f0f5a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0f5a-114">Requirement</span></span> | <span data-ttu-id="f0f5a-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f0f5a-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0f5a-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f0f5a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="f0f5a-117"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f0f5a-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f0f5a-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f0f5a-118">Library</span></span><br/> | <dl> <span data-ttu-id="f0f5a-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="f0f5a-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0f5a-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0f5a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0f5a-121">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="f0f5a-121">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 





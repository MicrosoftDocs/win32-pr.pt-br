---
description: Esse operador divide um tempo de referência por um valor.
ms.assetid: fb2e2a4b-dc0b-42e3-86c7-8aa2c60daedc
title: COARefTime. Operator/Method (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator/
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e1e4d7b7adb881ac11988a2d2c46946ff6cddcc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756192"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="f77aa-103">COARefTime. Operator/Method</span><span class="sxs-lookup"><span data-stu-id="f77aa-103">COARefTime.operator/ method</span></span>

<span data-ttu-id="f77aa-104">Esse operador divide um tempo de referência por um valor.</span><span class="sxs-lookup"><span data-stu-id="f77aa-104">This operator divides a reference time by a value.</span></span>

## <a name="syntax"></a><span data-ttu-id="f77aa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f77aa-105">Syntax</span></span>


```C++
COARefTime operator/(
   LONG l
);
```



## <a name="parameters"></a><span data-ttu-id="f77aa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f77aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f77aa-107">*l*</span><span class="sxs-lookup"><span data-stu-id="f77aa-107">*l*</span></span> 
</dt> <dd>

<span data-ttu-id="f77aa-108">Divisor.</span><span class="sxs-lookup"><span data-stu-id="f77aa-108">Divisor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f77aa-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f77aa-109">Return value</span></span>

<span data-ttu-id="f77aa-110">Retorna um novo objeto **COARefTime** igual ao quociente deste objeto e **l**.</span><span class="sxs-lookup"><span data-stu-id="f77aa-110">Returns a new **COARefTime** object equal to the quotient of this object and **l**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f77aa-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f77aa-111">Requirements</span></span>



| <span data-ttu-id="f77aa-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="f77aa-112">Requirement</span></span> | <span data-ttu-id="f77aa-113">Valor</span><span class="sxs-lookup"><span data-stu-id="f77aa-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f77aa-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f77aa-114">Header</span></span><br/>  | <dl> <span data-ttu-id="f77aa-115"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f77aa-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f77aa-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f77aa-116">Library</span></span><br/> | <dl> <span data-ttu-id="f77aa-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="f77aa-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f77aa-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="f77aa-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f77aa-119">**Classe COARefTime**</span><span class="sxs-lookup"><span data-stu-id="f77aa-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 





---
description: Esse operador multiplica um tempo de referência por um valor.
ms.assetid: f575fd41-1d3e-43a6-abf8-8e64093e408e
title: Método COARefTime. Operator * (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator*
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c62a4282f7a43ba3d7ba35daf81530f8b246be32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778615"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="9b07a-103">Método COARefTime. Operator \*</span><span class="sxs-lookup"><span data-stu-id="9b07a-103">COARefTime.operator\* method</span></span>

<span data-ttu-id="9b07a-104">Esse operador multiplica um tempo de referência por um valor.</span><span class="sxs-lookup"><span data-stu-id="9b07a-104">This operator multiplies a reference time by a value.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b07a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9b07a-105">Syntax</span></span>


```C++
COARefTime operator*(
   LONG l
);
```



## <a name="parameters"></a><span data-ttu-id="9b07a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9b07a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b07a-107">*l*</span><span class="sxs-lookup"><span data-stu-id="9b07a-107">*l*</span></span> 
</dt> <dd>

<span data-ttu-id="9b07a-108">Multiplicador.</span><span class="sxs-lookup"><span data-stu-id="9b07a-108">Multiplier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b07a-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9b07a-109">Return value</span></span>

<span data-ttu-id="9b07a-110">Retorna um novo objeto **COARefTime** igual ao produto deste objeto e **l**.</span><span class="sxs-lookup"><span data-stu-id="9b07a-110">Returns a new **COARefTime** object equal to the product of this object and **l**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b07a-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b07a-111">Requirements</span></span>



| <span data-ttu-id="9b07a-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b07a-112">Requirement</span></span> | <span data-ttu-id="9b07a-113">Valor</span><span class="sxs-lookup"><span data-stu-id="9b07a-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b07a-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9b07a-114">Header</span></span><br/>  | <dl> <span data-ttu-id="9b07a-115"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9b07a-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9b07a-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b07a-116">Library</span></span><br/> | <dl> <span data-ttu-id="9b07a-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="9b07a-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b07a-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b07a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b07a-119">**Classe COARefTime**</span><span class="sxs-lookup"><span data-stu-id="9b07a-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 





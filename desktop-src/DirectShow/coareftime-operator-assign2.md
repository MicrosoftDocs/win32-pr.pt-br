---
description: O operador atribui um novo tempo de referência e usa o parâmetro ' RT [REF] '.
ms.assetid: e3a005c0-95d5-41e0-80bb-e70399a50dca
title: COARefTime. Operator = Method (Ctlutil. h)-parâmetro RT [REF]
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bad1e0d7ee63fe9bcfa7fc1664a7349e787d9927
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/19/2021
ms.locfileid: "105775625"
---
# <a name="coareftimeoperator-method-ctlutilh---rt-ref-parameter"></a><span data-ttu-id="5a6c8-103">COARefTime. Operator = Method (Ctlutil. h)-parâmetro RT [REF]</span><span class="sxs-lookup"><span data-stu-id="5a6c8-103">COARefTime.operator= method (Ctlutil.h) - rt [ref] parameter</span></span>

<span data-ttu-id="5a6c8-104">Esse operador atribui um novo tempo de referência.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-104">This operator assigns a new reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a6c8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5a6c8-105">Syntax</span></span>


```C++
COARefTime& operator=(
  [ref] const REFERENCE_TIME &rt
);
```



## <a name="parameters"></a><span data-ttu-id="5a6c8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5a6c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a6c8-107">*RT* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="5a6c8-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="5a6c8-108">Referência a um valor de [**\_ tempo de referência**](reference-time.md) que especifica o novo tempo de referência em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-108">Reference to a [**REFERENCE\_TIME**](reference-time.md) value that specifies the new reference time in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a6c8-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5a6c8-109">Return value</span></span>

<span data-ttu-id="5a6c8-110">Retorna uma referência ao objeto.</span><span class="sxs-lookup"><span data-stu-id="5a6c8-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a6c8-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a6c8-111">Requirements</span></span>

| <span data-ttu-id="5a6c8-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a6c8-112">Requirement</span></span>                    | <span data-ttu-id="5a6c8-113">Valor</span><span class="sxs-lookup"><span data-stu-id="5a6c8-113">Value</span></span>                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a6c8-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5a6c8-114">Header</span></span>  | <span data-ttu-id="5a6c8-115">Ctlutil. h (incluir fluxos. h)</span><span class="sxs-lookup"><span data-stu-id="5a6c8-115">Ctlutil.h (include Streams.h)</span></span>                                                                                   |
| <span data-ttu-id="5a6c8-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5a6c8-116">Library</span></span> | <span data-ttu-id="5a6c8-117">Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração)</span><span class="sxs-lookup"><span data-stu-id="5a6c8-117">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="5a6c8-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a6c8-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a6c8-119">**Classe COARefTime**</span><span class="sxs-lookup"><span data-stu-id="5a6c8-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 





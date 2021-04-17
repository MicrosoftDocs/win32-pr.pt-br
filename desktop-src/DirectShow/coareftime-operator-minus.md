---
description: Esse operador subtrai um tempo de referência de outro.
ms.assetid: 5691cd76-0d25-45c0-bb58-6668abe1db01
title: Método COARefTime. Operator-Method (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator-
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e51ee8aaed69830a498d1d22cebdc3927987f045
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811324"
---
# <a name="coareftimeoperator--method"></a><span data-ttu-id="d8ad7-103">Método COARefTime. Operator</span><span class="sxs-lookup"><span data-stu-id="d8ad7-103">COARefTime.operator- method</span></span>

<span data-ttu-id="d8ad7-104">Esse operador subtrai um tempo de referência de outro.</span><span class="sxs-lookup"><span data-stu-id="d8ad7-104">This operator subtracts one reference time from another.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8ad7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8ad7-105">Syntax</span></span>


```C++
COARefTime operator-(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="d8ad7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8ad7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8ad7-107">*RT* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="d8ad7-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="d8ad7-108">Referência ao objeto **COARefTime** a ser subtraído.</span><span class="sxs-lookup"><span data-stu-id="d8ad7-108">Reference to the **COARefTime** object to subtract.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8ad7-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d8ad7-109">Return value</span></span>

<span data-ttu-id="d8ad7-110">Retorna um novo objeto **COARefTime** igual à diferença dos tempos de referência.</span><span class="sxs-lookup"><span data-stu-id="d8ad7-110">Returns a new **COARefTime** object equal to the difference of the reference times.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8ad7-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8ad7-111">Requirements</span></span>



| <span data-ttu-id="d8ad7-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8ad7-112">Requirement</span></span> | <span data-ttu-id="d8ad7-113">Valor</span><span class="sxs-lookup"><span data-stu-id="d8ad7-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8ad7-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d8ad7-114">Header</span></span><br/>  | <dl> <span data-ttu-id="d8ad7-115"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d8ad7-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d8ad7-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d8ad7-116">Library</span></span><br/> | <dl> <span data-ttu-id="d8ad7-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d8ad7-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8ad7-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8ad7-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8ad7-119">**Classe COARefTime**</span><span class="sxs-lookup"><span data-stu-id="d8ad7-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 





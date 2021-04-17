---
description: Esse operador testa a igualdade entre dois tempos de referência.
ms.assetid: a265f7c6-8334-4bb3-8cb7-c7918ebdf97a
title: Método COARefTime. Operator = = (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator==
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 04b19f7b75be840a293920b36fe5ab63d30520d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782261"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="ebe7b-103">Método COARefTime. Operator = =</span><span class="sxs-lookup"><span data-stu-id="ebe7b-103">COARefTime.operator== method</span></span>

<span data-ttu-id="ebe7b-104">Esse operador testa a igualdade entre dois tempos de referência.</span><span class="sxs-lookup"><span data-stu-id="ebe7b-104">This operator tests for equality between two reference times.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebe7b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ebe7b-105">Syntax</span></span>


```C++
BOOL operator==(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="ebe7b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ebe7b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebe7b-107">*RT* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="ebe7b-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ebe7b-108">Referência ao objeto **COARefTime** a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="ebe7b-108">Reference to the **COARefTime** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebe7b-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ebe7b-109">Return value</span></span>

<span data-ttu-id="ebe7b-110">Retornará **true** se os dois objetos forem iguais.</span><span class="sxs-lookup"><span data-stu-id="ebe7b-110">Returns **TRUE** if the two objects are equal.</span></span> <span data-ttu-id="ebe7b-111">Caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="ebe7b-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebe7b-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebe7b-112">Requirements</span></span>



| <span data-ttu-id="ebe7b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebe7b-113">Requirement</span></span> | <span data-ttu-id="ebe7b-114">Valor</span><span class="sxs-lookup"><span data-stu-id="ebe7b-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebe7b-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ebe7b-115">Header</span></span><br/>  | <dl> <span data-ttu-id="ebe7b-116"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ebe7b-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ebe7b-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ebe7b-117">Library</span></span><br/> | <dl> <span data-ttu-id="ebe7b-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ebe7b-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebe7b-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="ebe7b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebe7b-120">**Classe COARefTime**</span><span class="sxs-lookup"><span data-stu-id="ebe7b-120">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 





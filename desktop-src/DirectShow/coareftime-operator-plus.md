---
description: Esse operador adiciona dois tempos de referência.
ms.assetid: 4dfc087a-ec4f-4a8a-8bd4-4da9e1699bcd
title: Método COARefTime. Operator + (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator+
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a6f5019c61d4c1baec47652db8842aa5085b675
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759565"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="27702-103">Método COARefTime. Operator +</span><span class="sxs-lookup"><span data-stu-id="27702-103">COARefTime.operator+ method</span></span>

<span data-ttu-id="27702-104">Esse operador adiciona dois tempos de referência.</span><span class="sxs-lookup"><span data-stu-id="27702-104">This operator adds two reference times.</span></span>

## <a name="syntax"></a><span data-ttu-id="27702-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="27702-105">Syntax</span></span>


```C++
COARefTime operator+(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="27702-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="27702-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27702-107">*RT* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="27702-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="27702-108">Referência ao objeto **COARefTime** a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="27702-108">Reference to the **COARefTime** object to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27702-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="27702-109">Return value</span></span>

<span data-ttu-id="27702-110">Retorna um novo objeto **COARefTime** igual à soma dos tempos de referência.</span><span class="sxs-lookup"><span data-stu-id="27702-110">Returns a new **COARefTime** object equal to the sum of the reference times.</span></span>

## <a name="requirements"></a><span data-ttu-id="27702-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27702-111">Requirements</span></span>



| <span data-ttu-id="27702-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="27702-112">Requirement</span></span> | <span data-ttu-id="27702-113">Valor</span><span class="sxs-lookup"><span data-stu-id="27702-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27702-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="27702-114">Header</span></span><br/>  | <dl> <span data-ttu-id="27702-115"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="27702-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="27702-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="27702-116">Library</span></span><br/> | <dl> <span data-ttu-id="27702-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="27702-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27702-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="27702-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27702-119">**Classe COARefTime**</span><span class="sxs-lookup"><span data-stu-id="27702-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 





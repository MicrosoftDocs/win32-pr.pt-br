---
description: Esse operador adiciona dois tempos de referência e define esse objeto como o resultado.
ms.assetid: 6d29014b-0e31-497e-8326-e3fefc022227
title: Método COARefTime. Operator + = (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator+=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6a03d9e98c3c2f2ca09c3f90f2cb0867d976e02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789706"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="3d086-103">Método COARefTime. Operator + =</span><span class="sxs-lookup"><span data-stu-id="3d086-103">COARefTime.operator+= method</span></span>

<span data-ttu-id="3d086-104">Esse operador adiciona dois tempos de referência e define esse objeto como o resultado.</span><span class="sxs-lookup"><span data-stu-id="3d086-104">This operator adds two reference times, and sets this object to the result.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d086-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3d086-105">Syntax</span></span>


```C++
COARefTime& operator+=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="3d086-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3d086-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d086-107">*RT* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="3d086-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="3d086-108">Referência ao objeto **COARefTime** a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="3d086-108">Reference to the **COARefTime** object to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d086-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3d086-109">Return value</span></span>

<span data-ttu-id="3d086-110">Retorna uma referência ao objeto.</span><span class="sxs-lookup"><span data-stu-id="3d086-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d086-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d086-111">Requirements</span></span>



| <span data-ttu-id="3d086-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d086-112">Requirement</span></span> | <span data-ttu-id="3d086-113">Valor</span><span class="sxs-lookup"><span data-stu-id="3d086-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d086-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3d086-114">Header</span></span><br/>  | <dl> <span data-ttu-id="3d086-115"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3d086-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3d086-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3d086-116">Library</span></span><br/> | <dl> <span data-ttu-id="3d086-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="3d086-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d086-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="3d086-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d086-119">**Classe COARefTime**</span><span class="sxs-lookup"><span data-stu-id="3d086-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 





---
description: Esse operador subtrai um tempo de referência de outro e define esse objeto como o resultado.
ms.assetid: 573b6f6b-7634-4e78-872c-f869b59a75e2
title: COARefTime. Operator-= método (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator-=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 29afc98da01351f63df45997b8cc338e17a1234c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769215"
---
# <a name="coareftimeoperator--method"></a><span data-ttu-id="7b2e1-103">Método COARefTime. Operator-=</span><span class="sxs-lookup"><span data-stu-id="7b2e1-103">COARefTime.operator-= method</span></span>

<span data-ttu-id="7b2e1-104">Esse operador subtrai um tempo de referência de outro e define esse objeto como o resultado.</span><span class="sxs-lookup"><span data-stu-id="7b2e1-104">This operator subtracts one reference time from another, and sets this object to the result.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b2e1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7b2e1-105">Syntax</span></span>


```C++
COARefTime& operator-=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="7b2e1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7b2e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b2e1-107">*RT* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="7b2e1-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="7b2e1-108">Referência ao objeto **COARefTime** a ser subtraído.</span><span class="sxs-lookup"><span data-stu-id="7b2e1-108">Reference to the **COARefTime** object to subtract.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b2e1-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7b2e1-109">Return value</span></span>

<span data-ttu-id="7b2e1-110">Retorna uma referência ao objeto.</span><span class="sxs-lookup"><span data-stu-id="7b2e1-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b2e1-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b2e1-111">Requirements</span></span>



| <span data-ttu-id="7b2e1-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b2e1-112">Requirement</span></span> | <span data-ttu-id="7b2e1-113">Valor</span><span class="sxs-lookup"><span data-stu-id="7b2e1-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b2e1-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7b2e1-114">Header</span></span><br/>  | <dl> <span data-ttu-id="7b2e1-115"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7b2e1-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7b2e1-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7b2e1-116">Library</span></span><br/> | <dl> <span data-ttu-id="7b2e1-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="7b2e1-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b2e1-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b2e1-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b2e1-119">**Classe COARefTime**</span><span class="sxs-lookup"><span data-stu-id="7b2e1-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 





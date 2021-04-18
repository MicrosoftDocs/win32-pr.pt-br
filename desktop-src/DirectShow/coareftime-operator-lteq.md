---
description: Esse operador testa se um tempo de referência é maior ou igual a outro.
ms.assetid: 1182db5b-2d58-4abb-b9ec-f14c3de5a942
title: COARefTime. Operator<= método (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator<=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b4d7c8f212f175760473e5cfe2fdcbd85c4f89f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785360"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="2f03e-103">COARefTime. Operator<= método</span><span class="sxs-lookup"><span data-stu-id="2f03e-103">COARefTime.operator<= method</span></span>

<span data-ttu-id="2f03e-104">Esse operador testa se um tempo de referência é maior ou igual a outro.</span><span class="sxs-lookup"><span data-stu-id="2f03e-104">This operator tests if one reference time is greater than or equal to another.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f03e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2f03e-105">Syntax</span></span>


```C++
BOOL operator<=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="2f03e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f03e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f03e-107">*RT* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="2f03e-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="2f03e-108">Referência ao objeto **COARefTime** a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="2f03e-108">Reference to the **COARefTime** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f03e-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2f03e-109">Return value</span></span>

<span data-ttu-id="2f03e-110">Retornará **true** se esse objeto for maior ou igual a *RT*.</span><span class="sxs-lookup"><span data-stu-id="2f03e-110">Returns **TRUE** if this object is greater than or equal to *rt*.</span></span> <span data-ttu-id="2f03e-111">Caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="2f03e-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f03e-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f03e-112">Requirements</span></span>



| <span data-ttu-id="2f03e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f03e-113">Requirement</span></span> | <span data-ttu-id="2f03e-114">Valor</span><span class="sxs-lookup"><span data-stu-id="2f03e-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f03e-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2f03e-115">Header</span></span><br/>  | <dl> <span data-ttu-id="2f03e-116"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f03e-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2f03e-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2f03e-117">Library</span></span><br/> | <dl> <span data-ttu-id="2f03e-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="2f03e-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f03e-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f03e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f03e-120">**Classe COARefTime**</span><span class="sxs-lookup"><span data-stu-id="2f03e-120">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 





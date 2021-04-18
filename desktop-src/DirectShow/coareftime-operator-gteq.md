---
description: Esse operador testa se um tempo de referência é menor ou igual a outro.
ms.assetid: ae7449b7-d319-4e76-892f-0f9ae63ddf94
title: COARefTime. Operator>= método (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator>=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 69b345f42c854e939c21a028827889a03e0ce735
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789963"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="cbcd8-103">COARefTime. Operator>= método</span><span class="sxs-lookup"><span data-stu-id="cbcd8-103">COARefTime.operator>= method</span></span>

<span data-ttu-id="cbcd8-104">Esse operador testa se um tempo de referência é menor ou igual a outro.</span><span class="sxs-lookup"><span data-stu-id="cbcd8-104">This operator tests if one reference time is less than or equal to another.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbcd8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cbcd8-105">Syntax</span></span>


```C++
BOOL operator>=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="cbcd8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cbcd8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbcd8-107">*RT* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="cbcd8-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="cbcd8-108">Referência ao objeto **COARefTime** a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="cbcd8-108">Reference to the **COARefTime** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbcd8-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cbcd8-109">Return value</span></span>

<span data-ttu-id="cbcd8-110">Retornará **true** se esse objeto for menor ou igual a *RT*.</span><span class="sxs-lookup"><span data-stu-id="cbcd8-110">Returns **TRUE** if this object is less than or equal to *rt*.</span></span> <span data-ttu-id="cbcd8-111">Caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="cbcd8-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbcd8-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbcd8-112">Requirements</span></span>



| <span data-ttu-id="cbcd8-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbcd8-113">Requirement</span></span> | <span data-ttu-id="cbcd8-114">Valor</span><span class="sxs-lookup"><span data-stu-id="cbcd8-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbcd8-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cbcd8-115">Header</span></span><br/>  | <dl> <span data-ttu-id="cbcd8-116"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cbcd8-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cbcd8-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cbcd8-117">Library</span></span><br/> | <dl> <span data-ttu-id="cbcd8-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="cbcd8-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbcd8-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="cbcd8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbcd8-120">**Classe COARefTime**</span><span class="sxs-lookup"><span data-stu-id="cbcd8-120">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 





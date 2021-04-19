---
description: Esse operador testa se um tempo de referência é maior que o outro.
ms.assetid: db281040-9bcf-41fc-95b4-5481ffc5061f
title: Método de>. Operator COARefTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator>
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7c796bd5194c5bdb2dcbe260b803274962f81347
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756618"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="fed62-103">Método de>. Operator COARefTime</span><span class="sxs-lookup"><span data-stu-id="fed62-103">COARefTime.operator> method</span></span>

<span data-ttu-id="fed62-104">Esse operador testa se um tempo de referência é maior que o outro.</span><span class="sxs-lookup"><span data-stu-id="fed62-104">This operator tests if one reference time is greater than another.</span></span>

## <a name="syntax"></a><span data-ttu-id="fed62-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fed62-105">Syntax</span></span>


```C++
BOOL operator>(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="fed62-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fed62-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fed62-107">*RT* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="fed62-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="fed62-108">Referência ao objeto **COARefTime** a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="fed62-108">Reference to the **COARefTime** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fed62-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fed62-109">Return value</span></span>

<span data-ttu-id="fed62-110">Retornará **true** se esse objeto for estritamente maior que *RT*.</span><span class="sxs-lookup"><span data-stu-id="fed62-110">Returns **TRUE** if this object is strictly greater than *rt*.</span></span> <span data-ttu-id="fed62-111">Caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="fed62-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fed62-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fed62-112">Requirements</span></span>



| <span data-ttu-id="fed62-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="fed62-113">Requirement</span></span> | <span data-ttu-id="fed62-114">Valor</span><span class="sxs-lookup"><span data-stu-id="fed62-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed62-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fed62-115">Header</span></span><br/>  | <dl> <span data-ttu-id="fed62-116"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fed62-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fed62-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fed62-117">Library</span></span><br/> | <dl> <span data-ttu-id="fed62-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="fed62-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fed62-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="fed62-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fed62-120">**Classe COARefTime**</span><span class="sxs-lookup"><span data-stu-id="fed62-120">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 





---
description: Esse operador atribui um novo tempo de referência.
ms.assetid: ae6a33ab-f4e0-4f1c-80a0-8a25ee1e9dc5
title: Método COARefTime. Operator = (Ctlutil. h)
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
ms.openlocfilehash: 3f5a051cea555975fd8606c3693d4b7d63cb9ce4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789965"
---
# <a name="coareftimeoperator-method-ctlutilh"></a><span data-ttu-id="66729-103">Método COARefTime. Operator = (Ctlutil. h)</span><span class="sxs-lookup"><span data-stu-id="66729-103">COARefTime.operator= method (Ctlutil.h)</span></span>

<span data-ttu-id="66729-104">Esse operador atribui um novo tempo de referência.</span><span class="sxs-lookup"><span data-stu-id="66729-104">This operator assigns a new reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="66729-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66729-105">Syntax</span></span>


```C++
COARefTime& operator=(
  [ref] const double &rd
);
```



## <a name="parameters"></a><span data-ttu-id="66729-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66729-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66729-107">*área de trabalho* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="66729-107">*rd* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="66729-108">Referência a um valor **duplo** que especifica o novo tempo de referência em segundos.</span><span class="sxs-lookup"><span data-stu-id="66729-108">Reference to a **double** value that specifies the new reference time in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66729-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="66729-109">Return value</span></span>

<span data-ttu-id="66729-110">Retorna uma referência ao objeto.</span><span class="sxs-lookup"><span data-stu-id="66729-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="66729-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66729-111">Requirements</span></span>



| <span data-ttu-id="66729-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="66729-112">Requirement</span></span> | <span data-ttu-id="66729-113">Valor</span><span class="sxs-lookup"><span data-stu-id="66729-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66729-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="66729-114">Header</span></span><br/>  | <dl> <span data-ttu-id="66729-115"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66729-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="66729-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="66729-116">Library</span></span><br/> | <dl> <span data-ttu-id="66729-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="66729-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66729-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="66729-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66729-119">**Classe COARefTime**</span><span class="sxs-lookup"><span data-stu-id="66729-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 





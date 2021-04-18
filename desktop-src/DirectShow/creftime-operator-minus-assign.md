---
description: O operador-= subtrai um tempo de referência de outro.
ms.assetid: 5b0ec72e-87d8-4562-96b1-40e4f5036fd4
title: CReftime. Operator-= método (REFTIME. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator-=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bf66abe11d5c61edbb70118020d882c82b08847
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810239"
---
# <a name="creftimeoperator--method"></a><span data-ttu-id="7b964-103">CReftime. Operator-= método</span><span class="sxs-lookup"><span data-stu-id="7b964-103">CRefTime.operator-= method</span></span>

<span data-ttu-id="7b964-104">O operador-= subtrai um tempo de referência de outro.</span><span class="sxs-lookup"><span data-stu-id="7b964-104">The -= operator subtracts one reference time from another.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b964-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7b964-105">Syntax</span></span>


```C++
CRefTime& operator-=(
  [ref] const CRefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="7b964-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7b964-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b964-107">*RT* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="7b964-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="7b964-108">Referência a um objeto **CRefTime** .</span><span class="sxs-lookup"><span data-stu-id="7b964-108">Reference to a **CRefTime** object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b964-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7b964-109">Return value</span></span>

<span data-ttu-id="7b964-110">Retorna uma referência ao objeto.</span><span class="sxs-lookup"><span data-stu-id="7b964-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b964-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b964-111">Requirements</span></span>



| <span data-ttu-id="7b964-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b964-112">Requirement</span></span> | <span data-ttu-id="7b964-113">Valor</span><span class="sxs-lookup"><span data-stu-id="7b964-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b964-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7b964-114">Header</span></span><br/>  | <dl> <span data-ttu-id="7b964-115"><dt>REFTIME. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7b964-115"><dt>Reftime.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7b964-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7b964-116">Library</span></span><br/> | <dl> <span data-ttu-id="7b964-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="7b964-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





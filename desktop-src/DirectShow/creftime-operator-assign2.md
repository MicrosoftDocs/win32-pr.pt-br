---
description: O operador = atribui um novo tempo de referência.
ms.assetid: 556c2e8a-4726-42ab-949d-9a028ebb1b95
title: CReftime. Operator = método (REFTIME. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8d93a57211c3bc7d787e68f70f36be868ff64449
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758530"
---
# <a name="creftimeoperator-method-reftimeh"></a><span data-ttu-id="380e6-103">CReftime. Operator = método (REFTIME. h)</span><span class="sxs-lookup"><span data-stu-id="380e6-103">CRefTime.operator= method (Reftime.h)</span></span>

<span data-ttu-id="380e6-104">O operador = atribui um novo tempo de referência.</span><span class="sxs-lookup"><span data-stu-id="380e6-104">The = operator assigns a new reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="380e6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="380e6-105">Syntax</span></span>


```C++
CRefTime& operator=(
   const LONGLONG ll
);
```



## <a name="parameters"></a><span data-ttu-id="380e6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="380e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="380e6-107">*precisa*</span><span class="sxs-lookup"><span data-stu-id="380e6-107">*ll*</span></span> 
</dt> <dd>

<span data-ttu-id="380e6-108">Novo tempo de referência, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="380e6-108">New reference time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="380e6-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="380e6-109">Return value</span></span>

<span data-ttu-id="380e6-110">Retorna uma referência ao objeto.</span><span class="sxs-lookup"><span data-stu-id="380e6-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="380e6-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="380e6-111">Requirements</span></span>



| <span data-ttu-id="380e6-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="380e6-112">Requirement</span></span> | <span data-ttu-id="380e6-113">Valor</span><span class="sxs-lookup"><span data-stu-id="380e6-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="380e6-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="380e6-114">Header</span></span><br/>  | <dl> <span data-ttu-id="380e6-115"><dt>REFTIME. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="380e6-115"><dt>Reftime.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="380e6-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="380e6-116">Library</span></span><br/> | <dl> <span data-ttu-id="380e6-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="380e6-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





---
description: O \_ operador tempo de referência () converte o objeto em um tipo de dados de tempo de referência \_ .
ms.assetid: 36f51e03-a458-46e6-9657-977b263c127f
title: Método CReftime. Operator REFERENCE_TIME (REFTIME. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3ceeeb00ba1de4f305f87ef3fe15e70a8d91457
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105775620"
---
# <a name="creftimeoperator-reference_time-method"></a><span data-ttu-id="cb553-103">Método de tempo de referência CReftime. Operator \_</span><span class="sxs-lookup"><span data-stu-id="cb553-103">CRefTime.operator REFERENCE\_TIME method</span></span>

<span data-ttu-id="cb553-104">O `REFERENCE_TIME()` operador converte o objeto em um tipo de dados de [**\_ tempo de referência**](reference-time.md) .</span><span class="sxs-lookup"><span data-stu-id="cb553-104">The `REFERENCE_TIME()` operator casts the object to a [**REFERENCE\_TIME**](reference-time.md) data type.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb553-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cb553-105">Syntax</span></span>


```C++
REFERENCE_TIME operator REFERENCE_TIME() const;
```



## <a name="parameters"></a><span data-ttu-id="cb553-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cb553-106">Parameters</span></span>

<span data-ttu-id="cb553-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="cb553-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cb553-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cb553-108">Return value</span></span>

<span data-ttu-id="cb553-109">Retorna o valor de [**CRefTime:: m \_ time**](creftime-m-time.md).</span><span class="sxs-lookup"><span data-stu-id="cb553-109">Returns the value of [**CRefTime::m\_time**](creftime-m-time.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cb553-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="cb553-110">Remarks</span></span>

<span data-ttu-id="cb553-111">O exemplo a seguir mostra como usar esse operador cast:</span><span class="sxs-lookup"><span data-stu-id="cb553-111">The following example shows how to use this cast operator:</span></span>


```C++
CRefTime cRT(1000);
REFERENCE_TIME rt = (REFERENCE_TIME)cRT;
```



## <a name="requirements"></a><span data-ttu-id="cb553-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb553-112">Requirements</span></span>



| <span data-ttu-id="cb553-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb553-113">Requirement</span></span> | <span data-ttu-id="cb553-114">Valor</span><span class="sxs-lookup"><span data-stu-id="cb553-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb553-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cb553-115">Header</span></span><br/>  | <dl> <span data-ttu-id="cb553-116"><dt>REFTIME. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb553-116"><dt>Reftime.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cb553-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cb553-117">Library</span></span><br/> | <dl> <span data-ttu-id="cb553-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="cb553-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





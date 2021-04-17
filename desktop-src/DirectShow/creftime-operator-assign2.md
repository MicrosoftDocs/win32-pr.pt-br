---
description: O operador = atribui um novo tempo de referência. Esse método usa o parâmetro *ll* .
ms.assetid: 556c2e8a-4726-42ab-949d-9a028ebb1b95
title: CReftime. Operator = método (REFTIME. h)-o parâmetro ll
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
ms.openlocfilehash: d09cb957e06d8b075cff3d831a7f68fbbdf662a8
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187839"
---
# <a name="creftimeoperator-method-reftimeh---ll-parameter"></a><span data-ttu-id="eecdd-104">CReftime. Operator = método (REFTIME. h)-o parâmetro ll</span><span class="sxs-lookup"><span data-stu-id="eecdd-104">CRefTime.operator= method (Reftime.h) - ll parameter</span></span>

<span data-ttu-id="eecdd-105">O operador = atribui um novo tempo de referência.</span><span class="sxs-lookup"><span data-stu-id="eecdd-105">The = operator assigns a new reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="eecdd-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eecdd-106">Syntax</span></span>


```C++
CRefTime& operator=(
   const LONGLONG ll
);
```



## <a name="parameters"></a><span data-ttu-id="eecdd-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eecdd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eecdd-108">*precisa*</span><span class="sxs-lookup"><span data-stu-id="eecdd-108">*ll*</span></span> 
</dt> <dd>

<span data-ttu-id="eecdd-109">Novo tempo de referência, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="eecdd-109">New reference time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eecdd-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eecdd-110">Return value</span></span>

<span data-ttu-id="eecdd-111">Retorna uma referência ao objeto.</span><span class="sxs-lookup"><span data-stu-id="eecdd-111">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="eecdd-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eecdd-112">Requirements</span></span>



| <span data-ttu-id="eecdd-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="eecdd-113">Requirement</span></span> | <span data-ttu-id="eecdd-114">Valor</span><span class="sxs-lookup"><span data-stu-id="eecdd-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eecdd-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eecdd-115">Header</span></span>  | <span data-ttu-id="eecdd-116">REFTIME. h (incluir fluxos. h)</span><span class="sxs-lookup"><span data-stu-id="eecdd-116">Reftime.h (include Streams.h)</span></span>                                                                                   |
| <span data-ttu-id="eecdd-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eecdd-117">Library</span></span> | <span data-ttu-id="eecdd-118">Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração)</span><span class="sxs-lookup"><span data-stu-id="eecdd-118">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |



 

 





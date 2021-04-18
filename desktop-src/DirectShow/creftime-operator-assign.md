---
description: O operador = atribui um novo tempo de referência.
ms.assetid: 0b11e2ea-23dc-4c75-88c6-94215a4b14b6
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
ms.openlocfilehash: b87e6517946c64cb2a60e95912aba423a1880215
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810240"
---
# <a name="creftimeoperator-method-reftimeh"></a><span data-ttu-id="d35fa-103">CReftime. Operator = método (REFTIME. h)</span><span class="sxs-lookup"><span data-stu-id="d35fa-103">CRefTime.operator= method (Reftime.h)</span></span>

<span data-ttu-id="d35fa-104">O operador = atribui um novo tempo de referência.</span><span class="sxs-lookup"><span data-stu-id="d35fa-104">The = operator assigns a new reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="d35fa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d35fa-105">Syntax</span></span>


```C++
CRefTime& operator=(
  [ref] const CRefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="d35fa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d35fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d35fa-107">*RT* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="d35fa-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="d35fa-108">Referência a um objeto **CRefTime** que especifica o novo tempo de referência.</span><span class="sxs-lookup"><span data-stu-id="d35fa-108">Reference to a **CRefTime** object that specifies the new reference time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d35fa-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d35fa-109">Return value</span></span>

<span data-ttu-id="d35fa-110">Retorna uma referência ao objeto.</span><span class="sxs-lookup"><span data-stu-id="d35fa-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="d35fa-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d35fa-111">Requirements</span></span>



| <span data-ttu-id="d35fa-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="d35fa-112">Requirement</span></span> | <span data-ttu-id="d35fa-113">Valor</span><span class="sxs-lookup"><span data-stu-id="d35fa-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d35fa-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d35fa-114">Header</span></span><br/>  | <dl> <span data-ttu-id="d35fa-115"><dt>REFTIME. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d35fa-115"><dt>Reftime.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d35fa-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d35fa-116">Library</span></span><br/> | <dl> <span data-ttu-id="d35fa-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d35fa-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





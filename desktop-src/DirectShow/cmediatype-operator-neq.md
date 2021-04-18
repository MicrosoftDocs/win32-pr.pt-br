---
description: Esse operador testa desigualdade entre objetos CMediaType.
ms.assetid: 9caf4cb9-f049-42e7-abe4-79f8bf0ea542
title: 'CMediaType. CMediaType:: Operator! = método (mtype. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator!=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe3d5b60ed1990423d5ad9375ffdf192da313b8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789708"
---
# <a name="cmediatypecmediatypeoperator-method"></a><span data-ttu-id="c2601-103">Método CMediaType. CMediaType:: Operator! =</span><span class="sxs-lookup"><span data-stu-id="c2601-103">CMediaType.CMediaType::operator!= method</span></span>

<span data-ttu-id="c2601-104">Esse operador testa desigualdade entre objetos [**CMediaType**](cmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="c2601-104">This operator tests for inequality between [**CMediaType**](cmediatype.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2601-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c2601-105">Syntax</span></span>


```C++
BOOL CMediaType::operator!=(
  [ref] const CMediaType &rt
);
```



## <a name="parameters"></a><span data-ttu-id="c2601-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2601-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2601-107">*RT* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="c2601-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c2601-108">Referência ao objeto **CMediaType** a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="c2601-108">Reference to the **CMediaType** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2601-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c2601-109">Return value</span></span>

<span data-ttu-id="c2601-110">Retornará **true** se *RT* não for igual a este objeto.</span><span class="sxs-lookup"><span data-stu-id="c2601-110">Returns **TRUE** if *rt* is not equal to this object.</span></span> <span data-ttu-id="c2601-111">Caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="c2601-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2601-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2601-112">Requirements</span></span>



| <span data-ttu-id="c2601-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2601-113">Requirement</span></span> | <span data-ttu-id="c2601-114">Valor</span><span class="sxs-lookup"><span data-stu-id="c2601-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2601-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c2601-115">Header</span></span><br/>  | <dl> <span data-ttu-id="c2601-116"><dt>Mtype. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c2601-116"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="c2601-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c2601-117">Library</span></span><br/> | <dl> <span data-ttu-id="c2601-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c2601-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2601-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2601-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2601-120">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="c2601-120">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 





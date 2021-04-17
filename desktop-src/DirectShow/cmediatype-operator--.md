---
description: Esse operador testa a igualdade entre os objetos CMediaType.
ms.assetid: d50f3a72-c5e8-44a5-aa0e-b1c40a19fee3
title: 'CMediaType. CMediaType:: Operator = = método (mtype. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator==
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 79631415ce562f1cf3d7251e1f325960f5baa28b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784032"
---
# <a name="cmediatypecmediatypeoperator-method"></a><span data-ttu-id="c26ec-103">Método CMediaType. CMediaType:: Operator = =</span><span class="sxs-lookup"><span data-stu-id="c26ec-103">CMediaType.CMediaType::operator== method</span></span>

<span data-ttu-id="c26ec-104">Esse operador testa a igualdade entre os objetos [**CMediaType**](cmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="c26ec-104">This operator tests for equality between [**CMediaType**](cmediatype.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="c26ec-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c26ec-105">Syntax</span></span>


```C++
BOOL CMediaType::operator==(
  [ref] const CMediaType &rt
);
```



## <a name="parameters"></a><span data-ttu-id="c26ec-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c26ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c26ec-107">*RT* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="c26ec-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c26ec-108">Referência ao objeto **CMediaType** a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="c26ec-108">Reference to the **CMediaType** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c26ec-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c26ec-109">Return value</span></span>

<span data-ttu-id="c26ec-110">Retornará **true** se *RT* for igual a este objeto.</span><span class="sxs-lookup"><span data-stu-id="c26ec-110">Returns **TRUE** if *rt* is equal to this object.</span></span> <span data-ttu-id="c26ec-111">Caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="c26ec-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c26ec-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c26ec-112">Requirements</span></span>



| <span data-ttu-id="c26ec-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c26ec-113">Requirement</span></span> | <span data-ttu-id="c26ec-114">Valor</span><span class="sxs-lookup"><span data-stu-id="c26ec-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c26ec-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c26ec-115">Header</span></span><br/>  | <dl> <span data-ttu-id="c26ec-116"><dt>Mtype. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c26ec-116"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="c26ec-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c26ec-117">Library</span></span><br/> | <dl> <span data-ttu-id="c26ec-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c26ec-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c26ec-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="c26ec-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c26ec-120">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="c26ec-120">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 





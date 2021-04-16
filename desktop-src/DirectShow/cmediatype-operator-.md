---
description: 'O método CMediaType. CMediaType:: Operator = (mtype. h) sobrecarrega o operador de atribuição para copiar um tipo de mídia.'
ms.assetid: 28115548-97a5-426d-97cd-c5e759d8e39e
title: 'CMediaType. CMediaType:: Operator = Method (mtype. h)-parâmetro cmtype'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56eb16c99d867e3cad3be9018c279e3e69f4f122
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/19/2021
ms.locfileid: "105759136"
---
# <a name="cmediatypecmediatypeoperator-method-mtypeh---cmtype-parameter"></a><span data-ttu-id="8acb8-103">CMediaType. CMediaType:: Operator = Method (mtype. h)-parâmetro cmtype</span><span class="sxs-lookup"><span data-stu-id="8acb8-103">CMediaType.CMediaType::operator= method (Mtype.h) - cmtype parameter</span></span>

<span data-ttu-id="8acb8-104">Esse operador sobrecarrega o operador de atribuição para copiar um tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="8acb8-104">This operator overloads the assignment operator to copy a media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="8acb8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8acb8-105">Syntax</span></span>


```C++
CMediaType& CMediaType::operator=(
  [ref] const CMediaType &cmtype
);
```



## <a name="parameters"></a><span data-ttu-id="8acb8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8acb8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8acb8-107">*cmtype* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="8acb8-107">*cmtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="8acb8-108">Referência a um objeto **CMediaType** .</span><span class="sxs-lookup"><span data-stu-id="8acb8-108">Reference to a **CMediaType** object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8acb8-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8acb8-109">Return value</span></span>

<span data-ttu-id="8acb8-110">Retorna uma referência ao objeto.</span><span class="sxs-lookup"><span data-stu-id="8acb8-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="8acb8-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8acb8-111">Requirements</span></span>

| <span data-ttu-id="8acb8-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="8acb8-112">Requirement</span></span>                   | <span data-ttu-id="8acb8-113">Valor</span><span class="sxs-lookup"><span data-stu-id="8acb8-113">Value</span></span>                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8acb8-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8acb8-114">Header</span></span>  | <span data-ttu-id="8acb8-115">Mtype. h (incluir fluxos. h)</span><span class="sxs-lookup"><span data-stu-id="8acb8-115">Mtype.h (include Streams.h)</span></span>                                                                                     |
| <span data-ttu-id="8acb8-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8acb8-116">Library</span></span> | <span data-ttu-id="8acb8-117">Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração)</span><span class="sxs-lookup"><span data-stu-id="8acb8-117">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="8acb8-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="8acb8-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8acb8-119">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="8acb8-119">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 





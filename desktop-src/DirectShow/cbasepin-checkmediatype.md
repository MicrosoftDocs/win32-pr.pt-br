---
description: O método CheckMediaType determina se o PIN aceita um tipo de mídia específico.
ms.assetid: 6a138679-02b7-4ccc-8881-a0d496f84f93
title: Método CBasePin. CheckMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e203851a44a5468567e75ee8c0cc955f8ad0278a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750676"
---
# <a name="cbasepincheckmediatype-method"></a><span data-ttu-id="0d510-103">Método CBasePin. CheckMediaType</span><span class="sxs-lookup"><span data-stu-id="0d510-103">CBasePin.CheckMediaType method</span></span>

<span data-ttu-id="0d510-104">O `CheckMediaType` método determina se o PIN aceita um tipo de mídia específico.</span><span class="sxs-lookup"><span data-stu-id="0d510-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d510-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d510-105">Syntax</span></span>


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pmt
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="0d510-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d510-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d510-107">*PMT*</span><span class="sxs-lookup"><span data-stu-id="0d510-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="0d510-108">Ponteiro para um objeto [**CMediaType**](cmediatype.md) que contém o tipo de mídia proposto.</span><span class="sxs-lookup"><span data-stu-id="0d510-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d510-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0d510-109">Return value</span></span>

<span data-ttu-id="0d510-110">Retornará S \_ OK se o tipo de mídia proposto for aceitável.</span><span class="sxs-lookup"><span data-stu-id="0d510-110">Returns S\_OK if the proposed media type is acceptable.</span></span> <span data-ttu-id="0d510-111">Caso contrário, retorna S \_ false ou um código de erro.</span><span class="sxs-lookup"><span data-stu-id="0d510-111">Otherwise, returns S\_FALSE or an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d510-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d510-112">Remarks</span></span>

<span data-ttu-id="0d510-113">A classe derivada deve substituir esse método virtual puro.</span><span class="sxs-lookup"><span data-stu-id="0d510-113">The derived class must override this pure virtual method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d510-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d510-114">Requirements</span></span>



| <span data-ttu-id="0d510-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d510-115">Requirement</span></span> | <span data-ttu-id="0d510-116">Valor</span><span class="sxs-lookup"><span data-stu-id="0d510-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d510-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0d510-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0d510-118"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0d510-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0d510-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0d510-119">Library</span></span><br/> | <dl> <span data-ttu-id="0d510-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0d510-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d510-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d510-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d510-122">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="0d510-122">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 





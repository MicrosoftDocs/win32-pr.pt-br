---
description: Método CBasePin. CheckMediaType – o método CheckMediaType determina se o PIN aceita um tipo de mídia específico.
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
ms.openlocfilehash: afe39f3a7aac155f3cc87fa6d58f402043861d1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099393"
---
# <a name="cbasepincheckmediatype-method"></a><span data-ttu-id="905cb-103">Método CBasePin. CheckMediaType</span><span class="sxs-lookup"><span data-stu-id="905cb-103">CBasePin.CheckMediaType method</span></span>

<span data-ttu-id="905cb-104">O `CheckMediaType` método determina se o PIN aceita um tipo de mídia específico.</span><span class="sxs-lookup"><span data-stu-id="905cb-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="905cb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="905cb-105">Syntax</span></span>


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pmt
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="905cb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="905cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="905cb-107">*PMT*</span><span class="sxs-lookup"><span data-stu-id="905cb-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="905cb-108">Ponteiro para um objeto [**CMediaType**](cmediatype.md) que contém o tipo de mídia proposto.</span><span class="sxs-lookup"><span data-stu-id="905cb-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="905cb-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="905cb-109">Return value</span></span>

<span data-ttu-id="905cb-110">Retornará S \_ OK se o tipo de mídia proposto for aceitável.</span><span class="sxs-lookup"><span data-stu-id="905cb-110">Returns S\_OK if the proposed media type is acceptable.</span></span> <span data-ttu-id="905cb-111">Caso contrário, retorna S \_ false ou um código de erro.</span><span class="sxs-lookup"><span data-stu-id="905cb-111">Otherwise, returns S\_FALSE or an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="905cb-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="905cb-112">Remarks</span></span>

<span data-ttu-id="905cb-113">A classe derivada deve substituir esse método virtual puro.</span><span class="sxs-lookup"><span data-stu-id="905cb-113">The derived class must override this pure virtual method.</span></span>

## <a name="requirements"></a><span data-ttu-id="905cb-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="905cb-114">Requirements</span></span>



| <span data-ttu-id="905cb-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="905cb-115">Requirement</span></span> | <span data-ttu-id="905cb-116">Valor</span><span class="sxs-lookup"><span data-stu-id="905cb-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="905cb-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="905cb-117">Header</span></span><br/>  | <dl> <span data-ttu-id="905cb-118"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="905cb-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="905cb-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="905cb-119">Library</span></span><br/> | <dl> <span data-ttu-id="905cb-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="905cb-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="905cb-121">Consulte também</span><span class="sxs-lookup"><span data-stu-id="905cb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="905cb-122">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="905cb-122">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 





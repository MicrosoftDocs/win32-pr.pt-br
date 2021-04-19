---
description: 'O método QueryAccept determina se o PIN aceita um tipo de mídia especificado. Esse método implementa o método IPin:: QueryAccept.'
ms.assetid: 7aa25b45-5116-474b-afee-1eddc8b7fd2a
title: Método CBasePin. QueryAccept (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryAccept
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2c4a982f583d1780dbab37d982fd9a54601e141
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753180"
---
# <a name="cbasepinqueryaccept-method"></a><span data-ttu-id="20245-104">Método CBasePin. QueryAccept</span><span class="sxs-lookup"><span data-stu-id="20245-104">CBasePin.QueryAccept method</span></span>

<span data-ttu-id="20245-105">O `QueryAccept` método determina se o PIN aceita um tipo de mídia especificado.</span><span class="sxs-lookup"><span data-stu-id="20245-105">The `QueryAccept` method determines whether the pin accepts a specified media type.</span></span> <span data-ttu-id="20245-106">Esse método implementa o método [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) .</span><span class="sxs-lookup"><span data-stu-id="20245-106">This method implements the [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="20245-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20245-107">Syntax</span></span>


```C++
HRESULT QueryAccept(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="20245-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20245-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20245-109">*PMT*</span><span class="sxs-lookup"><span data-stu-id="20245-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="20245-110">Ponteiro para uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que especifica o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="20245-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20245-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="20245-111">Return value</span></span>

<span data-ttu-id="20245-112">Retornará S \_ OK se o tipo de mídia for aceitável.</span><span class="sxs-lookup"><span data-stu-id="20245-112">Returns S\_OK if the media type is acceptable.</span></span> <span data-ttu-id="20245-113">Caso contrário, retornará S \_ false.</span><span class="sxs-lookup"><span data-stu-id="20245-113">Otherwise, returns S\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="20245-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="20245-114">Remarks</span></span>

<span data-ttu-id="20245-115">Na classe base, esse método delega para o método [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="20245-115">In the base class, this method delegates to the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span> <span data-ttu-id="20245-116">Se **CheckMediaType** falhar, `QueryAccept` retornará S \_ false.</span><span class="sxs-lookup"><span data-stu-id="20245-116">If **CheckMediaType** fails, `QueryAccept` returns S\_FALSE.</span></span>

<span data-ttu-id="20245-117">Esse método não mantém a seção crítica do PIN ([**CBasePin:: m \_ pLock**](cbasepin-m-plock.md)).</span><span class="sxs-lookup"><span data-stu-id="20245-117">This method does not hold the pin's critical section ([**CBasePin::m\_pLock**](cbasepin-m-plock.md)).</span></span> <span data-ttu-id="20245-118">Se a classe derivada modificar dinamicamente o conjunto de tipos de mídia aceitáveis, você deverá substituir esse método para manter a seção crítica.</span><span class="sxs-lookup"><span data-stu-id="20245-118">If your derived class dynamically modifies the set of acceptable media types, you should override this method to hold the critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="20245-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20245-119">Requirements</span></span>



| <span data-ttu-id="20245-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="20245-120">Requirement</span></span> | <span data-ttu-id="20245-121">Valor</span><span class="sxs-lookup"><span data-stu-id="20245-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20245-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="20245-122">Header</span></span><br/>  | <dl> <span data-ttu-id="20245-123"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="20245-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="20245-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="20245-124">Library</span></span><br/> | <dl> <span data-ttu-id="20245-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="20245-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20245-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="20245-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20245-127">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="20245-127">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 





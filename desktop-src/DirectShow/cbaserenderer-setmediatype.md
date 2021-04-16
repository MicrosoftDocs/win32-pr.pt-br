---
description: O método SetMediaType é chamado quando o tipo de mídia do PIN é definido.
ms.assetid: 91d88523-006e-49fe-92f3-92825fbb323b
title: Método CBaseRenderer. SetMediaType (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6ccb364545df514e098811ff6135e0c8cf72a329
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757429"
---
# <a name="cbaserenderersetmediatype-method"></a><span data-ttu-id="3e010-103">Método CBaseRenderer. SetMediaType</span><span class="sxs-lookup"><span data-stu-id="3e010-103">CBaseRenderer.SetMediaType method</span></span>

<span data-ttu-id="3e010-104">O `SetMediaType` método é chamado quando o tipo de mídia do PIN é definido.</span><span class="sxs-lookup"><span data-stu-id="3e010-104">The `SetMediaType` method is called when the pin's media type is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e010-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e010-105">Syntax</span></span>


```C++
virtual HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="3e010-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e010-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e010-107">*PMT*</span><span class="sxs-lookup"><span data-stu-id="3e010-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="3e010-108">Ponteiro para um objeto [**CMediaType**](cmediatype.md) que especifica o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="3e010-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e010-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3e010-109">Return value</span></span>

<span data-ttu-id="3e010-110">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3e010-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e010-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e010-111">Remarks</span></span>

<span data-ttu-id="3e010-112">O pino de entrada chama esse método de seu próprio método [**CRendererInputPin:: SetMediaType**](crendererinputpin-setmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="3e010-112">The input pin calls this method from its own [**CRendererInputPin::SetMediaType**](crendererinputpin-setmediatype.md) method.</span></span> <span data-ttu-id="3e010-113">Esse método não faz nada na classe base.</span><span class="sxs-lookup"><span data-stu-id="3e010-113">This method does nothing in the base class.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e010-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e010-114">Requirements</span></span>



| <span data-ttu-id="3e010-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e010-115">Requirement</span></span> | <span data-ttu-id="3e010-116">Valor</span><span class="sxs-lookup"><span data-stu-id="3e010-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e010-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3e010-117">Header</span></span><br/>  | <dl> <span data-ttu-id="3e010-118"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3e010-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3e010-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3e010-119">Library</span></span><br/> | <dl> <span data-ttu-id="3e010-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="3e010-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e010-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e010-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e010-122">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="3e010-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 





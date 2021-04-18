---
description: 'O método SetMediaType define o tipo de mídia para a conexão. Esse método substitui o método CBasePin:: SetMediaType.'
ms.assetid: b2668bb1-0739-413c-bea8-ec5541acfb3e
title: Método CRendererInputPin. SetMediaType (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca70878f8f6358a3297c22cbb9ac8e49ba0ce310
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753165"
---
# <a name="crendererinputpinsetmediatype-method"></a><span data-ttu-id="d2687-104">Método CRendererInputPin. SetMediaType</span><span class="sxs-lookup"><span data-stu-id="d2687-104">CRendererInputPin.SetMediaType method</span></span>

<span data-ttu-id="d2687-105">O `SetMediaType` método define o tipo de mídia para a conexão.</span><span class="sxs-lookup"><span data-stu-id="d2687-105">The `SetMediaType` method sets the media type for the connection.</span></span> <span data-ttu-id="d2687-106">Esse método substitui o método [**CBasePin:: SetMediaType**](cbasepin-setmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="d2687-106">This method overrides the [**CBasePin::SetMediaType**](cbasepin-setmediatype.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2687-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2687-107">Syntax</span></span>


```C++
HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="d2687-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2687-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2687-109">*PMT*</span><span class="sxs-lookup"><span data-stu-id="d2687-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="d2687-110">Ponteiro para um objeto [**CMediaType**](cmediatype.md) que especifica o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="d2687-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2687-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d2687-111">Return value</span></span>

<span data-ttu-id="d2687-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d2687-112">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2687-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2687-113">Requirements</span></span>



| <span data-ttu-id="d2687-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2687-114">Requirement</span></span> | <span data-ttu-id="d2687-115">Valor</span><span class="sxs-lookup"><span data-stu-id="d2687-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2687-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d2687-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d2687-117"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d2687-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d2687-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d2687-118">Library</span></span><br/> | <dl> <span data-ttu-id="d2687-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d2687-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2687-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2687-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2687-121">**Classe CRendererInputPin**</span><span class="sxs-lookup"><span data-stu-id="d2687-121">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 





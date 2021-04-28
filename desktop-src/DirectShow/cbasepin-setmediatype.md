---
description: Método CBasePin. SetMediaType – o método SetMediaType define o tipo de mídia para a conexão.
ms.assetid: db32b33b-df71-4f46-b53f-d7e647f5f559
title: Método CBasePin. SetMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b61b6179aa6364ebddd940b8853e22d628463e56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095975"
---
# <a name="cbasepinsetmediatype-method"></a><span data-ttu-id="8b75e-103">Método CBasePin. SetMediaType</span><span class="sxs-lookup"><span data-stu-id="8b75e-103">CBasePin.SetMediaType method</span></span>

<span data-ttu-id="8b75e-104">O `SetMediaType` método define o tipo de mídia para a conexão.</span><span class="sxs-lookup"><span data-stu-id="8b75e-104">The `SetMediaType` method sets the media type for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b75e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8b75e-105">Syntax</span></span>


```C++
virtual HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="8b75e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8b75e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b75e-107">*PMT*</span><span class="sxs-lookup"><span data-stu-id="8b75e-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="8b75e-108">Ponteiro para um objeto [**CMediaType**](cmediatype.md) que especifica o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="8b75e-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b75e-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="8b75e-109">Return value</span></span>

<span data-ttu-id="8b75e-110">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8b75e-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b75e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b75e-111">Remarks</span></span>

<span data-ttu-id="8b75e-112">Esse método estabelece o formato para uma conexão de PIN.</span><span class="sxs-lookup"><span data-stu-id="8b75e-112">This method establishes the format for a pin connection.</span></span> <span data-ttu-id="8b75e-113">Antes de chamar esse método, o PIN chama o método [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) para determinar se o tipo de mídia é aceitável.</span><span class="sxs-lookup"><span data-stu-id="8b75e-113">Before calling this method, the pin calls the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method to determine whether the media type is acceptable.</span></span> <span data-ttu-id="8b75e-114">Portanto, o parâmetro *PGTO* é considerado um tipo de mídia aceitável.</span><span class="sxs-lookup"><span data-stu-id="8b75e-114">Therefore, the *pmt* parameter is assumed to be an acceptable media type.</span></span>

<span data-ttu-id="8b75e-115">Na classe base, esse método define a variável de membro [**CBasePin:: m \_ MT**](cbasepin-m-mt.md) e retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8b75e-115">In the base class, this method sets the [**CBasePin::m\_mt**](cbasepin-m-mt.md) member variable and returns S\_OK.</span></span> <span data-ttu-id="8b75e-116">Uma classe derivada pode substituir esse método se precisar de notificação quando o tipo de mídia estiver definido.</span><span class="sxs-lookup"><span data-stu-id="8b75e-116">A derived class can override this method if it requires notification when the media type is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b75e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b75e-117">Requirements</span></span>



| <span data-ttu-id="8b75e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b75e-118">Requirement</span></span> | <span data-ttu-id="8b75e-119">Valor</span><span class="sxs-lookup"><span data-stu-id="8b75e-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b75e-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8b75e-120">Header</span></span><br/>  | <dl> <span data-ttu-id="8b75e-121"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8b75e-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8b75e-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8b75e-122">Library</span></span><br/> | <dl> <span data-ttu-id="8b75e-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="8b75e-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b75e-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="8b75e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b75e-125">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="8b75e-125">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 





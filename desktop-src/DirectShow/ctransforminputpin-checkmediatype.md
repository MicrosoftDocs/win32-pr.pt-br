---
description: Método CTransformInputPin. CheckMediaType – o método CheckMediaType determina se o PIN aceita um tipo de mídia específico.
ms.assetid: e09a4a3e-ac39-4d0e-9e8c-3e8f18057d0d
title: Método CTransformInputPin. CheckMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c775618c9fe30de6171919d5b8bc8a80ea81d3a5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084994"
---
# <a name="ctransforminputpincheckmediatype-method"></a><span data-ttu-id="a514e-103">Método CTransformInputPin. CheckMediaType</span><span class="sxs-lookup"><span data-stu-id="a514e-103">CTransformInputPin.CheckMediaType method</span></span>

<span data-ttu-id="a514e-104">O `CheckMediaType` método determina se o PIN aceita um tipo de mídia específico.</span><span class="sxs-lookup"><span data-stu-id="a514e-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="a514e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a514e-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *mtIn
);
```



## <a name="parameters"></a><span data-ttu-id="a514e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a514e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a514e-107">*mtIn*</span><span class="sxs-lookup"><span data-stu-id="a514e-107">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="a514e-108">Ponteiro para um objeto [**CMediaType**](cmediatype.md) que contém o tipo de mídia proposto.</span><span class="sxs-lookup"><span data-stu-id="a514e-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a514e-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a514e-109">Return value</span></span>

<span data-ttu-id="a514e-110">Retorna S \_ OK ou outro valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a514e-110">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a514e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a514e-111">Remarks</span></span>

<span data-ttu-id="a514e-112">Esse método implementa o método puramente virtual [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="a514e-112">This method implements the pure virtual [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span> <span data-ttu-id="a514e-113">Ele chama o método [**CTransformFilter:: CheckInputType**](ctransformfilter-checkinputtype.md) do filtro, que também é virtual puro.</span><span class="sxs-lookup"><span data-stu-id="a514e-113">It calls the filter's [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method, which is also pure virtual.</span></span> <span data-ttu-id="a514e-114">A classe derivada do filtro deve implementar **CheckInputType** para determinar se um determinado tipo de entrada é aceitável.</span><span class="sxs-lookup"><span data-stu-id="a514e-114">The filter's derived class must implement **CheckInputType** to determine whether a given input type is acceptable.</span></span>

<span data-ttu-id="a514e-115">Se o pino de saída do filtro estiver conectado, esse método também chamará o método [**CTransformFilter:: CheckTransform**](ctransformfilter-checktransform.md) do filtro para determinar se o tipo de entrada é compatível com o tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="a514e-115">If the filter's output pin is connected, this method also calls the filter's [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method to determine whether the input type is compatible with the output type.</span></span> <span data-ttu-id="a514e-116">O método **CheckTransform** também é virtual puro.</span><span class="sxs-lookup"><span data-stu-id="a514e-116">The **CheckTransform** method is pure virtual as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="a514e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a514e-117">Requirements</span></span>



| <span data-ttu-id="a514e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a514e-118">Requirement</span></span> | <span data-ttu-id="a514e-119">Valor</span><span class="sxs-lookup"><span data-stu-id="a514e-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a514e-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a514e-120">Header</span></span><br/>  | <dl> <span data-ttu-id="a514e-121"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a514e-121"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a514e-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a514e-122">Library</span></span><br/> | <dl> <span data-ttu-id="a514e-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a514e-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 





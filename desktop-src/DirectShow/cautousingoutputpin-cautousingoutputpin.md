---
description: Método de construtor. O construtor obtém acesso ao PIN especificado.
ms.assetid: 518d41aa-8361-4769-aa9b-14676b676d6f
title: Construtor CAutoUsingOutputPin. CAutoUsingOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoUsingOutputPin.CAutoUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94bafcdcb6e44a07afdccea382d783c20a9ad2ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756210"
---
# <a name="cautousingoutputpincautousingoutputpin-constructor"></a><span data-ttu-id="93e40-104">Construtor CAutoUsingOutputPin. CAutoUsingOutputPin</span><span class="sxs-lookup"><span data-stu-id="93e40-104">CAutoUsingOutputPin.CAutoUsingOutputPin constructor</span></span>

<span data-ttu-id="93e40-105">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="93e40-105">Constructor method.</span></span> <span data-ttu-id="93e40-106">O construtor obtém acesso ao PIN especificado.</span><span class="sxs-lookup"><span data-stu-id="93e40-106">The constructor obtains access to the specified pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="93e40-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="93e40-107">Syntax</span></span>


```C++
CAutoUsingOutputPin(
   CDynamicOutputPin *pOutputPin,
   HRESULT           *phr
);
```



## <a name="parameters"></a><span data-ttu-id="93e40-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="93e40-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93e40-109">*pOutputPin*</span><span class="sxs-lookup"><span data-stu-id="93e40-109">*pOutputPin*</span></span> 
</dt> <dd>

<span data-ttu-id="93e40-110">Ponteiro para um objeto [**CDynamicOutputPin**](cdynamicoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="93e40-110">Pointer to a [**CDynamicOutputPin**](cdynamicoutputpin.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="93e40-111">*phr*</span><span class="sxs-lookup"><span data-stu-id="93e40-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="93e40-112">Ponteiro para uma variável que contém um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="93e40-112">Pointer to a variable that contains an **HRESULT** value.</span></span> <span data-ttu-id="93e40-113">O valor deve ser S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="93e40-113">The value must be S\_OK.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="93e40-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="93e40-114">Remarks</span></span>

<span data-ttu-id="93e40-115">Quando o método retorna, o valor de *\* PHR* indica o êxito ou a falha do método.</span><span class="sxs-lookup"><span data-stu-id="93e40-115">When the method returns, the value of *\*phr* indicates the success or failure of the method.</span></span>

## <a name="requirements"></a><span data-ttu-id="93e40-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93e40-116">Requirements</span></span>



| <span data-ttu-id="93e40-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="93e40-117">Requirement</span></span> | <span data-ttu-id="93e40-118">Valor</span><span class="sxs-lookup"><span data-stu-id="93e40-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93e40-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="93e40-119">Header</span></span><br/>  | <dl> <span data-ttu-id="93e40-120"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="93e40-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="93e40-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="93e40-121">Library</span></span><br/> | <dl> <span data-ttu-id="93e40-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="93e40-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93e40-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="93e40-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93e40-124">**Classe CAutoUsingOutputPin**</span><span class="sxs-lookup"><span data-stu-id="93e40-124">**CAutoUsingOutputPin Class**</span></span>](cautousingoutputpin-cautousingoutputpin.md)
</dt> </dl>

 

 





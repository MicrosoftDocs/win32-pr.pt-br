---
description: 'O método SetSink define um Gerenciador de qualidade externo. Esse método implementa o método IQualityControl:: SetSink.'
ms.assetid: 714e6839-954e-4231-824d-72a45f270f59
title: Método CBasePin. SetSink (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetSink
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4237e342f8f49059cab017b17a1f116ca6e2da67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748642"
---
# <a name="cbasepinsetsink-method"></a><span data-ttu-id="e8394-104">Método CBasePin. SetSink</span><span class="sxs-lookup"><span data-stu-id="e8394-104">CBasePin.SetSink method</span></span>

<span data-ttu-id="e8394-105">O `SetSink` método define um Gerenciador de qualidade externo.</span><span class="sxs-lookup"><span data-stu-id="e8394-105">The `SetSink` method sets an external quality manager.</span></span> <span data-ttu-id="e8394-106">Esse método implementa o método [**IQualityControl:: SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) .</span><span class="sxs-lookup"><span data-stu-id="e8394-106">This method implements the [**IQualityControl::SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8394-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e8394-107">Syntax</span></span>


```C++
HRESULT SetSink(
   IQualityControl *piqc
);
```



## <a name="parameters"></a><span data-ttu-id="e8394-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e8394-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8394-109">*piqc*</span><span class="sxs-lookup"><span data-stu-id="e8394-109">*piqc*</span></span> 
</dt> <dd>

<span data-ttu-id="e8394-110">Ponteiro para a interface [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) do Gerenciador de qualidade.</span><span class="sxs-lookup"><span data-stu-id="e8394-110">Pointer to the [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) interface of the quality manager.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8394-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e8394-111">Return value</span></span>

<span data-ttu-id="e8394-112">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e8394-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8394-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8394-113">Remarks</span></span>

<span data-ttu-id="e8394-114">Chame esse método para redirecionar mensagens de controle de qualidade para um Gerenciador de qualidade externo.</span><span class="sxs-lookup"><span data-stu-id="e8394-114">Call this method to redirect quality-control messages to an external quality manager.</span></span> <span data-ttu-id="e8394-115">Para obter mais informações, consulte [Gerenciamento de controle de qualidade](quality-control-management.md).</span><span class="sxs-lookup"><span data-stu-id="e8394-115">For more information, see [Quality-Control Management](quality-control-management.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e8394-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8394-116">Requirements</span></span>



| <span data-ttu-id="e8394-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8394-117">Requirement</span></span> | <span data-ttu-id="e8394-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e8394-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8394-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e8394-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e8394-120"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e8394-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e8394-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e8394-121">Library</span></span><br/> | <dl> <span data-ttu-id="e8394-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e8394-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8394-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8394-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8394-124">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="e8394-124">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 





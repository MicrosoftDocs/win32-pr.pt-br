---
description: 'O método Run notifica o PIN de que o filtro agora está em execução. Esse método substitui o método CBasePin:: Run.'
ms.assetid: ee0285aa-9afd-464a-b8b4-d8b7faa49dbd
title: Método CRenderedInputPin. Run (Amextra. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef3de4d5ab9a06766ccce171c9d417639ce66a42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749013"
---
# <a name="crenderedinputpinrun-method"></a><span data-ttu-id="fc639-104">Método CRenderedInputPin. Run</span><span class="sxs-lookup"><span data-stu-id="fc639-104">CRenderedInputPin.Run method</span></span>

<span data-ttu-id="fc639-105">O `Run` método notifica o PIN de que o filtro agora está em execução.</span><span class="sxs-lookup"><span data-stu-id="fc639-105">The `Run` method notifies the pin that the filter is now running.</span></span> <span data-ttu-id="fc639-106">Esse método substitui o método [**CBasePin:: Run**](cbasepin-run.md) .</span><span class="sxs-lookup"><span data-stu-id="fc639-106">This method overrides the [**CBasePin::Run**](cbasepin-run.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc639-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fc639-107">Syntax</span></span>


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a><span data-ttu-id="fc639-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fc639-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc639-109">*tStart*</span><span class="sxs-lookup"><span data-stu-id="fc639-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="fc639-110">A hora de início que foi passada para o método [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) do filtro.</span><span class="sxs-lookup"><span data-stu-id="fc639-110">The start time that was passed to the filter's [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc639-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fc639-111">Return value</span></span>

<span data-ttu-id="fc639-112">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fc639-112">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc639-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc639-113">Requirements</span></span>



| <span data-ttu-id="fc639-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc639-114">Requirement</span></span> | <span data-ttu-id="fc639-115">Valor</span><span class="sxs-lookup"><span data-stu-id="fc639-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc639-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fc639-116">Header</span></span><br/>  | <dl> <span data-ttu-id="fc639-117"><dt>Amextra. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fc639-117"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fc639-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fc639-118">Library</span></span><br/> | <dl> <span data-ttu-id="fc639-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="fc639-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc639-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc639-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc639-121">**Classe CRenderedInputPin**</span><span class="sxs-lookup"><span data-stu-id="fc639-121">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 





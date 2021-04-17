---
description: 'O método GetStopPosition recupera a hora em que a reprodução será interrompida, em relação à duração do fluxo. Esse método implementa o método IMediaSeeking:: GetStopPosition.'
ms.assetid: 83928f62-7acc-43b9-9537-49131ed0b0d4
title: Método CSourceSeeking. GetStopPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetStopPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d9f61ad26c32cfeec285874edfcc26038d57b117
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812991"
---
# <a name="csourceseekinggetstopposition-method"></a><span data-ttu-id="ba7cd-104">Método CSourceSeeking. GetStopPosition</span><span class="sxs-lookup"><span data-stu-id="ba7cd-104">CSourceSeeking.GetStopPosition method</span></span>

<span data-ttu-id="ba7cd-105">O `GetStopPosition` método recupera a hora em que a reprodução será interrompida, em relação à duração do fluxo.</span><span class="sxs-lookup"><span data-stu-id="ba7cd-105">The `GetStopPosition` method retrieves the time when playback will stop, relative to the duration of the stream.</span></span> <span data-ttu-id="ba7cd-106">Esse método implementa o método [**IMediaSeeking:: GetStopPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) .</span><span class="sxs-lookup"><span data-stu-id="ba7cd-106">This method implements the [**IMediaSeeking::GetStopPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba7cd-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba7cd-107">Syntax</span></span>


```C++
HRESULT GetStopPosition(
   LONGLONG *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="ba7cd-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba7cd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba7cd-109">*pStop*</span><span class="sxs-lookup"><span data-stu-id="ba7cd-109">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="ba7cd-110">Ponteiro para uma variável que recebe a hora de parada, em unidades do formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="ba7cd-110">Pointer to a variable that receives the stop time, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba7cd-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ba7cd-111">Return value</span></span>

<span data-ttu-id="ba7cd-112">Retorna um dos valores **HRESULT** listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ba7cd-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="ba7cd-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ba7cd-113">Return code</span></span>                                                                               | <span data-ttu-id="ba7cd-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="ba7cd-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="ba7cd-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ba7cd-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="ba7cd-116">Sucesso</span><span class="sxs-lookup"><span data-stu-id="ba7cd-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="ba7cd-117"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="ba7cd-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="ba7cd-118">Valor de ponteiro **nulo**</span><span class="sxs-lookup"><span data-stu-id="ba7cd-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ba7cd-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba7cd-119">Remarks</span></span>

<span data-ttu-id="ba7cd-120">A hora de parada é especificada pela variável de membro [**CSourceSeeking:: m \_ rtStop**](csourceseeking-m-rtstop.md) .</span><span class="sxs-lookup"><span data-stu-id="ba7cd-120">The stop time is specified by the [**CSourceSeeking::m\_rtStop**](csourceseeking-m-rtstop.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba7cd-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba7cd-121">Requirements</span></span>



| <span data-ttu-id="ba7cd-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba7cd-122">Requirement</span></span> | <span data-ttu-id="ba7cd-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ba7cd-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba7cd-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ba7cd-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ba7cd-125"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ba7cd-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ba7cd-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ba7cd-126">Library</span></span><br/> | <dl> <span data-ttu-id="ba7cd-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ba7cd-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba7cd-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba7cd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba7cd-129">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="ba7cd-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 





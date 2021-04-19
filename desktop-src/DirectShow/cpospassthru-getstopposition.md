---
description: 'O método GetStopPosition recupera a hora em que a reprodução será interrompida, em relação à duração do fluxo. Esse método implementa o método IMediaSeeking:: GetStopPosition.'
ms.assetid: 11486371-da0a-4b83-956b-ef6b92721e74
title: Método CPosPassThru. GetStopPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetStopPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ee704a47074db032badfa1f02ffbf2db8c7efa4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778491"
---
# <a name="cpospassthrugetstopposition-method"></a><span data-ttu-id="42490-104">Método CPosPassThru. GetStopPosition</span><span class="sxs-lookup"><span data-stu-id="42490-104">CPosPassThru.GetStopPosition method</span></span>

<span data-ttu-id="42490-105">O `GetStopPosition` método recupera a hora em que a reprodução será interrompida, em relação à duração do fluxo.</span><span class="sxs-lookup"><span data-stu-id="42490-105">The `GetStopPosition` method retrieves the time at which the playback will stop, relative to the duration of the stream.</span></span> <span data-ttu-id="42490-106">Esse método implementa o método [**IMediaSeeking:: GetStopPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) .</span><span class="sxs-lookup"><span data-stu-id="42490-106">This method implements the [**IMediaSeeking::GetStopPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="42490-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="42490-107">Syntax</span></span>


```C++
HRESULT GetStopPosition(
   LONGLONG *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="42490-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42490-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42490-109">*pStop*</span><span class="sxs-lookup"><span data-stu-id="42490-109">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="42490-110">Ponteiro para uma variável que recebe a hora de parada, em unidades do formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="42490-110">Pointer to a variable that receives the stop time, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42490-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="42490-111">Return value</span></span>

<span data-ttu-id="42490-112">Retorna o valor **HRESULT** do PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="42490-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="42490-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42490-113">Requirements</span></span>



| <span data-ttu-id="42490-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="42490-114">Requirement</span></span> | <span data-ttu-id="42490-115">Valor</span><span class="sxs-lookup"><span data-stu-id="42490-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42490-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="42490-116">Header</span></span><br/>  | <dl> <span data-ttu-id="42490-117"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="42490-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="42490-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="42490-118">Library</span></span><br/> | <dl> <span data-ttu-id="42490-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="42490-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42490-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="42490-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42490-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="42490-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 





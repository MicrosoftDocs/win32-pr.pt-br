---
description: O \_ método Put StopTime define a hora em que a reprodução será interrompida, em relação à duração do fluxo. Esse método implementa o método IMediaPosition::p UT \_ StopTime.
ms.assetid: 0a344cad-df93-47f1-8c7f-5d5ef775b850
title: Método de CPosPassThru.put_StopTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_StopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f5763700947596a0fb437ba3840df058d4d3239
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752082"
---
# <a name="cpospassthruput_stoptime-method"></a><span data-ttu-id="991f0-104">Método StopTime de CPosPassThru. put \_</span><span class="sxs-lookup"><span data-stu-id="991f0-104">CPosPassThru.put\_StopTime method</span></span>

<span data-ttu-id="991f0-105">O `put_StopTime` método define a hora em que a reprodução será interrompida, em relação à duração do fluxo.</span><span class="sxs-lookup"><span data-stu-id="991f0-105">The `put_StopTime` method sets the time at which the playback will stop, relative to the duration of the stream.</span></span> <span data-ttu-id="991f0-106">Esse método implementa o método [**IMediaPosition::p UT \_ StopTime**](/windows/desktop/api/Control/nf-control-imediaposition-put_stoptime) .</span><span class="sxs-lookup"><span data-stu-id="991f0-106">This method implements the [**IMediaPosition::put\_StopTime**](/windows/desktop/api/Control/nf-control-imediaposition-put_stoptime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="991f0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="991f0-107">Syntax</span></span>


```C++
HRESULT put_StopTime(
   REFTIME llTime
);
```



## <a name="parameters"></a><span data-ttu-id="991f0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="991f0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="991f0-109">*llTime*</span><span class="sxs-lookup"><span data-stu-id="991f0-109">*llTime*</span></span> 
</dt> <dd>

<span data-ttu-id="991f0-110">Hora de parada como um valor **duplo** , em segundos.</span><span class="sxs-lookup"><span data-stu-id="991f0-110">Stop time as a **double** value, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="991f0-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="991f0-111">Return value</span></span>

<span data-ttu-id="991f0-112">Retorna o valor **HRESULT** do PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="991f0-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="991f0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="991f0-113">Requirements</span></span>



| <span data-ttu-id="991f0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="991f0-114">Requirement</span></span> | <span data-ttu-id="991f0-115">Valor</span><span class="sxs-lookup"><span data-stu-id="991f0-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="991f0-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="991f0-116">Header</span></span><br/>  | <dl> <span data-ttu-id="991f0-117"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="991f0-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="991f0-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="991f0-118">Library</span></span><br/> | <dl> <span data-ttu-id="991f0-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="991f0-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="991f0-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="991f0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="991f0-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="991f0-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 





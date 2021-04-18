---
description: 'O \_ método Get StopTime recupera a hora em que a reprodução será interrompida, em relação à duração do fluxo. Esse método implementa o método IMediaPosition:: get \_ StopTime.'
ms.assetid: 0ca3f047-ac43-419e-a1ed-b406f89f7af7
title: Método de CPosPassThru.get_StopTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_StopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 227b054a9737c06e56f7311acc7e0093766608b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751686"
---
# <a name="cpospassthruget_stoptime-method"></a><span data-ttu-id="4673b-104">CPosPassThru. obter \_ método StopTime</span><span class="sxs-lookup"><span data-stu-id="4673b-104">CPosPassThru.get\_StopTime method</span></span>

<span data-ttu-id="4673b-105">O `get_StopTime` método recupera a hora em que a reprodução será interrompida, em relação à duração do fluxo.</span><span class="sxs-lookup"><span data-stu-id="4673b-105">The `get_StopTime` method retrieves the time at which the playback will stop, relative to the duration of the stream.</span></span> <span data-ttu-id="4673b-106">Esse método implementa o método [**IMediaPosition:: get \_ StopTime**](/windows/desktop/api/Control/nf-control-imediaposition-get_stoptime) .</span><span class="sxs-lookup"><span data-stu-id="4673b-106">This method implements the [**IMediaPosition::get\_StopTime**](/windows/desktop/api/Control/nf-control-imediaposition-get_stoptime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4673b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4673b-107">Syntax</span></span>


```C++
HRESULT get_StopTime(
   REFTIME *pllTime
);
```



## <a name="parameters"></a><span data-ttu-id="4673b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4673b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4673b-109">*pllTime*</span><span class="sxs-lookup"><span data-stu-id="4673b-109">*pllTime*</span></span> 
</dt> <dd>

<span data-ttu-id="4673b-110">Ponteiro para uma variável que recebe a hora de parada, em segundos.</span><span class="sxs-lookup"><span data-stu-id="4673b-110">Pointer to a variable that receives the stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4673b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4673b-111">Return value</span></span>

<span data-ttu-id="4673b-112">Retorna o valor **HRESULT** do PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="4673b-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="4673b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4673b-113">Requirements</span></span>



| <span data-ttu-id="4673b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4673b-114">Requirement</span></span> | <span data-ttu-id="4673b-115">Valor</span><span class="sxs-lookup"><span data-stu-id="4673b-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4673b-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4673b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="4673b-117"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4673b-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4673b-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4673b-118">Library</span></span><br/> | <dl> <span data-ttu-id="4673b-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="4673b-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4673b-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="4673b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4673b-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="4673b-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 





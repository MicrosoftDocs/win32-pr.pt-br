---
description: 'O método SetMediaTime define as horas de mídia para este exemplo. Esse método implementa o método IMediaSample:: SetMediaTime.'
ms.assetid: 768812f8-c044-4499-9149-7c334c51e539
title: Método CMediaSample. SetMediaTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0240ef40f4c37f6c5528c979b2e89b43b03b3451
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756198"
---
# <a name="cmediasamplesetmediatime-method"></a><span data-ttu-id="c99fc-104">Método CMediaSample. SetMediaTime</span><span class="sxs-lookup"><span data-stu-id="c99fc-104">CMediaSample.SetMediaTime method</span></span>

<span data-ttu-id="c99fc-105">O `SetMediaTime` método define os horários de mídia para este exemplo.</span><span class="sxs-lookup"><span data-stu-id="c99fc-105">The `SetMediaTime` method sets the media times for this sample.</span></span> <span data-ttu-id="c99fc-106">Esse método implementa o método [**IMediaSample:: SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) .</span><span class="sxs-lookup"><span data-stu-id="c99fc-106">This method implements the [**IMediaSample::SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c99fc-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c99fc-107">Syntax</span></span>


```C++
HRESULT SetMediaTime(
   LONGLONG *pStart,
   LONGLONG *pEnd
);
```



## <a name="parameters"></a><span data-ttu-id="c99fc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c99fc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c99fc-109">*pStart*</span><span class="sxs-lookup"><span data-stu-id="c99fc-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="c99fc-110">Ponteiro para a hora de início da mídia ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="c99fc-110">Pointer to the media start time, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c99fc-111">*Pendente*</span><span class="sxs-lookup"><span data-stu-id="c99fc-111">*pEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="c99fc-112">Ponteiro para a hora de parada da mídia ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="c99fc-112">Pointer to the media stop time, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c99fc-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c99fc-113">Return value</span></span>

<span data-ttu-id="c99fc-114">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c99fc-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="c99fc-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="c99fc-115">Remarks</span></span>

<span data-ttu-id="c99fc-116">A hora de parada da mídia deve ser maior que a hora de início da mídia.</span><span class="sxs-lookup"><span data-stu-id="c99fc-116">The media stop time must be greater than the media start time.</span></span> <span data-ttu-id="c99fc-117">Use **NULL** para invalidar os horários de mídia.</span><span class="sxs-lookup"><span data-stu-id="c99fc-117">Use **NULL** to invalidate the media times.</span></span>

<span data-ttu-id="c99fc-118">O parâmetro *pendente* especifica um tempo de mídia absoluto, mas a variável de membro [**CMediaSample:: m \_ MediaEnd**](cmediasample-m-mediaend.md) é calculada como um deslocamento de *PStart*.</span><span class="sxs-lookup"><span data-stu-id="c99fc-118">The *pEnd* parameter specifies an absolute media time, but the [**CMediaSample::m\_MediaEnd**](cmediasample-m-mediaend.md) member variable is calculated as an offset from *pStart*.</span></span> <span data-ttu-id="c99fc-119">Em outras palavras, **m \_ MediaEnd**  =  \* *pTimeEnd* \* *pTimeStart*.  </span><span class="sxs-lookup"><span data-stu-id="c99fc-119">In other words, **m\_MediaEnd** = \**pTimeEnd*  \**pTimeStart*.</span></span>

<span data-ttu-id="c99fc-120">Para obter informações sobre os tempos de mídia, consulte [tempo e relógios no DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="c99fc-120">For information about media times, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c99fc-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c99fc-121">Requirements</span></span>



| <span data-ttu-id="c99fc-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c99fc-122">Requirement</span></span> | <span data-ttu-id="c99fc-123">Valor</span><span class="sxs-lookup"><span data-stu-id="c99fc-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c99fc-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c99fc-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c99fc-125"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c99fc-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c99fc-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c99fc-126">Library</span></span><br/> | <dl> <span data-ttu-id="c99fc-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c99fc-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c99fc-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="c99fc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c99fc-129">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="c99fc-129">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 





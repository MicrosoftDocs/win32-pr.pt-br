---
description: 'O método setTime define os tempos de transmissão quando este exemplo deve começar e terminar. Esse método implementa o método IMediaSample:: SetTime.'
ms.assetid: cab4907f-eb6f-4444-9b41-1f95a6ecffed
title: Método CMediaSample. setTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 935c4f3aa565b291e459d36e067805944b4fd6b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757699"
---
# <a name="cmediasamplesettime-method"></a><span data-ttu-id="aa4d2-104">Método CMediaSample. setTime</span><span class="sxs-lookup"><span data-stu-id="aa4d2-104">CMediaSample.SetTime method</span></span>

<span data-ttu-id="aa4d2-105">O `SetTime` método define os tempos de transmissão quando este exemplo deve começar e terminar.</span><span class="sxs-lookup"><span data-stu-id="aa4d2-105">The `SetTime` method sets the stream times when this sample should begin and finish.</span></span> <span data-ttu-id="aa4d2-106">Esse método implementa o método [**IMediaSample:: SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) .</span><span class="sxs-lookup"><span data-stu-id="aa4d2-106">This method implements the [**IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa4d2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa4d2-107">Syntax</span></span>


```C++
HRESULT SetTime(
   REFERENCE_TIME *pTimeStart,
   REFERENCE_TIME *pTimeEnd
);
```



## <a name="parameters"></a><span data-ttu-id="aa4d2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa4d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa4d2-109">*pTimeStart*</span><span class="sxs-lookup"><span data-stu-id="aa4d2-109">*pTimeStart*</span></span> 
</dt> <dd>

<span data-ttu-id="aa4d2-110">Aponta para a hora do fluxo no qual o exemplo começa, em unidades de 100 a nanossegundos ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="aa4d2-110">Pointer to the stream time at which the sample begins, in 100-nanosecond units, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="aa4d2-111">*pTimeEnd*</span><span class="sxs-lookup"><span data-stu-id="aa4d2-111">*pTimeEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="aa4d2-112">Aponta para a hora do fluxo em que o exemplo termina, em unidades de 100 nanossegundos ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="aa4d2-112">Pointer to the stream time at which the sample ends, in 100-nanosecond units, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa4d2-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aa4d2-113">Return value</span></span>

<span data-ttu-id="aa4d2-114">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="aa4d2-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa4d2-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa4d2-115">Remarks</span></span>

<span data-ttu-id="aa4d2-116">Esse método define as variáveis de membro final [**CMediaSample:: m \_ Start**](cmediasample-m-start.md) e [**CMediaSample:: m \_**](cmediasample-m-end.md) , que especificam os carimbos de data/hora.</span><span class="sxs-lookup"><span data-stu-id="aa4d2-116">This method sets the [**CMediaSample::m\_Start**](cmediasample-m-start.md) and [**CMediaSample::m\_End**](cmediasample-m-end.md) member variables, which specify the time stamps.</span></span> <span data-ttu-id="aa4d2-117">Ele também atualiza a variável de membro [**CMediaSample:: m \_ dwFlags**](cmediasample-m-dwflags.md) , que especifica se os carimbos de data/hora são válidos.</span><span class="sxs-lookup"><span data-stu-id="aa4d2-117">It also updates the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable, which specifies whether the time stamps are valid.</span></span>

<span data-ttu-id="aa4d2-118">Para obter informações sobre carimbos de data/hora, consulte [tempo e relógios no DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="aa4d2-118">For information about time stamps, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa4d2-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa4d2-119">Requirements</span></span>



| <span data-ttu-id="aa4d2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa4d2-120">Requirement</span></span> | <span data-ttu-id="aa4d2-121">Valor</span><span class="sxs-lookup"><span data-stu-id="aa4d2-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa4d2-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aa4d2-122">Header</span></span><br/>  | <dl> <span data-ttu-id="aa4d2-123"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aa4d2-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="aa4d2-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aa4d2-124">Library</span></span><br/> | <dl> <span data-ttu-id="aa4d2-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="aa4d2-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa4d2-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa4d2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa4d2-127">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="aa4d2-127">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 





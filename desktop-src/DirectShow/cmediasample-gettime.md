---
description: 'O método getTime recupera os tempos de transmissão em que este exemplo deve começar e terminar. Esse método implementa o método IMediaSample:: getTime.'
ms.assetid: ddb0df1c-707d-405d-9e73-0d5a59f487b6
title: Método CMediaSample. getTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8ff2035ede3e49feb2bc14a7aa31cfc18f2e7d23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756628"
---
# <a name="cmediasamplegettime-method"></a><span data-ttu-id="8e7c4-104">Método CMediaSample. getTime</span><span class="sxs-lookup"><span data-stu-id="8e7c4-104">CMediaSample.GetTime method</span></span>

<span data-ttu-id="8e7c4-105">O `GetTime` método recupera os tempos de transmissão em que este exemplo deve começar e terminar.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-105">The `GetTime` method retrieves the stream times at which this sample should begin and finish.</span></span> <span data-ttu-id="8e7c4-106">Esse método implementa o método [**IMediaSample:: getTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) .</span><span class="sxs-lookup"><span data-stu-id="8e7c4-106">This method implements the [**IMediaSample::GetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e7c4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8e7c4-107">Syntax</span></span>


```C++
HRESULT GetTime(
   REFERENCE_TIME *pTimeStart,
   REFERENCE_TIME *pTimeEnd
);
```



## <a name="parameters"></a><span data-ttu-id="8e7c4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e7c4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e7c4-109">*pTimeStart*</span><span class="sxs-lookup"><span data-stu-id="8e7c4-109">*pTimeStart*</span></span> 
</dt> <dd>

<span data-ttu-id="8e7c4-110">Ponteiro para uma variável que recebe a hora de início do fluxo, em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-110">Pointer to a variable that receives the beginning stream time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="8e7c4-111">*pTimeEnd*</span><span class="sxs-lookup"><span data-stu-id="8e7c4-111">*pTimeEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="8e7c4-112">Ponteiro para uma variável que recebe a hora final do fluxo, em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-112">Pointer to a variable that receives the ending stream time, in 100-nanosecond units.</span></span> <span data-ttu-id="8e7c4-113">Se o exemplo não tiver hora de parada, o valor será definido como a hora de início mais um.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-113">If the sample has no stop time, the value is set to the start time plus one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e7c4-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8e7c4-114">Return value</span></span>

<span data-ttu-id="8e7c4-115">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-115">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="8e7c4-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8e7c4-116">Return code</span></span>                                                                                                   | <span data-ttu-id="8e7c4-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e7c4-117">Description</span></span>                                                 |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="8e7c4-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8e7c4-118"><dt>**S\_OK**</dt></span></span> </dl>                          | <span data-ttu-id="8e7c4-119">Êxito.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-119">Success.</span></span><br/>                                         |
| <dl> <span data-ttu-id="8e7c4-120"><dt>**VFW \_ S \_ sem \_ hora de parada \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8e7c4-120"><dt>**VFW\_S\_NO\_STOP\_TIME**</dt></span></span> </dl>         | <span data-ttu-id="8e7c4-121">O exemplo tem uma hora de início válida, mas nenhuma hora de parada.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-121">Sample has a valid start time, but no stop time.</span></span><br/> |
| <dl> <span data-ttu-id="8e7c4-122"><dt>**VFW \_ E \_ tempo de amostra \_ \_ não \_ definido**</dt></span><span class="sxs-lookup"><span data-stu-id="8e7c4-122"><dt>**VFW\_E\_SAMPLE\_TIME\_NOT\_SET**</dt></span></span> </dl> | <span data-ttu-id="8e7c4-123">O exemplo não tem carimbos de data/hora válidos.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-123">Sample does not have valid time stamps.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="8e7c4-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e7c4-124">Remarks</span></span>

<span data-ttu-id="8e7c4-125">As variáveis de membro end [**CMediaSample:: m \_ Start**](cmediasample-m-start.md) e [**CMediaSample:: m \_**](cmediasample-m-end.md) especificam os carimbos de data/hora.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-125">The [**CMediaSample::m\_Start**](cmediasample-m-start.md) and [**CMediaSample::m\_End**](cmediasample-m-end.md) member variables specify the time stamps.</span></span> <span data-ttu-id="8e7c4-126">A variável de membro [**CMediaSample:: m \_ dwFlags**](cmediasample-m-dwflags.md) especifica se os carimbos de data/hora são válidos.</span><span class="sxs-lookup"><span data-stu-id="8e7c4-126">The [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable specifies whether the time stamps are valid.</span></span>

<span data-ttu-id="8e7c4-127">Para obter informações sobre carimbos de data/hora, consulte [tempo e relógios no DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="8e7c4-127">For information about time stamps, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8e7c4-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e7c4-128">Requirements</span></span>



| <span data-ttu-id="8e7c4-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e7c4-129">Requirement</span></span> | <span data-ttu-id="8e7c4-130">Valor</span><span class="sxs-lookup"><span data-stu-id="8e7c4-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e7c4-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8e7c4-131">Header</span></span><br/>  | <dl> <span data-ttu-id="8e7c4-132"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8e7c4-132"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8e7c4-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8e7c4-133">Library</span></span><br/> | <dl> <span data-ttu-id="8e7c4-134"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="8e7c4-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e7c4-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e7c4-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e7c4-136">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="8e7c4-136">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 





---
description: 'O método GetMediaTime recupera os horários de mídia para este exemplo. Esse método implementa o método IMediaSample:: GetMediaTime.'
ms.assetid: f58a2162-5764-48f2-8984-ee4bba1229ab
title: Método CMediaSample. GetMediaTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9a41d29e46d29cff9023421a661cc90731d4c06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757704"
---
# <a name="cmediasamplegetmediatime-method"></a><span data-ttu-id="d01cf-104">Método CMediaSample. GetMediaTime</span><span class="sxs-lookup"><span data-stu-id="d01cf-104">CMediaSample.GetMediaTime method</span></span>

<span data-ttu-id="d01cf-105">O `GetMediaTime` método recupera os horários de mídia para este exemplo.</span><span class="sxs-lookup"><span data-stu-id="d01cf-105">The `GetMediaTime` method retrieves the media times for this sample.</span></span> <span data-ttu-id="d01cf-106">Esse método implementa o método [**IMediaSample:: GetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatime) .</span><span class="sxs-lookup"><span data-stu-id="d01cf-106">This method implements the [**IMediaSample::GetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d01cf-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d01cf-107">Syntax</span></span>


```C++
HRESULT GetMediaTime(
   LONGLONG *pStart,
   LONGLONG *pEnd
);
```



## <a name="parameters"></a><span data-ttu-id="d01cf-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d01cf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d01cf-109">*pStart*</span><span class="sxs-lookup"><span data-stu-id="d01cf-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="d01cf-110">Ponteiro para uma variável que recebe a hora de início da mídia.</span><span class="sxs-lookup"><span data-stu-id="d01cf-110">Pointer to a variable that receives the media start time.</span></span>

</dd> <dt>

<span data-ttu-id="d01cf-111">*Pendente*</span><span class="sxs-lookup"><span data-stu-id="d01cf-111">*pEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="d01cf-112">Ponteiro para uma variável que recebe a hora de parada da mídia.</span><span class="sxs-lookup"><span data-stu-id="d01cf-112">Pointer to a variable that receives the media stop time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d01cf-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d01cf-113">Return value</span></span>

<span data-ttu-id="d01cf-114">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d01cf-114">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="d01cf-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d01cf-115">Return code</span></span>                                                                                                  | <span data-ttu-id="d01cf-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="d01cf-116">Description</span></span>                                         |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="d01cf-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d01cf-117"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="d01cf-118">Êxito.</span><span class="sxs-lookup"><span data-stu-id="d01cf-118">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="d01cf-119"><dt>**VFW \_ E \_ hora de mídia \_ \_ não \_ definida**</dt></span><span class="sxs-lookup"><span data-stu-id="d01cf-119"><dt>**VFW\_E\_MEDIA\_TIME\_NOT\_SET**</dt></span></span> </dl> | <span data-ttu-id="d01cf-120">Nenhum horário de mídia foi definido para este exemplo.</span><span class="sxs-lookup"><span data-stu-id="d01cf-120">No media times were set for this sample.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d01cf-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="d01cf-121">Remarks</span></span>

<span data-ttu-id="d01cf-122">A variável de membro [**CMediaSample:: m \_ MediaEnd**](cmediasample-m-mediaend.md) especifica um deslocamento [**de CMediaSample:: m \_ MediaStart**](cmediasample-m-mediastart.md), mas o valor recebido pelo parâmetro *pendente* é um tempo de mídia absoluto, calculado como **m \_ MediaStart**  +  **m \_ MediaEnd**.</span><span class="sxs-lookup"><span data-stu-id="d01cf-122">The [**CMediaSample::m\_MediaEnd**](cmediasample-m-mediaend.md) member variable specifies an offset from [**CMediaSample::m\_MediaStart**](cmediasample-m-mediastart.md), but the value received by the *pEnd* parameter is an absolute media time, calculated as **m\_MediaStart** + **m\_MediaEnd**.</span></span>

<span data-ttu-id="d01cf-123">Para obter informações sobre os tempos de mídia, consulte [tempo e relógios no DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="d01cf-123">For information about media times, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d01cf-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d01cf-124">Requirements</span></span>



| <span data-ttu-id="d01cf-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d01cf-125">Requirement</span></span> | <span data-ttu-id="d01cf-126">Valor</span><span class="sxs-lookup"><span data-stu-id="d01cf-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d01cf-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d01cf-127">Header</span></span><br/>  | <dl> <span data-ttu-id="d01cf-128"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d01cf-128"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d01cf-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d01cf-129">Library</span></span><br/> | <dl> <span data-ttu-id="d01cf-130"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d01cf-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d01cf-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="d01cf-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d01cf-132">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="d01cf-132">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 





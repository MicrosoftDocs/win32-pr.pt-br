---
description: O método GetSampleTimes recupera os carimbos de data/hora de um exemplo.
ms.assetid: a8fead22-a12c-489d-9c42-d5b61f480c25
title: Método CBaseRenderer. GetSampleTimes (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetSampleTimes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c389c2ea55ddb15c59fe30e03f392d68aa3b5ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748029"
---
# <a name="cbaserenderergetsampletimes-method"></a><span data-ttu-id="d1cbf-103">Método CBaseRenderer. GetSampleTimes</span><span class="sxs-lookup"><span data-stu-id="d1cbf-103">CBaseRenderer.GetSampleTimes method</span></span>

<span data-ttu-id="d1cbf-104">O `GetSampleTimes` método recupera os carimbos de data/hora de um exemplo.</span><span class="sxs-lookup"><span data-stu-id="d1cbf-104">The `GetSampleTimes` method retrieves the time stamps from a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1cbf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1cbf-105">Syntax</span></span>


```C++
virtual HRESULT GetSampleTimes(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="d1cbf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1cbf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1cbf-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="d1cbf-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="d1cbf-108">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.</span><span class="sxs-lookup"><span data-stu-id="d1cbf-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> <dt>

<span data-ttu-id="d1cbf-109">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="d1cbf-109">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="d1cbf-110">Ponteiro para uma variável que recebe a hora de início.</span><span class="sxs-lookup"><span data-stu-id="d1cbf-110">Pointer to a variable that receives the start time.</span></span>

</dd> <dt>

<span data-ttu-id="d1cbf-111">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="d1cbf-111">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="d1cbf-112">Ponteiro para uma variável que recebe a hora de término.</span><span class="sxs-lookup"><span data-stu-id="d1cbf-112">Pointer to a variable that receives the end time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1cbf-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d1cbf-113">Return value</span></span>

<span data-ttu-id="d1cbf-114">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d1cbf-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d1cbf-115">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d1cbf-115">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="d1cbf-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d1cbf-116">Return code</span></span>                                                                                                    | <span data-ttu-id="d1cbf-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="d1cbf-117">Description</span></span>                                                                        |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d1cbf-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d1cbf-118"><dt>**S\_OK**</dt></span></span> </dl>                           | <span data-ttu-id="d1cbf-119">O exemplo deve ser renderizado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="d1cbf-119">The sample should be rendered immediately.</span></span><br/>                              |
| <dl> <span data-ttu-id="d1cbf-120"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="d1cbf-120"><dt>**S\_FALSE**</dt></span></span> </dl>                        | <span data-ttu-id="d1cbf-121">O exemplo deve ser agendado para renderização, com base nos carimbos de data/hora.</span><span class="sxs-lookup"><span data-stu-id="d1cbf-121">The sample should be scheduled for rendering, based on the time stamps.</span></span><br/> |
| <dl> <span data-ttu-id="d1cbf-122"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="d1cbf-122"><dt>**E\_FAIL**</dt></span></span> </dl>                         | <span data-ttu-id="d1cbf-123">Não processar este exemplo.</span><span class="sxs-lookup"><span data-stu-id="d1cbf-123">Do not render this sample.</span></span><br/>                                              |
| <dl> <span data-ttu-id="d1cbf-124"><dt>**VFW \_ \_ hora de início E \_ \_ término após o \_ final**</dt></span><span class="sxs-lookup"><span data-stu-id="d1cbf-124"><dt>**VFW\_E\_START\_TIME\_AFTER\_END**</dt></span></span> </dl> | <span data-ttu-id="d1cbf-125">Carimbo de data/hora inadequado: a hora de término é anterior à hora de início.</span><span class="sxs-lookup"><span data-stu-id="d1cbf-125">Bad time stamp: The end time is earlier than the start time.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="d1cbf-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1cbf-126">Remarks</span></span>

<span data-ttu-id="d1cbf-127">O filtro chama esse método para determinar como ele deve lidar com um exemplo.</span><span class="sxs-lookup"><span data-stu-id="d1cbf-127">The filter calls this method to determine how it should handle a sample.</span></span> <span data-ttu-id="d1cbf-128">Se o valor de retorno for S \_ OK, o filtro renderizará o exemplo imediatamente.</span><span class="sxs-lookup"><span data-stu-id="d1cbf-128">If the return value is S\_OK, the filter renders the sample immediately.</span></span> <span data-ttu-id="d1cbf-129">Se o valor de retorno for S \_ false, o filtro agendará o exemplo para renderização, com base nos carimbos de data/hora.</span><span class="sxs-lookup"><span data-stu-id="d1cbf-129">If the return value is S\_FALSE, the filter schedules the sample for rendering, based on the time stamps.</span></span> <span data-ttu-id="d1cbf-130">Se o valor de retorno for um código de erro, o filtro rejeitará o exemplo.</span><span class="sxs-lookup"><span data-stu-id="d1cbf-130">If the return value is an error code, the filter rejects the sample.</span></span>

<span data-ttu-id="d1cbf-131">Esse método retornará S \_ OK se o exemplo não tiver carimbos de data/hora ou se o filtro não tiver um relógio de referência.</span><span class="sxs-lookup"><span data-stu-id="d1cbf-131">This method returns S\_OK if the sample has no time stamps, or if the filter does not have a reference clock.</span></span> <span data-ttu-id="d1cbf-132">Caso contrário, ele retorna o valor do método [**CBaseRenderer:: ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md) .</span><span class="sxs-lookup"><span data-stu-id="d1cbf-132">Otherwise, it returns the value of the [**CBaseRenderer::ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md) method.</span></span> <span data-ttu-id="d1cbf-133">Na classe base, **ShouldDrawSampleNow** sempre retorna S \_ false.</span><span class="sxs-lookup"><span data-stu-id="d1cbf-133">In the base class, **ShouldDrawSampleNow** always returns S\_FALSE.</span></span> <span data-ttu-id="d1cbf-134">A classe derivada pode substituir esse comportamento.</span><span class="sxs-lookup"><span data-stu-id="d1cbf-134">The derived class can override this behavior.</span></span> <span data-ttu-id="d1cbf-135">Por exemplo, se a classe derivada implementar o gerenciamento de controle de qualidade, ela poderá retornar E \_ falhar ao descartar um exemplo.</span><span class="sxs-lookup"><span data-stu-id="d1cbf-135">For example, if the derived class implements quality control management, it might return E\_FAIL to drop a sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1cbf-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1cbf-136">Requirements</span></span>



| <span data-ttu-id="d1cbf-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1cbf-137">Requirement</span></span> | <span data-ttu-id="d1cbf-138">Valor</span><span class="sxs-lookup"><span data-stu-id="d1cbf-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1cbf-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d1cbf-139">Header</span></span><br/>  | <dl> <span data-ttu-id="d1cbf-140"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d1cbf-140"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d1cbf-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d1cbf-141">Library</span></span><br/> | <dl> <span data-ttu-id="d1cbf-142"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d1cbf-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1cbf-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1cbf-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1cbf-144">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="d1cbf-144">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 





---
description: O método ShouldDrawSampleNow determina como um exemplo é agendado para renderização.
ms.assetid: 92994f1f-53d5-42d4-90a2-2984b693e4c0
title: Método CBaseRenderer. ShouldDrawSampleNow (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ShouldDrawSampleNow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27fbf603fd670cac2a39831114a7f141b17ffd2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751499"
---
# <a name="cbaserenderershoulddrawsamplenow-method"></a><span data-ttu-id="6e270-103">Método CBaseRenderer. ShouldDrawSampleNow</span><span class="sxs-lookup"><span data-stu-id="6e270-103">CBaseRenderer.ShouldDrawSampleNow method</span></span>

<span data-ttu-id="6e270-104">O `ShouldDrawSampleNow` método determina como um exemplo é agendado para renderização.</span><span class="sxs-lookup"><span data-stu-id="6e270-104">The `ShouldDrawSampleNow` method determines how a sample is scheduled for rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e270-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6e270-105">Syntax</span></span>


```C++
virtual HRESULT ShouldDrawSampleNow(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="6e270-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e270-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e270-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="6e270-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="6e270-108">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.</span><span class="sxs-lookup"><span data-stu-id="6e270-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> <dt>

<span data-ttu-id="6e270-109">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="6e270-109">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="6e270-110">Ponteiro para uma variável que contém a hora de início da amostra.</span><span class="sxs-lookup"><span data-stu-id="6e270-110">Pointer to a variable that contains the sample's start time.</span></span>

</dd> <dt>

<span data-ttu-id="6e270-111">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="6e270-111">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="6e270-112">Ponteiro para uma variável que contém a hora de término da amostra.</span><span class="sxs-lookup"><span data-stu-id="6e270-112">Pointer to a variable that contains the sample's end time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e270-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6e270-113">Return value</span></span>

<span data-ttu-id="6e270-114">Retorna S \_ false.</span><span class="sxs-lookup"><span data-stu-id="6e270-114">Returns S\_FALSE.</span></span> <span data-ttu-id="6e270-115">Se a classe derivada substituir esse método, retorne um dos valores mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="6e270-115">If the derived class overrides this method, return one of the values shown in the following table.</span></span>



| <span data-ttu-id="6e270-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6e270-116">Return code</span></span>                                                                               | <span data-ttu-id="6e270-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="6e270-117">Description</span></span>                                                                        |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6e270-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6e270-118"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="6e270-119">O exemplo deve ser renderizado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="6e270-119">The sample should be rendered immediately.</span></span><br/>                              |
| <dl> <span data-ttu-id="6e270-120"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="6e270-120"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="6e270-121">O exemplo deve ser agendado para renderização, com base nos carimbos de data/hora.</span><span class="sxs-lookup"><span data-stu-id="6e270-121">The sample should be scheduled for rendering, based on the time stamps.</span></span><br/> |
| <dl> <span data-ttu-id="6e270-122"><dt>**Código de erro**</dt></span><span class="sxs-lookup"><span data-stu-id="6e270-122"><dt>**Error code**</dt></span></span> </dl> | <span data-ttu-id="6e270-123">Não processar este exemplo.</span><span class="sxs-lookup"><span data-stu-id="6e270-123">Do not render this sample.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="6e270-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e270-124">Remarks</span></span>

<span data-ttu-id="6e270-125">O método [**CBaseRenderer:: GetSampleTimes**](cbaserenderer-getsampletimes.md) chama esse método.</span><span class="sxs-lookup"><span data-stu-id="6e270-125">The [**CBaseRenderer::GetSampleTimes**](cbaserenderer-getsampletimes.md) method calls this method.</span></span> <span data-ttu-id="6e270-126">Por padrão, os exemplos são sempre agendados para renderização com base em seus carimbos de data/hora.</span><span class="sxs-lookup"><span data-stu-id="6e270-126">By default, samples are always scheduled for rendering based on their time stamps.</span></span> <span data-ttu-id="6e270-127">A classe derivada pode substituir esse método; por exemplo, para implementar o controle de qualidade.</span><span class="sxs-lookup"><span data-stu-id="6e270-127">The derived class can override this method; for example, to implement quality control.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e270-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e270-128">Requirements</span></span>



| <span data-ttu-id="6e270-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e270-129">Requirement</span></span> | <span data-ttu-id="6e270-130">Valor</span><span class="sxs-lookup"><span data-stu-id="6e270-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e270-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6e270-131">Header</span></span><br/>  | <dl> <span data-ttu-id="6e270-132"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6e270-132"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6e270-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6e270-133">Library</span></span><br/> | <dl> <span data-ttu-id="6e270-134"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="6e270-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e270-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e270-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e270-136">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="6e270-136">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 





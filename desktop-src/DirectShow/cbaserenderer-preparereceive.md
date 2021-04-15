---
description: O método PrepareReceive prepara o filtro para renderizar um exemplo.
ms.assetid: 873b6b3b-623e-4cec-91ea-fa628618348d
title: Método CBaseRenderer. PrepareReceive (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.PrepareReceive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b15f2a83d8cb20f7204e58dd12d5f94491904c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747600"
---
# <a name="cbaserendererpreparereceive-method"></a><span data-ttu-id="c3e19-103">Método CBaseRenderer. PrepareReceive</span><span class="sxs-lookup"><span data-stu-id="c3e19-103">CBaseRenderer.PrepareReceive method</span></span>

<span data-ttu-id="c3e19-104">O `PrepareReceive` método prepara o filtro para renderizar um exemplo.</span><span class="sxs-lookup"><span data-stu-id="c3e19-104">The `PrepareReceive` method prepares the filter to render a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3e19-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c3e19-105">Syntax</span></span>


```C++
virtual HRESULT PrepareReceive(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="c3e19-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3e19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3e19-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="c3e19-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="c3e19-108">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.</span><span class="sxs-lookup"><span data-stu-id="c3e19-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3e19-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c3e19-109">Return value</span></span>

<span data-ttu-id="c3e19-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c3e19-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c3e19-111">Os valores possíveis incluem os da tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3e19-111">Possible values include those in the following table.</span></span>



| <span data-ttu-id="c3e19-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c3e19-112">Return code</span></span>                                                                                             | <span data-ttu-id="c3e19-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3e19-113">Description</span></span>                                |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="c3e19-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c3e19-114"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="c3e19-115">Êxito.</span><span class="sxs-lookup"><span data-stu-id="c3e19-115">Success.</span></span><br/>                        |
| <dl> <span data-ttu-id="c3e19-116"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="c3e19-116"><dt>**E\_FAIL**</dt></span></span> </dl>                  | <span data-ttu-id="c3e19-117">Falhou.</span><span class="sxs-lookup"><span data-stu-id="c3e19-117">Failed.</span></span><br/>                         |
| <dl> <span data-ttu-id="c3e19-118"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="c3e19-118"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>            | <span data-ttu-id="c3e19-119">Erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="c3e19-119">Unexpected error.</span></span><br/>               |
| <dl> <span data-ttu-id="c3e19-120"><dt>**VFW \_ E \_ amostra \_ rejeitadas**</dt></span><span class="sxs-lookup"><span data-stu-id="c3e19-120"><dt>**VFW\_E\_SAMPLE\_REJECTED**</dt></span></span> </dl> | <span data-ttu-id="c3e19-121">O filtro está descartando este exemplo.</span><span class="sxs-lookup"><span data-stu-id="c3e19-121">Filter is dropping this sample.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c3e19-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3e19-122">Remarks</span></span>

<span data-ttu-id="c3e19-123">O filtro chama esse método de dentro do método [**CBaseRenderer:: Receive**](cbaserenderer-receive.md) , antes de renderizar um exemplo.</span><span class="sxs-lookup"><span data-stu-id="c3e19-123">The filter calls this method from inside the [**CBaseRenderer::Receive**](cbaserenderer-receive.md) method, before it renders a sample.</span></span> <span data-ttu-id="c3e19-124">Se o filtro estiver em execução, esse método agendará o exemplo para renderização.</span><span class="sxs-lookup"><span data-stu-id="c3e19-124">If the filter is running, this method schedules the sample for rendering.</span></span>

<span data-ttu-id="c3e19-125">Se o filtro já tiver um exemplo pendente ou se o fim do fluxo já tiver sido atingido, o método retornará E \_ inesperado.</span><span class="sxs-lookup"><span data-stu-id="c3e19-125">If the filter already has a pending sample, or if the end-of-stream was already reached, the method returns E\_UNEXPECTED.</span></span> <span data-ttu-id="c3e19-126">Possivelmente, o filtro upstream não está serializando suas chamadas de streaming corretamente.</span><span class="sxs-lookup"><span data-stu-id="c3e19-126">Possibly the upstream filter is not serializing its streaming calls correctly.</span></span>

<span data-ttu-id="c3e19-127">Se o algoritmo de agendamento determinar que o exemplo deve ser descartado (consulte [**CBaseRenderer:: ScheduleSample**](cbaserenderer-schedulesample.md)), o método retornará VFW \_ E \_ Sample \_ rejeitado.</span><span class="sxs-lookup"><span data-stu-id="c3e19-127">If the scheduling algorithm determines that the sample should be dropped (see [**CBaseRenderer::ScheduleSample**](cbaserenderer-schedulesample.md)), the method returns VFW\_E\_SAMPLE\_REJECTED.</span></span> <span data-ttu-id="c3e19-128">No entanto, o método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) do pino de entrada não passa esse código de erro para o filtro upstream, pois remover um exemplo não é um erro.</span><span class="sxs-lookup"><span data-stu-id="c3e19-128">However, the input pin's [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method does not pass this error code to the upstream filter, because dropping a sample is not an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3e19-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3e19-129">Requirements</span></span>



| <span data-ttu-id="c3e19-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3e19-130">Requirement</span></span> | <span data-ttu-id="c3e19-131">Valor</span><span class="sxs-lookup"><span data-stu-id="c3e19-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3e19-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c3e19-132">Header</span></span><br/>  | <dl> <span data-ttu-id="c3e19-133"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3e19-133"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c3e19-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c3e19-134">Library</span></span><br/> | <dl> <span data-ttu-id="c3e19-135"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c3e19-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3e19-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3e19-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3e19-137">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="c3e19-137">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 





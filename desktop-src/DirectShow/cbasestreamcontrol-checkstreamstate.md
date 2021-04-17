---
description: O método CheckStreamState determina se um exemplo de mídia deve ser entregue ou descartado.
ms.assetid: 1533f4b9-e13e-458b-9614-96d733cef4ed
title: Método CBaseStreamControl. CheckStreamState (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.CheckStreamState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e469e288e853ca88a0cf15c209882a8114e33509
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748213"
---
# <a name="cbasestreamcontrolcheckstreamstate-method"></a><span data-ttu-id="bfdec-103">Método CBaseStreamControl. CheckStreamState</span><span class="sxs-lookup"><span data-stu-id="bfdec-103">CBaseStreamControl.CheckStreamState method</span></span>

<span data-ttu-id="bfdec-104">O `CheckStreamState` método determina se um exemplo de mídia deve ser entregue ou descartado.</span><span class="sxs-lookup"><span data-stu-id="bfdec-104">The `CheckStreamState` method determines whether a media sample should be delivered or discarded.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfdec-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bfdec-105">Syntax</span></span>


```C++
enum CheckStreamState(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="bfdec-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bfdec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfdec-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="bfdec-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="bfdec-108">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.</span><span class="sxs-lookup"><span data-stu-id="bfdec-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfdec-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bfdec-109">Return value</span></span>

<span data-ttu-id="bfdec-110">Retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="bfdec-110">Returns one of the following values.</span></span>



| <span data-ttu-id="bfdec-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="bfdec-111">Return code</span></span>                                                                                       | <span data-ttu-id="bfdec-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="bfdec-112">Description</span></span>                     |
|---------------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="bfdec-113"><dt>**descartando o fluxo \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bfdec-113"><dt>**STREAM\_DISCARDING**</dt></span></span> </dl> | <span data-ttu-id="bfdec-114">Descartar este exemplo.</span><span class="sxs-lookup"><span data-stu-id="bfdec-114">Discard this sample.</span></span><br/> |
| <dl> <span data-ttu-id="bfdec-115"><dt>**FLUXO \_ fluindo**</dt></span><span class="sxs-lookup"><span data-stu-id="bfdec-115"><dt>**STREAM\_FLOWING**</dt></span></span> </dl>    | <span data-ttu-id="bfdec-116">Forneça este exemplo.</span><span class="sxs-lookup"><span data-stu-id="bfdec-116">Deliver this sample.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bfdec-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="bfdec-117">Remarks</span></span>

<span data-ttu-id="bfdec-118">Chame esse método quando o PIN receber uma amostra.</span><span class="sxs-lookup"><span data-stu-id="bfdec-118">Call this method when your pin receives a sample.</span></span> <span data-ttu-id="bfdec-119">Entregue o exemplo somente se o valor de retorno for fluxo \_ fluindo.</span><span class="sxs-lookup"><span data-stu-id="bfdec-119">Deliver the sample only if the return value is STREAM\_FLOWING.</span></span> <span data-ttu-id="bfdec-120">Se o valor de retorno for \_ DEScartando o fluxo, descarte o exemplo.</span><span class="sxs-lookup"><span data-stu-id="bfdec-120">If the return value is STREAM\_DISCARDING, discard the sample.</span></span>

<span data-ttu-id="bfdec-121">Se o PIN descartar quaisquer exemplos, ele deverá marcar o próximo exemplo que ele fornece como uma descontinuidade, chamando o método [**IMediaSample:: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) .</span><span class="sxs-lookup"><span data-stu-id="bfdec-121">If the pin discards any samples, it should mark the next sample that it delivers as a discontinuity, by calling the [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) method.</span></span>

<span data-ttu-id="bfdec-122">Se o filtro implementar a interface [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) para contar quantos quadros eles descartam, não conte um quadro Descartado como um quadro solto.</span><span class="sxs-lookup"><span data-stu-id="bfdec-122">If your filter implements the [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) interface to count how many frames it drops, do not count a discarded frame as a dropped frame.</span></span>

<span data-ttu-id="bfdec-123">Quando o valor de retorno é \_ DEScartando o fluxo, o método é bloqueado até que o tempo de referência atinja a hora de início do exemplo.</span><span class="sxs-lookup"><span data-stu-id="bfdec-123">When the return value is STREAM\_DISCARDING, the method blocks until the reference time reaches the sample's start time.</span></span> <span data-ttu-id="bfdec-124">Isso impede que seu PIN descartasse amostras muito rapidamente.</span><span class="sxs-lookup"><span data-stu-id="bfdec-124">This prevents your pin from discarding samples too quickly.</span></span> <span data-ttu-id="bfdec-125">Se o filtro for pausado, o tempo de espera será infinito, até que o filtro seja executado, pare ou libere dados.</span><span class="sxs-lookup"><span data-stu-id="bfdec-125">If the filter is paused, the wait time is infinite, until the filter runs, stops, or flushes data.</span></span> <span data-ttu-id="bfdec-126">(As alterações de estado de filtro e o streaming acontecem em threads separados, portanto, isso não causa nenhum deadlock.)</span><span class="sxs-lookup"><span data-stu-id="bfdec-126">(Filter state changes and streaming happen on separate threads, so this does not cause any deadlock.)</span></span>

<span data-ttu-id="bfdec-127">A enumeração **CBaseStreamControl:: StreamControlState** é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="bfdec-127">The **CBaseStreamControl::StreamControlState** enumeration is defined as follows:</span></span>


```C++
enum StreamControlState{ 
    STREAM_FLOWING = 0x1000,
    STREAM_DISCARDING
};
```



## <a name="examples"></a><span data-ttu-id="bfdec-128">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bfdec-128">Examples</span></span>

<span data-ttu-id="bfdec-129">O exemplo a seguir pressupõe que o PIN usa uma variável de membro chamada m \_ fLastSampleDiscarded para controlar o descontinuidades.</span><span class="sxs-lookup"><span data-stu-id="bfdec-129">The following example assumes that the pin uses a member variable named m\_fLastSampleDiscarded to keep track of discontinuities.</span></span>


```C++
CMyPin::Receive(IMediaSample *pSample)
{
    if (!pSample) return E_POINTER;

    int iStreamState = CheckStreamState(pSample);
    if (iStreamState == STREAM_FLOWING) 
    {
        if (m_fLastSampleDiscarded)
            pSample->SetDiscontinuity(TRUE);
        m_fLastSampleDiscarded = FALSE;
        /* Deliver the sample. */
    } 
    else 
    {
        m_fLastSampleDiscarded = TRUE;  
       // Discard this sample. Do not deliver it.
    }
}
```



## <a name="requirements"></a><span data-ttu-id="bfdec-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfdec-130">Requirements</span></span>



| <span data-ttu-id="bfdec-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfdec-131">Requirement</span></span> | <span data-ttu-id="bfdec-132">Valor</span><span class="sxs-lookup"><span data-stu-id="bfdec-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfdec-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bfdec-133">Header</span></span><br/>  | <dl> <span data-ttu-id="bfdec-134"><dt>Strmctl. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bfdec-134"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bfdec-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bfdec-135">Library</span></span><br/> | <dl> <span data-ttu-id="bfdec-136"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="bfdec-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfdec-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="bfdec-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfdec-138">**Classe CBaseStreamControl**</span><span class="sxs-lookup"><span data-stu-id="bfdec-138">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 





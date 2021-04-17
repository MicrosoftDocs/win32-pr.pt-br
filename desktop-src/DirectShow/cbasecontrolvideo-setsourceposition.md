---
description: O método SetSourcePosition define uma nova posição de origem para o vídeo.
ms.assetid: e3c9ce31-9c24-4ef5-9526-ef6b890f5109
title: Método CBaseControlVideo. SetSourcePosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetSourcePosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5493779b623108f713f8da252e8696140883395b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748836"
---
# <a name="cbasecontrolvideosetsourceposition-method"></a><span data-ttu-id="0615b-103">Método CBaseControlVideo. SetSourcePosition</span><span class="sxs-lookup"><span data-stu-id="0615b-103">CBaseControlVideo.SetSourcePosition method</span></span>

<span data-ttu-id="0615b-104">O `SetSourcePosition` método define uma nova posição de origem para o vídeo.</span><span class="sxs-lookup"><span data-stu-id="0615b-104">The `SetSourcePosition` method sets a new source position for the video.</span></span>

## <a name="syntax"></a><span data-ttu-id="0615b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0615b-105">Syntax</span></span>


```C++
HRESULT SetSourcePosition(
   long Left,
   long Top,
   long Width,
   long Height
);
```



## <a name="parameters"></a><span data-ttu-id="0615b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0615b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0615b-107">*Mantida*</span><span class="sxs-lookup"><span data-stu-id="0615b-107">*Left*</span></span> 
</dt> <dd>

<span data-ttu-id="0615b-108">Nova coordenada esquerda.</span><span class="sxs-lookup"><span data-stu-id="0615b-108">New left coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="0615b-109">*Top*</span><span class="sxs-lookup"><span data-stu-id="0615b-109">*Top*</span></span> 
</dt> <dd>

<span data-ttu-id="0615b-110">Nova coordenada superior.</span><span class="sxs-lookup"><span data-stu-id="0615b-110">New top coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="0615b-111">*Largura*</span><span class="sxs-lookup"><span data-stu-id="0615b-111">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="0615b-112">Nova largura.</span><span class="sxs-lookup"><span data-stu-id="0615b-112">New width.</span></span>

</dd> <dt>

<span data-ttu-id="0615b-113">*Altura*</span><span class="sxs-lookup"><span data-stu-id="0615b-113">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="0615b-114">Nova altura.</span><span class="sxs-lookup"><span data-stu-id="0615b-114">New height.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0615b-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0615b-115">Return value</span></span>

<span data-ttu-id="0615b-116">Retorna um valor **HRESULT** que depende da implementação; pode ser um dos valores a seguir ou outros valores não listados.</span><span class="sxs-lookup"><span data-stu-id="0615b-116">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="0615b-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0615b-117">Return code</span></span>                                                                                           | <span data-ttu-id="0615b-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="0615b-118">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0615b-119"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="0615b-119"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="0615b-120">Falha.</span><span class="sxs-lookup"><span data-stu-id="0615b-120">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="0615b-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0615b-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="0615b-122">Argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="0615b-122">Invalid argument.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="0615b-123"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="0615b-123"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="0615b-124">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="0615b-124">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="0615b-125"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="0615b-125"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="0615b-126">Êxito.</span><span class="sxs-lookup"><span data-stu-id="0615b-126">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="0615b-127"><dt>**VFW \_ E \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="0615b-127"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="0615b-128">A operação não pode ser executada porque os Pins não estão conectados.</span><span class="sxs-lookup"><span data-stu-id="0615b-128">The operation cannot be performed because the pins are not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0615b-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="0615b-129">Remarks</span></span>

<span data-ttu-id="0615b-130">Um aplicativo pode alterar os retângulos de origem e de destino para o vídeo por meio da interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="0615b-130">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="0615b-131">O retângulo de origem afeta qual seção da fonte de vídeo nativa será exibida na exibição; o retângulo de destino afeta o local em que o vídeo será exibido quando for reproduzido.</span><span class="sxs-lookup"><span data-stu-id="0615b-131">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="0615b-132">O retângulo de destino é relativo à área do cliente da janela na qual está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="0615b-132">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="0615b-133">O canto superior esquerdo da janela é coordenada (0, 0).</span><span class="sxs-lookup"><span data-stu-id="0615b-133">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="0615b-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0615b-134">Requirements</span></span>



| <span data-ttu-id="0615b-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="0615b-135">Requirement</span></span> | <span data-ttu-id="0615b-136">Valor</span><span class="sxs-lookup"><span data-stu-id="0615b-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0615b-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0615b-137">Header</span></span><br/>  | <dl> <span data-ttu-id="0615b-138"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0615b-138"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0615b-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0615b-139">Library</span></span><br/> | <dl> <span data-ttu-id="0615b-140"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0615b-140"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0615b-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="0615b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0615b-142">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="0615b-142">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





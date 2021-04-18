---
description: O \_ método Put SourceLeft define a coordenada esquerda do retângulo de origem.
ms.assetid: 94511eb7-0255-4e53-a9c6-62c8c47f197a
title: Método de CBaseControlVideo.put_SourceLeft (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.put_SourceLeft
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ae678b060cd228fe7bf073690d87e3b831e78f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758878"
---
# <a name="cbasecontrolvideoput_sourceleft-method"></a><span data-ttu-id="20f3f-103">Método CBaseControlVideo. put \_ SourceLeft</span><span class="sxs-lookup"><span data-stu-id="20f3f-103">CBaseControlVideo.put\_SourceLeft method</span></span>

<span data-ttu-id="20f3f-104">O `put_SourceLeft` método define a coordenada esquerda do retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="20f3f-104">The `put_SourceLeft` method sets the source rectangle left coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="20f3f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20f3f-105">Syntax</span></span>


```C++
HRESULT put_SourceLeft(
   long SourceLeft
);
```



## <a name="parameters"></a><span data-ttu-id="20f3f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20f3f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20f3f-107">*SourceLeft*</span><span class="sxs-lookup"><span data-stu-id="20f3f-107">*SourceLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="20f3f-108">Nova coordenada esquerda do retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="20f3f-108">New left coordinate of the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20f3f-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="20f3f-109">Return value</span></span>

<span data-ttu-id="20f3f-110">Retorna um valor **HRESULT** que depende da implementação; pode ser um dos valores a seguir ou outros valores não listados.</span><span class="sxs-lookup"><span data-stu-id="20f3f-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="20f3f-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="20f3f-111">Return code</span></span>                                                                                           | <span data-ttu-id="20f3f-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="20f3f-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="20f3f-113"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="20f3f-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="20f3f-114">Falha.</span><span class="sxs-lookup"><span data-stu-id="20f3f-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="20f3f-115"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="20f3f-115"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="20f3f-116">Argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="20f3f-116">Invalid argument.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="20f3f-117"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="20f3f-117"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="20f3f-118">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="20f3f-118">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="20f3f-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="20f3f-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="20f3f-120">Êxito.</span><span class="sxs-lookup"><span data-stu-id="20f3f-120">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="20f3f-121"><dt>**VFW \_ E \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="20f3f-121"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="20f3f-122">A operação não pode ser executada porque os Pins não estão conectados.</span><span class="sxs-lookup"><span data-stu-id="20f3f-122">The operation cannot be performed because the pins are not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="20f3f-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="20f3f-123">Remarks</span></span>

<span data-ttu-id="20f3f-124">Um aplicativo pode alterar os retângulos de origem e de destino para o vídeo por meio da interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="20f3f-124">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="20f3f-125">O retângulo de origem afeta qual seção da fonte de vídeo nativa será exibida na exibição; o retângulo de destino afeta o local em que o vídeo será exibido quando for reproduzido.</span><span class="sxs-lookup"><span data-stu-id="20f3f-125">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="20f3f-126">O retângulo de destino é relativo à área do cliente da janela na qual está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="20f3f-126">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="20f3f-127">O canto superior esquerdo da janela é coordenada (0, 0).</span><span class="sxs-lookup"><span data-stu-id="20f3f-127">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="20f3f-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20f3f-128">Requirements</span></span>



| <span data-ttu-id="20f3f-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="20f3f-129">Requirement</span></span> | <span data-ttu-id="20f3f-130">Valor</span><span class="sxs-lookup"><span data-stu-id="20f3f-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20f3f-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="20f3f-131">Header</span></span><br/>  | <dl> <span data-ttu-id="20f3f-132"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="20f3f-132"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="20f3f-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="20f3f-133">Library</span></span><br/> | <dl> <span data-ttu-id="20f3f-134"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="20f3f-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20f3f-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="20f3f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20f3f-136">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="20f3f-136">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





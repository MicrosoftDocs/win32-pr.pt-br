---
description: O \_ método Get SourceWidth recupera a largura do retângulo de origem atual.
ms.assetid: e8e27f8f-57e5-489c-aae7-86493677b380
title: Método de CBaseControlVideo.get_SourceWidth (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_SourceWidth
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60a78fe647ebf488a47907c058962f13790f2538
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747620"
---
# <a name="cbasecontrolvideoget_sourcewidth-method"></a><span data-ttu-id="c628a-103">CBaseControlVideo. obter \_ método SourceWidth</span><span class="sxs-lookup"><span data-stu-id="c628a-103">CBaseControlVideo.get\_SourceWidth method</span></span>

<span data-ttu-id="c628a-104">O `get_SourceWidth` método recupera a largura do retângulo de origem atual.</span><span class="sxs-lookup"><span data-stu-id="c628a-104">The `get_SourceWidth` method retrieves the width of the current source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="c628a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c628a-105">Syntax</span></span>


```C++
HRESULT get_SourceWidth(
   long *pSourceWidth
);
```



## <a name="parameters"></a><span data-ttu-id="c628a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c628a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c628a-107">*pSourceWidth*</span><span class="sxs-lookup"><span data-stu-id="c628a-107">*pSourceWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="c628a-108">Ponteiro para a largura do retângulo de origem atual.</span><span class="sxs-lookup"><span data-stu-id="c628a-108">Pointer to the width of the current source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c628a-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c628a-109">Return value</span></span>

<span data-ttu-id="c628a-110">Retorna um valor **HRESULT** que depende da implementação; pode ser um dos valores a seguir ou outros valores não listados.</span><span class="sxs-lookup"><span data-stu-id="c628a-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="c628a-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c628a-111">Return code</span></span>                                                                                           | <span data-ttu-id="c628a-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="c628a-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c628a-113"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="c628a-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="c628a-114">Falha.</span><span class="sxs-lookup"><span data-stu-id="c628a-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="c628a-115"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="c628a-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="c628a-116">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="c628a-116">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="c628a-117"><dt>**VFW \_ E \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="c628a-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="c628a-118">A operação não pode ser executada porque os Pins não estão conectados.</span><span class="sxs-lookup"><span data-stu-id="c628a-118">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="c628a-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="c628a-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="c628a-120">Êxito.</span><span class="sxs-lookup"><span data-stu-id="c628a-120">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="c628a-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="c628a-121">Remarks</span></span>

<span data-ttu-id="c628a-122">Essa função de membro implementa o método [**IBasicVideo:: get \_ SourceWidth**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_sourcewidth) .</span><span class="sxs-lookup"><span data-stu-id="c628a-122">This member function implements the [**IBasicVideo::get\_SourceWidth**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_sourcewidth) method.</span></span>

<span data-ttu-id="c628a-123">Um aplicativo pode alterar os retângulos de origem e de destino para o vídeo por meio da interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="c628a-123">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="c628a-124">O retângulo de origem afeta qual seção da fonte de vídeo nativa será exibida na exibição; o retângulo de destino afeta o local em que o vídeo será exibido quando for reproduzido.</span><span class="sxs-lookup"><span data-stu-id="c628a-124">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="c628a-125">O retângulo de destino é relativo à área do cliente da janela na qual está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="c628a-125">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="c628a-126">O canto superior esquerdo da janela é coordenada (0, 0).</span><span class="sxs-lookup"><span data-stu-id="c628a-126">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="c628a-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c628a-127">Requirements</span></span>



| <span data-ttu-id="c628a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c628a-128">Requirement</span></span> | <span data-ttu-id="c628a-129">Valor</span><span class="sxs-lookup"><span data-stu-id="c628a-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c628a-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c628a-130">Header</span></span><br/>  | <dl> <span data-ttu-id="c628a-131"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c628a-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c628a-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c628a-132">Library</span></span><br/> | <dl> <span data-ttu-id="c628a-133"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c628a-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c628a-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="c628a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c628a-135">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="c628a-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





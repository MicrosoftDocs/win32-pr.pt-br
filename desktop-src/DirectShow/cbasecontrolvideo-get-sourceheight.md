---
description: O \_ método Get SourceHeight recupera a altura do retângulo de origem atual.
ms.assetid: bf727cf6-9143-41f0-a482-782a4178ea92
title: Método de CBaseControlVideo.get_SourceHeight (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_SourceHeight
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b724f63907c8372867095b059ff728b4c646df21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752917"
---
# <a name="cbasecontrolvideoget_sourceheight-method"></a><span data-ttu-id="bb2f1-103">CBaseControlVideo. obter \_ método SourceHeight</span><span class="sxs-lookup"><span data-stu-id="bb2f1-103">CBaseControlVideo.get\_SourceHeight method</span></span>

<span data-ttu-id="bb2f1-104">O `get_SourceHeight` método recupera a altura do retângulo de origem atual.</span><span class="sxs-lookup"><span data-stu-id="bb2f1-104">The `get_SourceHeight` method retrieves the height of the current source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb2f1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bb2f1-105">Syntax</span></span>


```C++
HRESULT get_SourceHeight(
   long *pSourceHeight
);
```



## <a name="parameters"></a><span data-ttu-id="bb2f1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bb2f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb2f1-107">*pSourceHeight*</span><span class="sxs-lookup"><span data-stu-id="bb2f1-107">*pSourceHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="bb2f1-108">Ponteiro para a altura do retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="bb2f1-108">Pointer to the height of the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb2f1-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bb2f1-109">Return value</span></span>

<span data-ttu-id="bb2f1-110">Retorna um valor **HRESULT** que depende da implementação; pode ser um dos valores a seguir ou outros valores não listados.</span><span class="sxs-lookup"><span data-stu-id="bb2f1-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="bb2f1-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="bb2f1-111">Return code</span></span>                                                                                           | <span data-ttu-id="bb2f1-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="bb2f1-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bb2f1-113"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="bb2f1-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="bb2f1-114">Falha.</span><span class="sxs-lookup"><span data-stu-id="bb2f1-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="bb2f1-115"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="bb2f1-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="bb2f1-116">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="bb2f1-116">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="bb2f1-117"><dt>**VFW \_ E \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="bb2f1-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="bb2f1-118">A operação não pode ser executada porque os Pins não estão conectados.</span><span class="sxs-lookup"><span data-stu-id="bb2f1-118">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="bb2f1-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="bb2f1-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="bb2f1-120">Êxito.</span><span class="sxs-lookup"><span data-stu-id="bb2f1-120">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="bb2f1-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb2f1-121">Remarks</span></span>

<span data-ttu-id="bb2f1-122">Essa função de membro implementa o método [**IBasicVideo:: get \_ SourceHeight**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_sourceheight) .</span><span class="sxs-lookup"><span data-stu-id="bb2f1-122">This member function implements the [**IBasicVideo::get\_SourceHeight**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_sourceheight) method.</span></span>

<span data-ttu-id="bb2f1-123">Um aplicativo pode alterar os retângulos de origem e de destino para o vídeo por meio da interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="bb2f1-123">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="bb2f1-124">O retângulo de origem afeta qual seção da fonte de vídeo nativa será exibida na exibição; o retângulo de destino afeta o local em que o vídeo será exibido quando for reproduzido.</span><span class="sxs-lookup"><span data-stu-id="bb2f1-124">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="bb2f1-125">O retângulo de destino é relativo à área do cliente da janela na qual está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="bb2f1-125">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="bb2f1-126">O canto superior esquerdo da janela é coordenada (0, 0).</span><span class="sxs-lookup"><span data-stu-id="bb2f1-126">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="bb2f1-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb2f1-127">Requirements</span></span>



| <span data-ttu-id="bb2f1-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb2f1-128">Requirement</span></span> | <span data-ttu-id="bb2f1-129">Valor</span><span class="sxs-lookup"><span data-stu-id="bb2f1-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb2f1-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bb2f1-130">Header</span></span><br/>  | <dl> <span data-ttu-id="bb2f1-131"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bb2f1-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bb2f1-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bb2f1-132">Library</span></span><br/> | <dl> <span data-ttu-id="bb2f1-133"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="bb2f1-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb2f1-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb2f1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb2f1-135">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="bb2f1-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





---
description: O método GetDestinationPosition recupera o retângulo de destino em uma operação atômica.
ms.assetid: 780cbcb5-1db5-4087-8c51-350183cfca31
title: Método CBaseControlVideo. GetDestinationPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetDestinationPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c86ed919af270df508eb8f76e32597b410dec56b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752727"
---
# <a name="cbasecontrolvideogetdestinationposition-method"></a><span data-ttu-id="b2852-103">Método CBaseControlVideo. GetDestinationPosition</span><span class="sxs-lookup"><span data-stu-id="b2852-103">CBaseControlVideo.GetDestinationPosition method</span></span>

<span data-ttu-id="b2852-104">O `GetDestinationPosition` método recupera o retângulo de destino em uma operação atômica.</span><span class="sxs-lookup"><span data-stu-id="b2852-104">The `GetDestinationPosition` method retrieves the destination rectangle in one atomic operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2852-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b2852-105">Syntax</span></span>


```C++
HRESULT GetDestinationPosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="b2852-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b2852-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2852-107">*pLeft*</span><span class="sxs-lookup"><span data-stu-id="b2852-107">*pLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="b2852-108">Ponteiro para a coordenada esquerda do retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="b2852-108">Pointer to the left coordinate of the destination rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="b2852-109">*pTop*</span><span class="sxs-lookup"><span data-stu-id="b2852-109">*pTop*</span></span> 
</dt> <dd>

<span data-ttu-id="b2852-110">Ponteiro para a coordenada superior do retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="b2852-110">Pointer to the top coordinate of the destination rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="b2852-111">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="b2852-111">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="b2852-112">Ponteiro para a largura do retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="b2852-112">Pointer to the width of the destination rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="b2852-113">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="b2852-113">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="b2852-114">Ponteiro para a altura do retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="b2852-114">Pointer to the height of the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2852-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b2852-115">Return value</span></span>

<span data-ttu-id="b2852-116">Retorna um valor **HRESULT** que depende da implementação; pode ser um dos valores a seguir ou outros valores não listados.</span><span class="sxs-lookup"><span data-stu-id="b2852-116">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="b2852-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b2852-117">Return code</span></span>                                                                                           | <span data-ttu-id="b2852-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="b2852-118">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b2852-119"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="b2852-119"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="b2852-120">Falha.</span><span class="sxs-lookup"><span data-stu-id="b2852-120">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="b2852-121"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="b2852-121"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="b2852-122">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="b2852-122">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="b2852-123"><dt>**VFW \_ E \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="b2852-123"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="b2852-124">A operação não pode ser executada porque os Pins não estão conectados.</span><span class="sxs-lookup"><span data-stu-id="b2852-124">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="b2852-125"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="b2852-125"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="b2852-126">Êxito.</span><span class="sxs-lookup"><span data-stu-id="b2852-126">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="b2852-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2852-127">Remarks</span></span>

<span data-ttu-id="b2852-128">Essa função de membro pode ser usada em vez de chamadas separadas para as funções de membro [**CBaseControlVideo:: get \_ DestinationLeft**](cbasecontrolvideo-get-destinationleft.md), [**CBaseControlVideo:: get \_ DestinationTop**](cbasecontrolvideo-get-destinationtop.md), [**CBaseControlVideo:: get \_ DestinationWidth**](cbasecontrolvideo-get-destinationwidth.md)e [**CBaseControlVideo:: get \_ DestinationHeight**](cbasecontrolvideo-get-destinationheight.md) .</span><span class="sxs-lookup"><span data-stu-id="b2852-128">This member function can be used in place of separate calls to the [**CBaseControlVideo::get\_DestinationLeft**](cbasecontrolvideo-get-destinationleft.md), [**CBaseControlVideo::get\_DestinationTop**](cbasecontrolvideo-get-destinationtop.md), [**CBaseControlVideo::get\_DestinationWidth**](cbasecontrolvideo-get-destinationwidth.md), and [**CBaseControlVideo::get\_DestinationHeight**](cbasecontrolvideo-get-destinationheight.md) member functions.</span></span> <span data-ttu-id="b2852-129">Um aplicativo pode alterar os retângulos de origem e de destino para o vídeo por meio da interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="b2852-129">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="b2852-130">O retângulo de origem afeta qual seção da fonte de vídeo nativa será exibida na exibição; o retângulo de destino afeta o local em que o vídeo será exibido quando for reproduzido.</span><span class="sxs-lookup"><span data-stu-id="b2852-130">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="b2852-131">O retângulo de destino é relativo à área do cliente da janela na qual está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="b2852-131">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="b2852-132">O canto superior esquerdo da janela é coordenada (0, 0).</span><span class="sxs-lookup"><span data-stu-id="b2852-132">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="b2852-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2852-133">Requirements</span></span>



| <span data-ttu-id="b2852-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2852-134">Requirement</span></span> | <span data-ttu-id="b2852-135">Valor</span><span class="sxs-lookup"><span data-stu-id="b2852-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2852-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b2852-136">Header</span></span><br/>  | <dl> <span data-ttu-id="b2852-137"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b2852-137"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b2852-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b2852-138">Library</span></span><br/> | <dl> <span data-ttu-id="b2852-139"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b2852-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2852-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2852-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2852-141">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="b2852-141">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





---
description: O método SetDefaultSourcePosition define o renderizador de volta para usando a posição de origem padrão (normalmente, todo o vídeo nativo).
ms.assetid: 1ac03298-4c25-45f7-9719-ea03fe4699b2
title: Método CBaseControlVideo. SetDefaultSourcePosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultSourcePosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e6296683235a3cf051d0b9f4ee56ce51a3516f66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755998"
---
# <a name="cbasecontrolvideosetdefaultsourceposition-method"></a><span data-ttu-id="a63d3-103">Método CBaseControlVideo. SetDefaultSourcePosition</span><span class="sxs-lookup"><span data-stu-id="a63d3-103">CBaseControlVideo.SetDefaultSourcePosition method</span></span>

<span data-ttu-id="a63d3-104">O `SetDefaultSourcePosition` método define o renderizador de volta para usar a posição de origem padrão (normalmente, todo o vídeo nativo).</span><span class="sxs-lookup"><span data-stu-id="a63d3-104">The `SetDefaultSourcePosition` method sets the renderer back to using the default source position (typically all the native video).</span></span>

## <a name="syntax"></a><span data-ttu-id="a63d3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a63d3-105">Syntax</span></span>


```C++
HRESULT SetDefaultSourcePosition();
```



## <a name="parameters"></a><span data-ttu-id="a63d3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a63d3-106">Parameters</span></span>

<span data-ttu-id="a63d3-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a63d3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a63d3-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a63d3-108">Return value</span></span>

<span data-ttu-id="a63d3-109">Retorna um valor **HRESULT** que depende da implementação; pode ser um dos valores a seguir ou outros valores não listados.</span><span class="sxs-lookup"><span data-stu-id="a63d3-109">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="a63d3-110">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a63d3-110">Return code</span></span>                                                                                           | <span data-ttu-id="a63d3-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="a63d3-111">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a63d3-112"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="a63d3-112"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="a63d3-113">Falha.</span><span class="sxs-lookup"><span data-stu-id="a63d3-113">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="a63d3-114"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="a63d3-114"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="a63d3-115">Êxito.</span><span class="sxs-lookup"><span data-stu-id="a63d3-115">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="a63d3-116"><dt>**VFW \_ E \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="a63d3-116"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="a63d3-117">A operação não pode ser executada porque os Pins não estão conectados.</span><span class="sxs-lookup"><span data-stu-id="a63d3-117">The operation cannot be performed because the pins are not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a63d3-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="a63d3-118">Remarks</span></span>

<span data-ttu-id="a63d3-119">Um aplicativo pode alterar os retângulos de origem e de destino para o vídeo por meio da interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="a63d3-119">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="a63d3-120">O retângulo de origem afeta qual seção da fonte de vídeo nativa será exibida na exibição; o retângulo de destino afeta o local em que o vídeo será exibido quando for reproduzido.</span><span class="sxs-lookup"><span data-stu-id="a63d3-120">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="a63d3-121">O retângulo de destino é relativo à área do cliente da janela na qual está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="a63d3-121">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="a63d3-122">O canto superior esquerdo da janela é coordenada (0, 0).</span><span class="sxs-lookup"><span data-stu-id="a63d3-122">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="a63d3-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a63d3-123">Requirements</span></span>



| <span data-ttu-id="a63d3-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a63d3-124">Requirement</span></span> | <span data-ttu-id="a63d3-125">Valor</span><span class="sxs-lookup"><span data-stu-id="a63d3-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a63d3-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a63d3-126">Header</span></span><br/>  | <dl> <span data-ttu-id="a63d3-127"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a63d3-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a63d3-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a63d3-128">Library</span></span><br/> | <dl> <span data-ttu-id="a63d3-129"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a63d3-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a63d3-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="a63d3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a63d3-131">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="a63d3-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





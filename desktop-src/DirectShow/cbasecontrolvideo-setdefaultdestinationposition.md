---
description: O método SetDefaultDestinationPosition define o renderizador de volta para usar a posição de destino padrão (normalmente a área inteira do cliente da janela).
ms.assetid: 228259d7-2f1f-4528-8c8a-d20d7542523c
title: Método CBaseControlVideo. SetDefaultDestinationPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultDestinationPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a959f462d410b83588fb1a8df87cebffd879d8ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754569"
---
# <a name="cbasecontrolvideosetdefaultdestinationposition-method"></a><span data-ttu-id="11a8c-103">Método CBaseControlVideo. SetDefaultDestinationPosition</span><span class="sxs-lookup"><span data-stu-id="11a8c-103">CBaseControlVideo.SetDefaultDestinationPosition method</span></span>

<span data-ttu-id="11a8c-104">O `SetDefaultDestinationPosition` método define o renderizador de volta para usar a posição de destino padrão (normalmente a área inteira do cliente da janela).</span><span class="sxs-lookup"><span data-stu-id="11a8c-104">The `SetDefaultDestinationPosition` method sets the renderer back to using the default destination position (typically the entire window client area).</span></span>

## <a name="syntax"></a><span data-ttu-id="11a8c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="11a8c-105">Syntax</span></span>


```C++
HRESULT SetDefaultDestinationPosition();
```



## <a name="parameters"></a><span data-ttu-id="11a8c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11a8c-106">Parameters</span></span>

<span data-ttu-id="11a8c-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="11a8c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="11a8c-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="11a8c-108">Return value</span></span>

<span data-ttu-id="11a8c-109">Retorna um valor **HRESULT** que depende da implementação; pode ser um dos valores a seguir ou outros valores não listados.</span><span class="sxs-lookup"><span data-stu-id="11a8c-109">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="11a8c-110">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="11a8c-110">Return code</span></span>                                                                                           | <span data-ttu-id="11a8c-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="11a8c-111">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="11a8c-112"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="11a8c-112"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="11a8c-113">Falha.</span><span class="sxs-lookup"><span data-stu-id="11a8c-113">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="11a8c-114"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="11a8c-114"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="11a8c-115">Êxito.</span><span class="sxs-lookup"><span data-stu-id="11a8c-115">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="11a8c-116"><dt>**VFW \_ E \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="11a8c-116"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="11a8c-117">A operação não pode ser executada porque os Pins não estão conectados.</span><span class="sxs-lookup"><span data-stu-id="11a8c-117">The operation cannot be performed because the pins are not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="11a8c-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="11a8c-118">Remarks</span></span>

<span data-ttu-id="11a8c-119">Um aplicativo pode alterar os retângulos de origem e de destino para o vídeo por meio da interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="11a8c-119">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="11a8c-120">O retângulo de origem afeta qual seção da fonte de vídeo nativa será exibida na exibição; o retângulo de destino afeta o local em que o vídeo será exibido quando for reproduzido.</span><span class="sxs-lookup"><span data-stu-id="11a8c-120">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="11a8c-121">O retângulo de destino é relativo à área do cliente da janela na qual está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="11a8c-121">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="11a8c-122">O canto superior esquerdo da janela é coordenada (0, 0).</span><span class="sxs-lookup"><span data-stu-id="11a8c-122">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="11a8c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11a8c-123">Requirements</span></span>



| <span data-ttu-id="11a8c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="11a8c-124">Requirement</span></span> | <span data-ttu-id="11a8c-125">Valor</span><span class="sxs-lookup"><span data-stu-id="11a8c-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11a8c-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="11a8c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="11a8c-127"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="11a8c-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="11a8c-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="11a8c-128">Library</span></span><br/> | <dl> <span data-ttu-id="11a8c-129"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="11a8c-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11a8c-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="11a8c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11a8c-131">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="11a8c-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





---
description: O \_ método Get SourceLeft recupera a coordenada esquerda do retângulo de origem atual.
ms.assetid: dbfb1850-6e49-481c-b26a-22ccb9e4455a
title: Método de CBaseControlVideo.get_SourceLeft (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_SourceLeft
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2b7ff62617b9fa378511dba2838f0dcbdb25dbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752526"
---
# <a name="cbasecontrolvideoget_sourceleft-method"></a><span data-ttu-id="4d780-103">CBaseControlVideo. obter \_ método SourceLeft</span><span class="sxs-lookup"><span data-stu-id="4d780-103">CBaseControlVideo.get\_SourceLeft method</span></span>

<span data-ttu-id="4d780-104">O `get_SourceLeft` método recupera a coordenada esquerda do retângulo de origem atual.</span><span class="sxs-lookup"><span data-stu-id="4d780-104">The `get_SourceLeft` method retrieves the left coordinate of the current source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d780-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4d780-105">Syntax</span></span>


```C++
HRESULT get_SourceLeft(
   long *pSourceLeft
);
```



## <a name="parameters"></a><span data-ttu-id="4d780-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4d780-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d780-107">*pSourceLeft*</span><span class="sxs-lookup"><span data-stu-id="4d780-107">*pSourceLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="4d780-108">Ponteiro para a coordenada esquerda do retângulo de origem atual.</span><span class="sxs-lookup"><span data-stu-id="4d780-108">Pointer to the left coordinate of the current source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d780-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4d780-109">Return value</span></span>

<span data-ttu-id="4d780-110">Retorna um valor **HRESULT** que depende da implementação; pode ser um dos valores a seguir ou outros valores não listados.</span><span class="sxs-lookup"><span data-stu-id="4d780-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="4d780-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="4d780-111">Return code</span></span>                                                                                           | <span data-ttu-id="4d780-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="4d780-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4d780-113"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="4d780-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="4d780-114">Falha.</span><span class="sxs-lookup"><span data-stu-id="4d780-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="4d780-115"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="4d780-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="4d780-116">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="4d780-116">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="4d780-117"><dt>**VFW \_ E \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="4d780-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="4d780-118">A operação não pode ser executada porque os Pins não estão conectados.</span><span class="sxs-lookup"><span data-stu-id="4d780-118">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="4d780-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="4d780-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="4d780-120">Êxito.</span><span class="sxs-lookup"><span data-stu-id="4d780-120">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="4d780-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="4d780-121">Remarks</span></span>

<span data-ttu-id="4d780-122">Um aplicativo pode alterar os retângulos de origem e de destino para o vídeo por meio da interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="4d780-122">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="4d780-123">O retângulo de origem afeta qual seção da fonte de vídeo nativa será exibida na exibição; o retângulo de destino afeta o local em que o vídeo será exibido quando for reproduzido.</span><span class="sxs-lookup"><span data-stu-id="4d780-123">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="4d780-124">O retângulo de destino é relativo à área do cliente da janela na qual está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="4d780-124">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="4d780-125">O canto superior esquerdo da janela é coordenada (0, 0).</span><span class="sxs-lookup"><span data-stu-id="4d780-125">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="4d780-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d780-126">Requirements</span></span>



| <span data-ttu-id="4d780-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d780-127">Requirement</span></span> | <span data-ttu-id="4d780-128">Valor</span><span class="sxs-lookup"><span data-stu-id="4d780-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d780-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4d780-129">Header</span></span><br/>  | <dl> <span data-ttu-id="4d780-130"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4d780-130"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4d780-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4d780-131">Library</span></span><br/> | <dl> <span data-ttu-id="4d780-132"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="4d780-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d780-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="4d780-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d780-134">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="4d780-134">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





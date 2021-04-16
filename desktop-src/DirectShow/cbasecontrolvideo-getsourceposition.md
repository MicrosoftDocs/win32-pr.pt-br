---
description: O método GetSourcePosition recupera a posição e as dimensões do retângulo de origem em uma operação atômica.
ms.assetid: 44356f62-8b14-4b0e-a587-f832adff3bba
title: Método CBaseControlVideo. GetSourcePosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetSourcePosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2422845a7b5c64bc07b8e8942b2f19cd10a54d26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753759"
---
# <a name="cbasecontrolvideogetsourceposition-method"></a><span data-ttu-id="2d5e1-103">Método CBaseControlVideo. GetSourcePosition</span><span class="sxs-lookup"><span data-stu-id="2d5e1-103">CBaseControlVideo.GetSourcePosition method</span></span>

<span data-ttu-id="2d5e1-104">O `GetSourcePosition` método recupera a posição e as dimensões do retângulo de origem em uma operação atômica.</span><span class="sxs-lookup"><span data-stu-id="2d5e1-104">The `GetSourcePosition` method retrieves the position and dimensions of the source rectangle in one atomic operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d5e1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d5e1-105">Syntax</span></span>


```C++
HRESULT GetSourcePosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="2d5e1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d5e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d5e1-107">*pLeft*</span><span class="sxs-lookup"><span data-stu-id="2d5e1-107">*pLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="2d5e1-108">Ponteiro para a coordenada esquerda do retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="2d5e1-108">Pointer to the left coordinate of the source rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="2d5e1-109">*pTop*</span><span class="sxs-lookup"><span data-stu-id="2d5e1-109">*pTop*</span></span> 
</dt> <dd>

<span data-ttu-id="2d5e1-110">Ponteiro para a coordenada superior do retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="2d5e1-110">Pointer to the top coordinate of the source rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="2d5e1-111">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="2d5e1-111">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="2d5e1-112">Ponteiro para a largura do retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="2d5e1-112">Pointer to the width of the source rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="2d5e1-113">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="2d5e1-113">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="2d5e1-114">Ponteiro para a altura do retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="2d5e1-114">Pointer to the height of the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d5e1-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2d5e1-115">Return value</span></span>

<span data-ttu-id="2d5e1-116">Retorna um valor **HRESULT** que depende da implementação; pode ser um dos valores a seguir ou outros valores não listados.</span><span class="sxs-lookup"><span data-stu-id="2d5e1-116">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="2d5e1-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="2d5e1-117">Return code</span></span>                                                                                           | <span data-ttu-id="2d5e1-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="2d5e1-118">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2d5e1-119"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="2d5e1-119"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="2d5e1-120">Falha.</span><span class="sxs-lookup"><span data-stu-id="2d5e1-120">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="2d5e1-121"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="2d5e1-121"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="2d5e1-122">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="2d5e1-122">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="2d5e1-123"><dt>**VFW \_ E \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="2d5e1-123"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="2d5e1-124">A operação não pode ser executada porque os Pins não estão conectados.</span><span class="sxs-lookup"><span data-stu-id="2d5e1-124">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="2d5e1-125"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="2d5e1-125"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="2d5e1-126">Êxito.</span><span class="sxs-lookup"><span data-stu-id="2d5e1-126">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="2d5e1-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d5e1-127">Remarks</span></span>

<span data-ttu-id="2d5e1-128">Um aplicativo pode alterar os retângulos de origem e de destino para o vídeo por meio da interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="2d5e1-128">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="2d5e1-129">O retângulo de origem afeta qual seção da fonte de vídeo nativa será exibida na exibição; o retângulo de destino afeta o local em que o vídeo será exibido quando for reproduzido.</span><span class="sxs-lookup"><span data-stu-id="2d5e1-129">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="2d5e1-130">O retângulo de destino é relativo à área do cliente da janela na qual está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="2d5e1-130">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="2d5e1-131">O canto superior esquerdo da janela é coordenada (0, 0).</span><span class="sxs-lookup"><span data-stu-id="2d5e1-131">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="2d5e1-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d5e1-132">Requirements</span></span>



| <span data-ttu-id="2d5e1-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d5e1-133">Requirement</span></span> | <span data-ttu-id="2d5e1-134">Valor</span><span class="sxs-lookup"><span data-stu-id="2d5e1-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d5e1-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2d5e1-135">Header</span></span><br/>  | <dl> <span data-ttu-id="2d5e1-136"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2d5e1-136"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2d5e1-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2d5e1-137">Library</span></span><br/> | <dl> <span data-ttu-id="2d5e1-138"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="2d5e1-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d5e1-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d5e1-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d5e1-140">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="2d5e1-140">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





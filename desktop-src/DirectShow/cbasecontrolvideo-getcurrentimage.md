---
description: O método GetCurrentImage recupera uma cópia da imagem atual no renderizador.
ms.assetid: fa322bd2-18e4-481d-bde1-92deb0f7de61
title: Método CBaseControlVideo. GetCurrentImage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetCurrentImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d44e6930d0d7e179162939c13a54f2953c5ab965
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105767686"
---
# <a name="cbasecontrolvideogetcurrentimage-method"></a><span data-ttu-id="29147-103">Método CBaseControlVideo. GetCurrentImage</span><span class="sxs-lookup"><span data-stu-id="29147-103">CBaseControlVideo.GetCurrentImage method</span></span>

<span data-ttu-id="29147-104">O `GetCurrentImage` método recupera uma cópia da imagem atual no renderizador.</span><span class="sxs-lookup"><span data-stu-id="29147-104">The `GetCurrentImage` method retrieves a copy of the current image at the renderer.</span></span>

## <a name="syntax"></a><span data-ttu-id="29147-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="29147-105">Syntax</span></span>


```C++
HRESULT GetCurrentImage(
   long *pBufferSize,
   long *pVideoImage
);
```



## <a name="parameters"></a><span data-ttu-id="29147-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="29147-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29147-107">*pBufferSize*</span><span class="sxs-lookup"><span data-stu-id="29147-107">*pBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="29147-108">Ponteiro para o tamanho do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="29147-108">Pointer to the size of the output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="29147-109">*pVideoImage*</span><span class="sxs-lookup"><span data-stu-id="29147-109">*pVideoImage*</span></span> 
</dt> <dd>

<span data-ttu-id="29147-110">Ponteiro para o buffer de saída da imagem.</span><span class="sxs-lookup"><span data-stu-id="29147-110">Pointer to the output buffer for the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29147-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="29147-111">Return value</span></span>

<span data-ttu-id="29147-112">Retorna um valor **HRESULT** que depende da implementação; pode ser um dos valores a seguir ou outros valores não listados.</span><span class="sxs-lookup"><span data-stu-id="29147-112">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="29147-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="29147-113">Return code</span></span>                                                                                        | <span data-ttu-id="29147-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="29147-114">Description</span></span>                                                                       |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="29147-115"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="29147-115"><dt>**E\_FAIL**</dt></span></span> </dl>             | <span data-ttu-id="29147-116">Falha.</span><span class="sxs-lookup"><span data-stu-id="29147-116">Failure.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="29147-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="29147-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>       | <span data-ttu-id="29147-118">Argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="29147-118">Invalid argument.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="29147-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="29147-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>      | <span data-ttu-id="29147-120">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="29147-120">Out of memory.</span></span> <span data-ttu-id="29147-121">Retornado quando o parâmetro *pVideoInfo* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="29147-121">Returned when the *pVideoInfo* parameter is **NULL**.</span></span><br/>   |
| <dl> <span data-ttu-id="29147-122"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="29147-122"><dt>**NOERROR**</dt></span></span> </dl>             | <span data-ttu-id="29147-123">Êxito.</span><span class="sxs-lookup"><span data-stu-id="29147-123">Success.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="29147-124"><dt>**VFW \_ E \_ não em \_ pausa**</dt></span><span class="sxs-lookup"><span data-stu-id="29147-124"><dt>**VFW\_E\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="29147-125">A operação não pôde ser executada porque o filtro não está em pausa.</span><span class="sxs-lookup"><span data-stu-id="29147-125">The operation could not be performed because the filter is not paused.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="29147-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="29147-126">Remarks</span></span>

<span data-ttu-id="29147-127">Essa função de membro recupera a imagem do exemplo e a copia para o buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="29147-127">This member function retrieves the image from the sample and copies it into the output buffer.</span></span> <span data-ttu-id="29147-128">A seção de vídeo copiada no buffer de saída reflete o retângulo de origem definido por meio da interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="29147-128">The section of video copied into the output buffer reflects the source rectangle set through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="29147-129">Ele não reflete o retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="29147-129">It does not reflect the destination rectangle.</span></span>

## <a name="requirements"></a><span data-ttu-id="29147-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29147-130">Requirements</span></span>



| <span data-ttu-id="29147-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="29147-131">Requirement</span></span> | <span data-ttu-id="29147-132">Valor</span><span class="sxs-lookup"><span data-stu-id="29147-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29147-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="29147-133">Header</span></span><br/>  | <dl> <span data-ttu-id="29147-134"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="29147-134"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="29147-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="29147-135">Library</span></span><br/> | <dl> <span data-ttu-id="29147-136"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="29147-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29147-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="29147-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29147-138">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="29147-138">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





---
description: Cria uma cópia de memória de uma imagem.
ms.assetid: 83a980bc-1298-439f-8dfc-49534591977f
title: Método CBaseControlVideo. CopyImage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CopyImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 23ada87e77d3c3441f489abed2e7af86a2a556ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751285"
---
# <a name="cbasecontrolvideocopyimage-method"></a><span data-ttu-id="de294-103">Método CBaseControlVideo. CopyImage</span><span class="sxs-lookup"><span data-stu-id="de294-103">CBaseControlVideo.CopyImage method</span></span>

<span data-ttu-id="de294-104">Cria uma cópia de memória de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="de294-104">Creates a memory copy of an image.</span></span>

## <a name="syntax"></a><span data-ttu-id="de294-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de294-105">Syntax</span></span>


```C++
HRESULT CopyImage(
   IMediaSample    *pMediaSample,
   VIDEOINFOHEADER *pVideoInfo,
   LONG            *pBufferSize,
   BYTE            *pVideoImage,
   RECT            *pSourceRect
);
```



## <a name="parameters"></a><span data-ttu-id="de294-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="de294-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de294-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="de294-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="de294-108">Ponteiro para o exemplo que contém a imagem de vídeo.</span><span class="sxs-lookup"><span data-stu-id="de294-108">Pointer to the sample containing the video image.</span></span>

</dd> <dt>

<span data-ttu-id="de294-109">*pVideoInfo*</span><span class="sxs-lookup"><span data-stu-id="de294-109">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="de294-110">Ponteiro para o formato que representa a imagem de vídeo.</span><span class="sxs-lookup"><span data-stu-id="de294-110">Pointer to the format representing the video image.</span></span>

</dd> <dt>

<span data-ttu-id="de294-111">*pBufferSize*</span><span class="sxs-lookup"><span data-stu-id="de294-111">*pBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="de294-112">Ponteiro para o tamanho do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="de294-112">Pointer to the size of the output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="de294-113">*pVideoImage*</span><span class="sxs-lookup"><span data-stu-id="de294-113">*pVideoImage*</span></span> 
</dt> <dd>

<span data-ttu-id="de294-114">Ponteiro para o buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="de294-114">Pointer to the output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="de294-115">*pSourceRect*</span><span class="sxs-lookup"><span data-stu-id="de294-115">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="de294-116">Ponteiro para o retângulo de vídeo de origem.</span><span class="sxs-lookup"><span data-stu-id="de294-116">Pointer to the source video rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de294-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="de294-117">Return value</span></span>

<span data-ttu-id="de294-118">Se o parâmetro *pVideoImage* for **NULL**, o parâmetro *pBufferSize* será preenchido com o número de bytes que o buffer de saída exigirá para armazenar a imagem.</span><span class="sxs-lookup"><span data-stu-id="de294-118">If the *pVideoImage* parameter is **NULL**, the *pBufferSize* parameter is filled in with the number of bytes the output buffer requires to store the image.</span></span> <span data-ttu-id="de294-119">Se o buffer passado for muito pequeno ou a função membro falhar em alocar memória suficiente, a função de membro retornará E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="de294-119">If the buffer passed in is too small or the member function fails to allocate sufficient memory, the member function returns E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="de294-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="de294-120">Remarks</span></span>

<span data-ttu-id="de294-121">A função membro recupera a imagem do exemplo e a copia para o buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="de294-121">The member function retrieves the image from the sample and copies it into the output buffer.</span></span> <span data-ttu-id="de294-122">A seção de vídeo copiada no buffer de saída reflete o retângulo de origem que é definido por meio da interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) (embora não reflita o retângulo de destino).</span><span class="sxs-lookup"><span data-stu-id="de294-122">The section of video copied into the output buffer reflects the source rectangle that is set through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface (although it does not reflect the destination rectangle).</span></span>

## <a name="requirements"></a><span data-ttu-id="de294-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de294-123">Requirements</span></span>



| <span data-ttu-id="de294-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="de294-124">Requirement</span></span> | <span data-ttu-id="de294-125">Valor</span><span class="sxs-lookup"><span data-stu-id="de294-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de294-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="de294-126">Header</span></span><br/>  | <dl> <span data-ttu-id="de294-127"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="de294-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="de294-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="de294-128">Library</span></span><br/> | <dl> <span data-ttu-id="de294-129"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="de294-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de294-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="de294-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de294-131">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="de294-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





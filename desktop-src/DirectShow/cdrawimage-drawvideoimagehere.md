---
description: O método DrawVideoImageHere desenha uma imagem de um exemplo de mídia para um contexto de dispositivo especificado.
ms.assetid: b11e1c6b-5a29-444f-a0a9-049cd9d49b13
title: Método CDrawImage. DrawVideoImageHere (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.DrawVideoImageHere
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 599dd82e282f2d14ac7e974363a62695e209c080
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752293"
---
# <a name="cdrawimagedrawvideoimagehere-method"></a><span data-ttu-id="0028f-103">Método CDrawImage. DrawVideoImageHere</span><span class="sxs-lookup"><span data-stu-id="0028f-103">CDrawImage.DrawVideoImageHere method</span></span>

<span data-ttu-id="0028f-104">O `DrawVideoImageHere` método desenha uma imagem de um exemplo de mídia para um contexto de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="0028f-104">The `DrawVideoImageHere` method draws an image from a media sample to a specified device context.</span></span>

## <a name="syntax"></a><span data-ttu-id="0028f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0028f-105">Syntax</span></span>


```C++
BOOL DrawVideoImageHere(
   HDC          hdc,
   IMediaSample *pMediaSample,
   RECT         *lprcSrc,
   RECT         *lprcDst
);
```



## <a name="parameters"></a><span data-ttu-id="0028f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0028f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0028f-107">*HDC*</span><span class="sxs-lookup"><span data-stu-id="0028f-107">*hdc*</span></span> 
</dt> <dd>

<span data-ttu-id="0028f-108">Identificador para um contexto de dispositivo, onde o desenho ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="0028f-108">Handle to a device context, where the drawing will occur.</span></span>

</dd> <dt>

<span data-ttu-id="0028f-109">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="0028f-109">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="0028f-110">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo que contém a imagem.</span><span class="sxs-lookup"><span data-stu-id="0028f-110">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample that contains the image.</span></span>

</dd> <dt>

<span data-ttu-id="0028f-111">*lprcSrc*</span><span class="sxs-lookup"><span data-stu-id="0028f-111">*lprcSrc*</span></span> 
</dt> <dd>

<span data-ttu-id="0028f-112">Ponteiro para um retângulo de origem a ser usado para desenhar.</span><span class="sxs-lookup"><span data-stu-id="0028f-112">Pointer to a source rectangle to use for drawing.</span></span> <span data-ttu-id="0028f-113">Se for **NULL**, o retângulo em [**CDrawImage:: m \_ SourceRect**](cdrawimage-m-sourcerect.md) será usado.</span><span class="sxs-lookup"><span data-stu-id="0028f-113">If **NULL**, the rectangle in [**CDrawImage::m\_SourceRect**](cdrawimage-m-sourcerect.md) is used.</span></span>

</dd> <dt>

<span data-ttu-id="0028f-114">*lprcDst*</span><span class="sxs-lookup"><span data-stu-id="0028f-114">*lprcDst*</span></span> 
</dt> <dd>

<span data-ttu-id="0028f-115">Ponteiro para um retângulo de destino a ser usado para desenhar.</span><span class="sxs-lookup"><span data-stu-id="0028f-115">Pointer to a target rectangle to use for drawing.</span></span> <span data-ttu-id="0028f-116">Se for **NULL**, o retângulo em [**CDrawImage:: m \_ TargetRect**](cdrawimage-m-targetrect.md) será usado.</span><span class="sxs-lookup"><span data-stu-id="0028f-116">If **NULL**, the rectangle in [**CDrawImage::m\_TargetRect**](cdrawimage-m-targetrect.md) is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0028f-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0028f-117">Return value</span></span>

<span data-ttu-id="0028f-118">Retornará **true** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="0028f-118">Returns **TRUE** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="0028f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0028f-119">Requirements</span></span>



| <span data-ttu-id="0028f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0028f-120">Requirement</span></span> | <span data-ttu-id="0028f-121">Valor</span><span class="sxs-lookup"><span data-stu-id="0028f-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0028f-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0028f-122">Header</span></span><br/>  | <dl> <span data-ttu-id="0028f-123"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0028f-123"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0028f-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0028f-124">Library</span></span><br/> | <dl> <span data-ttu-id="0028f-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0028f-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0028f-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="0028f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0028f-127">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="0028f-127">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 





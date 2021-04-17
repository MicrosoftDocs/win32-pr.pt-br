---
description: O método FastRender desenha a imagem de vídeo usando as funções BitBlt ou StretchBlt.
ms.assetid: 8bbc96ce-393f-46fb-bf90-61d3ce0ef0d6
title: Método CDrawImage. FastRender (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.FastRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 823583beed6696d40803ccc098410dac053b8948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754991"
---
# <a name="cdrawimagefastrender-method"></a><span data-ttu-id="b64a3-103">Método CDrawImage. FastRender</span><span class="sxs-lookup"><span data-stu-id="b64a3-103">CDrawImage.FastRender method</span></span>

<span data-ttu-id="b64a3-104">O `FastRender` método desenha a imagem de vídeo usando as funções **BitBlt** ou **StretchBlt** .</span><span class="sxs-lookup"><span data-stu-id="b64a3-104">The `FastRender` method draws the video image using the **BitBlt** or **StretchBlt** functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="b64a3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b64a3-105">Syntax</span></span>


```C++
void FastRender(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="b64a3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b64a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b64a3-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="b64a3-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="b64a3-108">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo que contém a imagem.</span><span class="sxs-lookup"><span data-stu-id="b64a3-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample that contains the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b64a3-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b64a3-109">Return value</span></span>

<span data-ttu-id="b64a3-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b64a3-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b64a3-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b64a3-111">Remarks</span></span>

<span data-ttu-id="b64a3-112">O método [**CDrawImage::D RawImage**](cdrawimage-drawimage.md) chama esse método, mas somente se o alocador da conexão for um objeto [**CImageAllocator**](cimageallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="b64a3-112">The [**CDrawImage::DrawImage**](cdrawimage-drawimage.md) method calls this method, but only if the allocator for the connection is a [**CImageAllocator**](cimageallocator.md) object.</span></span> <span data-ttu-id="b64a3-113">Nesse caso, é garantido que o exemplo de mídia seja um objeto [**CImageSample**](cimagesample.md) .</span><span class="sxs-lookup"><span data-stu-id="b64a3-113">In that case, the media sample is guaranteed to be a [**CImageSample**](cimagesample.md) object.</span></span> <span data-ttu-id="b64a3-114">O objeto **CImageSample** usa a função **CreateDIBSection** para alocar memória compartilhada para o bitmap, o que torna possível desenhar a imagem usando **BitBlt** ou **StretchBlt**.</span><span class="sxs-lookup"><span data-stu-id="b64a3-114">The **CImageSample** object uses the **CreateDIBSection** function to allocate shared memory for the bitmap, which makes it possible to draw the image using either **BitBlt** or **StretchBlt**.</span></span>

<span data-ttu-id="b64a3-115">Esse método chama **BitBlt** se os retângulos de origem e destino correspondem exatamente ou **StretchBlt** de outra forma.</span><span class="sxs-lookup"><span data-stu-id="b64a3-115">This method calls **BitBlt** if the source and targer rectangles exactly match, or **StretchBlt** otherwise.</span></span>

<span data-ttu-id="b64a3-116">Se o filtro não possuir o alocador, o método **DrawImage** usará [**CDrawImage:: SlowRender**](cdrawimage-slowrender.md) para desenhar a imagem.</span><span class="sxs-lookup"><span data-stu-id="b64a3-116">If the filter does not own the allocator, the **DrawImage** method uses [**CDrawImage::SlowRender**](cdrawimage-slowrender.md) to draw the image.</span></span>

## <a name="requirements"></a><span data-ttu-id="b64a3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b64a3-117">Requirements</span></span>



| <span data-ttu-id="b64a3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b64a3-118">Requirement</span></span> | <span data-ttu-id="b64a3-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b64a3-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b64a3-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b64a3-120">Header</span></span><br/>  | <dl> <span data-ttu-id="b64a3-121"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b64a3-121"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b64a3-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b64a3-122">Library</span></span><br/> | <dl> <span data-ttu-id="b64a3-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b64a3-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b64a3-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="b64a3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b64a3-125">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="b64a3-125">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 





---
description: O método DrawImage desenha um quadro de vídeo na janela de vídeo.
ms.assetid: 22e7f59c-90f7-4e0c-8993-eea1eaf58fba
title: Método CDrawImage. DrawImage (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.DrawImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d219eb82ab2cf1929605eee4045c2f278022ad98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750051"
---
# <a name="cdrawimagedrawimage-method"></a><span data-ttu-id="a73a1-103">Método CDrawImage. DrawImage</span><span class="sxs-lookup"><span data-stu-id="a73a1-103">CDrawImage.DrawImage method</span></span>

<span data-ttu-id="a73a1-104">O `DrawImage` método desenha um quadro de vídeo na janela de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a73a1-104">The `DrawImage` method draws a video frame on the video window.</span></span>

## <a name="syntax"></a><span data-ttu-id="a73a1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a73a1-105">Syntax</span></span>


```C++
BOOL DrawImage(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="a73a1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a73a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a73a1-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="a73a1-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="a73a1-108">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo que contém a imagem.</span><span class="sxs-lookup"><span data-stu-id="a73a1-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample that contains the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a73a1-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a73a1-109">Return value</span></span>

<span data-ttu-id="a73a1-110">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="a73a1-110">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a73a1-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a73a1-111">Remarks</span></span>

<span data-ttu-id="a73a1-112">Esse método delega para [**CDrawImage:: FastRender**](cdrawimage-fastrender.md) ou [**CDrawImage:: SlowRender**](cdrawimage-slowrender.md), dependendo se o filtro possui o alocador que forneceu o exemplo.</span><span class="sxs-lookup"><span data-stu-id="a73a1-112">This method delegates to [**CDrawImage::FastRender**](cdrawimage-fastrender.md) or [**CDrawImage::SlowRender**](cdrawimage-slowrender.md), depending on whether the filter owns the allocator that provided the sample.</span></span> <span data-ttu-id="a73a1-113">Se o filtro possuir o alocador, será garantido que o exemplo seja um objeto [**CImageSample**](cimagesample.md) .</span><span class="sxs-lookup"><span data-stu-id="a73a1-113">If the filter does own the allocator, the sample is guaranteed to be a [**CImageSample**](cimagesample.md) object.</span></span> <span data-ttu-id="a73a1-114">Nesse caso, o exemplo usa a memória compartilhada alocada pela GDI e a imagem pode ser desenhada usando **BitBlt** ou **StretchBlt**.</span><span class="sxs-lookup"><span data-stu-id="a73a1-114">In that case, the sample uses shared memory allocated by GDI, and the image can be drawn using either **BitBlt** or **StretchBlt**.</span></span> <span data-ttu-id="a73a1-115">Caso contrário, as imagens devem ser desenhadas usando as funções **SetDIBitsToDevice** ou **StretchDIBits** mais lentas.</span><span class="sxs-lookup"><span data-stu-id="a73a1-115">Otherwise, the images must be drawn using the slower **SetDIBitsToDevice** or **StretchDIBits** functions.</span></span>

<span data-ttu-id="a73a1-116">Em compilações de depuração, esse método chama **DisplaySampleTimes** para desenhar os carimbos de data/hora da amostra na imagem de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a73a1-116">In debug builds, this method calls **DisplaySampleTimes** to draw the sample's time stamps over the video image.</span></span>

## <a name="requirements"></a><span data-ttu-id="a73a1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a73a1-117">Requirements</span></span>



| <span data-ttu-id="a73a1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a73a1-118">Requirement</span></span> | <span data-ttu-id="a73a1-119">Valor</span><span class="sxs-lookup"><span data-stu-id="a73a1-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a73a1-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a73a1-120">Header</span></span><br/>  | <dl> <span data-ttu-id="a73a1-121"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a73a1-121"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a73a1-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a73a1-122">Library</span></span><br/> | <dl> <span data-ttu-id="a73a1-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a73a1-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a73a1-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="a73a1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a73a1-125">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="a73a1-125">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="a73a1-126">**CDrawImage::UsingImageAllocator**</span><span class="sxs-lookup"><span data-stu-id="a73a1-126">**CDrawImage::UsingImageAllocator**</span></span>](cdrawimage-usingimageallocator.md)
</dt> </dl>

 

 





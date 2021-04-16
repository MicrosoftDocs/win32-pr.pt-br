---
description: O método SlowRender desenha a imagem de vídeo usando as funções SetDIBitsToDevice ou StretchDIBits.
ms.assetid: e1d8b189-b588-48eb-988a-3e5dedb38dbd
title: Método CDrawImage. SlowRender (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SlowRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b736bf6c44d4ada6e0a28408c449c9f8b2f1e1cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752291"
---
# <a name="cdrawimageslowrender-method"></a><span data-ttu-id="60f7f-103">Método CDrawImage. SlowRender</span><span class="sxs-lookup"><span data-stu-id="60f7f-103">CDrawImage.SlowRender method</span></span>

<span data-ttu-id="60f7f-104">O `SlowRender` método desenha a imagem de vídeo usando as funções **SetDIBitsToDevice** ou **StretchDIBits** .</span><span class="sxs-lookup"><span data-stu-id="60f7f-104">The `SlowRender` method draws the video image using the **SetDIBitsToDevice** or **StretchDIBits** functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="60f7f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="60f7f-105">Syntax</span></span>


```C++
void SlowRender(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="60f7f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="60f7f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60f7f-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="60f7f-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="60f7f-108">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo que contém a imagem.</span><span class="sxs-lookup"><span data-stu-id="60f7f-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample that contains the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60f7f-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="60f7f-109">Return value</span></span>

<span data-ttu-id="60f7f-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="60f7f-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="60f7f-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="60f7f-111">Remarks</span></span>

<span data-ttu-id="60f7f-112">Se [**CDrawImage:: UsingImageAllocator**](cdrawimage-usingimageallocator.md) retornar **false**, o método [**CDrawImage::D RawImage**](cdrawimage-drawimage.md) usará `SlowRender` para desenhar a imagem de vídeo.</span><span class="sxs-lookup"><span data-stu-id="60f7f-112">If [**CDrawImage::UsingImageAllocator**](cdrawimage-usingimageallocator.md) returns **FALSE**, the [**CDrawImage::DrawImage**](cdrawimage-drawimage.md) method uses `SlowRender` to draw the video image.</span></span> <span data-ttu-id="60f7f-113">Caso contrário, o DrawImage usará o método **FastRender** .</span><span class="sxs-lookup"><span data-stu-id="60f7f-113">Otherwise, DrawImage uses the **FastRender** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="60f7f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60f7f-114">Requirements</span></span>



| <span data-ttu-id="60f7f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="60f7f-115">Requirement</span></span> | <span data-ttu-id="60f7f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="60f7f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60f7f-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="60f7f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="60f7f-118"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="60f7f-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="60f7f-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="60f7f-119">Library</span></span><br/> | <dl> <span data-ttu-id="60f7f-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="60f7f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60f7f-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="60f7f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60f7f-122">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="60f7f-122">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="60f7f-123">**CDrawImage::FastRender**</span><span class="sxs-lookup"><span data-stu-id="60f7f-123">**CDrawImage::FastRender**</span></span>](cdrawimage-fastrender.md)
</dt> </dl>

 

 





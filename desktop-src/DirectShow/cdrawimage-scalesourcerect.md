---
description: O método ScaleSourceRect dimensiona um retângulo, se houver uma diferença entre o tamanho do vídeo nativo e o formato do tipo de mídia.
ms.assetid: 7bd4d555-5782-4ce5-9f0d-928b199ef897
title: Método CDrawImage. ScaleSourceRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.ScaleSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9800f405c0002fb58ca68ebd2369eb068f6319a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756634"
---
# <a name="cdrawimagescalesourcerect-method"></a><span data-ttu-id="3e49f-103">Método CDrawImage. ScaleSourceRect</span><span class="sxs-lookup"><span data-stu-id="3e49f-103">CDrawImage.ScaleSourceRect method</span></span>

<span data-ttu-id="3e49f-104">O `ScaleSourceRect` método dimensionará um retângulo se houver uma diferença entre o tamanho do vídeo nativo e o formato do tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="3e49f-104">The `ScaleSourceRect` method scales a rectangle, if there is a difference between the native video size and the media type format.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e49f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e49f-105">Syntax</span></span>


```C++
virtual RECT ScaleSourceRect(
   const RECT *pSource
);
```



## <a name="parameters"></a><span data-ttu-id="3e49f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e49f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e49f-107">*pSource*</span><span class="sxs-lookup"><span data-stu-id="3e49f-107">*pSource*</span></span> 
</dt> <dd>

<span data-ttu-id="3e49f-108">Ponteiro para um retângulo não dimensionado.</span><span class="sxs-lookup"><span data-stu-id="3e49f-108">Pointer to an unscaled rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e49f-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3e49f-109">Return value</span></span>

<span data-ttu-id="3e49f-110">Retorna o retângulo dimensionado.</span><span class="sxs-lookup"><span data-stu-id="3e49f-110">Returns the scaled rectangle.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e49f-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e49f-111">Remarks</span></span>

<span data-ttu-id="3e49f-112">Na classe **CDrawImage** , esse método retorna *pSource* sem nenhuma alteração.</span><span class="sxs-lookup"><span data-stu-id="3e49f-112">In the **CDrawImage** class, this method returns *pSource* without any change.</span></span> <span data-ttu-id="3e49f-113">Você pode substituir esse método se o filtro alongar a imagem de vídeo de entrada.</span><span class="sxs-lookup"><span data-stu-id="3e49f-113">You can override this method if the filter stretches the incoming video image.</span></span> <span data-ttu-id="3e49f-114">Por exemplo, o tamanho de vídeo nativo pode ser 320 240, mas o tipo de mídia no pino de entrada pode ser 640 480.</span><span class="sxs-lookup"><span data-stu-id="3e49f-114">For example, the native video size might be 320   240, but the media type on the input pin might be 640   480.</span></span> <span data-ttu-id="3e49f-115">Nesse caso, o filtro precisaria dimensionar o retângulo de origem por um fator de 2.</span><span class="sxs-lookup"><span data-stu-id="3e49f-115">In that case the filter would need to scale the source rectangle by a factor of 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e49f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e49f-116">Requirements</span></span>



| <span data-ttu-id="3e49f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e49f-117">Requirement</span></span> | <span data-ttu-id="3e49f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="3e49f-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e49f-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3e49f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="3e49f-120"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3e49f-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3e49f-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3e49f-121">Library</span></span><br/> | <dl> <span data-ttu-id="3e49f-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="3e49f-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e49f-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e49f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e49f-124">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="3e49f-124">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 





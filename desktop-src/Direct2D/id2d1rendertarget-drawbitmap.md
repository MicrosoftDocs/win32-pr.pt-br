---
title: Métodos ID2D1RenderTarget DrawBitmap
description: Desenha o ID2D1Bitmap especificado.
ms.assetid: 241df698-ca5e-4d94-902a-a9e140820c14
keywords:
- Métodos DrawBitmap Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: d82bbf557d7e53f06f614afbba578de40c789953
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812857"
---
# <a name="id2d1rendertargetdrawbitmap-methods"></a><span data-ttu-id="230c1-104">ID2D1RenderTarget: métodos de rawBitmap de:D</span><span class="sxs-lookup"><span data-stu-id="230c1-104">ID2D1RenderTarget::DrawBitmap methods</span></span>

<span data-ttu-id="230c1-105">Desenha o [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)especificado.</span><span class="sxs-lookup"><span data-stu-id="230c1-105">Draws the specified [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span></span>

### <a name="overload-list"></a><span data-ttu-id="230c1-106">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="230c1-106">Overload list</span></span>



| <span data-ttu-id="230c1-107">Método</span><span class="sxs-lookup"><span data-stu-id="230c1-107">Method</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="230c1-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="230c1-108">Description</span></span>                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| <span data-ttu-id="230c1-109">[**DrawBitmap (ID2D1Bitmap \* , d2d1 \_ rect \_ f&, float, d2d1 \_ bitmap \_ do \_ modo de interpolação, d2d1 \_ Rect \_ f&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_))</span><span class="sxs-lookup"><span data-stu-id="230c1-109">[**DrawBitmap(ID2D1Bitmap\*,D2D1\_RECT\_F&,FLOAT,D2D1\_BITMAP\_INTERPOLATION\_MODE,D2D1\_RECT\_F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_))</span></span>   | <span data-ttu-id="230c1-110">Desenha o bitmap especificado depois de dimensioná-lo para o tamanho do retângulo especificado.</span><span class="sxs-lookup"><span data-stu-id="230c1-110">Draws the specified bitmap after scaling it to the size of the specified rectangle.</span></span> <br/> |
| <span data-ttu-id="230c1-111">[**DrawBitmap (ID2D1Bitmap \* , d2d1 \_ rect \_ f&, float, d2d1 \_ bitmap \_ \_ modo de interpolação, d2d1 \_ Rect \_ f \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f))</span><span class="sxs-lookup"><span data-stu-id="230c1-111">[**DrawBitmap(ID2D1Bitmap\*,D2D1\_RECT\_F&,FLOAT,D2D1\_BITMAP\_INTERPOLATION\_MODE,D2D1\_RECT\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f))</span></span>  | <span data-ttu-id="230c1-112">Desenha o bitmap especificado depois de dimensioná-lo para o tamanho do retângulo especificado.</span><span class="sxs-lookup"><span data-stu-id="230c1-112">Draws the specified bitmap after scaling it to the size of the specified rectangle.</span></span> <br/> |
| <span data-ttu-id="230c1-113">[**DrawBitmap (ID2D1Bitmap \* , d2d1 \_ Rect \_ f \* , float, d2d1 \_ bitmap \_ do \_ modo de interpolação, d2d1 \_ Rect \_ f \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f_float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f))</span><span class="sxs-lookup"><span data-stu-id="230c1-113">[**DrawBitmap(ID2D1Bitmap\*,D2D1\_RECT\_F\*,FLOAT,D2D1\_BITMAP\_INTERPOLATION\_MODE,D2D1\_RECT\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f_float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f))</span></span> | <span data-ttu-id="230c1-114">Desenha o bitmap especificado depois de dimensioná-lo para o tamanho do retângulo especificado.</span><span class="sxs-lookup"><span data-stu-id="230c1-114">Draws the specified bitmap after scaling it to the size of the specified rectangle.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="230c1-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="230c1-115">Remarks</span></span>

<span data-ttu-id="230c1-116">Esse método não retornará um código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="230c1-116">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="230c1-117">Para determinar se uma operação de desenho (como **DrawBitmap**) falhou, verifique o resultado retornado pelos métodos [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**ID2D1RenderTarget:: flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .</span><span class="sxs-lookup"><span data-stu-id="230c1-117">To determine whether a drawing operation (such as **DrawBitmap**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="230c1-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="230c1-118">Examples</span></span>

<span data-ttu-id="230c1-119">Para obter um exemplo, consulte [como desenhar um bitmap](how-to-draw-a-bitmap.md).</span><span class="sxs-lookup"><span data-stu-id="230c1-119">For an example, see [How to Draw a Bitmap](how-to-draw-a-bitmap.md).</span></span> <span data-ttu-id="230c1-120">Para obter um exemplo que mostra como carregar um bitmap de um recurso ou arquivo, consulte [como carregar um bitmap de um recurso](how-to-load-a-bitmap-from-a-resource.md) e [como carregar um bitmap de um arquivo](how-to-load-a-direct2d-bitmap-from-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="230c1-120">For an example showing how to load a bitmap from a resource or a file, see [How to Load a Bitmap from a Resource](how-to-load-a-bitmap-from-a-resource.md) and [How to Load a Bitmap from a File](how-to-load-a-direct2d-bitmap-from-a-file.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="230c1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="230c1-121">Requirements</span></span>



| <span data-ttu-id="230c1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="230c1-122">Requirement</span></span> | <span data-ttu-id="230c1-123">Valor</span><span class="sxs-lookup"><span data-stu-id="230c1-123">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="230c1-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="230c1-124">Library</span></span><br/> | <dl> <span data-ttu-id="230c1-125"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="230c1-125"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="230c1-126">DLL</span><span class="sxs-lookup"><span data-stu-id="230c1-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="230c1-127"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="230c1-127"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="230c1-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="230c1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="230c1-129">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="230c1-129">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="230c1-130">Como desenhar um bitmap</span><span class="sxs-lookup"><span data-stu-id="230c1-130">How to Draw a Bitmap</span></span>](how-to-draw-a-bitmap.md)
</dt> <dt>

[<span data-ttu-id="230c1-131">Como carregar um bitmap de um recurso</span><span class="sxs-lookup"><span data-stu-id="230c1-131">How to Load a Bitmap from a Resource</span></span>](how-to-load-a-bitmap-from-a-resource.md)
</dt> <dt>

[<span data-ttu-id="230c1-132">Como carregar um bitmap de um arquivo</span><span class="sxs-lookup"><span data-stu-id="230c1-132">How to Load a Bitmap from a File</span></span>](how-to-load-a-direct2d-bitmap-from-a-file.md)
</dt> </dl>

 


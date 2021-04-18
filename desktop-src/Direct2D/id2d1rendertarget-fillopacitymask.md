---
title: Métodos ID2D1RenderTarget FillOpacityMask
description: Aplica a máscara de opacidade descrita pelo bitmap especificado a um pincel e usa esse pincel para pintar uma região do destino de renderização.
ms.assetid: a5e56d8a-2929-4f7b-b1c4-fb358c202721
keywords:
- Métodos FillOpacityMask Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: e988994b849c193725dfdd75773f22a63fed6754
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749277"
---
# <a name="id2d1rendertargetfillopacitymask-methods"></a><span data-ttu-id="9843a-104">Métodos ID2D1RenderTarget:: FillOpacityMask</span><span class="sxs-lookup"><span data-stu-id="9843a-104">ID2D1RenderTarget::FillOpacityMask methods</span></span>

<span data-ttu-id="9843a-105">Aplica a máscara de opacidade descrita pelo bitmap especificado a um pincel e usa esse pincel para pintar uma região do destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="9843a-105">Applies the opacity mask described by the specified bitmap to a brush and uses that brush to paint a region of the render target.</span></span>

### <a name="overload-list"></a><span data-ttu-id="9843a-106">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="9843a-106">Overload list</span></span>



| <span data-ttu-id="9843a-107">Método</span><span class="sxs-lookup"><span data-stu-id="9843a-107">Method</span></span>                                                                                                                                                                                                                          | <span data-ttu-id="9843a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="9843a-108">Description</span></span>                                                                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9843a-109">[**FillOpacityMask (ID2D1Bitmap \* , ID2D1Brush \* , d2d1 \_ OPACITY \_ \_ CONTENT, D2D \_ Rect \_ f&, D2D \_ Rect \_ f&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_))</span><span class="sxs-lookup"><span data-stu-id="9843a-109">[**FillOpacityMask(ID2D1Bitmap\*,ID2D1Brush\*,D2D1\_OPACITY\_MASK\_CONTENT,D2D\_RECT\_F&,D2D\_RECT\_F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_))</span></span>       | <span data-ttu-id="9843a-110">Aplica a máscara de opacidade descrita pelo bitmap especificado a um pincel e usa esse pincel para pintar uma região do destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="9843a-110">Applies the opacity mask described by the specified bitmap to a brush and uses that brush to paint a region of the render target.</span></span> <br/> |
| <span data-ttu-id="9843a-111">[**FillOpacityMask (ID2D1Bitmap \* , ID2D1Brush \* , d2d1 \_ de \_ máscara de opacidade \_ , D2D \_ Rect f \_ \* , D2D \_ Rect \_ f \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f_constd2d1_rect_f))</span><span class="sxs-lookup"><span data-stu-id="9843a-111">[**FillOpacityMask(ID2D1Bitmap\*,ID2D1Brush\*,D2D1\_OPACITY\_MASK\_CONTENT,D2D\_RECT\_F\*,D2D\_RECT\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f_constd2d1_rect_f))</span></span> | <span data-ttu-id="9843a-112">Aplica a máscara de opacidade descrita pelo bitmap especificado a um pincel e usa esse pincel para pintar uma região do destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="9843a-112">Applies the opacity mask described by the specified bitmap to a brush and uses that brush to paint a region of the render target.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="9843a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="9843a-113">Remarks</span></span>

<span data-ttu-id="9843a-114">Para que esse método funcione corretamente, o destino de renderização deve usar o modo de anti-aliasing com [**\_ \_ \_ ALIAS do modo AntiAlias d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) .</span><span class="sxs-lookup"><span data-stu-id="9843a-114">For this method to work properly, the render target must be using the [**D2D1\_ANTIALIAS\_MODE\_ALIASED**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) antialiasing mode.</span></span> <span data-ttu-id="9843a-115">Você pode definir o modo de suavização chamando o método [**ID2D1RenderTarget:: SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) .</span><span class="sxs-lookup"><span data-stu-id="9843a-115">You can set the antialiasing mode by calling the [**ID2D1RenderTarget::SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) method.</span></span>

<span data-ttu-id="9843a-116">Esse método não retornará um código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="9843a-116">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="9843a-117">Para determinar se uma operação de desenho (como **FillOpacityMask**) falhou, verifique o resultado retornado pelos métodos [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**ID2D1RenderTarget:: flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .</span><span class="sxs-lookup"><span data-stu-id="9843a-117">To determine whether a drawing operation (such as **FillOpacityMask**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="9843a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9843a-118">Requirements</span></span>



| <span data-ttu-id="9843a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9843a-119">Requirement</span></span> | <span data-ttu-id="9843a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9843a-120">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9843a-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9843a-121">Library</span></span><br/> | <dl> <span data-ttu-id="9843a-122"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9843a-122"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="9843a-123">DLL</span><span class="sxs-lookup"><span data-stu-id="9843a-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="9843a-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9843a-124"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9843a-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="9843a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9843a-126">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="9843a-126">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

 


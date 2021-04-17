---
title: Métodos ID2D1RenderTarget PushAxisAlignedClip (D2d1 \_ 1. h)
description: Especifica um retângulo para o qual todas as operações de desenho subsequentes são recortadas.
ms.assetid: 8b777425-07b1-4494-889a-0c947fb61315
keywords:
- Métodos PushAxisAlignedClip Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: d7e6d59f1c4cbffcde74ecb7b5adb5b12eff06bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754274"
---
# <a name="id2d1rendertargetpushaxisalignedclip-methods"></a><span data-ttu-id="7bbd1-104">ID2D1RenderTarget: métodos de ushAxisAlignedClip de:P</span><span class="sxs-lookup"><span data-stu-id="7bbd1-104">ID2D1RenderTarget::PushAxisAlignedClip methods</span></span>

<span data-ttu-id="7bbd1-105">Especifica um retângulo para o qual todas as operações de desenho subsequentes são recortadas.</span><span class="sxs-lookup"><span data-stu-id="7bbd1-105">Specifies a rectangle to which all subsequent drawing operations are clipped.</span></span>

### <a name="overload-list"></a><span data-ttu-id="7bbd1-106">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="7bbd1-106">Overload list</span></span>



| <span data-ttu-id="7bbd1-107">Método</span><span class="sxs-lookup"><span data-stu-id="7bbd1-107">Method</span></span>                                                                                                                                         | <span data-ttu-id="7bbd1-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="7bbd1-108">Description</span></span>                                                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bbd1-109">[**PushAxisAlignedClip (D2D1 \_ Rect \_ F&, d2d1 \_ modo AntiAlias \_ )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))</span><span class="sxs-lookup"><span data-stu-id="7bbd1-109">[**PushAxisAlignedClip(D2D1\_RECT\_F&,D2D1\_ANTIALIAS\_MODE)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))</span></span>  | <span data-ttu-id="7bbd1-110">Especifica um retângulo para o qual todas as operações de desenho subsequentes são recortadas.</span><span class="sxs-lookup"><span data-stu-id="7bbd1-110">Specifies a rectangle to which all subsequent drawing operations are clipped.</span></span> <br/> |
| <span data-ttu-id="7bbd1-111">[**PushAxisAlignedClip (D2D1 \_ Rect \_ F \* , d2d1 \_ modo AntiAlias \_ )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))</span><span class="sxs-lookup"><span data-stu-id="7bbd1-111">[**PushAxisAlignedClip(D2D1\_RECT\_F\*,D2D1\_ANTIALIAS\_MODE)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))</span></span> | <span data-ttu-id="7bbd1-112">Especifica um retângulo para o qual todas as operações de desenho subsequentes são recortadas.</span><span class="sxs-lookup"><span data-stu-id="7bbd1-112">Specifies a rectangle to which all subsequent drawing operations are clipped.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="7bbd1-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="7bbd1-113">Remarks</span></span>

<span data-ttu-id="7bbd1-114">Um par [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) e [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) pode ocorrer ao contrário ou dentro de um [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) e [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer), mas não pode se sobrepor.</span><span class="sxs-lookup"><span data-stu-id="7bbd1-114">A [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) and [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) pair can occur around or within a [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer), but cannot overlap.</span></span> <span data-ttu-id="7bbd1-115">Por exemplo, a sequência de **PushAxisAlignedClip**, [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)), **PopLayer**, **PopAxisAlignedClip** é válida, mas a sequência de **PushAxisAlignedClip**, **PushLayer**, **PopAxisAlignedClip**, **PopLayer** é inválida.</span><span class="sxs-lookup"><span data-stu-id="7bbd1-115">For example, the sequence of **PushAxisAlignedClip**, [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)), **PopLayer**, **PopAxisAlignedClip** is valid, but the sequence of **PushAxisAlignedClip**, **PushLayer**, **PopAxisAlignedClip**, **PopLayer** is invalid.</span></span>

<span data-ttu-id="7bbd1-116">Esse método não retornará um código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="7bbd1-116">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="7bbd1-117">Para determinar se uma operação de desenho (como **PushAxisAlignedClip**) falhou, verifique o resultado retornado pelos métodos [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**ID2D1RenderTarget:: flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .</span><span class="sxs-lookup"><span data-stu-id="7bbd1-117">To determine whether a drawing operation (such as **PushAxisAlignedClip**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="7bbd1-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7bbd1-118">Examples</span></span>

<span data-ttu-id="7bbd1-119">Para obter um exemplo, consulte [como recortar com um Axis-Aligned clip Rectangle](how-to-clip-with-axis-aligned-rects.md).</span><span class="sxs-lookup"><span data-stu-id="7bbd1-119">For an example, see the [How to Clip with an Axis-Aligned Clip Rectangle](how-to-clip-with-axis-aligned-rects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7bbd1-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7bbd1-120">Requirements</span></span>



| <span data-ttu-id="7bbd1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bbd1-121">Requirement</span></span> | <span data-ttu-id="7bbd1-122">Valor</span><span class="sxs-lookup"><span data-stu-id="7bbd1-122">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bbd1-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7bbd1-123">Header</span></span><br/>  | <dl> <span data-ttu-id="7bbd1-124"><dt>D2d1 \_ 1. h (inclui D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7bbd1-124"><dt>D2d1\_1.h (include D2d1.h)</dt></span></span> </dl> |
| <span data-ttu-id="7bbd1-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7bbd1-125">Library</span></span><br/> | <dl> <span data-ttu-id="7bbd1-126"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7bbd1-126"><dt>D2d1.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="7bbd1-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7bbd1-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="7bbd1-128"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7bbd1-128"><dt>D2d1.dll</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="7bbd1-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="7bbd1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bbd1-130">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="7bbd1-130">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

<span data-ttu-id="7bbd1-131">�</span><span class="sxs-lookup"><span data-stu-id="7bbd1-131">�</span></span>

<span data-ttu-id="7bbd1-132">�</span><span class="sxs-lookup"><span data-stu-id="7bbd1-132">�</span></span>

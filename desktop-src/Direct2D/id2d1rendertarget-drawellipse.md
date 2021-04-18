---
title: Métodos ID2D1RenderTarget DrawEllipse (D2d1. h)
description: Desenha o contorno de uma elipse com as dimensões e o traço especificados.
ms.assetid: dabbb399-2d72-41c3-8b2f-aea49d7ad0cb
keywords:
- Métodos DrawEllipse Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 9647591b5033b912283500a0ddb1dba20004ec38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810408"
---
# <a name="id2d1rendertargetdrawellipse-methods"></a><span data-ttu-id="28a0e-104">ID2D1RenderTarget: métodos de rawEllipse de:D</span><span class="sxs-lookup"><span data-stu-id="28a0e-104">ID2D1RenderTarget::DrawEllipse methods</span></span>

<span data-ttu-id="28a0e-105">Desenha o contorno de uma elipse com as dimensões e o traço especificados.</span><span class="sxs-lookup"><span data-stu-id="28a0e-105">Draws the outline of an ellipse with the specified dimensions and stroke.</span></span>

### <a name="overload-list"></a><span data-ttu-id="28a0e-106">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="28a0e-106">Overload list</span></span>



| <span data-ttu-id="28a0e-107">Método</span><span class="sxs-lookup"><span data-stu-id="28a0e-107">Method</span></span>                                                                                                                                                                 | <span data-ttu-id="28a0e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="28a0e-108">Description</span></span>                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28a0e-109">[**DrawEllipse (D2D1 \_ ELLIPSE&, ID2D1Brush \* , float, ID2D1StrokeStyle \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))</span><span class="sxs-lookup"><span data-stu-id="28a0e-109">[**DrawEllipse(D2D1\_ELLIPSE&,ID2D1Brush\*,FLOAT,ID2D1StrokeStyle\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))</span></span>  | <span data-ttu-id="28a0e-110">Desenha o contorno da elipse especificada usando o estilo de traço especificado.</span><span class="sxs-lookup"><span data-stu-id="28a0e-110">Draws the outline of the specified ellipse using the specified stroke style.</span></span> <br/> |
| <span data-ttu-id="28a0e-111">[**DrawEllipse (D2D1 \_ Ellipse \* , ID2D1Brush \* , float, ID2D1StrokeStyle \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))</span><span class="sxs-lookup"><span data-stu-id="28a0e-111">[**DrawEllipse(D2D1\_ELLIPSE\*,ID2D1Brush\*,FLOAT,ID2D1StrokeStyle\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))</span></span> | <span data-ttu-id="28a0e-112">Desenha o contorno da elipse especificada usando o estilo de traço especificado.</span><span class="sxs-lookup"><span data-stu-id="28a0e-112">Draws the outline of the specified ellipse using the specified stroke style.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="28a0e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="28a0e-113">Remarks</span></span>

<span data-ttu-id="28a0e-114">O método **DrawEllipse** não retornará um código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="28a0e-114">The **DrawEllipse** method doesn't return an error code if it fails.</span></span> <span data-ttu-id="28a0e-115">Para determinar se uma operação de desenho (como **DrawEllipse**) falhou, verifique o resultado retornado pelos métodos [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**ID2D1RenderTarget:: flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .</span><span class="sxs-lookup"><span data-stu-id="28a0e-115">To determine whether a drawing operation (such as **DrawEllipse**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="28a0e-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="28a0e-116">Examples</span></span>

<span data-ttu-id="28a0e-117">Para obter um exemplo, consulte [como desenhar e preencher uma forma básica](how-to-draw-an-ellipse.md).</span><span class="sxs-lookup"><span data-stu-id="28a0e-117">For an example, see [How to Draw and Fill a Basic Shape](how-to-draw-an-ellipse.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="28a0e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28a0e-118">Requirements</span></span>



| <span data-ttu-id="28a0e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="28a0e-119">Requirement</span></span> | <span data-ttu-id="28a0e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="28a0e-120">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="28a0e-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="28a0e-121">Header</span></span><br/>  | <dl> <span data-ttu-id="28a0e-122"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="28a0e-122"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="28a0e-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="28a0e-123">Library</span></span><br/> | <dl> <span data-ttu-id="28a0e-124"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="28a0e-124"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="28a0e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="28a0e-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="28a0e-126"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28a0e-126"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28a0e-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="28a0e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28a0e-128">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="28a0e-128">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

<span data-ttu-id="28a0e-129">[**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse_id2d1brush))</span><span class="sxs-lookup"><span data-stu-id="28a0e-129">[**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse_id2d1brush))</span></span>
</dt> </dl>

<span data-ttu-id="28a0e-130">�</span><span class="sxs-lookup"><span data-stu-id="28a0e-130">�</span></span>

<span data-ttu-id="28a0e-131">�</span><span class="sxs-lookup"><span data-stu-id="28a0e-131">�</span></span>

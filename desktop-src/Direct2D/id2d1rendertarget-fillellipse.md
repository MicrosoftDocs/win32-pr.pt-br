---
title: Métodos ID2D1RenderTarget FillEllipse (D2d1. h)
description: Pinta o interior da elipse especificada.
ms.assetid: 149fb303-d2e8-416c-b28f-8bc5f1482ba6
keywords:
- Métodos FillEllipse Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: b8328775d87dd4df0fd015990d31db0751b729bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757904"
---
# <a name="id2d1rendertargetfillellipse-methods"></a><span data-ttu-id="9cda7-104">Métodos ID2D1RenderTarget:: FillEllipse</span><span class="sxs-lookup"><span data-stu-id="9cda7-104">ID2D1RenderTarget::FillEllipse methods</span></span>

<span data-ttu-id="9cda7-105">Pinta o interior da elipse especificada.</span><span class="sxs-lookup"><span data-stu-id="9cda7-105">Paints the interior of the specified ellipse.</span></span>

### <a name="overload-list"></a><span data-ttu-id="9cda7-106">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="9cda7-106">Overload list</span></span>



| <span data-ttu-id="9cda7-107">Método</span><span class="sxs-lookup"><span data-stu-id="9cda7-107">Method</span></span>                                                                                                             | <span data-ttu-id="9cda7-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="9cda7-108">Description</span></span>                                               |
|:-------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------|
| <span data-ttu-id="9cda7-109">[**FillEllipse (D2D1 \_ ELLIPSE&, ID2D1Brush \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))</span><span class="sxs-lookup"><span data-stu-id="9cda7-109">[**FillEllipse(D2D1\_ELLIPSE&,ID2D1Brush\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))</span></span>  | <span data-ttu-id="9cda7-110">Pinta o interior da elipse especificada.</span><span class="sxs-lookup"><span data-stu-id="9cda7-110">Paints the interior of the specified ellipse.</span></span> <br/> |
| <span data-ttu-id="9cda7-111">[**FillEllipse (D2D1 \_ Ellipse \* , ID2D1Brush \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))</span><span class="sxs-lookup"><span data-stu-id="9cda7-111">[**FillEllipse(D2D1\_ELLIPSE\*,ID2D1Brush\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))</span></span> | <span data-ttu-id="9cda7-112">Pinta o interior da elipse especificada.</span><span class="sxs-lookup"><span data-stu-id="9cda7-112">Paints the interior of the specified ellipse.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="9cda7-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="9cda7-113">Remarks</span></span>

<span data-ttu-id="9cda7-114">Esse método não retornará um código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="9cda7-114">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="9cda7-115">Para determinar se uma operação de desenho (como **FillEllipse**) falhou, verifique o resultado retornado pelos métodos [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**ID2D1RenderTarget:: flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .</span><span class="sxs-lookup"><span data-stu-id="9cda7-115">To determine whether a drawing operation (such as **FillEllipse**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="9cda7-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9cda7-116">Examples</span></span>

<span data-ttu-id="9cda7-117">Para obter um exemplo, consulte [como desenhar e preencher uma forma básica](how-to-draw-an-ellipse.md).</span><span class="sxs-lookup"><span data-stu-id="9cda7-117">For an example, see [How to Draw and Fill a Basic Shape](how-to-draw-an-ellipse.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9cda7-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9cda7-118">Requirements</span></span>



| <span data-ttu-id="9cda7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cda7-119">Requirement</span></span> | <span data-ttu-id="9cda7-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9cda7-120">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9cda7-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9cda7-121">Header</span></span><br/>  | <dl> <span data-ttu-id="9cda7-122"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="9cda7-122"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="9cda7-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9cda7-123">Library</span></span><br/> | <dl> <span data-ttu-id="9cda7-124"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9cda7-124"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="9cda7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9cda7-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="9cda7-126"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9cda7-126"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cda7-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="9cda7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cda7-128">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="9cda7-128">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="9cda7-129">Como desenhar e preencher uma forma básica</span><span class="sxs-lookup"><span data-stu-id="9cda7-129">How to Draw and Fill a Basic Shape</span></span>](how-to-draw-an-ellipse.md)
</dt> </dl>

<span data-ttu-id="9cda7-130">�</span><span class="sxs-lookup"><span data-stu-id="9cda7-130">�</span></span>

<span data-ttu-id="9cda7-131">�</span><span class="sxs-lookup"><span data-stu-id="9cda7-131">�</span></span>

---
title: Métodos ID2D1RenderTarget FillRoundedRectangle (D2d1. h)
description: Pinta o interior do retângulo arredondado especificado.
ms.assetid: 9c4765b0-858f-4a20-b044-0acf87a1f131
keywords:
- Métodos FillRoundedRectangle Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 2abc39ed364de0653813aab14ee5777ccf3c4e08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750920"
---
# <a name="id2d1rendertargetfillroundedrectangle-methods"></a><span data-ttu-id="55f5b-104">Métodos ID2D1RenderTarget:: FillRoundedRectangle</span><span class="sxs-lookup"><span data-stu-id="55f5b-104">ID2D1RenderTarget::FillRoundedRectangle methods</span></span>

<span data-ttu-id="55f5b-105">Pinta o interior do retângulo arredondado especificado.</span><span class="sxs-lookup"><span data-stu-id="55f5b-105">Paints the interior of the specified rounded rectangle.</span></span>

### <a name="overload-list"></a><span data-ttu-id="55f5b-106">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="55f5b-106">Overload list</span></span>



| <span data-ttu-id="55f5b-107">Método</span><span class="sxs-lookup"><span data-stu-id="55f5b-107">Method</span></span>                                                                                                                                          | <span data-ttu-id="55f5b-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="55f5b-108">Description</span></span>                                                         |
|:------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------|
| <span data-ttu-id="55f5b-109">[**FillRoundedRectangle (D2D1 \_ arredondado \_ retangular&, ID2D1Brush \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillroundedrectangle(constd2d1_rounded_rect__id2d1brush))</span><span class="sxs-lookup"><span data-stu-id="55f5b-109">[**FillRoundedRectangle(D2D1\_ROUNDED\_RECT&,ID2D1Brush\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillroundedrectangle(constd2d1_rounded_rect__id2d1brush))</span></span>  | <span data-ttu-id="55f5b-110">Pinta o interior do retângulo arredondado especificado.</span><span class="sxs-lookup"><span data-stu-id="55f5b-110">Paints the interior of the specified rounded rectangle.</span></span> <br/> |
| <span data-ttu-id="55f5b-111">[**FillRoundedRectangle ( \_ retângulo arredondado d2d1 \_ \* , ID2D1Brush \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillroundedrectangle(constd2d1_rounded_rect__id2d1brush))</span><span class="sxs-lookup"><span data-stu-id="55f5b-111">[**FillRoundedRectangle(D2D1\_ROUNDED\_RECT\*,ID2D1Brush\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillroundedrectangle(constd2d1_rounded_rect__id2d1brush))</span></span> | <span data-ttu-id="55f5b-112">Pinta o interior do retângulo arredondado especificado.</span><span class="sxs-lookup"><span data-stu-id="55f5b-112">Paints the interior of the specified rounded rectangle.</span></span><br/>  |



## <a name="remarks"></a><span data-ttu-id="55f5b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="55f5b-113">Remarks</span></span>

<span data-ttu-id="55f5b-114">Esse método não retornará um código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="55f5b-114">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="55f5b-115">Para determinar se uma operação de desenho (como **FillRoundedRectangle**) falhou, verifique o resultado retornado pelos métodos [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**ID2D1RenderTarget:: flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .</span><span class="sxs-lookup"><span data-stu-id="55f5b-115">To determine whether a drawing operation (such as **FillRoundedRectangle**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="55f5b-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="55f5b-116">Examples</span></span>

<span data-ttu-id="55f5b-117">O exemplo a seguir usa os métodos [**DrawRoundedRectangle**](id2d1rendertarget-drawroundedrectangle.md) e **FillRoundedRectangle** para descrever e preencher um retângulo arredondado.</span><span class="sxs-lookup"><span data-stu-id="55f5b-117">The following example uses the [**DrawRoundedRectangle**](id2d1rendertarget-drawroundedrectangle.md) and **FillRoundedRectangle** methods to outline and fill a rounded rectangle.</span></span> <span data-ttu-id="55f5b-118">Este exemplo produz a saída mostrada na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="55f5b-118">This example produces the output shown in the following illustration.</span></span>

![ilustração de quatro retângulos arredondados com diferentes estilos de traço e preenchimentos](images/drawroundedrectangle-scr.png)


```C++
//  Called whenever the application needs to display the client
//  window.
HRESULT DrawAndFillRoundedRectangleExample::OnRender()
{
    HRESULT hr;

    // Create the render target and brushes if they
    // don't already exists.
    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        // Retrieve the size of the render target.
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget->GetSize();

        m_pRenderTarget->BeginDraw();
        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());
        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        // Paint a grid background.
        m_pRenderTarget->FillRectangle(
            D2D1::RectF(0.0f, 0.0f, renderTargetSize.width, renderTargetSize.height),
            m_pGridPatternBitmapBrush
            );

        // Define a rounded rectangle.
        D2D1_ROUNDED_RECT roundedRect = D2D1::RoundedRect(
            D2D1::RectF(20.f, 20.f, 150.f, 100.f),
            10.f,
            10.f
            );

        // Draw the rectangle.
        m_pRenderTarget->DrawRoundedRectangle(roundedRect, m_pBlackBrush, 10.f);

        // Apply a translation transform.
        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Translation(200.f, 0.f));

        // Draw the rounded rectangle again, this time with a dashed stroke.
        m_pRenderTarget->DrawRoundedRectangle(roundedRect, m_pBlackBrush, 10.f, m_pStrokeStyle);

        // Apply another translation transform.
        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Translation(0.f, 150.f));

        // Draw, then fill the rounded rectangle.
        m_pRenderTarget->DrawRoundedRectangle(roundedRect, m_pBlackBrush, 10.f, m_pStrokeStyle);
        m_pRenderTarget->FillRoundedRectangle(roundedRect, m_pSilverBrush);

        // Apply another translation transform.
        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Translation(200.f, 150.f));

        // Fill, then draw the rounded rectangle.
        m_pRenderTarget->FillRoundedRectangle(roundedRect, m_pSilverBrush);
        m_pRenderTarget->DrawRoundedRectangle(roundedRect, m_pBlackBrush, 10.f, m_pStrokeStyle);

        hr = m_pRenderTarget->EndDraw();

        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="55f5b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55f5b-120">Requirements</span></span>



| <span data-ttu-id="55f5b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="55f5b-121">Requirement</span></span> | <span data-ttu-id="55f5b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="55f5b-122">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="55f5b-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="55f5b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="55f5b-124"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="55f5b-124"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="55f5b-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="55f5b-125">Library</span></span><br/> | <dl> <span data-ttu-id="55f5b-126"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="55f5b-126"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="55f5b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="55f5b-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="55f5b-128"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55f5b-128"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55f5b-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="55f5b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55f5b-130">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="55f5b-130">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="55f5b-131">Como desenhar e preencher uma forma básica</span><span class="sxs-lookup"><span data-stu-id="55f5b-131">How to Draw and Fill a Basic Shape</span></span>](how-to-draw-an-ellipse.md)
</dt> <dt>

[<span data-ttu-id="55f5b-132">**D2D1::RoundedRect**</span><span class="sxs-lookup"><span data-stu-id="55f5b-132">**D2D1::RoundedRect**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1roundedrectanglegeometry-getroundedrect)
</dt> </dl>

<span data-ttu-id="55f5b-133">�</span><span class="sxs-lookup"><span data-stu-id="55f5b-133">�</span></span>

<span data-ttu-id="55f5b-134">�</span><span class="sxs-lookup"><span data-stu-id="55f5b-134">�</span></span>

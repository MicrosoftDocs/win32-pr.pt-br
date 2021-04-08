---
title: Como desenhar um bitmap
description: Mostra como renderizar bitmaps com Direct2D.
ms.assetid: 9c6fc8b1-47ba-46fa-b812-2636cd8ff2b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbfa13b75b4fe34ce6ff2b80598fac35f8483a2f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823811"
---
# <a name="how-to-draw-a-bitmap"></a><span data-ttu-id="2da9d-103">Como desenhar um bitmap</span><span class="sxs-lookup"><span data-stu-id="2da9d-103">How to Draw a Bitmap</span></span>

<span data-ttu-id="2da9d-104">Para renderizar um bitmap, use o método [**ID2D1RenderTarget::D rawbitmap**](id2d1rendertarget-drawbitmap.md) .</span><span class="sxs-lookup"><span data-stu-id="2da9d-104">To render a bitmap, use the [**ID2D1RenderTarget::DrawBitmap**](id2d1rendertarget-drawbitmap.md) method.</span></span> <span data-ttu-id="2da9d-105">O exemplo a seguir mostra como usar o método **DrawBitmap** para desenhar um [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span><span class="sxs-lookup"><span data-stu-id="2da9d-105">The following example shows how to use the **DrawBitmap** method to draw an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span></span> <span data-ttu-id="2da9d-106">Ele cria a saída mostrada na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="2da9d-106">It creates the output shown in the following illustration.</span></span>

![ilustração de um bitmap original e bitmaps resultantes com diferentes configurações de opacidade e transformações](images/drawbitmapexample.png)

<span data-ttu-id="2da9d-108">Primeiro, crie um [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span><span class="sxs-lookup"><span data-stu-id="2da9d-108">First, create an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span></span> <span data-ttu-id="2da9d-109">O exemplo a seguir carrega um bitmap do arquivo de recursos do aplicativo e o armazena como *m \_ pBitmap*.</span><span class="sxs-lookup"><span data-stu-id="2da9d-109">The following example loads a bitmap from the application's resource file and stores it as *m\_pBitmap*.</span></span> <span data-ttu-id="2da9d-110">(Para ver como o `LoadResourceBitmap` método é implementado, consulte [como carregar um bitmap de um recurso](how-to-load-a-bitmap-from-a-resource.md).)</span><span class="sxs-lookup"><span data-stu-id="2da9d-110">(To see how the `LoadResourceBitmap` method is implemented, refer to [How to Load a Bitmap from a Resource](how-to-load-a-bitmap-from-a-resource.md).)</span></span>


```C++
// Create a bitmap from an application resource.
hr = LoadResourceBitmap(
    m_pRenderTarget,
    m_pWICFactory,
    L"SampleImage",
    L"Image",
    200,
    0,
    &m_pBitmap
    );
```



<span data-ttu-id="2da9d-111">Crie o [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) no mesmo método em que você criou o destino de renderização que será usado para desenhar o bitmap e libere o bitmap quando o destino de renderização for liberado.</span><span class="sxs-lookup"><span data-stu-id="2da9d-111">Create the [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) in the same method where you created the render target that you will use to draw the bitmap, and release the bitmap when the render target is released.</span></span>

<span data-ttu-id="2da9d-112">Depois que o bitmap for criado, renderize-o.</span><span class="sxs-lookup"><span data-stu-id="2da9d-112">Once the bitmap is created, render it.</span></span> <span data-ttu-id="2da9d-113">O exemplo a seguir usa o método [**DrawBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f_float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f)) para renderizar um bitmap várias vezes usando configurações de tamanho e opacidade diferentes.</span><span class="sxs-lookup"><span data-stu-id="2da9d-113">The following example uses the [**DrawBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f_float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f)) method to render a bitmap several times using different size and opacity settings.</span></span>


```C++
HRESULT DrawBitmapExample::OnRender()
{
    HRESULT hr;

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

        // Retrieve the size of the bitmap.
        D2D1_SIZE_F size = m_pBitmap->GetSize();

        D2D1_POINT_2F upperLeftCorner = D2D1::Point2F(100.f, 10.f);

        // Draw a bitmap.
        m_pRenderTarget->DrawBitmap(
            m_pBitmap,
            D2D1::RectF(
                upperLeftCorner.x,
                upperLeftCorner.y,
                upperLeftCorner.x + size.width,
                upperLeftCorner.y + size.height)
            );

        // Draw the next bitmap below the first one.
        upperLeftCorner.y = upperLeftCorner.y + size.height + 10.f;

        // Scale the bitmap to half its size using the linear
        // interoplation mode and draw it.
        float scaledWidth = size.width / 2.f;
        float scaledHeight = size.height / 2.f;
        m_pRenderTarget->DrawBitmap(
            m_pBitmap,
            D2D1::RectF(
                upperLeftCorner.x,
                upperLeftCorner.y,
                upperLeftCorner.x + scaledWidth,
                upperLeftCorner.y + scaledHeight),
            1.0,
            D2D1_BITMAP_INTERPOLATION_MODE_LINEAR
            );

        // Draw the bitmap at half its size and half its opacity.
        upperLeftCorner.y = upperLeftCorner.y + size.height / 2.f + 10.f;
        m_pRenderTarget->DrawBitmap(
            m_pBitmap,
            D2D1::RectF(
                upperLeftCorner.x,
                upperLeftCorner.y,
                upperLeftCorner.x + scaledWidth,
                upperLeftCorner.y + scaledHeight),
            0.5,
            D2D1_BITMAP_INTERPOLATION_MODE_LINEAR
            );

        // Draw a series of bitmaps with different opacity and
        // rotation angles.
        upperLeftCorner.y = upperLeftCorner.y + scaledHeight + 20.f;
        m_pRenderTarget->DrawBitmap(
            m_pBitmap,
            D2D1::RectF(
                upperLeftCorner.x,
                upperLeftCorner.y,
                upperLeftCorner.x + scaledWidth,
                upperLeftCorner.y + scaledHeight),
            0.5,
            D2D1_BITMAP_INTERPOLATION_MODE_LINEAR
            );

        D2D1_POINT_2F lowerLeftCorner = D2D1::Point2F(upperLeftCorner.x, upperLeftCorner.y + scaledHeight);
        D2D1_POINT_2F imageCenter = D2D1::Point2F(
            upperLeftCorner.x + scaledWidth / 2,
            upperLeftCorner.y + scaledHeight / 2
            );

        // Rotate the next bitmap by -20 degrees.
        m_pRenderTarget->SetTransform(
            D2D1::Matrix3x2F::Rotation(-20, imageCenter)
            );

        m_pRenderTarget->DrawBitmap(
            m_pBitmap,
            D2D1::RectF(
                upperLeftCorner.x,
                upperLeftCorner.y,
                upperLeftCorner.x + scaledWidth,
                upperLeftCorner.y + scaledHeight),
            0.75,
            D2D1_BITMAP_INTERPOLATION_MODE_LINEAR
            );

        m_pRenderTarget->SetTransform(
            D2D1::Matrix3x2F::Rotation(-45, imageCenter)
            );

        // Make the last bitmap fully opaque.
        m_pRenderTarget->DrawBitmap(
            m_pBitmap,
            D2D1::RectF(
                upperLeftCorner.x,
                upperLeftCorner.y,
                upperLeftCorner.x + scaledWidth,
                upperLeftCorner.y + scaledHeight),
            1.0,
            D2D1_BITMAP_INTERPOLATION_MODE_LINEAR
            );

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



<span data-ttu-id="2da9d-114">O método [**DrawBitmap**](id2d1rendertarget-drawbitmap.md) não retornará um código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="2da9d-114">The [**DrawBitmap**](id2d1rendertarget-drawbitmap.md) method does not return an error code if it fails.</span></span> <span data-ttu-id="2da9d-115">Para determinar se uma operação de desenho (como **DrawBitmap**) falhou, verifique o resultado retornado pelo método [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) , conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="2da9d-115">To determine whether a drawing operation (such as **DrawBitmap**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method, as shown in the following example.</span></span>


```C++
hr = m_pRenderTarget->EndDraw();
```



<span data-ttu-id="2da9d-116">O código foi omitido neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="2da9d-116">Code has been omitted from this example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2da9d-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2da9d-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2da9d-118">**DrawBitmap**</span><span class="sxs-lookup"><span data-stu-id="2da9d-118">**DrawBitmap**</span></span>](id2d1rendertarget-drawbitmap.md)
</dt> <dt>

[<span data-ttu-id="2da9d-119">**ID2D1Bitmap**</span><span class="sxs-lookup"><span data-stu-id="2da9d-119">**ID2D1Bitmap**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)
</dt> <dt>

[<span data-ttu-id="2da9d-120">Como carregar um bitmap de um recurso</span><span class="sxs-lookup"><span data-stu-id="2da9d-120">How to Load a Bitmap from a Resource</span></span>](how-to-load-a-bitmap-from-a-resource.md)
</dt> </dl>

 

 
---
title: Como criar um pincel de bitmap
description: Mostra como criar um pincel de bitmap usando Direct2D.
ms.assetid: 8f78b30a-7507-4dd8-b6f4-12d88e3c9a1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd8f28735368916d1abd0c1c9aa091dec4fd93f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105779566"
---
# <a name="how-to-create-a-bitmap-brush"></a><span data-ttu-id="b1091-103">Como criar um pincel de bitmap</span><span class="sxs-lookup"><span data-stu-id="b1091-103">How to Create a Bitmap Brush</span></span>

<span data-ttu-id="b1091-104">Para criar um pincel de bitmap, use o método [**ID2D1RenderTarget:: CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) e especifique as propriedades do pincel de bitmap.</span><span class="sxs-lookup"><span data-stu-id="b1091-104">To create a bitmap brush, use the [**ID2D1RenderTarget::CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) method and specify the bitmap brush properties.</span></span> <span data-ttu-id="b1091-105">Algumas sobrecargas permitem que você especifique as propriedades do pincel.</span><span class="sxs-lookup"><span data-stu-id="b1091-105">Some overloads enable you to specify the brush properties.</span></span> <span data-ttu-id="b1091-106">O código a seguir mostra como criar um pincel de bitmap para preencher um quadrado e um pincel preto sólido para desenhar o contorno do quadrado.</span><span class="sxs-lookup"><span data-stu-id="b1091-106">The following code shows how to create a bitmap brush to fill a square, and a solid black brush to draw the outline of the square.</span></span> <span data-ttu-id="b1091-107">O código produz a saída mostrada na captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b1091-107">The code produces the output shown in the following screen shot.</span></span>

> [!Note]  
> <span data-ttu-id="b1091-108">A partir do Windows 8, você pode usar o método [**CreateBitmapBrush**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties1_constd2d1_brush_properties_id2d1bitmapbrush1)) na interface [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) para criar um [**ID2D1BitmapBrush1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmapbrush1) em vez de um **ID2D1BitmapBrush**.</span><span class="sxs-lookup"><span data-stu-id="b1091-108">Starting with Windows 8, you can use the [**CreateBitmapBrush**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties1_constd2d1_brush_properties_id2d1bitmapbrush1)) method on the [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interface to create a [**ID2D1BitmapBrush1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmapbrush1) instead of a **ID2D1BitmapBrush**.</span></span> <span data-ttu-id="b1091-109">**ID2D1BitmapBrush1** adiciona modos de dimensionamento de alta qualidade ao pincel de bitmap.</span><span class="sxs-lookup"><span data-stu-id="b1091-109">**ID2D1BitmapBrush1** adds high-quality scaling modes to the bitmap brush.</span></span>

 

![captura de tela de um quadrado preenchido com um bitmap de fábrica](images/brushes-ovw-bitmap.png)

1.  <span data-ttu-id="b1091-111">Declare uma variável do tipo [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span><span class="sxs-lookup"><span data-stu-id="b1091-111">Declare a variable of type [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span></span>
    ```C++
        ID2D1BitmapBrush *m_pBitmapBrush;
    ```

    

2.  <span data-ttu-id="b1091-112">Carregar um bitmap de um recurso.</span><span class="sxs-lookup"><span data-stu-id="b1091-112">Load a bitmap from a resource.</span></span> <span data-ttu-id="b1091-113">Para obter mais informações, consulte [como carregar um bitmap de um recurso](how-to-load-a-bitmap-from-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="b1091-113">For more information, see [How to Load a Bitmap from a Resource](how-to-load-a-bitmap-from-a-resource.md).</span></span>
    ```C++
    // Create the bitmap to be used by the bitmap brush.
    if (SUCCEEDED(hr))
    {
        hr = LoadResourceBitmap(
            m_pRenderTarget,
            m_pWICFactory,
            L"FERN",
            L"Image",
            &m_pBitmap
            );
    ```

    

3.  <span data-ttu-id="b1091-114">Escolha os modos de extensão [**( \_ \_ modo de extensão de d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)) e modo de interpolação ([**\_ \_ \_ modo de interpolação de bitmap d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_bitmap_interpolation_mode)) do pincel de bitmap e, em seguida, chame o método [**CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) para criar um pincel, conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="b1091-114">Choose the extend modes ([**D2D1\_EXTEND\_MODE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)) and interpolation mode ([**D2D1\_BITMAP\_INTERPOLATION\_MODE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_bitmap_interpolation_mode)) of the bitmap brush and then call the [**CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) method to create a brush, as shown in the following code.</span></span>
    ```C++
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="b1091-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b1091-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1091-116">Referência de Direct2D</span><span class="sxs-lookup"><span data-stu-id="b1091-116">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 
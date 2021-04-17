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
# <a name="how-to-create-a-bitmap-brush"></a>Como criar um pincel de bitmap

Para criar um pincel de bitmap, use o método [**ID2D1RenderTarget:: CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) e especifique as propriedades do pincel de bitmap. Algumas sobrecargas permitem que você especifique as propriedades do pincel. O código a seguir mostra como criar um pincel de bitmap para preencher um quadrado e um pincel preto sólido para desenhar o contorno do quadrado. O código produz a saída mostrada na captura de tela a seguir.

> [!Note]  
> A partir do Windows 8, você pode usar o método [**CreateBitmapBrush**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties1_constd2d1_brush_properties_id2d1bitmapbrush1)) na interface [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) para criar um [**ID2D1BitmapBrush1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmapbrush1) em vez de um **ID2D1BitmapBrush**. **ID2D1BitmapBrush1** adiciona modos de dimensionamento de alta qualidade ao pincel de bitmap.

 

![captura de tela de um quadrado preenchido com um bitmap de fábrica](images/brushes-ovw-bitmap.png)

1.  Declare uma variável do tipo [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).
    ```C++
        ID2D1BitmapBrush *m_pBitmapBrush;
    ```

    

2.  Carregar um bitmap de um recurso. Para obter mais informações, consulte [como carregar um bitmap de um recurso](how-to-load-a-bitmap-from-a-resource.md).
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

    

3.  Escolha os modos de extensão [**( \_ \_ modo de extensão de d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)) e modo de interpolação ([**\_ \_ \_ modo de interpolação de bitmap d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_bitmap_interpolation_mode)) do pincel de bitmap e, em seguida, chame o método [**CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) para criar um pincel, conforme mostrado no código a seguir.
    ```C++
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
    ```

    

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de Direct2D](reference.md)
</dt> </dl>

 

 
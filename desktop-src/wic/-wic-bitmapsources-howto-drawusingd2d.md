---
description: Este tópico demonstra o processo para desenhar um IWICBitmapSource usando Direct2D.
ms.assetid: 11d38c9a-775d-41f7-a193-37b702b29a96
title: Como desenhar um BitmapSource usando Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d6636bb1d0b0294e7d496ffd8839c645ad046bb256001b2abd1744714eb4c48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117668696"
---
# <a name="how-to-draw-a-bitmapsource-using-direct2d"></a>Como desenhar um BitmapSource usando Direct2D

Este tópico demonstra o processo para desenhar [**um IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) usando Direct2D.

Para desenhar uma origem de bitmap usando Direct2D

1.  Decodificar uma imagem de origem e obter uma origem de bitmap. Neste exemplo, um [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) é usado para decodificar a imagem e o primeiro quadro de imagem é recuperado.

    ```C++
       // Create a decoder
       IWICBitmapDecoder *pDecoder = NULL;

       hr = m_pIWICFactory->CreateDecoderFromFilename(
           szFileName,                      // Image to be decoded
           NULL,                            // Do not prefer a particular vendor
           GENERIC_READ,                    // Desired read access to the file
           WICDecodeMetadataCacheOnDemand,  // Cache metadata when needed
           &pDecoder                        // Pointer to the decoder
           );

       // Retrieve the first frame of the image from the decoder
       IWICBitmapFrameDecode *pFrame = NULL;

       if (SUCCEEDED(hr))
       {
           hr = pDecoder->GetFrame(0, &pFrame);
       }
    ```

    

    Para obter tipos adicionais de fontes de bitmap a desenhar, consulte Visão [geral das fontes de bitmap.](-wic-bitmapsources.md)

2.  Converta a origem do bitmap em um formato de pixel 32bppPBGRA.

    Antes Direct2D pode usar uma imagem, ela deve ser convertida no formato de pixel 32bppPBGRA. Para converter o formato de imagem, use o [**método CreateFormatConverter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) para criar [**um objeto IWICFormatConverter.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) Depois de criado, use o [**método Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize) para executar a conversão.

    ```C++
       // Format convert the frame to 32bppPBGRA
       if (SUCCEEDED(hr))
       {
           SafeRelease(&m_pConvertedSourceBitmap);
           hr = m_pIWICFactory->CreateFormatConverter(&m_pConvertedSourceBitmap);
       }

       if (SUCCEEDED(hr))
       {
           hr = m_pConvertedSourceBitmap->Initialize(
               pFrame,                          // Input bitmap to convert
               GUID_WICPixelFormat32bppPBGRA,   // Destination pixel format
               WICBitmapDitherTypeNone,         // Specified dither pattern
               NULL,                            // Specify a particular palette 
               0.f,                             // Alpha threshold
               WICBitmapPaletteTypeCustom       // Palette translation type
               );
       }
    ```

    

3.  Crie um [objeto ID2D1RenderTarget](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) para renderização em um identificador de janela.

    ```C++
       // Create a D2D render target properties
       D2D1_RENDER_TARGET_PROPERTIES renderTargetProperties = D2D1::RenderTargetProperties();

       // Set the DPI to be the default system DPI to allow direct mapping
       // between image pixels and desktop pixels in different system DPI settings
       renderTargetProperties.dpiX = DEFAULT_DPI;
       renderTargetProperties.dpiY = DEFAULT_DPI;

       // Create a D2D render target
       D2D1_SIZE_U size = D2D1::SizeU(rc.right - rc.left, rc.bottom - rc.top);

       hr = m_pD2DFactory->CreateHwndRenderTarget(
           renderTargetProperties,
           D2D1::HwndRenderTargetProperties(hWnd, size),
           &m_pRT
           );
    ```

    

    Para obter mais informações sobre destinos de renderização, consulte a Visão geral Direct2D [destinos de renderização.](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)

4.  Crie um [objeto ID2D1Bitmap](../direct2d/render-targets-overview.md) usando o [método ID2D1RenderTarget::CreateBitmapFromWicBitmap.](../direct2d/id2d1rendertarget-createbitmapfromwicbitmap.md)

    ```C++
        // D2DBitmap may have been released due to device loss. 
        // If so, re-create it from the source bitmap
        if (m_pConvertedSourceBitmap && !m_pD2DBitmap)
        {
            m_pRT->CreateBitmapFromWicBitmap(m_pConvertedSourceBitmap, NULL, &m_pD2DBitmap);
        }
    ```

    

5.  Desenhe [o ID2D1Bitmap](../direct2d/render-targets-overview.md) usando o método D2D [ID2D1RenderTarget::D rawBitmap.](../direct2d/id2d1rendertarget-drawbitmap.md)

    ```C++
        // Draws an image and scales it to the current window size
        if (m_pD2DBitmap)
        {
            m_pRT->DrawBitmap(m_pD2DBitmap, rectangle);
        }
    ```

    

O código foi omitido neste exemplo. Para ver o código completo, consulte [Visualizador de Imagens do WIC usando Direct2D exemplo.](-wic-sample-d2d-viewer.md)

## <a name="see-also"></a>Consulte Também

[Guia de programação](-wic-programming-guide.md)


[Referência](-wic-codec-reference.md)


[Amostras](-wic-samples.md)


[Direct2D](../direct2d/direct2d-portal.md)


 

 

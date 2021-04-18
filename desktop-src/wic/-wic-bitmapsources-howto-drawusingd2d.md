---
description: Este tópico demonstra o processo para desenhar um IWICBitmapSource usando Direct2D.
ms.assetid: 11d38c9a-775d-41f7-a193-37b702b29a96
title: Como desenhar um BitmapSource usando Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6dfdddb7cd6f7ab7341eb3c13a9fe40b797f09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105816032"
---
# <a name="how-to-draw-a-bitmapsource-using-direct2d"></a><span data-ttu-id="cc9dd-103">Como desenhar um BitmapSource usando Direct2D</span><span class="sxs-lookup"><span data-stu-id="cc9dd-103">How to Draw a BitmapSource Using Direct2D</span></span>

<span data-ttu-id="cc9dd-104">Este tópico demonstra o processo para desenhar um [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) usando Direct2D.</span><span class="sxs-lookup"><span data-stu-id="cc9dd-104">This topic demonstrates the process for drawing an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) by using Direct2D.</span></span>

<span data-ttu-id="cc9dd-105">Para desenhar uma fonte de bitmap usando Direct2D</span><span class="sxs-lookup"><span data-stu-id="cc9dd-105">To draw a bitmap source by using Direct2D</span></span>

1.  <span data-ttu-id="cc9dd-106">Decodifique uma imagem de origem e obtenha uma fonte de bitmap.</span><span class="sxs-lookup"><span data-stu-id="cc9dd-106">Decode a source image and obtain a bitmap source.</span></span> <span data-ttu-id="cc9dd-107">Neste exemplo, um [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) é usado para decodificar a imagem e o primeiro quadro de imagem é recuperado.</span><span class="sxs-lookup"><span data-stu-id="cc9dd-107">In this example, an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) is used to decode the image and the first image frame is retrieved.</span></span>

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

    

    <span data-ttu-id="cc9dd-108">Para obter tipos adicionais de fontes de bitmap a serem desenhadas, consulte a [visão geral de fontes de bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="cc9dd-108">For additional types of bitmap sources to draw, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

2.  <span data-ttu-id="cc9dd-109">Converta a origem do bitmap em um formato de pixel 32bppPBGRA.</span><span class="sxs-lookup"><span data-stu-id="cc9dd-109">Convert the bitmap source to an 32bppPBGRA pixel format.</span></span>

    <span data-ttu-id="cc9dd-110">Antes que Direct2D possa usar uma imagem, ela deve ser convertida no formato de pixel 32bppPBGRA.</span><span class="sxs-lookup"><span data-stu-id="cc9dd-110">Before Direct2D can use an image, it must be converted to the 32bppPBGRA pixel format.</span></span> <span data-ttu-id="cc9dd-111">Para converter o formato de imagem, use o método [**Createformaconverter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) para criar um objeto [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) .</span><span class="sxs-lookup"><span data-stu-id="cc9dd-111">To convert the image format, use the [**CreateFormatConverter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) method to create an [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) object.</span></span> <span data-ttu-id="cc9dd-112">Depois de criado, use o método [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize) para executar a conversão.</span><span class="sxs-lookup"><span data-stu-id="cc9dd-112">Once created, use the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize) method to perform the conversion.</span></span>

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

    

3.  <span data-ttu-id="cc9dd-113">Crie um objeto [ID2D1RenderTarget](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) para renderização em um identificador de janela.</span><span class="sxs-lookup"><span data-stu-id="cc9dd-113">Create an [ID2D1RenderTarget](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) object for rendering to a window handle.</span></span>

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

    

    <span data-ttu-id="cc9dd-114">Para obter mais informações sobre destinos de renderização, consulte a [visão geral dos destinos de renderização](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)do Direct2D.</span><span class="sxs-lookup"><span data-stu-id="cc9dd-114">For more information render targets, see the Direct2D [Render Targets Overview](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget).</span></span>

4.  <span data-ttu-id="cc9dd-115">Crie um objeto [ID2D1Bitmap](../direct2d/render-targets-overview.md) usando o método [ID2D1RenderTarget:: CreateBitmapFromWicBitmap](../direct2d/id2d1rendertarget-createbitmapfromwicbitmap.md) .</span><span class="sxs-lookup"><span data-stu-id="cc9dd-115">Create an [ID2D1Bitmap](../direct2d/render-targets-overview.md) object using the [ID2D1RenderTarget::CreateBitmapFromWicBitmap](../direct2d/id2d1rendertarget-createbitmapfromwicbitmap.md) method.</span></span>

    ```C++
        // D2DBitmap may have been released due to device loss. 
        // If so, re-create it from the source bitmap
        if (m_pConvertedSourceBitmap && !m_pD2DBitmap)
        {
            m_pRT->CreateBitmapFromWicBitmap(m_pConvertedSourceBitmap, NULL, &m_pD2DBitmap);
        }
    ```

    

5.  <span data-ttu-id="cc9dd-116">Desenhe o [ID2D1Bitmap](../direct2d/render-targets-overview.md) usando D2D [ID2D1RenderTarget::D método rawbitmap](../direct2d/id2d1rendertarget-drawbitmap.md) .</span><span class="sxs-lookup"><span data-stu-id="cc9dd-116">Draw the [ID2D1Bitmap](../direct2d/render-targets-overview.md) using D2D [ID2D1RenderTarget::DrawBitmap](../direct2d/id2d1rendertarget-drawbitmap.md) method.</span></span>

    ```C++
        // Draws an image and scales it to the current window size
        if (m_pD2DBitmap)
        {
            m_pRT->DrawBitmap(m_pD2DBitmap, rectangle);
        }
    ```

    

<span data-ttu-id="cc9dd-117">O código foi omitido neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="cc9dd-117">Code has been omitted from this example.</span></span> <span data-ttu-id="cc9dd-118">Para obter o código completo, consulte o [Visualizador de imagem do WIC usando o exemplo Direct2D](-wic-sample-d2d-viewer.md).</span><span class="sxs-lookup"><span data-stu-id="cc9dd-118">For the complete code, see the [WIC Image Viewer Using Direct2D Sample](-wic-sample-d2d-viewer.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="cc9dd-119">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="cc9dd-119">See Also</span></span>

[<span data-ttu-id="cc9dd-120">Guia de programação</span><span class="sxs-lookup"><span data-stu-id="cc9dd-120">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="cc9dd-121">Referência</span><span class="sxs-lookup"><span data-stu-id="cc9dd-121">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="cc9dd-122">Amostras</span><span class="sxs-lookup"><span data-stu-id="cc9dd-122">Samples</span></span>](-wic-samples.md)


[<span data-ttu-id="cc9dd-123">Direct2D</span><span class="sxs-lookup"><span data-stu-id="cc9dd-123">Direct2D</span></span>](../direct2d/direct2d-portal.md)


 

 

---
title: Como carregar um bitmap de um arquivo
description: Mostra como carregar um bitmap Direct2D de um arquivo de imagem.
ms.assetid: 4abfbc2b-2730-4d96-897e-1e2232383a72
ms.topic: article
ms.date: 03/09/2019
ms.openlocfilehash: c9590e799e71e92056157b75573565cf79b9236b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641499"
---
# <a name="how-to-load-a-bitmap-from-a-file"></a><span data-ttu-id="c51a0-103">Como carregar um bitmap de um arquivo</span><span class="sxs-lookup"><span data-stu-id="c51a0-103">How to Load a Bitmap from a File</span></span>

<span data-ttu-id="c51a0-104">O Direct2D usa o Windows Imaging Component (WIC) para carregar bitmaps.</span><span class="sxs-lookup"><span data-stu-id="c51a0-104">Direct2D uses the Windows Imaging Component (WIC) to load bitmaps.</span></span> <span data-ttu-id="c51a0-105">Para carregar um bitmap de um arquivo, primeiro use os objetos do WIC para carregar a imagem e convertê-la em um formato compatível com Direct2D e, em seguida, use o método [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) para criar um [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span><span class="sxs-lookup"><span data-stu-id="c51a0-105">To load a bitmap from a file, first use WIC objects to load the image and to convert it to a Direct2D-compatible format, then use the [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) method to create an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span></span>

1.  <span data-ttu-id="c51a0-106">Crie um [**IWICBitmapDecoder**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapdecoder) usando o método [**IWICImagingFactory:: CreateDecoderFromFileName**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) .</span><span class="sxs-lookup"><span data-stu-id="c51a0-106">Create an [**IWICBitmapDecoder**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapdecoder) by using the [**IWICImagingFactory::CreateDecoderFromFileName**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method.</span></span>

    ```C++
    HRESULT DemoApp::LoadBitmapFromFile(
        ID2D1RenderTarget *pRenderTarget,
        IWICImagingFactory *pIWICFactory,
        PCWSTR uri,
        UINT destinationWidth,
        UINT destinationHeight,
        ID2D1Bitmap **ppBitmap
        )
    {
        IWICBitmapDecoder *pDecoder = NULL;
        IWICBitmapFrameDecode *pSource = NULL;
        IWICStream *pStream = NULL;
        IWICFormatConverter *pConverter = NULL;
        IWICBitmapScaler *pScaler = NULL;

        HRESULT hr = pIWICFactory->CreateDecoderFromFilename(
            uri,
            NULL,
            GENERIC_READ,
            WICDecodeMetadataCacheOnLoad,
            &pDecoder
            );
            
    ```

    

2.  <span data-ttu-id="c51a0-107">Recupere um quadro da imagem e armazene o quadro em um objeto [**IWICBitmapFrameDecode**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="c51a0-107">Retrieve a frame from the image and store the frame in an [**IWICBitmapFrameDecode**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

    ```C++
        if (SUCCEEDED(hr))
        {
            // Create the initial frame.
            hr = pDecoder->GetFrame(0, &pSource);
        }
    ```

    

3.  <span data-ttu-id="c51a0-108">O bitmap deve ser convertido em um formato que Direct2D possa usar, portanto, converta o formato de pixel da imagem em 32bppPBGRA.</span><span class="sxs-lookup"><span data-stu-id="c51a0-108">The bitmap must be converted to a format that Direct2D can use, so convert the image's pixel format to 32bppPBGRA.</span></span> <span data-ttu-id="c51a0-109">(Para obter uma lista de formatos com suporte, consulte [formatos de pixel e modos alfa](supported-pixel-formats-and-alpha-modes.md).).</span><span class="sxs-lookup"><span data-stu-id="c51a0-109">(For a list of supported formats, see [Pixel Formats and Alpha Modes](supported-pixel-formats-and-alpha-modes.md).).</span></span> <span data-ttu-id="c51a0-110">Chame o método [**IWICImagingFactory:: Createformaconverter**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) para criar um objeto [**IWICFormatConverter**](/windows/win32/api/wincodec/nn-wincodec-iwicformatconverter) e, em seguida, chame o método [**Initialize**](/windows/win32/api/wincodec/nf-wincodec-iwicformatconverter-initialize) do objeto **IWICFormatConverter** para executar a conversão.</span><span class="sxs-lookup"><span data-stu-id="c51a0-110">Call the [**IWICImagingFactory::CreateFormatConverter**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) method to create an [**IWICFormatConverter**](/windows/win32/api/wincodec/nn-wincodec-iwicformatconverter) object, then call the **IWICFormatConverter** object's [**Initialize**](/windows/win32/api/wincodec/nf-wincodec-iwicformatconverter-initialize) method to perform the conversion.</span></span>
    ```C++
        if (SUCCEEDED(hr))
        {

            // Convert the image format to 32bppPBGRA
            // (DXGI_FORMAT_B8G8R8A8_UNORM + D2D1_ALPHA_MODE_PREMULTIPLIED).
            hr = pIWICFactory->CreateFormatConverter(&pConverter);

        }
     
     
        if (SUCCEEDED(hr))
        {
            hr = pConverter->Initialize(
                pSource,
                GUID_WICPixelFormat32bppPBGRA,
                WICBitmapDitherTypeNone,
                NULL,
                0.f,
                WICBitmapPaletteTypeMedianCut
                );
    ```

    

4.  <span data-ttu-id="c51a0-111">Chame o método [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) para criar um objeto [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) que pode ser desenhado por um destino de renderização e usado com outros objetos Direct2D.</span><span class="sxs-lookup"><span data-stu-id="c51a0-111">Call the [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) method to create an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) object that can be drawn by a render target and used with other Direct2D objects.</span></span>
    ```C++
        if (SUCCEEDED(hr))
        {
        
            // Create a Direct2D bitmap from the WIC bitmap.
            hr = pRenderTarget->CreateBitmapFromWicBitmap(
                pConverter,
                NULL,
                ppBitmap
                );
        }

        SafeRelease(&pDecoder);
        SafeRelease(&pSource);
        SafeRelease(&pStream);
        SafeRelease(&pConverter);
        SafeRelease(&pScaler);

        return hr;
    }
    ```

    

<span data-ttu-id="c51a0-112">Algum código foi omitido deste exemplo.</span><span class="sxs-lookup"><span data-stu-id="c51a0-112">Some code has been omitted from this example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c51a0-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c51a0-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c51a0-114">**ID2D1Bitmap**</span><span class="sxs-lookup"><span data-stu-id="c51a0-114">**ID2D1Bitmap**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)
</dt> <dt>

[<span data-ttu-id="c51a0-115">**CreateBitmapFromWicBitmap**</span><span class="sxs-lookup"><span data-stu-id="c51a0-115">**CreateBitmapFromWicBitmap**</span></span>](id2d1rendertarget-createbitmapfromwicbitmap.md)
</dt> <dt>

[<span data-ttu-id="c51a0-116">Como carregar um bitmap de um recurso</span><span class="sxs-lookup"><span data-stu-id="c51a0-116">How to Load a Bitmap from a Resource</span></span>](how-to-load-a-bitmap-from-a-resource.md)
</dt> </dl>

 

 
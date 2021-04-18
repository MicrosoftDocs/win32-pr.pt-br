---
title: Como carregar um bitmap de um recurso (Direct2D)
description: Mostra como carregar um bitmap Direct2D armazenado como um recurso de aplicativo.
ms.assetid: 7285e6ea-ebc7-4693-8a77-99bff0b5d0d1
ms.topic: article
ms.date: 03/09/2019
ms.openlocfilehash: fe96ba4e0674392333173df7daeb5a354a379343
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105759151"
---
# <a name="how-to-load-a-bitmap-from-a-resource-direct2d"></a><span data-ttu-id="6c022-103">Como carregar um bitmap de um recurso (Direct2D)</span><span class="sxs-lookup"><span data-stu-id="6c022-103">How to Load a Bitmap from a Resource (Direct2D)</span></span>

<span data-ttu-id="6c022-104">Conforme descrito em [como carregar um bitmap de um arquivo](how-to-load-a-direct2d-bitmap-from-a-file.md), o Direct2D usa o Windows Imaging Component (WIC) para carregar bitmaps.</span><span class="sxs-lookup"><span data-stu-id="6c022-104">As described in [How to Load a Bitmap from a File](how-to-load-a-direct2d-bitmap-from-a-file.md), Direct2D uses the Windows Imaging Component (WIC) to load bitmaps.</span></span> <span data-ttu-id="6c022-105">Para carregar um bitmap de um recurso, use objetos WIC para carregar a imagem e convertê-la em um formato compatível com Direct2D; em seguida, use o método [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) para criar um [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span><span class="sxs-lookup"><span data-stu-id="6c022-105">To load a bitmap from a resource, use WIC objects to load the image and to convert it to a Direct2D-compatible format; then, use the [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) method to create an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span></span>

1.  <span data-ttu-id="6c022-106">No [arquivo de definição de recurso de aplicativo](/windows/desktop/menurc/about-resource-files), defina o recurso.</span><span class="sxs-lookup"><span data-stu-id="6c022-106">In the [application resource definition file](/windows/desktop/menurc/about-resource-files), define the resource.</span></span> <span data-ttu-id="6c022-107">O exemplo a seguir define um recurso chamado "SampleImage".</span><span class="sxs-lookup"><span data-stu-id="6c022-107">The following example defines a resource named "SampleImage".</span></span>

    ```C++
    // THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
    // ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
    // THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
    // PARTICULAR PURPOSE.
    //
    // Copyright (c) Microsoft Corporation. All rights reserved
    #include "windows.h"

    SampleImage Image "sampleImage.jpg"
    ```

<span data-ttu-id="6c022-108">Este recurso será adicionado ao arquivo de recursos do aplicativo quando o aplicativo for compilado.</span><span class="sxs-lookup"><span data-stu-id="6c022-108">This resource will be added to the application's resource file when the application is built.</span></span>

2.  <span data-ttu-id="6c022-109">Carregue a imagem do arquivo de recurso do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6c022-109">Load the image from the application resource file.</span></span>

    ```C++
    HRESULT DemoApp::LoadResourceBitmap(
        ID2D1RenderTarget *pRenderTarget,
        IWICImagingFactory *pIWICFactory,
        PCWSTR resourceName,
        PCWSTR resourceType,
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

        HRSRC imageResHandle = NULL;
        HGLOBAL imageResDataHandle = NULL;
        void *pImageFile = NULL;
        DWORD imageFileSize = 0;

        // Locate the resource.
        imageResHandle = FindResourceW(HINST_THISCOMPONENT, resourceName, resourceType);
        HRESULT hr = imageResHandle ? S_OK : E_FAIL;
        if (SUCCEEDED(hr))
        {
            // Load the resource.
            imageResDataHandle = LoadResource(HINST_THISCOMPONENT, imageResHandle);

            hr = imageResDataHandle ? S_OK : E_FAIL;
        }
    ```

    

3.  <span data-ttu-id="6c022-110">Bloqueie o recurso e calcule o tamanho da imagem.</span><span class="sxs-lookup"><span data-stu-id="6c022-110">Lock the resource and calculate the image's size.</span></span>
    ```C++
        if (SUCCEEDED(hr))
        {
            // Lock it to get a system memory pointer.
            pImageFile = LockResource(imageResDataHandle);

            hr = pImageFile ? S_OK : E_FAIL;
        }
        if (SUCCEEDED(hr))
        {
            // Calculate the size.
            imageFileSize = SizeofResource(HINST_THISCOMPONENT, imageResHandle);

            hr = imageFileSize ? S_OK : E_FAIL;
            
        }
    ```

    

4.  <span data-ttu-id="6c022-111">Use o método [**IWICImagingFactory:: CreateStream**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createstream) para criar um objeto [**IWICStream**](/windows/win32/api/wincodec/nn-wincodec-iwicstream) .</span><span class="sxs-lookup"><span data-stu-id="6c022-111">Use the [**IWICImagingFactory::CreateStream**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createstream) method to create an [**IWICStream**](/windows/win32/api/wincodec/nn-wincodec-iwicstream) object.</span></span>
    ```C++
        if (SUCCEEDED(hr))
        {
              // Create a WIC stream to map onto the memory.
            hr = pIWICFactory->CreateStream(&pStream);
        }
        if (SUCCEEDED(hr))
        {
            // Initialize the stream with the memory pointer and size.
            hr = pStream->InitializeFromMemory(
                reinterpret_cast<BYTE*>(pImageFile),
                imageFileSize
                );
        }
    ```

    

5.  <span data-ttu-id="6c022-112">Use o método [**IWICImagingFactory:: CreateDecoderFromStream**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) para criar um [**IWICBitmapDecoder**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapdecoder).</span><span class="sxs-lookup"><span data-stu-id="6c022-112">Use the [**IWICImagingFactory::CreateDecoderFromStream**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) method to create an [**IWICBitmapDecoder**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

    ```C++
        if (SUCCEEDED(hr))
        {
            // Create a decoder for the stream.
            hr = pIWICFactory->CreateDecoderFromStream(
                pStream,
                NULL,
                WICDecodeMetadataCacheOnLoad,
                &pDecoder
                );
        }
    ```

    

6.  <span data-ttu-id="6c022-113">Recupere um quadro da imagem e armazene-o em um objeto [**IWICBitmapFrameDecode**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="6c022-113">Retrieve a frame from the image and store it in an [**IWICBitmapFrameDecode**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

    ```C++
        if (SUCCEEDED(hr))
        {
            // Create the initial frame.
            hr = pDecoder->GetFrame(0, &pSource);
        }
    ```

    

7.  <span data-ttu-id="6c022-114">Antes que Direct2D possa usar a imagem, ela deve ser convertida no formato de pixel 32bppPBGRA.</span><span class="sxs-lookup"><span data-stu-id="6c022-114">Before Direct2D can use the image, it must be converted to the 32bppPBGRA pixel format.</span></span> <span data-ttu-id="6c022-115">Para converter o formato de imagem, use o método [**IWICImagingFactory:: Createformaconverter**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) para criar um objeto [**IWICFormatConverter**](/windows/win32/api/wincodec/nn-wincodec-iwicformatconverter) e, em seguida, use o método [**Initialize**](/windows/win32/api/wincodec/nf-wincodec-iwicformatconverter-initialize) do objeto **IWICFormatConverter** para executar a conversão.</span><span class="sxs-lookup"><span data-stu-id="6c022-115">To convert the image format, use the [**IWICImagingFactory::CreateFormatConverter**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) method to create an [**IWICFormatConverter**](/windows/win32/api/wincodec/nn-wincodec-iwicformatconverter) object, then use the **IWICFormatConverter** object's [**Initialize**](/windows/win32/api/wincodec/nf-wincodec-iwicformatconverter-initialize) method to perform the conversion.</span></span>
 
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

    

8.  <span data-ttu-id="6c022-116">Por fim, use o método [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) para criar um objeto [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) que pode ser desenhado por um destino de renderização e usado com outros objetos Direct2D.</span><span class="sxs-lookup"><span data-stu-id="6c022-116">Finally, use the [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) method to create an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) object that can be drawn by a render target and used with other Direct2D objects.</span></span>
    ```C++
        if (SUCCEEDED(hr))
        {
            //create a Direct2D bitmap from the WIC bitmap.
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

    

<span data-ttu-id="6c022-117">Algum código foi omitido deste exemplo.</span><span class="sxs-lookup"><span data-stu-id="6c022-117">Some code has been omitted from this example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6c022-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6c022-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c022-119">Como carregar um bitmap de um arquivo</span><span class="sxs-lookup"><span data-stu-id="6c022-119">How to Load a Bitmap from a File</span></span>](how-to-load-a-direct2d-bitmap-from-a-file.md)
</dt> </dl>

 

 

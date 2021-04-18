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
# <a name="how-to-load-a-bitmap-from-a-resource-direct2d"></a>Como carregar um bitmap de um recurso (Direct2D)

Conforme descrito em [como carregar um bitmap de um arquivo](how-to-load-a-direct2d-bitmap-from-a-file.md), o Direct2D usa o Windows Imaging Component (WIC) para carregar bitmaps. Para carregar um bitmap de um recurso, use objetos WIC para carregar a imagem e convertê-la em um formato compatível com Direct2D; em seguida, use o método [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) para criar um [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).

1.  No [arquivo de definição de recurso de aplicativo](/windows/desktop/menurc/about-resource-files), defina o recurso. O exemplo a seguir define um recurso chamado "SampleImage".

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

Este recurso será adicionado ao arquivo de recursos do aplicativo quando o aplicativo for compilado.

2.  Carregue a imagem do arquivo de recurso do aplicativo.

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

    

3.  Bloqueie o recurso e calcule o tamanho da imagem.
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

    

4.  Use o método [**IWICImagingFactory:: CreateStream**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createstream) para criar um objeto [**IWICStream**](/windows/win32/api/wincodec/nn-wincodec-iwicstream) .
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

    

5.  Use o método [**IWICImagingFactory:: CreateDecoderFromStream**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) para criar um [**IWICBitmapDecoder**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapdecoder).

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

    

6.  Recupere um quadro da imagem e armazene-o em um objeto [**IWICBitmapFrameDecode**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframedecode) .

    ```C++
        if (SUCCEEDED(hr))
        {
            // Create the initial frame.
            hr = pDecoder->GetFrame(0, &pSource);
        }
    ```

    

7.  Antes que Direct2D possa usar a imagem, ela deve ser convertida no formato de pixel 32bppPBGRA. Para converter o formato de imagem, use o método [**IWICImagingFactory:: Createformaconverter**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) para criar um objeto [**IWICFormatConverter**](/windows/win32/api/wincodec/nn-wincodec-iwicformatconverter) e, em seguida, use o método [**Initialize**](/windows/win32/api/wincodec/nf-wincodec-iwicformatconverter-initialize) do objeto **IWICFormatConverter** para executar a conversão.
 
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

    

8.  Por fim, use o método [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) para criar um objeto [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) que pode ser desenhado por um destino de renderização e usado com outros objetos Direct2D.
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

    

Algum código foi omitido deste exemplo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como carregar um bitmap de um arquivo](how-to-load-a-direct2d-bitmap-from-a-file.md)
</dt> </dl>

 

 

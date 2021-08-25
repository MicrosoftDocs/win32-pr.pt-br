---
title: Como carregar um bitmap de um arquivo
description: Mostra como carregar um bitmap Direct2D de um arquivo de imagem.
ms.assetid: 4abfbc2b-2730-4d96-897e-1e2232383a72
ms.topic: article
ms.date: 03/09/2019
ms.openlocfilehash: a330f0e32ee4abf62eb7df1c1d6a00b3f217e6f04502cebae6c489aa01eaaa9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824556"
---
# <a name="how-to-load-a-bitmap-from-a-file"></a>Como carregar um bitmap de um arquivo

Direct2D usa o WIC (Windows Imaging Component) para carregar bitmaps. Para carregar um bitmap de um arquivo, primeiro use objetos WIC para carregar a imagem e convertê-la em um formato compatível com Direct2D e, em seguida, use o método [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) para criar [**um ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).

1.  Crie um [**IWICBitmapDecoder**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapdecoder) usando o [**método IWICImagingFactory::CreateDecoderFromFileName.**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename)

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

    

2.  Recupere um quadro da imagem e armazene o quadro em um [**objeto IWICBitmapFrameDecode.**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframedecode)

    ```C++
        if (SUCCEEDED(hr))
        {
            // Create the initial frame.
            hr = pDecoder->GetFrame(0, &pSource);
        }
    ```

    

3.  O bitmap deve ser convertido em um formato que Direct2D pode usar, portanto, converta o formato de pixel da imagem em 32bppPBGRA. (Para ver uma lista dos formatos com suporte, consulte [Formatos de pixel e modos alfa.).](supported-pixel-formats-and-alpha-modes.md) Chame o método [**IWICImagingFactory::CreateFormatConverter**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) para criar um objeto [**IWICFormatConverter**](/windows/win32/api/wincodec/nn-wincodec-iwicformatconverter) e, em seguida, chame o método [**Initialize**](/windows/win32/api/wincodec/nf-wincodec-iwicformatconverter-initialize) do objeto **IWICFormatConverter** para executar a conversão.
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

    

4.  Chame o [**método CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) para criar um objeto [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) que pode ser desenhado por um destino de renderização e usado com outros Direct2D objetos.
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

    

Algum código foi omitido deste exemplo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)
</dt> <dt>

[**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md)
</dt> <dt>

[Como carregar um bitmap de um recurso](how-to-load-a-bitmap-from-a-resource.md)
</dt> </dl>

 

 
---
description: Este tópico demonstra como modificar os pixels de uma fonte de bitmap usando os componentes IWICBitmap e IWICBitmapLock.
ms.assetid: a08af015-bc42-4a31-af03-106714b08d08
title: Como modificar os pixels de uma origem de bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbfa25a5f09742066c4e67af1fb1735aa038f086d6a107e88ae34e7b7c597770
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965385"
---
# <a name="how-to-modify-the-pixels-of-a-bitmap-source"></a>Como modificar os pixels de uma origem de bitmap

Este tópico demonstra como modificar os pixels de uma fonte de bitmap usando os componentes [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) e [**IWICBitmapLock.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)

Para modificar os pixels de uma origem de bitmap

1.  Crie um [**objeto IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) para criar Windows WIC (Componente de Imagem).

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  Use o [**método CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) para criar [**um IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) de um arquivo de imagem.

    ```C++
    HRESULT hr = S_OK;

    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame  = NULL;

    hr = m_pIWICFactory->CreateDecoderFromFilename(
       L"turtle.jpg",                  // Image to be decoded
       NULL,                           // Do not prefer a particular vendor
       GENERIC_READ,                   // Desired read access to the file
       WICDecodeMetadataCacheOnDemand, // Cache metadata when needed
       &pIDecoder                      // Pointer to the decoder
       );
    ```

    

3.  Obter o [**primeiro IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) da imagem.

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    O formato de arquivo JPEG dá suporte apenas a um único quadro. Como o arquivo neste exemplo é um arquivo JPEG, o primeiro quadro ( `0` ) é usado. Para formatos de imagem que têm vários quadros, consulte [Como](-wic-bitmapsources-howto-retrieveimageframes.md) recuperar os quadros de uma imagem para acessar cada quadro da imagem.

4.  Crie um [**IWICBitmap do**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) quadro de imagem obtido anteriormente.

    ```C++
    IWICBitmap *pIBitmap = NULL;
    IWICBitmapLock *pILock = NULL;

    UINT uiWidth = 10;
    UINT uiHeight = 10;

    WICRect rcLock = { 0, 0, uiWidth, uiHeight };

    // Create the bitmap from the image frame.
    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapFromSource(
          pIDecoderFrame,          // Create a bitmap from the image frame
          WICBitmapCacheOnDemand,  // Cache metadata when needed
          &pIBitmap);              // Pointer to the bitmap
    }
    ```

    

5.  Obtenha um [**IWICBitmapLock para**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) um retângulo especificado do [**IWICBitmap.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)

    ```C++
    if (SUCCEEDED(hr))
    {
       // Obtain a bitmap lock for exclusive write.
       // The lock is for a 10x10 rectangle starting at the top left of the
       // bitmap.
       hr = pIBitmap->Lock(&rcLock, WICBitmapLockWrite, &pILock);
    ```

    

6.  Processe os dados de pixel que agora estão bloqueados pelo [**objeto IWICBitmapLock.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)

    ```C++
       if (SUCCEEDED(hr))
       {
          UINT cbBufferSize = 0;
          BYTE *pv = NULL;

          // Retrieve a pointer to the pixel data.
          if (SUCCEEDED(hr))
          {
             hr = pILock->GetDataPointer(&cbBufferSize, &pv);
          }
          
          // Pixel manipulation using the image data pointer pv.
          // ...

          // Release the bitmap lock.
          SafeRelease(&pILock);
       }
    }
    ```

    

    Para desbloquear [**o IWICBitmap,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)chame [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) em todos os [**objetos IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) associados ao **IWICBitmap.**

7.  Limpar objetos criados.

    ```C++
    SafeRelease(&pIBitmap);
    SafeRelease(&pIDecoder);
    SafeRelease(&pIDecoderFrame);
    ```

    

## <a name="see-also"></a>Consulte Também

[Guia de programação](-wic-programming-guide.md)


[Referência](-wic-codec-reference.md)


[Amostras](-wic-samples.md)


 

 

---
description: Este tópico demonstra como girar um IWICBitmapSource usando um componente IWICBitmapFlipRotator.
ms.assetid: 371c7759-0165-4a2a-b2ff-f9c8a31053a4
title: Como inverter e girar uma fonte de bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f6a805144025f185a4f4793fc4fafb27d7695a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090286"
---
# <a name="how-to-flip-and-rotate-a-bitmap-source"></a>Como inverter e girar uma fonte de bitmap

Este tópico demonstra como girar um [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) usando um componente [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) .

Para inverter e girar uma origem de bitmap

1.  Crie um objeto [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) para criar objetos do Windows Imaging Component (WIC).

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  Use o método [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) para criar um [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) a partir de um arquivo de imagem.

    ```C++
    HRESULT hr = S_OK;

    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame  = NULL;
    IWICBitmapFlipRotator *pIFlipRotator = NULL;

    hr = m_pIWICFactory->CreateDecoderFromFilename(
       L"turtle.jpg",                  // Image to be decoded
       NULL,                           // Do not prefer a particular vendor
       GENERIC_READ,                   // Desired read access to the file
       WICDecodeMetadataCacheOnDemand, // Cache metadata when needed
       &pIDecoder                      // Pointer to the decoder
       );
    ```

    

3.  Obtenha o primeiro [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) da imagem.

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    O formato de arquivo JPEG só dá suporte a um único quadro. Como o arquivo neste exemplo é um arquivo JPEG, o primeiro quadro ( `0` ) é usado. Para formatos de imagem que têm vários quadros, consulte [como recuperar os quadros de uma imagem](-wic-bitmapsources-howto-retrieveimageframes.md) para acessar cada quadro da imagem.

4.  Crie o [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) a ser usado para inverter a imagem.

    ```C++
    // Create the flip/rotator.
    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapFlipRotator(&pIFlipRotator);
    }
    ```

    

5.  Inicialize o objeto flip/roto com os dados da imagem do quadro de bitmap virado horizontalmente (ao longo do eixo y vertical).

    ```C++
    // Initialize the flip/rotator to flip the original source horizontally.
    if (SUCCEEDED(hr))
    {
       hr = pIFlipRotator->Initialize(
          pIDecoderFrame,                     // Bitmap source to flip.
          WICBitmapTransformFlipHorizontal);  // Flip the pixels along the 
                                              //  vertical y-axis.
    }
    ```

    

    Consulte [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) para ver rotações adicionais e opções de inversão.

6.  Desenhe ou processe a origem do bitmap invertido.

    > [!Note]  
    > A interface [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) herda da interface [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) , de modo que você pode usar o objeto de flip/roto inicializado em qualquer lugar que aceite um **IWICBitmapSource**.

     

    A ilustração a seguir demonstra como inverter uma imagem horizontalmente (ao longo do eixo x vertical).

    ![ilustração mostrando um flip horizontal (ao longo do eixo x do Verital) de uma imagem](graphics/fliphorizontal.png)

## <a name="see-also"></a>Consulte Também

[Guia de programação](-wic-programming-guide.md)


[Referência](-wic-codec-reference.md)


[Amostras](-wic-samples.md)


 

 




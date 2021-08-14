---
description: Este tópico demonstra como dimensionar um IWICBitmapSource usando o componente IWICBitmapScaler.
ms.assetid: d2c65c9b-6f52-46f7-935d-0c582ca83867
title: Como dimensionar uma origem de bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2771ed13c23fdb3d74cf9c24899bea7a355efefcb5e541ac21aff53f372ded0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118439676"
---
# <a name="how-to-scale-a-bitmap-source"></a>Como dimensionar uma origem de bitmap

Este tópico demonstra como dimensionar um [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) usando o [**componente IWICBitmapScaler.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)

Para dimensionar uma origem de bitmap

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
    IWICBitmapScaler *pIScaler = NULL;


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

4.  Crie o [**IWICBitmapScaler a**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) ser usado para o dimensionamento de imagem.

    ```C++
    // Create the scaler.
    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapScaler(&pIScaler);
    }
    ```

    

5.  Inicialize o objeto de dimensionador com os dados de imagem do quadro de bitmap pela metade do tamanho.

    ```C++
    // Initialize the scaler to half the size of the original source.
    if (SUCCEEDED(hr))
    {
       hr = pIScaler->Initialize(
          pIDecoderFrame,                    // Bitmap source to scale.
          uiWidth/2,                         // Scale width to half of original.
          uiHeight/2,                        // Scale height to half of original.
          WICBitmapInterpolationModeFant);   // Use Fant mode interpolation.
    }
    ```

    

6.  Desenhar ou processar a origem do bitmap dimensionado.

    A ilustração a seguir demonstra o dimensionamento de imagens. A imagem original à esquerda é de 200 x 130 pixels. A imagem à direita é a imagem original dimensionada para metade do tamanho.

    ![ilustração mostrando o dimensionamento de uma imagem para um tamanho menor](graphics/scaledregion.png)

## <a name="see-also"></a>Consulte Também

[Guia de programação](-wic-programming-guide.md)


[Referência](-wic-codec-reference.md)


[Amostras](-wic-samples.md)


 

 




---
description: Este tópico descreve como criar um decodificador de bitmap usando um nome de arquivo de imagem.
ms.assetid: b384861d-4e71-4e07-8b44-5c1cbcb3a70f
title: Como criar um decodificador usando um nome de arquivo de imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 113ea82b741f2a8dab6c92d6391d65eb7d7e99c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760964"
---
# <a name="how-to-create-a-decoder-using-an-image-filename"></a>Como criar um decodificador usando um nome de arquivo de imagem

Este tópico descreve como criar um decodificador de bitmap usando um nome de arquivo de imagem.

Para criar um decodificador de bitmap usando um nome de arquivo de imagem

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

4.  Processar o quadro da imagem. Para obter informações adicionais sobre objetos [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) , consulte a [visão geral de fontes de bitmap](-wic-bitmapsources.md).

## <a name="see-also"></a>Consulte Também

[Guia de programação](-wic-programming-guide.md)


[Referência](-wic-codec-reference.md)


[Amostras](-wic-samples.md)


 

 




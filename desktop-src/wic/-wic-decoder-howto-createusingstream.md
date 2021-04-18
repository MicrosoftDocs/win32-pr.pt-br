---
description: Este tópico descreve como criar um decodificador de bitmap usando um fluxo.
ms.assetid: 982d2110-ff2f-43e0-a931-cb2b8146ad0a
title: Como criar um decodificador usando um fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b0a76badec0e2587f9136cfa6bc3ff041b76592
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788874"
---
# <a name="how-to-create-a-decoder-using-a-stream"></a>Como criar um decodificador usando um fluxo

Este tópico descreve como criar um decodificador de bitmap usando um fluxo.

Para criar um decodificador de bitmap usando um fluxo

1.  Carregar um arquivo de imagem em um fluxo. Neste exemplo, um fluxo é criado para um recurso de aplicativo.

    No arquivo de definição de recurso de aplicativo (. rc), defina o recurso. O exemplo a seguir define um `Image` recurso chamado `IDR_SAMPLE_IMAGE` .

    ```C++
    IDR_SAMPLE_IMAGE IMAGE "turtle.jpg"
    ```

    

    O recurso será adicionado aos recursos do aplicativo quando o aplicativo for compilado.

2.  Carregue o recurso do aplicativo.

    ```C++
    HRESULT hr = S_OK;

    // WIC interface pointers.
    IWICStream *pIWICStream = NULL;
    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame = NULL;

    // Resource management.
    HRSRC imageResHandle = NULL;
    HGLOBAL imageResDataHandle = NULL;
    void *pImageFile = NULL;
    DWORD imageFileSize = 0;

    // Locate the resource in the application's executable.
    imageResHandle = FindResource(
       NULL,             // This component.
       L"SampleImage",   // Resource name.
       L"Image");        // Resource type.

    hr = (imageResHandle ? S_OK : E_FAIL);

    // Load the resource to the HGLOBAL.
    if (SUCCEEDED(hr)){
       imageResDataHandle = LoadResource(NULL, imageResHandle);
       hr = (imageResDataHandle ? S_OK : E_FAIL);
    }
    
    ```

    

3.  Bloqueie o recurso e obtenha o tamanho.

    ```C++
    // Lock the resource to retrieve memory pointer.
    if (SUCCEEDED(hr)){
       pImageFile = LockResource(imageResDataHandle);
       hr = (pImageFile ? S_OK : E_FAIL);
    }

    // Calculate the size.
    if (SUCCEEDED(hr)){
       imageFileSize = SizeofResource(NULL, imageResHandle);
       hr = (imageFileSize ? S_OK : E_FAIL);
    }
    
    ```

    

4.  Crie um [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) para criar objetos do Windows Imaging Component (WIC).

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

5.  Use o método [**CreateStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) para criar um objeto [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) e inicializá-lo usando o ponteiro de memória da imagem.

    ```C++
    // Create a WIC stream to map onto the memory.
    if (SUCCEEDED(hr)){
       hr = m_pIWICFactory->CreateStream(&pIWICStream);
    }

    // Initialize the stream with the memory pointer and size.
    if (SUCCEEDED(hr)){
       hr = pIWICStream->InitializeFromMemory(
             reinterpret_cast<BYTE*>(pImageFile),
             imageFileSize);
    }
    ```

    

6.  Crie um [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) a partir do novo objeto de fluxo usando o método [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) .

    ```C++
    // Create a decoder for the stream.
    if (SUCCEEDED(hr)){
       hr = m_pIWICFactory->CreateDecoderFromStream(
          pIWICStream,                   // The stream to use to create the decoder
          NULL,                          // Do not prefer a particular vendor
          WICDecodeMetadataCacheOnLoad,  // Cache metadata when needed
          &pIDecoder);                   // Pointer to the decoder
    }
    ```

    

7.  Obtenha o primeiro [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) da imagem.

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    O formato de arquivo JPEG só dá suporte a um único quadro. Como o arquivo neste exemplo é um arquivo JPEG, o primeiro quadro ( `0` ) é usado. Para formatos de imagem que têm vários quadros, consulte [como recuperar os quadros de uma imagem](-wic-bitmapsources-howto-retrieveimageframes.md) para acessar cada quadro da imagem.

8.  Processar o quadro da imagem. Para obter informações adicionais sobre objetos [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) , consulte a [visão geral de fontes de bitmap](-wic-bitmapsources.md).

## <a name="see-also"></a>Consulte Também

[Guia de programação](-wic-programming-guide.md)


[Referência](-wic-codec-reference.md)


[Amostras](-wic-samples.md)


 

 




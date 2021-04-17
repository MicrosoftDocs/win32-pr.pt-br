---
description: O exemplo a seguir demonstra como codificar novamente uma imagem e seus metadados para um novo arquivo do mesmo formato.
ms.assetid: a7cfaa6d-e17d-458a-ae63-72963615bef8
title: Como codificar novamente uma imagem JPEG com metadados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c023defb760faeab2bc6ea92232fcc916ef15126
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/20/2021
ms.locfileid: "105780329"
---
# <a name="how-to-re-encode-a-jpeg-image-with-metadata"></a>Como codificar novamente uma imagem JPEG com metadados

O exemplo a seguir demonstra como codificar novamente uma imagem e seus metadados para um novo arquivo do mesmo formato. Além disso, este exemplo adiciona metadados para demonstrar uma expressão de item único usada por um gravador de consulta.

Este tópico inclui as seções a seguir.

-   [Pré-requisitos](#prerequisites)
-   [Parte 1: decodificar uma imagem](#part-1-decode-an-image)
-   [Parte 2: criar e inicializar o codificador de imagem](#part-2-create-and-initialize-the-image-encoder)
-   [Parte 3: copiar informações de quadro decodificado](#part-3-copy-decoded-frame-information)
-   [Parte 4: copiar os metadados](#part-4-copy-the-metadata)
-   [Parte 5: adicionar metadados adicionais](#part-5-add-additional-metadata)
-   [Parte 6: finalizar a imagem codificada](#part-6-finalize-the-encoded-image)
-   [Código de exemplo de recodificação JPEG](#jpeg-re-encode-example-code)
-   [Tópicos relacionados](#related-topics)

## <a name="prerequisites"></a>Pré-requisitos

Para entender este tópico, você deve estar familiarizado com o sistema de metadados do Windows Imaging Component (WIC), conforme descrito na [visão geral dos metadados do WIC](-wic-about-metadata.md). Você também deve estar familiarizado com os componentes do codec do WIC, conforme descrito na [visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md).

## <a name="part-1-decode-an-image"></a>Parte 1: decodificar uma imagem

Antes de copiar dados de imagem ou metadados para um novo arquivo de imagem, você deve primeiro criar um decodificador para a imagem existente que deseja codificar novamente. O código a seguir demonstra como criar um decodificador WIC para o arquivo de imagem test.jpg.


```C++
    // Initialize COM.
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    IWICImagingFactory *piFactory = NULL;
    IWICBitmapDecoder *piDecoder = NULL;

    // Create the COM imaging factory.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_WICImagingFactory,
        NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&piFactory));
    }

    // Create the decoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateDecoderFromFilename(L"test.jpg", NULL, GENERIC_READ,
            WICDecodeMetadataCacheOnDemand, //For JPEG lossless decoding/encoding.
            &piDecoder);
    }
```



A chamada para **CreateDecoderFromFilename** usou o valor WICDecodeMetadataCacheOnDemand da enumeração [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) como o quarto parâmetro. Isso informa ao decodificador para armazenar em cache os metadados quando os metadados são necessários, obtendo um leitor de consulta ou usando o leitor de metadados subjacente. O uso dessa opção permite que você retenha o fluxo para os metadados, o que é necessário para executar a codificação de metadados rápida e permite a decodificação e a codificação de imagens JPEG sem perdas. Como alternativa, você pode usar o outro valor **WICDecodeOptions** , WICDecodeMetadataCacheOnLoad, que armazena em cache os metadados da imagem inserida assim que a imagem é carregada.

## <a name="part-2-create-and-initialize-the-image-encoder"></a>Parte 2: criar e inicializar o codificador de imagem

O código a seguir demonstra a criação do codificador que você usará para codificar a imagem decodificada anteriormente.


```C++
    // Variables used for encoding.
    IWICStream *piFileStream = NULL;
    IWICBitmapEncoder *piEncoder = NULL;
    IWICMetadataBlockWriter *piBlockWriter = NULL;
    IWICMetadataBlockReader *piBlockReader = NULL;

    WICPixelFormatGUID pixelFormat = { 0 };
    UINT count = 0;
    double dpiX, dpiY = 0.0;
    UINT width, height = 0;

    // Create a file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateStream(&piFileStream);
    }

    // Initialize our new file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFileStream->InitializeFromFilename(L"test2.jpg", GENERIC_WRITE);
    }

    // Create the encoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateEncoder(GUID_ContainerFormatJpeg, NULL, &piEncoder);
    }
    // Initialize the encoder
    if (SUCCEEDED(hr))
    {
        hr = piEncoder->Initialize(piFileStream,WICBitmapEncoderNoCache);
    }
```



Um fluxo de arquivos do WIC piFileStream é criado e inicializado para gravar no arquivo de imagem "test2.jpg". em seguida, piFileStream é usado para inicializar o codificador, informando ao codificador onde gravar os bits de imagem quando a codificação é concluída.

## <a name="part-3-copy-decoded-frame-information"></a>Parte 3: copiar informações de quadro decodificado

O código a seguir copia cada quadro de uma imagem para um novo quadro do codificador. Esta cópia inclui o tamanho, a resolução e o formato de pixel; todos os que são necessários para criar um quadro válido.

> [!Note]  
> Imagens JPEG só terão um quadro e o loop abaixo não é tecnicamente necessário, mas está incluído para demonstrar o uso de vários quadros para formatos que dão suporte a ele.

 


```C++
    if (SUCCEEDED(hr))
    {
        hr = piDecoder->GetFrameCount(&count);
    }

    if (SUCCEEDED(hr))
    {
        // Process each frame of the image.
        for (UINT i=0; i<count && SUCCEEDED(hr); i++)
        {
            // Frame variables.
            IWICBitmapFrameDecode *piFrameDecode = NULL;
            IWICBitmapFrameEncode *piFrameEncode = NULL;
            IWICMetadataQueryReader *piFrameQReader = NULL;
            IWICMetadataQueryWriter *piFrameQWriter = NULL;

            // Get and create the image frame.
            if (SUCCEEDED(hr))
            {
                hr = piDecoder->GetFrame(i, &piFrameDecode);
            }
            if (SUCCEEDED(hr))
            {
                hr = piEncoder->CreateNewFrame(&piFrameEncode, NULL);
            }

            // Initialize the encoder.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Initialize(NULL);
            }
            // Get and set the size.
            if (SUCCEEDED(hr))
            {
                hr = piFrameDecode->GetSize(&width, &height);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetSize(width, height);
            }
            // Get and set the resolution.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetResolution(&dpiX, &dpiY);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetResolution(dpiX, dpiY);
            }
            // Set the pixel format.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetPixelFormat(&pixelFormat);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetPixelFormat(&pixelFormat);
            }
```



O código a seguir executa uma verificação rápida para determinar se os formatos de imagem de origem e destino são os mesmos. Isso é necessário, pois a parte 4 mostra uma operação com suporte apenas quando o formato de origem e destino são os mesmos.


```C++
            // Check that the destination format and source formats are the same.
            bool formatsEqual = FALSE;
            if (SUCCEEDED(hr))
            {
                GUID srcFormat;
                GUID destFormat;

                hr = piDecoder->GetContainerFormat(&srcFormat);
                if (SUCCEEDED(hr))
                {
                    hr = piEncoder->GetContainerFormat(&destFormat);
                }
                if (SUCCEEDED(hr))
                {
                    if (srcFormat == destFormat)
                        formatsEqual = true;
                    else
                        formatsEqual = false;
                }
            }
```



## <a name="part-4-copy-the-metadata"></a>Parte 4: copiar os metadados

> [!Note]  
> O código nesta seção é válido somente quando os formatos de imagem de origem e destino são os mesmos. Você não pode copiar todos os metadados de uma imagem em uma única operação ao codificar para um formato de imagem diferente.

 

Para preservar os metadados ao codificar novamente uma imagem no mesmo formato de imagem, há métodos disponíveis para copiar todos os metadados em uma única operação. Cada uma dessas operações segue um padrão semelhante; cada um define os metadados do quadro decodificado diretamente no novo quadro que está sendo codificado. Observe que isso é feito para cada quadro de imagem individual.

O método preferencial para copiar metadados é inicializar o gravador de bloco do novo quadro com o leitor de bloco do quadro decodificado. O código a seguir demonstra esse método.


```C++
            if (SUCCEEDED(hr) && formatsEqual)
            {
                // Copy metadata using metadata block reader/writer.
                if (SUCCEEDED(hr))
                {
                    piFrameDecode->QueryInterface(IID_PPV_ARGS(&piBlockReader));
                }
                if (SUCCEEDED(hr))
                {
                    piFrameEncode->QueryInterface(IID_PPV_ARGS(&piBlockWriter));
                }
                if (SUCCEEDED(hr))
                {
                    piBlockWriter->InitializeFromBlockReader(piBlockReader);
                }
            }
```



Neste exemplo, você simplesmente obtém o leitor de bloco e o gravador de bloco do quadro de origem e do quadro de destino, respectivamente. Em seguida, o gravador de bloco é inicializado a partir do leitor de blocos. Isso inicializa o gravador de bloco com os metadados preenchidos previamente do leitor de bloco. Para aprender métodos adicionais para copiar metadados, consulte a seção gravando metadados na [visão geral da leitura e gravação de metadados de imagem](-wic-codec-readingwritingmetadata.md).

Novamente, essa operação só funcionará quando as imagens de origem e de destino tiverem o mesmo formato. Isso ocorre porque diferentes formatos de imagem armazenam os blocos de metadados em locais diferentes. Por exemplo, JPEG e TIFF (Tagged Image File Format) dão suporte a blocos de metadados XMP (Extensible Metadata Platform). Em imagens JPEG, o bloco XMP está no bloco de metadados raiz, conforme ilustrado na [visão geral dos metadados do WIC](-wic-about-metadata.md). No entanto, em uma imagem TIFF, o bloco XMP é inserido no bloco de IFD raiz.

## <a name="part-5-add-additional-metadata"></a>Parte 5: adicionar metadados adicionais

O exemplo a seguir demonstra como adicionar metadados à imagem de destino. Isso é feito chamando o método **SetMetadataByName** do gravador de consulta usando uma expressão de consulta e os dados armazenados em um [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).


```C++
            if(SUCCEEDED(hr))
            {
                hr = piFrameEncode->GetMetadataQueryWriter(&piFrameQWriter);
            }
            if (SUCCEEDED(hr))
            {
                // Add additional metadata.
                PROPVARIANT    value;
                value.vt = VT_LPWSTR;
                value.pwszVal= L"Metadata Test Image.";
                hr = piFrameQWriter->SetMetadataByName(L"/xmp/dc:title", &value);
            }
```



Para obter mais informações sobre a expressão de consulta, consulte a [visão geral da linguagem de consulta de metadados](-wic-codec-metadataquerylanguage.md).

## <a name="part-6-finalize-the-encoded-image"></a>Parte 6: finalizar a imagem codificada

As etapas finais para copiar a imagem são gravar os dados de pixel para o quadro, confirmar o quadro no codificador e confirmar o codificador. A confirmação do codificador grava o fluxo de imagem no arquivo.


```C++
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->WriteSource(
                    static_cast<IWICBitmapSource*> (piFrameDecode),
                    NULL); // Using NULL enables JPEG loss-less encoding.
            }

            // Commit the frame.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Commit();
            }

            if (piFrameDecode)
            {
                piFrameDecode->Release();
            }

            if (piFrameEncode)
            {
                piFrameEncode->Release();
            }

            if (piFrameQReader)
            {
                piFrameQReader->Release();
            }

            if (piFrameQWriter)
            {
                piFrameQWriter->Release();
            }
        }
    }

    if (SUCCEEDED(hr))
    {
        piEncoder->Commit();
    }

    if (SUCCEEDED(hr))
    {
        piFileStream->Commit(STGC_DEFAULT);
    }

    if (piFileStream)
    {
        piFileStream->Release();
    }
    if (piEncoder)
    {
        piEncoder->Release();
    }
    if (piBlockWriter)
    {
        piBlockWriter->Release();
    }
    if (piBlockReader)
    {
        piBlockReader->Release();
    }
```



O método **WriteState** do quadro é usado para gravar os dados de pixel da imagem. Observe que isso é feito depois que os metadados são gravados. Isso é necessário para garantir que os metadados tenham espaço suficiente no arquivo de imagem. Depois que os dados de pixel são gravados, o quadro é gravado no fluxo usando o método **Commit** do quadro. Depois que todos os quadros tiverem sido processados, o codificador (e, portanto, a imagem) será finalizado usando o método **Commit** do codificador.

Depois de confirmar o quadro, você deve liberar os objetos COM criados no loop.

## <a name="jpeg-re-encode-example-code"></a>Código de exemplo de recodificação JPEG

Veja a seguir o código das partes 1 a 6 em um bloco convienient.


```C++
#include <Windows.h>
#include <Wincodecsdk.h>

int main()
{
    // Initialize COM.
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    IWICImagingFactory *piFactory = NULL;
    IWICBitmapDecoder *piDecoder = NULL;

    // Create the COM imaging factory.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_WICImagingFactory,
        NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&piFactory));
    }

    // Create the decoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateDecoderFromFilename(L"test.jpg", NULL, GENERIC_READ,
            WICDecodeMetadataCacheOnDemand, //For JPEG lossless decoding/encoding.
            &piDecoder);
    }

    // Variables used for encoding.
    IWICStream *piFileStream = NULL;
    IWICBitmapEncoder *piEncoder = NULL;
    IWICMetadataBlockWriter *piBlockWriter = NULL;
    IWICMetadataBlockReader *piBlockReader = NULL;

    WICPixelFormatGUID pixelFormat = { 0 };
    UINT count = 0;
    double dpiX, dpiY = 0.0;
    UINT width, height = 0;

    // Create a file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateStream(&piFileStream);
    }

    // Initialize our new file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFileStream->InitializeFromFilename(L"test2.jpg", GENERIC_WRITE);
    }

    // Create the encoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateEncoder(GUID_ContainerFormatJpeg, NULL, &piEncoder);
    }
    // Initialize the encoder
    if (SUCCEEDED(hr))
    {
        hr = piEncoder->Initialize(piFileStream,WICBitmapEncoderNoCache);
    }

    if (SUCCEEDED(hr))
    {
        hr = piDecoder->GetFrameCount(&count);
    }

    if (SUCCEEDED(hr))
    {
        // Process each frame of the image.
        for (UINT i=0; i<count && SUCCEEDED(hr); i++)
        {
            // Frame variables.
            IWICBitmapFrameDecode *piFrameDecode = NULL;
            IWICBitmapFrameEncode *piFrameEncode = NULL;
            IWICMetadataQueryReader *piFrameQReader = NULL;
            IWICMetadataQueryWriter *piFrameQWriter = NULL;

            // Get and create the image frame.
            if (SUCCEEDED(hr))
            {
                hr = piDecoder->GetFrame(i, &piFrameDecode);
            }
            if (SUCCEEDED(hr))
            {
                hr = piEncoder->CreateNewFrame(&piFrameEncode, NULL);
            }

            // Initialize the encoder.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Initialize(NULL);
            }
            // Get and set the size.
            if (SUCCEEDED(hr))
            {
                hr = piFrameDecode->GetSize(&width, &height);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetSize(width, height);
            }
            // Get and set the resolution.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetResolution(&dpiX, &dpiY);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetResolution(dpiX, dpiY);
            }
            // Set the pixel format.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetPixelFormat(&pixelFormat);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetPixelFormat(&pixelFormat);
            }

            // Check that the destination format and source formats are the same.
            bool formatsEqual = FALSE;
            if (SUCCEEDED(hr))
            {
                GUID srcFormat;
                GUID destFormat;

                hr = piDecoder->GetContainerFormat(&srcFormat);
                if (SUCCEEDED(hr))
                {
                    hr = piEncoder->GetContainerFormat(&destFormat);
                }
                if (SUCCEEDED(hr))
                {
                    if (srcFormat == destFormat)
                        formatsEqual = true;
                    else
                        formatsEqual = false;
                }
            }

            if (SUCCEEDED(hr) && formatsEqual)
            {
                // Copy metadata using metadata block reader/writer.
                if (SUCCEEDED(hr))
                {
                    piFrameDecode->QueryInterface(IID_PPV_ARGS(&piBlockReader));
                }
                if (SUCCEEDED(hr))
                {
                    piFrameEncode->QueryInterface(IID_PPV_ARGS(&piBlockWriter));
                }
                if (SUCCEEDED(hr))
                {
                    piBlockWriter->InitializeFromBlockReader(piBlockReader);
                }
            }

            if(SUCCEEDED(hr))
            {
                hr = piFrameEncode->GetMetadataQueryWriter(&piFrameQWriter);
            }
            if (SUCCEEDED(hr))
            {
                // Add additional metadata.
                PROPVARIANT    value;
                value.vt = VT_LPWSTR;
                value.pwszVal= L"Metadata Test Image.";
                hr = piFrameQWriter->SetMetadataByName(L"/xmp/dc:title", &value);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->WriteSource(
                    static_cast<IWICBitmapSource*> (piFrameDecode),
                    NULL); // Using NULL enables JPEG loss-less encoding.
            }

            // Commit the frame.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Commit();
            }

            if (piFrameDecode)
            {
                piFrameDecode->Release();
            }

            if (piFrameEncode)
            {
                piFrameEncode->Release();
            }

            if (piFrameQReader)
            {
                piFrameQReader->Release();
            }

            if (piFrameQWriter)
            {
                piFrameQWriter->Release();
            }
        }
    }

    if (SUCCEEDED(hr))
    {
        piEncoder->Commit();
    }

    if (SUCCEEDED(hr))
    {
        piFileStream->Commit(STGC_DEFAULT);
    }

    if (piFileStream)
    {
        piFileStream->Release();
    }
    if (piEncoder)
    {
        piEncoder->Release();
    }
    if (piBlockWriter)
    {
        piBlockWriter->Release();
    }
    if (piBlockReader)
    {
        piBlockReader->Release();
    }
    return 0;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão geral dos metadados do WIC](-wic-about-metadata.md)
</dt> <dt>

[Visão geral da linguagem de consulta de metadados](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[Visão geral da leitura e gravação de metadados de imagem](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Visão geral da extensibilidade de metadados](-wic-codec-metadatahandlers.md)
</dt> </dl>

 

 

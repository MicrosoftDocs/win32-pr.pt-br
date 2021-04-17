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
# <a name="how-to-re-encode-a-jpeg-image-with-metadata"></a><span data-ttu-id="e77fe-103">Como codificar novamente uma imagem JPEG com metadados</span><span class="sxs-lookup"><span data-stu-id="e77fe-103">How-to re-encode a JPEG image with metadata</span></span>

<span data-ttu-id="e77fe-104">O exemplo a seguir demonstra como codificar novamente uma imagem e seus metadados para um novo arquivo do mesmo formato.</span><span class="sxs-lookup"><span data-stu-id="e77fe-104">The following example demonstrates how to re-encode an image and its metadata to a new file of the same format.</span></span> <span data-ttu-id="e77fe-105">Além disso, este exemplo adiciona metadados para demonstrar uma expressão de item único usada por um gravador de consulta.</span><span class="sxs-lookup"><span data-stu-id="e77fe-105">In addition, this example adds metadata to demonstrate a single-item expression used by a query writer.</span></span>

<span data-ttu-id="e77fe-106">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="e77fe-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="e77fe-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="e77fe-107">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="e77fe-108">Parte 1: decodificar uma imagem</span><span class="sxs-lookup"><span data-stu-id="e77fe-108">Part 1: Decode an Image</span></span>](#part-1-decode-an-image)
-   [<span data-ttu-id="e77fe-109">Parte 2: criar e inicializar o codificador de imagem</span><span class="sxs-lookup"><span data-stu-id="e77fe-109">Part 2: Create and Initialize the Image Encoder</span></span>](#part-2-create-and-initialize-the-image-encoder)
-   [<span data-ttu-id="e77fe-110">Parte 3: copiar informações de quadro decodificado</span><span class="sxs-lookup"><span data-stu-id="e77fe-110">Part 3: Copy Decoded Frame Information</span></span>](#part-3-copy-decoded-frame-information)
-   [<span data-ttu-id="e77fe-111">Parte 4: copiar os metadados</span><span class="sxs-lookup"><span data-stu-id="e77fe-111">Part 4: Copy the Metadata</span></span>](#part-4-copy-the-metadata)
-   [<span data-ttu-id="e77fe-112">Parte 5: adicionar metadados adicionais</span><span class="sxs-lookup"><span data-stu-id="e77fe-112">Part 5: Add Additional Metadata</span></span>](#part-5-add-additional-metadata)
-   [<span data-ttu-id="e77fe-113">Parte 6: finalizar a imagem codificada</span><span class="sxs-lookup"><span data-stu-id="e77fe-113">Part 6: Finalize the Encoded Image</span></span>](#part-6-finalize-the-encoded-image)
-   [<span data-ttu-id="e77fe-114">Código de exemplo de recodificação JPEG</span><span class="sxs-lookup"><span data-stu-id="e77fe-114">JPEG Re-encode Example Code</span></span>](#jpeg-re-encode-example-code)
-   [<span data-ttu-id="e77fe-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e77fe-115">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="e77fe-116">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="e77fe-116">Prerequisites</span></span>

<span data-ttu-id="e77fe-117">Para entender este tópico, você deve estar familiarizado com o sistema de metadados do Windows Imaging Component (WIC), conforme descrito na [visão geral dos metadados do WIC](-wic-about-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="e77fe-117">To understand this topic, you should be familiar with the Windows Imaging Component (WIC) metadata system as described in the [WIC Metadata Overview](-wic-about-metadata.md).</span></span> <span data-ttu-id="e77fe-118">Você também deve estar familiarizado com os componentes do codec do WIC, conforme descrito na [visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md).</span><span class="sxs-lookup"><span data-stu-id="e77fe-118">You should also be familiar with the WIC codec components as described in the [Windows Imaging Component Overview](-wic-about-windows-imaging-codec.md).</span></span>

## <a name="part-1-decode-an-image"></a><span data-ttu-id="e77fe-119">Parte 1: decodificar uma imagem</span><span class="sxs-lookup"><span data-stu-id="e77fe-119">Part 1: Decode an Image</span></span>

<span data-ttu-id="e77fe-120">Antes de copiar dados de imagem ou metadados para um novo arquivo de imagem, você deve primeiro criar um decodificador para a imagem existente que deseja codificar novamente.</span><span class="sxs-lookup"><span data-stu-id="e77fe-120">Before you can copy image data or metadata to a new image file, you must first create a decoder for the existing image that you want to re-encode.</span></span> <span data-ttu-id="e77fe-121">O código a seguir demonstra como criar um decodificador WIC para o arquivo de imagem test.jpg.</span><span class="sxs-lookup"><span data-stu-id="e77fe-121">The following code demonstrates how to create a WIC decoder for the image file test.jpg.</span></span>


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



<span data-ttu-id="e77fe-122">A chamada para **CreateDecoderFromFilename** usou o valor WICDecodeMetadataCacheOnDemand da enumeração [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) como o quarto parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e77fe-122">The call to **CreateDecoderFromFilename** used the value WICDecodeMetadataCacheOnDemand from the [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) enumeration as the fourth parameter.</span></span> <span data-ttu-id="e77fe-123">Isso informa ao decodificador para armazenar em cache os metadados quando os metadados são necessários, obtendo um leitor de consulta ou usando o leitor de metadados subjacente.</span><span class="sxs-lookup"><span data-stu-id="e77fe-123">This tells the decoder to cache the metadata when the metadata is needed, either by obtaining a query reader or by using the underlying metadata reader.</span></span> <span data-ttu-id="e77fe-124">O uso dessa opção permite que você retenha o fluxo para os metadados, o que é necessário para executar a codificação de metadados rápida e permite a decodificação e a codificação de imagens JPEG sem perdas.</span><span class="sxs-lookup"><span data-stu-id="e77fe-124">Using this option enables you to retain the stream to the metadata, which is required for performing fast metadata encoding and enables lossless decoding and encoding of JPEG images.</span></span> <span data-ttu-id="e77fe-125">Como alternativa, você pode usar o outro valor **WICDecodeOptions** , WICDecodeMetadataCacheOnLoad, que armazena em cache os metadados da imagem inserida assim que a imagem é carregada.</span><span class="sxs-lookup"><span data-stu-id="e77fe-125">Alternatively, you could use the other **WICDecodeOptions** value, WICDecodeMetadataCacheOnLoad, which caches the embedded image metadata as soon as the image is loaded.</span></span>

## <a name="part-2-create-and-initialize-the-image-encoder"></a><span data-ttu-id="e77fe-126">Parte 2: criar e inicializar o codificador de imagem</span><span class="sxs-lookup"><span data-stu-id="e77fe-126">Part 2: Create and Initialize the Image Encoder</span></span>

<span data-ttu-id="e77fe-127">O código a seguir demonstra a criação do codificador que você usará para codificar a imagem decodificada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="e77fe-127">The following code demonstrates the creation of the encoder you will use to encode the image you previously decoded.</span></span>


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



<span data-ttu-id="e77fe-128">Um fluxo de arquivos do WIC piFileStream é criado e inicializado para gravar no arquivo de imagem "test2.jpg".</span><span class="sxs-lookup"><span data-stu-id="e77fe-128">A WIC file stream piFileStream is created and initialized for writing to the image file "test2.jpg".</span></span> <span data-ttu-id="e77fe-129">em seguida, piFileStream é usado para inicializar o codificador, informando ao codificador onde gravar os bits de imagem quando a codificação é concluída.</span><span class="sxs-lookup"><span data-stu-id="e77fe-129">piFileStream is then used to initialize the encoder, informing the encoder where to write the image bits when the encoding is complete.</span></span>

## <a name="part-3-copy-decoded-frame-information"></a><span data-ttu-id="e77fe-130">Parte 3: copiar informações de quadro decodificado</span><span class="sxs-lookup"><span data-stu-id="e77fe-130">Part 3: Copy Decoded Frame Information</span></span>

<span data-ttu-id="e77fe-131">O código a seguir copia cada quadro de uma imagem para um novo quadro do codificador.</span><span class="sxs-lookup"><span data-stu-id="e77fe-131">The following code copies each frame of an image to a new frame of the encoder.</span></span> <span data-ttu-id="e77fe-132">Esta cópia inclui o tamanho, a resolução e o formato de pixel; todos os que são necessários para criar um quadro válido.</span><span class="sxs-lookup"><span data-stu-id="e77fe-132">This copy includes size, resolution, and pixel format; all of which are necessary to create a valid frame.</span></span>

> [!Note]  
> <span data-ttu-id="e77fe-133">Imagens JPEG só terão um quadro e o loop abaixo não é tecnicamente necessário, mas está incluído para demonstrar o uso de vários quadros para formatos que dão suporte a ele.</span><span class="sxs-lookup"><span data-stu-id="e77fe-133">JPEG images will only have one frame and the loop below is not technically necessary but is included to demonstrate multi-frame usage for formats that support it.</span></span>

 


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



<span data-ttu-id="e77fe-134">O código a seguir executa uma verificação rápida para determinar se os formatos de imagem de origem e destino são os mesmos.</span><span class="sxs-lookup"><span data-stu-id="e77fe-134">The following code performs a quick check to determine whether the source and destination image formats are the same.</span></span> <span data-ttu-id="e77fe-135">Isso é necessário, pois a parte 4 mostra uma operação com suporte apenas quando o formato de origem e destino são os mesmos.</span><span class="sxs-lookup"><span data-stu-id="e77fe-135">This is needed as Part 4 shows an operation that is only supported when the source and destination format are the same.</span></span>


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



## <a name="part-4-copy-the-metadata"></a><span data-ttu-id="e77fe-136">Parte 4: copiar os metadados</span><span class="sxs-lookup"><span data-stu-id="e77fe-136">Part 4: Copy the Metadata</span></span>

> [!Note]  
> <span data-ttu-id="e77fe-137">O código nesta seção é válido somente quando os formatos de imagem de origem e destino são os mesmos.</span><span class="sxs-lookup"><span data-stu-id="e77fe-137">The code in this section is valid only when the source and destination image formats are the same.</span></span> <span data-ttu-id="e77fe-138">Você não pode copiar todos os metadados de uma imagem em uma única operação ao codificar para um formato de imagem diferente.</span><span class="sxs-lookup"><span data-stu-id="e77fe-138">You cannot copy all of an image's metadata in a single operation when encoding to a different image format.</span></span>

 

<span data-ttu-id="e77fe-139">Para preservar os metadados ao codificar novamente uma imagem no mesmo formato de imagem, há métodos disponíveis para copiar todos os metadados em uma única operação.</span><span class="sxs-lookup"><span data-stu-id="e77fe-139">To preserve metadata while re-encoding an image to the same image format, there are methods available for copying all the metadata in a single operation.</span></span> <span data-ttu-id="e77fe-140">Cada uma dessas operações segue um padrão semelhante; cada um define os metadados do quadro decodificado diretamente no novo quadro que está sendo codificado.</span><span class="sxs-lookup"><span data-stu-id="e77fe-140">Each of these operations follows a similar pattern; each sets the decoded frame's metadata directly into the new frame being encoded.</span></span> <span data-ttu-id="e77fe-141">Observe que isso é feito para cada quadro de imagem individual.</span><span class="sxs-lookup"><span data-stu-id="e77fe-141">Note that this is done for each individual image frame.</span></span>

<span data-ttu-id="e77fe-142">O método preferencial para copiar metadados é inicializar o gravador de bloco do novo quadro com o leitor de bloco do quadro decodificado.</span><span class="sxs-lookup"><span data-stu-id="e77fe-142">The preferred method for copying metadata is to initialize the new frame's block writer with the decoded frame's block reader.</span></span> <span data-ttu-id="e77fe-143">O código a seguir demonstra esse método.</span><span class="sxs-lookup"><span data-stu-id="e77fe-143">The following code demonstrates this method.</span></span>


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



<span data-ttu-id="e77fe-144">Neste exemplo, você simplesmente obtém o leitor de bloco e o gravador de bloco do quadro de origem e do quadro de destino, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="e77fe-144">In this example, you simply obtain the block reader and block writer from the source frame and destination frame, respectively.</span></span> <span data-ttu-id="e77fe-145">Em seguida, o gravador de bloco é inicializado a partir do leitor de blocos.</span><span class="sxs-lookup"><span data-stu-id="e77fe-145">The block writer is then initialized from the block reader.</span></span> <span data-ttu-id="e77fe-146">Isso inicializa o gravador de bloco com os metadados preenchidos previamente do leitor de bloco.</span><span class="sxs-lookup"><span data-stu-id="e77fe-146">This initializes the block writer with the pre-populated metadata of the block reader.</span></span> <span data-ttu-id="e77fe-147">Para aprender métodos adicionais para copiar metadados, consulte a seção gravando metadados na [visão geral da leitura e gravação de metadados de imagem](-wic-codec-readingwritingmetadata.md).</span><span class="sxs-lookup"><span data-stu-id="e77fe-147">To learn additional methods for copying metadata, see the Writing Metadata section in the [Overview of Reading and Writing Image Metadata](-wic-codec-readingwritingmetadata.md).</span></span>

<span data-ttu-id="e77fe-148">Novamente, essa operação só funcionará quando as imagens de origem e de destino tiverem o mesmo formato.</span><span class="sxs-lookup"><span data-stu-id="e77fe-148">Again, this operation works only when the source and destination images have the same format.</span></span> <span data-ttu-id="e77fe-149">Isso ocorre porque diferentes formatos de imagem armazenam os blocos de metadados em locais diferentes.</span><span class="sxs-lookup"><span data-stu-id="e77fe-149">This is because different image formats store the metadata blocks in different locations.</span></span> <span data-ttu-id="e77fe-150">Por exemplo, JPEG e TIFF (Tagged Image File Format) dão suporte a blocos de metadados XMP (Extensible Metadata Platform).</span><span class="sxs-lookup"><span data-stu-id="e77fe-150">For instance, both JPEG and Tagged Image File Format (TIFF) support Extensible Metadata Platform (XMP) metadata blocks.</span></span> <span data-ttu-id="e77fe-151">Em imagens JPEG, o bloco XMP está no bloco de metadados raiz, conforme ilustrado na [visão geral dos metadados do WIC](-wic-about-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="e77fe-151">In JPEG images, the XMP block is at the root metadata block as illustrated in the [WIC Metadata Overview](-wic-about-metadata.md).</span></span> <span data-ttu-id="e77fe-152">No entanto, em uma imagem TIFF, o bloco XMP é inserido no bloco de IFD raiz.</span><span class="sxs-lookup"><span data-stu-id="e77fe-152">However, in a TIFF image, the XMP block is embedded in the root IFD block.</span></span>

## <a name="part-5-add-additional-metadata"></a><span data-ttu-id="e77fe-153">Parte 5: adicionar metadados adicionais</span><span class="sxs-lookup"><span data-stu-id="e77fe-153">Part 5: Add Additional Metadata</span></span>

<span data-ttu-id="e77fe-154">O exemplo a seguir demonstra como adicionar metadados à imagem de destino.</span><span class="sxs-lookup"><span data-stu-id="e77fe-154">The following example demonstrates how to add metadata to the destination image.</span></span> <span data-ttu-id="e77fe-155">Isso é feito chamando o método **SetMetadataByName** do gravador de consulta usando uma expressão de consulta e os dados armazenados em um [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span><span class="sxs-lookup"><span data-stu-id="e77fe-155">This is done by calling the query writer's **SetMetadataByName** method using a query expression and the data stored in a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span></span>


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



<span data-ttu-id="e77fe-156">Para obter mais informações sobre a expressão de consulta, consulte a [visão geral da linguagem de consulta de metadados](-wic-codec-metadataquerylanguage.md).</span><span class="sxs-lookup"><span data-stu-id="e77fe-156">For more information on the query expression, see the [Metadata Query Language Overview](-wic-codec-metadataquerylanguage.md).</span></span>

## <a name="part-6-finalize-the-encoded-image"></a><span data-ttu-id="e77fe-157">Parte 6: finalizar a imagem codificada</span><span class="sxs-lookup"><span data-stu-id="e77fe-157">Part 6: Finalize the Encoded Image</span></span>

<span data-ttu-id="e77fe-158">As etapas finais para copiar a imagem são gravar os dados de pixel para o quadro, confirmar o quadro no codificador e confirmar o codificador.</span><span class="sxs-lookup"><span data-stu-id="e77fe-158">The final steps for copying the image are to write the pixel data for the frame, commit the frame to the encoder, and commit the encoder.</span></span> <span data-ttu-id="e77fe-159">A confirmação do codificador grava o fluxo de imagem no arquivo.</span><span class="sxs-lookup"><span data-stu-id="e77fe-159">Committing the encoder writes the image stream to the file.</span></span>


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



<span data-ttu-id="e77fe-160">O método **WriteState** do quadro é usado para gravar os dados de pixel da imagem.</span><span class="sxs-lookup"><span data-stu-id="e77fe-160">The frame's **WriteSource** method is used to write the pixel data for the image.</span></span> <span data-ttu-id="e77fe-161">Observe que isso é feito depois que os metadados são gravados.</span><span class="sxs-lookup"><span data-stu-id="e77fe-161">Note that this is done after the metadata has been written.</span></span> <span data-ttu-id="e77fe-162">Isso é necessário para garantir que os metadados tenham espaço suficiente no arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="e77fe-162">This is necessary to ensure that the metadata has enough space within the image file.</span></span> <span data-ttu-id="e77fe-163">Depois que os dados de pixel são gravados, o quadro é gravado no fluxo usando o método **Commit** do quadro.</span><span class="sxs-lookup"><span data-stu-id="e77fe-163">After the pixel data is written, the frame is written to the stream using the frame's **Commit** method.</span></span> <span data-ttu-id="e77fe-164">Depois que todos os quadros tiverem sido processados, o codificador (e, portanto, a imagem) será finalizado usando o método **Commit** do codificador.</span><span class="sxs-lookup"><span data-stu-id="e77fe-164">After all frames have been processed, the encoder (and thus the image) is finalized using the encoder's **Commit** method.</span></span>

<span data-ttu-id="e77fe-165">Depois de confirmar o quadro, você deve liberar os objetos COM criados no loop.</span><span class="sxs-lookup"><span data-stu-id="e77fe-165">Once you commit the frame, you must release the COM objects created in the loop.</span></span>

## <a name="jpeg-re-encode-example-code"></a><span data-ttu-id="e77fe-166">Código de exemplo de recodificação JPEG</span><span class="sxs-lookup"><span data-stu-id="e77fe-166">JPEG Re-encode Example Code</span></span>

<span data-ttu-id="e77fe-167">Veja a seguir o código das partes 1 a 6 em um bloco convienient.</span><span class="sxs-lookup"><span data-stu-id="e77fe-167">The following is the code from Parts 1 through 6 in one convienient block.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e77fe-168">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e77fe-168">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e77fe-169">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="e77fe-169">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e77fe-170">Visão geral dos metadados do WIC</span><span class="sxs-lookup"><span data-stu-id="e77fe-170">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

[<span data-ttu-id="e77fe-171">Visão geral da linguagem de consulta de metadados</span><span class="sxs-lookup"><span data-stu-id="e77fe-171">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[<span data-ttu-id="e77fe-172">Visão geral da leitura e gravação de metadados de imagem</span><span class="sxs-lookup"><span data-stu-id="e77fe-172">Overview of Reading and Writing Image Metadata</span></span>](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[<span data-ttu-id="e77fe-173">Visão geral da extensibilidade de metadados</span><span class="sxs-lookup"><span data-stu-id="e77fe-173">Metadata Extensibility Overview</span></span>](-wic-codec-metadatahandlers.md)
</dt> </dl>

 

 

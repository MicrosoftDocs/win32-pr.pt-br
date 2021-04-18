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
# <a name="how-to-create-a-decoder-using-a-stream"></a><span data-ttu-id="4ea5c-103">Como criar um decodificador usando um fluxo</span><span class="sxs-lookup"><span data-stu-id="4ea5c-103">How to Create a Decoder Using a Stream</span></span>

<span data-ttu-id="4ea5c-104">Este tópico descreve como criar um decodificador de bitmap usando um fluxo.</span><span class="sxs-lookup"><span data-stu-id="4ea5c-104">This topic describes how to create a bitmap decoder by using a stream.</span></span>

<span data-ttu-id="4ea5c-105">Para criar um decodificador de bitmap usando um fluxo</span><span class="sxs-lookup"><span data-stu-id="4ea5c-105">To create a bitmap decoder by using a stream</span></span>

1.  <span data-ttu-id="4ea5c-106">Carregar um arquivo de imagem em um fluxo.</span><span class="sxs-lookup"><span data-stu-id="4ea5c-106">Load an image file into a stream.</span></span> <span data-ttu-id="4ea5c-107">Neste exemplo, um fluxo é criado para um recurso de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4ea5c-107">In this example, a stream is created for an application resource.</span></span>

    <span data-ttu-id="4ea5c-108">No arquivo de definição de recurso de aplicativo (. rc), defina o recurso.</span><span class="sxs-lookup"><span data-stu-id="4ea5c-108">In the application resource definition (.rc) file, define the resource.</span></span> <span data-ttu-id="4ea5c-109">O exemplo a seguir define um `Image` recurso chamado `IDR_SAMPLE_IMAGE` .</span><span class="sxs-lookup"><span data-stu-id="4ea5c-109">The following example defines an `Image` resource named `IDR_SAMPLE_IMAGE`.</span></span>

    ```C++
    IDR_SAMPLE_IMAGE IMAGE "turtle.jpg"
    ```

    

    <span data-ttu-id="4ea5c-110">O recurso será adicionado aos recursos do aplicativo quando o aplicativo for compilado.</span><span class="sxs-lookup"><span data-stu-id="4ea5c-110">The resource will be added to the application's resources when the application is built.</span></span>

2.  <span data-ttu-id="4ea5c-111">Carregue o recurso do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4ea5c-111">Load the resource from the application.</span></span>

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

    

3.  <span data-ttu-id="4ea5c-112">Bloqueie o recurso e obtenha o tamanho.</span><span class="sxs-lookup"><span data-stu-id="4ea5c-112">Lock the resource and get the size.</span></span>

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

    

4.  <span data-ttu-id="4ea5c-113">Crie um [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) para criar objetos do Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="4ea5c-113">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

5.  <span data-ttu-id="4ea5c-114">Use o método [**CreateStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) para criar um objeto [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) e inicializá-lo usando o ponteiro de memória da imagem.</span><span class="sxs-lookup"><span data-stu-id="4ea5c-114">Use the [**CreateStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) method to create an [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) object and initialize it by using the image memory pointer.</span></span>

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

    

6.  <span data-ttu-id="4ea5c-115">Crie um [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) a partir do novo objeto de fluxo usando o método [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) .</span><span class="sxs-lookup"><span data-stu-id="4ea5c-115">Create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from the new stream object using the [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) method.</span></span>

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

    

7.  <span data-ttu-id="4ea5c-116">Obtenha o primeiro [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) da imagem.</span><span class="sxs-lookup"><span data-stu-id="4ea5c-116">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="4ea5c-117">O formato de arquivo JPEG só dá suporte a um único quadro.</span><span class="sxs-lookup"><span data-stu-id="4ea5c-117">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="4ea5c-118">Como o arquivo neste exemplo é um arquivo JPEG, o primeiro quadro ( `0` ) é usado.</span><span class="sxs-lookup"><span data-stu-id="4ea5c-118">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="4ea5c-119">Para formatos de imagem que têm vários quadros, consulte [como recuperar os quadros de uma imagem](-wic-bitmapsources-howto-retrieveimageframes.md) para acessar cada quadro da imagem.</span><span class="sxs-lookup"><span data-stu-id="4ea5c-119">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

8.  <span data-ttu-id="4ea5c-120">Processar o quadro da imagem.</span><span class="sxs-lookup"><span data-stu-id="4ea5c-120">Process the image frame.</span></span> <span data-ttu-id="4ea5c-121">Para obter informações adicionais sobre objetos [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) , consulte a [visão geral de fontes de bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="4ea5c-121">For additional information about [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) objects, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="4ea5c-122">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="4ea5c-122">See Also</span></span>

[<span data-ttu-id="4ea5c-123">Guia de programação</span><span class="sxs-lookup"><span data-stu-id="4ea5c-123">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="4ea5c-124">Referência</span><span class="sxs-lookup"><span data-stu-id="4ea5c-124">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="4ea5c-125">Amostras</span><span class="sxs-lookup"><span data-stu-id="4ea5c-125">Samples</span></span>](-wic-samples.md)


 

 




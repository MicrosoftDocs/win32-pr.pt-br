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
# <a name="how-to-create-a-decoder-using-an-image-filename"></a><span data-ttu-id="e6316-103">Como criar um decodificador usando um nome de arquivo de imagem</span><span class="sxs-lookup"><span data-stu-id="e6316-103">How to Create a Decoder Using an Image Filename</span></span>

<span data-ttu-id="e6316-104">Este tópico descreve como criar um decodificador de bitmap usando um nome de arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="e6316-104">This topic describes how to create a bitmap decoder by using an image filename.</span></span>

<span data-ttu-id="e6316-105">Para criar um decodificador de bitmap usando um nome de arquivo de imagem</span><span class="sxs-lookup"><span data-stu-id="e6316-105">To create a bitmap decoder by using an image filename</span></span>

1.  <span data-ttu-id="e6316-106">Crie um objeto [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) para criar objetos do Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="e6316-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="e6316-107">Use o método [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) para criar um [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) a partir de um arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="e6316-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

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

    

3.  <span data-ttu-id="e6316-108">Obtenha o primeiro [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) da imagem.</span><span class="sxs-lookup"><span data-stu-id="e6316-108">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="e6316-109">O formato de arquivo JPEG só dá suporte a um único quadro.</span><span class="sxs-lookup"><span data-stu-id="e6316-109">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="e6316-110">Como o arquivo neste exemplo é um arquivo JPEG, o primeiro quadro ( `0` ) é usado.</span><span class="sxs-lookup"><span data-stu-id="e6316-110">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="e6316-111">Para formatos de imagem que têm vários quadros, consulte [como recuperar os quadros de uma imagem](-wic-bitmapsources-howto-retrieveimageframes.md) para acessar cada quadro da imagem.</span><span class="sxs-lookup"><span data-stu-id="e6316-111">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

4.  <span data-ttu-id="e6316-112">Processar o quadro da imagem.</span><span class="sxs-lookup"><span data-stu-id="e6316-112">Process the image frame.</span></span> <span data-ttu-id="e6316-113">Para obter informações adicionais sobre objetos [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) , consulte a [visão geral de fontes de bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="e6316-113">For additional information about [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) objects, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e6316-114">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="e6316-114">See Also</span></span>

[<span data-ttu-id="e6316-115">Guia de programação</span><span class="sxs-lookup"><span data-stu-id="e6316-115">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="e6316-116">Referência</span><span class="sxs-lookup"><span data-stu-id="e6316-116">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="e6316-117">Amostras</span><span class="sxs-lookup"><span data-stu-id="e6316-117">Samples</span></span>](-wic-samples.md)


 

 




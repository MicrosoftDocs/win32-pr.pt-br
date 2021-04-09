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
# <a name="how-to-flip-and-rotate-a-bitmap-source"></a><span data-ttu-id="6f22f-103">Como inverter e girar uma fonte de bitmap</span><span class="sxs-lookup"><span data-stu-id="6f22f-103">How to Flip and Rotate a Bitmap Source</span></span>

<span data-ttu-id="6f22f-104">Este tópico demonstra como girar um [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) usando um componente [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) .</span><span class="sxs-lookup"><span data-stu-id="6f22f-104">This topic demonstrates how to rotate an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) by using an [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) component.</span></span>

<span data-ttu-id="6f22f-105">Para inverter e girar uma origem de bitmap</span><span class="sxs-lookup"><span data-stu-id="6f22f-105">To flip and rotate a bitmap source</span></span>

1.  <span data-ttu-id="6f22f-106">Crie um objeto [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) para criar objetos do Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="6f22f-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="6f22f-107">Use o método [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) para criar um [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) a partir de um arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="6f22f-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

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

    

3.  <span data-ttu-id="6f22f-108">Obtenha o primeiro [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) da imagem.</span><span class="sxs-lookup"><span data-stu-id="6f22f-108">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="6f22f-109">O formato de arquivo JPEG só dá suporte a um único quadro.</span><span class="sxs-lookup"><span data-stu-id="6f22f-109">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="6f22f-110">Como o arquivo neste exemplo é um arquivo JPEG, o primeiro quadro ( `0` ) é usado.</span><span class="sxs-lookup"><span data-stu-id="6f22f-110">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="6f22f-111">Para formatos de imagem que têm vários quadros, consulte [como recuperar os quadros de uma imagem](-wic-bitmapsources-howto-retrieveimageframes.md) para acessar cada quadro da imagem.</span><span class="sxs-lookup"><span data-stu-id="6f22f-111">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

4.  <span data-ttu-id="6f22f-112">Crie o [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) a ser usado para inverter a imagem.</span><span class="sxs-lookup"><span data-stu-id="6f22f-112">Create the [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) to use for flipping the image.</span></span>

    ```C++
    // Create the flip/rotator.
    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapFlipRotator(&pIFlipRotator);
    }
    ```

    

5.  <span data-ttu-id="6f22f-113">Inicialize o objeto flip/roto com os dados da imagem do quadro de bitmap virado horizontalmente (ao longo do eixo y vertical).</span><span class="sxs-lookup"><span data-stu-id="6f22f-113">Initialize the flip/rotator object with the image data of the bitmap frame flipped horizontally (along the vertical y-axis).</span></span>

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

    

    <span data-ttu-id="6f22f-114">Consulte [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) para ver rotações adicionais e opções de inversão.</span><span class="sxs-lookup"><span data-stu-id="6f22f-114">See [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) for additional rotations and flipping options.</span></span>

6.  <span data-ttu-id="6f22f-115">Desenhe ou processe a origem do bitmap invertido.</span><span class="sxs-lookup"><span data-stu-id="6f22f-115">Draw or process the flipped bitmap source.</span></span>

    > [!Note]  
    > <span data-ttu-id="6f22f-116">A interface [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) herda da interface [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) , de modo que você pode usar o objeto de flip/roto inicializado em qualquer lugar que aceite um **IWICBitmapSource**.</span><span class="sxs-lookup"><span data-stu-id="6f22f-116">The [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) interface inherits from the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) interface, so you can use the initialized flip/rotator object anywhere that accepts a **IWICBitmapSource**.</span></span>

     

    <span data-ttu-id="6f22f-117">A ilustração a seguir demonstra como inverter uma imagem horizontalmente (ao longo do eixo x vertical).</span><span class="sxs-lookup"><span data-stu-id="6f22f-117">The following illustration demonstrates flipping an imaging horizontally (along the vertical x-axis).</span></span>

    ![ilustração mostrando um flip horizontal (ao longo do eixo x do Verital) de uma imagem](graphics/fliphorizontal.png)

## <a name="see-also"></a><span data-ttu-id="6f22f-119">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="6f22f-119">See Also</span></span>

[<span data-ttu-id="6f22f-120">Guia de programação</span><span class="sxs-lookup"><span data-stu-id="6f22f-120">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="6f22f-121">Referência</span><span class="sxs-lookup"><span data-stu-id="6f22f-121">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="6f22f-122">Amostras</span><span class="sxs-lookup"><span data-stu-id="6f22f-122">Samples</span></span>](-wic-samples.md)


 

 




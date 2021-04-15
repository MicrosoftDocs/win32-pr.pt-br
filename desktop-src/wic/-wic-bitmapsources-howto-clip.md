---
description: Este tópico demonstra como obter uma parte retangular de um IWICBitmapSource usando um componente IWICBitmapClipper.
ms.assetid: c9834827-8e1d-436d-be82-c1a2a2f7ca5c
title: Como recortar uma fonte de bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43919e03d5d866d37ad4af203e741d2b10e60889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104569855"
---
# <a name="how-to-clip-a-bitmap-source"></a><span data-ttu-id="61fbe-103">Como recortar uma fonte de bitmap</span><span class="sxs-lookup"><span data-stu-id="61fbe-103">How to Clip a Bitmap Source</span></span>

<span data-ttu-id="61fbe-104">Este tópico demonstra como obter uma parte retangular de um [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) usando um componente [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) .</span><span class="sxs-lookup"><span data-stu-id="61fbe-104">This topic demonstrates how to obtain a rectangular portion of an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) using an [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) component.</span></span>

<span data-ttu-id="61fbe-105">Para recortar uma fonte de bitmap</span><span class="sxs-lookup"><span data-stu-id="61fbe-105">To clip a bitmap source</span></span>

1.  <span data-ttu-id="61fbe-106">Crie um objeto [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) para criar objetos do Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="61fbe-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="61fbe-107">Use o método [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) para criar um [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) a partir de um arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="61fbe-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

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

    

3.  <span data-ttu-id="61fbe-108">Obtenha o primeiro [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) da imagem.</span><span class="sxs-lookup"><span data-stu-id="61fbe-108">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="61fbe-109">O formato de arquivo JPEG só dá suporte a um único quadro.</span><span class="sxs-lookup"><span data-stu-id="61fbe-109">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="61fbe-110">Como o arquivo neste exemplo é um arquivo JPEG, o primeiro quadro ( `0` ) é usado.</span><span class="sxs-lookup"><span data-stu-id="61fbe-110">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="61fbe-111">Para formatos de imagem que têm vários quadros, consulte [como recuperar os quadros de uma imagem](-wic-bitmapsources-howto-retrieveimageframes.md) para acessar cada quadro da imagem.</span><span class="sxs-lookup"><span data-stu-id="61fbe-111">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

4.  <span data-ttu-id="61fbe-112">Crie o [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) a ser usado para o recorte de imagem.</span><span class="sxs-lookup"><span data-stu-id="61fbe-112">Create the [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) to use for the image clipping.</span></span>

    ```C++
    IWICBitmapClipper *pIClipper = NULL;

    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapClipper(&pIClipper);
    }
    ```

    

5.  <span data-ttu-id="61fbe-113">Inicialize o objeto do Clipper com os dados da imagem dentro do retângulo fornecido do quadro de bitmap.</span><span class="sxs-lookup"><span data-stu-id="61fbe-113">Initialize the clipper object with the image data within the given rectangle of the bitmap frame.</span></span>

    ```C++
    // Create the clipping rectangle.
    WICRect rcClip = { 0, 0, uiWidth/2, uiHeight/2 };

    // Initialize the clipper with the given rectangle of the frame's image data.
    if (SUCCEEDED(hr))
    {
       hr = pIClipper->Initialize(pIDecoderFrame, &rcClip);
    }
    ```

    

6.  <span data-ttu-id="61fbe-114">Desenhe ou processe a imagem recortada.</span><span class="sxs-lookup"><span data-stu-id="61fbe-114">Draw or process the clipped image.</span></span>

    <span data-ttu-id="61fbe-115">A ilustração a seguir demonstra o recorte de imagem.</span><span class="sxs-lookup"><span data-stu-id="61fbe-115">The following illustration demonstrates imaging clipping.</span></span> <span data-ttu-id="61fbe-116">A imagem original à esquerda é 200 x 130 pixels.</span><span class="sxs-lookup"><span data-stu-id="61fbe-116">The original image on the left is 200 x 130 pixels.</span></span> <span data-ttu-id="61fbe-117">A imagem à direita é a imagem original recortada para um retângulo definido como `{20,20,100,100}` .</span><span class="sxs-lookup"><span data-stu-id="61fbe-117">The image on the right is the original image clipped to a rectangle defined as `{20,20,100,100}`.</span></span>

    ![ilustração do recorte de imagens](graphics/cliparegion_axisalignedclip.png)

## <a name="see-also"></a><span data-ttu-id="61fbe-119">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="61fbe-119">See Also</span></span>

[<span data-ttu-id="61fbe-120">Guia de programação</span><span class="sxs-lookup"><span data-stu-id="61fbe-120">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="61fbe-121">Referência</span><span class="sxs-lookup"><span data-stu-id="61fbe-121">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="61fbe-122">Amostras</span><span class="sxs-lookup"><span data-stu-id="61fbe-122">Samples</span></span>](-wic-samples.md)


 

 




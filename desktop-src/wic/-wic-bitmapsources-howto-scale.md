---
description: Este tópico demonstra como dimensionar um IWICBitmapSource usando o componente IWICBitmapScaler.
ms.assetid: d2c65c9b-6f52-46f7-935d-0c582ca83867
title: Como dimensionar uma fonte de bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 737f72014929065bc63ec9c6021b05e38799d06e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090284"
---
# <a name="how-to-scale-a-bitmap-source"></a><span data-ttu-id="cf736-103">Como dimensionar uma fonte de bitmap</span><span class="sxs-lookup"><span data-stu-id="cf736-103">How to Scale a Bitmap Source</span></span>

<span data-ttu-id="cf736-104">Este tópico demonstra como dimensionar um [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) usando o componente [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) .</span><span class="sxs-lookup"><span data-stu-id="cf736-104">This topic demonstrates how to scale an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) using the [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) component.</span></span>

<span data-ttu-id="cf736-105">Para dimensionar uma fonte de bitmap</span><span class="sxs-lookup"><span data-stu-id="cf736-105">To scale a bitmap source</span></span>

1.  <span data-ttu-id="cf736-106">Crie um objeto [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) para criar objetos do Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="cf736-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="cf736-107">Use o método [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) para criar um [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) a partir de um arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="cf736-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

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

    

3.  <span data-ttu-id="cf736-108">Obtenha o primeiro [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) da imagem.</span><span class="sxs-lookup"><span data-stu-id="cf736-108">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="cf736-109">O formato de arquivo JPEG só dá suporte a um único quadro.</span><span class="sxs-lookup"><span data-stu-id="cf736-109">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="cf736-110">Como o arquivo neste exemplo é um arquivo JPEG, o primeiro quadro ( `0` ) é usado.</span><span class="sxs-lookup"><span data-stu-id="cf736-110">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="cf736-111">Para formatos de imagem que têm vários quadros, consulte [como recuperar os quadros de uma imagem](-wic-bitmapsources-howto-retrieveimageframes.md) para acessar cada quadro da imagem.</span><span class="sxs-lookup"><span data-stu-id="cf736-111">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

4.  <span data-ttu-id="cf736-112">Crie o [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) a ser usado para o dimensionamento de imagem.</span><span class="sxs-lookup"><span data-stu-id="cf736-112">Create the [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) to use for the image scaling.</span></span>

    ```C++
    // Create the scaler.
    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapScaler(&pIScaler);
    }
    ```

    

5.  <span data-ttu-id="cf736-113">Inicialize o objeto scaler com os dados da imagem do quadro de bitmap com metade do tamanho.</span><span class="sxs-lookup"><span data-stu-id="cf736-113">Initialize the scaler object with the image data of the bitmap frame at half the size.</span></span>

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

    

6.  <span data-ttu-id="cf736-114">Desenhe ou processe a origem do bitmap em escala.</span><span class="sxs-lookup"><span data-stu-id="cf736-114">Draw or process the scaled bitmap source.</span></span>

    <span data-ttu-id="cf736-115">A ilustração a seguir demonstra o dimensionamento da imagem.</span><span class="sxs-lookup"><span data-stu-id="cf736-115">The following illustration demonstrates imaging scaling.</span></span> <span data-ttu-id="cf736-116">A imagem original à esquerda é 200 x 130 pixels.</span><span class="sxs-lookup"><span data-stu-id="cf736-116">The original image on the left is 200 x 130 pixels.</span></span> <span data-ttu-id="cf736-117">A imagem à direita é a imagem original dimensionada para metade do tamanho.</span><span class="sxs-lookup"><span data-stu-id="cf736-117">The image on the right is the original image scaled to half the size.</span></span>

    ![ilustração mostrando o dimensionamento de uma imagem para um tamanho menor](graphics/scaledregion.png)

## <a name="see-also"></a><span data-ttu-id="cf736-119">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="cf736-119">See Also</span></span>

[<span data-ttu-id="cf736-120">Guia de programação</span><span class="sxs-lookup"><span data-stu-id="cf736-120">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="cf736-121">Referência</span><span class="sxs-lookup"><span data-stu-id="cf736-121">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="cf736-122">Amostras</span><span class="sxs-lookup"><span data-stu-id="cf736-122">Samples</span></span>](-wic-samples.md)


 

 




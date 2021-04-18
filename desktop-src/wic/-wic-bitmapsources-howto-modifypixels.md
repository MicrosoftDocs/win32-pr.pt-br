---
description: Este tópico demonstra como modificar os pixels de uma fonte de bitmap usando os componentes IWICBitmap e IWICBitmapLock.
ms.assetid: a08af015-bc42-4a31-af03-106714b08d08
title: Como modificar os pixels de uma origem de bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8be623d540fcd313476ea5c7ec5e724231d33aec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796153"
---
# <a name="how-to-modify-the-pixels-of-a-bitmap-source"></a><span data-ttu-id="afb5d-103">Como modificar os pixels de uma origem de bitmap</span><span class="sxs-lookup"><span data-stu-id="afb5d-103">How to Modify the Pixels of a Bitmap Source</span></span>

<span data-ttu-id="afb5d-104">Este tópico demonstra como modificar os pixels de uma fonte de bitmap usando os componentes [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) e [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) .</span><span class="sxs-lookup"><span data-stu-id="afb5d-104">This topic demonstrates how to modify the pixels of a bitmap source using the [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) and [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) components.</span></span>

<span data-ttu-id="afb5d-105">Para modificar os pixels de uma origem de bitmap</span><span class="sxs-lookup"><span data-stu-id="afb5d-105">To modify the pixels of a bitmap source</span></span>

1.  <span data-ttu-id="afb5d-106">Crie um objeto [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) para criar objetos do Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="afb5d-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="afb5d-107">Use o método [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) para criar um [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) a partir de um arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="afb5d-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

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

    

3.  <span data-ttu-id="afb5d-108">Obtenha o primeiro [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) da imagem.</span><span class="sxs-lookup"><span data-stu-id="afb5d-108">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="afb5d-109">O formato de arquivo JPEG só dá suporte a um único quadro.</span><span class="sxs-lookup"><span data-stu-id="afb5d-109">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="afb5d-110">Como o arquivo neste exemplo é um arquivo JPEG, o primeiro quadro ( `0` ) é usado.</span><span class="sxs-lookup"><span data-stu-id="afb5d-110">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="afb5d-111">Para formatos de imagem que têm vários quadros, consulte [como recuperar os quadros de uma imagem](-wic-bitmapsources-howto-retrieveimageframes.md) para acessar cada quadro da imagem.</span><span class="sxs-lookup"><span data-stu-id="afb5d-111">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

4.  <span data-ttu-id="afb5d-112">Crie um [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) a partir do quadro de imagem obtido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="afb5d-112">Create an [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) from the previously obtained image frame.</span></span>

    ```C++
    IWICBitmap *pIBitmap = NULL;
    IWICBitmapLock *pILock = NULL;

    UINT uiWidth = 10;
    UINT uiHeight = 10;

    WICRect rcLock = { 0, 0, uiWidth, uiHeight };

    // Create the bitmap from the image frame.
    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapFromSource(
          pIDecoderFrame,          // Create a bitmap from the image frame
          WICBitmapCacheOnDemand,  // Cache metadata when needed
          &pIBitmap);              // Pointer to the bitmap
    }
    ```

    

5.  <span data-ttu-id="afb5d-113">Obtenha um [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) para um retângulo especificado de [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap).</span><span class="sxs-lookup"><span data-stu-id="afb5d-113">Obtain an [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) for a specified rectangle of the [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap).</span></span>

    ```C++
    if (SUCCEEDED(hr))
    {
       // Obtain a bitmap lock for exclusive write.
       // The lock is for a 10x10 rectangle starting at the top left of the
       // bitmap.
       hr = pIBitmap->Lock(&rcLock, WICBitmapLockWrite, &pILock);
    ```

    

6.  <span data-ttu-id="afb5d-114">Processe os dados de pixel que agora estão bloqueados pelo objeto [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) .</span><span class="sxs-lookup"><span data-stu-id="afb5d-114">Process the pixel data that is now locked by the [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) object.</span></span>

    ```C++
       if (SUCCEEDED(hr))
       {
          UINT cbBufferSize = 0;
          BYTE *pv = NULL;

          // Retrieve a pointer to the pixel data.
          if (SUCCEEDED(hr))
          {
             hr = pILock->GetDataPointer(&cbBufferSize, &pv);
          }
          
          // Pixel manipulation using the image data pointer pv.
          // ...

          // Release the bitmap lock.
          SafeRelease(&pILock);
       }
    }
    ```

    

    <span data-ttu-id="afb5d-115">Para desbloquear o [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap), chame [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) em todos os objetos [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) associados ao **IWICBitmap**.</span><span class="sxs-lookup"><span data-stu-id="afb5d-115">To unlock the [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap), call [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on all [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) objects associated with the **IWICBitmap**.</span></span>

7.  <span data-ttu-id="afb5d-116">Limpar os objetos criados.</span><span class="sxs-lookup"><span data-stu-id="afb5d-116">Clean up created objects.</span></span>

    ```C++
    SafeRelease(&pIBitmap);
    SafeRelease(&pIDecoder);
    SafeRelease(&pIDecoderFrame);
    ```

    

## <a name="see-also"></a><span data-ttu-id="afb5d-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="afb5d-117">See Also</span></span>

[<span data-ttu-id="afb5d-118">Guia de programação</span><span class="sxs-lookup"><span data-stu-id="afb5d-118">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="afb5d-119">Referência</span><span class="sxs-lookup"><span data-stu-id="afb5d-119">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="afb5d-120">Amostras</span><span class="sxs-lookup"><span data-stu-id="afb5d-120">Samples</span></span>](-wic-samples.md)


 

 

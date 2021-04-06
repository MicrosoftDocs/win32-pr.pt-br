---
description: Implementando IWICBitmapSource
ms.assetid: d092e9e5-c041-42f5-84c8-0af52bb5c810
title: Implementando IWICBitmapSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c88e2f7dfd073405f9de8c82b2ce6d9592b241a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662755"
---
# <a name="implementing-iwicbitmapsource"></a><span data-ttu-id="b30a8-103">Implementando IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="b30a8-103">Implementing IWICBitmapSource</span></span>

## <a name="iwicbitmapsource"></a><span data-ttu-id="b30a8-104">IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="b30a8-104">IWICBitmapSource</span></span>

<span data-ttu-id="b30a8-105">[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) é importante para trabalhar com imagens de uma perspectiva do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b30a8-105">[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) is important for working with images from an application perspective.</span></span> <span data-ttu-id="b30a8-106">Ele representa a abstração de nível mais alto para uma origem de imagem e todas as interfaces do Windows Imaging Component (WIC) que representam uma imagem, incluindo [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)e todas as interfaces de transformação ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)e [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) são derivadas dela.</span><span class="sxs-lookup"><span data-stu-id="b30a8-106">It represents the highest level abstraction for an image source, and all Windows Imaging Component (WIC) interfaces that represent an image, including [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap), and all the transform interfaces ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator), and [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) are derived from it.</span></span> <span data-ttu-id="b30a8-107">Em qualquer momento específico, um objeto **IWICBitmapSource** pode ou não ser apoiado por um bitmap real na memória.</span><span class="sxs-lookup"><span data-stu-id="b30a8-107">At any specific time, an **IWICBitmapSource** object may or may not be backed by an actual bitmap in memory.</span></span> <span data-ttu-id="b30a8-108">Isso permite um processamento muito eficiente por um aplicativo, pois uma imagem pode ser tratada como uma abstração.</span><span class="sxs-lookup"><span data-stu-id="b30a8-108">This enables very efficient processing by an application, because an image can be dealt with as an abstraction.</span></span> <span data-ttu-id="b30a8-109">As operações de transformação podem ser encadeadas em um pipeline de transformação sem consumir recursos de memória até que o aplicativo esteja pronto para renderizar ou imprimir a imagem e, nesse momento, ele invoca o método [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) na transformação final para obter um bitmap na memória da imagem com as transformações selecionadas aplicadas.</span><span class="sxs-lookup"><span data-stu-id="b30a8-109">Transform operations can be chained in a transform pipeline without consuming memory resources until the application is ready to render or print the image, at which time it invokes the [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) method on the final transform to get a bitmap in memory of the image with the selected transforms applied.</span></span>

``` syntax
interface IWICBitmapSource : IUnknown
{
   // Required methods
   HRESULT GetSize ( UINT *puiWidth, UINT *puiHeight );
   HRESULT GetPixelFormat ( WICPixelFormatGUID *pPixelFormat );
   HRESULT GetResolution ( double *pDpiX, double *pDpiY );
   HRESULT CopyPixels ( const WICRect *prc,
      UINT cbStride,
      UINT cbBufferSize, 
      BYTE *pbBuffer );
   // Optional method
   HRESULT CopyPalette ( IWICPalette *pIPalette );
}
```

<span data-ttu-id="b30a8-110">De uma perspectiva de codec, os métodos [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) são implementados no objeto decodificador de quadro.</span><span class="sxs-lookup"><span data-stu-id="b30a8-110">From a codec perspective, the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) methods are implemented on the frame decoder object.</span></span> <span data-ttu-id="b30a8-111">Esses métodos são descritos em implementando IWICBitmapSource, juntamente com os outros métodos em [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), que é derivado de **IWICBitmapSource**.</span><span class="sxs-lookup"><span data-stu-id="b30a8-111">These methods are described in Implementing IWICBitmapSource, along with the other methods on [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), which is derived from **IWICBitmapSource**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b30a8-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b30a8-112">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b30a8-113">**Referência**</span><span class="sxs-lookup"><span data-stu-id="b30a8-113">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b30a8-114">**IWICBitmapDecoder**</span><span class="sxs-lookup"><span data-stu-id="b30a8-114">**IWICBitmapDecoder**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[<span data-ttu-id="b30a8-115">**IWICBitmapSource**</span><span class="sxs-lookup"><span data-stu-id="b30a8-115">**IWICBitmapSource**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)
</dt> <dt>

[<span data-ttu-id="b30a8-116">**IWICBitmapFrameDecode**</span><span class="sxs-lookup"><span data-stu-id="b30a8-116">**IWICBitmapFrameDecode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

<span data-ttu-id="b30a8-117">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="b30a8-117">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b30a8-118">Implementando IWICBitmapCodecProgressNotification (decodificador)</span><span class="sxs-lookup"><span data-stu-id="b30a8-118">Implementing IWICBitmapCodecProgressNotification (Decoder)</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> <dt>

[<span data-ttu-id="b30a8-119">Implementando IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="b30a8-119">Implementing IWICBitmapFrameDecode</span></span>](-wic-imp-iwicbitmapframedecode.md)
</dt> <dt>

[<span data-ttu-id="b30a8-120">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="b30a8-120">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="b30a8-121">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="b30a8-121">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 




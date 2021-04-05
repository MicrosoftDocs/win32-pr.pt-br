---
description: Implementando IWICBitmapFrameDecode
ms.assetid: 7dc626ad-1158-4b67-8ca7-47b4cf88e278
title: Implementando IWICBitmapFrameDecode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 394b5858ec5eee37ef1c7f52b766806c4a0c1a92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662756"
---
# <a name="implementing-iwicbitmapframedecode"></a><span data-ttu-id="d4b37-103">Implementando IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="d4b37-103">Implementing IWICBitmapFrameDecode</span></span>

## <a name="iwicbitmapframedecode"></a><span data-ttu-id="d4b37-104">IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="d4b37-104">IWICBitmapFrameDecode</span></span>

<span data-ttu-id="d4b37-105">[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) é a interface de nível de quadro que fornece acesso aos bits de imagem reais.</span><span class="sxs-lookup"><span data-stu-id="d4b37-105">[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) is the frame-level interface that provides access to the actual image bits.</span></span> <span data-ttu-id="d4b37-106">Você implementa essa interface em sua classe de decodificação de nível de quadro.</span><span class="sxs-lookup"><span data-stu-id="d4b37-106">You implement this interface on your frame-level decoding class.</span></span> <span data-ttu-id="d4b37-107">Como ele é derivado de [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource), sua implementação de **IWICBitmapFrameDecode** incluirá uma implementação dos métodos **IWICBitmapSource** .</span><span class="sxs-lookup"><span data-stu-id="d4b37-107">Because it’s derived from [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource), your implementation of **IWICBitmapFrameDecode** will include an implementation of the **IWICBitmapSource** methods.</span></span> <span data-ttu-id="d4b37-108">Os métodos adicionais em **IWICBitmapFrameDecode** fornecem acesso à miniatura de nível de quadro, qualquer contextos de cor para a imagem e o leitor de consulta de metadados para o quadro.</span><span class="sxs-lookup"><span data-stu-id="d4b37-108">The additional methods on **IWICBitmapFrameDecode** provide access to the frame-level thumbnail, any color contexts for the image, and the metadata query reader for the frame.</span></span>

``` syntax
interface IWICBitmapFrameDecode : IWICBitmapSource
{
// Required methods
HRESULT GetThumbnail ( IWICBitmapSource **ppIThumbnail );
HRESULT GetColorContexts ( UINT cCount, 
IWICColorContext **ppIColorContexts, UINT *pcActualCount );
HRESULT GetMetadataQueryReader ( IWICMetadataQueryReader **ppIMetadataQueryReader );

// Methods inherited from IWICBitmapSource
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

-   [<span data-ttu-id="d4b37-109">GetThumbnail</span><span class="sxs-lookup"><span data-stu-id="d4b37-109">GetThumbnail</span></span>](#getthumbnail)
-   [<span data-ttu-id="d4b37-110">GetColorContexts</span><span class="sxs-lookup"><span data-stu-id="d4b37-110">GetColorContexts</span></span>](#getcolorcontexts)
-   [<span data-ttu-id="d4b37-111">GetMetadataQueryReader</span><span class="sxs-lookup"><span data-stu-id="d4b37-111">GetMetadataQueryReader</span></span>](#getmetadataqueryreader)
-   [<span data-ttu-id="d4b37-112">GetSize, GetPixelFormat e Resolution</span><span class="sxs-lookup"><span data-stu-id="d4b37-112">GetSize, GetPixelFormat, and GetResolution</span></span>](#getsize-getpixelformat-and-getresolution)
-   [<span data-ttu-id="d4b37-113">CopyPixels</span><span class="sxs-lookup"><span data-stu-id="d4b37-113">CopyPixels</span></span>](#copypixels)
-   [<span data-ttu-id="d4b37-114">CopyPalette</span><span class="sxs-lookup"><span data-stu-id="d4b37-114">CopyPalette</span></span>](#copypalette)

### <a name="getthumbnail"></a><span data-ttu-id="d4b37-115">GetThumbnail</span><span class="sxs-lookup"><span data-stu-id="d4b37-115">GetThumbnail</span></span>

<span data-ttu-id="d4b37-116">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) retorna a miniatura do quadro atual.</span><span class="sxs-lookup"><span data-stu-id="d4b37-116">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) returns the thumbnail for the current frame.</span></span> <span data-ttu-id="d4b37-117">Por motivos de desempenho, as miniaturas são geralmente codificadas em um formato JPEG.</span><span class="sxs-lookup"><span data-stu-id="d4b37-117">For performance reasons, thumbnails are most commonly encoded in a JPEG format.</span></span> <span data-ttu-id="d4b37-118">Assim como acontece com a visualização do decodificador, não é necessário ou recomendado fornecer seu próprio decodificador de JPEG para miniaturas.</span><span class="sxs-lookup"><span data-stu-id="d4b37-118">Just as with the Preview on the decoder, it is not necessary or recommended to provide your own JPEG decoder for thumbnails.</span></span> <span data-ttu-id="d4b37-119">Em vez disso, você deve delegar ao decodificador de JPEG fornecido pelo Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="d4b37-119">Instead, you should delegate to the JPEG decoder provided by Windows Imaging Component (WIC).</span></span>

<span data-ttu-id="d4b37-120">Para obter mais informações sobre miniaturas, consulte o método [SetThumbnail](-wic-imp-iwicbitmapframeencode.md) sobre [implementação de IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md).</span><span class="sxs-lookup"><span data-stu-id="d4b37-120">For more information on thumbnails, see the [SetThumbnail](-wic-imp-iwicbitmapframeencode.md) method on [Implementing IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md).</span></span>

### <a name="getcolorcontexts"></a><span data-ttu-id="d4b37-121">GetColorContexts</span><span class="sxs-lookup"><span data-stu-id="d4b37-121">GetColorContexts</span></span>

<span data-ttu-id="d4b37-122">[**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) retorna os contextos de cor válidos (também conhecidos como perfis de cor) associados à imagem neste quadro.</span><span class="sxs-lookup"><span data-stu-id="d4b37-122">[**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) returns the valid color contexts (also known as color profiles) associated with the image in this frame.</span></span> <span data-ttu-id="d4b37-123">Na maioria dos casos, isso só será um, mas pode haver casos em que há dois ou, raramente, mais.</span><span class="sxs-lookup"><span data-stu-id="d4b37-123">In most cases, this will only be one, but there could be cases where there are two or, rarely, more.</span></span> <span data-ttu-id="d4b37-124">O chamador passará um ou mais objetos [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) , definindo o parâmetro *conta* para indicar quantos eles estão passando.</span><span class="sxs-lookup"><span data-stu-id="d4b37-124">The caller will pass in one or more [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) objects, setting the *cCount* parameter to indicate how many they are passing in.</span></span> <span data-ttu-id="d4b37-125">Esse método popula os objetos **IWICColorContext** com os dados de contexto de cor reais para os perfis de cor associados à imagem.</span><span class="sxs-lookup"><span data-stu-id="d4b37-125">This method populates the **IWICColorContext** objects with the actual color context data for the color profiles associated with the image.</span></span> <span data-ttu-id="d4b37-126">Defina o parâmetro *pcActualCount* como o número real de contextos de cor associados à imagem, mesmo que isso seja maior que o número que você pode retornar.</span><span class="sxs-lookup"><span data-stu-id="d4b37-126">Set the *pcActualCount* parameter to the actual number of color contexts associated with the image, even if this is greater than the number you can return.</span></span> <span data-ttu-id="d4b37-127">(No caso em que mais contextos de cor estão disponíveis do que o número de objetos **IWICColorContext** passados pelo chamador, isso informa ao chamador que há um ou mais outros disponíveis.)</span><span class="sxs-lookup"><span data-stu-id="d4b37-127">(In the case where more color contexts are available than the number of **IWICColorContext** objects passed in by the caller, this tells the caller there are one or more others available.)</span></span>

### <a name="getmetadataqueryreader"></a><span data-ttu-id="d4b37-128">GetMetadataQueryReader</span><span class="sxs-lookup"><span data-stu-id="d4b37-128">GetMetadataQueryReader</span></span>

<span data-ttu-id="d4b37-129">[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) retorna um [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) que pode ser usado por um aplicativo para recuperar metadados do quadro da imagem.</span><span class="sxs-lookup"><span data-stu-id="d4b37-129">[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) returns an [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) that an application can use to retrieve metadata from the image frame.</span></span> <span data-ttu-id="d4b37-130">Essa interface é implementada por um manipulador de metadados e permite que um aplicativo consulte Propriedades de metadados específicas que pertencem a um formato de metadados específico.</span><span class="sxs-lookup"><span data-stu-id="d4b37-130">This interface is implemented by a metadata handler, and allows an application to query for specific metadata properties belonging to a particular metadata format.</span></span> <span data-ttu-id="d4b37-131">Para obter mais informações, consulte [implementando o IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md).</span><span class="sxs-lookup"><span data-stu-id="d4b37-131">For more information, see [Implementing IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md).</span></span>

<span data-ttu-id="d4b37-132">Para criar uma instância de um [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader), chame [**CreateQueryReaderFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createqueryreaderfromblockreader) no [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory).</span><span class="sxs-lookup"><span data-stu-id="d4b37-132">To instantiate an [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader), call [**CreateQueryReaderFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createqueryreaderfromblockreader) on the [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory).</span></span>


```C++
IWICMetadataQueryReader* pQueryReader = NULL;
HRESULT hr;

hr = m_pComponentFactory->CreateQueryReaderFromBlockReader( 
  static_cast<IWICMetadataBlockWriter*>(this),
  &pQueryReader);
```



### <a name="getsize-getpixelformat-and-getresolution"></a><span data-ttu-id="d4b37-133">GetSize, GetPixelFormat e Resolution</span><span class="sxs-lookup"><span data-stu-id="d4b37-133">GetSize, GetPixelFormat, and GetResolution</span></span>

<span data-ttu-id="d4b37-134">[**GetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize), [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat)e [**Resolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) são auto-explicativos e retornam as propriedades solicitadas da imagem.</span><span class="sxs-lookup"><span data-stu-id="d4b37-134">[**GetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize), [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat), and [**GetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) are self-explanatory, and return the requested properties of the image.</span></span>

### <a name="copypixels"></a><span data-ttu-id="d4b37-135">CopyPixels</span><span class="sxs-lookup"><span data-stu-id="d4b37-135">CopyPixels</span></span>

<span data-ttu-id="d4b37-136">[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) é o método chamado por um aplicativo quando ele deseja criar um bitmap na memória que pode ser renderizado para a exibição ou impressora.</span><span class="sxs-lookup"><span data-stu-id="d4b37-136">[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) is the method an application calls when it wants to create a bitmap in memory that can be rendered to the display or printer.</span></span> <span data-ttu-id="d4b37-137">Esse é o método que faz a decodificação real dos bits de imagem.</span><span class="sxs-lookup"><span data-stu-id="d4b37-137">This is the method that does the actual decoding of the image bits.</span></span> <span data-ttu-id="d4b37-138">Os parâmetros são um retângulo, que representa a região de interesse na imagem de origem a ser copiada na memória; o stride, que especifica o número de bytes em uma linha de digitalização; o tamanho do buffer na memória que foi alocado pelo aplicativo; e um ponteiro para o buffer no qual os bits de imagem solicitados devem ser copiados.</span><span class="sxs-lookup"><span data-stu-id="d4b37-138">The parameters are a rectangle, which represents the region of interest in the source image to copy into memory; the stride, which specifies the number of bytes in one scan line; the size of the buffer in memory that has been allocated by the application; and a pointer to the buffer into which the requested image bits should be copied.</span></span> <span data-ttu-id="d4b37-139">(Para evitar que estouros de buffer em potencial introduzam vulnerabilidades de segurança, certifique-se de copiar apenas a quantidade de dados de imagem no buffer que o parâmetro *cbBufferSize* especifica.)</span><span class="sxs-lookup"><span data-stu-id="d4b37-139">(To prevent potential buffer overruns from introducing security vulnerabilities, be sure to copy only as much image data into the buffer as the *cbBufferSize* parameter specifies.)</span></span>

### <a name="copypalette"></a><span data-ttu-id="d4b37-140">CopyPalette</span><span class="sxs-lookup"><span data-stu-id="d4b37-140">CopyPalette</span></span>

<span data-ttu-id="d4b37-141">Somente os codecs que têm formatos de pixel indexados devem implementar o método [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) .</span><span class="sxs-lookup"><span data-stu-id="d4b37-141">Only codecs that have indexed pixel formats must implement the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) method.</span></span> <span data-ttu-id="d4b37-142">Se uma imagem usar um formato indexado, use esse método para retornar a paleta de cores usadas na imagem.</span><span class="sxs-lookup"><span data-stu-id="d4b37-142">If an image uses an indexed format, use this method to return the palette of colors used in the image.</span></span> <span data-ttu-id="d4b37-143">Se o seu codec não tiver um formato indexado, retornará WINCODEC \_ Err \_ PALETTEUNAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="d4b37-143">If your codec doesn’t have an indexed format, return WINCODEC\_ERR\_PALETTEUNAVAILABLE.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4b37-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d4b37-144">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d4b37-145">**Referência**</span><span class="sxs-lookup"><span data-stu-id="d4b37-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d4b37-146">**IWICBitmapSource**</span><span class="sxs-lookup"><span data-stu-id="d4b37-146">**IWICBitmapSource**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)
</dt> <dt>

[<span data-ttu-id="d4b37-147">**IWICBitmapDecoder**</span><span class="sxs-lookup"><span data-stu-id="d4b37-147">**IWICBitmapDecoder**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[<span data-ttu-id="d4b37-148">**IWICBitmapFrameDecode**</span><span class="sxs-lookup"><span data-stu-id="d4b37-148">**IWICBitmapFrameDecode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

<span data-ttu-id="d4b37-149">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="d4b37-149">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d4b37-150">Implementando IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="d4b37-150">Implementing IWICBitmapSource</span></span>](-wic-imp-iwicbitmapsource.md)
</dt> <dt>

[<span data-ttu-id="d4b37-151">Implementando o IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="d4b37-151">Implementing IWICMetadataBlockReader</span></span>](-wic-imp-iwicmetadatablockreader.md)
</dt> <dt>

[<span data-ttu-id="d4b37-152">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="d4b37-152">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="d4b37-153">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="d4b37-153">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 




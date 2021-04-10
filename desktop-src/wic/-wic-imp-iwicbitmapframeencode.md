---
description: Implementando IWICBitmapFrameEncode
ms.assetid: 509fa49c-c90d-4270-a338-6ce638ccd89a
title: Implementando IWICBitmapFrameEncode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d2a5ea0412ea4a45ea329618d00443c1755391
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170872"
---
# <a name="implementing-iwicbitmapframeencode"></a><span data-ttu-id="356f1-103">Implementando IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="356f1-103">Implementing IWICBitmapFrameEncode</span></span>

## <a name="iwicbitmapframeencode"></a><span data-ttu-id="356f1-104">IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="356f1-104">IWICBitmapFrameEncode</span></span>

<span data-ttu-id="356f1-105">[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) é o equivalente do codificador à interface [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="356f1-105">[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) is the encoder’s counterpart to the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) interface.</span></span> <span data-ttu-id="356f1-106">Você pode implementar essa interface em sua classe de codificação de nível de quadro, que é a classe que faz a codificação real dos bits de imagem para cada quadro.</span><span class="sxs-lookup"><span data-stu-id="356f1-106">You can implement this interface on your frame-level encoding class, which is the class that does the actual encoding of the image bits for each frame.</span></span>


```C++
interface IWICBitmapFrameEncode : public IUnknown
{
   // Required methods
   HRESULT Initialize ( IPropertyBag2 *pIEncoderOptions );
   HRESULT SetSize ( UINT width,
               UINT height );
   HRESULT SetResolution ( double dpiX,
               double dpiY );
   HRESULT SetPixelFormat (WICPixelFormatGUID *pPixelFormat);
   HRESULT SetColorContexts ( UINT cCount,
               IWICColorContext **ppIColorContext );
   HRESULT GetMetadataQueryWriter ( IWICMetadataQueryWriter 
               **ppIMetadataQueryWriter );
   HRESULT SetThumbnail ( IWICBitmapSource *pIThumbnail );
   HRESULT WritePixels ( UINT lineCount,
               UINT cbStride,
               UINT cbBufferSize,
               BYTE *pbPixels );
   HRESULT WriteSource ( IWICBitmapSource *pIWICBitmapSource,
               WICRect *prc );
   HRESULT Commit ( void );

// Optional method
   HRESULT SetPalette ( IWICPalette *pIPalette );
};
```



-   [<span data-ttu-id="356f1-107">Inicializar</span><span class="sxs-lookup"><span data-stu-id="356f1-107">Initialize</span></span>](#initialize)
-   [<span data-ttu-id="356f1-108">SetSize e Resolution</span><span class="sxs-lookup"><span data-stu-id="356f1-108">SetSize and SetResolution</span></span>](#setsize-and-setresolution)
-   [<span data-ttu-id="356f1-109">SetPixelFormat</span><span class="sxs-lookup"><span data-stu-id="356f1-109">SetPixelFormat</span></span>](#setpixelformat)
-   [<span data-ttu-id="356f1-110">SetColorContexts</span><span class="sxs-lookup"><span data-stu-id="356f1-110">SetColorContexts</span></span>](#setcolorcontexts)
-   [<span data-ttu-id="356f1-111">GetMetadataQueryWriter</span><span class="sxs-lookup"><span data-stu-id="356f1-111">GetMetadataQueryWriter</span></span>](#getmetadataquerywriter)
-   [<span data-ttu-id="356f1-112">SetThumbnail</span><span class="sxs-lookup"><span data-stu-id="356f1-112">SetThumbnail</span></span>](#setthumbnail)
-   [<span data-ttu-id="356f1-113">WritePixels</span><span class="sxs-lookup"><span data-stu-id="356f1-113">WritePixels</span></span>](#writepixels)
-   [<span data-ttu-id="356f1-114">Gravação</span><span class="sxs-lookup"><span data-stu-id="356f1-114">WriteSource</span></span>](#writesource)
-   [<span data-ttu-id="356f1-115">Confirmar</span><span class="sxs-lookup"><span data-stu-id="356f1-115">Commit</span></span>](#commit)
-   [<span data-ttu-id="356f1-116">SetPalette</span><span class="sxs-lookup"><span data-stu-id="356f1-116">SetPalette</span></span>](#setpalette)

### <a name="initialize"></a><span data-ttu-id="356f1-117">Inicializar</span><span class="sxs-lookup"><span data-stu-id="356f1-117">Initialize</span></span>

<span data-ttu-id="356f1-118">[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) é o primeiro método invocado em um objeto [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) depois de ter sido instanciado.</span><span class="sxs-lookup"><span data-stu-id="356f1-118">[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) is the first method invoked on an [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object after it has been instantiated.</span></span> <span data-ttu-id="356f1-119">Esse método tem um parâmetro, que pode ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="356f1-119">This method has one parameter, which may be set to **NULL**.</span></span> <span data-ttu-id="356f1-120">Esse parâmetro representa as opções de codificador e é a mesma instância de [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) que você criou no método [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) no decodificador de nível de contêiner e passado de volta para o chamador no parâmetro pIEncoderOptions desse método.</span><span class="sxs-lookup"><span data-stu-id="356f1-120">This parameter represents the encoder options, and is the same [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) instance that you created in the [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) method on the container-level decoder, and passed back to the caller in the pIEncoderOptions parameter of that method.</span></span> <span data-ttu-id="356f1-121">Nesse momento, você preencheu o struct IPropertyBag2 com propriedades que representam as opções de codificação com suporte no seu codificador de nível de quadro.</span><span class="sxs-lookup"><span data-stu-id="356f1-121">At that time, you populated the IPropertyBag2 struct with properties that represent the encoding options supported by your frame-level encoder.</span></span> <span data-ttu-id="356f1-122">O chamador agora forneceu valores para essas propriedades para indicar determinados parâmetros de opção de codificação e está passando o mesmo objeto de volta para você inicializar o objeto **IWICBitmapFrameEncode** .</span><span class="sxs-lookup"><span data-stu-id="356f1-122">The caller has now provided values for those properties to indicate certain encoding option parameters, and is passing the same object back to you to initialize the **IWICBitmapFrameEncode** object.</span></span> <span data-ttu-id="356f1-123">Você deve aplicar as opções especificadas ao codificar os bits de imagem.</span><span class="sxs-lookup"><span data-stu-id="356f1-123">You should apply the specified options when encoding the image bits.</span></span>

### <a name="setsize-and-setresolution"></a><span data-ttu-id="356f1-124">SetSize e Resolution</span><span class="sxs-lookup"><span data-stu-id="356f1-124">SetSize and SetResolution</span></span>

<span data-ttu-id="356f1-125">[**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) e [**Resolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) são auto-explicativos.</span><span class="sxs-lookup"><span data-stu-id="356f1-125">[**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) and [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) are self-explanatory.</span></span> <span data-ttu-id="356f1-126">O chamador usa esses métodos para especificar o tamanho e a resolução da imagem codificada.</span><span class="sxs-lookup"><span data-stu-id="356f1-126">The caller uses these methods to specify the size and resolution for the encoded image.</span></span>

### <a name="setpixelformat"></a><span data-ttu-id="356f1-127">SetPixelFormat</span><span class="sxs-lookup"><span data-stu-id="356f1-127">SetPixelFormat</span></span>

<span data-ttu-id="356f1-128">[**SetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat) é usado para solicitar um formato de pixel no qual codificar a imagem.</span><span class="sxs-lookup"><span data-stu-id="356f1-128">[**SetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat) is used to request a pixel format in which to encode the image.</span></span> <span data-ttu-id="356f1-129">Se não houver suporte para o formato de pixel solicitado, você deverá retornar o GUID do formato de pixel mais próximo com suporte em *pPixelFormat*, que é um parâmetro in/out.</span><span class="sxs-lookup"><span data-stu-id="356f1-129">If the requested pixel format is not supported, you should return the GUID of the closest pixel format that is supported in *pPixelFormat*, which is an in/out parameter.</span></span>

### <a name="setcolorcontexts"></a><span data-ttu-id="356f1-130">SetColorContexts</span><span class="sxs-lookup"><span data-stu-id="356f1-130">SetColorContexts</span></span>

<span data-ttu-id="356f1-131">[**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts) é usado para especificar um ou mais contextos de cor válidos (também conhecidos como perfis de cor) para esta imagem.</span><span class="sxs-lookup"><span data-stu-id="356f1-131">[**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts) is used to specify one or more valid color contexts (also known as color profiles) for this image.</span></span> <span data-ttu-id="356f1-132">É importante especificar os contextos de cor, de modo que um aplicativo que decodifique a imagem posteriormente possa converter do perfil de cor de origem para o perfil de destino do dispositivo que está sendo usado para exibir ou imprimir a imagem.</span><span class="sxs-lookup"><span data-stu-id="356f1-132">It’s important to specify the color contexts, so an application that decodes the image at a later time can convert from the source color profile to the destination profile of the device being used to display or print the image.</span></span> <span data-ttu-id="356f1-133">Sem um perfil de cor, não é possível obter cores consistentes em diferentes dispositivos.</span><span class="sxs-lookup"><span data-stu-id="356f1-133">Without a color profile, it is not possible to get consistent colors across different devices.</span></span> <span data-ttu-id="356f1-134">Isso pode ser frustrante para os usuários finais quando suas fotos parecem diferentes em monitores diferentes e não conseguem fazer as cópias coincidirem com o que vêem na tela.</span><span class="sxs-lookup"><span data-stu-id="356f1-134">This can be frustrating for end users when their photos look different on different monitors, and they can’t get the prints to match what they see on screen.</span></span>

### <a name="getmetadataquerywriter"></a><span data-ttu-id="356f1-135">GetMetadataQueryWriter</span><span class="sxs-lookup"><span data-stu-id="356f1-135">GetMetadataQueryWriter</span></span>

<span data-ttu-id="356f1-136">[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) retorna um [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) que pode ser usado por um aplicativo para inserir ou editar propriedades de metadados específicas em um bloco de metadados no quadro da imagem.</span><span class="sxs-lookup"><span data-stu-id="356f1-136">[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) returns an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) that an application can use to insert or edit specific metadata properties in a metadata block on the image frame.</span></span>

<span data-ttu-id="356f1-137">Você pode criar uma instância de um [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) do [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) de várias maneiras.</span><span class="sxs-lookup"><span data-stu-id="356f1-137">You can instantiate an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) from the [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) in several ways.</span></span> <span data-ttu-id="356f1-138">Você pode criá-lo de seu [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter), da mesma forma que [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) foi criado a partir de um [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) no método [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) na interface [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="356f1-138">You can either create it from your [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter), the same way [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) was created from an [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) in the [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) method on the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) interface.</span></span>


```C++
IWICMetadataQueryWriter* piMetadataQueryWriter = NULL;
HRESULT hr;

hr = m_piComponentFactory->CreateQueryWriterFromBlockWriter( 
      static_cast<IWICMetadataBlockWriter*>(this), 
      &piMetadataQueryWriter);

```



<span data-ttu-id="356f1-139">Você também pode criá-lo de um [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)existente, como aquele obtido usando o método anterior.</span><span class="sxs-lookup"><span data-stu-id="356f1-139">You can also create it from an existing [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader), such as the one obtained using the previous method.</span></span>


```C++
hr = m_piComponentFactory->CreateQueryWriterFromReader( 
      piMetadataQueryReader, pguidVendor, &piMetadataQueryWriter);
```



<span data-ttu-id="356f1-140">O parâmetro *pguidVendor* permite que você especifique um fornecedor específico para o gravador de consulta usar ao instanciar um gravador de metadados.</span><span class="sxs-lookup"><span data-stu-id="356f1-140">The *pguidVendor* parameter allows you to specify a particular vendor for the query writer to use when instantiating a metadata writer.</span></span> <span data-ttu-id="356f1-141">Por exemplo, se você fornecer seus próprios gravadores de metadados, talvez queira especificar seu próprio GUID de fornecedor.</span><span class="sxs-lookup"><span data-stu-id="356f1-141">For example, if you provide your own metadata writers, you may want to specify your own vendor GUID.</span></span> <span data-ttu-id="356f1-142">Você pode passar **NULL** para esse parâmetro se não tiver uma preferência.</span><span class="sxs-lookup"><span data-stu-id="356f1-142">You can pass **NULL** to this parameter if you don’t have a preference.</span></span>

### <a name="setthumbnail"></a><span data-ttu-id="356f1-143">SetThumbnail</span><span class="sxs-lookup"><span data-stu-id="356f1-143">SetThumbnail</span></span>

<span data-ttu-id="356f1-144">[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) é usado para fornecer uma miniatura.</span><span class="sxs-lookup"><span data-stu-id="356f1-144">[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) is used to provide a thumbnail.</span></span> <span data-ttu-id="356f1-145">Todas as imagens devem fornecer uma miniatura globalmente, em cada quadro ou em ambas.</span><span class="sxs-lookup"><span data-stu-id="356f1-145">All images should provide a thumbnail either globally, on each frame, or both.</span></span> <span data-ttu-id="356f1-146">Os métodos **GetThumbnail** e **SetThumbnail** são opcionais no nível do contêiner, mas, se um codec retornar WINCODEC \_ Err \_ CODECNOTHUMBNAIL do método [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) , o Windows Imaging Component (WIC) invocará o método [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) para o quadro 0.</span><span class="sxs-lookup"><span data-stu-id="356f1-146">The **GetThumbnail** and **SetThumbnail** methods are optional at the container-level but, if a codec returns WINCODEC\_ERR\_CODECNOTHUMBNAIL from the [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) method, Windows Imaging Component (WIC) will invoke the [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) method for Frame 0.</span></span> <span data-ttu-id="356f1-147">Se nenhuma miniatura for encontrada em qualquer lugar, o WIC deverá decodificar a imagem completa e dimensioná-la para o tamanho da miniatura, o que pode incorrer em uma grande penalidade de desempenho para imagens maiores.</span><span class="sxs-lookup"><span data-stu-id="356f1-147">If no thumbnail is found in either place, WIC must decode the full image and scale it to thumbnail size, which could incur a large performance penalty for larger images.</span></span>

<span data-ttu-id="356f1-148">A miniatura deve ter um tamanho e uma resolução que tornem a decodificação e a exibição rápidas.</span><span class="sxs-lookup"><span data-stu-id="356f1-148">The thumbnail should be of a size and resolution that makes it quick to decode and display.</span></span> <span data-ttu-id="356f1-149">Por esse motivo, as miniaturas são imagens JPEG mais comuns.</span><span class="sxs-lookup"><span data-stu-id="356f1-149">For this reason, thumbnails are most commonly JPEG images.</span></span> <span data-ttu-id="356f1-150">Observe que, se você usar JPEG para suas miniaturas, não precisará escrever um codificador de JPEG para codificá-las ou um decodificador de JPEG para decodificá-las.</span><span class="sxs-lookup"><span data-stu-id="356f1-150">Note that, if you use JPEG for your thumbnails, you don’t have to write a JPEG encoder to encode them, or a JPEG decoder to decode them.</span></span> <span data-ttu-id="356f1-151">Você sempre deve delegar ao codec JPEG fornecido com a plataforma WIC para codificação e decodificação de miniaturas.</span><span class="sxs-lookup"><span data-stu-id="356f1-151">You should always delegate to the JPEG codec that ships with the WIC platform for encoding and decoding thumbnails.</span></span>

### <a name="writepixels"></a><span data-ttu-id="356f1-152">WritePixels</span><span class="sxs-lookup"><span data-stu-id="356f1-152">WritePixels</span></span>

<span data-ttu-id="356f1-153">[**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) é o método usado para passar linhas de verificação de um bitmap na memória para codificação.</span><span class="sxs-lookup"><span data-stu-id="356f1-153">[**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) is the method used to pass in scan lines from a bitmap in memory for encoding.</span></span> <span data-ttu-id="356f1-154">O método será chamado repetidamente até que todas as linhas de verificação tenham sido passadas.</span><span class="sxs-lookup"><span data-stu-id="356f1-154">The method will be called repeatedly until all of the scan lines have been passed in.</span></span> <span data-ttu-id="356f1-155">O parâmetro *LineCount* indica quantas linhas de verificação devem ser gravadas nesta chamada.</span><span class="sxs-lookup"><span data-stu-id="356f1-155">The *lineCount* parameter indicates how many scan lines are to be written in this call.</span></span> <span data-ttu-id="356f1-156">O parâmetro *cbStride* indica o número de bytes por linha de varredura.</span><span class="sxs-lookup"><span data-stu-id="356f1-156">The *cbStride* parameter indicates the number of bytes per scan line.</span></span> <span data-ttu-id="356f1-157">*cbBufferSize* indica o tamanho do buffer passado no parâmetro pbPixels, que contém os bits de imagem reais a serem codificados.</span><span class="sxs-lookup"><span data-stu-id="356f1-157">*cbBufferSize* indicates the size of the buffer passed in the pbPixels parameter, which contains the actual image bits to be encoded.</span></span> <span data-ttu-id="356f1-158">Se a altura combinada das linhas de verificação das chamadas cumulativas for maior que a altura especificada no método [**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) , retornará WINCODEC \_ Err \_ TOOMANYSCANLINES.</span><span class="sxs-lookup"><span data-stu-id="356f1-158">If the combined height of the scan lines from cumulative calls is greater than the height specified in [**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) method, return WINCODEC\_ERR\_TOOMANYSCANLINES.</span></span>

<span data-ttu-id="356f1-159">Quando [**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) for **WICBitmapEncoderCacheInMemory**, as linhas de verificação deverão ser armazenadas em cache na memória até que todas as linhas de verificação tenham sido passadas.</span><span class="sxs-lookup"><span data-stu-id="356f1-159">When the [**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) is **WICBitmapEncoderCacheInMemory**, the scan lines should be cached in memory until all scan lines have been passed in.</span></span> <span data-ttu-id="356f1-160">Se a opção de cache do codificador for **WICBitmapEncoderCacheTempFile**, as linhas de verificação deverão ser armazenadas em cache em um arquivo temporário, criado durante a inicialização do objeto.</span><span class="sxs-lookup"><span data-stu-id="356f1-160">If the encoder cache option is **WICBitmapEncoderCacheTempFile**, the scan lines should be cached in a temporary file, created when initializing the object.</span></span> <span data-ttu-id="356f1-161">Em qualquer um desses casos, a imagem não deve ser codificada até que o chamador chame [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit).</span><span class="sxs-lookup"><span data-stu-id="356f1-161">In either of these cases, the image should not be encoded until the caller calls [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit).</span></span> <span data-ttu-id="356f1-162">No caso em que a opção de cache é **WICBitmapEncoderNoCache**, o codificador deve codificar as linhas de varredura conforme elas são recebidas, se possível.</span><span class="sxs-lookup"><span data-stu-id="356f1-162">In the case where the cache option is **WICBitmapEncoderNoCache**, the encoder should encode the scan lines as they’re received, if possible.</span></span> <span data-ttu-id="356f1-163">(Em alguns formatos, isso não é possível e as linhas de verificação devem ser armazenadas em cache até que a confirmação seja chamada.)</span><span class="sxs-lookup"><span data-stu-id="356f1-163">(In some formats, this is not possible, and the scan lines must be cached until Commit is called.)</span></span>

<span data-ttu-id="356f1-164">A maioria dos codecs brutos não implementará [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels), pois eles não dão suporte à alteração dos bits de imagem no arquivo bruto.</span><span class="sxs-lookup"><span data-stu-id="356f1-164">Most raw codecs will not implement [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels), because they don’t support altering the image bits in the raw file.</span></span> <span data-ttu-id="356f1-165">No entanto, os codecs brutos ainda devem implementar **WritePixels**, porque quando os metadados são adicionados, ele pode aumentar o tamanho do arquivo, exigindo que o arquivo seja regravado no disco.</span><span class="sxs-lookup"><span data-stu-id="356f1-165">Raw codecs should still implement **WritePixels**, however, because when metadata is added, it may increase the size of the file, requiring the file to be rewritten on the disk.</span></span> <span data-ttu-id="356f1-166">Nesse caso, é necessário ser capaz de copiar os bits de imagem existentes, que é o que o método **WritePixels** faz.</span><span class="sxs-lookup"><span data-stu-id="356f1-166">In that case, it’s necessary to be able to copy the existing image bits, which is what the **WritePixels** method does.</span></span>

### <a name="writesource"></a><span data-ttu-id="356f1-167">Gravação</span><span class="sxs-lookup"><span data-stu-id="356f1-167">WriteSource</span></span>

<span data-ttu-id="356f1-168">O [**writeprovider**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) é usado para codificar um objeto [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .</span><span class="sxs-lookup"><span data-stu-id="356f1-168">[**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) is used to encode an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span> <span data-ttu-id="356f1-169">O primeiro parâmetro é um ponteiro para um objeto **IWICBitmapSource** .</span><span class="sxs-lookup"><span data-stu-id="356f1-169">The first parameter is a pointer to an **IWICBitmapSource** object.</span></span> <span data-ttu-id="356f1-170">O segundo parâmetro é um WICRect que especifica a região de interesse a ser codificada.</span><span class="sxs-lookup"><span data-stu-id="356f1-170">The second parameter is a WICRect that specifies the region of interest to encode.</span></span> <span data-ttu-id="356f1-171">Esse método pode ser chamado várias vezes em sucessão, desde que a largura de cada retângulo tenha a mesma largura da imagem final a ser codificada.</span><span class="sxs-lookup"><span data-stu-id="356f1-171">This method may be called multiple times in succession, as long as the width of each rectangle is the same width of the final image to be encoded.</span></span> <span data-ttu-id="356f1-172">Se a largura do retângulo passado no parâmetro prc for diferente da largura especificada no método setSize, retornará WINCODEC \_ Err \_ SOURCERECTDOESNOTMATCHDIMENSIONS.</span><span class="sxs-lookup"><span data-stu-id="356f1-172">If the width of the rectangle passed in the prc parameter is different than the width specified in the SetSize method, return WINCODEC\_ERR\_SOURCERECTDOESNOTMATCHDIMENSIONS.</span></span> <span data-ttu-id="356f1-173">Se a altura combinada das linhas de verificação das chamadas cumulativas for maior que a altura especificada no método setSize, retornará WINCODEC \_ Err \_ TOOMANYSCANLINES.</span><span class="sxs-lookup"><span data-stu-id="356f1-173">If the combined height of the scan lines from cumulative calls is greater than the height specified in SetSize method, return WINCODEC\_ERR\_TOOMANYSCANLINES.</span></span>

<span data-ttu-id="356f1-174">As opções de cache funcionam da mesma maneira com esse método, como com o método [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="356f1-174">The cache options work the same way with this method as with the [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) method described previously.</span></span>

### <a name="commit"></a><span data-ttu-id="356f1-175">Commit</span><span class="sxs-lookup"><span data-stu-id="356f1-175">Commit</span></span>

<span data-ttu-id="356f1-176">[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) é o método que serializa os bits de imagem codificada para o fluxo de arquivos e faz a iteração por todos os gravadores de metadados para o quadro que os solicita para serializar seus metadados para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="356f1-176">[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) is the method that serializes the encoded image bits to the file stream, and iterates through all the metadata writers for the frame requesting them to serialize their metadata to the stream.</span></span> <span data-ttu-id="356f1-177">No caso em que a opção de cache do codificador é WICBitmapEncoderCacheInMemory ou WICBitmapEncoderCacheTempFile, esse método também é responsável por codificar a imagem e, quando a opção cache é WICBitmapEncoderCacheTempFile, o método **Commit** também deve excluir o arquivo temporário usado para armazenar em cache os dados da imagem antes da codificação.</span><span class="sxs-lookup"><span data-stu-id="356f1-177">In the case where the encoder cache option is WICBitmapEncoderCacheInMemory or WICBitmapEncoderCacheTempFile, this method is also responsible for encoding the image, and when the cache option is WICBitmapEncoderCacheTempFile, the **Commit** method should also delete the temporary file used to cache the image data before encoding.</span></span>

<span data-ttu-id="356f1-178">Esse método é sempre invocado depois que todas as linhas de verificação ou retângulos que compõem a imagem foram passados usando o método [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) ou [**writery**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) .</span><span class="sxs-lookup"><span data-stu-id="356f1-178">This method is always invoked after all the scan lines or rectangles that make up the image have been passed in using either the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) or [**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) method.</span></span> <span data-ttu-id="356f1-179">O tamanho do retângulo final que é composto por meio das chamadas acumuladas para WritePixels ou WriteName deve ter o mesmo tamanho que foi especificado no método setSize.</span><span class="sxs-lookup"><span data-stu-id="356f1-179">The size of the final rectangle that is composed through the accumulated calls to WritePixels or WriteSource must be the same size as was specified in the SetSize method.</span></span> <span data-ttu-id="356f1-180">Se o tamanho não corresponder ao tamanho esperado, esse método deverá retornar WINCODECERROR \_ UNEXPECTEDSIZE.</span><span class="sxs-lookup"><span data-stu-id="356f1-180">If the size does not match the expected size, this method should return WINCODECERROR\_UNEXPECTEDSIZE.</span></span>

<span data-ttu-id="356f1-181">Para iterar os gravadores de metadados e informar a cada gravador de metadados para serializar seus metadados, acesse o fluxo, invoque GetWriterByIndex para iterar pelos gravadores para cada bloco e invoque IWICPersistStream. Save em cada gravador de metadados.</span><span class="sxs-lookup"><span data-stu-id="356f1-181">To iterate through the metadata writers and tell each metadata writer to serialize its metadata go the stream, invoke GetWriterByIndex to iterate through the writers for each block, and invoke IWICPersistStream.Save on each metadata writer.</span></span>


```C++
IWICMetadataWriter* piMetadataWRiter = NULL;
IWICPersistStream* piPersistStream = NULL;
HRESULT hr;

for (UINT x=0; x < m_blockCount; x++) 
{
    hr = GetWriterByIndex(x, & piMetadataWriter);
hr = piMetadataWriter->QueryInterface(
IID_IWICPersistStream,(void**)&piPersistStream);

hr = piPersistStream->Save(m_piStream, 
WICPersistOptions.WicPersistOptionDefault, 
true);
...
}
```



### <a name="setpalette"></a><span data-ttu-id="356f1-182">SetPalette</span><span class="sxs-lookup"><span data-stu-id="356f1-182">SetPalette</span></span>

<span data-ttu-id="356f1-183">Somente os codecs que têm formatos indexados precisam implementar o método [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpalette) .</span><span class="sxs-lookup"><span data-stu-id="356f1-183">Only codecs that have indexed formats need to implement the [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpalette) method.</span></span> <span data-ttu-id="356f1-184">Se uma imagem usar um formato indexado, use esse método para especificar a paleta de cores usadas na imagem.</span><span class="sxs-lookup"><span data-stu-id="356f1-184">If an image uses an indexed format, use this method to specify the palette of colors used in the image.</span></span> <span data-ttu-id="356f1-185">Se o seu codec não tiver um formato indexado, retorne WINCODEC \_ Err \_ PALETTEUNAVAILABLE a partir desse método.</span><span class="sxs-lookup"><span data-stu-id="356f1-185">If your codec doesn’t have an indexed format, return WINCODEC\_ERR\_PALETTEUNAVAILABLE from this method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="356f1-186">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="356f1-186">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="356f1-187">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="356f1-187">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="356f1-188">Implementando IWICBitmapCodecProgressNotification (codificador)</span><span class="sxs-lookup"><span data-stu-id="356f1-188">Implementing IWICBitmapCodecProgressNotification (Encoder)</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)
</dt> <dt>

[<span data-ttu-id="356f1-189">Implementando IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="356f1-189">Implementing IWICMetadataBlockWriter</span></span>](-wic-imp-iwicmetadatablockwriter.md)
</dt> <dt>

[<span data-ttu-id="356f1-190">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="356f1-190">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="356f1-191">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="356f1-191">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 

---
description: Implementando IWICBitmapDecoder
ms.assetid: 9e316bdd-803a-47af-b004-7675478eb829
title: Implementando IWICBitmapDecoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b31bca377828606fe1beb68d6f1d95d290e01407
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011091"
---
# <a name="implementing-iwicbitmapdecoder"></a><span data-ttu-id="339b5-103">Implementando IWICBitmapDecoder</span><span class="sxs-lookup"><span data-stu-id="339b5-103">Implementing IWICBitmapDecoder</span></span>

## <a name="iwicbitmapdecoder"></a><span data-ttu-id="339b5-104">IWICBitmapDecoder</span><span class="sxs-lookup"><span data-stu-id="339b5-104">IWICBitmapDecoder</span></span>

<span data-ttu-id="339b5-105">Quando um aplicativo solicita um decodificador, o primeiro ponto de interação com o codec é por meio da interface [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="339b5-105">When an application requests a decoder, the first point of interaction with the codec is through the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) interface.</span></span> <span data-ttu-id="339b5-106">Essa é a interface de nível de contêiner que fornece acesso às propriedades de nível superior do contêiner e, o mais importante, os quadros que ele contém.</span><span class="sxs-lookup"><span data-stu-id="339b5-106">This is the container-level interface that provides access to the top-level properties of the container and, most importantly, the frames it contains.</span></span> <span data-ttu-id="339b5-107">Essa é a interface principal em sua classe de decodificador de nível de contêiner.</span><span class="sxs-lookup"><span data-stu-id="339b5-107">This is the primary interface on your container-level decoder class.</span></span>

``` syntax
interface IWICBitmapDecoder : IUnknown
{
// Required methods
   HRESULT QueryCapability (IStream *pIStream, 
      DWORD *pdwCapabilities );
   HRESULT Initialize ( IStream *pIStream,
      WICDecodeOptions cacheOptions );
   HRESULT GetContainerFormat ( GUID *pguidContainerFormat );
   HRESULT GetDecoderInfo ( IWICBitmapDecoderInfo **pIDecoderInfo );
   HRESULT GetFrameCount ( UINT *pCount );
   HRESULT GetFrame ( UINT index, 
      IWICBitmapFrameDecode **ppIBitmapFrame );

// Optional methods
   HRESULT GetPreview ( IWICBitmapSource **ppIPreview );
   HRESULT GetThumbnail ( IWICBitmapSource **ppIThumbnail );
   HRESULT GetColorContexts ( UINT cCount, 
      IWICColorContext **ppIColorContexts, 
      UINT *pcActualCount );
   HRESULT GetMetadataQueryReader ( IWICMetadataQueryReader **ppIMetadataQueryReader);
   HRESULT CopyPalette ( IWICPalette *pIPalette );
}
```

<span data-ttu-id="339b5-108">Alguns formatos de imagem têm miniaturas globais, contextos de cor ou metadados, enquanto muitos formatos de imagem só fornecem isso por quadro.</span><span class="sxs-lookup"><span data-stu-id="339b5-108">Some image formats have global thumbnails, color contexts, or metadata, while many image formats provide these only on a per-frame basis.</span></span> <span data-ttu-id="339b5-109">Os métodos para acessar esses itens são opcionais em [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder), mas são necessários em [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode).</span><span class="sxs-lookup"><span data-stu-id="339b5-109">The methods for accessing these items are optional on [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder), but are required on [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode).</span></span> <span data-ttu-id="339b5-110">Da mesma forma, alguns codecs não usam formatos de pixel indexados e, portanto, não precisam implementar os métodos [CopyPalette](-wic-imp-iwicbitmapframedecode.md) em nenhuma das interfaces.</span><span class="sxs-lookup"><span data-stu-id="339b5-110">Likewise, some codecs do not use indexed pixel formats and so do not need to implement the [CopyPalette](-wic-imp-iwicbitmapframedecode.md) methods on either interface.</span></span> <span data-ttu-id="339b5-111">Para obter mais informações sobre os métodos **IWICBitmapDecoder** opcionais, consulte [implementando IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md), onde eles são mais comumente implementados.</span><span class="sxs-lookup"><span data-stu-id="339b5-111">For more information on the optional **IWICBitmapDecoder** methods, see [Implementing IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md), where they are most commonly implemented.</span></span>

### <a name="querycapability"></a><span data-ttu-id="339b5-112">QueryCapability</span><span class="sxs-lookup"><span data-stu-id="339b5-112">QueryCapability</span></span>

<span data-ttu-id="339b5-113">[**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) é o método usado para arbitragem de codec.</span><span class="sxs-lookup"><span data-stu-id="339b5-113">[**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) is the method used for codec arbitration.</span></span> <span data-ttu-id="339b5-114">(Consulte [descoberta e arbitragem](-wic-howwicworks.md) no tópico [como o componente do Windows Imaging Component funciona](-wic-howwicworks.md) ).</span><span class="sxs-lookup"><span data-stu-id="339b5-114">(See [Discovery and Arbitration](-wic-howwicworks.md) in the [How The Windows Imaging Component Works](-wic-howwicworks.md) topic).</span></span> <span data-ttu-id="339b5-115">Se dois codecs forem capazes de decodificar o mesmo formato de imagem, ou se ocorrer uma colisão de padrão em que dois codecs usem o mesmo padrão de identificação, esse método permitirá que você selecione o codec que pode lidar melhor com qualquer imagem específica.</span><span class="sxs-lookup"><span data-stu-id="339b5-115">If two codecs are capable of decoding the same image format, or if a pattern collision occurs in which two codecs use the same identifying pattern, this method allows you to select the codec that can best handle any specific image.</span></span>

<span data-ttu-id="339b5-116">Ao invocar esse método, o Windows Imaging Component (WIC) passa o fluxo real que contém a imagem.</span><span class="sxs-lookup"><span data-stu-id="339b5-116">When invoking this method, Windows Imaging Component (WIC) passes you the actual stream containing the image.</span></span> <span data-ttu-id="339b5-117">Você deve verificar se é possível decodificar cada quadro dentro da imagem e enumerar os blocos de metadados para declarar com precisão quais recursos esse decodificador tem em relação ao fluxo de arquivo específico passado para ele.</span><span class="sxs-lookup"><span data-stu-id="339b5-117">You must verify whether you can decode each frame within the image and enumerate through the metadata blocks, to accurately declare what capabilities this decoder has with respect to the specific file stream passed to it.</span></span> <span data-ttu-id="339b5-118">Isso é importante para todos os decodificadores, mas particularmente importante para formatos de imagem com base em contêineres TIFF (Tagged Image File Format).</span><span class="sxs-lookup"><span data-stu-id="339b5-118">This is important for all decoders, but particularly important for image formats based on Tagged Image File Format (TIFF) containers.</span></span> <span data-ttu-id="339b5-119">O processo de descoberta funciona por padrões correspondentes associados aos decodificadores no registro para padrões no arquivo de imagem real.</span><span class="sxs-lookup"><span data-stu-id="339b5-119">The discovery process works by matching patterns associated with decoders in the registry to patterns in the actual image file.</span></span> <span data-ttu-id="339b5-120">Declarar seu padrão de identificação no registro garante que seu decodificador sempre será detectado para imagens no seu formato de imagem.</span><span class="sxs-lookup"><span data-stu-id="339b5-120">Declaring your identifying pattern in the registry guarantees that your decoder will always be detected for images in your image format.</span></span> <span data-ttu-id="339b5-121">No entanto, seu decodificador ainda pode ser detectado para imagens em outros formatos.</span><span class="sxs-lookup"><span data-stu-id="339b5-121">However, your decoder could still be detected for images in other formats.</span></span> <span data-ttu-id="339b5-122">Por exemplo, todos os contêineres TIFF incluem o padrão TIFF, que é um padrão de identificação válido para o formato de imagem TIFF.</span><span class="sxs-lookup"><span data-stu-id="339b5-122">For example, all TIFF containers include the TIFF pattern, which is a valid identifying pattern for the TIFF image format.</span></span> <span data-ttu-id="339b5-123">Isso significa que, durante a descoberta, pelo menos dois padrões de identificação serão encontrados em arquivos de imagem para qualquer formato de imagem baseado em um contêiner de estilo TIFF.</span><span class="sxs-lookup"><span data-stu-id="339b5-123">This means that, during discovery, at least two identifying patterns will be found in image files for any image format that’s based on a TIFF-style container.</span></span> <span data-ttu-id="339b5-124">Um será o padrão TIFF e o outro será o padrão de formato de imagem real.</span><span class="sxs-lookup"><span data-stu-id="339b5-124">One will be the TIFF pattern and the other will be the actual image format pattern.</span></span> <span data-ttu-id="339b5-125">Embora menos provável, também pode haver colisões de padrões entre outros formatos de imagem não relacionados.</span><span class="sxs-lookup"><span data-stu-id="339b5-125">While less likely, there could be pattern collisions between other unrelated image formats as well.</span></span> <span data-ttu-id="339b5-126">É por isso que a descoberta e a arbitragem são um processo de duas etapas.</span><span class="sxs-lookup"><span data-stu-id="339b5-126">This is why discovery and arbitration is a two-stage process.</span></span> <span data-ttu-id="339b5-127">Sempre verifique se o fluxo de imagem passado para [**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) é, na verdade, uma instância válida do seu próprio formato de imagem.</span><span class="sxs-lookup"><span data-stu-id="339b5-127">Always verify that the image stream passed to [**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) is actually a valid instance of your own image format.</span></span> <span data-ttu-id="339b5-128">Além disso, se o codec decodificar um formato de imagem para o qual você não possui a especificação, sua implementação de **QueryCapability** deverá verificar a presença de qualquer recurso que possa ser válido na especificação de formato de imagem que o codec não implementa.</span><span class="sxs-lookup"><span data-stu-id="339b5-128">Also, if your codec decodes an image format for which you don’t own the specification, your **QueryCapability** implementation should check for the presence of any feature that may be valid under the image format specification that your codec doesn’t implement.</span></span> <span data-ttu-id="339b5-129">Isso garantirá que os usuários não tenham falhas de decodificação desnecessárias ou obtenham resultados inesperados com seu codec.</span><span class="sxs-lookup"><span data-stu-id="339b5-129">This will ensure that users do not experience unnecessary decoding failures or get unexpected results with your codec.</span></span>

<span data-ttu-id="339b5-130">Antes de executar qualquer operação na imagem, você deve salvar a posição atual do fluxo, para que possa restaurá-la para sua posição original antes de retornar do método.</span><span class="sxs-lookup"><span data-stu-id="339b5-130">Before performing any operation on the image, you must save the current position of the stream, so you can restore it to its original position before returning from the method.</span></span> <span data-ttu-id="339b5-131">A enumeração [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) que especifica os recursos é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="339b5-131">The [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) enumeration that specifies the capabilities is defined as follows:</span></span>

``` syntax
enum WICBitmapDecoderCapabilities
{   
   WICBitmapDecoderCapabilitySameEncoder,
   WICBitmapDecoderCapabilityCanDecodeAllImages,
   WICBitmapDecoderCapabilityCanDecodeSomeImages,
   WICBitmapDecoderCapabilityCanEnumerateMetadata,
   WICBitmapDecoderCapabilityCanDecodeThumbnail
}
```

<span data-ttu-id="339b5-132">Você deve declarar **WICBitmapDecoderCapabilitySameEncoder** somente se o codificador foi aquele que codificou a imagem.</span><span class="sxs-lookup"><span data-stu-id="339b5-132">You should declare **WICBitmapDecoderCapabilitySameEncoder** only if your encoder was the one that encoded the image.</span></span> <span data-ttu-id="339b5-133">Depois de verificar se você pode decodificar cada quadro no contêiner, declare **WICBitmapDecoderCapabilityCanDecodeSomeImages** se você puder decodificar alguns, mas não todos os quadros, **WICBitmapDecoderCapabilityCanDecodeAllImages** se você puder decodificar todos os quadros, ou nenhum deles, se não for possível decodificar nenhum deles.</span><span class="sxs-lookup"><span data-stu-id="339b5-133">After verifying whether you can decode each frame in the container, declare either **WICBitmapDecoderCapabilityCanDecodeSomeImages** if you can decode some but not all of the frames, **WICBitmapDecoderCapabilityCanDecodeAllImages** if you can decode all of the frames, or neither if you cannot decode any of them.</span></span> <span data-ttu-id="339b5-134">(Essas duas enumerações são mutuamente exclusivas; se você retornar **WICBitmapDecoderCapabilityCanDecodeAllImages**, **WICBitmapDecoderCapabilityCanDecodeSomeImages** será ignorado.) Declare **WICBitmapDecoderCapabilityCanEnumerateMetadata** depois de verificar se você pode enumerar os blocos de metadados no contêiner de imagem.</span><span class="sxs-lookup"><span data-stu-id="339b5-134">(These two enums are mutually exclusive; if you return **WICBitmapDecoderCapabilityCanDecodeAllImages**, **WICBitmapDecoderCapabilityCanDecodeSomeImages** will be ignored.) Declare **WICBitmapDecoderCapabilityCanEnumerateMetadata** after verifying that you can enumerate through the metadata blocks in the image container.</span></span> <span data-ttu-id="339b5-135">Você não precisa verificar uma miniatura em todos os quadros.</span><span class="sxs-lookup"><span data-stu-id="339b5-135">You don’t have to check for a thumbnail in every frame.</span></span> <span data-ttu-id="339b5-136">Se houver uma miniatura global e você puder decodificá-la, você poderá declarar **WICBitmapDecoderCapabilityCanDecodeThumbnail**.</span><span class="sxs-lookup"><span data-stu-id="339b5-136">If there is a global thumbnail and you can decode it, you can declare **WICBitmapDecoderCapabilityCanDecodeThumbnail**.</span></span> <span data-ttu-id="339b5-137">Se não houver uma miniatura global, tente decodificar a miniatura do quadro 0.</span><span class="sxs-lookup"><span data-stu-id="339b5-137">If there is no global thumbnail, then attempt to decode the thumbnail for Frame 0.</span></span> <span data-ttu-id="339b5-138">Se não houver nenhuma miniatura em nenhum desses locais, não declare esse recurso.</span><span class="sxs-lookup"><span data-stu-id="339b5-138">If there is no thumbnail in either of these places, do not declare this capability.</span></span>

<span data-ttu-id="339b5-139">Depois de determinar os recursos do decodificador em relação ao fluxo de imagem passado para esse método, execute uma operação OR com o [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) que você verificou que esse decodificador pode executar nessa imagem e retorne o resultado.</span><span class="sxs-lookup"><span data-stu-id="339b5-139">After determining the capabilities of the decoder with respect to the image stream passed to this method, perform an OR operation with the [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) you have verified that this decoder can perform on this image, and return the result.</span></span> <span data-ttu-id="339b5-140">Lembre-se de restaurar o fluxo para sua posição original antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="339b5-140">Remember to restore the stream to its original position before returning.</span></span>

### <a name="initialize"></a><span data-ttu-id="339b5-141">Inicializar</span><span class="sxs-lookup"><span data-stu-id="339b5-141">Initialize</span></span>

<span data-ttu-id="339b5-142">A [**inicialização**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize) é invocada por um aplicativo após a seleção de um decodificador para decodificar uma imagem específica.</span><span class="sxs-lookup"><span data-stu-id="339b5-142">[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize) is invoked by an application after a decoder has been selected to decode a specific image.</span></span> <span data-ttu-id="339b5-143">O fluxo de imagem é passado para o decodificador, e um chamador pode opcionalmente especificar a opção de cache [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) para lidar com os metadados no arquivo.</span><span class="sxs-lookup"><span data-stu-id="339b5-143">The image stream is passed to the decoder, and a caller may optionally specify the [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) cache option for dealing with the metadata in the file.</span></span>

``` syntax
enum WICDecodeOptions
{
   WICDecodeMetadataCacheOnDemand,
   WICDecodeMetadataCacheOnLoad
}
```

<span data-ttu-id="339b5-144">Alguns aplicativos usam metadados mais do que outros.</span><span class="sxs-lookup"><span data-stu-id="339b5-144">Some applications use metadata more than others.</span></span> <span data-ttu-id="339b5-145">A maioria dos aplicativos não precisa acessar todos os metadados em um arquivo de imagem e solicitará metadados específicos conforme eles precisarem.</span><span class="sxs-lookup"><span data-stu-id="339b5-145">Most applications don’t need to access all the metadata in an image file, and will request specific metadata as they need it.</span></span> <span data-ttu-id="339b5-146">Outros aplicativos, em vez disso, armazenariam em cache todos os metadados antecipadamente que mantêm o fluxo de arquivos aberto e executam e/s de disco toda vez que precisam acessar metadados.</span><span class="sxs-lookup"><span data-stu-id="339b5-146">Other applications would rather cache all the metadata up front than keep the file stream open and perform disk I/O every time they need to access metadata.</span></span> <span data-ttu-id="339b5-147">Se o chamador não especificar uma opção de cache de metadados, o comportamento de cache padrão deverá ser o cache sob demanda.</span><span class="sxs-lookup"><span data-stu-id="339b5-147">If the caller doesn’t specify a metadata cache option, the default caching behavior should be cache on demand.</span></span> <span data-ttu-id="339b5-148">Isso significa que nenhum metadado deve ser carregado na memória até que o aplicativo faça uma solicitação específica para esses metadados.</span><span class="sxs-lookup"><span data-stu-id="339b5-148">This means no metadata should be loaded into memory until the application makes a specific request for that metadata.</span></span> <span data-ttu-id="339b5-149">Se o aplicativo especificar **WICDecodeMetadataCacheOnLoad**, os metadados deverão ser carregados na memória imediatamente e armazenados em cache.</span><span class="sxs-lookup"><span data-stu-id="339b5-149">If the application specifies **WICDecodeMetadataCacheOnLoad**, the metadata should be loaded in memory immediately and cached.</span></span> <span data-ttu-id="339b5-150">Quando os metadados são armazenados em cache no carregamento, o fluxo de arquivos pode ser liberado depois que os metadados são armazenados em cache.</span><span class="sxs-lookup"><span data-stu-id="339b5-150">When metadata is cached on load, the file stream may be released after the metadata has been cached.</span></span>

### <a name="getcontainerformat"></a><span data-ttu-id="339b5-151">GetContainerFormat</span><span class="sxs-lookup"><span data-stu-id="339b5-151">GetContainerFormat</span></span>

<span data-ttu-id="339b5-152">Para implementar [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat), basta retornar o GUID do formato de imagem da imagem para a qual o decodificador é instanciado.</span><span class="sxs-lookup"><span data-stu-id="339b5-152">To implement [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat), just return the GUID of the image format of the image for which the decoder is instantiated.</span></span> <span data-ttu-id="339b5-153">Esse método também é implementado em [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) e [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder).</span><span class="sxs-lookup"><span data-stu-id="339b5-153">This method is also implemented on [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) and [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder).</span></span>

### <a name="getdecoderinfo"></a><span data-ttu-id="339b5-154">GetDecoderInfo</span><span class="sxs-lookup"><span data-stu-id="339b5-154">GetDecoderInfo</span></span>

<span data-ttu-id="339b5-155">[**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) retorna um objeto [**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo) .</span><span class="sxs-lookup"><span data-stu-id="339b5-155">[**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) returns an [**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo) object.</span></span> <span data-ttu-id="339b5-156">Para obter o objeto **IWICBitmapDecoderInfo** , basta passar o GUID do decodificador para o método [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) em [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)e, em seguida, solicitar a interface **IWICBitmapDecoderInfo** nele, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="339b5-156">To get the **IWICBitmapDecoderInfo** object, just pass the GUID of your decoder to the [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) method on [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), and then request the **IWICBitmapDecoderInfo** interface on it, as shown in the following example.</span></span>


```C++
IWICComponentInfo* pComponentInfo = NULL;
HRESULT hr;
 
hr = m_pImagingFactory->CreateComponentInfo(CLSID_This, &pComponentInfo);

hr = pComponentInfo->QueryInterface(IID_IWICBitmapDecoderInfo, (void**)ppIDecoderInfo);

```



### <a name="getframecount"></a><span data-ttu-id="339b5-157">GetFrameCount</span><span class="sxs-lookup"><span data-stu-id="339b5-157">GetFrameCount</span></span>

<span data-ttu-id="339b5-158">[**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) retorna apenas o número de quadros no contêiner.</span><span class="sxs-lookup"><span data-stu-id="339b5-158">[**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) just returns the number of frames in the container.</span></span> <span data-ttu-id="339b5-159">Alguns formatos de contêiner dão suporte a vários quadros e outros dão suporte a apenas um quadro por contêiner.</span><span class="sxs-lookup"><span data-stu-id="339b5-159">Some container formats support multiple frames, and others support only one frame per container.</span></span>

### <a name="getframe"></a><span data-ttu-id="339b5-160">GetFrame</span><span class="sxs-lookup"><span data-stu-id="339b5-160">GetFrame</span></span>

<span data-ttu-id="339b5-161">[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) é um método importante na interface [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) porque o quadro contém os bits de imagem reais, e o objeto decodificador de quadro retornado desse método é o objeto que faz a decodificação real da imagem solicitada.</span><span class="sxs-lookup"><span data-stu-id="339b5-161">[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) is an important method on the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) interface because the frame contains the actual image bits, and the frame decoder object returned from this method is the object that does the actual decoding of the requested image.</span></span> <span data-ttu-id="339b5-162">Esse é o outro objeto que você precisa implementar ao escrever um decodificador.</span><span class="sxs-lookup"><span data-stu-id="339b5-162">That is the other object you need to implement when writing a decoder.</span></span> <span data-ttu-id="339b5-163">Para obter mais informações sobre decodificadores de quadros, consulte [implementando IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md).</span><span class="sxs-lookup"><span data-stu-id="339b5-163">For more information on frame decoders, see [Implementing IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md).</span></span>

### <a name="getpreview"></a><span data-ttu-id="339b5-164">GetPreview</span><span class="sxs-lookup"><span data-stu-id="339b5-164">GetPreview</span></span>

<span data-ttu-id="339b5-165">[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) retorna uma visualização da imagem.</span><span class="sxs-lookup"><span data-stu-id="339b5-165">[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) returns a preview of the image.</span></span> <span data-ttu-id="339b5-166">Para obter uma discussão detalhada sobre visualizações, consulte o método [implementando IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md) na interface de [implementação IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md) .</span><span class="sxs-lookup"><span data-stu-id="339b5-166">For a detailed discussion of previews, see the [Implementing IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md) method on the [Implementing IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md) interface.</span></span>

<span data-ttu-id="339b5-167">Se o formato de imagem contiver uma visualização JPEG incorporada, é altamente recomendável que, em vez de gravar um decodificador de JPEG para decodificá-lo, você delegue ao decodificador de JPEG que é fornecido com a plataforma WIC para decodificar visualizações e miniaturas.</span><span class="sxs-lookup"><span data-stu-id="339b5-167">If your image format contains an embedded JPEG preview, it is strongly recommend that, instead of writing a JPEG decoder to decode it, you delegate to the JPEG decoder that ships with the WIC platform for decoding previews and thumbnails.</span></span> <span data-ttu-id="339b5-168">Para fazer isso, procure o início dos dados da imagem de visualização no fluxo e invoque o método [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) no [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span><span class="sxs-lookup"><span data-stu-id="339b5-168">To do this, seek to the beginning of the preview image data in the stream and invoke the [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) method on the [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span></span>


```C++
IWICBitmapDecoder* pPreviewDecoder = NULL;
IWICBitmapFrameDecode* pPreviewFrame = NULL;
IWICBitmapSource* pPreview = NULL;
HRESULT hr;

hr = m_pImagingFactory->CreateDecoderFromStream(
                               m_pStream, NULL, 
                               WICDecodeMetadataCacheOnDemand, &pPreviewDecoder);
hr = pPreviewDecoder->GetFrame(0, pPreviewFrame);
hr = pPreviewFrame->QueryInterface(IID_IWICBitmapSource, (void**)&pPreview);

```



## <a name="related-topics"></a><span data-ttu-id="339b5-169">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="339b5-169">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="339b5-170">**Referência**</span><span class="sxs-lookup"><span data-stu-id="339b5-170">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="339b5-171">**IWICBitmapDecoder**</span><span class="sxs-lookup"><span data-stu-id="339b5-171">**IWICBitmapDecoder**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[<span data-ttu-id="339b5-172">**IWICBitmapFrameDecode**</span><span class="sxs-lookup"><span data-stu-id="339b5-172">**IWICBitmapFrameDecode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

<span data-ttu-id="339b5-173">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="339b5-173">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="339b5-174">Interfaces do decodificador</span><span class="sxs-lookup"><span data-stu-id="339b5-174">Decoder Interfaces</span></span>](-wic-decoderinterfaces.md)
</dt> <dt>

[<span data-ttu-id="339b5-175">Implementando IWICBitmapCodecProgressNotification (decodificador)</span><span class="sxs-lookup"><span data-stu-id="339b5-175">Implementing IWICBitmapCodecProgressNotification (Decoder)</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> <dt>

[<span data-ttu-id="339b5-176">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="339b5-176">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="339b5-177">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="339b5-177">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 




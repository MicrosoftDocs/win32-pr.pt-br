---
description: Um codificador grava dados de imagem em um fluxo. Os codificadores podem compactar, criptografar e alterar os pixels da imagem de várias maneiras antes de gravá-los no fluxo.
ms.assetid: e1e3a9d9-209b-46a6-92da-5570476507cf
title: Visão geral da codificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be46aa73082071deb69fdd402f42866b18ef0aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171526"
---
# <a name="encoding-overview"></a><span data-ttu-id="237a5-104">Visão geral da codificação</span><span class="sxs-lookup"><span data-stu-id="237a5-104">Encoding Overview</span></span>

<span data-ttu-id="237a5-105">Um codificador grava dados de imagem em um fluxo.</span><span class="sxs-lookup"><span data-stu-id="237a5-105">An encoder writes image data to a stream.</span></span> <span data-ttu-id="237a5-106">Os codificadores podem compactar, criptografar e alterar os pixels da imagem de várias maneiras antes de gravá-los no fluxo.</span><span class="sxs-lookup"><span data-stu-id="237a5-106">Encoders can compress, encrypt, and alter the image pixels in a number of ways prior to writing them to the stream.</span></span> <span data-ttu-id="237a5-107">O uso de alguns codificadores resulta em compensações — por exemplo, JPEG, que compensa informações de cores para uma melhor compactação.</span><span class="sxs-lookup"><span data-stu-id="237a5-107">Using some encoders results in tradeoffs—for example, JPEG, which trades off color information for better compression.</span></span> <span data-ttu-id="237a5-108">Outros codificadores não resultam em tais perdas — por exemplo, bitmap (BMP).</span><span class="sxs-lookup"><span data-stu-id="237a5-108">Other encoders do not result in such losses—for example, bitmap (BMP).</span></span> <span data-ttu-id="237a5-109">Como muitos codecs usam tecnologia proprietária para obter melhor compactação e fidelidade de imagem, os detalhes sobre como uma imagem é codificada são até o desenvolvedor do codec.</span><span class="sxs-lookup"><span data-stu-id="237a5-109">Because many codecs use proprietary technology to achieve better compression and image fidelity, the details on how an image gets encoded are up to the codec developer.</span></span>

<span data-ttu-id="237a5-110">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="237a5-110">This topic includes the following sections.</span></span>

-   [<span data-ttu-id="237a5-111">IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="237a5-111">IWICBitmapEncoder</span></span>](#iwicbitmapencoder)
-   [<span data-ttu-id="237a5-112">IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="237a5-112">IWICBitmapFrameEncode</span></span>](#iwicbitmapframeencode)
-   [<span data-ttu-id="237a5-113">Exemplo de codificação TIFF</span><span class="sxs-lookup"><span data-stu-id="237a5-113">TIFF Encoding Example</span></span>](#tiff-encoding-example)
-   [<span data-ttu-id="237a5-114">Uso de opções de codificador</span><span class="sxs-lookup"><span data-stu-id="237a5-114">Encoder Options Usage</span></span>](#encoder-options-usage)
-   [<span data-ttu-id="237a5-115">Opções de codificador</span><span class="sxs-lookup"><span data-stu-id="237a5-115">Encoder Options</span></span>](#encoder-options-usage)
-   [<span data-ttu-id="237a5-116">Exemplos de opções de codificador</span><span class="sxs-lookup"><span data-stu-id="237a5-116">Encoder Options Examples</span></span>](#encoder-options-examples)
-   [<span data-ttu-id="237a5-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="237a5-117">Related topics</span></span>](#related-topics)

## <a name="iwicbitmapencoder"></a><span data-ttu-id="237a5-118">IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="237a5-118">IWICBitmapEncoder</span></span>

<span data-ttu-id="237a5-119">[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) é a interface principal para codificar uma imagem para o formato de destino e usada para serializar os componentes de uma imagem, como miniatura ([**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)) e frames ([**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)), para o arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="237a5-119">[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) is the main interface for encoding an image to the target format and used to serialize an image's components, such as thumbnail ([**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)) and frames ([**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)), to the image file.</span></span>

<span data-ttu-id="237a5-120">Como e quando a serialização ocorre é deixada para o desenvolvedor do codec.</span><span class="sxs-lookup"><span data-stu-id="237a5-120">How and when serialization occurs is left up to the codec developer.</span></span> <span data-ttu-id="237a5-121">Cada bloco de dados individual no formato de arquivo de destino deve ser capaz de definir independentemente da ordem, mas novamente, essa é a decisão do desenvolvedor do codec.</span><span class="sxs-lookup"><span data-stu-id="237a5-121">Each individual block of data within the target file format should be able to set independent of order, but again, this is the codec developer's decision.</span></span> <span data-ttu-id="237a5-122">Quando o método [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) é chamado no entanto, as alterações na imagem não devem ser permitidas e o fluxo deve ser fechado.</span><span class="sxs-lookup"><span data-stu-id="237a5-122">Once the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) method is called however, changes to the image should not be allowed and the stream should be closed.</span></span>

## <a name="iwicbitmapframeencode"></a><span data-ttu-id="237a5-123">IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="237a5-123">IWICBitmapFrameEncode</span></span>

<span data-ttu-id="237a5-124">[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) é a interface para codificar os quadros individuais de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="237a5-124">[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) is the interface for encoding the individual frames of an image.</span></span> <span data-ttu-id="237a5-125">Ele fornece métodos para definir componentes individuais de imagem de quadro, como miniaturas e quadros, bem como dimensões de imagem, DPI e formatos de pixel.</span><span class="sxs-lookup"><span data-stu-id="237a5-125">It provides methods for setting individual frame imaging components, such as thumbnails and frames, as well as image dimensions, DPI, and pixel formats.</span></span>

<span data-ttu-id="237a5-126">Quadros individuais podem ser codificados com metadados específicos do quadro para que o [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) forneça acesso a um gravador de metadados por meio do método [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="237a5-126">Individual frames may be encoded with frame-specific metadata so [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) provides access to a metadata writer through the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) method.</span></span>

<span data-ttu-id="237a5-127">O método [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) do quadro confirma todas as alterações no quadro individual e indica que as alterações feitas nesse quadro não devem mais ser aceitas.</span><span class="sxs-lookup"><span data-stu-id="237a5-127">The frame's [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) method commits all changes to the individual frame and indicates that changes to that frame should no longer be accepted.</span></span>

## <a name="tiff-encoding-example"></a><span data-ttu-id="237a5-128">Exemplo de codificação TIFF</span><span class="sxs-lookup"><span data-stu-id="237a5-128">TIFF Encoding Example</span></span>

<span data-ttu-id="237a5-129">No exemplo a seguir, uma imagem TIFF (Tagged Image File Format) é codificada usando [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) e um [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode).</span><span class="sxs-lookup"><span data-stu-id="237a5-129">In the following example, a Tagged Image File Format (TIFF) image is encoded using [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) and an [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode).</span></span> <span data-ttu-id="237a5-130">A saída TIFF é personalizada usando o [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) e o quadro de bitmap é inicializado usando as opções fornecidas.</span><span class="sxs-lookup"><span data-stu-id="237a5-130">The TIFF output is customized using the [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) and the bitmap frame is initialized using the given options.</span></span> <span data-ttu-id="237a5-131">Depois que a imagem tiver sido criada usando [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels), o quadro será confirmado por meio de [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) e a imagem será salva usando [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit).</span><span class="sxs-lookup"><span data-stu-id="237a5-131">Once the image has been created using [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels), the frame is committed by way of [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) and the image is saved using [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit).</span></span>


```C++
IWICImagingFactory *piFactory = NULL;
IWICBitmapEncoder *piEncoder = NULL;
IWICBitmapFrameEncode *piBitmapFrame = NULL;
IPropertyBag2 *pPropertybag = NULL;

IWICStream *piStream = NULL;
UINT uiWidth = 640;
UINT uiHeight = 480;

HRESULT hr = CoCreateInstance(
                CLSID_WICImagingFactory,
                NULL,
                CLSCTX_INPROC_SERVER,
                IID_IWICImagingFactory,
                (LPVOID*) &piFactory);

if (SUCCEEDED(hr))
{
    hr = piFactory->CreateStream(&piStream);
}

if (SUCCEEDED(hr))
{
    hr = piStream->InitializeFromFilename(L"output.tif", GENERIC_WRITE);
}

if (SUCCEEDED(hr))
{
   hr = piFactory->CreateEncoder(GUID_ContainerFormatTiff, NULL, &piEncoder);
}

if (SUCCEEDED(hr))
{
    hr = piEncoder->Initialize(piStream, WICBitmapEncoderNoCache);
}

if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // This is how you customize the TIFF output.
    PROPBAG2 option = { 0 };
    option.pstrName = L"TiffCompressionMethod";
    VARIANT varValue;    
    VariantInit(&varValue);
    varValue.vt = VT_UI1;
    varValue.bVal = WICTiffCompressionZIP;      
    hr = pPropertybag->Write(1, &option, &varValue);        
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}

if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->SetSize(uiWidth, uiHeight);
}

WICPixelFormatGUID formatGUID = GUID_WICPixelFormat24bppBGR;
if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->SetPixelFormat(&formatGUID);
}

if (SUCCEEDED(hr))
{
    // We're expecting to write out 24bppRGB. Fail if the encoder cannot do it.
    hr = IsEqualGUID(formatGUID, GUID_WICPixelFormat24bppBGR) ? S_OK : E_FAIL;
}

if (SUCCEEDED(hr))
{
    UINT cbStride = (uiWidth * 24 + 7)/8/***WICGetStride**_/;
    UINT cbBufferSize = uiHeight _ cbStride;

    BYTE *pbBuffer = new BYTE[cbBufferSize];

    if (pbBuffer != NULL)
    {
        for (UINT i = 0; i < cbBufferSize; i++)
        {
            pbBuffer[i] = static_cast<BYTE>(rand());
        }

        hr = piBitmapFrame->WritePixels(uiHeight, cbStride, cbBufferSize, pbBuffer);

        delete[] pbBuffer;
    }
    else
    {
        hr = E_OUTOFMEMORY;
    }
}

if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->Commit();
}    

if (SUCCEEDED(hr))
{
    hr = piEncoder->Commit();
}

if (piFactory)
    piFactory->Release();

if (piEncoder)
    piEncoder->Release();

if (piBitmapFrame)
    piBitmapFrame->Release();

if (pPropertybag)
    pPropertybag->Release();

if (piStream)
    piStream->Release();

return hr;
```



## <a name="encoder-options-usage"></a><span data-ttu-id="237a5-132">Uso de opções de codificador</span><span class="sxs-lookup"><span data-stu-id="237a5-132">Encoder Options Usage</span></span>

<span data-ttu-id="237a5-133">Codificadores diferentes para formatos diferentes precisam expor opções diferentes para a forma como uma imagem é codificado.</span><span class="sxs-lookup"><span data-stu-id="237a5-133">Different encoders for different formats need to expose different options for how an image is encoded.</span></span> <span data-ttu-id="237a5-134">O Windows Imaging Component (WIC) fornece um mecanismo consistente para expressar se as opções de codificação são necessárias e, ao mesmo tempo, permitir que os aplicativos funcionem com vários codificadores sem a necessidade de conhecimento de um formato específico.</span><span class="sxs-lookup"><span data-stu-id="237a5-134">Windows Imaging Component (WIC) provides a consistent mechanism for expressing whether encoding options are required while still enabling applications to work with multiple encoders without requiring knowledge of a particular format.</span></span> <span data-ttu-id="237a5-135">Isso é feito fornecendo um parâmetro [IPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)) no método [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) e o método [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) .</span><span class="sxs-lookup"><span data-stu-id="237a5-135">This is accomplished by providing an [IPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)) parameter on the [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) method and the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) method.</span></span>

<span data-ttu-id="237a5-136">A fábrica de componentes fornece um ponto de criação fácil para a criação de um recipiente de propriedades de opções de codificador.</span><span class="sxs-lookup"><span data-stu-id="237a5-136">The component factory provides an easy creation point for creating an encoder options property bag.</span></span> <span data-ttu-id="237a5-137">Os codecs podem usar esse serviço se precisarem fornecer um conjunto simples, intuitivo e não conflitante de opções de codificador.</span><span class="sxs-lookup"><span data-stu-id="237a5-137">Codecs can use this service if they need to provide a simple, intuitive and non-conflicting set of encoder options.</span></span> <span data-ttu-id="237a5-138">O recipiente de propriedades de geração de imagens deve ser inicializado durante a criação com todas as opções de codificador relevantes para esse codec.</span><span class="sxs-lookup"><span data-stu-id="237a5-138">The imaging property bag must be initialized during creation with all the encoder options relevant to that codec.</span></span> <span data-ttu-id="237a5-139">Para as opções de codificador do conjunto canônico, o intervalo de valores será imposto na gravação.</span><span class="sxs-lookup"><span data-stu-id="237a5-139">For encoder options from the canonical set, the value range will be enforced on Write.</span></span> <span data-ttu-id="237a5-140">Para necessidades mais avançadas, os codecs devem gravar sua própria implementação do recipiente de propriedades.</span><span class="sxs-lookup"><span data-stu-id="237a5-140">For more advanced needs, codecs should write their own property bag implementation.</span></span>

<span data-ttu-id="237a5-141">Um aplicativo recebe o recipiente de opções do codificador durante a criação do quadro e deve configurar quaisquer valores antes de inicializar o quadro do codificador.</span><span class="sxs-lookup"><span data-stu-id="237a5-141">An application is given the encoder options bag during frame creation and must configure any values prior to initializing the encoder frame.</span></span> <span data-ttu-id="237a5-142">Para um aplicativo controlado por interface do usuário, ele pode oferecer uma interface do usuário fixa para as opções canônicas de codificador e uma exibição avançada para as opções restantes.</span><span class="sxs-lookup"><span data-stu-id="237a5-142">For a UI-driven application, it can offer a fixed UI for the canonical encoder options and an advanced view for remaining options.</span></span> <span data-ttu-id="237a5-143">As alterações podem ser feitas uma de cada vez por meio do método Write e qualquer erro será relatado por meio de IErrorLog.</span><span class="sxs-lookup"><span data-stu-id="237a5-143">Changes can be made one at a time through the Write method and any error will be reported through IErrorLog.</span></span> <span data-ttu-id="237a5-144">O aplicativo de interface do usuário sempre deve ler novamente e exibir todas as opções depois de fazer uma alteração caso a alteração tenha causado um efeito em cascata.</span><span class="sxs-lookup"><span data-stu-id="237a5-144">The UI application should always re-read and display all options after making a change in case the change caused a cascade effect.</span></span> <span data-ttu-id="237a5-145">Um aplicativo deve estar preparado para manipular a inicialização de quadro com falha para codecs que fornecem apenas relatórios de erros mínimos por meio de seu recipiente de propriedades.</span><span class="sxs-lookup"><span data-stu-id="237a5-145">An application should be prepared to handle failed frame initialization for codecs that only provide minimal error reporting through their property bag.</span></span>

## <a name="encoder-options"></a><span data-ttu-id="237a5-146">Opções de codificador</span><span class="sxs-lookup"><span data-stu-id="237a5-146">Encoder Options</span></span>

<span data-ttu-id="237a5-147">Um aplicativo pode esperar encontrar o seguinte conjunto de opções de codificador.</span><span class="sxs-lookup"><span data-stu-id="237a5-147">An application can expect to encounter the following set of encoder options.</span></span> <span data-ttu-id="237a5-148">As opções de codificador refletem os recursos de um codificador e o formato de contêiner subjacente e, portanto, por sua natureza não é realmente independente de codec.</span><span class="sxs-lookup"><span data-stu-id="237a5-148">Encoder options reflect the capabilities of an encoder and the underlying container format, and therefore are by their nature not really codec-agnostic.</span></span> <span data-ttu-id="237a5-149">Quando possível, as novas opções devem ser normalizadas para que possam ser aplicadas a novos codecs que surgirem.</span><span class="sxs-lookup"><span data-stu-id="237a5-149">When possible, new options should be normalized so they can be applied to new codecs that emerge.</span></span>



| <span data-ttu-id="237a5-150">Nome da Propriedade</span><span class="sxs-lookup"><span data-stu-id="237a5-150">Property Name</span></span>      | <span data-ttu-id="237a5-151">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="237a5-151">VARTYPE</span></span>  | <span data-ttu-id="237a5-152">Valor</span><span class="sxs-lookup"><span data-stu-id="237a5-152">Value</span></span>                                                                     | <span data-ttu-id="237a5-153">Codecs aplicáveis</span><span class="sxs-lookup"><span data-stu-id="237a5-153">Applicable Codecs</span></span> |
|--------------------|----------|---------------------------------------------------------------------------|-------------------|
| <span data-ttu-id="237a5-154">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="237a5-154">ImageQuality</span></span>       | <span data-ttu-id="237a5-155">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="237a5-155">VT\_R4</span></span>   | <span data-ttu-id="237a5-156">0-1,0</span><span class="sxs-lookup"><span data-stu-id="237a5-156">0-1.0</span></span>                                                                     | <span data-ttu-id="237a5-157">JPEG, HDPhoto</span><span class="sxs-lookup"><span data-stu-id="237a5-157">JPEG, HDPhoto</span></span>     |
| <span data-ttu-id="237a5-158">CompressionQuality</span><span class="sxs-lookup"><span data-stu-id="237a5-158">CompressionQuality</span></span> | <span data-ttu-id="237a5-159">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="237a5-159">VT\_R4</span></span>   | <span data-ttu-id="237a5-160">0-1,0</span><span class="sxs-lookup"><span data-stu-id="237a5-160">0-1.0</span></span>                                                                     | <span data-ttu-id="237a5-161">TIFF</span><span class="sxs-lookup"><span data-stu-id="237a5-161">TIFF</span></span>              |
| <span data-ttu-id="237a5-162">Lossless</span><span class="sxs-lookup"><span data-stu-id="237a5-162">Lossless</span></span>           | <span data-ttu-id="237a5-163">BOOL do VT \_</span><span class="sxs-lookup"><span data-stu-id="237a5-163">VT\_BOOL</span></span> | <span data-ttu-id="237a5-164">**verdadeiro**, **falso**</span><span class="sxs-lookup"><span data-stu-id="237a5-164">**TRUE**, **FALSE**</span></span>                                                       | <span data-ttu-id="237a5-165">HDPhoto</span><span class="sxs-lookup"><span data-stu-id="237a5-165">HDPhoto</span></span>           |
| <span data-ttu-id="237a5-166">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="237a5-166">BitmapTransform</span></span>    | <span data-ttu-id="237a5-167">\_UI1 VT</span><span class="sxs-lookup"><span data-stu-id="237a5-167">VT\_UI1</span></span>  | [<span data-ttu-id="237a5-168">**WICBitmapTransformOptions**</span><span class="sxs-lookup"><span data-stu-id="237a5-168">**WICBitmapTransformOptions**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | <span data-ttu-id="237a5-169">JPEG</span><span class="sxs-lookup"><span data-stu-id="237a5-169">JPEG</span></span>              |



 

<span data-ttu-id="237a5-170">ImageQualty de 0,0 significa a menor rendição de fidelidade possível e 1,0 significa a maior fidelidade, que também pode significar sem perdas dependendo do codec.</span><span class="sxs-lookup"><span data-stu-id="237a5-170">ImageQualty of 0.0 means the lowest possible fidelity rendition and 1.0 means the highest fidelity, which may also imply lossless depending on the codec.</span></span>

<span data-ttu-id="237a5-171">CompressionQuality de 0,0 significa o esquema de compactação menos eficiente disponível, normalmente resultando em uma codificação rápida, mas uma saída maior.</span><span class="sxs-lookup"><span data-stu-id="237a5-171">CompressionQuality of 0.0 means the least efficient compression scheme available, typically resulting in a fast encode but larger output.</span></span> <span data-ttu-id="237a5-172">Um valor de 1,0 significa o esquema mais eficiente disponível, normalmente demorando mais tempo para codificar, mas produzindo saída menor.</span><span class="sxs-lookup"><span data-stu-id="237a5-172">A value of 1.0 means the most efficient scheme available, typically taking more time to encode but producing smaller output.</span></span> <span data-ttu-id="237a5-173">Dependendo dos recursos do codec, esse intervalo pode ser mapeado para um conjunto discreto de métodos de compactação disponíveis.</span><span class="sxs-lookup"><span data-stu-id="237a5-173">Depending on the capabilities of the codec, this range may be mapped onto a discrete set of available compression methods.</span></span>

<span data-ttu-id="237a5-174">Sem perdas significa que o codec codifica a imagem como sem perdas, sem perda de dados de imagem.</span><span class="sxs-lookup"><span data-stu-id="237a5-174">Lossless means that the codec encodes the image as lossless with no image data loss.</span></span> <span data-ttu-id="237a5-175">Se o Lossless estiver habilitado, o ImageQuality será ignorado.</span><span class="sxs-lookup"><span data-stu-id="237a5-175">If Lossless is enabled, ImageQuality is ignored.</span></span>

<span data-ttu-id="237a5-176">Além das opções de codificador genérico acima, os codecs fornecidos com o WIC dão suporte às seguintes opções.</span><span class="sxs-lookup"><span data-stu-id="237a5-176">In addition to the above generic encoder options, codecs supplied with WIC support the following options.</span></span> <span data-ttu-id="237a5-177">Se um codec tiver a necessidade de oferecer suporte a uma opção consistente com o uso nesses codecs fornecidos, é recomendável fazer isso.</span><span class="sxs-lookup"><span data-stu-id="237a5-177">If a codec has a need to support an option that is consistent with the usage in these supplied codecs, it is encouraged to do so.</span></span>



| <span data-ttu-id="237a5-178">Nome da Propriedade</span><span class="sxs-lookup"><span data-stu-id="237a5-178">Property Name</span></span>           | <span data-ttu-id="237a5-179">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="237a5-179">VARTYPE</span></span>           | <span data-ttu-id="237a5-180">Valor</span><span class="sxs-lookup"><span data-stu-id="237a5-180">Value</span></span>                                                                             | <span data-ttu-id="237a5-181">Codecs aplicáveis</span><span class="sxs-lookup"><span data-stu-id="237a5-181">Applicable Codecs</span></span> |
|-------------------------|-------------------|-----------------------------------------------------------------------------------|-------------------|
| <span data-ttu-id="237a5-182">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="237a5-182">InterlaceOption</span></span>         | <span data-ttu-id="237a5-183">BOOL do VT \_</span><span class="sxs-lookup"><span data-stu-id="237a5-183">VT\_BOOL</span></span>          | <span data-ttu-id="237a5-184">Ativar/desativar</span><span class="sxs-lookup"><span data-stu-id="237a5-184">On/Off</span></span>                                                                            | <span data-ttu-id="237a5-185">PNG</span><span class="sxs-lookup"><span data-stu-id="237a5-185">PNG</span></span>               |
| <span data-ttu-id="237a5-186">FilterOption</span><span class="sxs-lookup"><span data-stu-id="237a5-186">FilterOption</span></span>            | <span data-ttu-id="237a5-187">\_UI1 VT</span><span class="sxs-lookup"><span data-stu-id="237a5-187">VT\_UI1</span></span>           | [<span data-ttu-id="237a5-188">**WICPngFilterOption**</span><span class="sxs-lookup"><span data-stu-id="237a5-188">**WICPngFilterOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption)                       | <span data-ttu-id="237a5-189">PNG</span><span class="sxs-lookup"><span data-stu-id="237a5-189">PNG</span></span>               |
| <span data-ttu-id="237a5-190">TiffCompressionMethod</span><span class="sxs-lookup"><span data-stu-id="237a5-190">TiffCompressionMethod</span></span>   | <span data-ttu-id="237a5-191">\_UI1 VT</span><span class="sxs-lookup"><span data-stu-id="237a5-191">VT\_UI1</span></span>           | [<span data-ttu-id="237a5-192">**WICTiffCompressionOption**</span><span class="sxs-lookup"><span data-stu-id="237a5-192">**WICTiffCompressionOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption)           | <span data-ttu-id="237a5-193">TIFF</span><span class="sxs-lookup"><span data-stu-id="237a5-193">TIFF</span></span>              |
| <span data-ttu-id="237a5-194">Luminância</span><span class="sxs-lookup"><span data-stu-id="237a5-194">Luminance</span></span>               | <span data-ttu-id="237a5-195">\_Matriz VT UI4/VT \_</span><span class="sxs-lookup"><span data-stu-id="237a5-195">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="237a5-196">64 entradas (DCT)</span><span class="sxs-lookup"><span data-stu-id="237a5-196">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="237a5-197">JPEG</span><span class="sxs-lookup"><span data-stu-id="237a5-197">JPEG</span></span>              |
| <span data-ttu-id="237a5-198">Crominância</span><span class="sxs-lookup"><span data-stu-id="237a5-198">Chrominance</span></span>             | <span data-ttu-id="237a5-199">\_Matriz VT UI4/VT \_</span><span class="sxs-lookup"><span data-stu-id="237a5-199">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="237a5-200">64 entradas (DCT)</span><span class="sxs-lookup"><span data-stu-id="237a5-200">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="237a5-201">JPEG</span><span class="sxs-lookup"><span data-stu-id="237a5-201">JPEG</span></span>              |
| <span data-ttu-id="237a5-202">JpegYCrCbSubsampling</span><span class="sxs-lookup"><span data-stu-id="237a5-202">JpegYCrCbSubsampling</span></span>    | <span data-ttu-id="237a5-203">\_UI1 VT</span><span class="sxs-lookup"><span data-stu-id="237a5-203">VT\_UI1</span></span>           | [<span data-ttu-id="237a5-204">**WICJpegYCrCbSubsamplingOption**</span><span class="sxs-lookup"><span data-stu-id="237a5-204">**WICJpegYCrCbSubsamplingOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | <span data-ttu-id="237a5-205">JPEG</span><span class="sxs-lookup"><span data-stu-id="237a5-205">JPEG</span></span>              |
| <span data-ttu-id="237a5-206">SuppressApp0</span><span class="sxs-lookup"><span data-stu-id="237a5-206">SuppressApp0</span></span>            | <span data-ttu-id="237a5-207">BOOL do VT \_</span><span class="sxs-lookup"><span data-stu-id="237a5-207">VT\_BOOL</span></span>          |                                                                                   | <span data-ttu-id="237a5-208">JPEG</span><span class="sxs-lookup"><span data-stu-id="237a5-208">JPEG</span></span>              |
| <span data-ttu-id="237a5-209">EnableV5Header32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="237a5-209">EnableV5Header32bppBGRA</span></span> | <span data-ttu-id="237a5-210">BOOL do VT \_</span><span class="sxs-lookup"><span data-stu-id="237a5-210">VT\_BOOL</span></span>          | <span data-ttu-id="237a5-211">Ativar/desativar</span><span class="sxs-lookup"><span data-stu-id="237a5-211">On/Off</span></span>                                                                            | <span data-ttu-id="237a5-212">BMP</span><span class="sxs-lookup"><span data-stu-id="237a5-212">BMP</span></span>               |



 

<span data-ttu-id="237a5-213">Use **VT \_ vazio** para indicar que **\* não \* está definido** como o padrão.</span><span class="sxs-lookup"><span data-stu-id="237a5-213">Use **VT\_EMPTY** to indicate **\*not set\*** as the default.</span></span> <span data-ttu-id="237a5-214">Se propriedades adicionais forem definidas, mas sem suporte, o codificador deverá ignorá-las; Isso permite que os aplicativos codifiquem menos lógica se desejam uma funcionalidade que pode ou não estar presente.</span><span class="sxs-lookup"><span data-stu-id="237a5-214">If additional properties are set but not supported, the encoder should ignore them; this allows applications to code less logic if they want a capability that may or may not be present.</span></span>

## <a name="encoder-options-examples"></a><span data-ttu-id="237a5-215">Exemplos de opções de codificador</span><span class="sxs-lookup"><span data-stu-id="237a5-215">Encoder Options Examples</span></span>

<span data-ttu-id="237a5-216">No [exemplo de codificação TIFF](#tiff-encoding-example) acima, uma opção de codificador específico é definida.</span><span class="sxs-lookup"><span data-stu-id="237a5-216">In the [TIFF Encoding Example](#tiff-encoding-example) above, a specific encoder option is set.</span></span> <span data-ttu-id="237a5-217">O membro *pstrName* da estrutura PROPBAG2 é definido como o nome de propriedade apropriado e a variante é definida como o VarType correspondente e o valor desejado — nesse caso, um membro da enumeração [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) .</span><span class="sxs-lookup"><span data-stu-id="237a5-217">The *pstrName* member of the PROPBAG2 structure is set to the appropriate property name, and the VARIANT is set to the corresponding VARTYPE and the desired value—in this case, a member of the [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) enumeration.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // This is how you customize the TIFF output.
    PROPBAG2 option = { 0 };
    option.pstrName = L"TiffCompressionMethod";
    VARIANT varValue;    
    VariantInit(&varValue);
    varValue.vt = VT_UI1;
    varValue.bVal = WICTiffCompressionZIP;      
    hr = pPropertybag->Write(1, &option, &varValue);        
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}
```



<span data-ttu-id="237a5-218">Para usar as opções de codificador padrão, basta inicializar o quadro de bitmap com o recipiente de propriedades retornado quando o quadro foi criado.</span><span class="sxs-lookup"><span data-stu-id="237a5-218">To use the default encoder options, simply initialize the bitmap frame with the property bag returned when the frame was created.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // Accept the default encoder options.
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}
```



<span data-ttu-id="237a5-219">Também é possível eliminar o recipiente de propriedades quando não há nenhuma opção de codificador sendo considerada.</span><span class="sxs-lookup"><span data-stu-id="237a5-219">It is also possible to eliminate the property bag when no encoder options are being considered.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, 0);
}

if (SUCCEEDED(hr))
{        
    // No encoder options.
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(0);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="237a5-220">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="237a5-220">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="237a5-221">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="237a5-221">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="237a5-222">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="237a5-222">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="237a5-223">Visão geral da decodificação</span><span class="sxs-lookup"><span data-stu-id="237a5-223">Decoding Overview</span></span>](-wic-creating-decoder.md)
</dt> <dt>

<span data-ttu-id="237a5-224">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="237a5-224">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="237a5-225">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="237a5-225">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 

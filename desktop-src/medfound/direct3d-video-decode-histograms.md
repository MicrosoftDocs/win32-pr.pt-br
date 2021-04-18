---
description: Este artigo contém diretrizes para gerar histogramas ao decodificar vídeo usando as APIs de vídeo do Direct3D 11 ou 12.
ms.assetid: ''
title: Histogramas de decodificação de vídeo Direct3D
ms.topic: article
ms.date: 08/19/2019
ms.openlocfilehash: 6e25abd39ba95b669c2d76ced5f825ea80c4e3c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812134"
---
# <a name="direct3d-video-decode-histograms"></a><span data-ttu-id="d4610-103">Histogramas de decodificação de vídeo Direct3D</span><span class="sxs-lookup"><span data-stu-id="d4610-103">Direct3D video decode histograms</span></span>

<span data-ttu-id="d4610-104">Este artigo contém diretrizes para gerar histogramas ao decodificar vídeo usando as APIs de vídeo do Direct3D 11 ou 12.</span><span class="sxs-lookup"><span data-stu-id="d4610-104">This article contains guidance for generating histograms while decoding video using Direct3D 11 or 12 video APIs.</span></span>

## <a name="checking-the-video-device-for-histogram-capabilities"></a><span data-ttu-id="d4610-105">Verificando o dispositivo de vídeo para recursos de histograma</span><span class="sxs-lookup"><span data-stu-id="d4610-105">Checking the video device for histogram capabilities</span></span>

<span data-ttu-id="d4610-106">Antes de tentar gerar histogramas, você deve verificar se o dispositivo de vídeo atual dá suporte ao recurso de histograma de decodificação de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d4610-106">Before attempting to generated histograms, you must check to see if the current video device supports the video decode histogram feature.</span></span>

### <a name="direct3d-12"></a><span data-ttu-id="d4610-107">Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="d4610-107">Direct3D 12</span></span>

<span data-ttu-id="d4610-108">Chame [ID3D12VideoDevice:: CheckFeatureSupport](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) para verificar os detalhes de suporte para operações de decodificação de vídeo do Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="d4610-108">Call [ID3D12VideoDevice::CheckFeatureSupport](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) to check for the support details for Direct3D 12 video decoding operations.</span></span> <span data-ttu-id="d4610-109">Passe o valor **D3D12_FEATURE_VIDEO_DECODE_HISTOGRAM** da enumeração [D3D12_FEATURE_VIDEO](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) para especificar que você está solicitando suporte para histogramas de decodificação de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d4610-109">Pass the **D3D12_FEATURE_VIDEO_DECODE_HISTOGRAM** value from the [D3D12_FEATURE_VIDEO](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) enumeration to specify that you are requesting support for video decode histograms.</span></span>

### <a name="direct3d-11"></a><span data-ttu-id="d4610-110">Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="d4610-110">Direct3D 11</span></span>

<span data-ttu-id="d4610-111">Chame [ID3D11VideoDevice2:: CheckFeatureSupport](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videodevice2-checkfeaturesupport) e transmita o valor **D3D11_FEATURE_VIDEO_DECODER_HISTOGRAM** da [D3D11_FEATURE_VIDEO](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_feature_video) para determinar se há suporte para histogramas para o dispositivo atual.</span><span class="sxs-lookup"><span data-stu-id="d4610-111">Call [ID3D11VideoDevice2::CheckFeatureSupport](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videodevice2-checkfeaturesupport) and pass in the **D3D11_FEATURE_VIDEO_DECODER_HISTOGRAM** value of the [D3D11_FEATURE_VIDEO](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_feature_video) to determine if histograms are supported for the current device.</span></span>

## <a name="enabling-histogram-during-decode"></a><span data-ttu-id="d4610-112">Habilitando o histograma durante a decodificação</span><span class="sxs-lookup"><span data-stu-id="d4610-112">Enabling histogram during decode</span></span>

<span data-ttu-id="d4610-113">A coleção de dados de histograma é habilitada pelo chamador fornecendo os buffers nos quais os dados de histograma são armazenados.</span><span class="sxs-lookup"><span data-stu-id="d4610-113">The collection of histogram data is enabled by the caller providing the buffers in which the histogram data is stored.</span></span>  <span data-ttu-id="d4610-114">Um buffer de saída de histograma nulo para um determinado componente indica que a coleção de histograma está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="d4610-114">A null histogram output buffer for a given component indicates that histogram collection is disabled.</span></span>

### <a name="direct3d-12"></a><span data-ttu-id="d4610-115">Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="d4610-115">Direct3D 12</span></span>

<span data-ttu-id="d4610-116">Para fornecer buffers de saída para receber dados de histograma usando o Direct3D 12, você deve criar sua lista de comandos de decodificação usando o método [ID3D12VideoDecodeCommandList1::D ecodeframe1](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist1-decodeframe1) .</span><span class="sxs-lookup"><span data-stu-id="d4610-116">In order to provide output buffers to receive histogram data using Direct3D 12, you should create your decode command list using the [ID3D12VideoDecodeCommandList1::DecodeFrame1](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist1-decodeframe1) method.</span></span> <span data-ttu-id="d4610-117">Esse método usa uma estrutura [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments1) como um argumento.</span><span class="sxs-lookup"><span data-stu-id="d4610-117">This method takes a [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments1) structure as an argument.</span></span> <span data-ttu-id="d4610-118">**D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1** tem um campo do tipo [D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_histogram), que permite especificar um [ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) no qual os dados do histograma são gerados.</span><span class="sxs-lookup"><span data-stu-id="d4610-118">**D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1** has a field of type [D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_histogram), which allows you to specify an [ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) into which histogram data is output.</span></span>

### <a name="direct3d-11"></a><span data-ttu-id="d4610-119">Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="d4610-119">Direct3D 11</span></span>

<span data-ttu-id="d4610-120">A interface [ID3D11VideoContext3](/windows/win32/api/d3d11_4/nn-d3d11_4-id3d11videocontext3) fornece o método [DecoderBeginFrame1](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videocontext3-decoderbeginframe1) , que permite que você forneça uma ou mais interfaces [ID3D11Buffer](/windows/win32/api/d3d11/nn-d3d11-id3d11buffer) nas quais os dados de histograma serão gerados.</span><span class="sxs-lookup"><span data-stu-id="d4610-120">The [ID3D11VideoContext3](/windows/win32/api/d3d11_4/nn-d3d11_4-id3d11videocontext3) interface provides the [DecoderBeginFrame1](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videocontext3-decoderbeginframe1) method, which allows you to provide one or more [ID3D11Buffer](/windows/win32/api/d3d11/nn-d3d11-id3d11buffer) interfaces into which the histogram data will be output.</span></span> <span data-ttu-id="d4610-121">O [D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_video_decoder_histogram_component) para especificar os componentes para os quais você deseja que os dados de histograma sejam gerados.</span><span class="sxs-lookup"><span data-stu-id="d4610-121">The [D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_video_decoder_histogram_component) to specify the components for which you want histogram data to be generated.</span></span>


## <a name="buffer-format"></a><span data-ttu-id="d4610-122">Formato de buffer</span><span class="sxs-lookup"><span data-stu-id="d4610-122">Buffer format</span></span>

<span data-ttu-id="d4610-123">A saída do histograma de decodificação é gravada em um buffer como um contador inteiro por componente.</span><span class="sxs-lookup"><span data-stu-id="d4610-123">The decode histogram output is written to a buffer as an integer counter per component.</span></span>  <span data-ttu-id="d4610-124">O formato do buffer é um valor de 32 bits por compartimento.</span><span class="sxs-lookup"><span data-stu-id="d4610-124">The buffer format is a 32-bit value per bin.</span></span>  <span data-ttu-id="d4610-125">Um dispositivo pode usar uma profundidade de bit de contador de inteiros menor que 32 bits, mas deve ser 16, 24 ou 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d4610-125">A device may use an integer counter bit depth that is smaller than 32 bits, but must be 16, 24, or 32 bits.</span></span>  <span data-ttu-id="d4610-126">Nesse caso, o valor do contador é armazenado nos bits inferiores e os bits não usados superiores são zero.</span><span class="sxs-lookup"><span data-stu-id="d4610-126">If so, the counter value is stored in the lower bits and the upper unused bits are zero.</span></span>  <span data-ttu-id="d4610-127">Quando a contagem de um compartimento exceder o valor máximo, o dispositivo definirá o valor máximo em vez disso.</span><span class="sxs-lookup"><span data-stu-id="d4610-127">When the count for a bin would exceed the max value, the device sets the max value instead.</span></span> <span data-ttu-id="d4610-128">Dispositivos relatam o número de compartimentos com suporte, que deve ser um valor que seja uma potência de 2.</span><span class="sxs-lookup"><span data-stu-id="d4610-128">Devices report the number of bins supported, which must be a value that is a power of 2.</span></span>  <span data-ttu-id="d4610-129">O número mínimo de compartimentos necessário para dispositivos que dão suporte a esse recurso é 64.</span><span class="sxs-lookup"><span data-stu-id="d4610-129">The minimum number of bins required for devices that support this feature is 64.</span></span> 

<span data-ttu-id="d4610-130">Você deve fornecer um buffer com um deslocamento alinhado de 256 bytes e um tamanho que seja o número de compartimentos com suporte multiplicado pelo tamanho do compartimento (4 bytes) para cada componente solicitado.</span><span class="sxs-lookup"><span data-stu-id="d4610-130">You must supply a buffer with a 256-byte aligned offset and a size that is the supported number of bins multiplied by the bin size (4 bytes) for each component requested.</span></span>  <span data-ttu-id="d4610-131">O posicionamento do compartimento é determinado por:</span><span class="sxs-lookup"><span data-stu-id="d4610-131">Bin placement is determined by:</span></span>

`binIndex = floor(value / [max value of channel + 1] * (countBins))`


<span data-ttu-id="d4610-132">Quando um formato define os bits úteis de um componente menor que o número de bits de armazenamento (por exemplo, P010 usa os 10 principais bits de 16 bits de armazenamento de componentes), somente os bits úteis são considerados (P010 é tratado como um valor de 10 bits).</span><span class="sxs-lookup"><span data-stu-id="d4610-132">When a format defines the useful bits of a component as less than the number of storage bits (for example, P010 uses the top 10 bits of 16 bits of component storage), only the useful bits are considered (P010 is treated as a 10 bit value).</span></span> 

<span data-ttu-id="d4610-133">O dispositivo de vídeo relata quais componentes têm suporte.</span><span class="sxs-lookup"><span data-stu-id="d4610-133">The video device reports which components are supported.</span></span>  <span data-ttu-id="d4610-134">Se o chamador não quiser um histograma para um determinado componente, ele especificará nullptr.</span><span class="sxs-lookup"><span data-stu-id="d4610-134">If the caller does not want a histogram for a given component, they specify nullptr.</span></span>  <span data-ttu-id="d4610-135">Se o driver não oferecer suporte a um histograma para um determinado componente, o buffer de histograma do componente deverá ser nullptr.</span><span class="sxs-lookup"><span data-stu-id="d4610-135">If the driver does not support a histogram for a given component, that component's histogram buffer must be nullptr.</span></span>

<span data-ttu-id="d4610-136">Quando há suporte para vários componentes, o aplicativo pode solicitar qualquer combinação de componentes por decodificação de quadro.</span><span class="sxs-lookup"><span data-stu-id="d4610-136">When multiple components are supported, the application may request any combination of components per frame decode.</span></span>  <span data-ttu-id="d4610-137">Por exemplo, se o hardware fornece suporte para os componentes Y, U e V, o aplicativo pode solicitar o histograma Y somente para o quadro um, o histograma de U somente para o quadro dois e o histograma V somente para o quadro 3.</span><span class="sxs-lookup"><span data-stu-id="d4610-137">For example,if the hardware reports support for Y, U, and V components, the application may request the Y histogram only for frame one, the U histogram only for frame two, and the V histogram only for frame 3.</span></span>  <span data-ttu-id="d4610-138">Eles também podem solicitar qualquer combinação de dois componentes ou de todos os três componentes.</span><span class="sxs-lookup"><span data-stu-id="d4610-138">They may also request any combination of two components or all three components.</span></span>

<span data-ttu-id="d4610-139">Os aplicativos fornecem um deslocamento/ponteiro de buffer/identificador separado para cada componente solicitado.</span><span class="sxs-lookup"><span data-stu-id="d4610-139">Applications supply a separate offset and buffer pointer/handle for each component requested.</span></span>  <span data-ttu-id="d4610-140">Esse ponteiro pode apontar para o mesmo recurso que outro componente ou um recurso separado.</span><span class="sxs-lookup"><span data-stu-id="d4610-140">This pointer may point to the same resource as another component or a separate resource.</span></span>  <span data-ttu-id="d4610-141">O deslocamento permite colocar vários componentes no mesmo buffer, mas a região de saída especificada pelo deslocamento e o tamanho do histograma não devem sobrepor outra saída do componente de histograma.</span><span class="sxs-lookup"><span data-stu-id="d4610-141">The offset allows placing multiple components in the same buffer, but the output region specified by the offset and the histogram size must not overlap another histogram component output.</span></span>  <span data-ttu-id="d4610-142">O histograma também pode ser gravado no mesmo buffer que outro conteúdo não relacionado, como quando usado em uma estratégia de subalocação de recursos.</span><span class="sxs-lookup"><span data-stu-id="d4610-142">The histogram may also be written to the same buffer as other unrelated content such as when being used in a resource sub-allocation strategy.</span></span>


<span data-ttu-id="d4610-143">O tempo de execução do D3D valida se os chamadores só habilitam o histograma para componentes com suporte, se o deslocamento do buffer está alinhado e se o tamanho do buffer é suficiente para o número relatado de compartimentos.</span><span class="sxs-lookup"><span data-stu-id="d4610-143">The D3D runtime validates that callers only enable histogram for supported components, that the buffer offset is aligned, and that buffer size is sufficient for the reported number of bins.</span></span>


## <a name="protected-content"></a><span data-ttu-id="d4610-144">Conteúdo protegido</span><span class="sxs-lookup"><span data-stu-id="d4610-144">Protected content</span></span>

<span data-ttu-id="d4610-145">Os buffers de histograma precisam ter a mesma proteção de superfície que a superfície de saída de decodificação.</span><span class="sxs-lookup"><span data-stu-id="d4610-145">The Histogram buffers are required to have the same surface protection as the decode output surface.</span></span> <span data-ttu-id="d4610-146">Se a superfície de saída de decodificação não for um recurso protegido, o buffer de histograma não deverá ser um recurso protegido.</span><span class="sxs-lookup"><span data-stu-id="d4610-146">If the decode output surface is not a protected resource, the histogram buffer must not be a protected resource.</span></span> <span data-ttu-id="d4610-147">Se a superfície de saída de decodificação for um recurso protegido, o histograma deverá ser um recurso protegido.</span><span class="sxs-lookup"><span data-stu-id="d4610-147">If the decode output surface is protected resource, the histogram must be a protected resource.</span></span>








## <a name="related-topics"></a><span data-ttu-id="d4610-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d4610-148">Related topics</span></span>

<dl> <span data-ttu-id="d4610-149"><dt>APIs de vídeo do 
[Direct3D 12](direct3d-12-video-apis.md) 
 [Guia de programação Media Foundation](media-foundation-programming-guide.md)
</dt> </span><span class="sxs-lookup"><span data-stu-id="d4610-149"><dt>
[Direct3D 12 Video APIs](direct3d-12-video-apis.md)
[Media Foundation Programming Guide](media-foundation-programming-guide.md)
</dt> </span></span></dl>

 

 





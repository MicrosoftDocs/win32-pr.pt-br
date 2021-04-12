---
description: O processamento de vídeo de DXVA encapsula as funções do hardware de gráficos que são dedicadas ao processamento de imagens de vídeo descompactadas. Os serviços de processamento de vídeo incluem desentrelaçamento e mixagem de vídeo.
ms.assetid: bd688f81-4b7c-4016-b0bd-e40782131f8e
title: Processamento de vídeo de DXVA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf5058d93ddd7c506a501eb6ca07c4661755fc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501173"
---
# <a name="dxva-video-processing"></a><span data-ttu-id="bdc17-104">Processamento de vídeo de DXVA</span><span class="sxs-lookup"><span data-stu-id="bdc17-104">DXVA Video Processing</span></span>

<span data-ttu-id="bdc17-105">O processamento de vídeo de DXVA encapsula as funções do hardware de gráficos que são dedicadas ao processamento de imagens de vídeo descompactadas.</span><span class="sxs-lookup"><span data-stu-id="bdc17-105">DXVA video processing encapsulates the functions of the graphics hardware that are devoted to processing uncompressed video images.</span></span> <span data-ttu-id="bdc17-106">Os serviços de processamento de vídeo incluem desentrelaçamento e mixagem de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bdc17-106">Video processing services include deinterlacing and video mixing.</span></span>

<span data-ttu-id="bdc17-107">Este tópico contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="bdc17-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="bdc17-108">Visão geral</span><span class="sxs-lookup"><span data-stu-id="bdc17-108">Overview</span></span>](#overview)
-   [<span data-ttu-id="bdc17-109">Criando um dispositivo de processamento de vídeo</span><span class="sxs-lookup"><span data-stu-id="bdc17-109">Creating a Video Processing Device</span></span>](#creating-a-video-processing-device)
    -   [<span data-ttu-id="bdc17-110">Obter o ponteiro IDirectXVideoProcessorService</span><span class="sxs-lookup"><span data-stu-id="bdc17-110">Get the IDirectXVideoProcessorService Pointer</span></span>](#get-the-idirectxvideoprocessorservice-pointer)
    -   [<span data-ttu-id="bdc17-111">Enumerar os dispositivos de processamento de vídeo</span><span class="sxs-lookup"><span data-stu-id="bdc17-111">Enumerate the Video Processing Devices</span></span>](#enumerate-the-video-processing-devices)
    -   [<span data-ttu-id="bdc17-112">Enumerar formatos de Render-Target</span><span class="sxs-lookup"><span data-stu-id="bdc17-112">Enumerate Render-Target Formats</span></span>](#enumerate-render-target-formats)
    -   [<span data-ttu-id="bdc17-113">Consultar os recursos do dispositivo</span><span class="sxs-lookup"><span data-stu-id="bdc17-113">Query the Device Capabilities</span></span>](#query-the-device-capabilities)
    -   [<span data-ttu-id="bdc17-114">Criar o dispositivo</span><span class="sxs-lookup"><span data-stu-id="bdc17-114">Create the Device</span></span>](#create-the-device)
-   [<span data-ttu-id="bdc17-115">Blit de processo de vídeo</span><span class="sxs-lookup"><span data-stu-id="bdc17-115">Video Process Blit</span></span>](#video-process-blit)
    -   [<span data-ttu-id="bdc17-116">Parâmetros de blit</span><span class="sxs-lookup"><span data-stu-id="bdc17-116">Blit Parameters</span></span>](#blit-parameters)
    -   [<span data-ttu-id="bdc17-117">Exemplos de entrada</span><span class="sxs-lookup"><span data-stu-id="bdc17-117">Input Samples</span></span>](#input-samples)
-   [<span data-ttu-id="bdc17-118">Composição de imagem</span><span class="sxs-lookup"><span data-stu-id="bdc17-118">Image Composition</span></span>](#image-composition)
    -   [<span data-ttu-id="bdc17-119">Exemplo 1: formato Letterbox</span><span class="sxs-lookup"><span data-stu-id="bdc17-119">Example 1: Letterboxing</span></span>](#example-1-letterboxing)
    -   [<span data-ttu-id="bdc17-120">Exemplo 2: alongar imagens de Subfluxo</span><span class="sxs-lookup"><span data-stu-id="bdc17-120">Example 2: Stretching Substream Images</span></span>](#example-2-stretching-substream-images)
    -   [<span data-ttu-id="bdc17-121">Exemplo 3: alturas de fluxo incompatíveis</span><span class="sxs-lookup"><span data-stu-id="bdc17-121">Example 3: Mismatched Stream Heights</span></span>](#example-3-mismatched-stream-heights)
    -   [<span data-ttu-id="bdc17-122">Exemplo 4: retângulo de destino menor que superfície de destino</span><span class="sxs-lookup"><span data-stu-id="bdc17-122">Example 4: Target Rectangle Smaller Than Destination Surface</span></span>](#example-4-target-rectangle-smaller-than-destination-surface)
    -   [<span data-ttu-id="bdc17-123">Exemplo 5: retângulos de origem</span><span class="sxs-lookup"><span data-stu-id="bdc17-123">Example 5: Source Rectangles</span></span>](#example-5-source-rectangles)
    -   [<span data-ttu-id="bdc17-124">Exemplo 6: retângulos de destino com interseção</span><span class="sxs-lookup"><span data-stu-id="bdc17-124">Example 6: Intersecting Destination Rectangles</span></span>](#example-6-intersecting-destination-rectangles)
    -   [<span data-ttu-id="bdc17-125">Exemplo 7: alongando e cortando vídeo</span><span class="sxs-lookup"><span data-stu-id="bdc17-125">Example 7: Stretching and Cropping Video</span></span>](#example-7-stretching-and-cropping-video)
-   [<span data-ttu-id="bdc17-126">Ordem de amostra de entrada</span><span class="sxs-lookup"><span data-stu-id="bdc17-126">Input Sample Order</span></span>](#input-sample-order)
    -   [<span data-ttu-id="bdc17-127">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bdc17-127">Example 1</span></span>](#example-1-letterboxing)
    -   [<span data-ttu-id="bdc17-128">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="bdc17-128">Example 2</span></span>](#example-2-stretching-substream-images)
    -   [<span data-ttu-id="bdc17-129">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="bdc17-129">Example 3</span></span>](#example-3-mismatched-stream-heights)
    -   [<span data-ttu-id="bdc17-130">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="bdc17-130">Example 4</span></span>](#example-4-target-rectangle-smaller-than-destination-surface)
-   [<span data-ttu-id="bdc17-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bdc17-131">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="bdc17-132">Visão geral</span><span class="sxs-lookup"><span data-stu-id="bdc17-132">Overview</span></span>

<span data-ttu-id="bdc17-133">O hardware de gráficos pode usar a GPU (unidade de processamento gráfico) para processar imagens de vídeo descompactadas.</span><span class="sxs-lookup"><span data-stu-id="bdc17-133">Graphics hardware can use the graphics processing unit (GPU) to process uncompressed video images.</span></span> <span data-ttu-id="bdc17-134">Um dispositivo de *processamento de vídeo* é um componente de software que encapsula essas funções.</span><span class="sxs-lookup"><span data-stu-id="bdc17-134">A *video processing* device is a software component that encapsulates these functions.</span></span> <span data-ttu-id="bdc17-135">Os aplicativos podem usar um dispositivo de processamento de vídeo para executar funções como:</span><span class="sxs-lookup"><span data-stu-id="bdc17-135">Applications can use a video processing device to perform functions such as:</span></span>

-   <span data-ttu-id="bdc17-136">Desentrelaçamento e telecineon inverso</span><span class="sxs-lookup"><span data-stu-id="bdc17-136">Deinterlacing and inverse telecine</span></span>
-   <span data-ttu-id="bdc17-137">Misturando subfluxos de vídeo na imagem de vídeo principal</span><span class="sxs-lookup"><span data-stu-id="bdc17-137">Mixing video substreams onto the main video image</span></span>
-   <span data-ttu-id="bdc17-138">Ajuste de cores (Procamp) e filtragem de imagem</span><span class="sxs-lookup"><span data-stu-id="bdc17-138">Color adjustment (ProcAmp) and image filtering</span></span>
-   <span data-ttu-id="bdc17-139">Dimensionamento de imagem</span><span class="sxs-lookup"><span data-stu-id="bdc17-139">Image scaling</span></span>
-   <span data-ttu-id="bdc17-140">Conversão de espaço de cor</span><span class="sxs-lookup"><span data-stu-id="bdc17-140">Color-space conversion</span></span>
-   <span data-ttu-id="bdc17-141">Mesclagem alfa</span><span class="sxs-lookup"><span data-stu-id="bdc17-141">Alpha blending</span></span>

<span data-ttu-id="bdc17-142">O diagrama a seguir mostra os estágios no pipeline de processamento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bdc17-142">The following diagram shows the stages in the video processing pipeline.</span></span> <span data-ttu-id="bdc17-143">O diagrama não deve mostrar uma implementação real.</span><span class="sxs-lookup"><span data-stu-id="bdc17-143">The diagram is not meant to show an actual implementation.</span></span> <span data-ttu-id="bdc17-144">Por exemplo, o driver de gráficos pode combinar vários estágios em uma única operação.</span><span class="sxs-lookup"><span data-stu-id="bdc17-144">For example, the graphics driver might combine several stages into a single operation.</span></span> <span data-ttu-id="bdc17-145">Todas essas operações podem ser executadas em uma única chamada para o dispositivo de processamento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bdc17-145">All of these operations can be performed in a single call to the video processing device.</span></span> <span data-ttu-id="bdc17-146">Alguns estágios mostrados aqui, como filtragem de ruído e de detalhes, podem não ser suportados pelo driver.</span><span class="sxs-lookup"><span data-stu-id="bdc17-146">Some stages shown here, such as noise and detail filtering, might not be supported by the driver.</span></span>

![diagrama mostrando os estágios do processamento de vídeo DXVA.](images/8581554e-a1bc-4cab-9ae1-99a6537e2a84.gif)

<span data-ttu-id="bdc17-148">A entrada para o pipeline de processamento de vídeo sempre inclui um fluxo de vídeo *primário* , que contém os dados da imagem principal.</span><span class="sxs-lookup"><span data-stu-id="bdc17-148">The input to the video processing pipeline always includes a *primary* video stream, which contains the main image data.</span></span> <span data-ttu-id="bdc17-149">O fluxo de vídeo primário determina a taxa de quadros para o vídeo de saída.</span><span class="sxs-lookup"><span data-stu-id="bdc17-149">The primary video stream determines the frame rate for the output video.</span></span> <span data-ttu-id="bdc17-150">Cada quadro do vídeo de saída é calculado em relação aos dados de entrada do fluxo de vídeo primário.</span><span class="sxs-lookup"><span data-stu-id="bdc17-150">Each frame of the output video is calculated relative to the input data from the primary video stream.</span></span> <span data-ttu-id="bdc17-151">Os pixels no fluxo primário são sempre opacos, sem dados alfa por pixel.</span><span class="sxs-lookup"><span data-stu-id="bdc17-151">Pixels in the primary stream are always opaque, with no per-pixel alpha data.</span></span> <span data-ttu-id="bdc17-152">O fluxo de vídeo primário pode ser progressivo ou entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="bdc17-152">The primary video stream can be progressive or interlaced.</span></span>

<span data-ttu-id="bdc17-153">Opcionalmente, o pipeline de processamento de vídeo pode receber até 15 subfluxos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bdc17-153">Optionally, the video processing pipeline can receive up to 15 video substreams.</span></span> <span data-ttu-id="bdc17-154">Um subfluxo contém dados de imagem auxiliares, como legendas codificadas ou subfiguras de DVD.</span><span class="sxs-lookup"><span data-stu-id="bdc17-154">A substream contains auxiliary image data, such as closed captions or DVD subpictures.</span></span> <span data-ttu-id="bdc17-155">Essas imagens são exibidas sobre o fluxo de vídeo primário e, em geral, não devem ser mostradas por si mesmas.</span><span class="sxs-lookup"><span data-stu-id="bdc17-155">These images are displayed over the primary video stream, and are generally not meant to be shown by themselves.</span></span> <span data-ttu-id="bdc17-156">As imagens de substream podem conter dados alfa por pixel e são sempre quadros progressivos.</span><span class="sxs-lookup"><span data-stu-id="bdc17-156">Substream pictures can contain per-pixel alpha data, and are always progressive frames.</span></span> <span data-ttu-id="bdc17-157">O dispositivo de processamento de vídeo Alpha-combina as imagens de subfluxo com o quadro desentrelaçado atual do fluxo de vídeo primário.</span><span class="sxs-lookup"><span data-stu-id="bdc17-157">The video processing device alpha-blends the substream images with the current deinterlaced frame from the primary video stream.</span></span>

<span data-ttu-id="bdc17-158">No restante deste tópico, o termo *imagem* é usado para os dados de entrada para um dispositivo de processamento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bdc17-158">In the remainder of this topic, the term *picture* is used for the input data to a video processing device.</span></span> <span data-ttu-id="bdc17-159">Uma imagem pode consistir em um quadro progressivo, um único campo ou dois campos intercalados.</span><span class="sxs-lookup"><span data-stu-id="bdc17-159">A picture might consist of a progressive frame, a single field, or two interleaved fields.</span></span> <span data-ttu-id="bdc17-160">A saída é sempre um quadro desentrelaçado.</span><span class="sxs-lookup"><span data-stu-id="bdc17-160">The output is always a deinterlaced frame.</span></span>

<span data-ttu-id="bdc17-161">Um driver de vídeo pode implementar mais de um dispositivo de processamento de vídeo, para fornecer diferentes conjuntos de recursos de processamento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bdc17-161">A video driver can implement more than one video processing device, to provide different sets of video processing capabilities.</span></span> <span data-ttu-id="bdc17-162">Os dispositivos são identificados por GUID.</span><span class="sxs-lookup"><span data-stu-id="bdc17-162">Devices are identified by GUID.</span></span> <span data-ttu-id="bdc17-163">Os GUIDs a seguir são predefinidos:</span><span class="sxs-lookup"><span data-stu-id="bdc17-163">The following GUIDs are predefined:</span></span>

-   <span data-ttu-id="bdc17-164">**DXVA2 \_ VideoProcBobDevice**.</span><span class="sxs-lookup"><span data-stu-id="bdc17-164">**DXVA2\_VideoProcBobDevice**.</span></span> <span data-ttu-id="bdc17-165">Este dispositivo executa Bob deentrelaçando.</span><span class="sxs-lookup"><span data-stu-id="bdc17-165">This device performs bob deinterlacing.</span></span>
-   <span data-ttu-id="bdc17-166">**DXVA2 \_ VideoProcProgressiveDevice**.</span><span class="sxs-lookup"><span data-stu-id="bdc17-166">**DXVA2\_VideoProcProgressiveDevice**.</span></span> <span data-ttu-id="bdc17-167">Este dispositivo será usado se o vídeo contiver apenas quadros progressivos, sem quadros entrelaçados.</span><span class="sxs-lookup"><span data-stu-id="bdc17-167">This device is used if the video contains only progressive frames, with no interlaced frames.</span></span> <span data-ttu-id="bdc17-168">(Alguns conteúdos de vídeo contêm uma mistura de quadros progressivos e entrelaçados.</span><span class="sxs-lookup"><span data-stu-id="bdc17-168">(Some video content contains a mix of progressive and interlaced frames.</span></span> <span data-ttu-id="bdc17-169">O dispositivo progressivo não pode ser usado para esse tipo de conteúdo de vídeo "misto", pois uma etapa de desentrelaçamento é necessária para os quadros entrelaçados.)</span><span class="sxs-lookup"><span data-stu-id="bdc17-169">The progressive device cannot be used for this kind of "mixed" video content, because a deinterlacing step is required for the interlaced frames.)</span></span>

<span data-ttu-id="bdc17-170">Cada driver de gráficos que dá suporte ao processamento de vídeo de DXVA deve implementar pelo menos esses dois dispositivos.</span><span class="sxs-lookup"><span data-stu-id="bdc17-170">Every graphics driver that supports DXVA video processing must implement at least these two devices.</span></span> <span data-ttu-id="bdc17-171">O driver de gráficos também pode fornecer outros dispositivos, que são identificados por GUIDs específicos de driver.</span><span class="sxs-lookup"><span data-stu-id="bdc17-171">The graphics driver may also provide other devices, which are identified by driver-specific GUIDs.</span></span> <span data-ttu-id="bdc17-172">Por exemplo, um driver pode implementar um algoritmo de desentrelaçamento proprietário que produz uma saída de qualidade melhor do que Bob desentrelaçar.</span><span class="sxs-lookup"><span data-stu-id="bdc17-172">For example, a driver might implement a proprietary deinterlacing algorithm that produces better quality output than bob deinterlacing.</span></span> <span data-ttu-id="bdc17-173">Alguns algoritmos de desentrelaçamento podem exigir imagens de referência diretas ou regressivas do fluxo principal.</span><span class="sxs-lookup"><span data-stu-id="bdc17-173">Some deinterlacing algorithms may require forward or backward reference pictures from the primary stream.</span></span> <span data-ttu-id="bdc17-174">Nesse caso, o chamador deve fornecer essas imagens para o driver na sequência correta, conforme descrito posteriormente nesta seção.</span><span class="sxs-lookup"><span data-stu-id="bdc17-174">If so, the caller must provide these pictures to the driver in the correct sequence, as described later in this section.</span></span>

<span data-ttu-id="bdc17-175">Também é fornecido um dispositivo de software de referência.</span><span class="sxs-lookup"><span data-stu-id="bdc17-175">A reference software device is also provided.</span></span> <span data-ttu-id="bdc17-176">O dispositivo de software é otimizado para qualidade em vez de velocidade e pode não ser adequado para processamento de vídeo em tempo real.</span><span class="sxs-lookup"><span data-stu-id="bdc17-176">The software device is optimized for quality rather than speed, and may not be adequate for real-time video processing.</span></span> <span data-ttu-id="bdc17-177">O dispositivo de software de referência usa o valor de GUID DXVA2 \_ VideoProcSoftwareDevice.</span><span class="sxs-lookup"><span data-stu-id="bdc17-177">The reference software device uses the GUID value DXVA2\_VideoProcSoftwareDevice.</span></span>

## <a name="creating-a-video-processing-device"></a><span data-ttu-id="bdc17-178">Criando um dispositivo de processamento de vídeo</span><span class="sxs-lookup"><span data-stu-id="bdc17-178">Creating a Video Processing Device</span></span>

<span data-ttu-id="bdc17-179">Antes de usar o processamento de vídeo de DXVA, o aplicativo deve criar um dispositivo de processamento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bdc17-179">Before using DXVA video processing, the application must create a video processing device.</span></span> <span data-ttu-id="bdc17-180">Aqui está uma breve descrição das etapas, que são explicadas com mais detalhes no restante desta seção:</span><span class="sxs-lookup"><span data-stu-id="bdc17-180">Here is a brief outline of the steps, which are explained in greater detail in the remainder of this section:</span></span>

1.  <span data-ttu-id="bdc17-181">Obtenha um ponteiro para a interface [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) .</span><span class="sxs-lookup"><span data-stu-id="bdc17-181">Get a pointer to the [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) interface.</span></span>
2.  <span data-ttu-id="bdc17-182">Crie uma descrição do formato de vídeo para o fluxo de vídeo primário.</span><span class="sxs-lookup"><span data-stu-id="bdc17-182">Create a description of the video format for the primary video stream.</span></span> <span data-ttu-id="bdc17-183">Use esta descrição para obter uma lista dos dispositivos de processamento de vídeo que dão suporte ao formato de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bdc17-183">Use this description to get a list of the video processing devices that support the video format.</span></span> <span data-ttu-id="bdc17-184">Os dispositivos são identificados por GUID.</span><span class="sxs-lookup"><span data-stu-id="bdc17-184">Devices are identified by GUID.</span></span>
3.  <span data-ttu-id="bdc17-185">Para um dispositivo específico, obtenha uma lista de formatos de destino de renderização com suporte no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bdc17-185">For a particular device, get a list of render-target formats supported by the device.</span></span> <span data-ttu-id="bdc17-186">Os formatos são retornados como uma lista de valores de **D3DFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="bdc17-186">The formats are returned as a list of **D3DFORMAT** values.</span></span> <span data-ttu-id="bdc17-187">Se você planeja misturar subfluxos, obtenha também uma lista dos formatos de subfluxo com suporte.</span><span class="sxs-lookup"><span data-stu-id="bdc17-187">If you plan to mix substreams, get a list of the supported substream formats as well.</span></span>
4.  <span data-ttu-id="bdc17-188">Consulte os recursos de cada dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bdc17-188">Query the capabilities of each device.</span></span>
5.  <span data-ttu-id="bdc17-189">Crie o dispositivo de processamento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bdc17-189">Create the video processing device.</span></span>

<span data-ttu-id="bdc17-190">Às vezes, você pode omitir algumas dessas etapas.</span><span class="sxs-lookup"><span data-stu-id="bdc17-190">Sometimes you can omit some of these steps.</span></span> <span data-ttu-id="bdc17-191">Por exemplo, em vez de obter a lista de formatos de destino de renderização, você poderia simplesmente tentar criar o dispositivo de processamento de vídeo com seu formato preferido e ver se ele foi bem sucedido.</span><span class="sxs-lookup"><span data-stu-id="bdc17-191">For example, instead of getting the list of render-target formats, you could simply try creating the video processing device with your preferred format, and see if it succeeds.</span></span> <span data-ttu-id="bdc17-192">Um formato comum, como D3DFMT \_ X8R8G8B8, provavelmente será bem sucedido.</span><span class="sxs-lookup"><span data-stu-id="bdc17-192">A common format such as D3DFMT\_X8R8G8B8 is likely to succeed.</span></span>

<span data-ttu-id="bdc17-193">O restante desta seção descreve essas etapas em detalhes.</span><span class="sxs-lookup"><span data-stu-id="bdc17-193">The remainder of this section describes these steps in detail.</span></span>

### <a name="get-the-idirectxvideoprocessorservice-pointer"></a><span data-ttu-id="bdc17-194">Obter o ponteiro IDirectXVideoProcessorService</span><span class="sxs-lookup"><span data-stu-id="bdc17-194">Get the IDirectXVideoProcessorService Pointer</span></span>

<span data-ttu-id="bdc17-195">A interface [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) é obtida do dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="bdc17-195">The [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) interface is obtained from the Direct3D device.</span></span> <span data-ttu-id="bdc17-196">Há duas maneiras de obter um ponteiro para essa interface:</span><span class="sxs-lookup"><span data-stu-id="bdc17-196">There are two ways to get a pointer to this interface:</span></span>

-   <span data-ttu-id="bdc17-197">De um dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="bdc17-197">From a Direct3D device.</span></span>
-   <span data-ttu-id="bdc17-198">Do [Direct3D gerenciador de dispositivos](direct3d-device-manager.md).</span><span class="sxs-lookup"><span data-stu-id="bdc17-198">From the [Direct3D Device Manager](direct3d-device-manager.md).</span></span>

<span data-ttu-id="bdc17-199">Se você tiver um ponteiro para um dispositivo Direct3D, poderá obter um ponteiro [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) chamando a função [**DXVA2CreateVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createvideoservice) .</span><span class="sxs-lookup"><span data-stu-id="bdc17-199">If you have a pointer to a Direct3D device, you can get an [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) pointer by calling the [**DXVA2CreateVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createvideoservice) function.</span></span> <span data-ttu-id="bdc17-200">Passe um ponteiro para a interface **IDirect3DDevice9** do dispositivo e especifique IDirectXVideoProcessorService de **IID \_** para o parâmetro *riid* , conforme mostrado no código a seguir:</span><span class="sxs-lookup"><span data-stu-id="bdc17-200">Pass in a pointer to the device's **IDirect3DDevice9** interface, and specify **IID\_IDirectXVideoProcessorService** for the *riid* parameter, as shown in the following code:</span></span>


```C++
    // Create the DXVA-2 Video Processor service.
    hr = DXVA2CreateVideoService(g_pD3DD9, IID_PPV_ARGS(&g_pDXVAVPS));
```



<span data-ttu-id="bdc17-201">n alguns casos, um objeto cria o dispositivo Direct3D e, em seguida, compartilha-o com outros objetos por meio do [Direct3D gerenciador de dispositivos](direct3d-device-manager.md).</span><span class="sxs-lookup"><span data-stu-id="bdc17-201">n some cases, one object creates the Direct3D device and then shares it with other objects through the [Direct3D Device Manager](direct3d-device-manager.md).</span></span> <span data-ttu-id="bdc17-202">Nessa situação, você pode chamar [**IDirect3DDeviceManager9:: GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) no Gerenciador de dispositivos para obter o ponteiro [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) , conforme mostrado no código a seguir:</span><span class="sxs-lookup"><span data-stu-id="bdc17-202">In this situation, you can call [**IDirect3DDeviceManager9::GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) on the device manager to get the [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) pointer, as shown in the following code:</span></span>


```C++
HRESULT GetVideoProcessorService(
    IDirect3DDeviceManager9 *pDeviceManager,
    IDirectXVideoProcessorService **ppVPService
    )
{
    *ppVPService = NULL;

    HANDLE hDevice;

    HRESULT hr = pDeviceManager->OpenDeviceHandle(&hDevice);
    if (SUCCEEDED(hr))
    {
        // Get the video processor service 
        HRESULT hr2 = pDeviceManager->GetVideoService(
            hDevice, 
            IID_PPV_ARGS(ppVPService)
            );

        // Close the device handle.
        hr = pDeviceManager->CloseDeviceHandle(hDevice);

        if (FAILED(hr2))
        {
            hr = hr2;
        }
    }

    if (FAILED(hr))
    {
        SafeRelease(ppVPService);
    }

    return hr;
}
```



### <a name="enumerate-the-video-processing-devices"></a><span data-ttu-id="bdc17-203">Enumerar os dispositivos de processamento de vídeo</span><span class="sxs-lookup"><span data-stu-id="bdc17-203">Enumerate the Video Processing Devices</span></span>

<span data-ttu-id="bdc17-204">Para obter uma lista de dispositivos de processamento de vídeo, preencha uma estrutura [**DXVA2 \_ VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) com o formato do fluxo de vídeo primário e passe essa estrutura para o método [**IDirectXVideoProcessorService:: GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) .</span><span class="sxs-lookup"><span data-stu-id="bdc17-204">To get a list of video processing devices, fill in a [**DXVA2\_VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) structure with the format of the primary video stream, and pass this structure to the [**IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) method.</span></span> <span data-ttu-id="bdc17-205">O método retorna uma matriz de GUIDs, uma para cada dispositivo de processamento de vídeo que pode ser usado com este formato de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bdc17-205">The method returns an array of GUIDs, one for each video processing device that can be used with this video format.</span></span>

<span data-ttu-id="bdc17-206">Considere um aplicativo que renderiza um fluxo de vídeo no formato YUY2, usando a definição BT. 709 da cor YUV, com uma taxa de quadros de 29,97 quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="bdc17-206">Consider an application that renders a video stream in YUY2 format, using the BT.709 definition of YUV color, with a frame rate of 29.97 frames per second.</span></span> <span data-ttu-id="bdc17-207">Suponha que o conteúdo do vídeo consiste inteiramente em quadros progressivos.</span><span class="sxs-lookup"><span data-stu-id="bdc17-207">Assume that the video content consists entirely of progressive frames.</span></span> <span data-ttu-id="bdc17-208">O fragmento de código a seguir mostra como preencher a descrição do formato e obter os GUIDs do dispositivo:</span><span class="sxs-lookup"><span data-stu-id="bdc17-208">The following code fragment shows how to fill in the format description and get the device GUIDs:</span></span>


```C++
    // Initialize the video descriptor.

    g_VideoDesc.SampleWidth                         = VIDEO_MAIN_WIDTH;
    g_VideoDesc.SampleHeight                        = VIDEO_MAIN_HEIGHT;
    g_VideoDesc.SampleFormat.VideoChromaSubsampling = DXVA2_VideoChromaSubsampling_MPEG2;
    g_VideoDesc.SampleFormat.NominalRange           = DXVA2_NominalRange_16_235;
    g_VideoDesc.SampleFormat.VideoTransferMatrix    = EX_COLOR_INFO[g_ExColorInfo][0];
    g_VideoDesc.SampleFormat.VideoLighting          = DXVA2_VideoLighting_dim;
    g_VideoDesc.SampleFormat.VideoPrimaries         = DXVA2_VideoPrimaries_BT709;
    g_VideoDesc.SampleFormat.VideoTransferFunction  = DXVA2_VideoTransFunc_709;
    g_VideoDesc.SampleFormat.SampleFormat           = DXVA2_SampleProgressiveFrame;
    g_VideoDesc.Format                              = VIDEO_MAIN_FORMAT;
    g_VideoDesc.InputSampleFreq.Numerator           = VIDEO_FPS;
    g_VideoDesc.InputSampleFreq.Denominator         = 1;
    g_VideoDesc.OutputFrameFreq.Numerator           = VIDEO_FPS;
    g_VideoDesc.OutputFrameFreq.Denominator         = 1;

    // Query the video processor GUID.

    UINT count;
    GUID* guids = NULL;

    hr = g_pDXVAVPS->GetVideoProcessorDeviceGuids(&g_VideoDesc, &count, &guids);
```



<span data-ttu-id="bdc17-209">O código para este exemplo é obtido do exemplo de SDK do [DXVA2 \_ VideoProc](dxva2-videoproc-sample.md) .</span><span class="sxs-lookup"><span data-stu-id="bdc17-209">The code for this example is taken from the [DXVA2\_VideoProc](dxva2-videoproc-sample.md) SDK sample.</span></span>

<span data-ttu-id="bdc17-210">A matriz *pGuids* neste exemplo é alocada pelo método [**GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) , de modo que o aplicativo deve liberar a matriz chamando [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="bdc17-210">The *pGuids* array in this example is allocated by the [**GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) method, so the application must free the array by calling [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span> <span data-ttu-id="bdc17-211">As etapas restantes podem ser executadas usando qualquer um dos GUIDs de dispositivo retornados por esse método.</span><span class="sxs-lookup"><span data-stu-id="bdc17-211">The remaining steps can be performed using any of the device GUIDs returned by this method.</span></span>

### <a name="enumerate-render-target-formats"></a><span data-ttu-id="bdc17-212">Enumerar formatos de Render-Target</span><span class="sxs-lookup"><span data-stu-id="bdc17-212">Enumerate Render-Target Formats</span></span>

<span data-ttu-id="bdc17-213">Para obter a lista de formatos de destino de renderização com suporte pelo dispositivo, passe o GUID do dispositivo e a estrutura [**DXVA2 \_ VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) para o método [**IDirectXVideoProcessorService:: GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) , conforme mostrado no código a seguir:</span><span class="sxs-lookup"><span data-stu-id="bdc17-213">To get the list of render-target formats supported by the device, pass the device GUID and the [**DXVA2\_VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) structure to the [**IDirectXVideoProcessorService::GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) method, as shown in the following code:</span></span>


```C++
    // Query the supported render-target formats.

    UINT i, count;
    D3DFORMAT* formats = NULL;

    HRESULT hr = g_pDXVAVPS->GetVideoProcessorRenderTargets(
        guid, &g_VideoDesc, &count, &formats);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorRenderTargets failed: 0x%x.\n", hr));
        return FALSE;
    }

    for (i = 0; i < count; i++)
    {
        if (formats[i] == VIDEO_RENDER_TARGET_FORMAT)
        {
            break;
        }
    }

    CoTaskMemFree(formats);

    if (i >= count)
    {
        DBGMSG((L"The device does not support the render-target format.\n"));
        return FALSE;
    }
```



<span data-ttu-id="bdc17-214">O método retorna uma matriz de valores **D3DFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="bdc17-214">The method returns an array of **D3DFORMAT** values.</span></span> <span data-ttu-id="bdc17-215">Neste exemplo, onde o tipo de entrada é YUY2, uma lista típica de formatos pode ser D3DFMT \_ X8R8G8B8 (32-bit RGB) e D3DMFT \_ YUY2 (o formato de entrada).</span><span class="sxs-lookup"><span data-stu-id="bdc17-215">In this example, where the input type is YUY2, a typical list of formats might be D3DFMT\_X8R8G8B8 (32-bit RGB) and D3DMFT\_YUY2 (the input format).</span></span> <span data-ttu-id="bdc17-216">No entanto, a lista exata dependerá do driver.</span><span class="sxs-lookup"><span data-stu-id="bdc17-216">However, the exact list will depend on the driver.</span></span>

<span data-ttu-id="bdc17-217">A lista de formatos disponíveis para os subfluxos pode variar dependendo do formato de destino de renderização e do formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="bdc17-217">The list of available formats for the substreams can vary depending on the render-target format and the input format.</span></span> <span data-ttu-id="bdc17-218">Para obter a lista de formatos de Subfluxo, passe o GUID do dispositivo, a estrutura de formato e o formato de destino de renderização para o método [**IDirectXVideoProcessorService:: GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) , conforme mostrado no código a seguir:</span><span class="sxs-lookup"><span data-stu-id="bdc17-218">To get the list of substream formats, pass the device GUID, the format structure, and the render-target format to the [**IDirectXVideoProcessorService::GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) method, as shown in the following code:</span></span>


```C++
    // Query the supported substream formats.

    formats = NULL;

    hr = g_pDXVAVPS->GetVideoProcessorSubStreamFormats(
        guid, &g_VideoDesc, VIDEO_RENDER_TARGET_FORMAT, &count, &formats);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorSubStreamFormats failed: 0x%x.\n", hr));
        return FALSE;
    }

    for (i = 0; i < count; i++)
    {
        if (formats[i] == VIDEO_SUB_FORMAT)
        {
            break;
        }
    }

    CoTaskMemFree(formats);

    if (i >= count)
    {
        DBGMSG((L"The device does not support the substream format.\n"));
        return FALSE;
    }
```



<span data-ttu-id="bdc17-219">Esse método retorna outra matriz de valores **D3DFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="bdc17-219">This method returns another array of **D3DFORMAT** values.</span></span> <span data-ttu-id="bdc17-220">Os formatos de Subfluxo típicos são AYUV e AI44.</span><span class="sxs-lookup"><span data-stu-id="bdc17-220">Typical substream formats are AYUV and AI44.</span></span>

### <a name="query-the-device-capabilities"></a><span data-ttu-id="bdc17-221">Consultar os recursos do dispositivo</span><span class="sxs-lookup"><span data-stu-id="bdc17-221">Query the Device Capabilities</span></span>

<span data-ttu-id="bdc17-222">Para obter os recursos de um dispositivo específico, passe o GUID do dispositivo, a estrutura de formato e um formato de destino de renderização para o método [**IDirectXVideoProcessorService:: GetVideoProcessorCaps**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorcaps) .</span><span class="sxs-lookup"><span data-stu-id="bdc17-222">To get the capabilities of a particular device, pass the device GUID, the format structure, and a render-target format to the [**IDirectXVideoProcessorService::GetVideoProcessorCaps**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorcaps) method.</span></span> <span data-ttu-id="bdc17-223">O método preenche uma estrutura de estrutura [**DXVA2 \_ VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) com os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bdc17-223">The method fills in a [**DXVA2\_VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) structure structure with the device capabilities.</span></span>


```C++
    // Query video processor capabilities.

    hr = g_pDXVAVPS->GetVideoProcessorCaps(
        guid, &g_VideoDesc, VIDEO_RENDER_TARGET_FORMAT, &g_VPCaps);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorCaps failed: 0x%x.\n", hr));
        return FALSE;
    }
```



### <a name="create-the-device"></a><span data-ttu-id="bdc17-224">Criar o dispositivo</span><span class="sxs-lookup"><span data-stu-id="bdc17-224">Create the Device</span></span>

<span data-ttu-id="bdc17-225">Para criar o dispositivo de processamento de vídeo, chame [**IDirectXVideoProcessorService:: CreateVideoProcessor**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-createvideoprocessor).</span><span class="sxs-lookup"><span data-stu-id="bdc17-225">To create the video processing device, call [**IDirectXVideoProcessorService::CreateVideoProcessor**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-createvideoprocessor).</span></span> <span data-ttu-id="bdc17-226">A entrada para esse método é o GUID do dispositivo, a descrição do formato, o formato de destino de renderização e o número máximo de subfluxos que você planeja misturar.</span><span class="sxs-lookup"><span data-stu-id="bdc17-226">The input to this method is the device GUID, the format description, the render-target format, and the maximum number of substreams that you plan to mix.</span></span> <span data-ttu-id="bdc17-227">O método retorna um ponteiro para a interface [**IDirectXVideoProcessor**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor) , que representa o dispositivo de processamento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bdc17-227">The method returns a pointer to the [**IDirectXVideoProcessor**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor) interface, which represents the video processing device.</span></span>


```C++
    // Finally create a video processor device.

    hr = g_pDXVAVPS->CreateVideoProcessor(
        guid,
        &g_VideoDesc,
        VIDEO_RENDER_TARGET_FORMAT,
        SUB_STREAM_COUNT,
        &g_pDXVAVPD
        );
```



## <a name="video-process-blit"></a><span data-ttu-id="bdc17-228">Blit de processo de vídeo</span><span class="sxs-lookup"><span data-stu-id="bdc17-228">Video Process Blit</span></span>

<span data-ttu-id="bdc17-229">A principal operação de processamento de vídeo é o *blit de processamento de vídeo*.</span><span class="sxs-lookup"><span data-stu-id="bdc17-229">The main video processing operation is the *video processing blit*.</span></span> <span data-ttu-id="bdc17-230">(Um *blit* é qualquer operação que combina dois ou mais bitmaps em um único bitmap.</span><span class="sxs-lookup"><span data-stu-id="bdc17-230">(A *blit* is any operation that combines two or more bitmaps into a single bitmap.</span></span> <span data-ttu-id="bdc17-231">Um blit de processamento de vídeo combina imagens de entrada para criar um quadro de saída.) Para executar um blit de processamento de vídeo, chame [**IDirectXVideoProcessor:: VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span><span class="sxs-lookup"><span data-stu-id="bdc17-231">A video processing blit combines input pictures to create an output frame.) To perform a video processing blit, call [**IDirectXVideoProcessor::VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span></span> <span data-ttu-id="bdc17-232">Esse método passa um conjunto de amostras de vídeo para o dispositivo de processamento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bdc17-232">This method passes a set of video samples to the video processing device.</span></span> <span data-ttu-id="bdc17-233">Em resposta, o dispositivo de processamento de vídeo processa as imagens de entrada e gera um quadro de saída.</span><span class="sxs-lookup"><span data-stu-id="bdc17-233">In response, the video processing device processes the input pictures and generates one output frame.</span></span> <span data-ttu-id="bdc17-234">O processamento pode incluir desentrelaçamento, conversão de espaço em cores e mistura de Subfluxo.</span><span class="sxs-lookup"><span data-stu-id="bdc17-234">Processing can include deinterlacing, color-space conversion, and substream mixing.</span></span> <span data-ttu-id="bdc17-235">A saída é gravada em uma superfície de destino fornecida pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="bdc17-235">The output is written to a destination surface provided by the caller.</span></span>

<span data-ttu-id="bdc17-236">O método [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) usa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="bdc17-236">The [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) method takes the following parameters:</span></span>

-   <span data-ttu-id="bdc17-237">o *pRT* aponta para uma superfície de destino de renderização **IDirect3DSurface9** que receberá o quadro de vídeo processado.</span><span class="sxs-lookup"><span data-stu-id="bdc17-237">*pRT* points to an **IDirect3DSurface9** render target surface that will receive the processed video frame.</span></span>
-   <span data-ttu-id="bdc17-238">*pBltParams* aponta para uma [**estrutura \_ VideoProcessBltParams DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) que especifica os parâmetros para o blit.</span><span class="sxs-lookup"><span data-stu-id="bdc17-238">*pBltParams* points to a [**DXVA2\_VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) structure that specifies the parameters for the blit.</span></span>
-   <span data-ttu-id="bdc17-239">*pSamples* é o endereço de uma matriz de [**estruturas \_ VideoSample DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) .</span><span class="sxs-lookup"><span data-stu-id="bdc17-239">*pSamples* is the address of an array of [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structures.</span></span> <span data-ttu-id="bdc17-240">Essas estruturas contêm os exemplos de entrada para o blit.</span><span class="sxs-lookup"><span data-stu-id="bdc17-240">These structures contain the input samples for the blit.</span></span>
-   <span data-ttu-id="bdc17-241">*NumSamples* fornece o tamanho da matriz *pSamples* .</span><span class="sxs-lookup"><span data-stu-id="bdc17-241">*NumSamples* gives the size of the *pSamples* array.</span></span>
-   <span data-ttu-id="bdc17-242">O parâmetro *reservado* é reservado e deve ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="bdc17-242">The *Reserved* parameter is reserved and should be set to **NULL**.</span></span>

<span data-ttu-id="bdc17-243">Na matriz *pSamples* , o chamador deve fornecer os seguintes exemplos de entrada:</span><span class="sxs-lookup"><span data-stu-id="bdc17-243">In the *pSamples* array, the caller must provide the following input samples:</span></span>

-   <span data-ttu-id="bdc17-244">A imagem atual do fluxo de vídeo primário.</span><span class="sxs-lookup"><span data-stu-id="bdc17-244">The current picture from the primary video stream.</span></span>
-   <span data-ttu-id="bdc17-245">Imagens de referência para frente e para trás, se exigido pelo algoritmo de desentrelaçamento.</span><span class="sxs-lookup"><span data-stu-id="bdc17-245">Forward and backward reference pictures, if required by the deinterlacing algorithm.</span></span>
-   <span data-ttu-id="bdc17-246">Zero ou mais imagens de Subfluxo, até um máximo de 15 subfluxos.</span><span class="sxs-lookup"><span data-stu-id="bdc17-246">Zero or more substream pictures, up to a maximum of 15 substreams.</span></span>

<span data-ttu-id="bdc17-247">O driver espera que essa matriz esteja em uma ordem específica, conforme descrito em [ordem de amostra de entrada](#input-sample-order).</span><span class="sxs-lookup"><span data-stu-id="bdc17-247">The driver expects this array to be in a particular order, as described in [Input Sample Order](#input-sample-order).</span></span>

### <a name="blit-parameters"></a><span data-ttu-id="bdc17-248">Parâmetros de blit</span><span class="sxs-lookup"><span data-stu-id="bdc17-248">Blit Parameters</span></span>

<span data-ttu-id="bdc17-249">A estrutura [**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) contém parâmetros gerais para o blit.</span><span class="sxs-lookup"><span data-stu-id="bdc17-249">The [**DXVA2\_VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) structure contains general parameters for the blit.</span></span> <span data-ttu-id="bdc17-250">Os parâmetros mais importantes são armazenados nos seguintes membros da estrutura:</span><span class="sxs-lookup"><span data-stu-id="bdc17-250">The most important parameters are stored in the following members of the structure:</span></span>

-   <span data-ttu-id="bdc17-251">**TargetFrame** é a hora da apresentação do quadro de saída.</span><span class="sxs-lookup"><span data-stu-id="bdc17-251">**TargetFrame** is the presentation time of the output frame.</span></span> <span data-ttu-id="bdc17-252">Para conteúdo progressivo, essa hora deve ser igual à hora de início do quadro atual do fluxo de vídeo primário.</span><span class="sxs-lookup"><span data-stu-id="bdc17-252">For progressive content, this time must equal the start time for the current frame from the primary video stream.</span></span> <span data-ttu-id="bdc17-253">Esse tempo é especificado no membro **inicial** da estrutura [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) para esse exemplo de entrada.</span><span class="sxs-lookup"><span data-stu-id="bdc17-253">This time is specified in the **Start** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure for that input sample.</span></span>

    <span data-ttu-id="bdc17-254">Para conteúdo entrelaçado, um quadro com dois campos intercalados produz dois quadros de saída desentrelaçados.</span><span class="sxs-lookup"><span data-stu-id="bdc17-254">For interlaced content, a frame with two interleaved fields produces two deinterlaced output frames.</span></span> <span data-ttu-id="bdc17-255">No primeiro quadro de saída, a hora da apresentação deve ser igual à hora de início da imagem atual no fluxo de vídeo primário, assim como o conteúdo progressivo.</span><span class="sxs-lookup"><span data-stu-id="bdc17-255">On the first output frame, the presentation time must equal the start time of the current picture in the primary video stream, just like progressive content.</span></span> <span data-ttu-id="bdc17-256">No segundo quadro de saída, a hora de início deve ser igual ao ponto médio entre a hora de início da imagem atual no fluxo de vídeo primário e a hora de início da próxima imagem no fluxo.</span><span class="sxs-lookup"><span data-stu-id="bdc17-256">On the second output frame, the start time must equal the midpoint between the start time of the current picture in the primary video stream and the start time of the next picture in the stream.</span></span> <span data-ttu-id="bdc17-257">Por exemplo, se o vídeo de entrada for de 25 quadros por segundo (50 campos por segundo), os quadros de saída terão os carimbos de data/hora mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="bdc17-257">For example, if the input video is 25 frames per second (50 fields per second), the output frames will have the time stamps shown in the following table.</span></span> <span data-ttu-id="bdc17-258">Os carimbos de data/hora são mostrados em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="bdc17-258">Time stamps are shown in units of 100 nanoseconds.</span></span>

    

    | <span data-ttu-id="bdc17-259">Imagem de entrada</span><span class="sxs-lookup"><span data-stu-id="bdc17-259">Input picture</span></span> | <span data-ttu-id="bdc17-260">**TargetFrame** (1)</span><span class="sxs-lookup"><span data-stu-id="bdc17-260">**TargetFrame** (1)</span></span> | <span data-ttu-id="bdc17-261">**TargetFrame** (2)</span><span class="sxs-lookup"><span data-stu-id="bdc17-261">**TargetFrame** (2)</span></span> |
    |---------------|---------------------|---------------------|
    | <span data-ttu-id="bdc17-262">0</span><span class="sxs-lookup"><span data-stu-id="bdc17-262">0</span></span>             | <span data-ttu-id="bdc17-263">0</span><span class="sxs-lookup"><span data-stu-id="bdc17-263">0</span></span>                   | <span data-ttu-id="bdc17-264">200000</span><span class="sxs-lookup"><span data-stu-id="bdc17-264">200000</span></span>              |
    | <span data-ttu-id="bdc17-265">400000</span><span class="sxs-lookup"><span data-stu-id="bdc17-265">400000</span></span>        | <span data-ttu-id="bdc17-266">0</span><span class="sxs-lookup"><span data-stu-id="bdc17-266">0</span></span>                   | <span data-ttu-id="bdc17-267">600000</span><span class="sxs-lookup"><span data-stu-id="bdc17-267">600000</span></span>              |
    | <span data-ttu-id="bdc17-268">800000</span><span class="sxs-lookup"><span data-stu-id="bdc17-268">800000</span></span>        | <span data-ttu-id="bdc17-269">800000</span><span class="sxs-lookup"><span data-stu-id="bdc17-269">800000</span></span>              | <span data-ttu-id="bdc17-270">1.000.000</span><span class="sxs-lookup"><span data-stu-id="bdc17-270">1000000</span></span>             |
    | <span data-ttu-id="bdc17-271">1,2 milhões</span><span class="sxs-lookup"><span data-stu-id="bdc17-271">1200000</span></span>       | <span data-ttu-id="bdc17-272">1,2 milhões</span><span class="sxs-lookup"><span data-stu-id="bdc17-272">1200000</span></span>             | <span data-ttu-id="bdc17-273">1,4 milhões</span><span class="sxs-lookup"><span data-stu-id="bdc17-273">1400000</span></span>             |

    

     

    <span data-ttu-id="bdc17-274">Se o conteúdo entrelaçado consistir em campos únicos em vez de campos intercalados, os tempos de saída sempre corresponderão aos tempos de entrada, como com conteúdo progressivo.</span><span class="sxs-lookup"><span data-stu-id="bdc17-274">If interlaced content consists of single fields rather than interleaved fields, the output times always match the input times, as with progressive content.</span></span>

-   <span data-ttu-id="bdc17-275">**TargetRect** define uma região retangular dentro da superfície de destino.</span><span class="sxs-lookup"><span data-stu-id="bdc17-275">**TargetRect** defines a rectangular region within the destination surface.</span></span> <span data-ttu-id="bdc17-276">O blit gravará a saída nessa região.</span><span class="sxs-lookup"><span data-stu-id="bdc17-276">The blit will write the output to this region.</span></span> <span data-ttu-id="bdc17-277">Especificamente, todos os pixels dentro de **TargetRect** serão modificados e nenhum pixel fora do **TargetRect** será modificado.</span><span class="sxs-lookup"><span data-stu-id="bdc17-277">Specifically, every pixel inside **TargetRect** will be modified, and no pixels outside of **TargetRect** will be modified.</span></span> <span data-ttu-id="bdc17-278">O retângulo de destino define o retângulo delimitador para todos os fluxos de vídeo de entrada.</span><span class="sxs-lookup"><span data-stu-id="bdc17-278">The target rectangle defines the bounding rectangle for all of the input video streams.</span></span> <span data-ttu-id="bdc17-279">O posicionamento de fluxos individuais dentro desse retângulo é controlado por meio do parâmetro *pSamples* de [**IDirectXVideoProcessor:: VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span><span class="sxs-lookup"><span data-stu-id="bdc17-279">Placement of individual streams within that rectangle is controlled through the *pSamples* parameter of [**IDirectXVideoProcessor::VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span></span>
-   <span data-ttu-id="bdc17-280">**BackgroundColor** fornece a cor do plano de fundo sempre que nenhuma imagem de vídeo é exibida.</span><span class="sxs-lookup"><span data-stu-id="bdc17-280">**BackgroundColor** gives the color of the background wherever no video image appears.</span></span> <span data-ttu-id="bdc17-281">Por exemplo, quando uma imagem de vídeo de 16 x 9 é exibida dentro de uma área 4 x 3 (formato Letterbox), as regiões letterboxed são exibidas com a cor do plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="bdc17-281">For example, when a 16 x 9 video image is displayed within a 4 x 3 area (letterboxing), the letterboxed regions are displayed with the background color.</span></span> <span data-ttu-id="bdc17-282">A cor do plano de fundo só se aplica dentro do retângulo de destino (**TargetRect**).</span><span class="sxs-lookup"><span data-stu-id="bdc17-282">The background color applies only within the target rectangle (**TargetRect**).</span></span> <span data-ttu-id="bdc17-283">Quaisquer pixels fora de **TargetRect** não são modificados.</span><span class="sxs-lookup"><span data-stu-id="bdc17-283">Any pixels outside of **TargetRect** are not modified.</span></span>
-   <span data-ttu-id="bdc17-284">**DestFormat** descreve o espaço de cores para o vídeo de saída — por exemplo, se a cor ITU-R BT. 709 ou BT. 601 é usada.</span><span class="sxs-lookup"><span data-stu-id="bdc17-284">**DestFormat** describes the color space for the output video—for example, whether ITU-R BT.709 or BT.601 color is used.</span></span> <span data-ttu-id="bdc17-285">Essas informações podem afetar a forma como a imagem é exibida.</span><span class="sxs-lookup"><span data-stu-id="bdc17-285">This information can affect how the image is displayed.</span></span> <span data-ttu-id="bdc17-286">Para obter mais informações, consulte [informações de cores estendidas](extended-color-information.md).</span><span class="sxs-lookup"><span data-stu-id="bdc17-286">For more information, see [Extended Color Information](extended-color-information.md).</span></span>

<span data-ttu-id="bdc17-287">Outros parâmetros são descritos na página de referência da estrutura [**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) .</span><span class="sxs-lookup"><span data-stu-id="bdc17-287">Other parameters are described on the reference page for the [**DXVA2\_VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) structure.</span></span>

### <a name="input-samples"></a><span data-ttu-id="bdc17-288">Exemplos de entrada</span><span class="sxs-lookup"><span data-stu-id="bdc17-288">Input Samples</span></span>

<span data-ttu-id="bdc17-289">O parâmetro *pSamples* de [**IDirectXVideoProcessor:: VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) aponta para uma matriz de [**estruturas \_ VideoSample DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) .</span><span class="sxs-lookup"><span data-stu-id="bdc17-289">The *pSamples* parameter of [**IDirectXVideoProcessor::VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) points to an array of [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structures.</span></span> <span data-ttu-id="bdc17-290">Cada uma dessas estruturas contém informações sobre um exemplo de entrada e um ponteiro para a superfície do Direct3D que contém o exemplo.</span><span class="sxs-lookup"><span data-stu-id="bdc17-290">Each of these structures contains information about one input sample and a pointer to the Direct3D surface that contains the sample.</span></span> <span data-ttu-id="bdc17-291">Cada exemplo é um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="bdc17-291">Each sample is one of the following:</span></span>

-   <span data-ttu-id="bdc17-292">A imagem atual do fluxo primário.</span><span class="sxs-lookup"><span data-stu-id="bdc17-292">The current picture from the primary stream.</span></span>
-   <span data-ttu-id="bdc17-293">Uma imagem de referência para frente ou para trás do fluxo principal, usada para desentrelaçar.</span><span class="sxs-lookup"><span data-stu-id="bdc17-293">A forward or backward reference picture from the primary stream, used for deinterlacing.</span></span>
-   <span data-ttu-id="bdc17-294">Uma imagem de Subfluxo.</span><span class="sxs-lookup"><span data-stu-id="bdc17-294">A substream picture.</span></span>

<span data-ttu-id="bdc17-295">A ordem exata na qual os exemplos devem aparecer na matriz é descrita posteriormente, na seção ordem de [exemplo de entrada](#input-sample-order).</span><span class="sxs-lookup"><span data-stu-id="bdc17-295">The exact order in which the samples must appear in the array is described later, in the section [Input Sample Order](#input-sample-order).</span></span>

<span data-ttu-id="bdc17-296">Até 15 imagens de Subfluxo podem ser fornecidas, embora a maioria dos aplicativos de vídeo precise apenas de um subfluxo, no máximo.</span><span class="sxs-lookup"><span data-stu-id="bdc17-296">Up to 15 substream pictures can be provided, although most video applications need only one substream, at the most.</span></span> <span data-ttu-id="bdc17-297">O número de subfluxos pode ser alterado com cada chamada para [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span><span class="sxs-lookup"><span data-stu-id="bdc17-297">The number of substreams can change with each call to [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span></span> <span data-ttu-id="bdc17-298">As imagens de substream são indicadas pela configuração do membro **SampleFormat. SampleFormat** da estrutura [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) igual a DXVA2 \_ SampleSubStream.</span><span class="sxs-lookup"><span data-stu-id="bdc17-298">Substream pictures are indicated by setting the **SampleFormat.SampleFormat** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure equal to DXVA2\_SampleSubStream.</span></span> <span data-ttu-id="bdc17-299">Para o fluxo de vídeo primário, esse membro descreve o entrelaçamento do vídeo de entrada.</span><span class="sxs-lookup"><span data-stu-id="bdc17-299">For the primary video stream, this member describes the interlacing of the input video.</span></span> <span data-ttu-id="bdc17-300">Para obter mais informações, consulte Enumeração do [**DXVA2 \_ SampleFormat**](/windows/desktop/api/dxva2api/ne-dxva2api-dxva2_sampleformat) .</span><span class="sxs-lookup"><span data-stu-id="bdc17-300">For more information, see [**DXVA2\_SampleFormat**](/windows/desktop/api/dxva2api/ne-dxva2api-dxva2_sampleformat) enumeration.</span></span>

<span data-ttu-id="bdc17-301">Para o fluxo de vídeo primário, os membros de **início** e **término** da estrutura [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) fornecem os horários de início e término do exemplo de entrada.</span><span class="sxs-lookup"><span data-stu-id="bdc17-301">For the primary video stream, the **Start** and **End** members of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure give the start and end times of the input sample.</span></span> <span data-ttu-id="bdc17-302">Para imagens de Subfluxo, defina esses valores como zero, porque a hora da apresentação é sempre calculada a partir do fluxo primário.</span><span class="sxs-lookup"><span data-stu-id="bdc17-302">For substream pictures, set these values to zero, because the presentation time is always calculated from the primary stream.</span></span> <span data-ttu-id="bdc17-303">O aplicativo é responsável por controlar quando cada imagem de Subfluxo deve ser apresentada e enviá-la para [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) no momento adequado.</span><span class="sxs-lookup"><span data-stu-id="bdc17-303">The application is responsible for tracking when each substream picture should be presented and submitting it to [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) at the proper time.</span></span>

<span data-ttu-id="bdc17-304">Dois retângulos definem como o vídeo de origem é posicionado para cada fluxo:</span><span class="sxs-lookup"><span data-stu-id="bdc17-304">Two rectangles define how the source video is positioned for each stream:</span></span>

-   <span data-ttu-id="bdc17-305">O membro **SrcRect** da estrutura [**\_ VideoSample DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) especifica o *retângulo de origem*, uma região retangular da imagem de origem que será exibida no quadro de saída composto.</span><span class="sxs-lookup"><span data-stu-id="bdc17-305">The **SrcRect** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure specifies the *source rectangle*, a rectangular region of the source picture that will appear in the composited output frame.</span></span> <span data-ttu-id="bdc17-306">Para cortar a imagem, defina-a com um valor menor que o tamanho do quadro.</span><span class="sxs-lookup"><span data-stu-id="bdc17-306">To crop the picture, set this to a value smaller than the frame size.</span></span> <span data-ttu-id="bdc17-307">Caso contrário, defina-o como igual ao tamanho do quadro.</span><span class="sxs-lookup"><span data-stu-id="bdc17-307">Otherwise, set it equal to the frame size.</span></span>
-   <span data-ttu-id="bdc17-308">O membro **DstRect** da mesma estrutura especifica o *retângulo de destino*, uma região retangular da superfície de destino onde o quadro de vídeo será exibido.</span><span class="sxs-lookup"><span data-stu-id="bdc17-308">The **DstRect** member of the same structure specifies the *destination rectangle*, a rectangular region of the destination surface where the video frame will appear.</span></span>

<span data-ttu-id="bdc17-309">O driver blits pixels do retângulo de origem para o retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="bdc17-309">The driver blits pixels from the source rectangle into the destination rectangle.</span></span> <span data-ttu-id="bdc17-310">Os dois retângulos podem ter diferentes tamanhos ou proporções; o driver dimensionará a imagem conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="bdc17-310">The two rectangles can have different sizes or aspect ratios; the driver will scale the image as needed.</span></span> <span data-ttu-id="bdc17-311">Além disso, cada fluxo de entrada pode usar um fator de dimensionamento diferente.</span><span class="sxs-lookup"><span data-stu-id="bdc17-311">Moreover, each input stream can use a different scaling factor.</span></span> <span data-ttu-id="bdc17-312">Na verdade, o dimensionamento pode ser necessário para produzir a taxa de proporção correta no quadro de saída.</span><span class="sxs-lookup"><span data-stu-id="bdc17-312">In fact, scaling might be necessary to produce the correct aspect ratio in the output frame.</span></span> <span data-ttu-id="bdc17-313">O driver não pega a taxa de proporção de pixel da origem em conta, portanto, se a imagem de origem usar pixels não quadrados, cabe ao aplicativo calcular o retângulo de destino correto.</span><span class="sxs-lookup"><span data-stu-id="bdc17-313">The driver does not take the source's pixel aspect ratio into account, so if the source image uses non-square pixels, it is up to the application to calculate the correct destination rectangle.</span></span>

<span data-ttu-id="bdc17-314">Os formatos de Subfluxo preferenciais são AYUV e AI44.</span><span class="sxs-lookup"><span data-stu-id="bdc17-314">The preferred substream formats are AYUV and AI44.</span></span> <span data-ttu-id="bdc17-315">O último é um formato de palete com 16 cores.</span><span class="sxs-lookup"><span data-stu-id="bdc17-315">The latter is a palletized format with 16 colors.</span></span> <span data-ttu-id="bdc17-316">As entradas da paleta são especificadas no membro **PAL** da estrutura [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) .</span><span class="sxs-lookup"><span data-stu-id="bdc17-316">Palette entries are specified in the **Pal** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure.</span></span> <span data-ttu-id="bdc17-317">(Se o formato de vídeo de origem for expresso originalmente como um tipo de mídia Media Foundation, as entradas da paleta serão armazenadas no atributo de [**\_ \_ paleta MF MT**](mf-mt-palette-attribute.md) .) Para formatos não paletes, limpe essa matriz para zero.</span><span class="sxs-lookup"><span data-stu-id="bdc17-317">(If your source video format is originally expressed as a Media Foundation media type, the palette entries are stored in the [**MF\_MT\_PALETTE**](mf-mt-palette-attribute.md) attribute.) For non-palletized formats, clear this array to zero.</span></span>

## <a name="image-composition"></a><span data-ttu-id="bdc17-318">Composição de imagem</span><span class="sxs-lookup"><span data-stu-id="bdc17-318">Image Composition</span></span>

<span data-ttu-id="bdc17-319">Cada operação blit é definida pelos três retângulos a seguir:</span><span class="sxs-lookup"><span data-stu-id="bdc17-319">Every blit operation is defined by the following three rectangles:</span></span>

-   <span data-ttu-id="bdc17-320">O retângulo de *destino* (**TargetRect**) define a região dentro da superfície de destino onde a saída será exibida.</span><span class="sxs-lookup"><span data-stu-id="bdc17-320">The *target* rectangle (**TargetRect**) defines the region within the destination surface where the output will appear.</span></span> <span data-ttu-id="bdc17-321">A imagem de saída é recortada para este retângulo.</span><span class="sxs-lookup"><span data-stu-id="bdc17-321">The output image is clipped to this rectangle.</span></span>
-   <span data-ttu-id="bdc17-322">O retângulo de *destino* de cada fluxo (**DstRect**) define onde o fluxo de entrada aparece na imagem compostada.</span><span class="sxs-lookup"><span data-stu-id="bdc17-322">The *destination* rectangle for each stream (**DstRect**) defines where the input stream appears in the composited image.</span></span>
-   <span data-ttu-id="bdc17-323">O retângulo de *origem* de cada fluxo (**SrcRect**) define qual parte da imagem de origem é exibida.</span><span class="sxs-lookup"><span data-stu-id="bdc17-323">The *source* rectangle for each stream (**SrcRect**) defines which part of the source image appears.</span></span>

<span data-ttu-id="bdc17-324">Os retângulos de destino e destino são especificados em relação à superfície de destino.</span><span class="sxs-lookup"><span data-stu-id="bdc17-324">The target and destination rectangles are specified relative to the destination surface.</span></span> <span data-ttu-id="bdc17-325">O retângulo de origem é especificado em relação à imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="bdc17-325">The source rectangle is specified relative to the source image.</span></span> <span data-ttu-id="bdc17-326">Todos os retângulos são especificados em pixels.</span><span class="sxs-lookup"><span data-stu-id="bdc17-326">All rectangles are specified in pixels.</span></span>

![diagrama mostrando os retângulos de origem, destino e destino](images/dxva-vp-rects.gif)

<span data-ttu-id="bdc17-328">O dispositivo de processamento de vídeo Alpha combina as imagens de entrada, usando qualquer uma das seguintes fontes de dados alfa:</span><span class="sxs-lookup"><span data-stu-id="bdc17-328">The video processing device alpha blends the input pictures, using any of the following sources of alpha data:</span></span>

-   <span data-ttu-id="bdc17-329">Dados alfa por pixel de subfluxos.</span><span class="sxs-lookup"><span data-stu-id="bdc17-329">Per-pixel alpha data from substreams.</span></span>
-   <span data-ttu-id="bdc17-330">Um valor alfa planar para cada fluxo de vídeo, especificado no membro **PlanarAlpha** da estrutura [**\_ VideoSample DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) .</span><span class="sxs-lookup"><span data-stu-id="bdc17-330">A planar alpha value for each video stream, specified in the **PlanarAlpha** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure.</span></span>
-   <span data-ttu-id="bdc17-331">O valor alfa planar da imagem compostada, especificado no membro **alfa** da estrutura [**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) .</span><span class="sxs-lookup"><span data-stu-id="bdc17-331">The planar alpha value of the composited image, specified in the **Alpha** member of the [**DXVA2\_VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) structure.</span></span> <span data-ttu-id="bdc17-332">Esse valor é usado para misturar toda a imagem composta com a cor do plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="bdc17-332">This value is used to blend the entire composited image with the background color.</span></span>

<span data-ttu-id="bdc17-333">Esta seção fornece uma série de exemplos que mostram como o dispositivo de processamento de vídeo cria a imagem de saída.</span><span class="sxs-lookup"><span data-stu-id="bdc17-333">This section gives a series of examples that show how the video processing device creates the output image.</span></span>

### <a name="example-1-letterboxing"></a><span data-ttu-id="bdc17-334">Exemplo 1: formato Letterbox</span><span class="sxs-lookup"><span data-stu-id="bdc17-334">Example 1: Letterboxing</span></span>

<span data-ttu-id="bdc17-335">Este exemplo mostra como Letterbox a imagem de origem, definindo o retângulo de destino como menor do que o retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="bdc17-335">This example shows how to letterbox the source image, by setting the destination rectangle to be smaller than the target rectangle.</span></span> <span data-ttu-id="bdc17-336">O fluxo de vídeo primário neste exemplo é uma imagem 720 × 480 e deve ser exibido com uma taxa de proporção de 16:9.</span><span class="sxs-lookup"><span data-stu-id="bdc17-336">The primary video stream in this example is a 720 × 480 image, and is meant to be displayed at a 16:9 aspect ratio.</span></span> <span data-ttu-id="bdc17-337">A superfície de destino é de 640 × 480 pixels (taxa de proporção de 4:3).</span><span class="sxs-lookup"><span data-stu-id="bdc17-337">The destination surface is 640 × 480 pixels (4:3 aspect ratio).</span></span> <span data-ttu-id="bdc17-338">Para obter a taxa de proporção correta, o retângulo de destino deve ser 640 × 360.</span><span class="sxs-lookup"><span data-stu-id="bdc17-338">To achieve the correct aspect ratio, the destination rectangle must be 640 × 360.</span></span> <span data-ttu-id="bdc17-339">Para simplificar, este exemplo não inclui um subfluxo.</span><span class="sxs-lookup"><span data-stu-id="bdc17-339">For simplicity, this example does not include a substream.</span></span> <span data-ttu-id="bdc17-340">O diagrama a seguir mostra os retângulos de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="bdc17-340">The following diagram shows the source and destination rectangles.</span></span>

![diagrama mostrando formato letterbox.](images/428105fa-a26b-48a6-991d-44d24ab786b1.gif)

<span data-ttu-id="bdc17-342">O diagrama anterior mostra os seguintes retângulos:</span><span class="sxs-lookup"><span data-stu-id="bdc17-342">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="bdc17-343">Retângulo de destino: {0, 0, 640, 480}</span><span class="sxs-lookup"><span data-stu-id="bdc17-343">Target rectangle: { 0, 0, 640, 480 }</span></span>
-   <span data-ttu-id="bdc17-344">Vídeo primário:</span><span class="sxs-lookup"><span data-stu-id="bdc17-344">Primary video:</span></span>

    -   <span data-ttu-id="bdc17-345">Retângulo de origem: {0, 0, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="bdc17-345">Source rectangle: { 0, 0, 720, 480 }</span></span>
    -   <span data-ttu-id="bdc17-346">Retângulo de destino: {0, 60, 640, 420}</span><span class="sxs-lookup"><span data-stu-id="bdc17-346">Destination rectangle: { 0, 60, 640, 420 }</span></span>

<span data-ttu-id="bdc17-347">O driver desentrelaçará o vídeo, reduzirá o quadro desentrelaçado para 640 × 360 e blit o quadro no retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="bdc17-347">The driver will deinterlace the video, shrink the deinterlaced frame to 640 × 360, and blit the frame into the destination rectangle.</span></span> <span data-ttu-id="bdc17-348">O retângulo de destino é maior que o retângulo de destino, portanto, o driver usará a cor da tela de fundo para preencher as barras horizontais acima e abaixo do quadro.</span><span class="sxs-lookup"><span data-stu-id="bdc17-348">The target rectangle is larger than the destination rectangle, so the driver will use the background color to fill the horizontal bars above and below the frame.</span></span> <span data-ttu-id="bdc17-349">A cor do plano de fundo é especificada na estrutura [**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) .</span><span class="sxs-lookup"><span data-stu-id="bdc17-349">The background color is specified in the [**DXVA2\_VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) structure.</span></span>

### <a name="example-2-stretching-substream-images"></a><span data-ttu-id="bdc17-350">Exemplo 2: alongar imagens de Subfluxo</span><span class="sxs-lookup"><span data-stu-id="bdc17-350">Example 2: Stretching Substream Images</span></span>

<span data-ttu-id="bdc17-351">As imagens de Subfluxo podem se estender além da imagem de vídeo principal.</span><span class="sxs-lookup"><span data-stu-id="bdc17-351">Substream pictures can extend beyond the primary video picture.</span></span> <span data-ttu-id="bdc17-352">No vídeo em DVD, por exemplo, o fluxo de vídeo primário pode ter uma taxa de proporção de 4:3, enquanto o Subfluxo é 16:9.</span><span class="sxs-lookup"><span data-stu-id="bdc17-352">In DVD video, for example, the primary video stream can have a 4:3 aspect ratio while the substream is 16:9.</span></span> <span data-ttu-id="bdc17-353">Neste exemplo, ambos os fluxos de vídeo têm as mesmas dimensões de origem (720 × 480), mas o Subfluxo destina-se a ser mostrado com uma taxa de proporção de 16:9.</span><span class="sxs-lookup"><span data-stu-id="bdc17-353">In this example, both video streams have the same source dimensions (720 × 480), but the substream is intended to be shown at a 16:9 aspect ratio.</span></span> <span data-ttu-id="bdc17-354">Para obter essa taxa de proporção, a imagem de Subfluxo é esticada horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="bdc17-354">To achieve this aspect ratio, the substream image is stretched horizontally.</span></span> <span data-ttu-id="bdc17-355">Os retângulos de origem e de destino são mostrados no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="bdc17-355">The source and destination rectangles are shown in the following diagram.</span></span>

![diagrama mostrando o alongamento da imagem de Subfluxo.](images/7ab31c65-06b9-4843-90b8-2f9fb6f6b20e.gif)

<span data-ttu-id="bdc17-357">O diagrama anterior mostra os seguintes retângulos:</span><span class="sxs-lookup"><span data-stu-id="bdc17-357">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="bdc17-358">Retângulo de destino: {0, 0, 854, 480}</span><span class="sxs-lookup"><span data-stu-id="bdc17-358">Target rectangle: { 0, 0, 854, 480 }</span></span>
-   <span data-ttu-id="bdc17-359">Vídeo primário:</span><span class="sxs-lookup"><span data-stu-id="bdc17-359">Primary video:</span></span>

    -   <span data-ttu-id="bdc17-360">Retângulo de origem: {0, 0, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="bdc17-360">Source rectangle: { 0, 0, 720, 480 }</span></span>
    -   <span data-ttu-id="bdc17-361">Retângulo de destino: {0, 107, 474, 480}</span><span class="sxs-lookup"><span data-stu-id="bdc17-361">Destination rectangle: { 0, 107, 474, 480 }</span></span>

-   <span data-ttu-id="bdc17-362">Subfluxo</span><span class="sxs-lookup"><span data-stu-id="bdc17-362">Substream:</span></span>
    -   <span data-ttu-id="bdc17-363">Retângulo de origem: {0, 0, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="bdc17-363">Source rectangle: { 0, 0, 720, 480 }</span></span>
    -   <span data-ttu-id="bdc17-364">Retângulo de destino: {0, 0, 854, 480}</span><span class="sxs-lookup"><span data-stu-id="bdc17-364">Destination rectangle: { 0, 0, 854, 480 }</span></span>

<span data-ttu-id="bdc17-365">Esses valores preservam a altura da imagem e dimensionam as imagens horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="bdc17-365">These values preserve the image height and scale both images horizontally.</span></span> <span data-ttu-id="bdc17-366">Nas regiões em que as duas imagens aparecem, elas são alfa misturadas.</span><span class="sxs-lookup"><span data-stu-id="bdc17-366">In the regions where both images appear, they are alpha blended.</span></span> <span data-ttu-id="bdc17-367">Onde a imagem de Subfluxo ultrapassa o vídeo primária, o Subfluxo é alfa misturado com a cor do plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="bdc17-367">Where the substream picture exends beyond the primay video, the substream is alpha blended with the background color.</span></span> <span data-ttu-id="bdc17-368">Essas contas de mesclagem alfa para as cores alteradas no lado direito do diagrama.</span><span class="sxs-lookup"><span data-stu-id="bdc17-368">This alpha blending accounts for the altered colors in the right-hand side of the diagram.</span></span>

### <a name="example-3-mismatched-stream-heights"></a><span data-ttu-id="bdc17-369">Exemplo 3: alturas de fluxo incompatíveis</span><span class="sxs-lookup"><span data-stu-id="bdc17-369">Example 3: Mismatched Stream Heights</span></span>

<span data-ttu-id="bdc17-370">No exemplo anterior, o Subfluxo e o fluxo principal têm a mesma altura.</span><span class="sxs-lookup"><span data-stu-id="bdc17-370">In the previous example, the substream and the primary stream are the same height.</span></span> <span data-ttu-id="bdc17-371">Os fluxos também podem ter alturas incompatíveis, conforme mostrado neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="bdc17-371">Streams can also have mismatched heights, as shown in this example.</span></span> <span data-ttu-id="bdc17-372">As áreas dentro do retângulo de destino onde nenhum vídeo é exibido são desenhadas usando a cor do plano de fundo — preto neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="bdc17-372">Areas within the target rectangle where no video appears are drawn using the background color—black in this example.</span></span> <span data-ttu-id="bdc17-373">Os retângulos de origem e de destino são mostrados no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="bdc17-373">The source and destination rectangles are shown in the following diagram.</span></span>

![diagrama mostrando alturas de fluxo incompatíveis,](images/0190a15a-d971-450f-90ed-ce5633e1069c.gif)

<span data-ttu-id="bdc17-375">O diagrama anterior mostra os seguintes retângulos:</span><span class="sxs-lookup"><span data-stu-id="bdc17-375">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="bdc17-376">Retângulo de destino: {0, 0, 150, 85}</span><span class="sxs-lookup"><span data-stu-id="bdc17-376">Target rectangle: { 0, 0, 150, 85 }</span></span>
-   <span data-ttu-id="bdc17-377">Vídeo primário:</span><span class="sxs-lookup"><span data-stu-id="bdc17-377">Primary video:</span></span>
    -   <span data-ttu-id="bdc17-378">Retângulo de origem: {0, 0, 150, 50}</span><span class="sxs-lookup"><span data-stu-id="bdc17-378">Source rectangle: { 0, 0, 150, 50 }</span></span>
    -   <span data-ttu-id="bdc17-379">Retângulo de destino: {0, 17, 150, 67}</span><span class="sxs-lookup"><span data-stu-id="bdc17-379">Destination rectangle: { 0, 17, 150, 67 }</span></span>
-   <span data-ttu-id="bdc17-380">Subfluxo</span><span class="sxs-lookup"><span data-stu-id="bdc17-380">Substream:</span></span>
    -   <span data-ttu-id="bdc17-381">Retângulo de origem: {0, 0, 100, 85}</span><span class="sxs-lookup"><span data-stu-id="bdc17-381">Source rectangle: { 0, 0, 100, 85 }</span></span>
    -   <span data-ttu-id="bdc17-382">Retângulo de destino: {25, 0, 125, 85}</span><span class="sxs-lookup"><span data-stu-id="bdc17-382">Destination rectangle: { 25, 0, 125, 85 }</span></span>

### <a name="example-4-target-rectangle-smaller-than-destination-surface"></a><span data-ttu-id="bdc17-383">Exemplo 4: retângulo de destino menor que superfície de destino</span><span class="sxs-lookup"><span data-stu-id="bdc17-383">Example 4: Target Rectangle Smaller Than Destination Surface</span></span>

<span data-ttu-id="bdc17-384">Este exemplo mostra um caso em que o retângulo de destino é menor do que a superfície de destino.</span><span class="sxs-lookup"><span data-stu-id="bdc17-384">This example shows a case where the target rectangle is smaller than the destination surface.</span></span>

![diagrama mostrando um blit para um retângulo de destino.](images/360a85a3-333c-4b32-b8f7-1beb1e805921.gif)

<span data-ttu-id="bdc17-386">O diagrama anterior mostra os seguintes retângulos:</span><span class="sxs-lookup"><span data-stu-id="bdc17-386">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="bdc17-387">Superfície de destino: {0, 0, 300, 200}</span><span class="sxs-lookup"><span data-stu-id="bdc17-387">Destination surface: { 0, 0, 300, 200 }</span></span>
-   <span data-ttu-id="bdc17-388">Retângulo de destino: {0, 0, 150, 85}</span><span class="sxs-lookup"><span data-stu-id="bdc17-388">Target rectangle: { 0, 0, 150, 85 }</span></span>
-   <span data-ttu-id="bdc17-389">Vídeo primário:</span><span class="sxs-lookup"><span data-stu-id="bdc17-389">Primary video:</span></span>
    -   <span data-ttu-id="bdc17-390">Retângulo de origem: {0, 0, 150, 50}</span><span class="sxs-lookup"><span data-stu-id="bdc17-390">Source rectangle: { 0, 0, 150, 50 }</span></span>
    -   <span data-ttu-id="bdc17-391">Retângulo de destino: {0, 17, 150, 67}</span><span class="sxs-lookup"><span data-stu-id="bdc17-391">Destination rectangle: { 0, 17, 150, 67 }</span></span>
-   <span data-ttu-id="bdc17-392">Subfluxo</span><span class="sxs-lookup"><span data-stu-id="bdc17-392">Substream:</span></span>
    -   <span data-ttu-id="bdc17-393">Retângulo de origem: {0, 0, 100, 85}</span><span class="sxs-lookup"><span data-stu-id="bdc17-393">Source rectangle: { 0, 0, 100, 85 }</span></span>
    -   <span data-ttu-id="bdc17-394">Retângulo de destino: {25, 0, 125, 85}</span><span class="sxs-lookup"><span data-stu-id="bdc17-394">Destination rectangle: { 25, 0, 125, 85 }</span></span>

<span data-ttu-id="bdc17-395">Os pixels fora do retângulo de destino não são modificados, portanto, a cor do plano de fundo aparece apenas dentro do retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="bdc17-395">Pixels outside of the target rectangle are not modified, so the background color appears only within the target rectangle.</span></span> <span data-ttu-id="bdc17-396">A área pontilhada indica partes da superfície de destino que não são afetadas pelo blit.</span><span class="sxs-lookup"><span data-stu-id="bdc17-396">The dotted area indicates portions of the destination surface that are not affected by the blit.</span></span>

### <a name="example-5-source-rectangles"></a><span data-ttu-id="bdc17-397">Exemplo 5: retângulos de origem</span><span class="sxs-lookup"><span data-stu-id="bdc17-397">Example 5: Source Rectangles</span></span>

<span data-ttu-id="bdc17-398">Se você especificar um retângulo de origem menor do que a imagem de origem, o driver blitrá apenas essa parte da imagem.</span><span class="sxs-lookup"><span data-stu-id="bdc17-398">If you specify a source rectangle that is smaller than the source picture, the driver will blit just that portion of the picture.</span></span> <span data-ttu-id="bdc17-399">Neste exemplo, os retângulos de origem especificam o quadrante inferior direito do fluxo de vídeo primário e o quadrante inferior esquerdo do Subfluxo (indicado pelas marcas de hash no diagrama).</span><span class="sxs-lookup"><span data-stu-id="bdc17-399">In this example, the source rectangles specify the lower-right quadrant of the primary video stream and the lower-left quadrant of the substream (indicated by hash marks in the diagram).</span></span> <span data-ttu-id="bdc17-400">Os retângulos de destino são os mesmos tamanhos que os retângulos de origem, portanto, o vídeo não é ampliado.</span><span class="sxs-lookup"><span data-stu-id="bdc17-400">The destination rectangles are the same sizes as the source rectangles, so the video is not stretched.</span></span> <span data-ttu-id="bdc17-401">Os retângulos de origem e de destino são mostrados no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="bdc17-401">The source and destination rectangles are shown in the following diagram.</span></span>

![diagrama mostrando um blit de dois retângulos de origem.](images/b1de4cc3-0155-40be-acac-b486e2af8c0d.gif)

<span data-ttu-id="bdc17-403">O diagrama anterior mostra os seguintes retângulos:</span><span class="sxs-lookup"><span data-stu-id="bdc17-403">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="bdc17-404">Retângulo de destino: {0, 0, 720, 576}</span><span class="sxs-lookup"><span data-stu-id="bdc17-404">Target rectangle: { 0, 0, 720, 576 }</span></span>
-   <span data-ttu-id="bdc17-405">Vídeo primário:</span><span class="sxs-lookup"><span data-stu-id="bdc17-405">Primary video:</span></span>
    -   <span data-ttu-id="bdc17-406">Tamanho da superfície de origem: {0, 0, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="bdc17-406">Source surface size: { 0, 0, 720, 480 }</span></span>
    -   <span data-ttu-id="bdc17-407">Retângulo de origem: {360, 240, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="bdc17-407">Source rectangle: { 360, 240, 720, 480 }</span></span>
    -   <span data-ttu-id="bdc17-408">Retângulo de destino: {0, 0, 360, 240}</span><span class="sxs-lookup"><span data-stu-id="bdc17-408">Destination rectangle: { 0, 0, 360, 240 }</span></span>
-   <span data-ttu-id="bdc17-409">Subfluxo</span><span class="sxs-lookup"><span data-stu-id="bdc17-409">Substream:</span></span>
    -   <span data-ttu-id="bdc17-410">Tamanho da superfície de origem: {0, 0, 640, 576}</span><span class="sxs-lookup"><span data-stu-id="bdc17-410">Source surface size: { 0, 0, 640, 576 }</span></span>
    -   <span data-ttu-id="bdc17-411">Retângulo de origem: {0, 288, 320, 576}</span><span class="sxs-lookup"><span data-stu-id="bdc17-411">Source rectangle: { 0, 288, 320, 576 }</span></span>
    -   <span data-ttu-id="bdc17-412">Retângulo de destino: {400, 0, 720, 288}</span><span class="sxs-lookup"><span data-stu-id="bdc17-412">Destination rectangle: { 400, 0, 720, 288 }</span></span>

### <a name="example-6-intersecting-destination-rectangles"></a><span data-ttu-id="bdc17-413">Exemplo 6: retângulos de destino com interseção</span><span class="sxs-lookup"><span data-stu-id="bdc17-413">Example 6: Intersecting Destination Rectangles</span></span>

<span data-ttu-id="bdc17-414">Este exemplo é semelhante ao anterior, mas os retângulos de destino se cruzam.</span><span class="sxs-lookup"><span data-stu-id="bdc17-414">This example is similar to previous one, but the destination rectangles intersect.</span></span> <span data-ttu-id="bdc17-415">As dimensões da superfície são as mesmas do exemplo anterior, mas os retângulos de origem e de destino não são.</span><span class="sxs-lookup"><span data-stu-id="bdc17-415">The surface dimensions are the same as in the previous example, but the source and destination rectangles are not.</span></span> <span data-ttu-id="bdc17-416">Novamente, o vídeo é cortado, mas não ampliado.</span><span class="sxs-lookup"><span data-stu-id="bdc17-416">Again, the video is cropped but not stretched.</span></span> <span data-ttu-id="bdc17-417">Os retângulos de origem e de destino são mostrados no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="bdc17-417">The source and destination rectangles are shown in the following diagram.</span></span>

![diagrama mostrando retângulos de destino de interseção.](images/fbe450cb-c84d-4110-9515-00f27601528e.gif)

<span data-ttu-id="bdc17-419">O diagrama anterior mostra os seguintes retângulos:</span><span class="sxs-lookup"><span data-stu-id="bdc17-419">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="bdc17-420">Retângulo de destino: {0, 0, 720, 576}</span><span class="sxs-lookup"><span data-stu-id="bdc17-420">Target rectangle: { 0, 0, 720, 576 }</span></span>
-   <span data-ttu-id="bdc17-421">Vídeo primário:</span><span class="sxs-lookup"><span data-stu-id="bdc17-421">Primary video:</span></span>
    -   <span data-ttu-id="bdc17-422">Tamanho da superfície de origem: {0, 0, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="bdc17-422">Source surface size: { 0, 0, 720, 480 }</span></span>
    -   <span data-ttu-id="bdc17-423">Retângulo de origem: {260, 92, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="bdc17-423">Source rectangle: { 260, 92, 720, 480 }</span></span>
    -   <span data-ttu-id="bdc17-424">Retângulo de destino: {0, 0, 460, 388}</span><span class="sxs-lookup"><span data-stu-id="bdc17-424">Destination rectangle: { 0, 0, 460, 388 }</span></span>
-   <span data-ttu-id="bdc17-425">Subfluxo</span><span class="sxs-lookup"><span data-stu-id="bdc17-425">Substream:</span></span>
    -   <span data-ttu-id="bdc17-426">Tamanho da superfície de origem: {0, 0, 640, 576}</span><span class="sxs-lookup"><span data-stu-id="bdc17-426">Source surface size: { 0, 0, 640, 576 }</span></span>
    -   <span data-ttu-id="bdc17-427">Retângulo de origem: {0, 0, 460, 388}</span><span class="sxs-lookup"><span data-stu-id="bdc17-427">Source rectangle: { 0, 0, 460, 388 }</span></span>
    -   <span data-ttu-id="bdc17-428">Retângulo de destino: {260, 188, 720, 576}</span><span class="sxs-lookup"><span data-stu-id="bdc17-428">Destination rectangle: { 260, 188, 720, 576 }</span></span>

### <a name="example-7-stretching-and-cropping-video"></a><span data-ttu-id="bdc17-429">Exemplo 7: alongando e cortando vídeo</span><span class="sxs-lookup"><span data-stu-id="bdc17-429">Example 7: Stretching and Cropping Video</span></span>

<span data-ttu-id="bdc17-430">Neste exemplo, o vídeo é alongado, bem como cortado.</span><span class="sxs-lookup"><span data-stu-id="bdc17-430">In this example, the video is stretched as well as cropped.</span></span> <span data-ttu-id="bdc17-431">Uma região 180 × 120 de cada fluxo é ampliada para cobrir uma área 360 × 240 no retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="bdc17-431">A 180 × 120 region from each stream is stretched to cover a 360 × 240 area in the destination rectangle.</span></span>

![diagrama mostrando alongamento e corte.](images/ce83529c-8545-492c-9d3e-ef221c30e326.gif)

<span data-ttu-id="bdc17-433">O diagrama anterior mostra os seguintes retângulos:</span><span class="sxs-lookup"><span data-stu-id="bdc17-433">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="bdc17-434">Retângulo de destino: {0, 0, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="bdc17-434">Target rectangle: { 0, 0, 720, 480 }</span></span>
-   <span data-ttu-id="bdc17-435">Vídeo primário:</span><span class="sxs-lookup"><span data-stu-id="bdc17-435">Primary video:</span></span>
    -   <span data-ttu-id="bdc17-436">Tamanho da superfície de origem: {0, 0, 360, 240}</span><span class="sxs-lookup"><span data-stu-id="bdc17-436">Source surface size: { 0, 0, 360, 240 }</span></span>
    -   <span data-ttu-id="bdc17-437">Retângulo de origem: {180, 120, 360, 240}</span><span class="sxs-lookup"><span data-stu-id="bdc17-437">Source rectangle: { 180, 120, 360, 240 }</span></span>
    -   <span data-ttu-id="bdc17-438">Retângulo de destino: {0, 0, 360, 240}</span><span class="sxs-lookup"><span data-stu-id="bdc17-438">Destination rectangle: { 0, 0, 360, 240 }</span></span>
-   <span data-ttu-id="bdc17-439">Subfluxo</span><span class="sxs-lookup"><span data-stu-id="bdc17-439">Substream:</span></span>
    -   <span data-ttu-id="bdc17-440">Tamanho da superfície de origem: {0, 0, 360, 240}</span><span class="sxs-lookup"><span data-stu-id="bdc17-440">Source surface size: { 0, 0, 360, 240 }</span></span>
    -   <span data-ttu-id="bdc17-441">Retângulo de origem: {0, 0, 180, 120}</span><span class="sxs-lookup"><span data-stu-id="bdc17-441">Source rectangle: { 0, 0, 180, 120 }</span></span>
    -   <span data-ttu-id="bdc17-442">Retângulo de destino: {360, 240, 720, 480}</span><span class="sxs-lookup"><span data-stu-id="bdc17-442">Destination rectangle: { 360, 240, 720, 480 }</span></span>

## <a name="input-sample-order"></a><span data-ttu-id="bdc17-443">Ordem de amostra de entrada</span><span class="sxs-lookup"><span data-stu-id="bdc17-443">Input Sample Order</span></span>

<span data-ttu-id="bdc17-444">O parâmetro *pSamples* do método [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) é um ponteiro para uma matriz de exemplos de entrada.</span><span class="sxs-lookup"><span data-stu-id="bdc17-444">The *pSamples* parameter of the [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) method is a pointer to an array of input samples.</span></span> <span data-ttu-id="bdc17-445">Os exemplos do fluxo de vídeo primário aparecem primeiro, seguidos pelas imagens de Subfluxo na ordem Z.</span><span class="sxs-lookup"><span data-stu-id="bdc17-445">Samples from the primary video stream appear first, followed by substream pictures in Z-order.</span></span> <span data-ttu-id="bdc17-446">Os exemplos devem ser colocados na matriz na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="bdc17-446">Samples must be placed into the array in the following order:</span></span>

-   <span data-ttu-id="bdc17-447">Os exemplos do fluxo de vídeo primário aparecem primeiro na matriz, em ordem temporal.</span><span class="sxs-lookup"><span data-stu-id="bdc17-447">Samples for the primary video stream appear first in the array, in temporal order.</span></span> <span data-ttu-id="bdc17-448">Dependendo do modo de desentrelaçamento, o driver pode exigir um ou mais exemplos de referência do fluxo de vídeo primário.</span><span class="sxs-lookup"><span data-stu-id="bdc17-448">Depending on the deinterlace mode, the driver may require one or more reference samples from the primary video stream.</span></span> <span data-ttu-id="bdc17-449">Os membros **NumForwardRefSamples** e **NumBackwardRefSamples** da estrutura [**DXVA2 \_ VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) especificam quantas amostras de referência para frente e para trás são necessárias.</span><span class="sxs-lookup"><span data-stu-id="bdc17-449">The **NumForwardRefSamples** and **NumBackwardRefSamples** members of the [**DXVA2\_VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) structure specify how many forward and backward reference samples are needed.</span></span> <span data-ttu-id="bdc17-450">O chamador deve fornecer esses exemplos de referência, mesmo se o conteúdo do vídeo for progressivo e não exigir desentrelaçamento.</span><span class="sxs-lookup"><span data-stu-id="bdc17-450">The caller must provide these reference samples even if the video content is progressive and does not require deinterlacing.</span></span> <span data-ttu-id="bdc17-451">(Isso pode ocorrer quando os quadros progressivos são fornecidos a um dispositivo de desentrelaçamento, por exemplo, quando a origem contém uma mistura de quadros entrelaçados e progressivos.)</span><span class="sxs-lookup"><span data-stu-id="bdc17-451">(This can occur when progressive frames are given to a deinterlacing device, for example when the source contains a mix of both interlaced and progressive frames.)</span></span>
-   <span data-ttu-id="bdc17-452">Após os exemplos do fluxo de vídeo primário, a matriz pode conter até 15 amostras de Subfluxo, organizadas em ordem Z, de baixo para cima.</span><span class="sxs-lookup"><span data-stu-id="bdc17-452">After the samples for the primary video stream, the array can contain up to 15 substream samples, arranged in Z-order, from bottom to top.</span></span> <span data-ttu-id="bdc17-453">Os subfluxos são sempre progressivos e não exigem imagens de referência.</span><span class="sxs-lookup"><span data-stu-id="bdc17-453">Substreams are always progressive and do not require reference pictures.</span></span>

<span data-ttu-id="bdc17-454">A qualquer momento, o fluxo de vídeo primário pode alternar entre conteúdo entrelaçado e progressivo, e o número de subfluxos pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="bdc17-454">At any time, the primary video stream can switch between interlaced and progressive content, and the number of substreams can change.</span></span>

<span data-ttu-id="bdc17-455">O membro **SampleFormat. SampleFormat** da estrutura [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) indica o tipo de imagem.</span><span class="sxs-lookup"><span data-stu-id="bdc17-455">The **SampleFormat.SampleFormat** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure indicates the type of picture.</span></span> <span data-ttu-id="bdc17-456">Para imagens de Subfluxo, defina esse valor como DXVA2 \_ SampleSubStream.</span><span class="sxs-lookup"><span data-stu-id="bdc17-456">For substream pictures, set this value to DXVA2\_SampleSubStream.</span></span> <span data-ttu-id="bdc17-457">Para imagens progressivas, o valor é DXVA2 \_ SampleProgressiveFrame.</span><span class="sxs-lookup"><span data-stu-id="bdc17-457">For progressive pictures, the value is DXVA2\_SampleProgressiveFrame.</span></span> <span data-ttu-id="bdc17-458">Para imagens entrelaçadas, o valor depende do layout do campo.</span><span class="sxs-lookup"><span data-stu-id="bdc17-458">For interlaced pictures, the value depends on the field layout.</span></span>

<span data-ttu-id="bdc17-459">Se o driver exigir amostras de referência para frente e para trás, o número completo de amostras poderá não estar disponível no início da sequência de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bdc17-459">If the driver requires forward and backward reference samples, the full number of samples might not be available at the start of the video sequence.</span></span> <span data-ttu-id="bdc17-460">Nesse caso, inclua entradas para elas na matriz *pSamples* , mas marque os exemplos ausentes como tendo o tipo DXVA2 \_ SampleUnknown.</span><span class="sxs-lookup"><span data-stu-id="bdc17-460">In that case, include entries for them in the *pSamples* array, but mark the missing samples as having type DXVA2\_SampleUnknown.</span></span>

<span data-ttu-id="bdc17-461">Os membros **inicial** e **final** da estrutura [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) fornecem o local temporal de cada amostra.</span><span class="sxs-lookup"><span data-stu-id="bdc17-461">The **Start** and **End** members of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure give the temporal location of each sample.</span></span> <span data-ttu-id="bdc17-462">Esses valores são usados apenas para exemplos do fluxo de vídeo primário.</span><span class="sxs-lookup"><span data-stu-id="bdc17-462">These values are used only for samples from the primary video stream.</span></span> <span data-ttu-id="bdc17-463">Para imagens de Subfluxo, defina ambos os membros como zero.</span><span class="sxs-lookup"><span data-stu-id="bdc17-463">For substream pictures, set both members to zero.</span></span>

<span data-ttu-id="bdc17-464">Os exemplos a seguir podem ajudar a esclarecer esses requisitos.</span><span class="sxs-lookup"><span data-stu-id="bdc17-464">The following examples may help to clarify these requirements.</span></span>

### <a name="example-1"></a><span data-ttu-id="bdc17-465">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bdc17-465">Example 1</span></span>

<span data-ttu-id="bdc17-466">O caso mais simples ocorre quando não há subfluxos e o algoritmo de desentrelaçamento não requer exemplos de referência (**NumForwardRefSamples** e **NumBackwardRefSamples** são ambos zero).</span><span class="sxs-lookup"><span data-stu-id="bdc17-466">The simplest case occurs when there are no substreams and the deinterlacing algorithm does not require reference samples (**NumForwardRefSamples** and **NumBackwardRefSamples** are both zero).</span></span> <span data-ttu-id="bdc17-467">Bob desentrelaçado é um exemplo desse algoritmo.</span><span class="sxs-lookup"><span data-stu-id="bdc17-467">Bob deinterlacing is an example of such an algorithm.</span></span> <span data-ttu-id="bdc17-468">Nesse caso, a matriz *pSamples* deve conter uma única superfície de entrada, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="bdc17-468">In this case, the *pSamples* array should contain a single input surface, as shown in the following table.</span></span>



| <span data-ttu-id="bdc17-469">Índice</span><span class="sxs-lookup"><span data-stu-id="bdc17-469">Index</span></span>           | <span data-ttu-id="bdc17-470">Tipo de superfície</span><span class="sxs-lookup"><span data-stu-id="bdc17-470">Surface type</span></span>        | <span data-ttu-id="bdc17-471">Local temporal</span><span class="sxs-lookup"><span data-stu-id="bdc17-471">Temporal location</span></span> |
|-----------------|---------------------|-------------------|
| <span data-ttu-id="bdc17-472">*pSamples* \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="bdc17-472">*pSamples*\[0\]</span></span> | <span data-ttu-id="bdc17-473">Imagem entrelaçada.</span><span class="sxs-lookup"><span data-stu-id="bdc17-473">Interlaced picture.</span></span> | <span data-ttu-id="bdc17-474">*T*</span><span class="sxs-lookup"><span data-stu-id="bdc17-474">*T*</span></span>               |



 

<span data-ttu-id="bdc17-475">O valor de hora *T* é considerado como a hora de início do quadro de vídeo atual.</span><span class="sxs-lookup"><span data-stu-id="bdc17-475">The time value *T* is assumed to be the start time of the current video frame.</span></span>

### <a name="example-2"></a><span data-ttu-id="bdc17-476">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="bdc17-476">Example 2</span></span>

<span data-ttu-id="bdc17-477">Neste exemplo, o aplicativo combina dois subfluxos com o fluxo principal.</span><span class="sxs-lookup"><span data-stu-id="bdc17-477">In this example, the application mixes two substreams with the primary stream.</span></span> <span data-ttu-id="bdc17-478">O algoritmo de desentrelaçamento não requer exemplos de referência.</span><span class="sxs-lookup"><span data-stu-id="bdc17-478">The deinterlacing algorithm does not require reference samples.</span></span> <span data-ttu-id="bdc17-479">A tabela a seguir mostra como esses exemplos são organizados na matriz *pSamples* .</span><span class="sxs-lookup"><span data-stu-id="bdc17-479">The following table shows how these samples are arranged in the *pSamples* array.</span></span>



| <span data-ttu-id="bdc17-480">Índice</span><span class="sxs-lookup"><span data-stu-id="bdc17-480">Index</span></span>           | <span data-ttu-id="bdc17-481">Tipo de superfície</span><span class="sxs-lookup"><span data-stu-id="bdc17-481">Surface type</span></span>       | <span data-ttu-id="bdc17-482">Local temporal</span><span class="sxs-lookup"><span data-stu-id="bdc17-482">Temporal location</span></span> | <span data-ttu-id="bdc17-483">Ordem z</span><span class="sxs-lookup"><span data-stu-id="bdc17-483">Z-order</span></span> |
|-----------------|--------------------|-------------------|---------|
| <span data-ttu-id="bdc17-484">*pSamples* \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="bdc17-484">*pSamples*\[0\]</span></span> | <span data-ttu-id="bdc17-485">Imagem entrelaçada</span><span class="sxs-lookup"><span data-stu-id="bdc17-485">Interlaced picture</span></span> | <span data-ttu-id="bdc17-486">*T*</span><span class="sxs-lookup"><span data-stu-id="bdc17-486">*T*</span></span>               | <span data-ttu-id="bdc17-487">0</span><span class="sxs-lookup"><span data-stu-id="bdc17-487">0</span></span>       |
| <span data-ttu-id="bdc17-488">*pSamples* \[ uma\]</span><span class="sxs-lookup"><span data-stu-id="bdc17-488">*pSamples*\[1\]</span></span> | <span data-ttu-id="bdc17-489">Subfluxo</span><span class="sxs-lookup"><span data-stu-id="bdc17-489">Substream</span></span>          | <span data-ttu-id="bdc17-490">0</span><span class="sxs-lookup"><span data-stu-id="bdc17-490">0</span></span>                 | <span data-ttu-id="bdc17-491">1</span><span class="sxs-lookup"><span data-stu-id="bdc17-491">1</span></span>       |
| <span data-ttu-id="bdc17-492">*pSamples* \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="bdc17-492">*pSamples*\[2\]</span></span> | <span data-ttu-id="bdc17-493">Subfluxo</span><span class="sxs-lookup"><span data-stu-id="bdc17-493">Substream</span></span>          | <span data-ttu-id="bdc17-494">0</span><span class="sxs-lookup"><span data-stu-id="bdc17-494">0</span></span>                 | <span data-ttu-id="bdc17-495">2</span><span class="sxs-lookup"><span data-stu-id="bdc17-495">2</span></span>       |



 

### <a name="example-3"></a><span data-ttu-id="bdc17-496">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="bdc17-496">Example 3</span></span>

<span data-ttu-id="bdc17-497">Agora suponha que o algoritmo de desentrelaçamento exija um exemplo de referência retroativa e um exemplo de referência de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="bdc17-497">Now suppose that the deinterlacing algorithm requires one backward reference sample and one forward reference sample.</span></span> <span data-ttu-id="bdc17-498">Além disso, duas imagens de Subfluxo são fornecidas, para um total de cinco superfícies.</span><span class="sxs-lookup"><span data-stu-id="bdc17-498">In addition, two substream pictures are provided, for a total of five surfaces.</span></span> <span data-ttu-id="bdc17-499">A ordenação correta é mostrada na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="bdc17-499">The correct ordering is shown in the following table.</span></span>



| <span data-ttu-id="bdc17-500">Índice</span><span class="sxs-lookup"><span data-stu-id="bdc17-500">Index</span></span>           | <span data-ttu-id="bdc17-501">Tipo de superfície</span><span class="sxs-lookup"><span data-stu-id="bdc17-501">Surface type</span></span>                   | <span data-ttu-id="bdc17-502">Local temporal</span><span class="sxs-lookup"><span data-stu-id="bdc17-502">Temporal location</span></span> | <span data-ttu-id="bdc17-503">Ordem z</span><span class="sxs-lookup"><span data-stu-id="bdc17-503">Z-order</span></span>        |
|-----------------|--------------------------------|-------------------|----------------|
| <span data-ttu-id="bdc17-504">*pSamples* \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="bdc17-504">*pSamples*\[0\]</span></span> | <span data-ttu-id="bdc17-505">Imagem entrelaçada (referência)</span><span class="sxs-lookup"><span data-stu-id="bdc17-505">Interlaced picture (reference)</span></span> | <span data-ttu-id="bdc17-506">*T* − 1</span><span class="sxs-lookup"><span data-stu-id="bdc17-506">*T* −1</span></span>            | <span data-ttu-id="bdc17-507">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="bdc17-507">Not applicable</span></span> |
| <span data-ttu-id="bdc17-508">*pSamples* \[ uma\]</span><span class="sxs-lookup"><span data-stu-id="bdc17-508">*pSamples*\[1\]</span></span> | <span data-ttu-id="bdc17-509">Imagem entrelaçada</span><span class="sxs-lookup"><span data-stu-id="bdc17-509">Interlaced picture</span></span>             | <span data-ttu-id="bdc17-510">*T*</span><span class="sxs-lookup"><span data-stu-id="bdc17-510">*T*</span></span>               | <span data-ttu-id="bdc17-511">0</span><span class="sxs-lookup"><span data-stu-id="bdc17-511">0</span></span>              |
| <span data-ttu-id="bdc17-512">*pSamples* \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="bdc17-512">*pSamples*\[2\]</span></span> | <span data-ttu-id="bdc17-513">Imagem entrelaçada (referência)</span><span class="sxs-lookup"><span data-stu-id="bdc17-513">Interlaced picture (reference)</span></span> | <span data-ttu-id="bdc17-514">*T* + 1</span><span class="sxs-lookup"><span data-stu-id="bdc17-514">*T* +1</span></span>            | <span data-ttu-id="bdc17-515">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="bdc17-515">Not applicable</span></span> |
| <span data-ttu-id="bdc17-516">*pSamples* \[ Beta\]</span><span class="sxs-lookup"><span data-stu-id="bdc17-516">*pSamples*\[3\]</span></span> | <span data-ttu-id="bdc17-517">Subfluxo</span><span class="sxs-lookup"><span data-stu-id="bdc17-517">Substream</span></span>                      | <span data-ttu-id="bdc17-518">0</span><span class="sxs-lookup"><span data-stu-id="bdc17-518">0</span></span>                 | <span data-ttu-id="bdc17-519">1</span><span class="sxs-lookup"><span data-stu-id="bdc17-519">1</span></span>              |
| <span data-ttu-id="bdc17-520">*pSamples* \[ quatro\]</span><span class="sxs-lookup"><span data-stu-id="bdc17-520">*pSamples*\[4\]</span></span> | <span data-ttu-id="bdc17-521">Subfluxo</span><span class="sxs-lookup"><span data-stu-id="bdc17-521">Substream</span></span>                      | <span data-ttu-id="bdc17-522">0</span><span class="sxs-lookup"><span data-stu-id="bdc17-522">0</span></span>                 | <span data-ttu-id="bdc17-523">2</span><span class="sxs-lookup"><span data-stu-id="bdc17-523">2</span></span>              |



 

<span data-ttu-id="bdc17-524">A hora *T* − 1 é a hora de início do quadro antes do quadro atual e *T* + 1 é a hora de início do quadro a seguir.</span><span class="sxs-lookup"><span data-stu-id="bdc17-524">The time *T* −1 is the start time of the frame before the current frame, and *T* +1 is the start time of the following frame.</span></span>

<span data-ttu-id="bdc17-525">Se o fluxo de vídeo mudar para o conteúdo progressivo, usando o mesmo modo de desentrelaçamento, o aplicativo deverá fornecer o mesmo número de amostras, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="bdc17-525">If the video stream switches to progressive content, using the same deinterlacing mode, the application must provide the same number of samples, as shown in the following table.</span></span>



| <span data-ttu-id="bdc17-526">Índice</span><span class="sxs-lookup"><span data-stu-id="bdc17-526">Index</span></span>           | <span data-ttu-id="bdc17-527">Tipo de superfície</span><span class="sxs-lookup"><span data-stu-id="bdc17-527">Surface type</span></span>                    | <span data-ttu-id="bdc17-528">Local temporal</span><span class="sxs-lookup"><span data-stu-id="bdc17-528">Temporal location</span></span> | <span data-ttu-id="bdc17-529">Ordem z</span><span class="sxs-lookup"><span data-stu-id="bdc17-529">Z-order</span></span>        |
|-----------------|---------------------------------|-------------------|----------------|
| <span data-ttu-id="bdc17-530">*pSamples* \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="bdc17-530">*pSamples*\[0\]</span></span> | <span data-ttu-id="bdc17-531">Imagem progressiva (referência)</span><span class="sxs-lookup"><span data-stu-id="bdc17-531">Progressive picture (reference)</span></span> | <span data-ttu-id="bdc17-532">*T* − 1</span><span class="sxs-lookup"><span data-stu-id="bdc17-532">*T* −1</span></span>            | <span data-ttu-id="bdc17-533">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="bdc17-533">Not applicable</span></span> |
| <span data-ttu-id="bdc17-534">*pSamples* \[ uma\]</span><span class="sxs-lookup"><span data-stu-id="bdc17-534">*pSamples*\[1\]</span></span> | <span data-ttu-id="bdc17-535">Imagem progressiva</span><span class="sxs-lookup"><span data-stu-id="bdc17-535">Progressive picture</span></span>             | <span data-ttu-id="bdc17-536">*T*</span><span class="sxs-lookup"><span data-stu-id="bdc17-536">*T*</span></span>               | <span data-ttu-id="bdc17-537">0</span><span class="sxs-lookup"><span data-stu-id="bdc17-537">0</span></span>              |
| <span data-ttu-id="bdc17-538">*pSamples* \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="bdc17-538">*pSamples*\[2\]</span></span> | <span data-ttu-id="bdc17-539">Imagem progressiva (referência)</span><span class="sxs-lookup"><span data-stu-id="bdc17-539">Progressive picture (reference)</span></span> | <span data-ttu-id="bdc17-540">*T* + 1</span><span class="sxs-lookup"><span data-stu-id="bdc17-540">*T* +1</span></span>            | <span data-ttu-id="bdc17-541">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="bdc17-541">Not applicable</span></span> |
| <span data-ttu-id="bdc17-542">*pSamples* \[ Beta\]</span><span class="sxs-lookup"><span data-stu-id="bdc17-542">*pSamples*\[3\]</span></span> | <span data-ttu-id="bdc17-543">Subfluxo</span><span class="sxs-lookup"><span data-stu-id="bdc17-543">Substream</span></span>                       | <span data-ttu-id="bdc17-544">0</span><span class="sxs-lookup"><span data-stu-id="bdc17-544">0</span></span>                 | <span data-ttu-id="bdc17-545">1</span><span class="sxs-lookup"><span data-stu-id="bdc17-545">1</span></span>              |
| <span data-ttu-id="bdc17-546">*pSamples* \[ quatro\]</span><span class="sxs-lookup"><span data-stu-id="bdc17-546">*pSamples*\[4\]</span></span> | <span data-ttu-id="bdc17-547">Subfluxo</span><span class="sxs-lookup"><span data-stu-id="bdc17-547">Substream</span></span>                       | <span data-ttu-id="bdc17-548">0</span><span class="sxs-lookup"><span data-stu-id="bdc17-548">0</span></span>                 | <span data-ttu-id="bdc17-549">2</span><span class="sxs-lookup"><span data-stu-id="bdc17-549">2</span></span>              |



 

### <a name="example-4"></a><span data-ttu-id="bdc17-550">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="bdc17-550">Example 4</span></span>

<span data-ttu-id="bdc17-551">No início de uma sequência de vídeo, amostras de referência para frente e para trás podem não estar disponíveis.</span><span class="sxs-lookup"><span data-stu-id="bdc17-551">At the start of a video sequence, forward and backward reference samples might not be available.</span></span> <span data-ttu-id="bdc17-552">Quando isso acontece, as entradas para os exemplos ausentes são incluídas na matriz *pSamples* , com o tipo de exemplo DXVA2 \_ SampleUnknown.</span><span class="sxs-lookup"><span data-stu-id="bdc17-552">When this happens, entries for the missing samples are included in the *pSamples* array, with sample type DXVA2\_SampleUnknown.</span></span>

<span data-ttu-id="bdc17-553">Supondo que o modo de desentrelaçamento precise de um exemplo de referência posterior e de um retrocesso, as três primeiras chamadas para [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) teriam as sequências de entradas mostradas nas três tabelas a seguir.</span><span class="sxs-lookup"><span data-stu-id="bdc17-553">Assuming that the deinterlacing mode needs one forward and one backward reference sample, the first three calls to [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) would have the sequences of inputs shown in the following three tables.</span></span>



| <span data-ttu-id="bdc17-554">Índice</span><span class="sxs-lookup"><span data-stu-id="bdc17-554">Index</span></span>           | <span data-ttu-id="bdc17-555">Tipo de superfície</span><span class="sxs-lookup"><span data-stu-id="bdc17-555">Surface type</span></span>                   | <span data-ttu-id="bdc17-556">Local temporal</span><span class="sxs-lookup"><span data-stu-id="bdc17-556">Temporal location</span></span> |
|-----------------|--------------------------------|-------------------|
| <span data-ttu-id="bdc17-557">*pSamples* \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="bdc17-557">*pSamples*\[0\]</span></span> | <span data-ttu-id="bdc17-558">Unknown</span><span class="sxs-lookup"><span data-stu-id="bdc17-558">Unknown</span></span>                        | <span data-ttu-id="bdc17-559">0</span><span class="sxs-lookup"><span data-stu-id="bdc17-559">0</span></span>                 |
| <span data-ttu-id="bdc17-560">*pSamples* \[ uma\]</span><span class="sxs-lookup"><span data-stu-id="bdc17-560">*pSamples*\[1\]</span></span> | <span data-ttu-id="bdc17-561">Unknown</span><span class="sxs-lookup"><span data-stu-id="bdc17-561">Unknown</span></span>                        | <span data-ttu-id="bdc17-562">0</span><span class="sxs-lookup"><span data-stu-id="bdc17-562">0</span></span>                 |
| <span data-ttu-id="bdc17-563">*pSamples* \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="bdc17-563">*pSamples*\[2\]</span></span> | <span data-ttu-id="bdc17-564">Imagem entrelaçada (referência)</span><span class="sxs-lookup"><span data-stu-id="bdc17-564">Interlaced picture (reference)</span></span> | <span data-ttu-id="bdc17-565">*T* + 1</span><span class="sxs-lookup"><span data-stu-id="bdc17-565">*T* +1</span></span>            |



 



| <span data-ttu-id="bdc17-566">Índice</span><span class="sxs-lookup"><span data-stu-id="bdc17-566">Index</span></span>           | <span data-ttu-id="bdc17-567">Tipo de superfície</span><span class="sxs-lookup"><span data-stu-id="bdc17-567">Surface type</span></span>                   | <span data-ttu-id="bdc17-568">Local temporal</span><span class="sxs-lookup"><span data-stu-id="bdc17-568">Temporal location</span></span> |
|-----------------|--------------------------------|-------------------|
| <span data-ttu-id="bdc17-569">*pSamples* \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="bdc17-569">*pSamples*\[0\]</span></span> | <span data-ttu-id="bdc17-570">Unknown</span><span class="sxs-lookup"><span data-stu-id="bdc17-570">Unknown</span></span>                        | <span data-ttu-id="bdc17-571">0</span><span class="sxs-lookup"><span data-stu-id="bdc17-571">0</span></span>                 |
| <span data-ttu-id="bdc17-572">*pSamples* \[ uma\]</span><span class="sxs-lookup"><span data-stu-id="bdc17-572">*pSamples*\[1\]</span></span> | <span data-ttu-id="bdc17-573">Imagem entrelaçada</span><span class="sxs-lookup"><span data-stu-id="bdc17-573">Interlaced picture</span></span>             | <span data-ttu-id="bdc17-574">*T*</span><span class="sxs-lookup"><span data-stu-id="bdc17-574">*T*</span></span>               |
| <span data-ttu-id="bdc17-575">*pSamples* \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="bdc17-575">*pSamples*\[2\]</span></span> | <span data-ttu-id="bdc17-576">Imagem entrelaçada (referência)</span><span class="sxs-lookup"><span data-stu-id="bdc17-576">Interlaced picture (reference)</span></span> | <span data-ttu-id="bdc17-577">*T* + 1</span><span class="sxs-lookup"><span data-stu-id="bdc17-577">*T* +1</span></span>            |



 



| <span data-ttu-id="bdc17-578">Índice</span><span class="sxs-lookup"><span data-stu-id="bdc17-578">Index</span></span>           | <span data-ttu-id="bdc17-579">Tipo de superfície</span><span class="sxs-lookup"><span data-stu-id="bdc17-579">Surface type</span></span>                   | <span data-ttu-id="bdc17-580">Local temporal</span><span class="sxs-lookup"><span data-stu-id="bdc17-580">Temporal location</span></span> |
|-----------------|--------------------------------|-------------------|
| <span data-ttu-id="bdc17-581">*pSamples* \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="bdc17-581">*pSamples*\[0\]</span></span> | <span data-ttu-id="bdc17-582">Imagem entrelaçada</span><span class="sxs-lookup"><span data-stu-id="bdc17-582">Interlaced picture</span></span>             | <span data-ttu-id="bdc17-583">*T* − 1</span><span class="sxs-lookup"><span data-stu-id="bdc17-583">*T* −1</span></span>            |
| <span data-ttu-id="bdc17-584">*pSamples* \[ uma\]</span><span class="sxs-lookup"><span data-stu-id="bdc17-584">*pSamples*\[1\]</span></span> | <span data-ttu-id="bdc17-585">Imagem entrelaçada</span><span class="sxs-lookup"><span data-stu-id="bdc17-585">Interlaced picture</span></span>             | <span data-ttu-id="bdc17-586">*T*</span><span class="sxs-lookup"><span data-stu-id="bdc17-586">*T*</span></span>               |
| <span data-ttu-id="bdc17-587">*pSamples* \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="bdc17-587">*pSamples*\[2\]</span></span> | <span data-ttu-id="bdc17-588">Imagem entrelaçada (referência)</span><span class="sxs-lookup"><span data-stu-id="bdc17-588">Interlaced picture (reference)</span></span> | <span data-ttu-id="bdc17-589">*T* + 1</span><span class="sxs-lookup"><span data-stu-id="bdc17-589">*T* +1</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="bdc17-590">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bdc17-590">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdc17-591">Aceleração de vídeo do DirectX 2,0</span><span class="sxs-lookup"><span data-stu-id="bdc17-591">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> <dt>

[<span data-ttu-id="bdc17-592">Exemplo de VideoProc de DXVA2 \_</span><span class="sxs-lookup"><span data-stu-id="bdc17-592">DXVA2\_VideoProc Sample</span></span>](dxva2-videoproc-sample.md)
</dt> </dl>

 

 

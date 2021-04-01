---
description: Gerenciamento de qualidade de vídeo
ms.assetid: 3617adf2-ed7b-4788-abce-58bc22a14511
title: Gerenciamento de qualidade de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233ccd54cfcb98742abef9a91241e903c07ba549
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921206"
---
# <a name="video-quality-management"></a><span data-ttu-id="3283e-103">Gerenciamento de qualidade de vídeo</span><span class="sxs-lookup"><span data-stu-id="3283e-103">Video Quality Management</span></span>

<span data-ttu-id="3283e-104">Este tópico descreve algumas melhorias no pipeline de vídeo no Windows 7, tanto para Microsoft Media Foundation quanto para o Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="3283e-104">This topic describes some improvements to the video pipeline in Windows 7, both for Microsoft Media Foundation and Microsoft DirectShow.</span></span>

<span data-ttu-id="3283e-105">Em um mundo perfeito, o vídeo nunca falharia, independentemente da resolução de vídeo ou da carga de CPU/GPU.</span><span class="sxs-lookup"><span data-stu-id="3283e-105">In a perfect world, video would never glitch, regardless of the video resolution or the CPU/GPU load.</span></span> <span data-ttu-id="3283e-106">Na realidade, é claro que o pipeline de vídeo deve ser capaz de lidar com os recursos de hardware finitos e deve adaptar a reprodução adaptável ao ambiente do sistema.</span><span class="sxs-lookup"><span data-stu-id="3283e-106">In reality, of course, the video pipeline must be able to cope with finite hardware resources, and it must adaptively tailor playback to the system environment.</span></span> <span data-ttu-id="3283e-107">As metas para o gerenciamento de qualidade de vídeo são:</span><span class="sxs-lookup"><span data-stu-id="3283e-107">The goals for video quality management are to:</span></span>

-   <span data-ttu-id="3283e-108">Reduzir a falha (quadros descartados ou atrasados).</span><span class="sxs-lookup"><span data-stu-id="3283e-108">Reduce glitching (dropped or late frames).</span></span>
-   <span data-ttu-id="3283e-109">Reduza o uso de memória, especialmente na GPU.</span><span class="sxs-lookup"><span data-stu-id="3283e-109">Reduce memory usage, especially in the GPU.</span></span>
-   <span data-ttu-id="3283e-110">Reduza o consumo de energia, especialmente em laptops em execução com energia da bateria.</span><span class="sxs-lookup"><span data-stu-id="3283e-110">Reduce power consumption, especially in laptops running on battery power.</span></span>
-   <span data-ttu-id="3283e-111">Obtenha a melhor qualidade de imagem possível, dadas as restrições de recursos.</span><span class="sxs-lookup"><span data-stu-id="3283e-111">Get the best image quality possible, given resource constraints.</span></span>
-   <span data-ttu-id="3283e-112">Mantenha o vídeo sincronizado com áudio.</span><span class="sxs-lookup"><span data-stu-id="3283e-112">Keep video synchronized with audio.</span></span>

<span data-ttu-id="3283e-113">Algumas dessas metas são contrárias, especialmente em sistemas low-end.</span><span class="sxs-lookup"><span data-stu-id="3283e-113">Some of these goals are contrary, particularly on low-end systems.</span></span> <span data-ttu-id="3283e-114">Geralmente, há uma compensação entre velocidade e qualidade.</span><span class="sxs-lookup"><span data-stu-id="3283e-114">Generally there is a trade-off between speed and quality.</span></span> <span data-ttu-id="3283e-115">A falha é mais censurável do que as reduções moderadas na qualidade visual.</span><span class="sxs-lookup"><span data-stu-id="3283e-115">Glitching is more objectionable than moderate reductions in visual quality.</span></span> <span data-ttu-id="3283e-116">A importância relativa do consumo de energia varia de acordo com o ambiente; em um laptop em execução com baterias, é muito importante.</span><span class="sxs-lookup"><span data-stu-id="3283e-116">The relative importance of power consumption varies with the environment; in a laptop running on battery power, it is very important.</span></span>

<span data-ttu-id="3283e-117">No Windows 7, o processador de vídeo avançado (EVR) tem melhor suporte para o gerenciamento de qualidade de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3283e-117">In Windows 7, the enhanced video renderer (EVR) has better support for video quality management.</span></span> <span data-ttu-id="3283e-118">O pipeline de Media Foundation e o pipeline do DirectShow foram atualizados para aproveitar esses recursos.</span><span class="sxs-lookup"><span data-stu-id="3283e-118">Both the Media Foundation pipeline and the DirectShow pipeline have been updated to take advantage of these capabilities.</span></span> <span data-ttu-id="3283e-119">Uma abordagem de duas pontas é usada:</span><span class="sxs-lookup"><span data-stu-id="3283e-119">A two-pronged approach is used:</span></span>

-   <span data-ttu-id="3283e-120">Antes de iniciar a reprodução, o pipeline pode executar otimizações estáticas, com base nas configurações de gerenciamento de energia do usuário e informações sobre o hardware.</span><span class="sxs-lookup"><span data-stu-id="3283e-120">Before playback starts, the pipeline can perform static optimizations, based on the user's power management settings and information about the hardware.</span></span>
-   <span data-ttu-id="3283e-121">Depois que a reprodução é iniciada, o pipeline pode aplicar otimizações dinâmicas com base no desempenho em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="3283e-121">After playback starts, the pipeline can apply dynamic optimizations, based on run-time performance.</span></span>

## <a name="quality-management-in-media-foundation"></a><span data-ttu-id="3283e-122">Gerenciamento de qualidade no Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3283e-122">Quality Management in Media Foundation</span></span>

<span data-ttu-id="3283e-123">Para habilitar otimizações estáticas, defina o atributo de [ \_ \_ \_ \_ otimizações de reprodução estática da topologia MF](mf-topology-static-playback-optimizations.md) na topologia parcial antes de resolver a topologia.</span><span class="sxs-lookup"><span data-stu-id="3283e-123">To enable static optimizations, set the [MF\_TOPOLOGY\_STATIC\_PLAYBACK\_OPTIMIZATIONS](mf-topology-static-playback-optimizations.md) attribute on the partial topology before resolving the topology.</span></span> <span data-ttu-id="3283e-124">O carregador de topologia consulta esse atributo em seu método [**IMFTopoLoader:: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) .</span><span class="sxs-lookup"><span data-stu-id="3283e-124">The topology loader queries this attribute in its [**IMFTopoLoader::Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) method.</span></span>

<span data-ttu-id="3283e-125">Se você habilitar otimizações estáticas, deverá definir dois outros atributos na topologia:</span><span class="sxs-lookup"><span data-stu-id="3283e-125">If you enable static optimizations, you should set two other attributes on the topology:</span></span>



| <span data-ttu-id="3283e-126">Atributo</span><span class="sxs-lookup"><span data-stu-id="3283e-126">Attribute</span></span>                                                                                                                                      | <span data-ttu-id="3283e-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="3283e-127">Description</span></span>                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="3283e-128"><span id="MF_TOPOLOGY_PLAYBACK_MAX_DIMS"></span><span id="mf_topology_playback_max_dims"></span>\_ \_ esmaecimento máximo da reprodução da topologia MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="3283e-128"><span id="MF_TOPOLOGY_PLAYBACK_MAX_DIMS"></span><span id="mf_topology_playback_max_dims"></span>MF\_TOPOLOGY\_PLAYBACK\_MAX\_DIMS</span></span><br/>   | <span data-ttu-id="3283e-129">Especifica o tamanho máximo da janela de reprodução de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3283e-129">Specifies the maximum size of the video playback window.</span></span><br/> |
| <span data-ttu-id="3283e-130"><span id="MF_TOPOLOGY_PLAYBACK_FRAMERATE"></span><span id="mf_topology_playback_framerate"></span>\_taxa de \_ quadros de reprodução da topologia MF \_</span><span class="sxs-lookup"><span data-stu-id="3283e-130"><span id="MF_TOPOLOGY_PLAYBACK_FRAMERATE"></span><span id="mf_topology_playback_framerate"></span>MF\_TOPOLOGY\_PLAYBACK\_FRAMERATE</span></span><br/> | <span data-ttu-id="3283e-131">Especifica a taxa de atualização do monitor.</span><span class="sxs-lookup"><span data-stu-id="3283e-131">Specifies the monitor refresh rate.</span></span><br/>                      |



 

<span data-ttu-id="3283e-132">Esses dois atributos ajudam o pipeline a calcular a configuração mais efetiva para o gerenciamento de qualidade.</span><span class="sxs-lookup"><span data-stu-id="3283e-132">These two attributes help the pipeline calculate the most effective setting for quality management.</span></span>

<span data-ttu-id="3283e-133">As otimizações dinâmicas são executadas pelo Gerenciador de qualidade.</span><span class="sxs-lookup"><span data-stu-id="3283e-133">Dynamic optimizations are performed by the quality manager.</span></span> <span data-ttu-id="3283e-134">Você não precisa fazer nada para habilitar o Gerenciador de qualidade; Ele é habilitado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="3283e-134">You do not need to do anything to enable the quality manager; it is automatically enabled.</span></span> <span data-ttu-id="3283e-135">O Gerenciador de qualidade existia no Windows Vista; no Windows 7, o EVR pode responder melhor às mensagens do Gerenciador de qualidade.</span><span class="sxs-lookup"><span data-stu-id="3283e-135">The quality manager existed in Windows Vista; in Windows 7, the EVR can respond better to messages from the quality manager.</span></span>

## <a name="quality-management-in-directshow"></a><span data-ttu-id="3283e-136">Gerenciamento de qualidade no DirectShow</span><span class="sxs-lookup"><span data-stu-id="3283e-136">Quality Management in DirectShow</span></span>

<span data-ttu-id="3283e-137">O DirectShow dá suporte a otimizações estáticas e dinâmicas para reprodução de DVD.</span><span class="sxs-lookup"><span data-stu-id="3283e-137">DirectShow supports static and dynamic optimizations for DVD playback.</span></span> <span data-ttu-id="3283e-138">Para habilitar essas otimizações em um aplicativo de reprodução de DVD, defina os seguintes sinalizadores no parâmetro *dwFlags* do método **IDvdGraphBuilder:: RenderDvdVideoVolume** :</span><span class="sxs-lookup"><span data-stu-id="3283e-138">To enable these optimizations in a DVD playback application, set the following flags in the *dwFlags* parameter of the **IDvdGraphBuilder::RenderDvdVideoVolume** method:</span></span>



| <span data-ttu-id="3283e-139">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="3283e-139">Flag</span></span>                  | <span data-ttu-id="3283e-140">Descrição</span><span class="sxs-lookup"><span data-stu-id="3283e-140">Description</span></span>                    |
|-----------------------|--------------------------------|
| <span data-ttu-id="3283e-141">\_grafo de \_ adaptação de DVD am \_</span><span class="sxs-lookup"><span data-stu-id="3283e-141">AM\_DVD\_ADAPT\_GRAPH</span></span> | <span data-ttu-id="3283e-142">Habilita otimizações estáticas.</span><span class="sxs-lookup"><span data-stu-id="3283e-142">Enables static optimizations.</span></span>  |
| <span data-ttu-id="3283e-143">\_ \_ EVR QoS de DVD am \_</span><span class="sxs-lookup"><span data-stu-id="3283e-143">AM\_DVD\_EVR\_QOS</span></span>     | <span data-ttu-id="3283e-144">Habilita otimizações dinâmicas.</span><span class="sxs-lookup"><span data-stu-id="3283e-144">Enables dynamic optimizations.</span></span> |



 

<span data-ttu-id="3283e-145">Outros aplicativos do DirectShow podem habilitar otimizações dinâmicas chamando o método [**IEVRFilterConfigEx:: SetConfigPrefs**](/windows/desktop/api/evr/nf-evr-ievrfilterconfigex-setconfigprefs) diretamente no filtro EVR.</span><span class="sxs-lookup"><span data-stu-id="3283e-145">Other DirectShow applications can enable dynamic optimizations by calling the [**IEVRFilterConfigEx::SetConfigPrefs**](/windows/desktop/api/evr/nf-evr-ievrfilterconfigex-setconfigprefs) method directly on the EVR filter.</span></span> <span data-ttu-id="3283e-146">Especifique o sinalizador **EVRFilterConfigPrefs \_ EnableQoS** .</span><span class="sxs-lookup"><span data-stu-id="3283e-146">Specify the **EVRFilterConfigPrefs\_EnableQoS** flag.</span></span>

> [!Note]  
> <span data-ttu-id="3283e-147">Otimizações estáticas no DirectShow são limitadas à reprodução de DVD.</span><span class="sxs-lookup"><span data-stu-id="3283e-147">Static optimizations in DirectShow are limited to DVD playback.</span></span>

 

## <a name="quality-management-in-the-evr"></a><span data-ttu-id="3283e-148">Gerenciamento de qualidade no EVR</span><span class="sxs-lookup"><span data-stu-id="3283e-148">Quality Management in the EVR</span></span>

<span data-ttu-id="3283e-149">O EVR dá suporte a alguns novos sinalizadores de configuração para gerenciamento de qualidade.</span><span class="sxs-lookup"><span data-stu-id="3283e-149">The EVR supports some new configuration flags for quality management.</span></span> <span data-ttu-id="3283e-150">Se você habilitar as otimizações de gerenciamento de qualidade descritas anteriormente, não precisará definir esses sinalizadores diretamente.</span><span class="sxs-lookup"><span data-stu-id="3283e-150">If you enable the quality management optimizations described previously, you do not have to set these flags directly.</span></span> <span data-ttu-id="3283e-151">No entanto, eles são documentados para aplicativos que desejam um controle mais granular sobre o EVR.</span><span class="sxs-lookup"><span data-stu-id="3283e-151">However, they are documented for applications that want more granular control over the EVR.</span></span>

<span data-ttu-id="3283e-152">Defina os seguintes sinalizadores no mixer EVR chamando o método [**IMFVideoMixerControl2:: SetMixingPrefs**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol2-setmixingprefs) :</span><span class="sxs-lookup"><span data-stu-id="3283e-152">Set the following flags on the EVR mixer by calling the [**IMFVideoMixerControl2::SetMixingPrefs**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol2-setmixingprefs) method:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3283e-153">Flags</span><span class="sxs-lookup"><span data-stu-id="3283e-153">Flags</span></span></th>
<th><span data-ttu-id="3283e-154">Descrição</span><span class="sxs-lookup"><span data-stu-id="3283e-154">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="3283e-155"><strong>MFVideoMixPrefs_ForceHalfInterlace</strong></span><span class="sxs-lookup"><span data-stu-id="3283e-155"><strong>MFVideoMixPrefs_ForceHalfInterlace</strong></span></span></li>
<li><span data-ttu-id="3283e-156"><strong>MFVideoMixPrefs_AllowDropToHalfInterlace</strong></span><span class="sxs-lookup"><span data-stu-id="3283e-156"><strong>MFVideoMixPrefs_AllowDropToHalfInterlace</strong></span></span></li>
</ul></td>
<td><span data-ttu-id="3283e-157">Ignore o segundo campo de cada quadro entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="3283e-157">Skip the second field of every interlaced frame.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="3283e-158"><strong>MFVideoMixPrefs_AllowDropToBob</strong></span><span class="sxs-lookup"><span data-stu-id="3283e-158"><strong>MFVideoMixPrefs_AllowDropToBob</strong></span></span></li>
<li><span data-ttu-id="3283e-159"><strong>MFVideoMixPrefs_ForceBob</strong></span><span class="sxs-lookup"><span data-stu-id="3283e-159"><strong>MFVideoMixPrefs_ForceBob</strong></span></span></li>
</ul></td>
<td><span data-ttu-id="3283e-160">Use Bob deentrelaçando, mesmo que o driver dê suporte a um modo de desentrelaçamento de qualidade superior.</span><span class="sxs-lookup"><span data-stu-id="3283e-160">Use bob deinterlacing, even if the driver supports a higher-quality deinterlace mode.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3283e-161">Defina os seguintes sinalizadores no apresentador EVR chamando o método [**IMFVideoDisplayControl:: SetRenderingPrefs**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setrenderingprefs) :</span><span class="sxs-lookup"><span data-stu-id="3283e-161">Set the following flags on the EVR presenter by calling the [**IMFVideoDisplayControl::SetRenderingPrefs**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setrenderingprefs) method:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3283e-162">Flags</span><span class="sxs-lookup"><span data-stu-id="3283e-162">Flags</span></span></th>
<th><span data-ttu-id="3283e-163">Descrição</span><span class="sxs-lookup"><span data-stu-id="3283e-163">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="3283e-164"><strong>MFVideoRenderPrefs_ForceOutputThrottling</strong></span><span class="sxs-lookup"><span data-stu-id="3283e-164"><strong>MFVideoRenderPrefs_ForceOutputThrottling</strong></span></span></li>
<li><span data-ttu-id="3283e-165"><strong>MFVideoRenderPrefs_AllowOutputThrottling</strong></span><span class="sxs-lookup"><span data-stu-id="3283e-165"><strong>MFVideoRenderPrefs_AllowOutputThrottling</strong></span></span></li>
</ul></td>
<td><span data-ttu-id="3283e-166">Limite a saída para corresponder à largura de banda da GPU.</span><span class="sxs-lookup"><span data-stu-id="3283e-166">Throttle output to match GPU bandwidth.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="3283e-167"><strong>MFVideoRenderPrefs_ForceBatching</strong></span><span class="sxs-lookup"><span data-stu-id="3283e-167"><strong>MFVideoRenderPrefs_ForceBatching</strong></span></span></li>
<li><span data-ttu-id="3283e-168"><strong>MFVideoRenderPrefs_AllowBatching</strong></span><span class="sxs-lookup"><span data-stu-id="3283e-168"><strong>MFVideoRenderPrefs_AllowBatching</strong></span></span></li>
</ul></td>
<td><span data-ttu-id="3283e-169">O Direct3D do lote apresenta chamadas.</span><span class="sxs-lookup"><span data-stu-id="3283e-169">Batch Direct3D Present calls.</span></span> <span data-ttu-id="3283e-170">Essa otimização permite que o sistema entre em Estados ociosos com mais frequência, o que pode reduzir o consumo de energia.</span><span class="sxs-lookup"><span data-stu-id="3283e-170">This optimization enables the system to enter into idle states more frequently, which can reduce power consumption.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="3283e-171">MFVideoRenderPrefs_ForceScaling</span><span class="sxs-lookup"><span data-stu-id="3283e-171">MFVideoRenderPrefs_ForceScaling</span></span></li>
<li><span data-ttu-id="3283e-172">MFVideoRenderPrefs_AllowScaling</span><span class="sxs-lookup"><span data-stu-id="3283e-172">MFVideoRenderPrefs_AllowScaling</span></span></li>
</ul></td>
<td><span data-ttu-id="3283e-173">Execute a mistura de vídeo usando um retângulo menor do que o retângulo de saída.</span><span class="sxs-lookup"><span data-stu-id="3283e-173">Perform video mixing using a rectangle smaller than the output rectangle.</span></span> <span data-ttu-id="3283e-174">Dimensione o resultado para o tamanho de saída correto.</span><span class="sxs-lookup"><span data-stu-id="3283e-174">Scale the result to the correct output size.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3283e-175">Além disso, o coletor de mídia EVR dá suporte a atributos de configuração que correspondem a cada um desses sinalizadores:</span><span class="sxs-lookup"><span data-stu-id="3283e-175">In addition, the EVR media sink supports configuration attributes that correspond to each of these flags:</span></span>

-   [<span data-ttu-id="3283e-176">EVRConfig \_ AllowBatching</span><span class="sxs-lookup"><span data-stu-id="3283e-176">EVRConfig\_AllowBatching</span></span>](evrconfig-allowbatching.md)
-   [<span data-ttu-id="3283e-177">EVRConfig \_ AllowDropToBob</span><span class="sxs-lookup"><span data-stu-id="3283e-177">EVRConfig\_AllowDropToBob</span></span>](evrconfig-allowdroptobob.md)
-   [<span data-ttu-id="3283e-178">EVRConfig \_ AllowDropToHalfInterlace</span><span class="sxs-lookup"><span data-stu-id="3283e-178">EVRConfig\_AllowDropToHalfInterlace</span></span>](evrconfig-allowdroptohalfinterlace.md)
-   [<span data-ttu-id="3283e-179">EVRConfig \_ AllowScaling</span><span class="sxs-lookup"><span data-stu-id="3283e-179">EVRConfig\_AllowScaling</span></span>](evrconfig-allowscaling.md)
-   [<span data-ttu-id="3283e-180">EVRConfig \_ AllowDropToThrottle</span><span class="sxs-lookup"><span data-stu-id="3283e-180">EVRConfig\_AllowDropToThrottle</span></span>](evrconfig-allowdroptothrottle.md)
-   [<span data-ttu-id="3283e-181">EVRConfig \_ ForceBatching</span><span class="sxs-lookup"><span data-stu-id="3283e-181">EVRConfig\_ForceBatching</span></span>](evrconfig-forcebatching.md)
-   [<span data-ttu-id="3283e-182">EVRConfig \_ ForceBob</span><span class="sxs-lookup"><span data-stu-id="3283e-182">EVRConfig\_ForceBob</span></span>](evrconfig-forcebob.md)
-   [<span data-ttu-id="3283e-183">EVRConfig \_ ForceHalfInterlace</span><span class="sxs-lookup"><span data-stu-id="3283e-183">EVRConfig\_ForceHalfInterlace</span></span>](evrconfig-forcehalfinterlace.md)
-   [<span data-ttu-id="3283e-184">EVRConfig \_ ForceScaling</span><span class="sxs-lookup"><span data-stu-id="3283e-184">EVRConfig\_ForceScaling</span></span>](evrconfig-forcescaling.md)
-   [<span data-ttu-id="3283e-185">EVRConfig \_ ForceThrottle</span><span class="sxs-lookup"><span data-stu-id="3283e-185">EVRConfig\_ForceThrottle</span></span>](evrconfig-forcethrottle.md)

<span data-ttu-id="3283e-186">Antes de iniciar a reprodução, você pode definir esses atributos diretamente no coletor de mídia do EVR, como uma alternativa para chamar os métodos [**IMFVideoMixerControl2**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol2) e [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) .</span><span class="sxs-lookup"><span data-stu-id="3283e-186">Before playback starts, you can set these attributes directly on the EVR media sink, as an alternative to calling the [**IMFVideoMixerControl2**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol2) and [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) methods.</span></span> <span data-ttu-id="3283e-187">Para definir esses atributos, consulte o coletor de mídia do EVR para [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span><span class="sxs-lookup"><span data-stu-id="3283e-187">To set these attributes, query the EVR media sink for [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3283e-188">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3283e-188">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3283e-189">Sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="3283e-189">Media Session</span></span>](media-session.md)
</dt> </dl>

 

 





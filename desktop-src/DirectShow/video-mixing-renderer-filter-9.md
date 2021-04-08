---
description: Filtro de processador de mixagem de vídeo 9
ms.assetid: 3885cca2-74b1-4066-8ecb-84c9841f9e66
title: Filtro de processador de mixagem de vídeo 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b2576f8c5f1b0f262b83141c14ce4836eecb4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662546"
---
# <a name="video-mixing-renderer-filter-9"></a><span data-ttu-id="4671f-103">Filtro de processador de mixagem de vídeo 9</span><span class="sxs-lookup"><span data-stu-id="4671f-103">Video Mixing Renderer Filter 9</span></span>

<span data-ttu-id="4671f-104">No DirectX 9, o filtro do processador de mixagem de vídeo 9 (VMR-9) oferece recursos avançados de renderização de vídeo em todas as plataformas com suporte no DirectX.</span><span class="sxs-lookup"><span data-stu-id="4671f-104">In DirectX 9, the Video Mixing Renderer 9 (VMR-9) filter offers advanced video rendering capabilities on all platforms supported by DirectX.</span></span> <span data-ttu-id="4671f-105">Ele é totalmente integrado aos recursos do DirectX 9 3D.</span><span class="sxs-lookup"><span data-stu-id="4671f-105">It is fully integrated with DirectX 9 3D capabilities.</span></span> <span data-ttu-id="4671f-106">Por exemplo, você pode adicionar facilmente vídeo a jogos e outros ambientes 3D ou transformar imagens de vídeo usando sombreadores de pixel do Direct3D e outros efeitos.</span><span class="sxs-lookup"><span data-stu-id="4671f-106">For example, that you can easily add video to games and other 3D environments or transform video images using the Direct3D pixel shaders and other effects.</span></span>

<span data-ttu-id="4671f-107">Este filtro não oferece suporte a portas de vídeo.</span><span class="sxs-lookup"><span data-stu-id="4671f-107">This filter does not support video ports.</span></span>

<span data-ttu-id="4671f-108">Para manter a compatibilidade com versões anteriores, o VMR-9 não é o renderizador padrão em nenhum sistema.</span><span class="sxs-lookup"><span data-stu-id="4671f-108">To maintain backward compatibility, the VMR-9 is not the default renderer on any system.</span></span> <span data-ttu-id="4671f-109">Para usar esse filtro, adicione-o ao grafo de filtro explicitamente e configure-o antes de conectar qualquer um de seus PINs de entrada.</span><span class="sxs-lookup"><span data-stu-id="4671f-109">To use this filter, add it to the filter graph explicitly and configure it before connecting any of its input pins.</span></span> <span data-ttu-id="4671f-110">O VMR-9 usa seu próprio conjunto de interfaces, estruturas e enumerações, que nem sempre são idênticas aos tipos de dados correspondentes usados com o VMR-7.</span><span class="sxs-lookup"><span data-stu-id="4671f-110">The VMR-9 uses its own set of interfaces, structures, and enumerations, which are not always identical to the corresponding data types used with the VMR-7.</span></span>

<span data-ttu-id="4671f-111">O VMR-9 dá suporte a até 16 monitores.</span><span class="sxs-lookup"><span data-stu-id="4671f-111">The VMR-9 supports up to 16 monitors.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4671f-112">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="4671f-112">Filter Interfaces</span></span></td>
<td><span data-ttu-id="4671f-113">O VMR-9 dá suporte a vários modos de renderização distintos.</span><span class="sxs-lookup"><span data-stu-id="4671f-113">The VMR-9 supports several distinct rendering modes.</span></span> <span data-ttu-id="4671f-114">Ele dá suporte a um conjunto diferente de interfaces, dependendo do modo de renderização:</span><span class="sxs-lookup"><span data-stu-id="4671f-114">It supports a different set of interfaces depending on the rendering mode:</span></span><br/>
<ul>
<li><span data-ttu-id="4671f-115">Todos os modos: <a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="4671f-115">All modes: <a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></span></span></li>
<li><span data-ttu-id="4671f-116">Modo de renderização: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"> <strong>IVMRSurfaceAllocatorNotify9</strong></a></span><span class="sxs-lookup"><span data-stu-id="4671f-116">Renderless mode: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"><strong>IVMRSurfaceAllocatorNotify9</strong></a></span></span></li>
<li><span data-ttu-id="4671f-117">Modo em janela: <a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></span><span class="sxs-lookup"><span data-stu-id="4671f-117">Windowed mode: <a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></span></span></li>
<li><span data-ttu-id="4671f-118">Modo sem janela: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="4671f-118">Windowless mode: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></span></span></li>
</ul>
<span data-ttu-id="4671f-119">Para definir o modo de renderização, chame <a href="/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode"><strong>IVMRFilterConfig9:: Setrenderizamode</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4671f-119">To set the rendering mode, call <a href="/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode"><strong>IVMRFilterConfig9::SetRenderingMode</strong></a>.</span></span> <span data-ttu-id="4671f-120">Para obter mais informações, consulte <a href="vmr-modes-of-operation.md">modos de operação do VMR</a>.</span><span class="sxs-lookup"><span data-stu-id="4671f-120">For more information, see <a href="vmr-modes-of-operation.md">VMR Modes of Operation</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4671f-121">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="4671f-121">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="4671f-122">Os Pins de entrada se conectarão a qualquer tipo compatível com o hardware de vídeo subjacente.</span><span class="sxs-lookup"><span data-stu-id="4671f-122">The input pins will connect with any type supported by the underlying video hardware.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4671f-123">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="4671f-123">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="4671f-124"><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrvideostreamcontrol9"><strong>IVMRVideoStreamControl9</strong></a></span><span class="sxs-lookup"><span data-stu-id="4671f-124"><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrvideostreamcontrol9"><strong>IVMRVideoStreamControl9</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4671f-125">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="4671f-125">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="4671f-126">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="4671f-126">Not applicable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4671f-127">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="4671f-127">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="4671f-128">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="4671f-128">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4671f-129">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="4671f-129">Filter CLSID</span></span></td>
<td><span data-ttu-id="4671f-130">CLSID_VideoMixingRenderer9</span><span class="sxs-lookup"><span data-stu-id="4671f-130">CLSID_VideoMixingRenderer9</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4671f-131">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="4671f-131">Property Page CLSID</span></span></td>
<td><span data-ttu-id="4671f-132">N/D</span><span class="sxs-lookup"><span data-stu-id="4671f-132">N/A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4671f-133">Executável</span><span class="sxs-lookup"><span data-stu-id="4671f-133">Executable</span></span></td>
<td><span data-ttu-id="4671f-134">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="4671f-134">Quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4671f-135"><a href="merit.md">Núcleo</a></span><span class="sxs-lookup"><span data-stu-id="4671f-135"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="4671f-136">MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="4671f-136">MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4671f-137"><a href="filter-categories.md">Categoria do filtro</a></span><span class="sxs-lookup"><span data-stu-id="4671f-137"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="4671f-138">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="4671f-138">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="4671f-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="4671f-139">Remarks</span></span>

<span data-ttu-id="4671f-140">Um aplicativo pode fornecer um objeto de apresentador de alocador personalizado que expõe as seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="4671f-140">An application can provide a custom allocator-presenter object that exposes the following interfaces:</span></span>

-   [<span data-ttu-id="4671f-141">**IVMRImagePresenter9**</span><span class="sxs-lookup"><span data-stu-id="4671f-141">**IVMRImagePresenter9**</span></span>](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9)
-   <span data-ttu-id="4671f-142">[**IVMRImagePresenterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9) (opcional)</span><span class="sxs-lookup"><span data-stu-id="4671f-142">[**IVMRImagePresenterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9) (optional)</span></span>
-   [<span data-ttu-id="4671f-143">**IVMRSurfaceAllocator9**</span><span class="sxs-lookup"><span data-stu-id="4671f-143">**IVMRSurfaceAllocator9**</span></span>](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9)
-   <span data-ttu-id="4671f-144">[**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) (opcional)</span><span class="sxs-lookup"><span data-stu-id="4671f-144">[**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) (optional)</span></span>
-   <span data-ttu-id="4671f-145">[**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) (opcional)</span><span class="sxs-lookup"><span data-stu-id="4671f-145">[**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) (optional)</span></span>

<span data-ttu-id="4671f-146">Para obter mais informações sobre os apresentadores de alocadores personalizados, consulte [fornecendo um Allocator-Presenter personalizado para o VMR-9](supplying-a-custom-allocator-presenter-for-vmr-9.md).</span><span class="sxs-lookup"><span data-stu-id="4671f-146">For more information about custom allocator-presenters, see [Supplying a Custom Allocator-Presenter for VMR-9](supplying-a-custom-allocator-presenter-for-vmr-9.md).</span></span>

<span data-ttu-id="4671f-147">Um aplicativo também pode fornecer um compositor de plug-in personalizado que expõe a seguinte interface:</span><span class="sxs-lookup"><span data-stu-id="4671f-147">An application can also provide a custom plug-in compositor that exposes the following interface:</span></span>

-   [<span data-ttu-id="4671f-148">**IVMRImageCompositor9**</span><span class="sxs-lookup"><span data-stu-id="4671f-148">**IVMRImageCompositor9**</span></span>](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9)

<span data-ttu-id="4671f-149">Para configurar o VMR com um compositor personalizado, chame [**IVMRFilterConfig9:: SetImageCompositor**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setimagecompositor).</span><span class="sxs-lookup"><span data-stu-id="4671f-149">To configure the VMR with a custom compositor, call [**IVMRFilterConfig9::SetImageCompositor**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setimagecompositor).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4671f-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4671f-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4671f-151">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="4671f-151">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="4671f-152">Usando o processador de mixagem de vídeo</span><span class="sxs-lookup"><span data-stu-id="4671f-152">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 





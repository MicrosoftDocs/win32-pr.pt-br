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
# <a name="video-mixing-renderer-filter-9"></a>Filtro de processador de mixagem de vídeo 9

No DirectX 9, o filtro do processador de mixagem de vídeo 9 (VMR-9) oferece recursos avançados de renderização de vídeo em todas as plataformas com suporte no DirectX. Ele é totalmente integrado aos recursos do DirectX 9 3D. Por exemplo, você pode adicionar facilmente vídeo a jogos e outros ambientes 3D ou transformar imagens de vídeo usando sombreadores de pixel do Direct3D e outros efeitos.

Este filtro não oferece suporte a portas de vídeo.

Para manter a compatibilidade com versões anteriores, o VMR-9 não é o renderizador padrão em nenhum sistema. Para usar esse filtro, adicione-o ao grafo de filtro explicitamente e configure-o antes de conectar qualquer um de seus PINs de entrada. O VMR-9 usa seu próprio conjunto de interfaces, estruturas e enumerações, que nem sempre são idênticas aos tipos de dados correspondentes usados com o VMR-7.

O VMR-9 dá suporte a até 16 monitores.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filtrar interfaces</td>
<td>O VMR-9 dá suporte a vários modos de renderização distintos. Ele dá suporte a um conjunto diferente de interfaces, dependendo do modo de renderização:<br/>
<ul>
<li>Todos os modos: <a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></li>
<li>Modo de renderização: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"> <strong>IVMRSurfaceAllocatorNotify9</strong></a></li>
<li>Modo em janela: <a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></li>
<li>Modo sem janela: <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></li>
</ul>
Para definir o modo de renderização, chame <a href="/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode"><strong>IVMRFilterConfig9:: Setrenderizamode</strong></a>. Para obter mais informações, consulte <a href="vmr-modes-of-operation.md">modos de operação do VMR</a>.<br/></td>
</tr>
<tr class="even">
<td>Tipos de mídia de pino de entrada</td>
<td>Os Pins de entrada se conectarão a qualquer tipo compatível com o hardware de vídeo subjacente.</td>
</tr>
<tr class="odd">
<td>Interfaces de pino de entrada</td>
<td><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrvideostreamcontrol9"><strong>IVMRVideoStreamControl9</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de mídia do pino de saída</td>
<td>Não aplicável.</td>
</tr>
<tr class="odd">
<td>Interfaces de pino de saída</td>
<td>Não aplicável.</td>
</tr>
<tr class="even">
<td>CLSID do filtro</td>
<td>CLSID_VideoMixingRenderer9</td>
</tr>
<tr class="odd">
<td>CLSID de página de propriedades</td>
<td>N/D</td>
</tr>
<tr class="even">
<td>Executável</td>
<td>Quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Núcleo</a></td>
<td>MERIT_DO_NOT_USE</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoria do filtro</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentários

Um aplicativo pode fornecer um objeto de apresentador de alocador personalizado que expõe as seguintes interfaces:

-   [**IVMRImagePresenter9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9)
-   [**IVMRImagePresenterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9) (opcional)
-   [**IVMRSurfaceAllocator9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9)
-   [**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) (opcional)
-   [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) (opcional)

Para obter mais informações sobre os apresentadores de alocadores personalizados, consulte [fornecendo um Allocator-Presenter personalizado para o VMR-9](supplying-a-custom-allocator-presenter-for-vmr-9.md).

Um aplicativo também pode fornecer um compositor de plug-in personalizado que expõe a seguinte interface:

-   [**IVMRImageCompositor9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9)

Para configurar o VMR com um compositor personalizado, chame [**IVMRFilterConfig9:: SetImageCompositor**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setimagecompositor).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> <dt>

[Usando o processador de mixagem de vídeo](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 





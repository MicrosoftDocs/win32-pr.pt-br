---
description: Filtro de processador de mixagem de vídeo 7
ms.assetid: c83e6c50-76f2-4aeb-944b-5b244c6bf776
title: Filtro de processador de mixagem de vídeo 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e396e15189e89dcebde69fb513419df340ab09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502242"
---
# <a name="video-mixing-renderer-filter-7"></a>Filtro de processador de mixagem de vídeo 7

Este tópico aplica-se ao Windows XP ou posterior.

No Windows XP e posterior, o processador de mixagem de vídeo 7 (VMR-7) é o renderizador de vídeo padrão. Ele é chamado de VMR-7 porque usa internamente o DirectDraw 7. No DirectX 9, um filtro semelhante, mas separado, o VMR-9, está disponível para redistribuição em sistemas não XP. O VMR-9 usa o Direct3D 9.

> [!Note]  
> O VMR está disponível no Windows XP e versões posteriores. Ele não está disponível por meio de pacotes redistribuíveis do DirectX ou em versões anteriores do Windows. Para a maioria dos cenários, os aplicativos devem usar o [processador de mixagem de vídeo 9](video-mixing-renderer-filter-9.md).

 

Os recursos do VMR incluem:

-   Mistura alfa verdadeira de até 16 fluxos de entrada
-   Acesso à imagem compostada antes de ser renderizada
-   Um modelo de plug-in que permite que terceiros implementem efeitos de vídeo personalizados.
-   Suporte para até 15 monitores.

Durante a criação do grafo no Windows XP e versões posteriores, o Gerenciador do grafo de filtro não usará os filtros mais antigos do mixer de vídeo ou de sobreposição, a menos que o aplicativo os crie explicitamente e adicione ao grafo.

Para obter mais informações, consulte [usando o processador de mixagem de vídeo](using-the-video-mixing-renderer.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filtrar interfaces</td>
<td>Todos os modos:
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li>
<li><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></li>
<li><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeinterlaceControl</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></li>
</ul>
Modo em janela:<br/>
<ul>
<li><a href="/windows/desktop/api/Control/nn-control-ibasicvideo"><strong>IBasicVideo</strong></a></li>
<li><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></li>
<li><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></li>
</ul>
Modo sem janela:<br/>
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig"><strong>IVMRMonitorConfig</strong></a></li>
</ul>
Modo de renderização:<br/>
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></li>
</ul>
Modo de mixer:<br/>
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></li>
</ul>
Para obter informações sobre os vários modos do VMR-7, consulte <a href="vmr-modes-of-operation.md">modos de operação do VMR</a>.<br/></td>
</tr>
<tr class="even">
<td>Tipos de mídia de pino de entrada</td>
<td>Tipo principal: MEDIATYPE_VideoSubtype: depende do hardware de gráficos. Deve ser um vídeo descompactado.<br/></td>
</tr>
<tr class="odd">
<td>Interfaces de pino de entrada</td>
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a> (consulte comentários)</li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol"><strong>IVMRVideoStreamControl</strong></a></li>
</ul></td>
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
<td>Há dois CLSIDs associados a este filtro:
<ul>
<li>CLSID_VideoMixingRenderer: cria o VMR-7. Se não houver recursos suficientes do sistema para criar o VMR-7, a chamada para <strong>CoCreateInstance</strong> falhará.</li>
<li>CLSID_VideoRendererDefault: cria o VMR-7 se os recursos do sistema estiverem disponíveis ou criará o filtro de <a href="video-renderer-filter.md">processamento de vídeo</a> antigo.</li>
</ul>
Use CLSID_VideoMixingRenderer se você precisar dos recursos específicos do VMR-7. Caso contrário, use CLSID_VideoRendererDefault, que é quase certo para não falhar, pois ele volta ao filtro de processamento de vídeo antigo.<br/></td>
</tr>
<tr class="odd">
<td>CLSID de página de propriedades</td>
<td>Não aplicável.</td>
</tr>
<tr class="even">
<td>Executável</td>
<td>Quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Núcleo</a></td>
<td>MERIT_PREFERRED + 1</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoria do filtro</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentários

O PIN de entrada expõe a interface **IOverlay** somente quando o filtro VMR-7 está no modo de janela. O único método **IOverlay** que o PIN implementa é **GetWindowHandle**, que permite que um aplicativo obtenha um identificador para a janela de vídeo do filtro. Todos os outros métodos **IOverlay** retornam E \_ NOTIMPL. No modo sem janela, o filtro não cria uma janela de vídeo, portanto, o PIN não expõe a interface.

Um aplicativo pode fornecer um objeto de apresentador de alocador personalizado que expõe as seguintes interfaces:

-   [**IVMRImagePresenter**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter)
-   [**IVMRImagePresenterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig) (opcional)
-   [**IVMRMonitorConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrmonitorconfig) (opcional)
-   [**IVMRSurfaceAllocator**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator)
-   [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) (opcional)

Para obter mais informações sobre os apresentadores de alocadores personalizados, consulte [fornecendo um Allocator-Presenter personalizado para o VMR-7](supplying-a-custom-allocator-presenter-for-vmr-7.md).

Um aplicativo também pode fornecer um compositor de plug-in personalizado que expõe a seguinte interface:

-   [**IVMRImageCompositor**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor)

Para configurar o VMR com um compositor personalizado, chame [**IVMRFilterConfig:: SetImageCompositor**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setimagecompositor).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> </dl>

 

 





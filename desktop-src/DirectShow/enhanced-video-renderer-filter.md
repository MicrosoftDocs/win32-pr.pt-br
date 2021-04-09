---
description: O filtro EVR (processador de vídeo avançado) é um processador e mixer de vídeo de 16 canais. Ele tem a mesma funcionalidade básica e modelo de plug-in que o coletor de mídia Media Foundation EVR.
ms.assetid: ead99cb3-2be2-42c6-ac22-be0c2ddf28d5
title: Filtro de processador de vídeo aprimorado
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ba6e7c14386ea37424364274263859844182ed7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104009974"
---
# <a name="enhanced-video-renderer-filter"></a>Filtro de processador de vídeo aprimorado

> [!Note]  
> Este tópico aplica-se ao Windows Vista e posterior.

 

O filtro EVR (processador de vídeo avançado) é um processador e mixer de vídeo de 16 canais. Ele tem a mesma funcionalidade básica e modelo de plug-in que o coletor de mídia Media Foundation EVR.

O filtro EVR do DirectShow está documentado na documentação do SDK do Media Foundation; para obter mais informações, consulte [processador de vídeo aprimorado](../medfound/enhanced-video-renderer.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filtrar interfaces (por meio de <strong>QueryInterface</strong>)</td>
<td>Interfaces do DirectShow:
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li>
<li><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaeventsink"><strong>IMediaEventSink</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></li>
</ul>
Interfaces de Media Foundation:<br/>
<ul>
<li><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig"><strong>IEVRFilterConfig</strong></a></li>
<li><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></li>
<li><a href="/windows/desktop/api/evr/nn-evr-imfvideopositionmapper"><strong>IMFVideoPositionMapper</strong></a></li>
<li><a href="/windows/desktop/api/evr/nn-evr-imfvideorenderer"><strong>IMFVideoRenderer</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>Tipos de mídia de pino de entrada</td>
<td>, Dependendo do driver de gráficos.</td>
</tr>
<tr class="odd">
<td>Interfaces de pino de entrada (por meio de <strong>QueryInterface</strong>)</td>
<td>Interfaces do DirectShow:
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li>
</ul>
Interfaces de Media Foundation:<br/>
<ul>
<li><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration"><strong>IDirectXVideoMemoryConfiguration</strong></a></li>
<li><a href="/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol"><strong>IEVRVideoStreamControl</strong></a></li>
<li><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></li>
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
<td>CLSID_EnhancedVideoRenderer</td>
</tr>
<tr class="odd">
<td>Executável</td>
<td>evr.dll</td>
</tr>
<tr class="even">
<td><a href="merit.md">Núcleo</a></td>
<td>MERIT_DO_NOT_USE</td>
</tr>
<tr class="odd">
<td><a href="filter-categories.md">Categoria do filtro</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentários

Além das interfaces expostas por meio de **QueryInterface**, o EVR expõe outras interfaces por meio do método [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) . Algumas dessas interfaces são implementadas pelo apresentador EVR ou o mixer EVR, em vez do EVR em si. Se o aplicativo definir um apresentador ou mixer personalizado no EVR, as versões personalizadas poderão expor um conjunto diferente de interfaces.



| Objeto     | Identificador de serviço                                              | Interfaces                                                                                                                                                                                                                                                                                                     |
|------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtro de EVR | \_ \_ \_ Serviço de RENDERIZAÇÃO de vídeo Mr (consultas EVR ou Presenter)<br/> | [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)<br/> [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)<br/>                                                          |
| Filtro de EVR | \_ \_ \_ Serviço de aceleração de vídeo do Mr (apresentador de consultas)<br/>  | [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9)                                                                                                                                                                                                                                                      |
| Filtro de EVR | \_ \_ \_ Serviço de mixer de vídeo Mr (mixer de consultas)<br/>             | [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)<br/> [**IMFVideoMixerControl**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol)<br/> [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)<br/> |
| Pins de entrada | \_serviço de \_ aceleração de vídeo Mr \_                                | [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)                                                                                                                                                                                                                                    |



 

O EVR pode misturar até 16 fluxos de vídeo. O primeiro fluxo de entrada (pino 0) é chamado de *fluxo de referência*. O fluxo de referência sempre aparece primeiro na ordem z. Quaisquer fluxos adicionais são chamados de subfluxos e misturados na parte superior do fluxo de referência. O aplicativo pode alterar a ordem z dos subfluxos, mas nenhum Subfluxo pode ser o primeiro na ordem z.

O driver de gráficos determina quais formatos de vídeo têm suporte, mas normalmente eles são limitados ao seguinte:

-   Fluxo de referência: YUV progressivo ou entrelaçado sem alfa por pixel (como NV12 ou YUY2); ou RGB progressivo.
-   Subfluxos: YUV progressivo com per-pixel-Alpha, como AYUV ou AI44.

Os formatos de Subfluxo disponíveis podem depender do formato do fluxo de referência.

O EVR encaminha os comandos de busca upstream por meio do pino 0. Os Pins de Subfluxo não encaminham os comandos de busca. É responsabilidade do filtro de origem ou de Splitter manter os subfluxos sincronizados com o fluxo de referência.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> </dl>


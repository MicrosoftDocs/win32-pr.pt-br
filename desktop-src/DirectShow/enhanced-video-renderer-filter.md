---
description: O filtro EVR (Renderização de Vídeo Aprimorado) é um renderização e um mixer de vídeo de 16 canais. Ele tem a mesma funcionalidade principal e o mesmo modelo de plug-in que o Media Foundation de mídia EVR.
ms.assetid: ead99cb3-2be2-42c6-ac22-be0c2ddf28d5
title: Filtro de renderização de vídeo aprimorado
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e6b99eefe8f31074c755f4f74b4cd8749e44de996f49592cea5827d6fa1e123
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537066"
---
# <a name="enhanced-video-renderer-filter"></a>Filtro de renderização de vídeo aprimorado

> [!Note]  
> Este tópico se aplica ao Windows Vista e posterior.

 

O filtro EVR (Renderização de Vídeo Aprimorado) é um renderização e um mixer de vídeo de 16 canais. Ele tem a mesma funcionalidade principal e o mesmo modelo de plug-in que o Media Foundation de mídia EVR.

O DirectShow filtro EVR está documentado na documentação Media Foundation SDK; Para obter mais informações, consulte [Renderização de vídeo aprimorada.](../medfound/enhanced-video-renderer.md)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaces de filtro (por <strong>meio de QueryInterface</strong>)</td>
<td>DirectShow interfaces:
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection"><strong>IAMCertifiedOutputProtection</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ibasefilter</strong></a></li>
<li><a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaeventsink"><strong>Imediaeventsink</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>Imediaseeking</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>Iqualitycontrol</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>Iqualprop</strong></a></li>
</ul>
Media Foundation interfaces:<br/>
<ul>
<li><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig"><strong>IEVRFilterConfig</strong></a></li>
<li><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></li>
<li><a href="/windows/desktop/api/evr/nn-evr-imfvideopositionmapper"><strong>IMFVideoPositionMapper</strong></a></li>
<li><a href="/windows/desktop/api/evr/nn-evr-imfvideorenderer"><strong>IMFVideoRenderer</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>Tipos de mídia de pino de entrada</td>
<td>Variável, dependendo do driver de gráficos.</td>
</tr>
<tr class="odd">
<td>Interfaces de pino de entrada (por <strong>meio de QueryInterface</strong>)</td>
<td>DirectShow interfaces:
<ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>Imeminputpin</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>Iqualitycontrol</strong></a></li>
</ul>
Media Foundation interfaces:<br/>
<ul>
<li><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration"><strong>IDirectXVideoMemoryConfiguration</strong></a></li>
<li><a href="/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol"><strong>IEVRVideoStreamControl</strong></a></li>
<li><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>Tipos de mídia de pino de saída</td>
<td>Não aplicável.</td>
</tr>
<tr class="odd">
<td>Interfaces de pino de saída</td>
<td>Não aplicável.</td>
</tr>
<tr class="even">
<td>Filtrar CLSID</td>
<td>CLSID_EnhancedVideoRenderer</td>
</tr>
<tr class="odd">
<td>Executável</td>
<td>evr.dll</td>
</tr>
<tr class="even">
<td><a href="merit.md">Mérito</a></td>
<td>Merit_do_not_use</td>
</tr>
<tr class="odd">
<td><a href="filter-categories.md">Categoria de filtro</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentários

Além das interfaces expostas por meio de **QueryInterface**, o EVR expõe outras interfaces por meio do [**método IMFGetService::GetService.**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) Algumas dessas interfaces são implementadas pelo apresentador EVR ou pelo mixer EVR, em vez do próprio EVR. Se o aplicativo definir um apresentador personalizado ou um mixer no EVR, as versões personalizadas poderão expor um conjunto diferente de interfaces.



| Objeto     | Identificador de Serviço                                              | Interfaces                                                                                                                                                                                                                                                                                                     |
|------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtro EVR | SERVIÇO DE RENDERIZAÇÃO DE VÍDEO DO MR \_ \_ \_ (Consulta EVR ou apresentador)<br/> | [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)<br/> [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)<br/>                                                          |
| Filtro EVR | SERVIÇO DE ACELERAÇÃO DE VÍDEO DO MR \_ \_ \_ (apresentador de consultas)<br/>  | [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9)                                                                                                                                                                                                                                                      |
| Filtro EVR | MR \_ VIDEO \_ MIXER \_ SERVICE(Queries mixer)<br/>             | [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)<br/> [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)<br/> [**IMFVideoMixerControl**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol)<br/> [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)<br/> [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)<br/> |
| Pinos de entrada | SERVIÇO DE \_ \_ ACELERAÇÃO DE VÍDEO DO MR \_                                | [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)                                                                                                                                                                                                                                    |



 

O EVR pode misturar até 16 fluxos de vídeo. O primeiro fluxo de entrada (pino 0) é chamado de *fluxo de referência*. O fluxo de referência sempre aparece primeiro na ordem z. Quaisquer fluxos adicionais são chamados de substreams e são mistos sobre o fluxo de referência. O aplicativo pode alterar a ordem z dos substreams, mas nenhum substream pode ser o primeiro na ordem z.

O driver gráfico determina quais formatos de vídeo têm suporte, mas normalmente eles são limitados ao seguinte:

-   Fluxo de referência: YUV progressivo ou entrelaçado sem alfa por pixel (como NV12 ou YUY2); ou RGB progressivo.
-   Substreams: YUV progressivo com por pixel alfa, como AYUV ou AI44.

Os formatos de substream disponíveis podem depender do formato do fluxo de referência.

O EVR encaminha os comandos de busca upstream por meio do pino 0. Os pinos de substream não encaminham comandos de busca. É responsabilidade do filtro de origem ou divisor manter os substreams sincronizados com o fluxo de referência.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>


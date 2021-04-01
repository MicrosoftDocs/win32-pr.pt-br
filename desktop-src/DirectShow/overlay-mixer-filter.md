---
description: Filtro de mixer de sobreposição
ms.assetid: e80938b7-31f0-467b-a3fa-c4511d14758d
title: Filtro de mixer de sobreposição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26ad8ba8a41a1cdb94eec0f4406c4845f25cda5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825494"
---
# <a name="overlay-mixer-filter"></a>Filtro de mixer de sobreposição

O filtro de mixer de sobreposição é um processador de vídeo projetado especificamente para reprodução de DVD e transmissão de fluxos de vídeo com legenda oculta de linha 21. O mixer de sobreposição também dá suporte a VPEs (extensões de porta de vídeo), permitindo que ele funcione com decodificadores de hardware MPEG-2 ou sintonizadores de TV analógicos que enviam vídeo diretamente para a placa gráfica, em vez do barramento PCI.

> [!Note]  
> O [processador de mixagem de vídeo 9](video-mixing-renderer-filter-9.md) agora é preferido sobre o filtro de mixer de sobreposição, exceto em cenários de VPE.

 

O mixer de sobreposição usa o DirectDraw para renderização. Ele requer uma superfície de sobreposição na placa gráfica. O fluxo de vídeo primário deve estar conectado ao PIN 0. Os fluxos secundários (imagens ocultas ou subfiguras de DVD) estão conectados aos pins 1 e superior. O mixer de sobreposição blits os fluxos secundários diretamente no suface primário; Ele não mistura ou mistura alfa.

O mixer de sobreposição usa o processador de vídeo para o gerenciamento de janelas. O renderizador de vídeo se conecta ao pino de saída do mixer de sobreposição.

Esse filtro é adicionado ao gráfico de filtro automaticamente quando os aplicativos usam as interfaces [**IDvdGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) e [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) para criar o grafo. O Gerenciador do grafo de filtro não adicionará automaticamente o mixer de sobreposição ao grafo.

> [!Note]  
> Na tabela a seguir, os subtipos de mídia aceitos no pino de entrada 0 são dependentes de hardware. O mixer de sobreposição não pode determinar se um subtipo específico tem suporte até que ele crie a superfície do DirectDraw. Portanto, a única maneira de um filtro upstream determinar se um subtipo tem suporte é tentar uma conexão com esse subtipo.

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Filtrar interfaces</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamoverlayfx"><strong>IAMOverlayFX</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties"><strong>IAMVideoDecimationProperties</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo</strong></a>, <a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/previous-versions/windows/desktop/api/Mixerocx/nn-mixerocx-imixerocx"><strong>IMixerOCX</strong></a>, <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a>, <a href="/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify"><strong>IVPNotify</strong></a>, <a href="/previous-versions/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify2"><strong>IVPNotify2</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de mídia de pino de entrada</td>
<td>Tipo principal: MEDIATYPE_Video<br/> Subtipos<br/>
<ul>
<li>MEDIASUBTYPE_Overlay (somente PIN 0)</li>
<li>Formatos YUV do DirectDraw (somente PIN 0)</li>
<li>Formatos de aceleração de vídeo do DirectDraw (somente PIN 0)</li>
<li>Formatos RGB do DirectDraw (todos os Pins de entrada)</li>
</ul>
Tipos de formato:<br/>
<ul>
<li>Format_VIDEOINFO</li>
<li>Format_VIDEOINFO2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces de pino de entrada</td>
<td><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a>, <a href="ikspin.md"><strong>IKsPin</strong></a>, <a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig"><strong>IMixerPinConfig</strong></a>, <a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2"><strong>IMixerPinConfig2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a> (somente PIN 0), <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify"><strong>IVPNotify</strong></a>, <a href="/previous-versions/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify2"><strong>IVPNotify2</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de mídia do pino de saída</td>
<td>MEDIATYPE_Video, MEDIASUBTYPE_Overlay</td>
</tr>
<tr class="odd">
<td>Interfaces de pino de saída</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>CLSID do filtro</td>
<td>CLSID_OverlayMixer</td>
</tr>
<tr class="odd">
<td>CLSID de página de propriedades</td>
<td>Nenhuma página de propriedades.</td>
</tr>
<tr class="even">
<td>Executável</td>
<td>qdvd.dll</td>
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



 

### <a name="remarks"></a>Comentários

O mixer de sobreposição usa o chaveamento de cor de destino para misturar superfícies de vídeo com sobreposições. Ele blits a chave de cor e o vídeo secundário para a superfície primária e envia o vídeo primário para a superfície de sobreposição. Em seguida, a placa gráfica compõe as duas superfícies em seu buffer de quadro.

Para testar se o driver de gráficos dá suporte à sobreposição de hardware, chame **IDirectDraw7:: GetCaps**. Se o campo **dwMaxVisibleOverlays** na estrutura **DDCAPS** for maior que zero, o driver dará suporte à sobreposição de hardware.

Os aplicativos podem controlar alguns comportamentos no mixer de sobreposição por meio da interface [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2) . Os desenvolvedores de jogos podem usar o mixer de sobreposição para exibir vídeo no modo exclusivo do DirectDraw, conforme descrito posteriormente nesta seção. No entanto, o [filtro de mixagem de vídeo 9](video-mixing-renderer-filter-9.md) (VMR-9) agora fornece um melhor suporte ao vídeo em jogos. Para obter mais informações, consulte [usando o processador de mixagem de vídeo](using-the-video-mixing-renderer.md).

As informações a seguir são fornecidas para o benefício dos desenvolvedores de filtro e dos desenvolvedores de jogos que desejam usar o mixer de sobreposição no modo exclusivo do DirectDraw.

**Operações internas do mixer de sobreposição**

O mixer de sobreposição expõe um pino de entrada para cada fluxo de entrada. Normalmente, há três pinos de entrada: pino 0 para dados de vídeo e pinos 1 e 2 para dados de subimagem de linha 21 e DVD. Internamente, o mixer de sobreposição cria um objeto DirectDraw com uma superfície primária que abrange toda a área de trabalho, além de uma superfície de sobreposição cujo retângulo é definido pelo tamanho do fluxo de vídeo no pino 0. Se o decodificador não especificar uma chave de cor, o mixer de sobreposição usará as chaves de cores padrão: cinza escuro para placas gráficas mais recentes e magenta para cartões de cor 256 mais antigos.

> [!Note]  
> Os resultados serão indefinidos se o decodificador entregar dois fluxos de vídeo secundários simultaneamente no mesmo lugar na superfície de sobreposição. (Isso às vezes ocorre com DVDs que contêm fluxos de subimagem e de linha 21.) O vídeo pode piscar ou exibir apenas um dos fluxos.

 

No Windows Vista ou posterior, o mixer de sobreposição desabilita a composição de Gerenciador de Janelas da Área de Trabalho (DWM) se o driver de vídeo oferecer suporte à sobreposição de hardware. Os aplicativos devem evitar o uso do filtro de mixer de sobreposição; Use o VMR-9 ou o EVR (processador de vídeo avançado) em vez disso.

**Conexão upstream com o decodificador de vídeo**

Normalmente, os pinos de entrada do mixer de sobreposição se conectam a um decodificador de vídeo upstream. O fluxo de vídeo primário deve se conectar ao PIN 0. Os fluxos de linha 21 ou subimagem se conectam ao pino 1 ou superior. Se o decodificador for um decodificador de software que usa a CPU do host exclusivamente, a conexão entre o decodificador e o PIN 0 será uma conexão [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) . Se o decodificador usar aceleração de hardware, a conexão com o PIN 0 deverá usar o [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) inferface. Esses dois tipos de conexões são mutuamente exclusivos.

Se o decodificador desenhar diretamente na superfície de sobreposição, ele deverá usar a interface [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) no pino 0 e implementar a interface [**IOverlayNotify**](/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify) .

Os filtros que encapsulam um decodificador de hardware e se conectam ao mixer de sobreposição por meio de uma porta de vídeo devem implementar a interface [**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) . O mixer de sobreposição implementa a interface [**IVPNotify**](/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify) . Essas duas interfaces permitem que o decodificador especifique as superfícies de sobreposição necessárias e habilita o mixer de sobreposição para informar o decodificador do local dessas superfícies na memória de vídeo.

O mixer de sobreposição também garante que o retângulo de vídeo seja dimensionado corretamente. A captura de vídeo envolve certos problemas em relação ao dimensionamento da imagem de visualização e à captura de quadros de vídeo intercalados. Se você estiver desenvolvendo um driver de filtro ou WDM para um dispositivo de captura de vídeo de hardware, consulte as páginas de referência [**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) e [**IVPNotify**](/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify) para obter mais informações sobre esses tópicos.

O mixer de sobreposição não é usado em cenários de captura 1394 ou USB. Ele é usado na captura de vídeo no barramento PCI.

**Conexão downstream com o processador de vídeo**

O mixer de sobreposição tem um pino de saída que se conecta ao filtro de [processador de vídeo](video-renderer-filter.md) . O processador de vídeo, nesse caso, não renderiza o vídeo; Ele simplesmente gerencia a janela de vídeo.

A conexão de PIN usa a interface [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) em vez da interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) . O processador de vídeo passa sua alça de janela por meio do mixer de sobreposição para o DirectDraw, que gerencia a recorte de retângulo. Os aplicativos podem controlar o processador de vídeo por meio das interfaces [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) e [**IBasicVideo2**](/windows/desktop/api/Control/nn-control-ibasicvideo2) no Gerenciador de gráficos de filtro.

**Modo exclusivo do DirectDraw**

O modo exclusivo do DirectDraw do mixer de sobreposição permite que os jogos exibam vídeo em alguma parte da tela. Nesse modo, o mixer de sobreposição renderiza o vídeo diretamente em uma superfície do DirectDraw criada pelo aplicativo de jogo, em vez de uma janela fornecida pelo processador de vídeo. Isso permite que os jogos controlem a chave de cor. O mixer de sobreposição expõe apenas um pino de entrada no modo exclusivo do DirectDraw, o que significa que nenhuma combinação da linha 21 ou da subimagem de DVD pode ser executada nesse modo.

Para usar o mixer de sobreposição no modo exclusivo do DirectDraw, crie uma instância do mixer de sobreposição e consulte-a para a interface [**IDDrawExclModeVideo**](/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo) antes de criar o grafo de filtro. Em seguida, chame [**IDDrawExclModeVideo:: SetDDrawSurface**](/windows/desktop/api/Strmif/nf-strmif-iddrawexclmodevideo-setddrawsurface) para especificar a superfície do DirectDraw para renderização. Uma limitação significativa desse modo é que o jogo não obtém acesso aos bits de vídeo reais. Se você usar **IDDrawExclModeVideo**, seu aplicativo criará a superfície primária e o mixer de sobreposição criará a superfície de sobreposição.

Você também pode usar o modo exclusivo do DirectDraw para executar a renderização sem janela — por exemplo, em uma página da Web — mas isso não é recomendado, pois o mixer de sobreposição não executa nenhuma combinação nesse modo. Isso significa que nenhum dado de linha 21 ou subimagem pode ser exibido.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> </dl>

 

 





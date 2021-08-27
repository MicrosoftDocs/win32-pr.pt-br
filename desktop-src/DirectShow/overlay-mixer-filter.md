---
description: Filtro de mixer de sobreposição
ms.assetid: e80938b7-31f0-467b-a3fa-c4511d14758d
title: Filtro de mixer de sobreposição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 475726607f282ce4b7885ec6c5aea562c0380cb0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476982"
---
# <a name="overlay-mixer-filter"></a>Filtro de mixer de sobreposição

O filtro sobreposição Mixer é um renderador de vídeo projetado especificamente para reprodução de DVD e transmissão de fluxos de vídeo com legendas fechadas de linha 21. O Mixer de sobreposição também dá suporte a VPEs (Extensões de Porta de Vídeo), permitindo que ele funcione com decodificadores MPEG-2 de hardware ou tuners de TV análogos que enviam vídeo diretamente para a placa gráfica, em vez de sobre o barramento PCI.

> [!Note]  
> O [Renderização de Combinação de Vídeo 9](video-mixing-renderer-filter-9.md) agora é preferencial em vez do filtro sobreposição Mixer, exceto em cenários de VPE.

 

A camada de Mixer usa DirectDraw para renderização. Ele requer uma superfície de sobreposição na placa gráfica. O fluxo de vídeo primário deve ser conectado ao pino 0. Fluxos secundários (elementos gráficos de legenda fechada ou subtípicos de DVD) são conectados aos pinos 1 e superior. A sobreposição Mixer blits os fluxos secundários diretamente no suface primário; ele não combina nem combina alfa.

A camada de Mixer usa o Renderador de Vídeo para gerenciamento de janelas. O Renderador de Vídeo conecta-se ao pino de Mixer de saída da sobreposição.

Esse filtro é adicionado ao grafo de filtro automaticamente quando os aplicativos usam as interfaces [**IDvdGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) e [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) para criar o grafo. O Gerenciador Graph Filtro não adicionará automaticamente o Mixer sobreposição ao grafo.

> [!Note]  
> Na tabela a seguir, os subtipos de mídia aceitos no pino de entrada 0 dependem do hardware. A camada Mixer não pode determinar se há suporte para um subtipo específico até que ele crie a superfície directDraw. Portanto, a única maneira de um filtro upstream determinar se há suporte para um subtipo é tentar uma conexão com esse subtipo.

 




| | | Interfaces de filtro | <a href="/windows/desktop/api/Strmif/nn-strmif-iamoverlayfx"><strong>IAMOverlayFX,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties"><strong>IAMVideoDecimationProperties,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo,</strong></a> <a href="ikspropertyset.md"><strong>IKsPropertySet,</strong></a> <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/previous-versions/windows/desktop/api/Mixerocx/nn-mixerocx-imixerocx"><strong>IMixerOCX,</strong></a> <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp,</strong></a> <a href="/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify"><strong>IVPNotify,</strong></a> <a href="/previous-versions/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify2"><strong>IVPNotify2</strong></a> | | Tipos de mídia de pino de entrada | Tipo principal: MEDIATYPE_Video<br /> Subtipos:<br /><ul><li>MEDIASUBTYPE_Overlay (somente pin 0)</li><li>Formatos YUV do DirectDraw (somente pin 0)</li><li>Formatos de Aceleração de Vídeo do DirectDraw (somente pin 0)</li><li>Formatos RGB do DirectDraw (todos os pinos de entrada)</li></ul>Tipos de formato:<br /><ul><li>Format_VIDEOINFO</li><li>Format_VIDEOINFO2</li></ul> | | Interfaces de pino de entrada | <a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator,</strong></a> <a href="ikspin.md"><strong>IKsPin,</strong></a> <a href="ikspropertyset.md"><strong>IKsPropertySet,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig"><strong>IMixerPinConfig,</strong></a> <a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2"><strong>IMixerPinConfig2,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a> (somente pin 0), <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl,</strong></a> <a href="/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify"><strong>IVPNotify,</strong></a> <a href="/previous-versions/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify2"><strong>IVPNotify2</strong></a> | | Tipos de mídia de pino de | MEDIATYPE_Video, MEDIASUBTYPE_Overlay | | Interfaces de pino de | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Filtrar CLSID | CLSID_OverlayMixer | | ClSID da página de propriedades | Nenhuma página de propriedades. | | Arquivo executável | qdvd.dll | | <a href="merit.md">|</a> MERIT_DO_NOT_USE | | <a href="filter-categories.md">Categoria de</a> filtro | CLSID_LegacyAmFilterCategory | 




 

### <a name="remarks"></a>Comentários

A camada de Mixer usa a chave de cores de destino para misturar superfícies de vídeo com sobreposições. Ele blits a chave de cor e o vídeo secundário para a superfície primária e envia o vídeo primário para a superfície de sobreposição. Em seguida, a placa gráfica composição das duas superfícies em seu buffer de quadro.

Para testar se o driver gráfico dá suporte à sobreposição de hardware, chame **IDirectDraw7::GetCaps.** Se o **campo dwMaxVisibleOverlays** na estrutura **DDCAPS** for maior que zero, o driver será compatível com a sobreposição de hardware.

Os aplicativos podem controlar alguns comportamentos na Mixer por meio da interface [**IMixerPinConfig2.**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2) Os desenvolvedores de jogos podem usar Mixer sobreposição para exibir vídeo no Modo Exclusivo do DirectDraw, conforme descrito posteriormente nesta seção. No entanto, o Filtro [de Renderização](video-mixing-renderer-filter-9.md) de Combinação de Vídeo 9 (VMR-9) agora oferece melhor suporte para vídeo em jogos. Para obter mais informações, [consulte Using the Video Mixing Renderer](using-the-video-mixing-renderer.md).

As informações a seguir são fornecidas para o benefício de desenvolvedores de filtros e desenvolvedores de jogos que querem usar o overlay Mixer no modo exclusivo do DirectDraw.

**Sobreposição Mixer operações internas**

O controle sobreposição Mixer expõe um pino de entrada para cada fluxo de entrada. Normalmente, há três pinos de entrada: pin 0 para dados de vídeo e pinos 1 e 2 para dados de subtípico de DVD e linha 21. Internamente, o Mixer de sobreposição cria um objeto DirectDraw com uma superfície primária que abrange toda a área de trabalho, além de uma superfície de sobreposição cujo retângulo é definido pelo tamanho do fluxo de vídeo no Pino 0. Se o decodificador não especificar uma chave de cor, o Mixer sobreposição usará chaves de cores padrão: cinza-escuro para cartões gráficos mais recentes e magenta para cartões de 256 cores mais antigos.

> [!Note]  
> Os resultados serão indefinido se o decodificador entregar dois fluxos de vídeo secundários simultaneamente no mesmo local na superfície de sobreposição. (Isso às vezes ocorre com DVDs que contêm subpicture e fluxos de linha 21.) O vídeo pode piscar ou exibir apenas um dos fluxos.

 

No Windows Vista ou posterior, o recurso sobreposição Mixer desabilitará a composição Gerenciador de Janelas da Área de Trabalho (DWM) se o driver de exibição for compatível com a sobreposição de hardware. Os aplicativos devem evitar o uso do filtro Mixer sobreposição; em vez disso, use a VMR-9 ou o EVR (Renderização de Vídeo Aprimorado).

**Conexão upstream com o decodificador de vídeo**

Normalmente, os pinos de Mixer de entrada do usuário se conectam a um decodificador de vídeo upstream. O fluxo de vídeo primário deve se conectar ao pino 0. Os fluxos de subtípico ou linha 21 se conectam ao pino 1 ou superior. Se o decodificador for um decodificador de software que usa exclusivamente a CPU do host, a conexão entre o decodificador e o Pin 0 será uma [**conexão IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) Se o decodificador usar aceleração de hardware, a conexão com o Pino 0 deverá usar a inferência [**IAMVideoAccelerator.**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) Esses dois tipos de conexões são mutuamente exclusivos.

Se o decodificador se desenhar diretamente na superfície de sobreposição, ele deverá usar a interface [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) no pino 0 e implementar a interface [**IOverlayNotify.**](/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify)

Filtros que quebram um decodificador de hardware e se conectam ao banco de dados Mixer por meio de uma porta de vídeo devem implementar a interface [**IVPConfig.**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) A camada de Mixer implementa a interface [**IVPNotify.**](/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify) Essas duas interfaces permitem que o decodificador especifique as superfícies de sobreposição que ele requer e permitem que o Mixer sobreposição informe o decodificador do local dessas superfícies na memória de vídeo.

A sobreposição Mixer também garante que o retângulo de vídeo seja dimensionado corretamente. A captura de vídeo envolve determinados problemas em relação ao dimensionamento da imagem de visualização e à captura de quadros de vídeo intercalados. Se você estiver desenvolvendo um filtro ou driver WDM para um dispositivo de captura de vídeo de hardware, consulte as páginas de referência [**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) e [**IVPNotify**](/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify) para obter mais informações sobre esses tópicos.

A camada de Mixer não é usada em cenários de captura 1394 ou USB. Ele é usado na captura de vídeo sobre o barramento PCI.

**Conexão downstream com o renderador de vídeo**

O filtro Sobreposição Mixer tem um pino de saída que se conecta ao filtro [do Renderdor de](video-renderer-filter.md) Vídeo. Nesse caso, o Renderador de Vídeo não renderiza o vídeo; ele simplesmente gerencia a janela de vídeo.

A conexão de pino usa a interface [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) em vez da interface [**IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) O Renderador de Vídeo passa seu alça de janela por meio do Mixer sobreposição para DirectDraw, que gerencia o recorte de retângulo. Os aplicativos podem controlar o Video Renderer por meio das interfaces [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) e [**IBasicVideo2**](/windows/desktop/api/Control/nn-control-ibasicvideo2) no Gerenciador Graph Filtro.

**Modo exclusivo do DirectDraw**

A sobreposição Mixer modo exclusivo do DirectDraw permite que os jogos exibem vídeo em alguma parte da tela. Nesse modo, o recurso Sobreposição Mixer renderiza o vídeo diretamente em uma superfície do DirectDraw criada pelo aplicativo de jogo, em vez de em uma janela fornecida pelo Video Renderer. Isso permite que os jogos controlem a chave de cor. O Mixer sobreposição expõe apenas um pino de entrada no modo exclusivo do DirectDraw, o que significa que nenhuma combinação da subpicture de Linha 21 ou DVD pode ser executada nesse modo.

Para usar o Mixer sobreposição no modo exclusivo do DirectDraw, crie uma instância do Mixer sobreposição e consulte-a para a interface [**IDDrawExclModeVideo**](/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo) antes de criar o grafo de filtro. Em [**seguida, chame IDDrawExclModeVideo::SetDDrawSurface**](/windows/desktop/api/Strmif/nf-strmif-iddrawexclmodevideo-setddrawsurface) para especificar a superfície do DirectDraw para renderização. Uma limitação significativa desse modo é que o jogo não tem acesso aos bits de vídeo reais. Se você usar **IDDrawExclModeVideo**, seu aplicativo criará a superfície primária e a camada de Mixer criará a superfície de sobreposição.

Você também pode usar o modo exclusivo do DirectDraw para executar a renderização sem janelas, por exemplo, em uma página da Web, mas isso não é recomendado, porque o Mixer sobreposição não executa nenhuma combinação nesse modo. Isso significa que nenhum dado de linha 21 ou subtípico pode ser exibido.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 





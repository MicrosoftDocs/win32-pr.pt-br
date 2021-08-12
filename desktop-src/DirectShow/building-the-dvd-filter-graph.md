---
description: Criando o filtro de DVD Graph
ms.assetid: 1d2f8284-2deb-4207-b067-24a54d6b286c
title: Criando o filtro de DVD Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 049c8bc52fd382be863cdf5a0e6b124534e0b9280d28536abc58a6f4e64e81e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662641"
---
# <a name="building-the-dvd-filter-graph"></a>Criando o filtro de DVD Graph

assim como ocorre com qualquer aplicativo DirectShow, um aplicativo de reprodução de DVD começa criando um grafo de filtro. DirectShow fornece os seguintes componentes para reprodução de DVD:

-   [construtor de Graph de DVD](dvd-graph-builder.md). Um objeto auxiliar que constrói o grafo de filtro. Ele expõe a interface [**IDvdGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) .
-   Filtro de [navegador de DVD](dvd-navigator-filter.md) . um filtro de DirectShow que manipula reprodução de DVD, navegação e outros comandos.

A reprodução de DVD também requer um decodificador MPEG-2. Os decodificadores de hardware e software MPEG-2 estão disponíveis de terceiros. primeiro, crie uma instância do objeto DVD Graph Builder.


```C++
IDvdGraphBuilder *pBuild = NULL;
hr = CoCreateInstance(CLSID_DvdGraphBuilder, NULL, 
    CLSCTX_INPROC_SERVER, IID_IDvdGraphBuilder, (void **)&pBuild);
```



Neste ponto, você pode selecionar e configurar o renderizador de vídeo antes de criar o restante do grafo. Essa etapa, que é opcional, é descrita mais detalhadamente na próxima seção. se você omitir essa etapa, o construtor de Graph DVD selecionará um renderizador padrão. Em seguida, compile o grafo chamando o método [**IDvdGraphBuilder:: RenderDvdVideoVolume**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume) .


```C++
AM_DVD_RENDERSTATUS buildStatus;
hr = pBuild->RenderDvdVideoVolume(L"Z:\\video_ts", 0, &buildStatus);
```



O primeiro parâmetro é o nome de um diretório que contém os arquivos de DVD. Em um disco DVD, esses arquivos residem em um diretório chamado vídeo \_ TS. se o primeiro parâmetro for **nulo**, o construtor de Graph de DVD usará a primeira unidade que contém um volume de DVD.

O segundo parâmetro contém vários sinalizadores opcionais para escolher o tipo de decodificador (hardware ou software) e outras opções.

O terceiro parâmetro é uma [**estrutura \_ \_ RENDERSTATUS de DVD am**](/windows/win32/api/strmif/ns-strmif-am_dvd_renderstatus) que recebe informações de status. Se o método [**RenderDvdVideoVolume**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume) retornar S \_ false, isso significa que a chamada foi parcialmente bem-sucedida (ou com falha parcial, se você for um pessimista). Por exemplo, o método pode falhar ao renderizar o fluxo de subimagem, embora os outros fluxos sejam renderizados com êxito. Se o método **RenderDvdVideoVolume** retornar um código de erro ou o valor S \_ false, você poderá examinar a estrutura **am \_ DVD \_ RENDERSTATUS** para obter detalhes sobre o erro.

em seguida, obtenha um ponteiro para o filtro Graph Manager chamando [**IDvdGraphBuilder:: GetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getfiltergraph). esse método retorna um ponteiro para o filtro Graph interface [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) do gerenciador.


```C++
IGraphBuilder *pGraph = NULL;
hr =  pBuild->GetFiltergraph(&m_pGraph);
```



Use o método [**IDvdGraphBuilder:: GetDvdInterface**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getdvdinterface) para recuperar interfaces relacionadas a DVD, incluindo o seguinte:

-   [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2). Controla reprodução e comandos de DVD
-   [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2). Retorna informações sobre o estado atual do navegador de DVD.
-   [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder). Controla a exibição da legenda oculta. A exibição de legenda oculta está habilitada por padrão. Para desabilitá-lo, chame [**IAMLine21Decoder:: Setservicestate**](/previous-versions/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setservicestate) com o \_ sinalizador am L21 \_ CCSTATE \_ off.
-   [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio). Controla o volume e o equilíbrio de áudio.

Por exemplo, o código a seguir retorna a interface [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) .


```C++
IDvdControl2 *pDvdControl = NULL;
hr = pBuild->GetDvdInterface(IID_IDvdControl2, (void**)&pDvdControl);
```



a maneira recomendada para criar o grafo de filtro de reprodução de dvd é ter um objeto [dvd Graph Builder](dvd-graph-builder.md) para fazer isso automaticamente. Essa abordagem é demonstrada abaixo e no aplicativo de exemplo de DVD. se você precisar criar o grafo de filtro de DVD manualmente, poderá fazer isso seguindo as regras básicas de criação de grafo discutidas em outro lugar na documentação do DirectShow. em geral, você não deve adicionar, remover, conectar ou desconectar manualmente filtros individuais no grafo criado pelo construtor de Graph de DVD, pois isso pode confundir o código de limpeza.

Configurando o processador de vídeo

DirectShow fornece vários filtros de processador de vídeo. Antes de criar o grafo, você pode escolher o processador de vídeo que preferir. Selecione o renderizador chamando [**IDvdGraphBuilder:: GetDvdInterface**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getdvdinterface) e solicitando uma interface que seja específica para esse renderizador:

-   Mixer filtro de sobreposição: [**IDDrawExclModeVideo**](/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo).
-   Processador de mixagem de vídeo 7 (VMR-7): [**IVMRFilterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig).
-   Processador de mixagem de vídeo 9 (VMR-9): [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9).
-   Processador de vídeo avançado (EVR): [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig).

se você solicitar qualquer uma dessas interfaces antes de criar o grafo de filtro, o DVD Graph Builder criará o renderizador de vídeo correspondente. posteriormente, quando você criar o grafo, o construtor de Graph DVD tentará usar esse processador. Mas se não for possível criar o grafo usando o renderizador selecionado, ele poderá mudar para outro processador. por exemplo, o decodificador MPEG-2 pode não ser compatível com o filtro VMR; nesse caso, o DVD Graph Builder usará como padrão a sobreposição Mixer.

Essas interfaces também lhe dão a oportunidade de configurar o renderizador antes que ele seja conectado ao decodificador. Por exemplo, você pode definir o VMR para usar o modo sem janela em vez do modo de janela padrão. Para obter mais informações sobre renderizadores de vídeo, consulte o tópico [sobre renderização de vídeo em DirectShow](about-video-rendering-in-directshow.md).

no Windows XP e posterior, o construtor de Graph de DVD sempre usa o [processador de mixagem de vídeo 7](video-mixing-renderer-filter-7.md) (VMR-7), a menos que:

-   o chamador consulta as interfaces que encontraram apenas a [Mixer de sobreposição](overlay-mixer-filter.md), como [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2). isso envia uma dica ao construtor de Graph de DVD que o aplicativo deseja usar a sobreposição Mixer e não o VMR. Windows Media Player também tem uma opção de caixa de diálogo para forçar o uso da sobreposição Mixer.
-   O decodificador instalado não é compatível com o VMR. Durante a criação do grafo, a nova interface [**IAMDecoderCaps**](/windows/desktop/api/Strmif/nn-strmif-iamdecodercaps) é usada para verificar o suporte do VMR do decodificador. se isso não estiver presente, o construtor de Graph de DVD usará o Mixer de sobreposição.
-   Ao usar um decodificador de hardware, o decodificador não pode se conectar ao VPM ( [Video Port Manager](video-port-manager.md) ). se um decodificador de hardware não puder usar o VPM, ele não poderá usar o VMR e, portanto, o DVD Graph Builder tentará criar um grafo usando a sobreposição Mixer.
-   O cartão de vídeo é conhecido por ter recursos e/ou recursos insuficientes para dar suporte ao VMR, mas não relata corretamente isso no driver. (alguns casos conhecidos são especificamente excluídos pelo construtor de Graph de DVD.)
-   A conexão entre o decodificador e o VMR falha por qualquer motivo, geralmente devido à falta de VRAM para criar as superfícies necessárias. nesses casos, o DVD Graph Builder alterna o uso do VMR e tenta usar a sobreposição Mixer para criar um grafo.

Modo em janela

no modo de janela (Overlay Mixer ou VMR), o renderizador cria sua própria janela de vídeo. Para tornar essa janela um filho da janela do aplicativo, chame [**IVideoWindow::p o \_ proprietário de UT**](/windows/desktop/api/Control/nf-control-ivideowindow-put_owner) com um identificador para o aplicativo. Além disso, chame [**IVideoWindow::p UT \_ WindowStyle**](/windows/desktop/api/Control/nf-control-ivideowindow-put_windowstyle) para definir os estilos WS- \_ Child e WS \_ CLIPSIBLINGS na janela de vídeo do processador. Para obter mensagens do mouse na janela de vídeo do renderizador, chame [**IVideoWindow::p UT \_ MessageDrain**](/windows/desktop/api/Control/nf-control-ivideowindow-put_messagedrain) com um identificador para a janela do aplicativo. Esse método configura uma "drenagem de mensagem" – a janela de vídeo encaminha todas as mensagens do mouse que ele recebe para a janela de drenagem de mensagem.


```C++
pVideoWindow->put_Owner((OAHWND)hwnd);
pVideoWindow->put_WindowStyle(WS_CHILD | WS_CLIPSIBLINGS);
pVideoWindow->put_MessageDrain((OAHWND)hwnd) ;
```



A mensagem drena torna a seleção de botões de menu de DVD um pouco complicada. Supondo que a janela de vídeo não preencha a área de cliente inteira do aplicativo, alguns eventos do mouse ficarão fora da janela de vídeo. Quando você recebe um evento de mouse de *dentro* da janela de vídeo, você deve processá-lo para navegação de menu do DVD. Eventos de mouse de *fora* da janela de vídeo não devem ser processados. Com o dreno da mensagem, não há como distinguir entre os dois. Além disso, as coordenadas para eventos de mouse da janela de vídeo são relativas à área de cliente da janela de vídeo; Mas eventos de mouse de fora da janela de vídeo são relativos à área do cliente do aplicativo.

Modo sem janela

O modo sem janela evita os problemas com as mensagens do mouse completamente. Você não precisa de uma drenagem de mensagem porque o VMR (ou EVR) não cria sua própria janela no modo sem janela. Em vez disso, ele é desenhado diretamente na janela do aplicativo. Se o retângulo de destino for menor do que a área do cliente do aplicativo, o navegador de DVD levará isso em conta quando calcular as posições do botão DVD. Portanto, quando você recebe uma mensagem de mouse, pode passar as coordenadas diretamente para o navegador de DVD, conforme descrito na seção navegação de menu.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicativos de DVD](dvd-applications.md)
</dt> </dl>

 

 

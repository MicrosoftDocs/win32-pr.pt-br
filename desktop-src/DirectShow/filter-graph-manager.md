---
description: Gerenciador de gráfico de filtro
ms.assetid: b1a53193-27c6-4e86-a5b9-f3c1e4401690
title: Gerenciador de gráfico de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7161f15ea04e1404425d4671ca7991420e0aa993
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825517"
---
# <a name="filter-graph-manager"></a>Gerenciador de gráfico de filtro

O Gerenciador de gráficos de filtro cria e controla os gráficos de filtro. Esse objeto é o componente central no DirectShow. Os aplicativos o usam para criar e controlar gráficos de filtro. O Gerenciador de gráficos de filtro também trata da sincronização, da notificação de eventos e de outros aspectos do controle do grafo de filtro. Crie esse objeto chamando **CoCreateInstance**.

### <a name="clsid"></a>CLSID

Há dois CLSIDs para criar o Gerenciador de gráficos de filtro:



| CLSID                      | Descrição                                                 |
|----------------------------|-------------------------------------------------------------|
| \_FILTERGRAPH CLSID         | Cria o Gerenciador de gráfico de filtro em um thread de trabalho compartilhado. |
| \_FILTERGRAPHNOTHREAD CLSID | Cria o Gerenciador de gráfico de filtro no thread do aplicativo. |



 

Em geral, os aplicativos devem usar CLSID \_ FilterGraph. Ambos os CLSIDs criam o mesmo objeto, mas usam modelos de Threading diferentes:

-   CLSID \_ FilterGraph cria o Gerenciador de gráfico de filtro em um thread de trabalho, que é compartilhado por todas as \_ instâncias de FILTERGRAPH do CLSID dentro do mesmo processo. O thread despacha mensagens enviadas por filtros e controla o tempo de vida de qualquer Windows criado por filtros.
-   CLSID \_ FilterGraphNoThread cria o Gerenciador de gráfico de filtro no thread do aplicativo. Se você usar esse CLSID, o thread que chama **CoCreateInstance** deverá ter um loop de mensagem que expedir mensagens; caso contrário, podem ocorrer deadlocks. Além disso, antes de o thread do aplicativo sair, ele deve liberar o Gerenciador do grafo de filtro e todos os objetos do grafo (como filtros, Pins, relógios de referência e assim por diante).

### <a name="interfaces"></a>Interfaces

O Gerenciador de gráficos de filtro expõe as seguintes interfaces:

-   [**IAMGraphStreams**](/windows/desktop/api/Strmif/nn-strmif-iamgraphstreams)
-   [**IAMStats**](/windows/desktop/api/Control/nn-control-iamstats)
-   [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio)
-   [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo)
-   [**IBasicVideo2**](/windows/desktop/api/Control/nn-control-ibasicvideo2)
-   [**IFilterChain**](/windows/desktop/api/Strmif/nn-strmif-ifilterchain)
-   [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph)
-   [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2)
-   [**IFilterGraph3**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph3)
-   [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)
-   [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)
-   [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig)
-   [**IGraphVersion**](/windows/desktop/api/Strmif/nn-strmif-igraphversion)
-   [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)
-   [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent)
-   [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex)
-   [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)
-   [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter)
-   [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)
-   [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)
-   [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand)
-   [**IRegisterServiceProvider**](/windows/desktop/api/Strmif/nn-strmif-iregisterserviceprovider)
-   [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager)
-   **IServiceProvider**
-   [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep)
-   [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objetos do DirectShow](directshow-objects.md)
</dt> </dl>

 

 




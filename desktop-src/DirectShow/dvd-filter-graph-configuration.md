---
description: Configuração de filtro Graph DVD
ms.assetid: 0c68c456-2240-4090-b45c-bd098cfea645
title: Configuração de filtro Graph DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ece69f77ac4a4e6674bbcd12404a10b7f765a514e18cb31963d2ed7f981799e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118653074"
---
# <a name="dvd-filter-graph-configuration"></a>Configuração de filtro Graph DVD

Esta seção descreve as várias configurações de grafo de filtro para reprodução de DVD DirectShow. Esses diagramas são fornecidos principalmente para referência. O Navegador de DVD cria o grafo, portanto, em geral, não é necessário entender os detalhes de como o grafo está configurado. Para obter mais informações, consulte [Criando o filtro de DVD Graph](building-the-dvd-filter-graph.md).

A ilustração a seguir mostra um grafo de filtro de DVD com um decodificador de software.

![grafo de filtro de dvd para o Windows Xp](images/dvd-graph-xp.png)

Quando um decodificador de hardware está presente, ele normalmente é conectado diretamente à placa de vídeo por uma porta de vídeo. Isso permite que os bits de vídeo decodificados sejam enviados diretamente para o buffer de quadros na placa gráfica sem passar para a memória do host. Para gerenciar essa conexão direta em versões anteriores do Windows, o DirectShow dá suporte a VPE (Extensões de Porta de Vídeo) directDraw por meio de uma interface no Filtro Mixer [Sobreposição](overlay-mixer-filter.md).

> [!Note]  
> A Mixer sobreposição foi preterida.

 

No Windows XP e posterior, um decodificador de hardware pode se conectar ao filtro [gerenciador de porta de](video-port-manager.md) vídeo.

![grafo de dvd para o Windows Xp com um decodificador de hardware](images/dvd-hwgraph-xp.png)

Em todos esses grafos, o Navegador de DVD é o filtro de origem; ele executa várias tarefas:

-   Lê os dados de navegação e vídeo do disco.
-   Demultiplexa os dados de vídeo, áudio e subpicture em fluxos separados.
-   Esvaia os fluxos no grafo para processamento e renderização eventual.
-   Informa sua aplicação de eventos relacionados ao DVD.

No fluxo de áudio, o Navegador de DVD conecta downstream a um decodificador de áudio, que se conecta ao Filtro de [Renderização DirectSound](directsound-renderer-filter.md), o renderdor de áudio padrão. Nos fluxos de vídeo e subpicture, os filtros downstream são o decodificador [](overlay-mixer-filter.md)de vídeo de terceiros e o Renderador de Combinação de Vídeo (ou o Mixer sobreposição e o [Renderador](video-renderer-filter.md) de Vídeo em aplicativos de nível baixo). Se o aplicativo manipular dados com legenda fechada da linha 21, você deverá adicionar o filtro DirectShow Linha 21 do Decodificador 2 ao grafo. Isso envolve uma única chamada de método; o filtro será conectado automaticamente.

Seu aplicativo se comunica com e controla o Navegador de DVD por meio das interfaces personalizadas que o Navegador de DVD expõe: [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)— os métodos "set" — e [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)— os métodos "get". Ele também deve se comunicar com o gerenciador de grafo de filtro (por [**meio de IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)) para parar, iniciar e controlar o grafo. Talvez você também precise controlar outros filtros individuais, como o filtro sobreposição Mixer para alternar entre a exibição em janelas e a tela inteira. Para obter mais informações, consulte [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2). A configuração exata do grafo variará dependendo do tipo de decodificador MPEG-2 que você instalou, se você precisa manipular dados com legenda fechada da linha 21 e outros fatores.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicativos de DVD](dvd-applications.md)
</dt> </dl>

 

 




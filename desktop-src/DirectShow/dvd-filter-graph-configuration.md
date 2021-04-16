---
description: Configuração de grafo de filtro de DVD
ms.assetid: 0c68c456-2240-4090-b45c-bd098cfea645
title: Configuração de grafo de filtro de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec7bb8757e5246fc01309fbef55e654436560b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500638"
---
# <a name="dvd-filter-graph-configuration"></a>Configuração de grafo de filtro de DVD

Esta seção descreve as várias configurações de gráfico de filtro para reprodução de DVD no DirectShow. Esses diagramas são fornecidos principalmente para referência. O navegador de DVD cria o grafo, de modo que, em geral, não é necessário entender os detalhes de como o grafo é configurado. Para obter mais informações, consulte [criando o grafo de filtro de DVD](building-the-dvd-filter-graph.md).

A ilustração a seguir mostra um grafo de filtro de DVD com um decodificador de software.

![Grafo de filtro de DVD para Windows XP](images/dvd-graph-xp.png)

Quando um decodificador de hardware está presente, ele normalmente é conectado diretamente à placa de vídeo por uma porta de vídeo. Isso permite que os bits de vídeo decodificados sejam enviados diretamente para o buffer de quadro na placa gráfica sem passar na memória do host. Para gerenciar essa conexão direta em versões anteriores do Windows, o DirectShow dá suporte a VPE (extensões de porta de vídeo) do DirectDraw por meio de uma interface no [filtro de mixer de sobreposição](overlay-mixer-filter.md).

> [!Note]  
> O mixer de sobreposição agora foi preterido.

 

No Windows XP e posterior, um decodificador de hardware pode se conectar ao filtro do [Gerenciador de portas de vídeo](video-port-manager.md) .

![DVD Graph para Windows XP com um decodificador de hardware](images/dvd-hwgraph-xp.png)

Em todos esses gráficos, o navegador de DVD é o filtro de origem; Ele executa várias tarefas:

-   Lê os dados de navegação e vídeo do disco.
-   Demultiplexa os dados de vídeo, áudio e subimagem em fluxos separados.
-   Bombas os fluxos no grafo para processamento adicional e renderização eventual.
-   Informa seu aplicativo de eventos relacionados a DVD.

No fluxo de áudio, o navegador de DVD conecta o downstream a um decodificador de áudio, que se conecta ao [filtro de processador DirectSound](directsound-renderer-filter.md), o processador de áudio padrão. Nos fluxos de vídeo e subimagem, os filtros downstream são o decodificador de vídeo de terceiros e o processador de mixagem de vídeo (ou o [mixer de sobreposição](overlay-mixer-filter.md)e o [processador de vídeo](video-renderer-filter.md) em aplicativos de nível inferior). Se seu aplicativo tratar dados de linha 21 com legenda codificada, você deverá adicionar o filtro do DirectShow linha 21 do decodificador 2 ao grafo. Isso envolve uma única chamada de método; o filtro será conectado automaticamente.

Seu aplicativo se comunica com o e controla o navegador de DVD por meio das interfaces personalizadas que o navegador de DVD expõe: [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)– os métodos "set" — e [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)– os métodos "Get". Ele também deve se comunicar com o Gerenciador de gráficos de filtro (por meio de [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)) para parar, iniciar e controlar o grafo. Talvez você também precise controlar outros filtros individuais, como o filtro de mixer de sobreposição para alternar entre a exibição em janela e em tela inteira. Para obter mais informações, consulte [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2). A configuração exata do grafo variará dependendo do tipo de decodificador MPEG-2 que você instalou, independentemente de você precisar lidar com os dados de legenda oculta da linha 21 e outros fatores.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicativos de DVD](dvd-applications.md)
</dt> </dl>

 

 




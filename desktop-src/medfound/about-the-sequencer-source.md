---
description: Sobre a origem do Sequencer
ms.assetid: 0d7ce9ca-9f34-4842-bd49-9211ae4454de
title: Sobre a origem do Sequencer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d81799a8bc1e46ade10989bbe485c69e839832fce0ded14220c536809e23e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118065550"
---
# <a name="about-the-sequencer-source"></a>Sobre a origem do Sequencer

A origem do sequenciador permite que [](media-sources.md) um aplicativo reproduza uma coleção de Fontes de Mídia sequencialmente, com transições perfeitas entre as fontes. A origem do sequenciador pode ser usada para os seguintes cenários:

-   Crie uma playlist que alterna perfeitamente de uma fonte de mídia para a próxima.
-   Reproduzir fluxos de várias fontes simultaneamente; por exemplo, reproduza o áudio de um arquivo com o vídeo de outro.
-   Alternar entre fluxos em diferentes fontes de mídia em entradas de playlist consecutivas; por exemplo, uma playlist pode ter entradas que compartilham a mesma fonte de vídeo, enquanto cada entrada contém uma fonte de áudio diferente.

Para cada elemento de uma playlist, o aplicativo cria uma topologia separada. As fontes de mídia nessas topologias são conhecidas como fontes *nativas*, para diferenciá-las da origem do sequenciador. Durante *a* reprodução, toda a sequência de topologias é chamada de apresentação e cada topologia dentro da sequência é chamada de *segmento*.

A reprodução é controlada pela Sessão [de Mídia](media-session.md), que fornece controles de transporte, como reproduzir, pausar e parar. A Sessão de Mídia também gerencia o tempo de apresentação e envia eventos para o aplicativo. (Os eventos da origem do sequenciador são encaminhados para o aplicativo por meio da Sessão de Mídia.)

Para criar uma playlist, o aplicativo cria uma ou mais topologias de reprodução e as coloca na fila na origem do sequenciador na ordem desejada de reprodução. Internamente, a origem do sequenciador modifica as topologias para que os nós de origem apontem para a origem do sequenciador em vez da origem nativa. O aplicativo envia essas topologias modificadas, em vez das topologias originais, para a Sessão de Mídia. Isso permite que a origem do sequenciador agregreque as fontes nativas e se comunique com a Sessão de Mídia.

Para obter transições perfeitas entre segmentos, a origem do sequenciador pré-rolla cada segmento. Enquanto um segmento está sendo reproduzindo e antes de ser hora de reproduzir o segmento a seguir, a origem do sequenciador dispara um evento [MENewPresentation](menewpresentation.md) que contém um descritor de apresentação. O aplicativo usa esse descritor de apresentação para obter a topologia para o próximo segmento na apresentação e enfilra a topologia na Sessão de Mídia.

A ilustração a seguir mostra o fluxo de dados para entradas de playlist por meio da origem do sequenciador. O aplicativo usa o resolvedor de origem para criar as fontes nativas, cria topologias para cada segmento e enfilra as topologias na origem do sequenciador.

![diagrama mostrando o fluxo de dados de segmentos de imfmediasession, imfsequencersource e playlist que levam à imfmediasource](images/dbf41a05-d8cc-4502-9cd3-74e5d1ce04a0.gif)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como criar uma playlist](how-to-create-a-playlist.md)
</dt> <dt>

[Topologias](topologies.md)
</dt> <dt>

[Usando a origem do Sequencer](using-the-sequencer-source.md)
</dt> <dt>

[Origem do Sequencer](sequencer-source.md)
</dt> </dl>

 

 




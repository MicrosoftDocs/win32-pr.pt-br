---
description: Sobre a origem do sequenciador
ms.assetid: 0d7ce9ca-9f34-4842-bd49-9211ae4454de
title: Sobre a origem do sequenciador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d8de3e0ff46cab1e68b767294633ecd09ebc161
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501842"
---
# <a name="about-the-sequencer-source"></a>Sobre a origem do sequenciador

A origem do sequenciador permite que um aplicativo reproduza uma coleção de [fontes de mídia](media-sources.md) sequencialmente, com transições diretas entre as fontes. A origem do sequenciador pode ser usada para os seguintes cenários:

-   Crie uma lista de reprodução que alterna diretamente de uma fonte de mídia para a próxima.
-   Reproduzir fluxos de várias fontes simultaneamente; por exemplo, reproduza o áudio de um arquivo com o vídeo de outro.
-   Alternar entre fluxos em diferentes fontes de mídia em entradas de playlist consecutivas; por exemplo, uma lista de reprodução pode ter entradas que compartilham a mesma fonte de vídeo enquanto cada entrada contém uma fonte de áudio diferente.

Para cada elemento de uma lista de reprodução, o aplicativo cria uma topologia separada. As fontes de mídia nessas topologias são chamadas de *Fontes nativas*, para distingui-las da origem do sequenciador. Durante a reprodução, toda a sequência de topologias é chamada de *apresentação*, e cada topologia dentro da sequência é chamada de *segmento*.

A reprodução é controlada pela [sessão de mídia](media-session.md), que fornece controles de transporte, como reproduzir, pausar e parar. A sessão de mídia também gerencia o tempo de apresentação e envia eventos para o aplicativo. (Os eventos da origem do sequenciador são encaminhados para o aplicativo por meio da sessão de mídia.)

Para criar uma lista de reprodução, o aplicativo cria uma ou mais topologias de reprodução e as enfileira na origem do sequenciador na ordem desejada de reprodução. Internamente, a origem do sequenciador modifica as topologias para que os nós de origem apontem para a origem do sequenciador em vez da fonte nativa. O aplicativo envia essas topologias modificadas, em vez das topologias originais, para a sessão de mídia. Isso permite que a origem do sequenciador agregue as fontes nativas e se comunique com a sessão de mídia.

Para obter transições diretas entre segmentos, a origem do sequenciador se registra em cada segmento. Enquanto um segmento está sendo reproduzido, e antes de ser a hora de reproduzir o segmento a seguir, a origem do sequenciador dispara um evento [MENewPresentation](menewpresentation.md) que contém um descritor de apresentação. O aplicativo usa este descritor de apresentação para obter a topologia para o próximo segmento na apresentação e enfileira a topologia na sessão de mídia.

A ilustração a seguir mostra o fluxo de dados para entradas de playlist por meio da origem do sequenciador. O aplicativo usa o resolvedor de origem para criar as fontes nativas, cria topologias para cada segmento e enfileira as topologias na origem do sequenciador.

![diagrama mostrando o fluxo de dados dos segmentos imfmediasession, imfsequencersource e playlist que levam ao imfmediasource](images/dbf41a05-d8cc-4502-9cd3-74e5d1ce04a0.gif)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como criar uma lista de reprodução](how-to-create-a-playlist.md)
</dt> <dt>

[Topologias](topologies.md)
</dt> <dt>

[Usando a origem do sequenciador](using-the-sequencer-source.md)
</dt> <dt>

[Origem do sequenciador](sequencer-source.md)
</dt> </dl>

 

 




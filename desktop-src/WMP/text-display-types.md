---
title: Tipos de exibição de texto
description: Tipos de exibição de texto
ms.assetid: 6aa3fc89-e5f5-420f-82e0-c605676078cb
keywords:
- Aparências móveis do Windows Media Player, texto
- texto em capas, tipos de exibição
- capas, texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4fa8871d889a271bcbc59ce7b3118bc05be2eb7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635590"
---
# <a name="text-display-types"></a>Tipos de exibição de texto

Você não precisa incluir exibições de texto em sua capa, mas há muitas instâncias em que você talvez queira. Por exemplo, talvez você queira incluir um TrackBar de busca para permitir que o usuário se mova para qualquer posição no item de mídia, mas você também pode desejar incluir uma exibição de texto que mostre o número de segundos decorridos desde que o item de mídia atual começou a ser reproduzido.

**Exibir caixas**

Estes são vários atributos que um elemento de texto pode exibir:

-   Hora
-   7.1
-   Rastrear\#
-   \#Controla
-   Título
-   Autor
-   Direitos autorais
-   Nome de arquivo
-   FilenameExt
-   Bitrate
-   Frequência
-   Status
-   VolPercent

Para obter mais informações sobre tipos de exibição de texto, consulte a seção [texto](text.md) da referência de capa.

**Letreiro digital de rolagem**

Além de usar os elementos de texto individuais, você pode combinar um ou mais atributos em um letreiro de texto de rolagem. Isso será útil se você quiser exibir um agrupamento de informações de texto relacionadas em uma pequena área. Por exemplo, você pode exibir informações de título, autor e direitos autorais em um letreiro.

Para obter mais informações sobre como criar uma marca de texto, consulte a seção [Marquee](marquee.md) da referência de capa.

**Exibição de status**

Outro tipo de exibição de texto é a exibição de status. Isso permite que você exiba automaticamente informações sobre o estado atual do Windows Media Player Mobile. Por exemplo, a exibição de status informará ao usuário quando um item de mídia estiver armazenando em buffer para que seja evidente que o jogador está funcionando.

As seguintes mensagens são exibidas na exibição de status:

-   de resposta
-   Connecting
-   Em Pausa
-   Reproduzindo
-   Ready
-   Parado

> [!Note]  
> Quando um item de mídia estiver sendo reproduzido, a exibição do status será girada através do subtítulo, do artista, do álbum, do gênero e da taxa de bits atual.

 

Para obter informações sobre como criar uma exibição de status por meio do elemento status, consulte a seção [status](status.md) da referência de Skin; no entanto, é preferível que você use o atributo status no elemento Text em vez do elemento status.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Funcionalidade móvel do Windows Media Player**](windows-media-player-mobile-functionality.md)
</dt> </dl>

 

 





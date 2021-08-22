---
title: Tipos de exibição de texto
description: Tipos de exibição de texto
ms.assetid: 6aa3fc89-e5f5-420f-82e0-c605676078cb
keywords:
- Windows Media Player Capas móveis, texto
- texto em capas, tipos de exibição
- skins,text
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01826f35db0d3877a3ecd34c351315872760b1b9b0713a36955bb3161ed6ba8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134599"
---
# <a name="text-display-types"></a>Tipos de exibição de texto

Você não precisa incluir exibições de texto em sua capa, mas há muitas instâncias em que você pode querer. Por exemplo, talvez você queira incluir uma barra de faixa Seek para permitir que o usuário se mova para qualquer posição no item de mídia, mas também pode incluir uma exibição de texto que mostra o número de segundos decorridos desde que o item de mídia atual começou a ser exibido.

**Caixas de exibição**

Veja a seguir vários atributos que um elemento de texto pode exibir:

-   Tempo
-   Playlist
-   Rastrear\#
-   \#Faixas
-   Título
-   Autor
-   Direitos autorais
-   Nome de arquivo
-   FilenameExt
-   Bitrate
-   Frequência
-   Status
-   VolPercent

Para obter mais informações sobre tipos de exibição de texto, consulte a [seção Texto](text.md) da Referência de Capa.

**Marca de rolagem**

Além de usar os elementos de texto individuais, você pode combinar um ou mais atributos em um letreiro de texto de rolagem. Isso será útil se você quiser exibir um grupo de informações de texto relacionadas em uma pequena área. Por exemplo, você pode exibir informações de Título, Autor e Direitos Autorais em uma Marca.

Para obter mais informações sobre como criar um letreiro de texto, consulte a seção [Marquee](marquee.md) da Referência de Capa.

**Exibição de status**

Outro tipo de exibição de texto é a exibição de status. Isso permite exibir automaticamente informações sobre o estado atual do Windows Media Player Mobile. Por exemplo, a exibição de status informará o usuário quando um item de mídia estiver em buffer para que seja evidente que o Player está funcionando.

As seguintes mensagens aparecem na exibição de status:

-   de resposta
-   Connecting
-   Em Pausa
-   Reproduzindo
-   Ready
-   Parado

> [!Note]  
> Quando um item de mídia estiver sendo exibido, a exibição de status girará por meio de subtítulo, música, gênero e taxa de bits atual.

 

Para obter informações sobre como criar uma exibição de status por meio do elemento Status, consulte a seção [Status](status.md) da Referência de Capa; no entanto, é preferível que você use o atributo de status no elemento Text em vez do elemento Status.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Windows Media Player Funcionalidade móvel**](windows-media-player-mobile-functionality.md)
</dt> </dl>

 

 





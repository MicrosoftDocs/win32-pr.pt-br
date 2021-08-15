---
title: usando bordas em pacotes de Download de mídia Windows (preterido)
description: usando bordas em pacotes de Download de mídia Windows (preterido)
ms.assetid: d3961c5f-8cce-439d-9a13-41be2f45d92c
keywords:
- Windows metaarquivos de mídia, Windows pacotes de Download de mídia
- Windows Media Player, Windows pacotes de Download de mídia
- metaarquivos, Windows pacotes de Download de mídia
- Windows pacotes de Download de mídia Windows mídia
- bordas, sobre
- Windows Pacotes de download de mídia, bordas
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 851edf0d2291d41212cf44829219235426463733ce95a99c3d59187eba490ca4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117931800"
---
# <a name="using-borders-in-windows-media-download-packages-deprecated"></a>usando bordas em pacotes de Download de mídia Windows (preterido)

esta página documenta um recurso que pode estar indisponível em versões futuras do Windows Media Player e o SDK do Windows Media Player.

As bordas permitem que você crie uma interface gráfica do usuário personalizada para o conteúdo do pacote. A borda pode incluir elementos como imagens, controles interativos e links para sites. Você pode usar bordas em casos em que deseja adicionar valor adicional ao conteúdo do pacote, como para identidade visual ou publicidade. depois que os usuários baixarem e abrirem seu pacote de download de mídia Windows, o Windows Media Player exibirá automaticamente a borda personalizada quando ele reproduzir o conteúdo empacotado.

ao contrário de uma capa, que permite que os usuários substituam completamente a interface do usuário do Windows Media Player, uma borda é exibida apenas no painel em **execução** do Player de modo completo. No entanto, as mesmas ferramentas e tecnologias que você usa para criar capas também são usadas para criar bordas. A ilustração a seguir mostra uma borda.

![uma borda exibida no Windows Media Player 10](images/border-v10.png)

É importante entender as técnicas básicas para criar uma capa antes de tentar criar uma borda. A programação de borda é realizada usando duas linguagens de programação: linguagem XML (XML) e Microsoft JScript. O XML é usado para definir elementos de interface, como botões, controles deslizantes e caixas de texto. Você não precisa entender todos os detalhes do XML, já que não precisa escrever novos elementos de código XML; Você pode simplesmente usar aquelas fornecidas pelo Windows Media Player. embora JScript não seja necessário para a criação de bordas, ela pode ser usada para fornecer funcionalidade adicional.

Um arquivo de borda compactado com uma extensão de nome de arquivo. wmz inclui um arquivo de definição de borda com uma extensão de nome de arquivo. WMS e todos os arquivos de imagem usados dentro da borda.

para incluir uma borda em um pacote de Download de mídia Windows, basta criar uma borda e fazer referência a essa borda em uma lista de reprodução de metarquivo de mídia Windows. o arquivo de borda é carregado em Windows Media Player depois que o Player analisa o metarquivo e interpreta o elemento de **capa** que faz referência à borda. O elemento **Skin** é usado somente para as bordas, e o atributo href do elemento **Skin** pode fazer referência a apenas uma capa para cada pacote.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**bordas para Windows Media Player (preterido)**](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[**Windows Pacotes de download de mídia (preterido)**](windows-media-download-packages--deprecated.md)
</dt> <dt>

[**Windows Media Player Skin**](windows-media-player-skins.md)
</dt> </dl>

 

 





---
title: Usando bordas em pacotes de download do Windows Media (preterido)
description: Usando bordas em pacotes de download do Windows Media (preterido)
ms.assetid: d3961c5f-8cce-439d-9a13-41be2f45d92c
keywords:
- Metaarquivos do Windows Media, pacotes de download do Windows Media
- Windows Media Player, pacotes de download do Windows Media
- metaarquivos, pacotes de download do Windows Media
- Windows Media, pacotes de download do Windows Media
- bordas, sobre
- Pacotes de download do Windows Media, bordas
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 87f7d0fec341bb79bfe9b8dd739b63a9ba3a66ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364089"
---
# <a name="using-borders-in-windows-media-download-packages-deprecated"></a>Usando bordas em pacotes de download do Windows Media (preterido)

Esta página documenta um recurso que pode não estar disponível em versões futuras do Windows Media Player e no SDK do Windows Media Player.

As bordas permitem que você crie uma interface gráfica do usuário personalizada para o conteúdo do pacote. A borda pode incluir elementos como imagens, controles interativos e links para sites. Você pode usar bordas em casos em que deseja adicionar valor adicional ao conteúdo do pacote, como para identidade visual ou publicidade. Depois que os usuários baixarem e abrirem o pacote de download do Windows Media, o Windows Media Player exibirá automaticamente sua borda personalizada quando ele reproduzir o conteúdo empacotado.

Ao contrário de uma capa, que permite que os usuários substituam completamente a interface do usuário do Windows Media Player, uma borda é exibida apenas no painel em **execução** do player de modo completo. No entanto, as mesmas ferramentas e tecnologias que você usa para criar capas também são usadas para criar bordas. A ilustração a seguir mostra uma borda.

![uma borda exibida no Windows Media Player 10](images/border-v10.png)

É importante entender as técnicas básicas para criar uma capa antes de tentar criar uma borda. A programação de borda é realizada usando duas linguagens de programação: linguagem XML (XML) e Microsoft JScript. O XML é usado para definir elementos de interface, como botões, controles deslizantes e caixas de texto. Você não precisa entender todos os detalhes do XML, já que não precisa escrever novos elementos de código XML; Você pode simplesmente usar aquelas fornecidas pelo Windows Media Player. Embora o JScript não seja necessário para a criação de bordas, ele pode ser usado para fornecer funcionalidade adicional.

Um arquivo de borda compactado com uma extensão de nome de arquivo. wmz inclui um arquivo de definição de borda com uma extensão de nome de arquivo. WMS e todos os arquivos de imagem usados dentro da borda.

Para incluir uma borda em um pacote de download do Windows Media, basta criar uma borda e fazer referência a essa borda em uma lista de reprodução do metarquivo do Windows Media. O arquivo de borda é carregado no Windows Media Player depois que o Player analisa o metarquivo e interpreta o elemento de **capa** que faz referência à borda. O elemento **Skin** é usado somente para as bordas, e o atributo href do elemento **Skin** pode fazer referência a apenas uma capa para cada pacote.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Bordas do Windows Media Player (preterido)**](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[**Pacotes de download do Windows Media (preterido)**](windows-media-download-packages--deprecated.md)
</dt> <dt>

[**Capas do Windows Media Player**](windows-media-player-skins.md)
</dt> </dl>

 

 





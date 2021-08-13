---
title: Sobre a biblioteca
description: Sobre a biblioteca
ms.assetid: a43c57ac-deb4-4c86-a8a2-bcfd214b9d0a
keywords:
- Windows Media Player, biblioteca
- Windows Media Player modelo de objeto, biblioteca
- modelo de objeto, biblioteca
- Windows Media Player ActiveX controle, biblioteca para o modelo de objeto
- ActiveX controle, biblioteca para modelo de objeto
- Windows Media Player Controle de ActiveX móvel, biblioteca para o modelo de objeto
- Windows Media Player Móvel, biblioteca para o modelo de objeto
- Windows Media Player, sobre
- library,about
- metadados, Windows Media Player biblioteca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63fdaa19fc8be11de1886074a21b0cc1fb6d4be7dde73faa05c67e1f496ac17c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470346"
---
# <a name="about-the-library"></a>Sobre a biblioteca

A biblioteca é um banco de dados de informações, ou metadados, sobre o conteúdo de mídia digital que está disponível para Windows Media Player. Algumas das informações são exibidas no **painel** Biblioteca no Player; mais dele está disponível por meio de código.

(No Windows Media Player Série 9 e anteriores, esse recurso é chamado **de Biblioteca de Mídia**.)

A biblioteca fornece aos usuários uma maneira fácil de organizar e acessar o conteúdo de mídia digital. Por exemplo, os usuários podem exibir música organizada por álbum, por artista, gênero ou simplesmente como uma lista de todas as músicas. Você pode usar o Windows Media Player de objeto do SDK para acessar a biblioteca para reproduzir conteúdo, recuperar playlists, adicionar conteúdo, remover conteúdo e alterar os metadados associados. Windows Media Player protege a privacidade dos usuários restringindo sua capacidade de acessar a biblioteca do código em determinadas condições. Para obter mais informações sobre direitos de acesso, consulte [Acesso à biblioteca.](library-access.md)

A biblioteca armazena metadados sobre dois tipos básicos de conteúdo de mídia digital. O primeiro tipo, itens de mídia digital, são arquivos de conteúdo individuais, como uma faixa de música ou uma foto. O segundo tipo, playlists, são arquivos que representam um grupo de itens de mídia digital, normalmente destinados a serem tocados em uma ordem especificada. Os metadados associados ao conteúdo de mídia digital são armazenados como pares nome-valor. Por exemplo, os metadados que descrevem a pessoa que realizou uma música são denominados "Artist" e o valor associado a ela normalmente é uma cadeia de caracteres de texto que contém o nome do ator. Cada nome de metadados exclusivo é chamado de *atributo*. Para uma lista de atributos com suporte, consulte a [Referência de atributo](attribute-reference.md). Para obter informações sobre como usar atributos no código, consulte [Atributos de item de mídia](media-item-attributes.md).

As seções a seguir fornecem mais informações sobre como trabalhar com a biblioteca:

-   [Acessando a biblioteca programaticamente](accessing-the-library-programmatically.md)
-   [Sobre os Serviços de Biblioteca](about-library-services.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre o modelo de objeto do player**](about-the-player-object-model.md)
</dt> </dl>

 

 





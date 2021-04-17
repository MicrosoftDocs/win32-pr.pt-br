---
title: Sobre a biblioteca
description: Sobre a biblioteca
ms.assetid: a43c57ac-deb4-4c86-a8a2-bcfd214b9d0a
keywords:
- Windows Media Player, biblioteca
- Modelo de objeto do Windows Media Player, biblioteca
- modelo de objeto, biblioteca
- Controle ActiveX do Windows Media Player, biblioteca para modelo de objeto
- Controle ActiveX, biblioteca para modelo de objeto
- Controle ActiveX móvel do Windows Media Player, biblioteca para modelo de objeto
- Windows Media Player Mobile, biblioteca para modelo de objeto
- Biblioteca do Windows Media Player, sobre
- biblioteca, sobre
- metadados, biblioteca do Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1781329a78bcb2e9cb25c45135e03465b9d63df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105813394"
---
# <a name="about-the-library"></a>Sobre a biblioteca

A biblioteca é um banco de dados de informações, ou *metadados*, sobre o conteúdo de mídia digital disponível para o Windows Media Player. Algumas das informações são exibidas no painel **biblioteca** no Player; mais informações estão disponíveis por meio de código.

(No Windows Media Player 9 Series e versões anteriores, esse recurso é chamado de **biblioteca de mídia**.)

A biblioteca oferece aos usuários uma maneira fácil de organizar e acessar o conteúdo de mídia digital. Por exemplo, os usuários podem exibir músicas organizadas por álbum, por artista, por gênero ou simplesmente como uma lista de todas as músicas. Você pode usar o modelo de objeto do SDK do Windows Media Player para acessar a biblioteca para reproduzir conteúdo, recuperar listas de reprodução, adicionar conteúdo, remover conteúdo e alterar os metadados associados. O Windows Media Player protege a privacidade dos usuários restringindo sua capacidade de acessar a biblioteca a partir do código sob determinadas condições. Para obter mais informações sobre direitos de acesso, consulte [acesso à biblioteca](library-access.md).

A biblioteca armazena metadados sobre dois tipos básicos de conteúdo de mídia digital. O primeiro tipo, itens de mídia digital, são arquivos de conteúdo individuais, como uma faixa de música ou uma foto. O segundo tipo, listas de reprodução, são arquivos que representam um grupo de itens de mídia digital, normalmente destinados a serem reproduzidos em uma ordem especificada. Os metadados associados ao conteúdo de mídia digital são armazenados como pares de nome-valor. Por exemplo, os metadados que descrevem a pessoa que realizou uma música se chamaram de "artista" e o valor associado a ele normalmente é uma cadeia de caracteres de texto que contém o nome do executor. Cada nome de metadados exclusivo é chamado de *atributo*. Para obter uma lista de atributos com suporte, consulte a [referência de atributo](attribute-reference.md). Para obter informações sobre como usar atributos no código, consulte [atributos de item de mídia](media-item-attributes.md).

As seções a seguir fornecem mais informações sobre como trabalhar com a biblioteca:

-   [Acessando a biblioteca programaticamente](accessing-the-library-programmatically.md)
-   [Sobre os serviços de biblioteca](about-library-services.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre o modelo de objeto do Player**](about-the-player-object-model.md)
</dt> </dl>

 

 





---
title: Elemento PLAYER
description: Elemento PLAYER
ms.assetid: 009090b3-0055-4700-9078-0749da239674
keywords:
- Capas do Windows Media Player, elemento PLAYER
- capas, elemento PLAYER
- Elemento PLAYER
- referência para capas, elemento PLAYER
- elementos, PLAYER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a50eb4383eab279c28b75467a9ed803501e7720b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084101"
---
# <a name="player-element"></a>Elemento PLAYER

O elemento **Player** permite definir manipuladores de eventos e especificar a propriedade **URL** do objeto **Player** em tempo de design em um arquivo de definição de capa. No código de script, o objeto **Player** é acessado por meio do atributo global **Player** , em vez de um nome especificado por um atributo de **ID** , que não tem suporte do elemento **Player** .

O elemento **Player** dá suporte ao atributo a seguir.



| Atributo             | Descrição                                          |
|-----------------------|------------------------------------------------------|
| [URL](player-url.md) | Especifica ou recupera o nome do arquivo a ser reproduzido. |



 

O elemento **Player** pode implementar manipuladores de eventos para os eventos a seguir acionados do objeto **Player** .



| Evento                                                                                            | Descrição                                                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [AudioLanguageChange](player-player-audiolanguagechange.md)                                     | Ocorre quando o idioma de áudio atual é alterado.                                  |
| [de resposta](player-player-buffering.md)                                                         | Ocorre quando o Windows Media Player inicia ou termina o armazenamento em buffer.                       |
| [CdromMediaChange](player-player-cdrommediachange.md)                                           | Ocorre quando a mídia do CD é alterada.                                                |
| [CurrentItemChange](player-player-currentitemchange.md)                                         | Ocorre quando o item atual é alterado.                                            |
| [CurrentMediaItemAvailable](player-player-currentmediaitemavailable.md)                         | Ocorre quando o item de mídia atual fica disponível.                            |
| [CurrentPlaylistChange](player-player-currentplaylistchange.md)                                 | Ocorre quando a playlist atual é alterada.                                        |
| [CurrentPlaylistItemAvailable](player-player-currentplaylistitemavailable.md)                   | Ocorre quando o item da playlist atual se torna disponível.                         |
| [DomainChange](player-player-domainchange.md)                                                   | Ocorre quando o domínio do DVD é alterado.                                              |
| [Erro](player-player-error.md)                                                                 | Ocorre quando o controle do Windows Media Player tem uma condição de erro.             |
| [MarkerHit](player-player-markerhit.md)                                                         | Ocorre quando o Windows Media Player encontra um marcador no clipe.                |
| [MediaChange](player-player-mediachange.md)                                                     | Ocorre quando um item de mídia é alterado.                                                |
| [MediaCollectionAttributeStringAdded](player-player-mediacollectionattributestringadded.md)     | Ocorre quando um valor de atributo é adicionado à biblioteca.                          |
| [MediaCollectionAttributeStringChanged](player-player-mediacollectionattributestringchanged.md) | Ocorre quando um valor de atributo na biblioteca é alterado.                        |
| [MediaCollectionAttributeStringRemoved](player-player-mediacollectionattributestringremoved.md) | Ocorre quando um valor de atributo é removido da biblioteca.                      |
| [MediaCollectionChange](player-player-mediacollectionchange.md)                                 | Ocorre quando o objeto **mediacollection** é alterado.                              |
| [MediaError](player-player-mediaerror.md)                                                       | Ocorre quando o objeto de **mídia** tem uma condição de erro.                         |
| [ModeChange](player-player-modechange.md)                                                       | Ocorre ao alternar entre o modo de ordem aleatória e normal.                           |
| [OpenPlaylistSwitch](player-player-openplaylistswitch.md)                                       | Ocorre quando um título em um DVD começa a ser reproduzido.                                     |
| [OpenStateChange](player-player-openstatechange.md)                                             | Ocorre quando o *Player*. alterações de **OpenState** .                                      |
| [PlaylistChange](player-player-playlistchange.md)                                               | Ocorre quando uma playlist é alterada.                                                  |
| [PlaylistCollectionChange](player-player-playlistcollectionchange.md)                           | Ocorre quando algo é alterado na coleção de playlist.                        |
| [PlaylistCollectionPlaylistAdded](player-player-playlistcollectionplaylistadded.md)             | Ocorre quando uma playlist é adicionada à coleção de playlist.                      |
| [PlaylistCollectionPlaylistRemoved](player-player-playlistcollectionplaylistremoved.md)         | Ocorre quando uma playlist é removida da coleção de playlist.                  |
| [PlayStateChange](player-player-playstatechange.md)                                             | Ocorre quando o *Player*. alterações de **PlayState** .                                      |
| [PositionChange](player-player-positionchange.md)                                               | Ocorre quando o *Player*. de *controle*. **CurrentPosition** alterações.                     |
| [ScriptCommand](player-player-scriptcommand.md)                                                 | Ocorre quando o Windows Media Player encontra um comando de script inserido em um arquivo. |
| [StatusChange](player-player-statuschange.md)                                                   | Ocorre quando o valor da propriedade **status** é alterado.                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Objeto de jogador**](player-object.md)
</dt> <dt>

[**Referência de programação de capa**](skin-programming-reference.md)
</dt> </dl>

 

 





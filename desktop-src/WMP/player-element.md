---
title: Elemento PLAYER
description: Elemento PLAYER
ms.assetid: 009090b3-0055-4700-9078-0749da239674
keywords:
- Windows Media Player capas, elemento PLAYER
- skins, elemento PLAYER
- Elemento PLAYER
- referência para capas, elemento PLAYER
- elementos, PLAYER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8bef2e7758a0146ae6197d17dc3790011a758f9d2fa4e3d54af9461a8b870c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338112"
---
# <a name="player-element"></a>Elemento PLAYER

O **elemento PLAYER** permite definir manipuladores de eventos e especificar a propriedade **URL** do objeto **Player** em tempo de design dentro de um arquivo de definição de capa. No código de script, o objeto **Player** é acessado por meio do atributo global do **player,** em vez de por meio de um nome especificado por um atributo **de ID,** que não é suportado pelo **elemento PLAYER.**

O **elemento PLAYER** dá suporte ao atributo a seguir.



| Atributo             | Descrição                                          |
|-----------------------|------------------------------------------------------|
| [URL](player-url.md) | Especifica ou recupera o nome do arquivo a ser reproduzir. |



 

O **elemento PLAYER** pode implementar manipuladores de eventos para os eventos a seguir disparados do **objeto** Player.



| Evento                                                                                            | Descrição                                                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [AudioLanguageChange](player-player-audiolanguagechange.md)                                     | Ocorre quando a linguagem de áudio atual é muda.                                  |
| [de resposta](player-player-buffering.md)                                                         | Ocorre quando o Windows Media Player começa ou termina o buffer.                       |
| [CdromMediaChange](player-player-cdrommediachange.md)                                           | Ocorre quando a mídia de CD é muda.                                                |
| [CurrentItemChange](player-player-currentitemchange.md)                                         | Ocorre quando o item atual é atualizado.                                            |
| [CurrentMediaItemAvailable](player-player-currentmediaitemavailable.md)                         | Ocorre quando o item de mídia atual fica disponível.                            |
| [CurrentPlaylistChange](player-player-currentplaylistchange.md)                                 | Ocorre quando a playlist atual é mudada.                                        |
| [CurrentPlaylistItemAvailable](player-player-currentplaylistitemavailable.md)                   | Ocorre quando o item de playlist atual fica disponível.                         |
| [DomainChange](player-player-domainchange.md)                                                   | Ocorre quando o domínio de DVD muda.                                              |
| [Erro](player-player-error.md)                                                                 | Ocorre quando o controle Windows Media Player tem uma condição de erro.             |
| [MarkerHit](player-player-markerhit.md)                                                         | Ocorre quando Windows Media Player encontra um marcador no clipe.                |
| [MediaChange](player-player-mediachange.md)                                                     | Ocorre quando um item de mídia muda.                                                |
| [MediaCollectionAttributeStringAdded](player-player-mediacollectionattributestringadded.md)     | Ocorre quando um valor de atributo é adicionado à biblioteca.                          |
| [MediaCollectionAttributeStringChanged](player-player-mediacollectionattributestringchanged.md) | Ocorre quando um valor de atributo na biblioteca é alterado.                        |
| [MediaCollectionAttributeStringRemoved](player-player-mediacollectionattributestringremoved.md) | Ocorre quando um valor de atributo é removido da biblioteca.                      |
| [MediaCollectionChange](player-player-mediacollectionchange.md)                                 | Ocorre quando o **objeto MediaCollection** muda.                              |
| [MediaError](player-player-mediaerror.md)                                                       | Ocorre quando o objeto **Media** tem uma condição de erro.                         |
| [ModeChange](player-player-modechange.md)                                                       | Ocorre ao alternar entre o modo de embaralhamento e o modo normal.                           |
| [OpenPlaylistSwitch](player-player-openplaylistswitch.md)                                       | Ocorre quando um título em um DVD começa a ser gravado.                                     |
| [OpenStateChange](player-player-openstatechange.md)                                             | Ocorre quando o *player*. **alterações de openState.**                                      |
| [PlaylistChange](player-player-playlistchange.md)                                               | Ocorre quando uma lista de reprodução é mudada.                                                  |
| [PlaylistCollectionChange](player-player-playlistcollectionchange.md)                           | Ocorre quando algo muda na coleção de playlists.                        |
| [PlaylistCollectionPlaylistAdded](player-player-playlistcollectionplaylistadded.md)             | Ocorre quando uma playlist é adicionada à coleção de playlists.                      |
| [PlaylistCollectionPlaylistRemoved](player-player-playlistcollectionplaylistremoved.md)         | Ocorre quando uma playlist é removida da coleção de playlists.                  |
| [PlayStateChange](player-player-playstatechange.md)                                             | Ocorre quando o *player*. **alterações de playState.**                                      |
| [PositionChange](player-player-positionchange.md)                                               | Ocorre quando o *player*. *controla*. **alterações currentPosition.**                     |
| [ScriptCommand](player-player-scriptcommand.md)                                                 | Ocorre quando Windows Media Player encontra um comando de script inserido em um arquivo. |
| [StatusChange](player-player-statuschange.md)                                                   | Ocorre quando a propriedade **de status** altera o valor.                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**Referência de programação de capa**](skin-programming-reference.md)
</dt> </dl>

 

 





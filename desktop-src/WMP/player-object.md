---
title: Objeto de jogador
description: O objeto Player é o objeto raiz do controle do Windows Media Player. Ele dá suporte às propriedades, métodos e eventos listados nas tabelas a seguir.
ms.assetid: 694bd6cc-c816-478a-87b9-1526e2d18869
keywords:
- Objeto do Player Windows Media Player
topic_type:
- apiref
api_name:
- Player Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0bdf6443557477c15497a36d4976b13d0cfea2fc
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2019
ms.locfileid: "104498913"
---
# <a name="player-object"></a>Objeto de jogador

O objeto Player é o objeto raiz do controle do Windows Media Player. Ele dá suporte às propriedades, métodos e eventos listados nas tabelas a seguir.

O objeto Player dá suporte às propriedades a seguir. As propriedades marcadas com um asterisco ( \* ) não estão acessíveis a capas.



| Propriedade                                             | Descrição                                                                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [cdromCollection](player-cdromcollection.md)        | Recupera o objeto [cdromCollection](cdromcollection-object.md) .                                                                          |
| [closedCaption](player-closedcaption.md)            | Recupera o objeto [ClosedCaption](closedcaption-object.md) .                                                                              |
| [controles](player-controls.md)                      | Recupera o objeto [Controls](controls-object.md) .                                                                                        |
| [currentMedia](player-currentmedia.md)              | Especifica ou recupera o objeto de [mídia](media-object.md) atual.                                                                         |
| [currentPlaylist](player-currentplaylist.md)        | Especifica ou recupera o objeto de [playlist](playlist-object.md) atual.                                                                   |
| [DVD](player-dvd.md)                                | Recupera o objeto de [DVD](dvd-object.md) .                                                                                                  |
| [enableContextMenu](player-enablecontextmenu.md)\* | Especifica ou recupera um valor que indica se o menu de contexto deve ser habilitado, que aparece quando o botão direito do mouse é clicado.          |
| [habilitado](player-enabled.md)\*                     | Especifica ou recupera um valor que indica se o controle do Windows Media Player está habilitado.                                               |
| [error](player-error.md)                            | Recupera o objeto de [erro](error-object.md) .                                                                                              |
| [tela inteira](player-fullscreen.md)\*               | Especifica ou recupera um valor que indica se o conteúdo do vídeo é reproduzido no modo de tela inteira.                                          |
| [IsOnline](player-isonline.md)                      | Recupera um valor que indica se o usuário está conectado a uma rede.                                                                     |
| [IsRemote](player-isremote.md)\*                   | Recupera um valor que indica se o controle do Windows Media Player está sendo executado no modo remoto.                                             |
| [mediacollection](player-mediacollection.md)        | Recupera o objeto [mediacollection](mediacollection-object.md) .                                                                          |
| [rede](player-network.md)                        | Recupera o objeto de [rede](network-object.md) .                                                                                          |
| [openState](player-openstate.md)                    | Recupera um valor que indica o estado da fonte de conteúdo.                                                                                |
| [playerApplication](player-playerapplication.md)\* | Recupera o objeto [PlayerApplication](playerapplication-object.md) quando um controle remoto do Windows Media Player está em execução.               |
| [playlistcollection](player-playlistcollection.md)  | Recupera o objeto [playlistcollection](playlistcollection-object.md) .                                                                    |
| [playState](player-playstate.md)                    | Recupera um valor que indica o estado da operação do Windows Media Player.                                                                |
| [configurações](player-settings.md)                      | Recupera o objeto de [configurações](settings-object.md) .                                                                                        |
| [status](player-status.md)                          | Recupera um valor que indica o status atual do Windows Media Player.                                                                     |
| [stretchToFit](player-stretchtofit.md)\*           | Especifica ou recupera um valor que indica se o vídeo será alongado para ajustar o tamanho da exibição de vídeo do controle do Windows Media Player.          |
| [UIMODE](player-uimode.md)\*                       | Especifica ou recupera um valor que indica quais controles são mostrados na interface do usuário quando o Windows Media Player é inserido em uma página da Web. |
| [URL](player-url.md)                                | Especifica ou recupera o nome do clipe a ser reproduzido.                                                                                         |
| [versionInfo](player-versioninfo.md)                | Recupera um valor de cadeia de caracteres que especifica a versão do Windows Media Player.                                                                 |
| [windowlessVideo](player-windowlessvideo.md)\*     | Especifica ou recupera um valor que indica se o controle do Windows Media Player renderiza o vídeo no modo sem janela.                         |



 

\* Não acessível para capas.

O objeto Player dá suporte aos seguintes métodos.



| Método                                | Descrição                                               |
|---------------------------------------|-----------------------------------------------------------|
| [close](player-close.md)             | Libera recursos do Windows Media Player.                  |
| [launchURL](player-launchurl.md)     | Envia uma URL para o navegador padrão do usuário a ser renderizado. |
| [newMedia](player-newmedia.md)       | Cria um novo objeto de [mídia](media-object.md) .           |
| [newPlaylist](player-newplaylist.md) | Cria um novo objeto de [lista de reprodução](playlist-object.md) .     |
| [openPlayer](player-openplayer.md)   | Abre o Windows Media Player usando a URL especificada.       |



 

O objeto Player dá suporte aos seguintes eventos. Eventos marcados com um asterisco ( \* ) não podem ser acessados por capas. Para obter informações sobre como manipular eventos de mouse e de teclado em capas, consulte [eventos externos](external-events.md).



| Evento                                                                                            | Descrição                                                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [AudioLanguageChange](player-player-audiolanguagechange.md)                                     | Ocorre quando o idioma de áudio atual é alterado.                                  |
| [de resposta](player-player-buffering.md)                                                         | Ocorre quando o controle do Windows Media Player começa ou termina o armazenamento em buffer.           |
| [CdromMediaChange](player-player-cdrommediachange.md)                                           | Ocorre quando um CD ou DVD é inserido ou ejetado de uma unidade de CD ou DVD.      |
| [Clicar](player-player-click.md) \*                                                              | Ocorre quando o usuário clica em um botão do mouse.                                      |
| [CurrentItemChange](player-player-currentitemchange.md)                                         | Ocorre quando os *controles*. **currentItem** é alterado.                                  |
| [CurrentMediaItemAvailable](player-player-currentmediaitemavailable.md)                         | Ocorre quando um item de metadados gráfico no item de mídia atual fica disponível. |
| [CurrentPlaylistChange](player-player-currentplaylistchange.md)                                 | Ocorre quando algo é alterado na playlist atual.                       |
| [CurrentPlaylistItemAvailable](player-player-currentplaylistitemavailable.md)                   | Ocorre quando o item da playlist atual se torna disponível.                         |
| **Desconectar**                                                                                   | Reservado para uso futuro.                                                         |
| [DomainChange](player-player-domainchange.md)                                                   | Ocorre quando o domínio do DVD é alterado.                                              |
| [DoubleClick](player-player-doubleclick.md)\*                                                  | Ocorre quando o usuário clica duas vezes com um botão do mouse.                               |
| **DurationUnitChange**                                                                           | Reservado para uso futuro.                                                         |
| **EndOfStream**                                                                                  | Reservado para uso futuro.                                                         |
| [Erro](player-player-error.md)                                                                 | Ocorre quando o controle do Windows Media Player tem uma condição de erro.             |
| [KeyDown](player-player-keydown.md) \*                                                          | Ocorre quando uma tecla é pressionada.                                                    |
| [KeyPress](player-player-keypress.md)\*                                                        | Ocorre quando uma tecla é pressionada e liberada.                                  |
| [KeyUp](player-player-keyup.md) \*                                                              | Ocorre quando uma tecla é liberada.                                                   |
| [MarkerHit](player-player-markerhit.md)                                                         | Ocorre quando um marcador é atingido.                                                 |
| [MediaChange](player-player-mediachange.md)                                                     | Ocorre quando um item de mídia é alterado.                                                |
| [MediaCollectionAttributeStringAdded](player-player-mediacollectionattributestringadded.md)     | Ocorre quando um valor de atributo é adicionado à biblioteca.                          |
| [MediaCollectionAttributeStringChanged](player-player-mediacollectionattributestringchanged.md) | Ocorre quando um valor de atributo na biblioteca é alterado.                        |
| [MediaCollectionAttributeStringRemoved](player-player-mediacollectionattributestringremoved.md) | Ocorre quando um valor de atributo é removido da biblioteca.                      |
| [MediaCollectionChange](player-player-mediacollectionchange.md)                                 | Ocorre quando a coleção de mídia é alterada.                                        |
| [MediaCollectionMediaAdded](player-player-mediacollectionmediaadded.md)                         | Ocorre quando um item de mídia é adicionado à biblioteca local.                          |
| [MediaCollectionMediaRemoved](player-player-mediacollectionmediaremoved.md)                     | Ocorre quando um item de mídia é removido da biblioteca local.                      |
| [MediaError](player-player-mediaerror.md)                                                       | Ocorre quando o objeto de **mídia** tem uma condição de erro.                         |
| [ModeChange](player-player-modechange.md)                                                       | Ocorre quando um modo do Windows Media Player é alterado.                           |
| [MouseDown](player-player-mousedown.md)\*                                                      | Ocorre quando um botão do mouse é pressionado.                                           |
| [MouseMove](player-player-mousemove.md)\*                                                      | Ocorre quando o ponteiro do mouse é movido.                                          |
| [MouseUp](player-player-mouseup.md)\*                                                          | Ocorre quando um botão do mouse é liberado.                                          |
| **NewStream**                                                                                    | Reservado para uso futuro.                                                         |
| [OpenPlaylistSwitch](player-player-openplaylistswitch.md)                                       | Ocorre quando um título em um DVD começa a ser reproduzido.                                     |
| [OpenStateChange](player-player-openstatechange.md)                                             | Ocorre quando o controle do Windows Media Player muda de estado.                      |
| [PlaylistChange](player-player-playlistchange.md)                                               | Ocorre quando uma playlist é alterada.                                                  |
| [PlaylistCollectionChange](player-player-playlistcollectionchange.md)                           | Ocorre quando algo é alterado na coleção de playlist.                        |
| [PlaylistCollectionPlaylistAdded](player-player-playlistcollectionplaylistadded.md)             | Ocorre quando uma playlist é adicionada à coleção de playlist.                      |
| [PlaylistCollectionPlaylistRemoved](player-player-playlistcollectionplaylistremoved.md)         | Ocorre quando uma playlist é removida da coleção de playlist.                  |
| **PlaylistCollectionPlaylistSetAsDeleted**                                                       | Reservado para uso futuro.                                                         |
| [PlayStateChange](player-player-playstatechange.md)                                             | Ocorre quando o estado de reprodução do controle do Windows Media Player é alterado.          |
| [PositionChange](player-player-positionchange.md)                                               | Ocorre quando a posição atual do item de mídia é alterada.             |
| [ScriptCommand](player-player-scriptcommand.md)                                                 | Ocorre quando um comando ou uma URL sincronizada é recebida.                           |
| [StatusChange](player-player-statuschange.md)                                                   | Ocorre quando o valor da propriedade **status** é alterado.                               |
| [StringCollectionChange](player-player-stringcollectionchange.md)                               | Ocorre quando uma coleção de cadeia de caracteres é alterada.                                         |
| **Aviso**                                                                                      | Reservado para uso futuro.                                                         |



 

\* Não acessível para capas. Para obter informações sobre como manipular eventos de mouse e de teclado em capas, consulte [manipuladores de eventos de ambiente](ambient-event-handlers.md).

Quando inserido em uma página da Web, o objeto **Player** pode ser acessado usando o valor de ID especificado na marca Object. Em um arquivo de definição de capa, ele é acessado usando o atributo global do **Player** . Para fins de ilustração, o **Player** será usado como a ID de objeto nas seções de sintaxe de referência.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de modelo de objeto para scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 





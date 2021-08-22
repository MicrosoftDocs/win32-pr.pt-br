---
title: Objeto Player
description: O objeto Player é o objeto raiz para o Windows Media Player controle. Ele dá suporte às propriedades, métodos e eventos listados nas tabelas a seguir.
ms.assetid: 694bd6cc-c816-478a-87b9-1526e2d18869
keywords:
- Player Object Windows Media Player
topic_type:
- apiref
api_name:
- Player Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ee314862aad1237036d5a7fa6a5627f42a6185d1ab6914f1e11ec19a831b755
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119616696"
---
# <a name="player-object"></a>Objeto Player

O objeto Player é o objeto raiz para o Windows Media Player controle. Ele dá suporte às propriedades, métodos e eventos listados nas tabelas a seguir.

O objeto Player dá suporte às propriedades a seguir. Propriedades marcadas com um asterisco ( \* ) não são acessíveis a capas.



| Propriedade                                             | Descrição                                                                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [cdromCollection](player-cdromcollection.md)        | Recupera o [objeto CdromCollection.](cdromcollection-object.md)                                                                          |
| [closedCaption](player-closedcaption.md)            | Recupera o [objeto ClosedCaption.](closedcaption-object.md)                                                                              |
| [Controles](player-controls.md)                      | Recupera o [objeto Controls.](controls-object.md)                                                                                        |
| [currentMedia](player-currentmedia.md)              | Especifica ou recupera o objeto [media](media-object.md) atual.                                                                         |
| [currentPlaylist](player-currentplaylist.md)        | Especifica ou recupera o objeto [playlist](playlist-object.md) atual.                                                                   |
| [Dvd](player-dvd.md)                                | Recupera o objeto [DVD.](dvd-object.md)                                                                                                  |
| [enableContextMenu](player-enablecontextmenu.md)\* | Especifica ou recupera um valor que indica se o menu de contexto deve ser habilitado, que aparece quando o botão direito do mouse é clicado.          |
| [habilitado](player-enabled.md)\*                     | Especifica ou recupera um valor que indica se o controle Windows Media Player está habilitado.                                               |
| [error](player-error.md)                            | Recupera o [objeto Error.](error-object.md)                                                                                              |
| [fullScreen](player-fullscreen.md)\*               | Especifica ou recupera um valor que indica se o conteúdo do vídeo é exibido novamente no modo de tela inteira.                                          |
| [Isonline](player-isonline.md)                      | Recupera um valor que indica se o usuário está conectado a uma rede.                                                                     |
| [isRemote](player-isremote.md)\*                   | Recupera um valor que indica se o controle Windows Media Player está em execução no modo remoto.                                             |
| [mediaCollection](player-mediacollection.md)        | Recupera o [objeto MediaCollection.](mediacollection-object.md)                                                                          |
| [network](player-network.md)                        | Recupera o [objeto Network.](network-object.md)                                                                                          |
| [openState](player-openstate.md)                    | Recupera um valor que indica o estado da fonte de conteúdo.                                                                                |
| [playerApplication](player-playerapplication.md)\* | Recupera o [objeto PlayerApplication](playerapplication-object.md) quando um controle Windows Media Player remoto está em execução.               |
| [playlistCollection](player-playlistcollection.md)  | Recupera o [objeto PlaylistCollection.](playlistcollection-object.md)                                                                    |
| [playState](player-playstate.md)                    | Recupera um valor que indica o estado da operação Windows Media Player dados.                                                                |
| [configurações](player-settings.md)                      | Recupera o [objeto Configurações](settings-object.md) objeto .                                                                                        |
| [status](player-status.md)                          | Recupera um valor que indica o status atual do Windows Media Player.                                                                     |
| [stretchToFit](player-stretchtofit.md)\*           | Especifica ou recupera um valor que indica se o vídeo será estendido para se ajustar ao tamanho da exibição Windows Media Player vídeo de controle.          |
| [uiMode](player-uimode.md)\*                       | Especifica ou recupera um valor que indica quais controles são mostrados na interface do usuário quando Windows Media Player é inserido em uma página da Web. |
| [URL](player-url.md)                                | Especifica ou recupera o nome do clipe a ser reproduzir.                                                                                         |
| [Versioninfo](player-versioninfo.md)                | Recupera um valor string que especifica a versão do Windows Media Player.                                                                 |
| [windowlessVideo](player-windowlessvideo.md)\*     | Especifica ou recupera um valor que indica se o controle Windows Media Player renderiza o vídeo no modo sem janela.                         |



 

\* Não acessível a capas.

O objeto Player dá suporte aos métodos a seguir.



| Método                                | Descrição                                               |
|---------------------------------------|-----------------------------------------------------------|
| [close](player-close.md)             | Versões Windows Media Player recursos.                  |
| [launchURL](player-launchurl.md)     | Envia uma URL para o navegador padrão do usuário a ser renderizado. |
| [newMedia](player-newmedia.md)       | Cria um novo [objeto Media.](media-object.md)           |
| [newPlaylist](player-newplaylist.md) | Cria um novo [objeto Playlist.](playlist-object.md)     |
| [openPlayer](player-openplayer.md)   | Abre Windows Media Player usando a URL especificada.       |



 

O objeto Player dá suporte aos seguintes eventos. Eventos marcados com um asterisco ( \* ) não são acessíveis a capas. Para obter informações sobre como lidar com eventos de mouse e teclado em capas, consulte [Eventos externos.](external-events.md)



| Evento                                                                                            | Descrição                                                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [AudioLanguageChange](player-player-audiolanguagechange.md)                                     | Ocorre quando a linguagem de áudio atual é muda.                                  |
| [de resposta](player-player-buffering.md)                                                         | Ocorre quando o controle Windows Media Player inicia ou termina o buffer.           |
| [CdromMediaChange](player-player-cdrommediachange.md)                                           | Ocorre quando um CD ou DVD é inserido ou ejetado de uma unidade de CD ou DVD.      |
| [Clicar](player-player-click.md) \*                                                              | Ocorre quando o usuário clica em um botão do mouse.                                      |
| [CurrentItemChange](player-player-currentitemchange.md)                                         | Ocorre quando *controla*. **alterações currentItem.**                                  |
| [CurrentMediaItemAvailable](player-player-currentmediaitemavailable.md)                         | Ocorre quando um item de metadados gráficos no item de mídia atual fica disponível. |
| [CurrentPlaylistChange](player-player-currentplaylistchange.md)                                 | Ocorre quando algo muda na playlist atual.                       |
| [CurrentPlaylistItemAvailable](player-player-currentplaylistitemavailable.md)                   | Ocorre quando o item de playlist atual fica disponível.                         |
| **Desconectar**                                                                                   | Reservado para uso futuro.                                                         |
| [DomainChange](player-player-domainchange.md)                                                   | Ocorre quando o domínio de DVD muda.                                              |
| [DoubleClick](player-player-doubleclick.md)\*                                                  | Ocorre quando o usuário clica duas vezes em um botão do mouse.                               |
| **DurationUnitChange**                                                                           | Reservado para uso futuro.                                                         |
| **Endofstream**                                                                                  | Reservado para uso futuro.                                                         |
| [Erro](player-player-error.md)                                                                 | Ocorre quando o controle Windows Media Player tem uma condição de erro.             |
| [KeyDown](player-player-keydown.md) \*                                                          | Ocorre quando uma tecla é pressionada.                                                    |
| [KeyPress](player-player-keypress.md)\*                                                        | Ocorre quando uma tecla é pressionada e liberada.                                  |
| [KeyUp](player-player-keyup.md) \*                                                              | Ocorre quando uma tecla é liberada.                                                   |
| [MarkerHit](player-player-markerhit.md)                                                         | Ocorre quando um marcador é atingido.                                                 |
| [MediaChange](player-player-mediachange.md)                                                     | Ocorre quando um item de mídia muda.                                                |
| [MediaCollectionAttributeStringAdded](player-player-mediacollectionattributestringadded.md)     | Ocorre quando um valor de atributo é adicionado à biblioteca.                          |
| [MediaCollectionAttributeStringChanged](player-player-mediacollectionattributestringchanged.md) | Ocorre quando um valor de atributo na biblioteca é alterado.                        |
| [MediaCollectionAttributeStringRemoved](player-player-mediacollectionattributestringremoved.md) | Ocorre quando um valor de atributo é removido da biblioteca.                      |
| [MediaCollectionChange](player-player-mediacollectionchange.md)                                 | Ocorre quando a coleção de mídias é mudada.                                        |
| [MediaCollectionMediaAdded](player-player-mediacollectionmediaadded.md)                         | Ocorre quando um item de mídia é adicionado à biblioteca local.                          |
| [MediaCollectionMediaRemoved](player-player-mediacollectionmediaremoved.md)                     | Ocorre quando um item de mídia é removido da biblioteca local.                      |
| [MediaError](player-player-mediaerror.md)                                                       | Ocorre quando o objeto **Media** tem uma condição de erro.                         |
| [ModeChange](player-player-modechange.md)                                                       | Ocorre quando um modo de Windows Media Player é alterado.                           |
| [MouseDown](player-player-mousedown.md)\*                                                      | Ocorre quando um botão do mouse é pressionado.                                           |
| [MouseMove](player-player-mousemove.md)\*                                                      | Ocorre quando o ponteiro do mouse é movido.                                          |
| [MouseUp](player-player-mouseup.md)\*                                                          | Ocorre quando um botão do mouse é liberado.                                          |
| **NewStream**                                                                                    | Reservado para uso futuro.                                                         |
| [OpenPlaylistSwitch](player-player-openplaylistswitch.md)                                       | Ocorre quando um título em um DVD começa a ser gravado.                                     |
| [OpenStateChange](player-player-openstatechange.md)                                             | Ocorre quando o controle Windows Media Player altera o estado.                      |
| [PlaylistChange](player-player-playlistchange.md)                                               | Ocorre quando uma lista de reprodução é mudada.                                                  |
| [PlaylistCollectionChange](player-player-playlistcollectionchange.md)                           | Ocorre quando algo muda na coleção de playlists.                        |
| [PlaylistCollectionPlaylistAdded](player-player-playlistcollectionplaylistadded.md)             | Ocorre quando uma playlist é adicionada à coleção de playlists.                      |
| [PlaylistCollectionPlaylistRemoved](player-player-playlistcollectionplaylistremoved.md)         | Ocorre quando uma playlist é removida da coleção de playlists.                  |
| **PlaylistCollectionPlaylistSetAsDeleted**                                                       | Reservado para uso futuro.                                                         |
| [PlayStateChange](player-player-playstatechange.md)                                             | Ocorre quando o estado de reprodução do controle Windows Media Player muda.          |
| [PositionChange](player-player-positionchange.md)                                               | Ocorre quando a posição atual do item de mídia foi alterada.             |
| [ScriptCommand](player-player-scriptcommand.md)                                                 | Ocorre quando um comando ou URL sincronizado é recebido.                           |
| [StatusChange](player-player-statuschange.md)                                                   | Ocorre quando a propriedade **de status** altera o valor.                               |
| [StringCollectionChange](player-player-stringcollectionchange.md)                               | Ocorre quando uma coleção de cadeias de caracteres é mudada.                                         |
| **Aviso**                                                                                      | Reservado para uso futuro.                                                         |



 

\* Não acessível a capas. Para obter informações sobre como manipular eventos de mouse e teclado em capas, consulte [Manipuladores de eventos de ambiente](ambient-event-handlers.md).

Quando inserido em uma página da Web, o **objeto Player** pode ser acessado usando o valor de ID especificado na marca OBJECT. Em um arquivo de definição de capa, ele é acessado usando o **atributo** global player. Para fins de ilustração, **o player** será usado como a ID do objeto nas seções de sintaxe de referência.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de modelo de objeto para scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 





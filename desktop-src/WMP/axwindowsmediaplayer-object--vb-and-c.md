---
title: Objeto AxWindowsMediaPlayer (VB e C)
description: Objeto AxWindowsMediaPlayer (VB e C \)
ms.assetid: d7eeac20-1afa-4e73-9af6-9772fbb65516
keywords:
- Windows Media Player, objeto AxWindowsMediaPlayer
- Windows Media Player Mobile, objeto AxWindowsMediaPlayer
- Modelo de objeto do Windows Media Player, objeto AxWindowsMediaPlayer
- modelo de objeto, objeto AxWindowsMediaPlayer
- Controle ActiveX, objeto AxWindowsMediaPlayer
- Controle ActiveX do Windows Media Player, objeto AxWindowsMediaPlayer
- Controle ActiveX móvel do Windows Media Player, objeto AxWindowsMediaPlayer
- referência do modelo de objeto, objeto AxWindowsMediaPlayer
- Objeto AxWindowsMediaPlayer
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 32f814560c8b6eb13dc5abb8736378432ec4565e
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2020
ms.locfileid: "104453890"
---
# <a name="axwindowsmediaplayer-object-vb-and-c"></a>Objeto AxWindowsMediaPlayer (VB e C#)

O objeto AxWindowsMediaPlayer é o objeto raiz do controle do Windows Media Player. Ele dá suporte às propriedades, métodos e eventos listados nas tabelas a seguir.

O objeto AxWindowsMediaPlayer dá suporte às propriedades a seguir.



| Propriedade                                                                             | Descrição                                                                                                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [cdromCollection](axwmplib-axwindowsmediaplayer-cdromcollection--vb-and-c.md)       | Obtém uma interface **IWMPCdromCollection** .                                                                                         |
| [closedCaption](axwmplib-axwindowsmediaplayer-closedcaption--vb-and-c.md)           | Obtém uma interface IWMPClosedCaption.                                                                                               |
| [Ctlcontrols](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md)               | Obtém uma interface IWMPControls.                                                                                                    |
| [Ctlenabled](axwmplib-axwindowsmediaplayer-ctlenabled--vb-and-c.md)                 | Obtém ou define um valor que indica se o controle do Windows Media Player está habilitado.                                               |
| [currentMedia](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)             | Obtém ou define a interface IWMPMedia que corresponde ao item de mídia atual.                                                   |
| [currentPlaylist](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)       | Obtém ou define a interface **IWMPPlaylist** atual.                                                                               |
| [DVD](axwmplib-axwindowsmediaplayer-dvd--vb-and-c.md)                               | Obtém uma interface IWMPDVD.                                                                                                         |
| [enableContextMenu](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md)   | Obtém ou define um valor que indica se o menu de contexto deve ser habilitado, que aparece quando o botão direito do mouse é clicado.          |
| [Erro](axwmplib-axwindowsmediaplayer-error--vb-and-c.md)                           | Obtém uma interface IWMPError.                                                                                                       |
| [Tela inteira](axwmplib-axwindowsmediaplayer-fullscreen--vb-and-c.md)                 | Obtém ou define um valor que indica se o conteúdo do vídeo é reproduzido no modo de tela inteira.                                          |
| [IsOnline](axwmplib-axwindowsmediaplayer-isonline--vb-and-c.md)                     | Obtém um valor que indica se o usuário está conectado a uma rede.                                                                |
| IsRemote                                                                             | Sem suporte para programação .NET.                                                                                                |
| [mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)       | Obtém uma interface IWMPMediaCollection.                                                                                             |
| [rede](axwmplib-axwindowsmediaplayer-network--vb-and-c.md)                       | Obtém uma interface IWMPNetwork.                                                                                                     |
| [openState](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)                   | Obtém um valor que indica o estado da fonte de conteúdo.                                                                           |
| playerApplication                                                                    | Sem suporte para programação .NET.                                                                                                |
| [playlistcollection](axwmplib-axwindowsmediaplayer-playlistcollection--vb-and-c.md) | Obtém uma interface IWMPPlaylistCollection.                                                                                          |
| [playState](axwmplib-axwindowsmediaplayer-playstate--vb-and-c.md)                   | Obtém um valor que indica o estado da operação do Windows Media Player.                                                           |
| [configurações](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md)                     | Obtém uma interface IWMPSettings.                                                                                                    |
| [status](axwmplib-axwindowsmediaplayer-status--vb-and-c.md)                         | Obtém um valor que indica o status atual do Windows Media Player.                                                                |
| [stretchToFit](axwmplib-axwindowsmediaplayer-stretchtofit--vb-and-c.md)             | Obtém ou define um valor que indica se o vídeo será alongado para ajustar o tamanho da exibição de vídeo do controle do Windows Media Player.          |
| [uiMode](axwmplib-axwindowsmediaplayer-uimode--vb-and-c.md)                         | Obtém ou define um valor que indica quais controles são mostrados na interface do usuário quando o Windows Media Player é inserido em uma página da Web. |
| [URL](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)                               | Obtém ou define o nome do clipe a ser reproduzido.                                                                                         |
| [versionInfo](axwmplib-axwindowsmediaplayer-versioninfo--vb-and-c.md)               | Obtém um valor que especifica a versão do Windows Media Player.                                                               |
| [windowlessVideo](axwmplib-axwindowsmediaplayer-windowlessvideo--vb-and-c.md)       | Obtém ou define um valor que indica se o controle do Windows Media Player renderiza o vídeo no modo sem janela.                         |



 

O objeto AxWindowsMediaPlayer dá suporte aos métodos a seguir.



| Método                                                       | Descrição                                               |
|--------------------------------------------------------------|-----------------------------------------------------------|
| [close](axwmplib-axwindowsmediaplayer-close.md)             | Libera recursos do Windows Media Player.                  |
| [launchURL](axwmplib-axwindowsmediaplayer-launchurl.md)     | Envia uma URL para o navegador padrão do usuário a ser renderizado. |
| [newMedia](axwmplib-axwindowsmediaplayer-newmedia.md)       | Retorna uma interface IWMPMedia para um novo item de mídia.      |
| [newPlaylist](axwmplib-axwindowsmediaplayer-newplaylist.md) | Retorna uma interface IWMPPlaylist para uma nova lista de reprodução.     |
| [openPlayer](axwmplib-axwindowsmediaplayer-openplayer.md)   | Abre o Windows Media Player usando a URL especificada.       |



 

O objeto AxWindowsMediaPlayer dá suporte aos seguintes eventos.



| Evento                                                                                                              | Descrição                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [AudioLanguageChange](axwmplib-axwindowsmediaplayer-audiolanguagechange.md)                                       | Ocorre quando o idioma de áudio atual é alterado.                                                            |
| [de resposta](axwmplib-axwindowsmediaplayer-buffering.md)                                                           | Ocorre quando o controle do Windows Media Player começa ou termina o armazenamento em buffer.                                     |
| [CdromBurnError](axwmplib-axwindowsmediaplayer-cdromburnerror.md)                                                 | Ocorre quando um erro genérico ocorre durante uma operação de gravação de CD.                                         |
| [CdromBurnMediaError](axwmplib-axwindowsmediaplayer-cdromburnmediaerror.md)                                       | Ocorre quando um erro ocorre durante a gravação de um item de mídia individual em um CD.                               |
| [CdromBurnStateChange](axwmplib-axwindowsmediaplayer-cdromburnstatechange.md)                                     | Ocorre quando uma operação de gravação de CD muda de estado.                                                          |
| [CdromMediaChange](axwmplib-axwindowsmediaplayer-cdrommediachange.md)                                             | Ocorre quando um CD ou DVD é inserido ou ejetado de uma unidade de CD ou DVD.                                |
| [CdromRipMediaError](axwmplib-axwindowsmediaplayer-cdromripmediaerror.md)                                         | Ocorre quando um erro ocorre ao copiar uma faixa individual de um CD.                                  |
| [CdromRipStateChange](axwmplib-axwindowsmediaplayer-cdromripstatechange.md)                                       | Ocorre quando uma operação de cópia de CD muda de estado.                                                          |
| [Clicar](axwmplib-axwindowsmediaplayer-click.md)                                                                   | Ocorre quando o usuário clica em um botão do mouse.                                                                |
| CreatePartnershipComplete                                                                                          | Sem suporte para programação .NET.                                                                        |
| [CurrentItemChange](axwmplib-axwindowsmediaplayer-currentitemchange.md)                                           | Ocorre quando [IWMPControls. currentItem](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md) é alterado. |
| [CurrentMediaItemAvailable](axwmplib-axwindowsmediaplayer-currentmediaitemavailable.md)                           | Ocorre quando um item de metadados gráfico no item de mídia atual fica disponível.                           |
| [CurrentPlaylistChange](axwmplib-axwindowsmediaplayer-currentplaylistchange.md)                                   | Ocorre quando algo é alterado na playlist atual.                                                 |
| [CurrentPlaylistItemAvailable](axwmplib-axwindowsmediaplayer-currentplaylistitemavailable.md)                     | Ocorre quando o item da playlist atual se torna disponível.                                                   |
| DeviceConnect                                                                                                      | Sem suporte para programação .NET.                                                                        |
| DeviceDisconnect                                                                                                   | Sem suporte para programação .NET.                                                                        |
| DeviceStatusChange                                                                                                 | Sem suporte para programação .NET.                                                                        |
| DeviceSyncError                                                                                                    | Sem suporte para programação .NET.                                                                        |
| DeviceSyncStateChange                                                                                              | Sem suporte para programação .NET.                                                                        |
| [Desconectar](axwmplib-axwindowsmediaplayer-disconnect.md)                                                         | Reservado para uso futuro.                                                                                   |
| [DomainChange](axwmplib-axwindowsmediaplayer-domainchange.md)                                                     | Ocorre quando o domínio do DVD é alterado.                                                                        |
| [Duplo](axwmplib-axwindowsmediaplayer-doubleclick.md)                                                       | Ocorre quando o usuário clica duas vezes com um botão do mouse.                                                         |
| [DurationUnitChange](axwmplib-axwindowsmediaplayer-durationunitchange.md)                                         | Reservado para uso futuro.                                                                                   |
| [EndOfStream](axwmplib-axwindowsmediaplayer-endofstream.md)                                                       | Reservado para uso futuro.                                                                                   |
| [Erro](axwmplib-axwindowsmediaplayer-error.md)                                                                   | Ocorre quando o controle do Windows Media Player tem uma condição de erro.                                       |
| [FolderScanStateChange](axwmplib-axwindowsmediaplayer-folderscanstatechange.md)                                   | Ocorre quando uma operação de monitoramento de pasta altera o estado.                                                   |
| [KeyDown](axwmplib-axwindowsmediaplayer-keydown.md)                                                               | Ocorre quando uma tecla é pressionada.                                                                              |
| [Pressionar](axwmplib-axwindowsmediaplayer-keypress.md)                                                             | Ocorre quando uma tecla é pressionada e liberada.                                                            |
| [KeyUp](axwmplib-axwindowsmediaplayer-keyup.md)                                                                   | Ocorre quando uma tecla é liberada.                                                                             |
| [LibraryConnect](axwmplib-axwindowsmediaplayer-libraryconnect.md)                                                 | Ocorre quando uma biblioteca fica disponível.                                                                   |
| [LibraryDisconnect](axwmplib-axwindowsmediaplayer-librarydisconnect.md)                                           | Ocorre quando uma biblioteca não está mais disponível.                                                              |
| [MarkerHit](axwmplib-axwindowsmediaplayer-markerhit.md)                                                           | Ocorre quando um marcador é atingido.                                                                           |
| [MediaChange](axwmplib-axwindowsmediaplayer-mediachange.md)                                                       | Ocorre quando um item de mídia é alterado.                                                                          |
| [MediaCollectionAttributeStringAdded](axwmplib-axwindowsmediaplayer-mediacollectionattributestringadded.md)       | Ocorre quando um valor de atributo é adicionado à biblioteca.                                                    |
| [MediaCollectionAttributeStringChanged](axwmplib-axwindowsmediaplayer-mediacollectionattributestringchanged.md)   | Ocorre quando um valor de atributo na biblioteca é alterado.                                                  |
| [MediaCollectionAttributeStringRemoved](axwmplib-axwindowsmediaplayer-mediacollectionattributestringremoved.md)   | Ocorre quando um valor de atributo é removido da biblioteca.                                                |
| [MediaCollectionChange](axwmplib-axwindowsmediaplayer-mediacollectionchange.md)                                   | Ocorre quando a coleção de mídia é alterada.                                                                  |
| [MediaCollectionMediaAdded](axwmplib-axwindowsmediaplayer-mediacollectionmediaadded.md)                           | Ocorre quando um item de mídia é adicionado à biblioteca local.                                                    |
| [MediaCollectionMediaRemoved](axwmplib-axwindowsmediaplayer-mediacollectionmediaremoved.md)                       | Ocorre quando um item de mídia é removido da biblioteca local.                                                |
| [MediaError](axwmplib-axwindowsmediaplayer-mediaerror.md)                                                         | Ocorre quando o objeto de **mídia** tem uma condição de erro.                                                   |
| [ModeChange](axwmplib-axwindowsmediaplayer-modechange.md)                                                         | Ocorre quando um modo do Windows Media Player é alterado.                                                     |
| [MouseDown](axwmplib-axwindowsmediaplayer-mousedown.md)                                                           | Ocorre quando um botão do mouse é pressionado.                                                                     |
| [Ocorra](axwmplib-axwindowsmediaplayer-mousemove.md)                                                           | Ocorre quando o ponteiro do mouse é movido.                                                                    |
| [MouseUp](axwmplib-axwindowsmediaplayer-mouseup.md)                                                               | Ocorre quando um botão do mouse é liberado.                                                                    |
| [NewStream](axwmplib-axwindowsmediaplayer-newstream.md)                                                           | Reservado para uso futuro.                                                                                   |
| [OpenPlaylistSwitch](axwmplib-axwindowsmediaplayer-openplaylistswitch.md)                                         | Ocorre quando um título em um DVD começa a ser reproduzido.                                                               |
| [OpenStateChange](axwmplib-axwindowsmediaplayer-openstatechange.md)                                               | Ocorre quando o controle do Windows Media Player muda de estado.                                                |
| PlayerDockedStateChange                                                                                            | Sem suporte para programação .NET.                                                                        |
| PlayerReconnect                                                                                                    | Sem suporte para programação .NET.                                                                        |
| [PlaylistChange](axwmplib-axwindowsmediaplayer-playlistchange.md)                                                 | Ocorre quando uma playlist é alterada.                                                                            |
| [PlaylistCollectionChange](axwmplib-axwindowsmediaplayer-playlistcollectionchange.md)                             | Ocorre quando algo é alterado na coleção de playlist.                                                  |
| [PlaylistCollectionPlaylistAdded](axwmplib-axwindowsmediaplayer-playlistcollectionplaylistadded.md)               | Ocorre quando uma playlist é adicionada à coleção de playlist.                                                |
| [PlaylistCollectionPlaylistRemoved](axwmplib-axwindowsmediaplayer-playlistcollectionplaylistremoved.md)           | Ocorre quando uma playlist é removida da coleção de playlist.                                            |
| [PlaylistCollectionPlaylistSetAsDeleted](axwmplib-axwindowsmediaplayer-playlistcollectionplaylistsetasdeleted.md) | Reservado para uso futuro.                                                                                   |
| [PlayStateChange](axwmplib-axwindowsmediaplayer-playstatechange.md)                                               | Ocorre quando o estado de reprodução do controle do Windows Media Player é alterado.                                    |
| [PositionChange](axwmplib-axwindowsmediaplayer-positionchange.md)                                                 | Ocorre quando a posição atual do item de mídia é alterada.                                       |
| [ScriptCommand](axwmplib-axwindowsmediaplayer-scriptcommand.md)                                                   | Ocorre quando um comando ou uma URL sincronizada é recebida.                                                     |
| [StatusChange](axwmplib-axwindowsmediaplayer-statuschange.md)                                                     | Ocorre quando o valor da propriedade **status** é alterado.                                                         |
| [StringCollectionChange](axwmplib-axwindowsmediaplayer-stringcollectionchange.md)                                 | Ocorre quando uma coleção de cadeia de caracteres é alterada.                                                                   |
| SwitchedToControl                                                                                                  | Sem suporte para programação .NET.                                                                        |
| SwitchedToPlayerApplication                                                                                        | Sem suporte para programação .NET.                                                                        |
| [Aviso](axwmplib-axwindowsmediaplayer-warning.md)                                                               | Reservado para uso futuro.                                                                                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interfaces para Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interface IWMPCdromCollection (VB e C#)**](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[**Interface IWMPClosedCaption (VB e C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**Interface IWMPControls (VB e C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**Interface IWMPDVD (VB e C#)**](iwmpdvd--vb-and-c.md)
</dt> <dt>

[**Interface IWMPError (VB e C#)**](iwmperror--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMediaCollection (VB e C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**Interface IWMPNetwork (VB e C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylistCollection (VB e C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[**Interface IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**Referência de modelo de objeto para Visual Basic .NET e C #**](object-model-reference-for-visual-basic--net-and-c.md)
</dt> <dt>

[**WMPOpenState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpopenstate)
</dt> <dt>

[**WMPPlayState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpplaystate)
</dt> </dl>

 

 





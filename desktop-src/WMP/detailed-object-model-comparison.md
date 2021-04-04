---
title: Comparação de modelo de objeto detalhado
description: Comparação de modelo de objeto detalhado
ms.assetid: 8f08e2a6-1944-4814-b3b7-680a3722e1a0
keywords:
- Windows Media Player, modelo de objeto
- Modelo de objeto do Windows Media Player, diferenças de versão
- modelo de objeto, diferenças de versão
- Controle ActiveX do Windows Media Player, diferenças de versão
- Controle ActiveX, diferenças de versão
- Controle ActiveX móvel do Windows Media Player, diferenças de versão
- Windows Media Player Mobile, modelo de objeto
- Guia de migração, diferenças de versão
- versões do Windows Media Player, modelo de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 086607a9d367f42479e155e3273c30d88425a457
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104007057"
---
# <a name="detailed-object-model-comparison"></a>Comparação de modelo de objeto detalhado

A tabela a seguir compara as propriedades do modelo de objeto do Windows Media Player 6,4 com o modelo de objeto do Windows Media Player 7 ou posterior.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Propriedade do Windows Media Player 6,4</th>
<th>Windows Media Player 7 ou posterior equivalente</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>Player6</em>. <strong>AllowChangeDisplaySize</strong></td>
<td>A exibição do Windows Media Player 7 ou posterior é redimensionada automaticamente para se ajustar à mídia. Você pode definir as propriedades Height e Width na <OBJECT> marca ou no script.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>AllowScan</strong></td>
<td>De <em>controle</em>. <strong>Fastforward</strong> e <em>Controls</em>. <strong>fastReverse</strong> são automaticamente habilitados para tipos de arquivo que dão suporte a esses métodos.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>AnglesAvailable</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>AnimationAtStart</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>AudioStream</strong></td>
<td>Use <em>controles</em>. <strong>currentAudioLanguageIndex</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>AudioStreamsAvailable</strong></td>
<td>Use <em>controles</em>. <strong>audioLanguageCount</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Rebobinar</strong></td>
<td>Use <em>controles</em>. <strong>CurrentPosition</strong> no script para especificar ou recuperar a posição atual. Como alternativa, use marcadores e o <em>Player</em>. evento <strong>markerHit</strong> .</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Dimensionamento automático</strong></td>
<td>O dimensionamento automático é o comportamento padrão. Para substituir o dimensionamento automático, defina as propriedades de altura e largura na <OBJECT> marca ou no script.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Inicialização automática</strong></td>
<td>Use <em>as configurações</em>. <strong>inicialização automática</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Saldo</strong></td>
<td>Use <em>as configurações</em>. <strong>saldo</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Largura de banda</strong></td>
<td>Usar <em>rede</em>. <strong>largura de banda</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>BaseURL</strong></td>
<td>Use <em>as configurações</em>. <strong>baseURL</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>BufferingCount</strong></td>
<td>Usar <em>rede.</em> <strong>bufferingCount</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>BufferingProgress</strong></td>
<td>Usar <em>rede</em>. <strong>bufferingProgress</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>BufferingTime</strong></td>
<td>Usar <em>rede</em>. <strong>bufferingTime</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ButtonsAvailable</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Canpreview</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Canexamine</strong></td>
<td>Use <em>controles</em>. <strong>IsAvailable</strong>( &quot; Fastforward &quot; ) e <em>Controls</em>.<strong> IsAvailable</strong>( &quot; fastReverse &quot; ).</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CanSeek</strong></td>
<td>Use <em>controles</em>. <strong>IsAvailable</strong> para testar se um método de busca específico pode ser executado.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CanSeekToMarkers</strong></td>
<td>Use <em>controles</em>. <strong>IsAvailable</strong>( &quot; CurrentMarker &quot; ). Usar <em>mídia</em>. <strong>markerCount</strong> para recuperar a contagem de marcadores em um item de mídia específico. Use <em>controles</em>. <strong>currentMarker</strong> para especificar ou recuperar o número do marcador atual.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CaptioningID</strong></td>
<td>Use <em>ClosedCaption</em>. <strong>captioningID</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CCActive</strong></td>
<td>Não disponível. Consulte <a href="closed-captioning.md">Legendagem oculta</a> para obter informações sobre como legendas ocultas foram alteradas no Windows Media Player.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ChannelDescription</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ChannelName</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ChannelURL</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ClickToPlay</strong></td>
<td>Não disponível. Você deve fornecer controles na sua interface do usuário para iniciar a reprodução. Como alternativa, o usuário pode clicar com o botão direito do mouse na imagem de vídeo para abrir um menu pop-up que contém uma seleção de <strong>reproduzir/pausar</strong> se o <em>Player</em>. <strong>enableContextMenu</strong> é igual a true.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ClientID</strong></td>
<td>Não disponível. O Windows Media Player 9 Series ou posterior permite que o usuário selecione se uma ID de Player exclusiva é transmitida aos provedores de conteúdo.<br/> Se o usuário selecionar essa opção, o Player enviará uma ID exclusiva para o Windows Media Server. A ID é registrada no arquivo de log do servidor, localizado no.. pasta <em>system32\logfiles</em> por padrão. O nome do campo de log é &quot; c-playerid &quot; . O registro em log do servidor não está habilitado por padrão no Windows Media Services.<br/> Se o usuário não selecionar essa opção, o servidor gerará uma ID de sessão aleatória, que é exclusiva para cada cliente para uma determinada sessão.<br/> Para obter mais informações, consulte a documentação do Windows Media Services 9 Series.<br/></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CodecCount</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>COLORKEY</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ConnectionSpeed</strong></td>
<td>Não disponível. Usar <em>rede</em>. taxa <strong>de bits para determinar</strong> a tarifa de bit atual.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ContactAddress</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ContactEmail</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ContactPhone</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CreationDate</strong></td>
<td>Use <em>mediacollection</em>. <strong>getMediaAtom</strong>( &quot; CreationDate &quot; ) para recuperar o índice do átomo de data de criação. Usar <em>mídia</em>. <strong>getItemInfoByAtom</strong> para recuperar os metadados.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentAngle</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentAudioStream</strong></td>
<td>Use <em>controles</em>. <strong>currentAudioLanguageIndex</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentButton</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentCCService</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentChapter</strong></td>
<td>Recupere a playlist atual. Se a playlist atual não for a mesma que a playlist retornada pelo <em>cdrom</em>. em <strong>seguida, não</strong>há um capítulo atual. Caso contrário, o número do capítulo atual será o índice da mídia atual na playlist atual.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentDiscSide</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentDomain</strong></td>
<td>Use o <em>DVD</em>. <strong>domínio</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentMarker</strong></td>
<td>Use <em>controles</em>. <strong>currentMarker</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentPosition</strong></td>
<td>Use <em>controles</em>. <strong>CurrentPosition</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentSubpictureStream</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentTime</strong></td>
<td>Use <em>controles</em>. <strong>currentPositionTimeCode</strong>, <em>Controls</em>. <strong>currentPositionString</strong>ou <em>Controls</em>. <strong>CurrentPosition.</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentTitle</strong></td>
<td>Recupere a playlist atual. Se a playlist atual for a mesma que a playlist retornada pelo <em>cdrom</em>. na lista de <strong>reprodução</strong>, o número do título é o índice da mídia atual na playlist atual.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentVolume</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CursorType</strong></td>
<td>Não disponível. Em vez disso, use os estilos do Internet Explorer.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>DefaultFrame</strong></td>
<td>Use <em>as configurações</em>. <strong>DefaultFrame</strong>ou usar um <PARAM> atributo no <OBJECT> elemento: <pre data-space="preserve"><code><PARAM NAME=&quot;defaultFrame&quot; VALUE=&quot;right&quot;></code></pre></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>DisplayBackColor</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>DisplayForeColor</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>DisplayMode</strong></td>
<td>A posição atual pode ser recuperada em segundos desde o início como um <strong>número</strong> usando <em>controles</em>. <strong>CurrentPosition</strong>, como uma <strong>cadeia de caracteres</strong> formatada como hh: mm: SS (horas, minutos, segundos) usando <em>controles</em>. <strong>currentPositionString</strong>, ou no formato de código de tempo usando <em>controles</em>. <strong>currentPositionTimeCode</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Exibir</strong></td>
<td>A exibição padrão é redimensionada automaticamente para se ajustar à mídia. Você pode definir as propriedades Height e Width na <OBJECT> marca ou no script. Use o <em>Player</em>. <strong>tela inteira</strong> para alternar para o modo de tela inteira.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Duração</strong></td>
<td>Usar <em>mídia</em>. <strong>duração</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>DVD</strong></td>
<td>Use o <em>Player</em>. <strong>DVD</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>EnableContextMenu</strong></td>
<td>Use o <em>Player</em>. <strong>enableContextMenu</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Habilitado</strong></td>
<td>Use o <em>Player</em>. <strong>habilitado</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>EnableFullScreenControls</strong></td>
<td>Ao usar o Windows Media Player 9 Series ou posterior, os controles de tela inteira são habilitados automaticamente, a menos que o <em>Player</em>. <strong></strong>  =  UIMODE &quot; nenhum &quot; .</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>EnablePositionControls</strong></td>
<td>Não disponível. Você pode fornecer controles personalizados ou usar o <em>Player</em>. <strong>UIMODE</strong> para escolher uma configuração padrão.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>EnableTracker</strong></td>
<td>Não disponível. Você pode fornecer um controle personalizado ou usar o <em>Player</em>. <strong>UIMODE</strong> para escolher uma configuração padrão.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>EntryCount</strong></td>
<td>Use a <em>lista de reprodução</em>. <strong>contagem</strong> de</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ErrorCode</strong></td>
<td>Use <em>ErrorItem</em>. <strong>ErrorCode</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ErrorCorrection</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ErrorDescription</strong></td>
<td>Use <em>ErrorItem</em>. <strong>errorDescription</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Nome do arquivo</strong></td>
<td>Use o <em>Player</em>. <strong>URL</strong> ou <em>Player</em>. <strong>currentMedia</strong>. Use <em>controles</em>. <strong>currentItem</strong> ao trabalhar em uma playlist.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>FramesPerSecond</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>HasError</strong></td>
<td><em>Erro</em>de uso. <strong>errorCount</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>HasMultipleItems</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ImageSourceHeight</strong></td>
<td>Usar <em>mídia</em>. <strong>imageSourceHeight</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ImageSourceWidth</strong></td>
<td>Usar <em>mídia</em>. <strong>imageSourceWidth</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>InvokeURLs</strong></td>
<td>Use <em>as configurações</em>. <strong>invokeURLs</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Isbroadcast</strong></td>
<td>Usar <em>rede</em>. <strong>sourceProtocol</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>IsDurationValid</strong></td>
<td>Não disponível. <em>Mídia</em>. <strong>Duration</strong> contém um valor válido quando usado com o objeto de mídia atual.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Idioma</strong> do</td>
<td>Use <em>controles</em>. <strong>currentAudioLanguage</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>LostPackets</strong></td>
<td>Usar <em>rede</em>. <strong>lostPackets</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>MarkerCount</strong></td>
<td>Usar <em>mídia</em>. <strong>markerCount</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Sem áudio</strong></td>
<td>Use <em>as configurações</em>. <strong>sem áudio</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>OpenState</strong></td>
<td>Use o <em>Player</em>. <strong>OpenState</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>PlayCount</strong></td>
<td>Use <em>as configurações</em>. <strong>playCount</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>PlayState</strong></td>
<td>Use o <em>Player</em>. <strong>PlayState</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Modo de exibição de visualização</strong></td>
<td>Não disponível. Use uma estrutura de loop de script com um temporizador HTML para duplicar essa funcionalidade.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Taxa</strong> de</td>
<td>Use <em>as configurações</em>. <strong>taxa</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ReadyState</strong></td>
<td>Use o <em>Player</em>. <strong>OpenState</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ReceivedPackets</strong></td>
<td>Usar <em>rede</em>. <strong>receivedPackets</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ReceptionQuality</strong></td>
<td>Usar <em>rede</em>. <strong>receptionQuality</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>RecoveredPackets</strong></td>
<td>Usar <em>rede</em>. <strong>recoveredPackets</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Raiz</strong> do</td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SAMIFileName</strong></td>
<td>Use <em>ClosedCaption</em>. <strong>SAMIFileName</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SAMILang</strong></td>
<td>Use <em>ClosedCaption</em>. <strong>SAMILang</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Samistyle</strong></td>
<td>Use <em>ClosedCaption</em>. <strong>Samistyle</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SelectionEnd</strong></td>
<td>Usar <em>mídia</em>. <strong>duração</strong> para determinar o comprimento de um objeto de <strong>mídia</strong> . Use um marcador com <em>controles</em>. <strong>currentMarker</strong> para especificar uma posição de extremidade personalizada.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SelectionStart</strong></td>
<td>Use <em>controles</em>. <strong>CurrentPosition</strong> para iniciar a reprodução de uma determinada posição ou usar um marcador com <em>controles</em>. <strong>currentMarker</strong> para especificar uma posição de início personalizada.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SendErrorEvents</strong></td>
<td>Os erros são enfileirados. Use o objeto <strong>Error</strong> e o objeto <strong>ErrorItem</strong> para recuperar informações de erro.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SendKeyboardEvents</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SendMouseClickEvents</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SendMouseMoveEvents</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SendOpenStateChangeEvents</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SendPlayStateChangeEvents</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SendWarningEvents</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ShowAudioControls</strong></td>
<td>Não disponível. Você pode fornecer controles personalizados ou usar o <em>Player</em>. <strong>UIMODE</strong> para escolher uma configuração padrão.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Conlegendas</strong></td>
<td>Não disponível. Você pode fornecer uma exibição personalizada de legenda oculta.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Percontroles</strong></td>
<td>Não disponível. Você pode fornecer controles personalizados ou usar o <em>Player</em>. <strong>UIMODE</strong> para escolher uma configuração padrão.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Exibir</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ShowGotoBar</strong></td>
<td>Não disponível. Você pode fornecer funcionalidade personalizada usando o objeto de mídia</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowPositionControls</strong></td>
<td>Não disponível. Você pode fornecer controles personalizados ou usar o <em>Player</em>. <strong>UIMODE</strong> para escolher uma configuração padrão.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Defaultstatusbar</strong></td>
<td>Não disponível. Você pode fornecer controles personalizados ou usar o <em>Player</em>. <strong>UIMODE</strong> para escolher uma configuração padrão.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Controle</strong> de</td>
<td>Não disponível. Você pode fornecer controles personalizados ou usar o <em>Player</em>. <strong>UIMODE</strong> para escolher uma configuração padrão.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Funcionalidade sourcelink</strong></td>
<td>Usar <em>mídia</em>. <strong>sourceURL</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SourceProtocol</strong></td>
<td>Usar <em>rede</em>. <strong>sourceProtocol</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>StreamCount</strong></td>
<td>Não disponível. Use <em>controles</em>. <strong>audioLanguageCount</strong> para recuperar o número de fluxos de idioma de áudio.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Subimagem</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SubpictureStreamsAvailable</strong></td>
<td>Não disponível</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>TitlesAvailable</strong></td>
<td>Use o seguinte:<code>Player.Cdrom.playlist.count - 1</code><br/></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>TotalTitleTime</strong></td>
<td>Use <em>currentMedia</em>. <strong>duração</strong> ou <em>currentMedia</em>. <strong>durationstring</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>TransparentAtStart</strong></td>
<td>Use o script para especificar os valores de altura e largura para tornar o Player visível ou invisível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>UniqueId</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>VideoBorder3D</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>VideoBorderColor</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>VideoBorderWidth</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Volume</strong> do</td>
<td>Use <em>as configurações</em>. <strong>Volume</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>VolumesAvailable</strong></td>
<td>Não disponível.</td>
</tr>
</tbody>
</table>



 

A tabela a seguir compara os métodos de modelo de objeto do Windows Media Player versão 6,4 com o modelo de objeto do Windows Media Player 7 ou posterior.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Método do Windows Media Player 6,4</th>
<th>Windows Media Player 7 ou posterior equivalente</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>Player6</em>. <strong>AboutBox</strong></td>
<td>Use o <em>Player</em>. <strong>versionInfo</strong> para recuperar a versão do Windows Media Player.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>BackwardScan</strong></td>
<td>Use <em>as configurações</em>. <strong>taxa</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ButtonActivate</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ButtonSelectAndActivate</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Cancelar</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ChapterPlay</strong></td>
<td>Se já estiver executando a playlist de título especificada, recupere o capítulo desejado como um objeto de mídia usando a seguinte sintaxe:
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
Em seguida, especifique <em>Player</em>. <strong>currentMedia</strong> usando o objeto de mídia retornado.<br/></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ChapterPlayAutoStop</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ChapterSearch</strong></td>
<td>Se já estiver executando a playlist de título especificada, recupere o capítulo desejado como um objeto de mídia usando a seguinte sintaxe:
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
Em seguida, especifique <em>Player</em>. <strong>currentMedia</strong> usando o objeto de mídia retornado.<br/></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Fastforward</strong></td>
<td>Use <em>controles</em>. <strong>Fastforward</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>FastReverse</strong></td>
<td>Use <em>controles</em>. <strong>fastReverse</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ForwardScan</strong></td>
<td>Use <em>as configurações</em>. <strong>taxa</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetAllGPRMs</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetAllSPRMs</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetAudioLanguage</strong></td>
<td>Use <em>controles</em>. <strong>currentAudioLanguage</strong> para recuperar o LCID do idioma de áudio atual.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetCodecDescription</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetCodecInstalled</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetCodecURL</strong></td>
<td>Use <em>ErrorItem</em>. <strong>customUrl</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetCurrentEntry</strong></td>
<td>Use o script para executar um loop na playlist atual. Usar <em>mídia</em>. <strong>isidêntico</strong> para comparar cada entrada da lista de reprodução com o <em>Player</em>. objeto <strong>currentMedia</strong> .</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong></strong> Getmarkname</td>
<td>Usar <em>mídia</em>. <strong>Getmarcadorname</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Getmarcadortime</strong></td>
<td>Usar <em>mídia</em>. <strong>Getmarcadortime</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetMediaInfoString</strong></td>
<td>Usar <em>mídia</em>. <strong>getItemInfo</strong>, <em>mídia</em>. <strong>getItemInfoByAtom</strong>e seus métodos associados para recuperar metadados.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetMediaParameter</strong></td>
<td>Use a <em>lista de reprodução</em>. <strong>Item</strong> para recuperar um item de mídia. Em seguida, use a <em>mídia</em>. <strong>getItemInfo</strong> para recuperar a cadeia de caracteres do parâmetro.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetMediaParameterName</strong></td>
<td>Use a <em>lista de reprodução</em>. <strong>Item</strong> para recuperar um item de mídia. Em seguida, use a <em>mídia</em>. <strong>GetAttributeName</strong> para recuperar a cadeia de caracteres do parâmetro.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetMoreInfoURL</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetNumberOfChapters</strong></td>
<td>Se um título estiver sendo executado no momento, use <em>currentPlaylist</em>. <strong>contagem</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetStream</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Getstreamname</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetStreamSelected</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetSubpictureLanguage</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Grupo</strong></td>
<td>Use o <em>DVD</em>. <strong>voltar</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>IsSoundCardEnabled</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>LeftButtonSelect</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>LowerButtonSelect</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>MenuCall</strong></td>
<td>Use o <em>DVD</em>. <strong>titleMenu</strong> ou <em>DVD</em>. <strong>topMenu</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Avançar</strong></td>
<td>Use <em>controles</em>. <strong>em seguida</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>NextPGSearch</strong></td>
<td>Use <em>controles</em>. <strong>em seguida</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Abrir</strong> o</td>
<td>Use o <em>Player</em>. <strong>URL</strong> ou <em>Player</em>. <strong>currentMedia</strong>. Os arquivos sempre são abertos de forma assíncrona.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Pausar</strong></td>
<td>Use <em>controles</em>. <strong>Pausar</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Reproduzir</strong></td>
<td>Use <em>controles</em>. <strong>reproduzir</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Anterior</strong></td>
<td>Use <em>controles</em>. <strong>anterior</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>PrevPGSearch</strong></td>
<td>Use <em>controles</em>. <strong>anterior</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ResumeFromMenu</strong></td>
<td>Use o <em>DVD</em>. <strong>retomar</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>RightButtonSelect</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SetCurrentEntry</strong></td>
<td>Recupere um objeto de mídia usando <em>currentPlaylist</em>. <strong>Item</strong>(<em>entryNumber</em>). Em seguida, especifique o objeto de mídia recuperado usando <em>controles</em>. <strong>currentItem</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowDialog</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>StillOff</strong></td>
<td>Use <em>controles</em>. <strong>reproduzir</strong>. Como alternativa, use <em>controles</em>. Em <strong>seguida</strong> , se estiver atualmente no modo ainda.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Parar</strong></td>
<td>Use <em>controles</em>. <strong>parar</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>StreamSelect</strong></td>
<td>Não disponível. Use <em>controles</em>. <strong>currentAudioLanguage</strong> para especificar um fluxo de idioma de áudio.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Timeplay</strong></td>
<td>Na lista de reprodução raiz, use <em>currentPlaylist</em>. <strong>Item</strong>(<em>índice</em>) para recuperar um objeto de mídia. Em seguida, defina o objeto de mídia como o atual usando <em>controles</em>. <strong>currentItem</strong>. Em seguida, especifique os <em>controles</em>. <strong>CurrentPosition</strong> usando um valor de tempo em segundos.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Timesearch</strong></td>
<td>Use <em>controles</em>. <strong>CurrentPosition</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>TitlePlay</strong></td>
<td>Se já estiver executando a playlist de título especificada, recupere o capítulo desejado como um objeto de mídia usando a seguinte sintaxe:
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
Em seguida, especifique <em>Player</em>. <strong>currentMedia</strong> usando o objeto de mídia retornado.<br/> Como alternativa, use <em>currentPlaylist</em>. <strong>Item</strong> para recuperar um objeto de mídia e, em seguida, use o objeto de mídia retornado para especificar <em>controles</em>. <strong>currentItem</strong>.<br/></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>TopPGSearch</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>UOPValid</strong></td>
<td>Não disponível</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>UpperButtonSelect</strong></td>
<td>Não disponível.</td>
</tr>
</tbody>
</table>



 

A tabela a seguir compara os eventos do modelo de objeto do Windows Media Player versão 6,4 com o modelo de objeto do Windows Media Player 7 ou posterior.



| Evento 6,4 do Windows Media Player  | Windows Media Player 7 ou posterior equivalente                                                                                                                                                                               |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Player6*. **Armazenamento em buffer**         | Use o *Player*. **Armazenamento em buffer**.                                                                                                                                                                                              |
| *Player6*. **Clique em**             | Use o *Player*. **Clique em**                                                                                                                                                                                                   |
| *Player6*. **DblClick**          | Use o *Player*. **DoubleClick**                                                                                                                                                                                             |
| *Player6*. **Desconectar**        | Não disponível.                                                                                                                                                                                                           |
| *Player6*. **DisplayModeChange** | Não disponível.                                                                                                                                                                                                           |
| *Player6*. **DVDNotify**         | *Player*. **DomainChange** e *Player*. **OpenPlaylistSwitch** são eventos específicos de DVD. Outros eventos relacionados às listas de reprodução, mídia e mídia de CD-ROM também podem se aplicar, dependendo do aplicativo.                        |
| *Player6*. **EndOfStream**       | Use o *Player*. **PlayState**.                                                                                                                                                                                              |
| *Player6*. **Erro** do             | O evento está inalterado. Os erros, no entanto, são enfileirados. Use o objeto de **erro** com o objeto **ErrorItem** para recuperar informações de erro da fila. Consulte o código de exemplo na seção anterior, tratamento de erro. |
| *Player6*. **KeyDown**           | Use o *Player*. **KeyDown**                                                                                                                                                                                                 |
| *Player6*. **KeyPress**          | Use o *Player*. **KeyPress**                                                                                                                                                                                                |
| *Player6*. **KeyUp**             | Use o *Player*. **KeyUp**                                                                                                                                                                                                   |
| *Player6*. **MarkerHit**         | Use o *Player*. **MarkerHit**.                                                                                                                                                                                              |
| *Player6*. **MouseDown**         | Use o *Player*. **MouseDown**                                                                                                                                                                                               |
| *Player6*. **MouseMove**         | Use o *Player*. **MouseMove**                                                                                                                                                                                               |
| *Player6*. **MouseUp**           | Use o *Player*. **MouseUp**                                                                                                                                                                                                 |
| *Player6*. **NewStream**         | Use o *Player*. **OpenStateChange**                                                                                                                                                                                         |
| *Player6*. **OpenStateChange**   | Use o *Player*. **OpenStateChange**.                                                                                                                                                                                        |
| *Player6*. **PlayStateChange**   | Use o *Player*. **PlayStateChange**.                                                                                                                                                                                        |
| *Player6*. **PositionChange**    | Use o *Player*. **PositionChange**.                                                                                                                                                                                         |
| *Player6*. **ReadyStateChange**  | Use o *Player*. **PlayStateChange**.                                                                                                                                                                                        |
| *Player6*. **ScriptCommand**     | Use o *Player*. **ScriptCommand**.                                                                                                                                                                                          |
| *Player6*. **Aviso**           | Não disponível.                                                                                                                                                                                                           |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de migração do modelo de objeto**](object-model-migration-guide.md)
</dt> <dt>

[**Referência de modelo de objeto para scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 






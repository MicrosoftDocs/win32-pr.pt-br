---
title: Comparação detalhada do modelo de objeto
description: Comparação detalhada do modelo de objeto
ms.assetid: 8f08e2a6-1944-4814-b3b7-680a3722e1a0
keywords:
- Windows Media Player,modelo de objeto
- Windows Media Player modelo de objeto, diferenças de versão
- modelo de objeto, diferenças de versão
- Windows Media Player ActiveX controle, diferenças de versão
- ActiveX controle, diferenças de versão
- Windows Media Player Controle ActiveX dispositivo móvel, diferenças de versão
- Windows Media Player Móvel, modelo de objeto
- guia de migração, diferenças de versão
- versões do Windows Media Player,modelo de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f2e092f7e32b889056841b5802dffa141c0be4
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884763"
---
# <a name="detailed-object-model-comparison"></a>Comparação detalhada do modelo de objeto

A tabela a seguir compara as Windows Media Player do modelo de objeto 6.4 com o modelo de objeto Windows Media Player 7 ou posterior.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Windows Media Player propriedade 6.4</th>
<th>Windows Media Player 7 ou posterior equivalente</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>Player6</em>. <strong>AllowChangeDisplaySize</strong></td>
<td>A exibição de Windows Media Player 7 ou posterior é relize automaticamente para se ajustar à mídia. Você pode definir as propriedades de altura e largura na &lt; marca OBJECT ou no &gt; script.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>AllowScan</strong></td>
<td><em>Controla</em>. <strong>fastForward</strong> e <em>Controls</em>. <strong>fastReverse são</strong> habilitados automaticamente para tipos de arquivo que suportam esses métodos.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ÂngulosAvailable</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>AnimationAtStart</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>AudioStream</strong></td>
<td>Use <em>Controles</em>. <strong>currentAudioLanguageIndex.</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>AudioStreamsAvailable</strong></td>
<td>Use <em>Controles</em>. <strong>audioLanguageCount.</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>AutoRewind</strong></td>
<td>Use <em>Controles</em>. <strong>currentPosition</strong> no script para especificar ou recuperar a posição atual. Como alternativa, use marcadores e o <em>Player</em>. <strong>evento markerHit.</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>AutoSize</strong></td>
<td>O ajuste automático é o comportamento padrão. Para substituir o tamanho automático, de definir as propriedades de altura e largura na &lt; marca OBJECT ou no &gt; script.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Início Automático</strong></td>
<td>Use <em>Configurações</em>. <strong>AutoStart</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Saldo</strong></td>
<td>Use <em>Configurações</em>. <strong>balancear</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Largura de banda</strong></td>
<td>Use <em>Rede</em>. <strong>bandWidth</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>BaseURL</strong></td>
<td>Use <em>Configurações</em>. <strong>baseURL</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>BufferingCount</strong></td>
<td>Use <em>Rede.</em> <strong>bufferingCount.</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>BufferingProgress</strong></td>
<td>Use <em>Rede</em>. <strong>bufferingProgress.</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>BufferingTime</strong></td>
<td>Use <em>Rede</em>. <strong>bufferingTime</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>BotõesAvailable</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CanPreview</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CanScan</strong></td>
<td>Use <em>Controles</em>. <strong>isAvailable</strong>( &quot; FastForward &quot; ) e <em>controles</em>.<strong> isAvailable</strong>( &quot; FastReverse &quot; ).</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CanSeek</strong></td>
<td>Use <em>Controles</em>. <strong>isAvailable</strong> para testar se um método de busca específico pode ser executado.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CanSeekToMarkers</strong></td>
<td>Use <em>Controles</em>. <strong>isAvailable</strong>( &quot; CurrentMarker &quot; ). Use <em>Mídia</em>. <strong>markerCount</strong> para recuperar a contagem de marcadores em um item de mídia específico. Use <em>Controles</em>. <strong>currentMarker</strong> para especificar ou recuperar o número do marcador atual.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CaptioningID</strong></td>
<td>Use <em>ClosedCaption</em>. <strong>captioningID.</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CCActive</strong></td>
<td>Não disponível. Consulte <a href="closed-captioning.md">Legendas fechadas para</a> obter informações sobre como a legenda fechada foi alterada Windows Media Player.</td>
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
<td>Não disponível. Você deve fornecer controles na interface do usuário para iniciar a reprodução. Como alternativa, o usuário pode clicar com o botão direito do mouse na imagem de vídeo para abrir um menu pop-up que contém uma seleção <strong>Reproduzir/Pausar</strong> se o <em>Player</em>. <strong>enableContextMenu</strong> é igual a true.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ClientID</strong></td>
<td>Não disponível. Windows Media Player Série 9 ou posterior permite que o usuário selecione se uma ID exclusiva do Player é transmitida para provedores de conteúdo.<br/> Se o usuário selecionar essa opção, o Player enviará uma ID exclusiva para o servidor Windows Mídia. A ID é registrada no arquivo de log do servidor, localizado no .. <em>pasta system32\logfiles</em> por padrão. O nome do campo de log &quot; é c-playerid. &quot; O registro em log do servidor não está habilitado por padrão Windows Media Services.<br/> Se o usuário não selecionar essa opção, o servidor gerará uma ID de sessão aleatória, que é exclusiva para cada cliente para uma determinada sessão.<br/> Para obter mais informações, consulte a documentação Windows Media Services série 9.<br/></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CodecCount</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ColorKey</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ConnectionSpeed</strong></td>
<td>Não disponível. Use <em>Rede</em>. <strong>bitRate</strong> para determinar a taxa de bits atual.</td>
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
<td>Use <em>MediaCollection</em>. <strong>getMediaAtom</strong>( &quot; CreationDate &quot; ) para recuperar o índice do atom de data de criação. Use <em>Mídia</em>. <strong>getItemInfoByAtom</strong> para recuperar os metadados.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentAngle</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentAudioStream</strong></td>
<td>Use <em>Controles</em>. <strong>currentAudioLanguageIndex.</strong></td>
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
<td>Recupere a playlist atual. Se a playlist atual não for a mesma que a playlist retornada por <em>Cdrom</em>. <strong>playlist</strong>, então não há nenhum capítulo atual. Caso contrário, o número do capítulo atual será o índice da mídia atual na playlist atual.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentDiscSide</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentDomain</strong></td>
<td>Use <em>DVD</em>. <strong>domínio</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentMarker</strong></td>
<td>Use <em>Controles</em>. <strong>currentMarker</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentPosition</strong></td>
<td>Use <em>Controles</em>. <strong>currentPosition</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentSubpictureStream</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentTime</strong></td>
<td>Use <em>Controles</em>. <strong>currentPositionTimeCode,</strong> <em>controla</em>. <strong>currentPositionString</strong>ou <em>Controla</em>. <strong>currentPosition.</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CurrentTitle</strong></td>
<td>Recupere a playlist atual. Se a playlist atual for a mesma que a playlist retornada por <em>Cdrom</em>. <strong>playlist</strong>, em seguida, o número do título é o índice da mídia atual na playlist atual.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentVolume</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CursorType</strong></td>
<td>Não disponível. Use Internet Explorer estilos em vez disso.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>DefaultFrame</strong></td>
<td>Use <em>Configurações</em>. <strong>defaultFrame</strong>ou use um <PARAM> atributo no &lt; elemento &gt; OBJECT:
<pre data-space="preserve"><code><PARAM NAME=&quot;defaultFrame&quot; VALUE=&quot;right&quot;></code></pre></td>
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
<td>A posição atual pode ser recuperada em segundos desde o início como um <strong>Número</strong> usando <em>Controles</em>. <strong>currentPosition</strong>, como uma <strong>Cadeia de</strong> caracteres formatada como HH:MM:SS (horas, minutos, segundos) usando <em>Controles</em>. <strong>currentPositionString</strong>ou no formato de código de tempo usando <em>Controles</em>. <strong>currentPositionTimeCode.</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>DisplaySize</strong></td>
<td>A exibição padrão é reessalvada automaticamente para se ajustar à mídia. Você pode definir as propriedades de altura e largura na &lt; marca OBJECT ou no &gt; script. Use <em>Player</em>. <strong>fullScreen para</strong> alternar para o modo de tela inteira.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Duração</strong></td>
<td>Use <em>Mídia</em>. <strong>duração</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>DVD</strong></td>
<td>Use <em>Player</em>. <strong>DVD</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>EnableContextMenu</strong></td>
<td>Use <em>Player</em>. <strong>enableContextMenu.</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Habilitado</strong></td>
<td>Use <em>Player</em>. <strong>habilitado.</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>EnableFullScreenControls</strong></td>
<td>Ao usar Windows Media Player Série 9 ou posterior, os controles de tela inteira são habilitados automaticamente, a menos que <em>o Player</em>. <strong>uiMode</strong>  =  &quot; nenhum &quot; .</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>EnablePositionControls</strong></td>
<td>Não disponível. Você pode fornecer controles personalizados ou usar <em>o Player</em>. <strong>uimode para</strong> escolher uma configuração padrão.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>EnableTracker</strong></td>
<td>Não disponível. Você pode fornecer um controle personalizado ou usar <em>o Player</em>. <strong>uimode para</strong> escolher uma configuração padrão.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>EntryCount</strong></td>
<td>Use <em>Playlist</em>. <strong>count</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ErrorCode</strong></td>
<td>Use <em>ErrorItem</em>. <strong>errorCode</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ErrorCorrection</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ErrorDescription</strong></td>
<td>Use <em>ErrorItem</em>. <strong>errorDescription.</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>FileName</strong></td>
<td>Use <em>Player</em>. <strong>URL ou</strong> <em>Player.</em> <strong>currentMedia</strong>. Use <em>Controles</em>. <strong>currentItem ao</strong> trabalhar em uma playlist.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>FramesPerSecond</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>HasError</strong></td>
<td>Use <em>o erro</em>. <strong>errorCount</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>HasMultipleItems</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ImageSourceHeight</strong></td>
<td>Use <em>Mídia</em>. <strong>imageSourceHeight.</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ImageSourceWidth</strong></td>
<td>Use <em>Mídia</em>. <strong>imageSourceWidth.</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>InvokeURLs</strong></td>
<td>Use <em>Configurações</em>. <strong>invokeURLs</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>IsBroadcast</strong></td>
<td>Use <em>Rede</em>. <strong>sourceProtocol.</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>IsDurationValid</strong></td>
<td>Não disponível. <em>Mídia</em>. <strong>duration</strong> contém um valor válido quando usado com o objeto de mídia atual.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Idioma</strong></td>
<td>Use <em>Controles</em>. <strong>currentAudioLanguage</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>LostPackets</strong></td>
<td>Use <em>Rede</em>. <strong>lostPackets.</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>MarkerCount</strong></td>
<td>Use <em>Mídia</em>. <strong>markerCount.</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Mute</strong></td>
<td>Use <em>Configurações</em>. <strong>mute</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>OpenState</strong></td>
<td>Use <em>Player</em>. <strong>openState</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>PlayCount</strong></td>
<td>Use <em>Configurações</em>. <strong>playCount</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>PlayState</strong></td>
<td>Use <em>Player</em>. <strong>playState</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>PreviewMode</strong></td>
<td>Não disponível. Use uma estrutura de loop de script com um temporizador HTML para duplicar essa funcionalidade.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Taxa</strong></td>
<td>Use <em>Configurações</em>. <strong>taxa</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ReadyState</strong></td>
<td>Use <em>Player</em>. <strong>openState</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ReceivedPackets</strong></td>
<td>Use <em>Rede</em>. <strong>receivedPackets</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Igualdade de Recepção</strong></td>
<td>Use <em>Rede</em>. <strong>receptionQuality</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>RecoveredPackets</strong></td>
<td>Use <em>Rede</em>. <strong>recoveredPackets.</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Raiz</strong></td>
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
<td><em>Player6</em>. <strong>SAMIStyle</strong></td>
<td>Use <em>ClosedCaption</em>. <strong>SAMIStyle.</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SelectionEnd</strong></td>
<td>Use <em>Mídia</em>. <strong>duração</strong> para determinar o comprimento de um <strong>objeto Media.</strong> Use um marcador com <em>Controles</em>. <strong>currentMarker</strong> para especificar uma posição de extremidade personalizada.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SelectionStart</strong></td>
<td>Use <em>Controles</em>. <strong>currentPosition</strong> para iniciar a reprodução de uma posição específica ou usar um marcador com <em>Controles</em>. <strong>currentMarker</strong> para especificar uma posição inicial personalizada.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SendErrorEvents</strong></td>
<td>Os erros são ensuados. Use o <strong>objeto Error</strong> e o <strong>objeto ErrorItem</strong> para recuperar informações de erro.</td>
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
<td>Não disponível. Você pode fornecer controles personalizados ou usar <em>o Player</em>. <strong>uimode para</strong> escolher uma configuração padrão.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowCaptioning</strong></td>
<td>Não disponível. Você pode fornecer uma exibição de legenda fechada personalizada.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ShowControls</strong></td>
<td>Não disponível. Você pode fornecer controles personalizados ou usar <em>o Player</em>. <strong>uimode para</strong> escolher uma configuração padrão.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowDisplay</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ShowGotoBar</strong></td>
<td>Não disponível. Você pode fornecer funcionalidade personalizada usando o objeto Mídia</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowPositionControls</strong></td>
<td>Não disponível. Você pode fornecer controles personalizados ou usar <em>o Player</em>. <strong>uimode para</strong> escolher uma configuração padrão.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ShowStatusBar</strong></td>
<td>Não disponível. Você pode fornecer controles personalizados ou usar <em>o Player</em>. <strong>uimode para</strong> escolher uma configuração padrão.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowTracker</strong></td>
<td>Não disponível. Você pode fornecer controles personalizados ou usar <em>o Player</em>. <strong>uimode para</strong> escolher uma configuração padrão.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SourceLink</strong></td>
<td>Use <em>Mídia</em>. <strong>sourceURL</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SourceProtocol</strong></td>
<td>Use <em>Rede</em>. <strong>sourceProtocol.</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>StreamCount</strong></td>
<td>Não disponível. Use <em>Controles</em>. <strong>audioLanguageCount para</strong> recuperar o número de fluxos de linguagem de áudio.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>SubpictureOn</strong></td>
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
<td>Use <em>currentMedia</em>. <strong>duration</strong> ou <em>currentMedia.</em> <strong>durationString</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>TransparentAtStart</strong></td>
<td>Use o script para especificar os valores de altura e largura para tornar o jogador visível ou invisível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>UniqueID</strong></td>
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
<td><em>Player6</em>. <strong>Volume</strong></td>
<td>Use <em>Configurações</em>. <strong>Volume</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>VolumesAvailable</strong></td>
<td>Não disponível.</td>
</tr>
</tbody>
</table>



 

A tabela a seguir compara os Windows Media Player modelo de objeto da versão 6.4 com o modelo de objeto Windows Media Player 7 ou posterior.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Windows Media Player método 6.4</th>
<th>Windows Media Player 7 ou posterior equivalente</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>Player6</em>. <strong>AboutBox</strong></td>
<td>Use <em>Player</em>. <strong>versionInfo</strong> para recuperar a versão do Windows Media Player.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>BackwardScan</strong></td>
<td>Use <em>Configurações</em>. <strong>taxa</strong>.</td>
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
<td>Se já estiver tocando a playlist de título especificada, recupere o capítulo desejado como um objeto de mídia usando a seguinte sintaxe:
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
Em seguida, especifique <em>Player</em>. <strong>currentMedia usando</strong> o objeto de mídia retornado.<br/></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ChapterPlayAutoStop</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ChapterSearch</strong></td>
<td>Se já estiver tocando a playlist de título especificada, recupere o capítulo desejado como um objeto de mídia usando a seguinte sintaxe:
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
Em seguida, especifique <em>Player</em>. <strong>currentMedia usando</strong> o objeto de mídia retornado.<br/></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>FastForward</strong></td>
<td>Use <em>Controles</em>. <strong>fastForward.</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>FastReverse</strong></td>
<td>Use <em>Controles</em>. <strong>fastReverse</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ForwardScan</strong></td>
<td>Use <em>Configurações</em>. <strong>taxa</strong>.</td>
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
<td>Use <em>Controles</em>. <strong>currentAudioLanguage</strong> para recuperar o LCID da linguagem de áudio atual.</td>
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
<td>Use <em>ErrorItem</em>. <strong>customUrl.</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetCurrentEntry</strong></td>
<td>Use o script para fazer um loop na playlist atual. Use <em>Mídia</em>. <strong>isIdentical para</strong> comparar cada entrada na playlist com o <em>Player</em>. <strong>objeto currentMedia.</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetMarkerName</strong></td>
<td>Use <em>Mídia</em>. <strong>getMarkerName.</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetMarkerTime</strong></td>
<td>Use <em>Mídia</em>. <strong>getMarkerTime.</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetMediaInfoString</strong></td>
<td>Use <em>Mídia</em>. <strong>getItemInfo,</strong> <em>Media</em>. <strong>getItemInfoByAtom</strong>e seus métodos associados para recuperar metadados.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetMediaParameter</strong></td>
<td>Use <em>Playlist</em>. <strong>item</strong> para recuperar um item de mídia. Em seguida, use <em>Mídia</em>. <strong>getItemInfo para</strong> recuperar a cadeia de caracteres de parâmetro.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetMediaParameterName</strong></td>
<td>Use <em>Playlist</em>. <strong>item</strong> para recuperar um item de mídia. Em seguida, use <em>Mídia</em>. <strong>getAttributeName para</strong> recuperar a cadeia de caracteres de parâmetro.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetMoreInfoURL</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetNumberOfChapters</strong></td>
<td>Se um título estiver em reprodução no momento, use <em>currentPlaylist</em>. <strong>count</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>GetStreamGroup</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>GetStreamName</strong></td>
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
<td><em>Player6</em>. <strong>GoUp</strong></td>
<td>Use <em>DVD</em>. <strong>back</strong>.</td>
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
<td>Use <em>DVD</em>. <strong>titleMenu ou</strong> <em>DVD.</em> <strong>topMenu</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Próximo</strong></td>
<td>Use <em>Controles</em>. <strong>em seguida,</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>NextPGSearch</strong></td>
<td>Use <em>Controles</em>. <strong>em seguida,</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Abrir</strong></td>
<td>Use <em>Player</em>. <strong>URL ou</strong> <em>Player.</em> <strong>currentMedia</strong>. Os arquivos sempre são abertos de forma assíncrona.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Pausar</strong></td>
<td>Use <em>Controles</em>. <strong>pause</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Reproduzir</strong></td>
<td>Use <em>Controles</em>. <strong>reproduzir</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Anterior</strong></td>
<td>Use <em>Controles</em>. <strong>anterior.</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>PrevPGSearch</strong></td>
<td>Use <em>Controles</em>. <strong>anterior.</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ResumeFromMenu</strong></td>
<td>Use <em>DVD</em>. <strong>retomar</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>RightButtonSelect</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SetCurrentEntry</strong></td>
<td>Recupere um objeto de mídia usando <em>currentPlaylist.</em> <strong>item</strong>(<em>entryNumber</em>). Em seguida, especifique o objeto de mídia recuperado usando <em>Controles</em>. <strong>currentItem</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowDialog</strong></td>
<td>Não disponível.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>StillOff</strong></td>
<td>Use <em>Controles</em>. <strong>reproduzir</strong>. Como alternativa, use <em>Controles</em>. <strong>Em</strong> seguida, se estiver no modo ainda.</td>
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



 

a tabela a seguir compara os eventos de modelo de objeto Windows Media Player versão 6,4 com o modelo de objeto Windows Media Player 7 ou posterior.



| evento Windows Media Player 6,4  | equivalente a Windows Media Player 7 ou posterior                                                                                                                                                                               |
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

 

 






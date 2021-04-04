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
# <a name="detailed-object-model-comparison"></a><span data-ttu-id="24c13-112">Comparação de modelo de objeto detalhado</span><span class="sxs-lookup"><span data-stu-id="24c13-112">Detailed Object Model Comparison</span></span>

<span data-ttu-id="24c13-113">A tabela a seguir compara as propriedades do modelo de objeto do Windows Media Player 6,4 com o modelo de objeto do Windows Media Player 7 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="24c13-113">The following table compares the Windows Media Player 6.4 object model properties with the Windows Media Player 7 or later object model.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="24c13-114">Propriedade do Windows Media Player 6,4</span><span class="sxs-lookup"><span data-stu-id="24c13-114">Windows Media Player 6.4 property</span></span></th>
<th><span data-ttu-id="24c13-115">Windows Media Player 7 ou posterior equivalente</span><span class="sxs-lookup"><span data-stu-id="24c13-115">Windows Media Player 7 or later equivalent</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="24c13-116"><em>Player6</em>. <strong>AllowChangeDisplaySize</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-116"><em>Player6</em>.<strong>AllowChangeDisplaySize</strong></span></span></td>
<td><span data-ttu-id="24c13-117">A exibição do Windows Media Player 7 ou posterior é redimensionada automaticamente para se ajustar à mídia.</span><span class="sxs-lookup"><span data-stu-id="24c13-117">The display of Windows Media Player 7 or later automatically resizes to fit the media.</span></span> <span data-ttu-id="24c13-118">Você pode definir as propriedades Height e Width na <OBJECT> marca ou no script.</span><span class="sxs-lookup"><span data-stu-id="24c13-118">You can set the height and width properties in the <OBJECT> tag or in script.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-119"><em>Player6</em>. <strong>AllowScan</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-119"><em>Player6</em>.<strong>AllowScan</strong></span></span></td>
<td><span data-ttu-id="24c13-120">De <em>controle</em>.</span><span class="sxs-lookup"><span data-stu-id="24c13-120"><em>Controls</em>.</span></span> <span data-ttu-id="24c13-121"><strong>Fastforward</strong> e <em>Controls</em>. <strong>fastReverse</strong> são automaticamente habilitados para tipos de arquivo que dão suporte a esses métodos.</span><span class="sxs-lookup"><span data-stu-id="24c13-121"><strong>fastForward</strong> and <em>Controls</em>.<strong>fastReverse</strong> are automatically enabled for file types that support these methods.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-122"><em>Player6</em>. <strong>AnglesAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-122"><em>Player6</em>.<strong>AnglesAvailable</strong></span></span></td>
<td><span data-ttu-id="24c13-123">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-123">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-124"><em>Player6</em>. <strong>AnimationAtStart</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-124"><em>Player6</em>.<strong>AnimationAtStart</strong></span></span></td>
<td><span data-ttu-id="24c13-125">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-125">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-126"><em>Player6</em>. <strong>AudioStream</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-126"><em>Player6</em>.<strong>AudioStream</strong></span></span></td>
<td><span data-ttu-id="24c13-127">Use <em>controles</em>. <strong>currentAudioLanguageIndex</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-127">Use <em>Controls</em>.<strong>currentAudioLanguageIndex</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-128"><em>Player6</em>. <strong>AudioStreamsAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-128"><em>Player6</em>.<strong>AudioStreamsAvailable</strong></span></span></td>
<td><span data-ttu-id="24c13-129">Use <em>controles</em>. <strong>audioLanguageCount</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-129">Use <em>Controls</em>.<strong>audioLanguageCount</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-130"><em>Player6</em>. <strong>Rebobinar</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-130"><em>Player6</em>.<strong>AutoRewind</strong></span></span></td>
<td><span data-ttu-id="24c13-131">Use <em>controles</em>. <strong>CurrentPosition</strong> no script para especificar ou recuperar a posição atual.</span><span class="sxs-lookup"><span data-stu-id="24c13-131">Use <em>Controls</em>.<strong>currentPosition</strong> in script to specify or retrieve the current position.</span></span> <span data-ttu-id="24c13-132">Como alternativa, use marcadores e o <em>Player</em>. evento <strong>markerHit</strong> .</span><span class="sxs-lookup"><span data-stu-id="24c13-132">Alternatively, use markers and the <em>Player</em>.<strong>markerHit</strong> event.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-133"><em>Player6</em>. <strong>Dimensionamento automático</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-133"><em>Player6</em>.<strong>AutoSize</strong></span></span></td>
<td><span data-ttu-id="24c13-134">O dimensionamento automático é o comportamento padrão.</span><span class="sxs-lookup"><span data-stu-id="24c13-134">Automatic sizing is the default behavior.</span></span> <span data-ttu-id="24c13-135">Para substituir o dimensionamento automático, defina as propriedades de altura e largura na <OBJECT> marca ou no script.</span><span class="sxs-lookup"><span data-stu-id="24c13-135">To override automatic sizing, set the height and width properties in the <OBJECT> tag or in script.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-136"><em>Player6</em>. <strong>Inicialização automática</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-136"><em>Player6</em>.<strong>AutoStart</strong></span></span></td>
<td><span data-ttu-id="24c13-137">Use <em>as configurações</em>. <strong>inicialização automática</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-137">Use <em>Settings</em>.<strong>autoStart</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-138"><em>Player6</em>. <strong>Saldo</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-138"><em>Player6</em>.<strong>Balance</strong></span></span></td>
<td><span data-ttu-id="24c13-139">Use <em>as configurações</em>. <strong>saldo</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-139">Use <em>Settings</em>.<strong>balance</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-140"><em>Player6</em>. <strong>Largura de banda</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-140"><em>Player6</em>.<strong>Bandwidth</strong></span></span></td>
<td><span data-ttu-id="24c13-141">Usar <em>rede</em>. <strong>largura de banda</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-141">Use <em>Network</em>.<strong>bandWidth</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-142"><em>Player6</em>. <strong>BaseURL</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-142"><em>Player6</em>.<strong>BaseURL</strong></span></span></td>
<td><span data-ttu-id="24c13-143">Use <em>as configurações</em>. <strong>baseURL</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-143">Use <em>Settings</em>.<strong>baseURL</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-144"><em>Player6</em>. <strong>BufferingCount</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-144"><em>Player6</em>.<strong>BufferingCount</strong></span></span></td>
<td><span data-ttu-id="24c13-145">Usar <em>rede.</em> <strong>bufferingCount</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-145">Use <em>Network.</em><strong>bufferingCount</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-146"><em>Player6</em>. <strong>BufferingProgress</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-146"><em>Player6</em>.<strong>BufferingProgress</strong></span></span></td>
<td><span data-ttu-id="24c13-147">Usar <em>rede</em>. <strong>bufferingProgress</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-147">Use <em>Network</em>.<strong>bufferingProgress</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-148"><em>Player6</em>. <strong>BufferingTime</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-148"><em>Player6</em>.<strong>BufferingTime</strong></span></span></td>
<td><span data-ttu-id="24c13-149">Usar <em>rede</em>. <strong>bufferingTime</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-149">Use <em>Network</em>.<strong>bufferingTime</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-150"><em>Player6</em>. <strong>ButtonsAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-150"><em>Player6</em>.<strong>ButtonsAvailable</strong></span></span></td>
<td><span data-ttu-id="24c13-151">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-151">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-152"><em>Player6</em>. <strong>Canpreview</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-152"><em>Player6</em>.<strong>CanPreview</strong></span></span></td>
<td><span data-ttu-id="24c13-153">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-153">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-154"><em>Player6</em>. <strong>Canexamine</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-154"><em>Player6</em>.<strong>CanScan</strong></span></span></td>
<td><span data-ttu-id="24c13-155">Use <em>controles</em>. <strong>IsAvailable</strong>( &quot; Fastforward &quot; ) e <em>Controls</em>.<strong> IsAvailable</strong>( &quot; fastReverse &quot; ).</span><span class="sxs-lookup"><span data-stu-id="24c13-155">Use <em>Controls</em>.<strong>isAvailable</strong>(&quot;FastForward&quot;) and <em>Controls</em>.<strong>isAvailable</strong>(&quot;FastReverse&quot;).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-156"><em>Player6</em>. <strong>CanSeek</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-156"><em>Player6</em>.<strong>CanSeek</strong></span></span></td>
<td><span data-ttu-id="24c13-157">Use <em>controles</em>. <strong>IsAvailable</strong> para testar se um método de busca específico pode ser executado.</span><span class="sxs-lookup"><span data-stu-id="24c13-157">Use <em>Controls</em>.<strong>isAvailable</strong> to test whether a particular seek method can be performed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-158"><em>Player6</em>. <strong>CanSeekToMarkers</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-158"><em>Player6</em>.<strong>CanSeekToMarkers</strong></span></span></td>
<td><span data-ttu-id="24c13-159">Use <em>controles</em>. <strong>IsAvailable</strong>( &quot; CurrentMarker &quot; ).</span><span class="sxs-lookup"><span data-stu-id="24c13-159">Use <em>Controls</em>.<strong>isAvailable</strong>(&quot;CurrentMarker&quot;).</span></span> <span data-ttu-id="24c13-160">Usar <em>mídia</em>. <strong>markerCount</strong> para recuperar a contagem de marcadores em um item de mídia específico.</span><span class="sxs-lookup"><span data-stu-id="24c13-160">Use <em>Media</em>.<strong>markerCount</strong> to retrieve the count of markers in a particular media item.</span></span> <span data-ttu-id="24c13-161">Use <em>controles</em>. <strong>currentMarker</strong> para especificar ou recuperar o número do marcador atual.</span><span class="sxs-lookup"><span data-stu-id="24c13-161">Use <em>Controls</em>.<strong>currentMarker</strong> to specify or retrieve the current marker number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-162"><em>Player6</em>. <strong>CaptioningID</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-162"><em>Player6</em>.<strong>CaptioningID</strong></span></span></td>
<td><span data-ttu-id="24c13-163">Use <em>ClosedCaption</em>. <strong>captioningID</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-163">Use <em>ClosedCaption</em>.<strong>captioningID</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-164"><em>Player6</em>. <strong>CCActive</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-164"><em>Player6</em>.<strong>CCActive</strong></span></span></td>
<td><span data-ttu-id="24c13-165">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-165">Not available.</span></span> <span data-ttu-id="24c13-166">Consulte <a href="closed-captioning.md">Legendagem oculta</a> para obter informações sobre como legendas ocultas foram alteradas no Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="24c13-166">See <a href="closed-captioning.md">Closed Captioning</a> for information about how closed captioning has changed in Windows Media Player.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-167"><em>Player6</em>. <strong>ChannelDescription</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-167"><em>Player6</em>.<strong>ChannelDescription</strong></span></span></td>
<td><span data-ttu-id="24c13-168">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-168">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-169"><em>Player6</em>. <strong>ChannelName</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-169"><em>Player6</em>.<strong>ChannelName</strong></span></span></td>
<td><span data-ttu-id="24c13-170">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-170">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-171"><em>Player6</em>. <strong>ChannelURL</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-171"><em>Player6</em>.<strong>ChannelURL</strong></span></span></td>
<td><span data-ttu-id="24c13-172">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-172">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-173"><em>Player6</em>. <strong>ClickToPlay</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-173"><em>Player6</em>.<strong>ClickToPlay</strong></span></span></td>
<td><span data-ttu-id="24c13-174">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-174">Not available.</span></span> <span data-ttu-id="24c13-175">Você deve fornecer controles na sua interface do usuário para iniciar a reprodução.</span><span class="sxs-lookup"><span data-stu-id="24c13-175">You should provide controls in your user interface to start playback.</span></span> <span data-ttu-id="24c13-176">Como alternativa, o usuário pode clicar com o botão direito do mouse na imagem de vídeo para abrir um menu pop-up que contém uma seleção de <strong>reproduzir/pausar</strong> se o <em>Player</em>. <strong>enableContextMenu</strong> é igual a true.</span><span class="sxs-lookup"><span data-stu-id="24c13-176">Alternatively, the user can right-click the video image to open a pop-up menu that contains a <strong>Play/Pause</strong> selection if <em>Player</em>.<strong>enableContextMenu</strong> equals true.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-177"><em>Player6</em>. <strong>ClientID</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-177"><em>Player6</em>.<strong>ClientID</strong></span></span></td>
<td><span data-ttu-id="24c13-178">Não disponível. O Windows Media Player 9 Series ou posterior permite que o usuário selecione se uma ID de Player exclusiva é transmitida aos provedores de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="24c13-178">Not available.Windows Media Player 9 Series or later allows the user to select whether a unique Player ID is transmitted to content providers.</span></span><br/> <span data-ttu-id="24c13-179">Se o usuário selecionar essa opção, o Player enviará uma ID exclusiva para o Windows Media Server.</span><span class="sxs-lookup"><span data-stu-id="24c13-179">If the user selects this option, the Player sends a unique ID to the Windows Media server.</span></span> <span data-ttu-id="24c13-180">A ID é registrada no arquivo de log do servidor, localizado no.. pasta <em>system32\logfiles</em> por padrão.</span><span class="sxs-lookup"><span data-stu-id="24c13-180">The ID is logged in the server's log file, located in the ..<em>system32\logfiles</em> folder by default.</span></span> <span data-ttu-id="24c13-181">O nome do campo de log é &quot; c-playerid &quot; .</span><span class="sxs-lookup"><span data-stu-id="24c13-181">The log field name is &quot;c-playerid&quot;.</span></span> <span data-ttu-id="24c13-182">O registro em log do servidor não está habilitado por padrão no Windows Media Services.</span><span class="sxs-lookup"><span data-stu-id="24c13-182">Server logging is not enabled by default in Windows Media Services.</span></span><br/> <span data-ttu-id="24c13-183">Se o usuário não selecionar essa opção, o servidor gerará uma ID de sessão aleatória, que é exclusiva para cada cliente para uma determinada sessão.</span><span class="sxs-lookup"><span data-stu-id="24c13-183">If the user does not select this option, the server generates a random session ID, which is unique for each client for a given session.</span></span><br/> <span data-ttu-id="24c13-184">Para obter mais informações, consulte a documentação do Windows Media Services 9 Series.</span><span class="sxs-lookup"><span data-stu-id="24c13-184">For more information, see the Windows Media Services 9 Series documentation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-185"><em>Player6</em>. <strong>CodecCount</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-185"><em>Player6</em>.<strong>CodecCount</strong></span></span></td>
<td><span data-ttu-id="24c13-186">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-186">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-187"><em>Player6</em>. <strong>COLORKEY</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-187"><em>Player6</em>.<strong>ColorKey</strong></span></span></td>
<td><span data-ttu-id="24c13-188">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-188">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-189"><em>Player6</em>. <strong>ConnectionSpeed</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-189"><em>Player6</em>.<strong>ConnectionSpeed</strong></span></span></td>
<td><span data-ttu-id="24c13-190">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-190">Not available.</span></span> <span data-ttu-id="24c13-191">Usar <em>rede</em>. taxa <strong>de bits para determinar</strong> a tarifa de bit atual.</span><span class="sxs-lookup"><span data-stu-id="24c13-191">Use <em>Network</em>.<strong>bitRate</strong> to determine the current bit rate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-192"><em>Player6</em>. <strong>ContactAddress</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-192"><em>Player6</em>.<strong>ContactAddress</strong></span></span></td>
<td><span data-ttu-id="24c13-193">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-193">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-194"><em>Player6</em>. <strong>ContactEmail</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-194"><em>Player6</em>.<strong>ContactEmail</strong></span></span></td>
<td><span data-ttu-id="24c13-195">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-195">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-196"><em>Player6</em>. <strong>ContactPhone</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-196"><em>Player6</em>.<strong>ContactPhone</strong></span></span></td>
<td><span data-ttu-id="24c13-197">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-197">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-198"><em>Player6</em>. <strong>CreationDate</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-198"><em>Player6</em>.<strong>CreationDate</strong></span></span></td>
<td><span data-ttu-id="24c13-199">Use <em>mediacollection</em>. <strong>getMediaAtom</strong>( &quot; CreationDate &quot; ) para recuperar o índice do átomo de data de criação.</span><span class="sxs-lookup"><span data-stu-id="24c13-199">Use <em>MediaCollection</em>.<strong>getMediaAtom</strong>(&quot;CreationDate&quot;) to retrieve the index of the creation date atom.</span></span> <span data-ttu-id="24c13-200">Usar <em>mídia</em>. <strong>getItemInfoByAtom</strong> para recuperar os metadados.</span><span class="sxs-lookup"><span data-stu-id="24c13-200">Use <em>Media</em>.<strong>getItemInfoByAtom</strong> to retrieve the metadata.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-201"><em>Player6</em>. <strong>CurrentAngle</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-201"><em>Player6</em>.<strong>CurrentAngle</strong></span></span></td>
<td><span data-ttu-id="24c13-202">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-202">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-203"><em>Player6</em>. <strong>CurrentAudioStream</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-203"><em>Player6</em>.<strong>CurrentAudioStream</strong></span></span></td>
<td><span data-ttu-id="24c13-204">Use <em>controles</em>. <strong>currentAudioLanguageIndex</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-204">Use <em>Controls</em>.<strong>currentAudioLanguageIndex</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-205"><em>Player6</em>. <strong>CurrentButton</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-205"><em>Player6</em>.<strong>CurrentButton</strong></span></span></td>
<td><span data-ttu-id="24c13-206">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-206">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-207"><em>Player6</em>. <strong>CurrentCCService</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-207"><em>Player6</em>.<strong>CurrentCCService</strong></span></span></td>
<td><span data-ttu-id="24c13-208">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-208">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-209"><em>Player6</em>. <strong>CurrentChapter</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-209"><em>Player6</em>.<strong>CurrentChapter</strong></span></span></td>
<td><span data-ttu-id="24c13-210">Recupere a playlist atual.</span><span class="sxs-lookup"><span data-stu-id="24c13-210">Retrieve the current playlist.</span></span> <span data-ttu-id="24c13-211">Se a playlist atual não for a mesma que a playlist retornada pelo <em>cdrom</em>. em <strong>seguida, não</strong>há um capítulo atual.</span><span class="sxs-lookup"><span data-stu-id="24c13-211">If the current playlist is not the same one as the playlist returned by <em>Cdrom</em>.<strong>playlist</strong>, then there is no current chapter.</span></span> <span data-ttu-id="24c13-212">Caso contrário, o número do capítulo atual será o índice da mídia atual na playlist atual.</span><span class="sxs-lookup"><span data-stu-id="24c13-212">Otherwise, the current chapter number is the index of the current media in the current playlist.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-213"><em>Player6</em>. <strong>CurrentDiscSide</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-213"><em>Player6</em>.<strong>CurrentDiscSide</strong></span></span></td>
<td><span data-ttu-id="24c13-214">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-214">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-215"><em>Player6</em>. <strong>CurrentDomain</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-215"><em>Player6</em>.<strong>CurrentDomain</strong></span></span></td>
<td><span data-ttu-id="24c13-216">Use o <em>DVD</em>. <strong>domínio</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-216">Use <em>DVD</em>.<strong>domain</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-217"><em>Player6</em>. <strong>CurrentMarker</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-217"><em>Player6</em>.<strong>CurrentMarker</strong></span></span></td>
<td><span data-ttu-id="24c13-218">Use <em>controles</em>. <strong>currentMarker</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-218">Use <em>Controls</em>.<strong>currentMarker</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-219"><em>Player6</em>. <strong>CurrentPosition</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-219"><em>Player6</em>.<strong>CurrentPosition</strong></span></span></td>
<td><span data-ttu-id="24c13-220">Use <em>controles</em>. <strong>CurrentPosition</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-220">Use <em>Controls</em>.<strong>currentPosition</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-221"><em>Player6</em>. <strong>CurrentSubpictureStream</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-221"><em>Player6</em>.<strong>CurrentSubpictureStream</strong></span></span></td>
<td><span data-ttu-id="24c13-222">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-222">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-223"><em>Player6</em>. <strong>CurrentTime</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-223"><em>Player6</em>.<strong>CurrentTime</strong></span></span></td>
<td><span data-ttu-id="24c13-224">Use <em>controles</em>. <strong>currentPositionTimeCode</strong>, <em>Controls</em>. <strong>currentPositionString</strong>ou <em>Controls</em>. <strong>CurrentPosition.</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-224">Use <em>Controls</em>.<strong>currentPositionTimeCode</strong>, <em>Controls</em>.<strong>currentPositionString</strong>, or <em>Controls</em>.<strong>currentPosition.</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-225"><em>Player6</em>. <strong>CurrentTitle</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-225"><em>Player6</em>.<strong>CurrentTitle</strong></span></span></td>
<td><span data-ttu-id="24c13-226">Recupere a playlist atual.</span><span class="sxs-lookup"><span data-stu-id="24c13-226">Retrieve the current playlist.</span></span> <span data-ttu-id="24c13-227">Se a playlist atual for a mesma que a playlist retornada pelo <em>cdrom</em>. na lista de <strong>reprodução</strong>, o número do título é o índice da mídia atual na playlist atual.</span><span class="sxs-lookup"><span data-stu-id="24c13-227">If the current playlist is the same one as the playlist returned by <em>Cdrom</em>.<strong>playlist</strong>, then the title number is the index of the current media in the current playlist.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-228"><em>Player6</em>. <strong>CurrentVolume</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-228"><em>Player6</em>.<strong>CurrentVolume</strong></span></span></td>
<td><span data-ttu-id="24c13-229">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-229">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-230"><em>Player6</em>. <strong>CursorType</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-230"><em>Player6</em>.<strong>CursorType</strong></span></span></td>
<td><span data-ttu-id="24c13-231">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-231">Not available.</span></span> <span data-ttu-id="24c13-232">Em vez disso, use os estilos do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="24c13-232">Use Internet Explorer styles instead.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-233"><em>Player6</em>. <strong>DefaultFrame</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-233"><em>Player6</em>.<strong>DefaultFrame</strong></span></span></td>
<td><span data-ttu-id="24c13-234">Use <em>as configurações</em>. <strong>DefaultFrame</strong>ou usar um</span><span class="sxs-lookup"><span data-stu-id="24c13-234">Use <em>Settings</em>.<strong>defaultFrame</strong>, or use a</span></span> <PARAM> <span data-ttu-id="24c13-235">atributo no <OBJECT> elemento: <pre data-space="preserve"><code><PARAM NAME=&quot;defaultFrame&quot; VALUE=&quot;right&quot;></code></pre></span><span class="sxs-lookup"><span data-stu-id="24c13-235">attribute in the <OBJECT> element: <pre data-space="preserve"><code><PARAM NAME=&quot;defaultFrame&quot; VALUE=&quot;right&quot;></code></pre></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-236"><em>Player6</em>. <strong>DisplayBackColor</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-236"><em>Player6</em>.<strong>DisplayBackColor</strong></span></span></td>
<td><span data-ttu-id="24c13-237">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-237">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-238"><em>Player6</em>. <strong>DisplayForeColor</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-238"><em>Player6</em>.<strong>DisplayForeColor</strong></span></span></td>
<td><span data-ttu-id="24c13-239">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-239">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-240"><em>Player6</em>. <strong>DisplayMode</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-240"><em>Player6</em>.<strong>DisplayMode</strong></span></span></td>
<td><span data-ttu-id="24c13-241">A posição atual pode ser recuperada em segundos desde o início como um <strong>número</strong> usando <em>controles</em>. <strong>CurrentPosition</strong>, como uma <strong>cadeia de caracteres</strong> formatada como hh: mm: SS (horas, minutos, segundos) usando <em>controles</em>. <strong>currentPositionString</strong>, ou no formato de código de tempo usando <em>controles</em>. <strong>currentPositionTimeCode</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-241">The current position can be retrieved in seconds from the beginning as a <strong>Number</strong> using <em>Controls</em>.<strong>currentPosition</strong>, as a <strong>String</strong> formatted as HH:MM:SS (hours, minutes, seconds) using <em>Controls</em>.<strong>currentPositionString</strong>, or in time code format using <em>Controls</em>.<strong>currentPositionTimeCode</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-242"><em>Player6</em>. <strong>Exibir</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-242"><em>Player6</em>.<strong>DisplaySize</strong></span></span></td>
<td><span data-ttu-id="24c13-243">A exibição padrão é redimensionada automaticamente para se ajustar à mídia.</span><span class="sxs-lookup"><span data-stu-id="24c13-243">The default display automatically resizes to fit the media.</span></span> <span data-ttu-id="24c13-244">Você pode definir as propriedades Height e Width na <OBJECT> marca ou no script.</span><span class="sxs-lookup"><span data-stu-id="24c13-244">You can set the height and width properties in the <OBJECT> tag, or in script.</span></span> <span data-ttu-id="24c13-245">Use o <em>Player</em>. <strong>tela inteira</strong> para alternar para o modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="24c13-245">Use <em>Player</em>.<strong>fullScreen</strong> to switch to full-screen mode.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-246"><em>Player6</em>. <strong>Duração</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-246"><em>Player6</em>.<strong>Duration</strong></span></span></td>
<td><span data-ttu-id="24c13-247">Usar <em>mídia</em>. <strong>duração</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-247">Use <em>Media</em>.<strong>duration</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-248"><em>Player6</em>. <strong>DVD</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-248"><em>Player6</em>.<strong>DVD</strong></span></span></td>
<td><span data-ttu-id="24c13-249">Use o <em>Player</em>. <strong>DVD</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-249">Use <em>Player</em>.<strong>DVD</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-250"><em>Player6</em>. <strong>EnableContextMenu</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-250"><em>Player6</em>.<strong>EnableContextMenu</strong></span></span></td>
<td><span data-ttu-id="24c13-251">Use o <em>Player</em>. <strong>enableContextMenu</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-251">Use <em>Player</em>.<strong>enableContextMenu</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-252"><em>Player6</em>. <strong>Habilitado</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-252"><em>Player6</em>.<strong>Enabled</strong></span></span></td>
<td><span data-ttu-id="24c13-253">Use o <em>Player</em>. <strong>habilitado</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-253">Use <em>Player</em>.<strong>enabled</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-254"><em>Player6</em>. <strong>EnableFullScreenControls</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-254"><em>Player6</em>.<strong>EnableFullScreenControls</strong></span></span></td>
<td><span data-ttu-id="24c13-255">Ao usar o Windows Media Player 9 Series ou posterior, os controles de tela inteira são habilitados automaticamente, a menos que o <em>Player</em>. <strong></strong>  =  UIMODE &quot; nenhum &quot; .</span><span class="sxs-lookup"><span data-stu-id="24c13-255">When using Windows Media Player 9 Series or later, full-screen controls are enabled automatically unless <em>Player</em>.<strong>uiMode</strong> = &quot;none&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-256"><em>Player6</em>. <strong>EnablePositionControls</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-256"><em>Player6</em>.<strong>EnablePositionControls</strong></span></span></td>
<td><span data-ttu-id="24c13-257">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-257">Not available.</span></span> <span data-ttu-id="24c13-258">Você pode fornecer controles personalizados ou usar o <em>Player</em>. <strong>UIMODE</strong> para escolher uma configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="24c13-258">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-259"><em>Player6</em>. <strong>EnableTracker</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-259"><em>Player6</em>.<strong>EnableTracker</strong></span></span></td>
<td><span data-ttu-id="24c13-260">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-260">Not available.</span></span> <span data-ttu-id="24c13-261">Você pode fornecer um controle personalizado ou usar o <em>Player</em>. <strong>UIMODE</strong> para escolher uma configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="24c13-261">You can provide a custom control or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-262"><em>Player6</em>. <strong>EntryCount</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-262"><em>Player6</em>.<strong>EntryCount</strong></span></span></td>
<td><span data-ttu-id="24c13-263">Use a <em>lista de reprodução</em>. <strong>contagem</strong> de</span><span class="sxs-lookup"><span data-stu-id="24c13-263">Use <em>Playlist</em>.<strong>count</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-264"><em>Player6</em>. <strong>ErrorCode</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-264"><em>Player6</em>.<strong>ErrorCode</strong></span></span></td>
<td><span data-ttu-id="24c13-265">Use <em>ErrorItem</em>. <strong>ErrorCode</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-265">Use <em>ErrorItem</em>.<strong>errorCode</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-266"><em>Player6</em>. <strong>ErrorCorrection</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-266"><em>Player6</em>.<strong>ErrorCorrection</strong></span></span></td>
<td><span data-ttu-id="24c13-267">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-267">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-268"><em>Player6</em>. <strong>ErrorDescription</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-268"><em>Player6</em>.<strong>ErrorDescription</strong></span></span></td>
<td><span data-ttu-id="24c13-269">Use <em>ErrorItem</em>. <strong>errorDescription</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-269">Use <em>ErrorItem</em>.<strong>errorDescription</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-270"><em>Player6</em>. <strong>Nome do arquivo</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-270"><em>Player6</em>.<strong>FileName</strong></span></span></td>
<td><span data-ttu-id="24c13-271">Use o <em>Player</em>. <strong>URL</strong> ou <em>Player</em>. <strong>currentMedia</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-271">Use <em>Player</em>.<strong>URL</strong> or <em>Player</em>.<strong>currentMedia</strong>.</span></span> <span data-ttu-id="24c13-272">Use <em>controles</em>. <strong>currentItem</strong> ao trabalhar em uma playlist.</span><span class="sxs-lookup"><span data-stu-id="24c13-272">Use <em>Controls</em>.<strong>currentItem</strong> when working within a playlist.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-273"><em>Player6</em>. <strong>FramesPerSecond</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-273"><em>Player6</em>.<strong>FramesPerSecond</strong></span></span></td>
<td><span data-ttu-id="24c13-274">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-274">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-275"><em>Player6</em>. <strong>HasError</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-275"><em>Player6</em>.<strong>HasError</strong></span></span></td>
<td><span data-ttu-id="24c13-276"><em>Erro</em>de uso. <strong>errorCount</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-276">Use <em>Error</em>.<strong>errorCount</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-277"><em>Player6</em>. <strong>HasMultipleItems</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-277"><em>Player6</em>.<strong>HasMultipleItems</strong></span></span></td>
<td><span data-ttu-id="24c13-278">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-278">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-279"><em>Player6</em>. <strong>ImageSourceHeight</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-279"><em>Player6</em>.<strong>ImageSourceHeight</strong></span></span></td>
<td><span data-ttu-id="24c13-280">Usar <em>mídia</em>. <strong>imageSourceHeight</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-280">Use <em>Media</em>.<strong>imageSourceHeight</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-281"><em>Player6</em>. <strong>ImageSourceWidth</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-281"><em>Player6</em>.<strong>ImageSourceWidth</strong></span></span></td>
<td><span data-ttu-id="24c13-282">Usar <em>mídia</em>. <strong>imageSourceWidth</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-282">Use <em>Media</em>.<strong>imageSourceWidth</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-283"><em>Player6</em>. <strong>InvokeURLs</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-283"><em>Player6</em>.<strong>InvokeURLs</strong></span></span></td>
<td><span data-ttu-id="24c13-284">Use <em>as configurações</em>. <strong>invokeURLs</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-284">Use <em>Settings</em>.<strong>invokeURLs</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-285"><em>Player6</em>. <strong>Isbroadcast</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-285"><em>Player6</em>.<strong>IsBroadcast</strong></span></span></td>
<td><span data-ttu-id="24c13-286">Usar <em>rede</em>. <strong>sourceProtocol</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-286">Use <em>Network</em>.<strong>sourceProtocol</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-287"><em>Player6</em>. <strong>IsDurationValid</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-287"><em>Player6</em>.<strong>IsDurationValid</strong></span></span></td>
<td><span data-ttu-id="24c13-288">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-288">Not available.</span></span> <span data-ttu-id="24c13-289"><em>Mídia</em>. <strong>Duration</strong> contém um valor válido quando usado com o objeto de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="24c13-289"><em>Media</em>.<strong>duration</strong> contains a valid value when used with the current media object.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-290"><em>Player6</em>. <strong>Idioma</strong> do</span><span class="sxs-lookup"><span data-stu-id="24c13-290"><em>Player6</em>.<strong>Language</strong></span></span></td>
<td><span data-ttu-id="24c13-291">Use <em>controles</em>. <strong>currentAudioLanguage</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-291">Use <em>Controls</em>.<strong>currentAudioLanguage</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-292"><em>Player6</em>. <strong>LostPackets</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-292"><em>Player6</em>.<strong>LostPackets</strong></span></span></td>
<td><span data-ttu-id="24c13-293">Usar <em>rede</em>. <strong>lostPackets</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-293">Use <em>Network</em>.<strong>lostPackets</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-294"><em>Player6</em>. <strong>MarkerCount</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-294"><em>Player6</em>.<strong>MarkerCount</strong></span></span></td>
<td><span data-ttu-id="24c13-295">Usar <em>mídia</em>. <strong>markerCount</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-295">Use <em>Media</em>.<strong>markerCount</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-296"><em>Player6</em>. <strong>Sem áudio</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-296"><em>Player6</em>.<strong>Mute</strong></span></span></td>
<td><span data-ttu-id="24c13-297">Use <em>as configurações</em>. <strong>sem áudio</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-297">Use <em>Settings</em>.<strong>mute</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-298"><em>Player6</em>. <strong>OpenState</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-298"><em>Player6</em>.<strong>OpenState</strong></span></span></td>
<td><span data-ttu-id="24c13-299">Use o <em>Player</em>. <strong>OpenState</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-299">Use <em>Player</em>.<strong>openState</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-300"><em>Player6</em>. <strong>PlayCount</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-300"><em>Player6</em>.<strong>PlayCount</strong></span></span></td>
<td><span data-ttu-id="24c13-301">Use <em>as configurações</em>. <strong>playCount</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-301">Use <em>Settings</em>.<strong>playCount</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-302"><em>Player6</em>. <strong>PlayState</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-302"><em>Player6</em>.<strong>PlayState</strong></span></span></td>
<td><span data-ttu-id="24c13-303">Use o <em>Player</em>. <strong>PlayState</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-303">Use <em>Player</em>.<strong>playState</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-304"><em>Player6</em>. <strong>Modo de exibição de visualização</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-304"><em>Player6</em>.<strong>PreviewMode</strong></span></span></td>
<td><span data-ttu-id="24c13-305">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-305">Not available.</span></span> <span data-ttu-id="24c13-306">Use uma estrutura de loop de script com um temporizador HTML para duplicar essa funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="24c13-306">Use a script loop structure with an HTML timer to duplicate this functionality.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-307"><em>Player6</em>. <strong>Taxa</strong> de</span><span class="sxs-lookup"><span data-stu-id="24c13-307"><em>Player6</em>.<strong>Rate</strong></span></span></td>
<td><span data-ttu-id="24c13-308">Use <em>as configurações</em>. <strong>taxa</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-308">Use <em>Settings</em>.<strong>rate</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-309"><em>Player6</em>. <strong>ReadyState</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-309"><em>Player6</em>.<strong>ReadyState</strong></span></span></td>
<td><span data-ttu-id="24c13-310">Use o <em>Player</em>. <strong>OpenState</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-310">Use <em>Player</em>.<strong>openState</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-311"><em>Player6</em>. <strong>ReceivedPackets</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-311"><em>Player6</em>.<strong>ReceivedPackets</strong></span></span></td>
<td><span data-ttu-id="24c13-312">Usar <em>rede</em>. <strong>receivedPackets</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-312">Use <em>Network</em>.<strong>receivedPackets</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-313"><em>Player6</em>. <strong>ReceptionQuality</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-313"><em>Player6</em>.<strong>ReceptionQuality</strong></span></span></td>
<td><span data-ttu-id="24c13-314">Usar <em>rede</em>. <strong>receptionQuality</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-314">Use <em>Network</em>.<strong>receptionQuality</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-315"><em>Player6</em>. <strong>RecoveredPackets</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-315"><em>Player6</em>.<strong>RecoveredPackets</strong></span></span></td>
<td><span data-ttu-id="24c13-316">Usar <em>rede</em>. <strong>recoveredPackets</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-316">Use <em>Network</em>.<strong>recoveredPackets</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-317"><em>Player6</em>. <strong>Raiz</strong> do</span><span class="sxs-lookup"><span data-stu-id="24c13-317"><em>Player6</em>.<strong>Root</strong></span></span></td>
<td><span data-ttu-id="24c13-318">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-318">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-319"><em>Player6</em>. <strong>SAMIFileName</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-319"><em>Player6</em>.<strong>SAMIFileName</strong></span></span></td>
<td><span data-ttu-id="24c13-320">Use <em>ClosedCaption</em>. <strong>SAMIFileName</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-320">Use <em>ClosedCaption</em>.<strong>SAMIFileName</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-321"><em>Player6</em>. <strong>SAMILang</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-321"><em>Player6</em>.<strong>SAMILang</strong></span></span></td>
<td><span data-ttu-id="24c13-322">Use <em>ClosedCaption</em>. <strong>SAMILang</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-322">Use <em>ClosedCaption</em>.<strong>SAMILang</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-323"><em>Player6</em>. <strong>Samistyle</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-323"><em>Player6</em>.<strong>SAMIStyle</strong></span></span></td>
<td><span data-ttu-id="24c13-324">Use <em>ClosedCaption</em>. <strong>Samistyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-324">Use <em>ClosedCaption</em>.<strong>SAMIStyle</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-325"><em>Player6</em>. <strong>SelectionEnd</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-325"><em>Player6</em>.<strong>SelectionEnd</strong></span></span></td>
<td><span data-ttu-id="24c13-326">Usar <em>mídia</em>. <strong>duração</strong> para determinar o comprimento de um objeto de <strong>mídia</strong> .</span><span class="sxs-lookup"><span data-stu-id="24c13-326">Use <em>Media</em>.<strong>duration</strong> to determine the length of a <strong>Media</strong> object.</span></span> <span data-ttu-id="24c13-327">Use um marcador com <em>controles</em>. <strong>currentMarker</strong> para especificar uma posição de extremidade personalizada.</span><span class="sxs-lookup"><span data-stu-id="24c13-327">Use a marker with <em>Controls</em>.<strong>currentMarker</strong> to specify a custom end position.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-328"><em>Player6</em>. <strong>SelectionStart</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-328"><em>Player6</em>.<strong>SelectionStart</strong></span></span></td>
<td><span data-ttu-id="24c13-329">Use <em>controles</em>. <strong>CurrentPosition</strong> para iniciar a reprodução de uma determinada posição ou usar um marcador com <em>controles</em>. <strong>currentMarker</strong> para especificar uma posição de início personalizada.</span><span class="sxs-lookup"><span data-stu-id="24c13-329">Use <em>Controls</em>.<strong>currentPosition</strong> to start playback from a particular position or use a marker with <em>Controls</em>.<strong>currentMarker</strong> to specify a custom start position.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-330"><em>Player6</em>. <strong>SendErrorEvents</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-330"><em>Player6</em>.<strong>SendErrorEvents</strong></span></span></td>
<td><span data-ttu-id="24c13-331">Os erros são enfileirados.</span><span class="sxs-lookup"><span data-stu-id="24c13-331">Errors are queued.</span></span> <span data-ttu-id="24c13-332">Use o objeto <strong>Error</strong> e o objeto <strong>ErrorItem</strong> para recuperar informações de erro.</span><span class="sxs-lookup"><span data-stu-id="24c13-332">Use the <strong>Error</strong> object and the <strong>ErrorItem</strong> object to retrieve error information.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-333"><em>Player6</em>. <strong>SendKeyboardEvents</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-333"><em>Player6</em>.<strong>SendKeyboardEvents</strong></span></span></td>
<td><span data-ttu-id="24c13-334">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-334">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-335"><em>Player6</em>. <strong>SendMouseClickEvents</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-335"><em>Player6</em>.<strong>SendMouseClickEvents</strong></span></span></td>
<td><span data-ttu-id="24c13-336">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-336">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-337"><em>Player6</em>. <strong>SendMouseMoveEvents</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-337"><em>Player6</em>.<strong>SendMouseMoveEvents</strong></span></span></td>
<td><span data-ttu-id="24c13-338">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-338">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-339"><em>Player6</em>. <strong>SendOpenStateChangeEvents</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-339"><em>Player6</em>.<strong>SendOpenStateChangeEvents</strong></span></span></td>
<td><span data-ttu-id="24c13-340">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-340">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-341"><em>Player6</em>. <strong>SendPlayStateChangeEvents</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-341"><em>Player6</em>.<strong>SendPlayStateChangeEvents</strong></span></span></td>
<td><span data-ttu-id="24c13-342">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-342">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-343"><em>Player6</em>. <strong>SendWarningEvents</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-343"><em>Player6</em>.<strong>SendWarningEvents</strong></span></span></td>
<td><span data-ttu-id="24c13-344">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-344">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-345"><em>Player6</em>. <strong>ShowAudioControls</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-345"><em>Player6</em>.<strong>ShowAudioControls</strong></span></span></td>
<td><span data-ttu-id="24c13-346">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-346">Not available.</span></span> <span data-ttu-id="24c13-347">Você pode fornecer controles personalizados ou usar o <em>Player</em>. <strong>UIMODE</strong> para escolher uma configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="24c13-347">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-348"><em>Player6</em>. <strong>Conlegendas</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-348"><em>Player6</em>.<strong>ShowCaptioning</strong></span></span></td>
<td><span data-ttu-id="24c13-349">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-349">Not available.</span></span> <span data-ttu-id="24c13-350">Você pode fornecer uma exibição personalizada de legenda oculta.</span><span class="sxs-lookup"><span data-stu-id="24c13-350">You can provide a custom closed caption display.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-351"><em>Player6</em>. <strong>Percontroles</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-351"><em>Player6</em>.<strong>ShowControls</strong></span></span></td>
<td><span data-ttu-id="24c13-352">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-352">Not available.</span></span> <span data-ttu-id="24c13-353">Você pode fornecer controles personalizados ou usar o <em>Player</em>. <strong>UIMODE</strong> para escolher uma configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="24c13-353">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-354"><em>Player6</em>. <strong>Exibir</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-354"><em>Player6</em>.<strong>ShowDisplay</strong></span></span></td>
<td><span data-ttu-id="24c13-355">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-355">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-356"><em>Player6</em>. <strong>ShowGotoBar</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-356"><em>Player6</em>.<strong>ShowGotoBar</strong></span></span></td>
<td><span data-ttu-id="24c13-357">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-357">Not available.</span></span> <span data-ttu-id="24c13-358">Você pode fornecer funcionalidade personalizada usando o objeto de mídia</span><span class="sxs-lookup"><span data-stu-id="24c13-358">You can provide custom functionality using the Media object</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-359"><em>Player6</em>. <strong>ShowPositionControls</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-359"><em>Player6</em>.<strong>ShowPositionControls</strong></span></span></td>
<td><span data-ttu-id="24c13-360">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-360">Not available.</span></span> <span data-ttu-id="24c13-361">Você pode fornecer controles personalizados ou usar o <em>Player</em>. <strong>UIMODE</strong> para escolher uma configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="24c13-361">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-362"><em>Player6</em>. <strong>Defaultstatusbar</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-362"><em>Player6</em>.<strong>ShowStatusBar</strong></span></span></td>
<td><span data-ttu-id="24c13-363">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-363">Not available.</span></span> <span data-ttu-id="24c13-364">Você pode fornecer controles personalizados ou usar o <em>Player</em>. <strong>UIMODE</strong> para escolher uma configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="24c13-364">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-365"><em>Player6</em>. <strong>Controle</strong> de</span><span class="sxs-lookup"><span data-stu-id="24c13-365"><em>Player6</em>.<strong>ShowTracker</strong></span></span></td>
<td><span data-ttu-id="24c13-366">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-366">Not available.</span></span> <span data-ttu-id="24c13-367">Você pode fornecer controles personalizados ou usar o <em>Player</em>. <strong>UIMODE</strong> para escolher uma configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="24c13-367">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-368"><em>Player6</em>. <strong>Funcionalidade sourcelink</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-368"><em>Player6</em>.<strong>SourceLink</strong></span></span></td>
<td><span data-ttu-id="24c13-369">Usar <em>mídia</em>. <strong>sourceURL</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-369">Use <em>Media</em>.<strong>sourceURL</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-370"><em>Player6</em>. <strong>SourceProtocol</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-370"><em>Player6</em>.<strong>SourceProtocol</strong></span></span></td>
<td><span data-ttu-id="24c13-371">Usar <em>rede</em>. <strong>sourceProtocol</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-371">Use <em>Network</em>.<strong>sourceProtocol</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-372"><em>Player6</em>. <strong>StreamCount</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-372"><em>Player6</em>.<strong>StreamCount</strong></span></span></td>
<td><span data-ttu-id="24c13-373">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-373">Not available.</span></span> <span data-ttu-id="24c13-374">Use <em>controles</em>. <strong>audioLanguageCount</strong> para recuperar o número de fluxos de idioma de áudio.</span><span class="sxs-lookup"><span data-stu-id="24c13-374">Use <em>Controls</em>.<strong>audioLanguageCount</strong> to retrieve the number of audio language streams.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-375"><em>Player6</em>. <strong>Subimagem</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-375"><em>Player6</em>.<strong>SubpictureOn</strong></span></span></td>
<td><span data-ttu-id="24c13-376">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-376">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-377"><em>Player6</em>. <strong>SubpictureStreamsAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-377"><em>Player6</em>.<strong>SubpictureStreamsAvailable</strong></span></span></td>
<td><span data-ttu-id="24c13-378">Não disponível</span><span class="sxs-lookup"><span data-stu-id="24c13-378">Not available</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-379"><em>Player6</em>. <strong>TitlesAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-379"><em>Player6</em>.<strong>TitlesAvailable</strong></span></span></td>
<td><span data-ttu-id="24c13-380">Use o seguinte:<code>Player.Cdrom.playlist.count - 1</code></span><span class="sxs-lookup"><span data-stu-id="24c13-380">Use the following:<code>Player.Cdrom.playlist.count - 1</code></span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-381"><em>Player6</em>. <strong>TotalTitleTime</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-381"><em>Player6</em>.<strong>TotalTitleTime</strong></span></span></td>
<td><span data-ttu-id="24c13-382">Use <em>currentMedia</em>. <strong>duração</strong> ou <em>currentMedia</em>. <strong>durationstring</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-382">Use <em>currentMedia</em>.<strong>duration</strong> or <em>currentMedia</em>.<strong>durationString</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-383"><em>Player6</em>. <strong>TransparentAtStart</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-383"><em>Player6</em>.<strong>TransparentAtStart</strong></span></span></td>
<td><span data-ttu-id="24c13-384">Use o script para especificar os valores de altura e largura para tornar o Player visível ou invisível.</span><span class="sxs-lookup"><span data-stu-id="24c13-384">Use script to specify the height and width values to make the player visible or invisible.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-385"><em>Player6</em>. <strong>UniqueId</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-385"><em>Player6</em>.<strong>UniqueID</strong></span></span></td>
<td><span data-ttu-id="24c13-386">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-386">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-387"><em>Player6</em>. <strong>VideoBorder3D</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-387"><em>Player6</em>.<strong>VideoBorder3D</strong></span></span></td>
<td><span data-ttu-id="24c13-388">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-388">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-389"><em>Player6</em>. <strong>VideoBorderColor</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-389"><em>Player6</em>.<strong>VideoBorderColor</strong></span></span></td>
<td><span data-ttu-id="24c13-390">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-390">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-391"><em>Player6</em>. <strong>VideoBorderWidth</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-391"><em>Player6</em>.<strong>VideoBorderWidth</strong></span></span></td>
<td><span data-ttu-id="24c13-392">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-392">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-393"><em>Player6</em>. <strong>Volume</strong> do</span><span class="sxs-lookup"><span data-stu-id="24c13-393"><em>Player6</em>.<strong>Volume</strong></span></span></td>
<td><span data-ttu-id="24c13-394">Use <em>as configurações</em>. <strong>Volume</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-394">Use <em>Settings</em>.<strong>Volume</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-395"><em>Player6</em>. <strong>VolumesAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-395"><em>Player6</em>.<strong>VolumesAvailable</strong></span></span></td>
<td><span data-ttu-id="24c13-396">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-396">Not available.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="24c13-397">A tabela a seguir compara os métodos de modelo de objeto do Windows Media Player versão 6,4 com o modelo de objeto do Windows Media Player 7 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="24c13-397">The following table compares the Windows Media Player version 6.4 object model methods with the Windows Media Player 7 or later object model.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="24c13-398">Método do Windows Media Player 6,4</span><span class="sxs-lookup"><span data-stu-id="24c13-398">Windows Media Player 6.4 method</span></span></th>
<th><span data-ttu-id="24c13-399">Windows Media Player 7 ou posterior equivalente</span><span class="sxs-lookup"><span data-stu-id="24c13-399">Windows Media Player 7 or later equivalent</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="24c13-400"><em>Player6</em>. <strong>AboutBox</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-400"><em>Player6</em>.<strong>AboutBox</strong></span></span></td>
<td><span data-ttu-id="24c13-401">Use o <em>Player</em>. <strong>versionInfo</strong> para recuperar a versão do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="24c13-401">Use <em>Player</em>.<strong>versionInfo</strong> to retrieve the version of Windows Media Player.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-402"><em>Player6</em>. <strong>BackwardScan</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-402"><em>Player6</em>.<strong>BackwardScan</strong></span></span></td>
<td><span data-ttu-id="24c13-403">Use <em>as configurações</em>. <strong>taxa</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-403">Use <em>Settings</em>.<strong>rate</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-404"><em>Player6</em>. <strong>ButtonActivate</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-404"><em>Player6</em>.<strong>ButtonActivate</strong></span></span></td>
<td><span data-ttu-id="24c13-405">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-405">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-406"><em>Player6</em>. <strong>ButtonSelectAndActivate</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-406"><em>Player6</em>.<strong>ButtonSelectAndActivate</strong></span></span></td>
<td><span data-ttu-id="24c13-407">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-407">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-408"><em>Player6</em>. <strong>Cancelar</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-408"><em>Player6</em>.<strong>Cancel</strong></span></span></td>
<td><span data-ttu-id="24c13-409">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-409">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-410"><em>Player6</em>. <strong>ChapterPlay</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-410"><em>Player6</em>.<strong>ChapterPlay</strong></span></span></td>
<td><span data-ttu-id="24c13-411">Se já estiver executando a playlist de título especificada, recupere o capítulo desejado como um objeto de mídia usando a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="24c13-411">If already playing the specified title playlist, retrieve the desired chapter as a media object using the following syntax:</span></span>
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
<span data-ttu-id="24c13-412">Em seguida, especifique <em>Player</em>. <strong>currentMedia</strong> usando o objeto de mídia retornado.</span><span class="sxs-lookup"><span data-stu-id="24c13-412">Then, specify <em>Player</em>.<strong>currentMedia</strong> using the media object returned.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-413"><em>Player6</em>. <strong>ChapterPlayAutoStop</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-413"><em>Player6</em>.<strong>ChapterPlayAutoStop</strong></span></span></td>
<td><span data-ttu-id="24c13-414">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-414">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-415"><em>Player6</em>. <strong>ChapterSearch</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-415"><em>Player6</em>.<strong>ChapterSearch</strong></span></span></td>
<td><span data-ttu-id="24c13-416">Se já estiver executando a playlist de título especificada, recupere o capítulo desejado como um objeto de mídia usando a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="24c13-416">If already playing the specified title playlist, retrieve the desired chapter as a media object using the following syntax:</span></span>
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
<span data-ttu-id="24c13-417">Em seguida, especifique <em>Player</em>. <strong>currentMedia</strong> usando o objeto de mídia retornado.</span><span class="sxs-lookup"><span data-stu-id="24c13-417">Then, specify <em>Player</em>.<strong>currentMedia</strong> using the media object returned.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-418"><em>Player6</em>. <strong>Fastforward</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-418"><em>Player6</em>.<strong>FastForward</strong></span></span></td>
<td><span data-ttu-id="24c13-419">Use <em>controles</em>. <strong>Fastforward</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-419">Use <em>Controls</em>.<strong>fastForward</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-420"><em>Player6</em>. <strong>FastReverse</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-420"><em>Player6</em>.<strong>FastReverse</strong></span></span></td>
<td><span data-ttu-id="24c13-421">Use <em>controles</em>. <strong>fastReverse</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-421">Use <em>Controls</em>.<strong>fastReverse</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-422"><em>Player6</em>. <strong>ForwardScan</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-422"><em>Player6</em>.<strong>ForwardScan</strong></span></span></td>
<td><span data-ttu-id="24c13-423">Use <em>as configurações</em>. <strong>taxa</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-423">Use <em>Settings</em>.<strong>rate</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-424"><em>Player6</em>. <strong>GetAllGPRMs</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-424"><em>Player6</em>.<strong>GetAllGPRMs</strong></span></span></td>
<td><span data-ttu-id="24c13-425">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-425">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-426"><em>Player6</em>. <strong>GetAllSPRMs</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-426"><em>Player6</em>.<strong>GetAllSPRMs</strong></span></span></td>
<td><span data-ttu-id="24c13-427">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-427">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-428"><em>Player6</em>. <strong>GetAudioLanguage</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-428"><em>Player6</em>.<strong>GetAudioLanguage</strong></span></span></td>
<td><span data-ttu-id="24c13-429">Use <em>controles</em>. <strong>currentAudioLanguage</strong> para recuperar o LCID do idioma de áudio atual.</span><span class="sxs-lookup"><span data-stu-id="24c13-429">Use <em>Controls</em>.<strong>currentAudioLanguage</strong> to retrieve the LCID of the current audio language.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-430"><em>Player6</em>. <strong>GetCodecDescription</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-430"><em>Player6</em>.<strong>GetCodecDescription</strong></span></span></td>
<td><span data-ttu-id="24c13-431">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-431">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-432"><em>Player6</em>. <strong>GetCodecInstalled</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-432"><em>Player6</em>.<strong>GetCodecInstalled</strong></span></span></td>
<td><span data-ttu-id="24c13-433">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-433">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-434"><em>Player6</em>. <strong>GetCodecURL</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-434"><em>Player6</em>.<strong>GetCodecURL</strong></span></span></td>
<td><span data-ttu-id="24c13-435">Use <em>ErrorItem</em>. <strong>customUrl</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-435">Use <em>ErrorItem</em>.<strong>customUrl</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-436"><em>Player6</em>. <strong>GetCurrentEntry</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-436"><em>Player6</em>.<strong>GetCurrentEntry</strong></span></span></td>
<td><span data-ttu-id="24c13-437">Use o script para executar um loop na playlist atual.</span><span class="sxs-lookup"><span data-stu-id="24c13-437">Use script to loop through the current playlist.</span></span> <span data-ttu-id="24c13-438">Usar <em>mídia</em>. <strong>isidêntico</strong> para comparar cada entrada da lista de reprodução com o <em>Player</em>. objeto <strong>currentMedia</strong> .</span><span class="sxs-lookup"><span data-stu-id="24c13-438">Use <em>Media</em>.<strong>isIdentical</strong> to compare each entry in the playlist to the <em>Player</em>.<strong>currentMedia</strong> object.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-439"><em>Player6</em>. <strong></strong> Getmarkname</span><span class="sxs-lookup"><span data-stu-id="24c13-439"><em>Player6</em>.<strong>GetMarkerName</strong></span></span></td>
<td><span data-ttu-id="24c13-440">Usar <em>mídia</em>. <strong>Getmarcadorname</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-440">Use <em>Media</em>.<strong>getMarkerName</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-441"><em>Player6</em>. <strong>Getmarcadortime</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-441"><em>Player6</em>.<strong>GetMarkerTime</strong></span></span></td>
<td><span data-ttu-id="24c13-442">Usar <em>mídia</em>. <strong>Getmarcadortime</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-442">Use <em>Media</em>.<strong>getMarkerTime</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-443"><em>Player6</em>. <strong>GetMediaInfoString</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-443"><em>Player6</em>.<strong>GetMediaInfoString</strong></span></span></td>
<td><span data-ttu-id="24c13-444">Usar <em>mídia</em>. <strong>getItemInfo</strong>, <em>mídia</em>. <strong>getItemInfoByAtom</strong>e seus métodos associados para recuperar metadados.</span><span class="sxs-lookup"><span data-stu-id="24c13-444">Use <em>Media</em>.<strong>getItemInfo</strong>, <em>Media</em>.<strong>getItemInfoByAtom</strong>, and their associated methods to retrieve metadata.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-445"><em>Player6</em>. <strong>GetMediaParameter</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-445"><em>Player6</em>.<strong>GetMediaParameter</strong></span></span></td>
<td><span data-ttu-id="24c13-446">Use a <em>lista de reprodução</em>. <strong>Item</strong> para recuperar um item de mídia.</span><span class="sxs-lookup"><span data-stu-id="24c13-446">Use <em>Playlist</em>.<strong>item</strong> to retrieve a media item.</span></span> <span data-ttu-id="24c13-447">Em seguida, use a <em>mídia</em>. <strong>getItemInfo</strong> para recuperar a cadeia de caracteres do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="24c13-447">Then use <em>Media</em>.<strong>getItemInfo</strong> to retrieve the parameter string.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-448"><em>Player6</em>. <strong>GetMediaParameterName</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-448"><em>Player6</em>.<strong>GetMediaParameterName</strong></span></span></td>
<td><span data-ttu-id="24c13-449">Use a <em>lista de reprodução</em>. <strong>Item</strong> para recuperar um item de mídia.</span><span class="sxs-lookup"><span data-stu-id="24c13-449">Use <em>Playlist</em>.<strong>item</strong> to retrieve a media item.</span></span> <span data-ttu-id="24c13-450">Em seguida, use a <em>mídia</em>. <strong>GetAttributeName</strong> para recuperar a cadeia de caracteres do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="24c13-450">Then use <em>Media</em>.<strong>getAttributeName</strong> to retrieve the parameter string.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-451"><em>Player6</em>. <strong>GetMoreInfoURL</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-451"><em>Player6</em>.<strong>GetMoreInfoURL</strong></span></span></td>
<td><span data-ttu-id="24c13-452">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-452">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-453"><em>Player6</em>. <strong>GetNumberOfChapters</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-453"><em>Player6</em>.<strong>GetNumberOfChapters</strong></span></span></td>
<td><span data-ttu-id="24c13-454">Se um título estiver sendo executado no momento, use <em>currentPlaylist</em>. <strong>contagem</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-454">If a title is currently playing, use <em>currentPlaylist</em>.<strong>count</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-455"><em>Player6</em>. <strong>GetStream</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-455"><em>Player6</em>.<strong>GetStreamGroup</strong></span></span></td>
<td><span data-ttu-id="24c13-456">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-456">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-457"><em>Player6</em>. <strong>Getstreamname</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-457"><em>Player6</em>.<strong>GetStreamName</strong></span></span></td>
<td><span data-ttu-id="24c13-458">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-458">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-459"><em>Player6</em>. <strong>GetStreamSelected</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-459"><em>Player6</em>.<strong>GetStreamSelected</strong></span></span></td>
<td><span data-ttu-id="24c13-460">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-460">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-461"><em>Player6</em>. <strong>GetSubpictureLanguage</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-461"><em>Player6</em>.<strong>GetSubpictureLanguage</strong></span></span></td>
<td><span data-ttu-id="24c13-462">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-462">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-463"><em>Player6</em>. <strong>Grupo</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-463"><em>Player6</em>.<strong>GoUp</strong></span></span></td>
<td><span data-ttu-id="24c13-464">Use o <em>DVD</em>. <strong>voltar</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-464">Use <em>DVD</em>.<strong>back</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-465"><em>Player6</em>. <strong>IsSoundCardEnabled</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-465"><em>Player6</em>.<strong>IsSoundCardEnabled</strong></span></span></td>
<td><span data-ttu-id="24c13-466">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-466">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-467"><em>Player6</em>. <strong>LeftButtonSelect</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-467"><em>Player6</em>.<strong>LeftButtonSelect</strong></span></span></td>
<td><span data-ttu-id="24c13-468">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-468">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-469"><em>Player6</em>. <strong>LowerButtonSelect</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-469"><em>Player6</em>.<strong>LowerButtonSelect</strong></span></span></td>
<td><span data-ttu-id="24c13-470">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-470">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-471"><em>Player6</em>. <strong>MenuCall</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-471"><em>Player6</em>.<strong>MenuCall</strong></span></span></td>
<td><span data-ttu-id="24c13-472">Use o <em>DVD</em>. <strong>titleMenu</strong> ou <em>DVD</em>. <strong>topMenu</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-472">Use <em>DVD</em>.<strong>titleMenu</strong> or <em>DVD</em>.<strong>topMenu</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-473"><em>Player6</em>. <strong>Avançar</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-473"><em>Player6</em>.<strong>Next</strong></span></span></td>
<td><span data-ttu-id="24c13-474">Use <em>controles</em>. <strong>em seguida</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-474">Use <em>Controls</em>.<strong>next</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-475"><em>Player6</em>. <strong>NextPGSearch</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-475"><em>Player6</em>.<strong>NextPGSearch</strong></span></span></td>
<td><span data-ttu-id="24c13-476">Use <em>controles</em>. <strong>em seguida</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-476">Use <em>Controls</em>.<strong>next</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-477"><em>Player6</em>. <strong>Abrir</strong> o</span><span class="sxs-lookup"><span data-stu-id="24c13-477"><em>Player6</em>.<strong>Open</strong></span></span></td>
<td><span data-ttu-id="24c13-478">Use o <em>Player</em>. <strong>URL</strong> ou <em>Player</em>. <strong>currentMedia</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-478">Use <em>Player</em>.<strong>URL</strong> or <em>Player</em>.<strong>currentMedia</strong>.</span></span> <span data-ttu-id="24c13-479">Os arquivos sempre são abertos de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="24c13-479">Files always open asynchronously.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-480"><em>Player6</em>. <strong>Pausar</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-480"><em>Player6</em>.<strong>Pause</strong></span></span></td>
<td><span data-ttu-id="24c13-481">Use <em>controles</em>. <strong>Pausar</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-481">Use <em>Controls</em>.<strong>pause</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-482"><em>Player6</em>. <strong>Reproduzir</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-482"><em>Player6</em>.<strong>Play</strong></span></span></td>
<td><span data-ttu-id="24c13-483">Use <em>controles</em>. <strong>reproduzir</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-483">Use <em>Controls</em>.<strong>play</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-484"><em>Player6</em>. <strong>Anterior</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-484"><em>Player6</em>.<strong>Previous</strong></span></span></td>
<td><span data-ttu-id="24c13-485">Use <em>controles</em>. <strong>anterior</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-485">Use <em>Controls</em>.<strong>previous</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-486"><em>Player6</em>. <strong>PrevPGSearch</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-486"><em>Player6</em>.<strong>PrevPGSearch</strong></span></span></td>
<td><span data-ttu-id="24c13-487">Use <em>controles</em>. <strong>anterior</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-487">Use <em>Controls</em>.<strong>previous</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-488"><em>Player6</em>. <strong>ResumeFromMenu</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-488"><em>Player6</em>.<strong>ResumeFromMenu</strong></span></span></td>
<td><span data-ttu-id="24c13-489">Use o <em>DVD</em>. <strong>retomar</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-489">Use <em>DVD</em>.<strong>resume</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-490"><em>Player6</em>. <strong>RightButtonSelect</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-490"><em>Player6</em>.<strong>RightButtonSelect</strong></span></span></td>
<td><span data-ttu-id="24c13-491">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-491">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-492"><em>Player6</em>. <strong>SetCurrentEntry</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-492"><em>Player6</em>.<strong>SetCurrentEntry</strong></span></span></td>
<td><span data-ttu-id="24c13-493">Recupere um objeto de mídia usando <em>currentPlaylist</em>. <strong>Item</strong>(<em>entryNumber</em>).</span><span class="sxs-lookup"><span data-stu-id="24c13-493">Retrieve a media object using <em>currentPlaylist</em>.<strong>item</strong>(<em>entryNumber</em>).</span></span> <span data-ttu-id="24c13-494">Em seguida, especifique o objeto de mídia recuperado usando <em>controles</em>. <strong>currentItem</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-494">Then, specify the retrieved media object using <em>Controls</em>.<strong>currentItem</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-495"><em>Player6</em>. <strong>ShowDialog</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-495"><em>Player6</em>.<strong>ShowDialog</strong></span></span></td>
<td><span data-ttu-id="24c13-496">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-496">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-497"><em>Player6</em>. <strong>StillOff</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-497"><em>Player6</em>.<strong>StillOff</strong></span></span></td>
<td><span data-ttu-id="24c13-498">Use <em>controles</em>. <strong>reproduzir</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-498">Use <em>Controls</em>.<strong>play</strong>.</span></span> <span data-ttu-id="24c13-499">Como alternativa, use <em>controles</em>. Em <strong>seguida</strong> , se estiver atualmente no modo ainda.</span><span class="sxs-lookup"><span data-stu-id="24c13-499">Alternatively, use <em>Controls</em>.<strong>Next</strong> if currently in still mode.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-500"><em>Player6</em>. <strong>Parar</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-500"><em>Player6</em>.<strong>Stop</strong></span></span></td>
<td><span data-ttu-id="24c13-501">Use <em>controles</em>. <strong>parar</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-501">Use <em>Controls</em>.<strong>stop</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-502"><em>Player6</em>. <strong>StreamSelect</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-502"><em>Player6</em>.<strong>StreamSelect</strong></span></span></td>
<td><span data-ttu-id="24c13-503">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-503">Not available.</span></span> <span data-ttu-id="24c13-504">Use <em>controles</em>. <strong>currentAudioLanguage</strong> para especificar um fluxo de idioma de áudio.</span><span class="sxs-lookup"><span data-stu-id="24c13-504">Use <em>Controls</em>.<strong>currentAudioLanguage</strong> to specify an audio language stream.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-505"><em>Player6</em>. <strong>Timeplay</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-505"><em>Player6</em>.<strong>TimePlay</strong></span></span></td>
<td><span data-ttu-id="24c13-506">Na lista de reprodução raiz, use <em>currentPlaylist</em>. <strong>Item</strong>(<em>índice</em>) para recuperar um objeto de mídia.</span><span class="sxs-lookup"><span data-stu-id="24c13-506">From the root playlist, use <em>currentPlaylist</em>.<strong>item</strong>(<em>index</em>) to retrieve a media object.</span></span> <span data-ttu-id="24c13-507">Em seguida, defina o objeto de mídia como o atual usando <em>controles</em>. <strong>currentItem</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-507">Then, set the media object as the current one using <em>Controls</em>.<strong>currentItem</strong>.</span></span> <span data-ttu-id="24c13-508">Em seguida, especifique os <em>controles</em>. <strong>CurrentPosition</strong> usando um valor de tempo em segundos.</span><span class="sxs-lookup"><span data-stu-id="24c13-508">Then, specify <em>Controls</em>.<strong>currentPosition</strong> using a time value in seconds.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-509"><em>Player6</em>. <strong>Timesearch</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-509"><em>Player6</em>.<strong>TimeSearch</strong></span></span></td>
<td><span data-ttu-id="24c13-510">Use <em>controles</em>. <strong>CurrentPosition</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-510">Use <em>Controls</em>.<strong>currentPosition</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-511"><em>Player6</em>. <strong>TitlePlay</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-511"><em>Player6</em>.<strong>TitlePlay</strong></span></span></td>
<td><span data-ttu-id="24c13-512">Se já estiver executando a playlist de título especificada, recupere o capítulo desejado como um objeto de mídia usando a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="24c13-512">If already playing the specified title playlist, retrieve the desired chapter as a media object using the following syntax:</span></span>
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
<span data-ttu-id="24c13-513">Em seguida, especifique <em>Player</em>. <strong>currentMedia</strong> usando o objeto de mídia retornado.</span><span class="sxs-lookup"><span data-stu-id="24c13-513">Then, specify <em>Player</em>.<strong>currentMedia</strong> using the media object returned.</span></span><br/> <span data-ttu-id="24c13-514">Como alternativa, use <em>currentPlaylist</em>. <strong>Item</strong> para recuperar um objeto de mídia e, em seguida, use o objeto de mídia retornado para especificar <em>controles</em>. <strong>currentItem</strong>.</span><span class="sxs-lookup"><span data-stu-id="24c13-514">Alternatively, use <em>currentPlaylist</em>.<strong>item</strong> to retrieve a media object, and then use the media object returned to specify <em>Controls</em>.<strong>currentItem</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-515"><em>Player6</em>. <strong>TopPGSearch</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-515"><em>Player6</em>.<strong>TopPGSearch</strong></span></span></td>
<td><span data-ttu-id="24c13-516">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-516">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24c13-517"><em>Player6</em>. <strong>UOPValid</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-517"><em>Player6</em>.<strong>UOPValid</strong></span></span></td>
<td><span data-ttu-id="24c13-518">Não disponível</span><span class="sxs-lookup"><span data-stu-id="24c13-518">Not available</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24c13-519"><em>Player6</em>. <strong>UpperButtonSelect</strong></span><span class="sxs-lookup"><span data-stu-id="24c13-519"><em>Player6</em>.<strong>UpperButtonSelect</strong></span></span></td>
<td><span data-ttu-id="24c13-520">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-520">Not available.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="24c13-521">A tabela a seguir compara os eventos do modelo de objeto do Windows Media Player versão 6,4 com o modelo de objeto do Windows Media Player 7 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="24c13-521">The following table compares the Windows Media Player version 6.4 object model events with the Windows Media Player 7 or later object model.</span></span>



| <span data-ttu-id="24c13-522">Evento 6,4 do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="24c13-522">Windows Media Player 6.4 event</span></span>  | <span data-ttu-id="24c13-523">Windows Media Player 7 ou posterior equivalente</span><span class="sxs-lookup"><span data-stu-id="24c13-523">Windows Media Player 7 or later equivalent</span></span>                                                                                                                                                                               |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24c13-524">*Player6*. **Armazenamento em buffer**</span><span class="sxs-lookup"><span data-stu-id="24c13-524">*Player6*.**Buffering**</span></span>         | <span data-ttu-id="24c13-525">Use o *Player*. **Armazenamento em buffer**.</span><span class="sxs-lookup"><span data-stu-id="24c13-525">Use *Player*.**Buffering**.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="24c13-526">*Player6*. **Clique em**</span><span class="sxs-lookup"><span data-stu-id="24c13-526">*Player6*.**Click**</span></span>             | <span data-ttu-id="24c13-527">Use o *Player*. **Clique em**</span><span class="sxs-lookup"><span data-stu-id="24c13-527">Use *Player*.**Click**</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="24c13-528">*Player6*. **DblClick**</span><span class="sxs-lookup"><span data-stu-id="24c13-528">*Player6*.**DblClick**</span></span>          | <span data-ttu-id="24c13-529">Use o *Player*. **DoubleClick**</span><span class="sxs-lookup"><span data-stu-id="24c13-529">Use *Player*.**DoubleClick**</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="24c13-530">*Player6*. **Desconectar**</span><span class="sxs-lookup"><span data-stu-id="24c13-530">*Player6*.**Disconnect**</span></span>        | <span data-ttu-id="24c13-531">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-531">Not available.</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="24c13-532">*Player6*. **DisplayModeChange**</span><span class="sxs-lookup"><span data-stu-id="24c13-532">*Player6*.**DisplayModeChange**</span></span> | <span data-ttu-id="24c13-533">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-533">Not available.</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="24c13-534">*Player6*. **DVDNotify**</span><span class="sxs-lookup"><span data-stu-id="24c13-534">*Player6*.**DVDNotify**</span></span>         | <span data-ttu-id="24c13-535">*Player*. **DomainChange** e *Player*. **OpenPlaylistSwitch** são eventos específicos de DVD.</span><span class="sxs-lookup"><span data-stu-id="24c13-535">*Player*.**DomainChange** and *Player*.**OpenPlaylistSwitch** are DVD-specific events.</span></span> <span data-ttu-id="24c13-536">Outros eventos relacionados às listas de reprodução, mídia e mídia de CD-ROM também podem se aplicar, dependendo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="24c13-536">Other events related to playlists, media, and CD-ROM media may apply as well depending on the application.</span></span>                        |
| <span data-ttu-id="24c13-537">*Player6*. **EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="24c13-537">*Player6*.**EndOfStream**</span></span>       | <span data-ttu-id="24c13-538">Use o *Player*. **PlayState**.</span><span class="sxs-lookup"><span data-stu-id="24c13-538">Use *Player*.**PlayState**.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="24c13-539">*Player6*. **Erro** do</span><span class="sxs-lookup"><span data-stu-id="24c13-539">*Player6*.**Error**</span></span>             | <span data-ttu-id="24c13-540">O evento está inalterado.</span><span class="sxs-lookup"><span data-stu-id="24c13-540">The event is unchanged.</span></span> <span data-ttu-id="24c13-541">Os erros, no entanto, são enfileirados.</span><span class="sxs-lookup"><span data-stu-id="24c13-541">Errors, however, are queued.</span></span> <span data-ttu-id="24c13-542">Use o objeto de **erro** com o objeto **ErrorItem** para recuperar informações de erro da fila.</span><span class="sxs-lookup"><span data-stu-id="24c13-542">Use the **Error** object with the **ErrorItem** object to retrieve error information from the queue.</span></span> <span data-ttu-id="24c13-543">Consulte o código de exemplo na seção anterior, tratamento de erro.</span><span class="sxs-lookup"><span data-stu-id="24c13-543">See the example code in the preceding section, Error handling.</span></span> |
| <span data-ttu-id="24c13-544">*Player6*. **KeyDown**</span><span class="sxs-lookup"><span data-stu-id="24c13-544">*Player6*.**KeyDown**</span></span>           | <span data-ttu-id="24c13-545">Use o *Player*. **KeyDown**</span><span class="sxs-lookup"><span data-stu-id="24c13-545">Use *Player*.**Keydown**</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="24c13-546">*Player6*. **KeyPress**</span><span class="sxs-lookup"><span data-stu-id="24c13-546">*Player6*.**KeyPress**</span></span>          | <span data-ttu-id="24c13-547">Use o *Player*. **KeyPress**</span><span class="sxs-lookup"><span data-stu-id="24c13-547">Use *Player*.**KeyPress**</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="24c13-548">*Player6*. **KeyUp**</span><span class="sxs-lookup"><span data-stu-id="24c13-548">*Player6*.**KeyUp**</span></span>             | <span data-ttu-id="24c13-549">Use o *Player*. **KeyUp**</span><span class="sxs-lookup"><span data-stu-id="24c13-549">Use *Player*.**KeyUp**</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="24c13-550">*Player6*. **MarkerHit**</span><span class="sxs-lookup"><span data-stu-id="24c13-550">*Player6*.**MarkerHit**</span></span>         | <span data-ttu-id="24c13-551">Use o *Player*. **MarkerHit**.</span><span class="sxs-lookup"><span data-stu-id="24c13-551">Use *Player*.**MarkerHit**.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="24c13-552">*Player6*. **MouseDown**</span><span class="sxs-lookup"><span data-stu-id="24c13-552">*Player6*.**MouseDown**</span></span>         | <span data-ttu-id="24c13-553">Use o *Player*. **MouseDown**</span><span class="sxs-lookup"><span data-stu-id="24c13-553">Use *Player*.**MouseDown**</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="24c13-554">*Player6*. **MouseMove**</span><span class="sxs-lookup"><span data-stu-id="24c13-554">*Player6*.**MouseMove**</span></span>         | <span data-ttu-id="24c13-555">Use o *Player*. **MouseMove**</span><span class="sxs-lookup"><span data-stu-id="24c13-555">Use *Player*.**MouseMove**</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="24c13-556">*Player6*. **MouseUp**</span><span class="sxs-lookup"><span data-stu-id="24c13-556">*Player6*.**MouseUp**</span></span>           | <span data-ttu-id="24c13-557">Use o *Player*. **MouseUp**</span><span class="sxs-lookup"><span data-stu-id="24c13-557">Use *Player*.**MouseUp**</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="24c13-558">*Player6*. **NewStream**</span><span class="sxs-lookup"><span data-stu-id="24c13-558">*Player6*.**NewStream**</span></span>         | <span data-ttu-id="24c13-559">Use o *Player*. **OpenStateChange**</span><span class="sxs-lookup"><span data-stu-id="24c13-559">Use *Player*.**OpenStateChange**</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="24c13-560">*Player6*. **OpenStateChange**</span><span class="sxs-lookup"><span data-stu-id="24c13-560">*Player6*.**OpenStateChange**</span></span>   | <span data-ttu-id="24c13-561">Use o *Player*. **OpenStateChange**.</span><span class="sxs-lookup"><span data-stu-id="24c13-561">Use *Player*.**OpenStateChange**.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="24c13-562">*Player6*. **PlayStateChange**</span><span class="sxs-lookup"><span data-stu-id="24c13-562">*Player6*.**PlayStateChange**</span></span>   | <span data-ttu-id="24c13-563">Use o *Player*. **PlayStateChange**.</span><span class="sxs-lookup"><span data-stu-id="24c13-563">Use *Player*.**PlayStateChange**.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="24c13-564">*Player6*. **PositionChange**</span><span class="sxs-lookup"><span data-stu-id="24c13-564">*Player6*.**PositionChange**</span></span>    | <span data-ttu-id="24c13-565">Use o *Player*. **PositionChange**.</span><span class="sxs-lookup"><span data-stu-id="24c13-565">Use *Player*.**PositionChange**.</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="24c13-566">*Player6*. **ReadyStateChange**</span><span class="sxs-lookup"><span data-stu-id="24c13-566">*Player6*.**ReadyStateChange**</span></span>  | <span data-ttu-id="24c13-567">Use o *Player*. **PlayStateChange**.</span><span class="sxs-lookup"><span data-stu-id="24c13-567">Use *Player*.**PlayStateChange**.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="24c13-568">*Player6*. **ScriptCommand**</span><span class="sxs-lookup"><span data-stu-id="24c13-568">*Player6*.**ScriptCommand**</span></span>     | <span data-ttu-id="24c13-569">Use o *Player*. **ScriptCommand**.</span><span class="sxs-lookup"><span data-stu-id="24c13-569">Use *Player*.**ScriptCommand**.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="24c13-570">*Player6*. **Aviso**</span><span class="sxs-lookup"><span data-stu-id="24c13-570">*Player6*.**Warning**</span></span>           | <span data-ttu-id="24c13-571">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="24c13-571">Not available.</span></span>                                                                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="24c13-572">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="24c13-572">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24c13-573">**Guia de migração do modelo de objeto**</span><span class="sxs-lookup"><span data-stu-id="24c13-573">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> <dt>

[<span data-ttu-id="24c13-574">**Referência de modelo de objeto para scripts**</span><span class="sxs-lookup"><span data-stu-id="24c13-574">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 






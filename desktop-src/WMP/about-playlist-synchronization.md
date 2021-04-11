---
title: Sobre a sincronização de playlist
description: Sobre a sincronização de playlist
ms.assetid: bc7d52e0-7906-4b5b-82e6-a84e9c4f0ff0
keywords:
- Windows Media Player, sincronização de playlist
- Modelo de objeto do Windows Media Player, sincronização de playlist
- modelo de objeto, sincronização de playlist
- Controle ActiveX do Windows Media Player, sincronização de playlist
- Controle ActiveX, sincronização de playlist
- Controle ActiveX móvel do Windows Media Player, sincronização de playlist
- Windows Media Player Mobile, sincronização de playlist
- Sincronizando dispositivos, listas de reprodução
- sincronização de dispositivo, listas de reprodução
- listas de reprodução, sincronização
- Listas de reprodução do metarquivo do Windows Media, sincronização
- listas de reprodução de metarquivo, sincronização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc019b31518fda1a49c8d3ae86f2d03c4ecefc8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104293762"
---
# <a name="about-playlist-synchronization"></a><span data-ttu-id="0c04b-115">Sobre a sincronização de playlist</span><span class="sxs-lookup"><span data-stu-id="0c04b-115">About Playlist Synchronization</span></span>

<span data-ttu-id="0c04b-116">O Windows Media Player 10 ou posterior foi projetado para sincronizar o conteúdo de mídia digital para dispositivos usando um modelo de sincronização de playlist.</span><span class="sxs-lookup"><span data-stu-id="0c04b-116">Windows Media Player 10 or later is designed to synchronize digital media content to devices using a playlist synchronization model.</span></span> <span data-ttu-id="0c04b-117">Isso significa que o conteúdo destinado a ser copiado para um dispositivo deve fazer parte de uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="0c04b-117">This means that content intended to be copied to a device must be part of a playlist.</span></span> <span data-ttu-id="0c04b-118">Quando o usuário opta por transferir o conteúdo de mídia digital individual do seu computador para um dispositivo, o Windows Media Player adiciona o conteúdo a uma lista de reprodução padrão para cópia.</span><span class="sxs-lookup"><span data-stu-id="0c04b-118">When the user chooses to transfer individual digital media content from his or her computer to a device, Windows Media Player adds the content to a default playlist for copying.</span></span>

<span data-ttu-id="0c04b-119">As APIs de sincronização de dispositivo do Windows Media Player também são projetadas para funcionar dessa forma.</span><span class="sxs-lookup"><span data-stu-id="0c04b-119">The Windows Media Player device synchronization APIs are designed to work like this as well.</span></span> <span data-ttu-id="0c04b-120">Como o Windows Media Player, seu programa pode apresentar ao usuário uma lista de listas de reprodução que ele definiu.</span><span class="sxs-lookup"><span data-stu-id="0c04b-120">Like Windows Media Player, your program can present the user with a list of playlists that he or she has defined.</span></span> <span data-ttu-id="0c04b-121">Em seguida, você pode permitir que o usuário escolha quais listas de reprodução sincronizar com um dispositivo específico e defina a ordem de prioridade para o processo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="0c04b-121">You can then enable the user to choose which playlists to synchronize with a particular device and to set the priority order for the synchronization process.</span></span>

<span data-ttu-id="0c04b-122">Como os dispositivos portáteis têm uma capacidade de armazenamento limitada, é possível que o usuário opte por sincronizar mais conteúdo de mídia digital do que o dispositivo pode armazenar.</span><span class="sxs-lookup"><span data-stu-id="0c04b-122">Because portable devices have a limited storage capacity, it is possible for the user to choose to synchronize more digital media content than the device can store.</span></span> <span data-ttu-id="0c04b-123">O Windows Media Player sincroniza o conteúdo em ordem de prioridade.</span><span class="sxs-lookup"><span data-stu-id="0c04b-123">Windows Media Player synchronizes content in priority order.</span></span> <span data-ttu-id="0c04b-124">O usuário pode definir a ordem de prioridade usando uma caixa de diálogo que pode ser acessada por meio do recurso **dispositivos** .</span><span class="sxs-lookup"><span data-stu-id="0c04b-124">The user can define the priority order by using a dialog box that can be accessed from the **Devices** feature.</span></span> <span data-ttu-id="0c04b-125">Em resposta à entrada do usuário para seu programa, você pode alterar a ordem de prioridade programaticamente alterando os valores de determinados atributos da lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="0c04b-125">In response to user input to your program, you can change the priority order programmatically by changing the values of certain playlist attributes.</span></span> <span data-ttu-id="0c04b-126">Coletivamente, esses atributos são chamados de atributos de *sincronização* .</span><span class="sxs-lookup"><span data-stu-id="0c04b-126">Collectively, these attributes are called the *Sync* attributes.</span></span>

<span data-ttu-id="0c04b-127">Cada playlist em uma biblioteca tem 16 atributos de sincronização: **Sync01** a **Sync16**.</span><span class="sxs-lookup"><span data-stu-id="0c04b-127">Each playlist in a library has 16 synchronization attributes: **Sync01** through **Sync16**.</span></span> <span data-ttu-id="0c04b-128">Cada atributo representa o dispositivo que tem o índice de parceria correspondente.</span><span class="sxs-lookup"><span data-stu-id="0c04b-128">Each attribute represents the device that has the corresponding partnership index.</span></span> <span data-ttu-id="0c04b-129">O valor de cada atributo informa duas coisas:</span><span class="sxs-lookup"><span data-stu-id="0c04b-129">The value of each attribute tells you two things:</span></span>

-   <span data-ttu-id="0c04b-130">Se a playlist deve ser sincronizada com o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0c04b-130">Whether the playlist should be synchronized with the device.</span></span>
-   <span data-ttu-id="0c04b-131">O valor de prioridade para a lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="0c04b-131">The priority value for the playlist.</span></span>

<span data-ttu-id="0c04b-132">Um valor de zero indica que o Windows Media Player não deve tentar sincronizar a playlist com o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0c04b-132">A value of zero indicates that Windows Media Player should not attempt to synchronize the playlist with the device.</span></span> <span data-ttu-id="0c04b-133">Qualquer outro valor é um número de prioridade.</span><span class="sxs-lookup"><span data-stu-id="0c04b-133">Any other value is a priority number.</span></span> <span data-ttu-id="0c04b-134">Valores mais baixos recebem prioridade mais alta no tempo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="0c04b-134">Lower values receive higher priority at synchronization time.</span></span>

<span data-ttu-id="0c04b-135">As listas de reprodução também têm um atributo **SyncOnly** que indica se a playlist está disponível apenas para sincronização.</span><span class="sxs-lookup"><span data-stu-id="0c04b-135">Playlists also have a **SyncOnly** attribute that indicates whether the playlist is available only for synchronization.</span></span>

<span data-ttu-id="0c04b-136">Itens individuais de conteúdo de mídia digital contêm metadados sobre a sincronização também.</span><span class="sxs-lookup"><span data-stu-id="0c04b-136">Individual items of digital media content contain metadata about synchronization as well.</span></span> <span data-ttu-id="0c04b-137">Ao recuperar um objeto de **mídia** da biblioteca, você pode inspecionar o valor do atributo **SyncState** .</span><span class="sxs-lookup"><span data-stu-id="0c04b-137">When you retrieve a **Media** object from the library, you can inspect the value of the **SyncState** attribute.</span></span> <span data-ttu-id="0c04b-138">Esse atributo fornece informações estendidas sobre se o conteúdo foi copiado com êxito no dispositivo ou se houve falha ao copiar o conteúdo porque ele não se ajustaria.</span><span class="sxs-lookup"><span data-stu-id="0c04b-138">This attribute provides extended information about whether the content has been successfully copied to the device or whether copying the content failed because it would not fit.</span></span>

> [!Note]  
> <span data-ttu-id="0c04b-139">Você deve evitar fornecer elementos de interface do usuário que permitem ao usuário criar listas de reprodução de todo o conteúdo da biblioteca para sincronização.</span><span class="sxs-lookup"><span data-stu-id="0c04b-139">You should avoid providing user interface elements that enable the user to create playlists from all library content for synchronization.</span></span>

 

<span data-ttu-id="0c04b-140">Para otimizar o desempenho, o Windows Media Player impõe um conjunto de regras para a criação de listas de reprodução de sincronização.</span><span class="sxs-lookup"><span data-stu-id="0c04b-140">To optimize performance, Windows Media Player enforces a set of rules for creating synchronization playlists.</span></span> <span data-ttu-id="0c04b-141">Seu programa deve criar somente listas de reprodução de sincronização para o conteúdo fornecido.</span><span class="sxs-lookup"><span data-stu-id="0c04b-141">Your program should only create synchronization playlists for content you provided.</span></span> <span data-ttu-id="0c04b-142">Permitir que o Windows Media Player crie listas de reprodução de sincronização para o conteúdo que o usuário adicionou à biblioteca de outras fontes.</span><span class="sxs-lookup"><span data-stu-id="0c04b-142">Allow Windows Media Player to create synchronization playlists for content that the user added to the library from other sources.</span></span>

<span data-ttu-id="0c04b-143">Como alternativa para criar sua própria interface do usuário de playlist, você pode apresentar aos usuários uma caixa de diálogo padrão para escolher as listas de reprodução e gerenciar a parceria para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0c04b-143">As an alternative to creating your own playlist user interface, you can present users with a default dialog box for choosing playlists and managing the partnership for a device.</span></span> <span data-ttu-id="0c04b-144">Para fazer isso, chame [IWMPSyncDevice:: Configurations](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-showsettings).</span><span class="sxs-lookup"><span data-stu-id="0c04b-144">To do this, call [IWMPSyncDevice::showSettings](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-showsettings).</span></span> <span data-ttu-id="0c04b-145">Quando você invoca esse método, o Windows Media Player exibe a caixa de diálogo Configurações de sincronização.</span><span class="sxs-lookup"><span data-stu-id="0c04b-145">When you invoke this method, Windows Media Player displays its synchronization settings dialog box.</span></span> <span data-ttu-id="0c04b-146">Quando o usuário fecha a caixa de diálogo, o Windows Media Player retorna automaticamente ao seu estado de encaixe anterior e passa o controle de volta para o programa remoto.</span><span class="sxs-lookup"><span data-stu-id="0c04b-146">When the user closes the dialog box, Windows Media Player automatically returns to its prior docking state and passes control back to your remoted program.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c04b-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0c04b-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c04b-148">**Sobre a sincronização do dispositivo**</span><span class="sxs-lookup"><span data-stu-id="0c04b-148">**About Device Synchronization**</span></span>](about-device-synchronization.md)
</dt> <dt>

[<span data-ttu-id="0c04b-149">**Gerenciando listas de reprodução de sincronização**</span><span class="sxs-lookup"><span data-stu-id="0c04b-149">**Managing Synchronization Playlists**</span></span>](managing-synchronization-playlists.md)
</dt> <dt>

[<span data-ttu-id="0c04b-150">**Atributos da lista de reprodução**</span><span class="sxs-lookup"><span data-stu-id="0c04b-150">**Playlist Attributes**</span></span>](playlist-attributes.md)
</dt> </dl>

 

 





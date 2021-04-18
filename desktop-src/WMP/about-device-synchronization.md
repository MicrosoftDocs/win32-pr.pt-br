---
title: Sobre a sincronização do dispositivo
description: Sobre a sincronização do dispositivo
ms.assetid: 87976357-f819-41ac-9645-36e799876881
keywords:
- Windows Media Player, sincronizando dispositivos
- Modelo de objeto do Windows Media Player, sincronizando dispositivos
- modelo de objeto, sincronizando dispositivos
- Controle ActiveX do Windows Media Player, sincronizando dispositivos
- Controle ActiveX, sincronizando dispositivos
- Controle ActiveX móvel do Windows Media Player, sincronizando dispositivos
- Windows Media Player Mobile, sincronizando dispositivos
- Sincronizando dispositivos, sobre
- sincronização de dispositivo, sobre
- Sincronizando dispositivos, transferência manual
- sincronização de dispositivo, transferência manual
- Sincronizando dispositivos, sincronização automática
- sincronização de dispositivo, sincronização automática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ad6b6526698def2f7d58ec7afc04c8e22e89c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105783642"
---
# <a name="about-device-synchronization"></a><span data-ttu-id="8a697-116">Sobre a sincronização do dispositivo</span><span class="sxs-lookup"><span data-stu-id="8a697-116">About Device Synchronization</span></span>

<span data-ttu-id="8a697-117">O Windows Media Player 10 introduziu um novo modelo de sincronização de conteúdo de mídia digital com dispositivos portáteis.</span><span class="sxs-lookup"><span data-stu-id="8a697-117">Windows Media Player 10 introduced a new model for synchronizing digital media content with portable devices.</span></span> <span data-ttu-id="8a697-118">Da perspectiva do usuário, isso significa que você pode especificar quais listas de reprodução (incluindo listas de reprodução automáticas) são sincronizadas automaticamente com dispositivos.</span><span class="sxs-lookup"><span data-stu-id="8a697-118">From the user's perspective, this means you can specify which playlists (including auto playlists) synchronize automatically with devices.</span></span> <span data-ttu-id="8a697-119">Você também pode transferir manualmente o conteúdo de mídia digital para dispositivos.</span><span class="sxs-lookup"><span data-stu-id="8a697-119">You can also manually transfer digital media content to devices.</span></span> <span data-ttu-id="8a697-120">Da perspectiva do desenvolvedor, isso significa que há uma nova funcionalidade exposta que você pode aproveitar em seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="8a697-120">From the developer's perspective, this means there is new functionality exposed that you can take advantage of in your applications.</span></span> <span data-ttu-id="8a697-121">Para fazer isso, você deve criar uma instância remota do controle do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8a697-121">To do this, you must create a remoted instance of the Windows Media Player control.</span></span>

<span data-ttu-id="8a697-122">Há duas maneiras pelas quais um usuário pode copiar conteúdo de mídia digital para um dispositivo:</span><span class="sxs-lookup"><span data-stu-id="8a697-122">There are two ways a user can copy digital media content to a device:</span></span>

-   <span data-ttu-id="8a697-123">**Transferência manual.**</span><span class="sxs-lookup"><span data-stu-id="8a697-123">**Manual transfer.**</span></span> <span data-ttu-id="8a697-124">O usuário seleciona o conteúdo de mídia digital na biblioteca e, em seguida, inicia uma transferência do conteúdo para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8a697-124">The user selects digital media content in the library and then initiates a transfer of the content to the device.</span></span> <span data-ttu-id="8a697-125">Isso é semelhante à funcionalidade fornecida pelas versões anteriores do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8a697-125">This is similar to the functionality provided by previous versions of Windows Media Player.</span></span> <span data-ttu-id="8a697-126">O SDK do Windows Media Player não fornece métodos para transferir mídia digital para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8a697-126">The Windows Media Player SDK does not provide methods for transferring digital media to a device.</span></span>
-   <span data-ttu-id="8a697-127">**Sincronização automática.**</span><span class="sxs-lookup"><span data-stu-id="8a697-127">**Automatic synchronization.**</span></span> <span data-ttu-id="8a697-128">O usuário especifica as listas de reprodução que sincronizam automaticamente com o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8a697-128">The user specifies playlists that automatically synchronize with the device.</span></span> <span data-ttu-id="8a697-129">Esse é um recurso do Windows Media Player 10 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="8a697-129">This is a feature of Windows Media Player 10 or later.</span></span> <span data-ttu-id="8a697-130">O SDK do Windows Media Player fornece a funcionalidade para gerenciar a sincronização automática.</span><span class="sxs-lookup"><span data-stu-id="8a697-130">The Windows Media Player SDK provides functionality for managing automatic synchronization.</span></span> <span data-ttu-id="8a697-131">Essa funcionalidade foi projetada para permitir que você crie uma interface do usuário personalizada para que seu aplicativo especifique como a sincronização do dispositivo ocorre e forneça informações de status aos usuários.</span><span class="sxs-lookup"><span data-stu-id="8a697-131">This functionality is designed to let you build a custom user interface for your application to specify how device synchronization happens and to provide status information to users.</span></span>

<span data-ttu-id="8a697-132">Para que a sincronização automática funcione, uma relação especial deve ser estabelecida entre o Windows Media Player e o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8a697-132">For automatic synchronization to work, a special relationship must be established between Windows Media Player and the device.</span></span> <span data-ttu-id="8a697-133">Essa relação é chamada de *parceria*.</span><span class="sxs-lookup"><span data-stu-id="8a697-133">This relationship is called a *partnership*.</span></span>

<span data-ttu-id="8a697-134">As seções a seguir fornecem mais informações sobre a sincronização de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="8a697-134">The following sections provide more information about device synchronization.</span></span>

-   [<span data-ttu-id="8a697-135">Sobre dispositivos</span><span class="sxs-lookup"><span data-stu-id="8a697-135">About Devices</span></span>](about-devices.md)
-   [<span data-ttu-id="8a697-136">Sobre parcerias</span><span class="sxs-lookup"><span data-stu-id="8a697-136">About Partnerships</span></span>](about-partnerships.md)
-   [<span data-ttu-id="8a697-137">Sobre o mecanismo de sincronização</span><span class="sxs-lookup"><span data-stu-id="8a697-137">About the Synchronization Engine</span></span>](about-the-synchronization-engine.md)
-   [<span data-ttu-id="8a697-138">Sobre a sincronização de playlist</span><span class="sxs-lookup"><span data-stu-id="8a697-138">About Playlist Synchronization</span></span>](about-playlist-synchronization.md)

## <a name="related-topics"></a><span data-ttu-id="8a697-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8a697-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a697-140">**Sobre o modelo de objeto do Player**</span><span class="sxs-lookup"><span data-stu-id="8a697-140">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> <dt>

[<span data-ttu-id="8a697-141">**Estabelecer comunicação remota do controle do Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="8a697-141">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> <dt>

[<span data-ttu-id="8a697-142">**Trabalhando com dispositivos portáteis**</span><span class="sxs-lookup"><span data-stu-id="8a697-142">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 





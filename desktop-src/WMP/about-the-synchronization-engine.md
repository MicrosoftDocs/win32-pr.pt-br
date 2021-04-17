---
title: Sobre o mecanismo de sincronização
description: Sobre o mecanismo de sincronização
ms.assetid: bb57ffb0-3833-463b-b66c-c23224fa2ba7
keywords:
- Windows Media Player, mecanismo de sincronização
- Modelo de objeto do Windows Media Player, mecanismo de sincronização
- modelo de objeto, mecanismo de sincronização
- Controle ActiveX do Windows Media Player, mecanismo de sincronização
- Controle ActiveX, mecanismo de sincronização
- Controle ActiveX móvel do Windows Media Player, mecanismo de sincronização
- Windows Media Player Mobile, mecanismo de sincronização
- Sincronizando dispositivos, mecanismo de sincronização
- sincronização de dispositivo, mecanismo de sincronização
- mecanismo de sincronização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe0768c4805b074fdaf628a25daf47b9ced97ee
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365591"
---
# <a name="about-the-synchronization-engine"></a><span data-ttu-id="6302b-113">Sobre o mecanismo de sincronização</span><span class="sxs-lookup"><span data-stu-id="6302b-113">About the Synchronization Engine</span></span>

<span data-ttu-id="6302b-114">O mecanismo de sincronização é o componente do Windows Media Player que gerencia a cópia de conteúdo de mídia digital para dispositivos portáteis.</span><span class="sxs-lookup"><span data-stu-id="6302b-114">The synchronization engine is the component of Windows Media Player that manages copying digital media content to portable devices.</span></span> <span data-ttu-id="6302b-115">O Windows Media Player dá suporte a uma única instância do mecanismo de sincronização para cada dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6302b-115">Windows Media Player supports a single instance of the synchronization engine for each device.</span></span> <span data-ttu-id="6302b-116">Você deve usar uma instância remota do controle do Windows Media Player para executar tarefas de sincronização programaticamente.</span><span class="sxs-lookup"><span data-stu-id="6302b-116">You must use a remoted instance of the Windows Media Player control to perform synchronization tasks programmatically.</span></span> <span data-ttu-id="6302b-117">Na verdade, o programa compartilha as instâncias do mecanismo de sincronização com o Windows Media Player e todos os outros programas que usam as interfaces do Player para a sincronização do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6302b-117">In effect, your program shares the synchronization engine instances with Windows Media Player and all other programs that use the Player interfaces for device synchronization.</span></span>

<span data-ttu-id="6302b-118">Você pode usar [IWMPSyncDevice:: Start](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-start) e [IWMPSyncDevice:: Stop](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-stop) para controlar quando o mecanismo de sincronização faz seu trabalho.</span><span class="sxs-lookup"><span data-stu-id="6302b-118">You can use [IWMPSyncDevice::start](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-start) and [IWMPSyncDevice::stop](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-stop) to control when the synchronization engine does its work.</span></span> <span data-ttu-id="6302b-119">Na maioria dos casos, você não deve usar esses métodos.</span><span class="sxs-lookup"><span data-stu-id="6302b-119">In most cases, you should not use these methods.</span></span> <span data-ttu-id="6302b-120">Em vez disso, você deve deixar o mecanismo de sincronização agendar seu trabalho automaticamente.</span><span class="sxs-lookup"><span data-stu-id="6302b-120">Instead, you should let the synchronization engine schedule its work automatically.</span></span> <span data-ttu-id="6302b-121">Os métodos **Start** e **Stop** existem para que você possa usá-los se o programa for projetado para substituir a interface do usuário do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6302b-121">The **start** and **stop** methods exist so that you can use them if your program is designed to replace the Windows Media Player user interface.</span></span> <span data-ttu-id="6302b-122">Nesse caso, talvez você queira fornecer um botão iniciar/parar semelhante ao fornecido pelo Windows Media Player na guia **dispositivos** .</span><span class="sxs-lookup"><span data-stu-id="6302b-122">In this case, you might want to provide a start/stop button similar to the one Windows Media Player provides in the **Devices** tab.</span></span>

<span data-ttu-id="6302b-123">Você pode monitorar o progresso da sincronização de um dispositivo ao sondar [IWMPSyncDevice:: obter \_ progresso](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress).</span><span class="sxs-lookup"><span data-stu-id="6302b-123">You can monitor the synchronization progress for a device by polling [IWMPSyncDevice::get\_progress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress).</span></span> <span data-ttu-id="6302b-124">Esse método recupera um valor de progresso para todo o processo de sincronização com um dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="6302b-124">This method retrieves a progress value for the entire synchronization process with a particular device.</span></span> <span data-ttu-id="6302b-125">O valor recuperado é um número que representa a porcentagem de sincronização concluída.</span><span class="sxs-lookup"><span data-stu-id="6302b-125">The value retrieved is a number that represents the percentage of synchronization complete.</span></span> <span data-ttu-id="6302b-126">Há dois eventos que você pode receber relacionados à sincronização.</span><span class="sxs-lookup"><span data-stu-id="6302b-126">There are two events you can receive that are related to synchronization.</span></span> <span data-ttu-id="6302b-127">O evento **DeviceSyncError** notifica quando ocorre um problema.</span><span class="sxs-lookup"><span data-stu-id="6302b-127">The **DeviceSyncError** event notifies you when a problem occurs.</span></span> <span data-ttu-id="6302b-128">O evento **DeviceSyncStateChange** alertará quando o estado do mecanismo de sincronização for alterado para o dispositivo atual.</span><span class="sxs-lookup"><span data-stu-id="6302b-128">The **DeviceSyncStateChange** event alerts you when the synchronization engine has changed state for the current device.</span></span>

<span data-ttu-id="6302b-129">Você pode limitar a quantidade de armazenamento de dispositivo que o Windows Media Player usa para sincronização chamando [IWMPSyncDevice2:: setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo) com o atributo **PercentSpaceReserved** .</span><span class="sxs-lookup"><span data-stu-id="6302b-129">You can limit the amount of device storage that Windows Media Player uses for synchronization by calling [IWMPSyncDevice2::setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo) with the **PercentSpaceReserved** attribute.</span></span> <span data-ttu-id="6302b-130">O uso desta interface requer o Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="6302b-130">Using this interface requires Windows Media Player 11.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6302b-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6302b-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6302b-132">**Sobre a sincronização do dispositivo**</span><span class="sxs-lookup"><span data-stu-id="6302b-132">**About Device Synchronization**</span></span>](about-device-synchronization.md)
</dt> <dt>

[<span data-ttu-id="6302b-133">**Interface IWMPEvents2**</span><span class="sxs-lookup"><span data-stu-id="6302b-133">**IWMPEvents2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[<span data-ttu-id="6302b-134">**Mostrando o progresso da sincronização**</span><span class="sxs-lookup"><span data-stu-id="6302b-134">**Showing Synchronization Progress**</span></span>](showing-synchronization-progress.md)
</dt> </dl>

 

 





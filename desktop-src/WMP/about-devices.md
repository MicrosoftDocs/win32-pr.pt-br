---
title: Sobre dispositivos
description: Sobre dispositivos
ms.assetid: 9e68c5eb-5fcb-4d7d-8dbb-7e951f253df8
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
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e89a074e4edb5bdbc7d90391398d5e0e4133505a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105760903"
---
# <a name="about-devices"></a><span data-ttu-id="47e4e-112">Sobre dispositivos</span><span class="sxs-lookup"><span data-stu-id="47e4e-112">About Devices</span></span>

<span data-ttu-id="47e4e-113">Dispositivos portáteis são dispositivos de hardware que os usuários executam para desfrutar do conteúdo de mídia digital quando estão fora do computador.</span><span class="sxs-lookup"><span data-stu-id="47e4e-113">Portable devices are hardware devices that users carry to enjoy digital media content when they are away from their computer.</span></span> <span data-ttu-id="47e4e-114">Normalmente, os dispositivos portáteis são operados pela bateria.</span><span class="sxs-lookup"><span data-stu-id="47e4e-114">Typically, portable devices are battery operated.</span></span> <span data-ttu-id="47e4e-115">Alguns dispositivos só podem reproduzir música.</span><span class="sxs-lookup"><span data-stu-id="47e4e-115">Some devices can play music only.</span></span> <span data-ttu-id="47e4e-116">Outros dispositivos podem reproduzir vídeo e música.</span><span class="sxs-lookup"><span data-stu-id="47e4e-116">Other devices can play video and music.</span></span>

<span data-ttu-id="47e4e-117">Alguns dispositivos dão suporte à sincronização automática de conteúdo de mídia digital com o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="47e4e-117">Some devices support automatic synchronization of digital media content with Windows Media Player.</span></span> <span data-ttu-id="47e4e-118">Outros dispositivos dão suporte apenas à transferência manual.</span><span class="sxs-lookup"><span data-stu-id="47e4e-118">Other devices support only manual transfer.</span></span> <span data-ttu-id="47e4e-119">Você pode determinar se um dispositivo específico dá suporte à sincronização automática chamando [IWMPSyncDevice:: get \_ status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) e, em seguida, inspecionando o valor de [WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) recuperado.</span><span class="sxs-lookup"><span data-stu-id="47e4e-119">You can determine whether a particular device supports automatic synchronization by calling [IWMPSyncDevice::get\_status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) and then inspecting the [WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) value retrieved.</span></span> <span data-ttu-id="47e4e-120">Se o valor recuperado for **wmpdsManualDevice**, o dispositivo não oferecerá suporte à sincronização automática.</span><span class="sxs-lookup"><span data-stu-id="47e4e-120">If the retrieved value is **wmpdsManualDevice**, the device does not support automatic synchronization.</span></span>

<span data-ttu-id="47e4e-121">Você pode enumerar os dispositivos conectados ao computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="47e4e-121">You can enumerate the devices connected to the user's computer.</span></span> <span data-ttu-id="47e4e-122">Para fazer isso, primeiro use [IWMPSyncServices:: get \_ deviceCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-get_devicecount) para recuperar a contagem de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="47e4e-122">To do this, first use [IWMPSyncServices::get\_deviceCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-get_devicecount) to retrieve the count of devices.</span></span> <span data-ttu-id="47e4e-123">Em seguida, em um loop, chame [IWMPSyncServices:: GetDevice](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-getdevice), passando o valor de índice apropriado a cada vez.</span><span class="sxs-lookup"><span data-stu-id="47e4e-123">Then, in a loop, call [IWMPSyncServices::getDevice](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-getdevice), passing the appropriate index value each time.</span></span> <span data-ttu-id="47e4e-124">Você pode usar [IWMPSyncDevice:: get \_ conectado](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected) para avaliar se um determinado dispositivo está conectado no momento.</span><span class="sxs-lookup"><span data-stu-id="47e4e-124">You can use [IWMPSyncDevice::get\_connected](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected) to evaluate whether a particular device is currently connected.</span></span>

<span data-ttu-id="47e4e-125">Para saber quando os dispositivos se conectam ou se desconectam, você pode receber os eventos **DeviceConnect** e **DeviceDisconnect** .</span><span class="sxs-lookup"><span data-stu-id="47e4e-125">To know when devices connect or disconnect, you can receive the **DeviceConnect** and **DeviceDisconnect** events.</span></span> <span data-ttu-id="47e4e-126">Esses eventos são recebidos por meio da interface **IWMPEvents2** .</span><span class="sxs-lookup"><span data-stu-id="47e4e-126">These events are received through the **IWMPEvents2** interface.</span></span>

<span data-ttu-id="47e4e-127">A interface **IWMPSyncDevice** fornece métodos adicionais para permitir que você obtenha ou defina informações sobre um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="47e4e-127">The **IWMPSyncDevice** interface provides additional methods to enable you to get or set information about a device.</span></span> <span data-ttu-id="47e4e-128">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="47e4e-128">For example:</span></span>

-   <span data-ttu-id="47e4e-129">Os métodos **Get \_ FriendlyName** e **Put \_ FriendlyName** permitem recuperar e especificar o nome do dispositivo definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="47e4e-129">The **get\_FriendlyName** and **put\_FriendlyName** methods enable you to retrieve and specify the user-defined device name.</span></span>
-   <span data-ttu-id="47e4e-130">O método **Get \_ DeviceName** permite que você recupere o nome do dispositivo que os usuários veem no Shell do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="47e4e-130">The **get\_deviceName** method enables you to retrieve the device name that users see in the Windows XP shell.</span></span>
-   <span data-ttu-id="47e4e-131">O método **getItemInfo** permite que você recupere metadados de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="47e4e-131">The **getItemInfo** method enables you to retrieve metadata from devices.</span></span>

## <a name="related-topics"></a><span data-ttu-id="47e4e-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="47e4e-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47e4e-133">**Sobre a sincronização do dispositivo**</span><span class="sxs-lookup"><span data-stu-id="47e4e-133">**About Device Synchronization**</span></span>](about-device-synchronization.md)
</dt> <dt>

[<span data-ttu-id="47e4e-134">**Interface IWMPEvents2**</span><span class="sxs-lookup"><span data-stu-id="47e4e-134">**IWMPEvents2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[<span data-ttu-id="47e4e-135">**Interface IWMPSyncDevice**</span><span class="sxs-lookup"><span data-stu-id="47e4e-135">**IWMPSyncDevice Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[<span data-ttu-id="47e4e-136">**Trabalhando com dispositivos portáteis**</span><span class="sxs-lookup"><span data-stu-id="47e4e-136">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 





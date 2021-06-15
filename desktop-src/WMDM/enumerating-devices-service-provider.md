---
title: Enumerando dispositivos (WMDM)
description: O Windows Media Gerenciador de Dispositivos mantém um cache de dispositivos conectados. Saiba como o Windows Media Gerenciador de Dispositivos mantém ou atualiza seu cache.
ms.assetid: 7602da65-4c98-4766-b206-2129dad4cc2a
keywords:
- Windows Media Gerenciador de Dispositivos, enumerando dispositivos
- Gerenciador de Dispositivos, enumerando dispositivos
- guia de programação, enumerando dispositivos
- provedores de serviços, enumerando dispositivos
- criando provedores de serviços, enumerando dispositivos
- enumerando dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9b2fd3a891e2c52710bd9a2f6d46a78e9eb238
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/14/2021
ms.locfileid: "112067903"
---
# <a name="enumerating-devices-wmdm"></a><span data-ttu-id="8f96c-110">Enumerando dispositivos (WMDM)</span><span class="sxs-lookup"><span data-stu-id="8f96c-110">Enumerating devices (WMDM)</span></span>

<span data-ttu-id="8f96c-111">O Windows Media Gerenciador de Dispositivos mantém um cache de dispositivos conectados que é atualizado quando um aplicativo do Windows Media Gerenciador de Dispositivos é iniciado, quando um dispositivo Plug and Play (PnP) se conecta ou desconecta ou quando o aplicativo chama [**IWMDeviceManager2::Reinicializar**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-reinitialize).</span><span class="sxs-lookup"><span data-stu-id="8f96c-111">Windows Media Device Manager maintains a cache of connected devices that is updated when a Windows Media Device Manager application starts, when a Plug and Play (PnP) device connects or disconnects, or when the application calls [**IWMDeviceManager2::Reinitialize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-reinitialize).</span></span> <span data-ttu-id="8f96c-112">Esse cache é exposto ao aplicativo quando chama [**IWMDeviceManager::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) ou [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2).</span><span class="sxs-lookup"><span data-stu-id="8f96c-112">This cache is exposed to the application when it calls [**IWMDeviceManager::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) or [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2).</span></span> <span data-ttu-id="8f96c-113">Cada dispositivo é exposto ao aplicativo como uma interface [**IWMDMDevice.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)</span><span class="sxs-lookup"><span data-stu-id="8f96c-113">Each device is exposed to the application as an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) interface.</span></span> <span data-ttu-id="8f96c-114">Se o provedor de serviços estiver registrado para lidar com dispositivos PnP, o Windows Media Gerenciador de Dispositivos estará ciente da lista atual de dispositivos conectados.</span><span class="sxs-lookup"><span data-stu-id="8f96c-114">If the service provider is registered to handle PnP devices, Windows Media Device Manager will be aware of the current list of connected devices.</span></span> <span data-ttu-id="8f96c-115">Se o provedor de serviços estiver registrado para lidar com dispositivos não PnP, o provedor de serviços será responsável por descobrir dispositivos anexados.</span><span class="sxs-lookup"><span data-stu-id="8f96c-115">If the service provider is registered to handle non-PnP devices, the service provider is responsible for discovering attached devices.</span></span> <span data-ttu-id="8f96c-116">Um provedor de serviços só pode ser registrado para dispositivos PnP ou não PnP, nunca ambos.</span><span class="sxs-lookup"><span data-stu-id="8f96c-116">A service provider can only be registered for PnP or non-PnP devices, never both.</span></span>

<span data-ttu-id="8f96c-117">As ações a seguir mostram como o Windows Media Gerenciador de Dispositivos mantém ou atualiza seu cache.</span><span class="sxs-lookup"><span data-stu-id="8f96c-117">The following actions show how Windows Media Device Manager maintains or updates its cache.</span></span> <span data-ttu-id="8f96c-118">Observe que o cache nunca é atualizado quando um dispositivo não PnP se conecta ou se desconecta.</span><span class="sxs-lookup"><span data-stu-id="8f96c-118">Notice that the cache is never updated when a non-PnP device connects or disconnects.</span></span>

<span data-ttu-id="8f96c-119">Um aplicativo de Gerenciador de Dispositivos Windows Media é iniciado</span><span class="sxs-lookup"><span data-stu-id="8f96c-119">A Windows Media Device Manager application starts</span></span>

-   <span data-ttu-id="8f96c-120">O Windows Media Gerenciador de Dispositivos recupera uma lista de dispositivos PnP anexados do subsistema PnP e chama [**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) no SP registrado para cada dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="8f96c-120">Windows Media Device Manager retrieves a list of attached PnP devices from the PnP subsystem, and calls [**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) on the SP registered for each connected device.</span></span> <span data-ttu-id="8f96c-121">(Ele descobre o provedor de serviços correto consultando o parâmetro de dispositivo WMDMSPCLSID para a ID de classe do provedor de serviços responsável por esse dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8f96c-121">(It discovers the correct service provider by querying the WMDMSPCLSID device parameter for the class ID of the service provider responsible for this device.</span></span> <span data-ttu-id="8f96c-122">Consulte [Parâmetros de dispositivo](device-parameters.md) para obter mais informações.) Todos os dispositivos retornados são adicionados ao cache Gerenciador de Dispositivos mídia do Windows de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="8f96c-122">See [Device Parameters](device-parameters.md) for more information.) All devices returned are added to the Windows Media Device Manager cache of devices.</span></span>
-   <span data-ttu-id="8f96c-123">O Windows Media Gerenciador de Dispositivos localiza todos os provedores de serviços não PnP registrados com ele e chama [**IMDServiceProvider::EnumDevices em**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices) cada provedor de serviços para obter uma lista de dispositivos de cada um.</span><span class="sxs-lookup"><span data-stu-id="8f96c-123">Windows Media Device Manager finds all non-PnP service providers registered with it and calls [**IMDServiceProvider::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices) on each service provider to get a list devices from each one.</span></span> <span data-ttu-id="8f96c-124">Todos os dispositivos retornados são adicionados ao cache.</span><span class="sxs-lookup"><span data-stu-id="8f96c-124">All devices returned are added to the cache.</span></span>

<span data-ttu-id="8f96c-125">O aplicativo chama IWMDeviceManager/2::EnumDevices/2</span><span class="sxs-lookup"><span data-stu-id="8f96c-125">The application calls IWMDeviceManager/2::EnumDevices/2</span></span>

-   <span data-ttu-id="8f96c-126">O Windows Media Gerenciador de Dispositivos retorna sua lista de dispositivos armazenados em cache.</span><span class="sxs-lookup"><span data-stu-id="8f96c-126">Windows Media Device Manager returns its cached device list.</span></span>

<span data-ttu-id="8f96c-127">Um dispositivo PnP se conecta</span><span class="sxs-lookup"><span data-stu-id="8f96c-127">A PnP device connects</span></span>

-   <span data-ttu-id="8f96c-128">O Windows Media Gerenciador de Dispositivos localiza o provedor de serviços relevante e chama **IMDServiceProvider2::CreateDevice** e adiciona o dispositivo ao cache.</span><span class="sxs-lookup"><span data-stu-id="8f96c-128">Windows Media Device Manager finds the relevant service provider and calls **IMDServiceProvider2::CreateDevice**, and adds the device to its cache.</span></span>
-   <span data-ttu-id="8f96c-129">Se o aplicativo implementar [**IWMDMNotification,**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification)o Windows Media Gerenciador de Dispositivos [**chamará IWMDMNotification::WMDMMessage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmnotification-wmdmmessage) com uma notificação de chegada.</span><span class="sxs-lookup"><span data-stu-id="8f96c-129">If the application implements [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification), Windows Media Device Manager calls [**IWMDMNotification::WMDMMessage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmnotification-wmdmmessage) with an arrival notification.</span></span>

<span data-ttu-id="8f96c-130">Um dispositivo PnP se desconecta</span><span class="sxs-lookup"><span data-stu-id="8f96c-130">A PnP device disconnects</span></span>

-   <span data-ttu-id="8f96c-131">O Windows Media Gerenciador de Dispositivos remove o item de seu cache.</span><span class="sxs-lookup"><span data-stu-id="8f96c-131">Windows Media Device Manager removes the item from its cache.</span></span>
-   <span data-ttu-id="8f96c-132">Se o aplicativo implementar IWMDMNotification, o Windows Media Gerenciador de Dispositivos chamarÁ IWMDMNotification::WMDMMessage com uma notificação de partida.</span><span class="sxs-lookup"><span data-stu-id="8f96c-132">If the application implements IWMDMNotification, Windows Media Device Manager calls IWMDMNotification::WMDMMessage with a departure notification.</span></span>

<span data-ttu-id="8f96c-133">O aplicativo chama IWMDeviceManager2::Reinitialize</span><span class="sxs-lookup"><span data-stu-id="8f96c-133">The application calls IWMDeviceManager2::Reinitialize</span></span>

-   <span data-ttu-id="8f96c-134">Atualiza o cache com todos os dispositivos conectados.</span><span class="sxs-lookup"><span data-stu-id="8f96c-134">Refreshes the cache with all connected devices.</span></span>

<span data-ttu-id="8f96c-135">Um dispositivo não PnP se conecta ou desconecta</span><span class="sxs-lookup"><span data-stu-id="8f96c-135">A non-PnP device connects or disconnects</span></span>

-   <span data-ttu-id="8f96c-136">O Windows Media Gerenciador de Dispositivos não é informado sobre a chegada ou partida e não toma nenhuma ação.</span><span class="sxs-lookup"><span data-stu-id="8f96c-136">Windows Media Device Manager is not informed of the arrival or departure, and takes no action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f96c-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8f96c-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f96c-138">**Criando um provedor de serviços**</span><span class="sxs-lookup"><span data-stu-id="8f96c-138">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> </dl>

 

 





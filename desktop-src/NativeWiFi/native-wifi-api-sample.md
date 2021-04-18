---
description: Demonstra o uso de funções básicas de gerenciamento de rede sem fio.
ms.assetid: 63af0b88-c20b-4b06-9db3-e8510fc80053
title: Exemplo de API WiFi nativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98ac72000363fcb91f013c3f55d4686335c0a59e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760234"
---
# <a name="native-wifi-api-sample"></a><span data-ttu-id="489cb-103">Exemplo de API WiFi nativa</span><span class="sxs-lookup"><span data-stu-id="489cb-103">Native Wifi API Sample</span></span>

<span data-ttu-id="489cb-104">Um exemplo de API WiFi nativo que demonstra o uso de funções básicas de gerenciamento de rede sem fio está incluído no SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="489cb-104">A Native Wifi API sample that demonstrates the use of basic wireless network management functions is included with the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="489cb-105">A versão mais recente do SDK do Windows está disponível no [centro de download](https://developer.microsoft.com/windows/downloads).</span><span class="sxs-lookup"><span data-stu-id="489cb-105">The latest version of the Windows SDK is available from the [Download Center](https://developer.microsoft.com/windows/downloads).</span></span>

<span data-ttu-id="489cb-106">Por padrão, o código-fonte de exemplo WiFi nativo é instalado no seguinte diretório:</span><span class="sxs-lookup"><span data-stu-id="489cb-106">By default, the Native Wifi sample source code is installed in the following directory:</span></span>

<span data-ttu-id="489cb-107">**C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ <version number> \\ amostras \\ NetDs \\ WLAN**</span><span class="sxs-lookup"><span data-stu-id="489cb-107">**C:\\Program Files\\Microsoft SDKs\\Windows\\<version number>\\Samples\\NetDs\\Wlan**</span></span>

<span data-ttu-id="489cb-108">O exemplo de API WiFi nativo está localizado na seguinte pasta:</span><span class="sxs-lookup"><span data-stu-id="489cb-108">The Native Wifi API sample is located under the following folder:</span></span>

<span data-ttu-id="489cb-109">**AutoConfig**</span><span class="sxs-lookup"><span data-stu-id="489cb-109">**autoconfig**</span></span>

<span data-ttu-id="489cb-110">O exemplo de WiFi nativo pode ser compilado e executado no Windows Vista e posterior, no Windows XP com Service Pack 3 (SP3) e na API de LAN sem fio para Windows XP com Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="489cb-110">The Native Wifi sample can be compiled and run on Windows Vista and later, Windows XP with Service Pack 3 (SP3), and Wireless LAN API for Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="489cb-111">Alguns recursos do exemplo não têm suporte no Windows XP com SP3 e na API de LAN sem fio para Windows XP com SP2.</span><span class="sxs-lookup"><span data-stu-id="489cb-111">Some features of the sample are not supported on Windows XP with SP3 and Wireless LAN API for Windows XP with SP2.</span></span> <span data-ttu-id="489cb-112">Para obter uma lista das funções com suporte pelo Windows XP com SP3 e pela API de LAN sem fio para Windows XP com SP2, consulte [suporte nativo à API WiFi no Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md).</span><span class="sxs-lookup"><span data-stu-id="489cb-112">For a list of functions supported by Windows XP with SP3 and Wireless LAN API for Windows XP with SP2, see [Native Wifi API Support on Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md).</span></span>

<span data-ttu-id="489cb-113">O exemplo de WiFi nativo demonstra como executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="489cb-113">The Native Wifi sample demonstrates how to perform the following tasks:</span></span>

-   <span data-ttu-id="489cb-114">Enumere as interfaces sem fio.</span><span class="sxs-lookup"><span data-stu-id="489cb-114">Enumerate wireless interfaces.</span></span> <span data-ttu-id="489cb-115">Consulte [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces).</span><span class="sxs-lookup"><span data-stu-id="489cb-115">See [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces).</span></span>
-   <span data-ttu-id="489cb-116">Obtenha os recursos de uma interface.</span><span class="sxs-lookup"><span data-stu-id="489cb-116">Get the capabilities of an interface.</span></span> <span data-ttu-id="489cb-117">Consulte [**WlanGetInterfaceCapability**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetinterfacecapability).</span><span class="sxs-lookup"><span data-stu-id="489cb-117">See [**WlanGetInterfaceCapability**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetinterfacecapability).</span></span>

    <span data-ttu-id="489cb-118">\* \* Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2: \* \* não há suporte para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="489cb-118">\*\*Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  \*\* This feature is not supported.</span></span>

-   <span data-ttu-id="489cb-119">Consultar uma interface.</span><span class="sxs-lookup"><span data-stu-id="489cb-119">Query an interface.</span></span> <span data-ttu-id="489cb-120">Consulte [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface).</span><span class="sxs-lookup"><span data-stu-id="489cb-120">See [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface).</span></span>
-   <span data-ttu-id="489cb-121">Definir parâmetros para uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="489cb-121">Set parameters for a network interface.</span></span> <span data-ttu-id="489cb-122">Consulte [**WlanSetInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface).</span><span class="sxs-lookup"><span data-stu-id="489cb-122">See [**WlanSetInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface).</span></span> <span data-ttu-id="489cb-123">Essa função pode ser usada para ativar e desativar o rádio sem fio (e, portanto, habilitar ou desabilitar a conectividade de rede sem fio).</span><span class="sxs-lookup"><span data-stu-id="489cb-123">This function can be used to turn the wireless radio on and off (and therefore enable or disable wireless network connectivity).</span></span>
-   <span data-ttu-id="489cb-124">Verificar se há redes sem fio disponíveis.</span><span class="sxs-lookup"><span data-stu-id="489cb-124">Scan for available wireless networks.</span></span> <span data-ttu-id="489cb-125">Consulte [**WlanScan**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan).</span><span class="sxs-lookup"><span data-stu-id="489cb-125">See [**WlanScan**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan).</span></span>
-   <span data-ttu-id="489cb-126">Obtenha a lista de redes sem fio disponíveis ou visíveis.</span><span class="sxs-lookup"><span data-stu-id="489cb-126">Get the list of available or visible wireless networks.</span></span> <span data-ttu-id="489cb-127">Consulte [**WlanGetAvailableNetworkList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist).</span><span class="sxs-lookup"><span data-stu-id="489cb-127">See [**WlanGetAvailableNetworkList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist).</span></span>
-   <span data-ttu-id="489cb-128">Obter, salvar ou excluir um perfil.</span><span class="sxs-lookup"><span data-stu-id="489cb-128">Get, save, or delete a profile.</span></span> <span data-ttu-id="489cb-129">Consulte [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile), [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)e [**WlanDeleteProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile).</span><span class="sxs-lookup"><span data-stu-id="489cb-129">See [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile), [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile), and [**WlanDeleteProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile).</span></span>
-   <span data-ttu-id="489cb-130">Conecte-se ou desconecte-se de uma rede sem fio.</span><span class="sxs-lookup"><span data-stu-id="489cb-130">Connect to or disconnect from a wireless network.</span></span> <span data-ttu-id="489cb-131">Consulte [**WlanConnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect) e [**WlanDisconnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect).</span><span class="sxs-lookup"><span data-stu-id="489cb-131">See [**WlanConnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect) and [**WlanDisconnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect).</span></span>

## <a name="related-topics"></a><span data-ttu-id="489cb-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="489cb-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="489cb-133">Usando WiFi nativo</span><span class="sxs-lookup"><span data-stu-id="489cb-133">Using Native Wifi</span></span>](using-native-wifi.md)
</dt> <dt>

[<span data-ttu-id="489cb-134">Fórum do SDK sem fio do Windows Vista</span><span class="sxs-lookup"><span data-stu-id="489cb-134">Windows Vista Wireless SDK Forum</span></span>](https://social.msdn.microsoft.com/Forums/b6bbd8f0-a921-480f-9b4b-845336462bc0/welcome-to-the-windows-vista-wireless-sdk-forum)
</dt> <dt>

<span data-ttu-id="489cb-135">[Solução de problemas de conexões sem fio do Windows Vista 802,11](/previous-versions/windows/it-pro/windows-vista/cc766215(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="489cb-135">[Troubleshooting Windows Vista 802.11 Wireless Connections](/previous-versions/windows/it-pro/windows-vista/cc766215(v=ws.10))</span></span>
</dt> </dl>

 

 

---
description: A API Wi-Fi nativa contém um conjunto de funções que dão suporte ao uso de Wi-Fi direto para aplicativos de área de trabalho.
ms.assetid: A649EBBA-1076-4426-9C4D-85AB8C415C66
title: Sobre o recurso Wi-Fi Direct
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e503cb2bf86f81904b1c85c2bdf96b66c0762e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785407"
---
# <a name="about-the-wi-fi-direct-feature"></a><span data-ttu-id="4008d-103">Sobre o recurso Wi-Fi Direct</span><span class="sxs-lookup"><span data-stu-id="4008d-103">About the Wi-Fi Direct feature</span></span>

<span data-ttu-id="4008d-104">A API Wi-Fi nativa contém um conjunto de funções que dão suporte ao uso de Wi-Fi direto para aplicativos de área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4008d-104">The Native Wifi API contains a set of functions that support the use of Wi-Fi Direct for desktop apps.</span></span> <span data-ttu-id="4008d-105">A partir do Windows 8 e do Windows Server 2012, Wi-Fi funções diretas foram adicionadas à API WiFi nativa.</span><span class="sxs-lookup"><span data-stu-id="4008d-105">Starting on Windows 8 and Windows Server 2012, Wi-Fi Direct functions were added to the Native Wifi API.</span></span>

<span data-ttu-id="4008d-106">O recurso direto Wi-Fi é baseado no desenvolvimento do Wi-Fi especificação técnica ponto a ponto v 1.1 pela Aliança de Wi-Fi (consulte [especificações publicadas da Wi-Fi Alliance](https://www.wi-fi.org/)).</span><span class="sxs-lookup"><span data-stu-id="4008d-106">The Wi-Fi Direct feature is based on the development of the Wi-Fi Peer-to-Peer Technical Specification v1.1 by the Wi-Fi Alliance (see [Wi-Fi Alliance Published Specifications](https://www.wi-fi.org/)).</span></span> <span data-ttu-id="4008d-107">O objetivo do Wi-Fi especificação técnica ponto a ponto é fornecer uma solução para Wi-Fi conectividade de dispositivo para dispositivo sem a necessidade de um ponto de acesso sem fio (AP sem fio) configurar a conexão ou o uso do mecanismo existente Wi-Fi ad hoc (IBSS).</span><span class="sxs-lookup"><span data-stu-id="4008d-107">The goal of the Wi-Fi Peer-to-Peer Technical Specification is to provide a solution for Wi-Fi device-to-device connectivity without the need for either a Wireless Access Point (wireless AP) to setup the connection or the use of the existing Wi-Fi ad hoc (IBSS) mechanism.</span></span>

> [!Note]  
> <span data-ttu-id="4008d-108">O modo ad hoc pode não estar disponível em versões futuras do Windows.</span><span class="sxs-lookup"><span data-stu-id="4008d-108">Ad hoc mode might not be available in future versions of Windows.</span></span> <span data-ttu-id="4008d-109">A partir do Windows 8.1 e do Windows Server 2012 R2, use Wi-Fi Direct em vez disso.</span><span class="sxs-lookup"><span data-stu-id="4008d-109">Starting with Windows 8.1 and Windows Server 2012 R2, use Wi-Fi Direct instead.</span></span>

 

<span data-ttu-id="4008d-110">Para um aplicativo de desktop, o recurso direto Wi-Fi requer que os dispositivos Wi-FI Direct sejam emparelhados anteriormente pelo usuário com a interface do usuário da experiência de emparelhamento do Windows.</span><span class="sxs-lookup"><span data-stu-id="4008d-110">For a desktop app, the Wi-Fi Direct feature requires that Wi-FI Direct devices be previously paired by the user with the Windows Pairing experience user interface.</span></span> <span data-ttu-id="4008d-111">Após a conclusão desse emparelhamento, é armazenado um perfil que permite que as funções Wi-Fi diretas sejam usadas para iniciar uma sessão Wi-Fi Direct para estabelecer uma conexão entre os dispositivos Wi-Fi Direct.</span><span class="sxs-lookup"><span data-stu-id="4008d-111">Once this pairing is completed, a profile is stored that allows the Wi-Fi Direct functions to be used to start a Wi-Fi Direct session to establish a connection between the Wi-Fi Direct devices.</span></span>

<span data-ttu-id="4008d-112">As funções a seguir dão suporte ao recurso direto Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="4008d-112">The following functions support the Wi-Fi Direct feature.</span></span>

-   <span data-ttu-id="4008d-113">[**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) -indica que o aplicativo deseja cancelar uma função [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) pendente que não foi concluída.</span><span class="sxs-lookup"><span data-stu-id="4008d-113">[**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) - Indicates that the app wants to cancel a pending [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function that has not completed.</span></span>
-   <span data-ttu-id="4008d-114">[**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) -fecha um identificador para o serviço direto Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="4008d-114">[**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) - Closes a handle to the Wi-Fi Direct service.</span></span>
-   <span data-ttu-id="4008d-115">[**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) -fecha uma sessão após uma chamada bem-sucedida anterior à função [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) .</span><span class="sxs-lookup"><span data-stu-id="4008d-115">[**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) - Closes a session after a previously successful call to the [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function.</span></span>
-   <span data-ttu-id="4008d-116">[**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) -abre um identificador para o serviço Wi-Fi Direct e negocia uma versão da API Wi-Fi Direct a ser usada.</span><span class="sxs-lookup"><span data-stu-id="4008d-116">[**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) - Opens a handle to the Wi-Fi Direct service and negotiates a version of the Wi-FI Direct API to use.</span></span>
-   <span data-ttu-id="4008d-117">[**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) – recupera e aplica um perfil armazenado para um Wi-Fi dispositivo herdado direto.</span><span class="sxs-lookup"><span data-stu-id="4008d-117">[**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) - Retrieves and applies a stored profile for a Wi-Fi Direct legacy device.</span></span>
-   <span data-ttu-id="4008d-118">[**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) -inicia uma conexão sob demanda com um dispositivo específico Wi-Fi Direct, que foi anteriormente emparelhado por meio da experiência de emparelhamento do Windows.</span><span class="sxs-lookup"><span data-stu-id="4008d-118">[**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) - Starts an on-demand connection to a specific Wi-Fi Direct device, which has been previously paired through the Windows Pairing experience.</span></span>
-   <span data-ttu-id="4008d-119">[**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) – atualiza a visibilidade do dispositivo para o endereço de dispositivo Wi-Fi direto para um determinado nó de dispositivo Wi-Fi Direct.</span><span class="sxs-lookup"><span data-stu-id="4008d-119">[**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) - Updates device visibility for the Wi-Fi Direct device address for a given installed Wi-Fi Direct device node.</span></span>
-   <span data-ttu-id="4008d-120">[**WFD \_ ABRIR \_ sessão \_ de \_ retorno de chamada concluído**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) – define a função de retorno de chamada que é chamado pela função [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) quando a operação **WFDStartOpenSession** é concluída</span><span class="sxs-lookup"><span data-stu-id="4008d-120">[**WFD\_OPEN\_SESSION\_COMPLETE\_CALLBACK**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) - Defines the callback function that is called by the [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function when the **WFDStartOpenSession** operation completes</span></span>

<span data-ttu-id="4008d-121">Para obter mais informações sobre como usar Wi-Fi diretamente em um aplicativo de área de trabalho, consulte [usando o Wi-Fi funções diretas](using-the-wi-fi-direct-api.md).</span><span class="sxs-lookup"><span data-stu-id="4008d-121">For more information on using Wi-Fi Direct in a desktop app, see [Using the Wi-Fi Direct functions](using-the-wi-fi-direct-api.md).</span></span>

<span data-ttu-id="4008d-122">Para obter mais informações sobre Wi-Fi Direct para uso em aplicativos da Windows Store, consulte [**PeerFinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) e classes relacionadas no namespace [**Windows. Networking. Proximity**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041) .</span><span class="sxs-lookup"><span data-stu-id="4008d-122">For more information on Wi-Fi Direct for use in Windows Store apps, see [**PeerFinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) and related classes in the [**Windows.Networking.Proximity**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041) namespace.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4008d-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4008d-123">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4008d-124">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="4008d-124">**Other resources**</span></span>
</dt> <dt>

[<span data-ttu-id="4008d-125">Sobre WiFi nativo</span><span class="sxs-lookup"><span data-stu-id="4008d-125">About Native Wifi</span></span>](about-native-wifi.md)
</dt> <dt>

[<span data-ttu-id="4008d-126">Sobre a API Wi-Fi nativa</span><span class="sxs-lookup"><span data-stu-id="4008d-126">About the Native Wifi API</span></span>](about-the-native-wifi-api.md)
</dt> <dt>

[<span data-ttu-id="4008d-127">Sobre a API ad hoc sem fio</span><span class="sxs-lookup"><span data-stu-id="4008d-127">About the Wireless Ad Hoc API</span></span>](about-the-wireless-ad-hoc-api.md)
</dt> <dt>

[<span data-ttu-id="4008d-128">Usando o Wi-Fi funções diretas</span><span class="sxs-lookup"><span data-stu-id="4008d-128">Using the Wi-Fi Direct functions</span></span>](using-the-wi-fi-direct-api.md)
</dt> <dt>

<span data-ttu-id="4008d-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="4008d-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4008d-130">**PeerFinder**</span><span class="sxs-lookup"><span data-stu-id="4008d-130">**PeerFinder**</span></span>](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041)
</dt> <dt>

[<span data-ttu-id="4008d-131">**\_retorno de \_ \_ chamada completo de sessão aberta WFD \_**</span><span class="sxs-lookup"><span data-stu-id="4008d-131">**WFD\_OPEN\_SESSION\_COMPLETE\_CALLBACK**</span></span>](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
</dt> <dt>

[<span data-ttu-id="4008d-132">**WFDCancelOpenSession**</span><span class="sxs-lookup"><span data-stu-id="4008d-132">**WFDCancelOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
</dt> <dt>

[<span data-ttu-id="4008d-133">**WFDCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="4008d-133">**WFDCloseHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
</dt> <dt>

[<span data-ttu-id="4008d-134">**WFDCloseSession**</span><span class="sxs-lookup"><span data-stu-id="4008d-134">**WFDCloseSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
</dt> <dt>

[<span data-ttu-id="4008d-135">**WFDOpenHandle**</span><span class="sxs-lookup"><span data-stu-id="4008d-135">**WFDOpenHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
</dt> <dt>

[<span data-ttu-id="4008d-136">**WFDOpenLegacySession**</span><span class="sxs-lookup"><span data-stu-id="4008d-136">**WFDOpenLegacySession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
</dt> <dt>

[<span data-ttu-id="4008d-137">**WFDStartOpenSession**</span><span class="sxs-lookup"><span data-stu-id="4008d-137">**WFDStartOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
</dt> <dt>

[<span data-ttu-id="4008d-138">**WFDUpdateDeviceVisibility**</span><span class="sxs-lookup"><span data-stu-id="4008d-138">**WFDUpdateDeviceVisibility**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)
</dt> <dt>

[<span data-ttu-id="4008d-139">**{1&amp;gt;{2&amp;gt;Windows.Networking.Proximity&amp;lt;2}&amp;lt;1}**</span><span class="sxs-lookup"><span data-stu-id="4008d-139">**Windows.Networking.Proximity**</span></span>](/uwp/api/Windows.Networking.Proximity?view=winrt-19041)
</dt> </dl>

 

 

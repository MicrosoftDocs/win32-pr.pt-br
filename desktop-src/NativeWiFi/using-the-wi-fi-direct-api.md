---
description: Mostra como usar Wi-Fi funções diretas em aplicativos da área de trabalho.
ms.assetid: 50B95B7D-B860-44DF-8E78-1E7D2DC5A9B6
title: Usando o Wi-Fi funções diretas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8850f5b278a158e32f78118cf5d0d408c123192e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753254"
---
# <a name="using-the-wi-fi-direct-functions"></a><span data-ttu-id="6b4f3-103">Usando o Wi-Fi funções diretas</span><span class="sxs-lookup"><span data-stu-id="6b4f3-103">Using the Wi-Fi Direct functions</span></span>

<span data-ttu-id="6b4f3-104">Este tópico mostra como usar Wi-Fi funções diretas em aplicativos da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-104">This topics shows how to use Wi-Fi Direct functions in desktop apps.</span></span> <span data-ttu-id="6b4f3-105">A partir do Windows 8 e do Windows Server 2012, Wi-Fi funções diretas foram adicionadas à API WiFi nativa.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-105">Starting on Windows 8 and Windows Server 2012, Wi-Fi Direct functions were added to the Native Wifi API.</span></span>

<span data-ttu-id="6b4f3-106">O recurso direto Wi-Fi é baseado no desenvolvimento do Wi-Fi especificação técnica ponto a ponto v 1.1 pela Aliança de Wi-Fi (consulte [especificações publicadas da Wi-Fi Alliance](https://www.wi-fi.org/)).</span><span class="sxs-lookup"><span data-stu-id="6b4f3-106">The Wi-Fi Direct feature is based on the development of the Wi-Fi Peer-to-Peer Technical Specification v1.1 by the Wi-Fi Alliance (see [Wi-Fi Alliance Published Specifications](https://www.wi-fi.org/)).</span></span> <span data-ttu-id="6b4f3-107">O objetivo do Wi-Fi especificação técnica ponto a ponto é fornecer uma solução para Wi-Fi conectividade de dispositivo para dispositivo sem a necessidade de um ponto de acesso sem fio (AP sem fio) configurar a conexão ou o uso do mecanismo existente Wi-Fi ad hoc (IBSS).</span><span class="sxs-lookup"><span data-stu-id="6b4f3-107">The goal of the Wi-Fi Peer-to-Peer Technical Specification is to provide a solution for Wi-Fi device-to-device connectivity without the need for either a Wireless Access Point (wireless AP) to setup the connection or the use of the existing Wi-Fi ad hoc (IBSS) mechanism.</span></span>

> [!Note]  
> <span data-ttu-id="6b4f3-108">O modo ad hoc pode não estar disponível em versões futuras do Windows.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-108">Ad hoc mode might not be available in future versions of Windows.</span></span> <span data-ttu-id="6b4f3-109">A partir do Windows 8.1 e do Windows Server 2012 R2, use Wi-Fi Direct em vez disso.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-109">Starting with Windows 8.1 and Windows Server 2012 R2, use Wi-Fi Direct instead.</span></span>

 

<span data-ttu-id="6b4f3-110">As funções a seguir dão suporte ao recurso direto Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-110">The following functions support the Wi-Fi Direct feature.</span></span>

-   <span data-ttu-id="6b4f3-111">[**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) -indica que o aplicativo deseja cancelar uma função [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) pendente que não foi concluída.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-111">[**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) - Indicates that the app wants to cancel a pending [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function that has not completed.</span></span>
-   <span data-ttu-id="6b4f3-112">[**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) -fecha um identificador para o serviço direto Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-112">[**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) - Closes a handle to the Wi-Fi Direct service.</span></span>
-   <span data-ttu-id="6b4f3-113">[**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) -fecha uma sessão após uma chamada bem-sucedida anterior à função [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) .</span><span class="sxs-lookup"><span data-stu-id="6b4f3-113">[**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) - Closes a session after a previously successful call to the [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function.</span></span>
-   <span data-ttu-id="6b4f3-114">[**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) -abre um identificador para o serviço Wi-Fi Direct e negocia uma versão da API Wi-Fi Direct a ser usada.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-114">[**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) - Opens a handle to the Wi-Fi Direct service and negotiates a version of the Wi-FI Direct API to use.</span></span>
-   <span data-ttu-id="6b4f3-115">[**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) – recupera e aplica um perfil armazenado para um Wi-Fi dispositivo herdado direto.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-115">[**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) - Retrieves and applies a stored profile for a Wi-Fi Direct legacy device.</span></span>
-   <span data-ttu-id="6b4f3-116">[**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) -inicia uma conexão sob demanda com um dispositivo específico Wi-Fi Direct, que foi anteriormente emparelhado por meio da experiência de emparelhamento do Windows.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-116">[**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) - Starts an on-demand connection to a specific Wi-Fi Direct device, which has been previously paired through the Windows Pairing experience.</span></span>
-   <span data-ttu-id="6b4f3-117">[**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) – atualiza a visibilidade do dispositivo para o endereço de dispositivo Wi-Fi direto para um determinado nó de dispositivo Wi-Fi Direct.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-117">[**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) - Updates device visibility for the Wi-Fi Direct device address for a given installed Wi-Fi Direct device node.</span></span>
-   <span data-ttu-id="6b4f3-118">[**WFD \_ ABRIR \_ sessão \_ de \_ retorno de chamada concluído**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) – define a função de retorno de chamada que é chamado pela função [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) quando a operação **WFDStartOpenSession** é concluída</span><span class="sxs-lookup"><span data-stu-id="6b4f3-118">[**WFD\_OPEN\_SESSION\_COMPLETE\_CALLBACK**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) - Defines the callback function that is called by the [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function when the **WFDStartOpenSession** operation completes</span></span>

<span data-ttu-id="6b4f3-119">Para um aplicativo de desktop, o recurso direto Wi-Fi requer que os dispositivos Wi-FI Direct sejam emparelhados anteriormente pelo usuário com a interface do usuário da experiência de emparelhamento do Windows.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-119">For a desktop app, the Wi-Fi Direct feature requires that Wi-FI Direct devices be previously paired by the user with the Windows Pairing experience user interface.</span></span> <span data-ttu-id="6b4f3-120">Após a conclusão desse emparelhamento, é armazenado um perfil que permite que as funções Wi-Fi diretas sejam usadas para iniciar uma sessão Wi-Fi Direct para estabelecer uma conexão entre os dispositivos Wi-Fi Direct.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-120">Once this pairing is completed, a profile is stored that allows the Wi-Fi Direct functions to be used to start a Wi-Fi Direct session to establish a connection between the Wi-Fi Direct devices.</span></span>

<span data-ttu-id="6b4f3-121">Para usar o Wi-Fi Direct, um aplicativo deve primeiro obter um identificador para o serviço Wi-Fi Direct chamando a função [**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) .</span><span class="sxs-lookup"><span data-stu-id="6b4f3-121">In order to use Wi-Fi Direct, an app must first obtain a handle to the Wi-Fi Direct service by calling the [**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) function.</span></span> <span data-ttu-id="6b4f3-122">O identificador de Wi-Fi direto (WFD) retornado pela função **WFDOpenHandle** é usado para chamadas de função diretas subsequentes Wi-Fi feitas ao serviço direto Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-122">The Wi-Fi Direct (WFD) handle returned by the **WFDOpenHandle** function is used for subsequent Wi-Fi Direct function calls made to the Wi-Fi Direct service.</span></span>

<span data-ttu-id="6b4f3-123">A função [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) inicia uma operação assíncrona para iniciar uma conexão sob demanda com um dispositivo específico Wi-Fi direto.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-123">The [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function starts an asynchronous operation to start an on-demand connection to a specific Wi-Fi Direct device.</span></span> <span data-ttu-id="6b4f3-124">O dispositivo de Wi-Fi de destino deve ter sido emparelhado anteriormente por meio da experiência de emparelhamento do Windows.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-124">The target Wi-Fi device must previously have been paired through the Windows Pairing experience.</span></span> <span data-ttu-id="6b4f3-125">Quando a operação assíncrona for concluída, a função de retorno de chamada especificada no parâmetro *pfnCallback* será chamada.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-125">When the asynchronous operation completes, the callback function specified in the *pfnCallback* parameter is called.</span></span>

<span data-ttu-id="6b4f3-126">Depois que um aplicativo é feito usando o serviço Wi-Fi Direct, o aplicativo deve chamar a função [**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) para sinalizar para o serviço Wi-Fi Direct que o aplicativo é feito usando o serviço.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-126">Once an application is done using the Wi-Fi Direct service, the application should call the [**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) function to signal to the Wi-Fi Direct service that the application is done using the service.</span></span> <span data-ttu-id="6b4f3-127">Isso permite que o serviço direto do Wi-Fi libere recursos usados pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6b4f3-127">This allows the Wi-Fi Direct service to release resources used by the application.</span></span>

<span data-ttu-id="6b4f3-128">Para obter mais informações sobre Wi-Fi Direct para uso em aplicativos da Windows Store, consulte [**PeerFinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) e classes relacionadas no namespace [**Windows. Networking. Proximity**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041) .</span><span class="sxs-lookup"><span data-stu-id="6b4f3-128">For more information on Wi-Fi Direct for use in Windows Store apps, see [**PeerFinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) and related classes in the [**Windows.Networking.Proximity**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041) namespace.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b4f3-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6b4f3-129">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6b4f3-130">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="6b4f3-130">**Other resources**</span></span>
</dt> <dt>

[<span data-ttu-id="6b4f3-131">Sobre WiFi nativo</span><span class="sxs-lookup"><span data-stu-id="6b4f3-131">About Native Wifi</span></span>](about-native-wifi.md)
</dt> <dt>

[<span data-ttu-id="6b4f3-132">Sobre a API Wi-Fi nativa</span><span class="sxs-lookup"><span data-stu-id="6b4f3-132">About the Native Wifi API</span></span>](about-the-native-wifi-api.md)
</dt> <dt>

[<span data-ttu-id="6b4f3-133">Sobre o recurso Wi-Fi Direct</span><span class="sxs-lookup"><span data-stu-id="6b4f3-133">About the Wi-Fi Direct feature</span></span>](about-the-wi-fi-direct-api.md)
</dt> <dt>

<span data-ttu-id="6b4f3-134">**Referência**</span><span class="sxs-lookup"><span data-stu-id="6b4f3-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6b4f3-135">**PeerFinder**</span><span class="sxs-lookup"><span data-stu-id="6b4f3-135">**PeerFinder**</span></span>](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041)
</dt> <dt>

[<span data-ttu-id="6b4f3-136">**\_retorno de \_ \_ chamada completo de sessão aberta WFD \_**</span><span class="sxs-lookup"><span data-stu-id="6b4f3-136">**WFD\_OPEN\_SESSION\_COMPLETE\_CALLBACK**</span></span>](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
</dt> <dt>

[<span data-ttu-id="6b4f3-137">**WFDCancelOpenSession**</span><span class="sxs-lookup"><span data-stu-id="6b4f3-137">**WFDCancelOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
</dt> <dt>

[<span data-ttu-id="6b4f3-138">**WFDCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="6b4f3-138">**WFDCloseHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
</dt> <dt>

[<span data-ttu-id="6b4f3-139">**WFDCloseSession**</span><span class="sxs-lookup"><span data-stu-id="6b4f3-139">**WFDCloseSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
</dt> <dt>

[<span data-ttu-id="6b4f3-140">**WFDOpenHandle**</span><span class="sxs-lookup"><span data-stu-id="6b4f3-140">**WFDOpenHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
</dt> <dt>

[<span data-ttu-id="6b4f3-141">**WFDOpenLegacySession**</span><span class="sxs-lookup"><span data-stu-id="6b4f3-141">**WFDOpenLegacySession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
</dt> <dt>

[<span data-ttu-id="6b4f3-142">**WFDStartOpenSession**</span><span class="sxs-lookup"><span data-stu-id="6b4f3-142">**WFDStartOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
</dt> <dt>

[<span data-ttu-id="6b4f3-143">**WFDUpdateDeviceVisibility**</span><span class="sxs-lookup"><span data-stu-id="6b4f3-143">**WFDUpdateDeviceVisibility**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)
</dt> <dt>

[<span data-ttu-id="6b4f3-144">**{1&amp;gt;{2&amp;gt;Windows.Networking.Proximity&amp;lt;2}&amp;lt;1}**</span><span class="sxs-lookup"><span data-stu-id="6b4f3-144">**Windows.Networking.Proximity**</span></span>](/uwp/api/Windows.Networking.Proximity?view=winrt-19041)
</dt> </dl>

 

 

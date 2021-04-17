---
description: Novidades no Wi-Fi nativo
ms.assetid: 76d60b95-a34a-4747-b0fa-9230aa60bd63
title: Novidades no Wi-Fi nativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2126627f4cf6431fbac2bf4d1f6ec58561bfd8bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780204"
---
# <a name="whats-new-in-native-wifi"></a><span data-ttu-id="6ec8d-103">Novidades no Wi-Fi nativo</span><span class="sxs-lookup"><span data-stu-id="6ec8d-103">What's New in Native Wifi</span></span>

## <a name="windows-10-version-2004"></a><span data-ttu-id="6ec8d-104">Windows 10, versão 2004</span><span class="sxs-lookup"><span data-stu-id="6ec8d-104">Windows 10, version 2004</span></span>

<span data-ttu-id="6ec8d-105">Consulte [provisionar um perfil de Wi-Fi por meio de um site](prov-wifi-profile-via-website.md).</span><span class="sxs-lookup"><span data-stu-id="6ec8d-105">See [Provision a Wi-Fi profile via a website](prov-wifi-profile-via-website.md).</span></span>

## <a name="windows-10"></a><span data-ttu-id="6ec8d-106">Windows 10</span><span class="sxs-lookup"><span data-stu-id="6ec8d-106">Windows 10</span></span>

<span data-ttu-id="6ec8d-107">O suporte para hotspot 2,0 foi adicionado ao [esquema de \_ perfil WLAN](wlan-profileschema-schema.md).</span><span class="sxs-lookup"><span data-stu-id="6ec8d-107">Support for Hotspot 2.0 has been added to the [WLAN\_profile schema](wlan-profileschema-schema.md).</span></span> <span data-ttu-id="6ec8d-108">O HotSpot 2,0 permite a conexão automática a serviços de Wi-Fi públicos usando credenciais existentes e associação em redes de provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="6ec8d-108">Hotspot 2.0 enables automatic connection to public Wi-Fi services using existing credentials and membership in service provider networks.</span></span> <span data-ttu-id="6ec8d-109">Os provedores de serviço especificam como as conexões são feitas usando os novos elementos de esquema para descrever quais redes usar e como se autenticar neles.</span><span class="sxs-lookup"><span data-stu-id="6ec8d-109">Service providers specify how connections are made using the new schema elements to describe which networks to use, and how to authenticate to them.</span></span> <span data-ttu-id="6ec8d-110">Consulte a documentação do elemento [**Hotspot2**](wlan-profileschema-hotspot2-element.md) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="6ec8d-110">See the [**Hotspot2**](wlan-profileschema-hotspot2-element.md) element documentation for details.</span></span>

## <a name="windows-8-and-windows-server-2012"></a><span data-ttu-id="6ec8d-111">Windows 8 e Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6ec8d-111">Windows 8 and Windows Server 2012</span></span>

<span data-ttu-id="6ec8d-112">Os recursos a seguir foram adicionados às APIs nativas do wifi no Windows 8 e no Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="6ec8d-112">The following features have been added to the Native Wifi APIs on Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="6ec8d-113">Um Wi-Fi recurso direto com base no desenvolvimento do Wi-Fi especificação técnica ponto a ponto v 1.1 pela Aliança de Wi-Fi (consulte [especificações publicadas da Wi-Fi Alliance](https://www.wi-fi.org/)).</span><span class="sxs-lookup"><span data-stu-id="6ec8d-113">A Wi-Fi Direct feature based on the development of the Wi-Fi Peer-to-Peer Technical Specification v1.1 by the Wi-Fi Alliance (see [Wi-Fi Alliance Published Specifications](https://www.wi-fi.org/)).</span></span> <span data-ttu-id="6ec8d-114">O objetivo do Wi-Fi especificação técnica ponto a ponto é fornecer uma solução para Wi-Fi conectividade de dispositivo para dispositivo sem a necessidade de um ponto de acesso sem fio (AP sem fio) configurar a conexão ou o uso do mecanismo existente Wi-Fi adhoc (IBSS).</span><span class="sxs-lookup"><span data-stu-id="6ec8d-114">The goal of the Wi-Fi Peer-to-Peer Technical Specification is to provide a solution for Wi-Fi device-to-device connectivity without the need for either a Wireless Access Point (wireless AP) to setup the connection or the use of the existing Wi-Fi adhoc (IBSS) mechanism.</span></span>

<span data-ttu-id="6ec8d-115">As funções a seguir dão suporte ao recurso direto Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="6ec8d-115">The following functions support the Wi-Fi Direct feature.</span></span>

-   [<span data-ttu-id="6ec8d-116">**\_retorno de \_ \_ chamada completo de sessão aberta WFD \_**</span><span class="sxs-lookup"><span data-stu-id="6ec8d-116">**WFD\_OPEN\_SESSION\_COMPLETE\_CALLBACK**</span></span>](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
-   [<span data-ttu-id="6ec8d-117">**WFDCancelOpenSession**</span><span class="sxs-lookup"><span data-stu-id="6ec8d-117">**WFDCancelOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
-   [<span data-ttu-id="6ec8d-118">**WFDCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="6ec8d-118">**WFDCloseHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
-   [<span data-ttu-id="6ec8d-119">**WFDCloseSession**</span><span class="sxs-lookup"><span data-stu-id="6ec8d-119">**WFDCloseSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
-   [<span data-ttu-id="6ec8d-120">**WFDOpenHandle**</span><span class="sxs-lookup"><span data-stu-id="6ec8d-120">**WFDOpenHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
-   [<span data-ttu-id="6ec8d-121">**WFDOpenLegacySession**</span><span class="sxs-lookup"><span data-stu-id="6ec8d-121">**WFDOpenLegacySession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
-   [<span data-ttu-id="6ec8d-122">**WFDStartOpenSession**</span><span class="sxs-lookup"><span data-stu-id="6ec8d-122">**WFDStartOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
-   [<span data-ttu-id="6ec8d-123">**WFDUpdateDeviceVisibility**</span><span class="sxs-lookup"><span data-stu-id="6ec8d-123">**WFDUpdateDeviceVisibility**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)

## <a name="windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="6ec8d-124">Windows 7 e Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6ec8d-124">Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="6ec8d-125">Os recursos a seguir foram adicionados às APIs nativas do wifi no Windows 7 e no Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="6ec8d-125">The following features have been added to the Native Wifi APIs on Windows 7 and Windows Server 2008 R2.</span></span>

<span data-ttu-id="6ec8d-126">A rede hospedada sem fio permite que um único adaptador sem fio físico se conecte como um cliente a um ponto de acesso de hardware (AP), ao mesmo tempo que atua como um AP de software, permitindo que outros dispositivos com capacidade de conexão sem fio se conectem a ele.</span><span class="sxs-lookup"><span data-stu-id="6ec8d-126">The wireless Hosted Network allows a single physical wireless adapter to connect as a client to a hardware access point (AP), while at the same time acting as a software AP allowing other wireless-capable devices to connect to it.</span></span>

<span data-ttu-id="6ec8d-127">As funções a seguir dão suporte ao recurso de rede hospedada sem fio.</span><span class="sxs-lookup"><span data-stu-id="6ec8d-127">The following functions support the wireless Hosted Network feature.</span></span>

-   [<span data-ttu-id="6ec8d-128">**WlanHostedNetworkForceStart**</span><span class="sxs-lookup"><span data-stu-id="6ec8d-128">**WlanHostedNetworkForceStart**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)
-   [<span data-ttu-id="6ec8d-129">**WlanHostedNetworkForceStop**</span><span class="sxs-lookup"><span data-stu-id="6ec8d-129">**WlanHostedNetworkForceStop**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop)
-   [<span data-ttu-id="6ec8d-130">**WlanHostedNetworkInitSettings**</span><span class="sxs-lookup"><span data-stu-id="6ec8d-130">**WlanHostedNetworkInitSettings**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)
-   [<span data-ttu-id="6ec8d-131">**WlanHostedNetworkQueryProperty**</span><span class="sxs-lookup"><span data-stu-id="6ec8d-131">**WlanHostedNetworkQueryProperty**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)
-   [<span data-ttu-id="6ec8d-132">**WlanHostedNetworkQuerySecondaryKey**</span><span class="sxs-lookup"><span data-stu-id="6ec8d-132">**WlanHostedNetworkQuerySecondaryKey**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey)
-   [<span data-ttu-id="6ec8d-133">**WlanHostedNetworkQueryStatus**</span><span class="sxs-lookup"><span data-stu-id="6ec8d-133">**WlanHostedNetworkQueryStatus**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus)
-   [<span data-ttu-id="6ec8d-134">**WlanHostedNetworkRefreshSecuritySettings**</span><span class="sxs-lookup"><span data-stu-id="6ec8d-134">**WlanHostedNetworkRefreshSecuritySettings**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)
-   [<span data-ttu-id="6ec8d-135">**WlanHostedNetworkSetProperty**</span><span class="sxs-lookup"><span data-stu-id="6ec8d-135">**WlanHostedNetworkSetProperty**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetproperty)
-   [<span data-ttu-id="6ec8d-136">**WlanHostedNetworkSetSecondaryKey**</span><span class="sxs-lookup"><span data-stu-id="6ec8d-136">**WlanHostedNetworkSetSecondaryKey**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey)
-   [<span data-ttu-id="6ec8d-137">**WlanHostedNetworkStartUsing**</span><span class="sxs-lookup"><span data-stu-id="6ec8d-137">**WlanHostedNetworkStartUsing**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)
-   [<span data-ttu-id="6ec8d-138">**WlanHostedNetworkStopUsing**</span><span class="sxs-lookup"><span data-stu-id="6ec8d-138">**WlanHostedNetworkStopUsing**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)
-   [<span data-ttu-id="6ec8d-139">**WlanRegisterVirtualStationNotification**</span><span class="sxs-lookup"><span data-stu-id="6ec8d-139">**WlanRegisterVirtualStationNotification**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanregistervirtualstationnotification)

<span data-ttu-id="6ec8d-140">As novas estruturas a seguir funcionam com a rede hospedada sem fio.</span><span class="sxs-lookup"><span data-stu-id="6ec8d-140">The following new structures that work with wireless Hosted Network.</span></span>

-   [<span data-ttu-id="6ec8d-141">**\_configurações de \_ conexão de rede hospedada da \_ WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="6ec8d-141">**WLAN\_HOSTED\_NETWORK\_CONNECTION\_SETTINGS**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_connection_settings)
-   [<span data-ttu-id="6ec8d-142">**\_alteração de \_ \_ estado de par de dados de rede \_ hospedado \_ da WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="6ec8d-142">**WLAN\_HOSTED\_NETWORK\_DATA\_PEER\_STATE\_CHANGE**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_data_peer_state_change)
-   [<span data-ttu-id="6ec8d-143">**\_estado de \_ par de rede hospedada da \_ WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="6ec8d-143">**WLAN\_HOSTED\_NETWORK\_PEER\_STATE**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_peer_state)
-   [<span data-ttu-id="6ec8d-144">**\_estado de \_ rádio da rede hospedada da \_ WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="6ec8d-144">**WLAN\_HOSTED\_NETWORK\_RADIO\_STATE**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_radio_state)
-   [<span data-ttu-id="6ec8d-145">**\_configurações de \_ segurança de rede hospedada da \_ WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="6ec8d-145">**WLAN\_HOSTED\_NETWORK\_SECURITY\_SETTINGS**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_security_settings)
-   [<span data-ttu-id="6ec8d-146">**\_alteração de \_ estado da rede hospedada pela \_ WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="6ec8d-146">**WLAN\_HOSTED\_NETWORK\_STATE\_CHANGE**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_state_change)
-   [<span data-ttu-id="6ec8d-147">**\_status da \_ rede hospedada da WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="6ec8d-147">**WLAN\_HOSTED\_NETWORK\_STATUS**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_status)

<span data-ttu-id="6ec8d-148">As novas enumerações a seguir funcionam com a rede hospedada sem fio.</span><span class="sxs-lookup"><span data-stu-id="6ec8d-148">The following new enumerations that work with wireless Hosted Network.</span></span>

-   [<span data-ttu-id="6ec8d-149">**\_código de \_ notificação de rede hospedada da \_ WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="6ec8d-149">**WLAN\_HOSTED\_NETWORK\_NOTIFICATION\_CODE**</span></span>](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_notification_code)
-   [<span data-ttu-id="6ec8d-150">**\_opcode de \_ rede hospedada da WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="6ec8d-150">**WLAN\_HOSTED\_NETWORK\_OPCODE**</span></span>](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_opcode)
-   [<span data-ttu-id="6ec8d-151">**\_estado de \_ \_ autenticação de mesmo nível de rede HOSPEDAda da \_ WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="6ec8d-151">**WLAN\_HOSTED\_NETWORK\_PEER\_AUTH\_STATE**</span></span>](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_peer_auth_state)
-   [<span data-ttu-id="6ec8d-152">**\_motivo da \_ rede hospedada da WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="6ec8d-152">**WLAN\_HOSTED\_NETWORK\_REASON**</span></span>](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_reason)
-   [<span data-ttu-id="6ec8d-153">**\_estado da \_ rede hospedada da WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="6ec8d-153">**WLAN\_HOSTED\_NETWORK\_STATE**</span></span>](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_state)

## <a name="related-topics"></a><span data-ttu-id="6ec8d-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6ec8d-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ec8d-155">Sobre a rede hospedada sem fio</span><span class="sxs-lookup"><span data-stu-id="6ec8d-155">About the Wireless Hosted Network</span></span>](about-the-wireless-hosted-network.md)
</dt> <dt>

[<span data-ttu-id="6ec8d-156">Usando rede hospedada sem fio e compartilhamento de conexão com a Internet</span><span class="sxs-lookup"><span data-stu-id="6ec8d-156">Using Wireless Hosted Network and Internet Connection Sharing</span></span>](using-hosted-network-and-internet-connection-sharing.md)
</dt> </dl>

 

 




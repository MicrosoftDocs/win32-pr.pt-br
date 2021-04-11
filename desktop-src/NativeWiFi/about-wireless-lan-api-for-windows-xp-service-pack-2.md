---
description: Há suporte para um subconjunto da funcionalidade nativa da API WiFi no Windows XP com Service Pack 2 (SP2) e no Windows XP com Service Pack 3 (SP3).
ms.assetid: d32c4a03-59e8-4fdd-9d5a-e7ef0eb25e84
title: Suporte nativo à API WiFi no Windows XP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cd422c6589b37f516b9d45d072489c9d5e00b82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296851"
---
# <a name="native-wifi-api-support-on-windows-xp"></a><span data-ttu-id="280b2-103">Suporte nativo à API WiFi no Windows XP</span><span class="sxs-lookup"><span data-stu-id="280b2-103">Native Wifi API Support on Windows XP</span></span>

<span data-ttu-id="280b2-104">Há suporte para um subconjunto da funcionalidade nativa da API WiFi no Windows XP com Service Pack 2 (SP2) e no Windows XP com Service Pack 3 (SP3).</span><span class="sxs-lookup"><span data-stu-id="280b2-104">A subset of the Native Wifi API functionality is supported on Windows XP with Service Pack 2 (SP2) and Windows XP with Service Pack 3 (SP3).</span></span> <span data-ttu-id="280b2-105">Por padrão, essa funcionalidade está incluída no Windows XP com SP3.</span><span class="sxs-lookup"><span data-stu-id="280b2-105">This functionality is included in Windows XP with SP3 by default.</span></span> <span data-ttu-id="280b2-106">No Windows XP com SP2, essa funcionalidade pode ser adicionada aplicando-se um hotfix, que é conhecido como API de LAN sem fio para Windows XP com Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="280b2-106">In Windows XP with SP2, this functionality can be added by applying a hotfix, which is known as Wireless LAN API for Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="280b2-107">Para obter mais informações ou baixar o hotfix, consulte "os desenvolvedores não podem criar programas de cliente sem fio que gerenciam perfis e conexões sem fio por meio do serviço de configuração zero sem fio no Microsoft Windows XP Service Pack 2 (SP2)" na base de dados de conhecimento de ajuda e suporte em [https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997) .</span><span class="sxs-lookup"><span data-stu-id="280b2-107">For more information or to download the hotfix, see "Developers cannot create wireless client programs that manage wireless profiles and connections over the Wireless Zero Configuration service in Microsoft Windows XP Service Pack 2 (SP2)" in the Help and Support Knowledge Base at [https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997).</span></span>

<span data-ttu-id="280b2-108">Devido a diferenças arquitetônicas subjacentes no Windows XP, a API Wi-Fi nativa no tem algumas limitações.</span><span class="sxs-lookup"><span data-stu-id="280b2-108">Because of underlying architectural differences in Windows XP, the Native Wifi API on has some limitations.</span></span> <span data-ttu-id="280b2-109">Aqui está uma lista de limitações:</span><span class="sxs-lookup"><span data-stu-id="280b2-109">Here is a list of limitations:</span></span>

-   <span data-ttu-id="280b2-110">No máximo um SSID pode ser associado a um perfil.</span><span class="sxs-lookup"><span data-stu-id="280b2-110">At most one SSID can be associated with a profile.</span></span>
-   <span data-ttu-id="280b2-111">As redes de infraestrutura sempre aparecem antes das redes ad hoc na lista de perfis.</span><span class="sxs-lookup"><span data-stu-id="280b2-111">Infrastructure networks always appear before ad hoc networks in the profile list.</span></span>
-   <span data-ttu-id="280b2-112">Os nomes de perfil são derivados do SSID e não podem ser definidos pelo usuário para uma cadeia de caracteres arbitrária.</span><span class="sxs-lookup"><span data-stu-id="280b2-112">Profile names are derived from the SSID, and cannot be set by the user to an arbitrary string.</span></span>
-   <span data-ttu-id="280b2-113">Não há suporte para tipos PHY.</span><span class="sxs-lookup"><span data-stu-id="280b2-113">PHY types are not supported.</span></span>
-   <span data-ttu-id="280b2-114">Não há suporte para o cache de PMK (chave mestra de paridade).</span><span class="sxs-lookup"><span data-stu-id="280b2-114">Pairwise master key (PMK) caching is not supported.</span></span>
-   <span data-ttu-id="280b2-115">Não há suporte para funções de extensibilidade de fornecedor de hardware independente (IHV).</span><span class="sxs-lookup"><span data-stu-id="280b2-115">Independent hardware vendor (IHV) extensibility functions are not supported.</span></span>
-   <span data-ttu-id="280b2-116">Não há suporte para permissões de perfil.</span><span class="sxs-lookup"><span data-stu-id="280b2-116">Profile permissions are not supported.</span></span>
-   <span data-ttu-id="280b2-117">Somente a conexão do ACM de notificação da WLAN \_ \_ \_ \_ foi concluída e as notificações de notificação de WLAN \_ \_ ACM \_ desconectadas estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="280b2-117">Only the wlan\_notification\_acm\_connection\_complete and the wlan\_notification\_acm\_disconnected notifications are available.</span></span>
-   <span data-ttu-id="280b2-118">Não há suporte para definições de configuração global 802.1 X e EAPOL.</span><span class="sxs-lookup"><span data-stu-id="280b2-118">Global 802.1X and EAPOL configuration settings are not supported.</span></span>

<span data-ttu-id="280b2-119">As funções a seguir têm suporte do Windows XP com SP3 e da API de LAN sem fio para Windows XP com SP2:</span><span class="sxs-lookup"><span data-stu-id="280b2-119">The following functions are supported by Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:</span></span>

-   [<span data-ttu-id="280b2-120">**retorno de chamada de \_ notificação de WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="280b2-120">**WLAN\_NOTIFICATION\_CALLBACK**</span></span>](/windows/win32/api/wlanapi/nc-wlanapi-wlan_notification_callback)
-   [<span data-ttu-id="280b2-121">**WlanAllocateMemory**</span><span class="sxs-lookup"><span data-stu-id="280b2-121">**WlanAllocateMemory**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanallocatememory)
-   [<span data-ttu-id="280b2-122">**WlanCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="280b2-122">**WlanCloseHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle)
-   [<span data-ttu-id="280b2-123">**WlanConnect**</span><span class="sxs-lookup"><span data-stu-id="280b2-123">**WlanConnect**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect)
-   [<span data-ttu-id="280b2-124">**WlanDeleteProfile**</span><span class="sxs-lookup"><span data-stu-id="280b2-124">**WlanDeleteProfile**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile)
-   [<span data-ttu-id="280b2-125">**WlanDisconnect**</span><span class="sxs-lookup"><span data-stu-id="280b2-125">**WlanDisconnect**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect)
-   [<span data-ttu-id="280b2-126">**WlanEnumInterfaces**</span><span class="sxs-lookup"><span data-stu-id="280b2-126">**WlanEnumInterfaces**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces)
-   [<span data-ttu-id="280b2-127">**WlanFreeMemory**</span><span class="sxs-lookup"><span data-stu-id="280b2-127">**WlanFreeMemory**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanfreememory)
-   [<span data-ttu-id="280b2-128">**WlanGetAvailableNetworkList**</span><span class="sxs-lookup"><span data-stu-id="280b2-128">**WlanGetAvailableNetworkList**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist)
-   [<span data-ttu-id="280b2-129">**WlanGetProfile**</span><span class="sxs-lookup"><span data-stu-id="280b2-129">**WlanGetProfile**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)
-   [<span data-ttu-id="280b2-130">**WlanGetProfileList**</span><span class="sxs-lookup"><span data-stu-id="280b2-130">**WlanGetProfileList**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilelist)
-   [<span data-ttu-id="280b2-131">**WlanOpenHandle**</span><span class="sxs-lookup"><span data-stu-id="280b2-131">**WlanOpenHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle)
-   [<span data-ttu-id="280b2-132">**WlanQueryInterface**</span><span class="sxs-lookup"><span data-stu-id="280b2-132">**WlanQueryInterface**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface)
-   [<span data-ttu-id="280b2-133">**WlanReasonCodeToString**</span><span class="sxs-lookup"><span data-stu-id="280b2-133">**WlanReasonCodeToString**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanreasoncodetostring)
-   [<span data-ttu-id="280b2-134">**WlanRegisterNotification**</span><span class="sxs-lookup"><span data-stu-id="280b2-134">**WlanRegisterNotification**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification)
-   [<span data-ttu-id="280b2-135">**WlanScan**</span><span class="sxs-lookup"><span data-stu-id="280b2-135">**WlanScan**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan)
-   [<span data-ttu-id="280b2-136">**WlanSetInterface**</span><span class="sxs-lookup"><span data-stu-id="280b2-136">**WlanSetInterface**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface)
-   [<span data-ttu-id="280b2-137">**WlanSetProfile**</span><span class="sxs-lookup"><span data-stu-id="280b2-137">**WlanSetProfile**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)
-   [<span data-ttu-id="280b2-138">**WlanSetProfileEapXmlUserData**</span><span class="sxs-lookup"><span data-stu-id="280b2-138">**WlanSetProfileEapXmlUserData**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileeapxmluserdata)
-   [<span data-ttu-id="280b2-139">**WlanSetProfileList**</span><span class="sxs-lookup"><span data-stu-id="280b2-139">**WlanSetProfileList**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist)
-   [<span data-ttu-id="280b2-140">**WlanSetProfilePosition**</span><span class="sxs-lookup"><span data-stu-id="280b2-140">**WlanSetProfilePosition**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition)

## <a name="related-topics"></a><span data-ttu-id="280b2-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="280b2-141">Related topics</span></span>

<dl> <dt>

[https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997)
</dt> <dt>

[<span data-ttu-id="280b2-142">Sobre WiFi nativo</span><span class="sxs-lookup"><span data-stu-id="280b2-142">About Native Wifi</span></span>](about-native-wifi.md)
</dt> </dl>

 

 

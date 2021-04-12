---
title: O que há de novo na plataforma de filtragem do Windows
description: O Windows 8 e o Windows Server 2012 apresentam novos elementos de programação da plataforma de filtragem do Windows.
ms.assetid: 7529F155-3DBC-4C22-A780-B6311C455E85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b5e441eff3242b530401235b085a1486527b98
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "104294659"
---
# <a name="whats-new-in-windows-filtering-platform"></a><span data-ttu-id="dbee7-103">O que há de novo na plataforma de filtragem do Windows</span><span class="sxs-lookup"><span data-stu-id="dbee7-103">What's New in Windows Filtering Platform</span></span>

<span data-ttu-id="dbee7-104">O Windows 8 e o Windows Server 2012 apresentam novos elementos de programação da plataforma de filtragem do Windows.</span><span class="sxs-lookup"><span data-stu-id="dbee7-104">Windows 8 and Windows Server 2012 introduce new Windows Filtering Platform programming elements.</span></span> <span data-ttu-id="dbee7-105">A nova funcionalidade inclui o seguinte:</span><span class="sxs-lookup"><span data-stu-id="dbee7-105">New functionality includes the following:</span></span>

-   <span data-ttu-id="dbee7-106">*Filtragem de camada 2*: fornece acesso à camada L2 (Mac), permitindo a filtragem de tráfego nessa camada.</span><span class="sxs-lookup"><span data-stu-id="dbee7-106">*Layer 2 filtering*: Provides access to the L2 (MAC) layer, allowing filtering of traffic at that layer.</span></span>
-   <span data-ttu-id="dbee7-107">*filtragem de vSwitch*: permite que os pacotes que atravessam um vSwitch sejam inspecionados e/ou modificados.</span><span class="sxs-lookup"><span data-stu-id="dbee7-107">*vSwitch filtering*: Allows packets traversing a vSwitch to be inspected and/or modified.</span></span> <span data-ttu-id="dbee7-108">Os filtros WFP ou os textos explicativos podem ser usados na entrada e saída do vSwitch.</span><span class="sxs-lookup"><span data-stu-id="dbee7-108">WFP filters or callouts can be used at the vSwitch ingress and egress.</span></span>
-   <span data-ttu-id="dbee7-109">*Gerenciamento de contêiner de aplicativos*: permite o acesso a informações sobre os contêineres de aplicativos e problemas de conectividade de isolamento de rede.</span><span class="sxs-lookup"><span data-stu-id="dbee7-109">*App container management*: Allows access to information about app containers and network isolation connectivity issues.</span></span>
-   <span data-ttu-id="dbee7-110">*Atualizações de IPSec*: funcionalidade de IPSec estendida, incluindo monitoramento de estado de conexão, seleção de certificado e gerenciamento de chaves.</span><span class="sxs-lookup"><span data-stu-id="dbee7-110">*IPsec updates*: Extended IPsec functionality including connection state monitoring, certificate selection, and key management.</span></span>

<span data-ttu-id="dbee7-111">O Windows Driver Kit também inclui informações sobre [alterações de WFP para o Windows 8](/windows-hardware/drivers/network/wfp-changes-for-windows-8).</span><span class="sxs-lookup"><span data-stu-id="dbee7-111">The Windows Driver Kit also includes information on [WFP Changes for Windows 8](/windows-hardware/drivers/network/wfp-changes-for-windows-8).</span></span>

## <a name="windows-8-api-updates"></a><span data-ttu-id="dbee7-112">Atualizações de API do Windows 8</span><span class="sxs-lookup"><span data-stu-id="dbee7-112">Windows 8 API updates</span></span>

<span data-ttu-id="dbee7-113">Muitas novas APIs foram adicionadas para o Windows 8 e o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="dbee7-113">Many new APIs have been added for Windows 8 and Windows Server 2012.</span></span>

## <a name="new-functions"></a><span data-ttu-id="dbee7-114">Novas funções</span><span class="sxs-lookup"><span data-stu-id="dbee7-114">New functions</span></span>

-   [<span data-ttu-id="dbee7-115">**FWPM \_ net \_ Event \_ CALLBACK1**</span><span class="sxs-lookup"><span data-stu-id="dbee7-115">**FWPM\_NET\_EVENT\_CALLBACK1**</span></span>](/windows/desktop/api/fwpmu/nc-fwpmu-fwpm_net_event_callback1)
-   [<span data-ttu-id="dbee7-116">**FwpmConnectionCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="dbee7-116">**FwpmConnectionCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectioncreateenumhandle0)
-   [<span data-ttu-id="dbee7-117">**FwpmConnectionDestroyEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="dbee7-117">**FwpmConnectionDestroyEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiondestroyenumhandle0)
-   [<span data-ttu-id="dbee7-118">**FwpmConnectionEnum0**</span><span class="sxs-lookup"><span data-stu-id="dbee7-118">**FwpmConnectionEnum0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionenum0)
-   [<span data-ttu-id="dbee7-119">**FwpmConnectionGetById0**</span><span class="sxs-lookup"><span data-stu-id="dbee7-119">**FwpmConnectionGetById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiongetbyid0)
-   [<span data-ttu-id="dbee7-120">**FwpmConnectionGetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="dbee7-120">**FwpmConnectionGetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiongetsecurityinfo0)
-   [<span data-ttu-id="dbee7-121">**FwpmConnectionSetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="dbee7-121">**FwpmConnectionSetSecurityInfo0**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmconnectionsetsecurityinfo0)
-   [<span data-ttu-id="dbee7-122">**FwpmConnectionSubscribe0**</span><span class="sxs-lookup"><span data-stu-id="dbee7-122">**FwpmConnectionSubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionsubscribe0)
-   [<span data-ttu-id="dbee7-123">**FwpmConnectionSubscriptionsGet0**</span><span class="sxs-lookup"><span data-stu-id="dbee7-123">**FwpmConnectionSubscriptionsGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionsubscriptionsget0)
-   [<span data-ttu-id="dbee7-124">**FwpmConnectionUnsubscribe0**</span><span class="sxs-lookup"><span data-stu-id="dbee7-124">**FwpmConnectionUnsubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionunsubscribe0)
-   [<span data-ttu-id="dbee7-125">**FwpmIPsecTunnelAdd2**</span><span class="sxs-lookup"><span data-stu-id="dbee7-125">**FwpmIPsecTunnelAdd2**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmipsectunneladd2)
-   [<span data-ttu-id="dbee7-126">**FwpmNetEventEnum2**</span><span class="sxs-lookup"><span data-stu-id="dbee7-126">**FwpmNetEventEnum2**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2)
-   [<span data-ttu-id="dbee7-127">**FwpmNetEventSubscribe1**</span><span class="sxs-lookup"><span data-stu-id="dbee7-127">**FwpmNetEventSubscribe1**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventsubscribe1)
-   [<span data-ttu-id="dbee7-128">**FwpmProviderContextAdd2**</span><span class="sxs-lookup"><span data-stu-id="dbee7-128">**FwpmProviderContextAdd2**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextadd2)
-   [<span data-ttu-id="dbee7-129">**FwpmProviderContextEnum2**</span><span class="sxs-lookup"><span data-stu-id="dbee7-129">**FwpmProviderContextEnum2**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextenum2)
-   [<span data-ttu-id="dbee7-130">**FwpmProviderContextGetById2**</span><span class="sxs-lookup"><span data-stu-id="dbee7-130">**FwpmProviderContextGetById2**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextgetbyid2)
-   [<span data-ttu-id="dbee7-131">**FwpmProviderContextGetByKey2**</span><span class="sxs-lookup"><span data-stu-id="dbee7-131">**FwpmProviderContextGetByKey2**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbykey2)
-   [<span data-ttu-id="dbee7-132">**FwpmvSwitchEventsGetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="dbee7-132">**FwpmvSwitchEventsGetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventsgetsecurityinfo0)
-   [<span data-ttu-id="dbee7-133">**FwpmvSwitchEventsSetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="dbee7-133">**FwpmvSwitchEventsSetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventssetsecurityinfo0)
-   [<span data-ttu-id="dbee7-134">**FwpmvSwitchEventSubscribe0**</span><span class="sxs-lookup"><span data-stu-id="dbee7-134">**FwpmvSwitchEventSubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventsubscribe0)
-   [<span data-ttu-id="dbee7-135">**FwpmvSwitchEventUnsubscribe0**</span><span class="sxs-lookup"><span data-stu-id="dbee7-135">**FwpmvSwitchEventUnsubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventunsubscribe0)
-   [<span data-ttu-id="dbee7-136">**IkeextSaEnum2**</span><span class="sxs-lookup"><span data-stu-id="dbee7-136">**IkeextSaEnum2**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum2)
-   [<span data-ttu-id="dbee7-137">**IkeextSaGetById2**</span><span class="sxs-lookup"><span data-stu-id="dbee7-137">**IkeextSaGetById2**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid2)
-   [<span data-ttu-id="dbee7-138">**\_Chave do Gerenciador de chaves IPSec \_ \_ \_ ditado \_ CHECK0**</span><span class="sxs-lookup"><span data-stu-id="dbee7-138">**IPSEC\_KEY\_MANAGER\_KEY\_DICTATION\_CHECK0**</span></span>](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_key_dictation_check0)
-   [<span data-ttu-id="dbee7-139">**\_Gerenciador de chaves IPSec \_ \_ ditar \_ Key0**</span><span class="sxs-lookup"><span data-stu-id="dbee7-139">**IPSEC\_KEY\_MANAGER\_DICTATE\_KEY0**</span></span>](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_dictate_key0)
-   [<span data-ttu-id="dbee7-140">**\_Gerenciador de chaves IPSec \_ \_ notificar \_ Key0**</span><span class="sxs-lookup"><span data-stu-id="dbee7-140">**IPSEC\_KEY\_MANAGER\_NOTIFY\_KEY0**</span></span>](/windows/desktop/api/fwpmu/nc-fwpmu-ipsec_key_manager_notify_key0)
-   [<span data-ttu-id="dbee7-141">**\_CALLBACK0 de \_ contexto \_ SA IPsec**</span><span class="sxs-lookup"><span data-stu-id="dbee7-141">**IPSEC\_SA\_CONTEXT\_CALLBACK0**</span></span>](/windows/win32/api/fwpmu/nc-fwpmu-ipsec_sa_context_callback0)
-   [<span data-ttu-id="dbee7-142">**IPsecKeyManagerAddAndRegister0**</span><span class="sxs-lookup"><span data-stu-id="dbee7-142">**IPsecKeyManagerAddAndRegister0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanageraddandregister0)
-   [<span data-ttu-id="dbee7-143">**IPsecKeyManagerGetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="dbee7-143">**IPsecKeyManagerGetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagergetsecurityinfobykey0)
-   [<span data-ttu-id="dbee7-144">**IPsecKeyManagerSetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="dbee7-144">**IPsecKeyManagerSetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersetsecurityinfobykey0)
-   [<span data-ttu-id="dbee7-145">**IPsecKeyManagersGet0**</span><span class="sxs-lookup"><span data-stu-id="dbee7-145">**IPsecKeyManagersGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersget0)
-   [<span data-ttu-id="dbee7-146">**IPsecKeyManagerUnregisterAndDelete0**</span><span class="sxs-lookup"><span data-stu-id="dbee7-146">**IPsecKeyManagerUnregisterAndDelete0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagerunregisteranddelete0)
-   [<span data-ttu-id="dbee7-147">**IPsecSaContextSubscribe0**</span><span class="sxs-lookup"><span data-stu-id="dbee7-147">**IPsecSaContextSubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscribe0)
-   [<span data-ttu-id="dbee7-148">**IPsecSaContextSubscriptionsGet0**</span><span class="sxs-lookup"><span data-stu-id="dbee7-148">**IPsecSaContextSubscriptionsGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscriptionsget0)
-   [<span data-ttu-id="dbee7-149">**IPsecSaContextUnsubscribe0**</span><span class="sxs-lookup"><span data-stu-id="dbee7-149">**IPsecSaContextUnsubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextunsubscribe0)
-   [<span data-ttu-id="dbee7-150">**NetworkIsolationDiagnoseConnectFailureAndGetInfo**</span><span class="sxs-lookup"><span data-stu-id="dbee7-150">**NetworkIsolationDiagnoseConnectFailureAndGetInfo**</span></span>](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationdiagnoseconnectfailureandgetinfo)
-   [<span data-ttu-id="dbee7-151">**NetworkIsolationEnumAppContainers**</span><span class="sxs-lookup"><span data-stu-id="dbee7-151">**NetworkIsolationEnumAppContainers**</span></span>](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationenumappcontainers)
-   [<span data-ttu-id="dbee7-152">**NetworkIsolationEnumerateAppContainerRules**</span><span class="sxs-lookup"><span data-stu-id="dbee7-152">**NetworkIsolationEnumerateAppContainerRules**</span></span>](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationenumerateappcontainerrules)
-   [<span data-ttu-id="dbee7-153">**NetworkIsolationFreeAppContainers**</span><span class="sxs-lookup"><span data-stu-id="dbee7-153">**NetworkIsolationFreeAppContainers**</span></span>](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationfreeappcontainers)
-   [<span data-ttu-id="dbee7-154">**NetworkIsolationGetAppContainerConfig**</span><span class="sxs-lookup"><span data-stu-id="dbee7-154">**NetworkIsolationGetAppContainerConfig**</span></span>](/windows/desktop/api/networkisolation/nf-networkisolation-networkisolationgetappcontainerconfig)
-   [<span data-ttu-id="dbee7-155">**NetworkIsolationRegisterForAppContainerChanges**</span><span class="sxs-lookup"><span data-stu-id="dbee7-155">**NetworkIsolationRegisterForAppContainerChanges**</span></span>](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationregisterforappcontainerchanges)
-   [<span data-ttu-id="dbee7-156">**NetworkIsolationSetAppContainerConfig**</span><span class="sxs-lookup"><span data-stu-id="dbee7-156">**NetworkIsolationSetAppContainerConfig**</span></span>](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationsetappcontainerconfig)
-   [<span data-ttu-id="dbee7-157">**NetworkIsolationSetupAppContainerBinaries**</span><span class="sxs-lookup"><span data-stu-id="dbee7-157">**NetworkIsolationSetupAppContainerBinaries**</span></span>](/windows/desktop/api/networkisolation/nf-networkisolation-networkisolationsetupappcontainerbinaries)
-   [<span data-ttu-id="dbee7-158">**retorno de chamada de alterações de PAC \_ \_ \_ FN**</span><span class="sxs-lookup"><span data-stu-id="dbee7-158">**PAC\_CHANGES\_CALLBACK\_FN**</span></span>](/windows/desktop/api/networkisolation/nc-networkisolation-pac_changes_callback_fn)

## <a name="new-structures"></a><span data-ttu-id="dbee7-159">Novas estruturas</span><span class="sxs-lookup"><span data-stu-id="dbee7-159">New structures</span></span>

-   [<span data-ttu-id="dbee7-160">**\_METHOD2 de autenticação IKEEXT \_**</span><span class="sxs-lookup"><span data-stu-id="dbee7-160">**IKEEXT\_AUTHENTICATION\_METHOD2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_authentication_method2)
-   [<span data-ttu-id="dbee7-161">**\_EKUS0 do certificado IKEEXT \_**</span><span class="sxs-lookup"><span data-stu-id="dbee7-161">**IKEEXT\_CERT\_EKUS0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_ekus0)
-   [<span data-ttu-id="dbee7-162">**\_NAME0 do certificado IKEEXT \_**</span><span class="sxs-lookup"><span data-stu-id="dbee7-162">**IKEEXT\_CERT\_NAME0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_name0)
-   [<span data-ttu-id="dbee7-163">**\_AUTHENTICATION2 do certificado IKEEXT \_**</span><span class="sxs-lookup"><span data-stu-id="dbee7-163">**IKEEXT\_CERTIFICATE\_AUTHENTICATION2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2)
-   [<span data-ttu-id="dbee7-164">**\_CRITERIA0 do certificado IKEEXT \_**</span><span class="sxs-lookup"><span data-stu-id="dbee7-164">**IKEEXT\_CERTIFICATE\_CRITERIA0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_criteria0)
-   [<span data-ttu-id="dbee7-165">**IKEEXT \_ em \_ POLICY2**</span><span class="sxs-lookup"><span data-stu-id="dbee7-165">**IKEEXT\_EM\_POLICY2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_em_policy2)
-   [<span data-ttu-id="dbee7-166">**\_AUTHENTICATION1 Kerberos \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="dbee7-166">**IKEEXT\_KERBEROS\_AUTHENTICATION1**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication1)
-   [<span data-ttu-id="dbee7-167">**\_POLICY2 IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="dbee7-167">**IKEEXT\_POLICY2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_policy2)
-   [<span data-ttu-id="dbee7-168">**\_MANAGER0 de chave IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="dbee7-168">**IPSEC\_KEY\_MANAGER0**</span></span>](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_key_manager0)
-   [<span data-ttu-id="dbee7-169">**\_Gerenciador de chaves IPSec \_ \_ CALLBACKS0**</span><span class="sxs-lookup"><span data-stu-id="dbee7-169">**IPSEC\_KEY\_MANAGER\_CALLBACKS0**</span></span>](/windows/desktop/api/fwpmu/ns-fwpmu-ipsec_key_manager_callbacks0)
-   [<span data-ttu-id="dbee7-170">**Chave do IPSEC \_ \_ POLICY1**</span><span class="sxs-lookup"><span data-stu-id="dbee7-170">**IPSEC\_KEYING\_POLICY1**</span></span>](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_keying_policy1)
-   [<span data-ttu-id="dbee7-171">**\_CHANGE0 de \_ contexto \_ SA IPsec**</span><span class="sxs-lookup"><span data-stu-id="dbee7-171">**IPSEC\_SA\_CONTEXT\_CHANGE0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_change0)
-   [<span data-ttu-id="dbee7-172">**\_SUBSCRIPTION0 de \_ contexto \_ SA IPsec**</span><span class="sxs-lookup"><span data-stu-id="dbee7-172">**IPSEC\_SA\_CONTEXT\_SUBSCRIPTION0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_subscription0)
-   [<span data-ttu-id="dbee7-173">**\_POLICY2 de transporte IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="dbee7-173">**IPSEC\_TRANSPORT\_POLICY2**</span></span>](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_transport_policy2)
-   [<span data-ttu-id="dbee7-174">**\_ENDPOINT0 de túnel IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="dbee7-174">**IPSEC\_TUNNEL\_ENDPOINT0**</span></span>](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoint0)
-   [<span data-ttu-id="dbee7-175">**\_ENDPOINTS2 de túnel IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="dbee7-175">**IPSEC\_TUNNEL\_ENDPOINTS2**</span></span>](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints2)
-   [<span data-ttu-id="dbee7-176">**\_POLICY2 de túnel IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="dbee7-176">**IPSEC\_TUNNEL\_POLICY2**</span></span>](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2)
-   [<span data-ttu-id="dbee7-177">**FWPM \_ CONNECTION0**</span><span class="sxs-lookup"><span data-stu-id="dbee7-177">**FWPM\_CONNECTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection0)
-   [<span data-ttu-id="dbee7-178">**\_TEMPLATE0 de \_ enumeração de conexão FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="dbee7-178">**FWPM\_CONNECTION\_ENUM\_TEMPLATE0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_enum_template0)
-   [<span data-ttu-id="dbee7-179">**FWPM de \_ conexão \_ SUBSCRIPTION0**</span><span class="sxs-lookup"><span data-stu-id="dbee7-179">**FWPM\_CONNECTION\_SUBSCRIPTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_subscription0)
-   [<span data-ttu-id="dbee7-180">**FWPM \_ net \_ EVENT2**</span><span class="sxs-lookup"><span data-stu-id="dbee7-180">**FWPM\_NET\_EVENT2**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event2)
-   [<span data-ttu-id="dbee7-181">**\_Funcionalidade de \_ evento FWPM NET \_ \_ ALLOW0**</span><span class="sxs-lookup"><span data-stu-id="dbee7-181">**FWPM\_NET\_EVENT\_CAPABILITY\_ALLOW0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_allow0)
-   [<span data-ttu-id="dbee7-182">**\_Funcionalidade de \_ evento FWPM NET \_ \_ DROP0**</span><span class="sxs-lookup"><span data-stu-id="dbee7-182">**FWPM\_NET\_EVENT\_CAPABILITY\_DROP0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_drop0)
-   [<span data-ttu-id="dbee7-183">**\_ALLOW0 de \_ classificação de evento FWPM NET \_ \_**</span><span class="sxs-lookup"><span data-stu-id="dbee7-183">**FWPM\_NET\_EVENT\_CLASSIFY\_ALLOW0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_allow0)
-   [<span data-ttu-id="dbee7-184">**\_DROP2 de \_ classificação de evento FWPM NET \_ \_**</span><span class="sxs-lookup"><span data-stu-id="dbee7-184">**FWPM\_NET\_EVENT\_CLASSIFY\_DROP2**</span></span>](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop2)
-   [<span data-ttu-id="dbee7-185">**\_MAC0 de \_ remoção de evento FWPM NET \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="dbee7-185">**FWPM\_NET\_EVENT\_CLASSIFY\_DROP\_MAC0**</span></span>](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop_mac0)
-   [<span data-ttu-id="dbee7-186">**FWPM \_ net \_ Event \_ HEADER2**</span><span class="sxs-lookup"><span data-stu-id="dbee7-186">**FWPM\_NET\_EVENT\_HEADER2**</span></span>](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_header2)
-   [<span data-ttu-id="dbee7-187">**\_Provedor FWPM \_ CONTEXT2**</span><span class="sxs-lookup"><span data-stu-id="dbee7-187">**FWPM\_PROVIDER\_CONTEXT2**</span></span>](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context2)
-   [<span data-ttu-id="dbee7-188">**FWPM \_ VSWITCH \_ EVENT0**</span><span class="sxs-lookup"><span data-stu-id="dbee7-188">**FWPM\_VSWITCH\_EVENT0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event0)
-   [<span data-ttu-id="dbee7-189">**\_ \_ Evento \_ SUBSCRIPTION0 do FWPM VSWITCH**</span><span class="sxs-lookup"><span data-stu-id="dbee7-189">**FWPM\_VSWITCH\_EVENT\_SUBSCRIPTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event_subscription0)

## <a name="new-enumerated-types"></a><span data-ttu-id="dbee7-190">Novos tipos enumerados</span><span class="sxs-lookup"><span data-stu-id="dbee7-190">New enumerated types</span></span>

-   [<span data-ttu-id="dbee7-191">**\_tipo de \_ rede fwp VSWITCH \_**</span><span class="sxs-lookup"><span data-stu-id="dbee7-191">**FWP\_VSWITCH\_NETWORK\_TYPE**</span></span>](/windows/win32/api/fwptypes/ne-fwptypes-fwp_vswitch_network_type)
-   [<span data-ttu-id="dbee7-192">**\_tipo de \_ recurso de rede FWPM APPC \_ \_**</span><span class="sxs-lookup"><span data-stu-id="dbee7-192">**FWPM\_APPC\_NETWORK\_CAPABILITY\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_appc_network_capability_type)
-   [<span data-ttu-id="dbee7-193">**\_tipo de \_ evento de conexão FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="dbee7-193">**FWPM\_CONNECTION\_EVENT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_connection_event_type)
-   [<span data-ttu-id="dbee7-194">**\_tipo de \_ evento FWPM VSWITCH \_**</span><span class="sxs-lookup"><span data-stu-id="dbee7-194">**FWPM\_VSWITCH\_EVENT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_vswitch_event_type)
-   [<span data-ttu-id="dbee7-195">**\_tipo de \_ nome de critérios de certificado IKEEXT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="dbee7-195">**IKEEXT\_CERT\_CRITERIA\_NAME\_TYPE**</span></span>](/windows/win32/api/iketypes/ne-iketypes-ikeext_cert_criteria_name_type)
-   [<span data-ttu-id="dbee7-196">**\_Evento de contexto SA de IPSec \_ \_ \_ TYPE0**</span><span class="sxs-lookup"><span data-stu-id="dbee7-196">**IPSEC\_SA\_CONTEXT\_EVENT\_TYPE0**</span></span>](/windows/desktop/api/Ipsectypes/ne-ipsectypes-ipsec_sa_context_event_type0)

## <a name="new-filtering-layer-identifiers"></a><span data-ttu-id="dbee7-197">Novos identificadores de camada de filtragem</span><span class="sxs-lookup"><span data-stu-id="dbee7-197">New filtering layer identifiers</span></span>

[<span data-ttu-id="dbee7-198">**Filtrando identificadores de camada:**</span><span class="sxs-lookup"><span data-stu-id="dbee7-198">**Filtering Layer Identifiers:**</span></span>](management-filtering-layer-identifiers-.md)

-   <span data-ttu-id="dbee7-199">\_ \_ \_ Mac \_ frame \_ Ethernet de entrada da camada FWPM</span><span class="sxs-lookup"><span data-stu-id="dbee7-199">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="dbee7-200">quadro de Mac de saída da camada do FWPM \_ \_ \_ \_ \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="dbee7-200">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="dbee7-201">\_quadro de Mac de entrada da camada FWPM \_ \_ \_ \_ nativa</span><span class="sxs-lookup"><span data-stu-id="dbee7-201">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="dbee7-202">\_quadro do Mac de saída da camada FWPM \_ \_ \_ \_ nativa</span><span class="sxs-lookup"><span data-stu-id="dbee7-202">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="dbee7-203">\_ \_ Ethernet VSWITCH de entrada de camada \_ FWPM \_</span><span class="sxs-lookup"><span data-stu-id="dbee7-203">FWPM\_LAYER\_INGRESS\_VSWITCH\_ETHERNET</span></span>
-   <span data-ttu-id="dbee7-204">\_ \_ Ethernet VSWITCH de egresso de camada FWPM \_ \_</span><span class="sxs-lookup"><span data-stu-id="dbee7-204">FWPM\_LAYER\_EGRESS\_VSWITCH\_ETHERNET</span></span>
-   <span data-ttu-id="dbee7-205">Transporte de \_ vSwitch de entrada de camada \_ \_ \_ \_ v4/FWPM de \_ entrada da camada \_ \_ \_ \_ do FWPM de ingresso do vSwitch V6</span><span class="sxs-lookup"><span data-stu-id="dbee7-205">FWPM\_LAYER\_INGRESS\_VSWITCH\_TRANSPORT\_V4 / FWPM\_LAYER\_INGRESS\_VSWITCH\_TRANSPORT\_V6</span></span>
-   <span data-ttu-id="dbee7-206">Transporte do \_ vSwitch de saída de camada FWPM \_ \_ \_ \_ v4/FWPM de \_ saída de camada de egresso do \_ \_ vSwitch \_ \_ V6</span><span class="sxs-lookup"><span data-stu-id="dbee7-206">FWPM\_LAYER\_EGRESS\_VSWITCH\_TRANSPORT\_V4 / FWPM\_LAYER\_EGRESS\_VSWITCH\_TRANSPORT\_V6</span></span>

## <a name="new-filtering-condition-identifiers"></a><span data-ttu-id="dbee7-207">Novos identificadores de condição de filtragem</span><span class="sxs-lookup"><span data-stu-id="dbee7-207">New filtering condition identifiers</span></span>

[<span data-ttu-id="dbee7-208">**Filtrando identificadores de condição:**</span><span class="sxs-lookup"><span data-stu-id="dbee7-208">**Filtering Condition Identifiers:**</span></span>](filtering-condition-identifiers-.md)

-   <span data-ttu-id="dbee7-209">\_ \_ endereço MAC da interface de condição FWPM \_ \_</span><span class="sxs-lookup"><span data-stu-id="dbee7-209">FWPM\_CONDITION\_INTERFACE\_MAC\_ADDRESS</span></span>
-   <span data-ttu-id="dbee7-210">\_ \_ \_ endereço local Mac do FWPM Condition \_</span><span class="sxs-lookup"><span data-stu-id="dbee7-210">FWPM\_CONDITION\_MAC\_LOCAL\_ADDRESS</span></span>
-   <span data-ttu-id="dbee7-211">\_ \_ \_ endereço remoto Mac do FWPM Condition \_</span><span class="sxs-lookup"><span data-stu-id="dbee7-211">FWPM\_CONDITION\_MAC\_REMOTE\_ADDRESS</span></span>
-   <span data-ttu-id="dbee7-212">\_tipo de \_ ether \_ Condition FWPM</span><span class="sxs-lookup"><span data-stu-id="dbee7-212">FWPM\_CONDITION\_ETHER\_TYPE</span></span>
-   <span data-ttu-id="dbee7-213">\_ID de \_ VLAN da condição FWPM \_</span><span class="sxs-lookup"><span data-stu-id="dbee7-213">FWPM\_CONDITION\_VLAN\_ID</span></span>
-   <span data-ttu-id="dbee7-214">\_ \_ porta NDIS da condição FWPM \_</span><span class="sxs-lookup"><span data-stu-id="dbee7-214">FWPM\_CONDITION\_NDIS\_PORT</span></span>
-   <span data-ttu-id="dbee7-215">\_tipo de \_ \_ mídia NDIS da condição \_ FWPM</span><span class="sxs-lookup"><span data-stu-id="dbee7-215">FWPM\_CONDITION\_NDIS\_MEDIA\_TYPE</span></span>
-   <span data-ttu-id="dbee7-216">\_tipo de \_ \_ mídia física \_ de NDIS da condição FWPM \_</span><span class="sxs-lookup"><span data-stu-id="dbee7-216">FWPM\_CONDITION\_NDIS\_PHYSICAL\_MEDIA\_TYPE</span></span>
-   <span data-ttu-id="dbee7-217">\_Sinalizadores de \_ L2 da condição FWPM \_</span><span class="sxs-lookup"><span data-stu-id="dbee7-217">FWPM\_CONDITION\_L2\_FLAGS</span></span>
-   <span data-ttu-id="dbee7-218">\_tipo de \_ \_ endereço local \_ Mac \_ do FWPM Condition</span><span class="sxs-lookup"><span data-stu-id="dbee7-218">FWPM\_CONDITION\_MAC\_LOCAL\_ADDRESS\_TYPE</span></span>
-   <span data-ttu-id="dbee7-219">\_tipo de \_ \_ endereço remoto \_ Mac \_ da condição FWPM</span><span class="sxs-lookup"><span data-stu-id="dbee7-219">FWPM\_CONDITION\_MAC\_REMOTE\_ADDRESS\_TYPE</span></span>
-   <span data-ttu-id="dbee7-220">\_ID do \_ pacote de Ale da condição FWPM \_ \_</span><span class="sxs-lookup"><span data-stu-id="dbee7-220">FWPM\_CONDITION\_ALE\_PACKAGE\_ID</span></span>
-   <span data-ttu-id="dbee7-221">\_endereço de \_ origem do Mac da condição FWPM \_ \_</span><span class="sxs-lookup"><span data-stu-id="dbee7-221">FWPM\_CONDITION\_MAC\_SOURCE\_ADDRESS</span></span>
-   <span data-ttu-id="dbee7-222">\_endereço de \_ \_ destino Mac da condição \_ FWPM</span><span class="sxs-lookup"><span data-stu-id="dbee7-222">FWPM\_CONDITION\_MAC\_DESTINATION\_ADDRESS</span></span>
-   <span data-ttu-id="dbee7-223">\_tipo de \_ endereço de origem do Mac da condição FWPM \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="dbee7-223">FWPM\_CONDITION\_MAC\_SOURCE\_ADDRESS\_TYPE</span></span>
-   <span data-ttu-id="dbee7-224">\_tipo de \_ \_ endereço de destino Mac da condição \_ FWPM \_</span><span class="sxs-lookup"><span data-stu-id="dbee7-224">FWPM\_CONDITION\_MAC\_DESTINATION\_ADDRESS\_TYPE</span></span>
-   <span data-ttu-id="dbee7-225">\_porta de \_ \_ origem IP da condição \_ FWPM</span><span class="sxs-lookup"><span data-stu-id="dbee7-225">FWPM\_CONDITION\_IP\_SOURCE\_PORT</span></span>
-   <span data-ttu-id="dbee7-226">\_porta de \_ \_ destino IP da condição \_ FWPM</span><span class="sxs-lookup"><span data-stu-id="dbee7-226">FWPM\_CONDITION\_IP\_DESTINATION\_PORT</span></span>
-   <span data-ttu-id="dbee7-227">\_ID do \_ VSWITCH da condição FWPM \_</span><span class="sxs-lookup"><span data-stu-id="dbee7-227">FWPM\_CONDITION\_VSWITCH\_ID</span></span>
-   <span data-ttu-id="dbee7-228">\_tipo de \_ rede do VSWITCH da condição FWPM \_ \_</span><span class="sxs-lookup"><span data-stu-id="dbee7-228">FWPM\_CONDITION\_VSWITCH\_NETWORK\_TYPE</span></span>
-   <span data-ttu-id="dbee7-229">ID da interface de origem do FWPM \_ condição \_ VSWITCH \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="dbee7-229">FWPM\_CONDITION\_VSWITCH\_SOURCE\_INTERFACE\_ID</span></span>
-   <span data-ttu-id="dbee7-230">ID da interface de destino do FWPM \_ Condition \_ VSWITCH \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="dbee7-230">FWPM\_CONDITION\_VSWITCH\_DESTINATION\_INTERFACE\_ID</span></span>
-   <span data-ttu-id="dbee7-231">ID da VM de origem do FWPM \_ condição \_ VSWITCH \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="dbee7-231">FWPM\_CONDITION\_VSWITCH\_SOURCE\_VM\_ID</span></span>
-   <span data-ttu-id="dbee7-232">ID da VM de destino do FWPM \_ Condition \_ VSWITCH \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="dbee7-232">FWPM\_CONDITION\_VSWITCH\_DESTINATION\_VM\_ID</span></span>
-   <span data-ttu-id="dbee7-233">tipo de interface de origem do FWPM \_ condição \_ VSWITCH \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="dbee7-233">FWPM\_CONDITION\_VSWITCH\_SOURCE\_INTERFACE\_TYPE</span></span>
-   <span data-ttu-id="dbee7-234">ID de rede do locatário do FWPM \_ Condition \_ VSWITCH \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="dbee7-234">FWPM\_CONDITION\_VSWITCH\_TENANT\_NETWORK\_ID</span></span>

## <a name="new-filtering-condition-flags"></a><span data-ttu-id="dbee7-235">Novos sinalizadores de condição de filtragem</span><span class="sxs-lookup"><span data-stu-id="dbee7-235">New filtering condition flags</span></span>

[<span data-ttu-id="dbee7-236">**Filtrando sinalizadores de condição:**</span><span class="sxs-lookup"><span data-stu-id="dbee7-236">**Filtering Condition Flags:**</span></span>](filtering-condition-flags-.md)

-   <span data-ttu-id="dbee7-237">o \_ sinalizador de condição fwp \_ é uma \_ \_ \_ conexão proxy</span><span class="sxs-lookup"><span data-stu-id="dbee7-237">FWP\_CONDITION\_FLAG\_IS\_PROXY\_CONNECTION</span></span>
-   <span data-ttu-id="dbee7-238">o \_ sinalizador de condição fwp \_ é o \_ \_ loopback do APPCONTAINER \_</span><span class="sxs-lookup"><span data-stu-id="dbee7-238">FWP\_CONDITION\_FLAG\_IS\_APPCONTAINER\_LOOPBACK</span></span>
-   <span data-ttu-id="dbee7-239">o \_ sinalizador de condição fwp não \_ é um \_ \_ \_ loopback de APPCONTAINER \_</span><span class="sxs-lookup"><span data-stu-id="dbee7-239">FWP\_CONDITION\_FLAG\_IS\_NON\_APPCONTAINER\_LOOPBACK</span></span>
-   <span data-ttu-id="dbee7-240">o \_ sinalizador de condição fwp \_ \_ está \_ respeitando a \_ política de \_ autorização</span><span class="sxs-lookup"><span data-stu-id="dbee7-240">FWP\_CONDITION\_FLAG\_IS\_HONORING\_POLICY\_AUTHORIZE</span></span>
-   <span data-ttu-id="dbee7-241">FWP \_ condição \_ L2 \_ é \_ \_ Ethernet nativa</span><span class="sxs-lookup"><span data-stu-id="dbee7-241">FWP\_CONDITION\_L2\_IS\_NATIVE\_ETHERNET</span></span>
-   <span data-ttu-id="dbee7-242">FWP \_ condição \_ L2 \_ é \_ WiFi</span><span class="sxs-lookup"><span data-stu-id="dbee7-242">FWP\_CONDITION\_L2\_IS\_WIFI</span></span>
-   <span data-ttu-id="dbee7-243">FWP \_ condição \_ L2 \_ é \_ \_ banda larga móvel</span><span class="sxs-lookup"><span data-stu-id="dbee7-243">FWP\_CONDITION\_L2\_IS\_MOBILE\_BROADBAND</span></span>
-   <span data-ttu-id="dbee7-244">FWP \_ condição \_ L2 \_ são \_ \_ dados diretos de WiFi \_</span><span class="sxs-lookup"><span data-stu-id="dbee7-244">FWP\_CONDITION\_L2\_IS\_WIFI\_DIRECT\_DATA</span></span>
-   <span data-ttu-id="dbee7-245">FWP \_ condição \_ L2 \_ é \_ VM2VM</span><span class="sxs-lookup"><span data-stu-id="dbee7-245">FWP\_CONDITION\_L2\_IS\_VM2VM</span></span>
-   <span data-ttu-id="dbee7-246">FWP \_ condição \_ L2 \_ é um \_ pacote malformado \_</span><span class="sxs-lookup"><span data-stu-id="dbee7-246">FWP\_CONDITION\_L2\_IS\_MALFORMED\_PACKET</span></span>
-   <span data-ttu-id="dbee7-247">FWP \_ condição \_ L2 \_ é \_ \_ grupo de fragmentos IP \_</span><span class="sxs-lookup"><span data-stu-id="dbee7-247">FWP\_CONDITION\_L2\_IS\_IP\_FRAGMENT\_GROUP</span></span>
-   <span data-ttu-id="dbee7-248">FWP \_ condição \_ L2 \_ se o \_ conector \_ estiver presente</span><span class="sxs-lookup"><span data-stu-id="dbee7-248">FWP\_CONDITION\_L2\_IF\_CONNECTOR\_PRESENT</span></span>

## <a name="windows-7-updates-to-the-windows-filtering-platform"></a><span data-ttu-id="dbee7-249">Atualizações do Windows 7 para a plataforma de filtragem do Windows</span><span class="sxs-lookup"><span data-stu-id="dbee7-249">Windows 7 updates to the Windows Filtering Platform</span></span>

<span data-ttu-id="dbee7-250">O documento [novidades na plataforma de filtragem do Windows]() detalha muitas das atualizações feitas para o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="dbee7-250">The document [What's New in Windows Filtering Platform]() details many of the updates made for Windows 7.</span></span> <span data-ttu-id="dbee7-251">As informações também estão disponíveis no kit de driver do Windows em [alterações de WFP para o Windows 7](/windows-hardware/drivers/network/wfp-changes-for-windows-7).</span><span class="sxs-lookup"><span data-stu-id="dbee7-251">Information is also available in the Windows Driver Kit on [WFP Changes for Windows 7](/windows-hardware/drivers/network/wfp-changes-for-windows-7).</span></span>

 

 
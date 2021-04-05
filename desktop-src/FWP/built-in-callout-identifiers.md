---
title: Identificadores de texto explicativo interno (Fwpmu. h)
description: Os identificadores para as funções de texto explicativo que são internas para a WFP (Windows Filtering Platform) são representadas por um GUID. Esses identificadores são definidos da seguinte maneira.
ms.assetid: b283cb2e-7f82-4d44-982a-38499504e3bc
topic_type:
- apiref
api_name:
- FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V4 / FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V6
- FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V4 / FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V6
- FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V4 / FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V6
- FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V4 / FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V6
- FWPM_CALLOUT_IPSEC_ALE_CONNECT_V4 / FWPM_CALLOUT_IPSEC_ALE_CONNECT_V6
- FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V4 / FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V6
- FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V4_SILENT_DROP / FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V6_SILENT_DROP
- FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V4 / FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V6
- FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V4 / FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V6
- FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V4 / FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V6
- FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V4 / FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V6
- FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V4 / FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V6
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6 / FWPM_CALLOUT_TEREDO_ALE_LISTEN_V6
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6 / FWPM_CALLOUT_TEREDO_ALE_RESOURCE_ASSIGNMENT_V6
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V4
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V4
- FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V4 / FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V6
- FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V4 / FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V6
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c21d0428953d8b3e27590b186d931a7d902db377
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919119"
---
# <a name="built-in-callout-identifiers"></a><span data-ttu-id="091b8-104">Identificadores de texto explicativo internos</span><span class="sxs-lookup"><span data-stu-id="091b8-104">Built-in Callout Identifiers</span></span>

<span data-ttu-id="091b8-105">Os identificadores para as funções de texto explicativo que são internas para a WFP (Windows Filtering Platform) são representadas por um GUID.</span><span class="sxs-lookup"><span data-stu-id="091b8-105">The identifiers for the callout functions that are built in to the Windows Filtering Platform (WFP) are each represented by a GUID.</span></span> <span data-ttu-id="091b8-106">Esses identificadores são definidos da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="091b8-106">These identifiers are defined as follows.</span></span>

<span data-ttu-id="091b8-107">Os sufixos v4 e V6 no final dos identificadores de texto explicativo indicam se o texto explicativo é para a pilha de rede IPv4 ou para a pilha de rede IPv6.</span><span class="sxs-lookup"><span data-stu-id="091b8-107">The V4 and V6 suffixes at the end of the callout identifiers indicate whether the callout is for the IPv4 network stack or for the IPv6 network stack.</span></span>

<dl> <dt>

<span data-ttu-id="091b8-108"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_inbound_transport_v4___fwpm_callout_ipsec_inbound_transport_v6_"></span>**\_Texto explicativo de FWPM de \_ protocolo IPsec \_ \_ \_ v4/FWPM \_ texto explicativo de \_ entrada IP V6 de transporte de \_ saída \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091b8-108"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_inbound_transport_v4___fwpm_callout_ipsec_inbound_transport_v6_"></span>**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V4 / FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V6**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="091b8-109">Verifica se cada pacote recebido que deve chegar em uma associação de segurança do modo de transporte chega com segurança.</span><span class="sxs-lookup"><span data-stu-id="091b8-109">Verifies that each received packet that is supposed to arrive over a transport mode security association arrives securely.</span></span>

<span data-ttu-id="091b8-110">Esse texto explicativo é aplicável na camada de transporte.</span><span class="sxs-lookup"><span data-stu-id="091b8-110">This callout is applicable at the transport layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091b8-111"><span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_outbound_transport_v4___fwpm_callout_ipsec_outbound_transport_v6_"></span>**FWPM \_ balão \_ de \_ transporte de saída IPSec \_ \_ v4/FWPM de \_ transporte de saída do \_ IPSec \_ \_ \_ V6**</span><span class="sxs-lookup"><span data-stu-id="091b8-111"><span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_outbound_transport_v4___fwpm_callout_ipsec_outbound_transport_v6_"></span>**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V4 / FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V6**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="091b8-112">Indica ao IPsec o tráfego de saída que deve ser protegido em associações de segurança do modo de transporte.</span><span class="sxs-lookup"><span data-stu-id="091b8-112">Indicates to IPsec the outbound traffic that must be secured over transport mode security associations.</span></span>

<span data-ttu-id="091b8-113">Esse texto explicativo é aplicável na camada de transporte.</span><span class="sxs-lookup"><span data-stu-id="091b8-113">This callout is applicable at the transport layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091b8-114"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_inbound_tunnel_v4___fwpm_callout_ipsec_inbound_tunnel_v6_"></span>**\_Texto explicativo IPSec de entrada do FWPM em balão \_ \_ \_ \_ v4/FWPM de \_ limite de entrada do \_ IPSec \_ \_ \_ V6**</span><span class="sxs-lookup"><span data-stu-id="091b8-114"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_inbound_tunnel_v4___fwpm_callout_ipsec_inbound_tunnel_v6_"></span>**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TUNNEL\_V4 / FWPM\_CALLOUT\_IPSEC\_INBOUND\_TUNNEL\_V6**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="091b8-115">Verifica se cada pacote recebido que deve chegar em uma associação de segurança do modo de túnel chega com segurança.</span><span class="sxs-lookup"><span data-stu-id="091b8-115">Verifies that each received packet that is supposed to arrive over a tunnel mode security association arrives securely.</span></span>

<span data-ttu-id="091b8-116">Esse texto explicativo é aplicável na camada de transporte.</span><span class="sxs-lookup"><span data-stu-id="091b8-116">This callout is applicable at the transport layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091b8-117"><span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_outbound_tunnel_v4___fwpm_callout_ipsec_outbound_tunnel_v6_"></span>**FWPM \_ balão \_ de \_ saída \_ IPSec \_ v4/FWPM \_ de \_ \_ túnel de saída IPSec \_ \_ V6**</span><span class="sxs-lookup"><span data-stu-id="091b8-117"><span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_outbound_tunnel_v4___fwpm_callout_ipsec_outbound_tunnel_v6_"></span>**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TUNNEL\_V4 / FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TUNNEL\_V6**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="091b8-118">Indica ao IPsec o tráfego de saída que deve ser protegido em relação às associações de segurança do modo de túnel.</span><span class="sxs-lookup"><span data-stu-id="091b8-118">Indicates to IPsec the outbound traffic that must be secured over tunnel mode security associations.</span></span>

<span data-ttu-id="091b8-119">Esse texto explicativo é aplicável na camada de transporte.</span><span class="sxs-lookup"><span data-stu-id="091b8-119">This callout is applicable at the transport layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091b8-120"><span id="FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_inbound_tunnel_v4___fwpm_callout_ipsec_forward_inbound_tunnel_v6"></span>**\_Texto explicativo de \_ encaminhamento IPSec enFWPM \_ Tunnel de \_ entrada \_ \_ v4/FWPM \_ balão de \_ \_ encaminhamento do túnel de \_ entrada \_ \_ V6 do IPSec**</span><span class="sxs-lookup"><span data-stu-id="091b8-120"><span id="FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_inbound_tunnel_v4___fwpm_callout_ipsec_forward_inbound_tunnel_v6"></span>**FWPM\_CALLOUT\_IPSEC\_FORWARD\_INBOUND\_TUNNEL\_V4 / FWPM\_CALLOUT\_IPSEC\_FORWARD\_INBOUND\_TUNNEL\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091b8-121">Verifica se cada pacote recebido que deve chegar em uma associação de segurança do modo de túnel chega com segurança.</span><span class="sxs-lookup"><span data-stu-id="091b8-121">Verifies that each received packet that is supposed to arrive over a tunnel mode security association arrives securely.</span></span>

<span data-ttu-id="091b8-122">Esse texto explicativo é aplicável na camada de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="091b8-122">This callout is applicable at the forwarding layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091b8-123"><span id="FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_outbound_tunnel_v4___fwpm_callout_ipsec_forward_outbound_tunnel_v6"></span>**\_Balão de \_ saída de \_ encaminhamento IPSec \_ v4/FWPM de túnel de saída de \_ \_ \_ \_ \_ encaminhamento IPSec \_ \_ \_ V6 do FWPM**</span><span class="sxs-lookup"><span data-stu-id="091b8-123"><span id="FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_outbound_tunnel_v4___fwpm_callout_ipsec_forward_outbound_tunnel_v6"></span>**FWPM\_CALLOUT\_IPSEC\_FORWARD\_OUTBOUND\_TUNNEL\_V4 / FWPM\_CALLOUT\_IPSEC\_FORWARD\_OUTBOUND\_TUNNEL\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091b8-124">Indica ao IPsec o tráfego de saída que deve ser protegido em uma associação de segurança do modo de túnel.</span><span class="sxs-lookup"><span data-stu-id="091b8-124">Indicates to IPsec the outbound traffic that must be secured over a tunnel mode security association.</span></span>

<span data-ttu-id="091b8-125">Esse texto explicativo é aplicável na camada de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="091b8-125">This callout is applicable at the forwarding layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091b8-126"><span id="FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V4___FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V6_"></span><span id="fwpm_callout_ipsec_inbound_initiate_secure_v4___fwpm_callout_ipsec_inbound_initiate_secure_v6_"></span>**FWPM \_ texto explicativo \_ IPSec de \_ entrada \_ Iniciar \_ segurança \_ v4/FWPM \_ texto explicativo \_ IPSec de \_ entrada \_ Iniciar \_ \_ V6 de segurança**</span><span class="sxs-lookup"><span data-stu-id="091b8-126"><span id="FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V4___FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V6_"></span><span id="fwpm_callout_ipsec_inbound_initiate_secure_v4___fwpm_callout_ipsec_inbound_initiate_secure_v6_"></span>**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V4 / FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V6**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="091b8-127">Verifica se cada conexão de entrada que deve chegar à segurança chega segura.</span><span class="sxs-lookup"><span data-stu-id="091b8-127">Verifies that each incoming connection that is supposed to arrive secure arrives securely.</span></span>

<span data-ttu-id="091b8-128">Esse texto explicativo é aplicável na camada de aceitação ALE.</span><span class="sxs-lookup"><span data-stu-id="091b8-128">This callout is applicable at the ALE accept layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091b8-129"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V6"></span><span id="fwpm_callout_ipsec_inbound_tunnel_ale_accept_v4___fwpm_callout_ipsec_inbound_tunnel_ale_accept_v6"></span>**FWPM \_ texto explicativo \_ IPSec de \_ túnel de entrada \_ \_ Ale \_ Accept \_ v4/FWPM \_ texto EXPLICAtivo de \_ \_ entrada Ale de túnel de saída do IPSec \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="091b8-129"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V6"></span><span id="fwpm_callout_ipsec_inbound_tunnel_ale_accept_v4___fwpm_callout_ipsec_inbound_tunnel_ale_accept_v6"></span>**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TUNNEL\_ALE\_ACCEPT\_V4 / FWPM\_CALLOUT\_IPSEC\_INBOUND\_TUNNEL\_ALE\_ACCEPT\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091b8-130">Permite os pacotes IP-in-IP do modo de túnel IPsec quando eles são classificados na camada de aceitação ALE.</span><span class="sxs-lookup"><span data-stu-id="091b8-130">Permits the IPsec tunnel mode IP-in-IP packets when they get classified at the ALE accept layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091b8-131"><span id="FWPM_CALLOUT_IPSEC_ALE_CONNECT_V4___FWPM_CALLOUT_IPSEC_ALE_CONNECT_V6"></span><span id="fwpm_callout_ipsec_ale_connect_v4___fwpm_callout_ipsec_ale_connect_v6"></span>**\_Texto explicativo FWPM de \_ \_ conexão Ale de IPSec \_ \_ /FWPM \_ texto explicativo de \_ \_ conexão Ale IPSec \_ \_ V6**</span><span class="sxs-lookup"><span data-stu-id="091b8-131"><span id="FWPM_CALLOUT_IPSEC_ALE_CONNECT_V4___FWPM_CALLOUT_IPSEC_ALE_CONNECT_V6"></span><span id="fwpm_callout_ipsec_ale_connect_v4___fwpm_callout_ipsec_ale_connect_v6"></span>**FWPM\_CALLOUT\_IPSEC\_ALE\_CONNECT\_V4 / FWPM\_CALLOUT\_IPSEC\_ALE\_CONNECT\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091b8-132">Aplica modificadores de política IPsec a aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="091b8-132">Applies IPsec policy modifiers to client applications.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091b8-133"><span id="FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V4___FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V6"></span><span id="fwpm_callout_ipsec_dosp_forward_v4___fwpm_callout_ipsec_dosp_forward_v6"></span>**FWPM \_ balão \_ IPSec \_ DOSP \_ Forward \_ v4/FWPM \_ balão \_ IPSec \_ DOSP \_ Forward \_ V6**</span><span class="sxs-lookup"><span data-stu-id="091b8-133"><span id="FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V4___FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V6"></span><span id="fwpm_callout_ipsec_dosp_forward_v4___fwpm_callout_ipsec_dosp_forward_v6"></span>**FWPM\_CALLOUT\_IPSEC\_DOSP\_FORWARD\_V4 / FWPM\_CALLOUT\_IPSEC\_DOSP\_FORWARD\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091b8-134">Sinaliza à proteção de DoS IPsec que o tráfego precisa ser verificado quanto ao DoS possíveis e pode precisar ter uma taxa limitada.</span><span class="sxs-lookup"><span data-stu-id="091b8-134">Signals to IPsec DoS Protection that traffic needs to be verified for potential DoS and may need to be rate limited.</span></span>

> [!Note]  
> <span data-ttu-id="091b8-135">Disponível somente no Windows 7 e no Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="091b8-135">Available only in Windows 7 and Windows Server 2008 R2.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="091b8-136"><span id="FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V4_SILENT_DROP___FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V6_SILENT_DROP"></span><span id="fwpm_callout_wfp_transport_layer_v4_silent_drop___fwpm_callout_wfp_transport_layer_v6_silent_drop"></span>**\_Texto explicativo FWPM \_ camada de \_ transporte WFP \_ \_ v4 \_ \_ soltar/FWPM \_ balão de camada de \_ \_ transporte WFP \_ \_ V6 \_ \_ drop silencioso**</span><span class="sxs-lookup"><span data-stu-id="091b8-136"><span id="FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V4_SILENT_DROP___FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V6_SILENT_DROP"></span><span id="fwpm_callout_wfp_transport_layer_v4_silent_drop___fwpm_callout_wfp_transport_layer_v6_silent_drop"></span>**FWPM\_CALLOUT\_WFP\_TRANSPORT\_LAYER\_V4\_SILENT\_DROP / FWPM\_CALLOUT\_WFP\_TRANSPORT\_LAYER\_V6\_SILENT\_DROP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091b8-137">Implementa a filtragem de modo furtivo descartando silenciosamente todos os pacotes de entrada para os quais o TCP não tem um ponto de extremidade de escuta.</span><span class="sxs-lookup"><span data-stu-id="091b8-137">Implements stealth-mode filtering by silently dropping all incoming packets for which TCP does not have a listening endpoint.</span></span>

<span data-ttu-id="091b8-138">Esse texto explicativo é aplicável na camada de descarte de transporte de entrada.</span><span class="sxs-lookup"><span data-stu-id="091b8-138">This callout is applicable at the inbound transport discard layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091b8-139"><span id="FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_connect_layer_v4___fwpm_callout_tcp_chimney_connect_layer_v6"></span>**\_Texto explicativo FWPM \_ TCP \_ Chimney \_ \_ Layer \_ v4/FWPM \_ texto explicativo \_ TCP \_ Chimney \_ Connect \_ camada \_ V6**</span><span class="sxs-lookup"><span data-stu-id="091b8-139"><span id="FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_connect_layer_v4___fwpm_callout_tcp_chimney_connect_layer_v6"></span>**FWPM\_CALLOUT\_TCP\_CHIMNEY\_CONNECT\_LAYER\_V4 / FWPM\_CALLOUT\_TCP\_CHIMNEY\_CONNECT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091b8-140">Habilita ou desabilita o descarregamento de Chimney TCP para cada conexão de saída.</span><span class="sxs-lookup"><span data-stu-id="091b8-140">Enables or disables TCP chimney offload for each outgoing connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091b8-141"><span id="FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_accept_layer_v4___fwpm_callout_tcp_chimney_accept_layer_v6"></span>**FWPM \_ balão \_ TCP \_ Chimney \_ Accept da \_ camada \_ v4/FWPM \_ texto explicativo \_ TCP \_ Chimney \_ aceito \_ camada \_ V6**</span><span class="sxs-lookup"><span data-stu-id="091b8-141"><span id="FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_accept_layer_v4___fwpm_callout_tcp_chimney_accept_layer_v6"></span>**FWPM\_CALLOUT\_TCP\_CHIMNEY\_ACCEPT\_LAYER\_V4 / FWPM\_CALLOUT\_TCP\_CHIMNEY\_ACCEPT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091b8-142">Habilita ou desabilita o descarregamento de Chimney TCP para cada conexão de entrada.</span><span class="sxs-lookup"><span data-stu-id="091b8-142">Enables or disables TCP chimney offload for each incoming connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091b8-143"><span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_connect_layer_v4___fwpm_callout_set_options_auth_connect_layer_v6"></span>**FWPM \_ balão \_ set \_ opções \_ auth \_ Connect \_ Layer \_ v4/FWPM \_ texto explicativo \_ definir \_ opções \_ auth \_ Connect \_ Layer \_ V6**</span><span class="sxs-lookup"><span data-stu-id="091b8-143"><span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_connect_layer_v4___fwpm_callout_set_options_auth_connect_layer_v6"></span>**FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_CONNECT\_LAYER\_V4 / FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_CONNECT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091b8-144">Define as opções de classificação em fluxos de saída.</span><span class="sxs-lookup"><span data-stu-id="091b8-144">Sets classify options on outbound flows.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091b8-145"><span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_recv_accept_layer_v4___fwpm_callout_set_options_auth_recv_accept_layer_v6"></span>**FWPM \_ callout \_ define \_ opções \_ auth \_ recv \_ Accept \_ camada \_ v4/FWPM \_ texto explicativo \_ definir \_ opções \_ auth \_ recv \_ aceitar \_ camada \_ V6**</span><span class="sxs-lookup"><span data-stu-id="091b8-145"><span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_recv_accept_layer_v4___fwpm_callout_set_options_auth_recv_accept_layer_v6"></span>**FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_RECV\_ACCEPT\_LAYER\_V4 / FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_RECV\_ACCEPT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091b8-146">Define opções de classificação em fluxos de entrada.</span><span class="sxs-lookup"><span data-stu-id="091b8-146">Sets classify options on inbound flows.</span></span>

> [!Note]  
> <span data-ttu-id="091b8-147">Disponível somente no Windows 8 e no Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="091b8-147">Available only in Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="091b8-148"><span id="FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_reserved_auth_connect_layer_v4___fwpm_callout_reserved_auth_connect_layer_v6"></span>**FWPM \_ balão \_ reservado \_ auth \_ Connect \_ Layer \_ v4/FWPM \_ called \_ \_ auth \_ Connect \_ Layer \_ V6**</span><span class="sxs-lookup"><span data-stu-id="091b8-148"><span id="FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_reserved_auth_connect_layer_v4___fwpm_callout_reserved_auth_connect_layer_v6"></span>**FWPM\_CALLOUT\_RESERVED\_AUTH\_CONNECT\_LAYER\_V4 / FWPM\_CALLOUT\_RESERVED\_AUTH\_CONNECT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091b8-149">Esse identificador é reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="091b8-149">This identifier is reserved for internal use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091b8-150"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6___FWPM_CALLOUT_TEREDO_ALE_LISTEN_V6"></span><span id="fwpm_callout_edge_traversal_ale_listen_v6___fwpm_callout_teredo_ale_listen_v6"></span>**\_Texto explicativo de borda transversal de chamada Ale de FWPM Call \_ \_ \_ \_ \_ V6/FWPM \_ balão de \_ \_ escuta Ale TEREDO \_ \_ V6**</span><span class="sxs-lookup"><span data-stu-id="091b8-150"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6___FWPM_CALLOUT_TEREDO_ALE_LISTEN_V6"></span><span id="fwpm_callout_edge_traversal_ale_listen_v6___fwpm_callout_teredo_ale_listen_v6"></span>**FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_LISTEN\_V6 / FWPM\_CALLOUT\_TEREDO\_ALE\_LISTEN\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091b8-151">Sinaliza para o serviço Teredo que um aplicativo requer um endereço Teredo.</span><span class="sxs-lookup"><span data-stu-id="091b8-151">Signals to the Teredo service that an application requires a Teredo address.</span></span>

> [!Note]  
> <span data-ttu-id="091b8-152">Para o Windows 7 e versões posteriores, use **FWPM \_ callout de chamada \_ Ale de borda \_ transversal \_ \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="091b8-152">For Windows 7 and later, use **FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_LISTEN\_V6**.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="091b8-153"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6___FWPM_CALLOUT_TEREDO_ALE_RESOURCE_ASSIGNMENT_V6"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v6___fwpm_callout_teredo_ale_resource_assignment_v6"></span>**FWPM \_ balão \_ de \_ atribuição de recurso Ale de borda transversal \_ \_ \_ \_ V6/FWPM \_ balão de atribuição de \_ \_ recursos Ale TEREDO \_ \_ \_ V6**</span><span class="sxs-lookup"><span data-stu-id="091b8-153"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6___FWPM_CALLOUT_TEREDO_ALE_RESOURCE_ASSIGNMENT_V6"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v6___fwpm_callout_teredo_ale_resource_assignment_v6"></span>**FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_RESOURCE\_ASSIGNMENT\_V6 / FWPM\_CALLOUT\_TEREDO\_ALE\_RESOURCE\_ASSIGNMENT\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091b8-154">Sinaliza para o serviço Teredo que um aplicativo requer um endereço Teredo.</span><span class="sxs-lookup"><span data-stu-id="091b8-154">Signals to the Teredo service that an application requires a Teredo address.</span></span>

> [!Note]  
> <span data-ttu-id="091b8-155">Para o Windows 7 e posterior, use **FWPM \_ called \_ \_ Ale Edge Traversal de \_ \_ atribuição de recursos \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="091b8-155">For Windows 7 and later, use **FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_RESOURCE\_ASSIGNMENT\_V6**.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="091b8-156"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V4_"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v4_"></span>**FWPM \_ de \_ \_ atribuição de recursos Ale de borda transversal de chamada de texto para o \_ \_ \_ \_ v4**</span><span class="sxs-lookup"><span data-stu-id="091b8-156"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V4_"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v4_"></span>**FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_RESOURCE\_ASSIGNMENT\_V4**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="091b8-157">Esse identificador é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="091b8-157">This identifier is reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091b8-158"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V4"></span><span id="fwpm_callout_edge_traversal_ale_listen_v4"></span>**FWPM \_ texto explicativo de \_ passagem Ale de borda de chamada \_ \_ \_ \_ v4**</span><span class="sxs-lookup"><span data-stu-id="091b8-158"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V4"></span><span id="fwpm_callout_edge_traversal_ale_listen_v4"></span>**FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_LISTEN\_V4**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091b8-159">Esse identificador é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="091b8-159">This identifier is reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="091b8-160"><span id="FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_connect_layer_v4___fwpm_callout_tcp_templates_connect_layer_v6"></span>**FWPM \_ balão \_ TCP \_ modelos de \_ conexão de \_ camada \_ v4/FWPM de \_ texto explicativo \_ modelos TCP de camada de \_ \_ conexão \_ \_ V6**</span><span class="sxs-lookup"><span data-stu-id="091b8-160"><span id="FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_connect_layer_v4___fwpm_callout_tcp_templates_connect_layer_v6"></span>**FWPM\_CALLOUT\_TCP\_TEMPLATES\_CONNECT\_LAYER\_V4 / FWPM\_CALLOUT\_TCP\_TEMPLATES\_CONNECT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091b8-161">Aplica configurações de modelo TCP para conexões de saída correspondentes.</span><span class="sxs-lookup"><span data-stu-id="091b8-161">Applies TCP template settings for matching outgoing connections.</span></span>

> [!Note]  
> <span data-ttu-id="091b8-162">Disponível somente no Windows 8 e no Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="091b8-162">Available only in Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="091b8-163"><span id="FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_accept_layer_v4___fwpm_callout_tcp_templates_accept_layer_v6"></span>**\_Modelos de TCP de texto explicativo FWPM \_ \_ \_ aceitar \_ camada \_ v4/FWPM os \_ \_ \_ modelos TCP \_ aceitam \_ camada \_ V6**</span><span class="sxs-lookup"><span data-stu-id="091b8-163"><span id="FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_accept_layer_v4___fwpm_callout_tcp_templates_accept_layer_v6"></span>**FWPM\_CALLOUT\_TCP\_TEMPLATES\_ACCEPT\_LAYER\_V4 / FWPM\_CALLOUT\_TCP\_TEMPLATES\_ACCEPT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="091b8-164">Aplica configurações de modelo TCP para conexões de entrada correspondentes.</span><span class="sxs-lookup"><span data-stu-id="091b8-164">Applies TCP template settings for matching incoming connections.</span></span>

> [!Note]  
> <span data-ttu-id="091b8-165">Disponível somente no Windows 8 e no Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="091b8-165">Available only in Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="091b8-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="091b8-166">Requirements</span></span>



| <span data-ttu-id="091b8-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="091b8-167">Requirement</span></span> | <span data-ttu-id="091b8-168">Valor</span><span class="sxs-lookup"><span data-stu-id="091b8-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="091b8-169">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="091b8-169">Minimum supported client</span></span><br/> | <span data-ttu-id="091b8-170">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="091b8-170">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="091b8-171">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="091b8-171">Minimum supported server</span></span><br/> | <span data-ttu-id="091b8-172">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="091b8-172">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="091b8-173">parâmetro</span><span class="sxs-lookup"><span data-stu-id="091b8-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="091b8-174"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="091b8-174"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 






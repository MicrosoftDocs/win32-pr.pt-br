---
title: Filtrando identificadores de condição (Fwpmu. h)
description: Os identificadores de condição de filtragem da WFP (Windows Filtering Platform) são representados por um GUID.
ms.assetid: 4f0b970a-e511-4107-8023-22a8775905b9
topic_type:
- apiref
api_name:
- FWPM_CONDITION_INTERFACE_MAC_ADDRESS
- FWPM_CONDITION_MAC_LOCAL_ADDRESS
- FWPM_CONDITION_MAC_REMOTE_ADDRESS
- FWPM_CONDITION_ETHER_TYPE
- FWPM_CONDITION_VLAN_ID
- FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID
- FWPM_CONDITION_NDIS_PORT
- FWPM_CONDITION_NDIS_MEDIA_TYPE
- FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE
- FWPM_CONDITION_L2_FLAGS
- FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE
- FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE
- FWPM_CONDITION_MAC_SOURCE_ADDRESS
- FWPM_CONDITION_MAC_DESTINATION_ADDRESS
- FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE
- FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE
- FWPM_CONDITION_IP_SOURCE_PORT
- FWPM_CONDITION_VSWITCH_ICMP_TYPE
- FWPM_CONDITION_IP_DESTINATION_PORT
- FWPM_CONDITION_VSWITCH_ICMP_CODE
- FWPM_CONDITION_VSWITCH_ID
- FWPM_CONDITION_VSWITCH_NETWORK_TYPE
- FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID
- FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID
- FWPM_CONDITION_VSWITCH_SOURCE_VM_ID
- FWPM_CONDITION_VSWITCH_DESTINATION_VM_ID
- FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE
- FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE
- FWPM_CONDITION_INTERFACE
- FWPM_CONDITION_ALE_PACKAGE_ID
- FWPM_CONDITION_ALE_ORIGINAL_APP_ID
- FWPM_CONDITION_IP_NEXTHOP_ADDRESS
- FWPM_CONDITION_IP_NEXTHOP_INTERFACE
- FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE
- FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE
- FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX
- FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX
- FWPM_CONDITION_ORIGINAL_PROFILE_ID
- FWPM_CONDITION_CURRENT_PROFILE_ID
- FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID
- FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID
- FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID
- FWPM_CONDITION_REAUTHORIZE_REASON
- FWPM_CONDITION_ALE_REAUTH_REASON
- FWPM_CONDITION_ORIGINAL_ICMP_TYPE
- FWPM_CONDITION_IP_PHYSICAL_ARRIVAL_INTERFACE
- FWPM_CONDITION_IP_PHYSICAL_NEXTHOP_INTERFACE
- FWPM_CONDITION_INTERFACE_QUARANTINE_EPOCH
- FWPM_CONDITION_ALE_SIO_FIREWALL_SOCKET_PROPERTY
- FWPM_CONDITION_IP_ARRIVAL_INTERFACE
- FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE
- FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE
- FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX
- FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX
- FWPM_CONDITION_LOCAL_INTERFACE_INDEX
- FWPM_CONDITION_LOCAL_INTERFACE_TYPE
- FWPM_CONDITION_LOCAL_TUNNEL_TYPE
- FWPM_CONDITION_IP_LOCAL_ADDRESS
- FWPM_CONDITION_IP_REMOTE_ADDRESS
- FWPM_CONDITION_IP_SOURCE_ADDRESS
- FWPM_CONDITION_IP_DESTINATION_ADDRESS
- FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE
- FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE
- FWPM_CONDITION_IP_LOCAL_INTERFACE
- FWPM_CONDITION_INTERFACE_TYPE
- FWPM_CONDITION_TUNNEL_TYPE
- FWPM_CONDITION_IP_FORWARD_INTERFACE
- FWPM_CONDITION_IP_PROTOCOL
- FWPM_CONDITION_IP_LOCAL_PORT
- FWPM_CONDITION_ICMP_TYPE
- FWPM_CONDITION_IP_REMOTE_PORT
- FWPM_CONDITION_ICMP_CODE
- FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE
- FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS
- FWPM_CONDITION_EMBEDDED_PROTOCOL
- FWPM_CONDITION_EMBEDDED_LOCAL_PORT
- FWPM_CONDITION_EMBEDDED_REMOTE_PORT
- FWPM_CONDITION_FLAGS
- FWPM_CONDITION_DIRECTION
- FWPM_CONDITION_INTERFACE_INDEX
- FWPM_CONDITION_SUB_INTERFACE_INDEX
- FWPM_CONDITION_SOURCE_INTERFACE_INDEX
- FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX
- FWPM_CONDITION_DESTINATION_INTERFACE_INDEX
- FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX
- FWPM_CONDITION_ALE_APP_ID
- FWPM_CONDITION_ALE_USER_ID
- FWPM_CONDITION_ALE_REMOTE_USER_ID
- FWPM_CONDITION_ALE_REMOTE_MACHINE_ID
- FWPM_CONDITION_ALE_PROMISCUOUS_MODE
- FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT
- FWPM_CONDITION_ALE_NAP_CONTEXT
- FWPM_CONDITION_QM_MODE
- FWPM_CONDITION_KM_AUTH_NAP_CONTEXT
- FWPM_CONDITION_PEER_NAME
- FWPM_CONDITION_REMOTE_ID
- FWPM_CONDITION_AUTHENTICATION_TYPE
- FWPM_CONDITION_KM_TYPE
- FWPM_CONDITION_KM_MODE
- FWPM_CONDITION_IPSEC_POLICY_KEY
- FWPM_CONDITION_AUTHENTICATION_TYPE
- FWPM_CONDITION_REMOTE_USER_TOKEN
- FWPM_CONDITION_RPC_IF_UUID
- FWPM_CONDITION_RPC_IF_VERSION
- FWPM_CONDITION_RPC_IF_FLAG
- FWPM_CONDITION_DCOM_APP_ID
- FWPM_CONDITION_IMAGE_NAME
- FWPM_CONDITION_RPC_PROTOCOL
- FWPM_CONDITION_RPC_AUTH_TYPE
- FWPM_CONDITION_RPC_AUTH_LEVEL
- FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM
- FWPM_CONDITION_SEC_KEY_SIZE
- FWPM_CONDITION_IP_LOCAL_ADDRESS_V4
- FWPM_CONDITION_IP_LOCAL_ADDRESS_V6
- FWPM_CONDITION_IP_REMOTE_ADDRESS_V4
- FWPM_CONDITION_IP_REMOTE_ADDRESS_V6
- FWPM_CONDITION_PIPE
- FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID
- FWPM_CONDITION_RPC_EP_VALUE
- FWPM_CONDITION_RPC_EP_FLAGS
- FWPM_CONDITION_CLIENT_TOKEN
- FWPM_CONDITION_RPC_SERVER_NAME
- FWPM_CONDITION_RPC_SERVER_PORT
- FWPM_CONDITION_RPC_PROXY_AUTH_TYPE
- FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH
- FWPM_CONDITION_CLIENT_CERT_OID
- FWPM_CONDITION_NET_EVENT_TYPE
api_location:
- Fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 617946e5708bb982f96edcad155bcbf2509596dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644236"
---
# <a name="filtering-condition-identifiers"></a><span data-ttu-id="3e505-103">Filtrando identificadores de condição</span><span class="sxs-lookup"><span data-stu-id="3e505-103">Filtering Condition Identifiers</span></span>

<span data-ttu-id="3e505-104">Os identificadores de condição de filtragem da WFP (Windows Filtering Platform) são representados por um **GUID**.</span><span class="sxs-lookup"><span data-stu-id="3e505-104">The Windows Filtering Platform (WFP) filtering condition identifiers are each represented by a **GUID**.</span></span> <span data-ttu-id="3e505-105">O tipo de dados para o valor da condição para cada condição de filtragem é especificado como um [**\_ \_ tipo de dados fwp**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span><span class="sxs-lookup"><span data-stu-id="3e505-105">The data type for the condition value for each filtering condition is specified as an [**FWP\_DATA\_TYPE**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span></span> <span data-ttu-id="3e505-106">Esses identificadores e seus tipos de dados são definidos aqui.</span><span class="sxs-lookup"><span data-stu-id="3e505-106">These identifiers and their data types are defined here.</span></span>

<span data-ttu-id="3e505-107">As condições padrão são listadas primeiro, seguidas pelas condições específicas para o modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="3e505-107">The standard conditions are listed first, followed by the conditions specific to user mode.</span></span> <span data-ttu-id="3e505-108">As condições são agrupadas por sistema operacional com suporte, para que você possa identificar facilmente quais condições têm suporte para um determinado so.</span><span class="sxs-lookup"><span data-stu-id="3e505-108">Conditions are grouped by supported operating system, so that you can easily tell which conditions are supported for a given OS.</span></span>

> [!Note]  
> <span data-ttu-id="3e505-109">Cada uma das condições de filtragem a seguir está disponível apenas em um subconjunto das camadas de filtragem WFP.</span><span class="sxs-lookup"><span data-stu-id="3e505-109">Each of the following filtering conditions is available only at a subset of the WFP filtering layers.</span></span> <span data-ttu-id="3e505-110">Para obter mais informações sobre a disponibilidade de cada condição em uma determinada camada, consulte [**condições de filtragem disponíveis em cada camada de filtragem**](filtering-conditions-available-at-each-filtering-layer.md).</span><span class="sxs-lookup"><span data-stu-id="3e505-110">For more information on each condition's availability at any given layer, see [**Filtering Conditions Available at Each Filtering Layer**](filtering-conditions-available-at-each-filtering-layer.md).</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="3e505-111">Condições disponíveis para o Windows 8 e o Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3e505-111">Conditions available for Windows 8 and Windows Server 2012</span></span></th>
<th style="text-align: left;"><span data-ttu-id="3e505-112">Description</span><span class="sxs-lookup"><span data-stu-id="3e505-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE_MAC_ADDRESS"></span><span id="fwpm_condition_interface_mac_address"></span><dl> <span data-ttu-id="3e505-113"><dt><strong>FWPM_CONDITION_INTERFACE_MAC_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-113"><dt><strong>FWPM_CONDITION_INTERFACE_MAC_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-114">O endereço MAC de uma interface local específica.</span><span class="sxs-lookup"><span data-stu-id="3e505-114">The MAC address of a particular local interface.</span></span><br/> <span data-ttu-id="3e505-115"><strong>Tipo de dados:</strong> FWP_BYTE_ARRAY6_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-115"><strong>Data type:</strong> FWP_BYTE_ARRAY6_TYPE</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_LOCAL_ADDRESS"></span><span id="fwpm_condition_mac_local_address"></span><dl> <span data-ttu-id="3e505-116"><dt><strong>FWPM_CONDITION_MAC_LOCAL_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-116"><dt><strong>FWPM_CONDITION_MAC_LOCAL_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-117">Endereço de destino de um quadro de entrada ou endereço de origem de um quadro de saída.</span><span class="sxs-lookup"><span data-stu-id="3e505-117">Destination address of an inbound frame, or source address of an outbound frame.</span></span><br/> <span data-ttu-id="3e505-118"><strong>Tipo de dados:</strong> FWP_BYTE_ARRAY6_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-118"><strong>Data type:</strong> FWP_BYTE_ARRAY6_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_REMOTE_ADDRESS"></span><span id="fwpm_condition_mac_remote_address"></span><dl> <span data-ttu-id="3e505-119"><dt><strong>FWPM_CONDITION_MAC_REMOTE_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-119"><dt><strong>FWPM_CONDITION_MAC_REMOTE_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-120">Endereço de origem de um quadro de entrada ou endereço de destino de um quadro de saída.</span><span class="sxs-lookup"><span data-stu-id="3e505-120">Source address of an inbound frame, or destination address of an outbound frame.</span></span><br/> <span data-ttu-id="3e505-121"><strong>Tipo de dados:</strong> FWP_BYTE_ARRAY6_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-121"><strong>Data type:</strong> FWP_BYTE_ARRAY6_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ETHER_TYPE"></span><span id="fwpm_condition_ether_type"></span><dl> <span data-ttu-id="3e505-122"><dt><strong>FWPM_CONDITION_ETHER_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-122"><dt><strong>FWPM_CONDITION_ETHER_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-123">O tipo de dados de carga de rede Ethernet v2.</span><span class="sxs-lookup"><span data-stu-id="3e505-123">The Ethernet V2 network payload data type.</span></span> <span data-ttu-id="3e505-124">(Consulte ETHERNET_TYPE_IPV4, etc. em netiodef. h.)</span><span class="sxs-lookup"><span data-stu-id="3e505-124">(See ETHERNET_TYPE_IPV4, etc. in netiodef.h.)</span></span><br/> <span data-ttu-id="3e505-125"><strong>Tipo de dados:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="3e505-125"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VLAN_ID"></span><span id="fwpm_condition_vlan_id"></span><dl> <span data-ttu-id="3e505-126"><dt><strong>FWPM_CONDITION_VLAN_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-126"><dt><strong>FWPM_CONDITION_VLAN_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-127">Os 16 bits de cabeçalho de VLAN, incluindo os campos VID, IPF e Priority de acordo com o padrão 802.1 q (consulte VLAN_TAG em netiodef. h para as posições de bitfields).</span><span class="sxs-lookup"><span data-stu-id="3e505-127">The 16-bits of VLAN header including the VID, CFI, and Priority fields as per the 802.1q standard (see VLAN_TAG in netiodef.h for the positions of the bitfields).</span></span><br/> <span data-ttu-id="3e505-128"><strong>Tipo de dados:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="3e505-128"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID"></span><span id="fwpm_condition_vswitch_tenant_network_id"></span><dl> <span data-ttu-id="3e505-129"><dt><strong>FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-129"><dt><strong>FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-130">Identificador exclusivo para a rede vSwitch.</span><span class="sxs-lookup"><span data-stu-id="3e505-130">Unique identifier for the vSwitch network.</span></span> <span data-ttu-id="3e505-131">Não pode ser usado em conjunto com VLAN_IDs.</span><span class="sxs-lookup"><span data-stu-id="3e505-131">Cannot be used in conjunction with VLAN_IDs.</span></span><br/> <span data-ttu-id="3e505-132"><strong>Tipo de dados:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="3e505-132"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_NDIS_PORT"></span><span id="fwpm_condition_ndis_port"></span><dl> <span data-ttu-id="3e505-133"><dt><strong>FWPM_CONDITION_NDIS_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-133"><dt><strong>FWPM_CONDITION_NDIS_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-134">O número da porta da porta NDIS.</span><span class="sxs-lookup"><span data-stu-id="3e505-134">The port number of the NDIS port.</span></span><br/> <span data-ttu-id="3e505-135"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-135"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_NDIS_MEDIA_TYPE"></span><span id="fwpm_condition_ndis_media_type"></span><dl> <span data-ttu-id="3e505-136"><dt><strong>FWPM_CONDITION_NDIS_MEDIA_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-136"><dt><strong>FWPM_CONDITION_NDIS_MEDIA_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-137">O tipo de mídia da porta NDIS.</span><span class="sxs-lookup"><span data-stu-id="3e505-137">The media type of the NDIS port.</span></span><br/> <span data-ttu-id="3e505-138"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-138"><strong>Data type:</strong> FWP_UINT32</span></span><br/> <span data-ttu-id="3e505-139"><strong>Valores possíveis:</strong> Qualquer um dos <strong>NDIS_MEDIUM</strong> valores de enumeração.</span><span class="sxs-lookup"><span data-stu-id="3e505-139"><strong>Possible values:</strong> Any of the <strong>NDIS_MEDIUM</strong> enumeration values.</span></span> <span data-ttu-id="3e505-140">(Consulte Ntddndis. h.)</span><span class="sxs-lookup"><span data-stu-id="3e505-140">(See ntddndis.h.)</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE"></span><span id="fwpm_condition_ndis_physical_media_type"></span><dl> <span data-ttu-id="3e505-141"><dt><strong>FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-141"><dt><strong>FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-142">O tipo de mídia física da porta NDIS.</span><span class="sxs-lookup"><span data-stu-id="3e505-142">The physical media type of the NDIS port.</span></span><br/> <span data-ttu-id="3e505-143"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-143"><strong>Data type:</strong> FWP_UINT32</span></span><br/> <span data-ttu-id="3e505-144"><strong>Valores possíveis:</strong> Qualquer um dos <strong>NDIS_PHYSICAL_MEDIUM</strong> valores de enumeração.</span><span class="sxs-lookup"><span data-stu-id="3e505-144"><strong>Possible values:</strong> Any of the <strong>NDIS_PHYSICAL_MEDIUM</strong> enumeration values.</span></span> <span data-ttu-id="3e505-145">(Consulte Ntddndis. h.)</span><span class="sxs-lookup"><span data-stu-id="3e505-145">(See ntddndis.h.)</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_L2_FLAGS"></span><span id="fwpm_condition_l2_flags"></span><dl> <span data-ttu-id="3e505-146"><dt><strong>FWPM_CONDITION_L2_FLAGS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-146"><dt><strong>FWPM_CONDITION_L2_FLAGS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-147">Uma operação OR de uma combinação de sinalizadores de condição de filtragem.</span><span class="sxs-lookup"><span data-stu-id="3e505-147">A bitwise OR of a combination of filtering condition flags.</span></span> <br/> <span data-ttu-id="3e505-148"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-148"><strong>Data type:</strong> FWP_UINT32</span></span><br/> <span data-ttu-id="3e505-149"><strong>Valores possíveis:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="3e505-149"><strong>Possible values:  </strong>
</span></span><ul>
<li><span data-ttu-id="3e505-150">FWP_CONDITION_L2_IS_MOBILE_BROADBAND</span><span class="sxs-lookup"><span data-stu-id="3e505-150">FWP_CONDITION_L2_IS_MOBILE_BROADBAND</span></span></li>
<li><span data-ttu-id="3e505-151">FWP_CONDITION_L2_IS_NATIVE_ETHERNET</span><span class="sxs-lookup"><span data-stu-id="3e505-151">FWP_CONDITION_L2_IS_NATIVE_ETHERNET</span></span></li>
<li><span data-ttu-id="3e505-152">FWP_CONDITION_L2_IS_WIFI</span><span class="sxs-lookup"><span data-stu-id="3e505-152">FWP_CONDITION_L2_IS_WIFI</span></span></li>
<li><span data-ttu-id="3e505-153">FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA</span><span class="sxs-lookup"><span data-stu-id="3e505-153">FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_local_address_type"></span><dl> <span data-ttu-id="3e505-154"><dt><strong>FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-154"><dt><strong>FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-155">O tipo de endereço do endereço local físico.</span><span class="sxs-lookup"><span data-stu-id="3e505-155">The address type of the physical local address.</span></span><br/> <span data-ttu-id="3e505-156"><strong>Tipo de dados:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="3e505-156"><strong>Data type:</strong> FWP_UINT8</span></span><br/> <span data-ttu-id="3e505-157"><strong>Valores possíveis:</strong> Qualquer um dos seguintes <strong>DL_ADDRESS_TYPE</strong> valores de enumeração.</span><span class="sxs-lookup"><span data-stu-id="3e505-157"><strong>Possible values:</strong> Any of the following <strong>DL_ADDRESS_TYPE</strong> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="3e505-158">DlUnicast</span><span class="sxs-lookup"><span data-stu-id="3e505-158">DlUnicast</span></span></li>
<li><span data-ttu-id="3e505-159">DlMulticast</span><span class="sxs-lookup"><span data-stu-id="3e505-159">DlMulticast</span></span></li>
<li><span data-ttu-id="3e505-160">DlBroadcast</span><span class="sxs-lookup"><span data-stu-id="3e505-160">DlBroadcast</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_remote_address_type"></span><dl> <span data-ttu-id="3e505-161"><dt><strong>FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-161"><dt><strong>FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-162">O tipo de endereço do endereço remoto físico.</span><span class="sxs-lookup"><span data-stu-id="3e505-162">The address type of the physical remote address.</span></span><br/> <span data-ttu-id="3e505-163"><strong>Tipo de dados:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="3e505-163"><strong>Data type:</strong> FWP_UINT8</span></span><br/> <span data-ttu-id="3e505-164"><strong>Valores possíveis:</strong> Qualquer um dos seguintes <strong>DL_ADDRESS_TYPE</strong> valores de enumeração.</span><span class="sxs-lookup"><span data-stu-id="3e505-164"><strong>Possible values:</strong> Any of the following <strong>DL_ADDRESS_TYPE</strong> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="3e505-165">DlUnicast</span><span class="sxs-lookup"><span data-stu-id="3e505-165">DlUnicast</span></span></li>
<li><span data-ttu-id="3e505-166">DlMulticast</span><span class="sxs-lookup"><span data-stu-id="3e505-166">DlMulticast</span></span></li>
<li><span data-ttu-id="3e505-167">DlBroadcast</span><span class="sxs-lookup"><span data-stu-id="3e505-167">DlBroadcast</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_SOURCE_ADDRESS"></span><span id="fwpm_condition_mac_source_address"></span><dl> <span data-ttu-id="3e505-168"><dt><strong>FWPM_CONDITION_MAC_SOURCE_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-168"><dt><strong>FWPM_CONDITION_MAC_SOURCE_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-169">O endereço de origem físico de um quadro.</span><span class="sxs-lookup"><span data-stu-id="3e505-169">The physical source address of a frame.</span></span><br/> <span data-ttu-id="3e505-170"><strong>Tipo de dados:</strong> FWP_BYTE_ARRAY6_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-170"><strong>Data type:</strong> FWP_BYTE_ARRAY6_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_DESTINATION_ADDRESS"></span><span id="fwpm_condition_mac_destination_address"></span><dl> <span data-ttu-id="3e505-171"><dt><strong>FWPM_CONDITION_MAC_DESTINATION_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-171"><dt><strong>FWPM_CONDITION_MAC_DESTINATION_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-172">O endereço de destino físico de um quadro.</span><span class="sxs-lookup"><span data-stu-id="3e505-172">The physical destination address of a frame.</span></span><br/> <span data-ttu-id="3e505-173"><strong>Tipo de dados:</strong> FWP_BYTE_ARRAY6_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-173"><strong>Data type:</strong> FWP_BYTE_ARRAY6_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_source_address_type"></span><dl> <span data-ttu-id="3e505-174"><dt><strong>FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-174"><dt><strong>FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-175">O tipo de endereço do endereço de destino físico.</span><span class="sxs-lookup"><span data-stu-id="3e505-175">The address type of the physical destination address.</span></span><br/> <span data-ttu-id="3e505-176"><strong>Tipo de dados:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="3e505-176"><strong>Data type:</strong> FWP_UINT8</span></span><br/> <span data-ttu-id="3e505-177"><strong>Valores possíveis:</strong> Qualquer um dos seguintes <strong>DL_ADDRESS_TYPE</strong> valores de enumeração.</span><span class="sxs-lookup"><span data-stu-id="3e505-177"><strong>Possible values:</strong> Any of the following <strong>DL_ADDRESS_TYPE</strong> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="3e505-178">DlUnicast</span><span class="sxs-lookup"><span data-stu-id="3e505-178">DlUnicast</span></span></li>
<li><span data-ttu-id="3e505-179">DlMulticast</span><span class="sxs-lookup"><span data-stu-id="3e505-179">DlMulticast</span></span></li>
<li><span data-ttu-id="3e505-180">DlBroadcast</span><span class="sxs-lookup"><span data-stu-id="3e505-180">DlBroadcast</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_destination_address_type"></span><dl> <span data-ttu-id="3e505-181"><dt><strong>FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-181"><dt><strong>FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-182">O tipo de endereço do endereço de destino físico.</span><span class="sxs-lookup"><span data-stu-id="3e505-182">The address type of the physical destination address.</span></span><br/> <span data-ttu-id="3e505-183"><strong>Tipo de dados:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="3e505-183"><strong>Data type:</strong> FWP_UINT8</span></span><br/> <span data-ttu-id="3e505-184"><strong>Valores possíveis:</strong> Qualquer um dos seguintes <strong>DL_ADDRESS_TYPE</strong> valores de enumeração.</span><span class="sxs-lookup"><span data-stu-id="3e505-184"><strong>Possible values:</strong> Any of the following <strong>DL_ADDRESS_TYPE</strong> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="3e505-185">DlUnicast</span><span class="sxs-lookup"><span data-stu-id="3e505-185">DlUnicast</span></span></li>
<li><span data-ttu-id="3e505-186">DlMulticast</span><span class="sxs-lookup"><span data-stu-id="3e505-186">DlMulticast</span></span></li>
<li><span data-ttu-id="3e505-187">DlBroadcast</span><span class="sxs-lookup"><span data-stu-id="3e505-187">DlBroadcast</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_SOURCE_PORT"></span><span id="fwpm_condition_ip_source_port"></span><dl> <span data-ttu-id="3e505-188"><dt><strong>FWPM_CONDITION_IP_SOURCE_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-188"><dt><strong>FWPM_CONDITION_IP_SOURCE_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-189">A porta de origem do transporte do pacote.</span><span class="sxs-lookup"><span data-stu-id="3e505-189">The source port of the packet's transport.</span></span><br/> <span data-ttu-id="3e505-190"><strong>Tipo de dados:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="3e505-190"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_ICMP_TYPE"></span><span id="fwpm_condition_vswitch_icmp_type"></span><dl> <span data-ttu-id="3e505-191"><dt><strong>FWPM_CONDITION_VSWITCH_ICMP_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-191"><dt><strong>FWPM_CONDITION_VSWITCH_ICMP_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-192">O campo tipo de ICMP, conforme especificado no RFC 792.</span><span class="sxs-lookup"><span data-stu-id="3e505-192">The ICMP type field, as specified in RFC 792.</span></span><br/> <span data-ttu-id="3e505-193"><strong>Tipo de dados:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="3e505-193"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_DESTINATION_PORT"></span><span id="fwpm_condition_ip_destination_port"></span><dl> <span data-ttu-id="3e505-194"><dt><strong>FWPM_CONDITION_IP_DESTINATION_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-194"><dt><strong>FWPM_CONDITION_IP_DESTINATION_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-195">A porta de destino do transporte do pacote.</span><span class="sxs-lookup"><span data-stu-id="3e505-195">The destination port of the packet's transport.</span></span><br/> <span data-ttu-id="3e505-196"><strong>Tipo de dados:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="3e505-196"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_ICMP_CODE"></span><span id="fwpm_condition_vswitch_icmp_code"></span><dl> <span data-ttu-id="3e505-197"><dt><strong>FWPM_CONDITION_VSWITCH_ICMP_CODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-197"><dt><strong>FWPM_CONDITION_VSWITCH_ICMP_CODE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-198">O campo de código ICMP, conforme especificado no RFC 792.</span><span class="sxs-lookup"><span data-stu-id="3e505-198">The ICMP code field, as specified in RFC 792.</span></span> <br/> <span data-ttu-id="3e505-199"><strong>Tipo de dados:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="3e505-199"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_ID"></span><span id="fwpm_condition_vswitch_id"></span><dl> <span data-ttu-id="3e505-200"><dt><strong>FWPM_CONDITION_VSWITCH_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-200"><dt><strong>FWPM_CONDITION_VSWITCH_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-201">Identificador exclusivo de uma instância de vSwitch.</span><span class="sxs-lookup"><span data-stu-id="3e505-201">Unique identifier of an vSwitch instance.</span></span><br/> <span data-ttu-id="3e505-202"><strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-202"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_NETWORK_TYPE"></span><span id="fwpm_condition_vswitch_network_type"></span><dl> <span data-ttu-id="3e505-203"><dt><strong>FWPM_CONDITION_VSWITCH_NETWORK_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-203"><dt><strong>FWPM_CONDITION_VSWITCH_NETWORK_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-204">Especifica se a instância do vSwitch faz parte de uma rede virtual externa, interna ou privada.</span><span class="sxs-lookup"><span data-stu-id="3e505-204">Specifies whether the vSwitch instance is part of an external, internal, or private virtual network.</span></span><br/> <span data-ttu-id="3e505-205"><strong>Tipo de dados:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="3e505-205"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID"></span><span id="fwpm_condition_vswitch_source_interface_id"></span><dl> <span data-ttu-id="3e505-206"><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-206"><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-207">Identificador exclusivo da origem do pacote atual.</span><span class="sxs-lookup"><span data-stu-id="3e505-207">Unique identifier of the source of the current packet.</span></span> <span data-ttu-id="3e505-208">(O nome de uma VM-NIC, P-NIC ou V-NIC.)</span><span class="sxs-lookup"><span data-stu-id="3e505-208">(The name of a VM-NIC, P-NIC, or V-NIC.)</span></span><br/> <span data-ttu-id="3e505-209"><strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-209"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID"></span><span id="fwpm_condition_vswitch_destination_interface_id"></span><dl> <span data-ttu-id="3e505-210"><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-210"><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-211">Identificador exclusivo do destino do pacote atual.</span><span class="sxs-lookup"><span data-stu-id="3e505-211">Unique identifier of the destination of the current packet.</span></span> <span data-ttu-id="3e505-212">(O nome de uma VM-NIC, P-NIC ou V-NIC.)</span><span class="sxs-lookup"><span data-stu-id="3e505-212">(The name of a VM-NIC, P-NIC, or V-NIC.)</span></span><br/> <span data-ttu-id="3e505-213"><strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-213"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_SOURCE_VM_ID"></span><span id="fwpm_condition_vswitch_source_vm_id"></span><dl> <span data-ttu-id="3e505-214"><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-214"><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-215">Identificador exclusivo da máquina virtual de origem do vSwitch.</span><span class="sxs-lookup"><span data-stu-id="3e505-215">Unique identifier of the vSwitch source virtual machine.</span></span><br/> <span data-ttu-id="3e505-216"><strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-216"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_DESTINATION_VM_ID"></span><span id="fwpm_condition_vswitch_destination_vm_id"></span><dl> <span data-ttu-id="3e505-217"><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_VM_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-217"><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_VM_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-218">Identificador exclusivo da máquina virtual de destino do vSwitch.</span><span class="sxs-lookup"><span data-stu-id="3e505-218">Unique identifier of the vSwitch destination virtual machine.</span></span><br/> <span data-ttu-id="3e505-219"><strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-219"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE"></span><span id="fwpm_condition_vswitch_source_interface_type"></span><dl> <span data-ttu-id="3e505-220"><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-220"><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-221">Tipo de interface da origem do pacote atual.</span><span class="sxs-lookup"><span data-stu-id="3e505-221">Interface type of the source of the current packet.</span></span><br/> <span data-ttu-id="3e505-222"><strong>Tipo de dados:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="3e505-222"><strong>Data type:</strong> FWP_UINT8</span></span><br/> <span data-ttu-id="3e505-223"><strong>Valores possíveis:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="3e505-223"><strong>Possible values:  </strong>
</span></span><ul>
<li><span data-ttu-id="3e505-224">SwitchNicSyntheticNic (quando o tipo de interface é VM-NIC)</span><span class="sxs-lookup"><span data-stu-id="3e505-224">SwitchNicSyntheticNic (when interface type is VM-NIC)</span></span></li>
<li><span data-ttu-id="3e505-225">SwitchNicEmulatedNic (quando o tipo de interface é VM-NIC)</span><span class="sxs-lookup"><span data-stu-id="3e505-225">SwitchNicEmulatedNic (when interface type is VM-NIC)</span></span></li>
<li><span data-ttu-id="3e505-226">SwitchNicPhysicalNic (quando o tipo de interface é P-NIC)</span><span class="sxs-lookup"><span data-stu-id="3e505-226">SwitchNicPhysicalNic (when interface type is P-NIC)</span></span></li>
<li><span data-ttu-id="3e505-227">SwitchNicVNic (quando o tipo de interface é V-NIC, conectado à partição de host)</span><span class="sxs-lookup"><span data-stu-id="3e505-227">SwitchNicVNic (when interface type is V-NIC, connected to the host partition)</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE"></span><span id="fwpm_condition_vswitch_destination_interface_type"></span><dl> <span data-ttu-id="3e505-228"><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-228"><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-229">Tipo de interface do destino do pacote atual.</span><span class="sxs-lookup"><span data-stu-id="3e505-229">Interface type of the destination of the current packet.</span></span><br/> <span data-ttu-id="3e505-230"><strong>Tipo de dados:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="3e505-230"><strong>Data type:</strong> FWP_UINT8</span></span><br/> <span data-ttu-id="3e505-231"><strong>Valores possíveis:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="3e505-231"><strong>Possible values:  </strong>
</span></span><ul>
<li><span data-ttu-id="3e505-232">SwitchNicSyntheticNic (quando o tipo de interface é VM-NIC)</span><span class="sxs-lookup"><span data-stu-id="3e505-232">SwitchNicSyntheticNic (when interface type is VM-NIC)</span></span></li>
<li><span data-ttu-id="3e505-233">SwitchNicEmulatedNic (quando o tipo de interface é VM-NIC)</span><span class="sxs-lookup"><span data-stu-id="3e505-233">SwitchNicEmulatedNic (when interface type is VM-NIC)</span></span></li>
<li><span data-ttu-id="3e505-234">SwitchNicPhysicalNic (quando o tipo de interface é P-NIC)</span><span class="sxs-lookup"><span data-stu-id="3e505-234">SwitchNicPhysicalNic (when interface type is P-NIC)</span></span></li>
<li><span data-ttu-id="3e505-235">SwitchNicVNic (quando o tipo de interface é V-NIC, conectado à partição de host)</span><span class="sxs-lookup"><span data-stu-id="3e505-235">SwitchNicVNic (when interface type is V-NIC, connected to the host partition)</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE"></span><span id="fwpm_condition_interface"></span><dl> <span data-ttu-id="3e505-236"><dt><strong>FWPM_CONDITION_INTERFACE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-236"><dt><strong>FWPM_CONDITION_INTERFACE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-237">O LUID para a interface de rede associada ao endereço IP local.</span><span class="sxs-lookup"><span data-stu-id="3e505-237">The LUID for the network interface associated with the local IP address.</span></span> <br/> <span data-ttu-id="3e505-238"><strong>Tipo de dados:</strong> FWP_UINT64</span><span class="sxs-lookup"><span data-stu-id="3e505-238"><strong>Data type:</strong> FWP_UINT64</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_PACKAGE_ID"></span><span id="fwpm_condition_ale_package_id"></span><dl> <span data-ttu-id="3e505-239"><dt><strong>FWPM_CONDITION_ALE_PACKAGE_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-239"><dt><strong>FWPM_CONDITION_ALE_PACKAGE_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-240">O SID (identificador de segurança) de um contêiner de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3e505-240">The security identifier (SID) of an app container.</span></span><br/> <span data-ttu-id="3e505-241"><strong>Tipo de dados:</strong> FWP_SID</span><span class="sxs-lookup"><span data-stu-id="3e505-241"><strong>Data type:</strong> FWP_SID</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_ORIGINAL_APP_ID"></span><span id="fwpm_condition_ale_original_app_id"></span><dl> <span data-ttu-id="3e505-242"><dt><strong>FWPM_CONDITION_ALE_ORIGINAL_APP_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-242"><dt><strong>FWPM_CONDITION_ALE_ORIGINAL_APP_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-243">O caminho do dispositivo totalmente qualificado do aplicativo, como &quot; \device0\hardiskvolume1\Program Files\Application.exe&quot; .</span><span class="sxs-lookup"><span data-stu-id="3e505-243">The fully qualified device path of the application, such as &quot;\device0\hardiskvolume1\Program Files\Application.exe&quot;.</span></span> <span data-ttu-id="3e505-244">Quando uma conexão for redirecionada, esse será o identificador do aplicativo de origem; caso contrário, isso será o mesmo que <strong>FWPM_CONDITION_ALE_APP_ID</strong>.</span><span class="sxs-lookup"><span data-stu-id="3e505-244">When a connection has been redirected, this will be the identifier of the originating app; otherwise this will be the same as <strong>FWPM_CONDITION_ALE_APP_ID</strong>.</span></span><br/> <span data-ttu-id="3e505-245"><strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-245"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
</tbody>
</table>





| <span data-ttu-id="3e505-246">Condições disponíveis para o Windows 7, o Windows Server 2008 R2 e posterior</span><span class="sxs-lookup"><span data-stu-id="3e505-246">Conditions available for Windows 7, Windows Server 2008 R2, and later</span></span>                                                                                                                                                                                                    | <span data-ttu-id="3e505-247">Description</span><span class="sxs-lookup"><span data-stu-id="3e505-247">Description</span></span>                                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_CONDITION_IP_NEXTHOP_ADDRESS"></span><span id="fwpm_condition_ip_nexthop_address"></span><dl> <span data-ttu-id="3e505-248"><dt>**\_ \_ \_ endereço IP NEXTHOP \_ da condição FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="3e505-248"><dt>**FWPM\_CONDITION\_IP\_NEXTHOP\_ADDRESS**</dt></span></span> </dl>                                             | <span data-ttu-id="3e505-249">O endereço IP da interface de próximo salto.</span><span class="sxs-lookup"><span data-stu-id="3e505-249">The IP address of the next-hop interface.</span></span><br/> <span data-ttu-id="3e505-250">**Tipo de dados:** \_Máscara de \_ endereço \_ v4 de fwp</span><span class="sxs-lookup"><span data-stu-id="3e505-250">**Data type:** FWP\_V4\_ADDR\_MASK</span></span><br/>                                                                                                                                                                                        |
| <span id="FWPM_CONDITION_IP_NEXTHOP_INTERFACE"></span><span id="fwpm_condition_ip_nexthop_interface"></span><dl> <span data-ttu-id="3e505-251"><dt>**\_ \_ interface NEXTHOP de IP de condição FWPM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3e505-251"><dt>**FWPM\_CONDITION\_IP\_NEXTHOP\_INTERFACE**</dt></span></span> </dl>                                       | <span data-ttu-id="3e505-252">A interface de próximo salto da qual o pacote será desparte.</span><span class="sxs-lookup"><span data-stu-id="3e505-252">The next-hop interface from which the packet will be departing.</span></span> <br/> <span data-ttu-id="3e505-253">**Tipo de dados:** FWP \_ UINT64</span><span class="sxs-lookup"><span data-stu-id="3e505-253">**Data type:** FWP\_UINT64</span></span><br/>                                                                                                                                                                         |
| <span id="FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE"></span><span id="fwpm_condition_nexthop_interface_type"></span><dl> <span data-ttu-id="3e505-254"><dt>**\_tipo de \_ \_ interface NEXTHOP da condição \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="3e505-254"><dt>**FWPM\_CONDITION\_NEXTHOP\_INTERFACE\_TYPE**</dt></span></span> </dl>                                 | <span data-ttu-id="3e505-255">O tipo de interface da interface de próximo salto.</span><span class="sxs-lookup"><span data-stu-id="3e505-255">The interface type of the next-hop interface.</span></span><br/> <span data-ttu-id="3e505-256">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-256">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                            |
| <span id="FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE"></span><span id="fwpm_condition_nexthop_tunnel_type"></span><dl> <span data-ttu-id="3e505-257"><dt>**\_tipo de \_ \_ túnel NEXTHOP da condição \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="3e505-257"><dt>**FWPM\_CONDITION\_NEXTHOP\_TUNNEL\_TYPE**</dt></span></span> </dl>                                          | <span data-ttu-id="3e505-258">O tipo de túnel da interface de próximo salto.</span><span class="sxs-lookup"><span data-stu-id="3e505-258">The tunnel type of the next-hop interface.</span></span><br/> <span data-ttu-id="3e505-259">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-259">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                               |
| <span id="FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX"></span><span id="fwpm_condition_nexthop_interface_index"></span><dl> <span data-ttu-id="3e505-260"><dt>**\_índice da \_ \_ interface NEXTHOP da condição \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="3e505-260"><dt>**FWPM\_CONDITION\_NEXTHOP\_INTERFACE\_INDEX**</dt></span></span> </dl>                              | <span data-ttu-id="3e505-261">O índice de interface da interface de próximo salto.</span><span class="sxs-lookup"><span data-stu-id="3e505-261">The interface index of the next-hop interface.</span></span><br/> <span data-ttu-id="3e505-262">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-262">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                           |
| <span id="FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_nexthop_sub_interface_index"></span><dl> <span data-ttu-id="3e505-263"><dt>**\_índice de \_ sub \_ - \_ interface NEXTHOP da \_ condição FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="3e505-263"><dt>**FWPM\_CONDITION\_NEXTHOP\_SUB\_INTERFACE\_INDEX**</dt></span></span> </dl>                 | <span data-ttu-id="3e505-264">O índice de subinterface da interface de próximo salto.</span><span class="sxs-lookup"><span data-stu-id="3e505-264">The sub-interface index of the next-hop interface.</span></span><br/> <span data-ttu-id="3e505-265">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-265">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                       |
| <span id="FWPM_CONDITION_ORIGINAL_PROFILE_ID"></span><span id="fwpm_condition_original_profile_id"></span><dl> <span data-ttu-id="3e505-266"><dt>**\_ID do \_ \_ perfil original da condição \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="3e505-266"><dt>**FWPM\_CONDITION\_ORIGINAL\_PROFILE\_ID**</dt></span></span> </dl>                                          | <span data-ttu-id="3e505-267">A categoria de rede da interface de chegada ou do próximo salto por meio da qual o fluxo ALE (entrada ou saída) é criado.</span><span class="sxs-lookup"><span data-stu-id="3e505-267">The network category of the arrival or next-hop interface through which the ALE flow (inbound or outbound) is created.</span></span> <br/> <span data-ttu-id="3e505-268">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-268">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                  |
| <span id="FWPM_CONDITION_CURRENT_PROFILE_ID"></span><span id="fwpm_condition_current_profile_id"></span><dl> <span data-ttu-id="3e505-269"><dt>**\_ID do \_ \_ perfil atual da condição \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="3e505-269"><dt>**FWPM\_CONDITION\_CURRENT\_PROFILE\_ID**</dt></span></span> </dl>                                             | <span data-ttu-id="3e505-270">A categoria de rede da interface de chegada ou do próximo salto por meio da qual o pacote atual (entrada ou saída) é criado.</span><span class="sxs-lookup"><span data-stu-id="3e505-270">The network category of the arrival or next-hop interface through which the current packet (inbound or outbound) is created.</span></span> <br/> <span data-ttu-id="3e505-271">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-271">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                            |
| <span id="FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID"></span><span id="fwpm_condition_local_interface_profile_id"></span><dl> <span data-ttu-id="3e505-272"><dt>**\_ID do \_ \_ perfil da interface local da condição \_ FWPM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3e505-272"><dt>**FWPM\_CONDITION\_LOCAL\_INTERFACE\_PROFILE\_ID**</dt></span></span> </dl>                    | <span data-ttu-id="3e505-273">A categoria de rede da interface de entrega.</span><span class="sxs-lookup"><span data-stu-id="3e505-273">The network category of the delivery interface.</span></span><br/> <span data-ttu-id="3e505-274">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-274">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                          |
| <span id="FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID"></span><span id="fwpm_condition_arrival_interface_profile_id"></span><dl> <span data-ttu-id="3e505-275"><dt>**\_ID do \_ perfil da interface de chegada da condição FWPM \_ \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3e505-275"><dt>**FWPM\_CONDITION\_ARRIVAL\_INTERFACE\_PROFILE\_ID**</dt></span></span> </dl>              | <span data-ttu-id="3e505-276">A categoria de rede da interface de chegada.</span><span class="sxs-lookup"><span data-stu-id="3e505-276">The network category of the arrival interface.</span></span><br/> <span data-ttu-id="3e505-277">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-277">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                           |
| <span id="FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID"></span><span id="fwpm_condition_nexthop_interface_profile_id"></span><dl> <span data-ttu-id="3e505-278"><dt>**\_ID do \_ \_ perfil da interface NEXTHOP \_ \_ do FWPM Condition**</dt></span><span class="sxs-lookup"><span data-stu-id="3e505-278"><dt>**FWPM\_CONDITION\_NEXTHOP\_INTERFACE\_PROFILE\_ID**</dt></span></span> </dl>              | <span data-ttu-id="3e505-279">A categoria de rede da interface de próximo salto.</span><span class="sxs-lookup"><span data-stu-id="3e505-279">The network category of the next-hop interface.</span></span><br/> <span data-ttu-id="3e505-280">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-280">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                          |
| <span id="FWPM_CONDITION_REAUTHORIZE_REASON"></span><span id="fwpm_condition_reauthorize_reason"></span><dl> <span data-ttu-id="3e505-281"><dt>**\_motivo da \_ Reautorização da \_ condição FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="3e505-281"><dt>**FWPM\_CONDITION\_REAUTHORIZE\_REASON**</dt></span></span> </dl>                                              | <span data-ttu-id="3e505-282">O motivo para reautorizar uma conexão anteriormente autorizada.</span><span class="sxs-lookup"><span data-stu-id="3e505-282">The reason for reauthorizing a previously authorized connection.</span></span><br/> <span data-ttu-id="3e505-283">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-283">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                         |
| <span id="FWPM_CONDITION_ALE_REAUTH_REASON"></span><span id="fwpm_condition_ale_reauth_reason"></span><dl> <span data-ttu-id="3e505-284"><dt>**\_motivo da \_ \_ reautenticação Ale da condição FWPM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3e505-284"><dt>**FWPM\_CONDITION\_ALE\_REAUTH\_REASON**</dt></span></span> </dl>                                                | <span data-ttu-id="3e505-285">O motivo para reautorizar uma conexão anteriormente autorizada, como **fwp \_ condição de \_ reautorizar a \_ alteração da \_ política \_ de motivo** (ou um dos outros valores listados em sinalizadores de condição de [**filtragem**](filtering-condition-flags-.md)).</span><span class="sxs-lookup"><span data-stu-id="3e505-285">The reason for reauthorizing a previously authorized connection, such as **FWP\_CONDITION\_REAUTHORIZE\_REASON\_POLICY\_CHANGE** (or one of the other values listed in [**Filtering Condition Flags**](filtering-condition-flags-.md)).</span></span><br/> <span data-ttu-id="3e505-286">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-286">**Data type:** FWP\_UINT32</span></span><br/> |
| <span id="FWPM_CONDITION_ORIGINAL_ICMP_TYPE"></span><span id="fwpm_condition_original_icmp_type"></span><dl> <span data-ttu-id="3e505-287"><dt>**\_tipo de \_ \_ ICMP original da condição \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="3e505-287"><dt>**FWPM\_CONDITION\_ORIGINAL\_ICMP\_TYPE**</dt></span></span> </dl>                                             | <span data-ttu-id="3e505-288">O tipo de ICMP com o qual o fluxo foi criado.</span><span class="sxs-lookup"><span data-stu-id="3e505-288">The ICMP type with which the flow was created.</span></span><br/> <span data-ttu-id="3e505-289">**Tipo de dados:** FWP \_ UINT16</span><span class="sxs-lookup"><span data-stu-id="3e505-289">**Data type:** FWP\_UINT16</span></span><br/>                                                                                                                                                                                           |
| <span id="FWPM_CONDITION_IP_PHYSICAL_ARRIVAL_INTERFACE"></span><span id="fwpm_condition_ip_physical_arrival_interface"></span><dl> <span data-ttu-id="3e505-290"><dt>**\_interface de \_ \_ chegada física \_ de IP de condição FWPM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3e505-290"><dt>**FWPM\_CONDITION\_IP\_PHYSICAL\_ARRIVAL\_INTERFACE**</dt></span></span> </dl>           | <span data-ttu-id="3e505-291">O LUID da interface física associada ao endereço IP de chegada.</span><span class="sxs-lookup"><span data-stu-id="3e505-291">The LUID of the physical interface associated with the arrival IP address.</span></span><br/> <span data-ttu-id="3e505-292">**Tipo de dados:** FWP \_ UINT64</span><span class="sxs-lookup"><span data-stu-id="3e505-292">**Data type:** FWP\_UINT64</span></span><br/>                                                                                                                                                               |
| <span id="FWPM_CONDITION_IP_PHYSICAL_NEXTHOP_INTERFACE"></span><span id="fwpm_condition_ip_physical_nexthop_interface"></span><dl> <span data-ttu-id="3e505-293"><dt>**\_interface de \_ \_ salto físico \_ de IP de condição FWPM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3e505-293"><dt>**FWPM\_CONDITION\_IP\_PHYSICAL\_NEXTHOP\_INTERFACE**</dt></span></span> </dl>           | <span data-ttu-id="3e505-294">O LUID da interface física do próximo salto.</span><span class="sxs-lookup"><span data-stu-id="3e505-294">The LUID of the physical interface of the next hop.</span></span><br/> <span data-ttu-id="3e505-295">**Tipo de dados:** FWP \_ UINT64</span><span class="sxs-lookup"><span data-stu-id="3e505-295">**Data type:** FWP\_UINT64</span></span><br/>                                                                                                                                                                                      |
| <span id="FWPM_CONDITION_INTERFACE_QUARANTINE_EPOCH"></span><span id="fwpm_condition_interface_quarantine_epoch"></span><dl> <span data-ttu-id="3e505-296"><dt>**\_época de \_ quarentena da interface de condição FWPM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3e505-296"><dt>**FWPM\_CONDITION\_INTERFACE\_QUARANTINE\_EPOCH**</dt></span></span> </dl>                     | <span data-ttu-id="3e505-297">A contagem de época associada a uma interface.</span><span class="sxs-lookup"><span data-stu-id="3e505-297">The epoch count associated with an interface.</span></span> <span data-ttu-id="3e505-298">Reservado.</span><span class="sxs-lookup"><span data-stu-id="3e505-298">Reserved.</span></span><br/> <span data-ttu-id="3e505-299">**Tipo de dados:** FWP \_ UINT64</span><span class="sxs-lookup"><span data-stu-id="3e505-299">**Data type:** FWP\_UINT64</span></span><br/>                                                                                                                                                                                  |
| <span id="FWPM_CONDITION_ALE_SIO_FIREWALL_SOCKET_PROPERTY"></span><span id="fwpm_condition_ale_sio_firewall_socket_property"></span><dl> <span data-ttu-id="3e505-300"><dt>**\_propriedade de \_ \_ soquete do \_ Firewall \_ sio da FWPM condição Ale \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3e505-300"><dt>**FWPM\_CONDITION\_ALE\_SIO\_FIREWALL\_SOCKET\_PROPERTY**</dt></span></span> </dl> | <span data-ttu-id="3e505-301">Reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="3e505-301">Reserved for internal use.</span></span> <br/> <span data-ttu-id="3e505-302">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-302">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                                              |





| <span data-ttu-id="3e505-303">Constantes disponíveis para o Windows Vista com SP1, Windows Server 2008 e posterior</span><span class="sxs-lookup"><span data-stu-id="3e505-303">Constants available for Windows Vista with SP1, Windows Server 2008, and later</span></span>                                                                                                                                                                           | <span data-ttu-id="3e505-304">Description</span><span class="sxs-lookup"><span data-stu-id="3e505-304">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_CONDITION_IP_ARRIVAL_INTERFACE"></span><span id="fwpm_condition_ip_arrival_interface"></span><dl> <span data-ttu-id="3e505-305"><dt>**\_interface de \_ chegada de IP da condição FWPM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3e505-305"><dt>**FWPM\_CONDITION\_IP\_ARRIVAL\_INTERFACE**</dt></span></span> </dl>                       | <span data-ttu-id="3e505-306">O LUID para a interface de rede associada ao endereço IP de chegada.</span><span class="sxs-lookup"><span data-stu-id="3e505-306">The LUID for the network interface associated with the arrival IP address.</span></span> <br/> <span data-ttu-id="3e505-307">**Tipo de dados:** FWP \_ UINT64</span><span class="sxs-lookup"><span data-stu-id="3e505-307">**Data type:** FWP\_UINT64</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE"></span><span id="fwpm_condition_arrival_interface_type"></span><dl> <span data-ttu-id="3e505-308"><dt>**\_tipo de \_ interface de chegada da condição FWPM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3e505-308"><dt>**FWPM\_CONDITION\_ARRIVAL\_INTERFACE\_TYPE**</dt></span></span> </dl>                 | <span data-ttu-id="3e505-309">O tipo de interface de rede de chegada, conforme definido pela IANA (Internet Assigned Names Authority).</span><span class="sxs-lookup"><span data-stu-id="3e505-309">The type of the arrival network interface as defined by the Internet Assigned Names Authority (IANA).</span></span> <span data-ttu-id="3e505-310">Para obter mais informações, confira [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="3e505-310">For more information, see [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <br/> <span data-ttu-id="3e505-311">**Valores possíveis:** Os valores do tipo de interface listados no arquivo de cabeçalho Ipifcons. h.</span><span class="sxs-lookup"><span data-stu-id="3e505-311">**Possible values:** The interface type values listed in the Ipifcons.h header file.</span></span><br/> <span data-ttu-id="3e505-312">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-312">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                   |
| <span id="_FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE"></span><span id="_fwpm_condition_arrival_tunnel_type"></span><dl> <span data-ttu-id="3e505-313"><dt>**FWPM \_ \_tipo de \_ túnel \_ de chegada de condição**</dt></span><span class="sxs-lookup"><span data-stu-id="3e505-313"><dt> **FWPM\_CONDITION\_ARRIVAL\_TUNNEL\_TYPE**</dt></span></span> </dl>                       | <span data-ttu-id="3e505-314">O método de encapsulamento usado por um túnel associado à interface de rede de chegada se o membro do tipo for o \_ tipo \_ Tunnel.</span><span class="sxs-lookup"><span data-stu-id="3e505-314">The encapsulation method used by a tunnel associated with the arrival network interface if the Type member is IF\_TYPE\_TUNNEL.</span></span> <span data-ttu-id="3e505-315">O tipo de túnel é definido pela IANA (Internet Assigned Names Authority).</span><span class="sxs-lookup"><span data-stu-id="3e505-315">The tunnel type is defined by the Internet Assigned Names Authority (IANA).</span></span> <span data-ttu-id="3e505-316">Para obter mais informações, confira [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="3e505-316">For more information, see [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <br/> <span data-ttu-id="3e505-317">**Valores possíveis:** Os valores de tipo de enumeração de tipo de túnel \_ listados no arquivo de cabeçalho ifdef. h.</span><span class="sxs-lookup"><span data-stu-id="3e505-317">**Possible values:** The TUNNEL\_TYPE enumeration type values listed in the Ifdef.h header file.</span></span><br/> <span data-ttu-id="3e505-318">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-318">**Data type:** FWP\_UINT32</span></span><br/> |
| <span id="FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX"></span><span id="fwpm_condition_arrival_interface_index"></span><dl> <span data-ttu-id="3e505-319"><dt>**\_índice da \_ interface de chegada da condição FWPM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3e505-319"><dt>**FWPM\_CONDITION\_ARRIVAL\_INTERFACE\_INDEX**</dt></span></span> </dl>              | <span data-ttu-id="3e505-320">O índice da interface de rede de chegada, conforme enumerado pela pilha de rede.</span><span class="sxs-lookup"><span data-stu-id="3e505-320">The index of the arrival network interface, as enumerated by the network stack.</span></span><br/> <span data-ttu-id="3e505-321">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-321">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_arrival_sub_interface_index"></span><dl> <span data-ttu-id="3e505-322"><dt>**\_índice da \_ \_ \_ subinterface de chegada da condição \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="3e505-322"><dt>**FWPM\_CONDITION\_ARRIVAL\_SUB\_INTERFACE\_INDEX**</dt></span></span> </dl> | <span data-ttu-id="3e505-323">O índice da interface de rede de chegada, conforme enumerado pela pilha de rede.</span><span class="sxs-lookup"><span data-stu-id="3e505-323">The index of the arrival network interface, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="3e505-324">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-324">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="FWPM_CONDITION_LOCAL_INTERFACE_INDEX"></span><span id="fwpm_condition_local_interface_index"></span><dl> <span data-ttu-id="3e505-325"><dt>**\_índice de \_ \_ interface local de condição \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="3e505-325"><dt>**FWPM\_CONDITION\_LOCAL\_INTERFACE\_INDEX**</dt></span></span> </dl>                    | <span data-ttu-id="3e505-326">O índice da interface de rede, conforme enumerado pela pilha de rede.</span><span class="sxs-lookup"><span data-stu-id="3e505-326">The index of the network interface, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="3e505-327">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-327">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="FWPM_CONDITION_LOCAL_INTERFACE_TYPE"></span><span id="fwpm_condition_local_interface_type"></span><dl> <span data-ttu-id="3e505-328"><dt>**\_tipo de \_ \_ interface local da condição \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="3e505-328"><dt>**FWPM\_CONDITION\_LOCAL\_INTERFACE\_TYPE**</dt></span></span> </dl>                       | <span data-ttu-id="3e505-329">O tipo de interface, conforme definido pela Internet Assigned Names Authority (IANA).</span><span class="sxs-lookup"><span data-stu-id="3e505-329">The interface type as defined by the Internet Assigned Names Authority (IANA).</span></span> <span data-ttu-id="3e505-330">Para obter mais informações, confira [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="3e505-330">For more information, see [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <br/> <span data-ttu-id="3e505-331">**Valores possíveis:** Os valores do tipo de interface listados no arquivo de cabeçalho Ipifcons. h.</span><span class="sxs-lookup"><span data-stu-id="3e505-331">**Possible values:** The interface type values listed in the Ipifcons.h header file.</span></span><br/> <span data-ttu-id="3e505-332">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-332">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                          |
| <span id="FWPM_CONDITION_LOCAL_TUNNEL_TYPE"></span><span id="fwpm_condition_local_tunnel_type"></span><dl> <span data-ttu-id="3e505-333"><dt>**\_tipo de \_ \_ túnel local da condição \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="3e505-333"><dt>**FWPM\_CONDITION\_LOCAL\_TUNNEL\_TYPE**</dt></span></span> </dl>                                | <span data-ttu-id="3e505-334">O método de encapsulamento usado por um túnel se o membro do tipo for o \_ tipo \_ Tunnel.</span><span class="sxs-lookup"><span data-stu-id="3e505-334">The encapsulation method used by a tunnel if the Type member is IF\_TYPE\_TUNNEL.</span></span> <span data-ttu-id="3e505-335">O tipo de túnel é definido pela IANA (Internet Assigned Names Authority).</span><span class="sxs-lookup"><span data-stu-id="3e505-335">The tunnel type is defined by the Internet Assigned Names Authority (IANA).</span></span> <span data-ttu-id="3e505-336">Para obter mais informações, confira [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="3e505-336">For more information, see [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <br/> <span data-ttu-id="3e505-337">**Valores possíveis:** Os valores de tipo de enumeração de tipo de túnel \_ listados no arquivo de cabeçalho ifdef. h.</span><span class="sxs-lookup"><span data-stu-id="3e505-337">**Possible values:** The TUNNEL\_TYPE enumeration type values listed in the Ifdef.h header file.</span></span><br/> <span data-ttu-id="3e505-338">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-338">**Data type:** FWP\_UINT32</span></span> <br/>                                              |





<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="3e505-339">Constantes disponíveis para o Windows Vista e posterior</span><span class="sxs-lookup"><span data-stu-id="3e505-339">Constants available for Windows Vista and later</span></span></th>
<th style="text-align: left;"><span data-ttu-id="3e505-340">Description</span><span class="sxs-lookup"><span data-stu-id="3e505-340">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS"></span><span id="fwpm_condition_ip_local_address"></span><dl> <span data-ttu-id="3e505-341"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-341"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-342">O endereço IP local.</span><span class="sxs-lookup"><span data-stu-id="3e505-342">The local IP address.</span></span> <br/> <span data-ttu-id="3e505-343"><strong>Tipo de dados:</strong> Para um endereço IPv4</span><span class="sxs-lookup"><span data-stu-id="3e505-343"><strong>Data type:</strong> For an IPv4 address</span></span>
<ul>
<li><span data-ttu-id="3e505-344">FWP_V4_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="3e505-344">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="3e505-345">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-345">FWP_UINT32</span></span></li>
</ul>
<br/> <span data-ttu-id="3e505-346"><strong>Tipo de dados:</strong> Para um endereço IPv6</span><span class="sxs-lookup"><span data-stu-id="3e505-346"><strong>Data type:</strong> For an IPv6 address</span></span>
<ul>
<li><span data-ttu-id="3e505-347">FWP_V6_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="3e505-347">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="3e505-348">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-348">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_ADDRESS"></span><span id="fwpm_condition_ip_remote_address"></span><dl> <span data-ttu-id="3e505-349"><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-349"><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-350">O endereço IP remoto.</span><span class="sxs-lookup"><span data-stu-id="3e505-350">The remote IP address.</span></span> <br/> <span data-ttu-id="3e505-351"><strong>Tipo de dados:</strong> Para um endereço IPv4</span><span class="sxs-lookup"><span data-stu-id="3e505-351"><strong>Data type:</strong> For an IPv4 address</span></span>
<ul>
<li><span data-ttu-id="3e505-352">FWP_V4_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="3e505-352">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="3e505-353">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-353">FWP_UINT32</span></span></li>
</ul>
<br/> <span data-ttu-id="3e505-354"><strong>Tipo de dados:</strong> Para um endereço IPv6</span><span class="sxs-lookup"><span data-stu-id="3e505-354"><strong>Data type:</strong> For an IPv6 address</span></span>
<ul>
<li><span data-ttu-id="3e505-355">FWP_V6_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="3e505-355">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="3e505-356">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-356">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_SOURCE_ADDRESS"></span><span id="fwpm_condition_ip_source_address"></span><dl> <span data-ttu-id="3e505-357"><dt><strong>FWPM_CONDITION_IP_SOURCE_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-357"><dt><strong>FWPM_CONDITION_IP_SOURCE_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-358">O endereço IP de origem para pacotes encaminhados.</span><span class="sxs-lookup"><span data-stu-id="3e505-358">The source IP address for forwarded packets.</span></span> <br/> <span data-ttu-id="3e505-359"><strong>Tipo de dados:</strong> Para um endereço IPv4</span><span class="sxs-lookup"><span data-stu-id="3e505-359"><strong>Data type:</strong> For an IPv4 address</span></span>
<ul>
<li><span data-ttu-id="3e505-360">FWP_V4_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="3e505-360">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="3e505-361">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-361">FWP_UINT32</span></span></li>
</ul>
<br/> <span data-ttu-id="3e505-362"><strong>Tipo de dados:</strong> Para um endereço IPv6</span><span class="sxs-lookup"><span data-stu-id="3e505-362"><strong>Data type:</strong> For an IPv6 address</span></span>
<ul>
<li><span data-ttu-id="3e505-363">FWP_V6_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="3e505-363">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="3e505-364">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-364">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_DESTINATION_ADDRESS"></span><span id="fwpm_condition_ip_destination_address"></span><dl> <span data-ttu-id="3e505-365"><dt><strong>FWPM_CONDITION_IP_DESTINATION_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-365"><dt><strong>FWPM_CONDITION_IP_DESTINATION_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-366">O endereço IP de destino para pacotes encaminhados.</span><span class="sxs-lookup"><span data-stu-id="3e505-366">The destination IP address for forwarded packets.</span></span> <br/> <span data-ttu-id="3e505-367"><strong>Tipo de dados:</strong> Para um endereço IPv4</span><span class="sxs-lookup"><span data-stu-id="3e505-367"><strong>Data type:</strong> For an IPv4 address</span></span>
<ul>
<li><span data-ttu-id="3e505-368">FWP_V4_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="3e505-368">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="3e505-369">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-369">FWP_UINT32</span></span></li>
</ul>
<br/> <span data-ttu-id="3e505-370"><strong>Tipo de dados:</strong> Para um endereço IPv6</span><span class="sxs-lookup"><span data-stu-id="3e505-370"><strong>Data type:</strong> For an IPv6 address</span></span>
<ul>
<li><span data-ttu-id="3e505-371">FWP_V6_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="3e505-371">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="3e505-372">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-372">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE"></span><span id="fwpm_condition_ip_local_address_type"></span><dl> <span data-ttu-id="3e505-373"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-373"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-374">O tipo de endereço IP local.</span><span class="sxs-lookup"><span data-stu-id="3e505-374">The local IP address type.</span></span> <br/> <span data-ttu-id="3e505-375"><strong>Valores possíveis:</strong> Qualquer um dos seguintes <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> valores de enumeração.</span><span class="sxs-lookup"><span data-stu-id="3e505-375"><strong>Possible values:</strong> Any of the following <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="3e505-376">NlatUnspecified</span><span class="sxs-lookup"><span data-stu-id="3e505-376">NlatUnspecified</span></span></li>
<li><span data-ttu-id="3e505-377">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="3e505-377">NlatUnicast</span></span></li>
<li><span data-ttu-id="3e505-378">NlatAnycast</span><span class="sxs-lookup"><span data-stu-id="3e505-378">NlatAnycast</span></span></li>
<li><span data-ttu-id="3e505-379">NlatMulticast</span><span class="sxs-lookup"><span data-stu-id="3e505-379">NlatMulticast</span></span></li>
<li><span data-ttu-id="3e505-380">NlatBroadcast</span><span class="sxs-lookup"><span data-stu-id="3e505-380">NlatBroadcast</span></span></li>
</ul>
<br/> <span data-ttu-id="3e505-381"><strong>Tipo de dados:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="3e505-381"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE"></span><span id="fwpm_condition_ip_destination_address_type"></span><dl> <span data-ttu-id="3e505-382"><dt><strong>FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-382"><dt><strong>FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-383">O tipo de endereço IP de destino para pacotes encaminhados.</span><span class="sxs-lookup"><span data-stu-id="3e505-383">The destination IP address type for forwarded packets.</span></span> <br/> <span data-ttu-id="3e505-384"><strong>Valores possíveis:</strong> Qualquer um dos seguintes <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> valores de enumeração.</span><span class="sxs-lookup"><span data-stu-id="3e505-384"><strong>Possible values:</strong> Any of the following <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="3e505-385">NlatUnspecified</span><span class="sxs-lookup"><span data-stu-id="3e505-385">NlatUnspecified</span></span></li>
<li><span data-ttu-id="3e505-386">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="3e505-386">NlatUnicast</span></span></li>
<li><span data-ttu-id="3e505-387">NlatAnycast</span><span class="sxs-lookup"><span data-stu-id="3e505-387">NlatAnycast</span></span></li>
<li><span data-ttu-id="3e505-388">NlatMulticast</span><span class="sxs-lookup"><span data-stu-id="3e505-388">NlatMulticast</span></span></li>
<li><span data-ttu-id="3e505-389">NlatBroadcast</span><span class="sxs-lookup"><span data-stu-id="3e505-389">NlatBroadcast</span></span></li>
</ul>
<br/> <span data-ttu-id="3e505-390"><strong>Tipo de dados:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="3e505-390"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_INTERFACE"></span><span id="fwpm_condition_ip_local_interface"></span><dl> <span data-ttu-id="3e505-391"><dt><strong>FWPM_CONDITION_IP_LOCAL_INTERFACE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-391"><dt><strong>FWPM_CONDITION_IP_LOCAL_INTERFACE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-392">O LUID para a interface de rede associada ao endereço IP local.</span><span class="sxs-lookup"><span data-stu-id="3e505-392">The LUID for the network interface associated with the local IP address.</span></span> <br/> <span data-ttu-id="3e505-393"><strong>Tipo de dados:</strong> FWP_UINT64</span><span class="sxs-lookup"><span data-stu-id="3e505-393"><strong>Data type:</strong> FWP_UINT64</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE_TYPE"></span><span id="fwpm_condition_interface_type"></span><dl> <span data-ttu-id="3e505-394"><dt><strong>FWPM_CONDITION_INTERFACE_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-394"><dt><strong>FWPM_CONDITION_INTERFACE_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-395">O tipo de interface, conforme definido pela Internet Assigned Names Authority (IANA).</span><span class="sxs-lookup"><span data-stu-id="3e505-395">The interface type as defined by the Internet Assigned Names Authority (IANA).</span></span> <span data-ttu-id="3e505-396">Para obter mais informações, confira [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="3e505-396">For more information, see [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <br/> <span data-ttu-id="3e505-397"><strong>Valores possíveis:</strong> Os valores do tipo de interface listados no arquivo de cabeçalho Ipifcons. h.</span><span class="sxs-lookup"><span data-stu-id="3e505-397"><strong>Possible values:</strong> The interface type values listed in the Ipifcons.h header file.</span></span><br/> <span data-ttu-id="3e505-398"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-398"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_TUNNEL_TYPE"></span><span id="fwpm_condition_tunnel_type"></span><dl> <span data-ttu-id="3e505-399"><dt><strong>FWPM_CONDITION_TUNNEL_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-399"><dt><strong>FWPM_CONDITION_TUNNEL_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-400">O método de encapsulamento usado por um túnel se o membro do tipo for IF_TYPE_TUNNEL.</span><span class="sxs-lookup"><span data-stu-id="3e505-400">The encapsulation method used by a tunnel if the Type member is IF_TYPE_TUNNEL.</span></span> <span data-ttu-id="3e505-401">O tipo de túnel é definido pela IANA (Internet Assigned Names Authority).</span><span class="sxs-lookup"><span data-stu-id="3e505-401">The tunnel type is defined by the Internet Assigned Names Authority (IANA).</span></span> <span data-ttu-id="3e505-402">Para obter mais informações, confira <a href="https://www.iana.org/assignments/ianaiftype-mib">https://www.iana.org/assignments/ianaiftype-mib</a>.</span><span class="sxs-lookup"><span data-stu-id="3e505-402">For more information, see <a href="https://www.iana.org/assignments/ianaiftype-mib">https://www.iana.org/assignments/ianaiftype-mib</a>.</span></span> <br/> <span data-ttu-id="3e505-403"><strong>Valores possíveis:</strong> Os valores de tipo de enumeração TUNNEL_TYPE listados no arquivo de cabeçalho ifdef. h.</span><span class="sxs-lookup"><span data-stu-id="3e505-403"><strong>Possible values:</strong> The TUNNEL_TYPE enumeration type values listed in the Ifdef.h header file.</span></span><br/> <span data-ttu-id="3e505-404"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-404"><strong>Data type:</strong> FWP_UINT32</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_FORWARD_INTERFACE"></span><span id="fwpm_condition_ip_forward_interface"></span><dl> <span data-ttu-id="3e505-405"><dt><strong>FWPM_CONDITION_IP_FORWARD_INTERFACE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-405"><dt><strong>FWPM_CONDITION_IP_FORWARD_INTERFACE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-406">A LUID para a interface de rede na qual o pacote que está sendo encaminhado deve ser enviada.</span><span class="sxs-lookup"><span data-stu-id="3e505-406">The LUID for the network interface on which the packet being forwarded is to be sent out.</span></span> <br/> <span data-ttu-id="3e505-407"><strong>Tipo de dados:</strong> FWP_UINT64</span><span class="sxs-lookup"><span data-stu-id="3e505-407"><strong>Data type:</strong> FWP_UINT64</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_PROTOCOL"></span><span id="fwpm_condition_ip_protocol"></span><dl> <span data-ttu-id="3e505-408"><dt><strong>FWPM_CONDITION_IP_PROTOCOL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-408"><dt><strong>FWPM_CONDITION_IP_PROTOCOL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-409">O número do protocolo IP, conforme especificado no RFC 1700.</span><span class="sxs-lookup"><span data-stu-id="3e505-409">The IP protocol number, as specified in RFC 1700.</span></span> <br/> <span data-ttu-id="3e505-410"><strong>Tipo de dados:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="3e505-410"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_PORT"></span><span id="fwpm_condition_ip_local_port"></span><dl> <span data-ttu-id="3e505-411"><dt><strong>FWPM_CONDITION_IP_LOCAL_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-411"><dt><strong>FWPM_CONDITION_IP_LOCAL_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-412">O número da porta do protocolo de transporte local.</span><span class="sxs-lookup"><span data-stu-id="3e505-412">The local transport protocol port number.</span></span><br/> <span data-ttu-id="3e505-413"><strong>Tipo de dados:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="3e505-413"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ICMP_TYPE"></span><span id="fwpm_condition_icmp_type"></span><dl> <span data-ttu-id="3e505-414"><dt><strong>FWPM_CONDITION_ICMP_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-414"><dt><strong>FWPM_CONDITION_ICMP_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-415">O campo tipo de ICMP, conforme especificado no RFC 792.</span><span class="sxs-lookup"><span data-stu-id="3e505-415">The ICMP type field, as specified in RFC 792.</span></span> <br/> <span data-ttu-id="3e505-416"><strong>Tipo de dados:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="3e505-416"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_PORT"></span><span id="fwpm_condition_ip_remote_port"></span><dl> <span data-ttu-id="3e505-417"><dt><strong>FWPM_CONDITION_IP_REMOTE_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-417"><dt><strong>FWPM_CONDITION_IP_REMOTE_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-418">O número da porta do protocolo de transporte remoto.</span><span class="sxs-lookup"><span data-stu-id="3e505-418">The remote transport protocol port number.</span></span> <br/> <span data-ttu-id="3e505-419"><strong>Tipo de dados:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="3e505-419"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ICMP_CODE"></span><span id="fwpm_condition_icmp_code"></span><dl> <span data-ttu-id="3e505-420"><dt><strong>FWPM_CONDITION_ICMP_CODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-420"><dt><strong>FWPM_CONDITION_ICMP_CODE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-421">O campo de código ICMP, conforme especificado no RFC 792.</span><span class="sxs-lookup"><span data-stu-id="3e505-421">The ICMP code field, as specified in RFC 792.</span></span> <br/> <span data-ttu-id="3e505-422"><strong>Tipo de dados:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="3e505-422"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE"></span><span id="fwpm_condition_embedded_local_address_type"></span><dl> <span data-ttu-id="3e505-423"><dt><strong>FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-423"><dt><strong>FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-424">O tipo de endereço IP local que é inserido no pacote ICMP.</span><span class="sxs-lookup"><span data-stu-id="3e505-424">The local IP address type that is embedded in the ICMP packet.</span></span><br/> <span data-ttu-id="3e505-425"><strong>Valores possíveis:</strong> Qualquer um dos seguintes <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> valores de enumeração.</span><span class="sxs-lookup"><span data-stu-id="3e505-425"><strong>Possible values:</strong> Any of the following <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="3e505-426">NlatUnspecified</span><span class="sxs-lookup"><span data-stu-id="3e505-426">NlatUnspecified</span></span></li>
<li><span data-ttu-id="3e505-427">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="3e505-427">NlatUnicast</span></span></li>
<li><span data-ttu-id="3e505-428">NlatAnycast</span><span class="sxs-lookup"><span data-stu-id="3e505-428">NlatAnycast</span></span></li>
<li><span data-ttu-id="3e505-429">NlatMulticast</span><span class="sxs-lookup"><span data-stu-id="3e505-429">NlatMulticast</span></span></li>
<li><span data-ttu-id="3e505-430">NlatBroadcast</span><span class="sxs-lookup"><span data-stu-id="3e505-430">NlatBroadcast</span></span></li>
</ul>
<br/> <span data-ttu-id="3e505-431"><strong>Tipo de dados:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="3e505-431"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS"></span><span id="fwpm_condition_embedded_remote_address"></span><dl> <span data-ttu-id="3e505-432"><dt><strong>FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-432"><dt><strong>FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-433">O endereço IP remoto que é inserido no pacote ICMP.</span><span class="sxs-lookup"><span data-stu-id="3e505-433">The remote IP address that is embedded in the ICMP packet.</span></span> <br/> <span data-ttu-id="3e505-434"><strong>Tipo de dados:</strong> Para um endereço IPv4</span><span class="sxs-lookup"><span data-stu-id="3e505-434"><strong>Data type:</strong> For an IPv4 address</span></span>
<ul>
<li><span data-ttu-id="3e505-435">FWP_V4_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="3e505-435">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="3e505-436">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-436">FWP_UINT32</span></span></li>
</ul>
<br/> <span data-ttu-id="3e505-437"><strong>Tipo de dados:</strong> Para um endereço IPv6</span><span class="sxs-lookup"><span data-stu-id="3e505-437"><strong>Data type:</strong> For an IPv6 address</span></span>
<ul>
<li><span data-ttu-id="3e505-438">FWP_V6_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="3e505-438">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="3e505-439">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-439">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_PROTOCOL"></span><span id="fwpm_condition_embedded_protocol"></span><dl> <span data-ttu-id="3e505-440"><dt><strong>FWPM_CONDITION_EMBEDDED_PROTOCOL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-440"><dt><strong>FWPM_CONDITION_EMBEDDED_PROTOCOL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-441">O número do protocolo IP inserido no pacote ICMP, conforme especificado no RFC 1700.</span><span class="sxs-lookup"><span data-stu-id="3e505-441">The IP protocol number that is embedded in the ICMP packet, as specified in RFC 1700.</span></span> <br/> <span data-ttu-id="3e505-442"><strong>Tipo de dados:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="3e505-442"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_LOCAL_PORT"></span><span id="fwpm_condition_embedded_local_port"></span><dl> <span data-ttu-id="3e505-443"><dt><strong>FWPM_CONDITION_EMBEDDED_LOCAL_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-443"><dt><strong>FWPM_CONDITION_EMBEDDED_LOCAL_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-444">O número da porta do protocolo de transporte local que é inserido no pacote ICMP.</span><span class="sxs-lookup"><span data-stu-id="3e505-444">The local transport protocol port number that is embedded in the ICMP packet.</span></span> <br/> <span data-ttu-id="3e505-445"><strong>Tipo de dados:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="3e505-445"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_REMOTE_PORT"></span><span id="fwpm_condition_embedded_remote_port"></span><dl> <span data-ttu-id="3e505-446"><dt><strong>FWPM_CONDITION_EMBEDDED_REMOTE_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-446"><dt><strong>FWPM_CONDITION_EMBEDDED_REMOTE_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-447">O número da porta do protocolo de transporte remoto que é inserido no pacote ICMP.</span><span class="sxs-lookup"><span data-stu-id="3e505-447">The remote transport protocol port number that is embedded in the ICMP packet.</span></span> <br/> <span data-ttu-id="3e505-448"><strong>Tipo de dados:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="3e505-448"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_FLAGS"></span><span id="fwpm_condition_flags"></span><dl> <span data-ttu-id="3e505-449"><dt><strong>FWPM_CONDITION_FLAGS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-449"><dt><strong>FWPM_CONDITION_FLAGS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-450">Uma operação OR de uma combinação de sinalizadores de condição de filtragem.</span><span class="sxs-lookup"><span data-stu-id="3e505-450">A bitwise OR of a combination of filtering condition flags.</span></span> <br/> <span data-ttu-id="3e505-451"><strong>Valores possíveis:</strong> Consulte <a href="filtering-condition-flags-.md"> <strong>filtrando sinalizadores de condição</strong></a></span><span class="sxs-lookup"><span data-stu-id="3e505-451"><strong>Possible values:</strong> See <a href="filtering-condition-flags-.md"><strong>Filtering Condition Flags</strong></a></span></span><br/> <span data-ttu-id="3e505-452"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-452"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_DIRECTION"></span><span id="fwpm_condition_direction"></span><dl> <span data-ttu-id="3e505-453"><dt><strong>FWPM_CONDITION_DIRECTION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-453"><dt><strong>FWPM_CONDITION_DIRECTION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-454">A direção do fluxo de tráfego ou de dados.</span><span class="sxs-lookup"><span data-stu-id="3e505-454">The direction of the traffic or data flow.</span></span> <br/> <span data-ttu-id="3e505-455"><strong>Valores possíveis:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="3e505-455"><strong>Possible values:  </strong>
</span></span><ul>
<li><span data-ttu-id="3e505-456">FWP_DIRECTION_INBOUND</span><span class="sxs-lookup"><span data-stu-id="3e505-456">FWP_DIRECTION_INBOUND</span></span></li>
<li><span data-ttu-id="3e505-457">FWP_DIRECTION_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="3e505-457">FWP_DIRECTION_OUTBOUND</span></span></li>
</ul>
<br/> <span data-ttu-id="3e505-458">Para camadas de datagrama (FWPM_LAYER_DATAGRAM_DATA_ *) e camadas de pacotes de fluxo (FWPM_LAYER_STREAM_PACKET_*), o valor será o mesmo que a direção do pacote.</span><span class="sxs-lookup"><span data-stu-id="3e505-458">For datagram layers (FWPM_LAYER_DATAGRAM_DATA_ *) and stream packet layers (FWPM_LAYER_STREAM_PACKET_*), the value will be the same as the direction of the packet.</span></span> <br/> <span data-ttu-id="3e505-459">Para camadas de fluxo (FWPM_LAYER_STREAM_ *) e camadas estabelecidas pelo Flow (FWPM_LAYER_ALE_FLOW_ESTABLISHED_*), o valor será o mesmo que a direção da conexão.</span><span class="sxs-lookup"><span data-stu-id="3e505-459">For stream layers (FWPM_LAYER_STREAM_ *) and flow established layers (FWPM_LAYER_ALE_FLOW_ESTABLISHED_*), the value will be the same as direction of the connection.</span></span> <span data-ttu-id="3e505-460">(Por exemplo, quando um aplicativo local inicia a conexão, um pacote de entrada tem <strong>FWPM_CONDITION_DIRECTION</strong> definido como <strong>FWP_DIRECTION_OUTBOUND</strong>.)</span><span class="sxs-lookup"><span data-stu-id="3e505-460">(For example, when a local application initiates the connection, an inbound packet has <strong>FWPM_CONDITION_DIRECTION</strong> set to <strong>FWP_DIRECTION_OUTBOUND</strong>.)</span></span> <br/> <span data-ttu-id="3e505-461"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-461"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE_INDEX"></span><span id="fwpm_condition_interface_index"></span><dl> <span data-ttu-id="3e505-462"><dt><strong>FWPM_CONDITION_INTERFACE_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-462"><dt><strong>FWPM_CONDITION_INTERFACE_INDEX</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-463">O índice da interface de rede, conforme enumerado pela pilha de rede.</span><span class="sxs-lookup"><span data-stu-id="3e505-463">The index of the network interface, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="3e505-464"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-464"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_sub_interface_index"></span><dl> <span data-ttu-id="3e505-465"><dt><strong>FWPM_CONDITION_SUB_INTERFACE_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-465"><dt><strong>FWPM_CONDITION_SUB_INTERFACE_INDEX</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-466">O índice da interface de rede lógica, conforme enumerado pela pilha de rede.</span><span class="sxs-lookup"><span data-stu-id="3e505-466">The index of the logical network interface, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="3e505-467"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-467"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_SOURCE_INTERFACE_INDEX"></span><span id="fwpm_condition_source_interface_index"></span><dl> <span data-ttu-id="3e505-468"><dt><strong>FWPM_CONDITION_SOURCE_INTERFACE_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-468"><dt><strong>FWPM_CONDITION_SOURCE_INTERFACE_INDEX</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-469">O índice da interface de rede de origem para pacotes encaminhados, conforme enumerado pela pilha de rede.</span><span class="sxs-lookup"><span data-stu-id="3e505-469">The index of the source network interface for forwarded packets, as enumerated by the network stack.</span></span><br/> <span data-ttu-id="3e505-470"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-470"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_source_sub_interface_index"></span><dl> <span data-ttu-id="3e505-471"><dt><strong>FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-471"><dt><strong>FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-472">O índice da interface de rede lógica de origem para pacotes encaminhados, conforme enumerado pela pilha de rede.</span><span class="sxs-lookup"><span data-stu-id="3e505-472">The index of the source logical network interface for forwarded packets, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="3e505-473"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-473"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_DESTINATION_INTERFACE_INDEX"></span><span id="fwpm_condition_destination_interface_index"></span><dl> <span data-ttu-id="3e505-474"><dt><strong>FWPM_CONDITION_DESTINATION_INTERFACE_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-474"><dt><strong>FWPM_CONDITION_DESTINATION_INTERFACE_INDEX</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-475">O índice da interface de rede de destino para pacotes encaminhados, conforme enumerado pela pilha de rede.</span><span class="sxs-lookup"><span data-stu-id="3e505-475">The index of the destination network interface for forwarded packets, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="3e505-476"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-476"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_destination_sub_interface_index"></span><dl> <span data-ttu-id="3e505-477"><dt><strong>FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-477"><dt><strong>FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-478">O índice da interface de rede lógica de destino para pacotes encaminhados, conforme enumerado pela pilha de rede.</span><span class="sxs-lookup"><span data-stu-id="3e505-478">The index of the destination logical network interface for forwarded packets, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="3e505-479"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-479"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_APP_ID"></span><span id="fwpm_condition_ale_app_id"></span><dl> <span data-ttu-id="3e505-480"><dt><strong>FWPM_CONDITION_ALE_APP_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-480"><dt><strong>FWPM_CONDITION_ALE_APP_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-481">O caminho do dispositivo totalmente qualificado do aplicativo, conforme retornado pela função <a href="/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmgetappidfromfilename0"><strong>FwpmGetAppIdFromFileName0</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3e505-481">The fully qualified device path of the application, as returned by the <a href="/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmgetappidfromfilename0"><strong>FwpmGetAppIdFromFileName0</strong></a> function.</span></span> <br/> <span data-ttu-id="3e505-482">(Por exemplo, &quot; \device0\hardiskvolume1\Program Files\Application.exe&quot; .)</span><span class="sxs-lookup"><span data-stu-id="3e505-482">(For example, &quot;\device0\hardiskvolume1\Program Files\Application.exe&quot;.)</span></span><br/> <span data-ttu-id="3e505-483"><strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-483"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_USER_ID"></span><span id="fwpm_condition_ale_user_id"></span><dl> <span data-ttu-id="3e505-484"><dt><strong>FWPM_CONDITION_ALE_USER_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-484"><dt><strong>FWPM_CONDITION_ALE_USER_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-485">A identificação do usuário local.</span><span class="sxs-lookup"><span data-stu-id="3e505-485">The identification of the local user.</span></span> <br/> <span data-ttu-id="3e505-486"><strong>Tipo de dados:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-486"><strong>Data type:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_REMOTE_USER_ID"></span><span id="fwpm_condition_ale_remote_user_id"></span><dl> <span data-ttu-id="3e505-487"><dt><strong>FWPM_CONDITION_ALE_REMOTE_USER_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-487"><dt><strong>FWPM_CONDITION_ALE_REMOTE_USER_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-488">A identificação do usuário remoto.</span><span class="sxs-lookup"><span data-stu-id="3e505-488">The identification of the remote user.</span></span> <br/> <span data-ttu-id="3e505-489"><strong>Tipo de dados:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-489"><strong>Data type:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_REMOTE_MACHINE_ID"></span><span id="fwpm_condition_ale_remote_machine_id"></span><dl> <span data-ttu-id="3e505-490"><dt><strong>FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-490"><dt><strong>FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-491">A identificação do computador remoto.</span><span class="sxs-lookup"><span data-stu-id="3e505-491">The identification of the remote machine.</span></span> <br/> <span data-ttu-id="3e505-492"><strong>Tipo de dados:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-492"><strong>Data type:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_PROMISCUOUS_MODE"></span><span id="fwpm_condition_ale_promiscuous_mode"></span><dl> <span data-ttu-id="3e505-493"><dt><strong>FWPM_CONDITION_ALE_PROMISCUOUS_MODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-493"><dt><strong>FWPM_CONDITION_ALE_PROMISCUOUS_MODE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-494">O modo de soquete bruto que é permitido ou negado.</span><span class="sxs-lookup"><span data-stu-id="3e505-494">The raw socket mode that is allowed or denied.</span></span><br/> <span data-ttu-id="3e505-495"><strong>Valores possíveis:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="3e505-495"><strong>Possible values:  </strong>
</span></span><ul>
<li><span data-ttu-id="3e505-496">SIO_RCVALL</span><span class="sxs-lookup"><span data-stu-id="3e505-496">SIO_RCVALL</span></span></li>
<li><span data-ttu-id="3e505-497">SIO_RCVALL_IGMPMCAST</span><span class="sxs-lookup"><span data-stu-id="3e505-497">SIO_RCVALL_IGMPMCAST</span></span></li>
<li><span data-ttu-id="3e505-498">SIO_RCVALL_MCAST</span><span class="sxs-lookup"><span data-stu-id="3e505-498">SIO_RCVALL_MCAST</span></span></li>
</ul>
<span data-ttu-id="3e505-499">Para obter uma descrição desses modos de soquete bruto, consulte a função <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl"><strong>WSAIoctl</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3e505-499">For a description of these raw socket modes, see the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl"><strong>WSAIoctl</strong></a> function.</span></span><br/> <span data-ttu-id="3e505-500"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-500"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT"></span><span id="fwpm_condition_ale_sio_firewall_system_port"></span><dl> <span data-ttu-id="3e505-501"><dt><strong>FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-501"><dt><strong>FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-502">Reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="3e505-502">Reserved for internal use.</span></span> <br/> <span data-ttu-id="3e505-503"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-503"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_NAP_CONTEXT"></span><span id="fwpm_condition_ale_nap_context"></span><dl> <span data-ttu-id="3e505-504"><dt><strong>FWPM_CONDITION_ALE_NAP_CONTEXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-504"><dt><strong>FWPM_CONDITION_ALE_NAP_CONTEXT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-505">Reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="3e505-505">Reserved for internal use.</span></span> <br/> <span data-ttu-id="3e505-506"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-506"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
</tbody>
</table>



<span data-ttu-id="3e505-507">As constantes a seguir estão disponíveis somente para o modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="3e505-507">The following constants are available for user mode only.</span></span>



| <span data-ttu-id="3e505-508">Condições de modo de usuário disponíveis para o Windows 8 e o Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3e505-508">User-mode conditions available for Windows 8 and Windows Server 2012</span></span>                                                                                                                       | <span data-ttu-id="3e505-509">Description</span><span class="sxs-lookup"><span data-stu-id="3e505-509">Description</span></span>                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_CONDITION_QM_MODE"></span><span id="fwpm_condition_qm_mode"></span><dl> <span data-ttu-id="3e505-510"><dt>**\_ \_ modo QM da condição FWPM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3e505-510"><dt>**FWPM\_CONDITION\_QM\_MODE**</dt></span></span> </dl> | <span data-ttu-id="3e505-511">O modo do filtro de modo rápido (QM).</span><span class="sxs-lookup"><span data-stu-id="3e505-511">The mode of the quick mode (QM) filter.</span></span> <span data-ttu-id="3e505-512">Consulte [**\_ \_ tipo de tráfego IPSec**](/windows/desktop/api/Ipsectypes/ne-ipsectypes-ipsec_traffic_type) para obter os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="3e505-512">See [**IPSEC\_TRAFFIC\_TYPE**](/windows/desktop/api/Ipsectypes/ne-ipsectypes-ipsec_traffic_type) for possible values.</span></span><br/> <span data-ttu-id="3e505-513">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-513">**Data type:** FWP\_UINT32</span></span><br/> |





<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="3e505-514">Condições de modo de usuário disponíveis para o Windows 7, o Windows Server 2008 R2 e posterior</span><span class="sxs-lookup"><span data-stu-id="3e505-514">User-mode conditions available for Windows 7, Windows Server 2008 R2, and later</span></span></th>
<th style="text-align: left;"><span data-ttu-id="3e505-515">Description</span><span class="sxs-lookup"><span data-stu-id="3e505-515">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_KM_AUTH_NAP_CONTEXT"></span><span id="fwpm_condition_km_auth_nap_context"></span><dl> <span data-ttu-id="3e505-516"><dt><strong>FWPM_CONDITION_KM_AUTH_NAP_CONTEXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-516"><dt><strong>FWPM_CONDITION_KM_AUTH_NAP_CONTEXT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-517">Reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="3e505-517">Reserved for internal use.</span></span><br/> <span data-ttu-id="3e505-518"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-518"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_PEER_NAME"></span><span id="fwpm_condition_peer_name"></span><dl> <span data-ttu-id="3e505-519"><dt><strong>FWPM_CONDITION_PEER_NAME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-519"><dt><strong>FWPM_CONDITION_PEER_NAME</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-520">O nome do par.</span><span class="sxs-lookup"><span data-stu-id="3e505-520">The name of the peer.</span></span> <span data-ttu-id="3e505-521">Por exemplo, o nome DNS do par.</span><span class="sxs-lookup"><span data-stu-id="3e505-521">For example, the peer's DNS name.</span></span><br/> <span data-ttu-id="3e505-522"><strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-522"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_REMOTE_ID"></span><span id="fwpm_condition_remote_id"></span><dl> <span data-ttu-id="3e505-523"><dt><strong>FWPM_CONDITION_REMOTE_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-523"><dt><strong>FWPM_CONDITION_REMOTE_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-524">A identidade da entidade de autenticação remota.</span><span class="sxs-lookup"><span data-stu-id="3e505-524">The identity of the remote authentication principal.</span></span> <br/> <span data-ttu-id="3e505-525"><strong>Tipo de dados:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-525"><strong>Data type:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_AUTHENTICATION_TYPE"></span><span id="fwpm_condition_authentication_type"></span><dl> <span data-ttu-id="3e505-526"><dt><strong>FWPM_CONDITION_AUTHENTICATION_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-526"><dt><strong>FWPM_CONDITION_AUTHENTICATION_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-527">O tipo de método de autenticação IKE, IKEv2 ou AuthIP.</span><span class="sxs-lookup"><span data-stu-id="3e505-527">The type of IKE, IKEv2, or AuthIP authentication method.</span></span> <br/> <span data-ttu-id="3e505-528"><strong>Tipo de dados:</strong> IKEEXT_AUTHENTICATION_METHOD_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-528"><strong>Data type:</strong> IKEEXT_AUTHENTICATION_METHOD_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_KM_TYPE"></span><span id="fwpm_condition_km_type"></span><dl> <span data-ttu-id="3e505-529"><dt><strong>FWPM_CONDITION_KM_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-529"><dt><strong>FWPM_CONDITION_KM_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-530">O tipo de módulo de criação de chaves.</span><span class="sxs-lookup"><span data-stu-id="3e505-530">The type of keying module.</span></span><br/> <span data-ttu-id="3e505-531"><strong>Tipo de dados:</strong> IKEEXT_KEY_MODULE_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-531"><strong>Data type:</strong> IKEEXT_KEY_MODULE_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_KM_MODE"></span><span id="fwpm_condition_km_mode"></span><dl> <span data-ttu-id="3e505-532"><dt><strong>FWPM_CONDITION_KM_MODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-532"><dt><strong>FWPM_CONDITION_KM_MODE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-533">O modo IPsec no qual um token pode ser obtido.</span><span class="sxs-lookup"><span data-stu-id="3e505-533">The IPsec mode in which a token can be obtained.</span></span><br/> <span data-ttu-id="3e505-534"><strong>Tipo de dados:</strong> IPSEC_TOKEN_MODE</span><span class="sxs-lookup"><span data-stu-id="3e505-534"><strong>Data type:</strong> IPSEC_TOKEN_MODE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IPSEC_POLICY_KEY"></span><span id="fwpm_condition_ipsec_policy_key"></span><dl> <span data-ttu-id="3e505-535"><dt><strong>FWPM_CONDITION_IPSEC_POLICY_KEY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-535"><dt><strong>FWPM_CONDITION_IPSEC_POLICY_KEY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-536">A chave de contexto do provedor de política de modo principal (MM) ou de modo rápido (QM) do SA que está sendo autorizado.</span><span class="sxs-lookup"><span data-stu-id="3e505-536">The main mode (MM) or quick mode (QM) policy provider context key of the SA being authorized.</span></span> <span data-ttu-id="3e505-537">Útil para restringir o escopo da regra de autorização à SAs formada usando uma chave de política IPsec MM ou QM especificada.</span><span class="sxs-lookup"><span data-stu-id="3e505-537">Useful for restricting the scope of the authorization rule to SAs formed using a specified IPsec MM or QM policy key.</span></span><br/> <span data-ttu-id="3e505-538"><strong>Tipo de dados:</strong> FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-538"><strong>Data type:</strong> FWP_BYTE_ARRAY16_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_AUTHENTICATION_TYPE"></span><span id="fwpm_condition_authentication_type"></span><dl> <span data-ttu-id="3e505-539"><dt><strong>FWPM_CONDITION_AUTHENTICATION_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-539"><dt><strong>FWPM_CONDITION_AUTHENTICATION_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-540">O método usado para autenticar a associação de segurança.</span><span class="sxs-lookup"><span data-stu-id="3e505-540">The method used to authenticate the security association.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3e505-541">Disponível apenas no Windows Server 2008 R2, Windows 7 e posterior.</span><span class="sxs-lookup"><span data-stu-id="3e505-541">Available only on Windows Server 2008 R2, Windows 7, and later.</span></span>
</blockquote>
<br/> <span data-ttu-id="3e505-542"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-542"><strong>Data type:</strong> FWP_UINT32</span></span> <br/></td>
</tr>
</tbody>
</table>





<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="3e505-543">Constantes disponíveis para o Windows Vista e posterior</span><span class="sxs-lookup"><span data-stu-id="3e505-543">Constants available for Windows Vista and later</span></span></th>
<th style="text-align: left;"><span data-ttu-id="3e505-544">Description</span><span class="sxs-lookup"><span data-stu-id="3e505-544">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_REMOTE_USER_TOKEN"></span><span id="fwpm_condition_remote_user_token"></span><dl> <span data-ttu-id="3e505-545"><dt><strong>FWPM_CONDITION_REMOTE_USER_TOKEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-545"><dt><strong>FWPM_CONDITION_REMOTE_USER_TOKEN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-546">A identificação do usuário remoto.</span><span class="sxs-lookup"><span data-stu-id="3e505-546">The identification of the remote user.</span></span><br/> <span data-ttu-id="3e505-547"><strong>Tipo de dados:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-547"><strong>Data type:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_IF_UUID"></span><span id="fwpm_condition_rpc_if_uuid"></span><dl> <span data-ttu-id="3e505-548"><dt><strong>FWPM_CONDITION_RPC_IF_UUID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-548"><dt><strong>FWPM_CONDITION_RPC_IF_UUID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-549">O UUID da interface RPC.</span><span class="sxs-lookup"><span data-stu-id="3e505-549">The UUID of the RPC interface.</span></span> <br/> <span data-ttu-id="3e505-550"><strong>Tipo de dados:</strong> FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-550"><strong>Data type:</strong> FWP_BYTE_ARRAY16_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_IF_VERSION"></span><span id="fwpm_condition_rpc_if_version"></span><dl> <span data-ttu-id="3e505-551"><dt><strong>FWPM_CONDITION_RPC_IF_VERSION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-551"><dt><strong>FWPM_CONDITION_RPC_IF_VERSION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-552">A versão da interface RPC.</span><span class="sxs-lookup"><span data-stu-id="3e505-552">The version of the RPC interface.</span></span> <br/> <span data-ttu-id="3e505-553"><strong>Tipo de dados:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="3e505-553"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_IF_FLAG"></span><span id="fwpm_condition_rpc_if_flag"></span><dl> <span data-ttu-id="3e505-554"><dt><strong>FWPM_CONDITION_RPC_IF_FLAG</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-554"><dt><strong>FWPM_CONDITION_RPC_IF_FLAG</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-555">Reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="3e505-555">Reserved for internal use.</span></span> <br/> <span data-ttu-id="3e505-556"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-556"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_DCOM_APP_ID"></span><span id="fwpm_condition_dcom_app_id"></span><dl> <span data-ttu-id="3e505-557"><dt><strong>FWPM_CONDITION_DCOM_APP_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-557"><dt><strong>FWPM_CONDITION_DCOM_APP_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-558">A identificação do aplicativo COM.</span><span class="sxs-lookup"><span data-stu-id="3e505-558">The identification of the COM application.</span></span><br/> <span data-ttu-id="3e505-559"><strong>Tipo de dados:</strong> FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-559"><strong>Data type:</strong> FWP_BYTE_ARRAY16_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IMAGE_NAME"></span><span id="fwpm_condition_image_name"></span><dl> <span data-ttu-id="3e505-560"><dt><strong>FWPM_CONDITION_IMAGE_NAME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-560"><dt><strong>FWPM_CONDITION_IMAGE_NAME</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-561">O nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3e505-561">The name of the application.</span></span><br/> <span data-ttu-id="3e505-562"><strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-562"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_PROTOCOL"></span><span id="fwpm_condition_rpc_protocol"></span><dl> <span data-ttu-id="3e505-563"><dt><strong>FWPM_CONDITION_RPC_PROTOCOL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-563"><dt><strong>FWPM_CONDITION_RPC_PROTOCOL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-564">O Protocolo RPC.</span><span class="sxs-lookup"><span data-stu-id="3e505-564">The RPC protocol.</span></span> <br/> <span data-ttu-id="3e505-565"><strong>Valores possíveis:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="3e505-565"><strong>Possible values:  </strong>
</span></span><ul>
<li><span data-ttu-id="3e505-566">RPC_PROTSEQ_TCP</span><span class="sxs-lookup"><span data-stu-id="3e505-566">RPC_PROTSEQ_TCP</span></span></li>
<li><span data-ttu-id="3e505-567">RPC_PROTSEQ_NMP</span><span class="sxs-lookup"><span data-stu-id="3e505-567">RPC_PROTSEQ_NMP</span></span></li>
<li><span data-ttu-id="3e505-568">RPC_PROTSEQ_LRPC</span><span class="sxs-lookup"><span data-stu-id="3e505-568">RPC_PROTSEQ_LRPC</span></span></li>
<li><span data-ttu-id="3e505-569">RPC_PROTSEQ_HTTP</span><span class="sxs-lookup"><span data-stu-id="3e505-569">RPC_PROTSEQ_HTTP</span></span></li>
</ul>
<br/> <span data-ttu-id="3e505-570"><strong>Tipo de dados:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="3e505-570"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_AUTH_TYPE"></span><span id="fwpm_condition_rpc_auth_type"></span><dl> <span data-ttu-id="3e505-571"><dt><strong>FWPM_CONDITION_RPC_AUTH_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-571"><dt><strong>FWPM_CONDITION_RPC_AUTH_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-572">O tipo de serviço de autenticação.</span><span class="sxs-lookup"><span data-stu-id="3e505-572">The authentication service type.</span></span> <span data-ttu-id="3e505-573">Para obter mais informações sobre os tipos de serviço de autenticação, consulte <a href="/windows/desktop/Rpc/authentication-service-constants"><strong>autenticação-constantes de serviço</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="3e505-573">For more information about authentication service types, see <a href="/windows/desktop/Rpc/authentication-service-constants"><strong>Authentication-Service Constants</strong></a>.</span></span> <br/> <span data-ttu-id="3e505-574"><strong>Tipo de dados:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="3e505-574"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_AUTH_LEVEL"></span><span id="fwpm_condition_rpc_auth_level"></span><dl> <span data-ttu-id="3e505-575"><dt><strong>FWPM_CONDITION_RPC_AUTH_LEVEL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-575"><dt><strong>FWPM_CONDITION_RPC_AUTH_LEVEL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-576">O nível de serviço de autenticação.</span><span class="sxs-lookup"><span data-stu-id="3e505-576">The authentication service level.</span></span> <span data-ttu-id="3e505-577">Para obter mais informações sobre os níveis de serviço de autenticação, consulte <a href="/windows/desktop/Rpc/authentication-level-constants"><strong>constantes de nível de autenticação</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="3e505-577">For more information about authentication service levels, see <a href="/windows/desktop/Rpc/authentication-level-constants"><strong>Authentication-Level Constants</strong></a>.</span></span> <br/> <span data-ttu-id="3e505-578"><strong>Tipo de dados:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="3e505-578"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM"></span><span id="fwpm_condition_sec_encrypt_algorithm"></span><dl> <span data-ttu-id="3e505-579"><dt><strong>FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-579"><dt><strong>FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-580">O algoritmo de criptografia SSPI (interface de provedor de serviço de segurança) baseado em certificado.</span><span class="sxs-lookup"><span data-stu-id="3e505-580">The certificate based Security Service Provider Interface (SSPI) encryption algorithm.</span></span><br/> <span data-ttu-id="3e505-581"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-581"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_SEC_KEY_SIZE"></span><span id="fwpm_condition_sec_key_size"></span><dl> <span data-ttu-id="3e505-582"><dt><strong>FWPM_CONDITION_SEC_KEY_SIZE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-582"><dt><strong>FWPM_CONDITION_SEC_KEY_SIZE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-583">O tamanho da chave de criptografia SSPI baseada em certificado.</span><span class="sxs-lookup"><span data-stu-id="3e505-583">The certificate based SSPI encryption key size.</span></span><br/> <span data-ttu-id="3e505-584"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-584"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS_V4"></span><span id="fwpm_condition_ip_local_address_v4"></span><dl> <span data-ttu-id="3e505-585"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-585"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-586">O endereço IPv4 local.</span><span class="sxs-lookup"><span data-stu-id="3e505-586">The local IPv4 address.</span></span> <br/> <span data-ttu-id="3e505-587"><strong>Tipo de dados:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="3e505-587"><strong>Data type:  </strong>
</span></span><ul>
<li><span data-ttu-id="3e505-588">FWP_V4_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="3e505-588">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="3e505-589">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-589">FWP_UINT32</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS_V6"></span><span id="fwpm_condition_ip_local_address_v6"></span><dl> <span data-ttu-id="3e505-590"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-590"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-591">O endereço IPv6 local.</span><span class="sxs-lookup"><span data-stu-id="3e505-591">The local IPv6 address.</span></span> <br/> <span data-ttu-id="3e505-592"><strong>Tipo de dados:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="3e505-592"><strong>Data type:  </strong>
</span></span><ul>
<li><span data-ttu-id="3e505-593">FWP_V6_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="3e505-593">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="3e505-594">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-594">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_ADDRESS_V4"></span><span id="fwpm_condition_ip_remote_address_v4"></span><dl> <span data-ttu-id="3e505-595"><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-595"><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-596">O endereço IPv4 remoto.</span><span class="sxs-lookup"><span data-stu-id="3e505-596">The remote IPv4 address.</span></span> <br/> <span data-ttu-id="3e505-597"><strong>Tipo de dados:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="3e505-597"><strong>Data type:  </strong>
</span></span><ul>
<li><span data-ttu-id="3e505-598">FWP_V4_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="3e505-598">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="3e505-599">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-599">FWP_UINT32</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_ADDRESS_V6"></span><span id="fwpm_condition_ip_remote_address_v6"></span><dl> <span data-ttu-id="3e505-600"><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-600"><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-601">O endereço IPv6 remoto.</span><span class="sxs-lookup"><span data-stu-id="3e505-601">The remote IPv6 address.</span></span> <br/> <span data-ttu-id="3e505-602"><strong>Tipo de dados:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="3e505-602"><strong>Data type:  </strong>
</span></span><ul>
<li><span data-ttu-id="3e505-603">FWP_V6_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="3e505-603">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="3e505-604">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-604">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_PIPE"></span><span id="fwpm_condition_pipe"></span><dl> <span data-ttu-id="3e505-605"><dt><strong>FWPM_CONDITION_PIPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-605"><dt><strong>FWPM_CONDITION_PIPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-606">O nome do pipe nomeado remoto.</span><span class="sxs-lookup"><span data-stu-id="3e505-606">The name of the remote named pipe.</span></span><br/> <span data-ttu-id="3e505-607"><strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-607"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID"></span><span id="fwpm_condition_process_with_rpc_if_uuid"></span><dl> <span data-ttu-id="3e505-608"><dt><strong>FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-608"><dt><strong>FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-609">O UUID do processo com a interface RPC.</span><span class="sxs-lookup"><span data-stu-id="3e505-609">The UUID of the process with the RPC interface.</span></span><br/> <span data-ttu-id="3e505-610"><strong>Tipo de dados:</strong> FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-610"><strong>Data type:</strong> FWP_BYTE_ARRAY16_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_EP_VALUE"></span><span id="fwpm_condition_rpc_ep_value"></span><dl> <span data-ttu-id="3e505-611"><dt><strong>FWPM_CONDITION_RPC_EP_VALUE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-611"><dt><strong>FWPM_CONDITION_RPC_EP_VALUE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-612">Reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="3e505-612">Reserved for internal use.</span></span><br/> <span data-ttu-id="3e505-613"><strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-613"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_EP_FLAGS"></span><span id="fwpm_condition_rpc_ep_flags"></span><dl> <span data-ttu-id="3e505-614"><dt><strong>FWPM_CONDITION_RPC_EP_FLAGS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-614"><dt><strong>FWPM_CONDITION_RPC_EP_FLAGS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-615">Reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="3e505-615">Reserved for internal use.</span></span><br/> <span data-ttu-id="3e505-616"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-616"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_CLIENT_TOKEN"></span><span id="fwpm_condition_client_token"></span><dl> <span data-ttu-id="3e505-617"><dt><strong>FWPM_CONDITION_CLIENT_TOKEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-617"><dt><strong>FWPM_CONDITION_CLIENT_TOKEN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-618">A identificação do cliente ao usar RpcProxy.</span><span class="sxs-lookup"><span data-stu-id="3e505-618">The identification of the client when using RpcProxy.</span></span><br/> <span data-ttu-id="3e505-619"><strong>Tipo de dados:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-619"><strong>Data type:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_SERVER_NAME"></span><span id="fwpm_condition_rpc_server_name"></span><dl> <span data-ttu-id="3e505-620"><dt><strong>FWPM_CONDITION_RPC_SERVER_NAME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-620"><dt><strong>FWPM_CONDITION_RPC_SERVER_NAME</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-621">O nome do servidor RPC ao usar RpcProxy.</span><span class="sxs-lookup"><span data-stu-id="3e505-621">The name of the RPC server when using RpcProxy.</span></span><br/> <span data-ttu-id="3e505-622"><strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-622"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_SERVER_PORT"></span><span id="fwpm_condition_rpc_server_port"></span><dl> <span data-ttu-id="3e505-623"><dt><strong>FWPM_CONDITION_RPC_SERVER_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-623"><dt><strong>FWPM_CONDITION_RPC_SERVER_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-624">A porta no servidor RPC ao usar RpcProxy.</span><span class="sxs-lookup"><span data-stu-id="3e505-624">The port on the RPC server when using RpcProxy.</span></span><br/> <span data-ttu-id="3e505-625"><strong>Tipo de dados:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="3e505-625"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_PROXY_AUTH_TYPE"></span><span id="fwpm_condition_rpc_proxy_auth_type"></span><dl> <span data-ttu-id="3e505-626"><dt><strong>FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-626"><dt><strong>FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-627">O tipo de serviço de autenticação de proxy RPC.</span><span class="sxs-lookup"><span data-stu-id="3e505-627">The RPC proxy authentication service type.</span></span><br/> <span data-ttu-id="3e505-628"><strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-628"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH"></span><span id="fwpm_condition_client_cert_key_length"></span><dl> <span data-ttu-id="3e505-629"><dt><strong>FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-629"><dt><strong>FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-630">O comprimento da chave SSL no certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="3e505-630">The Secure Socket Layer (SSL) key length in the client certificate.</span></span><br/> <span data-ttu-id="3e505-631"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-631"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_CLIENT_CERT_OID"></span><span id="fwpm_condition_client_cert_oid"></span><dl> <span data-ttu-id="3e505-632"><dt><strong>FWPM_CONDITION_CLIENT_CERT_OID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-632"><dt><strong>FWPM_CONDITION_CLIENT_CERT_OID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-633">O identificador de objeto no certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="3e505-633">The object identifier in the client certificate.</span></span><br/> <span data-ttu-id="3e505-634"><strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="3e505-634"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_NET_EVENT_TYPE"></span><span id="fwpm_condition_net_event_type"></span><dl> <span data-ttu-id="3e505-635"><dt><strong>FWPM_CONDITION_NET_EVENT_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3e505-635"><dt><strong>FWPM_CONDITION_NET_EVENT_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3e505-636">O tipo de evento de rede.</span><span class="sxs-lookup"><span data-stu-id="3e505-636">The type of net event.</span></span><br/> <span data-ttu-id="3e505-637"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="3e505-637"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="3e505-638">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e505-638">Remarks</span></span>

<span data-ttu-id="3e505-639">Quando os endereços IP são armazenados no \_ formato fwp UINT32 ou quando uma porta IP é armazenada no \_ formato fwp UINT16, eles são armazenados em ordem de host, não em ordem de rede.</span><span class="sxs-lookup"><span data-stu-id="3e505-639">When IP addresses are stored in FWP\_UINT32 format or when an IP port is stored in FWP\_UINT16 format, they are stored in host-order, not network-order.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e505-640">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e505-640">Requirements</span></span>



| <span data-ttu-id="3e505-641">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e505-641">Requirement</span></span> | <span data-ttu-id="3e505-642">Valor</span><span class="sxs-lookup"><span data-stu-id="3e505-642">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3e505-643">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e505-643">Minimum supported client</span></span><br/> | <span data-ttu-id="3e505-644">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3e505-644">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3e505-645">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e505-645">Minimum supported server</span></span><br/> | <span data-ttu-id="3e505-646">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3e505-646">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3e505-647">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3e505-647">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e505-648"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e505-648"><dt>Fwpmu.h</dt></span></span> </dl> |

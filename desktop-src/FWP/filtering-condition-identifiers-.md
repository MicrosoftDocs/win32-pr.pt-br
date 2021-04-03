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
# <a name="filtering-condition-identifiers"></a><span data-ttu-id="27d8c-103">Filtrando identificadores de condição</span><span class="sxs-lookup"><span data-stu-id="27d8c-103">Filtering Condition Identifiers</span></span>

<span data-ttu-id="27d8c-104">Os identificadores de condição de filtragem da WFP (Windows Filtering Platform) são representados por um **GUID**.</span><span class="sxs-lookup"><span data-stu-id="27d8c-104">The Windows Filtering Platform (WFP) filtering condition identifiers are each represented by a **GUID**.</span></span> <span data-ttu-id="27d8c-105">O tipo de dados para o valor da condição para cada condição de filtragem é especificado como um [**\_ \_ tipo de dados fwp**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span><span class="sxs-lookup"><span data-stu-id="27d8c-105">The data type for the condition value for each filtering condition is specified as an [**FWP\_DATA\_TYPE**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span></span> <span data-ttu-id="27d8c-106">Esses identificadores e seus tipos de dados são definidos aqui.</span><span class="sxs-lookup"><span data-stu-id="27d8c-106">These identifiers and their data types are defined here.</span></span>

<span data-ttu-id="27d8c-107">As condições padrão são listadas primeiro, seguidas pelas condições específicas para o modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="27d8c-107">The standard conditions are listed first, followed by the conditions specific to user mode.</span></span> <span data-ttu-id="27d8c-108">As condições são agrupadas por sistema operacional com suporte, para que você possa identificar facilmente quais condições têm suporte para um determinado so.</span><span class="sxs-lookup"><span data-stu-id="27d8c-108">Conditions are grouped by supported operating system, so that you can easily tell which conditions are supported for a given OS.</span></span>

> [!Note]  
> <span data-ttu-id="27d8c-109">Cada uma das condições de filtragem a seguir está disponível apenas em um subconjunto das camadas de filtragem WFP.</span><span class="sxs-lookup"><span data-stu-id="27d8c-109">Each of the following filtering conditions is available only at a subset of the WFP filtering layers.</span></span> <span data-ttu-id="27d8c-110">Para obter mais informações sobre a disponibilidade de cada condição em uma determinada camada, consulte [**condições de filtragem disponíveis em cada camada de filtragem**](filtering-conditions-available-at-each-filtering-layer.md).</span><span class="sxs-lookup"><span data-stu-id="27d8c-110">For more information on each condition's availability at any given layer, see [**Filtering Conditions Available at Each Filtering Layer**](filtering-conditions-available-at-each-filtering-layer.md).</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="27d8c-111">Condições disponíveis para o Windows 8 e o Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="27d8c-111">Conditions available for Windows 8 and Windows Server 2012</span></span></th>
<th style="text-align: left;"><span data-ttu-id="27d8c-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="27d8c-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE_MAC_ADDRESS"></span><span id="fwpm_condition_interface_mac_address"></span><dl> <span data-ttu-id="27d8c-113"><dt><strong>FWPM_CONDITION_INTERFACE_MAC_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-113"><dt><strong>FWPM_CONDITION_INTERFACE_MAC_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-114">O endereço MAC de uma interface local específica.</span><span class="sxs-lookup"><span data-stu-id="27d8c-114">The MAC address of a particular local interface.</span></span><br/> <span data-ttu-id="27d8c-115"><strong>Tipo de dados:</strong> FWP_BYTE_ARRAY6_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-115"><strong>Data type:</strong> FWP_BYTE_ARRAY6_TYPE</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_LOCAL_ADDRESS"></span><span id="fwpm_condition_mac_local_address"></span><dl> <span data-ttu-id="27d8c-116"><dt><strong>FWPM_CONDITION_MAC_LOCAL_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-116"><dt><strong>FWPM_CONDITION_MAC_LOCAL_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-117">Endereço de destino de um quadro de entrada ou endereço de origem de um quadro de saída.</span><span class="sxs-lookup"><span data-stu-id="27d8c-117">Destination address of an inbound frame, or source address of an outbound frame.</span></span><br/> <span data-ttu-id="27d8c-118"><strong>Tipo de dados:</strong> FWP_BYTE_ARRAY6_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-118"><strong>Data type:</strong> FWP_BYTE_ARRAY6_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_REMOTE_ADDRESS"></span><span id="fwpm_condition_mac_remote_address"></span><dl> <span data-ttu-id="27d8c-119"><dt><strong>FWPM_CONDITION_MAC_REMOTE_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-119"><dt><strong>FWPM_CONDITION_MAC_REMOTE_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-120">Endereço de origem de um quadro de entrada ou endereço de destino de um quadro de saída.</span><span class="sxs-lookup"><span data-stu-id="27d8c-120">Source address of an inbound frame, or destination address of an outbound frame.</span></span><br/> <span data-ttu-id="27d8c-121"><strong>Tipo de dados:</strong> FWP_BYTE_ARRAY6_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-121"><strong>Data type:</strong> FWP_BYTE_ARRAY6_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ETHER_TYPE"></span><span id="fwpm_condition_ether_type"></span><dl> <span data-ttu-id="27d8c-122"><dt><strong>FWPM_CONDITION_ETHER_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-122"><dt><strong>FWPM_CONDITION_ETHER_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-123">O tipo de dados de carga de rede Ethernet v2.</span><span class="sxs-lookup"><span data-stu-id="27d8c-123">The Ethernet V2 network payload data type.</span></span> <span data-ttu-id="27d8c-124">(Consulte ETHERNET_TYPE_IPV4, etc. em netiodef. h.)</span><span class="sxs-lookup"><span data-stu-id="27d8c-124">(See ETHERNET_TYPE_IPV4, etc. in netiodef.h.)</span></span><br/> <span data-ttu-id="27d8c-125"><strong>Tipo de dados:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="27d8c-125"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VLAN_ID"></span><span id="fwpm_condition_vlan_id"></span><dl> <span data-ttu-id="27d8c-126"><dt><strong>FWPM_CONDITION_VLAN_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-126"><dt><strong>FWPM_CONDITION_VLAN_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-127">Os 16 bits de cabeçalho de VLAN, incluindo os campos VID, IPF e Priority de acordo com o padrão 802.1 q (consulte VLAN_TAG em netiodef. h para as posições de bitfields).</span><span class="sxs-lookup"><span data-stu-id="27d8c-127">The 16-bits of VLAN header including the VID, CFI, and Priority fields as per the 802.1q standard (see VLAN_TAG in netiodef.h for the positions of the bitfields).</span></span><br/> <span data-ttu-id="27d8c-128"><strong>Tipo de dados:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="27d8c-128"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID"></span><span id="fwpm_condition_vswitch_tenant_network_id"></span><dl> <span data-ttu-id="27d8c-129"><dt><strong>FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-129"><dt><strong>FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-130">Identificador exclusivo para a rede vSwitch.</span><span class="sxs-lookup"><span data-stu-id="27d8c-130">Unique identifier for the vSwitch network.</span></span> <span data-ttu-id="27d8c-131">Não pode ser usado em conjunto com VLAN_IDs.</span><span class="sxs-lookup"><span data-stu-id="27d8c-131">Cannot be used in conjunction with VLAN_IDs.</span></span><br/> <span data-ttu-id="27d8c-132"><strong>Tipo de dados:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="27d8c-132"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_NDIS_PORT"></span><span id="fwpm_condition_ndis_port"></span><dl> <span data-ttu-id="27d8c-133"><dt><strong>FWPM_CONDITION_NDIS_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-133"><dt><strong>FWPM_CONDITION_NDIS_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-134">O número da porta da porta NDIS.</span><span class="sxs-lookup"><span data-stu-id="27d8c-134">The port number of the NDIS port.</span></span><br/> <span data-ttu-id="27d8c-135"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-135"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_NDIS_MEDIA_TYPE"></span><span id="fwpm_condition_ndis_media_type"></span><dl> <span data-ttu-id="27d8c-136"><dt><strong>FWPM_CONDITION_NDIS_MEDIA_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-136"><dt><strong>FWPM_CONDITION_NDIS_MEDIA_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-137">O tipo de mídia da porta NDIS.</span><span class="sxs-lookup"><span data-stu-id="27d8c-137">The media type of the NDIS port.</span></span><br/> <span data-ttu-id="27d8c-138"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-138"><strong>Data type:</strong> FWP_UINT32</span></span><br/> <span data-ttu-id="27d8c-139"><strong>Valores possíveis:</strong> Qualquer um dos <strong>NDIS_MEDIUM</strong> valores de enumeração.</span><span class="sxs-lookup"><span data-stu-id="27d8c-139"><strong>Possible values:</strong> Any of the <strong>NDIS_MEDIUM</strong> enumeration values.</span></span> <span data-ttu-id="27d8c-140">(Consulte Ntddndis. h.)</span><span class="sxs-lookup"><span data-stu-id="27d8c-140">(See ntddndis.h.)</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE"></span><span id="fwpm_condition_ndis_physical_media_type"></span><dl> <span data-ttu-id="27d8c-141"><dt><strong>FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-141"><dt><strong>FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-142">O tipo de mídia física da porta NDIS.</span><span class="sxs-lookup"><span data-stu-id="27d8c-142">The physical media type of the NDIS port.</span></span><br/> <span data-ttu-id="27d8c-143"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-143"><strong>Data type:</strong> FWP_UINT32</span></span><br/> <span data-ttu-id="27d8c-144"><strong>Valores possíveis:</strong> Qualquer um dos <strong>NDIS_PHYSICAL_MEDIUM</strong> valores de enumeração.</span><span class="sxs-lookup"><span data-stu-id="27d8c-144"><strong>Possible values:</strong> Any of the <strong>NDIS_PHYSICAL_MEDIUM</strong> enumeration values.</span></span> <span data-ttu-id="27d8c-145">(Consulte Ntddndis. h.)</span><span class="sxs-lookup"><span data-stu-id="27d8c-145">(See ntddndis.h.)</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_L2_FLAGS"></span><span id="fwpm_condition_l2_flags"></span><dl> <span data-ttu-id="27d8c-146"><dt><strong>FWPM_CONDITION_L2_FLAGS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-146"><dt><strong>FWPM_CONDITION_L2_FLAGS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-147">Uma operação OR de uma combinação de sinalizadores de condição de filtragem.</span><span class="sxs-lookup"><span data-stu-id="27d8c-147">A bitwise OR of a combination of filtering condition flags.</span></span> <br/> <span data-ttu-id="27d8c-148"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-148"><strong>Data type:</strong> FWP_UINT32</span></span><br/> <span data-ttu-id="27d8c-149"><strong>Valores possíveis:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="27d8c-149"><strong>Possible values:  </strong>
</span></span><ul>
<li><span data-ttu-id="27d8c-150">FWP_CONDITION_L2_IS_MOBILE_BROADBAND</span><span class="sxs-lookup"><span data-stu-id="27d8c-150">FWP_CONDITION_L2_IS_MOBILE_BROADBAND</span></span></li>
<li><span data-ttu-id="27d8c-151">FWP_CONDITION_L2_IS_NATIVE_ETHERNET</span><span class="sxs-lookup"><span data-stu-id="27d8c-151">FWP_CONDITION_L2_IS_NATIVE_ETHERNET</span></span></li>
<li><span data-ttu-id="27d8c-152">FWP_CONDITION_L2_IS_WIFI</span><span class="sxs-lookup"><span data-stu-id="27d8c-152">FWP_CONDITION_L2_IS_WIFI</span></span></li>
<li><span data-ttu-id="27d8c-153">FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA</span><span class="sxs-lookup"><span data-stu-id="27d8c-153">FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_local_address_type"></span><dl> <span data-ttu-id="27d8c-154"><dt><strong>FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-154"><dt><strong>FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-155">O tipo de endereço do endereço local físico.</span><span class="sxs-lookup"><span data-stu-id="27d8c-155">The address type of the physical local address.</span></span><br/> <span data-ttu-id="27d8c-156"><strong>Tipo de dados:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="27d8c-156"><strong>Data type:</strong> FWP_UINT8</span></span><br/> <span data-ttu-id="27d8c-157"><strong>Valores possíveis:</strong> Qualquer um dos seguintes <strong>DL_ADDRESS_TYPE</strong> valores de enumeração.</span><span class="sxs-lookup"><span data-stu-id="27d8c-157"><strong>Possible values:</strong> Any of the following <strong>DL_ADDRESS_TYPE</strong> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="27d8c-158">DlUnicast</span><span class="sxs-lookup"><span data-stu-id="27d8c-158">DlUnicast</span></span></li>
<li><span data-ttu-id="27d8c-159">DlMulticast</span><span class="sxs-lookup"><span data-stu-id="27d8c-159">DlMulticast</span></span></li>
<li><span data-ttu-id="27d8c-160">DlBroadcast</span><span class="sxs-lookup"><span data-stu-id="27d8c-160">DlBroadcast</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_remote_address_type"></span><dl> <span data-ttu-id="27d8c-161"><dt><strong>FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-161"><dt><strong>FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-162">O tipo de endereço do endereço remoto físico.</span><span class="sxs-lookup"><span data-stu-id="27d8c-162">The address type of the physical remote address.</span></span><br/> <span data-ttu-id="27d8c-163"><strong>Tipo de dados:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="27d8c-163"><strong>Data type:</strong> FWP_UINT8</span></span><br/> <span data-ttu-id="27d8c-164"><strong>Valores possíveis:</strong> Qualquer um dos seguintes <strong>DL_ADDRESS_TYPE</strong> valores de enumeração.</span><span class="sxs-lookup"><span data-stu-id="27d8c-164"><strong>Possible values:</strong> Any of the following <strong>DL_ADDRESS_TYPE</strong> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="27d8c-165">DlUnicast</span><span class="sxs-lookup"><span data-stu-id="27d8c-165">DlUnicast</span></span></li>
<li><span data-ttu-id="27d8c-166">DlMulticast</span><span class="sxs-lookup"><span data-stu-id="27d8c-166">DlMulticast</span></span></li>
<li><span data-ttu-id="27d8c-167">DlBroadcast</span><span class="sxs-lookup"><span data-stu-id="27d8c-167">DlBroadcast</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_SOURCE_ADDRESS"></span><span id="fwpm_condition_mac_source_address"></span><dl> <span data-ttu-id="27d8c-168"><dt><strong>FWPM_CONDITION_MAC_SOURCE_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-168"><dt><strong>FWPM_CONDITION_MAC_SOURCE_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-169">O endereço de origem físico de um quadro.</span><span class="sxs-lookup"><span data-stu-id="27d8c-169">The physical source address of a frame.</span></span><br/> <span data-ttu-id="27d8c-170"><strong>Tipo de dados:</strong> FWP_BYTE_ARRAY6_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-170"><strong>Data type:</strong> FWP_BYTE_ARRAY6_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_DESTINATION_ADDRESS"></span><span id="fwpm_condition_mac_destination_address"></span><dl> <span data-ttu-id="27d8c-171"><dt><strong>FWPM_CONDITION_MAC_DESTINATION_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-171"><dt><strong>FWPM_CONDITION_MAC_DESTINATION_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-172">O endereço de destino físico de um quadro.</span><span class="sxs-lookup"><span data-stu-id="27d8c-172">The physical destination address of a frame.</span></span><br/> <span data-ttu-id="27d8c-173"><strong>Tipo de dados:</strong> FWP_BYTE_ARRAY6_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-173"><strong>Data type:</strong> FWP_BYTE_ARRAY6_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_source_address_type"></span><dl> <span data-ttu-id="27d8c-174"><dt><strong>FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-174"><dt><strong>FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-175">O tipo de endereço do endereço de destino físico.</span><span class="sxs-lookup"><span data-stu-id="27d8c-175">The address type of the physical destination address.</span></span><br/> <span data-ttu-id="27d8c-176"><strong>Tipo de dados:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="27d8c-176"><strong>Data type:</strong> FWP_UINT8</span></span><br/> <span data-ttu-id="27d8c-177"><strong>Valores possíveis:</strong> Qualquer um dos seguintes <strong>DL_ADDRESS_TYPE</strong> valores de enumeração.</span><span class="sxs-lookup"><span data-stu-id="27d8c-177"><strong>Possible values:</strong> Any of the following <strong>DL_ADDRESS_TYPE</strong> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="27d8c-178">DlUnicast</span><span class="sxs-lookup"><span data-stu-id="27d8c-178">DlUnicast</span></span></li>
<li><span data-ttu-id="27d8c-179">DlMulticast</span><span class="sxs-lookup"><span data-stu-id="27d8c-179">DlMulticast</span></span></li>
<li><span data-ttu-id="27d8c-180">DlBroadcast</span><span class="sxs-lookup"><span data-stu-id="27d8c-180">DlBroadcast</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_destination_address_type"></span><dl> <span data-ttu-id="27d8c-181"><dt><strong>FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-181"><dt><strong>FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-182">O tipo de endereço do endereço de destino físico.</span><span class="sxs-lookup"><span data-stu-id="27d8c-182">The address type of the physical destination address.</span></span><br/> <span data-ttu-id="27d8c-183"><strong>Tipo de dados:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="27d8c-183"><strong>Data type:</strong> FWP_UINT8</span></span><br/> <span data-ttu-id="27d8c-184"><strong>Valores possíveis:</strong> Qualquer um dos seguintes <strong>DL_ADDRESS_TYPE</strong> valores de enumeração.</span><span class="sxs-lookup"><span data-stu-id="27d8c-184"><strong>Possible values:</strong> Any of the following <strong>DL_ADDRESS_TYPE</strong> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="27d8c-185">DlUnicast</span><span class="sxs-lookup"><span data-stu-id="27d8c-185">DlUnicast</span></span></li>
<li><span data-ttu-id="27d8c-186">DlMulticast</span><span class="sxs-lookup"><span data-stu-id="27d8c-186">DlMulticast</span></span></li>
<li><span data-ttu-id="27d8c-187">DlBroadcast</span><span class="sxs-lookup"><span data-stu-id="27d8c-187">DlBroadcast</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_SOURCE_PORT"></span><span id="fwpm_condition_ip_source_port"></span><dl> <span data-ttu-id="27d8c-188"><dt><strong>FWPM_CONDITION_IP_SOURCE_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-188"><dt><strong>FWPM_CONDITION_IP_SOURCE_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-189">A porta de origem do transporte do pacote.</span><span class="sxs-lookup"><span data-stu-id="27d8c-189">The source port of the packet's transport.</span></span><br/> <span data-ttu-id="27d8c-190"><strong>Tipo de dados:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="27d8c-190"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_ICMP_TYPE"></span><span id="fwpm_condition_vswitch_icmp_type"></span><dl> <span data-ttu-id="27d8c-191"><dt><strong>FWPM_CONDITION_VSWITCH_ICMP_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-191"><dt><strong>FWPM_CONDITION_VSWITCH_ICMP_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-192">O campo tipo de ICMP, conforme especificado no RFC 792.</span><span class="sxs-lookup"><span data-stu-id="27d8c-192">The ICMP type field, as specified in RFC 792.</span></span><br/> <span data-ttu-id="27d8c-193"><strong>Tipo de dados:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="27d8c-193"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_DESTINATION_PORT"></span><span id="fwpm_condition_ip_destination_port"></span><dl> <span data-ttu-id="27d8c-194"><dt><strong>FWPM_CONDITION_IP_DESTINATION_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-194"><dt><strong>FWPM_CONDITION_IP_DESTINATION_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-195">A porta de destino do transporte do pacote.</span><span class="sxs-lookup"><span data-stu-id="27d8c-195">The destination port of the packet's transport.</span></span><br/> <span data-ttu-id="27d8c-196"><strong>Tipo de dados:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="27d8c-196"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_ICMP_CODE"></span><span id="fwpm_condition_vswitch_icmp_code"></span><dl> <span data-ttu-id="27d8c-197"><dt><strong>FWPM_CONDITION_VSWITCH_ICMP_CODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-197"><dt><strong>FWPM_CONDITION_VSWITCH_ICMP_CODE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-198">O campo de código ICMP, conforme especificado no RFC 792.</span><span class="sxs-lookup"><span data-stu-id="27d8c-198">The ICMP code field, as specified in RFC 792.</span></span> <br/> <span data-ttu-id="27d8c-199"><strong>Tipo de dados:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="27d8c-199"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_ID"></span><span id="fwpm_condition_vswitch_id"></span><dl> <span data-ttu-id="27d8c-200"><dt><strong>FWPM_CONDITION_VSWITCH_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-200"><dt><strong>FWPM_CONDITION_VSWITCH_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-201">Identificador exclusivo de uma instância de vSwitch.</span><span class="sxs-lookup"><span data-stu-id="27d8c-201">Unique identifier of an vSwitch instance.</span></span><br/> <span data-ttu-id="27d8c-202"><strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-202"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_NETWORK_TYPE"></span><span id="fwpm_condition_vswitch_network_type"></span><dl> <span data-ttu-id="27d8c-203"><dt><strong>FWPM_CONDITION_VSWITCH_NETWORK_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-203"><dt><strong>FWPM_CONDITION_VSWITCH_NETWORK_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-204">Especifica se a instância do vSwitch faz parte de uma rede virtual externa, interna ou privada.</span><span class="sxs-lookup"><span data-stu-id="27d8c-204">Specifies whether the vSwitch instance is part of an external, internal, or private virtual network.</span></span><br/> <span data-ttu-id="27d8c-205"><strong>Tipo de dados:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="27d8c-205"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID"></span><span id="fwpm_condition_vswitch_source_interface_id"></span><dl> <span data-ttu-id="27d8c-206"><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-206"><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-207">Identificador exclusivo da origem do pacote atual.</span><span class="sxs-lookup"><span data-stu-id="27d8c-207">Unique identifier of the source of the current packet.</span></span> <span data-ttu-id="27d8c-208">(O nome de uma VM-NIC, P-NIC ou V-NIC.)</span><span class="sxs-lookup"><span data-stu-id="27d8c-208">(The name of a VM-NIC, P-NIC, or V-NIC.)</span></span><br/> <span data-ttu-id="27d8c-209"><strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-209"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID"></span><span id="fwpm_condition_vswitch_destination_interface_id"></span><dl> <span data-ttu-id="27d8c-210"><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-210"><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-211">Identificador exclusivo do destino do pacote atual.</span><span class="sxs-lookup"><span data-stu-id="27d8c-211">Unique identifier of the destination of the current packet.</span></span> <span data-ttu-id="27d8c-212">(O nome de uma VM-NIC, P-NIC ou V-NIC.)</span><span class="sxs-lookup"><span data-stu-id="27d8c-212">(The name of a VM-NIC, P-NIC, or V-NIC.)</span></span><br/> <span data-ttu-id="27d8c-213"><strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-213"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_SOURCE_VM_ID"></span><span id="fwpm_condition_vswitch_source_vm_id"></span><dl> <span data-ttu-id="27d8c-214"><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-214"><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-215">Identificador exclusivo da máquina virtual de origem do vSwitch.</span><span class="sxs-lookup"><span data-stu-id="27d8c-215">Unique identifier of the vSwitch source virtual machine.</span></span><br/> <span data-ttu-id="27d8c-216"><strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-216"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_DESTINATION_VM_ID"></span><span id="fwpm_condition_vswitch_destination_vm_id"></span><dl> <span data-ttu-id="27d8c-217"><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_VM_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-217"><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_VM_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-218">Identificador exclusivo da máquina virtual de destino do vSwitch.</span><span class="sxs-lookup"><span data-stu-id="27d8c-218">Unique identifier of the vSwitch destination virtual machine.</span></span><br/> <span data-ttu-id="27d8c-219"><strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-219"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE"></span><span id="fwpm_condition_vswitch_source_interface_type"></span><dl> <span data-ttu-id="27d8c-220"><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-220"><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-221">Tipo de interface da origem do pacote atual.</span><span class="sxs-lookup"><span data-stu-id="27d8c-221">Interface type of the source of the current packet.</span></span><br/> <span data-ttu-id="27d8c-222"><strong>Tipo de dados:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="27d8c-222"><strong>Data type:</strong> FWP_UINT8</span></span><br/> <span data-ttu-id="27d8c-223"><strong>Valores possíveis:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="27d8c-223"><strong>Possible values:  </strong>
</span></span><ul>
<li><span data-ttu-id="27d8c-224">SwitchNicSyntheticNic (quando o tipo de interface é VM-NIC)</span><span class="sxs-lookup"><span data-stu-id="27d8c-224">SwitchNicSyntheticNic (when interface type is VM-NIC)</span></span></li>
<li><span data-ttu-id="27d8c-225">SwitchNicEmulatedNic (quando o tipo de interface é VM-NIC)</span><span class="sxs-lookup"><span data-stu-id="27d8c-225">SwitchNicEmulatedNic (when interface type is VM-NIC)</span></span></li>
<li><span data-ttu-id="27d8c-226">SwitchNicPhysicalNic (quando o tipo de interface é P-NIC)</span><span class="sxs-lookup"><span data-stu-id="27d8c-226">SwitchNicPhysicalNic (when interface type is P-NIC)</span></span></li>
<li><span data-ttu-id="27d8c-227">SwitchNicVNic (quando o tipo de interface é V-NIC, conectado à partição de host)</span><span class="sxs-lookup"><span data-stu-id="27d8c-227">SwitchNicVNic (when interface type is V-NIC, connected to the host partition)</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE"></span><span id="fwpm_condition_vswitch_destination_interface_type"></span><dl> <span data-ttu-id="27d8c-228"><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-228"><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-229">Tipo de interface do destino do pacote atual.</span><span class="sxs-lookup"><span data-stu-id="27d8c-229">Interface type of the destination of the current packet.</span></span><br/> <span data-ttu-id="27d8c-230"><strong>Tipo de dados:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="27d8c-230"><strong>Data type:</strong> FWP_UINT8</span></span><br/> <span data-ttu-id="27d8c-231"><strong>Valores possíveis:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="27d8c-231"><strong>Possible values:  </strong>
</span></span><ul>
<li><span data-ttu-id="27d8c-232">SwitchNicSyntheticNic (quando o tipo de interface é VM-NIC)</span><span class="sxs-lookup"><span data-stu-id="27d8c-232">SwitchNicSyntheticNic (when interface type is VM-NIC)</span></span></li>
<li><span data-ttu-id="27d8c-233">SwitchNicEmulatedNic (quando o tipo de interface é VM-NIC)</span><span class="sxs-lookup"><span data-stu-id="27d8c-233">SwitchNicEmulatedNic (when interface type is VM-NIC)</span></span></li>
<li><span data-ttu-id="27d8c-234">SwitchNicPhysicalNic (quando o tipo de interface é P-NIC)</span><span class="sxs-lookup"><span data-stu-id="27d8c-234">SwitchNicPhysicalNic (when interface type is P-NIC)</span></span></li>
<li><span data-ttu-id="27d8c-235">SwitchNicVNic (quando o tipo de interface é V-NIC, conectado à partição de host)</span><span class="sxs-lookup"><span data-stu-id="27d8c-235">SwitchNicVNic (when interface type is V-NIC, connected to the host partition)</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE"></span><span id="fwpm_condition_interface"></span><dl> <span data-ttu-id="27d8c-236"><dt><strong>FWPM_CONDITION_INTERFACE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-236"><dt><strong>FWPM_CONDITION_INTERFACE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-237">O LUID para a interface de rede associada ao endereço IP local.</span><span class="sxs-lookup"><span data-stu-id="27d8c-237">The LUID for the network interface associated with the local IP address.</span></span> <br/> <span data-ttu-id="27d8c-238"><strong>Tipo de dados:</strong> FWP_UINT64</span><span class="sxs-lookup"><span data-stu-id="27d8c-238"><strong>Data type:</strong> FWP_UINT64</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_PACKAGE_ID"></span><span id="fwpm_condition_ale_package_id"></span><dl> <span data-ttu-id="27d8c-239"><dt><strong>FWPM_CONDITION_ALE_PACKAGE_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-239"><dt><strong>FWPM_CONDITION_ALE_PACKAGE_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-240">O SID (identificador de segurança) de um contêiner de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="27d8c-240">The security identifier (SID) of an app container.</span></span><br/> <span data-ttu-id="27d8c-241"><strong>Tipo de dados:</strong> FWP_SID</span><span class="sxs-lookup"><span data-stu-id="27d8c-241"><strong>Data type:</strong> FWP_SID</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_ORIGINAL_APP_ID"></span><span id="fwpm_condition_ale_original_app_id"></span><dl> <span data-ttu-id="27d8c-242"><dt><strong>FWPM_CONDITION_ALE_ORIGINAL_APP_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-242"><dt><strong>FWPM_CONDITION_ALE_ORIGINAL_APP_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-243">O caminho do dispositivo totalmente qualificado do aplicativo, como &quot; \device0\hardiskvolume1\Program Files\Application.exe&quot; .</span><span class="sxs-lookup"><span data-stu-id="27d8c-243">The fully qualified device path of the application, such as &quot;\device0\hardiskvolume1\Program Files\Application.exe&quot;.</span></span> <span data-ttu-id="27d8c-244">Quando uma conexão for redirecionada, esse será o identificador do aplicativo de origem; caso contrário, isso será o mesmo que <strong>FWPM_CONDITION_ALE_APP_ID</strong>.</span><span class="sxs-lookup"><span data-stu-id="27d8c-244">When a connection has been redirected, this will be the identifier of the originating app; otherwise this will be the same as <strong>FWPM_CONDITION_ALE_APP_ID</strong>.</span></span><br/> <span data-ttu-id="27d8c-245"><strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-245"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
</tbody>
</table>





| <span data-ttu-id="27d8c-246">Condições disponíveis para o Windows 7, o Windows Server 2008 R2 e posterior</span><span class="sxs-lookup"><span data-stu-id="27d8c-246">Conditions available for Windows 7, Windows Server 2008 R2, and later</span></span>                                                                                                                                                                                                    | <span data-ttu-id="27d8c-247">Descrição</span><span class="sxs-lookup"><span data-stu-id="27d8c-247">Description</span></span>                                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_CONDITION_IP_NEXTHOP_ADDRESS"></span><span id="fwpm_condition_ip_nexthop_address"></span><dl> <span data-ttu-id="27d8c-248"><dt>**\_ \_ \_ endereço IP NEXTHOP \_ da condição FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="27d8c-248"><dt>**FWPM\_CONDITION\_IP\_NEXTHOP\_ADDRESS**</dt></span></span> </dl>                                             | <span data-ttu-id="27d8c-249">O endereço IP da interface de próximo salto.</span><span class="sxs-lookup"><span data-stu-id="27d8c-249">The IP address of the next-hop interface.</span></span><br/> <span data-ttu-id="27d8c-250">**Tipo de dados:** \_Máscara de \_ endereço \_ v4 de fwp</span><span class="sxs-lookup"><span data-stu-id="27d8c-250">**Data type:** FWP\_V4\_ADDR\_MASK</span></span><br/>                                                                                                                                                                                        |
| <span id="FWPM_CONDITION_IP_NEXTHOP_INTERFACE"></span><span id="fwpm_condition_ip_nexthop_interface"></span><dl> <span data-ttu-id="27d8c-251"><dt>**\_ \_ interface NEXTHOP de IP de condição FWPM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="27d8c-251"><dt>**FWPM\_CONDITION\_IP\_NEXTHOP\_INTERFACE**</dt></span></span> </dl>                                       | <span data-ttu-id="27d8c-252">A interface de próximo salto da qual o pacote será desparte.</span><span class="sxs-lookup"><span data-stu-id="27d8c-252">The next-hop interface from which the packet will be departing.</span></span> <br/> <span data-ttu-id="27d8c-253">**Tipo de dados:** FWP \_ UINT64</span><span class="sxs-lookup"><span data-stu-id="27d8c-253">**Data type:** FWP\_UINT64</span></span><br/>                                                                                                                                                                         |
| <span id="FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE"></span><span id="fwpm_condition_nexthop_interface_type"></span><dl> <span data-ttu-id="27d8c-254"><dt>**\_tipo de \_ \_ interface NEXTHOP da condição \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="27d8c-254"><dt>**FWPM\_CONDITION\_NEXTHOP\_INTERFACE\_TYPE**</dt></span></span> </dl>                                 | <span data-ttu-id="27d8c-255">O tipo de interface da interface de próximo salto.</span><span class="sxs-lookup"><span data-stu-id="27d8c-255">The interface type of the next-hop interface.</span></span><br/> <span data-ttu-id="27d8c-256">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-256">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                            |
| <span id="FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE"></span><span id="fwpm_condition_nexthop_tunnel_type"></span><dl> <span data-ttu-id="27d8c-257"><dt>**\_tipo de \_ \_ túnel NEXTHOP da condição \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="27d8c-257"><dt>**FWPM\_CONDITION\_NEXTHOP\_TUNNEL\_TYPE**</dt></span></span> </dl>                                          | <span data-ttu-id="27d8c-258">O tipo de túnel da interface de próximo salto.</span><span class="sxs-lookup"><span data-stu-id="27d8c-258">The tunnel type of the next-hop interface.</span></span><br/> <span data-ttu-id="27d8c-259">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-259">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                               |
| <span id="FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX"></span><span id="fwpm_condition_nexthop_interface_index"></span><dl> <span data-ttu-id="27d8c-260"><dt>**\_índice da \_ \_ interface NEXTHOP da condição \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="27d8c-260"><dt>**FWPM\_CONDITION\_NEXTHOP\_INTERFACE\_INDEX**</dt></span></span> </dl>                              | <span data-ttu-id="27d8c-261">O índice de interface da interface de próximo salto.</span><span class="sxs-lookup"><span data-stu-id="27d8c-261">The interface index of the next-hop interface.</span></span><br/> <span data-ttu-id="27d8c-262">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-262">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                           |
| <span id="FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_nexthop_sub_interface_index"></span><dl> <span data-ttu-id="27d8c-263"><dt>**\_índice de \_ sub \_ - \_ interface NEXTHOP da \_ condição FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="27d8c-263"><dt>**FWPM\_CONDITION\_NEXTHOP\_SUB\_INTERFACE\_INDEX**</dt></span></span> </dl>                 | <span data-ttu-id="27d8c-264">O índice de subinterface da interface de próximo salto.</span><span class="sxs-lookup"><span data-stu-id="27d8c-264">The sub-interface index of the next-hop interface.</span></span><br/> <span data-ttu-id="27d8c-265">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-265">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                       |
| <span id="FWPM_CONDITION_ORIGINAL_PROFILE_ID"></span><span id="fwpm_condition_original_profile_id"></span><dl> <span data-ttu-id="27d8c-266"><dt>**\_ID do \_ \_ perfil original da condição \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="27d8c-266"><dt>**FWPM\_CONDITION\_ORIGINAL\_PROFILE\_ID**</dt></span></span> </dl>                                          | <span data-ttu-id="27d8c-267">A categoria de rede da interface de chegada ou do próximo salto por meio da qual o fluxo ALE (entrada ou saída) é criado.</span><span class="sxs-lookup"><span data-stu-id="27d8c-267">The network category of the arrival or next-hop interface through which the ALE flow (inbound or outbound) is created.</span></span> <br/> <span data-ttu-id="27d8c-268">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-268">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                  |
| <span id="FWPM_CONDITION_CURRENT_PROFILE_ID"></span><span id="fwpm_condition_current_profile_id"></span><dl> <span data-ttu-id="27d8c-269"><dt>**\_ID do \_ \_ perfil atual da condição \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="27d8c-269"><dt>**FWPM\_CONDITION\_CURRENT\_PROFILE\_ID**</dt></span></span> </dl>                                             | <span data-ttu-id="27d8c-270">A categoria de rede da interface de chegada ou do próximo salto por meio da qual o pacote atual (entrada ou saída) é criado.</span><span class="sxs-lookup"><span data-stu-id="27d8c-270">The network category of the arrival or next-hop interface through which the current packet (inbound or outbound) is created.</span></span> <br/> <span data-ttu-id="27d8c-271">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-271">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                            |
| <span id="FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID"></span><span id="fwpm_condition_local_interface_profile_id"></span><dl> <span data-ttu-id="27d8c-272"><dt>**\_ID do \_ \_ perfil da interface local da condição \_ FWPM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="27d8c-272"><dt>**FWPM\_CONDITION\_LOCAL\_INTERFACE\_PROFILE\_ID**</dt></span></span> </dl>                    | <span data-ttu-id="27d8c-273">A categoria de rede da interface de entrega.</span><span class="sxs-lookup"><span data-stu-id="27d8c-273">The network category of the delivery interface.</span></span><br/> <span data-ttu-id="27d8c-274">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-274">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                          |
| <span id="FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID"></span><span id="fwpm_condition_arrival_interface_profile_id"></span><dl> <span data-ttu-id="27d8c-275"><dt>**\_ID do \_ perfil da interface de chegada da condição FWPM \_ \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="27d8c-275"><dt>**FWPM\_CONDITION\_ARRIVAL\_INTERFACE\_PROFILE\_ID**</dt></span></span> </dl>              | <span data-ttu-id="27d8c-276">A categoria de rede da interface de chegada.</span><span class="sxs-lookup"><span data-stu-id="27d8c-276">The network category of the arrival interface.</span></span><br/> <span data-ttu-id="27d8c-277">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-277">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                           |
| <span id="FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID"></span><span id="fwpm_condition_nexthop_interface_profile_id"></span><dl> <span data-ttu-id="27d8c-278"><dt>**\_ID do \_ \_ perfil da interface NEXTHOP \_ \_ do FWPM Condition**</dt></span><span class="sxs-lookup"><span data-stu-id="27d8c-278"><dt>**FWPM\_CONDITION\_NEXTHOP\_INTERFACE\_PROFILE\_ID**</dt></span></span> </dl>              | <span data-ttu-id="27d8c-279">A categoria de rede da interface de próximo salto.</span><span class="sxs-lookup"><span data-stu-id="27d8c-279">The network category of the next-hop interface.</span></span><br/> <span data-ttu-id="27d8c-280">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-280">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                          |
| <span id="FWPM_CONDITION_REAUTHORIZE_REASON"></span><span id="fwpm_condition_reauthorize_reason"></span><dl> <span data-ttu-id="27d8c-281"><dt>**\_motivo da \_ Reautorização da \_ condição FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="27d8c-281"><dt>**FWPM\_CONDITION\_REAUTHORIZE\_REASON**</dt></span></span> </dl>                                              | <span data-ttu-id="27d8c-282">O motivo para reautorizar uma conexão anteriormente autorizada.</span><span class="sxs-lookup"><span data-stu-id="27d8c-282">The reason for reauthorizing a previously authorized connection.</span></span><br/> <span data-ttu-id="27d8c-283">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-283">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                         |
| <span id="FWPM_CONDITION_ALE_REAUTH_REASON"></span><span id="fwpm_condition_ale_reauth_reason"></span><dl> <span data-ttu-id="27d8c-284"><dt>**\_motivo da \_ \_ reautenticação Ale da condição FWPM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="27d8c-284"><dt>**FWPM\_CONDITION\_ALE\_REAUTH\_REASON**</dt></span></span> </dl>                                                | <span data-ttu-id="27d8c-285">O motivo para reautorizar uma conexão anteriormente autorizada, como **fwp \_ condição de \_ reautorizar a \_ alteração da \_ política \_ de motivo** (ou um dos outros valores listados em sinalizadores de condição de [**filtragem**](filtering-condition-flags-.md)).</span><span class="sxs-lookup"><span data-stu-id="27d8c-285">The reason for reauthorizing a previously authorized connection, such as **FWP\_CONDITION\_REAUTHORIZE\_REASON\_POLICY\_CHANGE** (or one of the other values listed in [**Filtering Condition Flags**](filtering-condition-flags-.md)).</span></span><br/> <span data-ttu-id="27d8c-286">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-286">**Data type:** FWP\_UINT32</span></span><br/> |
| <span id="FWPM_CONDITION_ORIGINAL_ICMP_TYPE"></span><span id="fwpm_condition_original_icmp_type"></span><dl> <span data-ttu-id="27d8c-287"><dt>**\_tipo de \_ \_ ICMP original da condição \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="27d8c-287"><dt>**FWPM\_CONDITION\_ORIGINAL\_ICMP\_TYPE**</dt></span></span> </dl>                                             | <span data-ttu-id="27d8c-288">O tipo de ICMP com o qual o fluxo foi criado.</span><span class="sxs-lookup"><span data-stu-id="27d8c-288">The ICMP type with which the flow was created.</span></span><br/> <span data-ttu-id="27d8c-289">**Tipo de dados:** FWP \_ UINT16</span><span class="sxs-lookup"><span data-stu-id="27d8c-289">**Data type:** FWP\_UINT16</span></span><br/>                                                                                                                                                                                           |
| <span id="FWPM_CONDITION_IP_PHYSICAL_ARRIVAL_INTERFACE"></span><span id="fwpm_condition_ip_physical_arrival_interface"></span><dl> <span data-ttu-id="27d8c-290"><dt>**\_interface de \_ \_ chegada física \_ de IP de condição FWPM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="27d8c-290"><dt>**FWPM\_CONDITION\_IP\_PHYSICAL\_ARRIVAL\_INTERFACE**</dt></span></span> </dl>           | <span data-ttu-id="27d8c-291">O LUID da interface física associada ao endereço IP de chegada.</span><span class="sxs-lookup"><span data-stu-id="27d8c-291">The LUID of the physical interface associated with the arrival IP address.</span></span><br/> <span data-ttu-id="27d8c-292">**Tipo de dados:** FWP \_ UINT64</span><span class="sxs-lookup"><span data-stu-id="27d8c-292">**Data type:** FWP\_UINT64</span></span><br/>                                                                                                                                                               |
| <span id="FWPM_CONDITION_IP_PHYSICAL_NEXTHOP_INTERFACE"></span><span id="fwpm_condition_ip_physical_nexthop_interface"></span><dl> <span data-ttu-id="27d8c-293"><dt>**\_interface de \_ \_ salto físico \_ de IP de condição FWPM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="27d8c-293"><dt>**FWPM\_CONDITION\_IP\_PHYSICAL\_NEXTHOP\_INTERFACE**</dt></span></span> </dl>           | <span data-ttu-id="27d8c-294">O LUID da interface física do próximo salto.</span><span class="sxs-lookup"><span data-stu-id="27d8c-294">The LUID of the physical interface of the next hop.</span></span><br/> <span data-ttu-id="27d8c-295">**Tipo de dados:** FWP \_ UINT64</span><span class="sxs-lookup"><span data-stu-id="27d8c-295">**Data type:** FWP\_UINT64</span></span><br/>                                                                                                                                                                                      |
| <span id="FWPM_CONDITION_INTERFACE_QUARANTINE_EPOCH"></span><span id="fwpm_condition_interface_quarantine_epoch"></span><dl> <span data-ttu-id="27d8c-296"><dt>**\_época de \_ quarentena da interface de condição FWPM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="27d8c-296"><dt>**FWPM\_CONDITION\_INTERFACE\_QUARANTINE\_EPOCH**</dt></span></span> </dl>                     | <span data-ttu-id="27d8c-297">A contagem de época associada a uma interface.</span><span class="sxs-lookup"><span data-stu-id="27d8c-297">The epoch count associated with an interface.</span></span> <span data-ttu-id="27d8c-298">Reservado.</span><span class="sxs-lookup"><span data-stu-id="27d8c-298">Reserved.</span></span><br/> <span data-ttu-id="27d8c-299">**Tipo de dados:** FWP \_ UINT64</span><span class="sxs-lookup"><span data-stu-id="27d8c-299">**Data type:** FWP\_UINT64</span></span><br/>                                                                                                                                                                                  |
| <span id="FWPM_CONDITION_ALE_SIO_FIREWALL_SOCKET_PROPERTY"></span><span id="fwpm_condition_ale_sio_firewall_socket_property"></span><dl> <span data-ttu-id="27d8c-300"><dt>**\_propriedade de \_ \_ soquete do \_ Firewall \_ sio da FWPM condição Ale \_**</dt></span><span class="sxs-lookup"><span data-stu-id="27d8c-300"><dt>**FWPM\_CONDITION\_ALE\_SIO\_FIREWALL\_SOCKET\_PROPERTY**</dt></span></span> </dl> | <span data-ttu-id="27d8c-301">Reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="27d8c-301">Reserved for internal use.</span></span> <br/> <span data-ttu-id="27d8c-302">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-302">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                                              |





| <span data-ttu-id="27d8c-303">Constantes disponíveis para o Windows Vista com SP1, Windows Server 2008 e posterior</span><span class="sxs-lookup"><span data-stu-id="27d8c-303">Constants available for Windows Vista with SP1, Windows Server 2008, and later</span></span>                                                                                                                                                                           | <span data-ttu-id="27d8c-304">Descrição</span><span class="sxs-lookup"><span data-stu-id="27d8c-304">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_CONDITION_IP_ARRIVAL_INTERFACE"></span><span id="fwpm_condition_ip_arrival_interface"></span><dl> <span data-ttu-id="27d8c-305"><dt>**\_interface de \_ chegada de IP da condição FWPM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="27d8c-305"><dt>**FWPM\_CONDITION\_IP\_ARRIVAL\_INTERFACE**</dt></span></span> </dl>                       | <span data-ttu-id="27d8c-306">O LUID para a interface de rede associada ao endereço IP de chegada.</span><span class="sxs-lookup"><span data-stu-id="27d8c-306">The LUID for the network interface associated with the arrival IP address.</span></span> <br/> <span data-ttu-id="27d8c-307">**Tipo de dados:** FWP \_ UINT64</span><span class="sxs-lookup"><span data-stu-id="27d8c-307">**Data type:** FWP\_UINT64</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE"></span><span id="fwpm_condition_arrival_interface_type"></span><dl> <span data-ttu-id="27d8c-308"><dt>**\_tipo de \_ interface de chegada da condição FWPM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="27d8c-308"><dt>**FWPM\_CONDITION\_ARRIVAL\_INTERFACE\_TYPE**</dt></span></span> </dl>                 | <span data-ttu-id="27d8c-309">O tipo de interface de rede de chegada, conforme definido pela IANA (Internet Assigned Names Authority).</span><span class="sxs-lookup"><span data-stu-id="27d8c-309">The type of the arrival network interface as defined by the Internet Assigned Names Authority (IANA).</span></span> <span data-ttu-id="27d8c-310">Para obter mais informações, confira [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="27d8c-310">For more information, see [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <br/> <span data-ttu-id="27d8c-311">**Valores possíveis:** Os valores do tipo de interface listados no arquivo de cabeçalho Ipifcons. h.</span><span class="sxs-lookup"><span data-stu-id="27d8c-311">**Possible values:** The interface type values listed in the Ipifcons.h header file.</span></span><br/> <span data-ttu-id="27d8c-312">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-312">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                   |
| <span id="_FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE"></span><span id="_fwpm_condition_arrival_tunnel_type"></span><dl> <span data-ttu-id="27d8c-313"><dt>**FWPM \_ \_tipo de \_ túnel \_ de chegada de condição**</dt></span><span class="sxs-lookup"><span data-stu-id="27d8c-313"><dt> **FWPM\_CONDITION\_ARRIVAL\_TUNNEL\_TYPE**</dt></span></span> </dl>                       | <span data-ttu-id="27d8c-314">O método de encapsulamento usado por um túnel associado à interface de rede de chegada se o membro do tipo for o \_ tipo \_ Tunnel.</span><span class="sxs-lookup"><span data-stu-id="27d8c-314">The encapsulation method used by a tunnel associated with the arrival network interface if the Type member is IF\_TYPE\_TUNNEL.</span></span> <span data-ttu-id="27d8c-315">O tipo de túnel é definido pela IANA (Internet Assigned Names Authority).</span><span class="sxs-lookup"><span data-stu-id="27d8c-315">The tunnel type is defined by the Internet Assigned Names Authority (IANA).</span></span> <span data-ttu-id="27d8c-316">Para obter mais informações, confira [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="27d8c-316">For more information, see [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <br/> <span data-ttu-id="27d8c-317">**Valores possíveis:** Os valores de tipo de enumeração de tipo de túnel \_ listados no arquivo de cabeçalho ifdef. h.</span><span class="sxs-lookup"><span data-stu-id="27d8c-317">**Possible values:** The TUNNEL\_TYPE enumeration type values listed in the Ifdef.h header file.</span></span><br/> <span data-ttu-id="27d8c-318">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-318">**Data type:** FWP\_UINT32</span></span><br/> |
| <span id="FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX"></span><span id="fwpm_condition_arrival_interface_index"></span><dl> <span data-ttu-id="27d8c-319"><dt>**\_índice da \_ interface de chegada da condição FWPM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="27d8c-319"><dt>**FWPM\_CONDITION\_ARRIVAL\_INTERFACE\_INDEX**</dt></span></span> </dl>              | <span data-ttu-id="27d8c-320">O índice da interface de rede de chegada, conforme enumerado pela pilha de rede.</span><span class="sxs-lookup"><span data-stu-id="27d8c-320">The index of the arrival network interface, as enumerated by the network stack.</span></span><br/> <span data-ttu-id="27d8c-321">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-321">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_arrival_sub_interface_index"></span><dl> <span data-ttu-id="27d8c-322"><dt>**\_índice da \_ \_ \_ subinterface de chegada da condição \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="27d8c-322"><dt>**FWPM\_CONDITION\_ARRIVAL\_SUB\_INTERFACE\_INDEX**</dt></span></span> </dl> | <span data-ttu-id="27d8c-323">O índice da interface de rede de chegada, conforme enumerado pela pilha de rede.</span><span class="sxs-lookup"><span data-stu-id="27d8c-323">The index of the arrival network interface, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="27d8c-324">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-324">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="FWPM_CONDITION_LOCAL_INTERFACE_INDEX"></span><span id="fwpm_condition_local_interface_index"></span><dl> <span data-ttu-id="27d8c-325"><dt>**\_índice de \_ \_ interface local de condição \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="27d8c-325"><dt>**FWPM\_CONDITION\_LOCAL\_INTERFACE\_INDEX**</dt></span></span> </dl>                    | <span data-ttu-id="27d8c-326">O índice da interface de rede, conforme enumerado pela pilha de rede.</span><span class="sxs-lookup"><span data-stu-id="27d8c-326">The index of the network interface, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="27d8c-327">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-327">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="FWPM_CONDITION_LOCAL_INTERFACE_TYPE"></span><span id="fwpm_condition_local_interface_type"></span><dl> <span data-ttu-id="27d8c-328"><dt>**\_tipo de \_ \_ interface local da condição \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="27d8c-328"><dt>**FWPM\_CONDITION\_LOCAL\_INTERFACE\_TYPE**</dt></span></span> </dl>                       | <span data-ttu-id="27d8c-329">O tipo de interface, conforme definido pela Internet Assigned Names Authority (IANA).</span><span class="sxs-lookup"><span data-stu-id="27d8c-329">The interface type as defined by the Internet Assigned Names Authority (IANA).</span></span> <span data-ttu-id="27d8c-330">Para obter mais informações, confira [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="27d8c-330">For more information, see [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <br/> <span data-ttu-id="27d8c-331">**Valores possíveis:** Os valores do tipo de interface listados no arquivo de cabeçalho Ipifcons. h.</span><span class="sxs-lookup"><span data-stu-id="27d8c-331">**Possible values:** The interface type values listed in the Ipifcons.h header file.</span></span><br/> <span data-ttu-id="27d8c-332">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-332">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                          |
| <span id="FWPM_CONDITION_LOCAL_TUNNEL_TYPE"></span><span id="fwpm_condition_local_tunnel_type"></span><dl> <span data-ttu-id="27d8c-333"><dt>**\_tipo de \_ \_ túnel local da condição \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="27d8c-333"><dt>**FWPM\_CONDITION\_LOCAL\_TUNNEL\_TYPE**</dt></span></span> </dl>                                | <span data-ttu-id="27d8c-334">O método de encapsulamento usado por um túnel se o membro do tipo for o \_ tipo \_ Tunnel.</span><span class="sxs-lookup"><span data-stu-id="27d8c-334">The encapsulation method used by a tunnel if the Type member is IF\_TYPE\_TUNNEL.</span></span> <span data-ttu-id="27d8c-335">O tipo de túnel é definido pela IANA (Internet Assigned Names Authority).</span><span class="sxs-lookup"><span data-stu-id="27d8c-335">The tunnel type is defined by the Internet Assigned Names Authority (IANA).</span></span> <span data-ttu-id="27d8c-336">Para obter mais informações, confira [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="27d8c-336">For more information, see [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <br/> <span data-ttu-id="27d8c-337">**Valores possíveis:** Os valores de tipo de enumeração de tipo de túnel \_ listados no arquivo de cabeçalho ifdef. h.</span><span class="sxs-lookup"><span data-stu-id="27d8c-337">**Possible values:** The TUNNEL\_TYPE enumeration type values listed in the Ifdef.h header file.</span></span><br/> <span data-ttu-id="27d8c-338">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-338">**Data type:** FWP\_UINT32</span></span> <br/>                                              |





<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="27d8c-339">Constantes disponíveis para o Windows Vista e posterior</span><span class="sxs-lookup"><span data-stu-id="27d8c-339">Constants available for Windows Vista and later</span></span></th>
<th style="text-align: left;"><span data-ttu-id="27d8c-340">Descrição</span><span class="sxs-lookup"><span data-stu-id="27d8c-340">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS"></span><span id="fwpm_condition_ip_local_address"></span><dl> <span data-ttu-id="27d8c-341"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-341"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-342">O endereço IP local.</span><span class="sxs-lookup"><span data-stu-id="27d8c-342">The local IP address.</span></span> <br/> <span data-ttu-id="27d8c-343"><strong>Tipo de dados:</strong> Para um endereço IPv4</span><span class="sxs-lookup"><span data-stu-id="27d8c-343"><strong>Data type:</strong> For an IPv4 address</span></span>
<ul>
<li><span data-ttu-id="27d8c-344">FWP_V4_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="27d8c-344">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="27d8c-345">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-345">FWP_UINT32</span></span></li>
</ul>
<br/> <span data-ttu-id="27d8c-346"><strong>Tipo de dados:</strong> Para um endereço IPv6</span><span class="sxs-lookup"><span data-stu-id="27d8c-346"><strong>Data type:</strong> For an IPv6 address</span></span>
<ul>
<li><span data-ttu-id="27d8c-347">FWP_V6_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="27d8c-347">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="27d8c-348">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-348">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_ADDRESS"></span><span id="fwpm_condition_ip_remote_address"></span><dl> <span data-ttu-id="27d8c-349"><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-349"><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-350">O endereço IP remoto.</span><span class="sxs-lookup"><span data-stu-id="27d8c-350">The remote IP address.</span></span> <br/> <span data-ttu-id="27d8c-351"><strong>Tipo de dados:</strong> Para um endereço IPv4</span><span class="sxs-lookup"><span data-stu-id="27d8c-351"><strong>Data type:</strong> For an IPv4 address</span></span>
<ul>
<li><span data-ttu-id="27d8c-352">FWP_V4_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="27d8c-352">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="27d8c-353">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-353">FWP_UINT32</span></span></li>
</ul>
<br/> <span data-ttu-id="27d8c-354"><strong>Tipo de dados:</strong> Para um endereço IPv6</span><span class="sxs-lookup"><span data-stu-id="27d8c-354"><strong>Data type:</strong> For an IPv6 address</span></span>
<ul>
<li><span data-ttu-id="27d8c-355">FWP_V6_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="27d8c-355">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="27d8c-356">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-356">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_SOURCE_ADDRESS"></span><span id="fwpm_condition_ip_source_address"></span><dl> <span data-ttu-id="27d8c-357"><dt><strong>FWPM_CONDITION_IP_SOURCE_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-357"><dt><strong>FWPM_CONDITION_IP_SOURCE_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-358">O endereço IP de origem para pacotes encaminhados.</span><span class="sxs-lookup"><span data-stu-id="27d8c-358">The source IP address for forwarded packets.</span></span> <br/> <span data-ttu-id="27d8c-359"><strong>Tipo de dados:</strong> Para um endereço IPv4</span><span class="sxs-lookup"><span data-stu-id="27d8c-359"><strong>Data type:</strong> For an IPv4 address</span></span>
<ul>
<li><span data-ttu-id="27d8c-360">FWP_V4_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="27d8c-360">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="27d8c-361">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-361">FWP_UINT32</span></span></li>
</ul>
<br/> <span data-ttu-id="27d8c-362"><strong>Tipo de dados:</strong> Para um endereço IPv6</span><span class="sxs-lookup"><span data-stu-id="27d8c-362"><strong>Data type:</strong> For an IPv6 address</span></span>
<ul>
<li><span data-ttu-id="27d8c-363">FWP_V6_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="27d8c-363">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="27d8c-364">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-364">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_DESTINATION_ADDRESS"></span><span id="fwpm_condition_ip_destination_address"></span><dl> <span data-ttu-id="27d8c-365"><dt><strong>FWPM_CONDITION_IP_DESTINATION_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-365"><dt><strong>FWPM_CONDITION_IP_DESTINATION_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-366">O endereço IP de destino para pacotes encaminhados.</span><span class="sxs-lookup"><span data-stu-id="27d8c-366">The destination IP address for forwarded packets.</span></span> <br/> <span data-ttu-id="27d8c-367"><strong>Tipo de dados:</strong> Para um endereço IPv4</span><span class="sxs-lookup"><span data-stu-id="27d8c-367"><strong>Data type:</strong> For an IPv4 address</span></span>
<ul>
<li><span data-ttu-id="27d8c-368">FWP_V4_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="27d8c-368">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="27d8c-369">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-369">FWP_UINT32</span></span></li>
</ul>
<br/> <span data-ttu-id="27d8c-370"><strong>Tipo de dados:</strong> Para um endereço IPv6</span><span class="sxs-lookup"><span data-stu-id="27d8c-370"><strong>Data type:</strong> For an IPv6 address</span></span>
<ul>
<li><span data-ttu-id="27d8c-371">FWP_V6_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="27d8c-371">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="27d8c-372">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-372">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE"></span><span id="fwpm_condition_ip_local_address_type"></span><dl> <span data-ttu-id="27d8c-373"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-373"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-374">O tipo de endereço IP local.</span><span class="sxs-lookup"><span data-stu-id="27d8c-374">The local IP address type.</span></span> <br/> <span data-ttu-id="27d8c-375"><strong>Valores possíveis:</strong> Qualquer um dos seguintes <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> valores de enumeração.</span><span class="sxs-lookup"><span data-stu-id="27d8c-375"><strong>Possible values:</strong> Any of the following <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="27d8c-376">NlatUnspecified</span><span class="sxs-lookup"><span data-stu-id="27d8c-376">NlatUnspecified</span></span></li>
<li><span data-ttu-id="27d8c-377">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="27d8c-377">NlatUnicast</span></span></li>
<li><span data-ttu-id="27d8c-378">NlatAnycast</span><span class="sxs-lookup"><span data-stu-id="27d8c-378">NlatAnycast</span></span></li>
<li><span data-ttu-id="27d8c-379">NlatMulticast</span><span class="sxs-lookup"><span data-stu-id="27d8c-379">NlatMulticast</span></span></li>
<li><span data-ttu-id="27d8c-380">NlatBroadcast</span><span class="sxs-lookup"><span data-stu-id="27d8c-380">NlatBroadcast</span></span></li>
</ul>
<br/> <span data-ttu-id="27d8c-381"><strong>Tipo de dados:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="27d8c-381"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE"></span><span id="fwpm_condition_ip_destination_address_type"></span><dl> <span data-ttu-id="27d8c-382"><dt><strong>FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-382"><dt><strong>FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-383">O tipo de endereço IP de destino para pacotes encaminhados.</span><span class="sxs-lookup"><span data-stu-id="27d8c-383">The destination IP address type for forwarded packets.</span></span> <br/> <span data-ttu-id="27d8c-384"><strong>Valores possíveis:</strong> Qualquer um dos seguintes <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> valores de enumeração.</span><span class="sxs-lookup"><span data-stu-id="27d8c-384"><strong>Possible values:</strong> Any of the following <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="27d8c-385">NlatUnspecified</span><span class="sxs-lookup"><span data-stu-id="27d8c-385">NlatUnspecified</span></span></li>
<li><span data-ttu-id="27d8c-386">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="27d8c-386">NlatUnicast</span></span></li>
<li><span data-ttu-id="27d8c-387">NlatAnycast</span><span class="sxs-lookup"><span data-stu-id="27d8c-387">NlatAnycast</span></span></li>
<li><span data-ttu-id="27d8c-388">NlatMulticast</span><span class="sxs-lookup"><span data-stu-id="27d8c-388">NlatMulticast</span></span></li>
<li><span data-ttu-id="27d8c-389">NlatBroadcast</span><span class="sxs-lookup"><span data-stu-id="27d8c-389">NlatBroadcast</span></span></li>
</ul>
<br/> <span data-ttu-id="27d8c-390"><strong>Tipo de dados:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="27d8c-390"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_INTERFACE"></span><span id="fwpm_condition_ip_local_interface"></span><dl> <span data-ttu-id="27d8c-391"><dt><strong>FWPM_CONDITION_IP_LOCAL_INTERFACE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-391"><dt><strong>FWPM_CONDITION_IP_LOCAL_INTERFACE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-392">O LUID para a interface de rede associada ao endereço IP local.</span><span class="sxs-lookup"><span data-stu-id="27d8c-392">The LUID for the network interface associated with the local IP address.</span></span> <br/> <span data-ttu-id="27d8c-393"><strong>Tipo de dados:</strong> FWP_UINT64</span><span class="sxs-lookup"><span data-stu-id="27d8c-393"><strong>Data type:</strong> FWP_UINT64</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE_TYPE"></span><span id="fwpm_condition_interface_type"></span><dl> <span data-ttu-id="27d8c-394"><dt><strong>FWPM_CONDITION_INTERFACE_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-394"><dt><strong>FWPM_CONDITION_INTERFACE_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-395">O tipo de interface, conforme definido pela Internet Assigned Names Authority (IANA).</span><span class="sxs-lookup"><span data-stu-id="27d8c-395">The interface type as defined by the Internet Assigned Names Authority (IANA).</span></span> <span data-ttu-id="27d8c-396">Para obter mais informações, confira [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="27d8c-396">For more information, see [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <br/> <span data-ttu-id="27d8c-397"><strong>Valores possíveis:</strong> Os valores do tipo de interface listados no arquivo de cabeçalho Ipifcons. h.</span><span class="sxs-lookup"><span data-stu-id="27d8c-397"><strong>Possible values:</strong> The interface type values listed in the Ipifcons.h header file.</span></span><br/> <span data-ttu-id="27d8c-398"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-398"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_TUNNEL_TYPE"></span><span id="fwpm_condition_tunnel_type"></span><dl> <span data-ttu-id="27d8c-399"><dt><strong>FWPM_CONDITION_TUNNEL_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-399"><dt><strong>FWPM_CONDITION_TUNNEL_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-400">O método de encapsulamento usado por um túnel se o membro do tipo for IF_TYPE_TUNNEL.</span><span class="sxs-lookup"><span data-stu-id="27d8c-400">The encapsulation method used by a tunnel if the Type member is IF_TYPE_TUNNEL.</span></span> <span data-ttu-id="27d8c-401">O tipo de túnel é definido pela IANA (Internet Assigned Names Authority).</span><span class="sxs-lookup"><span data-stu-id="27d8c-401">The tunnel type is defined by the Internet Assigned Names Authority (IANA).</span></span> <span data-ttu-id="27d8c-402">Para obter mais informações, confira <a href="https://www.iana.org/assignments/ianaiftype-mib">https://www.iana.org/assignments/ianaiftype-mib</a>.</span><span class="sxs-lookup"><span data-stu-id="27d8c-402">For more information, see <a href="https://www.iana.org/assignments/ianaiftype-mib">https://www.iana.org/assignments/ianaiftype-mib</a>.</span></span> <br/> <span data-ttu-id="27d8c-403"><strong>Valores possíveis:</strong> Os valores de tipo de enumeração TUNNEL_TYPE listados no arquivo de cabeçalho ifdef. h.</span><span class="sxs-lookup"><span data-stu-id="27d8c-403"><strong>Possible values:</strong> The TUNNEL_TYPE enumeration type values listed in the Ifdef.h header file.</span></span><br/> <span data-ttu-id="27d8c-404"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-404"><strong>Data type:</strong> FWP_UINT32</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_FORWARD_INTERFACE"></span><span id="fwpm_condition_ip_forward_interface"></span><dl> <span data-ttu-id="27d8c-405"><dt><strong>FWPM_CONDITION_IP_FORWARD_INTERFACE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-405"><dt><strong>FWPM_CONDITION_IP_FORWARD_INTERFACE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-406">A LUID para a interface de rede na qual o pacote que está sendo encaminhado deve ser enviada.</span><span class="sxs-lookup"><span data-stu-id="27d8c-406">The LUID for the network interface on which the packet being forwarded is to be sent out.</span></span> <br/> <span data-ttu-id="27d8c-407"><strong>Tipo de dados:</strong> FWP_UINT64</span><span class="sxs-lookup"><span data-stu-id="27d8c-407"><strong>Data type:</strong> FWP_UINT64</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_PROTOCOL"></span><span id="fwpm_condition_ip_protocol"></span><dl> <span data-ttu-id="27d8c-408"><dt><strong>FWPM_CONDITION_IP_PROTOCOL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-408"><dt><strong>FWPM_CONDITION_IP_PROTOCOL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-409">O número do protocolo IP, conforme especificado no RFC 1700.</span><span class="sxs-lookup"><span data-stu-id="27d8c-409">The IP protocol number, as specified in RFC 1700.</span></span> <br/> <span data-ttu-id="27d8c-410"><strong>Tipo de dados:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="27d8c-410"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_PORT"></span><span id="fwpm_condition_ip_local_port"></span><dl> <span data-ttu-id="27d8c-411"><dt><strong>FWPM_CONDITION_IP_LOCAL_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-411"><dt><strong>FWPM_CONDITION_IP_LOCAL_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-412">O número da porta do protocolo de transporte local.</span><span class="sxs-lookup"><span data-stu-id="27d8c-412">The local transport protocol port number.</span></span><br/> <span data-ttu-id="27d8c-413"><strong>Tipo de dados:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="27d8c-413"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ICMP_TYPE"></span><span id="fwpm_condition_icmp_type"></span><dl> <span data-ttu-id="27d8c-414"><dt><strong>FWPM_CONDITION_ICMP_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-414"><dt><strong>FWPM_CONDITION_ICMP_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-415">O campo tipo de ICMP, conforme especificado no RFC 792.</span><span class="sxs-lookup"><span data-stu-id="27d8c-415">The ICMP type field, as specified in RFC 792.</span></span> <br/> <span data-ttu-id="27d8c-416"><strong>Tipo de dados:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="27d8c-416"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_PORT"></span><span id="fwpm_condition_ip_remote_port"></span><dl> <span data-ttu-id="27d8c-417"><dt><strong>FWPM_CONDITION_IP_REMOTE_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-417"><dt><strong>FWPM_CONDITION_IP_REMOTE_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-418">O número da porta do protocolo de transporte remoto.</span><span class="sxs-lookup"><span data-stu-id="27d8c-418">The remote transport protocol port number.</span></span> <br/> <span data-ttu-id="27d8c-419"><strong>Tipo de dados:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="27d8c-419"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ICMP_CODE"></span><span id="fwpm_condition_icmp_code"></span><dl> <span data-ttu-id="27d8c-420"><dt><strong>FWPM_CONDITION_ICMP_CODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-420"><dt><strong>FWPM_CONDITION_ICMP_CODE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-421">O campo de código ICMP, conforme especificado no RFC 792.</span><span class="sxs-lookup"><span data-stu-id="27d8c-421">The ICMP code field, as specified in RFC 792.</span></span> <br/> <span data-ttu-id="27d8c-422"><strong>Tipo de dados:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="27d8c-422"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE"></span><span id="fwpm_condition_embedded_local_address_type"></span><dl> <span data-ttu-id="27d8c-423"><dt><strong>FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-423"><dt><strong>FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-424">O tipo de endereço IP local que é inserido no pacote ICMP.</span><span class="sxs-lookup"><span data-stu-id="27d8c-424">The local IP address type that is embedded in the ICMP packet.</span></span><br/> <span data-ttu-id="27d8c-425"><strong>Valores possíveis:</strong> Qualquer um dos seguintes <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> valores de enumeração.</span><span class="sxs-lookup"><span data-stu-id="27d8c-425"><strong>Possible values:</strong> Any of the following <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="27d8c-426">NlatUnspecified</span><span class="sxs-lookup"><span data-stu-id="27d8c-426">NlatUnspecified</span></span></li>
<li><span data-ttu-id="27d8c-427">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="27d8c-427">NlatUnicast</span></span></li>
<li><span data-ttu-id="27d8c-428">NlatAnycast</span><span class="sxs-lookup"><span data-stu-id="27d8c-428">NlatAnycast</span></span></li>
<li><span data-ttu-id="27d8c-429">NlatMulticast</span><span class="sxs-lookup"><span data-stu-id="27d8c-429">NlatMulticast</span></span></li>
<li><span data-ttu-id="27d8c-430">NlatBroadcast</span><span class="sxs-lookup"><span data-stu-id="27d8c-430">NlatBroadcast</span></span></li>
</ul>
<br/> <span data-ttu-id="27d8c-431"><strong>Tipo de dados:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="27d8c-431"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS"></span><span id="fwpm_condition_embedded_remote_address"></span><dl> <span data-ttu-id="27d8c-432"><dt><strong>FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-432"><dt><strong>FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-433">O endereço IP remoto que é inserido no pacote ICMP.</span><span class="sxs-lookup"><span data-stu-id="27d8c-433">The remote IP address that is embedded in the ICMP packet.</span></span> <br/> <span data-ttu-id="27d8c-434"><strong>Tipo de dados:</strong> Para um endereço IPv4</span><span class="sxs-lookup"><span data-stu-id="27d8c-434"><strong>Data type:</strong> For an IPv4 address</span></span>
<ul>
<li><span data-ttu-id="27d8c-435">FWP_V4_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="27d8c-435">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="27d8c-436">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-436">FWP_UINT32</span></span></li>
</ul>
<br/> <span data-ttu-id="27d8c-437"><strong>Tipo de dados:</strong> Para um endereço IPv6</span><span class="sxs-lookup"><span data-stu-id="27d8c-437"><strong>Data type:</strong> For an IPv6 address</span></span>
<ul>
<li><span data-ttu-id="27d8c-438">FWP_V6_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="27d8c-438">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="27d8c-439">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-439">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_PROTOCOL"></span><span id="fwpm_condition_embedded_protocol"></span><dl> <span data-ttu-id="27d8c-440"><dt><strong>FWPM_CONDITION_EMBEDDED_PROTOCOL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-440"><dt><strong>FWPM_CONDITION_EMBEDDED_PROTOCOL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-441">O número do protocolo IP inserido no pacote ICMP, conforme especificado no RFC 1700.</span><span class="sxs-lookup"><span data-stu-id="27d8c-441">The IP protocol number that is embedded in the ICMP packet, as specified in RFC 1700.</span></span> <br/> <span data-ttu-id="27d8c-442"><strong>Tipo de dados:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="27d8c-442"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_LOCAL_PORT"></span><span id="fwpm_condition_embedded_local_port"></span><dl> <span data-ttu-id="27d8c-443"><dt><strong>FWPM_CONDITION_EMBEDDED_LOCAL_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-443"><dt><strong>FWPM_CONDITION_EMBEDDED_LOCAL_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-444">O número da porta do protocolo de transporte local que é inserido no pacote ICMP.</span><span class="sxs-lookup"><span data-stu-id="27d8c-444">The local transport protocol port number that is embedded in the ICMP packet.</span></span> <br/> <span data-ttu-id="27d8c-445"><strong>Tipo de dados:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="27d8c-445"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_REMOTE_PORT"></span><span id="fwpm_condition_embedded_remote_port"></span><dl> <span data-ttu-id="27d8c-446"><dt><strong>FWPM_CONDITION_EMBEDDED_REMOTE_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-446"><dt><strong>FWPM_CONDITION_EMBEDDED_REMOTE_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-447">O número da porta do protocolo de transporte remoto que é inserido no pacote ICMP.</span><span class="sxs-lookup"><span data-stu-id="27d8c-447">The remote transport protocol port number that is embedded in the ICMP packet.</span></span> <br/> <span data-ttu-id="27d8c-448"><strong>Tipo de dados:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="27d8c-448"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_FLAGS"></span><span id="fwpm_condition_flags"></span><dl> <span data-ttu-id="27d8c-449"><dt><strong>FWPM_CONDITION_FLAGS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-449"><dt><strong>FWPM_CONDITION_FLAGS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-450">Uma operação OR de uma combinação de sinalizadores de condição de filtragem.</span><span class="sxs-lookup"><span data-stu-id="27d8c-450">A bitwise OR of a combination of filtering condition flags.</span></span> <br/> <span data-ttu-id="27d8c-451"><strong>Valores possíveis:</strong> Consulte <a href="filtering-condition-flags-.md"> <strong>filtrando sinalizadores de condição</strong></a></span><span class="sxs-lookup"><span data-stu-id="27d8c-451"><strong>Possible values:</strong> See <a href="filtering-condition-flags-.md"><strong>Filtering Condition Flags</strong></a></span></span><br/> <span data-ttu-id="27d8c-452"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-452"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_DIRECTION"></span><span id="fwpm_condition_direction"></span><dl> <span data-ttu-id="27d8c-453"><dt><strong>FWPM_CONDITION_DIRECTION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-453"><dt><strong>FWPM_CONDITION_DIRECTION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-454">A direção do fluxo de tráfego ou de dados.</span><span class="sxs-lookup"><span data-stu-id="27d8c-454">The direction of the traffic or data flow.</span></span> <br/> <span data-ttu-id="27d8c-455"><strong>Valores possíveis:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="27d8c-455"><strong>Possible values:  </strong>
</span></span><ul>
<li><span data-ttu-id="27d8c-456">FWP_DIRECTION_INBOUND</span><span class="sxs-lookup"><span data-stu-id="27d8c-456">FWP_DIRECTION_INBOUND</span></span></li>
<li><span data-ttu-id="27d8c-457">FWP_DIRECTION_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="27d8c-457">FWP_DIRECTION_OUTBOUND</span></span></li>
</ul>
<br/> <span data-ttu-id="27d8c-458">Para camadas de datagrama (FWPM_LAYER_DATAGRAM_DATA_ *) e camadas de pacotes de fluxo (FWPM_LAYER_STREAM_PACKET_*), o valor será o mesmo que a direção do pacote.</span><span class="sxs-lookup"><span data-stu-id="27d8c-458">For datagram layers (FWPM_LAYER_DATAGRAM_DATA_ *) and stream packet layers (FWPM_LAYER_STREAM_PACKET_*), the value will be the same as the direction of the packet.</span></span> <br/> <span data-ttu-id="27d8c-459">Para camadas de fluxo (FWPM_LAYER_STREAM_ *) e camadas estabelecidas pelo Flow (FWPM_LAYER_ALE_FLOW_ESTABLISHED_*), o valor será o mesmo que a direção da conexão.</span><span class="sxs-lookup"><span data-stu-id="27d8c-459">For stream layers (FWPM_LAYER_STREAM_ *) and flow established layers (FWPM_LAYER_ALE_FLOW_ESTABLISHED_*), the value will be the same as direction of the connection.</span></span> <span data-ttu-id="27d8c-460">(Por exemplo, quando um aplicativo local inicia a conexão, um pacote de entrada tem <strong>FWPM_CONDITION_DIRECTION</strong> definido como <strong>FWP_DIRECTION_OUTBOUND</strong>.)</span><span class="sxs-lookup"><span data-stu-id="27d8c-460">(For example, when a local application initiates the connection, an inbound packet has <strong>FWPM_CONDITION_DIRECTION</strong> set to <strong>FWP_DIRECTION_OUTBOUND</strong>.)</span></span> <br/> <span data-ttu-id="27d8c-461"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-461"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE_INDEX"></span><span id="fwpm_condition_interface_index"></span><dl> <span data-ttu-id="27d8c-462"><dt><strong>FWPM_CONDITION_INTERFACE_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-462"><dt><strong>FWPM_CONDITION_INTERFACE_INDEX</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-463">O índice da interface de rede, conforme enumerado pela pilha de rede.</span><span class="sxs-lookup"><span data-stu-id="27d8c-463">The index of the network interface, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="27d8c-464"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-464"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_sub_interface_index"></span><dl> <span data-ttu-id="27d8c-465"><dt><strong>FWPM_CONDITION_SUB_INTERFACE_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-465"><dt><strong>FWPM_CONDITION_SUB_INTERFACE_INDEX</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-466">O índice da interface de rede lógica, conforme enumerado pela pilha de rede.</span><span class="sxs-lookup"><span data-stu-id="27d8c-466">The index of the logical network interface, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="27d8c-467"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-467"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_SOURCE_INTERFACE_INDEX"></span><span id="fwpm_condition_source_interface_index"></span><dl> <span data-ttu-id="27d8c-468"><dt><strong>FWPM_CONDITION_SOURCE_INTERFACE_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-468"><dt><strong>FWPM_CONDITION_SOURCE_INTERFACE_INDEX</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-469">O índice da interface de rede de origem para pacotes encaminhados, conforme enumerado pela pilha de rede.</span><span class="sxs-lookup"><span data-stu-id="27d8c-469">The index of the source network interface for forwarded packets, as enumerated by the network stack.</span></span><br/> <span data-ttu-id="27d8c-470"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-470"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_source_sub_interface_index"></span><dl> <span data-ttu-id="27d8c-471"><dt><strong>FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-471"><dt><strong>FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-472">O índice da interface de rede lógica de origem para pacotes encaminhados, conforme enumerado pela pilha de rede.</span><span class="sxs-lookup"><span data-stu-id="27d8c-472">The index of the source logical network interface for forwarded packets, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="27d8c-473"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-473"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_DESTINATION_INTERFACE_INDEX"></span><span id="fwpm_condition_destination_interface_index"></span><dl> <span data-ttu-id="27d8c-474"><dt><strong>FWPM_CONDITION_DESTINATION_INTERFACE_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-474"><dt><strong>FWPM_CONDITION_DESTINATION_INTERFACE_INDEX</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-475">O índice da interface de rede de destino para pacotes encaminhados, conforme enumerado pela pilha de rede.</span><span class="sxs-lookup"><span data-stu-id="27d8c-475">The index of the destination network interface for forwarded packets, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="27d8c-476"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-476"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_destination_sub_interface_index"></span><dl> <span data-ttu-id="27d8c-477"><dt><strong>FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-477"><dt><strong>FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-478">O índice da interface de rede lógica de destino para pacotes encaminhados, conforme enumerado pela pilha de rede.</span><span class="sxs-lookup"><span data-stu-id="27d8c-478">The index of the destination logical network interface for forwarded packets, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="27d8c-479"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-479"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_APP_ID"></span><span id="fwpm_condition_ale_app_id"></span><dl> <span data-ttu-id="27d8c-480"><dt><strong>FWPM_CONDITION_ALE_APP_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-480"><dt><strong>FWPM_CONDITION_ALE_APP_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-481">O caminho do dispositivo totalmente qualificado do aplicativo, conforme retornado pela função <a href="/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmgetappidfromfilename0"><strong>FwpmGetAppIdFromFileName0</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="27d8c-481">The fully qualified device path of the application, as returned by the <a href="/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmgetappidfromfilename0"><strong>FwpmGetAppIdFromFileName0</strong></a> function.</span></span> <br/> <span data-ttu-id="27d8c-482">(Por exemplo, &quot; \device0\hardiskvolume1\Program Files\Application.exe&quot; .)</span><span class="sxs-lookup"><span data-stu-id="27d8c-482">(For example, &quot;\device0\hardiskvolume1\Program Files\Application.exe&quot;.)</span></span><br/> <span data-ttu-id="27d8c-483"><strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-483"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_USER_ID"></span><span id="fwpm_condition_ale_user_id"></span><dl> <span data-ttu-id="27d8c-484"><dt><strong>FWPM_CONDITION_ALE_USER_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-484"><dt><strong>FWPM_CONDITION_ALE_USER_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-485">A identificação do usuário local.</span><span class="sxs-lookup"><span data-stu-id="27d8c-485">The identification of the local user.</span></span> <br/> <span data-ttu-id="27d8c-486"><strong>Tipo de dados:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-486"><strong>Data type:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_REMOTE_USER_ID"></span><span id="fwpm_condition_ale_remote_user_id"></span><dl> <span data-ttu-id="27d8c-487"><dt><strong>FWPM_CONDITION_ALE_REMOTE_USER_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-487"><dt><strong>FWPM_CONDITION_ALE_REMOTE_USER_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-488">A identificação do usuário remoto.</span><span class="sxs-lookup"><span data-stu-id="27d8c-488">The identification of the remote user.</span></span> <br/> <span data-ttu-id="27d8c-489"><strong>Tipo de dados:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-489"><strong>Data type:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_REMOTE_MACHINE_ID"></span><span id="fwpm_condition_ale_remote_machine_id"></span><dl> <span data-ttu-id="27d8c-490"><dt><strong>FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-490"><dt><strong>FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-491">A identificação do computador remoto.</span><span class="sxs-lookup"><span data-stu-id="27d8c-491">The identification of the remote machine.</span></span> <br/> <span data-ttu-id="27d8c-492"><strong>Tipo de dados:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-492"><strong>Data type:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_PROMISCUOUS_MODE"></span><span id="fwpm_condition_ale_promiscuous_mode"></span><dl> <span data-ttu-id="27d8c-493"><dt><strong>FWPM_CONDITION_ALE_PROMISCUOUS_MODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-493"><dt><strong>FWPM_CONDITION_ALE_PROMISCUOUS_MODE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-494">O modo de soquete bruto que é permitido ou negado.</span><span class="sxs-lookup"><span data-stu-id="27d8c-494">The raw socket mode that is allowed or denied.</span></span><br/> <span data-ttu-id="27d8c-495"><strong>Valores possíveis:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="27d8c-495"><strong>Possible values:  </strong>
</span></span><ul>
<li><span data-ttu-id="27d8c-496">SIO_RCVALL</span><span class="sxs-lookup"><span data-stu-id="27d8c-496">SIO_RCVALL</span></span></li>
<li><span data-ttu-id="27d8c-497">SIO_RCVALL_IGMPMCAST</span><span class="sxs-lookup"><span data-stu-id="27d8c-497">SIO_RCVALL_IGMPMCAST</span></span></li>
<li><span data-ttu-id="27d8c-498">SIO_RCVALL_MCAST</span><span class="sxs-lookup"><span data-stu-id="27d8c-498">SIO_RCVALL_MCAST</span></span></li>
</ul>
<span data-ttu-id="27d8c-499">Para obter uma descrição desses modos de soquete bruto, consulte a função <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl"><strong>WSAIoctl</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="27d8c-499">For a description of these raw socket modes, see the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl"><strong>WSAIoctl</strong></a> function.</span></span><br/> <span data-ttu-id="27d8c-500"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-500"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT"></span><span id="fwpm_condition_ale_sio_firewall_system_port"></span><dl> <span data-ttu-id="27d8c-501"><dt><strong>FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-501"><dt><strong>FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-502">Reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="27d8c-502">Reserved for internal use.</span></span> <br/> <span data-ttu-id="27d8c-503"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-503"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_NAP_CONTEXT"></span><span id="fwpm_condition_ale_nap_context"></span><dl> <span data-ttu-id="27d8c-504"><dt><strong>FWPM_CONDITION_ALE_NAP_CONTEXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-504"><dt><strong>FWPM_CONDITION_ALE_NAP_CONTEXT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-505">Reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="27d8c-505">Reserved for internal use.</span></span> <br/> <span data-ttu-id="27d8c-506"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-506"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
</tbody>
</table>



<span data-ttu-id="27d8c-507">As constantes a seguir estão disponíveis somente para o modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="27d8c-507">The following constants are available for user mode only.</span></span>



| <span data-ttu-id="27d8c-508">Condições de modo de usuário disponíveis para o Windows 8 e o Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="27d8c-508">User-mode conditions available for Windows 8 and Windows Server 2012</span></span>                                                                                                                       | <span data-ttu-id="27d8c-509">Descrição</span><span class="sxs-lookup"><span data-stu-id="27d8c-509">Description</span></span>                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_CONDITION_QM_MODE"></span><span id="fwpm_condition_qm_mode"></span><dl> <span data-ttu-id="27d8c-510"><dt>**\_ \_ modo QM da condição FWPM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="27d8c-510"><dt>**FWPM\_CONDITION\_QM\_MODE**</dt></span></span> </dl> | <span data-ttu-id="27d8c-511">O modo do filtro de modo rápido (QM).</span><span class="sxs-lookup"><span data-stu-id="27d8c-511">The mode of the quick mode (QM) filter.</span></span> <span data-ttu-id="27d8c-512">Consulte [**\_ \_ tipo de tráfego IPSec**](/windows/desktop/api/Ipsectypes/ne-ipsectypes-ipsec_traffic_type) para obter os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="27d8c-512">See [**IPSEC\_TRAFFIC\_TYPE**](/windows/desktop/api/Ipsectypes/ne-ipsectypes-ipsec_traffic_type) for possible values.</span></span><br/> <span data-ttu-id="27d8c-513">**Tipo de dados:** FWP \_ UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-513">**Data type:** FWP\_UINT32</span></span><br/> |





<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="27d8c-514">Condições de modo de usuário disponíveis para o Windows 7, o Windows Server 2008 R2 e posterior</span><span class="sxs-lookup"><span data-stu-id="27d8c-514">User-mode conditions available for Windows 7, Windows Server 2008 R2, and later</span></span></th>
<th style="text-align: left;"><span data-ttu-id="27d8c-515">Descrição</span><span class="sxs-lookup"><span data-stu-id="27d8c-515">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_KM_AUTH_NAP_CONTEXT"></span><span id="fwpm_condition_km_auth_nap_context"></span><dl> <span data-ttu-id="27d8c-516"><dt><strong>FWPM_CONDITION_KM_AUTH_NAP_CONTEXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-516"><dt><strong>FWPM_CONDITION_KM_AUTH_NAP_CONTEXT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-517">Reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="27d8c-517">Reserved for internal use.</span></span><br/> <span data-ttu-id="27d8c-518"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-518"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_PEER_NAME"></span><span id="fwpm_condition_peer_name"></span><dl> <span data-ttu-id="27d8c-519"><dt><strong>FWPM_CONDITION_PEER_NAME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-519"><dt><strong>FWPM_CONDITION_PEER_NAME</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-520">O nome do par.</span><span class="sxs-lookup"><span data-stu-id="27d8c-520">The name of the peer.</span></span> <span data-ttu-id="27d8c-521">Por exemplo, o nome DNS do par.</span><span class="sxs-lookup"><span data-stu-id="27d8c-521">For example, the peer's DNS name.</span></span><br/> <span data-ttu-id="27d8c-522"><strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-522"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_REMOTE_ID"></span><span id="fwpm_condition_remote_id"></span><dl> <span data-ttu-id="27d8c-523"><dt><strong>FWPM_CONDITION_REMOTE_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-523"><dt><strong>FWPM_CONDITION_REMOTE_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-524">A identidade da entidade de autenticação remota.</span><span class="sxs-lookup"><span data-stu-id="27d8c-524">The identity of the remote authentication principal.</span></span> <br/> <span data-ttu-id="27d8c-525"><strong>Tipo de dados:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-525"><strong>Data type:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_AUTHENTICATION_TYPE"></span><span id="fwpm_condition_authentication_type"></span><dl> <span data-ttu-id="27d8c-526"><dt><strong>FWPM_CONDITION_AUTHENTICATION_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-526"><dt><strong>FWPM_CONDITION_AUTHENTICATION_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-527">O tipo de método de autenticação IKE, IKEv2 ou AuthIP.</span><span class="sxs-lookup"><span data-stu-id="27d8c-527">The type of IKE, IKEv2, or AuthIP authentication method.</span></span> <br/> <span data-ttu-id="27d8c-528"><strong>Tipo de dados:</strong> IKEEXT_AUTHENTICATION_METHOD_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-528"><strong>Data type:</strong> IKEEXT_AUTHENTICATION_METHOD_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_KM_TYPE"></span><span id="fwpm_condition_km_type"></span><dl> <span data-ttu-id="27d8c-529"><dt><strong>FWPM_CONDITION_KM_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-529"><dt><strong>FWPM_CONDITION_KM_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-530">O tipo de módulo de criação de chaves.</span><span class="sxs-lookup"><span data-stu-id="27d8c-530">The type of keying module.</span></span><br/> <span data-ttu-id="27d8c-531"><strong>Tipo de dados:</strong> IKEEXT_KEY_MODULE_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-531"><strong>Data type:</strong> IKEEXT_KEY_MODULE_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_KM_MODE"></span><span id="fwpm_condition_km_mode"></span><dl> <span data-ttu-id="27d8c-532"><dt><strong>FWPM_CONDITION_KM_MODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-532"><dt><strong>FWPM_CONDITION_KM_MODE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-533">O modo IPsec no qual um token pode ser obtido.</span><span class="sxs-lookup"><span data-stu-id="27d8c-533">The IPsec mode in which a token can be obtained.</span></span><br/> <span data-ttu-id="27d8c-534"><strong>Tipo de dados:</strong> IPSEC_TOKEN_MODE</span><span class="sxs-lookup"><span data-stu-id="27d8c-534"><strong>Data type:</strong> IPSEC_TOKEN_MODE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IPSEC_POLICY_KEY"></span><span id="fwpm_condition_ipsec_policy_key"></span><dl> <span data-ttu-id="27d8c-535"><dt><strong>FWPM_CONDITION_IPSEC_POLICY_KEY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-535"><dt><strong>FWPM_CONDITION_IPSEC_POLICY_KEY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-536">A chave de contexto do provedor de política de modo principal (MM) ou de modo rápido (QM) do SA que está sendo autorizado.</span><span class="sxs-lookup"><span data-stu-id="27d8c-536">The main mode (MM) or quick mode (QM) policy provider context key of the SA being authorized.</span></span> <span data-ttu-id="27d8c-537">Útil para restringir o escopo da regra de autorização à SAs formada usando uma chave de política IPsec MM ou QM especificada.</span><span class="sxs-lookup"><span data-stu-id="27d8c-537">Useful for restricting the scope of the authorization rule to SAs formed using a specified IPsec MM or QM policy key.</span></span><br/> <span data-ttu-id="27d8c-538"><strong>Tipo de dados:</strong> FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-538"><strong>Data type:</strong> FWP_BYTE_ARRAY16_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_AUTHENTICATION_TYPE"></span><span id="fwpm_condition_authentication_type"></span><dl> <span data-ttu-id="27d8c-539"><dt><strong>FWPM_CONDITION_AUTHENTICATION_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-539"><dt><strong>FWPM_CONDITION_AUTHENTICATION_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-540">O método usado para autenticar a associação de segurança.</span><span class="sxs-lookup"><span data-stu-id="27d8c-540">The method used to authenticate the security association.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="27d8c-541">Disponível apenas no Windows Server 2008 R2, Windows 7 e posterior.</span><span class="sxs-lookup"><span data-stu-id="27d8c-541">Available only on Windows Server 2008 R2, Windows 7, and later.</span></span>
</blockquote>
<br/> <span data-ttu-id="27d8c-542"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-542"><strong>Data type:</strong> FWP_UINT32</span></span> <br/></td>
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
<th style="text-align: left;"><span data-ttu-id="27d8c-543">Constantes disponíveis para o Windows Vista e posterior</span><span class="sxs-lookup"><span data-stu-id="27d8c-543">Constants available for Windows Vista and later</span></span></th>
<th style="text-align: left;"><span data-ttu-id="27d8c-544">Descrição</span><span class="sxs-lookup"><span data-stu-id="27d8c-544">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_REMOTE_USER_TOKEN"></span><span id="fwpm_condition_remote_user_token"></span><dl> <span data-ttu-id="27d8c-545"><dt><strong>FWPM_CONDITION_REMOTE_USER_TOKEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-545"><dt><strong>FWPM_CONDITION_REMOTE_USER_TOKEN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-546">A identificação do usuário remoto.</span><span class="sxs-lookup"><span data-stu-id="27d8c-546">The identification of the remote user.</span></span><br/> <span data-ttu-id="27d8c-547"><strong>Tipo de dados:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-547"><strong>Data type:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_IF_UUID"></span><span id="fwpm_condition_rpc_if_uuid"></span><dl> <span data-ttu-id="27d8c-548"><dt><strong>FWPM_CONDITION_RPC_IF_UUID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-548"><dt><strong>FWPM_CONDITION_RPC_IF_UUID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-549">O UUID da interface RPC.</span><span class="sxs-lookup"><span data-stu-id="27d8c-549">The UUID of the RPC interface.</span></span> <br/> <span data-ttu-id="27d8c-550"><strong>Tipo de dados:</strong> FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-550"><strong>Data type:</strong> FWP_BYTE_ARRAY16_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_IF_VERSION"></span><span id="fwpm_condition_rpc_if_version"></span><dl> <span data-ttu-id="27d8c-551"><dt><strong>FWPM_CONDITION_RPC_IF_VERSION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-551"><dt><strong>FWPM_CONDITION_RPC_IF_VERSION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-552">A versão da interface RPC.</span><span class="sxs-lookup"><span data-stu-id="27d8c-552">The version of the RPC interface.</span></span> <br/> <span data-ttu-id="27d8c-553"><strong>Tipo de dados:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="27d8c-553"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_IF_FLAG"></span><span id="fwpm_condition_rpc_if_flag"></span><dl> <span data-ttu-id="27d8c-554"><dt><strong>FWPM_CONDITION_RPC_IF_FLAG</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-554"><dt><strong>FWPM_CONDITION_RPC_IF_FLAG</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-555">Reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="27d8c-555">Reserved for internal use.</span></span> <br/> <span data-ttu-id="27d8c-556"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-556"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_DCOM_APP_ID"></span><span id="fwpm_condition_dcom_app_id"></span><dl> <span data-ttu-id="27d8c-557"><dt><strong>FWPM_CONDITION_DCOM_APP_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-557"><dt><strong>FWPM_CONDITION_DCOM_APP_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-558">A identificação do aplicativo COM.</span><span class="sxs-lookup"><span data-stu-id="27d8c-558">The identification of the COM application.</span></span><br/> <span data-ttu-id="27d8c-559"><strong>Tipo de dados:</strong> FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-559"><strong>Data type:</strong> FWP_BYTE_ARRAY16_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IMAGE_NAME"></span><span id="fwpm_condition_image_name"></span><dl> <span data-ttu-id="27d8c-560"><dt><strong>FWPM_CONDITION_IMAGE_NAME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-560"><dt><strong>FWPM_CONDITION_IMAGE_NAME</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-561">O nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="27d8c-561">The name of the application.</span></span><br/> <span data-ttu-id="27d8c-562"><strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-562"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_PROTOCOL"></span><span id="fwpm_condition_rpc_protocol"></span><dl> <span data-ttu-id="27d8c-563"><dt><strong>FWPM_CONDITION_RPC_PROTOCOL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-563"><dt><strong>FWPM_CONDITION_RPC_PROTOCOL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-564">O Protocolo RPC.</span><span class="sxs-lookup"><span data-stu-id="27d8c-564">The RPC protocol.</span></span> <br/> <span data-ttu-id="27d8c-565"><strong>Valores possíveis:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="27d8c-565"><strong>Possible values:  </strong>
</span></span><ul>
<li><span data-ttu-id="27d8c-566">RPC_PROTSEQ_TCP</span><span class="sxs-lookup"><span data-stu-id="27d8c-566">RPC_PROTSEQ_TCP</span></span></li>
<li><span data-ttu-id="27d8c-567">RPC_PROTSEQ_NMP</span><span class="sxs-lookup"><span data-stu-id="27d8c-567">RPC_PROTSEQ_NMP</span></span></li>
<li><span data-ttu-id="27d8c-568">RPC_PROTSEQ_LRPC</span><span class="sxs-lookup"><span data-stu-id="27d8c-568">RPC_PROTSEQ_LRPC</span></span></li>
<li><span data-ttu-id="27d8c-569">RPC_PROTSEQ_HTTP</span><span class="sxs-lookup"><span data-stu-id="27d8c-569">RPC_PROTSEQ_HTTP</span></span></li>
</ul>
<br/> <span data-ttu-id="27d8c-570"><strong>Tipo de dados:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="27d8c-570"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_AUTH_TYPE"></span><span id="fwpm_condition_rpc_auth_type"></span><dl> <span data-ttu-id="27d8c-571"><dt><strong>FWPM_CONDITION_RPC_AUTH_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-571"><dt><strong>FWPM_CONDITION_RPC_AUTH_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-572">O tipo de serviço de autenticação.</span><span class="sxs-lookup"><span data-stu-id="27d8c-572">The authentication service type.</span></span> <span data-ttu-id="27d8c-573">Para obter mais informações sobre os tipos de serviço de autenticação, consulte <a href="/windows/desktop/Rpc/authentication-service-constants"><strong>autenticação-constantes de serviço</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="27d8c-573">For more information about authentication service types, see <a href="/windows/desktop/Rpc/authentication-service-constants"><strong>Authentication-Service Constants</strong></a>.</span></span> <br/> <span data-ttu-id="27d8c-574"><strong>Tipo de dados:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="27d8c-574"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_AUTH_LEVEL"></span><span id="fwpm_condition_rpc_auth_level"></span><dl> <span data-ttu-id="27d8c-575"><dt><strong>FWPM_CONDITION_RPC_AUTH_LEVEL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-575"><dt><strong>FWPM_CONDITION_RPC_AUTH_LEVEL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-576">O nível de serviço de autenticação.</span><span class="sxs-lookup"><span data-stu-id="27d8c-576">The authentication service level.</span></span> <span data-ttu-id="27d8c-577">Para obter mais informações sobre os níveis de serviço de autenticação, consulte <a href="/windows/desktop/Rpc/authentication-level-constants"><strong>constantes de nível de autenticação</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="27d8c-577">For more information about authentication service levels, see <a href="/windows/desktop/Rpc/authentication-level-constants"><strong>Authentication-Level Constants</strong></a>.</span></span> <br/> <span data-ttu-id="27d8c-578"><strong>Tipo de dados:</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="27d8c-578"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM"></span><span id="fwpm_condition_sec_encrypt_algorithm"></span><dl> <span data-ttu-id="27d8c-579"><dt><strong>FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-579"><dt><strong>FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-580">O algoritmo de criptografia SSPI (interface de provedor de serviço de segurança) baseado em certificado.</span><span class="sxs-lookup"><span data-stu-id="27d8c-580">The certificate based Security Service Provider Interface (SSPI) encryption algorithm.</span></span><br/> <span data-ttu-id="27d8c-581"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-581"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_SEC_KEY_SIZE"></span><span id="fwpm_condition_sec_key_size"></span><dl> <span data-ttu-id="27d8c-582"><dt><strong>FWPM_CONDITION_SEC_KEY_SIZE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-582"><dt><strong>FWPM_CONDITION_SEC_KEY_SIZE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-583">O tamanho da chave de criptografia SSPI baseada em certificado.</span><span class="sxs-lookup"><span data-stu-id="27d8c-583">The certificate based SSPI encryption key size.</span></span><br/> <span data-ttu-id="27d8c-584"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-584"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS_V4"></span><span id="fwpm_condition_ip_local_address_v4"></span><dl> <span data-ttu-id="27d8c-585"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-585"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-586">O endereço IPv4 local.</span><span class="sxs-lookup"><span data-stu-id="27d8c-586">The local IPv4 address.</span></span> <br/> <span data-ttu-id="27d8c-587"><strong>Tipo de dados:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="27d8c-587"><strong>Data type:  </strong>
</span></span><ul>
<li><span data-ttu-id="27d8c-588">FWP_V4_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="27d8c-588">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="27d8c-589">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-589">FWP_UINT32</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS_V6"></span><span id="fwpm_condition_ip_local_address_v6"></span><dl> <span data-ttu-id="27d8c-590"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-590"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-591">O endereço IPv6 local.</span><span class="sxs-lookup"><span data-stu-id="27d8c-591">The local IPv6 address.</span></span> <br/> <span data-ttu-id="27d8c-592"><strong>Tipo de dados:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="27d8c-592"><strong>Data type:  </strong>
</span></span><ul>
<li><span data-ttu-id="27d8c-593">FWP_V6_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="27d8c-593">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="27d8c-594">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-594">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_ADDRESS_V4"></span><span id="fwpm_condition_ip_remote_address_v4"></span><dl> <span data-ttu-id="27d8c-595"><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-595"><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-596">O endereço IPv4 remoto.</span><span class="sxs-lookup"><span data-stu-id="27d8c-596">The remote IPv4 address.</span></span> <br/> <span data-ttu-id="27d8c-597"><strong>Tipo de dados:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="27d8c-597"><strong>Data type:  </strong>
</span></span><ul>
<li><span data-ttu-id="27d8c-598">FWP_V4_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="27d8c-598">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="27d8c-599">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-599">FWP_UINT32</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_ADDRESS_V6"></span><span id="fwpm_condition_ip_remote_address_v6"></span><dl> <span data-ttu-id="27d8c-600"><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-600"><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-601">O endereço IPv6 remoto.</span><span class="sxs-lookup"><span data-stu-id="27d8c-601">The remote IPv6 address.</span></span> <br/> <span data-ttu-id="27d8c-602"><strong>Tipo de dados:  </strong>
</span><span class="sxs-lookup"><span data-stu-id="27d8c-602"><strong>Data type:  </strong>
</span></span><ul>
<li><span data-ttu-id="27d8c-603">FWP_V6_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="27d8c-603">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="27d8c-604">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-604">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_PIPE"></span><span id="fwpm_condition_pipe"></span><dl> <span data-ttu-id="27d8c-605"><dt><strong>FWPM_CONDITION_PIPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-605"><dt><strong>FWPM_CONDITION_PIPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-606">O nome do pipe nomeado remoto.</span><span class="sxs-lookup"><span data-stu-id="27d8c-606">The name of the remote named pipe.</span></span><br/> <span data-ttu-id="27d8c-607"><strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-607"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID"></span><span id="fwpm_condition_process_with_rpc_if_uuid"></span><dl> <span data-ttu-id="27d8c-608"><dt><strong>FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-608"><dt><strong>FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-609">O UUID do processo com a interface RPC.</span><span class="sxs-lookup"><span data-stu-id="27d8c-609">The UUID of the process with the RPC interface.</span></span><br/> <span data-ttu-id="27d8c-610"><strong>Tipo de dados:</strong> FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-610"><strong>Data type:</strong> FWP_BYTE_ARRAY16_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_EP_VALUE"></span><span id="fwpm_condition_rpc_ep_value"></span><dl> <span data-ttu-id="27d8c-611"><dt><strong>FWPM_CONDITION_RPC_EP_VALUE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-611"><dt><strong>FWPM_CONDITION_RPC_EP_VALUE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-612">Reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="27d8c-612">Reserved for internal use.</span></span><br/> <span data-ttu-id="27d8c-613"><strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-613"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_EP_FLAGS"></span><span id="fwpm_condition_rpc_ep_flags"></span><dl> <span data-ttu-id="27d8c-614"><dt><strong>FWPM_CONDITION_RPC_EP_FLAGS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-614"><dt><strong>FWPM_CONDITION_RPC_EP_FLAGS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-615">Reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="27d8c-615">Reserved for internal use.</span></span><br/> <span data-ttu-id="27d8c-616"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-616"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_CLIENT_TOKEN"></span><span id="fwpm_condition_client_token"></span><dl> <span data-ttu-id="27d8c-617"><dt><strong>FWPM_CONDITION_CLIENT_TOKEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-617"><dt><strong>FWPM_CONDITION_CLIENT_TOKEN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-618">A identificação do cliente ao usar RpcProxy.</span><span class="sxs-lookup"><span data-stu-id="27d8c-618">The identification of the client when using RpcProxy.</span></span><br/> <span data-ttu-id="27d8c-619"><strong>Tipo de dados:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-619"><strong>Data type:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_SERVER_NAME"></span><span id="fwpm_condition_rpc_server_name"></span><dl> <span data-ttu-id="27d8c-620"><dt><strong>FWPM_CONDITION_RPC_SERVER_NAME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-620"><dt><strong>FWPM_CONDITION_RPC_SERVER_NAME</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-621">O nome do servidor RPC ao usar RpcProxy.</span><span class="sxs-lookup"><span data-stu-id="27d8c-621">The name of the RPC server when using RpcProxy.</span></span><br/> <span data-ttu-id="27d8c-622"><strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-622"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_SERVER_PORT"></span><span id="fwpm_condition_rpc_server_port"></span><dl> <span data-ttu-id="27d8c-623"><dt><strong>FWPM_CONDITION_RPC_SERVER_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-623"><dt><strong>FWPM_CONDITION_RPC_SERVER_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-624">A porta no servidor RPC ao usar RpcProxy.</span><span class="sxs-lookup"><span data-stu-id="27d8c-624">The port on the RPC server when using RpcProxy.</span></span><br/> <span data-ttu-id="27d8c-625"><strong>Tipo de dados:</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="27d8c-625"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_PROXY_AUTH_TYPE"></span><span id="fwpm_condition_rpc_proxy_auth_type"></span><dl> <span data-ttu-id="27d8c-626"><dt><strong>FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-626"><dt><strong>FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-627">O tipo de serviço de autenticação de proxy RPC.</span><span class="sxs-lookup"><span data-stu-id="27d8c-627">The RPC proxy authentication service type.</span></span><br/> <span data-ttu-id="27d8c-628"><strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-628"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH"></span><span id="fwpm_condition_client_cert_key_length"></span><dl> <span data-ttu-id="27d8c-629"><dt><strong>FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-629"><dt><strong>FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-630">O comprimento da chave SSL no certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="27d8c-630">The Secure Socket Layer (SSL) key length in the client certificate.</span></span><br/> <span data-ttu-id="27d8c-631"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-631"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_CLIENT_CERT_OID"></span><span id="fwpm_condition_client_cert_oid"></span><dl> <span data-ttu-id="27d8c-632"><dt><strong>FWPM_CONDITION_CLIENT_CERT_OID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-632"><dt><strong>FWPM_CONDITION_CLIENT_CERT_OID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-633">O identificador de objeto no certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="27d8c-633">The object identifier in the client certificate.</span></span><br/> <span data-ttu-id="27d8c-634"><strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="27d8c-634"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_NET_EVENT_TYPE"></span><span id="fwpm_condition_net_event_type"></span><dl> <span data-ttu-id="27d8c-635"><dt><strong>FWPM_CONDITION_NET_EVENT_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="27d8c-635"><dt><strong>FWPM_CONDITION_NET_EVENT_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="27d8c-636">O tipo de evento de rede.</span><span class="sxs-lookup"><span data-stu-id="27d8c-636">The type of net event.</span></span><br/> <span data-ttu-id="27d8c-637"><strong>Tipo de dados:</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="27d8c-637"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="27d8c-638">Comentários</span><span class="sxs-lookup"><span data-stu-id="27d8c-638">Remarks</span></span>

<span data-ttu-id="27d8c-639">Quando os endereços IP são armazenados no \_ formato fwp UINT32 ou quando uma porta IP é armazenada no \_ formato fwp UINT16, eles são armazenados em ordem de host, não em ordem de rede.</span><span class="sxs-lookup"><span data-stu-id="27d8c-639">When IP addresses are stored in FWP\_UINT32 format or when an IP port is stored in FWP\_UINT16 format, they are stored in host-order, not network-order.</span></span>

## <a name="requirements"></a><span data-ttu-id="27d8c-640">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27d8c-640">Requirements</span></span>



| <span data-ttu-id="27d8c-641">Requisito</span><span class="sxs-lookup"><span data-stu-id="27d8c-641">Requirement</span></span> | <span data-ttu-id="27d8c-642">Valor</span><span class="sxs-lookup"><span data-stu-id="27d8c-642">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="27d8c-643">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27d8c-643">Minimum supported client</span></span><br/> | <span data-ttu-id="27d8c-644">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="27d8c-644">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="27d8c-645">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27d8c-645">Minimum supported server</span></span><br/> | <span data-ttu-id="27d8c-646">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="27d8c-646">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="27d8c-647">parâmetro</span><span class="sxs-lookup"><span data-stu-id="27d8c-647">Header</span></span><br/>                   | <dl> <span data-ttu-id="27d8c-648"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="27d8c-648"><dt>Fwpmu.h</dt></span></span> </dl> |

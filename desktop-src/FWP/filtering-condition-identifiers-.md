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
# <a name="filtering-condition-identifiers"></a>Filtrando identificadores de condição

Os identificadores de condição de filtragem da WFP (Windows Filtering Platform) são representados por um **GUID**. O tipo de dados para o valor da condição para cada condição de filtragem é especificado como um [**\_ \_ tipo de dados fwp**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type). Esses identificadores e seus tipos de dados são definidos aqui.

As condições padrão são listadas primeiro, seguidas pelas condições específicas para o modo de usuário. As condições são agrupadas por sistema operacional com suporte, para que você possa identificar facilmente quais condições têm suporte para um determinado so.

> [!Note]  
> Cada uma das condições de filtragem a seguir está disponível apenas em um subconjunto das camadas de filtragem WFP. Para obter mais informações sobre a disponibilidade de cada condição em uma determinada camada, consulte [**condições de filtragem disponíveis em cada camada de filtragem**](filtering-conditions-available-at-each-filtering-layer.md).

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Condições disponíveis para o Windows 8 e o Windows Server 2012</th>
<th style="text-align: left;">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE_MAC_ADDRESS"></span><span id="fwpm_condition_interface_mac_address"></span><dl> <dt><strong>FWPM_CONDITION_INTERFACE_MAC_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">O endereço MAC de uma interface local específica.<br/> <strong>Tipo de dados:</strong> FWP_BYTE_ARRAY6_TYPE <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_LOCAL_ADDRESS"></span><span id="fwpm_condition_mac_local_address"></span><dl> <dt><strong>FWPM_CONDITION_MAC_LOCAL_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">Endereço de destino de um quadro de entrada ou endereço de origem de um quadro de saída.<br/> <strong>Tipo de dados:</strong> FWP_BYTE_ARRAY6_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_REMOTE_ADDRESS"></span><span id="fwpm_condition_mac_remote_address"></span><dl> <dt><strong>FWPM_CONDITION_MAC_REMOTE_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">Endereço de origem de um quadro de entrada ou endereço de destino de um quadro de saída.<br/> <strong>Tipo de dados:</strong> FWP_BYTE_ARRAY6_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ETHER_TYPE"></span><span id="fwpm_condition_ether_type"></span><dl> <dt><strong>FWPM_CONDITION_ETHER_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">O tipo de dados de carga de rede Ethernet v2. (Consulte ETHERNET_TYPE_IPV4, etc. em netiodef. h.)<br/> <strong>Tipo de dados:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VLAN_ID"></span><span id="fwpm_condition_vlan_id"></span><dl> <dt><strong>FWPM_CONDITION_VLAN_ID</strong></dt> </dl></td>
<td style="text-align: left;">Os 16 bits de cabeçalho de VLAN, incluindo os campos VID, IPF e Priority de acordo com o padrão 802.1 q (consulte VLAN_TAG em netiodef. h para as posições de bitfields).<br/> <strong>Tipo de dados:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID"></span><span id="fwpm_condition_vswitch_tenant_network_id"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</strong></dt> </dl></td>
<td style="text-align: left;">Identificador exclusivo para a rede vSwitch. Não pode ser usado em conjunto com VLAN_IDs.<br/> <strong>Tipo de dados:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_NDIS_PORT"></span><span id="fwpm_condition_ndis_port"></span><dl> <dt><strong>FWPM_CONDITION_NDIS_PORT</strong></dt> </dl></td>
<td style="text-align: left;">O número da porta da porta NDIS.<br/> <strong>Tipo de dados:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_NDIS_MEDIA_TYPE"></span><span id="fwpm_condition_ndis_media_type"></span><dl> <dt><strong>FWPM_CONDITION_NDIS_MEDIA_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">O tipo de mídia da porta NDIS.<br/> <strong>Tipo de dados:</strong> FWP_UINT32<br/> <strong>Valores possíveis:</strong> Qualquer um dos <strong>NDIS_MEDIUM</strong> valores de enumeração. (Consulte Ntddndis. h.) <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE"></span><span id="fwpm_condition_ndis_physical_media_type"></span><dl> <dt><strong>FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">O tipo de mídia física da porta NDIS.<br/> <strong>Tipo de dados:</strong> FWP_UINT32<br/> <strong>Valores possíveis:</strong> Qualquer um dos <strong>NDIS_PHYSICAL_MEDIUM</strong> valores de enumeração. (Consulte Ntddndis. h.) <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_L2_FLAGS"></span><span id="fwpm_condition_l2_flags"></span><dl> <dt><strong>FWPM_CONDITION_L2_FLAGS</strong></dt> </dl></td>
<td style="text-align: left;">Uma operação OR de uma combinação de sinalizadores de condição de filtragem. <br/> <strong>Tipo de dados:</strong> FWP_UINT32<br/> <strong>Valores possíveis:  </strong>
<ul>
<li>FWP_CONDITION_L2_IS_MOBILE_BROADBAND</li>
<li>FWP_CONDITION_L2_IS_NATIVE_ETHERNET</li>
<li>FWP_CONDITION_L2_IS_WIFI</li>
<li>FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_local_address_type"></span><dl> <dt><strong>FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">O tipo de endereço do endereço local físico.<br/> <strong>Tipo de dados:</strong> FWP_UINT8<br/> <strong>Valores possíveis:</strong> Qualquer um dos seguintes <strong>DL_ADDRESS_TYPE</strong> valores de enumeração.
<ul>
<li>DlUnicast</li>
<li>DlMulticast</li>
<li>DlBroadcast</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_remote_address_type"></span><dl> <dt><strong>FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">O tipo de endereço do endereço remoto físico.<br/> <strong>Tipo de dados:</strong> FWP_UINT8<br/> <strong>Valores possíveis:</strong> Qualquer um dos seguintes <strong>DL_ADDRESS_TYPE</strong> valores de enumeração.
<ul>
<li>DlUnicast</li>
<li>DlMulticast</li>
<li>DlBroadcast</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_SOURCE_ADDRESS"></span><span id="fwpm_condition_mac_source_address"></span><dl> <dt><strong>FWPM_CONDITION_MAC_SOURCE_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">O endereço de origem físico de um quadro.<br/> <strong>Tipo de dados:</strong> FWP_BYTE_ARRAY6_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_DESTINATION_ADDRESS"></span><span id="fwpm_condition_mac_destination_address"></span><dl> <dt><strong>FWPM_CONDITION_MAC_DESTINATION_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">O endereço de destino físico de um quadro.<br/> <strong>Tipo de dados:</strong> FWP_BYTE_ARRAY6_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_source_address_type"></span><dl> <dt><strong>FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">O tipo de endereço do endereço de destino físico.<br/> <strong>Tipo de dados:</strong> FWP_UINT8<br/> <strong>Valores possíveis:</strong> Qualquer um dos seguintes <strong>DL_ADDRESS_TYPE</strong> valores de enumeração.
<ul>
<li>DlUnicast</li>
<li>DlMulticast</li>
<li>DlBroadcast</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_destination_address_type"></span><dl> <dt><strong>FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">O tipo de endereço do endereço de destino físico.<br/> <strong>Tipo de dados:</strong> FWP_UINT8<br/> <strong>Valores possíveis:</strong> Qualquer um dos seguintes <strong>DL_ADDRESS_TYPE</strong> valores de enumeração.
<ul>
<li>DlUnicast</li>
<li>DlMulticast</li>
<li>DlBroadcast</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_SOURCE_PORT"></span><span id="fwpm_condition_ip_source_port"></span><dl> <dt><strong>FWPM_CONDITION_IP_SOURCE_PORT</strong></dt> </dl></td>
<td style="text-align: left;">A porta de origem do transporte do pacote.<br/> <strong>Tipo de dados:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_ICMP_TYPE"></span><span id="fwpm_condition_vswitch_icmp_type"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_ICMP_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">O campo tipo de ICMP, conforme especificado no RFC 792.<br/> <strong>Tipo de dados:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_DESTINATION_PORT"></span><span id="fwpm_condition_ip_destination_port"></span><dl> <dt><strong>FWPM_CONDITION_IP_DESTINATION_PORT</strong></dt> </dl></td>
<td style="text-align: left;">A porta de destino do transporte do pacote.<br/> <strong>Tipo de dados:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_ICMP_CODE"></span><span id="fwpm_condition_vswitch_icmp_code"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_ICMP_CODE</strong></dt> </dl></td>
<td style="text-align: left;">O campo de código ICMP, conforme especificado no RFC 792. <br/> <strong>Tipo de dados:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_ID"></span><span id="fwpm_condition_vswitch_id"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_ID</strong></dt> </dl></td>
<td style="text-align: left;">Identificador exclusivo de uma instância de vSwitch.<br/> <strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_NETWORK_TYPE"></span><span id="fwpm_condition_vswitch_network_type"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_NETWORK_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Especifica se a instância do vSwitch faz parte de uma rede virtual externa, interna ou privada.<br/> <strong>Tipo de dados:</strong> FWP_UINT8<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID"></span><span id="fwpm_condition_vswitch_source_interface_id"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</strong></dt> </dl></td>
<td style="text-align: left;">Identificador exclusivo da origem do pacote atual. (O nome de uma VM-NIC, P-NIC ou V-NIC.)<br/> <strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID"></span><span id="fwpm_condition_vswitch_destination_interface_id"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID</strong></dt> </dl></td>
<td style="text-align: left;">Identificador exclusivo do destino do pacote atual. (O nome de uma VM-NIC, P-NIC ou V-NIC.)<br/> <strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_SOURCE_VM_ID"></span><span id="fwpm_condition_vswitch_source_vm_id"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</strong></dt> </dl></td>
<td style="text-align: left;">Identificador exclusivo da máquina virtual de origem do vSwitch.<br/> <strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_DESTINATION_VM_ID"></span><span id="fwpm_condition_vswitch_destination_vm_id"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_VM_ID</strong></dt> </dl></td>
<td style="text-align: left;">Identificador exclusivo da máquina virtual de destino do vSwitch.<br/> <strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE"></span><span id="fwpm_condition_vswitch_source_interface_type"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Tipo de interface da origem do pacote atual.<br/> <strong>Tipo de dados:</strong> FWP_UINT8<br/> <strong>Valores possíveis:  </strong>
<ul>
<li>SwitchNicSyntheticNic (quando o tipo de interface é VM-NIC)</li>
<li>SwitchNicEmulatedNic (quando o tipo de interface é VM-NIC)</li>
<li>SwitchNicPhysicalNic (quando o tipo de interface é P-NIC)</li>
<li>SwitchNicVNic (quando o tipo de interface é V-NIC, conectado à partição de host)</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE"></span><span id="fwpm_condition_vswitch_destination_interface_type"></span><dl> <dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">Tipo de interface do destino do pacote atual.<br/> <strong>Tipo de dados:</strong> FWP_UINT8<br/> <strong>Valores possíveis:  </strong>
<ul>
<li>SwitchNicSyntheticNic (quando o tipo de interface é VM-NIC)</li>
<li>SwitchNicEmulatedNic (quando o tipo de interface é VM-NIC)</li>
<li>SwitchNicPhysicalNic (quando o tipo de interface é P-NIC)</li>
<li>SwitchNicVNic (quando o tipo de interface é V-NIC, conectado à partição de host)</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE"></span><span id="fwpm_condition_interface"></span><dl> <dt><strong>FWPM_CONDITION_INTERFACE</strong></dt> </dl></td>
<td style="text-align: left;">O LUID para a interface de rede associada ao endereço IP local. <br/> <strong>Tipo de dados:</strong> FWP_UINT64<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_PACKAGE_ID"></span><span id="fwpm_condition_ale_package_id"></span><dl> <dt><strong>FWPM_CONDITION_ALE_PACKAGE_ID</strong></dt> </dl></td>
<td style="text-align: left;">O SID (identificador de segurança) de um contêiner de aplicativo.<br/> <strong>Tipo de dados:</strong> FWP_SID<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_ORIGINAL_APP_ID"></span><span id="fwpm_condition_ale_original_app_id"></span><dl> <dt><strong>FWPM_CONDITION_ALE_ORIGINAL_APP_ID</strong></dt> </dl></td>
<td style="text-align: left;">O caminho do dispositivo totalmente qualificado do aplicativo, como &quot; \device0\hardiskvolume1\Program Files\Application.exe&quot; . Quando uma conexão for redirecionada, esse será o identificador do aplicativo de origem; caso contrário, isso será o mesmo que <strong>FWPM_CONDITION_ALE_APP_ID</strong>.<br/> <strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
</tbody>
</table>





| Condições disponíveis para o Windows 7, o Windows Server 2008 R2 e posterior                                                                                                                                                                                                    | Descrição                                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_CONDITION_IP_NEXTHOP_ADDRESS"></span><span id="fwpm_condition_ip_nexthop_address"></span><dl> <dt>**\_ \_ \_ endereço IP NEXTHOP \_ da condição FWPM**</dt> </dl>                                             | O endereço IP da interface de próximo salto.<br/> **Tipo de dados:** \_Máscara de \_ endereço \_ v4 de fwp<br/>                                                                                                                                                                                        |
| <span id="FWPM_CONDITION_IP_NEXTHOP_INTERFACE"></span><span id="fwpm_condition_ip_nexthop_interface"></span><dl> <dt>**\_ \_ interface NEXTHOP de IP de condição FWPM \_ \_**</dt> </dl>                                       | A interface de próximo salto da qual o pacote será desparte. <br/> **Tipo de dados:** FWP \_ UINT64<br/>                                                                                                                                                                         |
| <span id="FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE"></span><span id="fwpm_condition_nexthop_interface_type"></span><dl> <dt>**\_tipo de \_ \_ interface NEXTHOP da condição \_ FWPM**</dt> </dl>                                 | O tipo de interface da interface de próximo salto.<br/> **Tipo de dados:** FWP \_ UINT32<br/>                                                                                                                                                                                            |
| <span id="FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE"></span><span id="fwpm_condition_nexthop_tunnel_type"></span><dl> <dt>**\_tipo de \_ \_ túnel NEXTHOP da condição \_ FWPM**</dt> </dl>                                          | O tipo de túnel da interface de próximo salto.<br/> **Tipo de dados:** FWP \_ UINT32<br/>                                                                                                                                                                                               |
| <span id="FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX"></span><span id="fwpm_condition_nexthop_interface_index"></span><dl> <dt>**\_índice da \_ \_ interface NEXTHOP da condição \_ FWPM**</dt> </dl>                              | O índice de interface da interface de próximo salto.<br/> **Tipo de dados:** FWP \_ UINT32<br/>                                                                                                                                                                                           |
| <span id="FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_nexthop_sub_interface_index"></span><dl> <dt>**\_índice de \_ sub \_ - \_ interface NEXTHOP da \_ condição FWPM**</dt> </dl>                 | O índice de subinterface da interface de próximo salto.<br/> **Tipo de dados:** FWP \_ UINT32<br/>                                                                                                                                                                                       |
| <span id="FWPM_CONDITION_ORIGINAL_PROFILE_ID"></span><span id="fwpm_condition_original_profile_id"></span><dl> <dt>**\_ID do \_ \_ perfil original da condição \_ FWPM**</dt> </dl>                                          | A categoria de rede da interface de chegada ou do próximo salto por meio da qual o fluxo ALE (entrada ou saída) é criado. <br/> **Tipo de dados:** FWP \_ UINT32<br/>                                                                                                                  |
| <span id="FWPM_CONDITION_CURRENT_PROFILE_ID"></span><span id="fwpm_condition_current_profile_id"></span><dl> <dt>**\_ID do \_ \_ perfil atual da condição \_ FWPM**</dt> </dl>                                             | A categoria de rede da interface de chegada ou do próximo salto por meio da qual o pacote atual (entrada ou saída) é criado. <br/> **Tipo de dados:** FWP \_ UINT32<br/>                                                                                                            |
| <span id="FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID"></span><span id="fwpm_condition_local_interface_profile_id"></span><dl> <dt>**\_ID do \_ \_ perfil da interface local da condição \_ FWPM \_**</dt> </dl>                    | A categoria de rede da interface de entrega.<br/> **Tipo de dados:** FWP \_ UINT32<br/>                                                                                                                                                                                          |
| <span id="FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID"></span><span id="fwpm_condition_arrival_interface_profile_id"></span><dl> <dt>**\_ID do \_ perfil da interface de chegada da condição FWPM \_ \_ \_**</dt> </dl>              | A categoria de rede da interface de chegada.<br/> **Tipo de dados:** FWP \_ UINT32<br/>                                                                                                                                                                                           |
| <span id="FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID"></span><span id="fwpm_condition_nexthop_interface_profile_id"></span><dl> <dt>**\_ID do \_ \_ perfil da interface NEXTHOP \_ \_ do FWPM Condition**</dt> </dl>              | A categoria de rede da interface de próximo salto.<br/> **Tipo de dados:** FWP \_ UINT32<br/>                                                                                                                                                                                          |
| <span id="FWPM_CONDITION_REAUTHORIZE_REASON"></span><span id="fwpm_condition_reauthorize_reason"></span><dl> <dt>**\_motivo da \_ Reautorização da \_ condição FWPM**</dt> </dl>                                              | O motivo para reautorizar uma conexão anteriormente autorizada.<br/> **Tipo de dados:** FWP \_ UINT32<br/>                                                                                                                                                                         |
| <span id="FWPM_CONDITION_ALE_REAUTH_REASON"></span><span id="fwpm_condition_ale_reauth_reason"></span><dl> <dt>**\_motivo da \_ \_ reautenticação Ale da condição FWPM \_**</dt> </dl>                                                | O motivo para reautorizar uma conexão anteriormente autorizada, como **fwp \_ condição de \_ reautorizar a \_ alteração da \_ política \_ de motivo** (ou um dos outros valores listados em sinalizadores de condição de [**filtragem**](filtering-condition-flags-.md)).<br/> **Tipo de dados:** FWP \_ UINT32<br/> |
| <span id="FWPM_CONDITION_ORIGINAL_ICMP_TYPE"></span><span id="fwpm_condition_original_icmp_type"></span><dl> <dt>**\_tipo de \_ \_ ICMP original da condição \_ FWPM**</dt> </dl>                                             | O tipo de ICMP com o qual o fluxo foi criado.<br/> **Tipo de dados:** FWP \_ UINT16<br/>                                                                                                                                                                                           |
| <span id="FWPM_CONDITION_IP_PHYSICAL_ARRIVAL_INTERFACE"></span><span id="fwpm_condition_ip_physical_arrival_interface"></span><dl> <dt>**\_interface de \_ \_ chegada física \_ de IP de condição FWPM \_**</dt> </dl>           | O LUID da interface física associada ao endereço IP de chegada.<br/> **Tipo de dados:** FWP \_ UINT64<br/>                                                                                                                                                               |
| <span id="FWPM_CONDITION_IP_PHYSICAL_NEXTHOP_INTERFACE"></span><span id="fwpm_condition_ip_physical_nexthop_interface"></span><dl> <dt>**\_interface de \_ \_ salto físico \_ de IP de condição FWPM \_**</dt> </dl>           | O LUID da interface física do próximo salto.<br/> **Tipo de dados:** FWP \_ UINT64<br/>                                                                                                                                                                                      |
| <span id="FWPM_CONDITION_INTERFACE_QUARANTINE_EPOCH"></span><span id="fwpm_condition_interface_quarantine_epoch"></span><dl> <dt>**\_época de \_ quarentena da interface de condição FWPM \_ \_**</dt> </dl>                     | A contagem de época associada a uma interface. Reservado.<br/> **Tipo de dados:** FWP \_ UINT64<br/>                                                                                                                                                                                  |
| <span id="FWPM_CONDITION_ALE_SIO_FIREWALL_SOCKET_PROPERTY"></span><span id="fwpm_condition_ale_sio_firewall_socket_property"></span><dl> <dt>**\_propriedade de \_ \_ soquete do \_ Firewall \_ sio da FWPM condição Ale \_**</dt> </dl> | Reservado para uso interno. <br/> **Tipo de dados:** FWP \_ UINT32<br/>                                                                                                                                                                                                              |





| Constantes disponíveis para o Windows Vista com SP1, Windows Server 2008 e posterior                                                                                                                                                                           | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_CONDITION_IP_ARRIVAL_INTERFACE"></span><span id="fwpm_condition_ip_arrival_interface"></span><dl> <dt>**\_interface de \_ chegada de IP da condição FWPM \_ \_**</dt> </dl>                       | O LUID para a interface de rede associada ao endereço IP de chegada. <br/> **Tipo de dados:** FWP \_ UINT64<br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE"></span><span id="fwpm_condition_arrival_interface_type"></span><dl> <dt>**\_tipo de \_ interface de chegada da condição FWPM \_ \_**</dt> </dl>                 | O tipo de interface de rede de chegada, conforme definido pela IANA (Internet Assigned Names Authority). Para obter mais informações, confira [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib). <br/> **Valores possíveis:** Os valores do tipo de interface listados no arquivo de cabeçalho Ipifcons. h.<br/> **Tipo de dados:** FWP \_ UINT32<br/>                                                                                                                   |
| <span id="_FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE"></span><span id="_fwpm_condition_arrival_tunnel_type"></span><dl> <dt>**FWPM \_ \_tipo de \_ túnel \_ de chegada de condição**</dt> </dl>                       | O método de encapsulamento usado por um túnel associado à interface de rede de chegada se o membro do tipo for o \_ tipo \_ Tunnel. O tipo de túnel é definido pela IANA (Internet Assigned Names Authority). Para obter mais informações, confira [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib). <br/> **Valores possíveis:** Os valores de tipo de enumeração de tipo de túnel \_ listados no arquivo de cabeçalho ifdef. h.<br/> **Tipo de dados:** FWP \_ UINT32<br/> |
| <span id="FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX"></span><span id="fwpm_condition_arrival_interface_index"></span><dl> <dt>**\_índice da \_ interface de chegada da condição FWPM \_ \_**</dt> </dl>              | O índice da interface de rede de chegada, conforme enumerado pela pilha de rede.<br/> **Tipo de dados:** FWP \_ UINT32<br/>                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_arrival_sub_interface_index"></span><dl> <dt>**\_índice da \_ \_ \_ subinterface de chegada da condição \_ FWPM**</dt> </dl> | O índice da interface de rede de chegada, conforme enumerado pela pilha de rede. <br/> **Tipo de dados:** FWP \_ UINT32<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="FWPM_CONDITION_LOCAL_INTERFACE_INDEX"></span><span id="fwpm_condition_local_interface_index"></span><dl> <dt>**\_índice de \_ \_ interface local de condição \_ FWPM**</dt> </dl>                    | O índice da interface de rede, conforme enumerado pela pilha de rede. <br/> **Tipo de dados:** FWP \_ UINT32<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="FWPM_CONDITION_LOCAL_INTERFACE_TYPE"></span><span id="fwpm_condition_local_interface_type"></span><dl> <dt>**\_tipo de \_ \_ interface local da condição \_ FWPM**</dt> </dl>                       | O tipo de interface, conforme definido pela Internet Assigned Names Authority (IANA). Para obter mais informações, confira [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib). <br/> **Valores possíveis:** Os valores do tipo de interface listados no arquivo de cabeçalho Ipifcons. h.<br/> **Tipo de dados:** FWP \_ UINT32<br/>                                                                                                                                          |
| <span id="FWPM_CONDITION_LOCAL_TUNNEL_TYPE"></span><span id="fwpm_condition_local_tunnel_type"></span><dl> <dt>**\_tipo de \_ \_ túnel local da condição \_ FWPM**</dt> </dl>                                | O método de encapsulamento usado por um túnel se o membro do tipo for o \_ tipo \_ Tunnel. O tipo de túnel é definido pela IANA (Internet Assigned Names Authority). Para obter mais informações, confira [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib). <br/> **Valores possíveis:** Os valores de tipo de enumeração de tipo de túnel \_ listados no arquivo de cabeçalho ifdef. h.<br/> **Tipo de dados:** FWP \_ UINT32 <br/>                                              |





<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constantes disponíveis para o Windows Vista e posterior</th>
<th style="text-align: left;">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS"></span><span id="fwpm_condition_ip_local_address"></span><dl> <dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">O endereço IP local. <br/> <strong>Tipo de dados:</strong> Para um endereço IPv4
<ul>
<li>FWP_V4_ADDR_MASK ou</li>
<li>FWP_UINT32</li>
</ul>
<br/> <strong>Tipo de dados:</strong> Para um endereço IPv6
<ul>
<li>FWP_V6_ADDR_MASK ou</li>
<li>FWP_BYTE_ARRAY16_TYPE</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_ADDRESS"></span><span id="fwpm_condition_ip_remote_address"></span><dl> <dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">O endereço IP remoto. <br/> <strong>Tipo de dados:</strong> Para um endereço IPv4
<ul>
<li>FWP_V4_ADDR_MASK ou</li>
<li>FWP_UINT32</li>
</ul>
<br/> <strong>Tipo de dados:</strong> Para um endereço IPv6
<ul>
<li>FWP_V6_ADDR_MASK ou</li>
<li>FWP_BYTE_ARRAY16_TYPE</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_SOURCE_ADDRESS"></span><span id="fwpm_condition_ip_source_address"></span><dl> <dt><strong>FWPM_CONDITION_IP_SOURCE_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">O endereço IP de origem para pacotes encaminhados. <br/> <strong>Tipo de dados:</strong> Para um endereço IPv4
<ul>
<li>FWP_V4_ADDR_MASK ou</li>
<li>FWP_UINT32</li>
</ul>
<br/> <strong>Tipo de dados:</strong> Para um endereço IPv6
<ul>
<li>FWP_V6_ADDR_MASK ou</li>
<li>FWP_BYTE_ARRAY16_TYPE</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_DESTINATION_ADDRESS"></span><span id="fwpm_condition_ip_destination_address"></span><dl> <dt><strong>FWPM_CONDITION_IP_DESTINATION_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">O endereço IP de destino para pacotes encaminhados. <br/> <strong>Tipo de dados:</strong> Para um endereço IPv4
<ul>
<li>FWP_V4_ADDR_MASK ou</li>
<li>FWP_UINT32</li>
</ul>
<br/> <strong>Tipo de dados:</strong> Para um endereço IPv6
<ul>
<li>FWP_V6_ADDR_MASK ou</li>
<li>FWP_BYTE_ARRAY16_TYPE</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE"></span><span id="fwpm_condition_ip_local_address_type"></span><dl> <dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">O tipo de endereço IP local. <br/> <strong>Valores possíveis:</strong> Qualquer um dos seguintes <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> valores de enumeração.
<ul>
<li>NlatUnspecified</li>
<li>NlatUnicast</li>
<li>NlatAnycast</li>
<li>NlatMulticast</li>
<li>NlatBroadcast</li>
</ul>
<br/> <strong>Tipo de dados:</strong> FWP_UINT8<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE"></span><span id="fwpm_condition_ip_destination_address_type"></span><dl> <dt><strong>FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">O tipo de endereço IP de destino para pacotes encaminhados. <br/> <strong>Valores possíveis:</strong> Qualquer um dos seguintes <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> valores de enumeração.
<ul>
<li>NlatUnspecified</li>
<li>NlatUnicast</li>
<li>NlatAnycast</li>
<li>NlatMulticast</li>
<li>NlatBroadcast</li>
</ul>
<br/> <strong>Tipo de dados:</strong> FWP_UINT8<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_INTERFACE"></span><span id="fwpm_condition_ip_local_interface"></span><dl> <dt><strong>FWPM_CONDITION_IP_LOCAL_INTERFACE</strong></dt> </dl></td>
<td style="text-align: left;">O LUID para a interface de rede associada ao endereço IP local. <br/> <strong>Tipo de dados:</strong> FWP_UINT64<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE_TYPE"></span><span id="fwpm_condition_interface_type"></span><dl> <dt><strong>FWPM_CONDITION_INTERFACE_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">O tipo de interface, conforme definido pela Internet Assigned Names Authority (IANA). Para obter mais informações, confira [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib). <br/> <strong>Valores possíveis:</strong> Os valores do tipo de interface listados no arquivo de cabeçalho Ipifcons. h.<br/> <strong>Tipo de dados:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_TUNNEL_TYPE"></span><span id="fwpm_condition_tunnel_type"></span><dl> <dt><strong>FWPM_CONDITION_TUNNEL_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">O método de encapsulamento usado por um túnel se o membro do tipo for IF_TYPE_TUNNEL. O tipo de túnel é definido pela IANA (Internet Assigned Names Authority). Para obter mais informações, confira <a href="https://www.iana.org/assignments/ianaiftype-mib">https://www.iana.org/assignments/ianaiftype-mib</a>. <br/> <strong>Valores possíveis:</strong> Os valores de tipo de enumeração TUNNEL_TYPE listados no arquivo de cabeçalho ifdef. h.<br/> <strong>Tipo de dados:</strong> FWP_UINT32 <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_FORWARD_INTERFACE"></span><span id="fwpm_condition_ip_forward_interface"></span><dl> <dt><strong>FWPM_CONDITION_IP_FORWARD_INTERFACE</strong></dt> </dl></td>
<td style="text-align: left;">A LUID para a interface de rede na qual o pacote que está sendo encaminhado deve ser enviada. <br/> <strong>Tipo de dados:</strong> FWP_UINT64<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_PROTOCOL"></span><span id="fwpm_condition_ip_protocol"></span><dl> <dt><strong>FWPM_CONDITION_IP_PROTOCOL</strong></dt> </dl></td>
<td style="text-align: left;">O número do protocolo IP, conforme especificado no RFC 1700. <br/> <strong>Tipo de dados:</strong> FWP_UINT8<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_PORT"></span><span id="fwpm_condition_ip_local_port"></span><dl> <dt><strong>FWPM_CONDITION_IP_LOCAL_PORT</strong></dt> </dl></td>
<td style="text-align: left;">O número da porta do protocolo de transporte local.<br/> <strong>Tipo de dados:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ICMP_TYPE"></span><span id="fwpm_condition_icmp_type"></span><dl> <dt><strong>FWPM_CONDITION_ICMP_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">O campo tipo de ICMP, conforme especificado no RFC 792. <br/> <strong>Tipo de dados:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_PORT"></span><span id="fwpm_condition_ip_remote_port"></span><dl> <dt><strong>FWPM_CONDITION_IP_REMOTE_PORT</strong></dt> </dl></td>
<td style="text-align: left;">O número da porta do protocolo de transporte remoto. <br/> <strong>Tipo de dados:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ICMP_CODE"></span><span id="fwpm_condition_icmp_code"></span><dl> <dt><strong>FWPM_CONDITION_ICMP_CODE</strong></dt> </dl></td>
<td style="text-align: left;">O campo de código ICMP, conforme especificado no RFC 792. <br/> <strong>Tipo de dados:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE"></span><span id="fwpm_condition_embedded_local_address_type"></span><dl> <dt><strong>FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">O tipo de endereço IP local que é inserido no pacote ICMP.<br/> <strong>Valores possíveis:</strong> Qualquer um dos seguintes <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> valores de enumeração.
<ul>
<li>NlatUnspecified</li>
<li>NlatUnicast</li>
<li>NlatAnycast</li>
<li>NlatMulticast</li>
<li>NlatBroadcast</li>
</ul>
<br/> <strong>Tipo de dados:</strong> FWP_UINT8<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS"></span><span id="fwpm_condition_embedded_remote_address"></span><dl> <dt><strong>FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS</strong></dt> </dl></td>
<td style="text-align: left;">O endereço IP remoto que é inserido no pacote ICMP. <br/> <strong>Tipo de dados:</strong> Para um endereço IPv4
<ul>
<li>FWP_V4_ADDR_MASK ou</li>
<li>FWP_UINT32</li>
</ul>
<br/> <strong>Tipo de dados:</strong> Para um endereço IPv6
<ul>
<li>FWP_V6_ADDR_MASK ou</li>
<li>FWP_BYTE_ARRAY16_TYPE</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_PROTOCOL"></span><span id="fwpm_condition_embedded_protocol"></span><dl> <dt><strong>FWPM_CONDITION_EMBEDDED_PROTOCOL</strong></dt> </dl></td>
<td style="text-align: left;">O número do protocolo IP inserido no pacote ICMP, conforme especificado no RFC 1700. <br/> <strong>Tipo de dados:</strong> FWP_UINT8<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_LOCAL_PORT"></span><span id="fwpm_condition_embedded_local_port"></span><dl> <dt><strong>FWPM_CONDITION_EMBEDDED_LOCAL_PORT</strong></dt> </dl></td>
<td style="text-align: left;">O número da porta do protocolo de transporte local que é inserido no pacote ICMP. <br/> <strong>Tipo de dados:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_REMOTE_PORT"></span><span id="fwpm_condition_embedded_remote_port"></span><dl> <dt><strong>FWPM_CONDITION_EMBEDDED_REMOTE_PORT</strong></dt> </dl></td>
<td style="text-align: left;">O número da porta do protocolo de transporte remoto que é inserido no pacote ICMP. <br/> <strong>Tipo de dados:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_FLAGS"></span><span id="fwpm_condition_flags"></span><dl> <dt><strong>FWPM_CONDITION_FLAGS</strong></dt> </dl></td>
<td style="text-align: left;">Uma operação OR de uma combinação de sinalizadores de condição de filtragem. <br/> <strong>Valores possíveis:</strong> Consulte <a href="filtering-condition-flags-.md"> <strong>filtrando sinalizadores de condição</strong></a><br/> <strong>Tipo de dados:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_DIRECTION"></span><span id="fwpm_condition_direction"></span><dl> <dt><strong>FWPM_CONDITION_DIRECTION</strong></dt> </dl></td>
<td style="text-align: left;">A direção do fluxo de tráfego ou de dados. <br/> <strong>Valores possíveis:  </strong>
<ul>
<li>FWP_DIRECTION_INBOUND</li>
<li>FWP_DIRECTION_OUTBOUND</li>
</ul>
<br/> Para camadas de datagrama (FWPM_LAYER_DATAGRAM_DATA_ *) e camadas de pacotes de fluxo (FWPM_LAYER_STREAM_PACKET_*), o valor será o mesmo que a direção do pacote. <br/> Para camadas de fluxo (FWPM_LAYER_STREAM_ *) e camadas estabelecidas pelo Flow (FWPM_LAYER_ALE_FLOW_ESTABLISHED_*), o valor será o mesmo que a direção da conexão. (Por exemplo, quando um aplicativo local inicia a conexão, um pacote de entrada tem <strong>FWPM_CONDITION_DIRECTION</strong> definido como <strong>FWP_DIRECTION_OUTBOUND</strong>.) <br/> <strong>Tipo de dados:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE_INDEX"></span><span id="fwpm_condition_interface_index"></span><dl> <dt><strong>FWPM_CONDITION_INTERFACE_INDEX</strong></dt> </dl></td>
<td style="text-align: left;">O índice da interface de rede, conforme enumerado pela pilha de rede. <br/> <strong>Tipo de dados:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_sub_interface_index"></span><dl> <dt><strong>FWPM_CONDITION_SUB_INTERFACE_INDEX</strong></dt> </dl></td>
<td style="text-align: left;">O índice da interface de rede lógica, conforme enumerado pela pilha de rede. <br/> <strong>Tipo de dados:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_SOURCE_INTERFACE_INDEX"></span><span id="fwpm_condition_source_interface_index"></span><dl> <dt><strong>FWPM_CONDITION_SOURCE_INTERFACE_INDEX</strong></dt> </dl></td>
<td style="text-align: left;">O índice da interface de rede de origem para pacotes encaminhados, conforme enumerado pela pilha de rede.<br/> <strong>Tipo de dados:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_source_sub_interface_index"></span><dl> <dt><strong>FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX</strong></dt> </dl></td>
<td style="text-align: left;">O índice da interface de rede lógica de origem para pacotes encaminhados, conforme enumerado pela pilha de rede. <br/> <strong>Tipo de dados:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_DESTINATION_INTERFACE_INDEX"></span><span id="fwpm_condition_destination_interface_index"></span><dl> <dt><strong>FWPM_CONDITION_DESTINATION_INTERFACE_INDEX</strong></dt> </dl></td>
<td style="text-align: left;">O índice da interface de rede de destino para pacotes encaminhados, conforme enumerado pela pilha de rede. <br/> <strong>Tipo de dados:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_destination_sub_interface_index"></span><dl> <dt><strong>FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX</strong></dt> </dl></td>
<td style="text-align: left;">O índice da interface de rede lógica de destino para pacotes encaminhados, conforme enumerado pela pilha de rede. <br/> <strong>Tipo de dados:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_APP_ID"></span><span id="fwpm_condition_ale_app_id"></span><dl> <dt><strong>FWPM_CONDITION_ALE_APP_ID</strong></dt> </dl></td>
<td style="text-align: left;">O caminho do dispositivo totalmente qualificado do aplicativo, conforme retornado pela função <a href="/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmgetappidfromfilename0"><strong>FwpmGetAppIdFromFileName0</strong></a> . <br/> (Por exemplo, &quot; \device0\hardiskvolume1\Program Files\Application.exe&quot; .)<br/> <strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_USER_ID"></span><span id="fwpm_condition_ale_user_id"></span><dl> <dt><strong>FWPM_CONDITION_ALE_USER_ID</strong></dt> </dl></td>
<td style="text-align: left;">A identificação do usuário local. <br/> <strong>Tipo de dados:</strong> FWP_SECURITY_DESCRIPTOR_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_REMOTE_USER_ID"></span><span id="fwpm_condition_ale_remote_user_id"></span><dl> <dt><strong>FWPM_CONDITION_ALE_REMOTE_USER_ID</strong></dt> </dl></td>
<td style="text-align: left;">A identificação do usuário remoto. <br/> <strong>Tipo de dados:</strong> FWP_SECURITY_DESCRIPTOR_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_REMOTE_MACHINE_ID"></span><span id="fwpm_condition_ale_remote_machine_id"></span><dl> <dt><strong>FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</strong></dt> </dl></td>
<td style="text-align: left;">A identificação do computador remoto. <br/> <strong>Tipo de dados:</strong> FWP_SECURITY_DESCRIPTOR_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_PROMISCUOUS_MODE"></span><span id="fwpm_condition_ale_promiscuous_mode"></span><dl> <dt><strong>FWPM_CONDITION_ALE_PROMISCUOUS_MODE</strong></dt> </dl></td>
<td style="text-align: left;">O modo de soquete bruto que é permitido ou negado.<br/> <strong>Valores possíveis:  </strong>
<ul>
<li>SIO_RCVALL</li>
<li>SIO_RCVALL_IGMPMCAST</li>
<li>SIO_RCVALL_MCAST</li>
</ul>
Para obter uma descrição desses modos de soquete bruto, consulte a função <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl"><strong>WSAIoctl</strong></a> .<br/> <strong>Tipo de dados:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT"></span><span id="fwpm_condition_ale_sio_firewall_system_port"></span><dl> <dt><strong>FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</strong></dt> </dl></td>
<td style="text-align: left;">Reservado para uso interno. <br/> <strong>Tipo de dados:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_NAP_CONTEXT"></span><span id="fwpm_condition_ale_nap_context"></span><dl> <dt><strong>FWPM_CONDITION_ALE_NAP_CONTEXT</strong></dt> </dl></td>
<td style="text-align: left;">Reservado para uso interno. <br/> <strong>Tipo de dados:</strong> FWP_UINT32<br/></td>
</tr>
</tbody>
</table>



As constantes a seguir estão disponíveis somente para o modo de usuário.



| Condições de modo de usuário disponíveis para o Windows 8 e o Windows Server 2012                                                                                                                       | Descrição                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_CONDITION_QM_MODE"></span><span id="fwpm_condition_qm_mode"></span><dl> <dt>**\_ \_ modo QM da condição FWPM \_**</dt> </dl> | O modo do filtro de modo rápido (QM). Consulte [**\_ \_ tipo de tráfego IPSec**](/windows/desktop/api/Ipsectypes/ne-ipsectypes-ipsec_traffic_type) para obter os valores possíveis.<br/> **Tipo de dados:** FWP \_ UINT32<br/> |





<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Condições de modo de usuário disponíveis para o Windows 7, o Windows Server 2008 R2 e posterior</th>
<th style="text-align: left;">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_KM_AUTH_NAP_CONTEXT"></span><span id="fwpm_condition_km_auth_nap_context"></span><dl> <dt><strong>FWPM_CONDITION_KM_AUTH_NAP_CONTEXT</strong></dt> </dl></td>
<td style="text-align: left;">Reservado para uso interno.<br/> <strong>Tipo de dados:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_PEER_NAME"></span><span id="fwpm_condition_peer_name"></span><dl> <dt><strong>FWPM_CONDITION_PEER_NAME</strong></dt> </dl></td>
<td style="text-align: left;">O nome do par. Por exemplo, o nome DNS do par.<br/> <strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_REMOTE_ID"></span><span id="fwpm_condition_remote_id"></span><dl> <dt><strong>FWPM_CONDITION_REMOTE_ID</strong></dt> </dl></td>
<td style="text-align: left;">A identidade da entidade de autenticação remota. <br/> <strong>Tipo de dados:</strong> FWP_SECURITY_DESCRIPTOR_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_AUTHENTICATION_TYPE"></span><span id="fwpm_condition_authentication_type"></span><dl> <dt><strong>FWPM_CONDITION_AUTHENTICATION_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">O tipo de método de autenticação IKE, IKEv2 ou AuthIP. <br/> <strong>Tipo de dados:</strong> IKEEXT_AUTHENTICATION_METHOD_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_KM_TYPE"></span><span id="fwpm_condition_km_type"></span><dl> <dt><strong>FWPM_CONDITION_KM_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">O tipo de módulo de criação de chaves.<br/> <strong>Tipo de dados:</strong> IKEEXT_KEY_MODULE_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_KM_MODE"></span><span id="fwpm_condition_km_mode"></span><dl> <dt><strong>FWPM_CONDITION_KM_MODE</strong></dt> </dl></td>
<td style="text-align: left;">O modo IPsec no qual um token pode ser obtido.<br/> <strong>Tipo de dados:</strong> IPSEC_TOKEN_MODE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IPSEC_POLICY_KEY"></span><span id="fwpm_condition_ipsec_policy_key"></span><dl> <dt><strong>FWPM_CONDITION_IPSEC_POLICY_KEY</strong></dt> </dl></td>
<td style="text-align: left;">A chave de contexto do provedor de política de modo principal (MM) ou de modo rápido (QM) do SA que está sendo autorizado. Útil para restringir o escopo da regra de autorização à SAs formada usando uma chave de política IPsec MM ou QM especificada.<br/> <strong>Tipo de dados:</strong> FWP_BYTE_ARRAY16_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_AUTHENTICATION_TYPE"></span><span id="fwpm_condition_authentication_type"></span><dl> <dt><strong>FWPM_CONDITION_AUTHENTICATION_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">O método usado para autenticar a associação de segurança.<br/>
<blockquote>
[!Note]<br />
Disponível apenas no Windows Server 2008 R2, Windows 7 e posterior.
</blockquote>
<br/> <strong>Tipo de dados:</strong> FWP_UINT32 <br/></td>
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
<th style="text-align: left;">Constantes disponíveis para o Windows Vista e posterior</th>
<th style="text-align: left;">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_REMOTE_USER_TOKEN"></span><span id="fwpm_condition_remote_user_token"></span><dl> <dt><strong>FWPM_CONDITION_REMOTE_USER_TOKEN</strong></dt> </dl></td>
<td style="text-align: left;">A identificação do usuário remoto.<br/> <strong>Tipo de dados:</strong> FWP_SECURITY_DESCRIPTOR_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_IF_UUID"></span><span id="fwpm_condition_rpc_if_uuid"></span><dl> <dt><strong>FWPM_CONDITION_RPC_IF_UUID</strong></dt> </dl></td>
<td style="text-align: left;">O UUID da interface RPC. <br/> <strong>Tipo de dados:</strong> FWP_BYTE_ARRAY16_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_IF_VERSION"></span><span id="fwpm_condition_rpc_if_version"></span><dl> <dt><strong>FWPM_CONDITION_RPC_IF_VERSION</strong></dt> </dl></td>
<td style="text-align: left;">A versão da interface RPC. <br/> <strong>Tipo de dados:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_IF_FLAG"></span><span id="fwpm_condition_rpc_if_flag"></span><dl> <dt><strong>FWPM_CONDITION_RPC_IF_FLAG</strong></dt> </dl></td>
<td style="text-align: left;">Reservado para uso interno. <br/> <strong>Tipo de dados:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_DCOM_APP_ID"></span><span id="fwpm_condition_dcom_app_id"></span><dl> <dt><strong>FWPM_CONDITION_DCOM_APP_ID</strong></dt> </dl></td>
<td style="text-align: left;">A identificação do aplicativo COM.<br/> <strong>Tipo de dados:</strong> FWP_BYTE_ARRAY16_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IMAGE_NAME"></span><span id="fwpm_condition_image_name"></span><dl> <dt><strong>FWPM_CONDITION_IMAGE_NAME</strong></dt> </dl></td>
<td style="text-align: left;">O nome do aplicativo.<br/> <strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_PROTOCOL"></span><span id="fwpm_condition_rpc_protocol"></span><dl> <dt><strong>FWPM_CONDITION_RPC_PROTOCOL</strong></dt> </dl></td>
<td style="text-align: left;">O Protocolo RPC. <br/> <strong>Valores possíveis:  </strong>
<ul>
<li>RPC_PROTSEQ_TCP</li>
<li>RPC_PROTSEQ_NMP</li>
<li>RPC_PROTSEQ_LRPC</li>
<li>RPC_PROTSEQ_HTTP</li>
</ul>
<br/> <strong>Tipo de dados:</strong> FWP_UINT8<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_AUTH_TYPE"></span><span id="fwpm_condition_rpc_auth_type"></span><dl> <dt><strong>FWPM_CONDITION_RPC_AUTH_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">O tipo de serviço de autenticação. Para obter mais informações sobre os tipos de serviço de autenticação, consulte <a href="/windows/desktop/Rpc/authentication-service-constants"><strong>autenticação-constantes de serviço</strong></a>. <br/> <strong>Tipo de dados:</strong> FWP_UINT8<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_AUTH_LEVEL"></span><span id="fwpm_condition_rpc_auth_level"></span><dl> <dt><strong>FWPM_CONDITION_RPC_AUTH_LEVEL</strong></dt> </dl></td>
<td style="text-align: left;">O nível de serviço de autenticação. Para obter mais informações sobre os níveis de serviço de autenticação, consulte <a href="/windows/desktop/Rpc/authentication-level-constants"><strong>constantes de nível de autenticação</strong></a>. <br/> <strong>Tipo de dados:</strong> FWP_UINT8<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM"></span><span id="fwpm_condition_sec_encrypt_algorithm"></span><dl> <dt><strong>FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</strong></dt> </dl></td>
<td style="text-align: left;">O algoritmo de criptografia SSPI (interface de provedor de serviço de segurança) baseado em certificado.<br/> <strong>Tipo de dados:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_SEC_KEY_SIZE"></span><span id="fwpm_condition_sec_key_size"></span><dl> <dt><strong>FWPM_CONDITION_SEC_KEY_SIZE</strong></dt> </dl></td>
<td style="text-align: left;">O tamanho da chave de criptografia SSPI baseada em certificado.<br/> <strong>Tipo de dados:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS_V4"></span><span id="fwpm_condition_ip_local_address_v4"></span><dl> <dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</strong></dt> </dl></td>
<td style="text-align: left;">O endereço IPv4 local. <br/> <strong>Tipo de dados:  </strong>
<ul>
<li>FWP_V4_ADDR_MASK ou</li>
<li>FWP_UINT32</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS_V6"></span><span id="fwpm_condition_ip_local_address_v6"></span><dl> <dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</strong></dt> </dl></td>
<td style="text-align: left;">O endereço IPv6 local. <br/> <strong>Tipo de dados:  </strong>
<ul>
<li>FWP_V6_ADDR_MASK ou</li>
<li>FWP_BYTE_ARRAY16_TYPE</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_ADDRESS_V4"></span><span id="fwpm_condition_ip_remote_address_v4"></span><dl> <dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</strong></dt> </dl></td>
<td style="text-align: left;">O endereço IPv4 remoto. <br/> <strong>Tipo de dados:  </strong>
<ul>
<li>FWP_V4_ADDR_MASK ou</li>
<li>FWP_UINT32</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_ADDRESS_V6"></span><span id="fwpm_condition_ip_remote_address_v6"></span><dl> <dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</strong></dt> </dl></td>
<td style="text-align: left;">O endereço IPv6 remoto. <br/> <strong>Tipo de dados:  </strong>
<ul>
<li>FWP_V6_ADDR_MASK ou</li>
<li>FWP_BYTE_ARRAY16_TYPE</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_PIPE"></span><span id="fwpm_condition_pipe"></span><dl> <dt><strong>FWPM_CONDITION_PIPE</strong></dt> </dl></td>
<td style="text-align: left;">O nome do pipe nomeado remoto.<br/> <strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID"></span><span id="fwpm_condition_process_with_rpc_if_uuid"></span><dl> <dt><strong>FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID</strong></dt> </dl></td>
<td style="text-align: left;">O UUID do processo com a interface RPC.<br/> <strong>Tipo de dados:</strong> FWP_BYTE_ARRAY16_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_EP_VALUE"></span><span id="fwpm_condition_rpc_ep_value"></span><dl> <dt><strong>FWPM_CONDITION_RPC_EP_VALUE</strong></dt> </dl></td>
<td style="text-align: left;">Reservado para uso interno.<br/> <strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_EP_FLAGS"></span><span id="fwpm_condition_rpc_ep_flags"></span><dl> <dt><strong>FWPM_CONDITION_RPC_EP_FLAGS</strong></dt> </dl></td>
<td style="text-align: left;">Reservado para uso interno.<br/> <strong>Tipo de dados:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_CLIENT_TOKEN"></span><span id="fwpm_condition_client_token"></span><dl> <dt><strong>FWPM_CONDITION_CLIENT_TOKEN</strong></dt> </dl></td>
<td style="text-align: left;">A identificação do cliente ao usar RpcProxy.<br/> <strong>Tipo de dados:</strong> FWP_SECURITY_DESCRIPTOR_TYPE<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_SERVER_NAME"></span><span id="fwpm_condition_rpc_server_name"></span><dl> <dt><strong>FWPM_CONDITION_RPC_SERVER_NAME</strong></dt> </dl></td>
<td style="text-align: left;">O nome do servidor RPC ao usar RpcProxy.<br/> <strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_SERVER_PORT"></span><span id="fwpm_condition_rpc_server_port"></span><dl> <dt><strong>FWPM_CONDITION_RPC_SERVER_PORT</strong></dt> </dl></td>
<td style="text-align: left;">A porta no servidor RPC ao usar RpcProxy.<br/> <strong>Tipo de dados:</strong> FWP_UINT16<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_PROXY_AUTH_TYPE"></span><span id="fwpm_condition_rpc_proxy_auth_type"></span><dl> <dt><strong>FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">O tipo de serviço de autenticação de proxy RPC.<br/> <strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH"></span><span id="fwpm_condition_client_cert_key_length"></span><dl> <dt><strong>FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</strong></dt> </dl></td>
<td style="text-align: left;">O comprimento da chave SSL no certificado do cliente.<br/> <strong>Tipo de dados:</strong> FWP_UINT32<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_CLIENT_CERT_OID"></span><span id="fwpm_condition_client_cert_oid"></span><dl> <dt><strong>FWPM_CONDITION_CLIENT_CERT_OID</strong></dt> </dl></td>
<td style="text-align: left;">O identificador de objeto no certificado do cliente.<br/> <strong>Tipo de dados:</strong> FWP_BYTE_BLOB_TYPE<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_NET_EVENT_TYPE"></span><span id="fwpm_condition_net_event_type"></span><dl> <dt><strong>FWPM_CONDITION_NET_EVENT_TYPE</strong></dt> </dl></td>
<td style="text-align: left;">O tipo de evento de rede.<br/> <strong>Tipo de dados:</strong> FWP_UINT32<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Comentários

Quando os endereços IP são armazenados no \_ formato fwp UINT32 ou quando uma porta IP é armazenada no \_ formato fwp UINT16, eles são armazenados em ordem de host, não em ordem de rede.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Fwpmu. h</dt> </dl> |

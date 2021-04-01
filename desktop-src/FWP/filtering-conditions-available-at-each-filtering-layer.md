---
title: Condições de filtragem disponíveis em cada camada de filtragem (Fwpmu. h)
description: O mecanismo de filtro da WFP (plataforma de filtragem do Windows) dá suporte a um conjunto diferente de condições de filtragem em cada uma de suas camadas de filtragem.
ms.assetid: 6faace21-44ec-49dd-8e77-e403c258c14a
topic_type:
- apiref
api_name:
- FWPM_LAYER_INBOUND_IPPACKET_V4 / FWPM_LAYER_INBOUND_IPPACKET_V4_DISCARD / FWPM_LAYER_INBOUND_IPPACKET_V6 / FWPM_LAYER_INBOUND_IPPACKET_V6_DISCARD
- FWPM_LAYER_OUTBOUND_IPPACKET_V4 / FWPM_LAYER_OUTBOUND_IPPACKET_V4_DISCARD / FWPM_LAYER_OUTBOUND_IPPACKET_V6 / FWPM_LAYER_OUTBOUND_IPPACKET_V6_DISCARD
- FWPM_LAYER_IPFORWARD_V4 / FWPM_LAYER_IPFORWARD_V4_DISCARD / FWPM_LAYER_IPFORWARD_V6 / FWPM_LAYER_IPFORWARD_V6_DISCARD
- FWPM_LAYER_INBOUND_TRANSPORT_V4 / FWPM_LAYER_INBOUND_TRANSPORT_V4_DISCARD / FWPM_LAYER_INBOUND_TRANSPORT_V6 / FWPM_LAYER_INBOUND_TRANSPORT_V6_DISCARD
- FWPM_LAYER_OUTBOUND_TRANSPORT_V4 / FWPM_LAYER_OUTBOUND_TRANSPORT_V4_DISCARD / FWPM_LAYER_OUTBOUND_TRANSPORT_V6 / FWPM_LAYER_OUTBOUND_TRANSPORT_V6_DISCARD
- FWPM_LAYER_STREAM_V4 / FWPM_LAYER_STREAM_V4_DISCARD / FWPM_LAYER_STREAM_V6 / FWPM_LAYER_STREAM_V6_DISCARD
- FWPM_LAYER_DATAGRAM_DATA_V4 / FWPM_LAYER_DATAGRAM_DATA_V4_DISCARD / FWPM_LAYER_DATAGRAM_DATA_V6 / FWPM_LAYER_DATAGRAM_DATA_V6_DISCARD
- FWPM_LAYER_STREAM_PACKET V4 / FWPM_LAYER_STREAM_PACKET V6
- FWPM_LAYER_INBOUND_ICMP_ERROR_V4 / FWPM_LAYER_INBOUND_ICMP_ERROR_V4_DISCARD / FWPM_LAYER_INBOUND_ICMP_ERROR_V6 / FWPM_LAYER_INBOUND_ICMP_ERROR_V6_DISCARD
- FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4 / FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4_DISCARD / FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6 / FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6_DISCARD
- FWPM_LAYER_ALE_BIND_REDIRECT_V4 / FWPM_LAYER_ALE_BIND_REDIRECT V6
- FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4 / FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4_DISCARD / FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6 / FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6_DISCARD
- FWPM_LAYER_ALE_RESOURCE_RELEASE_V4 / FWPM_LAYER_ALE_RESOURCE_RELEASE_V6
- FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V4 / FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V6
- FWPM_LAYER_ALE_AUTH_LISTEN_V4 / FWPM_LAYER_ALE_AUTH_LISTEN_V4_DISCARD / FWPM_LAYER_ALE_AUTH_LISTEN_V6 / FWPM_LAYER_ALE_AUTH_LISTEN_V6_DISCARD
- FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4 / FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4_DISCARD / FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6 / FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6_DISCARD
- FWPM_LAYER_ALE_CONNECT_REDIRECT_V4 / FWPM_LAYER_ALE_CONNECT_REDIRECT V6
- FWPM_LAYER_ALE_AUTH_CONNECT_V4 / FWPM_LAYER_ALE_AUTH_CONNECT_V4_DISCARD / FWPM_LAYER_ALE_AUTH_CONNECT_V6 / FWPM_LAYER_ALE_AUTH_CONNECT_V6_DISCARD
- FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4 / FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4_DISCARD / FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6 / FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6_DISCARD
- FWPM_LAYER_NAME_RESOLUTION_CACHE_V4 / FWPM_LAYER_NAME_RESOLUTION_CACHE_V6
- FWPM_LAYER_IPSEC_KM_DEMUX_V4 / FWPM_LAYER_IPSEC_KM_DEMUX_V6
- FWPM_LAYER_IPSEC_V4 / FWPM_LAYER_IPSEC_V6
- FWPM_LAYER_IKEEXT_V4 / FWPM_LAYER_IKEEXT_V6
- FWPM_LAYER_RPC_UM
- FWPM_LAYER_RPC_EPMAP
- FWPM_LAYER_RPC_EP_ADD
- FWPM_LAYER_RPC_PROXY_CONN
- FWPM_LAYER_RPC_PROXY_IF
- FWPM_LAYER_KM_AUTHORIZATION
- FWPM_LAYER_INBOUND_MAC_FRAME_ETHERNET / FWPM_LAYER_OUTBOUND_MAC_FRAME_ETHERNET
- FWPM_LAYER_INBOUND_MAC_FRAME_NATIVE / FWPM_LAYER_OUTBOUND_MAC_FRAME_NATIVE
- FWPM_LAYER_EGRESS_VSWITCH_ETHERNET / FWPM_LAYER_INGRESS_VSWITCH_ETHERNET
- FWPM_LAYER_EGRESS_VSWITCH_TRANSPORT_V4 / FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V4 / FWPM_LAYER_EGRESSVSWITCH_TRANSPORT_V6 / FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V6
api_location:
- Fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd0c3806c7c3c7a5fa7f10af0e5e11c212bd93e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103917976"
---
# <a name="filtering-conditions-available-at-each-filtering-layer"></a><span data-ttu-id="ac051-103">Condições de filtragem disponíveis em cada camada de filtragem</span><span class="sxs-lookup"><span data-stu-id="ac051-103">Filtering Conditions Available at Each Filtering Layer</span></span>

<span data-ttu-id="ac051-104">O mecanismo de filtro da WFP (plataforma de filtragem do Windows) dá suporte a um conjunto diferente de condições de filtragem em cada uma de suas camadas de filtragem.</span><span class="sxs-lookup"><span data-stu-id="ac051-104">The Windows Filtering Platform (WFP) filter engine supports a different set of filtering conditions at each of its filtering layers.</span></span>

<span data-ttu-id="ac051-105">A lista de condições de filtragem que estão disponíveis em cada camada são as seguintes.</span><span class="sxs-lookup"><span data-stu-id="ac051-105">The list of filtering conditions that are available at each layer are as follows.</span></span>

## <a name="fwpm_layer_inbound_ippacket_v4--fwpm_layer_inbound_ippacket_v4_discard--fwpm_layer_inbound_ippacket_v6--fwpm_layer_inbound_ippacket_v6_discard"></a><span data-ttu-id="ac051-106">FWPM_LAYER_INBOUND_IPPACKET_V4/FWPM_LAYER_INBOUND_IPPACKET_V4_DISCARD/FWPM_LAYER_INBOUND_IPPACKET_V6/FWPM_LAYER_INBOUND_IPPACKET_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="ac051-106">FWPM_LAYER_INBOUND_IPPACKET_V4 / FWPM_LAYER_INBOUND_IPPACKET_V4_DISCARD / FWPM_LAYER_INBOUND_IPPACKET_V6 / FWPM_LAYER_INBOUND_IPPACKET_V6_DISCARD</span></span>
- <span data-ttu-id="ac051-107">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="ac051-107">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="ac051-108">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="ac051-108">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="ac051-109">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-109">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="ac051-110">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-110">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="ac051-111">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-111">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="ac051-112">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="ac051-112">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="ac051-113">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-113">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="ac051-114">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="ac051-114">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="ac051-115">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-115">FWPM_CONDITION_TUNNEL_TYPE</span></span>
## <a name="fwpm_layer_outbound_ippacket_v4--fwpm_layer_outbound_ippacket_v4_discard--fwpm_layer_outbound_ippacket_v6--fwpm_layer_outbound_ippacket_v6_discard"></a><span data-ttu-id="ac051-116">FWPM_LAYER_OUTBOUND_IPPACKET_V4/FWPM_LAYER_OUTBOUND_IPPACKET_V4_DISCARD/FWPM_LAYER_OUTBOUND_IPPACKET_V6/FWPM_LAYER_OUTBOUND_IPPACKET_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="ac051-116">FWPM_LAYER_OUTBOUND_IPPACKET_V4 / FWPM_LAYER_OUTBOUND_IPPACKET_V4_DISCARD / FWPM_LAYER_OUTBOUND_IPPACKET_V6 / FWPM_LAYER_OUTBOUND_IPPACKET_V6_DISCARD</span></span>
- <span data-ttu-id="ac051-117">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="ac051-117">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="ac051-118">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="ac051-118">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="ac051-119">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-119">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="ac051-120">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-120">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="ac051-121">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-121">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="ac051-122">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="ac051-122">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="ac051-123">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-123">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="ac051-124">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="ac051-124">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="ac051-125">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-125">FWPM_CONDITION_TUNNEL_TYPE</span></span>
## <a name="fwpm_layer_ipforward_v4--fwpm_layer_ipforward_v4_discard--fwpm_layer_ipforward_v6--fwpm_layer_ipforward_v6_discard"></a><span data-ttu-id="ac051-126">FWPM_LAYER_IPFORWARD_V4/FWPM_LAYER_IPFORWARD_V4_DISCARD/FWPM_LAYER_IPFORWARD_V6/FWPM_LAYER_IPFORWARD_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="ac051-126">FWPM_LAYER_IPFORWARD_V4 / FWPM_LAYER_IPFORWARD_V4_DISCARD / FWPM_LAYER_IPFORWARD_V6 / FWPM_LAYER_IPFORWARD_V6_DISCARD</span></span>
- <span data-ttu-id="ac051-127">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="ac051-127">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="ac051-128">FWPM_CONDITION_DESTINATION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="ac051-128">FWPM_CONDITION_DESTINATION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="ac051-129">FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="ac051-129">FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="ac051-130">FWPM_CONDITION_IP_DESTINATION_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-130">FWPM_CONDITION_IP_DESTINATION_ADDRESS</span></span>
- <span data-ttu-id="ac051-131">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-131">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span></span>
- <span data-ttu-id="ac051-132">FWPM_CONDITION_IP_FORWARD_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="ac051-132">FWPM_CONDITION_IP_FORWARD_INTERFACE</span></span>
- <span data-ttu-id="ac051-133">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="ac051-133">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="ac051-134">FWPM_CONDITION_IP_SOURCE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-134">FWPM_CONDITION_IP_SOURCE_ADDRESS</span></span>
- <span data-ttu-id="ac051-135">FWPM_CONDITION_SOURCE_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="ac051-135">FWPM_CONDITION_SOURCE_INTERFACE_INDEX</span></span>
- <span data-ttu-id="ac051-136">FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="ac051-136">FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="ac051-137">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="ac051-137">Windows 7  and later</span></span>
- <span data-ttu-id="ac051-138">FWPM_CONDITION_IP_PHYSICAL_ARRIVAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="ac051-138">FWPM_CONDITION_IP_PHYSICAL_ARRIVAL_INTERFACE</span></span> 
- <span data-ttu-id="ac051-139">FWPM_CONDITION_IP_PHYSICAL_NEXTHOP_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="ac051-139">FWPM_CONDITION_IP_PHYSICAL_NEXTHOP_INTERFACE</span></span>
- <span data-ttu-id="ac051-140">FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-140">FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID</span></span>
- <span data-ttu-id="ac051-141">FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-141">FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID</span></span>
## <a name="fwpm_layer_inbound_transport_v4--fwpm_layer_inbound_transport_v4_discard--fwpm_layer_inbound_transport_v6--fwpm_layer_inbound_transport_v6_discard"></a><span data-ttu-id="ac051-142">FWPM_LAYER_INBOUND_TRANSPORT_V4/FWPM_LAYER_INBOUND_TRANSPORT_V4_DISCARD/FWPM_LAYER_INBOUND_TRANSPORT_V6/FWPM_LAYER_INBOUND_TRANSPORT_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="ac051-142">FWPM_LAYER_INBOUND_TRANSPORT_V4 / FWPM_LAYER_INBOUND_TRANSPORT_V4_DISCARD / FWPM_LAYER_INBOUND_TRANSPORT_V6 / FWPM_LAYER_INBOUND_TRANSPORT_V6_DISCARD</span></span>
- <span data-ttu-id="ac051-143">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="ac051-143">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="ac051-144">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="ac051-144">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="ac051-145">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-145">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="ac051-146">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-146">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="ac051-147">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-147">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="ac051-148">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="ac051-148">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="ac051-149">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-149">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="ac051-150">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="ac051-150">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="ac051-151">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-151">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="ac051-152">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-152">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="ac051-153">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="ac051-153">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="ac051-154">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-154">FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="ac051-155">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="ac051-155">Windows 7  and later</span></span>
- <span data-ttu-id="ac051-156">FWPM_CONDITION_CURRENT_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-156">FWPM_CONDITION_CURRENT_PROFILE_ID</span></span>
## <a name="fwpm_layer_outbound_transport_v4--fwpm_layer_outbound_transport_v4_discard--fwpm_layer_outbound_transport_v6--fwpm_layer_outbound_transport_v6_discard"></a><span data-ttu-id="ac051-157">FWPM_LAYER_OUTBOUND_TRANSPORT_V4/FWPM_LAYER_OUTBOUND_TRANSPORT_V4_DISCARD/FWPM_LAYER_OUTBOUND_TRANSPORT_V6/FWPM_LAYER_OUTBOUND_TRANSPORT_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="ac051-157">FWPM_LAYER_OUTBOUND_TRANSPORT_V4 / FWPM_LAYER_OUTBOUND_TRANSPORT_V4_DISCARD / FWPM_LAYER_OUTBOUND_TRANSPORT_V6 / FWPM_LAYER_OUTBOUND_TRANSPORT_V6_DISCARD</span></span>
- <span data-ttu-id="ac051-158">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="ac051-158">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="ac051-159">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="ac051-159">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="ac051-160">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-160">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="ac051-161">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-161">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span></span>
- <span data-ttu-id="ac051-162">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-162">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="ac051-163">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-163">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="ac051-164">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="ac051-164">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="ac051-165">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-165">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="ac051-166">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="ac051-166">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="ac051-167">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-167">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="ac051-168">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-168">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="ac051-169">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="ac051-169">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="ac051-170">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-170">FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="ac051-171">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="ac051-171">Windows 7  and later</span></span>
- <span data-ttu-id="ac051-172">FWPM_CONDITION_CURRENT_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-172">FWPM_CONDITION_CURRENT_PROFILE_ID</span></span>
## <a name="fwpm_layer_stream_v4--fwpm_layer_stream_v4_discard--fwpm_layer_stream_v6--fwpm_layer_stream_v6_discard"></a><span data-ttu-id="ac051-173">FWPM_LAYER_STREAM_V4/FWPM_LAYER_STREAM_V4_DISCARD/FWPM_LAYER_STREAM_V6/FWPM_LAYER_STREAM_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="ac051-173">FWPM_LAYER_STREAM_V4 / FWPM_LAYER_STREAM_V4_DISCARD / FWPM_LAYER_STREAM_V6 / FWPM_LAYER_STREAM_V6_DISCARD</span></span>
- <span data-ttu-id="ac051-174">FWPM_CONDITION_DIRECTION</span><span class="sxs-lookup"><span data-stu-id="ac051-174">FWPM_CONDITION_DIRECTION</span></span>
- <span data-ttu-id="ac051-175">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="ac051-175">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="ac051-176">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-176">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="ac051-177">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-177">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="ac051-178">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-178">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="ac051-179">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-179">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="ac051-180">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-180">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
## <a name="fwpm_layer_datagram_data_v4--fwpm_layer_datagram_data_v4_discard--fwpm_layer_datagram_data_v6--fwpm_layer_datagram_data_v6_discard"></a><span data-ttu-id="ac051-181">FWPM_LAYER_DATAGRAM_DATA_V4/FWPM_LAYER_DATAGRAM_DATA_V4_DISCARD/FWPM_LAYER_DATAGRAM_DATA_V6/FWPM_LAYER_DATAGRAM_DATA_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="ac051-181">FWPM_LAYER_DATAGRAM_DATA_V4 / FWPM_LAYER_DATAGRAM_DATA_V4_DISCARD / FWPM_LAYER_DATAGRAM_DATA_V6 / FWPM_LAYER_DATAGRAM_DATA_V6_DISCARD</span></span>
- <span data-ttu-id="ac051-182">FWPM_CONDITION_DIRECTION</span><span class="sxs-lookup"><span data-stu-id="ac051-182">FWPM_CONDITION_DIRECTION</span></span>
- <span data-ttu-id="ac051-183">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="ac051-183">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="ac051-184">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="ac051-184">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="ac051-185">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-185">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="ac051-186">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-186">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="ac051-187">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-187">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="ac051-188">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="ac051-188">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="ac051-189">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-189">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="ac051-190">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="ac051-190">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="ac051-191">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-191">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="ac051-192">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-192">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="ac051-193">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="ac051-193">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="ac051-194">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-194">FWPM_CONDITION_TUNNEL_TYPE</span></span>
## <a name="fwpm_layer_stream_packet-v4--fwpm_layer_stream_packet-v6"></a><span data-ttu-id="ac051-195">FWPM_LAYER_STREAM_PACKET V4/FWPM_LAYER_STREAM_PACKET V6</span><span class="sxs-lookup"><span data-stu-id="ac051-195">FWPM_LAYER_STREAM_PACKET V4 / FWPM_LAYER_STREAM_PACKET V6</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="ac051-196">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="ac051-196">Windows 7  and later</span></span>
- <span data-ttu-id="ac051-197">FWPM_CONDITION_DIRECTION</span><span class="sxs-lookup"><span data-stu-id="ac051-197">FWPM_CONDITION_DIRECTION</span></span>
- <span data-ttu-id="ac051-198">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="ac051-198">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="ac051-199">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="ac051-199">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="ac051-200">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-200">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="ac051-201">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-201">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="ac051-202">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="ac051-202">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="ac051-203">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-203">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="ac051-204">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-204">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="ac051-205">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-205">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="ac051-206">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="ac051-206">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="ac051-207">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-207">FWPM_CONDITION_TUNNEL_TYPE</span></span>
## <a name="fwpm_layer_inbound_icmp_error_v4--fwpm_layer_inbound_icmp_error_v4_discard--fwpm_layer_inbound_icmp_error_v6--fwpm_layer_inbound_icmp_error_v6_discard"></a><span data-ttu-id="ac051-208">FWPM_LAYER_INBOUND_ICMP_ERROR_V4/FWPM_LAYER_INBOUND_ICMP_ERROR_V4_DISCARD/FWPM_LAYER_INBOUND_ICMP_ERROR_V6/FWPM_LAYER_INBOUND_ICMP_ERROR_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="ac051-208">FWPM_LAYER_INBOUND_ICMP_ERROR_V4 / FWPM_LAYER_INBOUND_ICMP_ERROR_V4_DISCARD / FWPM_LAYER_INBOUND_ICMP_ERROR_V6 / FWPM_LAYER_INBOUND_ICMP_ERROR_V6_DISCARD</span></span>
- <span data-ttu-id="ac051-209">FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="ac051-209">FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX</span></span>
- <span data-ttu-id="ac051-210">FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-210">FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE</span></span>
- <span data-ttu-id="ac051-211">FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX **Windows Vista/Windows 7:** FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="ac051-211">FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX **Windows Vista / Windows 7:** FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="ac051-212">FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-212">FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE</span></span>
- <span data-ttu-id="ac051-213">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="ac051-213">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="ac051-214">FWPM_CONDITION_ICMP_CODE</span><span class="sxs-lookup"><span data-stu-id="ac051-214">FWPM_CONDITION_ICMP_CODE</span></span>
- <span data-ttu-id="ac051-215">FWPM_CONDITION_ICMP_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-215">FWPM_CONDITION_ICMP_TYPE</span></span>

- <span data-ttu-id="ac051-216">FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-216">FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="ac051-217">FWPM_CONDITION_EMBEDDED_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-217">FWPM_CONDITION_EMBEDDED_LOCAL_PORT</span></span>
- <span data-ttu-id="ac051-218">FWPM_CONDITION_EMBEDDED_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="ac051-218">FWPM_CONDITION_EMBEDDED_PROTOCOL</span></span>
- <span data-ttu-id="ac051-219">FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-219">FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="ac051-220">FWPM_CONDITION_EMBEDDED_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-220">FWPM_CONDITION_EMBEDDED_REMOTE_PORT</span></span>
- <span data-ttu-id="ac051-221">FWPM_CONDITION_IP_ARRIVAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="ac051-221">FWPM_CONDITION_IP_ARRIVAL_INTERFACE</span></span>
- <span data-ttu-id="ac051-222">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-222">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="ac051-223">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="ac051-223">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="ac051-224">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-224">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="ac051-225">FWPM_CONDITION_LOCAL_INTERFACE_INDEX **Windows Vista/Windows 7:** FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="ac051-225">FWPM_CONDITION_LOCAL_INTERFACE_INDEX **Windows Vista / Windows 7:** FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="ac051-226">FWPM_CONDITION_LOCAL_INTERFACE_TYPE **Windows Vista/Windows 7:** FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-226">FWPM_CONDITION_LOCAL_INTERFACE_TYPE **Windows Vista / Windows 7:** FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="ac051-227">FWPM_CONDITION_LOCAL_TUNNEL_TYPE **Windows Vista/Windows 7:** FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-227">FWPM_CONDITION_LOCAL_TUNNEL_TYPE **Windows Vista / Windows 7:** FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="ac051-228">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="ac051-228">Windows 7  and later</span></span>
- <span data-ttu-id="ac051-229">FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-229">FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID</span></span>
## <a name="fwpm_layer_outbound_icmp_error_v4--fwpm_layer_outbound_icmp_error_v4_discard--fwpm_layer_outbound_icmp_error_v6--fwpm_layer_outbound_icmp_error_v6_discard"></a><span data-ttu-id="ac051-230">FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4/FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4_DISCARD/FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6/FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="ac051-230">FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4 / FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4_DISCARD / FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6 / FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6_DISCARD</span></span>
- <span data-ttu-id="ac051-231">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="ac051-231">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="ac051-232">FWPM_CONDITION_ICMP_CODE</span><span class="sxs-lookup"><span data-stu-id="ac051-232">FWPM_CONDITION_ICMP_CODE</span></span>
- <span data-ttu-id="ac051-233">FWPM_CONDITION_ICMP_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-233">FWPM_CONDITION_ICMP_TYPE</span></span>

- <span data-ttu-id="ac051-234">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="ac051-234">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="ac051-235">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-235">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="ac051-236">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-236">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="ac051-237">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-237">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="ac051-238">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="ac051-238">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="ac051-239">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-239">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="ac051-240">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="ac051-240">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="ac051-241">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-241">FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="ac051-242">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="ac051-242">Windows 7  and later</span></span>
- <span data-ttu-id="ac051-243">FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-243">FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID</span></span>
## <a name="fwpm_layer_ale_bind_redirect_v4--fwpm_layer_ale_bind_redirect-v6"></a><span data-ttu-id="ac051-244">FWPM_LAYER_ALE_BIND_REDIRECT_V4/FWPM_LAYER_ALE_BIND_REDIRECT V6</span><span class="sxs-lookup"><span data-stu-id="ac051-244">FWPM_LAYER_ALE_BIND_REDIRECT_V4 / FWPM_LAYER_ALE_BIND_REDIRECT V6</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="ac051-245">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="ac051-245">Windows 7  and later</span></span>
- <span data-ttu-id="ac051-246">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-246">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="ac051-247">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-247">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="ac051-248">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="ac051-248">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="ac051-249">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-249">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="ac051-250">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-250">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="ac051-251">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-251">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="ac051-252">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="ac051-252">FWPM_CONDITION_IP_PROTOCOL</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="ac051-253">Windows 8 e posterior</span><span class="sxs-lookup"><span data-stu-id="ac051-253">Windows 8  and later</span></span>
- <span data-ttu-id="ac051-254">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-254">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_resource_assignment_v4--fwpm_layer_ale_resource_assignment_v4_discard--fwpm_layer_ale_resource_assignment_v6--fwpm_layer_ale_resource_assignment_v6_discard"></a><span data-ttu-id="ac051-255">FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4/FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4_DISCARD/FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6/FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="ac051-255">FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4 / FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4_DISCARD / FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6 / FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6_DISCARD</span></span>
- <span data-ttu-id="ac051-256">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-256">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="ac051-257">FWPM_CONDITION_ALE_PROMISCUOUS_MODE</span><span class="sxs-lookup"><span data-stu-id="ac051-257">FWPM_CONDITION_ALE_PROMISCUOUS_MODE</span></span>
- <span data-ttu-id="ac051-258">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-258">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="ac051-259">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="ac051-259">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="ac051-260">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-260">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="ac051-261">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-261">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="ac051-262">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-262">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="ac051-263">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="ac051-263">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="ac051-264">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-264">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="ac051-265">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="ac051-265">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="ac051-266">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-266">FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="ac051-267">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="ac051-267">Windows 7  and later</span></span>
- <span data-ttu-id="ac051-268">FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-268">FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID</span></span>
- <span data-ttu-id="ac051-269">FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-269">FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="ac051-270">Windows 8 e posterior</span><span class="sxs-lookup"><span data-stu-id="ac051-270">Windows 8  and later</span></span>
- <span data-ttu-id="ac051-271">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-271">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_resource_release_v4--fwpm_layer_ale_resource_release_v6"></a><span data-ttu-id="ac051-272">FWPM_LAYER_ALE_RESOURCE_RELEASE_V4/FWPM_LAYER_ALE_RESOURCE_RELEASE_V6</span><span class="sxs-lookup"><span data-stu-id="ac051-272">FWPM_LAYER_ALE_RESOURCE_RELEASE_V4 / FWPM_LAYER_ALE_RESOURCE_RELEASE_V6</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="ac051-273">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="ac051-273">Windows 7  and later</span></span>
- <span data-ttu-id="ac051-274">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-274">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="ac051-275">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-275">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="ac051-276">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="ac051-276">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="ac051-277">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-277">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="ac051-278">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-278">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="ac051-279">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="ac051-279">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="ac051-280">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-280">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="ac051-281">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="ac051-281">FWPM_CONDITION_IP_PROTOCOL</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="ac051-282">Windows 8 e posterior</span><span class="sxs-lookup"><span data-stu-id="ac051-282">Windows 8  and later</span></span>
- <span data-ttu-id="ac051-283">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-283">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_endpoint_closure_v4--fwpm_layer_ale_endpoint_closure_v6"></a><span data-ttu-id="ac051-284">FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V4/FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V6</span><span class="sxs-lookup"><span data-stu-id="ac051-284">FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V4 / FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V6</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="ac051-285">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="ac051-285">Windows 7  and later</span></span>
- <span data-ttu-id="ac051-286">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-286">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="ac051-287">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-287">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="ac051-288">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="ac051-288">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="ac051-289">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-289">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="ac051-290">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-290">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="ac051-291">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="ac051-291">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="ac051-292">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-292">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="ac051-293">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="ac051-293">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="ac051-294">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-294">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="ac051-295">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-295">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="ac051-296">Windows 8 e posterior</span><span class="sxs-lookup"><span data-stu-id="ac051-296">Windows 8  and later</span></span>
- <span data-ttu-id="ac051-297">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-297">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_auth_listen_v4--fwpm_layer_ale_auth_listen_v4_discard--fwpm_layer_ale_auth_listen_v6--fwpm_layer_ale_auth_listen_v6_discard"></a><span data-ttu-id="ac051-298">FWPM_LAYER_ALE_AUTH_LISTEN_V4/FWPM_LAYER_ALE_AUTH_LISTEN_V4_DISCARD/FWPM_LAYER_ALE_AUTH_LISTEN_V6/FWPM_LAYER_ALE_AUTH_LISTEN_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="ac051-298">FWPM_LAYER_ALE_AUTH_LISTEN_V4 / FWPM_LAYER_ALE_AUTH_LISTEN_V4_DISCARD / FWPM_LAYER_ALE_AUTH_LISTEN_V6 / FWPM_LAYER_ALE_AUTH_LISTEN_V6_DISCARD</span></span>
- <span data-ttu-id="ac051-299">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-299">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="ac051-300">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-300">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="ac051-301">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="ac051-301">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="ac051-302">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-302">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="ac051-303">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-303">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="ac051-304">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-304">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="ac051-305">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="ac051-305">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="ac051-306">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-306">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="ac051-307">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-307">FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="ac051-308">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="ac051-308">Windows 7  and later</span></span>
- <span data-ttu-id="ac051-309">FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-309">FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID</span></span>
- <span data-ttu-id="ac051-310">FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-310">FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="ac051-311">Windows 8 e posterior</span><span class="sxs-lookup"><span data-stu-id="ac051-311">Windows 8  and later</span></span>
- <span data-ttu-id="ac051-312">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-312">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_auth_recv_accept_v4--fwpm_layer_ale_auth_recv_accept_v4_discard--fwpm_layer_ale_auth_recv_accept_v6--fwpm_layer_ale_auth_recv_accept_v6_discard"></a><span data-ttu-id="ac051-313">FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4/FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4_DISCARD/FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6/FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="ac051-313">FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4 / FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4_DISCARD / FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6 / FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6_DISCARD</span></span>
- <span data-ttu-id="ac051-314">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-314">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="ac051-315">FWPM_CONDITION_ALE_NAP_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="ac051-315">FWPM_CONDITION_ALE_NAP_CONTEXT</span></span>
- <span data-ttu-id="ac051-316">FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-316">FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</span></span>
- <span data-ttu-id="ac051-317">FWPM_CONDITION_ALE_REMOTE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-317">FWPM_CONDITION_ALE_REMOTE_USER_ID</span></span>
- <span data-ttu-id="ac051-318">FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-318">FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</span></span>
- <span data-ttu-id="ac051-319">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-319">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="ac051-320">FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="ac051-320">FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX</span></span>
- <span data-ttu-id="ac051-321">FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-321">FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE</span></span>
- <span data-ttu-id="ac051-322">FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX **Windows Vista/Windows 7:** FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="ac051-322">FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX **Windows Vista / Windows 7:** FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="ac051-323">FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-323">FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE</span></span>
- <span data-ttu-id="ac051-324">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="ac051-324">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="ac051-325">FWPM_CONDITION_IP_ARRIVAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="ac051-325">FWPM_CONDITION_IP_ARRIVAL_INTERFACE</span></span>
- <span data-ttu-id="ac051-326">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-326">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="ac051-327">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-327">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="ac051-328">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="ac051-328">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="ac051-329">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-329">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="ac051-330">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="ac051-330">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="ac051-331">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-331">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="ac051-332">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-332">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="ac051-333">FWPM_CONDITION_LOCAL_INTERFACE_INDEX **Windows Vista/Windows 7:** FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="ac051-333">FWPM_CONDITION_LOCAL_INTERFACE_INDEX **Windows Vista / Windows 7:** FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="ac051-334">FWPM_CONDITION_LOCAL_INTERFACE_TYPE **Windows Vista/Windows 7:** FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-334">FWPM_CONDITION_LOCAL_INTERFACE_TYPE **Windows Vista / Windows 7:** FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="ac051-335">FWPM_CONDITION_LOCAL_TUNNEL_TYPE **Windows Vista/Windows 7:** FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-335">FWPM_CONDITION_LOCAL_TUNNEL_TYPE **Windows Vista / Windows 7:** FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="ac051-336">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="ac051-336">Windows 7  and later</span></span>
- <span data-ttu-id="ac051-337">FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="ac051-337">FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="ac051-338">FWPM_CONDITION_IP_NEXTHOP_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="ac051-338">FWPM_CONDITION_IP_NEXTHOP_INTERFACE</span></span>
- <span data-ttu-id="ac051-339">FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-339">FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE</span></span>
- <span data-ttu-id="ac051-340">FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-340">FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE</span></span>
- <span data-ttu-id="ac051-341">FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="ac051-341">FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX</span></span>
- <span data-ttu-id="ac051-342">FWPM_CONDITION_ORIGINAL_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-342">FWPM_CONDITION_ORIGINAL_PROFILE_ID</span></span>
- <span data-ttu-id="ac051-343">FWPM_CONDITION_CURRENT_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-343">FWPM_CONDITION_CURRENT_PROFILE_ID</span></span>
- <span data-ttu-id="ac051-344">FWPM_CONDITION_REAUTHORIZE_REASON</span><span class="sxs-lookup"><span data-stu-id="ac051-344">FWPM_CONDITION_REAUTHORIZE_REASON</span></span>
- <span data-ttu-id="ac051-345">FWPM_CONDITION_ORIGINAL_ICMP_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-345">FWPM_CONDITION_ORIGINAL_ICMP_TYPE</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="ac051-346">Windows 8 e posterior</span><span class="sxs-lookup"><span data-stu-id="ac051-346">Windows 8  and later</span></span>
- <span data-ttu-id="ac051-347">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-347">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_connect_redirect_v4--fwpm_layer_ale_connect_redirect-v6"></a><span data-ttu-id="ac051-348">FWPM_LAYER_ALE_CONNECT_REDIRECT_V4/FWPM_LAYER_ALE_CONNECT_REDIRECT V6</span><span class="sxs-lookup"><span data-stu-id="ac051-348">FWPM_LAYER_ALE_CONNECT_REDIRECT_V4 / FWPM_LAYER_ALE_CONNECT_REDIRECT V6</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="ac051-349">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="ac051-349">Windows 7  and later</span></span>
- <span data-ttu-id="ac051-350">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-350">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="ac051-351">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-351">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="ac051-352">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="ac051-352">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="ac051-353">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-353">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="ac051-354">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-354">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="ac051-355">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-355">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="ac051-356">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="ac051-356">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="ac051-357">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-357">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="ac051-358">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-358">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="ac051-359">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-359">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="ac051-360">Windows 8 e posterior</span><span class="sxs-lookup"><span data-stu-id="ac051-360">Windows 8  and later</span></span>
- <span data-ttu-id="ac051-361">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-361">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_auth_connect_v4--fwpm_layer_ale_auth_connect_v4_discard--fwpm_layer_ale_auth_connect_v6--fwpm_layer_ale_auth_connect_v6_discard"></a><span data-ttu-id="ac051-362">FWPM_LAYER_ALE_AUTH_CONNECT_V4/FWPM_LAYER_ALE_AUTH_CONNECT_V4_DISCARD/FWPM_LAYER_ALE_AUTH_CONNECT_V6/FWPM_LAYER_ALE_AUTH_CONNECT_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="ac051-362">FWPM_LAYER_ALE_AUTH_CONNECT_V4 / FWPM_LAYER_ALE_AUTH_CONNECT_V4_DISCARD / FWPM_LAYER_ALE_AUTH_CONNECT_V6 / FWPM_LAYER_ALE_AUTH_CONNECT_V6_DISCARD</span></span>
- <span data-ttu-id="ac051-363">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-363">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="ac051-364">FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-364">FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</span></span>
- <span data-ttu-id="ac051-365">FWPM_CONDITION_ALE_REMOTE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-365">FWPM_CONDITION_ALE_REMOTE_USER_ID</span></span>
- <span data-ttu-id="ac051-366">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-366">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="ac051-367">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="ac051-367">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="ac051-368">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-368">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="ac051-369">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-369">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span></span>
- <span data-ttu-id="ac051-370">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-370">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="ac051-371">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-371">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="ac051-372">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="ac051-372">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="ac051-373">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-373">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="ac051-374">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="ac051-374">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="ac051-375">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-375">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="ac051-376">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-376">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="ac051-377">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="ac051-377">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="ac051-378">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-378">FWPM_CONDITION_TUNNEL_TYPE</span></span>
- <span data-ttu-id="ac051-379">FWPM_CONDITION_IP_ARRIVAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="ac051-379">FWPM_CONDITION_IP_ARRIVAL_INTERFACE</span></span>
- <span data-ttu-id="ac051-380">FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-380">FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE</span></span>
- <span data-ttu-id="ac051-381">FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-381">FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE</span></span>
- <span data-ttu-id="ac051-382">FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX Windows Vista _sp1 e laterFWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="ac051-382">FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX Windows Vista _sp1 and laterFWPM_CONDITION_INTERFACE_INDEX</span></span> 
###  <a name="windows-7--and-later"></a><span data-ttu-id="ac051-383">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="ac051-383">Windows 7  and later</span></span>
- <span data-ttu-id="ac051-384">FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="ac051-384">FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="ac051-385">FWPM_CONDITION_IP_NEXTHOP_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="ac051-385">FWPM_CONDITION_IP_NEXTHOP_INTERFACE</span></span>
- <span data-ttu-id="ac051-386">FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-386">FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE</span></span>
- <span data-ttu-id="ac051-387">FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-387">FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE</span></span>
- <span data-ttu-id="ac051-388">FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="ac051-388">FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX</span></span>
- <span data-ttu-id="ac051-389">FWPM_CONDITION_ORIGINAL_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-389">FWPM_CONDITION_ORIGINAL_PROFILE_ID</span></span>
- <span data-ttu-id="ac051-390">FWPM_CONDITION_CURRENT_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-390">FWPM_CONDITION_CURRENT_PROFILE_ID</span></span>
- <span data-ttu-id="ac051-391">FWPM_CONDITION_REAUTHORIZE_REASON</span><span class="sxs-lookup"><span data-stu-id="ac051-391">FWPM_CONDITION_REAUTHORIZE_REASON</span></span>
- <span data-ttu-id="ac051-392">FWPM_CONDITION_PEER_NAME</span><span class="sxs-lookup"><span data-stu-id="ac051-392">FWPM_CONDITION_PEER_NAME</span></span>
- <span data-ttu-id="ac051-393">FWPM_CONDITION_ORIGINAL_ICMP_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-393">FWPM_CONDITION_ORIGINAL_ICMP_TYPE</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="ac051-394">Windows 8 e posterior</span><span class="sxs-lookup"><span data-stu-id="ac051-394">Windows 8  and later</span></span>
- <span data-ttu-id="ac051-395">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-395">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_flow_established_v4--fwpm_layer_ale_flow_established_v4_discard--fwpm_layer_ale_flow_established_v6--fwpm_layer_ale_flow_established_v6_discard"></a><span data-ttu-id="ac051-396">FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4/FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4_DISCARD/FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6/FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="ac051-396">FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4 / FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4_DISCARD / FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6 / FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6_DISCARD</span></span>
- <span data-ttu-id="ac051-397">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-397">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="ac051-398">FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-398">FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</span></span>
- <span data-ttu-id="ac051-399">FWPM_CONDITION_ALE_REMOTE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-399">FWPM_CONDITION_ALE_REMOTE_USER_ID</span></span>
- <span data-ttu-id="ac051-400">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-400">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="ac051-401">FWPM_CONDITION_DIRECTION</span><span class="sxs-lookup"><span data-stu-id="ac051-401">FWPM_CONDITION_DIRECTION</span></span>
- <span data-ttu-id="ac051-402">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="ac051-402">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="ac051-403">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-403">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="ac051-404">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-404">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span></span>
- <span data-ttu-id="ac051-405">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-405">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="ac051-406">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-406">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="ac051-407">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="ac051-407">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="ac051-408">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-408">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="ac051-409">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="ac051-409">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="ac051-410">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-410">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="ac051-411">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-411">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="ac051-412">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-412">FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="ac051-413">Windows 8 e posterior</span><span class="sxs-lookup"><span data-stu-id="ac051-413">Windows 8  and later</span></span>
- <span data-ttu-id="ac051-414">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-414">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_name_resolution_cache_v4--fwpm_layer_name_resolution_cache_v6"></a><span data-ttu-id="ac051-415">FWPM_LAYER_NAME_RESOLUTION_CACHE_V4/FWPM_LAYER_NAME_RESOLUTION_CACHE_V6</span><span class="sxs-lookup"><span data-stu-id="ac051-415">FWPM_LAYER_NAME_RESOLUTION_CACHE_V4 / FWPM_LAYER_NAME_RESOLUTION_CACHE_V6</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="ac051-416">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="ac051-416">Windows 7  and later</span></span>
- <span data-ttu-id="ac051-417">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-417">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="ac051-418">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-418">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="ac051-419">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-419">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="ac051-420">FWPM_CONDITION_PEER_NAME</span><span class="sxs-lookup"><span data-stu-id="ac051-420">FWPM_CONDITION_PEER_NAME</span></span>
## <a name="fwpm_layer_ipsec_km_demux_v4--fwpm_layer_ipsec_km_demux_v6"></a><span data-ttu-id="ac051-421">FWPM_LAYER_IPSEC_KM_DEMUX_V4/FWPM_LAYER_IPSEC_KM_DEMUX_V6</span><span class="sxs-lookup"><span data-stu-id="ac051-421">FWPM_LAYER_IPSEC_KM_DEMUX_V4 / FWPM_LAYER_IPSEC_KM_DEMUX_V6</span></span>
- <span data-ttu-id="ac051-422">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-422">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="ac051-423">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-423">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
## <a name="fwpm_layer_ipsec_v4--fwpm_layer_ipsec_v6"></a><span data-ttu-id="ac051-424">FWPM_LAYER_IPSEC_V4/FWPM_LAYER_IPSEC_V6</span><span class="sxs-lookup"><span data-stu-id="ac051-424">FWPM_LAYER_IPSEC_V4 / FWPM_LAYER_IPSEC_V6</span></span>
- <span data-ttu-id="ac051-425">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-425">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="ac051-426">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-426">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="ac051-427">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="ac051-427">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="ac051-428">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-428">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="ac051-429">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-429">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="ac051-430">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="ac051-430">Windows 7  and later</span></span>
- <span data-ttu-id="ac051-431">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="ac051-431">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="ac051-432">FWPM_CONDITION_CURRENT_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-432">FWPM_CONDITION_CURRENT_PROFILE_ID</span></span>
## <a name="fwpm_layer_ikeext_v4--fwpm_layer_ikeext_v6"></a><span data-ttu-id="ac051-433">FWPM_LAYER_IKEEXT_V4/FWPM_LAYER_IKEEXT_V6</span><span class="sxs-lookup"><span data-stu-id="ac051-433">FWPM_LAYER_IKEEXT_V4 / FWPM_LAYER_IKEEXT_V6</span></span>
- <span data-ttu-id="ac051-434">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-434">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="ac051-435">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-435">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="ac051-436">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="ac051-436">Windows 7  and later</span></span>
- <span data-ttu-id="ac051-437">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="ac051-437">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="ac051-438">FWPM_CONDITION_CURRENT_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-438">FWPM_CONDITION_CURRENT_PROFILE_ID</span></span>
## <a name="fwpm_layer_rpc_um"></a><span data-ttu-id="ac051-439">FWPM_LAYER_RPC_UM</span><span class="sxs-lookup"><span data-stu-id="ac051-439">FWPM_LAYER_RPC_UM</span></span>
- <span data-ttu-id="ac051-440">FWPM_CONDITION_DCOM_APP_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-440">FWPM_CONDITION_DCOM_APP_ID</span></span>
- <span data-ttu-id="ac051-441">FWPM_CONDITION_IMAGE_NAME</span><span class="sxs-lookup"><span data-stu-id="ac051-441">FWPM_CONDITION_IMAGE_NAME</span></span>
- <span data-ttu-id="ac051-442">FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</span><span class="sxs-lookup"><span data-stu-id="ac051-442">FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</span></span>
- <span data-ttu-id="ac051-443">FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</span><span class="sxs-lookup"><span data-stu-id="ac051-443">FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</span></span>
- <span data-ttu-id="ac051-444">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-444">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="ac051-445">FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</span><span class="sxs-lookup"><span data-stu-id="ac051-445">FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</span></span>
- <span data-ttu-id="ac051-446">FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</span><span class="sxs-lookup"><span data-stu-id="ac051-446">FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</span></span>
- <span data-ttu-id="ac051-447">FWPM_CONDITION_PIPE</span><span class="sxs-lookup"><span data-stu-id="ac051-447">FWPM_CONDITION_PIPE</span></span>
- <span data-ttu-id="ac051-448">FWPM_CONDITION_REMOTE_USER_TOKEN</span><span class="sxs-lookup"><span data-stu-id="ac051-448">FWPM_CONDITION_REMOTE_USER_TOKEN</span></span>
- <span data-ttu-id="ac051-449">FWPM_CONDITION_RPC_AUTH_LEVEL</span><span class="sxs-lookup"><span data-stu-id="ac051-449">FWPM_CONDITION_RPC_AUTH_LEVEL</span></span>
- <span data-ttu-id="ac051-450">FWPM_CONDITION_RPC_AUTH_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-450">FWPM_CONDITION_RPC_AUTH_TYPE</span></span>
- <span data-ttu-id="ac051-451">FWPM_CONDITION_RPC_IF_FLAG</span><span class="sxs-lookup"><span data-stu-id="ac051-451">FWPM_CONDITION_RPC_IF_FLAG</span></span>
- <span data-ttu-id="ac051-452">FWPM_CONDITION_RPC_IF_UUID</span><span class="sxs-lookup"><span data-stu-id="ac051-452">FWPM_CONDITION_RPC_IF_UUID</span></span>
- <span data-ttu-id="ac051-453">FWPM_CONDITION_RPC_IF_VERSION</span><span class="sxs-lookup"><span data-stu-id="ac051-453">FWPM_CONDITION_RPC_IF_VERSION</span></span>
- <span data-ttu-id="ac051-454">FWPM_CONDITION_RPC_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="ac051-454">FWPM_CONDITION_RPC_PROTOCOL</span></span>
- <span data-ttu-id="ac051-455">FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</span><span class="sxs-lookup"><span data-stu-id="ac051-455">FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</span></span>
- <span data-ttu-id="ac051-456">FWPM_CONDITION_SEC_KEY_SIZE</span><span class="sxs-lookup"><span data-stu-id="ac051-456">FWPM_CONDITION_SEC_KEY_SIZE</span></span>
## <a name="fwpm_layer_rpc_epmap"></a><span data-ttu-id="ac051-457">FWPM_LAYER_RPC_EPMAP</span><span class="sxs-lookup"><span data-stu-id="ac051-457">FWPM_LAYER_RPC_EPMAP</span></span>
- <span data-ttu-id="ac051-458">FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</span><span class="sxs-lookup"><span data-stu-id="ac051-458">FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</span></span>
- <span data-ttu-id="ac051-459">FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</span><span class="sxs-lookup"><span data-stu-id="ac051-459">FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</span></span>
- <span data-ttu-id="ac051-460">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-460">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="ac051-461">FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</span><span class="sxs-lookup"><span data-stu-id="ac051-461">FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</span></span>
- <span data-ttu-id="ac051-462">FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</span><span class="sxs-lookup"><span data-stu-id="ac051-462">FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</span></span>

- <span data-ttu-id="ac051-463">FWPM_CONDITION_PIPE</span><span class="sxs-lookup"><span data-stu-id="ac051-463">FWPM_CONDITION_PIPE</span></span>
- <span data-ttu-id="ac051-464">FWPM_CONDITION_REMOTE_USER_TOKEN</span><span class="sxs-lookup"><span data-stu-id="ac051-464">FWPM_CONDITION_REMOTE_USER_TOKEN</span></span>
- <span data-ttu-id="ac051-465">FWPM_CONDITION_RPC_AUTH_LEVEL</span><span class="sxs-lookup"><span data-stu-id="ac051-465">FWPM_CONDITION_RPC_AUTH_LEVEL</span></span>
- <span data-ttu-id="ac051-466">FWPM_CONDITION_RPC_AUTH_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-466">FWPM_CONDITION_RPC_AUTH_TYPE</span></span>
- <span data-ttu-id="ac051-467">FWPM_CONDITION_RPC_IF_UUID</span><span class="sxs-lookup"><span data-stu-id="ac051-467">FWPM_CONDITION_RPC_IF_UUID</span></span>
- <span data-ttu-id="ac051-468">FWPM_CONDITION_RPC_IF_VERSION</span><span class="sxs-lookup"><span data-stu-id="ac051-468">FWPM_CONDITION_RPC_IF_VERSION</span></span>
- <span data-ttu-id="ac051-469">FWPM_CONDITION_RPC_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="ac051-469">FWPM_CONDITION_RPC_PROTOCOL</span></span>
- <span data-ttu-id="ac051-470">FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</span><span class="sxs-lookup"><span data-stu-id="ac051-470">FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</span></span>
- <span data-ttu-id="ac051-471">FWPM_CONDITION_SEC_KEY_SIZE</span><span class="sxs-lookup"><span data-stu-id="ac051-471">FWPM_CONDITION_SEC_KEY_SIZE</span></span>
## <a name="fwpm_layer_rpc_ep_add"></a><span data-ttu-id="ac051-472">FWPM_LAYER_RPC_EP_ADD</span><span class="sxs-lookup"><span data-stu-id="ac051-472">FWPM_LAYER_RPC_EP_ADD</span></span>
- <span data-ttu-id="ac051-473">FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID</span><span class="sxs-lookup"><span data-stu-id="ac051-473">FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID</span></span>
- <span data-ttu-id="ac051-474">FWPM_CONDITION_RPC_EP_FLAGS</span><span class="sxs-lookup"><span data-stu-id="ac051-474">FWPM_CONDITION_RPC_EP_FLAGS</span></span>
- <span data-ttu-id="ac051-475">FWPM_CONDITION_RPC_EP_VALUE</span><span class="sxs-lookup"><span data-stu-id="ac051-475">FWPM_CONDITION_RPC_EP_VALUE</span></span>
- <span data-ttu-id="ac051-476">FWPM_CONDITION_RPC_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="ac051-476">FWPM_CONDITION_RPC_PROTOCOL</span></span>
## <a name="fwpm_layer_rpc_proxy_conn"></a><span data-ttu-id="ac051-477">FWPM_LAYER_RPC_PROXY_CONN</span><span class="sxs-lookup"><span data-stu-id="ac051-477">FWPM_LAYER_RPC_PROXY_CONN</span></span>
- <span data-ttu-id="ac051-478">FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</span><span class="sxs-lookup"><span data-stu-id="ac051-478">FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</span></span>
- <span data-ttu-id="ac051-479">FWPM_CONDITION_CLIENT_CERT_OID</span><span class="sxs-lookup"><span data-stu-id="ac051-479">FWPM_CONDITION_CLIENT_CERT_OID</span></span>
- <span data-ttu-id="ac051-480">FWPM_CONDITION_CLIENT_TOKEN</span><span class="sxs-lookup"><span data-stu-id="ac051-480">FWPM_CONDITION_CLIENT_TOKEN</span></span>
- <span data-ttu-id="ac051-481">FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-481">FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</span></span>
- <span data-ttu-id="ac051-482">FWPM_CONDITION_RPC_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="ac051-482">FWPM_CONDITION_RPC_SERVER_NAME</span></span>
- <span data-ttu-id="ac051-483">FWPM_CONDITION_RPC_SERVER_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-483">FWPM_CONDITION_RPC_SERVER_PORT</span></span>
## <a name="fwpm_layer_rpc_proxy_if"></a><span data-ttu-id="ac051-484">FWPM_LAYER_RPC_PROXY_IF</span><span class="sxs-lookup"><span data-stu-id="ac051-484">FWPM_LAYER_RPC_PROXY_IF</span></span>
- <span data-ttu-id="ac051-485">FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</span><span class="sxs-lookup"><span data-stu-id="ac051-485">FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</span></span>
- <span data-ttu-id="ac051-486">FWPM_CONDITION_CLIENT_CERT_OID</span><span class="sxs-lookup"><span data-stu-id="ac051-486">FWPM_CONDITION_CLIENT_CERT_OID</span></span>
- <span data-ttu-id="ac051-487">FWPM_CONDITION_CLIENT_TOKEN</span><span class="sxs-lookup"><span data-stu-id="ac051-487">FWPM_CONDITION_CLIENT_TOKEN</span></span>
- <span data-ttu-id="ac051-488">FWPM_CONDITION_RPC_IF_UUID</span><span class="sxs-lookup"><span data-stu-id="ac051-488">FWPM_CONDITION_RPC_IF_UUID</span></span>
- <span data-ttu-id="ac051-489">FWPM_CONDITION_RPC_IF_VERSION</span><span class="sxs-lookup"><span data-stu-id="ac051-489">FWPM_CONDITION_RPC_IF_VERSION</span></span>
- <span data-ttu-id="ac051-490">FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-490">FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</span></span>
- <span data-ttu-id="ac051-491">FWPM_CONDITION_RPC_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="ac051-491">FWPM_CONDITION_RPC_SERVER_NAME</span></span>
- <span data-ttu-id="ac051-492">FWPM_CONDITION_RPC_SERVER_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-492">FWPM_CONDITION_RPC_SERVER_PORT</span></span>
## <a name="fwpm_layer_km_authorization"></a><span data-ttu-id="ac051-493">FWPM_LAYER_KM_AUTHORIZATION</span><span class="sxs-lookup"><span data-stu-id="ac051-493">FWPM_LAYER_KM_AUTHORIZATION</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="ac051-494">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="ac051-494">Windows 7  and later</span></span>
- <span data-ttu-id="ac051-495">FWPM_CONDITION_REMOTE_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-495">FWPM_CONDITION_REMOTE_ID</span></span>
- <span data-ttu-id="ac051-496">FWPM_CONDITION_AUTHENTICATION_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-496">FWPM_CONDITION_AUTHENTICATION_TYPE</span></span>
- <span data-ttu-id="ac051-497">FWPM_CONDITION_KM_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-497">FWPM_CONDITION_KM_TYPE</span></span>
- <span data-ttu-id="ac051-498">FWPM_CONDITION_KM_MODE</span><span class="sxs-lookup"><span data-stu-id="ac051-498">FWPM_CONDITION_KM_MODE</span></span>
- <span data-ttu-id="ac051-499">FWPM_CONDITION_DIRECTION</span><span class="sxs-lookup"><span data-stu-id="ac051-499">FWPM_CONDITION_DIRECTION</span></span>
- <span data-ttu-id="ac051-500">FWPM_CONDITION_IPSEC_POLICY_KEY</span><span class="sxs-lookup"><span data-stu-id="ac051-500">FWPM_CONDITION_IPSEC_POLICY_KEY</span></span>
## <a name="fwpm_layer_inbound_mac_frame_ethernet--fwpm_layer_outbound_mac_frame_ethernet"></a><span data-ttu-id="ac051-501">FWPM_LAYER_INBOUND_MAC_FRAME_ETHERNET/FWPM_LAYER_OUTBOUND_MAC_FRAME_ETHERNET</span><span class="sxs-lookup"><span data-stu-id="ac051-501">FWPM_LAYER_INBOUND_MAC_FRAME_ETHERNET / FWPM_LAYER_OUTBOUND_MAC_FRAME_ETHERNET</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="ac051-502">Windows 8 e posterior</span><span class="sxs-lookup"><span data-stu-id="ac051-502">Windows 8  and later</span></span>
- <span data-ttu-id="ac051-503">FWPM_CONDITION_INTERFACE_MAC_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-503">FWPM_CONDITION_INTERFACE_MAC_ADDRESS</span></span>
- <span data-ttu-id="ac051-504">FWPM_CONDITION_MAC_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-504">FWPM_CONDITION_MAC_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="ac051-505">FWPM_CONDITION_MAC_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-505">FWPM_CONDITION_MAC_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="ac051-506">FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-506">FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="ac051-507">FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-507">FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE</span></span>
- <span data-ttu-id="ac051-508">FWPM_CONDITION_ETHER_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-508">FWPM_CONDITION_ETHER_TYPE</span></span>
- <span data-ttu-id="ac051-509">FWPM_CONDITION_VLAN_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-509">FWPM_CONDITION_VLAN_ID</span></span>
- <span data-ttu-id="ac051-510">FWPM_CONDITION_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="ac051-510">FWPM_CONDITION_INTERFACE</span></span>
- <span data-ttu-id="ac051-511">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="ac051-511">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="ac051-512">FWPM_CONDITION_NDIS_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-512">FWPM_CONDITION_NDIS_PORT</span></span>
- <span data-ttu-id="ac051-513">FWPM_CONDITION_L2_FLAGS</span><span class="sxs-lookup"><span data-stu-id="ac051-513">FWPM_CONDITION_L2_FLAGS</span></span>
##  <a name="fwpm_layer_inbound_mac_frame_native--fwpm_layer_outbound_mac_frame_native"></a><span data-ttu-id="ac051-514">FWPM_LAYER_INBOUND_MAC_FRAME_NATIVE/FWPM_LAYER_OUTBOUND_MAC_FRAME_NATIVE</span><span class="sxs-lookup"><span data-stu-id="ac051-514">FWPM_LAYER_INBOUND_MAC_FRAME_NATIVE / FWPM_LAYER_OUTBOUND_MAC_FRAME_NATIVE</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="ac051-515">Windows 8 e posterior</span><span class="sxs-lookup"><span data-stu-id="ac051-515">Windows 8  and later</span></span>
- <span data-ttu-id="ac051-516">FWPM_CONDITION_NDIS_MEDIA_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-516">FWPM_CONDITION_NDIS_MEDIA_TYPE</span></span>
- <span data-ttu-id="ac051-517">FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-517">FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE</span></span>
- <span data-ttu-id="ac051-518">FWPM_CONDITION_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="ac051-518">FWPM_CONDITION_INTERFACE</span></span>
- <span data-ttu-id="ac051-519">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-519">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="ac051-520">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="ac051-520">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="ac051-521">FWPM_CONDITION_NDIS_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-521">FWPM_CONDITION_NDIS_PORT</span></span>
- <span data-ttu-id="ac051-522">FWPM_CONDITION_L2_FLAGS</span><span class="sxs-lookup"><span data-stu-id="ac051-522">FWPM_CONDITION_L2_FLAGS</span></span>
## <a name="fwpm_layer_egress_vswitch_ethernet--fwpm_layer_ingress_vswitch_ethernet"></a><span data-ttu-id="ac051-523">FWPM_LAYER_EGRESS_VSWITCH_ETHERNET/FWPM_LAYER_INGRESS_VSWITCH_ETHERNET</span><span class="sxs-lookup"><span data-stu-id="ac051-523">FWPM_LAYER_EGRESS_VSWITCH_ETHERNET / FWPM_LAYER_INGRESS_VSWITCH_ETHERNET</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="ac051-524">Windows 8 e posterior</span><span class="sxs-lookup"><span data-stu-id="ac051-524">Windows 8  and later</span></span>
- <span data-ttu-id="ac051-525">FWPM_CONDITION_MAC_SOURCE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-525">FWPM_CONDITION_MAC_SOURCE_ADDRESS</span></span>
- <span data-ttu-id="ac051-526">FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-526">FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE</span></span>
- <span data-ttu-id="ac051-527">FWPM_CONDITION_MAC_DESTINATION_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-527">FWPM_CONDITION_MAC_DESTINATION_ADDRESS</span></span>
- <span data-ttu-id="ac051-528">FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-528">FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE</span></span>
- <span data-ttu-id="ac051-529">FWPM_CONDITION_ETHER_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-529">FWPM_CONDITION_ETHER_TYPE</span></span>
- <span data-ttu-id="ac051-530">FWPM_CONDITION_VLAN_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-530">FWPM_CONDITION_VLAN_ID</span></span>
- <span data-ttu-id="ac051-531">FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-531">FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</span></span>
- <span data-ttu-id="ac051-532">FWPM_CONDITION_VSWITCH_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-532">FWPM_CONDITION_VSWITCH_ID</span></span>
- <span data-ttu-id="ac051-533">FWPM_CONDITION_VSWITCH_NETWORK_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-533">FWPM_CONDITION_VSWITCH_NETWORK_TYPE</span></span>
- <span data-ttu-id="ac051-534">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-534">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</span></span>
- <span data-ttu-id="ac051-535">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-535">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</span></span>
- <span data-ttu-id="ac051-536">FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-536">FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</span></span>
- <span data-ttu-id="ac051-537">FWPM_CONDITION_VSWITCH_L2_FLAGS</span><span class="sxs-lookup"><span data-stu-id="ac051-537">FWPM_CONDITION_VSWITCH_L2_FLAGS</span></span>
##  <a name="fwpm_layer_egress_vswitch_transport_v4--fwpm_layer_ingress_vswitch_transport_v4--fwpm_layer_egressvswitch_transport_v6--fwpm_layer_ingress_vswitch_transport_v6"></a><span data-ttu-id="ac051-538">FWPM_LAYER_EGRESS_VSWITCH_TRANSPORT_V4/FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V4/FWPM_LAYER_EGRESSVSWITCH_TRANSPORT_V6/FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V6</span><span class="sxs-lookup"><span data-stu-id="ac051-538">FWPM_LAYER_EGRESS_VSWITCH_TRANSPORT_V4 / FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V4 / FWPM_LAYER_EGRESSVSWITCH_TRANSPORT_V6 / FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V6</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="ac051-539">Windows 8 e posterior</span><span class="sxs-lookup"><span data-stu-id="ac051-539">Windows 8  and later</span></span>
- <span data-ttu-id="ac051-540">FWPM_CONDITION_IP_SOURCE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-540">FWPM_CONDITION_IP_SOURCE_ADDRESS</span></span>
- <span data-ttu-id="ac051-541">FWPM_CONDITION_IP_DESTINATION_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="ac051-541">FWPM_CONDITION_IP_DESTINATION_ADDRESS</span></span>
- <span data-ttu-id="ac051-542">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="ac051-542">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="ac051-543">FWPM_CONDITION_IP_SOURCE_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-543">FWPM_CONDITION_IP_SOURCE_PORT</span></span>
- <span data-ttu-id="ac051-544">FWPM_CONDITION_IP_DESTINATION_PORT</span><span class="sxs-lookup"><span data-stu-id="ac051-544">FWPM_CONDITION_IP_DESTINATION_PORT</span></span>
- <span data-ttu-id="ac051-545">FWPM_CONDITION_VLAN_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-545">FWPM_CONDITION_VLAN_ID</span></span>
- <span data-ttu-id="ac051-546">FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-546">FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</span></span>
- <span data-ttu-id="ac051-547">FWPM_CONDITION_VSWITCH_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-547">FWPM_CONDITION_VSWITCH_ID</span></span>
- <span data-ttu-id="ac051-548">FWPM_CONDITION_VSWITCH_NETWORK_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-548">FWPM_CONDITION_VSWITCH_NETWORK_TYPE</span></span>
- <span data-ttu-id="ac051-549">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-549">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</span></span>
- <span data-ttu-id="ac051-550">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-550">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</span></span>
- <span data-ttu-id="ac051-551">FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-551">FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</span></span>
- <span data-ttu-id="ac051-552">FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID</span><span class="sxs-lookup"><span data-stu-id="ac051-552">FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID</span></span>
- <span data-ttu-id="ac051-553">FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="ac051-553">FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="ac051-554">FWPM_CONDITION_VSWITCH_L2_FLAGS</span><span class="sxs-lookup"><span data-stu-id="ac051-554">FWPM_CONDITION_VSWITCH_L2_FLAGS</span></span>



## <a name="remarks"></a><span data-ttu-id="ac051-555">Comentários</span><span class="sxs-lookup"><span data-stu-id="ac051-555">Remarks</span></span>

<span data-ttu-id="ac051-556">Os sufixos v4 e V6 no final dos identificadores de camada indicam se a camada está localizada na pilha de rede IPv4 ou na pilha de rede IPv6.</span><span class="sxs-lookup"><span data-stu-id="ac051-556">The V4 and V6 suffixes at the end of the layer identifiers indicate whether the layer is located in the IPv4 network stack or in the IPv6 network stack.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac051-557">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac051-557">Requirements</span></span>



| <span data-ttu-id="ac051-558">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac051-558">Requirement</span></span> | <span data-ttu-id="ac051-559">Valor</span><span class="sxs-lookup"><span data-stu-id="ac051-559">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ac051-560">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac051-560">Minimum supported client</span></span><br/> | <span data-ttu-id="ac051-561">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ac051-561">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ac051-562">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac051-562">Minimum supported server</span></span><br/> | <span data-ttu-id="ac051-563">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ac051-563">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ac051-564">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ac051-564">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac051-565"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac051-565"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 






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
# <a name="filtering-conditions-available-at-each-filtering-layer"></a><span data-ttu-id="69b49-103">Condições de filtragem disponíveis em cada camada de filtragem</span><span class="sxs-lookup"><span data-stu-id="69b49-103">Filtering Conditions Available at Each Filtering Layer</span></span>

<span data-ttu-id="69b49-104">O mecanismo de filtro da WFP (plataforma de filtragem do Windows) dá suporte a um conjunto diferente de condições de filtragem em cada uma de suas camadas de filtragem.</span><span class="sxs-lookup"><span data-stu-id="69b49-104">The Windows Filtering Platform (WFP) filter engine supports a different set of filtering conditions at each of its filtering layers.</span></span>

<span data-ttu-id="69b49-105">A lista de condições de filtragem que estão disponíveis em cada camada são as seguintes.</span><span class="sxs-lookup"><span data-stu-id="69b49-105">The list of filtering conditions that are available at each layer are as follows.</span></span>

## <a name="fwpm_layer_inbound_ippacket_v4--fwpm_layer_inbound_ippacket_v4_discard--fwpm_layer_inbound_ippacket_v6--fwpm_layer_inbound_ippacket_v6_discard"></a><span data-ttu-id="69b49-106">FWPM_LAYER_INBOUND_IPPACKET_V4/FWPM_LAYER_INBOUND_IPPACKET_V4_DISCARD/FWPM_LAYER_INBOUND_IPPACKET_V6/FWPM_LAYER_INBOUND_IPPACKET_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="69b49-106">FWPM_LAYER_INBOUND_IPPACKET_V4 / FWPM_LAYER_INBOUND_IPPACKET_V4_DISCARD / FWPM_LAYER_INBOUND_IPPACKET_V6 / FWPM_LAYER_INBOUND_IPPACKET_V6_DISCARD</span></span>
- <span data-ttu-id="69b49-107">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="69b49-107">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="69b49-108">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="69b49-108">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="69b49-109">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-109">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="69b49-110">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-110">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="69b49-111">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-111">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="69b49-112">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="69b49-112">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="69b49-113">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-113">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="69b49-114">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="69b49-114">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="69b49-115">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-115">FWPM_CONDITION_TUNNEL_TYPE</span></span>
## <a name="fwpm_layer_outbound_ippacket_v4--fwpm_layer_outbound_ippacket_v4_discard--fwpm_layer_outbound_ippacket_v6--fwpm_layer_outbound_ippacket_v6_discard"></a><span data-ttu-id="69b49-116">FWPM_LAYER_OUTBOUND_IPPACKET_V4/FWPM_LAYER_OUTBOUND_IPPACKET_V4_DISCARD/FWPM_LAYER_OUTBOUND_IPPACKET_V6/FWPM_LAYER_OUTBOUND_IPPACKET_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="69b49-116">FWPM_LAYER_OUTBOUND_IPPACKET_V4 / FWPM_LAYER_OUTBOUND_IPPACKET_V4_DISCARD / FWPM_LAYER_OUTBOUND_IPPACKET_V6 / FWPM_LAYER_OUTBOUND_IPPACKET_V6_DISCARD</span></span>
- <span data-ttu-id="69b49-117">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="69b49-117">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="69b49-118">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="69b49-118">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="69b49-119">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-119">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="69b49-120">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-120">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="69b49-121">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-121">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="69b49-122">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="69b49-122">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="69b49-123">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-123">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="69b49-124">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="69b49-124">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="69b49-125">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-125">FWPM_CONDITION_TUNNEL_TYPE</span></span>
## <a name="fwpm_layer_ipforward_v4--fwpm_layer_ipforward_v4_discard--fwpm_layer_ipforward_v6--fwpm_layer_ipforward_v6_discard"></a><span data-ttu-id="69b49-126">FWPM_LAYER_IPFORWARD_V4/FWPM_LAYER_IPFORWARD_V4_DISCARD/FWPM_LAYER_IPFORWARD_V6/FWPM_LAYER_IPFORWARD_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="69b49-126">FWPM_LAYER_IPFORWARD_V4 / FWPM_LAYER_IPFORWARD_V4_DISCARD / FWPM_LAYER_IPFORWARD_V6 / FWPM_LAYER_IPFORWARD_V6_DISCARD</span></span>
- <span data-ttu-id="69b49-127">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="69b49-127">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="69b49-128">FWPM_CONDITION_DESTINATION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="69b49-128">FWPM_CONDITION_DESTINATION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="69b49-129">FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="69b49-129">FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="69b49-130">FWPM_CONDITION_IP_DESTINATION_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-130">FWPM_CONDITION_IP_DESTINATION_ADDRESS</span></span>
- <span data-ttu-id="69b49-131">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-131">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span></span>
- <span data-ttu-id="69b49-132">FWPM_CONDITION_IP_FORWARD_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="69b49-132">FWPM_CONDITION_IP_FORWARD_INTERFACE</span></span>
- <span data-ttu-id="69b49-133">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="69b49-133">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="69b49-134">FWPM_CONDITION_IP_SOURCE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-134">FWPM_CONDITION_IP_SOURCE_ADDRESS</span></span>
- <span data-ttu-id="69b49-135">FWPM_CONDITION_SOURCE_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="69b49-135">FWPM_CONDITION_SOURCE_INTERFACE_INDEX</span></span>
- <span data-ttu-id="69b49-136">FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="69b49-136">FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="69b49-137">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="69b49-137">Windows 7  and later</span></span>
- <span data-ttu-id="69b49-138">FWPM_CONDITION_IP_PHYSICAL_ARRIVAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="69b49-138">FWPM_CONDITION_IP_PHYSICAL_ARRIVAL_INTERFACE</span></span> 
- <span data-ttu-id="69b49-139">FWPM_CONDITION_IP_PHYSICAL_NEXTHOP_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="69b49-139">FWPM_CONDITION_IP_PHYSICAL_NEXTHOP_INTERFACE</span></span>
- <span data-ttu-id="69b49-140">FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-140">FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID</span></span>
- <span data-ttu-id="69b49-141">FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-141">FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID</span></span>
## <a name="fwpm_layer_inbound_transport_v4--fwpm_layer_inbound_transport_v4_discard--fwpm_layer_inbound_transport_v6--fwpm_layer_inbound_transport_v6_discard"></a><span data-ttu-id="69b49-142">FWPM_LAYER_INBOUND_TRANSPORT_V4/FWPM_LAYER_INBOUND_TRANSPORT_V4_DISCARD/FWPM_LAYER_INBOUND_TRANSPORT_V6/FWPM_LAYER_INBOUND_TRANSPORT_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="69b49-142">FWPM_LAYER_INBOUND_TRANSPORT_V4 / FWPM_LAYER_INBOUND_TRANSPORT_V4_DISCARD / FWPM_LAYER_INBOUND_TRANSPORT_V6 / FWPM_LAYER_INBOUND_TRANSPORT_V6_DISCARD</span></span>
- <span data-ttu-id="69b49-143">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="69b49-143">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="69b49-144">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="69b49-144">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="69b49-145">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-145">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="69b49-146">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-146">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="69b49-147">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-147">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="69b49-148">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="69b49-148">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="69b49-149">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-149">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="69b49-150">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="69b49-150">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="69b49-151">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-151">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="69b49-152">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-152">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="69b49-153">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="69b49-153">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="69b49-154">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-154">FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="69b49-155">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="69b49-155">Windows 7  and later</span></span>
- <span data-ttu-id="69b49-156">FWPM_CONDITION_CURRENT_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-156">FWPM_CONDITION_CURRENT_PROFILE_ID</span></span>
## <a name="fwpm_layer_outbound_transport_v4--fwpm_layer_outbound_transport_v4_discard--fwpm_layer_outbound_transport_v6--fwpm_layer_outbound_transport_v6_discard"></a><span data-ttu-id="69b49-157">FWPM_LAYER_OUTBOUND_TRANSPORT_V4/FWPM_LAYER_OUTBOUND_TRANSPORT_V4_DISCARD/FWPM_LAYER_OUTBOUND_TRANSPORT_V6/FWPM_LAYER_OUTBOUND_TRANSPORT_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="69b49-157">FWPM_LAYER_OUTBOUND_TRANSPORT_V4 / FWPM_LAYER_OUTBOUND_TRANSPORT_V4_DISCARD / FWPM_LAYER_OUTBOUND_TRANSPORT_V6 / FWPM_LAYER_OUTBOUND_TRANSPORT_V6_DISCARD</span></span>
- <span data-ttu-id="69b49-158">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="69b49-158">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="69b49-159">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="69b49-159">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="69b49-160">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-160">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="69b49-161">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-161">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span></span>
- <span data-ttu-id="69b49-162">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-162">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="69b49-163">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-163">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="69b49-164">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="69b49-164">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="69b49-165">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-165">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="69b49-166">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="69b49-166">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="69b49-167">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-167">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="69b49-168">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-168">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="69b49-169">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="69b49-169">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="69b49-170">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-170">FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="69b49-171">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="69b49-171">Windows 7  and later</span></span>
- <span data-ttu-id="69b49-172">FWPM_CONDITION_CURRENT_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-172">FWPM_CONDITION_CURRENT_PROFILE_ID</span></span>
## <a name="fwpm_layer_stream_v4--fwpm_layer_stream_v4_discard--fwpm_layer_stream_v6--fwpm_layer_stream_v6_discard"></a><span data-ttu-id="69b49-173">FWPM_LAYER_STREAM_V4/FWPM_LAYER_STREAM_V4_DISCARD/FWPM_LAYER_STREAM_V6/FWPM_LAYER_STREAM_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="69b49-173">FWPM_LAYER_STREAM_V4 / FWPM_LAYER_STREAM_V4_DISCARD / FWPM_LAYER_STREAM_V6 / FWPM_LAYER_STREAM_V6_DISCARD</span></span>
- <span data-ttu-id="69b49-174">FWPM_CONDITION_DIRECTION</span><span class="sxs-lookup"><span data-stu-id="69b49-174">FWPM_CONDITION_DIRECTION</span></span>
- <span data-ttu-id="69b49-175">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="69b49-175">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="69b49-176">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-176">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="69b49-177">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-177">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="69b49-178">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-178">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="69b49-179">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-179">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="69b49-180">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-180">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
## <a name="fwpm_layer_datagram_data_v4--fwpm_layer_datagram_data_v4_discard--fwpm_layer_datagram_data_v6--fwpm_layer_datagram_data_v6_discard"></a><span data-ttu-id="69b49-181">FWPM_LAYER_DATAGRAM_DATA_V4/FWPM_LAYER_DATAGRAM_DATA_V4_DISCARD/FWPM_LAYER_DATAGRAM_DATA_V6/FWPM_LAYER_DATAGRAM_DATA_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="69b49-181">FWPM_LAYER_DATAGRAM_DATA_V4 / FWPM_LAYER_DATAGRAM_DATA_V4_DISCARD / FWPM_LAYER_DATAGRAM_DATA_V6 / FWPM_LAYER_DATAGRAM_DATA_V6_DISCARD</span></span>
- <span data-ttu-id="69b49-182">FWPM_CONDITION_DIRECTION</span><span class="sxs-lookup"><span data-stu-id="69b49-182">FWPM_CONDITION_DIRECTION</span></span>
- <span data-ttu-id="69b49-183">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="69b49-183">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="69b49-184">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="69b49-184">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="69b49-185">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-185">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="69b49-186">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-186">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="69b49-187">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-187">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="69b49-188">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="69b49-188">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="69b49-189">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-189">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="69b49-190">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="69b49-190">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="69b49-191">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-191">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="69b49-192">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-192">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="69b49-193">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="69b49-193">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="69b49-194">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-194">FWPM_CONDITION_TUNNEL_TYPE</span></span>
## <a name="fwpm_layer_stream_packet-v4--fwpm_layer_stream_packet-v6"></a><span data-ttu-id="69b49-195">FWPM_LAYER_STREAM_PACKET V4/FWPM_LAYER_STREAM_PACKET V6</span><span class="sxs-lookup"><span data-stu-id="69b49-195">FWPM_LAYER_STREAM_PACKET V4 / FWPM_LAYER_STREAM_PACKET V6</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="69b49-196">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="69b49-196">Windows 7  and later</span></span>
- <span data-ttu-id="69b49-197">FWPM_CONDITION_DIRECTION</span><span class="sxs-lookup"><span data-stu-id="69b49-197">FWPM_CONDITION_DIRECTION</span></span>
- <span data-ttu-id="69b49-198">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="69b49-198">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="69b49-199">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="69b49-199">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="69b49-200">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-200">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="69b49-201">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-201">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="69b49-202">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="69b49-202">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="69b49-203">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-203">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="69b49-204">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-204">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="69b49-205">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-205">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="69b49-206">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="69b49-206">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="69b49-207">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-207">FWPM_CONDITION_TUNNEL_TYPE</span></span>
## <a name="fwpm_layer_inbound_icmp_error_v4--fwpm_layer_inbound_icmp_error_v4_discard--fwpm_layer_inbound_icmp_error_v6--fwpm_layer_inbound_icmp_error_v6_discard"></a><span data-ttu-id="69b49-208">FWPM_LAYER_INBOUND_ICMP_ERROR_V4/FWPM_LAYER_INBOUND_ICMP_ERROR_V4_DISCARD/FWPM_LAYER_INBOUND_ICMP_ERROR_V6/FWPM_LAYER_INBOUND_ICMP_ERROR_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="69b49-208">FWPM_LAYER_INBOUND_ICMP_ERROR_V4 / FWPM_LAYER_INBOUND_ICMP_ERROR_V4_DISCARD / FWPM_LAYER_INBOUND_ICMP_ERROR_V6 / FWPM_LAYER_INBOUND_ICMP_ERROR_V6_DISCARD</span></span>
- <span data-ttu-id="69b49-209">FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="69b49-209">FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX</span></span>
- <span data-ttu-id="69b49-210">FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-210">FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE</span></span>
- <span data-ttu-id="69b49-211">FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX **Windows Vista/Windows 7:** FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="69b49-211">FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX **Windows Vista / Windows 7:** FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="69b49-212">FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-212">FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE</span></span>
- <span data-ttu-id="69b49-213">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="69b49-213">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="69b49-214">FWPM_CONDITION_ICMP_CODE</span><span class="sxs-lookup"><span data-stu-id="69b49-214">FWPM_CONDITION_ICMP_CODE</span></span>
- <span data-ttu-id="69b49-215">FWPM_CONDITION_ICMP_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-215">FWPM_CONDITION_ICMP_TYPE</span></span>

- <span data-ttu-id="69b49-216">FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-216">FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="69b49-217">FWPM_CONDITION_EMBEDDED_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-217">FWPM_CONDITION_EMBEDDED_LOCAL_PORT</span></span>
- <span data-ttu-id="69b49-218">FWPM_CONDITION_EMBEDDED_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="69b49-218">FWPM_CONDITION_EMBEDDED_PROTOCOL</span></span>
- <span data-ttu-id="69b49-219">FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-219">FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="69b49-220">FWPM_CONDITION_EMBEDDED_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-220">FWPM_CONDITION_EMBEDDED_REMOTE_PORT</span></span>
- <span data-ttu-id="69b49-221">FWPM_CONDITION_IP_ARRIVAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="69b49-221">FWPM_CONDITION_IP_ARRIVAL_INTERFACE</span></span>
- <span data-ttu-id="69b49-222">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-222">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="69b49-223">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="69b49-223">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="69b49-224">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-224">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="69b49-225">FWPM_CONDITION_LOCAL_INTERFACE_INDEX **Windows Vista/Windows 7:** FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="69b49-225">FWPM_CONDITION_LOCAL_INTERFACE_INDEX **Windows Vista / Windows 7:** FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="69b49-226">FWPM_CONDITION_LOCAL_INTERFACE_TYPE **Windows Vista/Windows 7:** FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-226">FWPM_CONDITION_LOCAL_INTERFACE_TYPE **Windows Vista / Windows 7:** FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="69b49-227">FWPM_CONDITION_LOCAL_TUNNEL_TYPE **Windows Vista/Windows 7:** FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-227">FWPM_CONDITION_LOCAL_TUNNEL_TYPE **Windows Vista / Windows 7:** FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="69b49-228">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="69b49-228">Windows 7  and later</span></span>
- <span data-ttu-id="69b49-229">FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-229">FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID</span></span>
## <a name="fwpm_layer_outbound_icmp_error_v4--fwpm_layer_outbound_icmp_error_v4_discard--fwpm_layer_outbound_icmp_error_v6--fwpm_layer_outbound_icmp_error_v6_discard"></a><span data-ttu-id="69b49-230">FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4/FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4_DISCARD/FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6/FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="69b49-230">FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4 / FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4_DISCARD / FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6 / FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6_DISCARD</span></span>
- <span data-ttu-id="69b49-231">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="69b49-231">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="69b49-232">FWPM_CONDITION_ICMP_CODE</span><span class="sxs-lookup"><span data-stu-id="69b49-232">FWPM_CONDITION_ICMP_CODE</span></span>
- <span data-ttu-id="69b49-233">FWPM_CONDITION_ICMP_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-233">FWPM_CONDITION_ICMP_TYPE</span></span>

- <span data-ttu-id="69b49-234">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="69b49-234">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="69b49-235">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-235">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="69b49-236">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-236">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="69b49-237">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-237">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="69b49-238">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="69b49-238">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="69b49-239">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-239">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="69b49-240">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="69b49-240">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="69b49-241">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-241">FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="69b49-242">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="69b49-242">Windows 7  and later</span></span>
- <span data-ttu-id="69b49-243">FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-243">FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID</span></span>
## <a name="fwpm_layer_ale_bind_redirect_v4--fwpm_layer_ale_bind_redirect-v6"></a><span data-ttu-id="69b49-244">FWPM_LAYER_ALE_BIND_REDIRECT_V4/FWPM_LAYER_ALE_BIND_REDIRECT V6</span><span class="sxs-lookup"><span data-stu-id="69b49-244">FWPM_LAYER_ALE_BIND_REDIRECT_V4 / FWPM_LAYER_ALE_BIND_REDIRECT V6</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="69b49-245">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="69b49-245">Windows 7  and later</span></span>
- <span data-ttu-id="69b49-246">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-246">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="69b49-247">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-247">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="69b49-248">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="69b49-248">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="69b49-249">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-249">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="69b49-250">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-250">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="69b49-251">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-251">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="69b49-252">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="69b49-252">FWPM_CONDITION_IP_PROTOCOL</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="69b49-253">Windows 8 e posterior</span><span class="sxs-lookup"><span data-stu-id="69b49-253">Windows 8  and later</span></span>
- <span data-ttu-id="69b49-254">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-254">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_resource_assignment_v4--fwpm_layer_ale_resource_assignment_v4_discard--fwpm_layer_ale_resource_assignment_v6--fwpm_layer_ale_resource_assignment_v6_discard"></a><span data-ttu-id="69b49-255">FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4/FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4_DISCARD/FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6/FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="69b49-255">FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4 / FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4_DISCARD / FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6 / FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6_DISCARD</span></span>
- <span data-ttu-id="69b49-256">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-256">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="69b49-257">FWPM_CONDITION_ALE_PROMISCUOUS_MODE</span><span class="sxs-lookup"><span data-stu-id="69b49-257">FWPM_CONDITION_ALE_PROMISCUOUS_MODE</span></span>
- <span data-ttu-id="69b49-258">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-258">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="69b49-259">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="69b49-259">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="69b49-260">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-260">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="69b49-261">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-261">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="69b49-262">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-262">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="69b49-263">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="69b49-263">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="69b49-264">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-264">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="69b49-265">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="69b49-265">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="69b49-266">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-266">FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="69b49-267">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="69b49-267">Windows 7  and later</span></span>
- <span data-ttu-id="69b49-268">FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-268">FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID</span></span>
- <span data-ttu-id="69b49-269">FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-269">FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="69b49-270">Windows 8 e posterior</span><span class="sxs-lookup"><span data-stu-id="69b49-270">Windows 8  and later</span></span>
- <span data-ttu-id="69b49-271">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-271">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_resource_release_v4--fwpm_layer_ale_resource_release_v6"></a><span data-ttu-id="69b49-272">FWPM_LAYER_ALE_RESOURCE_RELEASE_V4/FWPM_LAYER_ALE_RESOURCE_RELEASE_V6</span><span class="sxs-lookup"><span data-stu-id="69b49-272">FWPM_LAYER_ALE_RESOURCE_RELEASE_V4 / FWPM_LAYER_ALE_RESOURCE_RELEASE_V6</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="69b49-273">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="69b49-273">Windows 7  and later</span></span>
- <span data-ttu-id="69b49-274">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-274">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="69b49-275">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-275">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="69b49-276">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="69b49-276">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="69b49-277">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-277">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="69b49-278">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-278">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="69b49-279">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="69b49-279">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="69b49-280">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-280">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="69b49-281">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="69b49-281">FWPM_CONDITION_IP_PROTOCOL</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="69b49-282">Windows 8 e posterior</span><span class="sxs-lookup"><span data-stu-id="69b49-282">Windows 8  and later</span></span>
- <span data-ttu-id="69b49-283">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-283">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_endpoint_closure_v4--fwpm_layer_ale_endpoint_closure_v6"></a><span data-ttu-id="69b49-284">FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V4/FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V6</span><span class="sxs-lookup"><span data-stu-id="69b49-284">FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V4 / FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V6</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="69b49-285">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="69b49-285">Windows 7  and later</span></span>
- <span data-ttu-id="69b49-286">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-286">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="69b49-287">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-287">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="69b49-288">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="69b49-288">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="69b49-289">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-289">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="69b49-290">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-290">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="69b49-291">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="69b49-291">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="69b49-292">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-292">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="69b49-293">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="69b49-293">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="69b49-294">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-294">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="69b49-295">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-295">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="69b49-296">Windows 8 e posterior</span><span class="sxs-lookup"><span data-stu-id="69b49-296">Windows 8  and later</span></span>
- <span data-ttu-id="69b49-297">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-297">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_auth_listen_v4--fwpm_layer_ale_auth_listen_v4_discard--fwpm_layer_ale_auth_listen_v6--fwpm_layer_ale_auth_listen_v6_discard"></a><span data-ttu-id="69b49-298">FWPM_LAYER_ALE_AUTH_LISTEN_V4/FWPM_LAYER_ALE_AUTH_LISTEN_V4_DISCARD/FWPM_LAYER_ALE_AUTH_LISTEN_V6/FWPM_LAYER_ALE_AUTH_LISTEN_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="69b49-298">FWPM_LAYER_ALE_AUTH_LISTEN_V4 / FWPM_LAYER_ALE_AUTH_LISTEN_V4_DISCARD / FWPM_LAYER_ALE_AUTH_LISTEN_V6 / FWPM_LAYER_ALE_AUTH_LISTEN_V6_DISCARD</span></span>
- <span data-ttu-id="69b49-299">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-299">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="69b49-300">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-300">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="69b49-301">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="69b49-301">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="69b49-302">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-302">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="69b49-303">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-303">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="69b49-304">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-304">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="69b49-305">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="69b49-305">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="69b49-306">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-306">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="69b49-307">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-307">FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="69b49-308">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="69b49-308">Windows 7  and later</span></span>
- <span data-ttu-id="69b49-309">FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-309">FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID</span></span>
- <span data-ttu-id="69b49-310">FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-310">FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="69b49-311">Windows 8 e posterior</span><span class="sxs-lookup"><span data-stu-id="69b49-311">Windows 8  and later</span></span>
- <span data-ttu-id="69b49-312">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-312">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_auth_recv_accept_v4--fwpm_layer_ale_auth_recv_accept_v4_discard--fwpm_layer_ale_auth_recv_accept_v6--fwpm_layer_ale_auth_recv_accept_v6_discard"></a><span data-ttu-id="69b49-313">FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4/FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4_DISCARD/FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6/FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="69b49-313">FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4 / FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4_DISCARD / FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6 / FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6_DISCARD</span></span>
- <span data-ttu-id="69b49-314">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-314">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="69b49-315">FWPM_CONDITION_ALE_NAP_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="69b49-315">FWPM_CONDITION_ALE_NAP_CONTEXT</span></span>
- <span data-ttu-id="69b49-316">FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-316">FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</span></span>
- <span data-ttu-id="69b49-317">FWPM_CONDITION_ALE_REMOTE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-317">FWPM_CONDITION_ALE_REMOTE_USER_ID</span></span>
- <span data-ttu-id="69b49-318">FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-318">FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</span></span>
- <span data-ttu-id="69b49-319">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-319">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="69b49-320">FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="69b49-320">FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX</span></span>
- <span data-ttu-id="69b49-321">FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-321">FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE</span></span>
- <span data-ttu-id="69b49-322">FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX **Windows Vista/Windows 7:** FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="69b49-322">FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX **Windows Vista / Windows 7:** FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="69b49-323">FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-323">FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE</span></span>
- <span data-ttu-id="69b49-324">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="69b49-324">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="69b49-325">FWPM_CONDITION_IP_ARRIVAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="69b49-325">FWPM_CONDITION_IP_ARRIVAL_INTERFACE</span></span>
- <span data-ttu-id="69b49-326">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-326">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="69b49-327">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-327">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="69b49-328">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="69b49-328">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="69b49-329">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-329">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="69b49-330">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="69b49-330">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="69b49-331">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-331">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="69b49-332">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-332">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="69b49-333">FWPM_CONDITION_LOCAL_INTERFACE_INDEX **Windows Vista/Windows 7:** FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="69b49-333">FWPM_CONDITION_LOCAL_INTERFACE_INDEX **Windows Vista / Windows 7:** FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="69b49-334">FWPM_CONDITION_LOCAL_INTERFACE_TYPE **Windows Vista/Windows 7:** FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-334">FWPM_CONDITION_LOCAL_INTERFACE_TYPE **Windows Vista / Windows 7:** FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="69b49-335">FWPM_CONDITION_LOCAL_TUNNEL_TYPE **Windows Vista/Windows 7:** FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-335">FWPM_CONDITION_LOCAL_TUNNEL_TYPE **Windows Vista / Windows 7:** FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="69b49-336">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="69b49-336">Windows 7  and later</span></span>
- <span data-ttu-id="69b49-337">FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="69b49-337">FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="69b49-338">FWPM_CONDITION_IP_NEXTHOP_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="69b49-338">FWPM_CONDITION_IP_NEXTHOP_INTERFACE</span></span>
- <span data-ttu-id="69b49-339">FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-339">FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE</span></span>
- <span data-ttu-id="69b49-340">FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-340">FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE</span></span>
- <span data-ttu-id="69b49-341">FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="69b49-341">FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX</span></span>
- <span data-ttu-id="69b49-342">FWPM_CONDITION_ORIGINAL_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-342">FWPM_CONDITION_ORIGINAL_PROFILE_ID</span></span>
- <span data-ttu-id="69b49-343">FWPM_CONDITION_CURRENT_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-343">FWPM_CONDITION_CURRENT_PROFILE_ID</span></span>
- <span data-ttu-id="69b49-344">FWPM_CONDITION_REAUTHORIZE_REASON</span><span class="sxs-lookup"><span data-stu-id="69b49-344">FWPM_CONDITION_REAUTHORIZE_REASON</span></span>
- <span data-ttu-id="69b49-345">FWPM_CONDITION_ORIGINAL_ICMP_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-345">FWPM_CONDITION_ORIGINAL_ICMP_TYPE</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="69b49-346">Windows 8 e posterior</span><span class="sxs-lookup"><span data-stu-id="69b49-346">Windows 8  and later</span></span>
- <span data-ttu-id="69b49-347">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-347">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_connect_redirect_v4--fwpm_layer_ale_connect_redirect-v6"></a><span data-ttu-id="69b49-348">FWPM_LAYER_ALE_CONNECT_REDIRECT_V4/FWPM_LAYER_ALE_CONNECT_REDIRECT V6</span><span class="sxs-lookup"><span data-stu-id="69b49-348">FWPM_LAYER_ALE_CONNECT_REDIRECT_V4 / FWPM_LAYER_ALE_CONNECT_REDIRECT V6</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="69b49-349">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="69b49-349">Windows 7  and later</span></span>
- <span data-ttu-id="69b49-350">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-350">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="69b49-351">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-351">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="69b49-352">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="69b49-352">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="69b49-353">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-353">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="69b49-354">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-354">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="69b49-355">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-355">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="69b49-356">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="69b49-356">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="69b49-357">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-357">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="69b49-358">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-358">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="69b49-359">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-359">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="69b49-360">Windows 8 e posterior</span><span class="sxs-lookup"><span data-stu-id="69b49-360">Windows 8  and later</span></span>
- <span data-ttu-id="69b49-361">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-361">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_auth_connect_v4--fwpm_layer_ale_auth_connect_v4_discard--fwpm_layer_ale_auth_connect_v6--fwpm_layer_ale_auth_connect_v6_discard"></a><span data-ttu-id="69b49-362">FWPM_LAYER_ALE_AUTH_CONNECT_V4/FWPM_LAYER_ALE_AUTH_CONNECT_V4_DISCARD/FWPM_LAYER_ALE_AUTH_CONNECT_V6/FWPM_LAYER_ALE_AUTH_CONNECT_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="69b49-362">FWPM_LAYER_ALE_AUTH_CONNECT_V4 / FWPM_LAYER_ALE_AUTH_CONNECT_V4_DISCARD / FWPM_LAYER_ALE_AUTH_CONNECT_V6 / FWPM_LAYER_ALE_AUTH_CONNECT_V6_DISCARD</span></span>
- <span data-ttu-id="69b49-363">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-363">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="69b49-364">FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-364">FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</span></span>
- <span data-ttu-id="69b49-365">FWPM_CONDITION_ALE_REMOTE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-365">FWPM_CONDITION_ALE_REMOTE_USER_ID</span></span>
- <span data-ttu-id="69b49-366">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-366">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="69b49-367">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="69b49-367">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="69b49-368">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-368">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="69b49-369">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-369">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span></span>
- <span data-ttu-id="69b49-370">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-370">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="69b49-371">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-371">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="69b49-372">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="69b49-372">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="69b49-373">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-373">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="69b49-374">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="69b49-374">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="69b49-375">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-375">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="69b49-376">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-376">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="69b49-377">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="69b49-377">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="69b49-378">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-378">FWPM_CONDITION_TUNNEL_TYPE</span></span>
- <span data-ttu-id="69b49-379">FWPM_CONDITION_IP_ARRIVAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="69b49-379">FWPM_CONDITION_IP_ARRIVAL_INTERFACE</span></span>
- <span data-ttu-id="69b49-380">FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-380">FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE</span></span>
- <span data-ttu-id="69b49-381">FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-381">FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE</span></span>
- <span data-ttu-id="69b49-382">FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX Windows Vista _sp1 e laterFWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="69b49-382">FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX Windows Vista _sp1 and laterFWPM_CONDITION_INTERFACE_INDEX</span></span> 
###  <a name="windows-7--and-later"></a><span data-ttu-id="69b49-383">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="69b49-383">Windows 7  and later</span></span>
- <span data-ttu-id="69b49-384">FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="69b49-384">FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="69b49-385">FWPM_CONDITION_IP_NEXTHOP_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="69b49-385">FWPM_CONDITION_IP_NEXTHOP_INTERFACE</span></span>
- <span data-ttu-id="69b49-386">FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-386">FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE</span></span>
- <span data-ttu-id="69b49-387">FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-387">FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE</span></span>
- <span data-ttu-id="69b49-388">FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="69b49-388">FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX</span></span>
- <span data-ttu-id="69b49-389">FWPM_CONDITION_ORIGINAL_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-389">FWPM_CONDITION_ORIGINAL_PROFILE_ID</span></span>
- <span data-ttu-id="69b49-390">FWPM_CONDITION_CURRENT_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-390">FWPM_CONDITION_CURRENT_PROFILE_ID</span></span>
- <span data-ttu-id="69b49-391">FWPM_CONDITION_REAUTHORIZE_REASON</span><span class="sxs-lookup"><span data-stu-id="69b49-391">FWPM_CONDITION_REAUTHORIZE_REASON</span></span>
- <span data-ttu-id="69b49-392">FWPM_CONDITION_PEER_NAME</span><span class="sxs-lookup"><span data-stu-id="69b49-392">FWPM_CONDITION_PEER_NAME</span></span>
- <span data-ttu-id="69b49-393">FWPM_CONDITION_ORIGINAL_ICMP_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-393">FWPM_CONDITION_ORIGINAL_ICMP_TYPE</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="69b49-394">Windows 8 e posterior</span><span class="sxs-lookup"><span data-stu-id="69b49-394">Windows 8  and later</span></span>
- <span data-ttu-id="69b49-395">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-395">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_flow_established_v4--fwpm_layer_ale_flow_established_v4_discard--fwpm_layer_ale_flow_established_v6--fwpm_layer_ale_flow_established_v6_discard"></a><span data-ttu-id="69b49-396">FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4/FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4_DISCARD/FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6/FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="69b49-396">FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4 / FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4_DISCARD / FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6 / FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6_DISCARD</span></span>
- <span data-ttu-id="69b49-397">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-397">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="69b49-398">FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-398">FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</span></span>
- <span data-ttu-id="69b49-399">FWPM_CONDITION_ALE_REMOTE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-399">FWPM_CONDITION_ALE_REMOTE_USER_ID</span></span>
- <span data-ttu-id="69b49-400">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-400">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="69b49-401">FWPM_CONDITION_DIRECTION</span><span class="sxs-lookup"><span data-stu-id="69b49-401">FWPM_CONDITION_DIRECTION</span></span>
- <span data-ttu-id="69b49-402">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="69b49-402">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="69b49-403">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-403">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="69b49-404">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-404">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span></span>
- <span data-ttu-id="69b49-405">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-405">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="69b49-406">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-406">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="69b49-407">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="69b49-407">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="69b49-408">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-408">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="69b49-409">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="69b49-409">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="69b49-410">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-410">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="69b49-411">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-411">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="69b49-412">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-412">FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="69b49-413">Windows 8 e posterior</span><span class="sxs-lookup"><span data-stu-id="69b49-413">Windows 8  and later</span></span>
- <span data-ttu-id="69b49-414">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-414">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_name_resolution_cache_v4--fwpm_layer_name_resolution_cache_v6"></a><span data-ttu-id="69b49-415">FWPM_LAYER_NAME_RESOLUTION_CACHE_V4/FWPM_LAYER_NAME_RESOLUTION_CACHE_V6</span><span class="sxs-lookup"><span data-stu-id="69b49-415">FWPM_LAYER_NAME_RESOLUTION_CACHE_V4 / FWPM_LAYER_NAME_RESOLUTION_CACHE_V6</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="69b49-416">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="69b49-416">Windows 7  and later</span></span>
- <span data-ttu-id="69b49-417">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-417">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="69b49-418">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-418">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="69b49-419">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-419">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="69b49-420">FWPM_CONDITION_PEER_NAME</span><span class="sxs-lookup"><span data-stu-id="69b49-420">FWPM_CONDITION_PEER_NAME</span></span>
## <a name="fwpm_layer_ipsec_km_demux_v4--fwpm_layer_ipsec_km_demux_v6"></a><span data-ttu-id="69b49-421">FWPM_LAYER_IPSEC_KM_DEMUX_V4/FWPM_LAYER_IPSEC_KM_DEMUX_V6</span><span class="sxs-lookup"><span data-stu-id="69b49-421">FWPM_LAYER_IPSEC_KM_DEMUX_V4 / FWPM_LAYER_IPSEC_KM_DEMUX_V6</span></span>
- <span data-ttu-id="69b49-422">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-422">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="69b49-423">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-423">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
## <a name="fwpm_layer_ipsec_v4--fwpm_layer_ipsec_v6"></a><span data-ttu-id="69b49-424">FWPM_LAYER_IPSEC_V4/FWPM_LAYER_IPSEC_V6</span><span class="sxs-lookup"><span data-stu-id="69b49-424">FWPM_LAYER_IPSEC_V4 / FWPM_LAYER_IPSEC_V6</span></span>
- <span data-ttu-id="69b49-425">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-425">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="69b49-426">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-426">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="69b49-427">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="69b49-427">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="69b49-428">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-428">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="69b49-429">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-429">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="69b49-430">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="69b49-430">Windows 7  and later</span></span>
- <span data-ttu-id="69b49-431">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="69b49-431">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="69b49-432">FWPM_CONDITION_CURRENT_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-432">FWPM_CONDITION_CURRENT_PROFILE_ID</span></span>
## <a name="fwpm_layer_ikeext_v4--fwpm_layer_ikeext_v6"></a><span data-ttu-id="69b49-433">FWPM_LAYER_IKEEXT_V4/FWPM_LAYER_IKEEXT_V6</span><span class="sxs-lookup"><span data-stu-id="69b49-433">FWPM_LAYER_IKEEXT_V4 / FWPM_LAYER_IKEEXT_V6</span></span>
- <span data-ttu-id="69b49-434">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-434">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="69b49-435">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-435">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="69b49-436">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="69b49-436">Windows 7  and later</span></span>
- <span data-ttu-id="69b49-437">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="69b49-437">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="69b49-438">FWPM_CONDITION_CURRENT_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-438">FWPM_CONDITION_CURRENT_PROFILE_ID</span></span>
## <a name="fwpm_layer_rpc_um"></a><span data-ttu-id="69b49-439">FWPM_LAYER_RPC_UM</span><span class="sxs-lookup"><span data-stu-id="69b49-439">FWPM_LAYER_RPC_UM</span></span>
- <span data-ttu-id="69b49-440">FWPM_CONDITION_DCOM_APP_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-440">FWPM_CONDITION_DCOM_APP_ID</span></span>
- <span data-ttu-id="69b49-441">FWPM_CONDITION_IMAGE_NAME</span><span class="sxs-lookup"><span data-stu-id="69b49-441">FWPM_CONDITION_IMAGE_NAME</span></span>
- <span data-ttu-id="69b49-442">FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</span><span class="sxs-lookup"><span data-stu-id="69b49-442">FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</span></span>
- <span data-ttu-id="69b49-443">FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</span><span class="sxs-lookup"><span data-stu-id="69b49-443">FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</span></span>
- <span data-ttu-id="69b49-444">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-444">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="69b49-445">FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</span><span class="sxs-lookup"><span data-stu-id="69b49-445">FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</span></span>
- <span data-ttu-id="69b49-446">FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</span><span class="sxs-lookup"><span data-stu-id="69b49-446">FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</span></span>
- <span data-ttu-id="69b49-447">FWPM_CONDITION_PIPE</span><span class="sxs-lookup"><span data-stu-id="69b49-447">FWPM_CONDITION_PIPE</span></span>
- <span data-ttu-id="69b49-448">FWPM_CONDITION_REMOTE_USER_TOKEN</span><span class="sxs-lookup"><span data-stu-id="69b49-448">FWPM_CONDITION_REMOTE_USER_TOKEN</span></span>
- <span data-ttu-id="69b49-449">FWPM_CONDITION_RPC_AUTH_LEVEL</span><span class="sxs-lookup"><span data-stu-id="69b49-449">FWPM_CONDITION_RPC_AUTH_LEVEL</span></span>
- <span data-ttu-id="69b49-450">FWPM_CONDITION_RPC_AUTH_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-450">FWPM_CONDITION_RPC_AUTH_TYPE</span></span>
- <span data-ttu-id="69b49-451">FWPM_CONDITION_RPC_IF_FLAG</span><span class="sxs-lookup"><span data-stu-id="69b49-451">FWPM_CONDITION_RPC_IF_FLAG</span></span>
- <span data-ttu-id="69b49-452">FWPM_CONDITION_RPC_IF_UUID</span><span class="sxs-lookup"><span data-stu-id="69b49-452">FWPM_CONDITION_RPC_IF_UUID</span></span>
- <span data-ttu-id="69b49-453">FWPM_CONDITION_RPC_IF_VERSION</span><span class="sxs-lookup"><span data-stu-id="69b49-453">FWPM_CONDITION_RPC_IF_VERSION</span></span>
- <span data-ttu-id="69b49-454">FWPM_CONDITION_RPC_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="69b49-454">FWPM_CONDITION_RPC_PROTOCOL</span></span>
- <span data-ttu-id="69b49-455">FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</span><span class="sxs-lookup"><span data-stu-id="69b49-455">FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</span></span>
- <span data-ttu-id="69b49-456">FWPM_CONDITION_SEC_KEY_SIZE</span><span class="sxs-lookup"><span data-stu-id="69b49-456">FWPM_CONDITION_SEC_KEY_SIZE</span></span>
## <a name="fwpm_layer_rpc_epmap"></a><span data-ttu-id="69b49-457">FWPM_LAYER_RPC_EPMAP</span><span class="sxs-lookup"><span data-stu-id="69b49-457">FWPM_LAYER_RPC_EPMAP</span></span>
- <span data-ttu-id="69b49-458">FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</span><span class="sxs-lookup"><span data-stu-id="69b49-458">FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</span></span>
- <span data-ttu-id="69b49-459">FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</span><span class="sxs-lookup"><span data-stu-id="69b49-459">FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</span></span>
- <span data-ttu-id="69b49-460">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-460">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="69b49-461">FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</span><span class="sxs-lookup"><span data-stu-id="69b49-461">FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</span></span>
- <span data-ttu-id="69b49-462">FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</span><span class="sxs-lookup"><span data-stu-id="69b49-462">FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</span></span>

- <span data-ttu-id="69b49-463">FWPM_CONDITION_PIPE</span><span class="sxs-lookup"><span data-stu-id="69b49-463">FWPM_CONDITION_PIPE</span></span>
- <span data-ttu-id="69b49-464">FWPM_CONDITION_REMOTE_USER_TOKEN</span><span class="sxs-lookup"><span data-stu-id="69b49-464">FWPM_CONDITION_REMOTE_USER_TOKEN</span></span>
- <span data-ttu-id="69b49-465">FWPM_CONDITION_RPC_AUTH_LEVEL</span><span class="sxs-lookup"><span data-stu-id="69b49-465">FWPM_CONDITION_RPC_AUTH_LEVEL</span></span>
- <span data-ttu-id="69b49-466">FWPM_CONDITION_RPC_AUTH_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-466">FWPM_CONDITION_RPC_AUTH_TYPE</span></span>
- <span data-ttu-id="69b49-467">FWPM_CONDITION_RPC_IF_UUID</span><span class="sxs-lookup"><span data-stu-id="69b49-467">FWPM_CONDITION_RPC_IF_UUID</span></span>
- <span data-ttu-id="69b49-468">FWPM_CONDITION_RPC_IF_VERSION</span><span class="sxs-lookup"><span data-stu-id="69b49-468">FWPM_CONDITION_RPC_IF_VERSION</span></span>
- <span data-ttu-id="69b49-469">FWPM_CONDITION_RPC_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="69b49-469">FWPM_CONDITION_RPC_PROTOCOL</span></span>
- <span data-ttu-id="69b49-470">FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</span><span class="sxs-lookup"><span data-stu-id="69b49-470">FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</span></span>
- <span data-ttu-id="69b49-471">FWPM_CONDITION_SEC_KEY_SIZE</span><span class="sxs-lookup"><span data-stu-id="69b49-471">FWPM_CONDITION_SEC_KEY_SIZE</span></span>
## <a name="fwpm_layer_rpc_ep_add"></a><span data-ttu-id="69b49-472">FWPM_LAYER_RPC_EP_ADD</span><span class="sxs-lookup"><span data-stu-id="69b49-472">FWPM_LAYER_RPC_EP_ADD</span></span>
- <span data-ttu-id="69b49-473">FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID</span><span class="sxs-lookup"><span data-stu-id="69b49-473">FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID</span></span>
- <span data-ttu-id="69b49-474">FWPM_CONDITION_RPC_EP_FLAGS</span><span class="sxs-lookup"><span data-stu-id="69b49-474">FWPM_CONDITION_RPC_EP_FLAGS</span></span>
- <span data-ttu-id="69b49-475">FWPM_CONDITION_RPC_EP_VALUE</span><span class="sxs-lookup"><span data-stu-id="69b49-475">FWPM_CONDITION_RPC_EP_VALUE</span></span>
- <span data-ttu-id="69b49-476">FWPM_CONDITION_RPC_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="69b49-476">FWPM_CONDITION_RPC_PROTOCOL</span></span>
## <a name="fwpm_layer_rpc_proxy_conn"></a><span data-ttu-id="69b49-477">FWPM_LAYER_RPC_PROXY_CONN</span><span class="sxs-lookup"><span data-stu-id="69b49-477">FWPM_LAYER_RPC_PROXY_CONN</span></span>
- <span data-ttu-id="69b49-478">FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</span><span class="sxs-lookup"><span data-stu-id="69b49-478">FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</span></span>
- <span data-ttu-id="69b49-479">FWPM_CONDITION_CLIENT_CERT_OID</span><span class="sxs-lookup"><span data-stu-id="69b49-479">FWPM_CONDITION_CLIENT_CERT_OID</span></span>
- <span data-ttu-id="69b49-480">FWPM_CONDITION_CLIENT_TOKEN</span><span class="sxs-lookup"><span data-stu-id="69b49-480">FWPM_CONDITION_CLIENT_TOKEN</span></span>
- <span data-ttu-id="69b49-481">FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-481">FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</span></span>
- <span data-ttu-id="69b49-482">FWPM_CONDITION_RPC_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="69b49-482">FWPM_CONDITION_RPC_SERVER_NAME</span></span>
- <span data-ttu-id="69b49-483">FWPM_CONDITION_RPC_SERVER_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-483">FWPM_CONDITION_RPC_SERVER_PORT</span></span>
## <a name="fwpm_layer_rpc_proxy_if"></a><span data-ttu-id="69b49-484">FWPM_LAYER_RPC_PROXY_IF</span><span class="sxs-lookup"><span data-stu-id="69b49-484">FWPM_LAYER_RPC_PROXY_IF</span></span>
- <span data-ttu-id="69b49-485">FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</span><span class="sxs-lookup"><span data-stu-id="69b49-485">FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</span></span>
- <span data-ttu-id="69b49-486">FWPM_CONDITION_CLIENT_CERT_OID</span><span class="sxs-lookup"><span data-stu-id="69b49-486">FWPM_CONDITION_CLIENT_CERT_OID</span></span>
- <span data-ttu-id="69b49-487">FWPM_CONDITION_CLIENT_TOKEN</span><span class="sxs-lookup"><span data-stu-id="69b49-487">FWPM_CONDITION_CLIENT_TOKEN</span></span>
- <span data-ttu-id="69b49-488">FWPM_CONDITION_RPC_IF_UUID</span><span class="sxs-lookup"><span data-stu-id="69b49-488">FWPM_CONDITION_RPC_IF_UUID</span></span>
- <span data-ttu-id="69b49-489">FWPM_CONDITION_RPC_IF_VERSION</span><span class="sxs-lookup"><span data-stu-id="69b49-489">FWPM_CONDITION_RPC_IF_VERSION</span></span>
- <span data-ttu-id="69b49-490">FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-490">FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</span></span>
- <span data-ttu-id="69b49-491">FWPM_CONDITION_RPC_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="69b49-491">FWPM_CONDITION_RPC_SERVER_NAME</span></span>
- <span data-ttu-id="69b49-492">FWPM_CONDITION_RPC_SERVER_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-492">FWPM_CONDITION_RPC_SERVER_PORT</span></span>
## <a name="fwpm_layer_km_authorization"></a><span data-ttu-id="69b49-493">FWPM_LAYER_KM_AUTHORIZATION</span><span class="sxs-lookup"><span data-stu-id="69b49-493">FWPM_LAYER_KM_AUTHORIZATION</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="69b49-494">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="69b49-494">Windows 7  and later</span></span>
- <span data-ttu-id="69b49-495">FWPM_CONDITION_REMOTE_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-495">FWPM_CONDITION_REMOTE_ID</span></span>
- <span data-ttu-id="69b49-496">FWPM_CONDITION_AUTHENTICATION_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-496">FWPM_CONDITION_AUTHENTICATION_TYPE</span></span>
- <span data-ttu-id="69b49-497">FWPM_CONDITION_KM_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-497">FWPM_CONDITION_KM_TYPE</span></span>
- <span data-ttu-id="69b49-498">FWPM_CONDITION_KM_MODE</span><span class="sxs-lookup"><span data-stu-id="69b49-498">FWPM_CONDITION_KM_MODE</span></span>
- <span data-ttu-id="69b49-499">FWPM_CONDITION_DIRECTION</span><span class="sxs-lookup"><span data-stu-id="69b49-499">FWPM_CONDITION_DIRECTION</span></span>
- <span data-ttu-id="69b49-500">FWPM_CONDITION_IPSEC_POLICY_KEY</span><span class="sxs-lookup"><span data-stu-id="69b49-500">FWPM_CONDITION_IPSEC_POLICY_KEY</span></span>
## <a name="fwpm_layer_inbound_mac_frame_ethernet--fwpm_layer_outbound_mac_frame_ethernet"></a><span data-ttu-id="69b49-501">FWPM_LAYER_INBOUND_MAC_FRAME_ETHERNET/FWPM_LAYER_OUTBOUND_MAC_FRAME_ETHERNET</span><span class="sxs-lookup"><span data-stu-id="69b49-501">FWPM_LAYER_INBOUND_MAC_FRAME_ETHERNET / FWPM_LAYER_OUTBOUND_MAC_FRAME_ETHERNET</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="69b49-502">Windows 8 e posterior</span><span class="sxs-lookup"><span data-stu-id="69b49-502">Windows 8  and later</span></span>
- <span data-ttu-id="69b49-503">FWPM_CONDITION_INTERFACE_MAC_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-503">FWPM_CONDITION_INTERFACE_MAC_ADDRESS</span></span>
- <span data-ttu-id="69b49-504">FWPM_CONDITION_MAC_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-504">FWPM_CONDITION_MAC_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="69b49-505">FWPM_CONDITION_MAC_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-505">FWPM_CONDITION_MAC_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="69b49-506">FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-506">FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="69b49-507">FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-507">FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE</span></span>
- <span data-ttu-id="69b49-508">FWPM_CONDITION_ETHER_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-508">FWPM_CONDITION_ETHER_TYPE</span></span>
- <span data-ttu-id="69b49-509">FWPM_CONDITION_VLAN_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-509">FWPM_CONDITION_VLAN_ID</span></span>
- <span data-ttu-id="69b49-510">FWPM_CONDITION_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="69b49-510">FWPM_CONDITION_INTERFACE</span></span>
- <span data-ttu-id="69b49-511">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="69b49-511">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="69b49-512">FWPM_CONDITION_NDIS_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-512">FWPM_CONDITION_NDIS_PORT</span></span>
- <span data-ttu-id="69b49-513">FWPM_CONDITION_L2_FLAGS</span><span class="sxs-lookup"><span data-stu-id="69b49-513">FWPM_CONDITION_L2_FLAGS</span></span>
##  <a name="fwpm_layer_inbound_mac_frame_native--fwpm_layer_outbound_mac_frame_native"></a><span data-ttu-id="69b49-514">FWPM_LAYER_INBOUND_MAC_FRAME_NATIVE/FWPM_LAYER_OUTBOUND_MAC_FRAME_NATIVE</span><span class="sxs-lookup"><span data-stu-id="69b49-514">FWPM_LAYER_INBOUND_MAC_FRAME_NATIVE / FWPM_LAYER_OUTBOUND_MAC_FRAME_NATIVE</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="69b49-515">Windows 8 e posterior</span><span class="sxs-lookup"><span data-stu-id="69b49-515">Windows 8  and later</span></span>
- <span data-ttu-id="69b49-516">FWPM_CONDITION_NDIS_MEDIA_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-516">FWPM_CONDITION_NDIS_MEDIA_TYPE</span></span>
- <span data-ttu-id="69b49-517">FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-517">FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE</span></span>
- <span data-ttu-id="69b49-518">FWPM_CONDITION_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="69b49-518">FWPM_CONDITION_INTERFACE</span></span>
- <span data-ttu-id="69b49-519">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-519">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="69b49-520">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="69b49-520">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="69b49-521">FWPM_CONDITION_NDIS_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-521">FWPM_CONDITION_NDIS_PORT</span></span>
- <span data-ttu-id="69b49-522">FWPM_CONDITION_L2_FLAGS</span><span class="sxs-lookup"><span data-stu-id="69b49-522">FWPM_CONDITION_L2_FLAGS</span></span>
## <a name="fwpm_layer_egress_vswitch_ethernet--fwpm_layer_ingress_vswitch_ethernet"></a><span data-ttu-id="69b49-523">FWPM_LAYER_EGRESS_VSWITCH_ETHERNET/FWPM_LAYER_INGRESS_VSWITCH_ETHERNET</span><span class="sxs-lookup"><span data-stu-id="69b49-523">FWPM_LAYER_EGRESS_VSWITCH_ETHERNET / FWPM_LAYER_INGRESS_VSWITCH_ETHERNET</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="69b49-524">Windows 8 e posterior</span><span class="sxs-lookup"><span data-stu-id="69b49-524">Windows 8  and later</span></span>
- <span data-ttu-id="69b49-525">FWPM_CONDITION_MAC_SOURCE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-525">FWPM_CONDITION_MAC_SOURCE_ADDRESS</span></span>
- <span data-ttu-id="69b49-526">FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-526">FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE</span></span>
- <span data-ttu-id="69b49-527">FWPM_CONDITION_MAC_DESTINATION_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-527">FWPM_CONDITION_MAC_DESTINATION_ADDRESS</span></span>
- <span data-ttu-id="69b49-528">FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-528">FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE</span></span>
- <span data-ttu-id="69b49-529">FWPM_CONDITION_ETHER_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-529">FWPM_CONDITION_ETHER_TYPE</span></span>
- <span data-ttu-id="69b49-530">FWPM_CONDITION_VLAN_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-530">FWPM_CONDITION_VLAN_ID</span></span>
- <span data-ttu-id="69b49-531">FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-531">FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</span></span>
- <span data-ttu-id="69b49-532">FWPM_CONDITION_VSWITCH_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-532">FWPM_CONDITION_VSWITCH_ID</span></span>
- <span data-ttu-id="69b49-533">FWPM_CONDITION_VSWITCH_NETWORK_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-533">FWPM_CONDITION_VSWITCH_NETWORK_TYPE</span></span>
- <span data-ttu-id="69b49-534">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-534">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</span></span>
- <span data-ttu-id="69b49-535">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-535">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</span></span>
- <span data-ttu-id="69b49-536">FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-536">FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</span></span>
- <span data-ttu-id="69b49-537">FWPM_CONDITION_VSWITCH_L2_FLAGS</span><span class="sxs-lookup"><span data-stu-id="69b49-537">FWPM_CONDITION_VSWITCH_L2_FLAGS</span></span>
##  <a name="fwpm_layer_egress_vswitch_transport_v4--fwpm_layer_ingress_vswitch_transport_v4--fwpm_layer_egressvswitch_transport_v6--fwpm_layer_ingress_vswitch_transport_v6"></a><span data-ttu-id="69b49-538">FWPM_LAYER_EGRESS_VSWITCH_TRANSPORT_V4/FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V4/FWPM_LAYER_EGRESSVSWITCH_TRANSPORT_V6/FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V6</span><span class="sxs-lookup"><span data-stu-id="69b49-538">FWPM_LAYER_EGRESS_VSWITCH_TRANSPORT_V4 / FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V4 / FWPM_LAYER_EGRESSVSWITCH_TRANSPORT_V6 / FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V6</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="69b49-539">Windows 8 e posterior</span><span class="sxs-lookup"><span data-stu-id="69b49-539">Windows 8  and later</span></span>
- <span data-ttu-id="69b49-540">FWPM_CONDITION_IP_SOURCE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-540">FWPM_CONDITION_IP_SOURCE_ADDRESS</span></span>
- <span data-ttu-id="69b49-541">FWPM_CONDITION_IP_DESTINATION_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="69b49-541">FWPM_CONDITION_IP_DESTINATION_ADDRESS</span></span>
- <span data-ttu-id="69b49-542">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="69b49-542">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="69b49-543">FWPM_CONDITION_IP_SOURCE_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-543">FWPM_CONDITION_IP_SOURCE_PORT</span></span>
- <span data-ttu-id="69b49-544">FWPM_CONDITION_IP_DESTINATION_PORT</span><span class="sxs-lookup"><span data-stu-id="69b49-544">FWPM_CONDITION_IP_DESTINATION_PORT</span></span>
- <span data-ttu-id="69b49-545">FWPM_CONDITION_VLAN_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-545">FWPM_CONDITION_VLAN_ID</span></span>
- <span data-ttu-id="69b49-546">FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-546">FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</span></span>
- <span data-ttu-id="69b49-547">FWPM_CONDITION_VSWITCH_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-547">FWPM_CONDITION_VSWITCH_ID</span></span>
- <span data-ttu-id="69b49-548">FWPM_CONDITION_VSWITCH_NETWORK_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-548">FWPM_CONDITION_VSWITCH_NETWORK_TYPE</span></span>
- <span data-ttu-id="69b49-549">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-549">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</span></span>
- <span data-ttu-id="69b49-550">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-550">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</span></span>
- <span data-ttu-id="69b49-551">FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-551">FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</span></span>
- <span data-ttu-id="69b49-552">FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID</span><span class="sxs-lookup"><span data-stu-id="69b49-552">FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID</span></span>
- <span data-ttu-id="69b49-553">FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b49-553">FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="69b49-554">FWPM_CONDITION_VSWITCH_L2_FLAGS</span><span class="sxs-lookup"><span data-stu-id="69b49-554">FWPM_CONDITION_VSWITCH_L2_FLAGS</span></span>



## <a name="remarks"></a><span data-ttu-id="69b49-555">Comentários</span><span class="sxs-lookup"><span data-stu-id="69b49-555">Remarks</span></span>

<span data-ttu-id="69b49-556">Os sufixos v4 e V6 no final dos identificadores de camada indicam se a camada está localizada na pilha de rede IPv4 ou na pilha de rede IPv6.</span><span class="sxs-lookup"><span data-stu-id="69b49-556">The V4 and V6 suffixes at the end of the layer identifiers indicate whether the layer is located in the IPv4 network stack or in the IPv6 network stack.</span></span>

## <a name="requirements"></a><span data-ttu-id="69b49-557">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69b49-557">Requirements</span></span>



| <span data-ttu-id="69b49-558">Requisito</span><span class="sxs-lookup"><span data-stu-id="69b49-558">Requirement</span></span> | <span data-ttu-id="69b49-559">Valor</span><span class="sxs-lookup"><span data-stu-id="69b49-559">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="69b49-560">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69b49-560">Minimum supported client</span></span><br/> | <span data-ttu-id="69b49-561">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="69b49-561">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="69b49-562">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69b49-562">Minimum supported server</span></span><br/> | <span data-ttu-id="69b49-563">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="69b49-563">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="69b49-564">parâmetro</span><span class="sxs-lookup"><span data-stu-id="69b49-564">Header</span></span><br/>                   | <dl> <span data-ttu-id="69b49-565"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="69b49-565"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 






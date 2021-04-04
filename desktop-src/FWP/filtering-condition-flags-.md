---
title: Filtrando sinalizadores de condição (Fwptypes. h)
description: Os sinalizadores de condição de filtragem da WFP (Windows Filtering Platform) são representados por um campo de bits.
ms.assetid: fe879479-331d-42ef-ac2f-634f0c13c21d
topic_type:
- apiref
api_name:
- FWP_CONDITION_FLAG_IS_LOOPBACK
- FWP_CONDITION_FLAG_IS_IPSEC_SECURED
- FWP_CONDITION_FLAG_IS_REAUTHORIZE
- FWP_CONDITION_FLAG_IS_WILDCARD_BIND
- FWP_CONDITION_FLAG_IS_RAW_ENDPOINT
- FWP_CONDITION_FLAG_IS_FRAGMENT
- FWP_CONDITION_FLAG_IS_FRAGMENT_GROUP
- FWP_CONDITION_FLAG_IS_IPSEC_NATT_RECLASSIFY
- FWP_CONDITION_FLAG_REQUIRES_ALE_CLASSIFY
- FWP_CONDITION_FLAG_IS_IMPLICIT_BIND
- FWP_CONDITION_FLAG_IS_REASSEMBLED
- FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED
- FWP_CONDITION_FLAG_IS_PROMISCUOUS
- FWP_CONDITION_FLAG_IS_AUTH_FW
- FWP_CONDITION_FLAG_IS_RECLASSIFY
- FWP_CONDITION_FLAG_IS_PROXY_CONNECTION
- FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK
- FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK
- FWP_CONDITION_FLAG_IS_RESERVED
- FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE
- FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE
- FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE
- FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE
- FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING
- FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION
- FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED
- FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION
- FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED
- FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET
- FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC
- FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC
- FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC
- FWP_CONDITION_L2_IS_NATIVE_ETHERNET
- FWP_CONDITION_L2_IS_WIFI
- FWP_CONDITION_L2_IS_MOBILE_BROADBAND
- FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA
- FWP_CONDITION_L2_IS_VM2VM
- FWP_CONDITION_L2_IS_MALFORMED_PACKET
- FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP
- FWP_CONDITION_L2_IF_CONNECTOR_PRESENT
api_location:
- fwptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c88fa56f37332d52ed31f5ef042c5064a82ac4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645062"
---
# <a name="filtering-condition-flags"></a><span data-ttu-id="61f78-103">Filtrando sinalizadores de condição</span><span class="sxs-lookup"><span data-stu-id="61f78-103">Filtering Condition Flags</span></span>

<span data-ttu-id="61f78-104">Os sinalizadores de condição de filtragem da WFP (Windows Filtering Platform) são representados por um campo de bits.</span><span class="sxs-lookup"><span data-stu-id="61f78-104">The Windows Filtering Platform (WFP) filtering condition flags are each represented by a bitfield.</span></span>

<span data-ttu-id="61f78-105">Esses sinalizadores e as camadas de filtragem em que podem ser usados são definidos da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="61f78-105">These flags and the filtering layers where they can be used are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="61f78-106"><span id="FWP_CONDITION_FLAG_IS_LOOPBACK"></span><span id="fwp_condition_flag_is_loopback"></span>**o \_ sinalizador de condição fwp \_ \_ é \_ loopback**</span><span class="sxs-lookup"><span data-stu-id="61f78-106"><span id="FWP_CONDITION_FLAG_IS_LOOPBACK"></span><span id="fwp_condition_flag_is_loopback"></span>**FWP\_CONDITION\_FLAG\_IS\_LOOPBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-107">Testa se o tráfego de rede é tráfego de loopback.</span><span class="sxs-lookup"><span data-stu-id="61f78-107">Tests if the network traffic is loopback traffic.</span></span>

<span data-ttu-id="61f78-108">Filtrando camadas:</span><span class="sxs-lookup"><span data-stu-id="61f78-108">Filtering layers:</span></span>

-   <span data-ttu-id="61f78-109">FWPM de \_ entrada da camada de \_ \_ IPPACKET \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-109">FWPM\_LAYER\_INBOUND\_IPPACKET\_V{4\|6}</span></span>
-   <span data-ttu-id="61f78-110">FWPM de \_ saída da camada de \_ \_ IPPACKET \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-110">FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V{4\|6}</span></span>
-   <span data-ttu-id="61f78-111">\_Transporte de entrada da camada FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-111">FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6}</span></span>
-   <span data-ttu-id="61f78-112">\_Transporte de saída da camada FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-112">FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6}</span></span>
-   <span data-ttu-id="61f78-113">Fluxo da camada de FWPM \_ \_ \_ {v4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-113">FWPM\_LAYER\_STREAM\_{V4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="61f78-114">Disponível apenas no Windows Server 2008, Windows Vista com SP1 e posterior.</span><span class="sxs-lookup"><span data-stu-id="61f78-114">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="61f78-115">\_Erro de ICMP de entrada na camada FWPM \_ \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-115">FWPM\_LAYER\_INBOUND\_ICMP\_ERROR\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="61f78-116">Disponível apenas no Windows Server 2008, Windows Vista com SP1 e posterior.</span><span class="sxs-lookup"><span data-stu-id="61f78-116">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="61f78-117">Erro de ICMP de saída de camada de FWPM \_ \_ \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-117">FWPM\_LAYER\_OUTBOUND\_ICMP\_ERROR\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="61f78-118">Disponível apenas no Windows Server 2008, Windows Vista com SP1 e posterior.</span><span class="sxs-lookup"><span data-stu-id="61f78-118">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="61f78-119">\_Aceitação da autenticação Ale de camada FWPM de \_ \_ \_ recebimento \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-119">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>
-   <span data-ttu-id="61f78-120">\_Conexão de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-120">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="61f78-121">Disponível apenas no Windows Server 2008, Windows Vista com SP1 e posterior.</span><span class="sxs-lookup"><span data-stu-id="61f78-121">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="61f78-122">O \_ fluxo Ale da camada FWPM foi \_ \_ \_ estabelecido \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-122">FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="61f78-123">Disponível apenas no Windows Server 2008, Windows Vista com SP1 e posterior.</span><span class="sxs-lookup"><span data-stu-id="61f78-123">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     


</dt> </dl> </dd> <dt>

<span data-ttu-id="61f78-124"><span id="FWP_CONDITION_FLAG_IS_IPSEC_SECURED"></span><span id="fwp_condition_flag_is_ipsec_secured"></span>**o \_ sinalizador de condição fwp \_ \_ é \_ protegido por IPsec \_**</span><span class="sxs-lookup"><span data-stu-id="61f78-124"><span id="FWP_CONDITION_FLAG_IS_IPSEC_SECURED"></span><span id="fwp_condition_flag_is_ipsec_secured"></span>**FWP\_CONDITION\_FLAG\_IS\_IPSEC\_SECURED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-125">Testa se o tráfego de rede é protegido pelo IPsec.</span><span class="sxs-lookup"><span data-stu-id="61f78-125">Tests if the network traffic is protected by IPsec.</span></span>

<span data-ttu-id="61f78-126">Filtrando camadas:</span><span class="sxs-lookup"><span data-stu-id="61f78-126">Filtering layers:</span></span>

-   <span data-ttu-id="61f78-127">FWPM de \_ entrada da camada de \_ \_ IPPACKET \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-127">FWPM\_LAYER\_INBOUND\_IPPACKET\_V{4\|6}</span></span>
-   <span data-ttu-id="61f78-128">\_Transporte de entrada da camada FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-128">FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6}</span></span>
-   <span data-ttu-id="61f78-129">\_Aceitação da autenticação Ale de camada FWPM de \_ \_ \_ recebimento \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-129">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>
-   <span data-ttu-id="61f78-130">\_Conexão de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-130">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61f78-131"><span id="FWP_CONDITION_FLAG_IS_REAUTHORIZE"></span><span id="fwp_condition_flag_is_reauthorize"></span>**o \_ sinalizador de condição fwp \_ \_ é \_ reautorizado**</span><span class="sxs-lookup"><span data-stu-id="61f78-131"><span id="FWP_CONDITION_FLAG_IS_REAUTHORIZE"></span><span id="fwp_condition_flag_is_reauthorize"></span>**FWP\_CONDITION\_FLAG\_IS\_REAUTHORIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-132">Os testes de uma política mudam em oposição a uma nova conexão.</span><span class="sxs-lookup"><span data-stu-id="61f78-132">Tests for a policy change as opposed to a new connection.</span></span>

<span data-ttu-id="61f78-133">Filtrando camadas:</span><span class="sxs-lookup"><span data-stu-id="61f78-133">Filtering layers:</span></span>

-   <span data-ttu-id="61f78-134">\_Aceitação da autenticação Ale de camada FWPM de \_ \_ \_ recebimento \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-134">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>
-   <span data-ttu-id="61f78-135">\_Conexão de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-135">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61f78-136"><span id="FWP_CONDITION_FLAG_IS_WILDCARD_BIND"></span><span id="fwp_condition_flag_is_wildcard_bind"></span>**o \_ sinalizador de condição fwp \_ é uma \_ \_ \_ Associação curinga**</span><span class="sxs-lookup"><span data-stu-id="61f78-136"><span id="FWP_CONDITION_FLAG_IS_WILDCARD_BIND"></span><span id="fwp_condition_flag_is_wildcard_bind"></span>**FWP\_CONDITION\_FLAG\_IS\_WILDCARD\_BIND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-137">Testa se o aplicativo especificou um endereço curinga ao ligar a um endereço de rede local.</span><span class="sxs-lookup"><span data-stu-id="61f78-137">Tests if the application specified a wildcard address when binding to a local network address.</span></span>

<span data-ttu-id="61f78-138">Camada de filtragem:</span><span class="sxs-lookup"><span data-stu-id="61f78-138">Filtering layer:</span></span>

-   <span data-ttu-id="61f78-139">\_Atribuição de \_ recursos Ale de camada FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-139">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61f78-140"><span id="FWP_CONDITION_FLAG_IS_RAW_ENDPOINT"></span><span id="fwp_condition_flag_is_raw_endpoint"></span>**o \_ sinalizador de condição fwp \_ é um ponto de \_ \_ \_ extremidade bruto**</span><span class="sxs-lookup"><span data-stu-id="61f78-140"><span id="FWP_CONDITION_FLAG_IS_RAW_ENDPOINT"></span><span id="fwp_condition_flag_is_raw_endpoint"></span>**FWP\_CONDITION\_FLAG\_IS\_RAW\_ENDPOINT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-141">Testa se o ponto de extremidade local que está enviando e recebendo tráfego é um ponto de extremidade bruto.</span><span class="sxs-lookup"><span data-stu-id="61f78-141">Tests if the local endpoint that is sending and receiving traffic is a raw endpoint.</span></span>

<span data-ttu-id="61f78-142">Filtrando camadas:</span><span class="sxs-lookup"><span data-stu-id="61f78-142">Filtering layers:</span></span>

-   <span data-ttu-id="61f78-143">\_Transporte de entrada da camada FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-143">FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="61f78-144">Disponível apenas no Windows Server 2008, Windows Vista com SP1 e posterior.</span><span class="sxs-lookup"><span data-stu-id="61f78-144">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="61f78-145">\_Transporte de saída da camada FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-145">FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="61f78-146">Disponível apenas no Windows Server 2008, Windows Vista com SP1 e posterior.</span><span class="sxs-lookup"><span data-stu-id="61f78-146">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="61f78-147">\_Dados de \_ datagrama de camada FWPM \_ \_ {v4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-147">FWPM\_LAYER\_DATAGRAM\_DATA\_{V4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="61f78-148">Disponível apenas no Windows Server 2008, Windows Vista com SP1 e posterior.</span><span class="sxs-lookup"><span data-stu-id="61f78-148">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="61f78-149">\_Atribuição de \_ recursos Ale de camada FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-149">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>
-   <span data-ttu-id="61f78-150">\_Aceitação da autenticação Ale de camada FWPM de \_ \_ \_ recebimento \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-150">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>
-   <span data-ttu-id="61f78-151">\_Conexão de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-151">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61f78-152"><span id="FWP_CONDITION_FLAG_IS_FRAGMENT"></span><span id="fwp_condition_flag_is_fragment"></span>**o \_ sinalizador de condição fwp \_ \_ é \_ fragmento**</span><span class="sxs-lookup"><span data-stu-id="61f78-152"><span id="FWP_CONDITION_FLAG_IS_FRAGMENT"></span><span id="fwp_condition_flag_is_fragment"></span>**FWP\_CONDITION\_FLAG\_IS\_FRAGMENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-153">Testa se a \_ estrutura da lista de buffers líquida \_ passada para um driver de texto explicativo é um fragmento de pacote IP.</span><span class="sxs-lookup"><span data-stu-id="61f78-153">Tests if the NET\_BUFFER\_LIST structure passed to a callout driver is an IP packet fragment.</span></span>

<span data-ttu-id="61f78-154">Filtrando camadas:</span><span class="sxs-lookup"><span data-stu-id="61f78-154">Filtering layers:</span></span>

-   <span data-ttu-id="61f78-155">FWPM de \_ entrada da camada de \_ \_ IPPACKET \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-155">FWPM\_LAYER\_INBOUND\_IPPACKET\_V{4\|6}</span></span>
-   <span data-ttu-id="61f78-156">FWPM da \_ camada de \_ entrada \_ IPPACKET \_ V {4 \| 6} \_ descartar</span><span class="sxs-lookup"><span data-stu-id="61f78-156">FWPM\_LAYER\_INBOUND\_IPPACKET\_V{4\|6}\_DISCARD</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61f78-157"><span id="FWP_CONDITION_FLAG_IS_FRAGMENT_GROUP"></span><span id="fwp_condition_flag_is_fragment_group"></span>**o \_ sinalizador de condição fwp \_ é um \_ \_ grupo de fragmentos \_**</span><span class="sxs-lookup"><span data-stu-id="61f78-157"><span id="FWP_CONDITION_FLAG_IS_FRAGMENT_GROUP"></span><span id="fwp_condition_flag_is_fragment_group"></span>**FWP\_CONDITION\_FLAG\_IS\_FRAGMENT\_GROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-158">Testa se a \_ estrutura de lista de buffers de rede \_ passada para um driver de texto explicativo descreve uma lista vinculada de fragmentos de pacote.</span><span class="sxs-lookup"><span data-stu-id="61f78-158">Tests if the NET\_BUFFER\_LIST structure passed to a callout driver describes a linked list of packet fragments.</span></span>

<span data-ttu-id="61f78-159">Camada de filtragem:</span><span class="sxs-lookup"><span data-stu-id="61f78-159">Filtering layer:</span></span>

-   <span data-ttu-id="61f78-160">\_Camada FWPM \_ IPFORWARD \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-160">FWPM\_LAYER\_IPFORWARD\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61f78-161"><span id="FWP_CONDITION_FLAG_IS_IPSEC_NATT_RECLASSIFY"></span><span id="fwp_condition_flag_is_ipsec_natt_reclassify"></span>**o \_ sinalizador de condição fwp \_ é o \_ \_ IPSec \_ NATT \_ reclassificar**</span><span class="sxs-lookup"><span data-stu-id="61f78-161"><span id="FWP_CONDITION_FLAG_IS_IPSEC_NATT_RECLASSIFY"></span><span id="fwp_condition_flag_is_ipsec_natt_reclassify"></span>**FWP\_CONDITION\_FLAG\_IS\_IPSEC\_NATT\_RECLASSIFY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-162">Indica que o mesmo pacote está sendo reclassificado na camada de transporte, quando a Shim de NAT do IPsec traduz o valor da porta remota.</span><span class="sxs-lookup"><span data-stu-id="61f78-162">Indicates that the same packet is being re-classified at the transport layer, when the IPsec NAT shim translates the remote port value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61f78-163"><span id="FWP_CONDITION_FLAG_REQUIRES_ALE_CLASSIFY"></span><span id="fwp_condition_flag_requires_ale_classify"></span>**o \_ sinalizador de condição fwp \_ \_ requer \_ \_ classificação Ale**</span><span class="sxs-lookup"><span data-stu-id="61f78-163"><span id="FWP_CONDITION_FLAG_REQUIRES_ALE_CLASSIFY"></span><span id="fwp_condition_flag_requires_ale_classify"></span>**FWP\_CONDITION\_FLAG\_REQUIRES\_ALE\_CLASSIFY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-164">Indica que o pacote será reclassificado na camada de recepção/aceitação ALE.</span><span class="sxs-lookup"><span data-stu-id="61f78-164">Indicates that the packet will be reclassified at the ALE receive/accept layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61f78-165"><span id="FWP_CONDITION_FLAG_IS_IMPLICIT_BIND"></span><span id="fwp_condition_flag_is_implicit_bind"></span>**o \_ sinalizador de condição fwp \_ é uma \_ \_ \_ associação implícita**</span><span class="sxs-lookup"><span data-stu-id="61f78-165"><span id="FWP_CONDITION_FLAG_IS_IMPLICIT_BIND"></span><span id="fwp_condition_flag_is_implicit_bind"></span>**FWP\_CONDITION\_FLAG\_IS\_IMPLICIT\_BIND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-166">Testa se o Windows Sockets está executando uma ligação implícita.</span><span class="sxs-lookup"><span data-stu-id="61f78-166">Tests if Windows Sockets is performing an implicit bind.</span></span>

<span data-ttu-id="61f78-167">Disponível apenas no Windows Vista e no Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="61f78-167">Available only on Windows Vista and Windows Server 2008.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61f78-168"><span id="FWP_CONDITION_FLAG_IS_REASSEMBLED"></span><span id="fwp_condition_flag_is_reassembled"></span>**o \_ sinalizador de condição fwp \_ \_ é \_ remontado**</span><span class="sxs-lookup"><span data-stu-id="61f78-168"><span id="FWP_CONDITION_FLAG_IS_REASSEMBLED"></span><span id="fwp_condition_flag_is_reassembled"></span>**FWP\_CONDITION\_FLAG\_IS\_REASSEMBLED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-169">Testa se o pacote foi remontado.</span><span class="sxs-lookup"><span data-stu-id="61f78-169">Tests if the packet has been reassembled.</span></span>

> [!Note]  
> <span data-ttu-id="61f78-170">Disponível apenas no Windows Server 2008, Windows Vista com SP1 e posterior.</span><span class="sxs-lookup"><span data-stu-id="61f78-170">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

 

<span data-ttu-id="61f78-171">Camada de filtragem:</span><span class="sxs-lookup"><span data-stu-id="61f78-171">Filtering layer:</span></span>

-   <span data-ttu-id="61f78-172">FWPM de \_ entrada da camada de \_ \_ IPPACKET \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-172">FWPM\_LAYER\_INBOUND\_IPPACKET\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61f78-173"><span id="FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED"></span><span id="fwp_condition_flag_is_name_app_specified"></span>**o \_ sinalizador de condição fwp \_ é um nome de \_ \_ \_ aplicativo \_ especificado**</span><span class="sxs-lookup"><span data-stu-id="61f78-173"><span id="FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED"></span><span id="fwp_condition_flag_is_name_app_specified"></span>**FWP\_CONDITION\_FLAG\_IS\_NAME\_APP\_SPECIFIED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-174">Testa se o nome do computador par ao qual o aplicativo está esperando se conectar foi recebido por meio de uma API como [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) e não obtido por meio da heurística de cache.</span><span class="sxs-lookup"><span data-stu-id="61f78-174">Tests if the name of the peer machine that the application is expecting to connect to has been received via an API such as [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) and not obtained via the caching heuristics.</span></span>

> [!Note]  
> <span data-ttu-id="61f78-175">Disponível apenas no Windows Server 2008 R2, Windows 7 e posterior.</span><span class="sxs-lookup"><span data-stu-id="61f78-175">Available only on Windows Server 2008 R2, Windows 7, and later.</span></span>

 

<span data-ttu-id="61f78-176">Camada de filtragem:</span><span class="sxs-lookup"><span data-stu-id="61f78-176">Filtering layer:</span></span>

-   <span data-ttu-id="61f78-177">\_Conexão de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-177">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61f78-178"><span id="FWP_CONDITION_FLAG_IS_PROMISCUOUS"></span><span id="fwp_condition_flag_is_promiscuous"></span>**o \_ sinalizador de condição fwp \_ \_ é \_ promíscuo**</span><span class="sxs-lookup"><span data-stu-id="61f78-178"><span id="FWP_CONDITION_FLAG_IS_PROMISCUOUS"></span><span id="fwp_condition_flag_is_promiscuous"></span>**FWP\_CONDITION\_FLAG\_IS\_PROMISCUOUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-179">Reservado.</span><span class="sxs-lookup"><span data-stu-id="61f78-179">Reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61f78-180"><span id="FWP_CONDITION_FLAG_IS_AUTH_FW"></span><span id="fwp_condition_flag_is_auth_fw"></span>**o \_ sinalizador de condição fwp \_ \_ é \_ FW de autenticação \_**</span><span class="sxs-lookup"><span data-stu-id="61f78-180"><span id="FWP_CONDITION_FLAG_IS_AUTH_FW"></span><span id="fwp_condition_flag_is_auth_fw"></span>**FWP\_CONDITION\_FLAG\_IS\_AUTH\_FW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-181">Testa se a conexão é autenticada de ponta a ponta, mesmo que os pacotes individuais não tenham sido verificados.</span><span class="sxs-lookup"><span data-stu-id="61f78-181">Tests if the connection is end-to-end authenticated, even if the individual packets have not been verified.</span></span>

> [!Note]  
> <span data-ttu-id="61f78-182">Disponível apenas no Windows Server 2008 R2, Windows 7 e posterior.</span><span class="sxs-lookup"><span data-stu-id="61f78-182">Available only on Windows Server 2008 R2, Windows 7, and later.</span></span>

 

<span data-ttu-id="61f78-183">Camada de filtragem:</span><span class="sxs-lookup"><span data-stu-id="61f78-183">Filtering layer:</span></span>

-   <span data-ttu-id="61f78-184">\_Conexão de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-184">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="61f78-185">\_Aceitação da autenticação Ale de camada FWPM de \_ \_ \_ recebimento \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-185">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61f78-186"><span id="FWP_CONDITION_FLAG_IS_RECLASSIFY"></span><span id="fwp_condition_flag_is_reclassify"></span>**o \_ sinalizador de condição fwp \_ \_ é \_ reclassificado**</span><span class="sxs-lookup"><span data-stu-id="61f78-186"><span id="FWP_CONDITION_FLAG_IS_RECLASSIFY"></span><span id="fwp_condition_flag_is_reclassify"></span>**FWP\_CONDITION\_FLAG\_IS\_RECLASSIFY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-187">Testa se o mecanismo de filtragem está reclassificando uma associação ou solicitação de escuta anterior.</span><span class="sxs-lookup"><span data-stu-id="61f78-187">Tests if the filtering engine is reclassifying a previous bind or listen request.</span></span>

> [!Note]  
> <span data-ttu-id="61f78-188">Disponível apenas no Windows Server 2008 R2, Windows 7 e posterior.</span><span class="sxs-lookup"><span data-stu-id="61f78-188">Available only on Windows Server 2008 R2, Windows 7, and later.</span></span>

 

<span data-ttu-id="61f78-189">Camada de filtragem:</span><span class="sxs-lookup"><span data-stu-id="61f78-189">Filtering layer:</span></span>

-   <span data-ttu-id="61f78-190">\_Escuta de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-190">FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V{4\|6}</span></span>
-   <span data-ttu-id="61f78-191">\_Atribuição de \_ recursos Ale de camada FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-191">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61f78-192"><span id="FWP_CONDITION_FLAG_IS_PROXY_CONNECTION"></span><span id="fwp_condition_flag_is_proxy_connection"></span>**o \_ sinalizador de condição fwp \_ é uma \_ \_ \_ conexão proxy**</span><span class="sxs-lookup"><span data-stu-id="61f78-192"><span id="FWP_CONDITION_FLAG_IS_PROXY_CONNECTION"></span><span id="fwp_condition_flag_is_proxy_connection"></span>**FWP\_CONDITION\_FLAG\_IS\_PROXY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-193">Testa se a conexão usa um proxy.</span><span class="sxs-lookup"><span data-stu-id="61f78-193">Tests if the connection uses a proxy.</span></span>

> [!Note]  
> <span data-ttu-id="61f78-194">Disponível somente no Windows 8 e no Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="61f78-194">Available only on Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="61f78-195"><span id="FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_appcontainer_loopback"></span>**o \_ sinalizador de condição fwp \_ é o \_ \_ loopback do APPCONTAINER \_**</span><span class="sxs-lookup"><span data-stu-id="61f78-195"><span id="FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_appcontainer_loopback"></span>**FWP\_CONDITION\_FLAG\_IS\_APPCONTAINER\_LOOPBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-196">Testa se o tráfego de rede é o tráfego de loopback do contêiner de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="61f78-196">Tests if the network traffic is app container loopback traffic.</span></span>

> [!Note]  
> <span data-ttu-id="61f78-197">Disponível somente no Windows 8 e no Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="61f78-197">Available only on Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="61f78-198"><span id="FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_non_appcontainer_loopback"></span>**o \_ sinalizador de condição fwp não \_ é um \_ \_ \_ loopback de APPCONTAINER \_**</span><span class="sxs-lookup"><span data-stu-id="61f78-198"><span id="FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_non_appcontainer_loopback"></span>**FWP\_CONDITION\_FLAG\_IS\_NON\_APPCONTAINER\_LOOPBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-199">Testa se o tráfego de rede é um tráfego de loopback de contêiner não aplicativo.</span><span class="sxs-lookup"><span data-stu-id="61f78-199">Tests if the network traffic is non-app container loopback traffic.</span></span>

> [!Note]  
> <span data-ttu-id="61f78-200">Disponível somente no Windows 8 e no Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="61f78-200">Available only on Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="61f78-201"><span id="FWP_CONDITION_FLAG_IS_RESERVED"></span><span id="fwp_condition_flag_is_reserved"></span>**o \_ sinalizador de condição fwp \_ \_ está \_ reservado**</span><span class="sxs-lookup"><span data-stu-id="61f78-201"><span id="FWP_CONDITION_FLAG_IS_RESERVED"></span><span id="fwp_condition_flag_is_reserved"></span>**FWP\_CONDITION\_FLAG\_IS\_RESERVED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-202">Reservado.</span><span class="sxs-lookup"><span data-stu-id="61f78-202">Reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61f78-203"><span id="FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE"></span><span id="fwp_condition_flag_is_honoring_policy_authorize"></span>**o \_ sinalizador de condição fwp \_ \_ está \_ respeitando a \_ política de \_ autorização**</span><span class="sxs-lookup"><span data-stu-id="61f78-203"><span id="FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE"></span><span id="fwp_condition_flag_is_honoring_policy_authorize"></span>**FWP\_CONDITION\_FLAG\_IS\_HONORING\_POLICY\_AUTHORIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-204">Indica que a classificação atual está sendo executada para honrar a intenção de um aplicativo Redirecionado da Windows Store para se conectar a um host especificado.</span><span class="sxs-lookup"><span data-stu-id="61f78-204">Indicates that the current classification is being performed to honor the intention of a redirected Windows Store app to connect to a specified host.</span></span> <span data-ttu-id="61f78-205">Essa classificação conterá os mesmos valores de campo classificáveis como se o aplicativo nunca fosse Redirecionado.</span><span class="sxs-lookup"><span data-stu-id="61f78-205">Such a classification will contain the same classifiable field values as if the app were never redirected.</span></span> <span data-ttu-id="61f78-206">O sinalizador também indica que uma classificação futura será invocada para corresponder ao destino Redirecionado efetivo.</span><span class="sxs-lookup"><span data-stu-id="61f78-206">The flag also indicates that a future classification will be invoked to match the effective redirected destination.</span></span> <span data-ttu-id="61f78-207">Se o aplicativo for Redirecionado para um serviço de proxy para inspeção, isso também significará que uma classificação futura será invocada na conexão de proxy.</span><span class="sxs-lookup"><span data-stu-id="61f78-207">If the app is redirected to a proxy service for inspection, it also means a future classification will be invoked on the proxy connection.</span></span> <span data-ttu-id="61f78-208">Os drivers de texto explicativo geralmente devem permitir essa classificação.</span><span class="sxs-lookup"><span data-stu-id="61f78-208">Callout drivers should generally allow this classification.</span></span>

> [!Note]  
> <span data-ttu-id="61f78-209">Disponível somente no Windows 8 e no Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="61f78-209">Available only on Windows 8 and Windows Server 2012.</span></span>

 

<span data-ttu-id="61f78-210">Camada de filtragem:</span><span class="sxs-lookup"><span data-stu-id="61f78-210">Filtering layer:</span></span>

-   <span data-ttu-id="61f78-211">\_Conexão de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-211">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="61f78-212">Os sinalizadores a seguir especificam o motivo para a Reautorização de uma conexão autorizada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="61f78-212">The following flags specify the reason for reauthorizing a previously authorized connection.</span></span> <span data-ttu-id="61f78-213">Esses sinalizadores e as camadas de filtragem em que podem ser usados são definidos da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="61f78-213">These flags and the filtering layers where they can be used are defined as follows.</span></span>

> [!Note]  
> <span data-ttu-id="61f78-214">Essas condições de filtragem estão disponíveis apenas no Windows Server 2008 R2, Windows 7 e posterior.</span><span class="sxs-lookup"><span data-stu-id="61f78-214">These filtering conditions are available only on Windows Server 2008 R2, Windows 7, and later.</span></span>

 

<dl> <dt>

<span data-ttu-id="61f78-215"><span id="FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE"></span><span id="fwp_condition_reauthorize_reason_policy_change"></span>**FWP \_ condição de \_ reautorizar \_ alteração de política de motivo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="61f78-215"><span id="FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE"></span><span id="fwp_condition_reauthorize_reason_policy_change"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_POLICY\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-216">Indica que a conexão foi reautorizada devido a filtros sendo adicionados ou removidos.</span><span class="sxs-lookup"><span data-stu-id="61f78-216">Indicates that the connection was reauthorized due to filters being added or removed.</span></span>

<span data-ttu-id="61f78-217">Camada de filtragem:</span><span class="sxs-lookup"><span data-stu-id="61f78-217">Filtering layer:</span></span>

-   <span data-ttu-id="61f78-218">\_Conexão de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-218">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="61f78-219">\_Aceitação da autenticação Ale de camada FWPM de \_ \_ \_ recebimento \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-219">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61f78-220"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_arrival_interface"></span>**FWP \_ condição de \_ reautorizar \_ motivo \_ nova \_ interface de chegada \_**</span><span class="sxs-lookup"><span data-stu-id="61f78-220"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_arrival_interface"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_NEW\_ARRIVAL\_INTERFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-221">Indica que o pacote chegou de uma interface desconhecida.</span><span class="sxs-lookup"><span data-stu-id="61f78-221">Indicates that the packet has arrived from an unknown interface.</span></span>

<span data-ttu-id="61f78-222">Camada de filtragem:</span><span class="sxs-lookup"><span data-stu-id="61f78-222">Filtering layer:</span></span>

-   <span data-ttu-id="61f78-223">\_Conexão de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-223">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="61f78-224">\_Aceitação da autenticação Ale de camada FWPM de \_ \_ \_ recebimento \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-224">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61f78-225"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_nexthop_interface"></span>**FWP \_ condição de \_ reautorizar \_ motivo \_ nova \_ \_ interface NEXTHOP**</span><span class="sxs-lookup"><span data-stu-id="61f78-225"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_nexthop_interface"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_NEW\_NEXTHOP\_INTERFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-226">Indica que o pacote será desparte de uma interface desconhecida.</span><span class="sxs-lookup"><span data-stu-id="61f78-226">Indicates that the packet will be departing from an unknown interface.</span></span>

<span data-ttu-id="61f78-227">Camada de filtragem:</span><span class="sxs-lookup"><span data-stu-id="61f78-227">Filtering layer:</span></span>

-   <span data-ttu-id="61f78-228">\_Conexão de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-228">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="61f78-229">\_Aceitação da autenticação Ale de camada FWPM de \_ \_ \_ recebimento \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-229">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61f78-230"><span id="FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING"></span><span id="fwp_condition_reauthorize_reason_profile_crossing"></span>**FWP \_ condição de \_ Reautorização de \_ perfil de motivo \_ \_ cruzado**</span><span class="sxs-lookup"><span data-stu-id="61f78-230"><span id="FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING"></span><span id="fwp_condition_reauthorize_reason_profile_crossing"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_PROFILE\_CROSSING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-231">Indica que o pacote passou por interfaces de mais de uma categoria de rede.</span><span class="sxs-lookup"><span data-stu-id="61f78-231">Indicates that the packet has passed through interfaces of more than one network category.</span></span>

<span data-ttu-id="61f78-232">Camada de filtragem:</span><span class="sxs-lookup"><span data-stu-id="61f78-232">Filtering layer:</span></span>

-   <span data-ttu-id="61f78-233">\_Conexão de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-233">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="61f78-234">\_Aceitação da autenticação Ale de camada FWPM de \_ \_ \_ recebimento \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-234">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61f78-235"><span id="FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION"></span><span id="fwp_condition_reauthorize_reason_classify_completion"></span>**FWP \_ condição de \_ reautorizar \_ motivo \_ classificar \_ conclusão**</span><span class="sxs-lookup"><span data-stu-id="61f78-235"><span id="FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION"></span><span id="fwp_condition_reauthorize_reason_classify_completion"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_CLASSIFY\_COMPLETION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-236">Indica que uma conexão anteriormente armazenada agora está sendo permitida para ser concluída.</span><span class="sxs-lookup"><span data-stu-id="61f78-236">Indicates that a previously held connection is now being allowed to complete.</span></span>

<span data-ttu-id="61f78-237">Camada de filtragem:</span><span class="sxs-lookup"><span data-stu-id="61f78-237">Filtering layer:</span></span>

-   <span data-ttu-id="61f78-238">\_Conexão de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-238">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="61f78-239">\_Aceitação da autenticação Ale de camada FWPM de \_ \_ \_ recebimento \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-239">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61f78-240"><span id="FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED"></span><span id="fwp_condition_reauthorize_reason_ipsec_properties_changed"></span>**FWP \_ condição de \_ reautorização do \_ motivo da \_ \_ alteração das propriedades de IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="61f78-240"><span id="FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED"></span><span id="fwp_condition_reauthorize_reason_ipsec_properties_changed"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_IPSEC\_PROPERTIES\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-241">Indica que as propriedades de IPsec foram alteradas ou que a conexão foi alterada de texto não criptografado para uma conexão segura.</span><span class="sxs-lookup"><span data-stu-id="61f78-241">Indicates that IPsec properties have changed, or that the connection has changed from clear text to a secure connection.</span></span>

<span data-ttu-id="61f78-242">Camada de filtragem:</span><span class="sxs-lookup"><span data-stu-id="61f78-242">Filtering layer:</span></span>

-   <span data-ttu-id="61f78-243">\_Conexão de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-243">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="61f78-244">\_Aceitação da autenticação Ale de camada FWPM de \_ \_ \_ recebimento \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-244">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61f78-245"><span id="FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION"></span><span id="fwp_condition_reauthorize_reason_mid_stream_inspection"></span>**FWP \_ condição de \_ reautorizar \_ motivo \_ médio \_ inspeção de fluxo \_**</span><span class="sxs-lookup"><span data-stu-id="61f78-245"><span id="FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION"></span><span id="fwp_condition_reauthorize_reason_mid_stream_inspection"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_MID\_STREAM\_INSPECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-246">Indica que uma conexão TCP estabelecida anteriormente agora está sendo inspecionada.</span><span class="sxs-lookup"><span data-stu-id="61f78-246">Indicates that a previously established TCP connection is now being inspected.</span></span>

<span data-ttu-id="61f78-247">Camada de filtragem:</span><span class="sxs-lookup"><span data-stu-id="61f78-247">Filtering layer:</span></span>

-   <span data-ttu-id="61f78-248">\_Conexão de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-248">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="61f78-249">\_Aceitação da autenticação Ale de camada FWPM de \_ \_ \_ recebimento \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-249">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61f78-250"><span id="FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED"></span><span id="fwp_condition_reauthorize_reason_socket_property_changed"></span>**FWP \_ condição de \_ reautorizar a \_ propriedade de soquete de motivo \_ \_ \_ alterada**</span><span class="sxs-lookup"><span data-stu-id="61f78-250"><span id="FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED"></span><span id="fwp_condition_reauthorize_reason_socket_property_changed"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_SOCKET\_PROPERTY\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-251">Indica que as propriedades de soquete foram definidas depois que uma conexão foi autorizada e estabelecida.</span><span class="sxs-lookup"><span data-stu-id="61f78-251">Indicates that socket properties have been set after a connection was authorized and established.</span></span>

<span data-ttu-id="61f78-252">Camada de filtragem:</span><span class="sxs-lookup"><span data-stu-id="61f78-252">Filtering layer:</span></span>

-   <span data-ttu-id="61f78-253">\_Conexão de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-253">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="61f78-254">\_Aceitação da autenticação Ale de camada FWPM de \_ \_ \_ recebimento \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-254">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61f78-255"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET"></span><span id="fwp_condition_reauthorize_reason_new_inbound_mcast_bcast_packet"></span>**FWP \_ condição de \_ reautorizar \_ motivo \_ novo \_ \_ pacote mcast \_ BCAST \_ de entrada**</span><span class="sxs-lookup"><span data-stu-id="61f78-255"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET"></span><span id="fwp_condition_reauthorize_reason_new_inbound_mcast_bcast_packet"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_NEW\_INBOUND\_MCAST\_BCAST\_PACKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-256">Indica que novos pacotes multicast de entrada ou difusão estão sendo autorizados novamente em \_ \_ textos explicativos de aceitação Ale de recepção.</span><span class="sxs-lookup"><span data-stu-id="61f78-256">Indicates that new inbound multicast or broadcast packets are being re-authorized at ALE\_RECV\_ACCEPT callouts.</span></span>

<span data-ttu-id="61f78-257">Camada de filtragem:</span><span class="sxs-lookup"><span data-stu-id="61f78-257">Filtering layer:</span></span>

-   <span data-ttu-id="61f78-258">\_Aceitação da autenticação Ale de camada FWPM de \_ \_ \_ recebimento \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-258">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="61f78-259">Os sinalizadores a seguir especificam as propriedades de soquete que estão relacionadas a se um aplicativo deseja receber o tráfego de percurso de borda.</span><span class="sxs-lookup"><span data-stu-id="61f78-259">The following flags specify socket properties which are related to whether an application wants to receive Edge Traversal traffic.</span></span> <span data-ttu-id="61f78-260">Esses sinalizadores e as camadas de filtragem em que podem ser usados são definidos da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="61f78-260">These flags and the filtering layers where they can be used are defined as follows.</span></span>

> [!Note]  
> <span data-ttu-id="61f78-261">Essas condições de filtragem estão disponíveis apenas no Windows Server 2008 R2, Windows 7 e posterior.</span><span class="sxs-lookup"><span data-stu-id="61f78-261">These filtering conditions are available only on Windows Server 2008 R2, Windows 7, and later.</span></span>

 

<dl> <dt>

<span data-ttu-id="61f78-262"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC"></span><span id="fwp_condition_socket_property_flag_is_system_port_rpc"></span>**o \_ sinalizador de propriedade de soquete de condição fwp \_ \_ \_ \_ é \_ RPC de porta do sistema \_ \_**</span><span class="sxs-lookup"><span data-stu-id="61f78-262"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC"></span><span id="fwp_condition_socket_property_flag_is_system_port_rpc"></span>**FWP\_CONDITION\_SOCKET\_PROPERTY\_FLAG\_IS\_SYSTEM\_PORT\_RPC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-263">Indica que o aplicativo está se comunicando com uma porta RPC dinâmica.</span><span class="sxs-lookup"><span data-stu-id="61f78-263">Indicates that the application is communicating with a dynamic RPC port.</span></span>

<span data-ttu-id="61f78-264">Camada de filtragem:</span><span class="sxs-lookup"><span data-stu-id="61f78-264">Filtering layer:</span></span>

-   <span data-ttu-id="61f78-265">\_Escuta de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-265">FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V{4\|6}</span></span>
-   <span data-ttu-id="61f78-266">\_Atribuição de \_ recursos Ale de camada FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-266">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61f78-267"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_allow_edge_traffic"></span>**\_sinalizador de propriedade de soquete de condição fwp \_ \_ \_ \_ permitir \_ tráfego de borda \_**</span><span class="sxs-lookup"><span data-stu-id="61f78-267"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_allow_edge_traffic"></span>**FWP\_CONDITION\_SOCKET\_PROPERTY\_FLAG\_ALLOW\_EDGE\_TRAFFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-268">Indica que o aplicativo deseja receber tráfego específico de passagem de borda.</span><span class="sxs-lookup"><span data-stu-id="61f78-268">Indicates that the application wants to receive edge traversal-specific traffic.</span></span>

<span data-ttu-id="61f78-269">Camada de filtragem:</span><span class="sxs-lookup"><span data-stu-id="61f78-269">Filtering layer:</span></span>

-   <span data-ttu-id="61f78-270">\_Escuta de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-270">FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V{4\|6}</span></span>
-   <span data-ttu-id="61f78-271">\_Atribuição de \_ recursos Ale de camada FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-271">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61f78-272"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_deny_edge_traffic"></span>**\_sinalizador de Propriedade do soquete de condição fwp \_ \_ \_ \_ negar \_ tráfego de borda \_**</span><span class="sxs-lookup"><span data-stu-id="61f78-272"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_deny_edge_traffic"></span>**FWP\_CONDITION\_SOCKET\_PROPERTY\_FLAG\_DENY\_EDGE\_TRAFFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-273">Indica que o aplicativo não deseja receber ou processar o tráfego específico de passagem de borda.</span><span class="sxs-lookup"><span data-stu-id="61f78-273">Indicates that the application does not want to receive or process edge traversal-specific traffic.</span></span>

<span data-ttu-id="61f78-274">Camada de filtragem:</span><span class="sxs-lookup"><span data-stu-id="61f78-274">Filtering layer:</span></span>

-   <span data-ttu-id="61f78-275">\_Escuta de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-275">FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V{4\|6}</span></span>
-   <span data-ttu-id="61f78-276">\_Atribuição de \_ recursos Ale de camada FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="61f78-276">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="61f78-277">Os sinalizadores a seguir especificam detalhes de conexão relacionados à filtragem de L2.</span><span class="sxs-lookup"><span data-stu-id="61f78-277">The following flags specify connection details related to L2 filtering.</span></span>

> [!Note]  
> <span data-ttu-id="61f78-278">Essas condições de filtragem estão disponíveis apenas no Windows 8 e no Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="61f78-278">These filtering conditions are available only on Windows 8 and Windows Server 2012.</span></span>

 

<dl> <dt>

<span data-ttu-id="61f78-279"><span id="FWP_CONDITION_L2_IS_NATIVE_ETHERNET"></span><span id="fwp_condition_l2_is_native_ethernet"></span>**FWP \_ condição \_ L2 \_ é \_ \_ Ethernet nativa**</span><span class="sxs-lookup"><span data-stu-id="61f78-279"><span id="FWP_CONDITION_L2_IS_NATIVE_ETHERNET"></span><span id="fwp_condition_l2_is_native_ethernet"></span>**FWP\_CONDITION\_L2\_IS\_NATIVE\_ETHERNET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-280">Indica que a conexão é Ethernet nativa.</span><span class="sxs-lookup"><span data-stu-id="61f78-280">Indicates that the connection is native Ethernet.</span></span>

<span data-ttu-id="61f78-281">Camada de filtragem:</span><span class="sxs-lookup"><span data-stu-id="61f78-281">Filtering layer:</span></span>

-   <span data-ttu-id="61f78-282">\_ \_ \_ Mac \_ frame \_ Ethernet de entrada da camada FWPM</span><span class="sxs-lookup"><span data-stu-id="61f78-282">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="61f78-283">\_quadro de Mac de entrada da camada FWPM \_ \_ \_ \_ nativa</span><span class="sxs-lookup"><span data-stu-id="61f78-283">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="61f78-284">quadro de Mac de saída da camada do FWPM \_ \_ \_ \_ \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="61f78-284">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="61f78-285">\_quadro do Mac de saída da camada FWPM \_ \_ \_ \_ nativa</span><span class="sxs-lookup"><span data-stu-id="61f78-285">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61f78-286"><span id="FWP_CONDITION_L2_IS_WIFI"></span><span id="fwp_condition_l2_is_wifi"></span>**FWP \_ condição \_ L2 \_ é \_ WiFi**</span><span class="sxs-lookup"><span data-stu-id="61f78-286"><span id="FWP_CONDITION_L2_IS_WIFI"></span><span id="fwp_condition_l2_is_wifi"></span>**FWP\_CONDITION\_L2\_IS\_WIFI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-287">Indica que a conexão é Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="61f78-287">Indicates that the connection is Wi-Fi.</span></span>

<span data-ttu-id="61f78-288">Camada de filtragem:</span><span class="sxs-lookup"><span data-stu-id="61f78-288">Filtering layer:</span></span>

-   <span data-ttu-id="61f78-289">\_ \_ \_ Mac \_ frame \_ Ethernet de entrada da camada FWPM</span><span class="sxs-lookup"><span data-stu-id="61f78-289">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="61f78-290">\_quadro de Mac de entrada da camada FWPM \_ \_ \_ \_ nativa</span><span class="sxs-lookup"><span data-stu-id="61f78-290">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="61f78-291">quadro de Mac de saída da camada do FWPM \_ \_ \_ \_ \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="61f78-291">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="61f78-292">\_quadro do Mac de saída da camada FWPM \_ \_ \_ \_ nativa</span><span class="sxs-lookup"><span data-stu-id="61f78-292">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61f78-293"><span id="FWP_CONDITION_L2_IS_MOBILE_BROADBAND"></span><span id="fwp_condition_l2_is_mobile_broadband"></span>**FWP \_ condição \_ L2 \_ é \_ \_ banda larga móvel**</span><span class="sxs-lookup"><span data-stu-id="61f78-293"><span id="FWP_CONDITION_L2_IS_MOBILE_BROADBAND"></span><span id="fwp_condition_l2_is_mobile_broadband"></span>**FWP\_CONDITION\_L2\_IS\_MOBILE\_BROADBAND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-294">Indica que a conexão é de banda larga móvel.</span><span class="sxs-lookup"><span data-stu-id="61f78-294">Indicates that the connection is mobile broadband.</span></span>

<span data-ttu-id="61f78-295">Camada de filtragem:</span><span class="sxs-lookup"><span data-stu-id="61f78-295">Filtering layer:</span></span>

-   <span data-ttu-id="61f78-296">\_ \_ \_ Mac \_ frame \_ Ethernet de entrada da camada FWPM</span><span class="sxs-lookup"><span data-stu-id="61f78-296">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="61f78-297">\_quadro de Mac de entrada da camada FWPM \_ \_ \_ \_ nativa</span><span class="sxs-lookup"><span data-stu-id="61f78-297">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="61f78-298">quadro de Mac de saída da camada do FWPM \_ \_ \_ \_ \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="61f78-298">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="61f78-299">\_quadro do Mac de saída da camada FWPM \_ \_ \_ \_ nativa</span><span class="sxs-lookup"><span data-stu-id="61f78-299">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61f78-300"><span id="FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA"></span><span id="fwp_condition_l2_is_wifi_direct_data"></span>**FWP \_ condição \_ L2 \_ são \_ \_ dados diretos de WiFi \_**</span><span class="sxs-lookup"><span data-stu-id="61f78-300"><span id="FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA"></span><span id="fwp_condition_l2_is_wifi_direct_data"></span>**FWP\_CONDITION\_L2\_IS\_WIFI\_DIRECT\_DATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-301">Indica que a conexão é Wi-Fi direta.</span><span class="sxs-lookup"><span data-stu-id="61f78-301">Indicates that the connection is Wi-Fi Direct.</span></span>

<span data-ttu-id="61f78-302">Camada de filtragem:</span><span class="sxs-lookup"><span data-stu-id="61f78-302">Filtering layer:</span></span>

-   <span data-ttu-id="61f78-303">\_ \_ \_ Mac \_ frame \_ Ethernet de entrada da camada FWPM</span><span class="sxs-lookup"><span data-stu-id="61f78-303">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="61f78-304">\_quadro de Mac de entrada da camada FWPM \_ \_ \_ \_ nativa</span><span class="sxs-lookup"><span data-stu-id="61f78-304">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="61f78-305">quadro de Mac de saída da camada do FWPM \_ \_ \_ \_ \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="61f78-305">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="61f78-306">\_quadro do Mac de saída da camada FWPM \_ \_ \_ \_ nativa</span><span class="sxs-lookup"><span data-stu-id="61f78-306">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61f78-307"><span id="FWP_CONDITION_L2_IS_VM2VM"></span><span id="fwp_condition_l2_is_vm2vm"></span>**FWP \_ condição \_ L2 \_ é \_ VM2VM**</span><span class="sxs-lookup"><span data-stu-id="61f78-307"><span id="FWP_CONDITION_L2_IS_VM2VM"></span><span id="fwp_condition_l2_is_vm2vm"></span>**FWP\_CONDITION\_L2\_IS\_VM2VM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-308">Indica que a conexão está entre máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="61f78-308">Indicates that the connection is between virtual machines.</span></span>

<span data-ttu-id="61f78-309">Camada de filtragem:</span><span class="sxs-lookup"><span data-stu-id="61f78-309">Filtering layer:</span></span>

-   <span data-ttu-id="61f78-310">\_ \_ \_ Mac \_ frame \_ Ethernet de entrada da camada FWPM</span><span class="sxs-lookup"><span data-stu-id="61f78-310">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="61f78-311">\_quadro de Mac de entrada da camada FWPM \_ \_ \_ \_ nativa</span><span class="sxs-lookup"><span data-stu-id="61f78-311">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="61f78-312">quadro de Mac de saída da camada do FWPM \_ \_ \_ \_ \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="61f78-312">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="61f78-313">\_quadro do Mac de saída da camada FWPM \_ \_ \_ \_ nativa</span><span class="sxs-lookup"><span data-stu-id="61f78-313">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61f78-314"><span id="FWP_CONDITION_L2_IS_MALFORMED_PACKET"></span><span id="fwp_condition_l2_is_malformed_packet"></span>**FWP \_ condição \_ L2 \_ é um \_ pacote malformado \_**</span><span class="sxs-lookup"><span data-stu-id="61f78-314"><span id="FWP_CONDITION_L2_IS_MALFORMED_PACKET"></span><span id="fwp_condition_l2_is_malformed_packet"></span>**FWP\_CONDITION\_L2\_IS\_MALFORMED\_PACKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-315">Indica que um pacote parece estar malformado.</span><span class="sxs-lookup"><span data-stu-id="61f78-315">Indicates that a packet appears to be malformed.</span></span>

<span data-ttu-id="61f78-316">Camada de filtragem:</span><span class="sxs-lookup"><span data-stu-id="61f78-316">Filtering layer:</span></span>

-   <span data-ttu-id="61f78-317">\_ \_ \_ Mac \_ frame \_ Ethernet de entrada da camada FWPM</span><span class="sxs-lookup"><span data-stu-id="61f78-317">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="61f78-318">\_quadro de Mac de entrada da camada FWPM \_ \_ \_ \_ nativa</span><span class="sxs-lookup"><span data-stu-id="61f78-318">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="61f78-319">quadro de Mac de saída da camada do FWPM \_ \_ \_ \_ \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="61f78-319">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="61f78-320">\_quadro do Mac de saída da camada FWPM \_ \_ \_ \_ nativa</span><span class="sxs-lookup"><span data-stu-id="61f78-320">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61f78-321"><span id="FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP"></span><span id="fwp_condition_l2_is_ip_fragment_group"></span>**FWP \_ condição \_ L2 \_ é \_ \_ grupo de fragmentos IP \_**</span><span class="sxs-lookup"><span data-stu-id="61f78-321"><span id="FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP"></span><span id="fwp_condition_l2_is_ip_fragment_group"></span>**FWP\_CONDITION\_L2\_IS\_IP\_FRAGMENT\_GROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-322">Indica um grupo de fragmentos de pacotes IP.</span><span class="sxs-lookup"><span data-stu-id="61f78-322">Indicates an IP packet fragment group.</span></span>

<span data-ttu-id="61f78-323">Camada de filtragem:</span><span class="sxs-lookup"><span data-stu-id="61f78-323">Filtering layer:</span></span>

-   <span data-ttu-id="61f78-324">\_ \_ \_ Mac \_ frame \_ Ethernet de entrada da camada FWPM</span><span class="sxs-lookup"><span data-stu-id="61f78-324">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="61f78-325">\_quadro de Mac de entrada da camada FWPM \_ \_ \_ \_ nativa</span><span class="sxs-lookup"><span data-stu-id="61f78-325">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="61f78-326">quadro de Mac de saída da camada do FWPM \_ \_ \_ \_ \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="61f78-326">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="61f78-327">\_quadro do Mac de saída da camada FWPM \_ \_ \_ \_ nativa</span><span class="sxs-lookup"><span data-stu-id="61f78-327">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="61f78-328"><span id="FWP_CONDITION_L2_IF_CONNECTOR_PRESENT"></span><span id="fwp_condition_l2_if_connector_present"></span>**FWP \_ condição \_ L2 \_ se o \_ conector \_ estiver presente**</span><span class="sxs-lookup"><span data-stu-id="61f78-328"><span id="FWP_CONDITION_L2_IF_CONNECTOR_PRESENT"></span><span id="fwp_condition_l2_if_connector_present"></span>**FWP\_CONDITION\_L2\_IF\_CONNECTOR\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="61f78-329">Indica que um conector está presente.</span><span class="sxs-lookup"><span data-stu-id="61f78-329">Indicates that a connector is present.</span></span>

<span data-ttu-id="61f78-330">Camada de filtragem:</span><span class="sxs-lookup"><span data-stu-id="61f78-330">Filtering layer:</span></span>

-   <span data-ttu-id="61f78-331">\_ \_ \_ Mac \_ frame \_ Ethernet de entrada da camada FWPM</span><span class="sxs-lookup"><span data-stu-id="61f78-331">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="61f78-332">\_quadro de Mac de entrada da camada FWPM \_ \_ \_ \_ nativa</span><span class="sxs-lookup"><span data-stu-id="61f78-332">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="61f78-333">quadro de Mac de saída da camada do FWPM \_ \_ \_ \_ \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="61f78-333">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="61f78-334">\_quadro do Mac de saída da camada FWPM \_ \_ \_ \_ nativa</span><span class="sxs-lookup"><span data-stu-id="61f78-334">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="61f78-335">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61f78-335">Requirements</span></span>



| <span data-ttu-id="61f78-336">Requisito</span><span class="sxs-lookup"><span data-stu-id="61f78-336">Requirement</span></span> | <span data-ttu-id="61f78-337">Valor</span><span class="sxs-lookup"><span data-stu-id="61f78-337">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61f78-338">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61f78-338">Minimum supported client</span></span><br/> | <span data-ttu-id="61f78-339">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="61f78-339">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="61f78-340">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61f78-340">Minimum supported server</span></span><br/> | <span data-ttu-id="61f78-341">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="61f78-341">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="61f78-342">parâmetro</span><span class="sxs-lookup"><span data-stu-id="61f78-342">Header</span></span><br/>                   | <dl> <span data-ttu-id="61f78-343"><dt>Fwptypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="61f78-343"><dt>Fwptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61f78-344">Confira também</span><span class="sxs-lookup"><span data-stu-id="61f78-344">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61f78-345">**Filtrando identificadores de camada**</span><span class="sxs-lookup"><span data-stu-id="61f78-345">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> </dl>

 


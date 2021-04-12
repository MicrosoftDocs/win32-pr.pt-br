---
title: Isenções de IKE/AuthIP
description: Protocolo IKE (IKE) e protocolo Authenticated IP (AuthIP), a fim de funcionar, precisam isentar o tráfego de rede da filtragem IPsec.
ms.assetid: 365bfebc-250a-440f-8056-ff9601daa030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d58a6d00ddd337d56c3c00a34b6949213be6ee26
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104365625"
---
# <a name="ikeauthip-exemptions"></a><span data-ttu-id="c0fd9-103">Isenções de IKE/AuthIP</span><span class="sxs-lookup"><span data-stu-id="c0fd9-103">IKE/AuthIP Exemptions</span></span>

<span data-ttu-id="c0fd9-104">Os módulos de criação de chaves IPsec (Internet Protocol Security), protocolo IKE (IKE) e protocolo Authenticated IP (AuthIP), para funcionar, precisam isentar seu tráfego de rede da filtragem IPsec.</span><span class="sxs-lookup"><span data-stu-id="c0fd9-104">The Internet Protocol security (IPsec) keying modules, Internet Key Exchange (IKE) and Authenticated Internet Protocol (AuthIP), in order to function, need to exempt their network traffic from the IPsec filtering.</span></span>

<span data-ttu-id="c0fd9-105">Na WFP (plataforma de filtragem do Windows), o BFE (mecanismo de filtragem básica) adiciona automaticamente filtros de isenção IKE e AuthIP quando o primeiro filtro de política de Ike ou AuthIP MM é adicionado e os exclui quando o último filtro de política IKE ou AuthIP cm é excluído.</span><span class="sxs-lookup"><span data-stu-id="c0fd9-105">In Windows Filtering Platform (WFP) the Base Filtering Engine (BFE) automatically adds IKE and AuthIP exemption filters when the first IKE or AuthIP main mode (MM) policy filter is added and deletes them when the last IKE or AuthIP MM policy filter is deleted.</span></span> <span data-ttu-id="c0fd9-106">Dessa forma, os provedores de política não precisam gerenciar as isenções de filtragem IKE e AuthIP individualmente.</span><span class="sxs-lookup"><span data-stu-id="c0fd9-106">This way, the policy providers do not have to manage IKE and AuthIP filtering exemptions individually.</span></span>

<span data-ttu-id="c0fd9-107">Um filtro de política de IKE MM é um filtro na camada de FWPM da camada do mecanismo [**\_ \_ IKEEXT \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) que faz referência a um contexto de provedor do tipo [**FWPM \_ IPSec \_ Ike \_ mm \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).</span><span class="sxs-lookup"><span data-stu-id="c0fd9-107">An IKE MM policy filter is a filter in the engine layer [**FWPM\_LAYER\_IKEEXT\_V{4\|6}**](management-filtering-layer-identifiers-.md) that references a provider context of type [**FWPM\_IPSEC\_IKE\_MM\_CONTEXT**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).</span></span>

<span data-ttu-id="c0fd9-108">Um filtro de política AuthIP MM é um filtro na camada de FWPM da camada do mecanismo [**\_ \_ IKEEXT \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) que faz referência a um contexto de provedor do tipo de [**\_ \_ \_ \_ contexto IPSec AuthIP mm de FWPM**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).</span><span class="sxs-lookup"><span data-stu-id="c0fd9-108">An AuthIP MM policy filter is a filter in the engine layer [**FWPM\_LAYER\_IKEEXT\_V{4\|6}**](management-filtering-layer-identifiers-.md) that references a provider context of type [**FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).</span></span>

<span data-ttu-id="c0fd9-109">Um filtro de isenção de IKE ou AuthIP é um filtro na camada de mecanismo [**FWPM transporte de entrada de camada \_ \_ \_ \_ v {4 \| 6}**](management-filtering-layer-identifiers-.md) ou **transporte de saída de \_ camada FWPM \_ \_ \_ v {4 \| 6}** automaticamente ponderado no intervalo de peso FWPM intervalo de pesos de [**\_ \_ \_ \_ isenções Ike**](filter-weight-identifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="c0fd9-109">An IKE or AuthIP exemption filter is a filter in the engine layer [**FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6}**](management-filtering-layer-identifiers-.md) or **FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6}** auto-weighted in the [**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**](filter-weight-identifiers.md) weight range.</span></span>

<span data-ttu-id="c0fd9-110">As isenções IKE e AuthIP implementadas pelo BFE são as seguintes.</span><span class="sxs-lookup"><span data-stu-id="c0fd9-110">The IKE and AuthIP exemptions implemented by BFE are as follows.</span></span>

| <span data-ttu-id="c0fd9-111">Versão IP</span><span class="sxs-lookup"><span data-stu-id="c0fd9-111">IP version</span></span>      | <span data-ttu-id="c0fd9-112">Porta</span><span class="sxs-lookup"><span data-stu-id="c0fd9-112">Port</span></span>                        | <span data-ttu-id="c0fd9-113">Isenção</span><span class="sxs-lookup"><span data-stu-id="c0fd9-113">Exemption</span></span>                                                                                                                                                                                                                             |
|-----------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0fd9-114">IPv4</span><span class="sxs-lookup"><span data-stu-id="c0fd9-114">IPv4</span></span><br/> | <span data-ttu-id="c0fd9-115">UDP: 500 UDP: 4500</span><span class="sxs-lookup"><span data-stu-id="c0fd9-115">UDP:500 UDP:4500</span></span><br/> | <span data-ttu-id="c0fd9-116">Permitir tráfego IKE e AuthIP na camada de transporte de entrada e na camada de transporte de saída.</span><span class="sxs-lookup"><span data-stu-id="c0fd9-116">Permit IKE and AuthIP traffic at the inbound transport layer and at the outbound transport layer.</span></span> <br/> <span data-ttu-id="c0fd9-117">Permitir o tráfego IKE e AuthIP na recepção/aceitação da ALE e conectar camadas, mas restringi-la ao sistema local.</span><span class="sxs-lookup"><span data-stu-id="c0fd9-117">Permit IKE and AuthIP traffic at the ALE receive/accept and connect layers, but restrict it to local system.</span></span><br/> |
| <span data-ttu-id="c0fd9-118">IPv6</span><span class="sxs-lookup"><span data-stu-id="c0fd9-118">IPv6</span></span><br/> | <span data-ttu-id="c0fd9-119">UDP: 500</span><span class="sxs-lookup"><span data-stu-id="c0fd9-119">UDP:500</span></span><br/>          | <span data-ttu-id="c0fd9-120">Permitir tráfego IKE e AuthIP na camada de transporte de entrada e na camada de transporte de saída.</span><span class="sxs-lookup"><span data-stu-id="c0fd9-120">Permit IKE and AuthIP traffic at the inbound transport layer and at the outbound transport layer.</span></span> <br/> <span data-ttu-id="c0fd9-121">Permitir o tráfego IKE e AuthIP na recepção/aceitação da ALE e conectar camadas, mas restringi-la ao sistema local.</span><span class="sxs-lookup"><span data-stu-id="c0fd9-121">Permit IKE and AuthIP traffic at the ALE receive/accept and connect layers, but restrict it to local system.</span></span><br/> |



 

<span data-ttu-id="c0fd9-122">Os filtros de isenção IKE e AuthIP estão abertos a todos os endereços.</span><span class="sxs-lookup"><span data-stu-id="c0fd9-122">The IKE and AuthIP exemption filters are open to all addresses.</span></span> <span data-ttu-id="c0fd9-123">Para implementar um firewall com controle mais granular, os provedores de política devem adicionar filtros em um intervalo de peso maior que as [**\_ \_ \_ \_ isenções Ike de intervalo de peso FWPM**](filter-weight-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="c0fd9-123">To implement a firewall with more granular control, policy providers should add filters in a weight range higher than [**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**](filter-weight-identifiers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0fd9-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c0fd9-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0fd9-125">Configuração de IPsec</span><span class="sxs-lookup"><span data-stu-id="c0fd9-125">IPsec Configuration</span></span>](ipsec-configuration.md)
</dt> <dt>

[<span data-ttu-id="c0fd9-126">Atribuição de peso de filtro</span><span class="sxs-lookup"><span data-stu-id="c0fd9-126">Filter Weight Assignment</span></span>](filter-weight-assignment.md)
</dt> </dl>

 

 






---
title: Autorização de identidade remota
description: O cenário da política IPsec de autorização de identidade remota requer que as conexões de entrada venham de um conjunto específico de entidades de segurança remotas que são especificadas em uma ACL (lista de controle de acesso) do Windows Security Descriptor (SD).
ms.assetid: 4d9f83d6-6f56-4416-8c35-d0260f9e888c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57287a0dd9af4686b1a2dab162677912213559a7
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314829"
---
# <a name="remote-identity-authorization"></a><span data-ttu-id="22beb-103">Autorização de identidade remota</span><span class="sxs-lookup"><span data-stu-id="22beb-103">Remote Identity Authorization</span></span>

<span data-ttu-id="22beb-104">O cenário da política IPsec de autorização de identidade remota requer que as conexões de entrada venham de um conjunto específico de entidades de segurança remotas que são especificadas em uma ACL (lista de controle de acesso) do Windows Security Descriptor (SD).</span><span class="sxs-lookup"><span data-stu-id="22beb-104">The Remote Identity Authorization IPsec policy scenario requires that inbound connections come from a specific set of remote security principals which are specified in a Windows security descriptor (SD) access control list (ACL).</span></span> <span data-ttu-id="22beb-105">Se a identidade remota (conforme determinado pelo IPsec) não corresponder ao conjunto de identidades permitidas, a conexão será descartada.</span><span class="sxs-lookup"><span data-stu-id="22beb-105">If the remote identity (as determined by IPsec) does not match the set of allowed identities, the connection will be dropped.</span></span> <span data-ttu-id="22beb-106">Essa política deve ser especificada em conjunto com uma das opções de política do modo de transporte.</span><span class="sxs-lookup"><span data-stu-id="22beb-106">This policy must be specified in conjunction with one of the transport mode policy options.</span></span>

<span data-ttu-id="22beb-107">Se o AuthIP estiver habilitado, dois descritores de segurança poderão ser especificados, um correspondente ao modo principal de AuthIP e o outro correspondente ao modo estendido AuthIP.</span><span class="sxs-lookup"><span data-stu-id="22beb-107">If AuthIP is enabled, two security descriptors can be specified, one corresponding to AuthIP main mode, and the other corresponding to AuthIP extended mode.</span></span>

<span data-ttu-id="22beb-108">Um exemplo de cenário de modo de transporte de descoberta de negociação é "proteger todos os tráfegos de dados unicast, exceto ICMP, usando o modo de transporte IPsec, habilitar a descoberta de negociação e restringir o acesso de entrada a identidades remotas permitidas de acordo com o modo estendido do AuthIP), para todo o tráfego unicast correspondente à porta TCP local 5555."</span><span class="sxs-lookup"><span data-stu-id="22beb-108">An example of a possible Negotiation Discovery Transport Mode scenario is "Secure all unicast data traffic, except ICMP, using IPsec transport mode, enable negotiation discovery, and restrict inbound access to remote identities allowed as per security descriptor SD1 (corresponding to IKE/AuthIP main mode) and security descriptor SD2 (corresponding to AuthIP extended mode), for all unicast traffic corresponding to TCP local port 5555."</span></span>

<span data-ttu-id="22beb-109">Para implementar este exemplo programaticamente, use a seguinte configuração de WFP.</span><span class="sxs-lookup"><span data-stu-id="22beb-109">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="22beb-110">**Na \_ camada FWPM \_ IKEEXT \_ V {4 \| 6} política de negociação de instalação mm**</span><span class="sxs-lookup"><span data-stu-id="22beb-110">**At FWPM\_LAYER\_IKEEXT\_V{4\|6} setup MM negotiation policy**</span></span>  

1.  <span data-ttu-id="22beb-111">Adicione um ou ambos os seguintes contextos do provedor de política MM.</span><span class="sxs-lookup"><span data-stu-id="22beb-111">Add one or both of the following MM policy provider contexts.</span></span>  
    -   <span data-ttu-id="22beb-112">Para IKE, um contexto de provedor de política do tipo **FWPM \_ IPSec \_ Ike \_ mm \_ Context**.</span><span class="sxs-lookup"><span data-stu-id="22beb-112">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_MM\_CONTEXT**.</span></span>
    -   <span data-ttu-id="22beb-113">Para AuthIP, um contexto de provedor de política do tipo **FWPM \_ IPSec \_ AuthIP \_ mm \_ Context**.</span><span class="sxs-lookup"><span data-stu-id="22beb-113">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT**.</span></span>

    > [!Note]  
    > <span data-ttu-id="22beb-114">Um módulo de chave comum será negociado e a política MM correspondente será aplicada.</span><span class="sxs-lookup"><span data-stu-id="22beb-114">A common keying module will be negotiated and the corresponding MM policy will be applied.</span></span> <span data-ttu-id="22beb-115">AuthIP é o módulo de chaveamento preferencial se o IKE e o AuthIP tiverem suporte.</span><span class="sxs-lookup"><span data-stu-id="22beb-115">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="22beb-116">Para cada um dos contextos adicionados na etapa 1, adicione um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="22beb-116">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 

    | <span data-ttu-id="22beb-117">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="22beb-117">Filter property</span></span>        | <span data-ttu-id="22beb-118">Valor</span><span class="sxs-lookup"><span data-stu-id="22beb-118">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="22beb-119">Condições de filtragem</span><span class="sxs-lookup"><span data-stu-id="22beb-119">Filtering conditions</span></span>   | <span data-ttu-id="22beb-120">Vazio.</span><span class="sxs-lookup"><span data-stu-id="22beb-120">Empty.</span></span> <span data-ttu-id="22beb-121">Todo o tráfego corresponderá ao filtro.</span><span class="sxs-lookup"><span data-stu-id="22beb-121">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="22beb-122">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="22beb-122">**providerContextKey**</span></span> | <span data-ttu-id="22beb-123">GUID do contexto do provedor MM adicionado na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="22beb-123">GUID of the MM provider context added in step 1.</span></span> |

        

<span data-ttu-id="22beb-124">**Na \_ camada FWPM \_ IPSec \_ V {4 \| 6} configurar política de negociação QM e em**</span><span class="sxs-lookup"><span data-stu-id="22beb-124">**At FWPM\_LAYER\_IPSEC\_V{4\|6} setup QM and EM negotiation policy**</span></span>  

1.  <span data-ttu-id="22beb-125">Adicione um ou ambos os seguintes contextos de provedor de política de modo de transporte QM e defina o sinalizador [**\_ \_ \_ \_ seguro do sinalizador de política IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) .</span><span class="sxs-lookup"><span data-stu-id="22beb-125">Add one or both of the following QM transport mode policy provider contexts and set the [**IPSEC\_POLICY\_FLAG\_ND\_SECURE**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) flag.</span></span>  
    -   <span data-ttu-id="22beb-126">Para IKE, um contexto de provedor de política do tipo **FWPM \_ IPSec de transporte de IP \_ \_ qm \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="22beb-126">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_QM\_TRANSPORT\_CONTEXT**.</span></span>
    -   <span data-ttu-id="22beb-127">Para AuthIP, um contexto de provedor de política do tipo **\_ \_ \_ \_ \_ contexto de transporte QM IPSec AuthIP de FWPM** que contém a política de negociação em modo estendido AuthIP.</span><span class="sxs-lookup"><span data-stu-id="22beb-127">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_QM\_TRANSPORT\_CONTEXT** that contains the AuthIP Extended Mode (EM) negotiation policy.</span></span>

    > [!Note]  
    > <span data-ttu-id="22beb-128">Um módulo de chave comum será negociado e a política QM correspondente será aplicada.</span><span class="sxs-lookup"><span data-stu-id="22beb-128">A common keying module will be negotiated and the corresponding QM policy will be applied.</span></span> <span data-ttu-id="22beb-129">AuthIP é o módulo de chaveamento preferencial se o IKE e o AuthIP tiverem suporte.</span><span class="sxs-lookup"><span data-stu-id="22beb-129">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="22beb-130">Para cada um dos contextos adicionados na etapa 1, adicione um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="22beb-130">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 

    | <span data-ttu-id="22beb-131">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="22beb-131">Filter property</span></span>        | <span data-ttu-id="22beb-132">Valor</span><span class="sxs-lookup"><span data-stu-id="22beb-132">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="22beb-133">Condições de filtragem</span><span class="sxs-lookup"><span data-stu-id="22beb-133">Filtering conditions</span></span>   | <span data-ttu-id="22beb-134">Vazio.</span><span class="sxs-lookup"><span data-stu-id="22beb-134">Empty.</span></span> <span data-ttu-id="22beb-135">Todo o tráfego corresponderá ao filtro.</span><span class="sxs-lookup"><span data-stu-id="22beb-135">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="22beb-136">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="22beb-136">**providerContextKey**</span></span> | <span data-ttu-id="22beb-137">GUID do contexto de provedor QM adicionado na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="22beb-137">GUID of the QM provider context added in step 1.</span></span> |

        

<span data-ttu-id="22beb-138">**Na \_ camada FWPM \_ transporte de \_ entrada \_ V {4 \| 6} configurar regras de filtragem de entrada por pacote**</span><span class="sxs-lookup"><span data-stu-id="22beb-138">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} setup inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="22beb-139">Adicione um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="22beb-139">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="22beb-140">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="22beb-140">Filter property</span></span>                                                   | <span data-ttu-id="22beb-141">Valor</span><span class="sxs-lookup"><span data-stu-id="22beb-141">Value</span></span>                                                                                              |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="22beb-142">**FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição**</span><span class="sxs-lookup"><span data-stu-id="22beb-142">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | [<span data-ttu-id="22beb-143">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="22beb-143">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | <span data-ttu-id="22beb-144">**ação. tipo**</span><span class="sxs-lookup"><span data-stu-id="22beb-144">**action.type**</span></span>                                                   | <span data-ttu-id="22beb-145">**o \_ \_ texto explicativo de ação fwp \_ termina**</span><span class="sxs-lookup"><span data-stu-id="22beb-145">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                              |
    | <span data-ttu-id="22beb-146">**ação. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="22beb-146">**action.calloutKey**</span></span>                                             | <span data-ttu-id="22beb-147">**FWPM \_ texto explicativo \_ IPSec de \_ transporte de entrada \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="22beb-147">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                              |
    | <span data-ttu-id="22beb-148">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="22beb-148">**rawContext**</span></span>                                                    | [<span data-ttu-id="22beb-149">**\_segurança de \_ \_ conexão de persistência de entrada IPsec \_ \_ de contexto \_ de FWPM**</span><span class="sxs-lookup"><span data-stu-id="22beb-149">**FWPM\_CONTEXT\_IPSEC\_INBOUND\_PERSIST\_CONNECTION\_SECURITY**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="22beb-150">Isentar o tráfego ICMP do IPsec adicionando um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="22beb-150">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 

    | <span data-ttu-id="22beb-151">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="22beb-151">Filter property</span></span>                                                   | <span data-ttu-id="22beb-152">Valor</span><span class="sxs-lookup"><span data-stu-id="22beb-152">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="22beb-153">**FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição**</span><span class="sxs-lookup"><span data-stu-id="22beb-153">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="22beb-154">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="22beb-154">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="22beb-155">**FWPM \_ Condição de filtragem de \_ \_ protocolo IP de condição**</span><span class="sxs-lookup"><span data-stu-id="22beb-155">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="22beb-156">**IPPROTO \_ ICMP {V6}** essas constantes são definidas no Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="22beb-156">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="22beb-157">**ação. tipo**</span><span class="sxs-lookup"><span data-stu-id="22beb-157">**action.type**</span></span>                                                   | <span data-ttu-id="22beb-158">\_permissão de ação fwp \_</span><span class="sxs-lookup"><span data-stu-id="22beb-158">FWP\_ACTION\_PERMIT</span></span>                                                        |
    | <span data-ttu-id="22beb-159">**weight**</span><span class="sxs-lookup"><span data-stu-id="22beb-159">**weight**</span></span>                                                        | [<span data-ttu-id="22beb-160">**\_ \_ isenções Ike de intervalo de peso FWPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22beb-160">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md)  |

        

<span data-ttu-id="22beb-161">**Em FWPM \_ camada de \_ saída do \_ transporte \_ V {4 \| 6} configurar regras de filtragem por pacote de saída**</span><span class="sxs-lookup"><span data-stu-id="22beb-161">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} setup outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="22beb-162">Adicione um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="22beb-162">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="22beb-163">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="22beb-163">Filter property</span></span>                                                   | <span data-ttu-id="22beb-164">Valor</span><span class="sxs-lookup"><span data-stu-id="22beb-164">Value</span></span>                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | <span data-ttu-id="22beb-165">**FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição**</span><span class="sxs-lookup"><span data-stu-id="22beb-165">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="22beb-166">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="22beb-166">NlatUnicast</span></span>                                                                               |
    | <span data-ttu-id="22beb-167">**ação. tipo**</span><span class="sxs-lookup"><span data-stu-id="22beb-167">**action.type**</span></span>                                                   | <span data-ttu-id="22beb-168">**o \_ \_ texto explicativo de ação fwp \_ termina**</span><span class="sxs-lookup"><span data-stu-id="22beb-168">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                     |
    | <span data-ttu-id="22beb-169">**ação. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="22beb-169">**action.calloutKey**</span></span>                                             | <span data-ttu-id="22beb-170">**FWPM do \_ balão de \_ \_ saída IPSec \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="22beb-170">**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                    |
    | <span data-ttu-id="22beb-171">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="22beb-171">**rawContext**</span></span>                                                    | [<span data-ttu-id="22beb-172">**\_descoberta de \_ \_ negociação de saída IPSec de contexto \_ FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="22beb-172">**FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_NEGOTIATE\_DISCOVER**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="22beb-173">Isentar o tráfego ICMP do IPsec adicionando um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="22beb-173">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 

    | <span data-ttu-id="22beb-174">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="22beb-174">Filter property</span></span>                                                   | <span data-ttu-id="22beb-175">Valor</span><span class="sxs-lookup"><span data-stu-id="22beb-175">Value</span></span>                                                                  |
    |-------------------------------------------------------------------|------------------------------------------------------------------------|
    | <span data-ttu-id="22beb-176">**FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição**</span><span class="sxs-lookup"><span data-stu-id="22beb-176">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="22beb-177">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="22beb-177">NlatUnicast</span></span>                                                            |
    | <span data-ttu-id="22beb-178">**FWPM \_ Condição de filtragem de \_ \_ protocolo IP de condição**</span><span class="sxs-lookup"><span data-stu-id="22beb-178">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="22beb-179">IPPROTO \_ ICMP {V6} essas constantes são definidas no Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="22beb-179">IPPROTO\_ICMP{V6}These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="22beb-180">**ação. tipo**</span><span class="sxs-lookup"><span data-stu-id="22beb-180">**action.type**</span></span>                                                   | <span data-ttu-id="22beb-181">**\_permissão de ação fwp \_**</span><span class="sxs-lookup"><span data-stu-id="22beb-181">**FWP\_ACTION\_PERMIT**</span></span>                                                |
    | <span data-ttu-id="22beb-182">**weight**</span><span class="sxs-lookup"><span data-stu-id="22beb-182">**weight**</span></span>                                                        | <span data-ttu-id="22beb-183">**\_ \_ isenções Ike de intervalo de peso FWPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22beb-183">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                               |

        

<span data-ttu-id="22beb-184">**Na camada FWPM de \_ \_ autenticação Ale, \_ \_ \_ aceite \_ V {4 \| 6} configurar regras de filtragem de entrada por conexão**</span><span class="sxs-lookup"><span data-stu-id="22beb-184">**At FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6} setup inbound per-connection filtering rules**</span></span>  

1.  <span data-ttu-id="22beb-185">Adicione um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="22beb-185">Add a filter with the following properties.</span></span> <span data-ttu-id="22beb-186">Esse filtro só permitirá tentativas de conexão de entrada se elas forem protegidas pelo IPsec.</span><span class="sxs-lookup"><span data-stu-id="22beb-186">This filter will only allow inbound connection attempts if they are secured by IPsec.</span></span> 

    | <span data-ttu-id="22beb-187">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="22beb-187">Filter property</span></span>                                                   | <span data-ttu-id="22beb-188">Valor</span><span class="sxs-lookup"><span data-stu-id="22beb-188">Value</span></span>                                                        |
    |-------------------------------------------------------------------|--------------------------------------------------------------|
    | <span data-ttu-id="22beb-189">**FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição**</span><span class="sxs-lookup"><span data-stu-id="22beb-189">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="22beb-190">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="22beb-190">NlatUnicast</span></span>                                                  |
    | <span data-ttu-id="22beb-191">**ação. tipo**</span><span class="sxs-lookup"><span data-stu-id="22beb-191">**action.type**</span></span>                                                   | <span data-ttu-id="22beb-192">**o \_ \_ texto explicativo de ação fwp \_ termina**</span><span class="sxs-lookup"><span data-stu-id="22beb-192">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                        |
    | <span data-ttu-id="22beb-193">**ação. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="22beb-193">**action.calloutKey**</span></span>                                             | <span data-ttu-id="22beb-194">**FWPM \_ texto explicativo \_ IPSec de \_ entrada \_ Iniciar \_ segurança \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="22beb-194">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V{4\|6}**</span></span> |

        
2.  <span data-ttu-id="22beb-195">Isentar o tráfego ICMP do IPsec adicionando um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="22beb-195">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 

    | <span data-ttu-id="22beb-196">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="22beb-196">Filter property</span></span>                                                   | <span data-ttu-id="22beb-197">Valor</span><span class="sxs-lookup"><span data-stu-id="22beb-197">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="22beb-198">**FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição**</span><span class="sxs-lookup"><span data-stu-id="22beb-198">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="22beb-199">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="22beb-199">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="22beb-200">**FWPM \_ Condição de filtragem de \_ \_ protocolo IP de condição**</span><span class="sxs-lookup"><span data-stu-id="22beb-200">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="22beb-201">**IPPROTO \_ ICMP {V6}** essas constantes são definidas no Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="22beb-201">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="22beb-202">**ação. tipo**</span><span class="sxs-lookup"><span data-stu-id="22beb-202">**action.type**</span></span>                                                   | <span data-ttu-id="22beb-203">**\_permissão de ação fwp \_**</span><span class="sxs-lookup"><span data-stu-id="22beb-203">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="22beb-204">**weight**</span><span class="sxs-lookup"><span data-stu-id="22beb-204">**weight**</span></span>                                                        | <span data-ttu-id="22beb-205">**\_ \_ isenções Ike de intervalo de peso FWPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22beb-205">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        
3.  <span data-ttu-id="22beb-206">Adicione um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="22beb-206">Add a filter with the following properties.</span></span> <span data-ttu-id="22beb-207">Esse filtro permitirá conexões de entrada para a porta TCP 5555 se as identidades remotas correspondentes forem permitidas por SD1 e SD2.</span><span class="sxs-lookup"><span data-stu-id="22beb-207">This filter will permit inbound connections to TCP port 5555 if the corresponding remote identities are allowed by both SD1 and SD2.</span></span> 

    | <span data-ttu-id="22beb-208">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="22beb-208">Filter property</span></span>                                                   | <span data-ttu-id="22beb-209">Valor</span><span class="sxs-lookup"><span data-stu-id="22beb-209">Value</span></span>                                                              |
    |-------------------------------------------------------------------|--------------------------------------------------------------------|
    | <span data-ttu-id="22beb-210">**FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição**</span><span class="sxs-lookup"><span data-stu-id="22beb-210">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="22beb-211">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="22beb-211">NlatUnicast</span></span>                                                        |
    | <span data-ttu-id="22beb-212">**FWPM \_ Condição de filtragem de \_ \_ protocolo IP de condição**</span><span class="sxs-lookup"><span data-stu-id="22beb-212">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="22beb-213">**IPPROTO \_ TCP** essa constante é definida no Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="22beb-213">**IPPROTO\_TCP** This constant is defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="22beb-214">**FWPM \_ Condição de filtragem de \_ \_ \_ porta local de IP de condição**</span><span class="sxs-lookup"><span data-stu-id="22beb-214">**FWPM\_CONDITION\_IP\_LOCAL\_PORT** filtering condition</span></span>          | <span data-ttu-id="22beb-215">5555</span><span class="sxs-lookup"><span data-stu-id="22beb-215">5555</span></span>                                                               |
    | <span data-ttu-id="22beb-216">**\_ID da \_ \_ máquina remota \_ Ale \_ da condição FWPM**</span><span class="sxs-lookup"><span data-stu-id="22beb-216">**FWPM\_CONDITION\_ALE\_REMOTE\_MACHINE\_ID**</span></span>                     | <span data-ttu-id="22beb-217">SD1</span><span class="sxs-lookup"><span data-stu-id="22beb-217">SD1</span></span>                                                                |
    | <span data-ttu-id="22beb-218">**\_ID de \_ \_ usuário remoto \_ Ale \_ da condição FWPM**</span><span class="sxs-lookup"><span data-stu-id="22beb-218">**FWPM\_CONDITION\_ALE\_REMOTE\_USER\_ID**</span></span>                        | <span data-ttu-id="22beb-219">SD2</span><span class="sxs-lookup"><span data-stu-id="22beb-219">SD2</span></span>                                                                |
    | <span data-ttu-id="22beb-220">**ação. tipo**</span><span class="sxs-lookup"><span data-stu-id="22beb-220">**action.type**</span></span>                                                   | <span data-ttu-id="22beb-221">**o \_ \_ texto explicativo de ação fwp \_ termina**</span><span class="sxs-lookup"><span data-stu-id="22beb-221">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                              |
    | <span data-ttu-id="22beb-222">**ação. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="22beb-222">**action.calloutKey**</span></span>                                             | <span data-ttu-id="22beb-223">**FWPM \_ texto explicativo \_ IPSec de \_ entrada \_ Iniciar \_ segurança \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="22beb-223">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V{4\|6}**</span></span>       |

        
4.  <span data-ttu-id="22beb-224">Adicione um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="22beb-224">Add a filter with the following properties.</span></span> <span data-ttu-id="22beb-225">Esse filtro bloqueará quaisquer outras conexões de entrada para a porta TCP 5555 que não correspondam ao filtro anterior.</span><span class="sxs-lookup"><span data-stu-id="22beb-225">This filter will block any other inbound connections to TCP port 5555 that did not match the previous filter.</span></span> 

    | <span data-ttu-id="22beb-226">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="22beb-226">Filter property</span></span>                                                   | <span data-ttu-id="22beb-227">Valor</span><span class="sxs-lookup"><span data-stu-id="22beb-227">Value</span></span>                                                              |
    |-------------------------------------------------------------------|--------------------------------------------------------------------|
    | <span data-ttu-id="22beb-228">**FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição**</span><span class="sxs-lookup"><span data-stu-id="22beb-228">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="22beb-229">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="22beb-229">NlatUnicast</span></span>                                                        |
    | <span data-ttu-id="22beb-230">**FWPM \_ Condição de filtragem de \_ \_ protocolo IP de condição**</span><span class="sxs-lookup"><span data-stu-id="22beb-230">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="22beb-231">**IPPROTO \_ TCP** essa constante é definida no Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="22beb-231">**IPPROTO\_TCP** This constant is defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="22beb-232">**FWPM \_ Condição de filtragem de \_ \_ \_ porta local de IP de condição**</span><span class="sxs-lookup"><span data-stu-id="22beb-232">**FWPM\_CONDITION\_IP\_LOCAL\_PORT** filtering condition</span></span>          | <span data-ttu-id="22beb-233">5555</span><span class="sxs-lookup"><span data-stu-id="22beb-233">5555</span></span>                                                               |
    | <span data-ttu-id="22beb-234">**ação. tipo**</span><span class="sxs-lookup"><span data-stu-id="22beb-234">**action.type**</span></span>                                                   | <span data-ttu-id="22beb-235">**\_bloco de ação fwp \_**</span><span class="sxs-lookup"><span data-stu-id="22beb-235">**FWP\_ACTION\_BLOCK**</span></span>                                             |

        

</dl>

## <a name="related-topics"></a><span data-ttu-id="22beb-236">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="22beb-236">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22beb-237">Código de exemplo: usando o modo de transporte</span><span class="sxs-lookup"><span data-stu-id="22beb-237">Sample code: Using Transport Mode</span></span>](using-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="22beb-238">Camadas ALE</span><span class="sxs-lookup"><span data-stu-id="22beb-238">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="22beb-239">**Identificadores de texto explicativo internos**</span><span class="sxs-lookup"><span data-stu-id="22beb-239">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> <dt>

[<span data-ttu-id="22beb-240">Condições de filtragem</span><span class="sxs-lookup"><span data-stu-id="22beb-240">Filtering Conditions</span></span>](filtering-conditions.md)
</dt> <dt>

[<span data-ttu-id="22beb-241">**Filtrando identificadores de camada**</span><span class="sxs-lookup"><span data-stu-id="22beb-241">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="22beb-242">**FWPM \_ ACTION0**</span><span class="sxs-lookup"><span data-stu-id="22beb-242">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[<span data-ttu-id="22beb-243">**\_tipo de \_ contexto do provedor FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="22beb-243">**FWPM\_PROVIDER\_CONTEXT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 


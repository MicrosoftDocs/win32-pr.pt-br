---
title: Modo de transporte de descoberta de negociação
description: O cenário de política IPsec do modo de transporte da descoberta de negociação requer a proteção do modo de transporte IPsec para todo o tráfego de entrada correspondente e solicita a proteção de IPsec para correspondência do tráfego de saída.
ms.assetid: c08d9d03-7d77-43c2-8468-964b498b45f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 216fec869eca28dc0661a37d44cce3a1fd05b80a
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314809"
---
# <a name="negotiation-discovery-transport-mode"></a><span data-ttu-id="9649d-103">Modo de transporte de descoberta de negociação</span><span class="sxs-lookup"><span data-stu-id="9649d-103">Negotiation Discovery Transport Mode</span></span>

<span data-ttu-id="9649d-104">O cenário de política IPsec do modo de transporte da descoberta de negociação requer a proteção do modo de transporte IPsec para todo o tráfego de entrada correspondente e solicita a proteção de IPsec para correspondência do tráfego de saída.</span><span class="sxs-lookup"><span data-stu-id="9649d-104">The Negotiation Discovery Transport Mode IPsec policy scenario requires IPsec transport mode protection for all matching inbound traffic, and requests IPsec protection for matching outbound traffic.</span></span> <span data-ttu-id="9649d-105">Portanto, as conexões de saída têm permissão para fazer fallback para texto não criptografado enquanto as conexões de entrada não são.</span><span class="sxs-lookup"><span data-stu-id="9649d-105">Therefore, outbound connections are allowed to fallback to clear-text while inbound connections are not.</span></span>

<span data-ttu-id="9649d-106">Com essa política, quando o computador host tenta uma nova conexão de saída e não há nenhuma SA IPsec existente que corresponda ao tráfego, o host envia simultaneamente os pacotes em texto não criptografado e inicia uma negociação IKE ou AuthIP.</span><span class="sxs-lookup"><span data-stu-id="9649d-106">With this policy, when the host machine attempts a new outbound connection and there is no existing IPsec SA matching the traffic, the host simultaneously sends the packets in clear-text and starts an IKE or AuthIP negotiation.</span></span> <span data-ttu-id="9649d-107">Se a negociação for realizada com sucesso, a conexão será atualizada para protegido por IPsec.</span><span class="sxs-lookup"><span data-stu-id="9649d-107">If the negotiation succeeds, the connection is upgraded to IPsec-protected.</span></span> <span data-ttu-id="9649d-108">Caso contrário, a conexão permanecerá em texto não criptografado.</span><span class="sxs-lookup"><span data-stu-id="9649d-108">Otherwise, the connection stays in clear-text.</span></span> <span data-ttu-id="9649d-109">Depois de protegida por IPsec, uma conexão nunca pode ser rebaixada para texto não criptografado.</span><span class="sxs-lookup"><span data-stu-id="9649d-109">Once IPsec-protected, a connection can never be downgraded to clear-text.</span></span>

<span data-ttu-id="9649d-110">O modo de transporte de descoberta de negociação normalmente é usado em ambientes que incluem máquinas compatíveis com IPsec e não com IPsec.</span><span class="sxs-lookup"><span data-stu-id="9649d-110">Negotiation Discovery Transport Mode is typically used in environments that include both IPsec capable and non-IPsec capable machines.</span></span>

<span data-ttu-id="9649d-111">Um exemplo de cenário de modo de transporte de descoberta de negociação é "proteger todo o tráfego de dados unicast, exceto ICMP, usando o modo de transporte IPsec e habilitar a descoberta de negociação".</span><span class="sxs-lookup"><span data-stu-id="9649d-111">An example of a possible Negotiation Discovery Transport Mode scenario is "Secure all unicast data traffic, except ICMP, using IPsec transport mode, and enable negotiation discovery."</span></span>

<span data-ttu-id="9649d-112">Para implementar este exemplo programaticamente, use a seguinte configuração de WFP.</span><span class="sxs-lookup"><span data-stu-id="9649d-112">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="9649d-113">**Na \_ camada FWPM \_ IKEEXT \_ V {4 \| 6} configurar a política de negociação mm**</span><span class="sxs-lookup"><span data-stu-id="9649d-113">**At FWPM\_LAYER\_IKEEXT\_V{4\|6} set up MM negotiation policy**</span></span>  

1.  <span data-ttu-id="9649d-114">Adicione um ou ambos os seguintes contextos do provedor de política MM.</span><span class="sxs-lookup"><span data-stu-id="9649d-114">Add one or both of the following MM policy provider contexts.</span></span>  
    -   <span data-ttu-id="9649d-115">Para IKE, um contexto de provedor de política do tipo **FWPM \_ IPSec \_ Ike \_ mm \_ Context**.</span><span class="sxs-lookup"><span data-stu-id="9649d-115">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_MM\_CONTEXT**.</span></span>
    -   <span data-ttu-id="9649d-116">Para AuthIP, um contexto de provedor de política do tipo **FWPM \_ IPSec \_ AuthIP \_ mm \_ Context**.</span><span class="sxs-lookup"><span data-stu-id="9649d-116">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT**.</span></span>

    > [!Note]  
    > <span data-ttu-id="9649d-117">Um módulo de chave comum será negociado e a política MM correspondente será aplicada.</span><span class="sxs-lookup"><span data-stu-id="9649d-117">A common keying module will be negotiated and the corresponding MM policy will be applied.</span></span> <span data-ttu-id="9649d-118">AuthIP é o módulo de chaveamento preferencial se o IKE e o AuthIP tiverem suporte.</span><span class="sxs-lookup"><span data-stu-id="9649d-118">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="9649d-119">Para cada um dos contextos adicionados na etapa 1, adicione um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="9649d-119">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 

    | <span data-ttu-id="9649d-120">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="9649d-120">Filter property</span></span>        | <span data-ttu-id="9649d-121">Valor</span><span class="sxs-lookup"><span data-stu-id="9649d-121">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="9649d-122">Condições de filtragem</span><span class="sxs-lookup"><span data-stu-id="9649d-122">Filtering conditions</span></span>   | <span data-ttu-id="9649d-123">Vazio.</span><span class="sxs-lookup"><span data-stu-id="9649d-123">Empty.</span></span> <span data-ttu-id="9649d-124">Todo o tráfego corresponderá ao filtro.</span><span class="sxs-lookup"><span data-stu-id="9649d-124">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="9649d-125">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="9649d-125">**providerContextKey**</span></span> | <span data-ttu-id="9649d-126">GUID do contexto do provedor MM adicionado na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="9649d-126">GUID of the MM provider context added in step 1.</span></span> |

        

<span data-ttu-id="9649d-127">**Na \_ camada FWPM \_ IPSec \_ V {4 \| 6} configurar política de negociação QM e em**</span><span class="sxs-lookup"><span data-stu-id="9649d-127">**At FWPM\_LAYER\_IPSEC\_V{4\|6} set up QM and EM negotiation policy**</span></span>  

1.  <span data-ttu-id="9649d-128">Adicione um ou ambos os seguintes contextos de provedor de política de modo de transporte QM e defina o sinalizador [**\_ \_ \_ \_ seguro do sinalizador de política IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) .</span><span class="sxs-lookup"><span data-stu-id="9649d-128">Add one or both of the following QM transport mode policy provider contexts and set the [**IPSEC\_POLICY\_FLAG\_ND\_SECURE**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) flag.</span></span>  
    -   <span data-ttu-id="9649d-129">Para IKE, um contexto de provedor de política do tipo FWPM \_ IPSec de transporte de IP \_ \_ qm \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9649d-129">For IKE, a policy provider context of type FWPM\_IPSEC\_IKE\_QM\_TRANSPORT\_CONTEXT.</span></span>
    -   <span data-ttu-id="9649d-130">Para AuthIP, um contexto de provedor de política do \_ tipo \_ \_ contexto de transporte QM IPSec AuthIP de FWPM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9649d-130">For AuthIP, a policy provider context of type FWPM\_IPSEC\_AUTHIP\_QM\_TRANSPORT\_CONTEXT.</span></span> <span data-ttu-id="9649d-131">Esse contexto pode, opcionalmente, conter a política de negociação de modo estendido AuthIP (em).</span><span class="sxs-lookup"><span data-stu-id="9649d-131">This context can optionally contain the AuthIP Extended Mode (EM) negotiation policy.</span></span>

    > [!Note]  
    > <span data-ttu-id="9649d-132">Um módulo de chave comum será negociado e a política QM correspondente será aplicada.</span><span class="sxs-lookup"><span data-stu-id="9649d-132">A common keying module will be negotiated and the corresponding QM policy will be applied.</span></span> <span data-ttu-id="9649d-133">AuthIP é o módulo de chaveamento preferencial se o IKE e o AuthIP tiverem suporte.</span><span class="sxs-lookup"><span data-stu-id="9649d-133">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="9649d-134">Para cada um dos contextos adicionados na etapa 1, adicione um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="9649d-134">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 

    | <span data-ttu-id="9649d-135">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="9649d-135">Filter property</span></span>        | <span data-ttu-id="9649d-136">Valor</span><span class="sxs-lookup"><span data-stu-id="9649d-136">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="9649d-137">Condições de filtragem</span><span class="sxs-lookup"><span data-stu-id="9649d-137">Filtering conditions</span></span>   | <span data-ttu-id="9649d-138">Vazio.</span><span class="sxs-lookup"><span data-stu-id="9649d-138">Empty.</span></span> <span data-ttu-id="9649d-139">Todo o tráfego corresponderá ao filtro.</span><span class="sxs-lookup"><span data-stu-id="9649d-139">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="9649d-140">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="9649d-140">**providerContextKey**</span></span> | <span data-ttu-id="9649d-141">GUID do contexto de provedor QM adicionado na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="9649d-141">GUID of the QM provider context added in step 1.</span></span> |

        

<span data-ttu-id="9649d-142">**No \_ transporte de entrada da camada FWPM \_ \_ \_ V {4 \| 6} configurar regras de filtragem de entrada por pacote**</span><span class="sxs-lookup"><span data-stu-id="9649d-142">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} set up inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="9649d-143">Adicione um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="9649d-143">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="9649d-144">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="9649d-144">Filter property</span></span>                                                   | <span data-ttu-id="9649d-145">Valor</span><span class="sxs-lookup"><span data-stu-id="9649d-145">Value</span></span>                                                                                              |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="9649d-146">**FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição**</span><span class="sxs-lookup"><span data-stu-id="9649d-146">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | [<span data-ttu-id="9649d-147">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="9649d-147">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | <span data-ttu-id="9649d-148">**ação. tipo**</span><span class="sxs-lookup"><span data-stu-id="9649d-148">**action.type**</span></span>                                                   | <span data-ttu-id="9649d-149">**o \_ \_ texto explicativo de ação fwp \_ termina**</span><span class="sxs-lookup"><span data-stu-id="9649d-149">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                              |
    | <span data-ttu-id="9649d-150">**ação. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="9649d-150">**action.calloutKey**</span></span>                                             | <span data-ttu-id="9649d-151">**FWPM \_ texto explicativo \_ IPSec de \_ transporte de entrada \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="9649d-151">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                              |
    | <span data-ttu-id="9649d-152">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="9649d-152">**rawContext**</span></span>                                                    | [<span data-ttu-id="9649d-153">**\_segurança de \_ \_ conexão de persistência de entrada IPsec \_ \_ de contexto \_ de FWPM**</span><span class="sxs-lookup"><span data-stu-id="9649d-153">**FWPM\_CONTEXT\_IPSEC\_INBOUND\_PERSIST\_CONNECTION\_SECURITY**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="9649d-154">Isentar o tráfego ICMP do IPsec adicionando um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="9649d-154">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="9649d-155">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="9649d-155">Filter property</span></span>                                                   | <span data-ttu-id="9649d-156">Valor</span><span class="sxs-lookup"><span data-stu-id="9649d-156">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="9649d-157">**FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição**</span><span class="sxs-lookup"><span data-stu-id="9649d-157">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="9649d-158">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="9649d-158">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="9649d-159">**FWPM \_ Condição de filtragem de \_ \_ protocolo IP de condição**</span><span class="sxs-lookup"><span data-stu-id="9649d-159">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="9649d-160">**IPPROTO \_ ICMP {V6}** essas constantes são definidas no Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="9649d-160">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="9649d-161">**ação. tipo**</span><span class="sxs-lookup"><span data-stu-id="9649d-161">**action.type**</span></span>                                                   | <span data-ttu-id="9649d-162">**\_permissão de ação fwp \_**</span><span class="sxs-lookup"><span data-stu-id="9649d-162">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="9649d-163">**weight**</span><span class="sxs-lookup"><span data-stu-id="9649d-163">**weight**</span></span>                                                        | [<span data-ttu-id="9649d-164">**\_ \_ isenções Ike de intervalo de peso FWPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9649d-164">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md)  |

        

<span data-ttu-id="9649d-165">**No transporte de saída da camada do FWPM \_ \_ \_ \_ V {4 \| 6} configurar regras de filtragem por pacote de saída**</span><span class="sxs-lookup"><span data-stu-id="9649d-165">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} set up outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="9649d-166">Adicione um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="9649d-166">Add a filter with the following properties.</span></span>

    | <span data-ttu-id="9649d-167">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="9649d-167">Filter property</span></span>                                                   | <span data-ttu-id="9649d-168">Valor</span><span class="sxs-lookup"><span data-stu-id="9649d-168">Value</span></span>                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | <span data-ttu-id="9649d-169">**FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição**</span><span class="sxs-lookup"><span data-stu-id="9649d-169">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="9649d-170">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="9649d-170">NlatUnicast</span></span>                                                                               |
    | <span data-ttu-id="9649d-171">**ação. tipo**</span><span class="sxs-lookup"><span data-stu-id="9649d-171">**action.type**</span></span>                                                   | <span data-ttu-id="9649d-172">**o \_ \_ texto explicativo de ação fwp \_ termina**</span><span class="sxs-lookup"><span data-stu-id="9649d-172">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                     |
    | <span data-ttu-id="9649d-173">**ação. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="9649d-173">**action.calloutKey**</span></span>                                             | <span data-ttu-id="9649d-174">**FWPM do \_ balão de \_ \_ saída IPSec \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="9649d-174">**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                    |
    | <span data-ttu-id="9649d-175">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="9649d-175">**rawContext**</span></span>                                                    | [<span data-ttu-id="9649d-176">**\_descoberta de \_ \_ negociação de saída IPSec de contexto \_ FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="9649d-176">**FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_NEGOTIATE\_DISCOVER**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="9649d-177">Isentar o tráfego ICMP do IPsec adicionando um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="9649d-177">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="9649d-178">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="9649d-178">Filter property</span></span>                                                   | <span data-ttu-id="9649d-179">Valor</span><span class="sxs-lookup"><span data-stu-id="9649d-179">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="9649d-180">**FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição**</span><span class="sxs-lookup"><span data-stu-id="9649d-180">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="9649d-181">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="9649d-181">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="9649d-182">**FWPM \_ Condição de filtragem de \_ \_ protocolo IP de condição**</span><span class="sxs-lookup"><span data-stu-id="9649d-182">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="9649d-183">**IPPROTO \_ ICMP {V6}** essas constantes são definidas no Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="9649d-183">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="9649d-184">**ação. tipo**</span><span class="sxs-lookup"><span data-stu-id="9649d-184">**action.type**</span></span>                                                   | <span data-ttu-id="9649d-185">**\_permissão de ação fwp \_**</span><span class="sxs-lookup"><span data-stu-id="9649d-185">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="9649d-186">**weight**</span><span class="sxs-lookup"><span data-stu-id="9649d-186">**weight**</span></span>                                                        | <span data-ttu-id="9649d-187">**\_ \_ isenções Ike de intervalo de peso FWPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9649d-187">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        

<span data-ttu-id="9649d-188">**Na camada FWPM de \_ \_ autenticação Ale, \_ \_ \_ aceite \_ V {4 \| 6} configurar regras de filtragem de entrada por conexão**</span><span class="sxs-lookup"><span data-stu-id="9649d-188">**At FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6} set up inbound per-connection filtering rules**</span></span>  

1.  <span data-ttu-id="9649d-189">Adicione um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="9649d-189">Add a filter with the following properties.</span></span> <span data-ttu-id="9649d-190">Esse filtro só permitirá tentativas de conexão de entrada se elas forem protegidas pelo IPsec.</span><span class="sxs-lookup"><span data-stu-id="9649d-190">This filter will only allow inbound connection attempts if they are secured by IPsec.</span></span> 

    | <span data-ttu-id="9649d-191">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="9649d-191">Filter property</span></span>                                                   | <span data-ttu-id="9649d-192">Valor</span><span class="sxs-lookup"><span data-stu-id="9649d-192">Value</span></span>                                                        |
    |-------------------------------------------------------------------|--------------------------------------------------------------|
    | <span data-ttu-id="9649d-193">**FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição**</span><span class="sxs-lookup"><span data-stu-id="9649d-193">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="9649d-194">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="9649d-194">NlatUnicast</span></span>                                                  |
    | <span data-ttu-id="9649d-195">**ação. tipo**</span><span class="sxs-lookup"><span data-stu-id="9649d-195">**action.type**</span></span>                                                   | <span data-ttu-id="9649d-196">**o \_ \_ texto explicativo de ação fwp \_ termina**</span><span class="sxs-lookup"><span data-stu-id="9649d-196">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                        |
    | <span data-ttu-id="9649d-197">**ação. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="9649d-197">**action.calloutKey**</span></span>                                             | <span data-ttu-id="9649d-198">**FWPM \_ texto explicativo \_ IPSec de \_ entrada \_ Iniciar \_ segurança \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="9649d-198">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V{4\|6}**</span></span> |

        
2.  <span data-ttu-id="9649d-199">Isentar o tráfego ICMP do IPsec adicionando um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="9649d-199">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="9649d-200">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="9649d-200">Filter property</span></span>                                                   | <span data-ttu-id="9649d-201">Valor</span><span class="sxs-lookup"><span data-stu-id="9649d-201">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="9649d-202">**FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição**</span><span class="sxs-lookup"><span data-stu-id="9649d-202">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="9649d-203">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="9649d-203">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="9649d-204">**FWPM \_ Condição de filtragem de \_ \_ protocolo IP de condição**</span><span class="sxs-lookup"><span data-stu-id="9649d-204">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="9649d-205">**IPPROTO \_ ICMP {V6}** essas constantes são definidas no Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="9649d-205">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="9649d-206">**ação. tipo**</span><span class="sxs-lookup"><span data-stu-id="9649d-206">**action.type**</span></span>                                                   | <span data-ttu-id="9649d-207">**\_permissão de ação fwp \_**</span><span class="sxs-lookup"><span data-stu-id="9649d-207">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="9649d-208">**weight**</span><span class="sxs-lookup"><span data-stu-id="9649d-208">**weight**</span></span>                                                        | <span data-ttu-id="9649d-209">**\_ \_ isenções Ike de intervalo de peso FWPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9649d-209">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        

</dl>

## <a name="related-topics"></a><span data-ttu-id="9649d-210">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9649d-210">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9649d-211">Código de exemplo: usando o modo de transporte</span><span class="sxs-lookup"><span data-stu-id="9649d-211">Sample code: Using Transport Mode</span></span>](using-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="9649d-212">Camadas ALE</span><span class="sxs-lookup"><span data-stu-id="9649d-212">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="9649d-213">**Identificadores de texto explicativo internos**</span><span class="sxs-lookup"><span data-stu-id="9649d-213">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> <dt>

[<span data-ttu-id="9649d-214">Condições de filtragem</span><span class="sxs-lookup"><span data-stu-id="9649d-214">Filtering Conditions</span></span>](filtering-conditions.md)
</dt> <dt>

[<span data-ttu-id="9649d-215">**Filtrando identificadores de camada**</span><span class="sxs-lookup"><span data-stu-id="9649d-215">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="9649d-216">**FWPM \_ ACTION0**</span><span class="sxs-lookup"><span data-stu-id="9649d-216">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[<span data-ttu-id="9649d-217">**\_tipo de \_ contexto do provedor FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="9649d-217">**FWPM\_PROVIDER\_CONTEXT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 


---
title: Modo de transporte de descoberta de negociação no modo de limite
description: O modo de transporte da descoberta de negociação no modo de limite cenário de política IPsec solicita a proteção do modo de transporte IPsec para todo o tráfego correspondente.
ms.assetid: 36ae74b3-30f5-49bd-8855-6f3c0fb04d70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9869be61923bff1c392c5abe2bd98099a0c3c89f
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314589"
---
# <a name="negotiation-discovery-transport-mode-in-boundary-mode"></a><span data-ttu-id="ed630-103">Modo de transporte de descoberta de negociação no modo de limite</span><span class="sxs-lookup"><span data-stu-id="ed630-103">Negotiation Discovery Transport Mode in Boundary Mode</span></span>

<span data-ttu-id="ed630-104">O modo de transporte da descoberta de negociação no modo de limite cenário de política IPsec solicita a proteção do modo de transporte IPsec para todo o tráfego correspondente.</span><span class="sxs-lookup"><span data-stu-id="ed630-104">The Negotiation Discovery Transport Mode in Boundary Mode IPsec policy scenario requests IPsec transport mode protection for all matching traffic.</span></span> <span data-ttu-id="ed630-105">Se a negociação IKE/AuthIP falhar, as conexões de entrada e saída terão permissão para fazer fallback para o texto não criptografado.</span><span class="sxs-lookup"><span data-stu-id="ed630-105">If the IKE/AuthIP negotiation fails, both inbound and outbound connections are allowed to fallback to clear-text .</span></span>

<span data-ttu-id="ed630-106">Essa diretiva IPsec é normalmente usada em computadores que são acessados por máquinas compatíveis com IPsec e não com IPsec.</span><span class="sxs-lookup"><span data-stu-id="ed630-106">This IPsec policy is typically used on machines that are accessed by both IPsec capable and non-IPsec capable machines.</span></span>

<span data-ttu-id="ed630-107">Um exemplo de cenário de modo de transporte de descoberta de negociação potencial é "proteger todo o tráfego de dados unicast, exceto ICMP, usando o modo de transporte IPsec e habilitar a descoberta de negociação no modo de limite".</span><span class="sxs-lookup"><span data-stu-id="ed630-107">An example of a potential Negotiation Discovery Transport Mode scenario is "Secure all unicast data traffic, except ICMP, using IPsec transport mode and enable negotiation discovery in boundary mode."</span></span>

<span data-ttu-id="ed630-108">Para implementar este exemplo programaticamente, use a seguinte configuração de WFP.</span><span class="sxs-lookup"><span data-stu-id="ed630-108">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="ed630-109">**Na \_ camada FWPM \_ IKEEXT \_ V {4 \| 6} política de negociação de instalação mm**</span><span class="sxs-lookup"><span data-stu-id="ed630-109">**At FWPM\_LAYER\_IKEEXT\_V{4\|6} setup MM negotiation policy**</span></span>  

1.  <span data-ttu-id="ed630-110">Adicione um ou ambos os seguintes contextos do provedor de política MM.</span><span class="sxs-lookup"><span data-stu-id="ed630-110">Add one or both of the following MM policy provider contexts.</span></span>  
    -   <span data-ttu-id="ed630-111">Para IKE, um contexto de provedor de política do tipo FWPM \_ IPSec \_ Ike \_ mm \_ Context.</span><span class="sxs-lookup"><span data-stu-id="ed630-111">For IKE, a policy provider context of type FWPM\_IPSEC\_IKE\_MM\_CONTEXT.</span></span>
    -   <span data-ttu-id="ed630-112">Para AuthIP, um contexto de provedor de política do tipo FWPM \_ IPSec \_ AuthIP \_ mm \_ Context.</span><span class="sxs-lookup"><span data-stu-id="ed630-112">For AuthIP, a policy provider context of type FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT.</span></span>

    > [!Note]  
    > <span data-ttu-id="ed630-113">Um módulo de chave comum será negociado e a política MM correspondente será aplicada.</span><span class="sxs-lookup"><span data-stu-id="ed630-113">A common keying module will be negotiated and the corresponding MM policy will be applied.</span></span> <span data-ttu-id="ed630-114">AuthIP é o módulo de chaveamento preferencial se o IKE e o AuthIP tiverem suporte.</span><span class="sxs-lookup"><span data-stu-id="ed630-114">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="ed630-115">Para cada um dos contextos adicionados na etapa 1, adicione um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="ed630-115">For each of the contexts added in step 1, add a filter with the following properties.</span></span>

    | <span data-ttu-id="ed630-116">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="ed630-116">Filter property</span></span>        | <span data-ttu-id="ed630-117">Valor</span><span class="sxs-lookup"><span data-stu-id="ed630-117">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="ed630-118">Condições de filtragem</span><span class="sxs-lookup"><span data-stu-id="ed630-118">Filtering conditions</span></span>   | <span data-ttu-id="ed630-119">Vazio.</span><span class="sxs-lookup"><span data-stu-id="ed630-119">Empty.</span></span> <span data-ttu-id="ed630-120">Todo o tráfego corresponderá ao filtro.</span><span class="sxs-lookup"><span data-stu-id="ed630-120">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="ed630-121">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="ed630-121">**providerContextKey**</span></span> | <span data-ttu-id="ed630-122">GUID do contexto do provedor MM adicionado na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="ed630-122">GUID of the MM provider context added in step 1.</span></span> |

        

<span data-ttu-id="ed630-123">**Na \_ camada FWPM \_ IPSec \_ V {4 \| 6} configurar política de negociação QM e em**</span><span class="sxs-lookup"><span data-stu-id="ed630-123">**At FWPM\_LAYER\_IPSEC\_V{4\|6} setup QM and EM negotiation policy**</span></span>  

1.  <span data-ttu-id="ed630-124">Adicione um ou ambos os seguintes contextos de provedor de política de modo de transporte QM e defina o sinalizador de [**\_ \_ \_ \_ limite do sinalizador de política IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) .</span><span class="sxs-lookup"><span data-stu-id="ed630-124">Add one or both of the following QM transport mode policy provider contexts and set the [**IPSEC\_POLICY\_FLAG\_ND\_BOUNDARY**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) flag.</span></span>  
    -   <span data-ttu-id="ed630-125">Para IKE, um contexto de provedor de política do tipo **FWPM \_ IPSec de transporte de IP \_ \_ qm \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="ed630-125">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_QM\_TRANSPORT\_CONTEXT**.</span></span>
    -   <span data-ttu-id="ed630-126">Para AuthIP, um contexto de provedor de política do tipo **\_ \_ \_ \_ \_ contexto de transporte QM IPSec AuthIP de FWPM**.</span><span class="sxs-lookup"><span data-stu-id="ed630-126">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_QM\_TRANSPORT\_CONTEXT**.</span></span> <span data-ttu-id="ed630-127">Esse contexto pode, opcionalmente, conter a política de negociação de modo estendido AuthIP (em).</span><span class="sxs-lookup"><span data-stu-id="ed630-127">This context can optionally contain the AuthIP Extended Mode (EM) negotiation policy.</span></span>

    > [!Note]  
    > <span data-ttu-id="ed630-128">Um módulo de chave comum será negociado e a política QM correspondente será aplicada.</span><span class="sxs-lookup"><span data-stu-id="ed630-128">A common keying module will be negotiated and the corresponding QM policy will be applied.</span></span> <span data-ttu-id="ed630-129">AuthIP é o módulo de chaveamento preferencial se o IKE e o AuthIP tiverem suporte.</span><span class="sxs-lookup"><span data-stu-id="ed630-129">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="ed630-130">Para cada um dos contextos adicionados na etapa 1, adicione um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="ed630-130">For each of the contexts added in step 1, add a filter with the following properties.</span></span>

    | <span data-ttu-id="ed630-131">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="ed630-131">Filter property</span></span>        | <span data-ttu-id="ed630-132">Valor</span><span class="sxs-lookup"><span data-stu-id="ed630-132">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="ed630-133">Condições de filtragem</span><span class="sxs-lookup"><span data-stu-id="ed630-133">Filtering conditions</span></span>   | <span data-ttu-id="ed630-134">Vazio.</span><span class="sxs-lookup"><span data-stu-id="ed630-134">Empty.</span></span> <span data-ttu-id="ed630-135">Todo o tráfego corresponderá ao filtro.</span><span class="sxs-lookup"><span data-stu-id="ed630-135">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="ed630-136">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="ed630-136">**providerContextKey**</span></span> | <span data-ttu-id="ed630-137">GUID do contexto de provedor QM adicionado na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="ed630-137">GUID of the QM provider context added in step 1.</span></span> |

        

<span data-ttu-id="ed630-138">**Na \_ camada FWPM \_ transporte de \_ entrada \_ V {4 \| 6} configurar regras de filtragem de entrada por pacote**</span><span class="sxs-lookup"><span data-stu-id="ed630-138">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} setup inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="ed630-139">Adicione um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="ed630-139">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="ed630-140">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="ed630-140">Filter property</span></span>                                                   | <span data-ttu-id="ed630-141">Valor</span><span class="sxs-lookup"><span data-stu-id="ed630-141">Value</span></span>                                                                                              |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="ed630-142">**FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição**</span><span class="sxs-lookup"><span data-stu-id="ed630-142">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | [<span data-ttu-id="ed630-143">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="ed630-143">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | <span data-ttu-id="ed630-144">**ação. tipo**</span><span class="sxs-lookup"><span data-stu-id="ed630-144">**action.type**</span></span>                                                   | <span data-ttu-id="ed630-145">**o \_ \_ texto explicativo de ação fwp \_ termina**</span><span class="sxs-lookup"><span data-stu-id="ed630-145">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                              |
    | <span data-ttu-id="ed630-146">**ação. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="ed630-146">**action.calloutKey**</span></span>                                             | <span data-ttu-id="ed630-147">**FWPM \_ texto explicativo \_ IPSec de \_ transporte de entrada \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="ed630-147">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                              |
    | <span data-ttu-id="ed630-148">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="ed630-148">**rawContext**</span></span>                                                    | [<span data-ttu-id="ed630-149">**\_segurança de \_ \_ conexão de persistência de entrada IPsec \_ \_ de contexto \_ de FWPM**</span><span class="sxs-lookup"><span data-stu-id="ed630-149">**FWPM\_CONTEXT\_IPSEC\_INBOUND\_PERSIST\_CONNECTION\_SECURITY**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="ed630-150">Isentar o tráfego ICMP do IPsec adicionando um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="ed630-150">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="ed630-151">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="ed630-151">Filter property</span></span>                                                   | <span data-ttu-id="ed630-152">Valor</span><span class="sxs-lookup"><span data-stu-id="ed630-152">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="ed630-153">**FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição**</span><span class="sxs-lookup"><span data-stu-id="ed630-153">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="ed630-154">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="ed630-154">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="ed630-155">**FWPM \_ Condição de filtragem de \_ \_ protocolo IP de condição**</span><span class="sxs-lookup"><span data-stu-id="ed630-155">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="ed630-156">**IPPROTO \_ ICMP {V6}** essas constantes são definidas no Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="ed630-156">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="ed630-157">**ação. tipo**</span><span class="sxs-lookup"><span data-stu-id="ed630-157">**action.type**</span></span>                                                   | <span data-ttu-id="ed630-158">\_permissão de ação fwp \_</span><span class="sxs-lookup"><span data-stu-id="ed630-158">FWP\_ACTION\_PERMIT</span></span>                                                        |
    | <span data-ttu-id="ed630-159">**weight**</span><span class="sxs-lookup"><span data-stu-id="ed630-159">**weight**</span></span>                                                        | [<span data-ttu-id="ed630-160">**\_ \_ isenções Ike de intervalo de peso FWPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ed630-160">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md)  |

        

<span data-ttu-id="ed630-161">**Em FWPM \_ camada de \_ saída do \_ transporte \_ V {4 \| 6} configurar regras de filtragem por pacote de saída**</span><span class="sxs-lookup"><span data-stu-id="ed630-161">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} setup outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="ed630-162">Adicione um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="ed630-162">Add a filter with the following properties.</span></span>

    | <span data-ttu-id="ed630-163">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="ed630-163">Filter property</span></span>                                                   | <span data-ttu-id="ed630-164">Valor</span><span class="sxs-lookup"><span data-stu-id="ed630-164">Value</span></span>                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | <span data-ttu-id="ed630-165">**FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição**</span><span class="sxs-lookup"><span data-stu-id="ed630-165">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="ed630-166">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="ed630-166">NlatUnicast</span></span>                                                                               |
    | <span data-ttu-id="ed630-167">**ação. tipo**</span><span class="sxs-lookup"><span data-stu-id="ed630-167">**action.type**</span></span>                                                   | <span data-ttu-id="ed630-168">**o \_ \_ texto explicativo de ação fwp \_ termina**</span><span class="sxs-lookup"><span data-stu-id="ed630-168">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                     |
    | <span data-ttu-id="ed630-169">**ação. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="ed630-169">**action.calloutKey**</span></span>                                             | <span data-ttu-id="ed630-170">**FWPM do \_ balão de \_ \_ saída IPSec \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="ed630-170">**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                    |
    | <span data-ttu-id="ed630-171">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="ed630-171">**rawContext**</span></span>                                                    | [<span data-ttu-id="ed630-172">**\_descoberta de \_ \_ negociação de saída IPSec de contexto \_ FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="ed630-172">**FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_NEGOTIATE\_DISCOVER**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="ed630-173">Isentar o tráfego ICMP do IPsec adicionando um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="ed630-173">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="ed630-174">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="ed630-174">Filter property</span></span>                                                   | <span data-ttu-id="ed630-175">Valor</span><span class="sxs-lookup"><span data-stu-id="ed630-175">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="ed630-176">**FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição**</span><span class="sxs-lookup"><span data-stu-id="ed630-176">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="ed630-177">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="ed630-177">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="ed630-178">**FWPM \_ Condição de filtragem de \_ \_ protocolo IP de condição**</span><span class="sxs-lookup"><span data-stu-id="ed630-178">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="ed630-179">**IPPROTO \_ ICMP {V6}** essas constantes são definidas no Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="ed630-179">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="ed630-180">**ação. tipo**</span><span class="sxs-lookup"><span data-stu-id="ed630-180">**action.type**</span></span>                                                   | <span data-ttu-id="ed630-181">**\_permissão de ação fwp \_**</span><span class="sxs-lookup"><span data-stu-id="ed630-181">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="ed630-182">**weight**</span><span class="sxs-lookup"><span data-stu-id="ed630-182">**weight**</span></span>                                                        | <span data-ttu-id="ed630-183">**\_ \_ isenções Ike de intervalo de peso FWPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ed630-183">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        

</dl>

> [!Note]  
> <span data-ttu-id="ed630-184">Em oposição ao modo de transporte de descoberta de negociação, para o modo de transporte de descoberta de negociação na política de modo de limite, não há necessidade de adicionar um filtro nas camadas de **\_ recebimento de autenticação Ale de camada FWPM \_ \_ \_ \_ \_ V {4 \| 6}** , pois essa política permite conexões de texto não criptografado de entrada não protegidas.</span><span class="sxs-lookup"><span data-stu-id="ed630-184">As opposed to Negotiation Discovery Transport Mode, for Negotiation Discovery Transport Mode in Boundary Mode policy there is no need to add a filter at the **FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}** layers because this policy allows inbound unprotected clear-text connections.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ed630-185">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ed630-185">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed630-186">Código de exemplo: usando o modo de transporte</span><span class="sxs-lookup"><span data-stu-id="ed630-186">Sample code: Using Transport Mode</span></span>](using-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="ed630-187">Camadas ALE</span><span class="sxs-lookup"><span data-stu-id="ed630-187">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="ed630-188">**Identificadores de texto explicativo internos**</span><span class="sxs-lookup"><span data-stu-id="ed630-188">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> <dt>

[<span data-ttu-id="ed630-189">Condições de filtragem</span><span class="sxs-lookup"><span data-stu-id="ed630-189">Filtering Conditions</span></span>](filtering-conditions.md)
</dt> <dt>

[<span data-ttu-id="ed630-190">**Filtrando identificadores de camada**</span><span class="sxs-lookup"><span data-stu-id="ed630-190">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="ed630-191">**FWPM \_ ACTION0**</span><span class="sxs-lookup"><span data-stu-id="ed630-191">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[<span data-ttu-id="ed630-192">**\_tipo de \_ contexto do provedor FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="ed630-192">**FWPM\_PROVIDER\_CONTEXT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 


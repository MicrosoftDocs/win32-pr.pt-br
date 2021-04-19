---
title: Criptografia garantida
description: O cenário de política IPsec de criptografia garantida requer criptografia IPsec para todo o tráfego correspondente. Essa política deve ser especificada em conjunto com uma das opções de política do modo de transporte.
ms.assetid: 68758f0c-f134-4b7a-820a-313e2a82f280
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbffa3d78a9e178850f3afaa4d6b7fa9831be875
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314639"
---
# <a name="guaranteed-encryption"></a><span data-ttu-id="c3e4f-104">Criptografia garantida</span><span class="sxs-lookup"><span data-stu-id="c3e4f-104">Guaranteed Encryption</span></span>

<span data-ttu-id="c3e4f-105">O cenário de política IPsec de criptografia garantida requer criptografia IPsec para todo o tráfego correspondente.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-105">The Guaranteed Encryption IPsec policy scenario requires IPsec encryption for all matching traffic.</span></span> <span data-ttu-id="c3e4f-106">Essa política deve ser especificada em conjunto com uma das opções de política do modo de transporte.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-106">This policy must be specified in conjunction with one of the transport mode policy options.</span></span>

<span data-ttu-id="c3e4f-107">A criptografia garantida normalmente é usada para criptografar o tráfego confidencial por aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-107">Guaranteed Encryption is typically used to encrypt sensitive traffic on a per application basis.</span></span>

<span data-ttu-id="c3e4f-108">Um exemplo de um possível cenário de criptografia garantida é "proteger todo o tráfego de dados unicast, exceto ICMP, usar o modo de transporte IPsec, habilitar a descoberta de negociação e exigir a criptografia garantida para todo o tráfego unicast correspondente à porta local TCP 5555".</span><span class="sxs-lookup"><span data-stu-id="c3e4f-108">An example of a possible Guaranteed Encryption scenario is "Secure all unicast data traffic, except ICMP, using IPsec transport mode, enable negotiation discovery, and require guaranteed encryption for all unicast traffic corresponding to TCP local port 5555."</span></span>

<span data-ttu-id="c3e4f-109">Para implementar este exemplo programaticamente, use a seguinte configuração de WFP.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-109">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="c3e4f-110">**Na \_ camada FWPM \_ IKEEXT \_ V {4 \| 6} política de negociação de instalação mm**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-110">**At FWPM\_LAYER\_IKEEXT\_V{4\|6} setup MM negotiation policy**</span></span>  

1.  <span data-ttu-id="c3e4f-111">Adicione um ou ambos os seguintes contextos do provedor de política MM.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-111">Add one or both of the following MM policy provider contexts.</span></span>  
    -   <span data-ttu-id="c3e4f-112">Para IKE, um contexto de provedor de política do tipo FWPM \_ IPSec \_ Ike \_ mm \_ Context.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-112">For IKE, a policy provider context of type FWPM\_IPSEC\_IKE\_MM\_CONTEXT.</span></span>
    -   <span data-ttu-id="c3e4f-113">Para AuthIP, um contexto de provedor de política do tipo FWPM \_ IPSec \_ AuthIP \_ mm \_ Context.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-113">For AuthIP, a policy provider context of type FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT.</span></span>

    > [!Note]  
    > <span data-ttu-id="c3e4f-114">Um módulo de chave comum será negociado e a política MM correspondente será aplicada.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-114">A common keying module will be negotiated and the corresponding MM policy will be applied.</span></span> <span data-ttu-id="c3e4f-115">AuthIP é o módulo de chaveamento preferencial se o IKE e o AuthIP tiverem suporte.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-115">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="c3e4f-116">Para cada um dos contextos adicionados na etapa 1, adicione um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-116">For each of the contexts added in step 1, add a filter with the following properties.</span></span>

    | <span data-ttu-id="c3e4f-117">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="c3e4f-117">Filter property</span></span>        | <span data-ttu-id="c3e4f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c3e4f-118">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="c3e4f-119">Condições de filtragem</span><span class="sxs-lookup"><span data-stu-id="c3e4f-119">Filtering conditions</span></span>   | <span data-ttu-id="c3e4f-120">Vazio.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-120">Empty.</span></span> <span data-ttu-id="c3e4f-121">Todo o tráfego corresponderá ao filtro.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-121">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="c3e4f-122">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-122">**providerContextKey**</span></span> | <span data-ttu-id="c3e4f-123">GUID do contexto do provedor MM adicionado na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-123">GUID of the MM provider context added in step 1.</span></span> |

        

<span data-ttu-id="c3e4f-124">**Na \_ camada FWPM \_ IPSec \_ V {4 \| 6} configurar política de negociação QM e em**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-124">**At FWPM\_LAYER\_IPSEC\_V{4\|6} setup QM and EM negotiation policy**</span></span>  

1.  <span data-ttu-id="c3e4f-125">Adicione um ou ambos os seguintes contextos de provedor de política de modo de transporte QM e defina o sinalizador [**\_ \_ \_ \_ seguro do sinalizador de política IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) .</span><span class="sxs-lookup"><span data-stu-id="c3e4f-125">Add one or both of the following QM transport mode policy provider contexts and set the [**IPSEC\_POLICY\_FLAG\_ND\_SECURE**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) flag.</span></span>  
    -   <span data-ttu-id="c3e4f-126">Para IKE, um contexto de provedor de política do tipo **FWPM \_ IPSec de transporte de IP \_ \_ qm \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-126">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_QM\_TRANSPORT\_CONTEXT**.</span></span>
    -   <span data-ttu-id="c3e4f-127">Para AuthIP, um contexto de provedor de política do tipo **\_ \_ \_ \_ \_ contexto de transporte QM IPSec AuthIP de FWPM**.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-127">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_QM\_TRANSPORT\_CONTEXT**.</span></span> <span data-ttu-id="c3e4f-128">Esse contexto pode, opcionalmente, conter a política de negociação de modo estendido AuthIP (em).</span><span class="sxs-lookup"><span data-stu-id="c3e4f-128">This context can optionally contain the AuthIP Extended Mode (EM) negotiation policy.</span></span>

    > [!Note]  
    > <span data-ttu-id="c3e4f-129">Um módulo de chave comum será negociado e a política QM correspondente será aplicada.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-129">A common keying module will be negotiated and the corresponding QM policy will be applied.</span></span> <span data-ttu-id="c3e4f-130">AuthIP é o módulo de chaveamento preferencial se o IKE e o AuthIP tiverem suporte.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-130">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="c3e4f-131">Para cada um dos contextos adicionados na etapa 1, adicione um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-131">For each of the contexts added in step 1, add a filter with the following properties.</span></span>

    | <span data-ttu-id="c3e4f-132">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="c3e4f-132">Filter property</span></span>        | <span data-ttu-id="c3e4f-133">Valor</span><span class="sxs-lookup"><span data-stu-id="c3e4f-133">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="c3e4f-134">Condições de filtragem</span><span class="sxs-lookup"><span data-stu-id="c3e4f-134">Filtering conditions</span></span>   | <span data-ttu-id="c3e4f-135">Vazio.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-135">Empty.</span></span> <span data-ttu-id="c3e4f-136">Todo o tráfego corresponderá ao filtro.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-136">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="c3e4f-137">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-137">**providerContextKey**</span></span> | <span data-ttu-id="c3e4f-138">GUID do contexto de provedor QM adicionado na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-138">GUID of the QM provider context added in step 1.</span></span> |

        

<span data-ttu-id="c3e4f-139">**Na \_ camada FWPM \_ transporte de \_ entrada \_ V {4 \| 6} configurar regras de filtragem de entrada por pacote**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-139">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} setup inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="c3e4f-140">Adicione um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-140">Add a filter with the following properties.</span></span> 

    | <span data-ttu-id="c3e4f-141">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="c3e4f-141">Filter property</span></span>                                               | <span data-ttu-id="c3e4f-142">Valor</span><span class="sxs-lookup"><span data-stu-id="c3e4f-142">Value</span></span>                                                                                              |
    |---------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="c3e4f-143">\_Condição de \_ filtragem \_ de \_ tipo de endereço local IP de condição FWPM \_</span><span class="sxs-lookup"><span data-stu-id="c3e4f-143">FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE filtering condition</span></span> | [<span data-ttu-id="c3e4f-144">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="c3e4f-144">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | <span data-ttu-id="c3e4f-145">**ação. tipo**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-145">**action.type**</span></span>                                               | <span data-ttu-id="c3e4f-146">**o \_ \_ texto explicativo de ação fwp \_ termina**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-146">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                              |
    | <span data-ttu-id="c3e4f-147">**ação. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-147">**action.calloutKey**</span></span>                                         | <span data-ttu-id="c3e4f-148">**FWPM \_ texto explicativo \_ IPSec de \_ transporte de entrada \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-148">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                              |
    | <span data-ttu-id="c3e4f-149">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-149">**rawContext**</span></span>                                                | [<span data-ttu-id="c3e4f-150">**\_segurança de \_ \_ conexão de persistência de entrada IPsec \_ \_ de contexto \_ de FWPM**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-150">**FWPM\_CONTEXT\_IPSEC\_INBOUND\_PERSIST\_CONNECTION\_SECURITY**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="c3e4f-151">Isentar o tráfego ICMP do IPsec adicionando um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-151">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="c3e4f-152">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="c3e4f-152">Filter property</span></span>                                                   | <span data-ttu-id="c3e4f-153">Valor</span><span class="sxs-lookup"><span data-stu-id="c3e4f-153">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="c3e4f-154">**FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-154">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="c3e4f-155">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="c3e4f-155">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="c3e4f-156">**FWPM \_ Condição de filtragem de \_ \_ protocolo IP de condição**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-156">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="c3e4f-157">**IPPROTO \_ ICMP {V6}** essas constantes são definidas no Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-157">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="c3e4f-158">**ação. tipo**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-158">**action.type**</span></span>                                                   | <span data-ttu-id="c3e4f-159">**\_permissão de ação fwp \_**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-159">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="c3e4f-160">**weight**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-160">**weight**</span></span>                                                        | [<span data-ttu-id="c3e4f-161">**\_ \_ isenções Ike de intervalo de peso FWPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-161">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md)  |

        

<span data-ttu-id="c3e4f-162">**Em FWPM \_ camada de \_ saída do \_ transporte \_ V {4 \| 6} configurar regras de filtragem por pacote de saída**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-162">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} setup outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="c3e4f-163">Adicione um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-163">Add a filter with the following properties.</span></span>

    | <span data-ttu-id="c3e4f-164">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="c3e4f-164">Filter property</span></span>                                                   | <span data-ttu-id="c3e4f-165">Valor</span><span class="sxs-lookup"><span data-stu-id="c3e4f-165">Value</span></span>                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | <span data-ttu-id="c3e4f-166">**FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-166">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="c3e4f-167">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="c3e4f-167">NlatUnicast</span></span>                                                                               |
    | <span data-ttu-id="c3e4f-168">**ação. tipo**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-168">**action.type**</span></span>                                                   | <span data-ttu-id="c3e4f-169">**o \_ \_ texto explicativo de ação fwp \_ termina**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-169">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                     |
    | <span data-ttu-id="c3e4f-170">**ação. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-170">**action.calloutKey**</span></span>                                             | <span data-ttu-id="c3e4f-171">**FWPM do \_ balão de \_ \_ saída IPSec \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-171">**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}**</span></span>                                    |
    | <span data-ttu-id="c3e4f-172">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-172">**rawContext**</span></span>                                                    | [<span data-ttu-id="c3e4f-173">**\_descoberta de \_ \_ negociação de saída IPSec de contexto \_ FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-173">**FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_NEGOTIATE\_DISCOVER**</span></span>](filter-context-identifiers.md) |

        
2.  <span data-ttu-id="c3e4f-174">Isentar o tráfego ICMP do IPsec adicionando um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-174">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="c3e4f-175">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="c3e4f-175">Filter property</span></span>                                                   | <span data-ttu-id="c3e4f-176">Valor</span><span class="sxs-lookup"><span data-stu-id="c3e4f-176">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="c3e4f-177">**FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-177">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="c3e4f-178">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="c3e4f-178">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="c3e4f-179">**FWPM \_ Condição de filtragem de \_ \_ protocolo IP de condição**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-179">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="c3e4f-180">**IPPROTO \_ ICMP {V6}** essas constantes são definidas no Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-180">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="c3e4f-181">**ação. tipo**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-181">**action.type**</span></span>                                                   | <span data-ttu-id="c3e4f-182">**\_permissão de ação fwp \_**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-182">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="c3e4f-183">**weight**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-183">**weight**</span></span>                                                        | <span data-ttu-id="c3e4f-184">**\_ \_ isenções Ike de intervalo de peso FWPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-184">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        

<span data-ttu-id="c3e4f-185">**Na camada FWPM de \_ \_ autenticação Ale, \_ \_ \_ aceite \_ V {4 \| 6} configurar regras de filtragem de entrada por conexão**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-185">**At FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6} setup inbound per-connection filtering rules**</span></span>  

1.  <span data-ttu-id="c3e4f-186">Adicione um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-186">Add a filter with the following properties.</span></span> <span data-ttu-id="c3e4f-187">Esse filtro só permitirá tentativas de conexão de entrada se elas forem protegidas pelo IPsec.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-187">This filter will only allow inbound connection attempts if they are secured by IPsec.</span></span> 

    | <span data-ttu-id="c3e4f-188">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="c3e4f-188">Filter property</span></span>                                                   | <span data-ttu-id="c3e4f-189">Valor</span><span class="sxs-lookup"><span data-stu-id="c3e4f-189">Value</span></span>                                                        |
    |-------------------------------------------------------------------|--------------------------------------------------------------|
    | <span data-ttu-id="c3e4f-190">**FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-190">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="c3e4f-191">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="c3e4f-191">NlatUnicast</span></span>                                                  |
    | <span data-ttu-id="c3e4f-192">**ação. tipo**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-192">**action.type**</span></span>                                                   | <span data-ttu-id="c3e4f-193">**o \_ \_ texto explicativo de ação fwp \_ termina**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-193">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                        |
    | <span data-ttu-id="c3e4f-194">**ação. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-194">**action.calloutKey**</span></span>                                             | <span data-ttu-id="c3e4f-195">**FWPM \_ texto explicativo \_ IPSec de \_ entrada \_ Iniciar \_ segurança \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-195">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V{4\|6}**</span></span> |

        
2.  <span data-ttu-id="c3e4f-196">Isentar o tráfego ICMP do IPsec adicionando um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-196">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>

    | <span data-ttu-id="c3e4f-197">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="c3e4f-197">Filter property</span></span>                                                   | <span data-ttu-id="c3e4f-198">Valor</span><span class="sxs-lookup"><span data-stu-id="c3e4f-198">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="c3e4f-199">**FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-199">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="c3e4f-200">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="c3e4f-200">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="c3e4f-201">**FWPM \_ Condição de filtragem de \_ \_ protocolo IP de condição**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-201">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="c3e4f-202">**IPPROTO \_ ICMP {V6}** essas constantes são definidas no Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-202">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="c3e4f-203">**ação. tipo**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-203">**action.type**</span></span>                                                   | <span data-ttu-id="c3e4f-204">**\_permissão de ação fwp \_**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-204">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="c3e4f-205">**weight**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-205">**weight**</span></span>                                                        | <span data-ttu-id="c3e4f-206">**\_ \_ isenções Ike de intervalo de peso FWPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-206">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        
3.  <span data-ttu-id="c3e4f-207">Adicione um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-207">Add a filter with the following properties.</span></span> <span data-ttu-id="c3e4f-208">Esse filtro só permitirá conexões de entrada para a porta TCP 5555 se elas forem criptografadas.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-208">This filter will only permit inbound connections to TCP port 5555 if they are encrypted.</span></span>

    | <span data-ttu-id="c3e4f-209">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="c3e4f-209">Filter property</span></span>                                                   | <span data-ttu-id="c3e4f-210">Valor</span><span class="sxs-lookup"><span data-stu-id="c3e4f-210">Value</span></span>                                                                                                 |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="c3e4f-211">**FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-211">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="c3e4f-212">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="c3e4f-212">NlatUnicast</span></span>                                                                                           |
    | <span data-ttu-id="c3e4f-213">**FWPM \_ Condição de filtragem de \_ \_ protocolo IP de condição**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-213">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="c3e4f-214">**IPPROTO \_ TCP** essa constante é definida no Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-214">**IPPROTO\_TCP** This constant is defined in winsock2.h.</span></span><br/>                                    |
    | <span data-ttu-id="c3e4f-215">**FWPM \_ Condição de filtragem de \_ \_ \_ porta local de IP de condição**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-215">**FWPM\_CONDITION\_IP\_LOCAL\_PORT** filtering condition</span></span>          | <span data-ttu-id="c3e4f-216">5555</span><span class="sxs-lookup"><span data-stu-id="c3e4f-216">5555</span></span>                                                                                                  |
    | <span data-ttu-id="c3e4f-217">**ação. tipo**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-217">**action.type**</span></span>                                                   | <span data-ttu-id="c3e4f-218">**o \_ \_ texto explicativo de ação fwp \_ termina**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-218">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                                 |
    | <span data-ttu-id="c3e4f-219">**ação. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-219">**action.calloutKey**</span></span>                                             | <span data-ttu-id="c3e4f-220">**FWPM \_ texto explicativo \_ IPSec de \_ entrada \_ Iniciar \_ segurança \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-220">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V{4\|6}**</span></span>                                          |
    | <span data-ttu-id="c3e4f-221">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-221">**rawContext**</span></span>                                                    | [<span data-ttu-id="c3e4f-222">**\_conexão do conjunto de Ale de contexto FWPM \_ \_ \_ \_ requer \_ \_ criptografia IPSec**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-222">**FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_REQUIRE\_IPSEC\_ENCRYPTION**</span></span>](filter-context-identifiers.md) |

        

<span data-ttu-id="c3e4f-223">**No FWPM \_ Layer \_ Ale \_ auth \_ Connect \_ V {4 \| 6} configurar as regras de filtragem por conexão de saída**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-223">**At FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6} setup outbound per-connection filtering rules**</span></span>

-   <span data-ttu-id="c3e4f-224">Adicione um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-224">Add a filter with the following properties.</span></span> <span data-ttu-id="c3e4f-225">Esse filtro só permitirá conexões de saída da porta TCP 5555 se elas forem criptografadas.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-225">This filter will only permit outbound connections from TCP port 5555 if they are encrypted.</span></span>

    | <span data-ttu-id="c3e4f-226">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="c3e4f-226">Filter property</span></span>                                                   | <span data-ttu-id="c3e4f-227">Valor</span><span class="sxs-lookup"><span data-stu-id="c3e4f-227">Value</span></span>                                                                                                 |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="c3e4f-228">**FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-228">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="c3e4f-229">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="c3e4f-229">NlatUnicast</span></span>                                                                                           |
    | <span data-ttu-id="c3e4f-230">**FWPM \_ Condição de filtragem de \_ \_ protocolo IP de condição**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-230">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="c3e4f-231">**IPPROTO \_ TCP** essa constante é definida no Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="c3e4f-231">**IPPROTO\_TCP** This constant is defined in winsock2.h.</span></span><br/>                                    |
    | <span data-ttu-id="c3e4f-232">**FWPM \_ Condição de filtragem de \_ \_ \_ porta local de IP de condição**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-232">**FWPM\_CONDITION\_IP\_LOCAL\_PORT** filtering condition</span></span>          | <span data-ttu-id="c3e4f-233">5555</span><span class="sxs-lookup"><span data-stu-id="c3e4f-233">5555</span></span>                                                                                                  |
    | <span data-ttu-id="c3e4f-234">**ação. tipo**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-234">**action.type**</span></span>                                                   | <span data-ttu-id="c3e4f-235">**o \_ \_ texto explicativo de ação fwp \_ termina**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-235">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                                                                 |
    | <span data-ttu-id="c3e4f-236">**ação. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-236">**action.calloutKey**</span></span>                                             | <span data-ttu-id="c3e4f-237">**FWPM \_ texto explicativo \_ IPSec \_ Ale \_ Connect \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-237">**FWPM\_CALLOUT\_IPSEC\_ALE\_CONNECT\_V{4\|6}**</span></span>                                                       |
    | <span data-ttu-id="c3e4f-238">**rawContext**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-238">**rawContext**</span></span>                                                    | [<span data-ttu-id="c3e4f-239">**\_conexão do conjunto de Ale de contexto FWPM \_ \_ \_ \_ requer \_ \_ criptografia IPSec**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-239">**FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_REQUIRE\_IPSEC\_ENCRYPTION**</span></span>](filter-context-identifiers.md) |

      

  
</dl>

## <a name="related-topics"></a><span data-ttu-id="c3e4f-240">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c3e4f-240">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3e4f-241">Código de exemplo: usando o modo de transporte</span><span class="sxs-lookup"><span data-stu-id="c3e4f-241">Sample code: Using Transport Mode</span></span>](using-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="c3e4f-242">Camadas ALE</span><span class="sxs-lookup"><span data-stu-id="c3e4f-242">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="c3e4f-243">**Identificadores de texto explicativo internos**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-243">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> <dt>

[<span data-ttu-id="c3e4f-244">Condições de filtragem</span><span class="sxs-lookup"><span data-stu-id="c3e4f-244">Filtering Conditions</span></span>](filtering-conditions.md)
</dt> <dt>

[<span data-ttu-id="c3e4f-245">**Filtrando identificadores de camada**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-245">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="c3e4f-246">**FWPM \_ ACTION0**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-246">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[<span data-ttu-id="c3e4f-247">**\_tipo de \_ contexto do provedor FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="c3e4f-247">**FWPM\_PROVIDER\_CONTEXT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 


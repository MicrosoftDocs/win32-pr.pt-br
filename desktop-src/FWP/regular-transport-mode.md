---
title: Modo de transporte
description: O cenário de política IPsec do modo de transporte requer a proteção do modo de transporte IPsec para todo o tráfego correspondente.
ms.assetid: 303f7cdc-fb7a-4e5c-8291-cadcb45035cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfb927aff1b3f0e3c7fd13a192f0fcb18fc3ec45
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365926"
---
# <a name="transport-mode"></a><span data-ttu-id="3769d-103">Modo de transporte</span><span class="sxs-lookup"><span data-stu-id="3769d-103">Transport Mode</span></span>

<span data-ttu-id="3769d-104">O cenário de política IPsec do modo de transporte requer a proteção do modo de transporte IPsec para todo o tráfego correspondente.</span><span class="sxs-lookup"><span data-stu-id="3769d-104">The Transport Mode IPsec policy scenario requires IPsec transport mode protection for all matching traffic.</span></span> <span data-ttu-id="3769d-105">Qualquer tráfego de texto não criptografado correspondente é Descartado até que a negociação IKE ou AuthIP seja concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="3769d-105">Any matching clear text traffic is dropped until the IKE or AuthIP negotiation has completed successfully.</span></span> <span data-ttu-id="3769d-106">Se a negociação falhar, a conectividade com o endereço IP correspondente permanecerá quebrada.</span><span class="sxs-lookup"><span data-stu-id="3769d-106">If the negotiation fails, connectivity with the corresponding IP address will remain broken.</span></span>

<span data-ttu-id="3769d-107">Um exemplo de um possível cenário de modo de transporte é "proteger todo o tráfego de dados unicast, exceto ICMP, usando o modo de transporte IPsec".</span><span class="sxs-lookup"><span data-stu-id="3769d-107">An example of a possible Transport Mode scenario is "Secure all unicast data traffic, except ICMP, using IPsec transport mode."</span></span>

<span data-ttu-id="3769d-108">Para implementar este exemplo programaticamente, use a seguinte configuração de WFP.</span><span class="sxs-lookup"><span data-stu-id="3769d-108">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="3769d-109">**Na \_ camada FWPM \_ IKEEXT \_ V {4 \| 6} política de negociação de instalação mm**</span><span class="sxs-lookup"><span data-stu-id="3769d-109">**At FWPM\_LAYER\_IKEEXT\_V{4\|6} setup MM negotiation policy**</span></span>  

1.  <span data-ttu-id="3769d-110">Adicione um ou ambos os seguintes contextos do provedor de política MM.</span><span class="sxs-lookup"><span data-stu-id="3769d-110">Add one or both of the following MM policy provider contexts.</span></span>  
    -   <span data-ttu-id="3769d-111">Para IKE, um contexto de provedor de política do tipo **FWPM \_ IPSec \_ Ike \_ mm \_ Context**.</span><span class="sxs-lookup"><span data-stu-id="3769d-111">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_MM\_CONTEXT**.</span></span>
    -   <span data-ttu-id="3769d-112">Para AuthIP, um contexto de provedor de política do tipo **FWPM \_ IPSec \_ AuthIP \_ mm \_ Context**.</span><span class="sxs-lookup"><span data-stu-id="3769d-112">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT**.</span></span>

    > [!Note]  
    > <span data-ttu-id="3769d-113">Um módulo de chave comum será negociado e a política MM correspondente será aplicada.</span><span class="sxs-lookup"><span data-stu-id="3769d-113">A common keying module will be negotiated and the corresponding MM policy will be applied.</span></span> <span data-ttu-id="3769d-114">AuthIP é o módulo de chaveamento preferencial se o IKE e o AuthIP tiverem suporte.</span><span class="sxs-lookup"><span data-stu-id="3769d-114">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="3769d-115">Para cada um dos contextos adicionados na etapa 1, adicione um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="3769d-115">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 
    | <span data-ttu-id="3769d-116">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="3769d-116">Filter property</span></span>        | <span data-ttu-id="3769d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="3769d-117">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="3769d-118">Condições de filtragem</span><span class="sxs-lookup"><span data-stu-id="3769d-118">Filtering conditions</span></span>   | <span data-ttu-id="3769d-119">Vazio.</span><span class="sxs-lookup"><span data-stu-id="3769d-119">Empty.</span></span> <span data-ttu-id="3769d-120">Todo o tráfego corresponderá ao filtro.</span><span class="sxs-lookup"><span data-stu-id="3769d-120">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="3769d-121">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="3769d-121">**providerContextKey**</span></span> | <span data-ttu-id="3769d-122">GUID do contexto do provedor MM adicionado na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="3769d-122">GUID of the MM provider context added in step 1.</span></span> |

        

<span data-ttu-id="3769d-123">**Na \_ camada FWPM \_ IPSec \_ V {4 \| 6} configurar política de negociação QM e em**</span><span class="sxs-lookup"><span data-stu-id="3769d-123">**At FWPM\_LAYER\_IPSEC\_V{4\|6} setup QM and EM negotiation policy**</span></span>  

1.  <span data-ttu-id="3769d-124">Adicione um ou ambos os seguintes contextos de provedor de política de modo de transporte QM.</span><span class="sxs-lookup"><span data-stu-id="3769d-124">Add one or both of the following QM transport mode policy provider contexts.</span></span>  
    -   <span data-ttu-id="3769d-125">Para IKE, um contexto de provedor de política do tipo **FWPM \_ IPSec de transporte de IP \_ \_ qm \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="3769d-125">For IKE, a policy provider context of type **FWPM\_IPSEC\_IKE\_QM\_TRANSPORT\_CONTEXT**.</span></span>
    -   <span data-ttu-id="3769d-126">Para AuthIP, um contexto de provedor de política do tipo **\_ \_ \_ \_ \_ contexto de transporte QM IPSec AuthIP de FWPM**.</span><span class="sxs-lookup"><span data-stu-id="3769d-126">For AuthIP, a policy provider context of type **FWPM\_IPSEC\_AUTHIP\_QM\_TRANSPORT\_CONTEXT**.</span></span> <span data-ttu-id="3769d-127">Esse contexto pode, opcionalmente, conter a política de negociação de modo estendido AuthIP (em).</span><span class="sxs-lookup"><span data-stu-id="3769d-127">This context can optionally contain the AuthIP Extended Mode (EM) negotiation policy.</span></span>

    > [!Note]  
    > <span data-ttu-id="3769d-128">Um módulo de chave comum será negociado e a política QM correspondente será aplicada.</span><span class="sxs-lookup"><span data-stu-id="3769d-128">A common keying module will be negotiated and the corresponding QM policy will be applied.</span></span> <span data-ttu-id="3769d-129">AuthIP é o módulo de chaveamento preferencial se o IKE e o AuthIP tiverem suporte.</span><span class="sxs-lookup"><span data-stu-id="3769d-129">AuthIP is the preferred keying module if both IKE and AuthIP are supported.</span></span>

     

2.  <span data-ttu-id="3769d-130">Para cada um dos contextos adicionados na etapa 1, adicione um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="3769d-130">For each of the contexts added in step 1, add a filter with the following properties.</span></span> 
    | <span data-ttu-id="3769d-131">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="3769d-131">Filter property</span></span>        | <span data-ttu-id="3769d-132">Valor</span><span class="sxs-lookup"><span data-stu-id="3769d-132">Value</span></span>                                            |
    |------------------------|--------------------------------------------------|
    | <span data-ttu-id="3769d-133">Condições de filtragem</span><span class="sxs-lookup"><span data-stu-id="3769d-133">Filtering conditions</span></span>   | <span data-ttu-id="3769d-134">Vazio.</span><span class="sxs-lookup"><span data-stu-id="3769d-134">Empty.</span></span> <span data-ttu-id="3769d-135">Todo o tráfego corresponderá ao filtro.</span><span class="sxs-lookup"><span data-stu-id="3769d-135">All traffic will match the filter.</span></span>        |
    | <span data-ttu-id="3769d-136">**providerContextKey**</span><span class="sxs-lookup"><span data-stu-id="3769d-136">**providerContextKey**</span></span> | <span data-ttu-id="3769d-137">GUID do contexto de provedor QM adicionado na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="3769d-137">GUID of the QM provider context added in step 1.</span></span> |

        

<span data-ttu-id="3769d-138">**Na \_ camada FWPM \_ transporte de \_ entrada \_ V {4 \| 6} configurar regras de filtragem de entrada por pacote**</span><span class="sxs-lookup"><span data-stu-id="3769d-138">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} setup inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="3769d-139">Adicione um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="3769d-139">Add a filter with the following properties.</span></span> 
    | <span data-ttu-id="3769d-140">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="3769d-140">Filter property</span></span>                                                   | <span data-ttu-id="3769d-141">Valor</span><span class="sxs-lookup"><span data-stu-id="3769d-141">Value</span></span>                                                         |
    |-------------------------------------------------------------------|---------------------------------------------------------------|
    | <span data-ttu-id="3769d-142">**FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição**</span><span class="sxs-lookup"><span data-stu-id="3769d-142">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | [<span data-ttu-id="3769d-143">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="3769d-143">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type) |
    | <span data-ttu-id="3769d-144">**ação. tipo**</span><span class="sxs-lookup"><span data-stu-id="3769d-144">**action.type**</span></span>                                                   | <span data-ttu-id="3769d-145">o \_ \_ texto explicativo de ação fwp \_ termina</span><span class="sxs-lookup"><span data-stu-id="3769d-145">FWP\_ACTION\_CALLOUT\_TERMINATING</span></span>                             |
    | <span data-ttu-id="3769d-146">**ação. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="3769d-146">**action.calloutKey**</span></span>                                             | <span data-ttu-id="3769d-147">FWPM \_ texto explicativo \_ IPSec de \_ transporte de entrada \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="3769d-147">FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}</span></span>             |

        
2.  <span data-ttu-id="3769d-148">Isentar o tráfego ICMP do IPsec adicionando um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="3769d-148">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>
    | <span data-ttu-id="3769d-149">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="3769d-149">Filter property</span></span>                                                  | <span data-ttu-id="3769d-150">Valor</span><span class="sxs-lookup"><span data-stu-id="3769d-150">Value</span></span>                                                                     |
    |------------------------------------------------------------------|---------------------------------------------------------------------------|
    | <span data-ttu-id="3769d-151">**FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição**</span><span class="sxs-lookup"><span data-stu-id="3769d-151">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="3769d-152">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="3769d-152">NlatUnicast</span></span>                                                               |
    | <span data-ttu-id="3769d-153">**FWPM \_ Condição de filtragem de \_ \_ protocolo IP de condição**</span><span class="sxs-lookup"><span data-stu-id="3769d-153">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>            | <span data-ttu-id="3769d-154">IPPROTO \_ ICMP {V6} essas constantes são definidas no Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="3769d-154">IPPROTO\_ICMP{V6}These constants are defined in winsock2.h.</span></span><br/>    |
    | <span data-ttu-id="3769d-155">**ação. tipo**</span><span class="sxs-lookup"><span data-stu-id="3769d-155">**action.type**</span></span>                                                  | <span data-ttu-id="3769d-156">\_permissão de ação fwp \_</span><span class="sxs-lookup"><span data-stu-id="3769d-156">FWP\_ACTION\_PERMIT</span></span>                                                       |
    | <span data-ttu-id="3769d-157">**weight**</span><span class="sxs-lookup"><span data-stu-id="3769d-157">**weight**</span></span>                                                       | [<span data-ttu-id="3769d-158">**\_ \_ isenções Ike de intervalo de peso FWPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3769d-158">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md) |

        

<span data-ttu-id="3769d-159">**Em FWPM \_ camada de \_ saída do \_ transporte \_ V {4 \| 6} configurar regras de filtragem por pacote de saída**</span><span class="sxs-lookup"><span data-stu-id="3769d-159">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} setup outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="3769d-160">Adicione um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="3769d-160">Add a filter with the following properties.</span></span>
    | <span data-ttu-id="3769d-161">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="3769d-161">Filter property</span></span>                                                   | <span data-ttu-id="3769d-162">Valor</span><span class="sxs-lookup"><span data-stu-id="3769d-162">Value</span></span>                                              |
    |-------------------------------------------------------------------|----------------------------------------------------|
    | <span data-ttu-id="3769d-163">**FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição**</span><span class="sxs-lookup"><span data-stu-id="3769d-163">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="3769d-164">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="3769d-164">NlatUnicast</span></span>                                        |
    | <span data-ttu-id="3769d-165">**ação. tipo**</span><span class="sxs-lookup"><span data-stu-id="3769d-165">**action.type**</span></span>                                                   | <span data-ttu-id="3769d-166">**o \_ \_ texto explicativo de ação fwp \_ termina**</span><span class="sxs-lookup"><span data-stu-id="3769d-166">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>              |
    | <span data-ttu-id="3769d-167">**ação. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="3769d-167">**action.calloutKey**</span></span>                                             | <span data-ttu-id="3769d-168">FWPM do \_ balão de \_ \_ saída IPSec \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="3769d-168">FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}</span></span> |

        
2.  <span data-ttu-id="3769d-169">Isentar o tráfego ICMP do IPsec adicionando um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="3769d-169">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span>
    | <span data-ttu-id="3769d-170">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="3769d-170">Filter property</span></span>                                                   | <span data-ttu-id="3769d-171">Valor</span><span class="sxs-lookup"><span data-stu-id="3769d-171">Value</span></span>                                                                  |
    |-------------------------------------------------------------------|------------------------------------------------------------------------|
    | <span data-ttu-id="3769d-172">**FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição**</span><span class="sxs-lookup"><span data-stu-id="3769d-172">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="3769d-173">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="3769d-173">NlatUnicast</span></span>                                                            |
    | <span data-ttu-id="3769d-174">**FWPM \_ Condição de filtragem de \_ \_ protocolo IP de condição**</span><span class="sxs-lookup"><span data-stu-id="3769d-174">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="3769d-175">IPPROTO \_ ICMP {V6} essas constantes são definidas no Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="3769d-175">IPPROTO\_ICMP{V6}These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="3769d-176">**ação. tipo**</span><span class="sxs-lookup"><span data-stu-id="3769d-176">**action.type**</span></span>                                                   | <span data-ttu-id="3769d-177">\_permissão de ação fwp \_</span><span class="sxs-lookup"><span data-stu-id="3769d-177">FWP\_ACTION\_PERMIT</span></span>                                                    |
    | <span data-ttu-id="3769d-178">**weight**</span><span class="sxs-lookup"><span data-stu-id="3769d-178">**weight**</span></span>                                                        | <span data-ttu-id="3769d-179">\_ \_ isenções Ike de intervalo de peso FWPM \_ \_</span><span class="sxs-lookup"><span data-stu-id="3769d-179">FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS</span></span>                                   |

        

</dl>

## <a name="related-topics"></a><span data-ttu-id="3769d-180">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3769d-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3769d-181">Código de exemplo: usando o modo de transporte</span><span class="sxs-lookup"><span data-stu-id="3769d-181">Sample code: Using Transport Mode</span></span>](using-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="3769d-182">**Filtrando identificadores de camada**</span><span class="sxs-lookup"><span data-stu-id="3769d-182">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="3769d-183">**Tipos de contexto do provedor**</span><span class="sxs-lookup"><span data-stu-id="3769d-183">**Provider Context Types**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> <dt>

[<span data-ttu-id="3769d-184">Condições de filtragem</span><span class="sxs-lookup"><span data-stu-id="3769d-184">Filtering Conditions</span></span>](filtering-conditions.md)
</dt> <dt>

[<span data-ttu-id="3769d-185">**FWPM \_ ACTION0**</span><span class="sxs-lookup"><span data-stu-id="3769d-185">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[<span data-ttu-id="3769d-186">**Identificadores de texto explicativo internos**</span><span class="sxs-lookup"><span data-stu-id="3769d-186">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> </dl>

 


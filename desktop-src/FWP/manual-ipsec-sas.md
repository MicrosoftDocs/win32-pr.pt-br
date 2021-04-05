---
title: SA manual
description: O cenário de diretiva IPsec SA (Associação de segurança manual) permite que os chamadores ignorem os módulos de criação de chaves IPsec (IKE e AuthIP), especificando diretamente as SAs IPsec para proteger qualquer tráfego de rede.
ms.assetid: 2bcc0b40-ca43-43c6-b1e4-b64426ef7ff4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7161447ff5cfd98878ab4ee0f4b18cbcc3a53643
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917208"
---
# <a name="manual-sa"></a><span data-ttu-id="5a27c-103">SA manual</span><span class="sxs-lookup"><span data-stu-id="5a27c-103">Manual SA</span></span>

<span data-ttu-id="5a27c-104">O cenário de diretiva IPsec SA (Associação de segurança manual) permite que os chamadores ignorem os módulos de criação de chaves IPsec (IKE e AuthIP), especificando diretamente as SAs IPsec para proteger qualquer tráfego de rede.</span><span class="sxs-lookup"><span data-stu-id="5a27c-104">The Manual Security Association (SA) IPsec policy scenario allows callers to bypass the built-in IPsec keying modules (IKE and AuthIP) by directly specifying IPsec SAs to secure any network traffic.</span></span>

<span data-ttu-id="5a27c-105">Um exemplo de cenário SA manual possível é "adicionar um par de SA IPsec para proteger todo o tráfego de dados unicast entre os endereços IP 1.1.1.1 & 2.2.2.2, exceto ICMP, usando o modo de transporte IPsec".</span><span class="sxs-lookup"><span data-stu-id="5a27c-105">An example of a possible Manual SA scenario is "Add an IPsec SA pair to secure all unicast data traffic between IP addresses 1.1.1.1 & 2.2.2.2, except ICMP, using IPsec transport mode."</span></span>

> [!Note]  
> <span data-ttu-id="5a27c-106">As etapas a seguir devem ser executadas em ambos os computadores com os endereços IP definidos adequadamente.</span><span class="sxs-lookup"><span data-stu-id="5a27c-106">The following steps must be executed on both machines with IP addresses appropriately set.</span></span>

 

<span data-ttu-id="5a27c-107">Para implementar este exemplo programaticamente, use a seguinte configuração de WFP.</span><span class="sxs-lookup"><span data-stu-id="5a27c-107">To implement this example programmatically, use the following WFP configuration.</span></span>

<dl>

<span data-ttu-id="5a27c-108">**Na \_ camada FWPM \_ transporte de \_ entrada \_ V {4 \| 6} configurar regras de filtragem de entrada por pacote**</span><span class="sxs-lookup"><span data-stu-id="5a27c-108">**At FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} setup inbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="5a27c-109">Adicione um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="5a27c-109">Add a filter with the following properties.</span></span> 
    | <span data-ttu-id="5a27c-110">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="5a27c-110">Filter property</span></span>                                                   | <span data-ttu-id="5a27c-111">Valor</span><span class="sxs-lookup"><span data-stu-id="5a27c-111">Value</span></span>                                                         |
    |-------------------------------------------------------------------|---------------------------------------------------------------|
    | <span data-ttu-id="5a27c-112">**FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição**</span><span class="sxs-lookup"><span data-stu-id="5a27c-112">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | [<span data-ttu-id="5a27c-113">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="5a27c-113">NlatUnicast</span></span>](/windows/win32/api/nldef/ne-nldef-nl_address_type) |
    | <span data-ttu-id="5a27c-114">**\_ \_ endereço local do IP da condição FWPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5a27c-114">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS**</span></span>                           | <span data-ttu-id="5a27c-115">O endereço local apropriado (1.1.1.1 ou 2.2.2.2).</span><span class="sxs-lookup"><span data-stu-id="5a27c-115">The appropriate local address (1.1.1.1 or 2.2.2.2).</span></span>           |
    | <span data-ttu-id="5a27c-116">**\_ \_ \_ endereço IP remoto \_ da condição FWPM**</span><span class="sxs-lookup"><span data-stu-id="5a27c-116">**FWPM\_CONDITION\_IP\_REMOTE\_ADDRESS**</span></span>                          | <span data-ttu-id="5a27c-117">O endereço remoto apropriado (1.1.1.1 ou 2.2.2.2).</span><span class="sxs-lookup"><span data-stu-id="5a27c-117">The appropriate remote address (1.1.1.1 or 2.2.2.2).</span></span>          |
    | <span data-ttu-id="5a27c-118">**ação. tipo**</span><span class="sxs-lookup"><span data-stu-id="5a27c-118">**action.type**</span></span>                                                   | <span data-ttu-id="5a27c-119">**o \_ \_ texto explicativo de ação fwp \_ termina**</span><span class="sxs-lookup"><span data-stu-id="5a27c-119">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                         |
    | <span data-ttu-id="5a27c-120">**ação. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="5a27c-120">**action.calloutKey**</span></span>                                             | <span data-ttu-id="5a27c-121">**FWPM \_ texto explicativo \_ IPSec de \_ transporte de entrada \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="5a27c-121">**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V{4\|6}**</span></span>         |

        
2.  <span data-ttu-id="5a27c-122">Isentar o tráfego ICMP do IPsec adicionando um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="5a27c-122">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 
    | <span data-ttu-id="5a27c-123">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="5a27c-123">Filter property</span></span>                                                   | <span data-ttu-id="5a27c-124">Valor</span><span class="sxs-lookup"><span data-stu-id="5a27c-124">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="5a27c-125">**FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição**</span><span class="sxs-lookup"><span data-stu-id="5a27c-125">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="5a27c-126">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="5a27c-126">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="5a27c-127">**FWPM \_ Condição de filtragem de \_ \_ protocolo IP de condição**</span><span class="sxs-lookup"><span data-stu-id="5a27c-127">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="5a27c-128">**IPPROTO \_ ICMP {V6}** essas constantes são definidas no Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="5a27c-128">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="5a27c-129">**ação. tipo**</span><span class="sxs-lookup"><span data-stu-id="5a27c-129">**action.type**</span></span>                                                   | <span data-ttu-id="5a27c-130">**\_permissão de ação fwp \_**</span><span class="sxs-lookup"><span data-stu-id="5a27c-130">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="5a27c-131">**weight**</span><span class="sxs-lookup"><span data-stu-id="5a27c-131">**weight**</span></span>                                                        | [<span data-ttu-id="5a27c-132">**\_ \_ isenções Ike de intervalo de peso FWPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5a27c-132">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>](filter-weight-identifiers.md)  |

        

<span data-ttu-id="5a27c-133">**Em FWPM \_ camada de \_ saída do \_ transporte \_ V {4 \| 6} configurar regras de filtragem por pacote de saída**</span><span class="sxs-lookup"><span data-stu-id="5a27c-133">**At FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} setup outbound per-packet filtering rules**</span></span>  

1.  <span data-ttu-id="5a27c-134">Adicione um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="5a27c-134">Add a filter with the following properties.</span></span> 
    | <span data-ttu-id="5a27c-135">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="5a27c-135">Filter property</span></span>                                                   | <span data-ttu-id="5a27c-136">Valor</span><span class="sxs-lookup"><span data-stu-id="5a27c-136">Value</span></span>                                                  |
    |-------------------------------------------------------------------|--------------------------------------------------------|
    | <span data-ttu-id="5a27c-137">**FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição**</span><span class="sxs-lookup"><span data-stu-id="5a27c-137">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="5a27c-138">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="5a27c-138">NlatUnicast</span></span>                                            |
    | <span data-ttu-id="5a27c-139">**FWPM \_ Condição de filtragem de \_ \_ \_ endereço IP local da condição**</span><span class="sxs-lookup"><span data-stu-id="5a27c-139">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS** filtering condition</span></span>       | <span data-ttu-id="5a27c-140">O endereço local apropriado (1.1.1.1 ou 2.2.2.2).</span><span class="sxs-lookup"><span data-stu-id="5a27c-140">The appropriate local address (1.1.1.1 or 2.2.2.2).</span></span>    |
    | <span data-ttu-id="5a27c-141">**FWPM \_ Condição de filtragem de \_ \_ \_ endereço IP remoto da condição**</span><span class="sxs-lookup"><span data-stu-id="5a27c-141">**FWPM\_CONDITION\_IP\_REMOTE\_ADDRESS** filtering condition</span></span>      | <span data-ttu-id="5a27c-142">O endereço remoto apropriado (1.1.1.1 ou 2.2.2.2).</span><span class="sxs-lookup"><span data-stu-id="5a27c-142">The appropriate remote address (1.1.1.1 or 2.2.2.2).</span></span>   |
    | <span data-ttu-id="5a27c-143">**ação. tipo**</span><span class="sxs-lookup"><span data-stu-id="5a27c-143">**action.type**</span></span>                                                   | <span data-ttu-id="5a27c-144">**o \_ \_ texto explicativo de ação fwp \_ termina**</span><span class="sxs-lookup"><span data-stu-id="5a27c-144">**FWP\_ACTION\_CALLOUT\_TERMINATING**</span></span>                  |
    | <span data-ttu-id="5a27c-145">**ação. calloutKey**</span><span class="sxs-lookup"><span data-stu-id="5a27c-145">**action.calloutKey**</span></span>                                             | <span data-ttu-id="5a27c-146">**FWPM do \_ balão de \_ \_ saída IPSec \_ \_ V {4 \| 6}**</span><span class="sxs-lookup"><span data-stu-id="5a27c-146">**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V{4\|6}**</span></span> |

        
2.  <span data-ttu-id="5a27c-147">Isentar o tráfego ICMP do IPsec adicionando um filtro com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="5a27c-147">Exempt ICMP traffic from IPsec by adding a filter with the following properties.</span></span> 
    | <span data-ttu-id="5a27c-148">Propriedade de filtro</span><span class="sxs-lookup"><span data-stu-id="5a27c-148">Filter property</span></span>                                                   | <span data-ttu-id="5a27c-149">Valor</span><span class="sxs-lookup"><span data-stu-id="5a27c-149">Value</span></span>                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="5a27c-150">**FWPM \_ Condição de filtragem de \_ \_ tipo de \_ endereço \_ IP local de condição**</span><span class="sxs-lookup"><span data-stu-id="5a27c-150">**FWPM\_CONDITION\_IP\_LOCAL\_ADDRESS\_TYPE** filtering condition</span></span> | <span data-ttu-id="5a27c-151">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="5a27c-151">NlatUnicast</span></span>                                                                |
    | <span data-ttu-id="5a27c-152">**FWPM \_ Condição de filtragem de \_ \_ protocolo IP de condição**</span><span class="sxs-lookup"><span data-stu-id="5a27c-152">**FWPM\_CONDITION\_IP\_PROTOCOL** filtering condition</span></span>             | <span data-ttu-id="5a27c-153">**IPPROTO \_ ICMP {V6}** essas constantes são definidas no Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="5a27c-153">**IPPROTO\_ICMP{V6}** These constants are defined in winsock2.h.</span></span><br/> |
    | <span data-ttu-id="5a27c-154">**ação. tipo**</span><span class="sxs-lookup"><span data-stu-id="5a27c-154">**action.type**</span></span>                                                   | <span data-ttu-id="5a27c-155">**\_permissão de ação fwp \_**</span><span class="sxs-lookup"><span data-stu-id="5a27c-155">**FWP\_ACTION\_PERMIT**</span></span>                                                    |
    | <span data-ttu-id="5a27c-156">**weight**</span><span class="sxs-lookup"><span data-stu-id="5a27c-156">**weight**</span></span>                                                        | <span data-ttu-id="5a27c-157">**\_ \_ isenções Ike de intervalo de peso FWPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5a27c-157">**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>                                   |

        

<span data-ttu-id="5a27c-158">**Configurar associações de segurança de entrada e saída**</span><span class="sxs-lookup"><span data-stu-id="5a27c-158">**Setup inbound and outbound security associations**</span></span>

1.  <span data-ttu-id="5a27c-159">Chame [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), com o parâmetro *outboundTraffic* que contém os endereços IP como 1.1.1.1 & 2.2.2.2 e **ipsecFilterId** como o LUID do filtro de texto explicativo IPSec da camada de transporte de saída adicionado acima.</span><span class="sxs-lookup"><span data-stu-id="5a27c-159">Call [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), with the *outboundTraffic* parameter containing the IP addresses as 1.1.1.1 & 2.2.2.2, and **ipsecFilterId** as the LUID of the outbound transport layer IPsec callout filter added above.</span></span>
2.  <span data-ttu-id="5a27c-160">Chame [**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0), com o parâmetro *ID* que contém a ID de contexto retornada de [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), e o parâmetro *getSpi* que contém os endereços IP como 1.1.1.1 & 2.2.2.2 e **ipsecFilterId** como o LUID do filtro de texto explicativo IPSec da camada de transporte de entrada adicionado acima.</span><span class="sxs-lookup"><span data-stu-id="5a27c-160">Call [**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0), with the *id* parameter containing the context ID returned from [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), and the *getSpi* parameter containing the IP addresses as 1.1.1.1 & 2.2.2.2, and **ipsecFilterId** as the LUID of the inbound transport layer IPsec callout filter added above.</span></span> <span data-ttu-id="5a27c-161">O valor SPI retornado deve ser usado como o SPI SA de entrada pelo computador local e como o SPI SA de saída pelo computador remoto correspondente.</span><span class="sxs-lookup"><span data-stu-id="5a27c-161">The returned SPI value is meant to be used as the inbound SA SPI by the local machine and as the outbound SA SPI by the corresponding remote machine.</span></span> <span data-ttu-id="5a27c-162">Ambos os computadores devem usar alguns meios fora de banda para trocar os valores SPI.</span><span class="sxs-lookup"><span data-stu-id="5a27c-162">Both machines must use some out-of-band means to exchange the SPI values.</span></span>
3.  <span data-ttu-id="5a27c-163">Chame [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0), com o parâmetro *ID* que contém a ID de contexto retornada de [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)e o parâmetro *INBOUNDBUNDLE* que descreve as propriedades do grupo SA de entrada (como o SPI de entrada SA, tipo de transformação, tipos de algoritmo, chaves, etc.).</span><span class="sxs-lookup"><span data-stu-id="5a27c-163">Call [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0), with the *id* parameter containing the context ID returned from [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), and the *inboundBundle* parameter describing the properties of the inbound SA bundle (such as the inbound SA SPI, transform type, algorithm types, keys, etc).</span></span>
4.  <span data-ttu-id="5a27c-164">Chame [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0), com o parâmetro *ID* que contém a ID de contexto retornada de [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)e o parâmetro *OUTBOUNDBUNDLE* que descreve as propriedades do pacote SA de saída (como o SPI de saída SA, tipo de transformação, tipos de algoritmo, chaves, etc.).</span><span class="sxs-lookup"><span data-stu-id="5a27c-164">Call [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0), with the *id* parameter containing the context ID returned from [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), and the *outboundBundle* parameter describing the properties of the outbound SA bundle (such as the outbound SA SPI, transform type, algorithm types, keys, etc).</span></span>

  
</dl>

## <a name="related-topics"></a><span data-ttu-id="5a27c-165">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5a27c-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a27c-166">Código de exemplo: chave SA manual</span><span class="sxs-lookup"><span data-stu-id="5a27c-166">Sample code: Manual SA Keying</span></span>](manual-sa-keying.md)
</dt> <dt>

[<span data-ttu-id="5a27c-167">**Identificadores de texto explicativo internos**</span><span class="sxs-lookup"><span data-stu-id="5a27c-167">**Built-in Callout Identifiers**</span></span>](built-in-callout-identifiers.md)
</dt> <dt>

[<span data-ttu-id="5a27c-168">**Filtrando identificadores de camada**</span><span class="sxs-lookup"><span data-stu-id="5a27c-168">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="5a27c-169">**FWPM \_ ACTION0**</span><span class="sxs-lookup"><span data-stu-id="5a27c-169">**FWPM\_ACTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> </dl>

 


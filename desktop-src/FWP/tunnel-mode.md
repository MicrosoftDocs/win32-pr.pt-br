---
title: Modo de túnel
description: O cenário da política IPsec do modo de túnel é usado para aplicar a proteção do modo de encapsulamento IPsec para todo o tráfego correspondente entre dois pontos de extremidade de túnel.
ms.assetid: 170046c5-28ec-4341-89e2-93494bf9c6b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75fdecb7f959a2f95aae2649a6e3f8f94def9b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292515"
---
# <a name="tunnel-mode"></a><span data-ttu-id="8f9cb-103">Modo de túnel</span><span class="sxs-lookup"><span data-stu-id="8f9cb-103">Tunnel Mode</span></span>

<span data-ttu-id="8f9cb-104">O cenário da política IPsec do modo de túnel é usado para aplicar a proteção do modo de encapsulamento IPsec para todo o tráfego correspondente entre dois pontos de extremidade de túnel.</span><span class="sxs-lookup"><span data-stu-id="8f9cb-104">The Tunnel Mode IPsec policy scenario is used to apply IPsec tunnel mode protection for all matching traffic between two tunnel endpoints.</span></span>

<span data-ttu-id="8f9cb-105">Esse cenário de política normalmente é usado para proteger o tráfego entre várias sub-redes de filial, quando ele é encaminhado entre os gateways correspondentes na Internet.</span><span class="sxs-lookup"><span data-stu-id="8f9cb-105">This policy scenario is typically used to protect traffic between multiple branch-office subnets, when it gets forwarded between the corresponding gateways on the Internet.</span></span> <span data-ttu-id="8f9cb-106">Ele também pode ser usado para proteger a comunicação de ponta a ponta entre dois computadores host, também chamados de túneis ponto a ponto.</span><span class="sxs-lookup"><span data-stu-id="8f9cb-106">It can also be used to secure end-to-end communication between two host machines, also referred to as point-to-point tunnels.</span></span>

<span data-ttu-id="8f9cb-107">Para implementar a política de modo de túnel usando a WFP (Windows Filtering Platform), chame a função [**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) que instancia os filtros de modo de túnel apropriados nas camadas apropriadas em nome do chamador.</span><span class="sxs-lookup"><span data-stu-id="8f9cb-107">To implement Tunnel Mode policy using the Windows Filtering Platform (WFP), call the [**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) function that instantiates the appropriate tunnel mode filters at the appropriate layers on behalf of the caller.</span></span> <span data-ttu-id="8f9cb-108">O chamador precisa especificar o modo principal, os contextos do provedor de modo rápido e as condições de filtro que descrevem o tráfego que deve ser protegido dentro do túnel.</span><span class="sxs-lookup"><span data-stu-id="8f9cb-108">The caller needs to specify the Main Mode, Quick Mode provider contexts, and the filter conditions describing the traffic that should be secured inside the tunnel.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f9cb-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8f9cb-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f9cb-110">Código de exemplo: usando o modo de túnel</span><span class="sxs-lookup"><span data-stu-id="8f9cb-110">Sample code: Using Tunnel Mode</span></span>](using-tunnel-mode.md)
</dt> <dt>

[<span data-ttu-id="8f9cb-111">**Filtrando identificadores de camada**</span><span class="sxs-lookup"><span data-stu-id="8f9cb-111">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 





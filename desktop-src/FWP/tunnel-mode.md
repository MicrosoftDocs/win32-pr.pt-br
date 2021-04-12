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
# <a name="tunnel-mode"></a>Modo de túnel

O cenário da política IPsec do modo de túnel é usado para aplicar a proteção do modo de encapsulamento IPsec para todo o tráfego correspondente entre dois pontos de extremidade de túnel.

Esse cenário de política normalmente é usado para proteger o tráfego entre várias sub-redes de filial, quando ele é encaminhado entre os gateways correspondentes na Internet. Ele também pode ser usado para proteger a comunicação de ponta a ponta entre dois computadores host, também chamados de túneis ponto a ponto.

Para implementar a política de modo de túnel usando a WFP (Windows Filtering Platform), chame a função [**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) que instancia os filtros de modo de túnel apropriados nas camadas apropriadas em nome do chamador. O chamador precisa especificar o modo principal, os contextos do provedor de modo rápido e as condições de filtro que descrevem o tráfego que deve ser protegido dentro do túnel.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Código de exemplo: usando o modo de túnel](using-tunnel-mode.md)
</dt> <dt>

[**Filtrando identificadores de camada**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 





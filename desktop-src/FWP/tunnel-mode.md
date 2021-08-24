---
title: Tunnel Modo
description: O cenário Tunnel de política IPsec do modo Tunnel é usado para aplicar a proteção de modo de túnel IPsec para todo o tráfego correspondente entre dois pontos de extremidade de túnel.
ms.assetid: 170046c5-28ec-4341-89e2-93494bf9c6b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbac16de0dc01bc37e0e4f4b997d00d19339de021ffce66a0d3cf6957addbe90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639066"
---
# <a name="tunnel-mode"></a>Tunnel Modo

O cenário Tunnel de política IPsec do modo Tunnel é usado para aplicar a proteção de modo de túnel IPsec para todo o tráfego correspondente entre dois pontos de extremidade de túnel.

Esse cenário de política normalmente é usado para proteger o tráfego entre várias sub-redes de filial, quando ele é encaminhado entre os gateways correspondentes na Internet. Ele também pode ser usado para proteger a comunicação de ponta a ponta entre dois máquinas host, também conhecidas como túneis ponto a ponto.

Para implementar a política de modo Tunnel usando a WFP (plataforma de filtragem de Windows), chame a [**função FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) que instania os filtros de modo de túnel apropriados nas camadas apropriadas em nome do chamador. O chamador precisa especificar os contextos do provedor modo principal, modo rápido e as condições de filtro que descrevem o tráfego que deve ser protegido dentro do túnel.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Código de exemplo: usando o modo Tunnel aplicativo](using-tunnel-mode.md)
</dt> <dt>

[**Filtrando identificadores de camada**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 





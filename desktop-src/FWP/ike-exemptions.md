---
title: Isenções de IKE/AuthIP
description: A IKE (Internet Key Exchange) e protocolo Authenticated IP (AuthIP), para funcionar, precisam isentar o tráfego de rede da filtragem de IPsec.
ms.assetid: 365bfebc-250a-440f-8056-ff9601daa030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2963c804c6bd63f191563566bcc99dcf9f0f4a74bb2c844a402adc856dbad3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069056"
---
# <a name="ikeauthip-exemptions"></a>Isenções de IKE/AuthIP

Os módulos de chave de protocolo IPsec, IKE (Internet Key Exchange) e protocolo Authenticated IP (AuthIP), para funcionarem, precisam isentar o tráfego de rede da filtragem IPsec.

Na plataforma de filtragem do Windows (WFP), o BFE (Mecanismo de Filtragem Base) adiciona automaticamente filtros de isenção de IKE e AuthIP quando o primeiro filtro de política do mm (modo principal) IKE ou AuthIP é adicionado e os exclui quando o último filtro de política IKE ou AuthIP MM é excluído. Dessa forma, os provedores de política não têm que gerenciar isenções de filtragem de IKE e AuthIP individualmente.

Um filtro de política mm IKE é um filtro na camada de mecanismo [**FWPM \_ LAYER \_ IKEEXT \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) que faz referência a um contexto de provedor do tipo [**FWPM \_ IPSEC \_ IKE \_ MM \_ CONTEXT**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).

Um filtro de política mm do AuthIP é um filtro na camada de mecanismo [**FWPM \_ LAYER \_ IKEEXT \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) que faz referência a um contexto de provedor do tipo [**FWPM \_ IPSEC \_ AUTHIP \_ MM \_ CONTEXT**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).

Um filtro de isenção de IKE ou AuthIP é um filtro na camada do mecanismo [**FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) ou **FWPM \_ LAYER \_ OUTBOUND TRANSPORT \_ \_ V{4 \| 6}** ponderado automaticamente no intervalo de peso ISENÇÕES de [**\_ \_ \_ IKE \_**](filter-weight-identifiers.md) DO INTERVALO DE PESO do FWPM.

As isenções de IKE e AuthIP implementadas pelo BFE são as a seguir.

| Versão IP      | Porta                        | Isenção                                                                                                                                                                                                                             |
|-----------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IPv4<br/> | UDP:500 UDP:4500<br/> | Permita o tráfego IKE e AuthIP na camada de transporte de entrada e na camada de transporte de saída. <br/> Permita o tráfego IKE e AuthIP nas camadas de recebimento/aceitação e conexão do ALE, mas restrinja-o ao sistema local.<br/> |
| IPv6<br/> | UDP:500<br/>          | Permita o tráfego IKE e AuthIP na camada de transporte de entrada e na camada de transporte de saída. <br/> Permita o tráfego IKE e AuthIP nas camadas de recebimento/aceitação e conexão do ALE, mas restrinja-o ao sistema local.<br/> |



 

Os filtros de isenção de IKE e AuthIP estão abertos para todos os endereços. Para implementar um firewall com controle mais granular, os provedores de política devem adicionar filtros em um intervalo de peso maior que ISENÇÕES de [**\_ \_ \_ IKE \_**](filter-weight-identifiers.md)de INTERVALO DE PESO do FWPM.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configuração do IPsec](ipsec-configuration.md)
</dt> <dt>

[Atribuição de peso de filtro](filter-weight-assignment.md)
</dt> </dl>

 

 






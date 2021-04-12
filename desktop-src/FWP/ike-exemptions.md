---
title: Isenções de IKE/AuthIP
description: Protocolo IKE (IKE) e protocolo Authenticated IP (AuthIP), a fim de funcionar, precisam isentar o tráfego de rede da filtragem IPsec.
ms.assetid: 365bfebc-250a-440f-8056-ff9601daa030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d58a6d00ddd337d56c3c00a34b6949213be6ee26
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104365625"
---
# <a name="ikeauthip-exemptions"></a>Isenções de IKE/AuthIP

Os módulos de criação de chaves IPsec (Internet Protocol Security), protocolo IKE (IKE) e protocolo Authenticated IP (AuthIP), para funcionar, precisam isentar seu tráfego de rede da filtragem IPsec.

Na WFP (plataforma de filtragem do Windows), o BFE (mecanismo de filtragem básica) adiciona automaticamente filtros de isenção IKE e AuthIP quando o primeiro filtro de política de Ike ou AuthIP MM é adicionado e os exclui quando o último filtro de política IKE ou AuthIP cm é excluído. Dessa forma, os provedores de política não precisam gerenciar as isenções de filtragem IKE e AuthIP individualmente.

Um filtro de política de IKE MM é um filtro na camada de FWPM da camada do mecanismo [**\_ \_ IKEEXT \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) que faz referência a um contexto de provedor do tipo [**FWPM \_ IPSec \_ Ike \_ mm \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).

Um filtro de política AuthIP MM é um filtro na camada de FWPM da camada do mecanismo [**\_ \_ IKEEXT \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) que faz referência a um contexto de provedor do tipo de [**\_ \_ \_ \_ contexto IPSec AuthIP mm de FWPM**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).

Um filtro de isenção de IKE ou AuthIP é um filtro na camada de mecanismo [**FWPM transporte de entrada de camada \_ \_ \_ \_ v {4 \| 6}**](management-filtering-layer-identifiers-.md) ou **transporte de saída de \_ camada FWPM \_ \_ \_ v {4 \| 6}** automaticamente ponderado no intervalo de peso FWPM intervalo de pesos de [**\_ \_ \_ \_ isenções Ike**](filter-weight-identifiers.md) .

As isenções IKE e AuthIP implementadas pelo BFE são as seguintes.

| Versão IP      | Porta                        | Isenção                                                                                                                                                                                                                             |
|-----------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IPv4<br/> | UDP: 500 UDP: 4500<br/> | Permitir tráfego IKE e AuthIP na camada de transporte de entrada e na camada de transporte de saída. <br/> Permitir o tráfego IKE e AuthIP na recepção/aceitação da ALE e conectar camadas, mas restringi-la ao sistema local.<br/> |
| IPv6<br/> | UDP: 500<br/>          | Permitir tráfego IKE e AuthIP na camada de transporte de entrada e na camada de transporte de saída. <br/> Permitir o tráfego IKE e AuthIP na recepção/aceitação da ALE e conectar camadas, mas restringi-la ao sistema local.<br/> |



 

Os filtros de isenção IKE e AuthIP estão abertos a todos os endereços. Para implementar um firewall com controle mais granular, os provedores de política devem adicionar filtros em um intervalo de peso maior que as [**\_ \_ \_ \_ isenções Ike de intervalo de peso FWPM**](filter-weight-identifiers.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configuração de IPsec](ipsec-configuration.md)
</dt> <dt>

[Atribuição de peso de filtro](filter-weight-assignment.md)
</dt> </dl>

 

 






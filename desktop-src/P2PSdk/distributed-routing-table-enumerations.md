---
description: As seguintes enumerações dão suporte à API de DRT (tabela de roteamento distribuído).
ms.assetid: 38ce95a0-1603-42c2-8a5e-4370f52c8fc9
title: Enumerações de tabela de roteamento distribuído
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c432b156a9299a9f70026a394a6fd97f06528a25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754517"
---
# <a name="distributed-routing-table-enumerations"></a>Enumerações de tabela de roteamento distribuído

As seguintes enumerações dão suporte à API de DRT (tabela de roteamento distribuído).



| Enumeração                                                            | Descrição                                                                                                                                                           |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**escopo de DRT \_**](/windows/desktop/api/drt/ne-drt-drt_scope)                                        | Define o conjunto de escopos IPv6 no qual a DRT operará ao usar o transporte UDP IPv6 criado pelo [**DrtCreateIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport). |
| [**\_sinalizadores de endereço DRT \_**](/windows/desktop/api/drt/ne-drt-drt_address_flags)                       | Define o conjunto de respostas que podem ser retornadas por um nó intermediário ao executar uma pesquisa de uma chave.                                                         |
| [**STATUS de DRT \_**](/windows/desktop/api/drt/ne-drt-drt_status)                                      | Define a possível conectividade e os Estados de erro de um nó local.                                                                                                   |
| [**\_tipo de correspondência DRT \_**](/windows/desktop/api/drt/ne-drt-drt_match_type)                             | Define a exata dos resultados retornados quando uma pesquisa é executada.                                                                                                 |
| [**\_tipo de alteração de chave de folha de \_ \_ \_ tipos DRT**](/windows/desktop/api/drt/ne-drt-drt_leafset_key_change_type) | Define o conjunto de tipos de alteração que podem ser executados em um nó de conjunto de folha local no cache DRT local.                                                                |
| [**\_tipo de evento DRT \_**](/windows/desktop/api/drt/ne-drt-drt_event_type)                             | Define o conjunto de eventos que podem ser gerados pelo DRT.                                                                                                              |
| [**\_modo de segurança DRT \_**](/windows/desktop/api/drt/ne-drt-drt_security_mode)                       | Define os possíveis modos de segurança do DRT. Essa enumeração é um campo da estrutura [**de \_ configurações de DRT**](/windows/desktop/api/drt/ns-drt-drt_settings) .                                   |
| [**\_estado de registro DRT \_**](/windows/desktop/api/drt/ne-drt-drt_registration_state)             | Define o estado de uma chave registrada.                                                                                                                                |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Estruturas de tabela de roteamento distribuído](distributed-routing-table-structures.md)
</dt> <dt>

[Funções de tabela de roteamento distribuído](distributed-routing-table-functions.md)
</dt> <dt>

[Referência de API de Tabela de roteamento distribuído](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 




---
description: As estruturas a seguir dão suporte às funções de API de DRT (tabela de roteamento distribuído).
ms.assetid: 3ff85b24-5ec0-4b26-b30e-1bf8030a575d
title: Estruturas de tabela de roteamento distribuído
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d454d2c28008422da897dc91ca9a3dc29db374b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764635"
---
# <a name="distributed-routing-table-structures"></a>Estruturas de tabela de roteamento distribuído

As estruturas a seguir dão suporte às funções de API de DRT (tabela de roteamento distribuído).



| Estrutura                                                  | Descrição                                                                                                                                                                              |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**dados de DRT \_**](/windows/desktop/api/drt/ns-drt-drt_data)                              | Contém um blob de dados. Essa estrutura é usada por várias funções DRT.                                                                                                                   |
| [**registro de DRT \_**](/windows/desktop/api/drt/ns-drt-drt_registration)              | Contém o registro de chave. Esse é um membro da estrutura [**de \_ \_ resultados da pesquisa DRT**](/windows/desktop/api/drt/ns-drt-drt_search_result) e é um argumento passado para [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey). |
| [**\_endereço DRT**](/windows/desktop/api/drt/ns-drt-drt_address)                        | Contém informações de ponto de extremidade sobre um nó DRT que participou de uma pesquisa. Essas informações se destinam ao uso na depuração de problemas de conectividade.                                   |
| [**\_lista de endereços DRT \_**](/windows/desktop/api/drt/ns-drt-drt_address_list)             | Contém um conjunto de estruturas de [**\_ endereço DRT**](/windows/desktop/api/drt/ns-drt-drt_address) que representa os nós contatados durante uma pesquisa de uma chave.                                                             |
| [**\_provedor de segurança DRT \_**](/windows/desktop/api/Drt/ns-drt-drt_security_provider)   | Define a interface que deve ser implementada por um provedor de segurança.                                                                                                                   |
| [**\_provedor de inicialização DRT \_**](/windows/desktop/api/drt/ns-drt-drt_bootstrap_provider) | Define a interface que deve ser implementada por um provedor de inicialização.                                                                                                                  |
| [**configurações de DRT \_**](/windows/desktop/api/drt/ns-drt-drt_settings)                      | Define as configurações de DRT na inicialização. Essa estrutura é passada como um argumento para [**DrtOpen**](/windows/desktop/api/drt/nf-drt-drtopen).                                                                           |
| [**\_informações de pesquisa DRT \_**](/windows/desktop/api/drt/ns-drt-drt_search_info)               | Define uma consulta de pesquisa. Essa estrutura é passada como um argumento para [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch).                                                                             |
| [**\_resultado da pesquisa DRT \_**](/windows/desktop/api/drt/ns-drt-drt_search_result)           | Contém um resultado de pesquisa. Essa estrutura é retornada por [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult).                                                                                |
| [**\_dados de evento DRT \_**](/windows/desktop/api/drt/ns-drt-drt_event_data)                 | Contém os dados de evento retornados chamando [**DrtGetEventData**](/windows/desktop/api/drt/nf-drt-drtgeteventdata) depois que um aplicativo recebe um sinal de evento.                                                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Enumerações de tabela de roteamento distribuído](distributed-routing-table-enumerations.md)
</dt> <dt>

[Funções de tabela de roteamento distribuído](distributed-routing-table-functions.md)
</dt> <dt>

[Referência de API de Tabela de roteamento distribuído](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 




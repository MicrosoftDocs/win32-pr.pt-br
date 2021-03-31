---
title: Gerenciador de tabela de roteamento versão 2 tipos de dados simples
description: A API RTMv2 define vários tipos de dados simples. A tabela a seguir lista esses tipos de dados.
ms.assetid: e935518e-b8d8-47fb-b2b2-c9750c2b540e
keywords:
- Serviço de roteamento e acesso remoto RRAS, Gerenciador de tabela de roteamento versão 2, tipos de dados simples
- Gerenciador de tabela de roteamento versão 2 RRAS, tipos de dados simples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6dbd7530799c1c7e1702e0384d51b37a77dda0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636431"
---
# <a name="routing-table-manager-version-2-simple-data-types"></a>Gerenciador de tabela de roteamento versão 2 tipos de dados simples

A API RTMv2 define vários tipos de dados simples. A tabela a seguir lista esses tipos de dados.



| Tipo de dados                                                                                                                                                                                                                                                                                                                   | Descrição                                                                                                                                      | Typedef              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| \_ID da exibição RTM \_ , ID da \* \_ exibição PRTM \_                                                                                                                                                                                                                                                                                             | Identifica uma determinada exibição.                                                                                                                    | INT                  |
| \_ \_ conjunto de exibição DWORD RTM \* , \_ conjunto de exibição PRTM \_                                                                                                                                                                                                                                                                                     | Identifica um conjunto de modos de exibição; expresso como uma máscara.                                                                                                  | DWORD                |
| \_ \_ identificador de entidade RTM, identificador de \* \_ entidade PRTM \_ , \_ identificador de dest da RTM \_ , \* \_ \_ identificador de dest PRTM, identificador de rota RTM, identificador de \_ rota PRTM, identificador de nexthop \_ \* \_ \_ \_ de RTM, identificador \_ \* de salto de PRTM, identificador de \_ \_ Enumeração RTM, identificador de \_ \_ \* \_ Enumeração PRTM, identificador \_ \_ de lista de rotas RTM, identificador de \_ \_ \* \_ lista de rotas de PRTM, identificador de notificação RTM, identificador \_ \_ \_ \_ de \* \_ notificação PRTM \_ | Identificadores que apontam para dados RTMv2.                                                                                                                  | PROCESSAMENTO               |
| \_ \_ \_ tipo de método de entidade RTM, \* tipo de \_ método de entidade PRTM \_ \_                                                                                                                                                                                                                                                                     | Identifica os métodos exportados por um cliente registrado.                                                                                              | DWORD                |
| \_ \_ método de exportação de entidade RTM \_ , \* método de exportação de \_ entidade PRTM \_ \_                                                                                                                                                                                                                                                                 | Especifica o protótipo comum para métodos de cliente.                                                                                               | \_método de entidade \_     |
| \_ \_ \_ sinalizadores de alteração de rota RTM, \* sinalizadores de \_ alteração de rota PRTM \_ \_                                                                                                                                                                                                                                                                     | Sinalizadores de entrada e saída usados para especificar o estado quando uma rota é adicionada ou atualizada.                                                               | DWORD                |
| \_ \_ \_ sinalizadores de alteração de nexthop de RTM, \* sinalizadores de alteração de \_ nexthop PRTM \_ \_                                                                                                                                                                                                                                                                 | Sinalizadores de saída usados para especificar o estado quando um próximo salto é adicionado.                                                                                 | DWORD                |
| \_ \_ sinalizadores de correspondência de RTM, \* sinalizadores de correspondência de PRTM \_ \_                                                                                                                                                                                                                                                                                     | Sinalizadores de entrada usados para especificar critérios ao correspondência de rotas na tabela de roteamento.                                                                  | DWORD                |
| \_ \_ sinalizadores de enumeração de RTM, \* \_ sinalizadores de enumeração PRTM \_                                                                                                                                                                                                                                                                                       | Identifica enumerações.                                                                                                                         | DWORD                |
| \_ \_ sinalizadores de notificação de RTM, \* \_ sinalizadores de notificação PRTM \_                                                                                                                                                                                                                                                                                   | Sinalizadores de saída usados para especificar qual tipo de notificação está sendo emitido; composto da seguinte maneira: (alterar tipos \| de dests) um cliente está interessado. | DWORD                |
| \_ \_ retorno de chamada de evento RTM, \* retorno de chamada de \_ evento PRTM \_ ;                                                                                                                                                                                                                                                                              | Identifica o retorno de chamada usado para notificar os clientes de que uma alteração ocorreu no estado de rota ou nos clientes registrados.                                  | retorno de chamada do \_ evento RTM \_ |



 

 

 





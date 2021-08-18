---
title: Acessando o armazenamento de reserva
description: A API do servidor HTTP mantém a lista de reserva de namespace para todos os usuários no computador.
ms.assetid: 4b1291fc-cc62-4d4f-9150-18cbb1f6e5c0
keywords:
- Acessando o armazenamento de reserva HTTP
- Armazenamento de reserva HTTP, acessando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14f9244fd4513517793bf85d205308fc49ac2d8ca0a246c17a68c730d1c76168
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015014"
---
# <a name="accessing-the-reservation-store"></a>Acessando o armazenamento de reserva

A API do servidor HTTP mantém a lista de reserva de namespace para todos os usuários no computador. Uma entrada de reserva consiste em um [URLPrefix](urlprefix-strings.md) e uma ACL correspondente. Cada UrlPrefix no repositório tem uma ACL que lista todos os usuários que têm permissão para se registrar para receber solicitações para o namespace. Os usuários com privilégios de delegação podem delegar subárvores do namespace que eles possuem a outros usuários ou excluir reservas existentes usando as APIs de configuração.

Para adicionar uma reserva ao repositório de reserva persistente, o aplicativo chama a função [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) com o parâmetro de ID de configuração definido como o valor **HttpServiceConfigUrlAclInfo** . A API do servidor HTTP verifica a propriedade do namespace e a ID do usuário antes de adicionar uma reserva à loja.

A API do servidor HTTP também fornece funções para consultar e excluir as configurações de serviço para namespaces de URL. A função [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration) chamada com o parâmetro de ID de configuração definido como as consultas de valor de **HttpServiceConfigUrlAclInfo** e a função [**HttpDeleteServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) exclui no repositório de namespace de URL.

 

 





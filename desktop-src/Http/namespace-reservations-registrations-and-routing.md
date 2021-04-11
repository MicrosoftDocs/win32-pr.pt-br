---
title: Reservas de namespace, registros e roteamento
description: Reserva e registro são as operações pelas quais a API do servidor HTTP dá acesso ao namespace da URL em um computador.
ms.assetid: dc66960b-36cd-4c09-be0a-3aec9a8a25d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a00801629b5b778bb6c87a0bff615cb9d5618f57
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292710"
---
# <a name="namespace-reservations-registrations-and-routing"></a>Reservas de namespace, registros e roteamento

Reserva e registro são as operações pelas quais a API do servidor HTTP dá acesso ao namespace da URL em um computador. Os aplicativos podem se registrar para uma parte do namespace da URL a fim de atender a solicitações de clientes HTTP. O aplicativo registra um namespace com a API do servidor HTTP usando a função [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) . A API do servidor HTTP adiciona as URLs à fila de solicitações para o aplicativo e roteia as solicitações para os aplicativos, dependendo das URLs em suas filas. Antes que o aplicativo possa se registrar para receber solicitações para um namespace de URL, no entanto, o administrador do sistema deve fazer uma reserva para essa URL em nome do usuário que está executando o aplicativo. Por padrão, o namespace é fechado, ou seja, somente o administrador pode registrar UrlPrefixes até que o administrador insira uma reserva.

Uma reserva aloca de forma persistente uma parte do namespace da URL para usuários individuais, permitindo que eles reservem ou "próprios" a parte do namespace. As reservas dão ao usuário o direito de se registrar em solicitações de serviço para o namespace. A API do servidor HTTP garante que os usuários não registrem URLs de partes do namespace que não são de sua propriedade. Para garantir a segurança do namespace, as ACLs (lista de controle de acesso) são aplicadas à parte do namespace reservado para cada usuário.

Os namespaces reservados são identificados por cadeias de caracteres de prefixo de URL, formatados da mesma maneira que os prefixos de URL usados para os registros. Isso significa que todas as várias categorias de especificador de host também estão disponíveis para reservas.

As reservas de namespace são mantidas entre reinicializações e as alterações entram em vigor dinamicamente, portanto, não é necessário parar e reiniciar o computador.

Os conceitos a seguir são esclarecidos ainda mais, pois se aplicam ao processo de registro e reserva de namespaces.

-   Falta. O registro é a operação pela qual um aplicativo indica interesse no recebimento de solicitações para um UrlPrefix especificado. A API para o registro de URL é [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl). Normalmente, o registro ocorre durante a inicialização do aplicativo e deve ser executado cada vez que o aplicativo é iniciado.
-   Zona. O roteamento é executado pela API do servidor HTTP para determinar o aplicativo para o qual enviar a solicitação, com base na melhor correspondência [URLPrefix](urlprefix-strings.md) registrada e/ou reservada. A operação de roteamento usa informações de registro e reserva.
-   Contra. A reserva aloca uma parte do namespace da URL para um ou mais usuários. Esta operação fornece aos usuários o direito de se registrar para o namespace especificado. Um usuário para o qual um namespace é reservado é dito como "proprietário" dessa parte do namespace da URL. As reservas de namespace normalmente são executadas durante a instalação do aplicativo e são uma operação infrequente. As reservas persistem entre reinicializações do computador e exigem privilégios de administrador no computador ou na propriedade com privilégios de delegação para criar ou excluir.
-   Delegação. Privilégios de delegação permitem que um usuário que possui um namespace entregue a propriedade de uma subárvore a outro usuário por uma reserva subsequente. Os privilégios de delegação são concedidos a um usuário pelo administrador do sistema quando a reserva é feita. Um ou mais de um usuário pode receber privilégios de delegação para um namespace.

 

 





---
title: Lista de escuta de IP
description: As APIs do servidor HTTP não se associam a nenhum endereço IP e a pares de portas TCP até que um usuário registre um UrlPrefix.
ms.assetid: f2f51e6c-9114-4ba9-a37c-1d1d1f0b444f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba085112c800d7845c76467c4dd2fdc3f5f0b00a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916596"
---
# <a name="ip-listen-list"></a>Lista de escuta de IP

As APIs do servidor HTTP não se associam a nenhum endereço IP e a pares de portas TCP até que um usuário registre um UrlPrefix. Por padrão, depois que um registro é inserido na fila de solicitações, a API do servidor HTTP é vinculada à porta especificada no UrlPrefix (por exemplo, a porta 80) para todos os endereços IP (inaddr \_ any ou INADDR6 \_ any) disponíveis no computador. Os problemas surgem quando os aplicativos de terceiros (não usando as APIs do servidor HTTP) são vinculados ao endereço IP e aos pares da porta 80 no computador. A API do servidor HTTP fornece uma maneira de configurar a lista de endereços IP que ele associa e resolve esse problema de coexistência. O administrador do sistema chama a função [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) com o parâmetro *configid* definido como o valor HttpServiceConfigIPListenList para especificar a lista de escuta de IP. Os endereços IPv4 e IPv6 podem ser adicionados à lista. Os endereços IP inseridos se aplicam a todos os aplicativos no computador usando a API do servidor HTTP e persistem entre reinicializações do computador. No entanto, quaisquer alterações na configuração da lista de escuta de IP não ocorrem dinamicamente; na maioria dos casos, uma reinicialização do sistema pode ser necessária.

 

 





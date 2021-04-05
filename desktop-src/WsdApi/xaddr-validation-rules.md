---
description: Os endereços de transporte (XAddrs) incluídos nas mensagens ProbeMatches e ResolveMatches estão sujeitos à validação básica antes de o WSDAPI enviar uma mensagem HTTP, como uma solicitação de metadados.
ms.assetid: 6b5139b5-aa31-42bc-a281-8784006edfbe
title: Regras de validação do XAddr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc91ce8a0e1bba267ea92fa79a6680b481297f24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165180"
---
# <a name="xaddr-validation-rules"></a>Regras de validação do XAddr

Os endereços de transporte (XAddrs) incluídos nas mensagens [ProbeMatches](probematches-message.md) e [ResolveMatches](resolvematches-message.md) estão sujeitos à validação básica antes de o WSDAPI enviar uma mensagem http, como uma solicitação de metadados.

Isso é para garantir que os XAddrs estejam na mesma sub-rede que o cliente.

O XML a seguir mostra um exemplo de elemento XAddrs. O prefixo WSD refere-se ao namespace `https://schemas.xmlsoap.org/ws/2005/04/discovery` .

``` syntax
<wsd:XAddrs>
    https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsd:XAddrs>
```

Todas as condições a seguir devem ser atendidas antes que a mensagem HTTP seja transmitida pela conexão.

-   XAddrs devem ser endereços HTTP ou HTTPS. XAddrs de outros esquemas são ignorados.
-   Se qualquer XAddrs HTTPS estiver presente, todos os XAddrs deverão ser HTTPS. As seções XAddr que incluem endereços HTTP e HTTPS são completamente ignoradas. Além disso, o endereço do ponto de extremidade do dispositivo deve corresponder exatamente ao XAddrs HTTPS.
-   XAddrs devem ser endereços IP ou nomes de host que poderão ser resolvidos por meio do DNS. Normalmente, os endereços IP são usados.
-   Pelo menos um endereço IP incluído no XAddrs (ou o endereço IP resolvido de um nome de host incluído no XAddrs) deve estar na mesma sub-rede que o adaptador no qual a mensagem [ProbeMatches](probematches-message.md) ou [ResolveMatches](resolvematches-message.md) foi recebida.
-   O endereço e a porta especificados no primeiro XAddr devem estar acessíveis. O WSDAPI tenta se conectar a esse endereço ao estabelecer uma conexão HTTP.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[ProbeMatches](probematches-message.md)
</dt> <dt>

[ResolveMatches](resolvematches-message.md)
</dt> <dt>

[Padrões de mensagem de troca de metadados e descoberta](discovery-and-metadata-exchange-message-patterns.md)
</dt> </dl>

 

 




---
description: Os endereços de transporte (XAddrs) incluídos nas mensagens ProbeMatches e ResolveMatches estão sujeitos à validação básica antes que o WSDAPI envie uma mensagem HTTP, como uma solicitação de metadados.
ms.assetid: 6b5139b5-aa31-42bc-a281-8784006edfbe
title: Regras de validação XAddr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e3b167101b6012bcf20779381993cfff4ea7ea22d35eef5397ac1349baa2cdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049504"
---
# <a name="xaddr-validation-rules"></a>Regras de validação XAddr

Os endereços de transporte (XAddrs) incluídos nas mensagens [ProbeMatches](probematches-message.md) e [ResolveMatches](resolvematches-message.md) estão sujeitos à validação básica antes que o WSDAPI envie uma mensagem HTTP, como uma solicitação de metadados.

Isso é para garantir que os XAddrs estão na mesma sub-rede que o cliente.

O XML a seguir mostra um elemento XAddrs de exemplo. O prefixo wsd refere-se ao namespace `https://schemas.xmlsoap.org/ws/2005/04/discovery` .

``` syntax
<wsd:XAddrs>
    https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsd:XAddrs>
```

Todas as condições a seguir devem ser atendidas antes que a mensagem HTTP saia pela transmissão.

-   XAddrs devem ser endereços HTTP ou HTTPS. XAddrs de outros esquemas são ignorados.
-   Se algum XAddrs HTTPS estiver presente, todos os XAddrs deverão ser HTTPS. As seções XAddr que incluem endereços HTTP e HTTPS são completamente ignoradas. Além disso, o endereço do ponto de extremidade do dispositivo deve corresponder exatamente aos XAddrs HTTPS.
-   Os XAddrs devem ser endereços IP ou nomes de host que podem ser resolvidos por meio do DNS. Normalmente, os endereços IP são usados.
-   Pelo menos um endereço IP incluído nos XAddrs (ou endereço IP resolvido de um nome de host incluído nos XAddrs) deve estar na mesma sub-rede que o adaptador pelo qual a mensagem [ProbeMatches](probematches-message.md) ou [ResolveMatches](resolvematches-message.md) foi recebida.
-   O endereço e a porta especificados no primeiro XAddr devem estar acessíveis. O WSDAPI tenta se conectar a esse endereço ao estabelecer uma conexão HTTP.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Probematches](probematches-message.md)
</dt> <dt>

[ResolveMatches](resolvematches-message.md)
</dt> <dt>

[Padrões de mensagem de descoberta e Exchange metadados](discovery-and-metadata-exchange-message-patterns.md)
</dt> </dl>

 

 




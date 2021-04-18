---
description: Especifica um prefixo que está no link para a interface \# 4.
ms.assetid: cc3aa99d-cf45-460c-bdc1-3e9a19806fe4
title: Prefixos de site IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bed8a21c59f9b6727c98ccb7fdacf4e9ec6ea5cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807937"
---
# <a name="ipv6-site-prefixes"></a>Prefixos de site IPv6

O comando IPv6 RTU permite que os prefixos em link publicados sejam configurados com um comprimento de prefixo de site. Se especificado, o comprimento do prefixo do site é colocado em uma opção de informações de prefixo em anúncios de roteador. Por exemplo:

``` syntax
ipv6 rtu 2002:836b:9820:2::/64 4 pub life 1800 spl 48
```

Especifica um prefixo que está no link para a interface \# 4. O prefixo é publicado, o que significa que ele será incluído em anúncios de roteador se \# a interface 4 for uma interface de anúncio. O tempo de vida na opção de informações de prefixo é de 1800 segundos (30 minutos). O comprimento do prefixo do site na opção de informações de prefixo é 48.

O recebimento de uma opção de informações de prefixo que especifica um prefixo de site faz com que uma entrada seja criada na tabela de prefixo do site, que pode ser exibida usando o comando SPT do IPv6. A tabela de prefixo do site é usada para remover endereços locais inadequados de site daqueles retornados pelo [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) e pelas funções relacionadas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Link IPv6-local e endereços locais do site](link-local-and-site-local-addresses-2.md)
</dt> <dt>

[Netsh.exe](netsh-exe.md)
</dt> </dl>

 

 




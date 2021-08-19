---
description: especifica um prefixo que está no link para a interface \# 4.
ms.assetid: cc3aa99d-cf45-460c-bdc1-3e9a19806fe4
title: Prefixos de site IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dd37370aa14bd6883f83e93d661f10b96d804dc3b85cf47173da4b1f0ee0f90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118111290"
---
# <a name="ipv6-site-prefixes"></a>Prefixos de site IPv6

O comando ipv6 rtu permite que prefixos publicados no link sejam configurados com um comprimento de prefixo de site. Se especificado, o comprimento do prefixo do site será colocado em uma opção de informações de prefixo em anúncios de roteador. Por exemplo:

``` syntax
ipv6 rtu 2002:836b:9820:2::/64 4 pub life 1800 spl 48
```

especifica um prefixo que está no link para a interface \# 4. O prefixo é publicado, o que significa que ele será incluído em anúncios de roteador se a interface \# 4 for uma interface publicitária. O tempo de vida na opção de informações de prefixo é de 1800 segundos (30 minutos). O comprimento do prefixo do site na opção de informações de prefixo é 48.

O recebimento de uma opção de informações de prefixo que especifica um prefixo do site faz com que uma entrada seja criada na tabela de prefixo do site, que pode ser exibida usando o comando ipv6 spt. A tabela de prefixo do site é usada para remover endereços locais de site inadequados daqueles retornados pelo [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) e funções relacionadas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Endereços locais e locais do link IPv6](link-local-and-site-local-addresses-2.md)
</dt> <dt>

[Netsh.exe](netsh-exe.md)
</dt> </dl>

 

 




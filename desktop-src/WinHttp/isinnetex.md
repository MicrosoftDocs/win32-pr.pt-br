---
description: Determina se um endereço IP está em uma sub-rede específica.
ms.assetid: 2fbfad9c-86b1-44c3-860b-a5c98ac6c2e9
title: Função isInNetEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- isInNetEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3a91555370bada5c4bb9257918d0920ac71ac5475c08201f30bf1fbbb4b95c1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114459"
---
# <a name="isinnetex-function"></a>Função isInNetEx

Determina se um endereço IP está em uma sub-rede específica.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Ipaddress* 
</dt> <dd>

Uma cadeia de caracteres que contém endereços IPv6/IPv4.

</dd> <dt>

*IPprefix* 
</dt> <dd>

Uma cadeia de caracteres que contém o prefixo IP delimitado por dois-pontos com os n bits principais especificados no campo de bits (ou seja, 3ffe:8311:ffff::/48 ou 123.112.0.0/16).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

TRUE se o host estiver na mesma sub-rede; caso contrário, FALSE.

Também retornará FALSE se o prefixo não estiver no formato correto ou se endereços e prefixos de diferentes tipos são usados na comparação (ou seja, prefixo IPv4 e um endereço IPv6).

## <a name="examples"></a>Exemplos

``` syntax
isInNetEx(host, "198.95.249.79/32");
    true if the IP address of host matches exactly 198.95.249.79
```

``` syntax
isInNetEx(host, "198.95.0.0/16");
    true if the IP address of the host matches 198.95.*.*
```

``` syntax
isInNetEx(host, "3ffe:8311:ffff::/48");
    true if the IP address of the host matches 3ffe:8311:fff:*:*:*:*:*
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Definições de API do Auxiliar de Proxy com IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[Extensões IPv6 para o formato de arquivo de configuração automática do navegador](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 




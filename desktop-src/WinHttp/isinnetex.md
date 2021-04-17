---
description: Determina se um endereço IP está em uma sub-rede específica.
ms.assetid: 2fbfad9c-86b1-44c3-860b-a5c98ac6c2e9
title: função isInNetEx
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
ms.openlocfilehash: d738fbf5788fbe56d8c801b6c5256e96e8d4a6f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782490"
---
# <a name="isinnetex-function"></a>função isInNetEx

Determina se um endereço IP está em uma sub-rede específica.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*IP* 
</dt> <dd>

Uma cadeia de caracteres que contém endereços IPv6/IPv4.

</dd> <dt>

*IPprefix* 
</dt> <dd>

Uma cadeia de caracteres que contém o prefixo de IP delimitado por dois bits com os n principais bit especificados no campo de bits (ou seja, 3FFE: 8311: ffff::/48 ou 123.112.0.0/16).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

TRUE se o host estiver na mesma sub-rede; caso contrário, FALSE.

Também retornará FALSE se o prefixo não estiver no formato correto ou se os endereços e prefixos de tipos diferentes forem usados na comparação (ou seja, o prefixo IPv4 e um endereço IPv6).

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

[Definições da API auxiliar de proxy com reconhecimento de IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[Formato de arquivo de configuração automática de extensões IPv6 para navegador](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 




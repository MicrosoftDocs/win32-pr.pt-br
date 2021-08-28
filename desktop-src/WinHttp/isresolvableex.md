---
description: Determina se uma determinada cadeia de caracteres de host pode ser resolvida para um endereço IP.
ms.assetid: 83e52ca7-2ea0-419d-b09d-9301c1982b98
title: Função isResolvableEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- isResolvableEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: 580f5400b59a1142de90843e2be26790aef25a9311f7aa6f732aebeef606c701
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899166"
---
# <a name="isresolvableex-function"></a>Função isResolvableEx

Determina se uma determinada cadeia de caracteres de host pode ser resolvida para um endereço IP.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*host* 
</dt> <dd>

Uma cadeia de caracteres que contém o host HTTP fornecido para FindProxyForUrl.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

TRUE se o host for resolvível para um endereço IPv4 ou IPv6; caso contrário, FALSE.

## <a name="examples"></a>Exemplos

``` syntax
isResolvableEx(host);
    true if the hostname can be resolved to and IP address 
```

``` syntax
isResolvableEx(host); 
    false if the hostname cannot be resolved to an IP address 
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Definições de API do Auxiliar de Proxy com IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[Extensões IPv6 para o formato de arquivo de configuração automática do navegador](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 




---
description: Determina se uma determinada cadeia de caracteres de host pode ser resolvida para um endereço IP.
ms.assetid: 83e52ca7-2ea0-419d-b09d-9301c1982b98
title: função isResolvableEx
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
ms.openlocfilehash: 1172aaed93a9fc6cede5ae5393c5dd430613a466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811550"
---
# <a name="isresolvableex-function"></a>função isResolvableEx

Determina se uma determinada cadeia de caracteres de host pode ser resolvida para um endereço IP.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hospedeira* 
</dt> <dd>

Uma cadeia de caracteres que contém o host HTTP que é fornecido para FindProxyForUrl.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

TRUE se o host puder ser resolvido para um endereço IPv4 ou IPv6; caso contrário, FALSE.

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

[Definições da API auxiliar de proxy com reconhecimento de IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[Formato de arquivo de configuração automática de extensões IPv6 para navegador](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 




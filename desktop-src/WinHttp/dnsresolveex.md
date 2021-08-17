---
description: Resolver uma cadeia de caracteres de host para seu endereço IP
ms.assetid: 32d70f10-803b-484d-a9e0-d4c61a8d897f
title: função dnsResolveEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- dnsResolveEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: f0f0100367d4fad6d6e0b013e5d552f733086e6ddd5bc720779ef1fb5b65cdce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133219"
---
# <a name="dnsresolveex-function"></a>função dnsResolveEx

Resolver uma cadeia de caracteres de host para seu endereço IP

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*host* 
</dt> <dd>

Uma cadeia de caracteres que contém o host HTTP que é fornecido para FindProxyForUrl.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Uma cadeia de caracteres delimitada por ponto e vírgula contendo endereços IPv6 e IPv4 ou uma cadeia de caracteres vazia se o host não puder ser resolvido.

## <a name="remarks"></a>Comentários

Os implementadores de FindProxyforURLEx devem adicionar um código que interrompa a cadeia de caracteres de endereços IP delimitados por ponto e vírgula em endereços separados.

## <a name="examples"></a>Exemplos

``` syntax
dnsResolveEx("testmachine1");
    returns the string "fe80::380c:2e71:f5b9:a3b5%15;fe80::982d:a3b3:97ad:7dd0%9;2001:4898:28:7:982d:a3b3:97ad:7dd0;2001:4898:28:7:adfe:a643:8130:2fdc;fe80::5efe:10.70.92.74%13;3ffe:8311:ffff:f70f:0:5efe:10.70.92.74;10.70.92.74;3ffe:831f:4136:e37e:380c:2e71
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Definições da API auxiliar de proxy com reconhecimento de IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[Formato de arquivo de configuração automática de extensões IPv6 para navegador](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 




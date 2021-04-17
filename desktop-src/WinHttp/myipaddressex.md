---
description: Localiza todos os endereços IP para localhost.
ms.assetid: 47f7d03e-c1a1-4395-9889-01891208fe0f
title: função myIPAddressEx
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
ms.openlocfilehash: 88c205dbd5ce071a809cf87f4f97bb6d42120dcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762371"
---
# <a name="myipaddressex-function"></a>função myIPAddressEx

Localiza todos os endereços IP para localhost.

## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Uma cadeia de caracteres delimitada por ponto e vírgula contendo todos os endereços IP para localhost (IPv6 e/ou IPv4) ou uma cadeia de caracteres vazia se não for possível resolver o localhost para um endereço IP.

## <a name="remarks"></a>Comentários

Os implementadores de FindProxyforURLEx devem adicionar um código que interrompa a cadeia de caracteres de endereços IP delimitados por ponto e vírgula em endereços separados.

## <a name="examples"></a>Exemplos

``` syntax
myIpAddressEx();
    would return the string "fe80::380c:2e71:f5b9:a3b5%15;fe80::982d:a3b3:97ad:7dd0%9;2001:4898:28:7:982d:a3b3:97ad:7dd0;2001:4898:28:7:adfe:a643:8130:2fdc;fe80::5efe:10.70.92.74%13;3ffe:8311:ffff:f70f:0:5efe:10.70.92.74;10.70.92.74;3ffe:831f:4136:e37e:380c:2e71:f5b9:a3b5" 
    if you were running on that host.
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Definições da API auxiliar de proxy com reconhecimento de IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[Formato de arquivo de configuração automática de extensões IPv6 para navegador](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 




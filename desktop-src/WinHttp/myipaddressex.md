---
description: Localiza todos os endereços IP para localhost.
ms.assetid: 47f7d03e-c1a1-4395-9889-01891208fe0f
title: Função myIPAddressEx
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
ms.openlocfilehash: 5db6107c061c845113e91590dab405bdd84cb4741f766abfeef6a1344652f115
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744158"
---
# <a name="myipaddressex-function"></a>Função myIPAddressEx

Localiza todos os endereços IP para localhost.

## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Uma cadeia de caracteres delimitada por pontos e vírgulas que contém todos os endereços IP para localhost (IPv6 e/ou IPv4) ou uma cadeia de caracteres vazia se não for possível resolver localhost para um endereço IP.

## <a name="remarks"></a>Comentários

Os implementadores FindProxyforURLEx devem adicionar código que divide a cadeia de caracteres de endereços IP delimitados por e vírgula em endereços separados.

## <a name="examples"></a>Exemplos

``` syntax
myIpAddressEx();
    would return the string "fe80::380c:2e71:f5b9:a3b5%15;fe80::982d:a3b3:97ad:7dd0%9;2001:4898:28:7:982d:a3b3:97ad:7dd0;2001:4898:28:7:adfe:a643:8130:2fdc;fe80::5efe:10.70.92.74%13;3ffe:8311:ffff:f70f:0:5efe:10.70.92.74;10.70.92.74;3ffe:831f:4136:e37e:380c:2e71:f5b9:a3b5" 
    if you were running on that host.
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Definições de API do Auxiliar de Proxy com IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[Extensões IPv6 para o formato de arquivo de configuração automática do navegador](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 




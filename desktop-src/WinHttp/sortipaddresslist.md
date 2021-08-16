---
description: Classifica uma lista de endereços IP.
ms.assetid: 1266d6f3-e9f5-4e6b-9431-7329df156f0a
title: Função sortIpAddressList
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
ms.openlocfilehash: 3144ecf044f832a49dd6aa4d9fabf76ce8e81c79c195ec101d294c432a8081e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118562442"
---
# <a name="sortipaddresslist-function"></a>Função sortIpAddressList

Classifica uma lista de endereços IP.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*IpAddressList* 
</dt> <dd>

Uma cadeia de caracteres delimitada por pontos e vírgulas que contém endereços IP.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Uma lista de endereços IP delimitados por e vírgulas ou uma cadeia de caracteres vazia se não for possível classificar a lista de endereços IP.

## <a name="remarks"></a>Comentários

Os implementadores FindProxyforURLEx devem adicionar código que divide a cadeia de caracteres de endereços IP delimitados por e vírgula em endereços separados.

## <a name="examples"></a>Exemplos

``` syntax
sortIpAddressList(2001:4898:28:3:201:2ff:feea:fc14; 
                  157.59.139.22; 
                  fe80::5efe:157.59.139.22");
    returns "fe80::5efe:157.59.139.22;2001:4898:28:3:201:2ff:feea:fc14;157.59.139.22" 
    A list of sorted IP addresses. If there both IPv6 and IPv4 IP addresses are passed as input to this function, then the sorted IPv6 addresses are followed by sorted IPv4 addresses
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Definições de API do Auxiliar de Proxy com IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[Extensões IPv6 para o formato de arquivo de configuração automática do navegador](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 




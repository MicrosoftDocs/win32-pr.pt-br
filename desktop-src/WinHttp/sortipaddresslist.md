---
description: Classifica uma lista de endereços IP.
ms.assetid: 1266d6f3-e9f5-4e6b-9431-7329df156f0a
title: função sortIpAddressList
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
ms.openlocfilehash: 600d87a58248aafdef5b0a8a7f284f4094c95780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814512"
---
# <a name="sortipaddresslist-function"></a>função sortIpAddressList

Classifica uma lista de endereços IP.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*IpAddresslist* 
</dt> <dd>

Uma cadeia de caracteres delimitada por ponto e vírgula contendo endereços IP.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Uma lista de endereços IP delimitados por ponto-e-vírgula ou uma cadeia de caracteres vazia se não for possível classificar a lista de endereços IP.

## <a name="remarks"></a>Comentários

Os implementadores de FindProxyforURLEx devem adicionar um código que interrompa a cadeia de caracteres de endereços IP delimitados por ponto e vírgula em endereços separados.

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

[Definições da API auxiliar de proxy com reconhecimento de IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[Formato de arquivo de configuração automática de extensões IPv6 para navegador](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 




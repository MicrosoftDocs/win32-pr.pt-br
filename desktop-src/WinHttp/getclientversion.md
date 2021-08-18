---
description: Obtém a versão do mecanismo de processamento WPAD.
ms.assetid: f9e9a867-d491-4d46-bbd8-c0c3d8d5b3d6
title: função getClientVersion
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
ms.openlocfilehash: 33aeb4bd59730c48407220fede0cec0a606614f4a9692cd0e9852d56757a7f9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133209"
---
# <a name="getclientversion-function"></a>função getClientVersion

Obtém a versão do mecanismo de processamento WPAD.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*IpAddresslist* 
</dt> <dd>

Uma cadeia de caracteres delimitada por ponto e vírgula contendo endereços IP.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Uma lista de endereços IP delimitados por ponto-e-vírgula ou uma cadeia de caracteres vazia se não for possível classificar a lista de endereços IP.

## <a name="remarks"></a>Comentários

Atualmente, essa função retorna a versão 1,0.

A Microsoft adicionou essa função para permitir que os administradores de ti atualizem seus scripts WPAD para usar versões diferentes do mecanismo de processamento WPAD sem causar interrupções na implantação existente. Por exemplo, se a Microsoft tiver adicionado uma função à versão 2,0 do mecanismo WPAD, os administradores poderão verificar a versão antes de tentar chamar essa função. Isso permite que o script funcione com o cliente executando as versões 1,0 e 2,0 do mecanismo WPAD.

## <a name="examples"></a>Exemplos

``` syntax
getClientVersion();
    returns the appropriate versions number of the WPAD engine.
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Definições da API auxiliar de proxy com reconhecimento de IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[Formato de arquivo de configuração automática de extensões IPv6 para navegador](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 




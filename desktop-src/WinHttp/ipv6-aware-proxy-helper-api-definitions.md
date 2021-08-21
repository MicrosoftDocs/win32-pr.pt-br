---
description: Para aproveitar as funções habilitadas para IPv6, os administradores de ti devem definir dentro de seu script de WPAD, uma função chamada FindProxyForURLEx (URL, host) que substituirá a função FindProxyForUrl herdada (URL, host).
ms.assetid: e531a66d-5c50-4065-a12a-783fd4d1d310
title: Definições de API do auxiliar de proxy IPv6-Aware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bdf7c36b0f0d29f84a0dfc0eb7c21cb577ef1b9ef75cb69cec34a7f7858e7a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052074"
---
# <a name="ipv6-aware-proxy-helper-api-definitions"></a>Definições de API do auxiliar de proxy IPv6-Aware

Para aproveitar as funções habilitadas para IPv6, os administradores de ti devem definir dentro de seu script de WPAD, uma função chamada FindProxyForURLEx (URL, host) que substituirá a função FindProxyForUrl herdada (URL, host). Somente da nova função FindProxyForURLEx os administradores poderão executar as novas funções.

Também tentamos simplificar o trabalho para desenvolvedores, alinhando nossas funções para retornar tipos diferentes de endereços IP na mesma ordem de preferência de outros componentes de rede, especificamente endereços IPv6 seguidos de endereços IPv4 (ou seja, o comportamento atual da função getaddrinfo (..) do Winsock).

As funções a seguir são extensões para a [especificação de formato de arquivo de configuração automática de proxy do navegador (PAC)](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html) para permitir que os scripts WPAD manipulem redes compatíveis com IPv6.

## <a name="predefined-functions-and-environment-for-the-javascript-function-findproxyforurlex"></a>Funções predefinidas e ambiente para a função JavaScript FindProxyforURLEx

Condições baseadas em nome de host

<dl> <dt>

[**isResolvableEx**](isresolvableex.md)
</dt> <dd>

Determina se uma determinada cadeia de caracteres de host pode ser resolvida para um endereço IP.

</dd> <dt>

[**isInNetEx**](isinnetex.md)
</dt> <dd>

Determina se um endereço IP está em uma sub-rede específica.

</dd> </dl>

Funções do utilitário relacionado

<dl> <dt>

[**dnsResolveEx**](dnsresolveex.md)
</dt> <dd>

Resolva uma cadeia de caracteres de host para seu endereço IP.

</dd> <dt>

[**myIPAddressEx**](myipaddressex.md)
</dt> <dd>

Localiza todos os endereços IP para localhost.

</dd> <dt>

[**sortIpAddressList**](sortipaddresslist.md)
</dt> <dd>

Classifica uma lista de endereços IP.

</dd> <dt>

[**getClientVersion**](getclientversion.md)
</dt> <dd>

Obtém a versão do mecanismo de processamento WPAD.

</dd> </dl>

> [!Note]  
> essa funcionalidade requer Windows Internet Explorer 7 ou superior.

 

 

 




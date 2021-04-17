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
ms.openlocfilehash: 1c63ba3e20653c41864394d9c563c851f2aab5e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105791375"
---
# <a name="dnsresolveex-function"></a><span data-ttu-id="a5319-103">função dnsResolveEx</span><span class="sxs-lookup"><span data-stu-id="a5319-103">dnsResolveEx function</span></span>

<span data-ttu-id="a5319-104">Resolver uma cadeia de caracteres de host para seu endereço IP</span><span class="sxs-lookup"><span data-stu-id="a5319-104">Resolve a host string to its IP address</span></span>

## <a name="parameters"></a><span data-ttu-id="a5319-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a5319-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5319-106">*hospedeira*</span><span class="sxs-lookup"><span data-stu-id="a5319-106">*host*</span></span> 
</dt> <dd>

<span data-ttu-id="a5319-107">Uma cadeia de caracteres que contém o host HTTP que é fornecido para FindProxyForUrl.</span><span class="sxs-lookup"><span data-stu-id="a5319-107">A string containing the HTTP host that is supplied to FindProxyForUrl.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5319-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a5319-108">Return value</span></span>

<span data-ttu-id="a5319-109">Uma cadeia de caracteres delimitada por ponto e vírgula contendo endereços IPv6 e IPv4 ou uma cadeia de caracteres vazia se o host não puder ser resolvido.</span><span class="sxs-lookup"><span data-stu-id="a5319-109">A semi-colon delimited string containing IPv6 and IPv4 addresses or an empty string if host is not resolvable.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5319-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5319-110">Remarks</span></span>

<span data-ttu-id="a5319-111">Os implementadores de FindProxyforURLEx devem adicionar um código que interrompa a cadeia de caracteres de endereços IP delimitados por ponto e vírgula em endereços separados.</span><span class="sxs-lookup"><span data-stu-id="a5319-111">FindProxyforURLEx implementers should add code that breaks the string of semi-colon delimited IP addresses into separate addresses.</span></span>

## <a name="examples"></a><span data-ttu-id="a5319-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a5319-112">Examples</span></span>

``` syntax
dnsResolveEx("testmachine1");
    returns the string "fe80::380c:2e71:f5b9:a3b5%15;fe80::982d:a3b3:97ad:7dd0%9;2001:4898:28:7:982d:a3b3:97ad:7dd0;2001:4898:28:7:adfe:a643:8130:2fdc;fe80::5efe:10.70.92.74%13;3ffe:8311:ffff:f70f:0:5efe:10.70.92.74;10.70.92.74;3ffe:831f:4136:e37e:380c:2e71
```

## <a name="see-also"></a><span data-ttu-id="a5319-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5319-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5319-114">Definições da API auxiliar de proxy com reconhecimento de IPv6</span><span class="sxs-lookup"><span data-stu-id="a5319-114">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[<span data-ttu-id="a5319-115">Formato de arquivo de configuração automática de extensões IPv6 para navegador</span><span class="sxs-lookup"><span data-stu-id="a5319-115">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 




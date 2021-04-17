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
# <a name="myipaddressex-function"></a><span data-ttu-id="4c4ce-103">função myIPAddressEx</span><span class="sxs-lookup"><span data-stu-id="4c4ce-103">myIPAddressEx function</span></span>

<span data-ttu-id="4c4ce-104">Localiza todos os endereços IP para localhost.</span><span class="sxs-lookup"><span data-stu-id="4c4ce-104">Finds all the IP addresses for localhost.</span></span>

## <a name="parameters"></a><span data-ttu-id="4c4ce-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c4ce-105">Parameters</span></span>

<span data-ttu-id="4c4ce-106">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4c4ce-106">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4c4ce-107">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4c4ce-107">Return value</span></span>

<span data-ttu-id="4c4ce-108">Uma cadeia de caracteres delimitada por ponto e vírgula contendo todos os endereços IP para localhost (IPv6 e/ou IPv4) ou uma cadeia de caracteres vazia se não for possível resolver o localhost para um endereço IP.</span><span class="sxs-lookup"><span data-stu-id="4c4ce-108">A semi-colon delimited string containing all IP addresses for localhost (IPv6 and/or IPv4), or an empty string if unable to resolve localhost to an IP address.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c4ce-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c4ce-109">Remarks</span></span>

<span data-ttu-id="4c4ce-110">Os implementadores de FindProxyforURLEx devem adicionar um código que interrompa a cadeia de caracteres de endereços IP delimitados por ponto e vírgula em endereços separados.</span><span class="sxs-lookup"><span data-stu-id="4c4ce-110">FindProxyforURLEx implementers should add code that breaks the string of semi-colon delimited IP addresses into separate addresses.</span></span>

## <a name="examples"></a><span data-ttu-id="4c4ce-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4c4ce-111">Examples</span></span>

``` syntax
myIpAddressEx();
    would return the string "fe80::380c:2e71:f5b9:a3b5%15;fe80::982d:a3b3:97ad:7dd0%9;2001:4898:28:7:982d:a3b3:97ad:7dd0;2001:4898:28:7:adfe:a643:8130:2fdc;fe80::5efe:10.70.92.74%13;3ffe:8311:ffff:f70f:0:5efe:10.70.92.74;10.70.92.74;3ffe:831f:4136:e37e:380c:2e71:f5b9:a3b5" 
    if you were running on that host.
```

## <a name="see-also"></a><span data-ttu-id="4c4ce-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c4ce-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c4ce-113">Definições da API auxiliar de proxy com reconhecimento de IPv6</span><span class="sxs-lookup"><span data-stu-id="4c4ce-113">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[<span data-ttu-id="4c4ce-114">Formato de arquivo de configuração automática de extensões IPv6 para navegador</span><span class="sxs-lookup"><span data-stu-id="4c4ce-114">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 




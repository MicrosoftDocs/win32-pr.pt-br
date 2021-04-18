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
# <a name="sortipaddresslist-function"></a><span data-ttu-id="908a5-103">função sortIpAddressList</span><span class="sxs-lookup"><span data-stu-id="908a5-103">sortIpAddressList function</span></span>

<span data-ttu-id="908a5-104">Classifica uma lista de endereços IP.</span><span class="sxs-lookup"><span data-stu-id="908a5-104">Sorts a list of IP addresses.</span></span>

## <a name="parameters"></a><span data-ttu-id="908a5-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="908a5-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="908a5-106">*IpAddresslist*</span><span class="sxs-lookup"><span data-stu-id="908a5-106">*IpAddressList*</span></span> 
</dt> <dd>

<span data-ttu-id="908a5-107">Uma cadeia de caracteres delimitada por ponto e vírgula contendo endereços IP.</span><span class="sxs-lookup"><span data-stu-id="908a5-107">A semi-colon delimited string containing IP addresses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="908a5-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="908a5-108">Return value</span></span>

<span data-ttu-id="908a5-109">Uma lista de endereços IP delimitados por ponto-e-vírgula ou uma cadeia de caracteres vazia se não for possível classificar a lista de endereços IP.</span><span class="sxs-lookup"><span data-stu-id="908a5-109">A list of sorted semi-colon delimited IP addresses or an empty string if unable to sort the IP Address list.</span></span>

## <a name="remarks"></a><span data-ttu-id="908a5-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="908a5-110">Remarks</span></span>

<span data-ttu-id="908a5-111">Os implementadores de FindProxyforURLEx devem adicionar um código que interrompa a cadeia de caracteres de endereços IP delimitados por ponto e vírgula em endereços separados.</span><span class="sxs-lookup"><span data-stu-id="908a5-111">FindProxyforURLEx implementers should add code that breaks the string of semi-colon delimited IP addresses into separate addresses.</span></span>

## <a name="examples"></a><span data-ttu-id="908a5-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="908a5-112">Examples</span></span>

``` syntax
sortIpAddressList(2001:4898:28:3:201:2ff:feea:fc14; 
                  157.59.139.22; 
                  fe80::5efe:157.59.139.22");
    returns "fe80::5efe:157.59.139.22;2001:4898:28:3:201:2ff:feea:fc14;157.59.139.22" 
    A list of sorted IP addresses. If there both IPv6 and IPv4 IP addresses are passed as input to this function, then the sorted IPv6 addresses are followed by sorted IPv4 addresses
```

## <a name="see-also"></a><span data-ttu-id="908a5-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="908a5-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="908a5-114">Definições da API auxiliar de proxy com reconhecimento de IPv6</span><span class="sxs-lookup"><span data-stu-id="908a5-114">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[<span data-ttu-id="908a5-115">Formato de arquivo de configuração automática de extensões IPv6 para navegador</span><span class="sxs-lookup"><span data-stu-id="908a5-115">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 




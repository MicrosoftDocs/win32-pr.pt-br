---
description: Determina se um endereço IP está em uma sub-rede específica.
ms.assetid: 2fbfad9c-86b1-44c3-860b-a5c98ac6c2e9
title: função isInNetEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- isInNetEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: d738fbf5788fbe56d8c801b6c5256e96e8d4a6f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782490"
---
# <a name="isinnetex-function"></a><span data-ttu-id="51f92-103">função isInNetEx</span><span class="sxs-lookup"><span data-stu-id="51f92-103">isInNetEx function</span></span>

<span data-ttu-id="51f92-104">Determina se um endereço IP está em uma sub-rede específica.</span><span class="sxs-lookup"><span data-stu-id="51f92-104">Determines if an IP address is in a specific subnet.</span></span>

## <a name="parameters"></a><span data-ttu-id="51f92-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="51f92-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51f92-106">*IP*</span><span class="sxs-lookup"><span data-stu-id="51f92-106">*IPaddress*</span></span> 
</dt> <dd>

<span data-ttu-id="51f92-107">Uma cadeia de caracteres que contém endereços IPv6/IPv4.</span><span class="sxs-lookup"><span data-stu-id="51f92-107">A string containing IPv6/IPv4 addresses.</span></span>

</dd> <dt>

<span data-ttu-id="51f92-108">*IPprefix*</span><span class="sxs-lookup"><span data-stu-id="51f92-108">*IPprefix*</span></span> 
</dt> <dd>

<span data-ttu-id="51f92-109">Uma cadeia de caracteres que contém o prefixo de IP delimitado por dois bits com os n principais bit especificados no campo de bits (ou seja, 3FFE: 8311: ffff::/48 ou 123.112.0.0/16).</span><span class="sxs-lookup"><span data-stu-id="51f92-109">A string containing colon delimited IP prefix with top n bits specified in the bit field (i.e. 3ffe:8311:ffff::/48 or 123.112.0.0/16).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51f92-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="51f92-110">Return value</span></span>

<span data-ttu-id="51f92-111">TRUE se o host estiver na mesma sub-rede; caso contrário, FALSE.</span><span class="sxs-lookup"><span data-stu-id="51f92-111">TRUE if the host is in the same subnet; otherwise, FALSE.</span></span>

<span data-ttu-id="51f92-112">Também retornará FALSE se o prefixo não estiver no formato correto ou se os endereços e prefixos de tipos diferentes forem usados na comparação (ou seja, o prefixo IPv4 e um endereço IPv6).</span><span class="sxs-lookup"><span data-stu-id="51f92-112">Also returns FALSE if the prefix is not in the correct format or if addresses and prefixes of different types are used in the comparison (i.e. IPv4 prefix and an IPv6 address).</span></span>

## <a name="examples"></a><span data-ttu-id="51f92-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="51f92-113">Examples</span></span>

``` syntax
isInNetEx(host, "198.95.249.79/32");
    true if the IP address of host matches exactly 198.95.249.79
```

``` syntax
isInNetEx(host, "198.95.0.0/16");
    true if the IP address of the host matches 198.95.*.*
```

``` syntax
isInNetEx(host, "3ffe:8311:ffff::/48");
    true if the IP address of the host matches 3ffe:8311:fff:*:*:*:*:*
```

## <a name="see-also"></a><span data-ttu-id="51f92-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="51f92-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51f92-115">Definições da API auxiliar de proxy com reconhecimento de IPv6</span><span class="sxs-lookup"><span data-stu-id="51f92-115">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[<span data-ttu-id="51f92-116">Formato de arquivo de configuração automática de extensões IPv6 para navegador</span><span class="sxs-lookup"><span data-stu-id="51f92-116">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 




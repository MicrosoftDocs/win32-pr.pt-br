---
description: Determina se uma determinada cadeia de caracteres de host pode ser resolvida para um endereço IP.
ms.assetid: 83e52ca7-2ea0-419d-b09d-9301c1982b98
title: função isResolvableEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- isResolvableEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1172aaed93a9fc6cede5ae5393c5dd430613a466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811550"
---
# <a name="isresolvableex-function"></a><span data-ttu-id="71f4e-103">função isResolvableEx</span><span class="sxs-lookup"><span data-stu-id="71f4e-103">isResolvableEx function</span></span>

<span data-ttu-id="71f4e-104">Determina se uma determinada cadeia de caracteres de host pode ser resolvida para um endereço IP.</span><span class="sxs-lookup"><span data-stu-id="71f4e-104">Determines if a given host string can resolve to an IP address.</span></span>

## <a name="parameters"></a><span data-ttu-id="71f4e-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71f4e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71f4e-106">*hospedeira*</span><span class="sxs-lookup"><span data-stu-id="71f4e-106">*host*</span></span> 
</dt> <dd>

<span data-ttu-id="71f4e-107">Uma cadeia de caracteres que contém o host HTTP que é fornecido para FindProxyForUrl.</span><span class="sxs-lookup"><span data-stu-id="71f4e-107">A string containing the HTTP host that is supplied to FindProxyForUrl.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71f4e-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="71f4e-108">Return value</span></span>

<span data-ttu-id="71f4e-109">TRUE se o host puder ser resolvido para um endereço IPv4 ou IPv6; caso contrário, FALSE.</span><span class="sxs-lookup"><span data-stu-id="71f4e-109">TRUE if the host is resolvable to a IPv4 or IPv6 address; otherwise, FALSE.</span></span>

## <a name="examples"></a><span data-ttu-id="71f4e-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="71f4e-110">Examples</span></span>

``` syntax
isResolvableEx(host);
    true if the hostname can be resolved to and IP address 
```

``` syntax
isResolvableEx(host); 
    false if the hostname cannot be resolved to an IP address 
```

## <a name="see-also"></a><span data-ttu-id="71f4e-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="71f4e-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71f4e-112">Definições da API auxiliar de proxy com reconhecimento de IPv6</span><span class="sxs-lookup"><span data-stu-id="71f4e-112">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[<span data-ttu-id="71f4e-113">Formato de arquivo de configuração automática de extensões IPv6 para navegador</span><span class="sxs-lookup"><span data-stu-id="71f4e-113">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 




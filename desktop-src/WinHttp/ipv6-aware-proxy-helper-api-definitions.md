---
description: Para aproveitar as funções habilitadas para IPv6, os administradores de ti devem definir dentro de seu script de WPAD, uma função chamada FindProxyForURLEx (URL, host) que substituirá a função FindProxyForUrl herdada (URL, host).
ms.assetid: e531a66d-5c50-4065-a12a-783fd4d1d310
title: Definições de API do auxiliar de proxy IPv6-Aware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79b1ff5a0c287327593e65e29a0b03cfb59269f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770484"
---
# <a name="ipv6-aware-proxy-helper-api-definitions"></a><span data-ttu-id="813ed-103">Definições de API do auxiliar de proxy IPv6-Aware</span><span class="sxs-lookup"><span data-stu-id="813ed-103">IPv6-Aware Proxy Helper API Definitions</span></span>

<span data-ttu-id="813ed-104">Para aproveitar as funções habilitadas para IPv6, os administradores de ti devem definir dentro de seu script de WPAD, uma função chamada FindProxyForURLEx (URL, host) que substituirá a função FindProxyForUrl herdada (URL, host).</span><span class="sxs-lookup"><span data-stu-id="813ed-104">In order to take advantage of the IPv6 enabled functions, IT administrators must define within their WPAD script, a function called FindProxyForURLEx (url, host) which will replace the legacy FindProxyForUrl (url, host) function.</span></span> <span data-ttu-id="813ed-105">Somente da nova função FindProxyForURLEx os administradores poderão executar as novas funções.</span><span class="sxs-lookup"><span data-stu-id="813ed-105">Only from the new FindProxyForURLEx function will administrators be able to execute the new functions.</span></span>

<span data-ttu-id="813ed-106">Também tentamos simplificar o trabalho para desenvolvedores, alinhando nossas funções para retornar tipos diferentes de endereços IP na mesma ordem de preferência de outros componentes de rede, especificamente endereços IPv6 seguidos de endereços IPv4 (ou seja, o comportamento atual da função getaddrinfo (..) do Winsock).</span><span class="sxs-lookup"><span data-stu-id="813ed-106">We also attempted to simplify work for developers, by aligning our functions to return different types of IP addresses in the same order of preference as other networking components, specifically IPv6 addresses followed by IPv4 addresses (i.e. current behavior for Winsock’s getaddrinfo(..) function).</span></span>

<span data-ttu-id="813ed-107">As funções a seguir são extensões para a [especificação de formato de arquivo de configuração automática de proxy do navegador (PAC)](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html) para permitir que os scripts WPAD manipulem redes compatíveis com IPv6.</span><span class="sxs-lookup"><span data-stu-id="813ed-107">The following functions are extensions to the [Navigator Proxy Auto-Config (PAC) File Format specification](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html) to enable WPAD scripts to handle IPv6 capable networks.</span></span>

## <a name="predefined-functions-and-environment-for-the-javascript-function-findproxyforurlex"></a><span data-ttu-id="813ed-108">Funções predefinidas e ambiente para a função JavaScript FindProxyforURLEx</span><span class="sxs-lookup"><span data-stu-id="813ed-108">Predefined Functions and Environment for the JavaScript Function FindProxyforURLEx</span></span>

<span data-ttu-id="813ed-109">Condições baseadas em nome de host</span><span class="sxs-lookup"><span data-stu-id="813ed-109">Hostname based conditions</span></span>

<dl> <dt>

[<span data-ttu-id="813ed-110">**isResolvableEx**</span><span class="sxs-lookup"><span data-stu-id="813ed-110">**isResolvableEx**</span></span>](isresolvableex.md)
</dt> <dd>

<span data-ttu-id="813ed-111">Determina se uma determinada cadeia de caracteres de host pode ser resolvida para um endereço IP.</span><span class="sxs-lookup"><span data-stu-id="813ed-111">Determines if a given host string can resolve to an IP address.</span></span>

</dd> <dt>

[<span data-ttu-id="813ed-112">**isInNetEx**</span><span class="sxs-lookup"><span data-stu-id="813ed-112">**isInNetEx**</span></span>](isinnetex.md)
</dt> <dd>

<span data-ttu-id="813ed-113">Determina se um endereço IP está em uma sub-rede específica.</span><span class="sxs-lookup"><span data-stu-id="813ed-113">Determines if an IP address is in a specific subnet.</span></span>

</dd> </dl>

<span data-ttu-id="813ed-114">Funções do utilitário relacionado</span><span class="sxs-lookup"><span data-stu-id="813ed-114">Related utility functions</span></span>

<dl> <dt>

[<span data-ttu-id="813ed-115">**dnsResolveEx**</span><span class="sxs-lookup"><span data-stu-id="813ed-115">**dnsResolveEx**</span></span>](dnsresolveex.md)
</dt> <dd>

<span data-ttu-id="813ed-116">Resolva uma cadeia de caracteres de host para seu endereço IP.</span><span class="sxs-lookup"><span data-stu-id="813ed-116">Resolve a host string to its IP address.</span></span>

</dd> <dt>

[<span data-ttu-id="813ed-117">**myIPAddressEx**</span><span class="sxs-lookup"><span data-stu-id="813ed-117">**myIPAddressEx**</span></span>](myipaddressex.md)
</dt> <dd>

<span data-ttu-id="813ed-118">Localiza todos os endereços IP para localhost.</span><span class="sxs-lookup"><span data-stu-id="813ed-118">Finds all the IP addresses for localhost.</span></span>

</dd> <dt>

[<span data-ttu-id="813ed-119">**sortIpAddressList**</span><span class="sxs-lookup"><span data-stu-id="813ed-119">**sortIpAddressList**</span></span>](sortipaddresslist.md)
</dt> <dd>

<span data-ttu-id="813ed-120">Classifica uma lista de endereços IP.</span><span class="sxs-lookup"><span data-stu-id="813ed-120">Sorts a list of IP addresses.</span></span>

</dd> <dt>

[<span data-ttu-id="813ed-121">**getClientVersion**</span><span class="sxs-lookup"><span data-stu-id="813ed-121">**getClientVersion**</span></span>](getclientversion.md)
</dt> <dd>

<span data-ttu-id="813ed-122">Obtém a versão do mecanismo de processamento WPAD.</span><span class="sxs-lookup"><span data-stu-id="813ed-122">Gets the version of the WPAD processing engine.</span></span>

</dd> </dl>

> [!Note]  
> <span data-ttu-id="813ed-123">Essa funcionalidade requer o Windows Internet Explorer 7 ou superior.</span><span class="sxs-lookup"><span data-stu-id="813ed-123">This functionality requires Windows Internet Explorer 7 or greater.</span></span>

 

 

 




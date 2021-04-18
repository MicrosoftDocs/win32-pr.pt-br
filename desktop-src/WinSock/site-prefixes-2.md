---
description: Especifica um prefixo que está no link para a interface \# 4.
ms.assetid: cc3aa99d-cf45-460c-bdc1-3e9a19806fe4
title: Prefixos de site IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bed8a21c59f9b6727c98ccb7fdacf4e9ec6ea5cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807937"
---
# <a name="ipv6-site-prefixes"></a><span data-ttu-id="dcfa3-103">Prefixos de site IPv6</span><span class="sxs-lookup"><span data-stu-id="dcfa3-103">IPv6 Site Prefixes</span></span>

<span data-ttu-id="dcfa3-104">O comando IPv6 RTU permite que os prefixos em link publicados sejam configurados com um comprimento de prefixo de site.</span><span class="sxs-lookup"><span data-stu-id="dcfa3-104">The ipv6 rtu command allows published on-link prefixes to be configured with a site prefix length.</span></span> <span data-ttu-id="dcfa3-105">Se especificado, o comprimento do prefixo do site é colocado em uma opção de informações de prefixo em anúncios de roteador.</span><span class="sxs-lookup"><span data-stu-id="dcfa3-105">If specified, the site prefix length is put into a prefix information option in router advertisements.</span></span> <span data-ttu-id="dcfa3-106">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="dcfa3-106">For example:</span></span>

``` syntax
ipv6 rtu 2002:836b:9820:2::/64 4 pub life 1800 spl 48
```

<span data-ttu-id="dcfa3-107">Especifica um prefixo que está no link para a interface \# 4.</span><span class="sxs-lookup"><span data-stu-id="dcfa3-107">specifies a prefix that is on-link to interface \#4.</span></span> <span data-ttu-id="dcfa3-108">O prefixo é publicado, o que significa que ele será incluído em anúncios de roteador se \# a interface 4 for uma interface de anúncio.</span><span class="sxs-lookup"><span data-stu-id="dcfa3-108">The prefix is published, meaning that it is included in router advertisements if interface \#4 is an advertising interface.</span></span> <span data-ttu-id="dcfa3-109">O tempo de vida na opção de informações de prefixo é de 1800 segundos (30 minutos).</span><span class="sxs-lookup"><span data-stu-id="dcfa3-109">The lifetime in the prefix information option is 1800 seconds (30 minutes).</span></span> <span data-ttu-id="dcfa3-110">O comprimento do prefixo do site na opção de informações de prefixo é 48.</span><span class="sxs-lookup"><span data-stu-id="dcfa3-110">The site prefix length in the prefix information option is 48.</span></span>

<span data-ttu-id="dcfa3-111">O recebimento de uma opção de informações de prefixo que especifica um prefixo de site faz com que uma entrada seja criada na tabela de prefixo do site, que pode ser exibida usando o comando SPT do IPv6.</span><span class="sxs-lookup"><span data-stu-id="dcfa3-111">The receipt of a prefix information option that specifies a site prefix causes an entry to be created in the site prefix table, which can be displayed by using the ipv6 spt command.</span></span> <span data-ttu-id="dcfa3-112">A tabela de prefixo do site é usada para remover endereços locais inadequados de site daqueles retornados pelo [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) e pelas funções relacionadas.</span><span class="sxs-lookup"><span data-stu-id="dcfa3-112">The site prefix table is used to remove inappropriate site-local addresses from those returned by the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and related functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dcfa3-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dcfa3-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dcfa3-114">Link IPv6-local e endereços locais do site</span><span class="sxs-lookup"><span data-stu-id="dcfa3-114">IPv6 Link-local and Site-local Addresses</span></span>](link-local-and-site-local-addresses-2.md)
</dt> <dt>

[<span data-ttu-id="dcfa3-115">Netsh.exe</span><span class="sxs-lookup"><span data-stu-id="dcfa3-115">Netsh.exe</span></span>](netsh-exe.md)
</dt> </dl>

 

 




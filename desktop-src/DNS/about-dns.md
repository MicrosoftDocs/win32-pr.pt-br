---
title: Sobre o DNS
description: O DNS (sistema de nomes de domínio) é um protocolo padrão do setor usado para localizar computadores em uma rede baseada em IP. Os usuários podem lembrar nomes de exibição, como www.microsoft.com mais fáceis do que endereços baseados em número, como 207.46.131.137.
ms.assetid: 3a899ba4-4338-4119-aa68-a969d196c4f5
keywords:
- Sobre DNS do sistema de nome de domínio
- DNS do sistema de nome de domínio, sobre
- DNS do sistema de nomes de domínio, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c98573e72db645d96c263efd479135807274c18a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "104172894"
---
# <a name="about-dns"></a><span data-ttu-id="16acd-107">Sobre o DNS</span><span class="sxs-lookup"><span data-stu-id="16acd-107">About DNS</span></span>

<span data-ttu-id="16acd-108">O DNS (sistema de nomes de domínio) é um protocolo padrão do setor usado para localizar computadores em uma rede baseada em IP.</span><span class="sxs-lookup"><span data-stu-id="16acd-108">Domain Name System (DNS) is an industry-standard protocol used to locate computers on an IP-based network.</span></span> <span data-ttu-id="16acd-109">Os usuários podem lembrar nomes de exibição, como `www.microsoft.com` mais fáceis do que endereços baseados em número, como 207.46.131.137.</span><span class="sxs-lookup"><span data-stu-id="16acd-109">Users can remember display names, such as `www.microsoft.com` easier than number-based addresses, such as 207.46.131.137.</span></span>

<span data-ttu-id="16acd-110">Redes IP, como redes Internet e Windows, dependem de endereços baseados em número para transmitir dados em toda a rede; Portanto, é necessário converter nomes de exibição (como `www.microsoft.com` ) em endereços numéricos que a rede possa reconhecer (como 207.46.131.137).</span><span class="sxs-lookup"><span data-stu-id="16acd-110">IP networks, such as the Internet and Windows networks, rely on number-based addresses to transmit data throughout the network; therefore, it is necessary to translate display names (such as `www.microsoft.com`) into numeric addresses that the network can recognize (such as 207.46.131.137).</span></span> <span data-ttu-id="16acd-111">O DNS é o serviço de escolha no Windows para localizar esses recursos e convertê-los em endereços IP.</span><span class="sxs-lookup"><span data-stu-id="16acd-111">DNS is the service of choice in Windows to locate such resources and translate them into IP addresses.</span></span>

<span data-ttu-id="16acd-112">O DNS é o serviço localizador primário para Active Directory e, portanto, o DNS pode ser considerado um serviço base para Windows e Active Directory.</span><span class="sxs-lookup"><span data-stu-id="16acd-112">DNS is the primary locator service for Active Directory, and therefore, DNS can be considered a base service for both Windows and Active Directory.</span></span> <span data-ttu-id="16acd-113">O Windows fornece funções que permitem que os programadores de aplicativos usem funções DNS, como fazer consultas de DNS programaticamente, comparar registros e pesquisar nomes.</span><span class="sxs-lookup"><span data-stu-id="16acd-113">Windows provides functions that enable application programmers to use DNS functions such as programmatically making DNS queries, comparing records, and looking up names.</span></span>

<span data-ttu-id="16acd-114">Muitas funções DNS são realmente tipos de função, pois há um nome de base para a função, mas seu uso depende da codificação de caracteres.</span><span class="sxs-lookup"><span data-stu-id="16acd-114">Many DNS functions are actually function types, in that there is a base name for the function, but its use depends on character encoding.</span></span> <span data-ttu-id="16acd-115">Por exemplo, a função [**DnsQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) está listada na referência de função da API (interface de programação de aplicativo) do DNS como **DnsQuery**, mas seu uso em aplicativos depende de a codificação de caracteres ser ANSI (designada ao acrescentar \_ um ao nome do tipo de função), Unicode (designado por acrescentar \_ W ao nome do tipo de função) ou UTF-8 (designado acrescentando \_ UTF ao nome do tipo de função).</span><span class="sxs-lookup"><span data-stu-id="16acd-115">For example, the [**DnsQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) function is listed in the function reference of the DNS Application Programming Interface (API) as **DnsQuery**, but its use in applications depends on whether the character encoding is ANSI (designated by appending \_A to the function type name), Unicode (designated by appending \_W to the function type name), or UTF-8 (designated by appending \_UTF to the function type name).</span></span> <span data-ttu-id="16acd-116">Portanto, a chamada de função para a função **DnsQuery** seria, na verdade, um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="16acd-116">Therefore, the function call for the **DnsQuery** function would actually be one of the following:</span></span>

<span data-ttu-id="16acd-117">DnsQuery \_ a ( \_ a para codificação ANSI)</span><span class="sxs-lookup"><span data-stu-id="16acd-117">DnsQuery\_A (\_A for ANSI encoding)</span></span>

<span data-ttu-id="16acd-118">DnsQuery \_ w ( \_ w para codificação Unicode)</span><span class="sxs-lookup"><span data-stu-id="16acd-118">DnsQuery\_W (\_W for Unicode encoding)</span></span>

<span data-ttu-id="16acd-119">DnsQuery \_ UTF8 ( \_ UTF8 para codificação UTF-8)</span><span class="sxs-lookup"><span data-stu-id="16acd-119">DnsQuery\_UTF8 (\_UTF8 for UTF-8 encoding)</span></span>

<span data-ttu-id="16acd-120">Todas as funções que exigem essa Convenção declaram claramente esse requisito nas primeiras frases de sua definição de função.</span><span class="sxs-lookup"><span data-stu-id="16acd-120">All functions that require this convention clearly state this requirement within the first few sentences of their function definition.</span></span> <span data-ttu-id="16acd-121">Usar o nome de função apropriado; por exemplo, você não pode simplesmente chamar [**DnsQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) em vez de DnsQuery \_ A.</span><span class="sxs-lookup"><span data-stu-id="16acd-121">Use the proper function name; for example, you cannot simply call [**DnsQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) instead of DnsQuery\_A.</span></span>

 

 





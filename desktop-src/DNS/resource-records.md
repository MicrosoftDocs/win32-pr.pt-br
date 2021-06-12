---
title: Registros de recursos
description: Saiba mais sobre os registros de recursos. Um registro de recurso é a unidade de entrada de informações nos arquivos de zona DNS, que é usada para resolver todas as consultas DNS.
ms.assetid: c64907c2-ebd3-4550-9454-13f51a6d7ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84bd000e2d88884bbb387748eaced1d0d58a324
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010669"
---
# <a name="resource-records"></a><span data-ttu-id="7fb6a-104">Registros de recursos</span><span class="sxs-lookup"><span data-stu-id="7fb6a-104">Resource Records</span></span>

<span data-ttu-id="7fb6a-105">Um registro de recurso, conhecido como RR, é a unidade de entrada de informações nos arquivos de zona DNS; RRs são os blocos de construção básicos de nome de host e informações de IP e são usados para resolver todas as consultas DNS.</span><span class="sxs-lookup"><span data-stu-id="7fb6a-105">A resource record, commonly referred to as an RR, is the unit of information entry in DNS zone files; RRs are the basic building blocks of host-name and IP information and are used to resolve all DNS queries.</span></span> <span data-ttu-id="7fb6a-106">Os registros de recursos existem tantos tipos para fornecer serviços de resolução de nomes estendidos.</span><span class="sxs-lookup"><span data-stu-id="7fb6a-106">Resource records exist as many types to provide extended name-resolution services.</span></span>

<span data-ttu-id="7fb6a-107">Tipos diferentes de RRs têm formatos diferentes, pois contêm dados diferentes.</span><span class="sxs-lookup"><span data-stu-id="7fb6a-107">Different types of RRs have different formats, as they contain different data.</span></span> <span data-ttu-id="7fb6a-108">Em geral, no entanto, muitos RRs compartilham um formato comum, como ilustra o exemplo de registros de recursos de endereço a seguir.</span><span class="sxs-lookup"><span data-stu-id="7fb6a-108">In general, however, many RRs share a common format, as the following address resource records example illustrates.</span></span> <span data-ttu-id="7fb6a-109">O exemplo fictício a seguir explica os campos encontrados em um registro de recurso:</span><span class="sxs-lookup"><span data-stu-id="7fb6a-109">The following fictional example explains the fields found in an A resource record:</span></span>

``` syntax
microsoft.com. 600 IN A 150.150.150.1
```

-   <span data-ttu-id="7fb6a-110">O primeiro campo (microsoft.com) denota o proprietário.</span><span class="sxs-lookup"><span data-stu-id="7fb6a-110">The first field (microsoft.com) denotes the owner.</span></span>
-   <span data-ttu-id="7fb6a-111">O segundo campo (600) é o parâmetro time-to-Live (TTL), em segundos.</span><span class="sxs-lookup"><span data-stu-id="7fb6a-111">The second field (600) is the time-to-live (TTL) parameter, in seconds.</span></span>
-   <span data-ttu-id="7fb6a-112">O terceiro campo (em) é o campo de classe que representa a família de protocolos, que é quase sempre no, para classe de Internet.</span><span class="sxs-lookup"><span data-stu-id="7fb6a-112">The third field (IN) is the class field that represents the protocol family, which is almost always IN, for Internet class.</span></span>
-   <span data-ttu-id="7fb6a-113">O quarto campo (A) é o tipo de recurso que o RR está representando.</span><span class="sxs-lookup"><span data-stu-id="7fb6a-113">The fourth field (A) is the type of resource the RR is representing.</span></span>
-   <span data-ttu-id="7fb6a-114">O quinto campo (150.150.150.1) são os dados do recurso ou RDATA.</span><span class="sxs-lookup"><span data-stu-id="7fb6a-114">The fifth field (150.150.150.1) is the resource data, or RDATA.</span></span> <span data-ttu-id="7fb6a-115">Este campo é um tipo de variável que fornece informações apropriadas para o tipo de recurso; Nesse caso, é um endereço IP de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="7fb6a-115">This field is a variable type that provides information appropriate for the type of resource; in this case, it's a 32-bit IP address.</span></span>

<span data-ttu-id="7fb6a-116">Os seguintes tipos de registro de recurso são comumente usados no DNS:</span><span class="sxs-lookup"><span data-stu-id="7fb6a-116">The following resource record types are commonly used in DNS:</span></span>

-   <span data-ttu-id="7fb6a-117">Início de autoridade (SOA)</span><span class="sxs-lookup"><span data-stu-id="7fb6a-117">Start of authority (SOA)</span></span>
-   <span data-ttu-id="7fb6a-118">Servidor de nomes (NS)</span><span class="sxs-lookup"><span data-stu-id="7fb6a-118">Name server (NS)</span></span>
-   <span data-ttu-id="7fb6a-119">[*Registro de ponteiro*](p-gly.md) (PTR)</span><span class="sxs-lookup"><span data-stu-id="7fb6a-119">[*Pointer record*](p-gly.md) (PTR)</span></span>
-   <span data-ttu-id="7fb6a-120">Endereço (A)</span><span class="sxs-lookup"><span data-stu-id="7fb6a-120">Address (A)</span></span>
-   <span data-ttu-id="7fb6a-121">Endereço IPv6 (AAAA)</span><span class="sxs-lookup"><span data-stu-id="7fb6a-121">IPv6 Address (AAAA)</span></span>
-   <span data-ttu-id="7fb6a-122">Troca de email (MX)</span><span class="sxs-lookup"><span data-stu-id="7fb6a-122">Mail exchange (MX)</span></span>
-   <span data-ttu-id="7fb6a-123">[*Nome canônico*](c-gly.md) (CNAME)</span><span class="sxs-lookup"><span data-stu-id="7fb6a-123">[*Canonical name*](c-gly.md) (CNAME)</span></span>
-   <span data-ttu-id="7fb6a-124">Internet Serviço de Nomenclatura do Windows (WINS)</span><span class="sxs-lookup"><span data-stu-id="7fb6a-124">Windows Internet Naming Service (WINS)</span></span>
-   <span data-ttu-id="7fb6a-125">Pesquisa inversa do WINS (WINSr)</span><span class="sxs-lookup"><span data-stu-id="7fb6a-125">WINS Reverse Look up (WINSR)</span></span>

<span data-ttu-id="7fb6a-126">Há muitos outros tipos de registro de recurso no DNS.</span><span class="sxs-lookup"><span data-stu-id="7fb6a-126">There are many other resource record types in DNS.</span></span> <span data-ttu-id="7fb6a-127">Para obter mais informações, consulte [referência do provedor WMI de DNS](dns-wmi-provider-reference.md).</span><span class="sxs-lookup"><span data-stu-id="7fb6a-127">For more information, see [DNS WMI Provider Reference](dns-wmi-provider-reference.md).</span></span>

 

 





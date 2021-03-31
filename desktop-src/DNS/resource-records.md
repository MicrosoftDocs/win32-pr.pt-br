---
title: Registros de recursos
description: Um registro de recurso, conhecido como RR, é a unidade de entrada de informações nos arquivos de zona DNS; RRs são os blocos de construção básicos de nome de host e informações de IP e são usados para resolver todas as consultas DNS.
ms.assetid: c64907c2-ebd3-4550-9454-13f51a6d7ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05b667b95a8ede32018e1aad7de375e77a890487
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636668"
---
# <a name="resource-records"></a><span data-ttu-id="33748-103">Registros de recursos</span><span class="sxs-lookup"><span data-stu-id="33748-103">Resource Records</span></span>

<span data-ttu-id="33748-104">Um registro de recurso, conhecido como RR, é a unidade de entrada de informações nos arquivos de zona DNS; RRs são os blocos de construção básicos de nome de host e informações de IP e são usados para resolver todas as consultas DNS.</span><span class="sxs-lookup"><span data-stu-id="33748-104">A resource record, commonly referred to as an RR, is the unit of information entry in DNS zone files; RRs are the basic building blocks of host-name and IP information and are used to resolve all DNS queries.</span></span> <span data-ttu-id="33748-105">Os registros de recursos existem tantos tipos para fornecer serviços de resolução de nomes estendidos.</span><span class="sxs-lookup"><span data-stu-id="33748-105">Resource records exist as many types to provide extended name-resolution services.</span></span>

<span data-ttu-id="33748-106">Tipos diferentes de RRs têm formatos diferentes, pois contêm dados diferentes.</span><span class="sxs-lookup"><span data-stu-id="33748-106">Different types of RRs have different formats, as they contain different data.</span></span> <span data-ttu-id="33748-107">Em geral, no entanto, muitos RRs compartilham um formato comum, como ilustra o exemplo de registros de recursos de endereço a seguir.</span><span class="sxs-lookup"><span data-stu-id="33748-107">In general, however, many RRs share a common format, as the following address resource records example illustrates.</span></span> <span data-ttu-id="33748-108">O exemplo fictício a seguir explica os campos encontrados em um registro de recurso:</span><span class="sxs-lookup"><span data-stu-id="33748-108">The following fictional example explains the fields found in an A resource record:</span></span>

``` syntax
microsoft.com. 600 IN A 150.150.150.1
```

-   <span data-ttu-id="33748-109">O primeiro campo (microsoft.com) denota o proprietário.</span><span class="sxs-lookup"><span data-stu-id="33748-109">The first field (microsoft.com) denotes the owner.</span></span>
-   <span data-ttu-id="33748-110">O segundo campo (600) é o parâmetro time-to-Live (TTL), em segundos.</span><span class="sxs-lookup"><span data-stu-id="33748-110">The second field (600) is the time-to-live (TTL) parameter, in seconds.</span></span>
-   <span data-ttu-id="33748-111">O terceiro campo (em) é o campo de classe que representa a família de protocolos, que é quase sempre no, para classe de Internet.</span><span class="sxs-lookup"><span data-stu-id="33748-111">The third field (IN) is the class field that represents the protocol family, which is almost always IN, for Internet class.</span></span>
-   <span data-ttu-id="33748-112">O quarto campo (A) é o tipo de recurso que o RR está representando.</span><span class="sxs-lookup"><span data-stu-id="33748-112">The fourth field (A) is the type of resource the RR is representing.</span></span>
-   <span data-ttu-id="33748-113">O quinto campo (150.150.150.1) são os dados do recurso ou RDATA.</span><span class="sxs-lookup"><span data-stu-id="33748-113">The fifth field (150.150.150.1) is the resource data, or RDATA.</span></span> <span data-ttu-id="33748-114">Este campo é um tipo de variável que fornece informações apropriadas para o tipo de recurso; Nesse caso, é um endereço IP de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="33748-114">This field is a variable type that provides information appropriate for the type of resource; in this case, it's a 32-bit IP address.</span></span>

<span data-ttu-id="33748-115">Os seguintes tipos de registro de recurso são comumente usados no DNS:</span><span class="sxs-lookup"><span data-stu-id="33748-115">The following resource record types are commonly used in DNS:</span></span>

-   <span data-ttu-id="33748-116">Início de autoridade (SOA)</span><span class="sxs-lookup"><span data-stu-id="33748-116">Start of authority (SOA)</span></span>
-   <span data-ttu-id="33748-117">Servidor de nomes (NS)</span><span class="sxs-lookup"><span data-stu-id="33748-117">Name server (NS)</span></span>
-   <span data-ttu-id="33748-118">[*Registro de ponteiro*](p-gly.md) (PTR)</span><span class="sxs-lookup"><span data-stu-id="33748-118">[*Pointer record*](p-gly.md) (PTR)</span></span>
-   <span data-ttu-id="33748-119">Endereço (A)</span><span class="sxs-lookup"><span data-stu-id="33748-119">Address (A)</span></span>
-   <span data-ttu-id="33748-120">Endereço IPv6 (AAAA)</span><span class="sxs-lookup"><span data-stu-id="33748-120">IPv6 Address (AAAA)</span></span>
-   <span data-ttu-id="33748-121">Troca de email (MX)</span><span class="sxs-lookup"><span data-stu-id="33748-121">Mail exchange (MX)</span></span>
-   <span data-ttu-id="33748-122">[*Nome canônico*](c-gly.md) (CNAME)</span><span class="sxs-lookup"><span data-stu-id="33748-122">[*Canonical name*](c-gly.md) (CNAME)</span></span>
-   <span data-ttu-id="33748-123">Internet Serviço de Nomenclatura do Windows (WINS)</span><span class="sxs-lookup"><span data-stu-id="33748-123">Windows Internet Naming Service (WINS)</span></span>
-   <span data-ttu-id="33748-124">Pesquisa inversa do WINS (WINSr)</span><span class="sxs-lookup"><span data-stu-id="33748-124">WINS Reverse Look up (WINSR)</span></span>

<span data-ttu-id="33748-125">Há muitos outros tipos de registro de recurso no DNS.</span><span class="sxs-lookup"><span data-stu-id="33748-125">There are many other resource record types in DNS.</span></span> <span data-ttu-id="33748-126">Para obter mais informações, consulte [referência do provedor WMI de DNS](dns-wmi-provider-reference.md).</span><span class="sxs-lookup"><span data-stu-id="33748-126">For more information, see [DNS WMI Provider Reference](dns-wmi-provider-reference.md).</span></span>

 

 





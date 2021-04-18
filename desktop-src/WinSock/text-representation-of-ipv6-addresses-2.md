---
description: Esta seção é copiada de &\# 0034; arquitetura de endereçamento IPv6&\# 0034; por R.
ms.assetid: 52faecb9-0d7a-40fa-a021-3cc6816a4db8
title: Representação de texto de endereços IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df97c1c8933f3708fee56e34e05f918d531d2a13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105815472"
---
# <a name="text-representation-of-ipv6-addresses"></a><span data-ttu-id="bcb1f-103">Representação de texto de endereços IPv6</span><span class="sxs-lookup"><span data-stu-id="bcb1f-103">Text Representation of IPv6 Addresses</span></span>

<span data-ttu-id="bcb1f-104">Esta seção é copiada de "arquitetura de endereçamento IPv6" em R. Hinden e S. Deering.</span><span class="sxs-lookup"><span data-stu-id="bcb1f-104">This section is copied from "IPv6 Addressing Architecture" by R. Hinden and S. Deering.</span></span> <span data-ttu-id="bcb1f-105">Há três formulários convencionais para representar endereços IPv6 como cadeias de caracteres de texto:</span><span class="sxs-lookup"><span data-stu-id="bcb1f-105">There are three conventional forms for representing IPv6 addresses as text strings:</span></span>

-   <span data-ttu-id="bcb1f-106">A forma preferida é x:x: x:x: x:x: x:x, onde os ' x ' são os valores hexadecimais das partes de 8 16 bits do endereço.</span><span class="sxs-lookup"><span data-stu-id="bcb1f-106">The preferred form is x:x:x:x:x:x:x:x, where the 'x's are the hexadecimal values of the eight 16-bit pieces of the address.</span></span>

    <span data-ttu-id="bcb1f-107">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="bcb1f-107">Examples:</span></span>

    <dl> <span data-ttu-id="bcb1f-108">FEDC:BA98:7654:3210:FEDC:BA98:7654:3210</span><span class="sxs-lookup"><span data-stu-id="bcb1f-108">FEDC:BA98:7654:3210:FEDC:BA98:7654:3210</span></span>  
    <span data-ttu-id="bcb1f-109">1080:0: 0:0: 8:800:200C: 417A</span><span class="sxs-lookup"><span data-stu-id="bcb1f-109">1080:0:0:0:8:800:200C:417A</span></span>  
    </dl>

> [!Note]  
> <span data-ttu-id="bcb1f-110">Não é necessário gravar os zeros à esquerda em um campo individual, mas deve haver pelo menos um numeral em cada campo (exceto pelo caso descrito no segundo formulário).</span><span class="sxs-lookup"><span data-stu-id="bcb1f-110">It is not necessary to write the leading zeros in an individual field, but there must be at least one numeral in every field (except for the case described in the second form).</span></span>

 

-   <span data-ttu-id="bcb1f-111">Devido ao método de alocar determinados estilos de endereços IPv6, é comum que os endereços contenham cadeias de caracteres longas de zero bits.</span><span class="sxs-lookup"><span data-stu-id="bcb1f-111">Due to the method of allocating certain styles of IPv6 addresses, it is common for addresses to contain long strings of zero bits.</span></span> <span data-ttu-id="bcb1f-112">Para tornar a gravação de endereços com zero bits mais fácil, uma sintaxe especial está disponível para compactar os zeros.</span><span class="sxs-lookup"><span data-stu-id="bcb1f-112">In order to make writing addresses containing zero bits easier, a special syntax is available to compress the zeros.</span></span> <span data-ttu-id="bcb1f-113">O uso de dois-pontos duplos ("::") indica vários grupos de 16 bits de zeros.</span><span class="sxs-lookup"><span data-stu-id="bcb1f-113">The use of double colons ("::") indicates multiple groups of 16-bits of zeros.</span></span>

    <span data-ttu-id="bcb1f-114">Por exemplo, o endereço de multicast</span><span class="sxs-lookup"><span data-stu-id="bcb1f-114">For example, the multicast address</span></span>

    <dl> <span data-ttu-id="bcb1f-115">FF01:0: 0:0: 0:0: 0:43</span><span class="sxs-lookup"><span data-stu-id="bcb1f-115">FF01:0:0:0:0:0:0:43</span></span>  
    </dl>

    <span data-ttu-id="bcb1f-116">pode ser representado como:</span><span class="sxs-lookup"><span data-stu-id="bcb1f-116">may be represented as:</span></span>

    <dl> <span data-ttu-id="bcb1f-117">FF01:: 43</span><span class="sxs-lookup"><span data-stu-id="bcb1f-117">FF01::43</span></span>  
    </dl>

    <span data-ttu-id="bcb1f-118">As aspas duplas ("::") só podem aparecer uma vez em um endereço.</span><span class="sxs-lookup"><span data-stu-id="bcb1f-118">The double quotation marks ("::") can only appear once in an address.</span></span> <span data-ttu-id="bcb1f-119">Eles podem ser usados para compactar zeros à esquerda ou à direita em um endereço.</span><span class="sxs-lookup"><span data-stu-id="bcb1f-119">They can be used to compress leading or trailing zeros in an address.</span></span>

-   <span data-ttu-id="bcb1f-120">Uma forma alternativa que pode ser mais conveniente ao lidar com um ambiente misto de nós IPv4 e IPv6 é o x:x: x:x: x:x: d. d. d. d, em que os "x" são os valores hexadecimais das seis partes de 16 bits de ordem superior do endereço, e os valores decimais das quatro partes de 8 bits de ordem inferior do endereço (representação IPv4 padrão).</span><span class="sxs-lookup"><span data-stu-id="bcb1f-120">An alternative form that may be more convenient when dealing with a mixed environment of IPv4 and IPv6 nodes is x:x:x:x:x:x:d.d.d.d, where the 'x's are the hexadecimal values of the six high-order 16-bit pieces of the address, and the 'd's are the decimal values of the four low-order 8-bit pieces of the address (standard IPv4 representation).</span></span>

    <span data-ttu-id="bcb1f-121">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="bcb1f-121">Examples:</span></span>

    <dl> <span data-ttu-id="bcb1f-122">0:0: 0:0: 0:0: 13.1.68.3</span><span class="sxs-lookup"><span data-stu-id="bcb1f-122">0:0:0:0:0:0:13.1.68.3</span></span>  
    <span data-ttu-id="bcb1f-123">0:0: 0:0: 0: FFFF: 129.144.52.38</span><span class="sxs-lookup"><span data-stu-id="bcb1f-123">0:0:0:0:0:FFFF:129.144.52.38</span></span>  
    </dl>

    <span data-ttu-id="bcb1f-124">ou em formato compactado:</span><span class="sxs-lookup"><span data-stu-id="bcb1f-124">or in compressed form:</span></span>

    <dl> <span data-ttu-id="bcb1f-125">::13.1.68.3</span><span class="sxs-lookup"><span data-stu-id="bcb1f-125">::13.1.68.3</span></span>  
    <span data-ttu-id="bcb1f-126">:: FFFF: 129.144.52.38</span><span class="sxs-lookup"><span data-stu-id="bcb1f-126">::FFFF:129.144.52.38</span></span>  
    </dl>

 

 




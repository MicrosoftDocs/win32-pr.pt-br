---
title: Dicas de migração
description: É importante considerar os cálculos de endereço e a aritmética de ponteiro ao portar seu código para o Windows de 64 bits.
ms.assetid: ae562a85-d6ea-4595-b54c-0a28e6532cf5
keywords:
- Guia de programação do Windows de 64 bits-programação do Windows de 64 bits, dicas de migração
- Dicas de migração-programação do Windows de 64 bits
- compatibilidade 64-programação do Windows de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5236012b84ee880b53f8d7e50b01694181e71112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636305"
---
# <a name="migration-tips"></a><span data-ttu-id="91a14-106">Dicas de migração</span><span class="sxs-lookup"><span data-stu-id="91a14-106">Migration Tips</span></span>

<span data-ttu-id="91a14-107">As duas áreas principais de preocupação ao examinar seu código para a compatibilidade de 64 bits são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="91a14-107">The two primary areas of concern when examining your code for 64-bit compatibility are as follows:</span></span>

-   <span data-ttu-id="91a14-108">Cálculos de endereço</span><span class="sxs-lookup"><span data-stu-id="91a14-108">Address calculations</span></span>
-   <span data-ttu-id="91a14-109">Aritmética do ponteiro</span><span class="sxs-lookup"><span data-stu-id="91a14-109">Pointer arithmetic</span></span>

<span data-ttu-id="91a14-110">Por muitos motivos, os desenvolvedores armazenavam endereços como um valor **ULONG** .</span><span class="sxs-lookup"><span data-stu-id="91a14-110">For many reasons, developers have stored addresses as a **ULONG** value.</span></span> <span data-ttu-id="91a14-111">Afinal, no Windows de 32 bits, um endereço, um ponteiro e um valor **ULONG** são todos 32 bits de comprimento.</span><span class="sxs-lookup"><span data-stu-id="91a14-111">After all, on 32-bit Windows, an address, a pointer, and a **ULONG** value are all 32 bits long.</span></span> <span data-ttu-id="91a14-112">No entanto, no Windows de 64 bits, um endereço e um **ULONG** não têm o mesmo comprimento.</span><span class="sxs-lookup"><span data-stu-id="91a14-112">However, on 64-bit Windows, an address and a **ULONG** are not the same length.</span></span> <span data-ttu-id="91a14-113">Embora um **ULONG** permaneça um valor de 32 bits, todos os ponteiros agora são valores de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="91a14-113">While a **ULONG** remains a 32-bit value, all pointers are now 64-bit values.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="91a14-114">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="91a14-114">In this Section</span></span>

-   [<span data-ttu-id="91a14-115">Diretrizes gerais de portabilidade</span><span class="sxs-lookup"><span data-stu-id="91a14-115">General Porting Guidelines</span></span>](general-porting-guidelines.md)
-   [<span data-ttu-id="91a14-116">Armazenando um valor de 64 bits</span><span class="sxs-lookup"><span data-stu-id="91a14-116">Storing a 64-bit Value</span></span>](storing-a-64-bit-value.md)
-   [<span data-ttu-id="91a14-117">Erros comuns do compilador</span><span class="sxs-lookup"><span data-stu-id="91a14-117">Common Compiler Errors</span></span>](common-compiler-errors.md)
-   [<span data-ttu-id="91a14-118">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="91a14-118">Additional Considerations</span></span>](additional-considerations.md)

 

 





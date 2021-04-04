---
title: C-problemas de empacotamento do compilador
description: Os níveis de embalagem afetam o layout de memória dos tipos do MIDL e do compilador C/C++ da Microsoft da mesma forma.
ms.assetid: 029e2f68-e68f-4627-bdf0-889939d7d3c6
keywords:
- MIDL do compilador MIDL, problemas de empacotamento do compilador C
- MIDL de empacotamento
- MIDL de layout de memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c441439499d1a9b22e36c697ab6615f3292744
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823733"
---
# <a name="c-compiler-packing-issues"></a><span data-ttu-id="7e69d-106">C-problemas de empacotamento do compilador</span><span class="sxs-lookup"><span data-stu-id="7e69d-106">C-Compiler Packing Issues</span></span>

<span data-ttu-id="7e69d-107">Os níveis de embalagem afetam o layout de memória dos tipos do MIDL e do compilador C/C++ da Microsoft da mesma forma.</span><span class="sxs-lookup"><span data-stu-id="7e69d-107">Packing levels affect the memory layout of types for both MIDL and the Microsoft C/C++ compiler in the same way.</span></span> <span data-ttu-id="7e69d-108">Em ambientes do Microsoft Build, como o ambiente de compilação definido pelo VC + + ou o SDK (Kit de desenvolvimento de software) de plataforma, o nível de embalagem padrão para compiladores MIDL e C/C++ é o mesmo; o nível de embalagem padrão para os ambientes de Build do Windows de 32 bits e 64 bits é 8.</span><span class="sxs-lookup"><span data-stu-id="7e69d-108">In Microsoft build environments, such as the build environment defined by VC++ or the Platform Software Development Kit (SDK), the default packing level for MIDL and C/C++ compilers is the same; the default packing level for the 32-bit and 64-bit Windows build environments is 8.</span></span>

## <a name="natural-alignment"></a><span data-ttu-id="7e69d-109">Alinhamento natural</span><span class="sxs-lookup"><span data-stu-id="7e69d-109">Natural Alignment</span></span>

<span data-ttu-id="7e69d-110">Para tipos na memória, o alinhamento padrão é o mesmo que seu alinhamento natural.</span><span class="sxs-lookup"><span data-stu-id="7e69d-110">For types in memory, the default alignment is the same as its natural alignment.</span></span>

-   <span data-ttu-id="7e69d-111">Um tipo base, como Short, float e \_ \_ Int64, e um ponteiro é alinhado naturalmente se sua representação começa em um endereço que tem seu tamanho de módulo.</span><span class="sxs-lookup"><span data-stu-id="7e69d-111">A base type, such as short, float and \_\_int64, and a pointer is aligned naturally if its representation starts at an address that is modulo its size.</span></span> <span data-ttu-id="7e69d-112">Todos os tipos de base com suporte no momento têm tamanhos de 1, 2, 4 ou 8.</span><span class="sxs-lookup"><span data-stu-id="7e69d-112">All the currently supported base types have sizes of 1, 2, 4 or 8.</span></span> <span data-ttu-id="7e69d-113">Os ponteiros têm um tamanho de 4 em ambientes de 32 bits e 8 em ambientes de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7e69d-113">Pointers have a size of 4 in 32-bit environments and 8 in 64-bit environments.</span></span>
-   <span data-ttu-id="7e69d-114">Um tipo composto é alinhado naturalmente se cada um de seus componentes está alinhado naturalmente em relação ao início do tipo e se não há lacunas desnecessárias (preenchimento) entre os componentes.</span><span class="sxs-lookup"><span data-stu-id="7e69d-114">A compound type is aligned naturally if each of its components is aligned naturally relative to the beginning of the type, and if there are no unnecessary gaps (padding) between components.</span></span> <span data-ttu-id="7e69d-115">Componentes compostos, como campos ou elementos, são recursivamente para componentes de tipo de ponteiro ou de base.</span><span class="sxs-lookup"><span data-stu-id="7e69d-115">Compound components, such as fields or elements, are recursed to pointer or base type components.</span></span>

<span data-ttu-id="7e69d-116">Uma regra simples para ajudar a lembrar esse comportamento é que o alinhamento natural de um tipo é igual aos maiores alinhamentos de seus componentes.</span><span class="sxs-lookup"><span data-stu-id="7e69d-116">A simple rule to help remember this behavior is that the natural alignment of a type is equal to the biggest alignments of its components.</span></span>

<span data-ttu-id="7e69d-117">Há uma conexão entre o alinhamento e o tamanho da memória de um tipo em linguagens como C ou C++ e IDL, conforme expresso pelo operador **sizeof ()**.</span><span class="sxs-lookup"><span data-stu-id="7e69d-117">There is a connection between alignment and memory size of a type in languages like C or C++ and IDL as expressed by the operator **sizeof()**.</span></span> <span data-ttu-id="7e69d-118">O tamanho é um múltiplo do alinhamento (o mínimo varia de abrangência do tipo).</span><span class="sxs-lookup"><span data-stu-id="7e69d-118">The size is a multiple of the alignment (the minimal multiple spanning the type).</span></span> <span data-ttu-id="7e69d-119">Isso segue de uma representação de matriz na memória.</span><span class="sxs-lookup"><span data-stu-id="7e69d-119">This follows from an array representation in memory.</span></span>

<span data-ttu-id="7e69d-120">O alinhamento natural é importante porque o acesso a dados desalinhados pode causar uma exceção em alguns sistemas.</span><span class="sxs-lookup"><span data-stu-id="7e69d-120">Natural alignment is important because accessing misaligned data may cause an exception on some systems.</span></span> <span data-ttu-id="7e69d-121">Os dados podem ser marcados para uma manipulação segura quando desalinhados, mas normalmente isso envolve uma penalidade de velocidade que pode ser substancial em algumas plataformas.</span><span class="sxs-lookup"><span data-stu-id="7e69d-121">Data can be marked for a safe manipulation when misaligned, but typically that involves a speed penalty that may be substantial on some platforms.</span></span>

> [!Note]  
> <span data-ttu-id="7e69d-122">Na memória, os objetos de tipos com um alinhamento natural de *n* são garantidos para serem alinhados corretamente quando colocados em endereços que são múltiplos de *n*.</span><span class="sxs-lookup"><span data-stu-id="7e69d-122">In memory, objects of types with a natural alignment of *n* are guaranteed to be aligned properly when placed at addresses that are a multiple of *n*.</span></span>

 

## <a name="packing-versus-alignment"></a><span data-ttu-id="7e69d-123">Empacotamento versus alinhamento</span><span class="sxs-lookup"><span data-stu-id="7e69d-123">Packing versus Alignment</span></span>

<span data-ttu-id="7e69d-124">A especificação de um nível de embalagem maior do que o alinhamento natural de um tipo não altera o alinhamento do tipo.</span><span class="sxs-lookup"><span data-stu-id="7e69d-124">Specifying a packing level larger than the natural alignment of a type does not change the type alignment.</span></span> <span data-ttu-id="7e69d-125">A especificação de um nível de embalagem menor do que o alinhamento natural reduz o alinhamento de tipo ao nível de embalagem.</span><span class="sxs-lookup"><span data-stu-id="7e69d-125">Specifying a packing level smaller than the natural alignment reduces the type alignment to the packing level.</span></span> <span data-ttu-id="7e69d-126">Como resultado, os tipos empacotados podem ser colocados na memória em endereços que são um múltiplo do nível de embalagem (o alinhamento reduzido) sem causar um desalinhamento.</span><span class="sxs-lookup"><span data-stu-id="7e69d-126">As a result, the packed types may be placed in memory at addresses that are a multiple of the packing level (the reduced alignment) without causing a misalignment.</span></span> <span data-ttu-id="7e69d-127">Isso afeta os tipos simples e os tipos de componentes.</span><span class="sxs-lookup"><span data-stu-id="7e69d-127">This affects both simple types and component types.</span></span> <span data-ttu-id="7e69d-128">Para tipos compostos, o layout interno do tipo pode ser afetado, pois o alinhamento reduzido dos componentes pode alterar o tamanho do preenchimento necessário para o alinhamento adequado dos componentes, reduzindo assim o tamanho do tipo.</span><span class="sxs-lookup"><span data-stu-id="7e69d-128">For compound types, the internal layout of the type may be affected, because the reduced alignment of the components may change the size of padding necessary for the proper alignment of the components, thus reducing the size of the type.</span></span>

<span data-ttu-id="7e69d-129">Uma regra simples para ajudar a lembrar esse comportamento é que o novo alinhamento de um tipo empacotado é menor do que o nível de embalagem e seu alinhamento natural.</span><span class="sxs-lookup"><span data-stu-id="7e69d-129">A simple rule to help remember this behavior is that the new alignment of a packed type is the smaller of the packing level and its natural alignment.</span></span> <span data-ttu-id="7e69d-130">O tamanho do tipo é um múltiplo do novo alinhamento.</span><span class="sxs-lookup"><span data-stu-id="7e69d-130">The size of the type is a multiple of the new alignment.</span></span> <span data-ttu-id="7e69d-131">O operador **sizeof ()** retorna o tamanho reduzido para os tipos empacotados.</span><span class="sxs-lookup"><span data-stu-id="7e69d-131">The **sizeof()** operator returns the reduced size for packed types.</span></span>

<span data-ttu-id="7e69d-132">Por exemplo, com o nível de embalagem 2, um longo torna-se alinhado a 2 e, portanto, pode ser colocado em qualquer endereço par, não apenas nos endereços que são um múltiplo de 4, como seria o caso com alinhamento natural.</span><span class="sxs-lookup"><span data-stu-id="7e69d-132">For example, with packing level 2 a long becomes aligned at 2, and therefore may be placed at any even address, not only at the addresses that are a multiple of 4 as would be the case with natural alignment.</span></span> <span data-ttu-id="7e69d-133">Uma estrutura com um curto e um longo, empacotada em 2, não precisa da lacuna interna entre o curto e o seguinte que era necessário para o alinhamento natural; Portanto, não só a estrutura agora está alinhada a 2; ela também tem seu tamanho reduzido de 8 para 6.</span><span class="sxs-lookup"><span data-stu-id="7e69d-133">A structure with a short and a long, packed at 2, does not need the internal gap between the short and the following long that was necessary for the natural alignment; hence, not only is the structure now aligned at 2, it also has its size reduced from 8 to 6.</span></span>

<span data-ttu-id="7e69d-134">Como exemplo, considere um tipo composto que consiste em um caractere de 1 byte, um inteiro de 4 bytes e um caractere de 1 byte:</span><span class="sxs-lookup"><span data-stu-id="7e69d-134">As an example, consider a compound type consisting of a 1-byte character, an integer 4 bytes long, and a 1-byte character:</span></span>

``` syntax
struct mystructtype 
{    
    char c1;  /* requires 1 byte  */
              /* 3 bytes of padding with natural alignment only */
    long l2;  /* requires 4 bytes */
    char c3;  /* requires 1 byte  */
              /* 3 bytes of padding with natural alignment only */
 } mystruct;
```

<span data-ttu-id="7e69d-135">Essa estrutura está naturalmente alinhada a 4 e tem o tamanho natural de 12.</span><span class="sxs-lookup"><span data-stu-id="7e69d-135">This structure is naturally aligned at 4 and has the natural size of 12.</span></span>

<span data-ttu-id="7e69d-136">Para o nível de embalagem 4 ou superior, a estrutura **MyStruct** é alinhada a 4 e `sizeof(struct mystructtype)` é igual a 12.</span><span class="sxs-lookup"><span data-stu-id="7e69d-136">For packing level 4 or greater, the structure **mystruct** is aligned at 4 and `sizeof(struct mystructtype)` is equal to 12.</span></span> <span data-ttu-id="7e69d-137">A estrutura será desalinhada se estiver localizada na memória em um endereço que não seja um múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="7e69d-137">The structure will be misaligned if located in memory at an address that is not a multiple of 4.</span></span>

<span data-ttu-id="7e69d-138">Para o nível de embalagem 2, a estrutura é alinhada em 2 e seu tamanho é 8.</span><span class="sxs-lookup"><span data-stu-id="7e69d-138">For packing level 2, the structure is aligned at 2 and its size is 8.</span></span> <span data-ttu-id="7e69d-139">A estrutura empacotada com nível 2 será desalinhada se estiver localizada na memória em um endereço que não seja um múltiplo de 2.</span><span class="sxs-lookup"><span data-stu-id="7e69d-139">The structure packed with level 2 will be misaligned if located in memory at an address that is not a multiple of 2.</span></span>

<span data-ttu-id="7e69d-140">Para o nível de embalagem 1, a estrutura é alinhada em 1 e seu tamanho é 6.</span><span class="sxs-lookup"><span data-stu-id="7e69d-140">For packing level 1, the structure is aligned at 1 and its size is 6.</span></span> <span data-ttu-id="7e69d-141">A estrutura empacotada com o nível 1 pode ser colocada em qualquer lugar sem causar uma falha de alinhamento incorreto.</span><span class="sxs-lookup"><span data-stu-id="7e69d-141">The structure packed with level 1 can be placed anywhere without causing a misalignment fault.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e69d-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7e69d-142">Related topics</span></span>

<dl> <span data-ttu-id="7e69d-143"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="7e69d-143"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="7e69d-144">/ZP</span><span class="sxs-lookup"><span data-stu-id="7e69d-144">/Zp</span></span>](./-zp.md)
</dt> <dt>

[<span data-ttu-id="7e69d-145">/Pack</span><span class="sxs-lookup"><span data-stu-id="7e69d-145">/pack</span></span>](./-pack.md)
</dt> </dl>

 

 
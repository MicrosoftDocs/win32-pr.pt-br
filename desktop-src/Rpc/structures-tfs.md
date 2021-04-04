---
title: Estruturas (RPC)
description: Descrição de vários tipos de estruturas na RPC (chamada de procedimento remoto).
ms.assetid: edaf547d-d3d1-443c-93dd-8e036bc42944
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ccae91f703badd2e0153dfc3d8acff1ace562f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007893"
---
# <a name="structures-rpc"></a><span data-ttu-id="3c14d-103">Estruturas (RPC)</span><span class="sxs-lookup"><span data-stu-id="3c14d-103">Structures (RPC)</span></span>

<span data-ttu-id="3c14d-104">Há várias categorias de estruturas, progressivamente mais complicadas em termos de ações necessárias para o marshaling.</span><span class="sxs-lookup"><span data-stu-id="3c14d-104">There are several categories of structures, progressively more complicated in terms of actions required for marshaling.</span></span> <span data-ttu-id="3c14d-105">Eles começam com uma estrutura simples que pode ser copiada em bloco como um todo e continuam em uma estrutura complexa que deve ser atendida em campo por campo.</span><span class="sxs-lookup"><span data-stu-id="3c14d-105">They begin with a simple structure that can be block-copied as a whole, and continue to a complex structure that has to be serviced field by field.</span></span>

-   [<span data-ttu-id="3c14d-106">Estrutura simples</span><span class="sxs-lookup"><span data-stu-id="3c14d-106">Simple Structure</span></span>](#simple-structure)
-   [<span data-ttu-id="3c14d-107">Estrutura simples com ponteiros</span><span class="sxs-lookup"><span data-stu-id="3c14d-107">Simple Structure with Pointers</span></span>](#simple-structure-with-pointers)
-   [<span data-ttu-id="3c14d-108">Estrutura de conformidade</span><span class="sxs-lookup"><span data-stu-id="3c14d-108">Conformant Structure</span></span>](#conformant-structure)
-   [<span data-ttu-id="3c14d-109">Estrutura compatível com ponteiros</span><span class="sxs-lookup"><span data-stu-id="3c14d-109">Conformant Structure with Pointers</span></span>](#conformant-structure-with-pointers)
-   [<span data-ttu-id="3c14d-110">Estrutura variável em conformidade (com ou sem ponteiros)</span><span class="sxs-lookup"><span data-stu-id="3c14d-110">Conformant Varying Structure (with or without Pointers)</span></span>](#conformant-varying-structure-with-or-without-pointers)
-   [<span data-ttu-id="3c14d-111">Estrutura rígida</span><span class="sxs-lookup"><span data-stu-id="3c14d-111">Hard Structure</span></span>](#hard-structure)
-   [<span data-ttu-id="3c14d-112">Estrutura complexa</span><span class="sxs-lookup"><span data-stu-id="3c14d-112">Complex Structure</span></span>](#complex-structure)
-   [<span data-ttu-id="3c14d-113">Descrição do layout do membro da estrutura</span><span class="sxs-lookup"><span data-stu-id="3c14d-113">Structure Member Layout Description</span></span>](#structure-member-layout-description)

> [!Note]  
> <span data-ttu-id="3c14d-114">Quando comparada às categorias de matriz, fica claro que apenas estruturas de até 64K podem ser descritas (o tamanho é para a parte plana da estrutura), ou seja, não há equivalente a matrizes SM e LG.</span><span class="sxs-lookup"><span data-stu-id="3c14d-114">When compared to array categories, it becomes clear that only structures up to 64k in size can be described (the size is for the flat part of the structure), that is there is no equivalent of SM and LG arrays.</span></span>

 

<span data-ttu-id="3c14d-115">**Membros comuns a estruturas**</span><span class="sxs-lookup"><span data-stu-id="3c14d-115">**Members Common to Structures**</span></span>

-   <span data-ttu-id="3c14d-116">**sintonia**</span><span class="sxs-lookup"><span data-stu-id="3c14d-116">**alignment**</span></span>

    <span data-ttu-id="3c14d-117">O alinhamento necessário do buffer antes de desempacotar a estrutura.</span><span class="sxs-lookup"><span data-stu-id="3c14d-117">The necessary alignment of the buffer before unmarshaling the structure.</span></span> <span data-ttu-id="3c14d-118">Os valores válidos são 0, 1, 3 e 7 (o alinhamento real menos 1).</span><span class="sxs-lookup"><span data-stu-id="3c14d-118">Valid values are 0, 1, 3, and 7 (the actual alignment minus 1).</span></span>

-   <span data-ttu-id="3c14d-119">**tamanho da memória \_**</span><span class="sxs-lookup"><span data-stu-id="3c14d-119">**memory\_size**</span></span>

    <span data-ttu-id="3c14d-120">Tamanho da estrutura na memória em bytes; para estruturas em conformidade, esse tamanho não inclui o tamanho da matriz.</span><span class="sxs-lookup"><span data-stu-id="3c14d-120">Size of the structure in memory in bytes; for conformant structures this size does not include the array's size.</span></span>

-   <span data-ttu-id="3c14d-121">**deslocamento \_ da \_ Descrição da matriz \_**</span><span class="sxs-lookup"><span data-stu-id="3c14d-121">**offset\_to\_array\_description**</span></span>

    <span data-ttu-id="3c14d-122">Deslocamento do ponteiro da cadeia de caracteres de formato atual para a descrição da matriz em conformidade contida em uma estrutura.</span><span class="sxs-lookup"><span data-stu-id="3c14d-122">Offset from the current format string pointer to the description of the conformant array contained in a structure.</span></span>

-   <span data-ttu-id="3c14d-123">**layout do membro \_**</span><span class="sxs-lookup"><span data-stu-id="3c14d-123">**member\_layout**</span></span>

    <span data-ttu-id="3c14d-124">Descrição de cada elemento da estrutura.</span><span class="sxs-lookup"><span data-stu-id="3c14d-124">Description of each element of the structure.</span></span> <span data-ttu-id="3c14d-125">As rotinas de NDR só precisam examinar essa parte da cadeia de caracteres de formato de um tipo se a transformação endian for necessária ou se o tipo for uma estrutura complexa.</span><span class="sxs-lookup"><span data-stu-id="3c14d-125">The NDR routines only need to examine this portion of a type's format string if endian transformation is needed or if the type is a complex structure.</span></span>

-   <span data-ttu-id="3c14d-126">**layout do ponteiro \_**</span><span class="sxs-lookup"><span data-stu-id="3c14d-126">**pointer\_layout**</span></span>

    <span data-ttu-id="3c14d-127">Consulte a seção [layout do ponteiro](pointer-layout-tfs.md) .</span><span class="sxs-lookup"><span data-stu-id="3c14d-127">See the [Pointer Layout](pointer-layout-tfs.md) section.</span></span>

## <a name="simple-structure"></a><span data-ttu-id="3c14d-128">Estrutura simples</span><span class="sxs-lookup"><span data-stu-id="3c14d-128">Simple Structure</span></span>

<span data-ttu-id="3c14d-129">Uma estrutura simples contém apenas tipos base, matrizes fixas e outras estruturas simples.</span><span class="sxs-lookup"><span data-stu-id="3c14d-129">A simple structure contains only base types, fixed arrays, and other simple structures.</span></span> <span data-ttu-id="3c14d-130">O principal recurso da estrutura simples é que ele pode ser copiado em bloco como um todo.</span><span class="sxs-lookup"><span data-stu-id="3c14d-130">The main feature of the simple structure is that it can be block-copied as a whole.</span></span>

``` syntax
FC_STRUCT alignment<1> 
memory_size<2> 
member_layout<> 
FC_END
```

## <a name="simple-structure-with-pointers"></a><span data-ttu-id="3c14d-131">Estrutura simples com ponteiros</span><span class="sxs-lookup"><span data-stu-id="3c14d-131">Simple Structure with Pointers</span></span>

<span data-ttu-id="3c14d-132">Uma estrutura simples com ponteiros contém apenas tipos base, ponteiros, matrizes fixas, estruturas simples e outras estruturas simples com ponteiros.</span><span class="sxs-lookup"><span data-stu-id="3c14d-132">A simple structure with pointers contains only base types, pointers, fixed arrays, simple structures, and other simple structures with pointers.</span></span> <span data-ttu-id="3c14d-133">Como o layout<> só precisará ser visitado ao fazer uma conversão endianess, ele será colocado no final da descrição.</span><span class="sxs-lookup"><span data-stu-id="3c14d-133">Because the layout<> will only have to be visited when doing an endianess conversion, it is placed at the end of the description.</span></span>

``` syntax
FC_PSTRUCT alignment<1> 
memory_size<2> 
pointer_layout<> 
member_layout<> 
FC_END
```

## <a name="conformant-structure"></a><span data-ttu-id="3c14d-134">Estrutura de conformidade</span><span class="sxs-lookup"><span data-stu-id="3c14d-134">Conformant Structure</span></span>

<span data-ttu-id="3c14d-135">Uma estrutura compatível contém apenas tipos base, matrizes fixas e estruturas simples e deve conter uma cadeia de caracteres de conformidade ou uma matriz compatível.</span><span class="sxs-lookup"><span data-stu-id="3c14d-135">A conformant structure contains only base types, fixed arrays, and simple structures, and must contain either a conformant string or a conformant array.</span></span> <span data-ttu-id="3c14d-136">Essa matriz pode realmente estar contida em outra estrutura compatível ou estrutura de conformidade com ponteiros que são inseridos nessa estrutura.</span><span class="sxs-lookup"><span data-stu-id="3c14d-136">This array could actually be contained in another conformant structure or conformant structure with pointers which is embedded in this structure.</span></span>

``` syntax
FC_CSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
member_layout<> 
FC_END
```

## <a name="conformant-structure-with-pointers"></a><span data-ttu-id="3c14d-137">Estrutura compatível com ponteiros</span><span class="sxs-lookup"><span data-stu-id="3c14d-137">Conformant Structure with Pointers</span></span>

<span data-ttu-id="3c14d-138">Uma estrutura compatível com ponteiros contém apenas tipos base, ponteiros, matrizes fixas, estruturas simples e estruturas simples com ponteiros; uma estrutura compatível deve conter uma matriz compatível.</span><span class="sxs-lookup"><span data-stu-id="3c14d-138">A conformant structure with pointers contains only base types, pointers, fixed arrays, simple structures, and simple structures with pointers; a conformant structure must contain a conformant array.</span></span> <span data-ttu-id="3c14d-139">Essa matriz pode realmente estar contida em outra estrutura compatível ou estrutura de conformidade com ponteiros inseridos nessa estrutura.</span><span class="sxs-lookup"><span data-stu-id="3c14d-139">This array could actually be contained in another conformant structure or conformant structure with pointers that is embedded in this structure.</span></span>

``` syntax
FC_CPSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
pointer_layout<> 
member_layout<> FC_END
```

## <a name="conformant-varying-structure-with-or-without-pointers"></a><span data-ttu-id="3c14d-140">Estrutura variável em conformidade (com ou sem ponteiros)</span><span class="sxs-lookup"><span data-stu-id="3c14d-140">Conformant Varying Structure (with or without Pointers)</span></span>

<span data-ttu-id="3c14d-141">Uma estrutura de variação em conformidade contém apenas tipos simples, ponteiros, matrizes fixas, estruturas simples e estruturas simples com ponteiros; uma estrutura de variação em conformidade deve conter uma cadeia de caracteres de conformidade ou uma matriz de variação variável.</span><span class="sxs-lookup"><span data-stu-id="3c14d-141">A conformant varying structure contains only simple types, pointers, fixed arrays, simple structures, and simple structures with pointers; a conformant varying structure must contain either a conformant string or a conformant-varying array.</span></span> <span data-ttu-id="3c14d-142">A cadeia de caracteres de conformidade ou a matriz pode realmente estar contida em outra estrutura compatível ou estrutura de conformidade com ponteiros inseridos nessa estrutura.</span><span class="sxs-lookup"><span data-stu-id="3c14d-142">The conformant string or array can actually be contained in another conformant structure or conformant structure with pointers that is embedded in this structure.</span></span>

``` syntax
FC_CVSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
[pointer_layout<>] 
layout<> 
FC_END
```

## <a name="hard-structure"></a><span data-ttu-id="3c14d-143">Estrutura rígida</span><span class="sxs-lookup"><span data-stu-id="3c14d-143">Hard Structure</span></span>

<span data-ttu-id="3c14d-144">A estrutura sólida era um conceito destinado à eliminação de penalidades acentuadas relacionadas ao processamento de estruturas complexas.</span><span class="sxs-lookup"><span data-stu-id="3c14d-144">The hard structure was a concept aimed at eliminating steep penalties related to processing complex structures.</span></span> <span data-ttu-id="3c14d-145">Ele é derivado de uma observação de que uma estrutura complexa normalmente tem apenas uma ou duas condições que impedem a cópia de bloco e, portanto, estragam seu desempenho em comparação com uma estrutura simples.</span><span class="sxs-lookup"><span data-stu-id="3c14d-145">It is derived from an observation that a complex structure typically has only one or two conditions that prevent block-copying, and therefore spoil its performance compared to a simple structure.</span></span> <span data-ttu-id="3c14d-146">Os culpados geralmente são campos de União ou de enumeração.</span><span class="sxs-lookup"><span data-stu-id="3c14d-146">The culprits are usually unions or enumeration fields.</span></span>

<span data-ttu-id="3c14d-147">Uma estrutura rígida é uma estrutura que tem um enum16, um preenchimento de extremidade na memória ou uma União como o último membro.</span><span class="sxs-lookup"><span data-stu-id="3c14d-147">A hard structure is a structure that has an enum16, end-padding in memory, or a union as the last member.</span></span> <span data-ttu-id="3c14d-148">Esses três elementos impedem que a estrutura caia em uma das categorias de estrutura anteriores, o que aproveita sobrecarga de interpretação pequena e potencial máximo de otimização, mas não a força na categoria de estrutura complexa muito dispendiosa.</span><span class="sxs-lookup"><span data-stu-id="3c14d-148">These three elements prevent the structure from falling into one of the previous structure categories, which enjoy small interpretation overhead and maximum optimization potential, but do not force it into the very costly complex structure category.</span></span>

<span data-ttu-id="3c14d-149">O enum16 não deve fazer com que a memória e os tamanhos de conexão da estrutura sejam diferentes.</span><span class="sxs-lookup"><span data-stu-id="3c14d-149">The enum16 must not cause the memory and wire sizes of the structure to differ.</span></span> <span data-ttu-id="3c14d-150">A estrutura não pode ter nenhuma matriz compatível nem ponteiros (a menos que parte da União); os únicos outros membros permitidos são tipos base, matrizes fixas e estruturas simples.</span><span class="sxs-lookup"><span data-stu-id="3c14d-150">The structure cannot have any conformant array, nor any pointers (unless part of the union); the only other members allowed are base types, fixed arrays, and simple structures.</span></span>

``` syntax
FC_HARD_STRUCTURE alignment<1> 
memory_size<2> 
reserved<4> 
enum_offset<2> 
copy_size<2> 
mem_copy_incr<2> 
union_description_offset<2>
member_layout<> 
FC_END
```

<span data-ttu-id="3c14d-151">O \_ campo deslocamento de enumeração<2> fornece o deslocamento do início da estrutura na memória para um enum16 se ele contiver um; caso contrário, o campo de deslocamento de enumeração \_<2> será – 1.</span><span class="sxs-lookup"><span data-stu-id="3c14d-151">The enum\_offset<2> field provides the offset from the beginning of the structure in memory to an enum16 if it contains one; otherwise the enum\_offset<2> field is –1.</span></span>

<span data-ttu-id="3c14d-152">O \_ campo tamanho da cópia<2> fornece o número total de bytes na estrutura, que podem ser copiados em bloco em/do buffer.</span><span class="sxs-lookup"><span data-stu-id="3c14d-152">The copy\_size<2> field provides the total number of bytes in the structure, which may be block-copied into/from the buffer.</span></span> <span data-ttu-id="3c14d-153">Esse total não inclui nenhuma União à direita nem qualquer preenchimento de extremidade na memória.</span><span class="sxs-lookup"><span data-stu-id="3c14d-153">This total does not include any trailing union nor any end-padding in memory.</span></span> <span data-ttu-id="3c14d-154">Esse valor também é a quantidade que o ponteiro de buffer deve ser incrementado após a cópia.</span><span class="sxs-lookup"><span data-stu-id="3c14d-154">This value is also the amount the buffer pointer should be incremented following the copy.</span></span>

<span data-ttu-id="3c14d-155">O \_ campo incr de cópia do mem \_<2> é o número de bytes que o ponteiro de memória deve ser incrementado após a cópia de bloco antes de manipular qualquer União à direita.</span><span class="sxs-lookup"><span data-stu-id="3c14d-155">The mem\_copy\_incr<2> field is the number of bytes the memory pointer should be incremented following the block-copy before handling any trailing union.</span></span> <span data-ttu-id="3c14d-156">Incrementar por esse valor (não pelo tamanho da cópia \_<2> bytes) produz um ponteiro de memória adequado para qualquer União à direita.</span><span class="sxs-lookup"><span data-stu-id="3c14d-156">Incrementing by this amount (not by copy\_size<2> bytes) yields a proper memory pointer to any trailing union.</span></span>

## <a name="complex-structure"></a><span data-ttu-id="3c14d-157">Estrutura complexa</span><span class="sxs-lookup"><span data-stu-id="3c14d-157">Complex Structure</span></span>

<span data-ttu-id="3c14d-158">Uma estrutura complexa é qualquer estrutura que contenha um ou mais campos que impeçam que a estrutura seja copiada em bloco ou para a qual verificação adicional deve ser executada durante o marshaling ou o desempacotamento (por exemplo, verificações associadas em uma enumeração).</span><span class="sxs-lookup"><span data-stu-id="3c14d-158">A complex structure is any structure containing one or more fields that either prevent the structure from being block-copied, or for which additional checking must be performed during marshaling or unmarshaling (for example, bound checks on an enumeration).</span></span> <span data-ttu-id="3c14d-159">Os seguintes tipos de NDR estão nesta categoria:</span><span class="sxs-lookup"><span data-stu-id="3c14d-159">The following NDR types fall in this category:</span></span>

-   <span data-ttu-id="3c14d-160">[tipos simples](simple-types-tfs.md): ENUM16, \_ \_ INT3264 (somente em plataformas de 64 bits), um integral com \[ [ **intervalo**](/windows/desktop/Midl/range)\]</span><span class="sxs-lookup"><span data-stu-id="3c14d-160">[simple types](simple-types-tfs.md): ENUM16, \_\_INT3264 (on 64-bit platforms only), an integral with \[[**range**](/windows/desktop/Midl/range)\]</span></span>
-   <span data-ttu-id="3c14d-161">preenchimento de alinhamento no final da estrutura</span><span class="sxs-lookup"><span data-stu-id="3c14d-161">alignment padding at the end of the structure</span></span>
-   <span data-ttu-id="3c14d-162">ponteiros de interface (eles vão usar um complexo incorporado)</span><span class="sxs-lookup"><span data-stu-id="3c14d-162">interface pointers (they go using an embedded complex)</span></span>
-   <span data-ttu-id="3c14d-163">ponteiros ignorados (relacionados ao \[ atributo [**ignore**](/windows/desktop/Midl/ignore) \] e ao \_ token de ignorar FC)</span><span class="sxs-lookup"><span data-stu-id="3c14d-163">ignored pointers (that is related to \[[**ignore**](/windows/desktop/Midl/ignore)\] attribute and FC\_IGNORE token)</span></span>
-   <span data-ttu-id="3c14d-164">matrizes complexas, matrizes variáveis, matrizes de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="3c14d-164">complex arrays, varying arrays, string arrays</span></span>
-   <span data-ttu-id="3c14d-165">matrizes de conformidade multidimensional com pelo menos uma dimensão não fixa</span><span class="sxs-lookup"><span data-stu-id="3c14d-165">multidimensional conformant arrays with at least one nonfixed dimension</span></span>
-   <span data-ttu-id="3c14d-166">uniões</span><span class="sxs-lookup"><span data-stu-id="3c14d-166">unions</span></span>
-   <span data-ttu-id="3c14d-167">elementos definidos com \[ [**transmitir \_ como**](/windows/desktop/Midl/transmit-as) \] , \[ [**representar \_ como**](/windows/desktop/Midl/represent-as) \] , \[ [**\_ empacotamento de conexão**](/windows/desktop/Midl/wire-marshal) \] , \[ [**\_ Marshal do usuário**](/windows/desktop/Midl/user-marshal)\]</span><span class="sxs-lookup"><span data-stu-id="3c14d-167">elements defined with \[[**transmit\_as**](/windows/desktop/Midl/transmit-as)\], \[[**represent\_as**](/windows/desktop/Midl/represent-as)\], \[[**wire\_marshal**](/windows/desktop/Midl/wire-marshal)\], \[[**user\_marshal**](/windows/desktop/Midl/user-marshal)\]</span></span>
-   <span data-ttu-id="3c14d-168">estruturas complexas inseridas</span><span class="sxs-lookup"><span data-stu-id="3c14d-168">embedded complex structures</span></span>
-   <span data-ttu-id="3c14d-169">preenchimento no final da estrutura</span><span class="sxs-lookup"><span data-stu-id="3c14d-169">padding at the end of the structure</span></span>

<span data-ttu-id="3c14d-170">Uma estrutura complexa tem a seguinte descrição de formato:</span><span class="sxs-lookup"><span data-stu-id="3c14d-170">A complex structure has the following format description:</span></span>

``` syntax
FC_BOGUS_STRUCT alignment<1> 
memory_size<2> 
offset_to_conformant_array_description<2> 
offset_to_pointer_layout<2> 
member_layout<> 
FC_END 
[pointer_layout<>]
```

<span data-ttu-id="3c14d-171">O tamanho da memória \_<2> campo é o tamanho da estrutura na memória, em bytes.</span><span class="sxs-lookup"><span data-stu-id="3c14d-171">The memory\_size<2> field is the size of the structure in memory, in bytes.</span></span>

<span data-ttu-id="3c14d-172">Se a estrutura contiver uma matriz em conformidade, a \_ Descrição da matriz de acordo com o \_ \_ \_<2> campo fornecerá o deslocamento para a descrição da matriz em conformidade, caso contrário, será zero.</span><span class="sxs-lookup"><span data-stu-id="3c14d-172">If the structure contains a conformant array, the offset\_to\_conformant\_array\_description<2> field provides the offset to the conformant array's description, otherwise it is zero.</span></span>

<span data-ttu-id="3c14d-173">Se a estrutura tiver ponteiros, o deslocamento \_ para o \_ \_ layout do ponteiro<2> campo fornecerá o deslocamento além do layout da estrutura para o layout do ponteiro, caso contrário, esse campo será zero.</span><span class="sxs-lookup"><span data-stu-id="3c14d-173">If the structure has pointers, the offset\_to\_pointer\_layout<2> field provides the offset past the structure's layout to the pointer layout, otherwise this field is zero.</span></span>

<span data-ttu-id="3c14d-174">O \_ layout do ponteiro<> campo de uma estrutura complexa é tratado de maneira um pouco diferente do que para outras estruturas.</span><span class="sxs-lookup"><span data-stu-id="3c14d-174">The pointer\_layout<> field of a complex structure is handled somewhat differently than for other structures.</span></span> <span data-ttu-id="3c14d-175">O layout do ponteiro \_<> campo de uma estrutura complexa só contém descrições dos campos de ponteiro reais na própria estrutura.</span><span class="sxs-lookup"><span data-stu-id="3c14d-175">The pointer\_layout<> field of a complex structure only contains descriptions of actual pointer fields in the structure itself.</span></span> <span data-ttu-id="3c14d-176">Todos os ponteiros contidos em quaisquer matrizes, uniões ou estruturas incorporadas não são descritos no campo<> layout de ponteiro da estrutura complexa \_ .</span><span class="sxs-lookup"><span data-stu-id="3c14d-176">Any pointers contained within any embedded arrays, unions, or structures are not described in the complex structure's pointer\_layout<> field.</span></span>

> [!Note]  
> <span data-ttu-id="3c14d-177">Isso é diferente de outras estruturas, que duplicam a descrição de quaisquer ponteiros contidos em matrizes ou estruturas inseridas em seu próprio layout de ponteiro \_<> campo também.</span><span class="sxs-lookup"><span data-stu-id="3c14d-177">This is in contrast to other structures, which duplicate the description of any pointers contained in embedded arrays or structures in their own pointer \_layout<> field as well.</span></span>

 

<span data-ttu-id="3c14d-178">O formato de um layout de ponteiro de estrutura complexa também é radicalmente diferente.</span><span class="sxs-lookup"><span data-stu-id="3c14d-178">The format of a complex structure's pointer layout is also radically different.</span></span> <span data-ttu-id="3c14d-179">Como ele contém apenas descrições de membros reais de ponteiro e porque uma estrutura complexa é empacotada e não empacotada um campo por vez, o layout do ponteiro \_<> campo simplesmente contém a descrição do ponteiro de todos os membros do ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3c14d-179">Because it only contains descriptions of actual pointer members and because a complex structure is marshaled and unmarshaled one field at a time, the pointer\_layout<> field simply contains the pointer description of all pointer members.</span></span> <span data-ttu-id="3c14d-180">Não há um FC \_ PP inicial e nenhum dos layouts de ponteiro usuais \_<> informações.</span><span class="sxs-lookup"><span data-stu-id="3c14d-180">There is no beginning FC\_PP, and none of the usual pointer\_layout<> information.</span></span>

## <a name="structure-member-layout-description"></a><span data-ttu-id="3c14d-181">Descrição do layout do membro da estrutura</span><span class="sxs-lookup"><span data-stu-id="3c14d-181">Structure Member Layout Description</span></span>

<span data-ttu-id="3c14d-182">A descrição do layout de uma estrutura contém um ou mais dos seguintes caracteres de formato:</span><span class="sxs-lookup"><span data-stu-id="3c14d-182">A structure's layout description contains one or more of the following format characters:</span></span>

-   <span data-ttu-id="3c14d-183">Qualquer um dos caracteres de tipo base, como FC \_ Char e assim por diante</span><span class="sxs-lookup"><span data-stu-id="3c14d-183">Any of the base type characters, like FC\_CHAR, and so on</span></span>
-   <span data-ttu-id="3c14d-184">Diretivas de alinhamento.</span><span class="sxs-lookup"><span data-stu-id="3c14d-184">Alignment directives.</span></span> <span data-ttu-id="3c14d-185">Há três caracteres de formato que especificam o alinhamento do ponteiro de memória: FC \_ ALIGNM2, FC \_ ALIGNM4 e FC \_ ALIGNM8.</span><span class="sxs-lookup"><span data-stu-id="3c14d-185">There are three format characters specifying alignment of the memory pointer: FC\_ALIGNM2, FC\_ALIGNM4, and FC\_ALIGNM8.</span></span>
    > [!Note]  
    > <span data-ttu-id="3c14d-186">Também há tokens de alinhamento de buffer, FC \_ ALIGNB2 por meio de \_ ALIGNM8 FC; eles não são usados.</span><span class="sxs-lookup"><span data-stu-id="3c14d-186">There are also buffer alignment tokens, FC\_ALIGNB2 through FC\_ALIGNM8; these are not used.</span></span>

     

-   <span data-ttu-id="3c14d-187">Enchimento da memória.</span><span class="sxs-lookup"><span data-stu-id="3c14d-187">Memory padding.</span></span> <span data-ttu-id="3c14d-188">Elas ocorrem apenas no final da descrição de uma estrutura e denotam o número de bytes de preenchimento na memória antes da matriz em conformidade na estrutura: FC \_ STRUCTPADn, em que n é o número de bytes de preenchimento.</span><span class="sxs-lookup"><span data-stu-id="3c14d-188">These occur only at the end of a structure's description and denote the number of bytes of padding in memory before the conformant array in the structure: FC\_STRUCTPADn, where n is the number of bytes of padding.</span></span>
-   <span data-ttu-id="3c14d-189">Qualquer tipo não base inserido (Observe, no entanto, que uma matriz em conformidade nunca ocorre no layout da estrutura).</span><span class="sxs-lookup"><span data-stu-id="3c14d-189">Any embedded nonbase type (note, however, that a conformant array never occurs in the structure layout).</span></span> <span data-ttu-id="3c14d-190">Isso tem uma descrição de 4 bytes:</span><span class="sxs-lookup"><span data-stu-id="3c14d-190">This has a 4-byte description:</span></span>

    ``` syntax
    FC_EMBEDDED_COMPLEX memory_pad<1> 
    offset_to_description<2>,
    ```

    <span data-ttu-id="3c14d-191">em que não há garantia de que o deslocamento seja alinhado em 2 bytes.</span><span class="sxs-lookup"><span data-stu-id="3c14d-191">where the offset is not guaranteed to be 2-byte aligned.</span></span>

    <span data-ttu-id="3c14d-192">\_o controle de memória<1> é um preenchimento necessário na memória antes do campo complexo.</span><span class="sxs-lookup"><span data-stu-id="3c14d-192">memory\_pad<1> is a padding needed in memory before the complex field.</span></span>

    <span data-ttu-id="3c14d-193">\_o deslocamento para a \_ Descrição<2> é um deslocamento de tipo relativo para o tipo inserido.</span><span class="sxs-lookup"><span data-stu-id="3c14d-193">offset\_to\_description<2> is a relative type offset to the embedded type.</span></span>

<span data-ttu-id="3c14d-194">Também pode haver um pad FC \_ antes do final do FC de terminação \_ , se necessário, para garantir que a cadeia de caracteres de formato seja alinhada a um limite de 2 bytes após a extremidade do FC \_ .</span><span class="sxs-lookup"><span data-stu-id="3c14d-194">There may also be an FC\_PAD before the terminating FC\_END if needed to ensure that the format string will be aligned at a 2-byte boundary following the FC\_END.</span></span>

 

 
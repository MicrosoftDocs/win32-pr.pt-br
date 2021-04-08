---
title: Layout do ponteiro
description: O layout do ponteiro descreve os ponteiros de uma estrutura ou de uma matriz.
ms.assetid: 1a4984c1-97b9-4e95-a17e-851b67fa94a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f26a6639b0c4b56c911be1e688995aaf3fb9d2d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822879"
---
# <a name="pointer-layout"></a><span data-ttu-id="09fce-103">Layout do ponteiro</span><span class="sxs-lookup"><span data-stu-id="09fce-103">Pointer Layout</span></span>

<span data-ttu-id="09fce-104">O layout do ponteiro descreve os ponteiros de uma estrutura ou de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="09fce-104">Pointer layout describes pointers of a structure or an array.</span></span>

## <a name="pointer_layout"></a><span data-ttu-id="09fce-105"><> de layout do ponteiro \_</span><span class="sxs-lookup"><span data-stu-id="09fce-105">pointer\_layout<></span></span>

<span data-ttu-id="09fce-106">Um \_ campo de<> de layout de ponteiro consiste no pad de formato FC \_ PP FC \_ seguido por uma ou mais descrições de ponteiro, conforme descrito posteriormente e terminando com um \_ caractere de formato FC end:</span><span class="sxs-lookup"><span data-stu-id="09fce-106">A pointer\_layout<> field consists of the format characters FC\_PP FC\_PAD followed by one or more pointer descriptions, as described later, and terminating with an FC\_END format character:</span></span>

``` syntax
FC_PP
FC_PAD
{ pointer_instance_layout<> }*
FC_END
```

<span data-ttu-id="09fce-107">Um layout de instância de ponteiro \_ \_<> campo é uma cadeia de caracteres de formato que descreve uma ou várias instâncias de ponteiros.</span><span class="sxs-lookup"><span data-stu-id="09fce-107">A pointer\_instance\_layout<> field is a format string describing single or multiple instances of pointers.</span></span> <span data-ttu-id="09fce-108">Os seguintes campos são usados nesses Descritores:</span><span class="sxs-lookup"><span data-stu-id="09fce-108">The following fields are used in these descriptors:</span></span>

-   <span data-ttu-id="09fce-109">deslocamento \_ na \_ memória</span><span class="sxs-lookup"><span data-stu-id="09fce-109">offset\_in\_memory</span></span>

    <span data-ttu-id="09fce-110">O deslocamento assinado para o local do ponteiro na memória.</span><span class="sxs-lookup"><span data-stu-id="09fce-110">The signed offset to the pointer's location in memory.</span></span> <span data-ttu-id="09fce-111">Para um ponteiro que reside em uma estrutura, esse deslocamento é um deslocamento negativo do final da estrutura (o final da parte não compatível das estruturas em conformidade); para matrizes, o deslocamento é do início da matriz.</span><span class="sxs-lookup"><span data-stu-id="09fce-111">For a pointer residing in a structure, this offset is a negative offset from the end of the structure (the end of the nonconformant portion of conformant structures); for arrays, the offset is from the beginning of the array.</span></span>

-   <span data-ttu-id="09fce-112">deslocamento \_ no \_ buffer</span><span class="sxs-lookup"><span data-stu-id="09fce-112">offset\_in\_buffer</span></span>

    <span data-ttu-id="09fce-113">O deslocamento assinado para o local do ponteiro no buffer.</span><span class="sxs-lookup"><span data-stu-id="09fce-113">The signed offset to the pointer's location in the buffer.</span></span> <span data-ttu-id="09fce-114">Para um ponteiro que reside em uma estrutura, esse deslocamento é um deslocamento negativo do final da estrutura (o final da parte não compatível das estruturas em conformidade): para matrizes, o deslocamento é do início da matriz.</span><span class="sxs-lookup"><span data-stu-id="09fce-114">For a pointer residing in a structure, this offset is a negative offset from the end of the structure (the end of the nonconformant portion of conformant structures): for arrays, the offset is from the beginning of the array.</span></span>

-   <span data-ttu-id="09fce-115">deslocamento \_ para \_ matriz</span><span class="sxs-lookup"><span data-stu-id="09fce-115">offset\_to\_array</span></span>

    <span data-ttu-id="09fce-116">Deslocamento de uma estrutura delimitadora para a matriz inserida cujos ponteiros estão sendo manipulados.</span><span class="sxs-lookup"><span data-stu-id="09fce-116">Offset from an enclosing structure to the embedded array whose pointers are being handled.</span></span> <span data-ttu-id="09fce-117">Para matrizes de nível superior, esse campo sempre será zero.</span><span class="sxs-lookup"><span data-stu-id="09fce-117">For top-level arrays, this field will always be zero.</span></span>

-   <span data-ttu-id="09fce-118">iterações</span><span class="sxs-lookup"><span data-stu-id="09fce-118">iterations</span></span>

    <span data-ttu-id="09fce-119">Número total de ponteiros que têm o mesmo layout<> descrito.</span><span class="sxs-lookup"><span data-stu-id="09fce-119">Total number of pointers that have the same layout<> described.</span></span>

-   <span data-ttu-id="09fce-120">incremento</span><span class="sxs-lookup"><span data-stu-id="09fce-120">increment</span></span>

    <span data-ttu-id="09fce-121">Incrementar entre ponteiros sucessivos durante uma repetição.</span><span class="sxs-lookup"><span data-stu-id="09fce-121">Increment between successive pointers during a REPEAT.</span></span>

-   <span data-ttu-id="09fce-122">número \_ de \_ ponteiros</span><span class="sxs-lookup"><span data-stu-id="09fce-122">number\_of\_pointers</span></span>

    <span data-ttu-id="09fce-123">Número de ponteiros diferentes em uma instância de repetição.</span><span class="sxs-lookup"><span data-stu-id="09fce-123">Number of different pointers in a repeat instance.</span></span>

-   <span data-ttu-id="09fce-124">Descrição do ponteiro \_</span><span class="sxs-lookup"><span data-stu-id="09fce-124">pointer\_description</span></span>

    <span data-ttu-id="09fce-125">Descrição do ponteiro.</span><span class="sxs-lookup"><span data-stu-id="09fce-125">Pointer description.</span></span>

<span data-ttu-id="09fce-126">Todos os layouts de instância de ponteiro usam a seguinte instância de ponteiro único \_<8>:</span><span class="sxs-lookup"><span data-stu-id="09fce-126">All pointer instance layouts use the following single pointer\_instance<8>:</span></span>

``` syntax
offset_to_pointer_in_memory<2> 
offset_to_pointer_in_buffer<2> 
pointer_description<4>
```

<span data-ttu-id="09fce-127">Veja a seguir os descritores de instância:</span><span class="sxs-lookup"><span data-stu-id="09fce-127">The following are instance descriptors:</span></span>

<span data-ttu-id="09fce-128">**Instância única de um ponteiro para um tipo simples:**</span><span class="sxs-lookup"><span data-stu-id="09fce-128">**Single instance of a pointer to a simple type:**</span></span>

``` syntax
FC_NO_REPEAT FC_PAD 
pointer_instance<8>
```

<span data-ttu-id="09fce-129">**Ponteiro de repetição fixo:**</span><span class="sxs-lookup"><span data-stu-id="09fce-129">**Fixed repeat pointer:**</span></span>

``` syntax
FC_FIXED_REPEAT FC_PAD 
iterations<2> 
increment<2> 
offset_to_array<2> 
number_of_pointers<2>
{ pointer_instance<8> }*
```

<span data-ttu-id="09fce-130">**Ponteiro de repetição de variável:**</span><span class="sxs-lookup"><span data-stu-id="09fce-130">**Variable repeat pointer:**</span></span>

``` syntax
FC_VARIABLE_REPEAT (FC_FIXED_OFFSET | FC_VARIABLE_OFFSET) 
increment<2> 
offset_to_array<2> 
number_of_pointers<2> 
{ pointer_instance<8> }*
```

<span data-ttu-id="09fce-131">Para instâncias de repetição fixa e de ponteiro de repetição variável, há um conjunto de descrições de deslocamento e ponteiro para cada ponteiro na instância de repetição.</span><span class="sxs-lookup"><span data-stu-id="09fce-131">For fixed repeat and variable repeat pointer instances there is a set of offset and pointer descriptions for each pointer in the repeat instance.</span></span>

## <a name="pointers-layout-design-issues"></a><span data-ttu-id="09fce-132">Problemas de design de layout de ponteiros</span><span class="sxs-lookup"><span data-stu-id="09fce-132">Pointers Layout Design Issues</span></span>

<span data-ttu-id="09fce-133">Esta seção aborda os problemas relacionados ao processamento de estruturas de conformidade e ponteiros incorporados.</span><span class="sxs-lookup"><span data-stu-id="09fce-133">This section addresses issues related to processing conformant structures and embedded pointers.</span></span> <span data-ttu-id="09fce-134">O problema é que o compilador gera layouts de ponteiro para estruturas e matrizes com alguma redundância.</span><span class="sxs-lookup"><span data-stu-id="09fce-134">The issue is that the compiler generates pointer layouts for structures and arrays with some redundancy.</span></span> <span data-ttu-id="09fce-135">Isso é benéfico, pois as informações são úteis e, por exemplo, uma estrutura compatível pode percorrer um layout de ponteiro para atender a todos os ponteiros da estrutura e da matriz de conformidade que faz parte da estrutura compatível.</span><span class="sxs-lookup"><span data-stu-id="09fce-135">This is beneficial, because the information is useful and as such, for example, a conformant structure can walk one pointer layout to service all the pointers from the structure and from the conformant array being part of the conformant structure.</span></span> <span data-ttu-id="09fce-136">No entanto, existem algumas situações incorporadas que exigem que o mecanismo de NDR execute trabalho adicional para processar todos os layouts de ponteiro na sequência apropriada, processando cada ponteiro exatamente uma vez.</span><span class="sxs-lookup"><span data-stu-id="09fce-136">However, some embedded situations exist that require the NDR engine to perform additional work to process all the pointer layouts in the proper sequence, processing each pointer exactly once.</span></span>

## <a name="what-the-compiler-generates"></a><span data-ttu-id="09fce-137">O que o compilador gera</span><span class="sxs-lookup"><span data-stu-id="09fce-137">What the Compiler Generates</span></span>

<span data-ttu-id="09fce-138">Cada objeto abordado nesta seção tem ponteiros, por exemplo, uma estrutura compatível tem ponteiros na parte da estrutura, bem como nos elementos da matriz.</span><span class="sxs-lookup"><span data-stu-id="09fce-138">Every object discussed in this section has pointers, so for example, a conformant structure has pointers in the structure part as well as in the array elements.</span></span> <span data-ttu-id="09fce-139">O elemento é uma estrutura simples com um ponteiro.</span><span class="sxs-lookup"><span data-stu-id="09fce-139">The element is a simple structure with a pointer.</span></span>

1.  <span data-ttu-id="09fce-140">Estrutura compatível, nível único</span><span class="sxs-lookup"><span data-stu-id="09fce-140">Conformant structure, single level</span></span>

    <span data-ttu-id="09fce-141">O descritor de conformidade tem uma PP parte onde todos os ponteiros são descritos, tanto da estrutura quanto da matriz.</span><span class="sxs-lookup"><span data-stu-id="09fce-141">The conformant descriptor has a PP part where all the pointers are described, both from the structure and from the array.</span></span> <span data-ttu-id="09fce-142">A lista de membros tem FC \_ longo no lugar de um ponteiro.</span><span class="sxs-lookup"><span data-stu-id="09fce-142">The member list has FC\_LONG in lieu of a pointer.</span></span> <span data-ttu-id="09fce-143">O descritor de matriz CARRAY tem elementos por meio do uso de um \_ complexo incorporado e nenhum descritor de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="09fce-143">The CARRAY array descriptor has elements through the use of an embedded\_complex and no pointer descriptors at all.</span></span> <span data-ttu-id="09fce-144">O elemento ainda tem seu único descritor de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="09fce-144">The element still has its single pointer descriptor.</span></span> <span data-ttu-id="09fce-145">O layout do ponteiro precede o layout do membro em uma estrutura compatível e descritores de estrutura simples.</span><span class="sxs-lookup"><span data-stu-id="09fce-145">Pointer layout precedes the member layout in a conformant structure and simple structure descriptors.</span></span>

2.  <span data-ttu-id="09fce-146">Estrutura compatível, dois ou mais níveis</span><span class="sxs-lookup"><span data-stu-id="09fce-146">Conformant structure, two or more levels</span></span>

    <span data-ttu-id="09fce-147">A descrição PP tem ponteiros de todos os níveis.</span><span class="sxs-lookup"><span data-stu-id="09fce-147">The PP description has pointers from all levels.</span></span> <span data-ttu-id="09fce-148">Ele reutiliza a mesma descrição de matriz da estrutura de conformidade interna.</span><span class="sxs-lookup"><span data-stu-id="09fce-148">It reuses the same array description as the internal conformant structure.</span></span> <span data-ttu-id="09fce-149">A lista de membros tem FC \_ longo no lugar de um ponteiro.</span><span class="sxs-lookup"><span data-stu-id="09fce-149">The member list has FC\_LONG in lieu of a pointer.</span></span> <span data-ttu-id="09fce-150">Uma estrutura incorporada vem pelo uso de um complexo incorporado.</span><span class="sxs-lookup"><span data-stu-id="09fce-150">An embedded structure comes through the use of an embedded complex.</span></span> <span data-ttu-id="09fce-151">O descritor de estrutura compatível é reutilizado como está.</span><span class="sxs-lookup"><span data-stu-id="09fce-151">The conformant structure descriptor is reused as-is.</span></span> <span data-ttu-id="09fce-152">O tamanho da parte plana da estrutura também é completo, o que significa que o tamanho da estrutura de nível superior incluirá o tamanho fixo da estrutura inserida.</span><span class="sxs-lookup"><span data-stu-id="09fce-152">The size of the flat portion of the structure comes out complete as well, meaning that the top-level structure size would include embedded structure's flat size.</span></span>

3.  <span data-ttu-id="09fce-153">Estrutura complexa, nível único</span><span class="sxs-lookup"><span data-stu-id="09fce-153">Complex structure, single level</span></span>

    <span data-ttu-id="09fce-154">Os membros do ponteiro são marcados pelo ponteiro do FC \_ .</span><span class="sxs-lookup"><span data-stu-id="09fce-154">Pointer members are marked by FC\_POINTER.</span></span> <span data-ttu-id="09fce-155">O layout do ponteiro é simplificado, de modo que haja um descritor de ponteiro (4 bytes) para cada entrada de ponteiro de FC \_ na lista.</span><span class="sxs-lookup"><span data-stu-id="09fce-155">Pointer layout is simplified such that there is a pointer descriptor (4 bytes) for each FC\_POINTER entry on the list.</span></span> <span data-ttu-id="09fce-156">O layout do ponteiro é movimentado em paralelo com uma movimentação de membro, ou seja, um \_ ponteiro de FC faz com que a próxima descrição do ponteiro seja processada.</span><span class="sxs-lookup"><span data-stu-id="09fce-156">Pointer layout is walked in parallel with a member walk, that is, an FC\_POINTER causes the next pointer description to be processed.</span></span> <span data-ttu-id="09fce-157">A matriz CARRAY tem layout de ponteiro com todos os descritores da matriz e, em seguida, o elemento, por meio do uso de um complexo incorporado.</span><span class="sxs-lookup"><span data-stu-id="09fce-157">The CARRAY array has pointer layout with all the descriptors of the array, and then element, through the use of an embedded complex.</span></span> <span data-ttu-id="09fce-158">O descritor de elemento é reutilizado.</span><span class="sxs-lookup"><span data-stu-id="09fce-158">The element descriptor is reused.</span></span> <span data-ttu-id="09fce-159">O tamanho da parte plana da estrutura é concluído; em outras palavras, o tamanho fixo da estrutura de nível superior inclui o tamanho fixo da estrutura incorporada.</span><span class="sxs-lookup"><span data-stu-id="09fce-159">The size of the flat portion of the structure comes out complete; in other words, the top-level structure's flat size includes the embedded structure's flat size.</span></span> <span data-ttu-id="09fce-160">O layout do membro precede o layout do ponteiro para estruturas complexas.</span><span class="sxs-lookup"><span data-stu-id="09fce-160">The member layout precedes the pointer layout for complex structures.</span></span>

    <span data-ttu-id="09fce-161">Portanto, a geração de descrição de matriz em conformidade é diferente dependendo se é uma matriz dentro de uma estrutura compatível ou dentro de uma estrutura complexa.</span><span class="sxs-lookup"><span data-stu-id="09fce-161">Hence, the conformant array description generation is different depending on whether it is an array inside of a conformant structure or inside a complex structure.</span></span>

4.  <span data-ttu-id="09fce-162">Estrutura complexa, 2 ou mais níveis, complexa em complexo</span><span class="sxs-lookup"><span data-stu-id="09fce-162">Complex structure, 2 or more levels, complex in complex</span></span>

    <span data-ttu-id="09fce-163">A estrutura complexa de nível superior tem seus ponteiros de membro, estrutura complexa inserida tem seus ponteiros de membro.</span><span class="sxs-lookup"><span data-stu-id="09fce-163">Top-level complex structure has its member pointers, embedded complex structure has its member pointers.</span></span> <span data-ttu-id="09fce-164">O descritor de estrutura compatível é reutilizado.</span><span class="sxs-lookup"><span data-stu-id="09fce-164">The conformant structure descriptor is reused.</span></span> <span data-ttu-id="09fce-165">O descritor de matriz na parte superior é a matriz reutilizada da estrutura inserida.</span><span class="sxs-lookup"><span data-stu-id="09fce-165">The array descriptor from the top is the reused array from the embedded structure.</span></span>

5.  <span data-ttu-id="09fce-166">Estrutura complexa com uma estrutura compatível incorporada</span><span class="sxs-lookup"><span data-stu-id="09fce-166">Complex structure with an embedded conformant structure</span></span>

    <span data-ttu-id="09fce-167">A estrutura compatível de nível superior = tem seus ponteiros de membro.</span><span class="sxs-lookup"><span data-stu-id="09fce-167">Top=level conformant structure has its member pointers.</span></span> <span data-ttu-id="09fce-168">O descritor de estrutura compatível é reutilizado como está.</span><span class="sxs-lookup"><span data-stu-id="09fce-168">The conformant structure descriptor is reused as-is.</span></span> <span data-ttu-id="09fce-169">O descritor de matriz é reutilizado da estrutura compatível incorporada; em outras palavras, ele não tem nenhum ponteiro no descritor de matriz.</span><span class="sxs-lookup"><span data-stu-id="09fce-169">The array descriptor is reused from the embedded conformant structure; in other words, it does not have any pointers at the array descriptor.</span></span> <span data-ttu-id="09fce-170">O elemento tem seu descritor de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="09fce-170">The element has its pointer descriptor.</span></span>

6.  <span data-ttu-id="09fce-171">Matrizes de estruturas com ponteiros</span><span class="sxs-lookup"><span data-stu-id="09fce-171">Arrays of structures with pointers</span></span>

    <span data-ttu-id="09fce-172">Uma matriz de estruturas simples com ponteiros é gerada como um SMFARRAY ou CARRAY dependendo se a matriz é dimensionada, mas em ambos os casos ele tem um layout de ponteiro concluído ( \_ repetição fixa ou repetição de variável \_ ).</span><span class="sxs-lookup"><span data-stu-id="09fce-172">An array of simple structures with pointers is generated as an SMFARRAY or CARRAY depending whether the array is sized, but in both cases it has a pointer layout that is complete (FIXED\_REPEAT or VARIABLE\_REPEAT).</span></span> <span data-ttu-id="09fce-173">O layout do ponteiro vem antes do layout do membro.</span><span class="sxs-lookup"><span data-stu-id="09fce-173">The pointer layout comes before the member layout.</span></span>

    <span data-ttu-id="09fce-174">Uma matriz de estruturas complexas com ponteiros é gerada como \_ matriz falsa, independentemente de ser fixa ou dimensionada, e em ambos os casos, não tem nenhum layout de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="09fce-174">An array of complex structures with pointers is generated as BOGUS\_ARRAY regardless whether it is fixed or sized, and in both cases, does not have any pointer layout.</span></span>

## <a name="what-the-ndr-engine-does"></a><span data-ttu-id="09fce-175">O que o mecanismo de NDR faz</span><span class="sxs-lookup"><span data-stu-id="09fce-175">What the NDR Engine Does</span></span>

<span data-ttu-id="09fce-176">Esta seção descreve o comportamento do mecanismo de NDR.</span><span class="sxs-lookup"><span data-stu-id="09fce-176">This section describes the NDR engine behavior.</span></span>

<span data-ttu-id="09fce-177">**A passagem de marshaling**</span><span class="sxs-lookup"><span data-stu-id="09fce-177">**The marshaling pass**</span></span>

1.  <span data-ttu-id="09fce-178">Estruturas de conformidade e estrutura de conformidade incorporada.</span><span class="sxs-lookup"><span data-stu-id="09fce-178">Conformant structures and embedded conformant structure.</span></span>

    <span data-ttu-id="09fce-179">A estrutura de nível superior se comporta como uma estrutura de nível único.</span><span class="sxs-lookup"><span data-stu-id="09fce-179">The top-level structure behaves like a single-level structure.</span></span>

2.  <span data-ttu-id="09fce-180">Estrutura complexa inserida com matriz em conformidade</span><span class="sxs-lookup"><span data-stu-id="09fce-180">Embedded complex structure with conformant array</span></span>

    <span data-ttu-id="09fce-181">Qualquer estrutura complexa força a estrutura externa a ser uma estrutura complexa.</span><span class="sxs-lookup"><span data-stu-id="09fce-181">Any complex structure forces the outer structure to be a complex structure.</span></span> <span data-ttu-id="09fce-182">A estrutura inserida nunca realiza marshaling de sua matriz.</span><span class="sxs-lookup"><span data-stu-id="09fce-182">Embedded structure never marshals its array.</span></span> <span data-ttu-id="09fce-183">Cada estrutura sempre passa por ponteiros incorporados simplesmente realizando marshaling de membros e um membro que está acontecendo como um ponteiro de FC \_ .</span><span class="sxs-lookup"><span data-stu-id="09fce-183">Every structure always goes through embedded pointers by simply marshaling members and a member happening to be an FC\_POINTER.</span></span>

3.  <span data-ttu-id="09fce-184">Estrutura complexa com estrutura compatível</span><span class="sxs-lookup"><span data-stu-id="09fce-184">Complex structure with conformant structure</span></span>

    <span data-ttu-id="09fce-185">A estrutura compatível mais alta incorporada realiza marshaling da matriz em conformidade e de todos os pontos.</span><span class="sxs-lookup"><span data-stu-id="09fce-185">The top-most embedded conformant structure marshals the conformant array and all the pointees.</span></span> <span data-ttu-id="09fce-186">O mecanismo de NDR nunca descende para estruturas de conformidade aninhadas mais profundas se houver alguma; Isso simplifica a solução, pois uma estrutura compatível é um objeto folha no que diz respeito ao marshaling de objetos inseridos.</span><span class="sxs-lookup"><span data-stu-id="09fce-186">The NDR engine never descends to deeper nested conformant structures if there are any; this simplifies the solution, as a conformant structure is a leaf object as far as the marshaling of embedded objects is concerned.</span></span> <span data-ttu-id="09fce-187">A estrutura complexa de nível superior ignora o empacotamento de matriz.</span><span class="sxs-lookup"><span data-stu-id="09fce-187">The top-level complex structure skips the array marshaling.</span></span>

<span data-ttu-id="09fce-188">**Desempacotamento, bufsizing e liberação de passagens**</span><span class="sxs-lookup"><span data-stu-id="09fce-188">**Unmarshaling, bufsizing and freeing passes**</span></span>

<span data-ttu-id="09fce-189">O desempacotamento é simétrico para o marshaling; a primeira operação que ele executa para estruturas complexas é descobrir o local dos pontos do buffer por meio da chamada da função **NdrComplexStructBufferSize** .</span><span class="sxs-lookup"><span data-stu-id="09fce-189">Unmarshaling is symmetrical to marshaling; the first operation it performs for complex structures is to find out the pointees' location in the buffer by means of calling the **NdrComplexStructBufferSize** function.</span></span> <span data-ttu-id="09fce-190">Em seguida, ele desempacota os pontos de ponto em paralelo, habilitando o mesmo esquema para desempacotamento dos pontos corretamente a serem usados.</span><span class="sxs-lookup"><span data-stu-id="09fce-190">It then unmarshals pointees in parallel, enabling the same scheme for unmarshaling the pointees correctly to be used.</span></span> <span data-ttu-id="09fce-191">Não deve haver nenhuma confusão sobre objetos e uniões de tamanho; a imagem de memória não deve ser usada para objetos dimensionados e uniões, apenas para o conteúdo do buffer.</span><span class="sxs-lookup"><span data-stu-id="09fce-191">There should be no confusion about sized objects and unions; the memory image should not be used for sized objects and unions, just for the buffer contents.</span></span>

<span data-ttu-id="09fce-192">Os sinalizadores usados para executar o marshaling e o desempacotamento corretamente são usados da mesma maneira no bufsizing e liberados para garantir que os pontos sejam percorridos exatamente uma vez.</span><span class="sxs-lookup"><span data-stu-id="09fce-192">The flags used to perform marshaling and unmarshaling correctly are used in the same way in bufsizing and freeing to make sure that pointees are walked exactly once.</span></span>

<span data-ttu-id="09fce-193">**Endianess Pass**</span><span class="sxs-lookup"><span data-stu-id="09fce-193">**Endianess pass**</span></span>

<span data-ttu-id="09fce-194">A princípio, o endianess Pass é um pouco semelhante ao empacotamento/desempacotamento; são necessárias duas passagens para processar estruturas complexas.</span><span class="sxs-lookup"><span data-stu-id="09fce-194">At first, the endianess pass is somewhat similar to marshaling/unmarshaling; two passes are required to process complex structures.</span></span> <span data-ttu-id="09fce-195">A primeira passagem converte a parte plana e localiza o local dos pontos do ponto no buffer, semelhante a como o bufsizing executa essa operação para desempacotamento.</span><span class="sxs-lookup"><span data-stu-id="09fce-195">First pass converts the flat part and finds the pointees' location in the buffer similar to how bufsizing performs this operation for unmarshaling.</span></span> <span data-ttu-id="09fce-196">Em seguida, a segunda passagem converte os pontos.</span><span class="sxs-lookup"><span data-stu-id="09fce-196">The second pass then converts the pointees.</span></span>

<span data-ttu-id="09fce-197">As passagens de endianess são diferentes da seguinte maneira: todas as estruturas e todos os membros têm que ser percorridos até que o membro folha ou o elemento seja um tipo simples.</span><span class="sxs-lookup"><span data-stu-id="09fce-197">Endianess passes differ in the following manner: every structure and every member has to be stepped until the leaf member or element is a simple type.</span></span> <span data-ttu-id="09fce-198">Isso é diferente do desempacotamento; no desempacotamento, por exemplo, nunca há necessidade de processar estruturas de conformidade inseridas em estruturas em conformidade ou em qualquer membro da estrutura compatível, para esse assunto.</span><span class="sxs-lookup"><span data-stu-id="09fce-198">This is different from unmarshaling; in unmarshaling, for example, there is never a need to process conformant structures embedded in conformant structures, or any member of the conformant structure, for that matter.</span></span> <span data-ttu-id="09fce-199">Outro problema é que a conversão não é uma operação idempotente; portanto, a passagem de desempacotamento pode refazer o desempacotamento de algumas partes sem danos, enquanto a conversão precisa ser executada em uma base de tipo estritamente única vez por qualquer um.</span><span class="sxs-lookup"><span data-stu-id="09fce-199">Another issue is that the conversion is not an idempotent operation—hence the unmarshaling pass could redo unmarshaling of some pieces without harm, while conversion has to be performed on a strictly once-per-any-simple-type basis.</span></span>

<span data-ttu-id="09fce-200">Portanto, o algoritmo endianess pode ser resumido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="09fce-200">Hence, the endianess algorithm can be summarized as the following.</span></span> <span data-ttu-id="09fce-201">O NDR tem uma noção da estrutura de conformidade de nível superior e um sinalizador para marcá-lo, conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="09fce-201">NDR has a notion of the top-level conformant structure and a flag to mark that, as appropriate.</span></span> <span data-ttu-id="09fce-202">Ao se movimentar pela primeira vez, como para converter a parte plana e obter o local dos pontos, essa noção não seria usada.</span><span class="sxs-lookup"><span data-stu-id="09fce-202">When walking the first time, such as to convert the flat portion and to obtain the location of the pointees, this notion would not be used.</span></span> <span data-ttu-id="09fce-203">O NDR se depararia com as partes simples de todos os níveis de estruturas e nunca se aventuraria no processamento de ponteiros.</span><span class="sxs-lookup"><span data-stu-id="09fce-203">NDR would descend through the flat parts of all levels of structures and never venture into pointer processing.</span></span> <span data-ttu-id="09fce-204">Por fim, o NDR iria converter a matriz no nível superior.</span><span class="sxs-lookup"><span data-stu-id="09fce-204">Finally, NDR would flat convert the array at the top-level.</span></span>

<span data-ttu-id="09fce-205">Ao percorrer a segunda vez, o sinalizador seria usado para marcar a passagem do ponteiro inserido para evitar a inserção de níveis mais detalhados das estruturas em conformidade e, em seguida, a estrutura compatível mais alta.</span><span class="sxs-lookup"><span data-stu-id="09fce-205">When walking the second time, the flag would be used to mark the embedded pointer's pass to avoid entering deeper levels of the conformant structures, then the top-most conformant structure.</span></span> <span data-ttu-id="09fce-206">Dessa forma, o sinalizador forçaria o comportamento comum de marshaling/desempacotamento, que é evitar decrescente em níveis mais detalhados de estruturas em conformidade.</span><span class="sxs-lookup"><span data-stu-id="09fce-206">In this way, the flag would force the common marshaling/unmarshaling behavior, which is to avoid descending into deeper levels of conformant structures.</span></span>

<span data-ttu-id="09fce-207">A segunda passagem para estruturas complexas com matrizes em conformidade funciona da seguinte maneira: as estruturas complexas funcionam da maneira comum; Isso significa que os níveis mais detalhados nunca examinarão nem ignorarão seu tamanho de conformidade ou suas matrizes de conformidade e, em vez disso, simplesmente percorrerão seus membros sem tocar na matriz.</span><span class="sxs-lookup"><span data-stu-id="09fce-207">The second pass for complex structures with conformant arrays works as follows: the complex structures work the common way; which means deeper levels would never look at or skip their conformant size or their conformant arrays, and would rather simply walk their members without touching the array.</span></span>

<span data-ttu-id="09fce-208">Para estruturas complexas com estruturas compatíveis, a estrutura compatível deve estar ciente se é de nível superior e se está em uma estrutura complexa.</span><span class="sxs-lookup"><span data-stu-id="09fce-208">For complex structures with conformant structures, the conformant structure must be aware whether it is top level, and whether it is in a complex structure.</span></span> <span data-ttu-id="09fce-209">A parte simples da matriz é processada pela estrutura compatível mais alta.</span><span class="sxs-lookup"><span data-stu-id="09fce-209">The flat portion of the array is processed by the top-most conformant structure.</span></span> <span data-ttu-id="09fce-210">Na segunda passagem, a estrutura compatível mais alta iria ignorar a parte plana e passar pelo layout do ponteiro e retornando.</span><span class="sxs-lookup"><span data-stu-id="09fce-210">On the second pass, the top-most conformant structure would skip the flat portion and go through the pointer layout and return.</span></span> <span data-ttu-id="09fce-211">A estrutura mais complexa ignoraria sua parte plana e também ignoraria o layout do ponteiro.</span><span class="sxs-lookup"><span data-stu-id="09fce-211">The top-most complex structure would skip its flat portion, and would also skip the pointer layout.</span></span>

<span data-ttu-id="09fce-212">**O aspecto robusto das endianess Walks**</span><span class="sxs-lookup"><span data-stu-id="09fce-212">**The robust aspect of the endianess walks**</span></span>

<span data-ttu-id="09fce-213">A endianess Walk verifica as condições normais do buffer e executa outras verificações de uma natureza não correlacionada.</span><span class="sxs-lookup"><span data-stu-id="09fce-213">The endianess walk checks for the usual out-of-the-buffer conditions and performs other checks of an uncorrelated nature.</span></span> <span data-ttu-id="09fce-214">As verificações destinadas a valores correlacionados (como o argumento de dimensionamento versus o tamanho de conformidade) não podem ser executadas usando essa etapa; Eles são executados mais tarde, ao desempacotamento.</span><span class="sxs-lookup"><span data-stu-id="09fce-214">The checks aimed at correlated values (such as the sizing argument versus the conformant size) cannot be performed using this step; they are performed later, when unmarshaling.</span></span>

 

 





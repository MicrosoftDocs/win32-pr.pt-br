---
title: Convenções de codificação do Windows
description: Se você for novo na programação do Windows, ele poderá ser desconcerto quando você vir um programa do Windows pela primeira vez.
ms.assetid: 466a66db-7681-4fce-9672-07849cd1b096
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365a9c8509d7cb799bafdfa70c326f1074b64d93
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105766259"
---
# <a name="windows-coding-conventions"></a><span data-ttu-id="60122-103">Convenções de codificação do Windows</span><span class="sxs-lookup"><span data-stu-id="60122-103">Windows Coding Conventions</span></span>

<span data-ttu-id="60122-104">Se você for novo na programação do Windows, ele poderá ser desconcerto quando você vir um programa do Windows pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="60122-104">If you are new to Windows programming, it can be disconcerting when you first see a Windows program.</span></span> <span data-ttu-id="60122-105">O código é preenchido com definições de tipo estranhas, como **DWORD \_ PTR** e **lpRect**, e variáveis têm nomes como *HWND* e *PWSZ* (chamado de notação húngara).</span><span class="sxs-lookup"><span data-stu-id="60122-105">The code is filled with strange type definitions like **DWORD\_PTR** and **LPRECT**, and variables have names like *hWnd* and *pwsz* (called Hungarian notation).</span></span> <span data-ttu-id="60122-106">Vale a pena dedicar um momento para aprender algumas das convenções de codificação do Windows.</span><span class="sxs-lookup"><span data-stu-id="60122-106">It's worth taking a moment to learn some of the Windows coding conventions.</span></span>

<span data-ttu-id="60122-107">A grande maioria das APIs do Windows consiste em funções ou em interfaces de Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="60122-107">The vast majority of Windows APIs consist of either functions or Component Object Model (COM) interfaces.</span></span> <span data-ttu-id="60122-108">Muito poucas APIs do Windows são fornecidas como classes do C++.</span><span class="sxs-lookup"><span data-stu-id="60122-108">Very few Windows APIs are provided as C++ classes.</span></span> <span data-ttu-id="60122-109">(Uma exceção notável é GDI+, uma das APIs de gráficos 2-D.)</span><span class="sxs-lookup"><span data-stu-id="60122-109">(A notable exception is GDI+, one of the 2-D graphics APIs.)</span></span>

## <a name="typedefs"></a><span data-ttu-id="60122-110">Typedefs</span><span class="sxs-lookup"><span data-stu-id="60122-110">Typedefs</span></span>

<span data-ttu-id="60122-111">Os cabeçalhos do Windows contêm muitos TYPEDEFs.</span><span class="sxs-lookup"><span data-stu-id="60122-111">The Windows headers contain a lot of typedefs.</span></span> <span data-ttu-id="60122-112">Muitos deles são definidos no arquivo de cabeçalho WinDef. h.</span><span class="sxs-lookup"><span data-stu-id="60122-112">Many of these are defined in the header file WinDef.h.</span></span> <span data-ttu-id="60122-113">Aqui estão alguns que você encontrará com frequência.</span><span class="sxs-lookup"><span data-stu-id="60122-113">Here are some that you will encounter often.</span></span>

### <a name="integer-types"></a><span data-ttu-id="60122-114">Tipos de inteiro</span><span class="sxs-lookup"><span data-stu-id="60122-114">Integer types</span></span>



| <span data-ttu-id="60122-115">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="60122-115">Data type</span></span>     | <span data-ttu-id="60122-116">Tamanho</span><span class="sxs-lookup"><span data-stu-id="60122-116">Size</span></span>    | <span data-ttu-id="60122-117">Inteiro?</span><span class="sxs-lookup"><span data-stu-id="60122-117">Signed?</span></span>  |
|---------------|---------|----------|
| <span data-ttu-id="60122-118">**BYTE**</span><span class="sxs-lookup"><span data-stu-id="60122-118">**BYTE**</span></span>      | <span data-ttu-id="60122-119">8 bits</span><span class="sxs-lookup"><span data-stu-id="60122-119">8 bits</span></span>  | <span data-ttu-id="60122-120">Não assinado</span><span class="sxs-lookup"><span data-stu-id="60122-120">Unsigned</span></span> |
| <span data-ttu-id="60122-121">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="60122-121">**DWORD**</span></span>     | <span data-ttu-id="60122-122">32 bits</span><span class="sxs-lookup"><span data-stu-id="60122-122">32 bits</span></span> | <span data-ttu-id="60122-123">Não assinado</span><span class="sxs-lookup"><span data-stu-id="60122-123">Unsigned</span></span> |
| <span data-ttu-id="60122-124">**INT32**</span><span class="sxs-lookup"><span data-stu-id="60122-124">**INT32**</span></span>     | <span data-ttu-id="60122-125">32 bits</span><span class="sxs-lookup"><span data-stu-id="60122-125">32 bits</span></span> | <span data-ttu-id="60122-126">Com sinal</span><span class="sxs-lookup"><span data-stu-id="60122-126">Signed</span></span>   |
| <span data-ttu-id="60122-127">**INT64**</span><span class="sxs-lookup"><span data-stu-id="60122-127">**INT64**</span></span>     | <span data-ttu-id="60122-128">64 bits</span><span class="sxs-lookup"><span data-stu-id="60122-128">64 bits</span></span> | <span data-ttu-id="60122-129">Com sinal</span><span class="sxs-lookup"><span data-stu-id="60122-129">Signed</span></span>   |
| <span data-ttu-id="60122-130">**LONG**</span><span class="sxs-lookup"><span data-stu-id="60122-130">**LONG**</span></span>      | <span data-ttu-id="60122-131">32 bits</span><span class="sxs-lookup"><span data-stu-id="60122-131">32 bits</span></span> | <span data-ttu-id="60122-132">Com sinal</span><span class="sxs-lookup"><span data-stu-id="60122-132">Signed</span></span>   |
| <span data-ttu-id="60122-133">**LONGLONG**</span><span class="sxs-lookup"><span data-stu-id="60122-133">**LONGLONG**</span></span>  | <span data-ttu-id="60122-134">64 bits</span><span class="sxs-lookup"><span data-stu-id="60122-134">64 bits</span></span> | <span data-ttu-id="60122-135">Com sinal</span><span class="sxs-lookup"><span data-stu-id="60122-135">Signed</span></span>   |
| <span data-ttu-id="60122-136">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="60122-136">**UINT32**</span></span>    | <span data-ttu-id="60122-137">32 bits</span><span class="sxs-lookup"><span data-stu-id="60122-137">32 bits</span></span> | <span data-ttu-id="60122-138">Não assinado</span><span class="sxs-lookup"><span data-stu-id="60122-138">Unsigned</span></span> |
| <span data-ttu-id="60122-139">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="60122-139">**UINT64**</span></span>    | <span data-ttu-id="60122-140">64 bits</span><span class="sxs-lookup"><span data-stu-id="60122-140">64 bits</span></span> | <span data-ttu-id="60122-141">Não assinado</span><span class="sxs-lookup"><span data-stu-id="60122-141">Unsigned</span></span> |
| <span data-ttu-id="60122-142">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="60122-142">**ULONG**</span></span>     | <span data-ttu-id="60122-143">32 bits</span><span class="sxs-lookup"><span data-stu-id="60122-143">32 bits</span></span> | <span data-ttu-id="60122-144">Não assinado</span><span class="sxs-lookup"><span data-stu-id="60122-144">Unsigned</span></span> |
| <span data-ttu-id="60122-145">**ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="60122-145">**ULONGLONG**</span></span> | <span data-ttu-id="60122-146">64 bits</span><span class="sxs-lookup"><span data-stu-id="60122-146">64 bits</span></span> | <span data-ttu-id="60122-147">Não assinado</span><span class="sxs-lookup"><span data-stu-id="60122-147">Unsigned</span></span> |
| <span data-ttu-id="60122-148">**WORD**</span><span class="sxs-lookup"><span data-stu-id="60122-148">**WORD**</span></span>      | <span data-ttu-id="60122-149">16 bits</span><span class="sxs-lookup"><span data-stu-id="60122-149">16 bits</span></span> | <span data-ttu-id="60122-150">Não assinado</span><span class="sxs-lookup"><span data-stu-id="60122-150">Unsigned</span></span> |



 

<span data-ttu-id="60122-151">Como você pode ver, há uma certa quantidade de redundância nesses TYPEDEFs.</span><span class="sxs-lookup"><span data-stu-id="60122-151">As you can see, there is a certain amount of redundancy in these typedefs.</span></span> <span data-ttu-id="60122-152">Parte dessa sobreposição é simplesmente devido ao histórico das APIs do Windows.</span><span class="sxs-lookup"><span data-stu-id="60122-152">Some of this overlap is simply due to the history of the Windows APIs.</span></span> <span data-ttu-id="60122-153">Os tipos listados aqui têm tamanho fixo e os tamanhos são os mesmos nos aplicativos de 32 bits e 64.</span><span class="sxs-lookup"><span data-stu-id="60122-153">The types listed here have fixed size, and the sizes are the same in both 32-bit and 64-applications.</span></span> <span data-ttu-id="60122-154">Por exemplo, o tipo **DWORD** é sempre de 32 bits de largura.</span><span class="sxs-lookup"><span data-stu-id="60122-154">For example, the **DWORD** type is always 32 bits wide.</span></span>

### <a name="boolean-type"></a><span data-ttu-id="60122-155">Tipo booliano</span><span class="sxs-lookup"><span data-stu-id="60122-155">Boolean Type</span></span>

<span data-ttu-id="60122-156">**Bool** é um typedef para um valor inteiro que é usado em um contexto booliano.</span><span class="sxs-lookup"><span data-stu-id="60122-156">**BOOL** is a typedef for an integer value that is used in a Boolean context.</span></span> <span data-ttu-id="60122-157">O arquivo de cabeçalho WinDef. h também define dois valores para uso com **bool**.</span><span class="sxs-lookup"><span data-stu-id="60122-157">The header file WinDef.h also defines two values for use with **BOOL**.</span></span>


```C++
#define FALSE    0 
#define TRUE     1
```



<span data-ttu-id="60122-158">Apesar dessa definição de **true**, no entanto, a maioria das funções que retornam um tipo **bool** pode retornar qualquer valor diferente de zero para indicar a verdade booliana.</span><span class="sxs-lookup"><span data-stu-id="60122-158">Despite this definition of **TRUE**, however, most functions that return a **BOOL** type can return any non-zero value to indicate Boolean truth.</span></span> <span data-ttu-id="60122-159">Portanto, você deve sempre escrever isto:</span><span class="sxs-lookup"><span data-stu-id="60122-159">Therefore, you should always write this:</span></span>


```C++
// Right way.
BOOL result = SomeFunctionThatReturnsBoolean();
if (result) 
{ 
    ...
}
```



<span data-ttu-id="60122-160">e não isso:</span><span class="sxs-lookup"><span data-stu-id="60122-160">and not this:</span></span>


```C++
// Wrong!
if (result == TRUE) 
{
    ... 
}
```



<span data-ttu-id="60122-161">Lembre-se de que **bool** é um tipo inteiro e não é intercambiável com o tipo **booliano** de C++.</span><span class="sxs-lookup"><span data-stu-id="60122-161">Be aware that **BOOL** is an integer type and is not interchangeable with the C++ **bool** type.</span></span>

### <a name="pointer-types"></a><span data-ttu-id="60122-162">Tipos de ponteiro</span><span class="sxs-lookup"><span data-stu-id="60122-162">Pointer Types</span></span>

<span data-ttu-id="60122-163">O Windows define vários tipos de dados do formato *ponteiro-para-X*.</span><span class="sxs-lookup"><span data-stu-id="60122-163">Windows defines many data types of the form *pointer-to-X*.</span></span> <span data-ttu-id="60122-164">Normalmente, eles têm o prefixo *P-* ou *LP-* no nome.</span><span class="sxs-lookup"><span data-stu-id="60122-164">These usually have the prefix *P-* or *LP-* in the name.</span></span> <span data-ttu-id="60122-165">Por exemplo, **lpRect** é um ponteiro para um [**Rect**](/previous-versions//dd162897(v=vs.85)), onde **Rect** é uma estrutura que descreve um retângulo.</span><span class="sxs-lookup"><span data-stu-id="60122-165">For example, **LPRECT** is a pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)), where **RECT** is a structure that describes a rectangle.</span></span> <span data-ttu-id="60122-166">As seguintes declarações de variável são equivalentes.</span><span class="sxs-lookup"><span data-stu-id="60122-166">The following variable declarations are equivalent.</span></span>


```C++
RECT*  rect;  // Pointer to a RECT structure.
LPRECT rect;  // The same
PRECT  rect;  // Also the same.
```



<span data-ttu-id="60122-167">Historicamente, *P* significa "ponteiro" e *LP* significa "ponteiro longo".</span><span class="sxs-lookup"><span data-stu-id="60122-167">Historically, *P* stands for "pointer" and *LP* stands for "long pointer".</span></span> <span data-ttu-id="60122-168">Ponteiros longos (também chamados de *ponteiros distantes*) são um remanescente do Windows de 16 bits, quando eles eram necessários para endereçar os intervalos de memória fora do segmento atual.</span><span class="sxs-lookup"><span data-stu-id="60122-168">Long pointers (also called *far pointers*) are a holdover from 16-bit Windows, when they were needed to address memory ranges outside the current segment.</span></span> <span data-ttu-id="60122-169">O prefixo *LP* foi preservado para tornar mais fácil a porta de código de 16 bits para o Windows de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="60122-169">The *LP* prefix was preserved to make it easier to port 16-bit code to 32-bit Windows.</span></span> <span data-ttu-id="60122-170">Atualmente, não há distinção — um ponteiro é um ponteiro.</span><span class="sxs-lookup"><span data-stu-id="60122-170">Today there is no distinction — a pointer is a pointer.</span></span>

### <a name="pointer-precision-types"></a><span data-ttu-id="60122-171">Tipos de precisão de ponteiro</span><span class="sxs-lookup"><span data-stu-id="60122-171">Pointer Precision Types</span></span>

<span data-ttu-id="60122-172">Os seguintes tipos de dados são sempre o tamanho de um ponteiro — ou seja, 32 bits de largura em aplicativos de 32 bits e 64 bits de largura em aplicativos de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="60122-172">The following data types are always the size of a pointer—that is, 32 bits wide in 32-bit applications, and 64 bits wide in 64-bit applications.</span></span> <span data-ttu-id="60122-173">O tamanho é determinado no momento da compilação.</span><span class="sxs-lookup"><span data-stu-id="60122-173">The size is determined at compile time.</span></span> <span data-ttu-id="60122-174">Quando um aplicativo de 32 bits é executado em janelas de 64 bits, esses tipos de dados ainda têm 4 bytes de largura.</span><span class="sxs-lookup"><span data-stu-id="60122-174">When a 32-bit application runs on 64-bit Windows, these data types are still 4 bytes wide.</span></span> <span data-ttu-id="60122-175">(Um aplicativo de 64 bits não pode ser executado em janelas de 32 bits, portanto, a situação inversa não ocorre.)</span><span class="sxs-lookup"><span data-stu-id="60122-175">(A 64-bit application cannot run on 32-bit Windows, so the reverse situation does not occur.)</span></span>

-   <span data-ttu-id="60122-176">**PTR de DWORD \_**</span><span class="sxs-lookup"><span data-stu-id="60122-176">**DWORD\_PTR**</span></span>
-   <span data-ttu-id="60122-177">**INT \_ PTR**</span><span class="sxs-lookup"><span data-stu-id="60122-177">**INT\_PTR**</span></span>
-   <span data-ttu-id="60122-178">**\_PTR longo**</span><span class="sxs-lookup"><span data-stu-id="60122-178">**LONG\_PTR**</span></span>
-   <span data-ttu-id="60122-179">**\_ponteiro ULONG**</span><span class="sxs-lookup"><span data-stu-id="60122-179">**ULONG\_PTR**</span></span>
-   <span data-ttu-id="60122-180">**PTR-UINT \_**</span><span class="sxs-lookup"><span data-stu-id="60122-180">**UINT\_PTR**</span></span>

<span data-ttu-id="60122-181">Esses tipos são usados em situações em que um inteiro pode ser convertido em um ponteiro.</span><span class="sxs-lookup"><span data-stu-id="60122-181">These types are used in situations where an integer might be cast to a pointer.</span></span> <span data-ttu-id="60122-182">Eles também são usados para definir variáveis para aritmética de ponteiro e para definir contadores de loop que iteram em todo o intervalo de bytes em buffers de memória.</span><span class="sxs-lookup"><span data-stu-id="60122-182">They are also used to define variables for pointer arithmetic and to define loop counters that iterate over the full range of bytes in memory buffers.</span></span> <span data-ttu-id="60122-183">Em geral, eles aparecem em locais onde um valor de 32 bits existente foi expandido para 64 bits no Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="60122-183">More generally, they appear in places where an existing 32-bit value was expanded to 64 bits on 64-bit Windows.</span></span>

## <a name="hungarian-notation"></a><span data-ttu-id="60122-184">Notação húngaro</span><span class="sxs-lookup"><span data-stu-id="60122-184">Hungarian Notation</span></span>

<span data-ttu-id="60122-185">A *notação húngara* é a prática de adicionar prefixos aos nomes de variáveis, para fornecer informações adicionais sobre a variável.</span><span class="sxs-lookup"><span data-stu-id="60122-185">*Hungarian notation* is the practice of adding prefixes to the names of variables, to give additional information about the variable.</span></span> <span data-ttu-id="60122-186">(O inventário da notação, Charles Simonyi, foi o húngaro, portanto seu nome).</span><span class="sxs-lookup"><span data-stu-id="60122-186">(The notation's inventor, Charles Simonyi, was Hungarian, hence its name).</span></span>

<span data-ttu-id="60122-187">Em sua forma original, a notação húngara fornece informações *semânticas* sobre uma variável, informando o uso pretendido.</span><span class="sxs-lookup"><span data-stu-id="60122-187">In its original form, Hungarian notation gives *semantic* information about a variable, telling you the intended use.</span></span> <span data-ttu-id="60122-188">Por exemplo, *eu* significa um índice, *CB* significa um tamanho em bytes ("contagem de bytes") e números de linha e coluna médias de *RW* e *Col* .</span><span class="sxs-lookup"><span data-stu-id="60122-188">For example, *i* means an index, *cb* means a size in bytes ("count of bytes"), and *rw* and *col* mean row and column numbers.</span></span> <span data-ttu-id="60122-189">Esses prefixos são projetados para evitar o uso acidental de uma variável no contexto errado.</span><span class="sxs-lookup"><span data-stu-id="60122-189">These prefixes are designed to avoid the accidental use of a variable in the wrong context.</span></span> <span data-ttu-id="60122-190">Por exemplo, se você viu a expressão `rwPosition +  cbTable` , saberia que um número de linha está sendo adicionado a um tamanho, o que é quase certamente um bug no código</span><span class="sxs-lookup"><span data-stu-id="60122-190">For example, if you saw the expression `rwPosition +  cbTable`, you would know that a row number is being added to a size, which is almost certainly a bug in the code</span></span>

<span data-ttu-id="60122-191">Uma forma mais comum de notação húngara usa prefixos para fornecer informações de *tipo* , por exemplo, *DW* para **DWORD** e *w* para **Word**.</span><span class="sxs-lookup"><span data-stu-id="60122-191">A more common form of Hungarian notation uses prefixes to give *type* information—for example, *dw* for **DWORD** and *w* for **WORD**.</span></span>

<span data-ttu-id="60122-192">Se você pesquisar na Web "notação húngara", encontrará muitas opiniões sobre se a notação húngara é boa ou ruim.</span><span class="sxs-lookup"><span data-stu-id="60122-192">If you search the Web for "Hungarian notation," you will find a lot of opinions about whether Hungarian notation is good or bad.</span></span> <span data-ttu-id="60122-193">Alguns programadores têm uma aparência intensa para a notação húngara.</span><span class="sxs-lookup"><span data-stu-id="60122-193">Some programmers have an intense dislike for Hungarian notation.</span></span> <span data-ttu-id="60122-194">Outras pessoas acham útil.</span><span class="sxs-lookup"><span data-stu-id="60122-194">Others find it helpful.</span></span> <span data-ttu-id="60122-195">Independentemente disso, muitos dos exemplos de código no MSDN usam a notação húngara, mas você não precisa memorizar os prefixos para entender o código.</span><span class="sxs-lookup"><span data-stu-id="60122-195">Regardless, many of the code examples on MSDN use Hungarian notation, but you don't need to memorize the prefixes to understand the code.</span></span>

## <a name="next"></a><span data-ttu-id="60122-196">Avançar</span><span class="sxs-lookup"><span data-stu-id="60122-196">Next</span></span>

[<span data-ttu-id="60122-197">Trabalhando com cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="60122-197">Working with Strings</span></span>](working-with-strings.md)

 

 
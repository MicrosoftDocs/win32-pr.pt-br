---
title: Descritores de correlação
description: Um descritor de correlação é uma cadeia de caracteres de formato que descreve uma expressão baseada em um argumento relacionado a outro argumento.
ms.assetid: 9f5f5077-d6a9-4253-bddf-b8cd0c868973
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f13f0793b99b80b7abb0b493c249b30ad53d76
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823954"
---
# <a name="correlation-descriptors"></a><span data-ttu-id="485f2-103">Descritores de correlação</span><span class="sxs-lookup"><span data-stu-id="485f2-103">Correlation Descriptors</span></span>

<span data-ttu-id="485f2-104">Um descritor de correlação é uma cadeia de caracteres de formato que descreve uma expressão baseada em um argumento relacionado a outro argumento.</span><span class="sxs-lookup"><span data-stu-id="485f2-104">A correlation descriptor is a format string that describes an expression based on one argument related to another argument.</span></span> <span data-ttu-id="485f2-105">Um descritor de correlação é necessário para lidar com semânticas relacionadas a atributos como o \[ **tamanho \_ é ()** \] , \[ **length \_ is ()** \] , \[ **switch \_ is ()** \] e \[ **IID \_ is ()** \] .</span><span class="sxs-lookup"><span data-stu-id="485f2-105">A correlation descriptor is needed for handling semantics related to attributes like \[**size\_is()**\], \[**length\_is()**\], \[**switch\_is()**\] and \[**iid\_is()**\].</span></span> <span data-ttu-id="485f2-106">Os descritores de correlação são usados com matrizes, ponteiros de tamanho, uniões e ponteiros de interface.</span><span class="sxs-lookup"><span data-stu-id="485f2-106">Correlation descriptors are used with arrays, sized pointers, unions, and interface pointers.</span></span> <span data-ttu-id="485f2-107">O valor da expressão eventual pode ser um tamanho, um comprimento, um discriminante de União ou um ponteiro para um IID, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="485f2-107">The eventual expression value can be a size, a length, a union discriminant, or a pointer to an IID, respectively.</span></span> <span data-ttu-id="485f2-108">Em termos de cadeias de caracteres de formato, os descritores de correlação são usados com matrizes, uniões e ponteiros de interface.</span><span class="sxs-lookup"><span data-stu-id="485f2-108">In terms of format strings, correlation descriptors are used with arrays, unions, and interface pointers.</span></span> <span data-ttu-id="485f2-109">Um ponteiro de tamanho é descrito em Formatar cadeias de caracteres como um ponteiro para uma matriz.</span><span class="sxs-lookup"><span data-stu-id="485f2-109">A sized pointer is described in format strings as a pointer to an array.</span></span>

<span data-ttu-id="485f2-110">Há duas rotinas executando cálculos de expressão básicos: NdrpComputeConformance é usado para tamanhos, switches e IID \* enquanto NdrpComputeVariance é usado para comprimentos.</span><span class="sxs-lookup"><span data-stu-id="485f2-110">There are two routines performing basic expression calculations: NdrpComputeConformance is used for sizes, switches and IID\* while NdrpComputeVariance is used for lengths.</span></span> <span data-ttu-id="485f2-111">Também há uma única rotina para executar uma validação de valor de correlação para a funcionalidade de negação de ataque.</span><span class="sxs-lookup"><span data-stu-id="485f2-111">There is also a single routine to perform a correlation value validation for denial-of-attack functionality.</span></span>

<span data-ttu-id="485f2-112">Os descritores de correlação foram projetados para dar suporte apenas a expressões muito limitadas.</span><span class="sxs-lookup"><span data-stu-id="485f2-112">Correlation descriptors have been designed to support only very limited expressions.</span></span> <span data-ttu-id="485f2-113">Para situações complicadas, o compilador gera uma rotina de avaliação de expressão a ser chamada pelo mecanismo quando necessário.</span><span class="sxs-lookup"><span data-stu-id="485f2-113">For complicated situations, the compiler generates an expression evaluation routine to be called by the engine when needed.</span></span>

<span data-ttu-id="485f2-114">Um descritor de correlação tem o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="485f2-114">A correlation descriptor has the following format:</span></span>

``` syntax
correlation_type<1>
correlation_operator<1>
offset<2>
[robust_flags<2>]
```

<span data-ttu-id="485f2-115">O tipo de correlação do descritor de correlação \_<1> consiste em dois Nibbles: os quatro bits superiores descrevem onde a expressão pode ser encontrada e os quatro bits inferiores descrevem o tipo do valor da expressão.</span><span class="sxs-lookup"><span data-stu-id="485f2-115">The correlation descriptor correlation\_type<1> consists of two nibbles: the upper 4 bits describe where the expression can be found and the lower 4 bits describe the type of the expression value.</span></span>

<span data-ttu-id="485f2-116">O Nibble superior pode ter um destes cinco valores:</span><span class="sxs-lookup"><span data-stu-id="485f2-116">The upper nibble can have one of these five values:</span></span>

``` syntax
00  FC_NORMAL_CONFORMANCE
10  FC_POINTER_CONFORMANCE
20  FC_TOP_LEVEL_CONFORMANCE
80  FC_TOP_LEVEL_MULTID_CONFORMANCE
40  FC_CONSTANT_CONFORMANCE
```

<dl> <dt>

<span data-ttu-id="485f2-117"><span id="FC_NORMAL_CONFORMANCE"></span><span id="fc_normal_conformance"></span>\_conformidade normal com FC \_</span><span class="sxs-lookup"><span data-stu-id="485f2-117"><span id="FC_NORMAL_CONFORMANCE"></span><span id="fc_normal_conformance"></span>FC\_NORMAL\_CONFORMANCE</span></span>
</dt> <dd>

<span data-ttu-id="485f2-118">Um caso de conformidade normal, como o descrito em um campo de uma estrutura.</span><span class="sxs-lookup"><span data-stu-id="485f2-118">A normal case of conformance, such as that described in a field of a structure.</span></span>

</dd> <dt>

<span data-ttu-id="485f2-119"><span id="FC_POINTER_CONFORMANCE"></span><span id="fc_pointer_conformance"></span>\_conformidade do ponteiro FC \_</span><span class="sxs-lookup"><span data-stu-id="485f2-119"><span id="FC_POINTER_CONFORMANCE"></span><span id="fc_pointer_conformance"></span>FC\_POINTER\_CONFORMANCE</span></span>
</dt> <dd>

<span data-ttu-id="485f2-120">Para ponteiros atribuídos (o **tamanho \_ é ()**, **length \_ is ()**), que são campos em uma estrutura.</span><span class="sxs-lookup"><span data-stu-id="485f2-120">For attributed pointers (**size\_is()**, **length\_is()**) which are fields in a structure.</span></span> <span data-ttu-id="485f2-121">Isso afeta a maneira como o ponteiro de memória base é definido.</span><span class="sxs-lookup"><span data-stu-id="485f2-121">This affects the way the base memory pointer is set.</span></span>

</dd> <dt>

<span data-ttu-id="485f2-122"><span id="FC_TOP_LEVEL_CONFORMANCE"></span><span id="fc_top_level_conformance"></span>\_conformidade de \_ nível \_ superior de FC</span><span class="sxs-lookup"><span data-stu-id="485f2-122"><span id="FC_TOP_LEVEL_CONFORMANCE"></span><span id="fc_top_level_conformance"></span>FC\_TOP\_LEVEL\_CONFORMANCE</span></span>
</dt> <dd>

<span data-ttu-id="485f2-123">Para conformidade de nível superior descrita por outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="485f2-123">For top-level conformance described by another parameter.</span></span>

</dd> <dt>

<span data-ttu-id="485f2-124"><span id="FC_TOP_LEVEL_MULTID_CONFORMANCE"></span><span id="fc_top_level_multid_conformance"></span>\_ \_ conformidade múltipla de nível superior \_ de FC \_</span><span class="sxs-lookup"><span data-stu-id="485f2-124"><span id="FC_TOP_LEVEL_MULTID_CONFORMANCE"></span><span id="fc_top_level_multid_conformance"></span>FC\_TOP\_LEVEL\_MULTID\_CONFORMANCE</span></span>
</dt> <dd>

<span data-ttu-id="485f2-125">Para conformidade de nível superior de uma matriz multidimensional descrita por outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="485f2-125">For top-level conformance of a multidimensional array described by another parameter.</span></span>

> [!Note]  
> <span data-ttu-id="485f2-126">Os ponteiros e as matrizes com dimensionamento multidimensional disparam um comutador para [**– Oicf**](/windows/desktop/Midl/-oi).</span><span class="sxs-lookup"><span data-stu-id="485f2-126">Multidimensional sized arrays and pointers trigger a switch to [**–Oicf**](/windows/desktop/Midl/-oi).</span></span>

 

</dd> <dt>

<span data-ttu-id="485f2-127"><span id="FC_CONSTANT_CONFORMANCE"></span><span id="fc_constant_conformance"></span>\_conformidade da constante de FC \_</span><span class="sxs-lookup"><span data-stu-id="485f2-127"><span id="FC_CONSTANT_CONFORMANCE"></span><span id="fc_constant_conformance"></span>FC\_CONSTANT\_CONFORMANCE</span></span>
</dt> <dd>

<span data-ttu-id="485f2-128">Para um valor constante.</span><span class="sxs-lookup"><span data-stu-id="485f2-128">For a constant value.</span></span> <span data-ttu-id="485f2-129">O compilador precalcula o valor de uma expressão constante fornecida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="485f2-129">The compiler precalculates the value from a constant expression supplied by the user.</span></span> <span data-ttu-id="485f2-130">Quando esse for o caso, os 3 bytes subsequentes na descrição de conformidade conterão os 3 bytes inferiores de um longo que descreve o tamanho de conformidade.</span><span class="sxs-lookup"><span data-stu-id="485f2-130">When this is the case, the subsequent 3 bytes in the conformance description contain the lower 3 bytes of a long describing the conformance size.</span></span> <span data-ttu-id="485f2-131">Nenhuma computação adicional é necessária.</span><span class="sxs-lookup"><span data-stu-id="485f2-131">No further computation is required.</span></span>

</dd> </dl>

<span data-ttu-id="485f2-132">O Nibble inferior fornece o tipo do valor que precisa ser extraído da memória:</span><span class="sxs-lookup"><span data-stu-id="485f2-132">The lower nibble gives the type of the value that needs to be extracted from memory:</span></span>

``` syntax
FC_LONG | FC_ULONG | 
FC_SHORT | FC_USHORT | 
FC_SMALL | FC_USMALL | 
FC_HYPER
```

> [!Note]
> <span data-ttu-id="485f2-133">Não há suporte para expressões de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="485f2-133">64-bit expressions are not supported.</span></span> <span data-ttu-id="485f2-134">O FC \_ Hyper é usado apenas para **IID \_ é ()** em plataformas de 64 bits para extrair o valor do ponteiro para IID \* .</span><span class="sxs-lookup"><span data-stu-id="485f2-134">FC\_HYPER is used only for **iid\_is()** on 64-bit platforms to extract the pointer value for IID\*.</span></span>
>
> <span data-ttu-id="485f2-135">O compilador define o tipo Nibble como zero para os seguintes casos: expressão constante mencionada acima e quando a rotina de expressão de avaliação precisa ser chamada, por exemplo, quando a conformidade com a \_ constante FC \_ e o \_ retorno de chamada FC são usados.</span><span class="sxs-lookup"><span data-stu-id="485f2-135">The compiler sets the type nibble to zero for the following cases: constant expression mentioned above and when evaluation expression routine needs to be called, for example, when FC\_CONSTANT\_CONFORMANCE and FC\_CALLBACK are used.</span></span>

 

<span data-ttu-id="485f2-136">O tamanho \_ é \_ op<1> campo permite que uma das seguintes operações seja aplicada à variável de conformidade:</span><span class="sxs-lookup"><span data-stu-id="485f2-136">The size\_is\_op<1> field allows for one of the following operations to be applied to the conformance variable:</span></span>

``` syntax
FC_DEREFERENCE | 
FC_DIV_2 | FC_MULT_2 | FC_SUB_1 | FC_ADD_1 | 
FC_CALLBACK
```

<span data-ttu-id="485f2-137">A \_ constante de desreferência de FC é usada para que a correlação seja um ponto, como para o **\[ tamanho \_ é ( \* pl) \]**.</span><span class="sxs-lookup"><span data-stu-id="485f2-137">The FC\_DEREFERENCE constant is used for correlation being a pointee, like for **\[size\_is(\*pL)\]**.</span></span> <span data-ttu-id="485f2-138">Os operadores aritméticos usam apenas a constante indicada.</span><span class="sxs-lookup"><span data-stu-id="485f2-138">Arithmetic operators just use the indicated constant.</span></span> <span data-ttu-id="485f2-139">A \_ constante de retorno de chamada FC indica que uma rotina de avaliação de expressão precisa ser chamada.</span><span class="sxs-lookup"><span data-stu-id="485f2-139">The FC\_CALLBACK constant indicates that an expression evaluation routine needs to be called.</span></span>

<span data-ttu-id="485f2-140">O campo deslocamento<2> normalmente é um deslocamento de memória relativo para a variável de argumento de expressão.</span><span class="sxs-lookup"><span data-stu-id="485f2-140">The offset<2> field is typically a relative memory offset to the expression argument variable.</span></span> <span data-ttu-id="485f2-141">Ele também pode ser uma avaliação de expressão – índice de rotina.</span><span class="sxs-lookup"><span data-stu-id="485f2-141">It can also be an expression evaluation–routine index.</span></span> <span data-ttu-id="485f2-142">Conforme mencionado anteriormente neste documento, para expressões constantes ele faz parte do valor real e final da expressão.</span><span class="sxs-lookup"><span data-stu-id="485f2-142">As mentioned previously in this document, for constant expressions it is a part of actual, final expression value.</span></span>

<span data-ttu-id="485f2-143">A interpretação do deslocamento<2> campo como deslocamento de memória depende da complexidade da expressão, do local da variável de expressão e, no caso de uma matriz, se a matriz é, na verdade, um ponteiro atribuído.</span><span class="sxs-lookup"><span data-stu-id="485f2-143">The interpretation of the offset<2> field as memory offset depends on the complexity of the expression, the location of the expression variable, and in the case of an array, whether the array is actually an attributed pointer.</span></span>

<span data-ttu-id="485f2-144">Se a matriz for um ponteiro atribuído e a variável de conformidade for um campo em uma estrutura, o campo de deslocamento conterá o deslocamento do início da estrutura até o campo conformidade-descrição.</span><span class="sxs-lookup"><span data-stu-id="485f2-144">If the array is an attributed pointer and the conformance variable is a field in a structure, the offset field contains the offset from the beginning of the structure to the conformance-describing field.</span></span> <span data-ttu-id="485f2-145">Se a matriz não for um ponteiro atribuído e a variável de conformidade for um campo em uma estrutura, o campo de deslocamento conterá o deslocamento do final da parte não compatível da estrutura para o campo conformidade-descrever.</span><span class="sxs-lookup"><span data-stu-id="485f2-145">If the array is not an attributed pointer and the conformance variable is a field in a structure, the offset field contains the offset from the end of the nonconformant part of the structure to the conformance-describing field.</span></span> <span data-ttu-id="485f2-146">Normalmente, a matriz em conformidade está no final da estrutura.</span><span class="sxs-lookup"><span data-stu-id="485f2-146">Typically, the conformant array is at the end of the structure.</span></span>

<span data-ttu-id="485f2-147">Para conformidade de nível superior, o campo de deslocamento contém o deslocamento do local do primeiro parâmetro do stub na pilha para o parâmetro que descreve a conformidade.</span><span class="sxs-lookup"><span data-stu-id="485f2-147">For top-level conformance, the offset field contains the offset from the stub's first parameter's location on the stack to the parameter that describes the conformance.</span></span> <span data-ttu-id="485f2-148">Isso não é usado no modo **– os** .</span><span class="sxs-lookup"><span data-stu-id="485f2-148">This is not used in **–Os** mode.</span></span> <span data-ttu-id="485f2-149">Há outras exceções à interpretação do campo de deslocamento; essas exceções são descritas na descrição desses tipos.</span><span class="sxs-lookup"><span data-stu-id="485f2-149">There are other exceptions to the interpretation of the offset field; such exceptions are described in the description of those types.</span></span>

<span data-ttu-id="485f2-150">Quando o deslocamento<2> é usado com \_ o retorno de chamada FC, ele contém um índice na tabela de rotina de avaliação de expressão gerada pelo compilador.</span><span class="sxs-lookup"><span data-stu-id="485f2-150">When offset<2> is used with FC\_CALLBACK, it contains an index in the expression evaluation routine table generated by the compiler.</span></span> <span data-ttu-id="485f2-151">A mensagem de stub é passada para a rotina de avaliação, que computa o valor de conformidade e o atribui ao campo MaxCount da mensagem de stub.</span><span class="sxs-lookup"><span data-stu-id="485f2-151">The stub message is passed to the evaluation routine, which then computes the conformance value and assigns it to the MaxCount field of the stub message.</span></span>

<span data-ttu-id="485f2-152">O campo de sinalizadores robustos \_<2> foi adicionado ao Windows 2000 para dar suporte a [**/robust**](/windows/desktop/Midl/-robust), como o recurso de negação de ataques.</span><span class="sxs-lookup"><span data-stu-id="485f2-152">The robust\_flags<2> field has been added for Windows 2000 to support [**/robust**](/windows/desktop/Midl/-robust), such as the denial-of-attacks feature.</span></span> <span data-ttu-id="485f2-153">Os seguintes sinalizadores são definidos no primeiro byte:</span><span class="sxs-lookup"><span data-stu-id="485f2-153">The following flags are defined on the first byte:</span></span>

``` syntax
typedef  struct  _NDR_CORRELATION_FLAGS
  {
  unsigned char   Early     : 1;
  unsigned char   Split     : 1;
  unsigned char   IsIidIs   : 1;
  unsigned char   DontCheck : 1;
  unsigned char   Unused    : 4;
  } NDR_CORRELATION_FLAGS;
```

<span data-ttu-id="485f2-154">O sinalizador inicial indica a correlação antecipada versus tardia.</span><span class="sxs-lookup"><span data-stu-id="485f2-154">The Early flag indicates early versus late correlation.</span></span> <span data-ttu-id="485f2-155">Uma correlação inicial é quando o argumento da expressão precede o argumento descrito, por exemplo, um argumento de tamanho é anterior a um argumento de ponteiro de tamanho.</span><span class="sxs-lookup"><span data-stu-id="485f2-155">An early correlation is when the expression argument precedes the described argument, for example a size argument is before a sized pointer argument.</span></span> <span data-ttu-id="485f2-156">Uma correlação tardia é quando o argumento da expressão vem após o argumento relacionado.</span><span class="sxs-lookup"><span data-stu-id="485f2-156">A late correlation is when the expression argument comes after the related argument.</span></span> <span data-ttu-id="485f2-157">O mecanismo executa a validação dos valores de correlação iniciais imediatamente, os valores de correlação tardias são armazenados para verificação após a conclusão do desempacotamento.</span><span class="sxs-lookup"><span data-stu-id="485f2-157">The engine performs validation of early correlation values right away, the late correlation values are stored for checking after unmarshaling is done.</span></span>

<span data-ttu-id="485f2-158">O sinalizador Split indica uma divisão assíncrona entre os \[ \] argumentos in e \[ out \] .</span><span class="sxs-lookup"><span data-stu-id="485f2-158">The Split flag indicates an async split among \[in\] and \[out\] arguments.</span></span> <span data-ttu-id="485f2-159">Por exemplo, um argumento de tamanho pode estar \[ no \] enquanto o ponteiro de tamanho pode estar \[ fora \] .</span><span class="sxs-lookup"><span data-stu-id="485f2-159">For example, a size argument may be \[in\] while the sized pointer may be \[out\].</span></span> <span data-ttu-id="485f2-160">No contexto assíncrono do DCOM, esses argumentos ocorrem em pilhas diferentes, portanto, o mecanismo deve estar ciente disso.</span><span class="sxs-lookup"><span data-stu-id="485f2-160">In the DCOM async context, these arguments happen to be on different stacks, so the engine must be aware of this.</span></span>

<span data-ttu-id="485f2-161">O sinalizador IsIidIs indica uma correlação de **IID \_ ()** .</span><span class="sxs-lookup"><span data-stu-id="485f2-161">The IsIidIs flag indicates an **iid\_is()** correlation.</span></span> <span data-ttu-id="485f2-162">A rotina NdrComputeConformance é induzida a obter um ponteiro para o IID como um valor de expressão, mas a rotina de validação não pode comparar esses valores (eles seriam ponteiros) e, portanto, o sinalizador indica que o IIDs real precisa ser comparado.</span><span class="sxs-lookup"><span data-stu-id="485f2-162">The NdrComputeConformance routine is tricked to obtain a pointer to IID as an expression value, but the validation routine cannot compare such values (they would be pointers) and so the flag indicates that actual IIDs need to be compared.</span></span>

### <a name="variance-description-and-other-array-attributes"></a><span data-ttu-id="485f2-163">Descrição da variância e outros atributos de matriz</span><span class="sxs-lookup"><span data-stu-id="485f2-163">Variance Description and Other Array Attributes</span></span>

<span data-ttu-id="485f2-164">O formato do campo de descrição da variação é idêntico ao campo de descrição de conformidade.</span><span class="sxs-lookup"><span data-stu-id="485f2-164">The variance description field format is identical to the conformance description field.</span></span> <span data-ttu-id="485f2-165">A diferença é que um campo de mensagem de stub diferente é usado pelo mecanismo de NDR como uma variável temporária.</span><span class="sxs-lookup"><span data-stu-id="485f2-165">The difference is that a different stub message field is used by the NDR engine as a temporary variable.</span></span> <span data-ttu-id="485f2-166">No caso da descrição da variação, é o comprimento que é avaliado e o campo correspondente é chamado de ActualLength.</span><span class="sxs-lookup"><span data-stu-id="485f2-166">In the case of variance description, it is the length that is evaluated and the corresponding field is called ActualLength.</span></span>

<span data-ttu-id="485f2-167">Com a variação, o deslocamento inicial geralmente é zero e o mecanismo é ajustado de acordo.</span><span class="sxs-lookup"><span data-stu-id="485f2-167">With variance, the starting offset is typically zero and the engine is tuned accordingly.</span></span> <span data-ttu-id="485f2-168">Se o **primeiro atributo \_ is ()** for aplicado a uma matriz de variação em conformidade, um retorno de chamada para uma rotina de avaliação de expressão será forçado.</span><span class="sxs-lookup"><span data-stu-id="485f2-168">If the **first\_is()** attribute is applied to a conformant varying array, a callback to an expression evaluation routine is forced.</span></span>

 

 
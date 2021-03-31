---
title: Atributo size_is
description: Use o atributo \ Size \_ is \ para especificar o tamanho da memória, em elementos, alocados para ponteiros de tamanho, ponteiros de tamanho para ponteiros de tamanho e matrizes de dimensão única ou multidimensionais.
ms.assetid: 1f3f3629-f668-460d-86fd-16ef22449973
keywords:
- size_is do atributo MIDL
topic_type:
- apiref
api_name:
- size_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f65a4c3ea93ea9ed55ce4f6f9ce846c81b60fa40
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640511"
---
# <a name="size_is-attribute"></a><span data-ttu-id="27c01-104">o tamanho \_ é atributo</span><span class="sxs-lookup"><span data-stu-id="27c01-104">size\_is attribute</span></span>

<span data-ttu-id="27c01-105">Use o \[ **atributo \_ tamanho** \] para especificar o tamanho da memória, em elementos, alocados para ponteiros de tamanho, ponteiros de tamanho para ponteiros de tamanho e matrizes de dimensão única ou multidimensional.</span><span class="sxs-lookup"><span data-stu-id="27c01-105">Use the \[**size\_is**\] attribute to specify the size of memory, in elements, allocated for sized pointers, sized pointers to sized pointers, and single- or multidimensional arrays.</span></span>

``` syntax
[ size_is(limited-expression-list) ]
```

## <a name="parameters"></a><span data-ttu-id="27c01-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="27c01-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27c01-107">*lista de expressões limitadas*</span><span class="sxs-lookup"><span data-stu-id="27c01-107">*limited-expression-list*</span></span> 
</dt> <dd>

<span data-ttu-id="27c01-108">Especifica uma ou mais expressões de linguagem C.</span><span class="sxs-lookup"><span data-stu-id="27c01-108">Specifies one or more C-language expressions.</span></span> <span data-ttu-id="27c01-109">Cada expressão é avaliada como um inteiro não negativo que representa a quantidade de memória alocada a um ponteiro de tamanho ou uma matriz.</span><span class="sxs-lookup"><span data-stu-id="27c01-109">Each expression evaluates to a non-negative integer that represents the amount of memory allocated to a sized pointer or an array.</span></span> <span data-ttu-id="27c01-110">No caso de uma matriz, especifica uma única expressão que representa o tamanho da alocação, em elementos, da primeira dimensão dessa matriz.</span><span class="sxs-lookup"><span data-stu-id="27c01-110">In the case of an array, specifies a single expression that represents the allocation size, in elements, of the first dimension of that array.</span></span> <span data-ttu-id="27c01-111">O compilador MIDL oferece suporte a expressões condicionais, expressões lógicas, expressões relacionais e expressões aritméticas.</span><span class="sxs-lookup"><span data-stu-id="27c01-111">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="27c01-112">MIDL não permite invocações de função em expressões e não permite operadores de incremento e decréscimo.</span><span class="sxs-lookup"><span data-stu-id="27c01-112">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span> <span data-ttu-id="27c01-113">Use vírgulas como espaços reservados para parâmetros implícitos ou para separar várias expressões.</span><span class="sxs-lookup"><span data-stu-id="27c01-113">Use commas as placeholders for implicit parameters, or to separate multiple expressions.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="27c01-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="27c01-114">Remarks</span></span>

<span data-ttu-id="27c01-115">Se você estiver usando o \[ **atributo \_ size** \] para alocar memória para uma matriz multidimensional e estiver usando a \[ \] notação de matriz, lembre-se de que apenas a primeira dimensão de uma matriz multidimensional pode ser determinada dinamicamente em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="27c01-115">If you are using the \[**size\_is**\] attribute to allocate memory for a multidimensional array and you are using array \[ \] notation, keep in mind that only the first dimension of a multidimensional array can be dynamically determined at run time.</span></span> <span data-ttu-id="27c01-116">As outras dimensões devem ser especificadas estaticamente.</span><span class="sxs-lookup"><span data-stu-id="27c01-116">The other dimensions must be statically specified.</span></span> <span data-ttu-id="27c01-117">Para obter mais informações sobre como usar o \[ **tamanho \_ é** o \] atributo com vários níveis de ponteiros para permitir que um servidor retorne uma matriz de dados de tamanho dinâmico para um cliente, como mostrado no exemplo Proc7, consulte [vários níveis de ponteiros](/windows/desktop/Rpc/multiple-levels-of-pointers).</span><span class="sxs-lookup"><span data-stu-id="27c01-117">For more information on using the \[**size\_is**\] attribute with multiple levels of pointers to enable a server to return a dynamically-sized array of data to a client, as shown in the example Proc7, see [Multiple Levels of Pointers](/windows/desktop/Rpc/multiple-levels-of-pointers).</span></span>

<span data-ttu-id="27c01-118">Você pode usar o \[ **tamanho \_** \] ou o [**máximo \_ é**](max-is.md) (mas não ambos na mesma lista de atributos) para especificar o tamanho de uma matriz cujos limites superiores são determinados em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="27c01-118">You can use either \[**size\_is**\] or [**max\_is**](max-is.md) (but not both in the same attribute list) to specify the size of an array whose upper bounds are determined at run time.</span></span> <span data-ttu-id="27c01-119">Observe, no entanto, que o \[ atributo **Size \_ is** \] não pode ser usado em dimensões de matriz que são fixas.</span><span class="sxs-lookup"><span data-stu-id="27c01-119">Note, however, that the \[**size\_is**\] attribute cannot be used on array dimensions that are fixed.</span></span> <span data-ttu-id="27c01-120">O \[ atributo **Max \_ is** \] especifica o índice de matriz válido máximo.</span><span class="sxs-lookup"><span data-stu-id="27c01-120">The \[**max\_is**\] attribute specifies the maximum valid array index.</span></span> <span data-ttu-id="27c01-121">Como resultado, especificar \[ Size \_ é (n) \] equivale a especificar \[ Max \_ é (n-1) \] .</span><span class="sxs-lookup"><span data-stu-id="27c01-121">As a result, specifying \[size\_is(n)\] is equivalent to specifying \[max\_is(n-1)\].</span></span>

<span data-ttu-id="27c01-122">Um \[ [](in.md) \] parâmetro de \[ matriz em [](out-idl.md) \] conformidade com ou para fora, com o atributo de \[ [**cadeia de caracteres**](string.md) , \] não precisa ter o \[ **tamanho \_** \] ou o \[ atributo [**máximo \_ é**](max-is.md) \] .</span><span class="sxs-lookup"><span data-stu-id="27c01-122">An \[ [**in**](in.md)\] or \[in, [**out**](out-idl.md)\] conformant-array parameter with the \[ [**string**](string.md)\] attribute need not have the \[**size\_is**\] or \[[**max\_is**](max-is.md)\] attribute.</span></span> <span data-ttu-id="27c01-123">Nesse caso, o tamanho da alocação é determinado do terminador nulo da cadeia de caracteres de entrada.</span><span class="sxs-lookup"><span data-stu-id="27c01-123">In this case, the size of the allocation is determined from the NULL terminator of the input string.</span></span> <span data-ttu-id="27c01-124">Todas as outras matrizes em conformidade com o \[ atributo de cadeia de caracteres \] devem ter um \[ atributo **Size \_** \] ou \[ **Max \_ is** \] .</span><span class="sxs-lookup"><span data-stu-id="27c01-124">All other conformant arrays with the \[string\] attribute must have a \[**size\_is**\] or \[**max\_is**\] attribute.</span></span>

<span data-ttu-id="27c01-125">Embora seja legal usar o \[ **tamanho \_** do \] atributo com uma constante, fazer isso é ineficiente e desnecessário.</span><span class="sxs-lookup"><span data-stu-id="27c01-125">While it is legal to use the \[**size\_is**\] attribute with a constant, doing so is inefficient and unnecessary.</span></span> <span data-ttu-id="27c01-126">Por exemplo, use uma matriz de tamanho fixo:</span><span class="sxs-lookup"><span data-stu-id="27c01-126">For example, use a fixed size array:</span></span>

``` syntax
HRESULT Proc3([in] short Arr[MAX_SIZE]);
```

<span data-ttu-id="27c01-127">em vez de:</span><span class="sxs-lookup"><span data-stu-id="27c01-127">instead of:</span></span>

``` syntax
// legal but marshaling code is much slower
HRESULT Proc3([in size_is(MAX_SIZE)] short Arr[] );
```

<span data-ttu-id="27c01-128">Você pode usar o \[ **tamanho \_** \] e o \[ [**comprimento \_ são**](length-is.md) \] atributos juntos.</span><span class="sxs-lookup"><span data-stu-id="27c01-128">You can use the \[**size\_is**\] and \[[**length\_is**](length-is.md)\] attributes together.</span></span> <span data-ttu-id="27c01-129">Quando você fizer isso, o \[ atributo **\_ size** \] controlará a quantidade de memória alocada para os dados.</span><span class="sxs-lookup"><span data-stu-id="27c01-129">When you do, the \[**size\_is**\] attribute controls the amount of memory allocated for the data.</span></span> <span data-ttu-id="27c01-130">O \[ **tamanho \_ é** \] atributo especifica quantos elementos são transmitidos.</span><span class="sxs-lookup"><span data-stu-id="27c01-130">The \[**length\_is**\] attribute specifies how many elements are transmitted.</span></span> <span data-ttu-id="27c01-131">A quantidade de memória especificada pelo \[ **tamanho \_ é** \] e o \[ **comprimento \_** dos \] atributos não precisam ser iguais.</span><span class="sxs-lookup"><span data-stu-id="27c01-131">The amount of memory specified by the \[**size\_is**\] and \[**length\_is**\] attributes need not be the same.</span></span> <span data-ttu-id="27c01-132">Por exemplo, o cliente pode passar um \[ parâmetro de entrada \] para um servidor e especificar uma grande alocação de memória com \[ **tamanho \_** \] , embora especifique um pequeno número de elementos de dados a serem passados com \[ **\_ comprimento** \] .</span><span class="sxs-lookup"><span data-stu-id="27c01-132">For instance, your client may pass an \[in,out\] parameter to a server and specify a large memory allocation with \[**size\_is**\], even though it specifies a small number of data elements to be passed with \[**length\_is**\].</span></span> <span data-ttu-id="27c01-133">Isso permite que o servidor preencha a matriz com mais dados do que ele recebeu, o que pode então enviar de volta para o cliente.</span><span class="sxs-lookup"><span data-stu-id="27c01-133">This enables the server to fill the array with more data than it received, which it can then send back to the client.</span></span>

<span data-ttu-id="27c01-134">Em geral, não é útil especificar o \[ **tamanho \_** \] e o \[ [**comprimento \_ está**](length-is.md) \] nos \[ parâmetros in \] ou \[ out \] .</span><span class="sxs-lookup"><span data-stu-id="27c01-134">In general, it isn't useful to specify both \[**size\_is**\] and \[[**length\_is**](length-is.md)\] on \[in\] or \[out\] parameters.</span></span> <span data-ttu-id="27c01-135">Em ambos os casos, o \[ **tamanho \_ é** \] controlar a alocação de memória.</span><span class="sxs-lookup"><span data-stu-id="27c01-135">In both cases, \[**size\_is**\] controls memory allocation.</span></span> <span data-ttu-id="27c01-136">Seu aplicativo pode usar o \[ **tamanho \_** \] para alocar mais elementos de matriz do que transmitidos (conforme especificado pelo \[ **comprimento \_** \] ).</span><span class="sxs-lookup"><span data-stu-id="27c01-136">Your application could use \[**size\_is**\] to allocate more array elements than it transmits (as specified by \[**length\_is**\]).</span></span> <span data-ttu-id="27c01-137">No entanto, isso seria ineficiente.</span><span class="sxs-lookup"><span data-stu-id="27c01-137">However, this would be inefficient.</span></span> <span data-ttu-id="27c01-138">Também seria ineficiente especificar valores idênticos para o \[ **tamanho \_** \] e o \[ **comprimento \_ é** \] .</span><span class="sxs-lookup"><span data-stu-id="27c01-138">It would also be inefficient to specify identical values for \[**size\_is**\] and \[**length\_is**\].</span></span> <span data-ttu-id="27c01-139">Ele criaria uma sobrecarga extra durante o marshaling do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="27c01-139">It would create extra overhead during parameter marshaling.</span></span> <span data-ttu-id="27c01-140">Se os valores de \[ **tamanho \_** \] e \[ **comprimento \_** \] forem sempre iguais, omita o \[ **comprimento \_ é** \] atributo.</span><span class="sxs-lookup"><span data-stu-id="27c01-140">If the values of \[**size\_is**\] and \[**length\_is**\] are always the same, omit the \[**length\_is**\] attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="27c01-141">Exemplos</span><span class="sxs-lookup"><span data-stu-id="27c01-141">Examples</span></span>

``` syntax
HRESULT Proc1(
    [in] short m;
    [in, size_is(m)] short a[]);  // If m = 10, a[10]
HRESULT Proc2(
    [in] short m;
    [in, size_is(m)] short b[][20]);  // If m = 10, b[10][20]
HRESULT Proc3(
    [in] short m;
    [size_is(m)] short * pshort); /* Specifies a pointer
                                  to an m-sized block of shorts */
HRESULT Proc4(
    [in] short m;
    [size_is( , m)] short ** ppshort); /* Specifies a pointer 
                                       to a pointer to an m-sized 
                                       block of shorts */
HRESULT Proc5(
    [in] short m;
    [size_is(m ,)] short ** ppshort); /* Specifies an
                                      m-sized block of pointers 
                                      to shorts */
HRESULT Proc6(
    [in] short m;
    [in] short n;
    [size_is(m,n)] short ** ppshort); /* Specifies a pointer to an 
                                      m-sized block of pointers, each 
                                      of which points to an n-sized 
                                      block of shorts. m associates with
                                      the pointer closeest to the identifer
                                      it decorates. n associates with rest.*/
 HRESULT Proc7(
     [out] long  * pSize,
     [out, size_is( , *pSize)] my_type ** ppMyType); /* Specifies a pointer 
                                              to a sized pointer, 
                                              which points to a block 
                                              of my_types, whose size is
                                              unknown when the stub 
                                              calls the server. */
```

## <a name="see-also"></a><span data-ttu-id="27c01-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="27c01-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27c01-143">**Storage**</span><span class="sxs-lookup"><span data-stu-id="27c01-143">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="27c01-144">Atributos de campo</span><span class="sxs-lookup"><span data-stu-id="27c01-144">Field Attributes</span></span>](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[<span data-ttu-id="27c01-145">**primeiro \_ é**</span><span class="sxs-lookup"><span data-stu-id="27c01-145">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="27c01-146">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="27c01-146">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="27c01-147">**no**</span><span class="sxs-lookup"><span data-stu-id="27c01-147">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="27c01-148">**último \_ é**</span><span class="sxs-lookup"><span data-stu-id="27c01-148">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="27c01-149">**comprimento \_ é**</span><span class="sxs-lookup"><span data-stu-id="27c01-149">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="27c01-150">**máximo \_ é**</span><span class="sxs-lookup"><span data-stu-id="27c01-150">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="27c01-151">**mín. \_ é**</span><span class="sxs-lookup"><span data-stu-id="27c01-151">**min\_is**</span></span>](min-is.md)
</dt> <dt>

[<span data-ttu-id="27c01-152">**fora**</span><span class="sxs-lookup"><span data-stu-id="27c01-152">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="27c01-153">**Strings**</span><span class="sxs-lookup"><span data-stu-id="27c01-153">**string**</span></span>](string.md)
</dt> </dl>

 

 
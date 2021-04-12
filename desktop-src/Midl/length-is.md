---
title: Atributo length_is
description: O atributo \ length \_ is \ especifica o número de elementos da matriz a serem transmitidos. Você deve especificar um valor não negativo.
ms.assetid: 060dbd4a-3078-4050-abfe-c1b633c06861
keywords:
- length_is do atributo MIDL
topic_type:
- apiref
api_name:
- length_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fac217bae01c6896c7dadd36bb18f15e425a0427
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104454046"
---
# <a name="length_is-attribute"></a><span data-ttu-id="0c90c-105">comprimento \_ é atributo</span><span class="sxs-lookup"><span data-stu-id="0c90c-105">length\_is attribute</span></span>

<span data-ttu-id="0c90c-106">O **\[ tamanho \_ é \]** atributo especifica o número de elementos da matriz a serem transmitidos.</span><span class="sxs-lookup"><span data-stu-id="0c90c-106">The **\[length\_is\]** attribute specifies the number of array elements to be transmitted.</span></span> <span data-ttu-id="0c90c-107">Você deve especificar um valor não negativo.</span><span class="sxs-lookup"><span data-stu-id="0c90c-107">You must specify a non-negative value.</span></span>

``` syntax
[length_is( limited-expression-list )]
```

## <a name="parameters"></a><span data-ttu-id="0c90c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0c90c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c90c-109">*lista de expressões limitadas*</span><span class="sxs-lookup"><span data-stu-id="0c90c-109">*limited-expression-list*</span></span> 
</dt> <dd>

<span data-ttu-id="0c90c-110">Especifica uma ou mais expressões de linguagem C.</span><span class="sxs-lookup"><span data-stu-id="0c90c-110">Specifies one or more C-language expressions.</span></span> <span data-ttu-id="0c90c-111">Cada expressão é avaliada como um inteiro que representa o número de elementos da matriz a serem transmitidos.</span><span class="sxs-lookup"><span data-stu-id="0c90c-111">Each expression evaluates to an integer that represents the number of array elements to be transmitted.</span></span> <span data-ttu-id="0c90c-112">O compilador MIDL oferece suporte a expressões condicionais, expressões lógicas, expressões relacionais e expressões aritméticas.</span><span class="sxs-lookup"><span data-stu-id="0c90c-112">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="0c90c-113">MIDL não permite invocações de função em expressões e não permite operadores de incremento e decréscimo.</span><span class="sxs-lookup"><span data-stu-id="0c90c-113">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span> <span data-ttu-id="0c90c-114">Separe várias expressões com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="0c90c-114">Separate multiple expressions with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c90c-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c90c-115">Remarks</span></span>

<span data-ttu-id="0c90c-116">O **\[ tamanho \_ é \]** o atributo determina o valor dos índices de matriz correspondentes ao **\[** [**\_**](last-is.md) **\]** **\[ \_ \]** último atributo é quando o último não é especificado.</span><span class="sxs-lookup"><span data-stu-id="0c90c-116">The **\[length\_is\]** attribute determines the value of the array indexes corresponding to the **\[**[**last\_is**](last-is.md)**\]** attribute when **\[last\_is\]** is not specified.</span></span> <span data-ttu-id="0c90c-117">A relação entre esses índices de matriz é a seguinte: comprimento = último-primeiro + 1.</span><span class="sxs-lookup"><span data-stu-id="0c90c-117">The relationship between these array indexes is as follows: length = last - first + 1.</span></span>

<span data-ttu-id="0c90c-118">O **\[ \_ tamanho \]** do atributo não pode ser usado ao mesmo tempo que o **\[** [**último \_**](last-is.md) atributo **\]** ou o atributo de **\[** [**cadeia de caracteres**](string.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="0c90c-118">The **\[length\_is\]** attribute cannot be used at the same time as the **\[**[**last\_is**](last-is.md)**\]** attribute or the **\[**[**string**](string.md)**\]** attribute.</span></span>

<span data-ttu-id="0c90c-119">Para definir uma cadeia de caracteres contada com um **\[ comprimento \_ \]** ou **\[** o [**último \_ é**](last-is.md) **\]** atributo, use uma matriz de caracteres ou um ponteiro sem o atributo de cadeia de **\[** [**caracteres**](string.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="0c90c-119">To define a counted string with a **\[length\_is\]** or **\[**[**last\_is**](last-is.md)**\]** attribute, use a character array or pointer without the **\[**[**string**](string.md)**\]** attribute.</span></span>

<span data-ttu-id="0c90c-120">Usar uma expressão constante com o **\[ comprimento \_ é \]** o atributo é um uso inadequado do atributo.</span><span class="sxs-lookup"><span data-stu-id="0c90c-120">Using a constant expression with the **\[length\_is\]** attribute is an inappropriate use of the attribute.</span></span> <span data-ttu-id="0c90c-121">É legal, mas ineficiente, e resultará em um código de marshaling mais lento.</span><span class="sxs-lookup"><span data-stu-id="0c90c-121">It is legal, but inefficient, and will result in slower marshaling code.</span></span>

<span data-ttu-id="0c90c-122">Você pode usar o **\[** [**tamanho \_**](size-is.md) **\]** e o **\[ comprimento \_ são \]** atributos juntos.</span><span class="sxs-lookup"><span data-stu-id="0c90c-122">You can use the **\[**[**size\_is**](size-is.md)**\]** and **\[length\_is\]** attributes together.</span></span> <span data-ttu-id="0c90c-123">Quando você fizer isso, o atributo **\[ Size \_ \]** controlará a quantidade de memória alocada para os dados.</span><span class="sxs-lookup"><span data-stu-id="0c90c-123">When you do, the **\[size\_is\]** attribute controls the amount of memory allocated for the data.</span></span> <span data-ttu-id="0c90c-124">O **\[ tamanho \_ é \]** atributo especifica quantos elementos são transmitidos.</span><span class="sxs-lookup"><span data-stu-id="0c90c-124">The **\[length\_is\]** attribute specifies how many elements are transmitted.</span></span> <span data-ttu-id="0c90c-125">A quantidade de memória especificada pelo **\[ tamanho \_ é \]** e o **\[ comprimento \_ \]** dos atributos não precisam ser iguais.</span><span class="sxs-lookup"><span data-stu-id="0c90c-125">The amount of memory specified by the **\[size\_is\]** and **\[length\_is\]** attributes need not be the same.</span></span> <span data-ttu-id="0c90c-126">Por exemplo, o cliente pode passar **um parâmetro \]** **\[ de entrada** para um servidor e especificar uma grande alocação de **\[ \_ \]** memória com tamanho, embora especifique um pequeno **\[ \_ \]** número de elementos de dados a serem passados com comprimento.</span><span class="sxs-lookup"><span data-stu-id="0c90c-126">For instance, your client may pass an **\[in**, **out\]** parameter to a server and specify a large memory allocation with **\[size\_is\]**, even though it specifies a small number of data elements to be passed with **\[length\_is\]**.</span></span> <span data-ttu-id="0c90c-127">Isso permite que o servidor preencha a matriz com mais dados do que ele recebeu, o que pode então enviar de volta para o cliente.</span><span class="sxs-lookup"><span data-stu-id="0c90c-127">This enables the server to fill the array with more data than it received, which it can then send back to the client.</span></span>

<span data-ttu-id="0c90c-128">Em geral, não é útil especificar o **\[** [**tamanho \_**](size-is.md) **\]** e o **\[ comprimento \_ está \]** nos **\[** parâmetros [**in**](in.md) **\]** ou **\[** [**out**](out-idl.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="0c90c-128">In general, it isn't useful to specify both **\[**[**size\_is**](size-is.md)**\]** and **\[length\_is\]** on **\[**[**in**](in.md)**\]** or **\[**[**out**](out-idl.md)**\]** parameters.</span></span> <span data-ttu-id="0c90c-129">Em ambos os casos, o **\[ tamanho \_ é \]** controlar a alocação de memória.</span><span class="sxs-lookup"><span data-stu-id="0c90c-129">In both cases, **\[size\_is\]** controls memory allocation.</span></span> <span data-ttu-id="0c90c-130">Seu aplicativo pode usar o **\[ tamanho \_ \]** para alocar mais elementos de matriz do que transmitidos (conforme **\[ \_ \]** especificado pelo comprimento).</span><span class="sxs-lookup"><span data-stu-id="0c90c-130">Your application could use **\[size\_is\]** to allocate more array elements than it transmits (as specified by **\[length\_is\]**).</span></span> <span data-ttu-id="0c90c-131">No entanto, isso seria ineficiente.</span><span class="sxs-lookup"><span data-stu-id="0c90c-131">However, this would be inefficient.</span></span> <span data-ttu-id="0c90c-132">Também seria ineficiente especificar valores idênticos para o **\[ tamanho \_ \]** e o **\[ comprimento \_ é \]**.</span><span class="sxs-lookup"><span data-stu-id="0c90c-132">It would also be inefficient to specify identical values for **\[size\_is\]** and **\[length\_is\]**.</span></span> <span data-ttu-id="0c90c-133">Porque ele criaria uma sobrecarga extra durante o marshaling do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0c90c-133">Because it would create extra overhead during parameter marshaling.</span></span> <span data-ttu-id="0c90c-134">Quando os valores de **\[ tamanho \_ \]** e **\[ \_ \] comprimento** são sempre iguais, omita o **\[ comprimento \_ é \]** atributo.</span><span class="sxs-lookup"><span data-stu-id="0c90c-134">When the values of **\[size\_is\]** and **\[length\_is\]** are always the same, omit the **\[length\_is\]** attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="0c90c-135">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0c90c-135">Examples</span></span>

``` syntax
/* counted string holding at most "size" characters */ 
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
 } COUNTED_STRING_TYPE; 
 
/* counted string holding at most 80 characters */ 
typedef struct 
{ 
    unsigned short length; 
    [length_is(length)] char string[80]; 
} STATIC_COUNTED_STRING_TYPE; 
 
HRESULT Proc1(
    [in] short iLength; 
    [in, length_is(iLength)] short asNumbers[10]);
```

## <a name="see-also"></a><span data-ttu-id="0c90c-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c90c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c90c-137">Atributos de campo</span><span class="sxs-lookup"><span data-stu-id="0c90c-137">Field Attributes</span></span>](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[<span data-ttu-id="0c90c-138">**primeiro \_ é**</span><span class="sxs-lookup"><span data-stu-id="0c90c-138">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="0c90c-139">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="0c90c-139">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="0c90c-140">**último \_ é**</span><span class="sxs-lookup"><span data-stu-id="0c90c-140">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="0c90c-141">**máximo \_ é**</span><span class="sxs-lookup"><span data-stu-id="0c90c-141">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="0c90c-142">**mín. \_ é**</span><span class="sxs-lookup"><span data-stu-id="0c90c-142">**min\_is**</span></span>](min-is.md)
</dt> <dt>

[<span data-ttu-id="0c90c-143">**o tamanho \_ é**</span><span class="sxs-lookup"><span data-stu-id="0c90c-143">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="0c90c-144">**string**</span><span class="sxs-lookup"><span data-stu-id="0c90c-144">**string**</span></span>](string.md)
</dt> </dl>

 

 
---
title: Atributo last_is
description: O atributo Field \ Last \_ is \ especifica o índice do último elemento de matriz a ser transmitido. Quando o índice especificado é zero ou negativo, nenhum elemento de matriz é transmitido.
ms.assetid: 42a5cb0d-0887-4aa7-b34f-2fbad0f4c8ab
keywords:
- last_is do atributo MIDL
topic_type:
- apiref
api_name:
- last_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 453a51109452f3cdacb1a48e67b76ccbc9f2e257
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104499040"
---
# <a name="last_is-attribute"></a><span data-ttu-id="c9768-105">último \_ atributo is</span><span class="sxs-lookup"><span data-stu-id="c9768-105">last\_is attribute</span></span>

<span data-ttu-id="c9768-106">O atributo de campo **\[ Last \_ é \]** especifica o índice do último elemento de matriz a ser transmitido.</span><span class="sxs-lookup"><span data-stu-id="c9768-106">The field attribute **\[last\_is\]** specifies the index of the last array element to be transmitted.</span></span> <span data-ttu-id="c9768-107">Quando o índice especificado é zero ou negativo, nenhum elemento de matriz é transmitido.</span><span class="sxs-lookup"><span data-stu-id="c9768-107">When the specified index is zero or negative, no array elements are transmitted.</span></span>

``` syntax
[last_is( limited-expression-list )]
```

## <a name="parameters"></a><span data-ttu-id="c9768-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c9768-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9768-109">*lista de expressões limitadas*</span><span class="sxs-lookup"><span data-stu-id="c9768-109">*limited-expression-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c9768-110">Especifica uma ou mais expressões de linguagem C.</span><span class="sxs-lookup"><span data-stu-id="c9768-110">Specifies one or more C-language expressions.</span></span> <span data-ttu-id="c9768-111">Cada expressão é avaliada como um inteiro que representa o índice de matriz do último elemento de matriz a ser transmitido.</span><span class="sxs-lookup"><span data-stu-id="c9768-111">Each expression evaluates to an integer that represents the array index of the last array element to be transmitted.</span></span> <span data-ttu-id="c9768-112">O compilador MIDL oferece suporte a expressões condicionais, expressões lógicas, expressões relacionais e expressões aritméticas.</span><span class="sxs-lookup"><span data-stu-id="c9768-112">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="c9768-113">MIDL não permite invocações de função em expressões e não permite operadores de incremento e decréscimo.</span><span class="sxs-lookup"><span data-stu-id="c9768-113">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span> <span data-ttu-id="c9768-114">Separe várias expressões com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="c9768-114">Separate multiple expressions with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c9768-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9768-115">Remarks</span></span>

<span data-ttu-id="c9768-116">O **\[ último \_ atributo \] is** determina o valor do índice de matriz correspondente ao **\[** [**\_**](length-is.md) **\]** **\[ \_ \]** comprimento é o atributo quando length não é especificado.</span><span class="sxs-lookup"><span data-stu-id="c9768-116">The **\[last\_is\]** attribute determines the value of the array index corresponding to the **\[**[**length\_is**](length-is.md)**\]** attribute when **\[length\_is\]** is not specified.</span></span> <span data-ttu-id="c9768-117">A relação entre esses índices de matriz é a seguinte: comprimento = último-primeiro + 1.</span><span class="sxs-lookup"><span data-stu-id="c9768-117">The relationship between these array indexes is as follows: length = last - first + 1.</span></span>

<span data-ttu-id="c9768-118">Se o valor do índice de matriz especificado pela **\[** [**primeira \_ for**](first-is.md) **\]** maior que o **\[ \_ \]** valor especificado pelo último, os elementos zero serão transmitidos.</span><span class="sxs-lookup"><span data-stu-id="c9768-118">If the value of the array index specified by **\[**[**first\_is**](first-is.md)**\]** is larger than the value specified by **\[last\_is\]**, zero elements are transmitted.</span></span>

<span data-ttu-id="c9768-119">O **\[ último \_ atributo \] is** não pode ser usado como um atributo de campo ao mesmo tempo que o **\[** [**comprimento \_ é**](length-is.md) um atributo **\]** ou o atributo de **\[** [**cadeia de caracteres**](string.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="c9768-119">The **\[last\_is\]** attribute cannot be used as a field attribute at the same time as the **\[**[**length\_is**](length-is.md)**\]** attribute or the **\[**[**string**](string.md)**\]** attribute.</span></span>

<span data-ttu-id="c9768-120">O uso de uma expressão constante com o **\[ último atributo \_ é \]** um uso inadequado do atributo.</span><span class="sxs-lookup"><span data-stu-id="c9768-120">Using a constant expression with the **\[last\_is\]** attribute is an inappropriate use of the attribute.</span></span> <span data-ttu-id="c9768-121">É legal, mas ineficiente, e resultará em um código de marshaling mais lento.</span><span class="sxs-lookup"><span data-stu-id="c9768-121">It is legal, but inefficient, and will result in slower marshaling code.</span></span>

<span data-ttu-id="c9768-122">Quando o valor especificado por **\[** [**Max \_ é**](max-is.md) **\]** igual ou maior que zero, a relação a seguir deve ser verdadeira: 0 <= Last \_ é <= Max \_ é.</span><span class="sxs-lookup"><span data-stu-id="c9768-122">When the value specified by **\[**[**max\_is**](max-is.md)**\]** is equal to or greater than zero, the following relationship must be true: 0 <= last\_is <= max\_is.</span></span>

## <a name="examples"></a><span data-ttu-id="c9768-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c9768-123">Examples</span></span>

``` syntax
proc1(
    [in] short Last,
    [in, last_is(Last)] short asNumbers[MAXSIZE]);
```

## <a name="see-also"></a><span data-ttu-id="c9768-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9768-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9768-125">Atributos de campo</span><span class="sxs-lookup"><span data-stu-id="c9768-125">Field Attributes</span></span>](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[<span data-ttu-id="c9768-126">**primeiro \_ é**</span><span class="sxs-lookup"><span data-stu-id="c9768-126">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="c9768-127">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="c9768-127">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="c9768-128">**comprimento \_ é**</span><span class="sxs-lookup"><span data-stu-id="c9768-128">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="c9768-129">**máximo \_ é**</span><span class="sxs-lookup"><span data-stu-id="c9768-129">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="c9768-130">**o tamanho \_ é**</span><span class="sxs-lookup"><span data-stu-id="c9768-130">**size\_is**</span></span>](size-is.md)
</dt> </dl>

 

 
---
title: Atributo max_is
description: O atributo \ Max \_ is \ designa o valor máximo para um índice de matriz válido.
ms.assetid: 8d09f610-cae6-45f6-815c-5ba916d8a5e7
keywords:
- max_is do atributo MIDL
topic_type:
- apiref
api_name:
- max_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f2e2040acbc0e8f65c02f4f4ec7c3ad329959b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293952"
---
# <a name="max_is-attribute"></a><span data-ttu-id="3dea9-104">\_atributo Max é</span><span class="sxs-lookup"><span data-stu-id="3dea9-104">max\_is attribute</span></span>

<span data-ttu-id="3dea9-105">O atributo **\[ Max \_ é \]** designa o valor máximo para um índice de matriz válido.</span><span class="sxs-lookup"><span data-stu-id="3dea9-105">The **\[max\_is\]** attribute designates the maximum value for a valid array index.</span></span>

``` syntax
[max_is(limited-expression-list )]
```

## <a name="parameters"></a><span data-ttu-id="3dea9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3dea9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dea9-107">*lista de expressões limitadas*</span><span class="sxs-lookup"><span data-stu-id="3dea9-107">*limited-expression-list*</span></span> 
</dt> <dd>

<span data-ttu-id="3dea9-108">Especifica uma ou mais expressões de linguagem C.</span><span class="sxs-lookup"><span data-stu-id="3dea9-108">Specifies one or more C-language expressions.</span></span> <span data-ttu-id="3dea9-109">Cada expressão é avaliada como um inteiro que representa o índice de matriz válido mais alto.</span><span class="sxs-lookup"><span data-stu-id="3dea9-109">Each expression evaluates to an integer that represents the highest valid array index.</span></span> <span data-ttu-id="3dea9-110">O compilador MIDL oferece suporte a expressões condicionais, expressões lógicas, expressões relacionais e expressões aritméticas.</span><span class="sxs-lookup"><span data-stu-id="3dea9-110">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="3dea9-111">MIDL não permite invocações de função em expressões e não permite operadores de incremento e decréscimo.</span><span class="sxs-lookup"><span data-stu-id="3dea9-111">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span> <span data-ttu-id="3dea9-112">Separe várias expressões com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="3dea9-112">Separate multiple expressions with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3dea9-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="3dea9-113">Remarks</span></span>

<span data-ttu-id="3dea9-114">O atributo **\[ Max \_ is \]** não corresponde necessariamente ao número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="3dea9-114">The **\[max\_is\]** attribute does not necessarily correspond to the number of elements in the array.</span></span> <span data-ttu-id="3dea9-115">Para uma matriz de tamanho *n* em C, em que o primeiro elemento de matriz é o número de elemento zero, o valor máximo para um índice de matriz válido é *n*– 1.</span><span class="sxs-lookup"><span data-stu-id="3dea9-115">For an array of size *n* in C, where the first array element is element number zero, the maximum value for a valid array index is *n*–1.</span></span>

<span data-ttu-id="3dea9-116">O atributo **\[ Max \_ is \]** não pode ser usado como um atributo Field ao mesmo tempo que o **\[** [**tamanho \_ é**](size-is.md) **\]** Attribute.</span><span class="sxs-lookup"><span data-stu-id="3dea9-116">The **\[max\_is\]** attribute cannot be used as a field attribute at the same time as the **\[**[**size\_is**](size-is.md)**\]** attribute.</span></span>

<span data-ttu-id="3dea9-117">Embora seja legal usar o atributo **\[ Max \_ is \]** com uma expressão constante, fazer isso é ineficiente e desnecessário.</span><span class="sxs-lookup"><span data-stu-id="3dea9-117">While it is legal to use the **\[max\_is\]** attribute with a constant expression, doing so is inefficient and unnecessary.</span></span> <span data-ttu-id="3dea9-118">Por exemplo, use uma matriz de tamanho fixo:</span><span class="sxs-lookup"><span data-stu-id="3dea9-118">For example, use a fixed size array:</span></span>

``` syntax
/* transmits values of a[0]... a[MAX_SIZE-1] */ 
HRESULT Proc3([in] short Arr[MAX_SIZE]); 
```

<span data-ttu-id="3dea9-119">em vez de:</span><span class="sxs-lookup"><span data-stu-id="3dea9-119">instead of:</span></span>

``` syntax
/* legal but marshaling code is much slower */ 
HRESULT Proc3([in max_is(MAX_SIZE-1)] short Arr[] );
```

## <a name="examples"></a><span data-ttu-id="3dea9-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3dea9-120">Examples</span></span>

``` syntax
/* if m = 10, there are 11 transmitted elements (a[0]...a[10])*/ 
HRESULT Proc1( 
    [in] short m, 
    [in, max_is(m)] short a[]);  
 
/* if m = 10, the valid range for b is b[0...10][20] */ 
HRESULT Proc2( 
    [in] short m, 
    [in, max_is(m)] short b[][20];
```

## <a name="see-also"></a><span data-ttu-id="3dea9-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="3dea9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dea9-122">Atributos de campo</span><span class="sxs-lookup"><span data-stu-id="3dea9-122">Field Attributes</span></span>](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[<span data-ttu-id="3dea9-123">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="3dea9-123">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="3dea9-124">**mín. \_ é**</span><span class="sxs-lookup"><span data-stu-id="3dea9-124">**min\_is**</span></span>](min-is.md)
</dt> <dt>

[<span data-ttu-id="3dea9-125">**o tamanho \_ é**</span><span class="sxs-lookup"><span data-stu-id="3dea9-125">**size\_is**</span></span>](size-is.md)
</dt> </dl>

 

 
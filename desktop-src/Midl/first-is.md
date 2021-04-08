---
title: Atributo first_is
description: O atributo \ First \_ is \ especifica o índice do primeiro elemento de matriz a ser transmitido.
ms.assetid: 1de7821c-19e7-4b2c-98fc-2fae3563831c
keywords:
- first_is do atributo MIDL
topic_type:
- apiref
api_name:
- first_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1d8d1be33299354e77ef92d885bb3b092cccfb6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823766"
---
# <a name="first_is-attribute"></a><span data-ttu-id="1f813-104">primeiro \_ atributo é</span><span class="sxs-lookup"><span data-stu-id="1f813-104">first\_is attribute</span></span>

<span data-ttu-id="1f813-105">O \[ **primeiro atributo \_ is** \] especifica o índice do primeiro elemento de matriz a ser transmitido.</span><span class="sxs-lookup"><span data-stu-id="1f813-105">The \[**first\_is**\] attribute specifies the index of the first array element to be transmitted.</span></span>

``` syntax
first_is(limited-expression-list)
```

## <a name="parameters"></a><span data-ttu-id="1f813-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f813-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f813-107">*lista de expressões limitadas*</span><span class="sxs-lookup"><span data-stu-id="1f813-107">*limited-expression-list*</span></span> 
</dt> <dd>

<span data-ttu-id="1f813-108">Especifica uma ou mais expressões de linguagem C.</span><span class="sxs-lookup"><span data-stu-id="1f813-108">Specifies one or more C-language expressions.</span></span> <span data-ttu-id="1f813-109">Cada expressão é avaliada como um inteiro que representa o índice de matriz do primeiro elemento de matriz a ser transmitido.</span><span class="sxs-lookup"><span data-stu-id="1f813-109">Each expression evaluates to an integer that represents the array index of the first array element to be transmitted.</span></span> <span data-ttu-id="1f813-110">O compilador MIDL oferece suporte a expressões condicionais, expressões lógicas, expressões relacionais e expressões aritméticas.</span><span class="sxs-lookup"><span data-stu-id="1f813-110">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="1f813-111">MIDL não permite invocações de função em expressões e não permite operadores de incremento e decréscimo.</span><span class="sxs-lookup"><span data-stu-id="1f813-111">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span> <span data-ttu-id="1f813-112">Separe várias expressões com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="1f813-112">Separate multiple expressions with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1f813-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f813-113">Remarks</span></span>

<span data-ttu-id="1f813-114">Se o **\[ primeiro \_ atributo \] for** não estiver presente, ou se o índice especificado for um número negativo, o elemento de matriz zero será o primeiro elemento transmitido.</span><span class="sxs-lookup"><span data-stu-id="1f813-114">If the **\[first\_is\]** attribute is not present, or if the specified index is a negative number, array element zero is the first element transmitted.</span></span>

<span data-ttu-id="1f813-115">O **\[ primeiro \_ atributo \] is** também pode ajudar a determinar os valores dos índices de matriz correspondentes ao **\[** atributo [**Last \_ is**](last-is.md) **\]** ou **\[** [**length \_**](length-is.md) , **\]** quando esses atributos não são especificados.</span><span class="sxs-lookup"><span data-stu-id="1f813-115">The **\[first\_is\]** attribute can also help determine the values of the array indexes corresponding to the **\[**[**last\_is**](last-is.md)**\]** or **\[**[**length\_is**](length-is.md)**\]** attribute when these attributes are not specified.</span></span> <span data-ttu-id="1f813-116">A relação entre esses índices de matriz é:</span><span class="sxs-lookup"><span data-stu-id="1f813-116">The relationship between these array indexes is:</span></span>

``` syntax
length = last - first + 1
```

<span data-ttu-id="1f813-117">A relação a seguir também deve conter:</span><span class="sxs-lookup"><span data-stu-id="1f813-117">The following relationship must also hold:</span></span>

``` syntax
0 <= first_is <= max_is
```

<span data-ttu-id="1f813-118">A relação a seguir deve ser mantida quando **\[** [**Max \_ é**](max-is.md) **\] <= 0:**</span><span class="sxs-lookup"><span data-stu-id="1f813-118">The following relationship must hold when **\[**[**max\_is**](max-is.md)**\] <= 0:**</span></span>

``` syntax
first_is == 0
```

<span data-ttu-id="1f813-119">O **\[ primeiro \_ atributo \] is** não pode ser usado ao mesmo tempo que o **\[** atributo de [**cadeia de caracteres**](string.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="1f813-119">The **\[first\_is\]** attribute cannot be used at the same time as the **\[**[**string**](string.md)**\]** attribute.</span></span>

<span data-ttu-id="1f813-120">O uso de uma expressão constante com o **\[ primeiro atributo \_ é \]** um uso inadequado do atributo.</span><span class="sxs-lookup"><span data-stu-id="1f813-120">Using a constant expression with the **\[first\_is\]** attribute is an inappropriate use of the attribute.</span></span> <span data-ttu-id="1f813-121">É legal, mas ineficiente, e resultará em um código de marshaling mais lento.</span><span class="sxs-lookup"><span data-stu-id="1f813-121">It is legal, but inefficient, and will result in slower marshaling code.</span></span>

## <a name="examples"></a><span data-ttu-id="1f813-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1f813-122">Examples</span></span>

``` syntax
HRESULT Proc1(
    [in] short First,
    [first_is(First)] Arr[10]);
```

## <a name="see-also"></a><span data-ttu-id="1f813-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f813-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f813-124">atributos de campo \_</span><span class="sxs-lookup"><span data-stu-id="1f813-124">field\_attributes</span></span>](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[<span data-ttu-id="1f813-125">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="1f813-125">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="1f813-126">**último \_ é**</span><span class="sxs-lookup"><span data-stu-id="1f813-126">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="1f813-127">**comprimento \_ é**</span><span class="sxs-lookup"><span data-stu-id="1f813-127">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="1f813-128">**máximo \_ é**</span><span class="sxs-lookup"><span data-stu-id="1f813-128">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="1f813-129">**mín. \_ é**</span><span class="sxs-lookup"><span data-stu-id="1f813-129">**min\_is**</span></span>](min-is.md)
</dt> <dt>

[<span data-ttu-id="1f813-130">**o tamanho \_ é**</span><span class="sxs-lookup"><span data-stu-id="1f813-130">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="1f813-131">**string**</span><span class="sxs-lookup"><span data-stu-id="1f813-131">**string**</span></span>](string.md)
</dt> </dl>

 

 
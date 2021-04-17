---
title: atributo de matrizes
description: As matrizes são coleções homogêneas de dados acessados por um índice ou número de elemento.
ms.assetid: 375fb795-8f18-45b7-898c-99f1273746d8
keywords:
- atributo de matrizes MIDL
topic_type:
- apiref
api_name:
- arrays
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e189eb1784a4ff24b799c7a4d4482d0f56b20e3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105758785"
---
# <a name="arrays-attribute"></a><span data-ttu-id="7c4d5-104">atributo de matrizes</span><span class="sxs-lookup"><span data-stu-id="7c4d5-104">arrays attribute</span></span>

<span data-ttu-id="7c4d5-105">As matrizes são coleções homogêneas de dados acessados por um índice ou número de elemento.</span><span class="sxs-lookup"><span data-stu-id="7c4d5-105">Arrays are homogenous collections of data accessed by an index or element number.</span></span>

``` syntax
typedef [ [type-attr-list] ] type-specifier [pointer-decl] array-declarator;

typedef [ [type-attr-list] ] struct [ tag ] 
{
    [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
    ...
};

typedef [ [type-attr-list] ] union [ tag ] 
{
    [ case (limited-expression [ , ... ] ) ]
  [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
  [ [ default ]
  [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
  ]
};

[[ [function-attribute-list] ]] type-specifier [[pointer-decl]] function-name(
        [[ [param-attr-list] ]] type-specifier [[pointer-decl]] array-declarator
        , ...);
```

## <a name="parameters"></a><span data-ttu-id="7c4d5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c4d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c4d5-107">*tipo-attr-List*</span><span class="sxs-lookup"><span data-stu-id="7c4d5-107">*type-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7c4d5-108">Especifica zero ou mais atributos que se aplicam ao tipo.</span><span class="sxs-lookup"><span data-stu-id="7c4d5-108">Specifies zero or more attributes that apply to the type.</span></span> <span data-ttu-id="7c4d5-109">Atributos de tipo válidos [**\[ incluem \] identificador**](handle.md), [**\[ \_ tipo \] de comutador**](switch-type.md), [**\[ transmissão \_ como \]**](transmit-as.md); o atributo de ponteiro [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)ou [**\[ PTR \]**](ptr.md); e o [**\[ \_ identificador \] de contexto**](context-handle.md)de atributos de uso, Cadeia de [**\[ caracteres \]**](string.md)e [**\[ ignorar \]**](ignore.md).</span><span class="sxs-lookup"><span data-stu-id="7c4d5-109">Valid type attributes include [**\[handle\]**](handle.md), [**\[switch\_type\]**](switch-type.md), [**\[transmit\_as\]**](transmit-as.md); the pointer attribute [**\[ref\]**](ref.md), [**\[unique\]**](unique.md), or [**\[ptr\]**](ptr.md); and the usage attributes [**\[context\_handle\]**](context-handle.md), [**\[string\]**](string.md), and [**\[ignore\]**](ignore.md).</span></span> <span data-ttu-id="7c4d5-110">Separe vários atributos com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="7c4d5-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="7c4d5-111">*especificador de tipo*</span><span class="sxs-lookup"><span data-stu-id="7c4d5-111">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="7c4d5-112">Especifica o identificador de tipo, tipo base, [**struct**](struct.md), [**União**](union.md)ou tipo de [**Enumeração**](enum.md) .</span><span class="sxs-lookup"><span data-stu-id="7c4d5-112">Specifies the type identifier, base type, [**struct**](struct.md), [**union**](union.md), or [**enum**](enum.md) type.</span></span> <span data-ttu-id="7c4d5-113">A especificação de tipo pode incluir uma especificação de armazenamento opcional.</span><span class="sxs-lookup"><span data-stu-id="7c4d5-113">The type specification can include an optional storage specification.</span></span>

</dd> <dt>

<span data-ttu-id="7c4d5-114">*ponteiro-decl*</span><span class="sxs-lookup"><span data-stu-id="7c4d5-114">*pointer-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="7c4d5-115">Especifica zero ou mais declaradores de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="7c4d5-115">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="7c4d5-116">Um Declarador de ponteiro é o mesmo que o Declarador de ponteiro usado em C, construído a partir do **\*** designador, modificadores como **distante** e o qualificador [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="7c4d5-116">A pointer declarator is the same as the pointer declarator used in C, constructed from the **\*** designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c4d5-117">*Declarador de matriz*</span><span class="sxs-lookup"><span data-stu-id="7c4d5-117">*array-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="7c4d5-118">Especifica o nome da matriz, seguido por uma das seguintes construções para cada dimensão da matriz: "**\[ \]**", " **\[\*\]** ", "**\[ ***Const1*** \]**" ou "**\[ ***Lower...*** Upper \]**"onde *Lower* e *Upper* são valores constantes que representam os limites inferior e superior.</span><span class="sxs-lookup"><span data-stu-id="7c4d5-118">Specifies the name of the array, followed by one of the following constructs for each dimension of the array: "**\[ \]**", "**\[\*\]**", "**\[***const1***\]**", or "**\[***lower...upper***\]**" where *lower* and *upper* are constant values that represent the lower and upper bounds.</span></span> <span data-ttu-id="7c4d5-119">A constante *inferior* deve ser avaliada como zero.</span><span class="sxs-lookup"><span data-stu-id="7c4d5-119">The constant *lower* must evaluate to zero.</span></span>

</dd> <dt>

<span data-ttu-id="7c4d5-120">*Tags*</span><span class="sxs-lookup"><span data-stu-id="7c4d5-120">*tag*</span></span> 
</dt> <dd>

<span data-ttu-id="7c4d5-121">Especifica uma marca opcional para a estrutura ou União.</span><span class="sxs-lookup"><span data-stu-id="7c4d5-121">Specifies an optional tag for the structure or union.</span></span>

</dd> <dt>

<span data-ttu-id="7c4d5-122">*lista de atributos de campo*</span><span class="sxs-lookup"><span data-stu-id="7c4d5-122">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7c4d5-123">Especifica zero ou mais atributos de campo que se aplicam à estrutura, ao membro de União ou ao parâmetro de função.</span><span class="sxs-lookup"><span data-stu-id="7c4d5-123">Specifies zero or more field attributes that apply to the structure, union member, or function parameter.</span></span> <span data-ttu-id="7c4d5-124">Os atributos de campo válidos incluem [**\[ primeiro \_ \]**](first-is.md), o [**\[ último \_ \]**](last-is.md)é [**\[ \]**](ptr.md) [**\[ \]**](ref.md) [**\[ \]**](unique.md) [**\[ \_ , comprimento é \]**](length-is.md), [**\[ máximo \_ é \]**](max-is.md), [**\[ tamanho, a cadeia de \_ caracteres de atributos de uso e ignore; os atributos de ponteiro ref, Unique e PTR; e o tipo de opção de atributo Union. \]**](size-is.md) [**\[ \_ \]**](switch-type.md) [**\[ \]**](string.md) [**\[ \]**](ignore.md)</span><span class="sxs-lookup"><span data-stu-id="7c4d5-124">Valid field attributes include [**\[first\_is\]**](first-is.md), [**\[last\_is\]**](last-is.md), [**\[length\_is\]**](length-is.md), [**\[max\_is\]**](max-is.md), [**\[size\_is\]**](size-is.md); the usage attributes [**\[string\]**](string.md), and [**\[ignore\]**](ignore.md); the pointer attributes [**\[ref\]**](ref.md), [**\[unique\]**](unique.md), and [**\[ptr\]**](ptr.md); and the union attribute [**\[switch\_type\]**](switch-type.md).</span></span> <span data-ttu-id="7c4d5-125">Separe vários atributos de campo com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="7c4d5-125">Separate multiple field attributes with commas.</span></span> <span data-ttu-id="7c4d5-126">Observe que os atributos listados acima, **\[ primeiro \_ é \]**, **\[ último \_ \]** são e [**\[ ignorar \]**](ignore.md) não são válidos para uniões.</span><span class="sxs-lookup"><span data-stu-id="7c4d5-126">Note that of the attributes listed above, **\[first\_is\]**, **\[last\_is\]**, and [**\[ignore\]**](ignore.md) are not valid for unions.</span></span>

</dd> <dt>

<span data-ttu-id="7c4d5-127">*expressão limitada*</span><span class="sxs-lookup"><span data-stu-id="7c4d5-127">*limited-expression*</span></span> 
</dt> <dd>

<span data-ttu-id="7c4d5-128">Especifica uma expressão de linguagem C.</span><span class="sxs-lookup"><span data-stu-id="7c4d5-128">Specifies a C-language expression.</span></span> <span data-ttu-id="7c4d5-129">O compilador MIDL oferece suporte a expressões condicionais, expressões lógicas, expressões relacionais e expressões aritméticas.</span><span class="sxs-lookup"><span data-stu-id="7c4d5-129">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="7c4d5-130">MIDL não permite invocações de função em expressões e não permite operadores de incremento e decréscimo.</span><span class="sxs-lookup"><span data-stu-id="7c4d5-130">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span>

</dd> <dt>

<span data-ttu-id="7c4d5-131">*lista de atributos de função*</span><span class="sxs-lookup"><span data-stu-id="7c4d5-131">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7c4d5-132">Especifica zero ou mais atributos que se aplicam à função.</span><span class="sxs-lookup"><span data-stu-id="7c4d5-132">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="7c4d5-133">Os atributos de função válidos são [**\[ retorno de \] chamada**](callback.md), [**\[ local \]**](local.md); o atributo de ponteiro [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)ou [**\[ PTR \]**](ptr.md); e a cadeia de [**\[ caracteres \]**](string.md)de atributos de uso e o [**\[ \_ identificador \] de contexto**](context-handle.md).</span><span class="sxs-lookup"><span data-stu-id="7c4d5-133">Valid function attributes are [**\[callback\]**](callback.md), [**\[local\]**](local.md); the pointer attribute [**\[ref\]**](ref.md), [**\[unique\]**](unique.md), or [**\[ptr\]**](ptr.md); and the usage attributes [**\[string\]**](string.md), and [**\[context\_handle\]**](context-handle.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c4d5-134">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="7c4d5-134">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7c4d5-135">Especifica o nome do procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="7c4d5-135">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="7c4d5-136">*param-attr-List*</span><span class="sxs-lookup"><span data-stu-id="7c4d5-136">*param-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7c4d5-137">Especifica os atributos direcionais e um ou mais atributos de campo opcionais que se aplicam ao parâmetro de matriz.</span><span class="sxs-lookup"><span data-stu-id="7c4d5-137">Specifies the directional attributes and one or more optional field attributes that apply to the array parameter.</span></span> <span data-ttu-id="7c4d5-138">Os atributos de campo válidos incluem [**\[ Max \_ is \]**](max-is.md), [**\[ Size \_ \] is**](size-is.md), [**\[ length \_ is \]**](length-is.md), [**\[ First \_ is \]**](first-is.md)e [**\[ Last \_ is \]**](last-is.md).</span><span class="sxs-lookup"><span data-stu-id="7c4d5-138">Valid field attributes include [**\[max\_is\]**](max-is.md), [**\[size\_is\]**](size-is.md), [**\[length\_is\]**](length-is.md), [**\[first\_is\]**](first-is.md), and [**\[last\_is\]**](last-is.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7c4d5-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c4d5-139">Remarks</span></span>

<span data-ttu-id="7c4d5-140">As matrizes no MIDL usam um estilo semelhante a, mas não exatamente igual a C e C++.</span><span class="sxs-lookup"><span data-stu-id="7c4d5-140">Arrays in MIDL use a style similar to but not exactly the same as C and C++.</span></span> <span data-ttu-id="7c4d5-141">Para obter mais informações, consulte [matrizes de MIDL](midl-arrays.md).</span><span class="sxs-lookup"><span data-stu-id="7c4d5-141">For more information, see [MIDL Arrays](midl-arrays.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="7c4d5-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c4d5-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c4d5-143">**retorno de chamada**</span><span class="sxs-lookup"><span data-stu-id="7c4d5-143">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="7c4d5-144">**const**</span><span class="sxs-lookup"><span data-stu-id="7c4d5-144">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="7c4d5-145">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="7c4d5-145">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="7c4d5-146">**enumera**</span><span class="sxs-lookup"><span data-stu-id="7c4d5-146">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="7c4d5-147">**primeiro \_ é**</span><span class="sxs-lookup"><span data-stu-id="7c4d5-147">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="7c4d5-148">**processamento**</span><span class="sxs-lookup"><span data-stu-id="7c4d5-148">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="7c4d5-149">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="7c4d5-149">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="7c4d5-150">**ignorar**</span><span class="sxs-lookup"><span data-stu-id="7c4d5-150">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="7c4d5-151">**último \_ é**</span><span class="sxs-lookup"><span data-stu-id="7c4d5-151">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="7c4d5-152">**comprimento \_ é**</span><span class="sxs-lookup"><span data-stu-id="7c4d5-152">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="7c4d5-153">**local**</span><span class="sxs-lookup"><span data-stu-id="7c4d5-153">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="7c4d5-154">**máximo \_ é**</span><span class="sxs-lookup"><span data-stu-id="7c4d5-154">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="7c4d5-155">**ptr**</span><span class="sxs-lookup"><span data-stu-id="7c4d5-155">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="7c4d5-156">**ref**</span><span class="sxs-lookup"><span data-stu-id="7c4d5-156">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="7c4d5-157">**o tamanho \_ é**</span><span class="sxs-lookup"><span data-stu-id="7c4d5-157">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="7c4d5-158">**string**</span><span class="sxs-lookup"><span data-stu-id="7c4d5-158">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="7c4d5-159">**struct**</span><span class="sxs-lookup"><span data-stu-id="7c4d5-159">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="7c4d5-160">**tipo de comutador \_**</span><span class="sxs-lookup"><span data-stu-id="7c4d5-160">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="7c4d5-161">**transmitir \_ como**</span><span class="sxs-lookup"><span data-stu-id="7c4d5-161">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="7c4d5-162">**unida**</span><span class="sxs-lookup"><span data-stu-id="7c4d5-162">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="7c4d5-163">**diferente**</span><span class="sxs-lookup"><span data-stu-id="7c4d5-163">**unique**</span></span>](unique.md)
</dt> </dl>

 

 





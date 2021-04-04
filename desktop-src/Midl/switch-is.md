---
title: Atributo switch_is
description: O atributo \ switch \_ is \ especifica a expressão ou o identificador que atua como o discriminante de União que seleciona o membro Union.
ms.assetid: 93552bdf-6a14-47ce-877e-32ed976bb895
keywords:
- switch_is do atributo MIDL
topic_type:
- apiref
api_name:
- switch_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c52661c4fa1ebce57011f4424901dd1ec18250f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103916778"
---
# <a name="switch_is-attribute"></a><span data-ttu-id="0565c-104">a opção \_ é um atributo</span><span class="sxs-lookup"><span data-stu-id="0565c-104">switch\_is attribute</span></span>

<span data-ttu-id="0565c-105">O atributo **\[ switch \_ é \]** especifica a expressão ou o identificador que atua como o discriminante de União que seleciona o membro Union.</span><span class="sxs-lookup"><span data-stu-id="0565c-105">The **\[switch\_is\]** attribute specifies the expression or identifier acting as the union discriminant that selects the union member.</span></span>

``` syntax
typedef struct [[ struct-tag ]] 
{
    [ switch_is(limited-expr) [[ , field-attr-list ]] ] union-type-specifier declarator;
    ...
}

[[ [function-attribute-list] ]] type-specifier [[pointer-declarator]] function-name(
    [ switch_is(limited-expr) [[ , param-attr-list ]] ] union-type [[declarator]]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="0565c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0565c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0565c-107">*struct-tag*</span><span class="sxs-lookup"><span data-stu-id="0565c-107">*struct-tag*</span></span> 
</dt> <dd>

<span data-ttu-id="0565c-108">Especifica uma marca opcional para uma estrutura.</span><span class="sxs-lookup"><span data-stu-id="0565c-108">Specifies an optional tag for a structure.</span></span>

</dd> <dt>

<span data-ttu-id="0565c-109">*expr limitado*</span><span class="sxs-lookup"><span data-stu-id="0565c-109">*limited-expr*</span></span> 
</dt> <dd>

<span data-ttu-id="0565c-110">Especifica uma expressão de linguagem C com suporte no MIDL.</span><span class="sxs-lookup"><span data-stu-id="0565c-110">Specifies a C-language expression supported by MIDL.</span></span> <span data-ttu-id="0565c-111">Quase todas as expressões de linguagem C têm suporte.</span><span class="sxs-lookup"><span data-stu-id="0565c-111">Almost all C-language expressions are supported.</span></span> <span data-ttu-id="0565c-112">O compilador MIDL oferece suporte a expressões condicionais, expressões lógicas, expressões relacionais e expressões aritméticas.</span><span class="sxs-lookup"><span data-stu-id="0565c-112">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="0565c-113">MIDL não permite invocações de função em expressões e não permite operadores pré e pós-incremento e pré e pós-backup.</span><span class="sxs-lookup"><span data-stu-id="0565c-113">MIDL does not allow function invocations in expressions and does not allow pre- and post-increment and pre- and post-decrement operators.</span></span>

</dd> <dt>

<span data-ttu-id="0565c-114">*campo – attr-lista*</span><span class="sxs-lookup"><span data-stu-id="0565c-114">*field-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="0565c-115">Especifica zero ou mais atributos de campo que se aplicam a um membro de União.</span><span class="sxs-lookup"><span data-stu-id="0565c-115">Specifies zero or more field attributes that apply to a union member.</span></span> <span data-ttu-id="0565c-116">Os atributos de campo válidos incluem **\[** [**primeiro \_**](first-is.md), **\]** **\[** o [**último \_**](last-is.md)é **\]** , **\[** o [**comprimento \_ é**](length-is.md) **\]** , **\[** [**máx \_**](max-is.md) **\]** ., **\[** o [**tamanho \_ é**](size-is.md) **\]** ; a cadeia de caracteres de atributos de uso **\[** [](string.md) **\]** , **\[** [**ignorar**](ignore.md) **\]** e **\[** o [**\_ identificador de contexto**](context-handle.md) **\]** ; o atributo de ponteiro **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** ou **\[** [**PTR**](ptr.md) **\]** ; e para os membros que estão em suas próprias uniões, o **\[** [**\_ tipo de alternância**](switch-type.md)de atributo Union **\]** .</span><span class="sxs-lookup"><span data-stu-id="0565c-116">Valid field attributes include **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and for members that are themselves unions, the union attribute **\[**[**switch\_type**](switch-type.md)**\]**.</span></span> <span data-ttu-id="0565c-117">Separe vários atributos de campo com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="0565c-117">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="0565c-118">*especificador de tipo Union*</span><span class="sxs-lookup"><span data-stu-id="0565c-118">*union-type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="0565c-119">Especifica o identificador de tipo de [**União**](union.md) .</span><span class="sxs-lookup"><span data-stu-id="0565c-119">Specifies the [**union**](union.md) type identifier.</span></span> <span data-ttu-id="0565c-120">Uma especificação de armazenamento opcional pode preceder o *especificador de tipo*.</span><span class="sxs-lookup"><span data-stu-id="0565c-120">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="0565c-121">*Declarador e Declarador-lista*</span><span class="sxs-lookup"><span data-stu-id="0565c-121">*declarator and declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="0565c-122">Especifica um Declarador C padrão, como um identificador, Declarador de ponteiro e Declarador de matriz.</span><span class="sxs-lookup"><span data-stu-id="0565c-122">Specifies a standard C declarator, such as an identifier, pointer declarator, and array declarator.</span></span> <span data-ttu-id="0565c-123">(Os declaradores de função e as declarações de campo de bits não são permitidas em uniões que são transmitidas em chamadas de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="0565c-123">(Function declarators and bit-field declarations are not allowed in unions that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="0565c-124">Esses declaradores são permitidos em uniões que não são transmitidas.) Separe vários declaradores com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="0565c-124">These declarators are allowed in unions that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> <dt>

<span data-ttu-id="0565c-125">*lista de atributos de função*</span><span class="sxs-lookup"><span data-stu-id="0565c-125">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="0565c-126">Especifica zero ou mais atributos que se aplicam à função.</span><span class="sxs-lookup"><span data-stu-id="0565c-126">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="0565c-127">Os atributos de função válidos são **\[** [**retorno de chamada**](callback.md) **\]** , **\[** [**local**](local.md) **\]** ; o atributo de ponteiro **\[ ref \]**, **\[ \] Unique** ou **\[ PTR \]**; e a cadeia de **\[ caracteres \]** de atributos de uso, **\[ ignorar \]** e **\[ \_ \] identificador de contexto**.</span><span class="sxs-lookup"><span data-stu-id="0565c-127">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**.</span></span>

</dd> <dt>

<span data-ttu-id="0565c-128">*especificador de tipo*</span><span class="sxs-lookup"><span data-stu-id="0565c-128">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="0565c-129">Especifica um [tipo base](midl-base-types.md), [**struct**](struct.md), [**Union**](union.md), tipo de [**Enumeração**](enum.md) ou identificador de tipo.</span><span class="sxs-lookup"><span data-stu-id="0565c-129">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="0565c-130">Uma especificação de armazenamento opcional pode preceder o *especificador de tipo*.</span><span class="sxs-lookup"><span data-stu-id="0565c-130">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="0565c-131">*Declarador de ponteiro*</span><span class="sxs-lookup"><span data-stu-id="0565c-131">*pointer-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="0565c-132">Especifica zero ou mais declaradores de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="0565c-132">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="0565c-133">Um Declarador de ponteiro é o mesmo que o Declarador de ponteiro usado em C; Ele é construído a partir do \* designador, modificadores, como **distante** e o qualificador [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="0565c-133">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="0565c-134">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="0565c-134">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="0565c-135">Especifica o nome do procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="0565c-135">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="0565c-136">*param-attr-List*</span><span class="sxs-lookup"><span data-stu-id="0565c-136">*param-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="0565c-137">Especifica zero ou mais atributos apropriados para o tipo de parâmetro especificado.</span><span class="sxs-lookup"><span data-stu-id="0565c-137">Specifies zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="0565c-138">Atributos de parâmetro podem levar os atributos direcionais para **\[ dentro \]** e para **\[ \] fora**, os atributos de campo **\[ primeiro \_ são \]**, **\[ Last \_ is \]**, **\[ length \_ is \]**, **\[ Max \_ is \]**, **\[ Size \_ is \]** e **\[ switch \_ Type \]**; o atributo ponteiro **\[ ref \]**, **\[ Unique \]** ou **\[ PTR \]**; e o **\[ \_ identificador \] de contexto** e a cadeia de **\[ caracteres \]** de uso de atributos de utilização.</span><span class="sxs-lookup"><span data-stu-id="0565c-138">Parameter attributes can take the directional attributes **\[in\]** and **\[out\]**, the field attributes **\[first\_is\]**, **\[last\_is\]**, **\[length\_is\]**, **\[max\_is\]**, **\[size\_is\]**, and **\[switch\_type\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[context\_handle\]** and **\[string\]**.</span></span> <span data-ttu-id="0565c-139">O atributo de uso **\[ ignore \]** não pode ser usado como um atributo de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0565c-139">The usage attribute **\[ignore\]** cannot be used as a parameter attribute.</span></span> <span data-ttu-id="0565c-140">Separe vários atributos com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="0565c-140">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="0565c-141">*tipo de União*</span><span class="sxs-lookup"><span data-stu-id="0565c-141">*union-type*</span></span> 
</dt> <dd>

<span data-ttu-id="0565c-142">Identifica o especificador de tipo [**Union**](union.md) .</span><span class="sxs-lookup"><span data-stu-id="0565c-142">Identifies the [**union**](union.md) type specifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0565c-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="0565c-143">Remarks</span></span>

<span data-ttu-id="0565c-144">O discriminante associado à **\[ opção \_ \]** o atributo deve ser definido no mesmo nível lógico que a União:</span><span class="sxs-lookup"><span data-stu-id="0565c-144">The discriminant associated with the **\[switch\_is\]** attribute must be defined at the same logical level as the union:</span></span>

-   <span data-ttu-id="0565c-145">Quando Union é um parâmetro, o discriminante de União deve ser outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0565c-145">When the union is a parameter, the union discriminant must be another parameter.</span></span>
-   <span data-ttu-id="0565c-146">Quando Union é um campo de uma estrutura, discriminante deve ser outro campo da mesma estrutura.</span><span class="sxs-lookup"><span data-stu-id="0565c-146">When the union is a field of a structure, the discriminant must be another field of the same structure.</span></span>

<span data-ttu-id="0565c-147">A sequência em uma estrutura ou uma lista de parâmetros de função não é significativa.</span><span class="sxs-lookup"><span data-stu-id="0565c-147">The sequence in a structure or a function parameter list is not significant.</span></span> <span data-ttu-id="0565c-148">A União pode preceder ou seguir o discriminante.</span><span class="sxs-lookup"><span data-stu-id="0565c-148">The union can either precede or follow the discriminant.</span></span>

<span data-ttu-id="0565c-149">O atributo **\[ switch \_ é \]** pode aparecer como um atributo de campo ou como um atributo de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0565c-149">The **\[switch\_is\]** attribute can appear as a field attribute or as a parameter attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="0565c-150">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0565c-150">Examples</span></span>

``` syntax
typedef [switch_type(short)] union _WILLIE_UNION_TYPE 
{ 
    [case(24)] 
        float fMays; 
    [case(25)] 
        double dMcCovey; 
    [default] 
        ; 
} WILLIE_UNION_TYPE; 
 
typedef struct _WINNER_TYPE 
{ 
    [switch_is(sUniformNumber)] WILLIE_UNION_TYPE w; 
    short sUniformNumber; 
} WINNER_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="0565c-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="0565c-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0565c-152">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="0565c-152">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="0565c-153">**retorno de chamada**</span><span class="sxs-lookup"><span data-stu-id="0565c-153">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="0565c-154">**const**</span><span class="sxs-lookup"><span data-stu-id="0565c-154">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="0565c-155">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="0565c-155">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="0565c-156">Uniões encapsuladas</span><span class="sxs-lookup"><span data-stu-id="0565c-156">Encapsulated Unions</span></span>](encapsulated-unions.md)
</dt> <dt>

[<span data-ttu-id="0565c-157">**enumera**</span><span class="sxs-lookup"><span data-stu-id="0565c-157">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="0565c-158">**primeiro \_ é**</span><span class="sxs-lookup"><span data-stu-id="0565c-158">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="0565c-159">**ignorar**</span><span class="sxs-lookup"><span data-stu-id="0565c-159">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="0565c-160">**último \_ é**</span><span class="sxs-lookup"><span data-stu-id="0565c-160">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="0565c-161">**comprimento \_ é**</span><span class="sxs-lookup"><span data-stu-id="0565c-161">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="0565c-162">**local**</span><span class="sxs-lookup"><span data-stu-id="0565c-162">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="0565c-163">**máximo \_ é**</span><span class="sxs-lookup"><span data-stu-id="0565c-163">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="0565c-164">Uniões não encapsuladas</span><span class="sxs-lookup"><span data-stu-id="0565c-164">Nonencapsulated Unions</span></span>](nonencapsulated-unions.md)
</dt> <dt>

[<span data-ttu-id="0565c-165">**ptr**</span><span class="sxs-lookup"><span data-stu-id="0565c-165">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="0565c-166">**ref**</span><span class="sxs-lookup"><span data-stu-id="0565c-166">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="0565c-167">**o tamanho \_ é**</span><span class="sxs-lookup"><span data-stu-id="0565c-167">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="0565c-168">**Strings**</span><span class="sxs-lookup"><span data-stu-id="0565c-168">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="0565c-169">**struct**</span><span class="sxs-lookup"><span data-stu-id="0565c-169">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="0565c-170">**tipo de comutador \_**</span><span class="sxs-lookup"><span data-stu-id="0565c-170">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="0565c-171">**unida**</span><span class="sxs-lookup"><span data-stu-id="0565c-171">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="0565c-172">**diferente**</span><span class="sxs-lookup"><span data-stu-id="0565c-172">**unique**</span></span>](unique.md)
</dt> </dl>

 

 





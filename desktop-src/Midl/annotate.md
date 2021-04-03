---
title: anotar atributo
description: O atributo \ anotar \ permite que você especifique uma cadeia de caracteres de anotação SAL para o método, o parâmetro ou o campo de estrutura especificado.
ms.assetid: D0A35DCD-BD2F-455B-A040-5D63E4572D83
keywords:
- atributo de anotação MIDL
topic_type:
- apiref
api_name:
- annotate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 820310c6aca0e5269d6febff5dc7d3208413110c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103642296"
---
# <a name="annotate-attribute"></a><span data-ttu-id="3f558-104">anotar atributo</span><span class="sxs-lookup"><span data-stu-id="3f558-104">annotate attribute</span></span>

<span data-ttu-id="3f558-105">O atributo **\[ anotar \]** permite que você especifique uma cadeia de caracteres de anotação sal para o método, o parâmetro ou o campo de estrutura especificado.</span><span class="sxs-lookup"><span data-stu-id="3f558-105">The **\[annotate\]** attribute allows you to specify a SAL annotation string for the specified method, parameter, or structure field.</span></span>

``` syntax
[ annotation(â€œstringâ€0,  [, function-attribute-list] ] function-declarator ;
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ annotation(â€œstringâ€) [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="3f558-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f558-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f558-107">*cadeia de caracteres*</span><span class="sxs-lookup"><span data-stu-id="3f558-107">*string*</span></span> 
</dt> <dd>

<span data-ttu-id="3f558-108">Cadeia de caracteres de anotação SAL especificada.</span><span class="sxs-lookup"><span data-stu-id="3f558-108">Specified SAL annotation string.</span></span>

</dd> <dt>

<span data-ttu-id="3f558-109">*lista de atributos de função*</span><span class="sxs-lookup"><span data-stu-id="3f558-109">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="3f558-110">Especifica zero ou mais atributos que se aplicam à função.</span><span class="sxs-lookup"><span data-stu-id="3f558-110">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="3f558-111">Os atributos de função válidos incluem [**\[ \] retorno de chamada**](callback.md); os atributos de ponteiro [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)ou [**\[ PTR \]**](ptr.md); e a cadeia de [**\[ caracteres \]**](string.md)de atributos de uso, [**\[ ignore \]**](ignore.md)e o [**\[ \_ identificador \] de contexto**](context-handle.md).</span><span class="sxs-lookup"><span data-stu-id="3f558-111">Valid function attributes include [**\[callback\]**](callback.md); the pointer attributes [**\[ref\]**](ref.md), [**\[unique\]**](unique.md), or [**\[ptr\]**](ptr.md); and the usage attributes [**\[string\]**](string.md), [**\[ignore\]**](ignore.md), and [**\[context\_handle\]**](context-handle.md).</span></span> <span data-ttu-id="3f558-112">Vários atributos devem ser separados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="3f558-112">Multiple attributes must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="3f558-113">*função-declaradora*</span><span class="sxs-lookup"><span data-stu-id="3f558-113">*function-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="3f558-114">Especifica o especificador de tipo, o nome da função e a lista de parâmetros para a função.</span><span class="sxs-lookup"><span data-stu-id="3f558-114">Specifies the type specifier, function name, and parameter list for the function.</span></span>

</dd> <dt>

<span data-ttu-id="3f558-115">*especificador de tipo*</span><span class="sxs-lookup"><span data-stu-id="3f558-115">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="3f558-116">Especifica um tipo de **base \_**, [**\[ struct \]**](struct.md), [**Union**](union.md)ou tipo de [**\[ enumeração \]**](enum.md) ou identificador de tipo.</span><span class="sxs-lookup"><span data-stu-id="3f558-116">Specifies a **base\_type**, [**\[struct\]**](struct.md), [**union**](union.md), or [**\[enum\]**](enum.md) type or type identifier.</span></span> <span data-ttu-id="3f558-117">Uma especificação de armazenamento opcional pode preceder o *especificador de tipo*.</span><span class="sxs-lookup"><span data-stu-id="3f558-117">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="3f558-118">*Declarador de ponteiro*</span><span class="sxs-lookup"><span data-stu-id="3f558-118">*pointer-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="3f558-119">Especifica zero ou mais declaradores de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3f558-119">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="3f558-120">Um Declarador de ponteiro é o mesmo que um Declarador de ponteiro usado em C; Ele é construído a partir do \* designador, modificadores, como **distante** e o qualificador [**\[ const \]**](const.md).</span><span class="sxs-lookup"><span data-stu-id="3f558-120">A pointer declarator is the same as a pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**\[const\]**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="3f558-121">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="3f558-121">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="3f558-122">Especifica o nome do procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="3f558-122">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="3f558-123">*lista de atributos de parâmetro*</span><span class="sxs-lookup"><span data-stu-id="3f558-123">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="3f558-124">Especifica zero ou mais atributos apropriados para o tipo de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="3f558-124">Specifies zero or more attributes appropriate for the parameter type.</span></span> <span data-ttu-id="3f558-125">Atributos de parâmetro com o atributo [**\[ \] in**](in.md) também podem pegar o atributo direcional [**\[ out \]**](out-idl.md); os atributos de campo [**\[ First \_ são \]**](first-is.md), [**\[ Last \_ is \]**](last-is.md), [**\[ length \_ is \]**](length-is.md), [**\[ Max \_ is \]**](max-is.md), [**\[ Size \_ is \]**](size-is.md)e [**\[ switch \_ Type \]**](switch-type.md); os atributos pointer [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)ou [**\[ PTR \]**](ptr.md); e o [**\[ \_ identificador \] de contexto**](context-handle.md) e a [**\[ cadeia \] de caracteres**](string.md)de atributos de uso.</span><span class="sxs-lookup"><span data-stu-id="3f558-125">Parameter attributes with the [**\[in\]**](in.md) attribute can also take the directional attribute [**\[out\]**](out-idl.md); the field attributes [**\[first\_is\]**](first-is.md), [**\[last\_is\]**](last-is.md), [**\[length\_is\]**](length-is.md), [**\[max\_is\]**](max-is.md), [**\[size\_is\]**](size-is.md), and [**\[switch\_type\]**](switch-type.md); the pointer attributes [**\[ref\]**](ref.md), [**\[unique\]**](unique.md), or [**\[ptr\]**](ptr.md); and the usage attributes [**\[context\_handle\]**](context-handle.md) and [**\[string\]**](string.md).</span></span> <span data-ttu-id="3f558-126">O atributo de uso [**\[ ignore \]**](ignore.md) não pode ser usado como um atributo de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="3f558-126">The usage attribute [**\[ignore\]**](ignore.md) cannot be used as a parameter attribute.</span></span> <span data-ttu-id="3f558-127">Vários atributos devem ser separados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="3f558-127">Multiple attributes must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="3f558-128">*Declarador*</span><span class="sxs-lookup"><span data-stu-id="3f558-128">*declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="3f558-129">Especifica os declaradores padrão C, como identificadores, declaradores de ponteiro e declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="3f558-129">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="3f558-130">Para obter mais informações, consulte [matriz e Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**\[ matrizes \]**](../rpc/arrays.md)e [matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="3f558-130">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**\[arrays\]**](../rpc/arrays.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="3f558-131">O Declarador de parâmetro no Declarador de função, como o nome do parâmetro, é opcional.</span><span class="sxs-lookup"><span data-stu-id="3f558-131">The parameter declarator in the function declarator, such as the parameter name, is optional.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3f558-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="3f558-132">Remarks</span></span>

<span data-ttu-id="3f558-133">O atributo **\[ anotar \]** permite substituir anotações sal geradas por MIDL ou adicioná-las em locais onde o MIDL não gera uma anotação explicitamente.</span><span class="sxs-lookup"><span data-stu-id="3f558-133">The **\[annotate\]** attribute allows overriding MIDL-generated SAL annotations or adding them in places where MIDL does not explicitly generate an annotation.</span></span> <span data-ttu-id="3f558-134">Se [**/sal**](-sal.md) não for especificado na linha de comando, esse atributo será ignorado.</span><span class="sxs-lookup"><span data-stu-id="3f558-134">If [**/sal**](-sal.md) is not specified on the command line, this attribute is ignored.</span></span>

## <a name="see-also"></a><span data-ttu-id="3f558-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f558-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f558-136">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="3f558-136">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="3f558-137">**/sal**</span><span class="sxs-lookup"><span data-stu-id="3f558-137">**/sal**</span></span>](-sal.md)
</dt> <dt>

[<span data-ttu-id="3f558-138">**/sal \_ local**</span><span class="sxs-lookup"><span data-stu-id="3f558-138">**/sal\_local**</span></span>](-sal-local.md)
</dt> </dl>

 

 
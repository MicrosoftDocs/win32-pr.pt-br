---
title: atributo string
description: O atributo \ String \ indica que a matriz char-dimensional, WCHAR \_ t, Byte (ou equivalente) ou o ponteiro para tal matriz deve ser tratado como uma cadeia de caracteres.
ms.assetid: 379cd59e-7540-4188-9b5c-6c25a8928999
keywords:
- atributo de cadeia de caracteres MIDL
topic_type:
- apiref
api_name:
- string
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae2bd3c56bcf09d1c47343f903653e9d83113b1d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917254"
---
# <a name="string-attribute"></a><span data-ttu-id="a22cf-104">atributo string</span><span class="sxs-lookup"><span data-stu-id="a22cf-104">string attribute</span></span>

<span data-ttu-id="a22cf-105">O atributo **\[ \] String** indica que a matriz [**Char**](char-idl.md)-dimensional, [**WCHAR \_ t**](wchar-t.md), [**byte**](byte.md) (ou equivalente) ou o ponteiro para tal matriz deve ser tratado como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a22cf-105">The **\[string\]** attribute indicates that the one-dimensional [**char**](char-idl.md), [**wchar\_t**](wchar-t.md), [**byte**](byte.md) (or equivalent) array or the pointer to such an array must be treated as a string.</span></span> <span data-ttu-id="a22cf-106">A cadeia de caracteres também pode ser uma matriz (ou um ponteiro para uma matriz) de construções cujos campos são todos do tipo **byte**.</span><span class="sxs-lookup"><span data-stu-id="a22cf-106">The string can also be an array (or a pointer to an array) of constructs whose fields are all of the type **byte**.</span></span>

``` syntax
typedef [ string [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef [ struct | union ] 
{
    [ string [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...
};

[ string [[ , function-attribute-list ]] ] type-specifier ptr-decl function-name(
  [[ [ parameter-attribute-list ] ]] type-specifier [[standard-declarator]]
  , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ string [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
  , ...);
```

## <a name="parameters"></a><span data-ttu-id="a22cf-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a22cf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a22cf-108">*lista de atributos de tipo*</span><span class="sxs-lookup"><span data-stu-id="a22cf-108">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a22cf-109">Especifica um ou mais atributos que se aplicam a um tipo.</span><span class="sxs-lookup"><span data-stu-id="a22cf-109">Specifies one or more attributes that apply to a type.</span></span> <span data-ttu-id="a22cf-110">Atributos de tipo válidos incluem **\[** [**identificador**](handle.md) **\]** , **\[** [**\_ tipo de comutador**](switch-type.md) **\]** , **\[** [**transmissão \_ como**](transmit-as.md) **\]** ; o atributo de ponteiro **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** ou **\[** [**PTR**](ptr.md) **\]** ; e o identificador de contexto de atributos de uso **\[** [**\_**](context-handle.md) **\]** , **\[ cadeia de \] caracteres** e **\[** [**ignorar**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="a22cf-110">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[string\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="a22cf-111">Separe vários atributos com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="a22cf-111">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="a22cf-112">*especificador de tipo*</span><span class="sxs-lookup"><span data-stu-id="a22cf-112">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="a22cf-113">Especifica um [tipo de base](midl-base-types.md), tipo de [**struct**](struct.md) ou identificador de tipo.</span><span class="sxs-lookup"><span data-stu-id="a22cf-113">Specifies a [base type](midl-base-types.md), [**struct**](struct.md) type, or type identifier.</span></span> <span data-ttu-id="a22cf-114">Uma especificação de armazenamento opcional pode preceder o *especificador de tipo*.</span><span class="sxs-lookup"><span data-stu-id="a22cf-114">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="a22cf-115">*padrão-Declarador*</span><span class="sxs-lookup"><span data-stu-id="a22cf-115">*standard-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="a22cf-116">Especifica um Declarador C padrão, como um identificador, um Declarador de ponteiro ou um Declarador de matriz.</span><span class="sxs-lookup"><span data-stu-id="a22cf-116">Specifies a standard C declarator, such as an identifier, a pointer declarator, or an array declarator.</span></span> <span data-ttu-id="a22cf-117">Para obter mais informações, consulte [matriz e Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrizes**](arrays-1.md)e [matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="a22cf-117">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md)., and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span>

</dd> <dt>

<span data-ttu-id="a22cf-118">*Declarador-lista*</span><span class="sxs-lookup"><span data-stu-id="a22cf-118">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a22cf-119">Especifica os declaradores padrão C, como identificadores, declaradores de ponteiro e declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="a22cf-119">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="a22cf-120">Para obter mais informações, consulte [matriz e Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrizes**](arrays-1.md)e [matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="a22cf-120">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md)., and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="a22cf-121">A *lista de declaradores* consiste em um ou mais declaradores separados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="a22cf-121">The *declarator-list* consists of one or more declarators separated by commas.</span></span> <span data-ttu-id="a22cf-122">O identificador de nome de parâmetro no Declarador de função é opcional.</span><span class="sxs-lookup"><span data-stu-id="a22cf-122">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="a22cf-123">*lista de atributos de campo*</span><span class="sxs-lookup"><span data-stu-id="a22cf-123">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a22cf-124">Especifica zero ou mais atributos de campo que se aplicam à estrutura, ao membro de União ou ao parâmetro de função.</span><span class="sxs-lookup"><span data-stu-id="a22cf-124">Specifies zero or more field attributes that apply to the structure, union member, or function parameter.</span></span> <span data-ttu-id="a22cf-125">Os dois atributos de campo válidos são **\[** [**\_ Max**](max-is.md) **\]** e **\[** [**Size \_ é**](size-is.md) **\]** ; a cadeia de **\[ caracteres \]** de atributos de uso, **\[ ignorar \]** e o **\[ \_ identificador \] de contexto**, o atributo de ponteiro **\[** [**ref**](ref.md) **\]** , **\[ Unique \]** ou **\[** [**PTR**](ptr.md) **\]** , e o **\[ \_ tipo \] de opção** de atributo Union.</span><span class="sxs-lookup"><span data-stu-id="a22cf-125">The two valid field attributes are **\[**[**max\_is**](max-is.md)**\]** and **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**, the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[unique\]**, or **\[**[**ptr**](ptr.md)**\]**, and the union attribute **\[switch\_type\]**.</span></span> <span data-ttu-id="a22cf-126">Separe vários atributos de campo com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="a22cf-126">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="a22cf-127">*lista de atributos de função*</span><span class="sxs-lookup"><span data-stu-id="a22cf-127">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a22cf-128">Especifica zero ou mais atributos que se aplicam à função.</span><span class="sxs-lookup"><span data-stu-id="a22cf-128">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="a22cf-129">Os atributos de função válidos são **\[** [**retorno de chamada**](callback.md) **\]** , **\[** [**local**](local.md) **\]** ; o atributo de ponteiro **\[ ref \]**, **\[ \] Unique** ou **\[ PTR \]**; e a cadeia de **\[ caracteres \]** de atributos de uso, **\[ ignorar \]** e **\[ \_ \] identificador de contexto**.</span><span class="sxs-lookup"><span data-stu-id="a22cf-129">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**.</span></span>

</dd> <dt>

<span data-ttu-id="a22cf-130">*declaração de PTR*</span><span class="sxs-lookup"><span data-stu-id="a22cf-130">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="a22cf-131">Especifica um Declarador de ponteiro opcional ao qual o atributo de **\[ cadeia de caracteres \]** se aplica.</span><span class="sxs-lookup"><span data-stu-id="a22cf-131">Specifies an optional pointer declarator to which the **\[string\]** attribute applies.</span></span> <span data-ttu-id="a22cf-132">Um Declarador de ponteiro é o mesmo que o Declarador de ponteiro usado em C; Ele é construído a partir do \* designador, modificadores, como **distante** e o qualificador [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="a22cf-132">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="a22cf-133">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="a22cf-133">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a22cf-134">Especifica o nome do procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="a22cf-134">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="a22cf-135">*lista de atributos de parâmetro*</span><span class="sxs-lookup"><span data-stu-id="a22cf-135">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a22cf-136">Consiste em zero ou mais atributos apropriados para o tipo de parâmetro especificado.</span><span class="sxs-lookup"><span data-stu-id="a22cf-136">Consists of zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="a22cf-137">Os atributos de parâmetro podem levar os atributos direcionais para **\[ dentro \]** e para **\[ \] fora**; o campo máximo de atributos **\[** [**\_ é**](max-is.md) **\]** e o **\[** [**tamanho \_ é**](size-is.md) **\]** ; o atributo de ponteiro **\[ ref \]**, **\[ Unique \]** ou **\[ PTR \]**; e o **\[ \_ identificador \] de contexto** e a cadeia de **\[ caracteres \]** de atributos de uso.</span><span class="sxs-lookup"><span data-stu-id="a22cf-137">Parameter attributes can take the directional attributes **\[in\]** and **\[out\]**; the field attributes **\[**[**max\_is**](max-is.md)**\]** and **\[**[**size\_is**](size-is.md)**\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[context\_handle\]** and **\[string\]**.</span></span> <span data-ttu-id="a22cf-138">O atributo de uso **\[ ignore \]** não pode ser usado como um atributo de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a22cf-138">The usage attribute **\[ignore\]** cannot be used as a parameter attribute.</span></span> <span data-ttu-id="a22cf-139">Separe vários atributos com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="a22cf-139">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a22cf-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="a22cf-140">Remarks</span></span>

<span data-ttu-id="a22cf-141">Se o atributo de **\[ cadeia de \] caracteres** for usado com uma matriz cujos limites são determinados em tempo de execução, você também deverá especificar que um **\[ tamanho \_ é \]** ou **\[ Max \_ é \]** o atributo, como no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="a22cf-141">If the **\[string\]** attribute is used with an array whose bounds are determined at run time, you must also specify a **\[size\_is\]** or **\[max\_is\]** attribute, as in the following example:</span></span>

``` syntax
/* a string that can hold up to MAX_STRING_LENGTH characters */
typedef [string, max_is(MAX_STRING_LENGTH)] char line[];
```

<span data-ttu-id="a22cf-142">O atributo de **\[ \] cadeia de caracteres** não pode ser usado com atributos que especificam o intervalo de elementos transmitidos, como **\[ First \_ é \]**, **\[ Last \_ is \]** e **\[ length \_ is \]**.</span><span class="sxs-lookup"><span data-stu-id="a22cf-142">The **\[string\]** attribute cannot be used with attributes that specify the range of transmitted elements, such as **\[first\_is\]**, **\[last\_is\]**, and **\[length\_is\]**.</span></span>

<span data-ttu-id="a22cf-143">Quando usado em matrizes multidimensionais, o atributo de **\[ cadeia de caracteres \]** se aplica à matriz mais à direita.</span><span class="sxs-lookup"><span data-stu-id="a22cf-143">When used on multidimensional arrays, the **\[string\]** attribute applies to the rightmost array.</span></span>

<span data-ttu-id="a22cf-144">Para definir uma cadeia de caracteres contada, não use o atributo de **\[ cadeia de caracteres \]** .</span><span class="sxs-lookup"><span data-stu-id="a22cf-144">To define a counted string, do not use the **\[string\]** attribute.</span></span> <span data-ttu-id="a22cf-145">Use uma matriz de caracteres ou um ponteiro baseado em caractere, como o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a22cf-145">Use a character array or character-based pointer such as the following:</span></span>

``` syntax
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
} counted_string;
```

<span data-ttu-id="a22cf-146">O atributo **\[ String \]** especifica que o stub deve usar um método fornecido por linguagem para determinar o comprimento das cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a22cf-146">The **\[string\]** attribute specifies that the stub should use a language-supplied method to determine the length of strings.</span></span>

<span data-ttu-id="a22cf-147">Ao declarar cadeias de caracteres em C, você deve alocar espaço para um caractere extra que marque o final da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a22cf-147">When declaring strings in C, you must allocate space for an extra character that marks the end of the string.</span></span>

## <a name="examples"></a><span data-ttu-id="a22cf-148">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a22cf-148">Examples</span></span>

``` syntax
/* a string type that can hold up to 80 characters */ 
typedef [string] char line[81]; 
 
HRESULT Proc1([in, string] char * pszName);
```

## <a name="see-also"></a><span data-ttu-id="a22cf-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="a22cf-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a22cf-150">**Storage**</span><span class="sxs-lookup"><span data-stu-id="a22cf-150">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="a22cf-151">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="a22cf-151">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="a22cf-152">**retorno de chamada**</span><span class="sxs-lookup"><span data-stu-id="a22cf-152">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="a22cf-153">**char**</span><span class="sxs-lookup"><span data-stu-id="a22cf-153">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="a22cf-154">**const**</span><span class="sxs-lookup"><span data-stu-id="a22cf-154">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="a22cf-155">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="a22cf-155">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="a22cf-156">**enumera**</span><span class="sxs-lookup"><span data-stu-id="a22cf-156">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="a22cf-157">**primeiro \_ é**</span><span class="sxs-lookup"><span data-stu-id="a22cf-157">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="a22cf-158">**processamento**</span><span class="sxs-lookup"><span data-stu-id="a22cf-158">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="a22cf-159">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="a22cf-159">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="a22cf-160">**ignorar**</span><span class="sxs-lookup"><span data-stu-id="a22cf-160">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="a22cf-161">**último \_ é**</span><span class="sxs-lookup"><span data-stu-id="a22cf-161">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="a22cf-162">**comprimento \_ é**</span><span class="sxs-lookup"><span data-stu-id="a22cf-162">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="a22cf-163">**local**</span><span class="sxs-lookup"><span data-stu-id="a22cf-163">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="a22cf-164">**máximo \_ é**</span><span class="sxs-lookup"><span data-stu-id="a22cf-164">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="a22cf-165">**padrão de ponteiro \_**</span><span class="sxs-lookup"><span data-stu-id="a22cf-165">**pointer\_default**</span></span>](pointer-default.md)
</dt> <dt>

[<span data-ttu-id="a22cf-166">**ptr**</span><span class="sxs-lookup"><span data-stu-id="a22cf-166">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="a22cf-167">**ref**</span><span class="sxs-lookup"><span data-stu-id="a22cf-167">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="a22cf-168">**o tamanho \_ é**</span><span class="sxs-lookup"><span data-stu-id="a22cf-168">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="a22cf-169">**struct**</span><span class="sxs-lookup"><span data-stu-id="a22cf-169">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="a22cf-170">**tipo de comutador \_**</span><span class="sxs-lookup"><span data-stu-id="a22cf-170">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="a22cf-171">**transmitir \_ como**</span><span class="sxs-lookup"><span data-stu-id="a22cf-171">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="a22cf-172">**unida**</span><span class="sxs-lookup"><span data-stu-id="a22cf-172">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="a22cf-173">**diferente**</span><span class="sxs-lookup"><span data-stu-id="a22cf-173">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="a22cf-174">**WCHAR \_ t**</span><span class="sxs-lookup"><span data-stu-id="a22cf-174">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 
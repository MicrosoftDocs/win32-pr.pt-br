---
title: atributo ref
description: O atributo \ ref \ identifica um ponteiro de referência. Ele é usado simplesmente para representar um nível de indireção.
ms.assetid: db4ff938-0f38-4f77-bb65-f728ffd609e0
keywords:
- MIDL do atributo ref
topic_type:
- apiref
api_name:
- ref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82bc5762eea78b3ce73ab3db58e9bb567b051675
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823698"
---
# <a name="ref-attribute"></a><span data-ttu-id="4fce6-105">atributo ref</span><span class="sxs-lookup"><span data-stu-id="4fce6-105">ref attribute</span></span>

<span data-ttu-id="4fce6-106">O atributo **\[ ref \]** identifica um ponteiro de referência.</span><span class="sxs-lookup"><span data-stu-id="4fce6-106">The **\[ref\]** attribute identifies a reference pointer.</span></span> <span data-ttu-id="4fce6-107">Ele é usado simplesmente para representar um nível de indireção.</span><span class="sxs-lookup"><span data-stu-id="4fce6-107">It is used simply to represent a level of indirection.</span></span>

``` syntax
pointer_default(ref)

typedef [ ref [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef [ struct | union ] 
{
    [ ref [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...}

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ ref [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="4fce6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4fce6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fce6-109">*lista de atributos de tipo*</span><span class="sxs-lookup"><span data-stu-id="4fce6-109">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4fce6-110">Especifica um ou mais atributos que se aplicam ao tipo.</span><span class="sxs-lookup"><span data-stu-id="4fce6-110">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="4fce6-111">Atributos de tipo válidos incluem **\[** [**identificador**](handle.md) **\]** , **\[** [**\_ tipo de comutador**](switch-type.md) **\]** , **\[** [**transmissão \_ como**](transmit-as.md) **\]** ; os atributos de ponteiro **\[ ref \]**, **\[** [**Unique**](unique.md) **\]** ou **\[** [**PTR**](ptr.md) **\]** ; e o identificador de contexto de atributos de uso **\[** [**\_**](context-handle.md) **\]** , **\[** [**cadeia de caracteres**](string.md) **\]** e **\[** [**ignorar**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="4fce6-111">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attributes **\[ref\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="4fce6-112">Separe vários atributos com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="4fce6-112">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="4fce6-113">*especificador de tipo*</span><span class="sxs-lookup"><span data-stu-id="4fce6-113">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="4fce6-114">Especifica um tipo de [base](midl-base-types.md), [**struct**](struct.md), [**Union**](union.md)ou tipo de [**Enumeração**](enum.md) ou identificador de tipo.</span><span class="sxs-lookup"><span data-stu-id="4fce6-114">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), or [**enum**](enum.md) type or type identifier.</span></span> <span data-ttu-id="4fce6-115">Uma especificação de armazenamento opcional pode preceder o *especificador de tipo*.</span><span class="sxs-lookup"><span data-stu-id="4fce6-115">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="4fce6-116">*padrão-Declarador*</span><span class="sxs-lookup"><span data-stu-id="4fce6-116">*standard-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="4fce6-117">Especifica um Declarador C padrão, como um identificador, um Declarador de ponteiro ou um Declarador de matriz.</span><span class="sxs-lookup"><span data-stu-id="4fce6-117">Specifies a standard C declarator, such as an identifier, a pointer declarator, or an array declarator.</span></span> <span data-ttu-id="4fce6-118">Para obter mais informações, consulte [matriz e Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrizes**](arrays-1.md)e [matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="4fce6-118">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span>

</dd> <dt>

<span data-ttu-id="4fce6-119">*Declarador-lista*</span><span class="sxs-lookup"><span data-stu-id="4fce6-119">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4fce6-120">Especifica os declaradores padrão C, como identificadores, declaradores de ponteiro e declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="4fce6-120">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="4fce6-121">Para obter mais informações, consulte [matriz e Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrizes**](arrays-1.md)e [matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="4fce6-121">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="4fce6-122">A *lista de declaradores* consiste em um ou mais declaradores separados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="4fce6-122">The *declarator-list* consists of one or more declarators separated by commas.</span></span> <span data-ttu-id="4fce6-123">O identificador de nome de parâmetro no Declarador de função é opcional.</span><span class="sxs-lookup"><span data-stu-id="4fce6-123">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="4fce6-124">*lista de atributos de campo*</span><span class="sxs-lookup"><span data-stu-id="4fce6-124">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4fce6-125">Especifica zero ou mais atributos de campo que se aplicam à estrutura, ao membro de União ou ao parâmetro de função.</span><span class="sxs-lookup"><span data-stu-id="4fce6-125">Specifies zero or more field attributes that apply to the structure, union member, or function parameter.</span></span> <span data-ttu-id="4fce6-126">Os atributos de campo válidos incluem **\[** [**primeiro \_**](first-is.md) **\]** , **\[** o [**último \_**](last-is.md)é **\]** , **\[** o [**comprimento \_ é**](length-is.md) **\]** , **\[** [**\_ máx**](max-is.md) **\]** ., **\[** o [**tamanho \_ é**](size-is.md) **\]** ; a cadeia de caracteres de atributos de uso **\[** [](string.md) **\]** , **\[** [**ignorar**](ignore.md) **\]** e **\[** o [**\_ identificador de contexto**](context-handle.md) **\]** ; o atributo de ponteiro **\[ ref \]**, **\[** [**Unique**](unique.md) **\]** ou **\[** [**PTR**](ptr.md) **\]** ; e o **\[** [**\_ tipo de opção**](switch-type.md)de atributo Union **\]** .</span><span class="sxs-lookup"><span data-stu-id="4fce6-126">Valid field attributes include **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**; the pointer attribute **\[ref\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the union attribute **\[**[**switch\_type**](switch-type.md)**\]**.</span></span> <span data-ttu-id="4fce6-127">Separe vários atributos de campo com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="4fce6-127">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="4fce6-128">*lista de atributos de função*</span><span class="sxs-lookup"><span data-stu-id="4fce6-128">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4fce6-129">Especifica zero ou mais atributos que se aplicam à função.</span><span class="sxs-lookup"><span data-stu-id="4fce6-129">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="4fce6-130">Os atributos de função válidos são **\[** [**retorno de chamada**](callback.md) **\]** , **\[** [**local**](local.md) **\]** ; o atributo de ponteiro **\[ \] ref**, **\[** [**Unique**](unique.md) **\]** ou **\[** [**PTR**](ptr.md) **\]** ; e a cadeia de caracteres de atributos de uso **\[** [](string.md) **\]** , **\[** [**ignorar**](ignore.md) **\]** e **\[** [**\_ identificador de contexto**](context-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="4fce6-130">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[ref\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="4fce6-131">*declaração de PTR*</span><span class="sxs-lookup"><span data-stu-id="4fce6-131">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="4fce6-132">Especifica pelo menos um Declarador de ponteiro ao qual o atributo **\[ ref \]** se aplica.</span><span class="sxs-lookup"><span data-stu-id="4fce6-132">Specifies at least one pointer declarator to which the **\[ref\]** attribute applies.</span></span> <span data-ttu-id="4fce6-133">Um Declarador de ponteiro é o mesmo que o Declarador de ponteiro usado em C; Ele é construído a partir do \* designador, modificadores, como **distante** e o qualificador [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="4fce6-133">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="4fce6-134">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="4fce6-134">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="4fce6-135">Especifica o nome do procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="4fce6-135">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="4fce6-136">*lista de atributos de parâmetro*</span><span class="sxs-lookup"><span data-stu-id="4fce6-136">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4fce6-137">Consiste em zero ou mais atributos apropriados para o tipo de parâmetro especificado.</span><span class="sxs-lookup"><span data-stu-id="4fce6-137">Consists of zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="4fce6-138">Os atributos de parâmetro podem levar os atributos direcionais para **\[** [**dentro**](in.md) **\]** e para **\[** [**fora**](out-idl.md) **\]** ; os atributos do campo **\[** [**primeiro \_ são**](first-is.md), **\]** **\[** [**Last \_ is**](last-is.md) **\]** , **\[** [**length \_ is**](length-is.md), **\]** **\[** [**Max \_ is**](max-is.md), **\]** **\[** [**Size \_ is**](size-is.md) **\]** e **\[** [**switch \_ Type**](switch-type.md) **\]** ; o atributo pointer **\[ \] ref**, **\[** [**Unique**](unique.md) **\]** ou **\[** [**PTR**](ptr.md) **\]** ; e o identificador de contexto de atributos de uso e a **\[** [**\_**](context-handle.md) **\]** cadeia de **\[** [**caracteres**](string.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="4fce6-138">Parameter attributes can take the directional attributes **\[**[**in**](in.md)**\]** and **\[**[**out**](out-idl.md)**\]**; the field attributes **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**, and **\[**[**switch\_type**](switch-type.md)**\]**; the pointer attribute **\[ref\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]** and **\[**[**string**](string.md)**\]**.</span></span> <span data-ttu-id="4fce6-139">O atributo de uso **\[** [**ignore**](ignore.md) **\]** não pode ser usado como um atributo de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="4fce6-139">The usage attribute **\[**[**ignore**](ignore.md)**\]** cannot be used as a parameter attribute.</span></span> <span data-ttu-id="4fce6-140">Separe vários atributos com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="4fce6-140">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4fce6-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="4fce6-141">Remarks</span></span>

<span data-ttu-id="4fce6-142">Um atributo de ponteiro pode ser aplicado como um atributo de tipo, como um atributo de campo que se aplica a um membro de estrutura, membro de União ou parâmetro; ou como um atributo de função que se aplica ao tipo de retorno da função.</span><span class="sxs-lookup"><span data-stu-id="4fce6-142">A pointer attribute can be applied as a type attribute, as a field attribute that applies to a structure member, union member, or parameter; or as a function attribute that applies to the function return type.</span></span> <span data-ttu-id="4fce6-143">O atributo pointer também pode aparecer com a **\[** palavra-chave [**\_ default do ponteiro**](pointer-default.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="4fce6-143">The pointer attribute can also appear with the **\[**[**pointer\_default**](pointer-default.md)**\]** keyword.</span></span>

<span data-ttu-id="4fce6-144">Um ponteiro de referência tem as seguintes características:</span><span class="sxs-lookup"><span data-stu-id="4fce6-144">A reference pointer has the following characteristics:</span></span>

-   <span data-ttu-id="4fce6-145">Sempre aponta para o armazenamento válido; Nunca tem o valor **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4fce6-145">Always points to valid storage; never has the value **NULL**.</span></span> <span data-ttu-id="4fce6-146">Um ponteiro de referência sempre pode ser desreferenciado.</span><span class="sxs-lookup"><span data-stu-id="4fce6-146">A reference pointer can always be dereferenced.</span></span>
-   <span data-ttu-id="4fce6-147">Nunca muda durante uma chamada.</span><span class="sxs-lookup"><span data-stu-id="4fce6-147">Never changes during a call.</span></span> <span data-ttu-id="4fce6-148">Um ponteiro de referência sempre aponta para o mesmo armazenamento no cliente antes e depois da chamada.</span><span class="sxs-lookup"><span data-stu-id="4fce6-148">A reference pointer always points to the same storage on the client before and after the call.</span></span>
-   <span data-ttu-id="4fce6-149">Não aloca uma nova memória no cliente.</span><span class="sxs-lookup"><span data-stu-id="4fce6-149">Does not allocate new memory on the client.</span></span> <span data-ttu-id="4fce6-150">Os dados retornados do servidor são gravados no armazenamento existente especificado pelo valor do ponteiro de referência antes da chamada.</span><span class="sxs-lookup"><span data-stu-id="4fce6-150">Data returned from the server is written into existing storage specified by the value of the reference pointer before the call.</span></span>
-   <span data-ttu-id="4fce6-151">Não causa alias.</span><span class="sxs-lookup"><span data-stu-id="4fce6-151">Does not cause aliasing.</span></span> <span data-ttu-id="4fce6-152">O armazenamento apontado por um ponteiro de referência não pode ser acessado de nenhum outro nome na função.</span><span class="sxs-lookup"><span data-stu-id="4fce6-152">Storage pointed to by a reference pointer cannot be reached from any other name in the function.</span></span>

<span data-ttu-id="4fce6-153">Um ponteiro de referência não pode ser usado como o tipo de um ponteiro retornado por uma função.</span><span class="sxs-lookup"><span data-stu-id="4fce6-153">A reference pointer cannot be used as the type of a pointer returned by a function.</span></span>

<span data-ttu-id="4fce6-154">Se nenhum atributo for especificado para um parâmetro de ponteiro de nível superior, ele será tratado como um ponteiro de referência.</span><span class="sxs-lookup"><span data-stu-id="4fce6-154">If no attribute is specified for a top-level pointer parameter, it is treated as a reference pointer.</span></span>

## <a name="examples"></a><span data-ttu-id="4fce6-155">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4fce6-155">Examples</span></span>

``` syntax
[unique] char * GetFirstName( 
    [in, ref] char * pszFullName);
```

## <a name="see-also"></a><span data-ttu-id="4fce6-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="4fce6-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fce6-157">**Storage**</span><span class="sxs-lookup"><span data-stu-id="4fce6-157">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="4fce6-158">Matrizes e ponteiros</span><span class="sxs-lookup"><span data-stu-id="4fce6-158">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="4fce6-159">Atributos de matriz e de Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="4fce6-159">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="4fce6-160">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="4fce6-160">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="4fce6-161">**retorno de chamada**</span><span class="sxs-lookup"><span data-stu-id="4fce6-161">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="4fce6-162">**const**</span><span class="sxs-lookup"><span data-stu-id="4fce6-162">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="4fce6-163">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="4fce6-163">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="4fce6-164">**enumera**</span><span class="sxs-lookup"><span data-stu-id="4fce6-164">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="4fce6-165">**primeiro \_ é**</span><span class="sxs-lookup"><span data-stu-id="4fce6-165">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="4fce6-166">**processamento**</span><span class="sxs-lookup"><span data-stu-id="4fce6-166">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="4fce6-167">**ignorar**</span><span class="sxs-lookup"><span data-stu-id="4fce6-167">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="4fce6-168">**último \_ é**</span><span class="sxs-lookup"><span data-stu-id="4fce6-168">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="4fce6-169">**comprimento \_ é**</span><span class="sxs-lookup"><span data-stu-id="4fce6-169">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="4fce6-170">**local**</span><span class="sxs-lookup"><span data-stu-id="4fce6-170">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="4fce6-171">**máximo \_ é**</span><span class="sxs-lookup"><span data-stu-id="4fce6-171">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="4fce6-172">**fora**</span><span class="sxs-lookup"><span data-stu-id="4fce6-172">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="4fce6-173">**ptr**</span><span class="sxs-lookup"><span data-stu-id="4fce6-173">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="4fce6-174">**o tamanho \_ é**</span><span class="sxs-lookup"><span data-stu-id="4fce6-174">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="4fce6-175">**string**</span><span class="sxs-lookup"><span data-stu-id="4fce6-175">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="4fce6-176">**struct**</span><span class="sxs-lookup"><span data-stu-id="4fce6-176">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="4fce6-177">**tipo de comutador \_**</span><span class="sxs-lookup"><span data-stu-id="4fce6-177">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="4fce6-178">**transmitir \_ como**</span><span class="sxs-lookup"><span data-stu-id="4fce6-178">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="4fce6-179">**unida**</span><span class="sxs-lookup"><span data-stu-id="4fce6-179">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="4fce6-180">**diferente**</span><span class="sxs-lookup"><span data-stu-id="4fce6-180">**unique**</span></span>](unique.md)
</dt> </dl>

 

 
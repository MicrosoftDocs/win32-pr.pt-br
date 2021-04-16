---
title: atributo exclusivo
description: O atributo \ Unique \ especifica um ponteiro exclusivo.
ms.assetid: 0d668148-e65a-478f-9e47-2528d3caa84c
keywords:
- MIDL de atributo exclusivo
topic_type:
- apiref
api_name:
- unique
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95b839a2abdd546842ef0d33d45a31428af840f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105758319"
---
# <a name="unique-attribute"></a><span data-ttu-id="8e26c-104">atributo exclusivo</span><span class="sxs-lookup"><span data-stu-id="8e26c-104">unique attribute</span></span>

<span data-ttu-id="8e26c-105">O atributo **\[ exclusivo \]** especifica um ponteiro exclusivo.</span><span class="sxs-lookup"><span data-stu-id="8e26c-105">The **\[unique\]** attribute specifies a unique pointer.</span></span>

``` syntax
pointer_default(unique)

typedef [ unique [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef struct-or-union-declarator 
{
    [ unique [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...}

[ unique [[ , function-attribute-list ]] ] type-specifier ptr-decl function-name(
    [[ [ parameter-attribute-list ] ]] type-specifier [[declarator]]
    , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ unique [[ , parameter-attribute-list ]] ] type-specifier [[declarator]]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="8e26c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e26c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e26c-107">*lista de atributos de tipo*</span><span class="sxs-lookup"><span data-stu-id="8e26c-107">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="8e26c-108">Especifica um ou mais atributos que se aplicam ao tipo.</span><span class="sxs-lookup"><span data-stu-id="8e26c-108">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="8e26c-109">Atributos de tipo válidos incluem **\[** [**identificador**](handle.md) **\]** , **\[** [**\_ tipo de comutador**](switch-type.md) **\]** , **\[** [**transmissão \_ como**](transmit-as.md) **\]** ; o atributo de ponteiro **\[** [**ref**](ref.md) **\]** , **\[ Unique \]** ou **\[** [**PTR**](ptr.md) **\]** ; e o identificador de contexto de atributos de uso **\[** [**\_**](context-handle.md) **\]** , **\[** [**cadeia de caracteres**](string.md) **\]** e **\[** [**ignorar**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="8e26c-109">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[unique\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="8e26c-110">Separe vários atributos com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="8e26c-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="8e26c-111">*especificador de tipo*</span><span class="sxs-lookup"><span data-stu-id="8e26c-111">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="8e26c-112">Especifica um [tipo base](midl-base-types.md), [**struct**](struct.md), [**Union**](union.md), tipo de [**Enumeração**](enum.md) ou identificador de tipo.</span><span class="sxs-lookup"><span data-stu-id="8e26c-112">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="8e26c-113">Uma especificação de armazenamento opcional pode preceder o *especificador de tipo*.</span><span class="sxs-lookup"><span data-stu-id="8e26c-113">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="8e26c-114">*Declarador e Declarador-lista*</span><span class="sxs-lookup"><span data-stu-id="8e26c-114">*declarator and declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="8e26c-115">Especifica os declaradores padrão C, como identificadores, declaradores de ponteiro e declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="8e26c-115">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="8e26c-116">Para obter mais informações, consulte [matriz e Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrizes**](arrays-1.md)e [matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="8e26c-116">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md)., and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="8e26c-117">A *lista de declaradores* consiste em um ou mais declaradores separados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="8e26c-117">The *declarator-list* consists of one or more declarators separated by commas.</span></span> <span data-ttu-id="8e26c-118">O identificador de nome de parâmetro no Declarador de função é opcional.</span><span class="sxs-lookup"><span data-stu-id="8e26c-118">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="8e26c-119">*struct-ou-Union-declaradora*</span><span class="sxs-lookup"><span data-stu-id="8e26c-119">*struct-or-union-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="8e26c-120">Especifica um Declarador [**de MIDL ou**](struct.md) [**Union**](union.md) .</span><span class="sxs-lookup"><span data-stu-id="8e26c-120">Specifies a MIDL [**struct**](struct.md) or [**union**](union.md) declarator.</span></span>

</dd> <dt>

<span data-ttu-id="8e26c-121">*lista de atributos de campo*</span><span class="sxs-lookup"><span data-stu-id="8e26c-121">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="8e26c-122">Especifica zero ou mais atributos de campo que se aplicam ao membro da estrutura, ao membro da União ou ao parâmetro de função.</span><span class="sxs-lookup"><span data-stu-id="8e26c-122">Specifies zero or more field attributes that apply to the structure member, union member, or function parameter.</span></span> <span data-ttu-id="8e26c-123">Os atributos de campo válidos incluem **\[** [**primeiro \_**](first-is.md) **\]** , **\[** o [**último \_**](last-is.md)é **\]** , **\[** [**o comprimento \_ é**](length-is.md) **\]** , **\[** [**máx \_**](max-is.md) **\]** ., **\[** o [**tamanho \_ é**](size-is.md) **\]** ; a cadeia de **\[ caracteres \]** de atributos de uso, **\[ ignorar \]** e o **\[ \_ identificador \] de contexto**; o atributo de ponteiro **\[ ref \]**, **\[ Unique \]** ou **\[ PTR \]**; e o **\[ \_ tipo \] de opção** de atributo Union.</span><span class="sxs-lookup"><span data-stu-id="8e26c-123">Valid field attributes include **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the union attribute **\[switch\_type\]**.</span></span> <span data-ttu-id="8e26c-124">Separe vários atributos de campo com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="8e26c-124">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="8e26c-125">*lista de atributos de função*</span><span class="sxs-lookup"><span data-stu-id="8e26c-125">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="8e26c-126">Especifica zero ou mais atributos que se aplicam à função.</span><span class="sxs-lookup"><span data-stu-id="8e26c-126">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="8e26c-127">Os atributos de função válidos são **\[** [**retorno de chamada**](callback.md) **\]** , **\[** [**local**](local.md) **\]** ; o atributo de ponteiro **\[ ref \]**, **\[ \] Unique** ou **\[ PTR \]**; e a cadeia de **\[ caracteres \]** de atributos de uso, **\[ ignorar \]** e **\[ \_ \] identificador de contexto**.</span><span class="sxs-lookup"><span data-stu-id="8e26c-127">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**.</span></span>

</dd> <dt>

<span data-ttu-id="8e26c-128">*declaração de PTR*</span><span class="sxs-lookup"><span data-stu-id="8e26c-128">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="8e26c-129">Especifica pelo menos um Declarador de ponteiro ao qual o atributo **\[ exclusivo \]** se aplica.</span><span class="sxs-lookup"><span data-stu-id="8e26c-129">Specifies at least one pointer declarator to which the **\[unique\]** attribute applies.</span></span> <span data-ttu-id="8e26c-130">Um Declarador de ponteiro é o mesmo que o Declarador de ponteiro usado em C; Ele é construído a partir do \* designador, modificadores, como **distante** e o qualificador [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="8e26c-130">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e26c-131">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="8e26c-131">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="8e26c-132">Especifica o nome do procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="8e26c-132">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="8e26c-133">*lista de atributos de parâmetro*</span><span class="sxs-lookup"><span data-stu-id="8e26c-133">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="8e26c-134">Consiste em zero ou mais atributos apropriados para o tipo de parâmetro especificado.</span><span class="sxs-lookup"><span data-stu-id="8e26c-134">Consists of zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="8e26c-135">Os atributos de parâmetro podem levar os atributos direcionais para **\[ \] dentro** e para **\[ fora \]**; os atributos do campo **\[ primeiro \_ são \]**, **\[ Last \_ is \]**, **\[ length \_ is \]**, **\[ Max \_ is \]**, **\[ Size \_ is \]** e **\[ switch \_ Type \]**; o atributo pointer **\[ ref \]**, **Unique** ou [**PTR**](ptr.md); e o **\[ \_ identificador \] de contexto** de atributos de uso e a cadeia de **\[ caracteres \]**.</span><span class="sxs-lookup"><span data-stu-id="8e26c-135">Parameter attributes can take the directional attributes **\[in\]** and **\[out\]**; the field attributes **\[first\_is\]**, **\[last\_is\]**, **\[length\_is\]**, **\[max\_is\]**, **\[size\_is\]**, and **\[switch\_type\]**; the pointer attribute **\[ref\]**, **unique**, or [**ptr**](ptr.md); and the usage attributes **\[context\_handle\]** and **\[string\]**.</span></span> <span data-ttu-id="8e26c-136">O atributo de uso **\[ ignore \]** não pode ser usado como um atributo de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="8e26c-136">The usage attribute **\[ignore\]** cannot be used as a parameter attribute.</span></span> <span data-ttu-id="8e26c-137">Separe vários atributos com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="8e26c-137">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8e26c-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e26c-138">Remarks</span></span>

<span data-ttu-id="8e26c-139">Os atributos de ponteiro podem ser aplicados como um atributo de tipo; como um atributo de campo que se aplica a um membro de estrutura, um membro de União ou um parâmetro; ou como um atributo de função que se aplica ao tipo de retorno da função.</span><span class="sxs-lookup"><span data-stu-id="8e26c-139">Pointer attributes can be applied as a type attribute; as a field attribute that applies to a structure member, union member, or parameter; or as a function attribute that applies to the function return type.</span></span> <span data-ttu-id="8e26c-140">O atributo pointer também pode aparecer com a **\[** palavra-chave [**\_ default do ponteiro**](pointer-default.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="8e26c-140">The pointer attribute can also appear with the **\[**[**pointer\_default**](pointer-default.md)**\]** keyword.</span></span>

<span data-ttu-id="8e26c-141">Um ponteiro exclusivo tem as seguintes características:</span><span class="sxs-lookup"><span data-stu-id="8e26c-141">A unique pointer has the following characteristics:</span></span>

-   <span data-ttu-id="8e26c-142">Pode ter o valor **NULL**.</span><span class="sxs-lookup"><span data-stu-id="8e26c-142">Can have the value **NULL**.</span></span>
-   <span data-ttu-id="8e26c-143">Pode ser alterado durante uma chamada de **NULL** para não **NULL**, de não **NULL** para **NULL** ou de um valor não **nulo** para outro.</span><span class="sxs-lookup"><span data-stu-id="8e26c-143">Can change during a call from **NULL** to non-**NULL**, from non-**NULL** to **NULL**, or from one non-**NULL** value to another.</span></span>
-   <span data-ttu-id="8e26c-144">Pode alocar nova memória no cliente.</span><span class="sxs-lookup"><span data-stu-id="8e26c-144">Can allocate new memory on the client.</span></span> <span data-ttu-id="8e26c-145">Quando o ponteiro exclusivo muda de **nulo** para não **nulo**, os dados retornados do servidor são gravados no novo armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8e26c-145">When the unique pointer changes from **NULL** to non-**NULL**, data returned from the server is written into new storage.</span></span>
-   <span data-ttu-id="8e26c-146">Pode usar a memória existente no cliente sem alocar nova memória.</span><span class="sxs-lookup"><span data-stu-id="8e26c-146">Can use existing memory on the client without allocating new memory.</span></span> <span data-ttu-id="8e26c-147">Quando um ponteiro exclusivo é alterado durante uma chamada de um valor não **nulo** para outro, o ponteiro é considerado para apontar para um objeto de dados do mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="8e26c-147">When a unique pointer changes during a call from one non-**NULL** value to another, the pointer is assumed to point to a data object of the same type.</span></span> <span data-ttu-id="8e26c-148">Os dados retornados do servidor são gravados no armazenamento existente especificado pelo valor do ponteiro exclusivo antes da chamada.</span><span class="sxs-lookup"><span data-stu-id="8e26c-148">Data returned from the server is written into existing storage specified by the value of the unique pointer before the call.</span></span>
-   <span data-ttu-id="8e26c-149">Pode órfão na memória do cliente.</span><span class="sxs-lookup"><span data-stu-id="8e26c-149">Can orphan memory on the client.</span></span> <span data-ttu-id="8e26c-150">A memória referenciada por um ponteiro exclusivo não **nulo** pode nunca ser liberada se o ponteiro exclusivo mudar para **NULL** durante uma chamada e o cliente não tiver outro meio de desreferenciar o armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8e26c-150">Memory referenced by a non-**NULL** unique pointer may never be freed if the unique pointer changes to **NULL** during a call and the client does not have another means of dereferencing the storage.</span></span>
-   <span data-ttu-id="8e26c-151">Não causa alias.</span><span class="sxs-lookup"><span data-stu-id="8e26c-151">Does not cause aliasing.</span></span> <span data-ttu-id="8e26c-152">Como o armazenamento apontado por um ponteiro de referência, o armazenamento apontado por um ponteiro exclusivo não pode ser acessado de nenhum outro nome na função.</span><span class="sxs-lookup"><span data-stu-id="8e26c-152">Like storage pointed to by a reference pointer, storage pointed to by a unique pointer cannot be reached from any other name in the function.</span></span>

<span data-ttu-id="8e26c-153">Os stubs chamam as funções de gerenciamento de memória fornecidas pelo usuário para [**\_ \_ alocar**](/windows/desktop/Rpc/the-midl-user-allocate-function) o usuário MIDL e o [**usuário de MIDL \_ \_ livres**](/windows/desktop/Rpc/the-midl-user-free-function) para alocar e desalocar a memória necessária para ponteiros exclusivos e seus referents.</span><span class="sxs-lookup"><span data-stu-id="8e26c-153">The stubs call the user-supplied memory-management functions [**midl\_user\_allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function) and [**midl\_user\_free**](/windows/desktop/Rpc/the-midl-user-free-function) to allocate and deallocate memory required for unique pointers and their referents.</span></span>

<span data-ttu-id="8e26c-154">As seguintes restrições se aplicam a ponteiros exclusivos:</span><span class="sxs-lookup"><span data-stu-id="8e26c-154">The following restrictions apply to unique pointers:</span></span>

-   <span data-ttu-id="8e26c-155">O atributo **\[ exclusivo \]** não pode ser aplicado a parâmetros de identificador de associação ( [**identificador \_ t**](handle-t.md)) e a parâmetros de identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="8e26c-155">The **\[unique\]** attribute cannot be applied to binding-handle parameters ( [**handle\_t**](handle-t.md)) and context-handle parameters.</span></span>
-   <span data-ttu-id="8e26c-156">O atributo **\[ exclusivo \]** não pode ser aplicado a parâmetros de ponteiro de **\[** [](out-idl.md) **\]** nível superior somente de saída (parâmetros que têm apenas o atributo direcional **\[ \] out** ).</span><span class="sxs-lookup"><span data-stu-id="8e26c-156">The **\[unique\]** attribute cannot be applied to **\[**[**out**](out-idl.md)**\]**-only top-level pointer parameters (parameters that have only the **\[out\]** directional attribute).</span></span>
-   <span data-ttu-id="8e26c-157">Por padrão, os ponteiros de nível superior nas listas de parâmetros são **\[** [](ref.md) **\]** ponteiros de referência.</span><span class="sxs-lookup"><span data-stu-id="8e26c-157">By default, top-level pointers in parameter lists are **\[**[**ref**](ref.md)**\]** pointers.</span></span> <span data-ttu-id="8e26c-158">Isso é verdadeiro mesmo que a interface especifique **o \_ padrão de ponteiro (exclusivo)**.</span><span class="sxs-lookup"><span data-stu-id="8e26c-158">This is true even if the interface specifies **pointer\_default(unique)**.</span></span> <span data-ttu-id="8e26c-159">Os parâmetros de nível superior nas listas de parâmetros devem ser especificados com o atributo **\[ exclusivo \]** como um ponteiro exclusivo.</span><span class="sxs-lookup"><span data-stu-id="8e26c-159">Top-level parameters in parameter lists must be specified with the **\[unique\]** attribute to be a unique pointer.</span></span>
-   <span data-ttu-id="8e26c-160">Ponteiros exclusivos não podem ser usados para descrever o tamanho de um ARM de matriz ou de União porque ponteiros exclusivos podem ter o valor **NULL**.</span><span class="sxs-lookup"><span data-stu-id="8e26c-160">Unique pointers cannot be used to describe the size of an array or union arm because unique pointers can have the value **NULL**.</span></span> <span data-ttu-id="8e26c-161">Essa restrição impede o erro que resulta se um valor **nulo** é usado como o tamanho da matriz ou o tamanho de União de braço.</span><span class="sxs-lookup"><span data-stu-id="8e26c-161">This restriction prevents the error that results if a **NULL** value is used as the array size or the union-arm size.</span></span>

## <a name="examples"></a><span data-ttu-id="8e26c-162">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8e26c-162">Examples</span></span>

``` syntax
pointer_default(unique) 
 
typedef [unique, string] unsigned char * MY_STRING_TYPE; 
 
[unique] char * MyFunction([in, out, unique] long * plNumber);
```

## <a name="see-also"></a><span data-ttu-id="8e26c-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e26c-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e26c-164">**Storage**</span><span class="sxs-lookup"><span data-stu-id="8e26c-164">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="8e26c-165">Matrizes e ponteiros</span><span class="sxs-lookup"><span data-stu-id="8e26c-165">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="8e26c-166">Atributos de matriz e de Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="8e26c-166">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="8e26c-167">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="8e26c-167">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="8e26c-168">**retorno de chamada**</span><span class="sxs-lookup"><span data-stu-id="8e26c-168">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="8e26c-169">**const**</span><span class="sxs-lookup"><span data-stu-id="8e26c-169">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="8e26c-170">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="8e26c-170">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="8e26c-171">**enumera**</span><span class="sxs-lookup"><span data-stu-id="8e26c-171">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="8e26c-172">**primeiro \_ é**</span><span class="sxs-lookup"><span data-stu-id="8e26c-172">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="8e26c-173">**processamento**</span><span class="sxs-lookup"><span data-stu-id="8e26c-173">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="8e26c-174">**lidar com \_ t**</span><span class="sxs-lookup"><span data-stu-id="8e26c-174">**handle\_t**</span></span>](handle-t.md)
</dt> <dt>

[<span data-ttu-id="8e26c-175">**ignorar**</span><span class="sxs-lookup"><span data-stu-id="8e26c-175">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="8e26c-176">**último \_ é**</span><span class="sxs-lookup"><span data-stu-id="8e26c-176">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="8e26c-177">**comprimento \_ é**</span><span class="sxs-lookup"><span data-stu-id="8e26c-177">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="8e26c-178">**local**</span><span class="sxs-lookup"><span data-stu-id="8e26c-178">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="8e26c-179">**máximo \_ é**</span><span class="sxs-lookup"><span data-stu-id="8e26c-179">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="8e26c-180">\_alocar usuário de MIDL \_</span><span class="sxs-lookup"><span data-stu-id="8e26c-180">midl\_user\_allocate</span></span>](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[<span data-ttu-id="8e26c-181">usuário de MIDL \_ \_ gratuito</span><span class="sxs-lookup"><span data-stu-id="8e26c-181">midl\_user\_free</span></span>](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[<span data-ttu-id="8e26c-182">**fora**</span><span class="sxs-lookup"><span data-stu-id="8e26c-182">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="8e26c-183">**padrão de ponteiro \_**</span><span class="sxs-lookup"><span data-stu-id="8e26c-183">**pointer\_default**</span></span>](pointer-default.md)
</dt> <dt>

[<span data-ttu-id="8e26c-184">**ptr**</span><span class="sxs-lookup"><span data-stu-id="8e26c-184">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="8e26c-185">**ref**</span><span class="sxs-lookup"><span data-stu-id="8e26c-185">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="8e26c-186">**o tamanho \_ é**</span><span class="sxs-lookup"><span data-stu-id="8e26c-186">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="8e26c-187">**string**</span><span class="sxs-lookup"><span data-stu-id="8e26c-187">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="8e26c-188">**struct**</span><span class="sxs-lookup"><span data-stu-id="8e26c-188">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="8e26c-189">**tipo de comutador \_**</span><span class="sxs-lookup"><span data-stu-id="8e26c-189">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="8e26c-190">**transmitir \_ como**</span><span class="sxs-lookup"><span data-stu-id="8e26c-190">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="8e26c-191">**unida**</span><span class="sxs-lookup"><span data-stu-id="8e26c-191">**union**</span></span>](union.md)
</dt> </dl>

 

 
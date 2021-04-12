---
title: atributo ptr
description: O atributo \ PTR \ designa um ponteiro como um ponteiro completo.
ms.assetid: a1233a25-b651-4a01-8abf-a64dc9ee168e
keywords:
- MIDL do atributo PTR
topic_type:
- apiref
api_name:
- ptr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2d8b2ee2e3ea4daccd1c4fa37ff1c1f1899dd3c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293948"
---
# <a name="ptr-attribute"></a><span data-ttu-id="9e240-104">atributo ptr</span><span class="sxs-lookup"><span data-stu-id="9e240-104">ptr attribute</span></span>

<span data-ttu-id="9e240-105">O atributo **\[ PTR \]** designa um ponteiro como um ponteiro completo.</span><span class="sxs-lookup"><span data-stu-id="9e240-105">The **\[ptr\]** attribute designates a pointer as a full pointer.</span></span>

``` syntax
pointer_default(ptr)

typedef [ ptr [ , type-attribute-list ] ] type-specifier declarator-list; 

typedef [ struct | union ]
{
    [ ptr [ , field-attribute-list ] ] type-specifier declarator-list;
    ...
}

[ ptr [ , function-attribute-list ] ] type-specifier ptr-decl function-name(
    [ [ parameter-attribute-list ] ] type-specifier [standard-declarator]
    , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ ptr [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="9e240-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9e240-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e240-107">*lista de atributos de tipo*</span><span class="sxs-lookup"><span data-stu-id="9e240-107">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="9e240-108">Especifica um ou mais atributos que se aplicam ao tipo.</span><span class="sxs-lookup"><span data-stu-id="9e240-108">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="9e240-109">Atributos de tipo válidos incluem **\[** [**identificador**](handle.md) **\]** , **\[** [**\_ tipo de comutador**](switch-type.md) **\]** , **\[** [**transmissão \_ como**](transmit-as.md) **\]** ; o atributo de ponteiro **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md)ou **\[ PTR \]**; e o identificador de contexto de atributos de uso **\[** [**\_**](context-handle.md) **\]** , **\[** [**cadeia de caracteres**](string.md) **\]** e **\[** [**ignorar**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="9e240-109">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md), or **\[ptr\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="9e240-110">Separe vários atributos com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="9e240-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="9e240-111">*especificador de tipo*</span><span class="sxs-lookup"><span data-stu-id="9e240-111">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="9e240-112">Especifica um tipo de [base](midl-base-types.md), [**struct**](struct.md), [**Union**](union.md)ou tipo de [**Enumeração**](enum.md) ou identificador de tipo.</span><span class="sxs-lookup"><span data-stu-id="9e240-112">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), or [**enum**](enum.md) type or type identifier.</span></span> <span data-ttu-id="9e240-113">Uma especificação de armazenamento opcional pode preceder o *especificador de tipo*.</span><span class="sxs-lookup"><span data-stu-id="9e240-113">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="9e240-114">*padrão-Declarador*</span><span class="sxs-lookup"><span data-stu-id="9e240-114">*standard-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="9e240-115">Especifica um Declarador C padrão, como um identificador, um Declarador de ponteiro ou um Declarador de matriz.</span><span class="sxs-lookup"><span data-stu-id="9e240-115">Specifies a standard C declarator, such as an identifier, a pointer declarator, or an array declarator.</span></span> <span data-ttu-id="9e240-116">Para obter mais informações, consulte [matriz e Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrizes**](arrays-1.md)e [matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="9e240-116">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span>

</dd> <dt>

<span data-ttu-id="9e240-117">*Declarador-lista*</span><span class="sxs-lookup"><span data-stu-id="9e240-117">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="9e240-118">Especifica os declaradores padrão C, como identificadores, declaradores de ponteiro e declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="9e240-118">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="9e240-119">Para obter mais informações, consulte [matriz e Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrizes**](arrays-1.md)e [matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="9e240-119">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="9e240-120">A *lista de declaradores* consiste em um ou mais declaradores separados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="9e240-120">The *declarator-list* consists of one or more declarators separated by commas.</span></span> <span data-ttu-id="9e240-121">O identificador de nome de parâmetro no Declarador de função é opcional.</span><span class="sxs-lookup"><span data-stu-id="9e240-121">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="9e240-122">*lista de atributos de campo*</span><span class="sxs-lookup"><span data-stu-id="9e240-122">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="9e240-123">Especifica zero ou mais atributos de campo que se aplicam ao parâmetro de função ou membro da estrutura ou União.</span><span class="sxs-lookup"><span data-stu-id="9e240-123">Specifies zero or more field attributes that apply to the structure or union member or function parameter.</span></span> <span data-ttu-id="9e240-124">Os atributos de campo válidos incluem **\[** [**primeiro \_**](first-is.md) **\]** , **\[** o [**último \_**](last-is.md)é **\]** , **\[** o [**comprimento \_ é**](length-is.md) **\]** , **\[** [**\_ máx**](max-is.md) **\]** ., **\[** o [**tamanho \_ é**](size-is.md) **\]** ; a cadeia de caracteres de atributos de uso **\[** [](string.md) **\]** , **\[** [**ignorar**](ignore.md) **\]** e **\[** o [**\_ identificador de contexto**](context-handle.md) **\]** ; o atributo de ponteiro **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** ou **\[ PTR \]**; e o **\[** [**\_ tipo de opção**](switch-type.md)de atributo Union **\]** .</span><span class="sxs-lookup"><span data-stu-id="9e240-124">Valid field attributes include **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[ptr\]**; and the union attribute **\[**[**switch\_type**](switch-type.md)**\]**.</span></span> <span data-ttu-id="9e240-125">Separe vários atributos de campo com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="9e240-125">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="9e240-126">*lista de atributos de função*</span><span class="sxs-lookup"><span data-stu-id="9e240-126">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="9e240-127">Especifica zero ou mais atributos que se aplicam à função.</span><span class="sxs-lookup"><span data-stu-id="9e240-127">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="9e240-128">Os atributos de função válidos são **\[** [**retorno de chamada**](callback.md) **\]** , **\[** [**local**](local.md) **\]** ; o atributo de ponteiro **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** ou **\[ \] PTR**; e a cadeia de caracteres de atributos de uso **\[** [](string.md) **\]** , **\[** [**ignorar**](ignore.md) **\]** e **\[** [**\_ identificador de contexto**](context-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="9e240-128">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[ptr\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="9e240-129">*declaração de PTR*</span><span class="sxs-lookup"><span data-stu-id="9e240-129">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="9e240-130">Especifica pelo menos um Declarador de ponteiro ao qual o atributo **\[ PTR \]** se aplica.</span><span class="sxs-lookup"><span data-stu-id="9e240-130">Specifies at least one pointer declarator to which the **\[ptr\]** attribute applies.</span></span> <span data-ttu-id="9e240-131">Um Declarador de ponteiro é o mesmo que o Declarador de ponteiro usado em C; Ele é construído a partir do \* designador, modificadores, como **distante** e o qualificador [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="9e240-131">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e240-132">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="9e240-132">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="9e240-133">Especifica o nome do procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="9e240-133">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="9e240-134">*lista de atributos de parâmetro*</span><span class="sxs-lookup"><span data-stu-id="9e240-134">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="9e240-135">Consiste em zero ou mais atributos apropriados para o tipo de parâmetro especificado.</span><span class="sxs-lookup"><span data-stu-id="9e240-135">Consists of zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="9e240-136">Os atributos de parâmetro podem levar os atributos direcionais para [**dentro**](in.md) e para [**fora**](out-idl.md); os atributos de [**campo \_ First são**](first-is.md), [**Last \_ is**](last-is.md), [**length \_ is**](length-is.md), [**Max \_ is**](max-is.md), [**Size \_ is**](size-is.md)e [**switch \_ Type**](switch-type.md); o atributo pointer [**ref**](ref.md), [**Unique**](unique.md)ou **\[ PTR \]**; e o [**\_ identificador de contexto**](context-handle.md) e a cadeia de [**caracteres**](string.md)de uso.</span><span class="sxs-lookup"><span data-stu-id="9e240-136">Parameter attributes can take the directional attributes [**in**](in.md) and [**out**](out-idl.md); the field attributes [**first\_is**](first-is.md), [**last\_is**](last-is.md), [**length\_is**](length-is.md), [**max\_is**](max-is.md), [**size\_is**](size-is.md), and [**switch\_type**](switch-type.md); the pointer attribute [**ref**](ref.md), [**unique**](unique.md), or **\[ptr\]**; and the usage attributes [**context\_handle**](context-handle.md) and [**string**](string.md).</span></span> <span data-ttu-id="9e240-137">O atributo de uso [**ignore**](ignore.md) não pode ser usado como um atributo de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="9e240-137">The usage attribute [**ignore**](ignore.md) cannot be used as a parameter attribute.</span></span> <span data-ttu-id="9e240-138">Separe vários atributos com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="9e240-138">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9e240-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e240-139">Remarks</span></span>

<span data-ttu-id="9e240-140">O ponteiro completo designado pelo atributo **\[ PTR \]** se aproxima da funcionalidade completa do ponteiro em linguagem C.</span><span class="sxs-lookup"><span data-stu-id="9e240-140">The full pointer designated by the **\[ptr\]** attribute approaches the full functionality of the C-language pointer.</span></span> <span data-ttu-id="9e240-141">O ponteiro completo pode ter o valor **NULL** e pode ser alterado durante a chamada de **NULL** para não **NULL**.</span><span class="sxs-lookup"><span data-stu-id="9e240-141">The full pointer can have the value **NULL** and can change during the call from **NULL** to non-**NULL**.</span></span> <span data-ttu-id="9e240-142">O armazenamento apontado por ponteiros completos pode ser alcançado por outros nomes no aplicativo com suporte a aliases e ciclos.</span><span class="sxs-lookup"><span data-stu-id="9e240-142">Storage pointed to by full pointers can be reached by other names in the application supporting aliasing and cycles.</span></span> <span data-ttu-id="9e240-143">Essa funcionalidade requer mais sobrecarga durante uma chamada de procedimento remoto para identificar os dados referenciados pelo ponteiro, determinar se o valor é **nulo** e descobrir se dois ponteiros apontam para os mesmos dados.</span><span class="sxs-lookup"><span data-stu-id="9e240-143">This functionality requires more overhead during a remote procedure call to identify the data referred to by the pointer, determine whether the value is **NULL**, and to discover if two pointers point to the same data.</span></span>

<span data-ttu-id="9e240-144">Use ponteiros completos para:</span><span class="sxs-lookup"><span data-stu-id="9e240-144">Use full pointers for:</span></span>

-   <span data-ttu-id="9e240-145">Valores de retorno remotos.</span><span class="sxs-lookup"><span data-stu-id="9e240-145">Remote return values.</span></span>
-   <span data-ttu-id="9e240-146">Ponteiros duplos, quando o tamanho de um parâmetro de saída não é conhecido.</span><span class="sxs-lookup"><span data-stu-id="9e240-146">Double pointers, when the size of an output parameter is not known.</span></span>
-   <span data-ttu-id="9e240-147">Ponteiros **nulos** .</span><span class="sxs-lookup"><span data-stu-id="9e240-147">**NULL** pointers.</span></span>

<span data-ttu-id="9e240-148">Ponteiros completos (e exclusivos) não podem ser usados para descrever o tamanho de uma matriz ou Union porque esses ponteiros podem ter o valor **NULL**.</span><span class="sxs-lookup"><span data-stu-id="9e240-148">Full (and unique) pointers cannot be used to describe the size of an array or union because these pointers can have the value **NULL**.</span></span> <span data-ttu-id="9e240-149">Essa restrição por MIDL impede um erro que pode ocorrer quando um valor **nulo** é usado como o tamanho.</span><span class="sxs-lookup"><span data-stu-id="9e240-149">This restriction by MIDL prevents an error that can result when a **NULL** value is used as the size.</span></span>

<span data-ttu-id="9e240-150">Referências e ponteiros exclusivos são considerados para não causar alias de dados.</span><span class="sxs-lookup"><span data-stu-id="9e240-150">Reference and unique pointers are assumed to cause no aliasing of data.</span></span> <span data-ttu-id="9e240-151">Um grafo direcionado obtido por meio de um ponteiro exclusivo ou de referência e seguir somente ponteiros exclusivos ou de referência não contém nenhuma revergência nem ciclos.</span><span class="sxs-lookup"><span data-stu-id="9e240-151">A directed graph obtained by starting from a unique or reference pointer and following only unique or reference pointers contains neither reconvergence nor cycles.</span></span>

<span data-ttu-id="9e240-152">Para evitar o alias, todos os valores de ponteiro devem ser obtidos de um ponteiro de entrada da mesma classe de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="9e240-152">To avoid aliasing, all pointer values should be obtained from an input pointer of the same class of pointer.</span></span> <span data-ttu-id="9e240-153">Se mais de um ponteiro apontar para o mesmo local de memória, todos esses ponteiros deverão ser ponteiros completos.</span><span class="sxs-lookup"><span data-stu-id="9e240-153">If more than one pointer points to the same memory location, all such pointers must be full pointers.</span></span>

<span data-ttu-id="9e240-154">Em alguns casos, ponteiros completos e exclusivos podem ser misturados.</span><span class="sxs-lookup"><span data-stu-id="9e240-154">In some cases, full and unique pointers can be mixed.</span></span> <span data-ttu-id="9e240-155">Um ponteiro completo pode ser atribuído ao valor de um ponteiro exclusivo, desde que a atribuição não viole as restrições de alteração do valor de um ponteiro exclusivo.</span><span class="sxs-lookup"><span data-stu-id="9e240-155">A full pointer can be assigned the value of a unique pointer, as long as the assignment does not violate the restrictions on changing the value of a unique pointer.</span></span> <span data-ttu-id="9e240-156">No entanto, quando você atribui um ponteiro exclusivo ao valor de um ponteiro completo, pode causar alias.</span><span class="sxs-lookup"><span data-stu-id="9e240-156">However, when you assign a unique pointer the value of a full pointer, you may cause aliasing.</span></span>

<span data-ttu-id="9e240-157">A combinação de ponteiros completos e exclusivos pode causar alias, conforme demonstrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="9e240-157">Mixing full and unique pointers can cause aliasing, as demonstrated in the following example:</span></span>

``` syntax
typedef struct 
{ 
    [ptr] short * pdata;          // full pointer  
} GRAPH_NODE_TYPE; 
 
typedef struct 
{ 
    [unique] graph_node * left;   // unique pointer  
    [unique] graph_node * right;  // unique pointer 
} TREE_NODE_TYPE; 
 
// application code: 
short a = 5; 
TREE_NODE_TYPE * t; 
GRAPH_NODE_TYPE g, h; 
 
g.pdata = h.pdata = &a; 
t->left = &g; 
t->right = &h; 
// t->left->pdata == t->right->pdata == &a
```

<span data-ttu-id="9e240-158">Embora "t->Left" e "t->Right" apontem para locais de memória exclusivos, "t->Left->pData" e "t->Right – >pData" têm alias.</span><span class="sxs-lookup"><span data-stu-id="9e240-158">Although "t->left" and "t->right" point to unique memory locations, "t->left->pdata" and "t->right->pdata" are aliased.</span></span> <span data-ttu-id="9e240-159">Por esse motivo, os algoritmos de suporte a alias devem seguir todos os ponteiros (incluindo ponteiros exclusivos e de referência) que podem eventualmente atingir um ponteiro completo.</span><span class="sxs-lookup"><span data-stu-id="9e240-159">For this reason, aliasing-support algorithms must follow all pointers (including unique and reference pointers) that may eventually reach a full pointer.</span></span>

## <a name="examples"></a><span data-ttu-id="9e240-160">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9e240-160">Examples</span></span>

``` syntax
pointer_default(ptr) 
 
typedef [ptr, string] unsigned char * MY_STRING_TYPE; 
 
[ptr] char * MyFunction([in, out, unique] long * plNumber);
```

## <a name="see-also"></a><span data-ttu-id="9e240-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e240-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e240-162">**Storage**</span><span class="sxs-lookup"><span data-stu-id="9e240-162">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="9e240-163">Matrizes e ponteiros</span><span class="sxs-lookup"><span data-stu-id="9e240-163">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="9e240-164">Atributos de matriz e de Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="9e240-164">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="9e240-165">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="9e240-165">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="9e240-166">**retorno de chamada**</span><span class="sxs-lookup"><span data-stu-id="9e240-166">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="9e240-167">**const**</span><span class="sxs-lookup"><span data-stu-id="9e240-167">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="9e240-168">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="9e240-168">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="9e240-169">**enumera**</span><span class="sxs-lookup"><span data-stu-id="9e240-169">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="9e240-170">**primeiro \_ é**</span><span class="sxs-lookup"><span data-stu-id="9e240-170">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="9e240-171">**processamento**</span><span class="sxs-lookup"><span data-stu-id="9e240-171">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="9e240-172">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="9e240-172">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="9e240-173">**ignorar**</span><span class="sxs-lookup"><span data-stu-id="9e240-173">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="9e240-174">**último \_ é**</span><span class="sxs-lookup"><span data-stu-id="9e240-174">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="9e240-175">**comprimento \_ é**</span><span class="sxs-lookup"><span data-stu-id="9e240-175">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="9e240-176">**local**</span><span class="sxs-lookup"><span data-stu-id="9e240-176">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="9e240-177">**máximo \_ é**</span><span class="sxs-lookup"><span data-stu-id="9e240-177">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="9e240-178">**padrão de ponteiro \_**</span><span class="sxs-lookup"><span data-stu-id="9e240-178">**pointer\_default**</span></span>](pointer-default.md)
</dt> <dt>

[<span data-ttu-id="9e240-179">**ref**</span><span class="sxs-lookup"><span data-stu-id="9e240-179">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="9e240-180">**o tamanho \_ é**</span><span class="sxs-lookup"><span data-stu-id="9e240-180">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="9e240-181">**string**</span><span class="sxs-lookup"><span data-stu-id="9e240-181">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="9e240-182">**struct**</span><span class="sxs-lookup"><span data-stu-id="9e240-182">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="9e240-183">**tipo de comutador \_**</span><span class="sxs-lookup"><span data-stu-id="9e240-183">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="9e240-184">**transmitir \_ como**</span><span class="sxs-lookup"><span data-stu-id="9e240-184">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="9e240-185">**unida**</span><span class="sxs-lookup"><span data-stu-id="9e240-185">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="9e240-186">**diferente**</span><span class="sxs-lookup"><span data-stu-id="9e240-186">**unique**</span></span>](unique.md)
</dt> </dl>

 

 
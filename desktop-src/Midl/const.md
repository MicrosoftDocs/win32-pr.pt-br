---
title: atributo const
description: A palavra-chave const modifica o tipo de uma declaração de tipo ou o tipo de um parâmetro de função, impedindo que o valor seja variado.
ms.assetid: 398fab76-93f3-4d5a-9223-1c57c612b2d7
keywords:
- MIDL do atributo const
topic_type:
- apiref
api_name:
- const
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2980f0f484c838e4f972bbf12fb72173edb3e7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640516"
---
# <a name="const-attribute"></a><span data-ttu-id="e133e-104">atributo const</span><span class="sxs-lookup"><span data-stu-id="e133e-104">const attribute</span></span>

<span data-ttu-id="e133e-105">A palavra-chave **const** modifica o tipo de uma declaração de tipo ou o tipo de um parâmetro de função, impedindo que o valor seja variado.</span><span class="sxs-lookup"><span data-stu-id="e133e-105">The **const** keyword modifies the type of a type declaration or the type of a function parameter, preventing the value from varying.</span></span>

``` syntax
const const-type identifier = const-expression ;

[ typedef [ , type-attribute-list ] ] const const-type declarator-list;

[ typedef [ , type-attribute-list ] ] pointer-type const declarator-list;

[ [ function-attr-list ] ] type-specifier [ ptr-decl ] function-name(
    [ [ parameter-attribute-list ] ] ) const; 

const-type [declarator], [ [ parameter-attribute-list ] ] pointer-type const [declarator], ...);
```

## <a name="parameters"></a><span data-ttu-id="e133e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e133e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e133e-107">*tipo const*</span><span class="sxs-lookup"><span data-stu-id="e133e-107">*const-type*</span></span> 
</dt> <dd>

<span data-ttu-id="e133e-108">Especifica um inteiro MIDL, caractere, Cadeia de caracteres ou tipo booliano válido.</span><span class="sxs-lookup"><span data-stu-id="e133e-108">Specifies a valid MIDL integer, character, string, or Boolean type.</span></span> <span data-ttu-id="e133e-109">Os tipos de MIDL válidos incluem [**pequeno**](small.md), [**curto**](short.md), [**longo**](long.md), [**Char**](char-idl.md), **charÂ \***, [**WCHAR \_ t**](wchar-t.md), **WCHAR \_ tâ \***, [**byte**](byte.md), **byteÂ \*** e [**voidÂ \***](void.md).</span><span class="sxs-lookup"><span data-stu-id="e133e-109">Valid MIDL types include [**small**](small.md), [**short**](short.md), [**long**](long.md), [**char**](char-idl.md), **charÂ \***, [**wchar\_t**](wchar-t.md), **wchar\_tÂ \***, [**byte**](byte.md), **byteÂ \***, and [**voidÂ \***](void.md).</span></span> <span data-ttu-id="e133e-110">O número inteiro e os tipos de caracteres podem ser [**assinados**](signed.md) ou [**não assinados**](unsigned.md).</span><span class="sxs-lookup"><span data-stu-id="e133e-110">The integer and character types can be [**signed**](signed.md) or [**unsigned**](unsigned.md).</span></span>

</dd> <dt>

<span data-ttu-id="e133e-111">*identifier*</span><span class="sxs-lookup"><span data-stu-id="e133e-111">*identifier*</span></span> 
</dt> <dd>

<span data-ttu-id="e133e-112">Especifica um identificador MIDL válido.</span><span class="sxs-lookup"><span data-stu-id="e133e-112">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="e133e-113">Os identificadores MIDL válidos consistem em até 31 caracteres alfanuméricos e/ou de sublinhado e devem começar com um caractere alfabético ou de sublinhado.</span><span class="sxs-lookup"><span data-stu-id="e133e-113">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> <dt>

<span data-ttu-id="e133e-114">*expressão const*</span><span class="sxs-lookup"><span data-stu-id="e133e-114">*const-expression*</span></span> 
</dt> <dd>

<span data-ttu-id="e133e-115">Especifica uma expressão, um identificador ou uma constante numérica ou de caractere apropriada para o tipo especificado: literais inteiros constantes ou expressões de inteiro constante para constantes de inteiro; Expressões booleanas que podem ser computadas na compilação para tipos [**boolianos**](boolean.md) ; constantes de caractere único para tipos de [**caracteres**](char-idl.md) ; e constantes de cadeia de caracteres para tipos de **\[** [**cadeia de caracteres**](string.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="e133e-115">Specifies an expression, identifier, or numeric or character constant appropriate for the specified type: constant integer literals or constant integer expressions for integer constants; Boolean expressions that can be computed at compilation for [**Boolean**](boolean.md) types; single-character constants for [**char**](char-idl.md) types; and string constants for **\[**[**string**](string.md)**\]** types.</span></span> <span data-ttu-id="e133e-116">O [**tipo \* voidÂ**](void.md) pode ser inicializado somente como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e133e-116">The [**voidÂ \***](void.md) type can be initialized only to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e133e-117">*lista de atributos de tipo*</span><span class="sxs-lookup"><span data-stu-id="e133e-117">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e133e-118">Especifica um ou mais atributos que se aplicam ao tipo.</span><span class="sxs-lookup"><span data-stu-id="e133e-118">Specifies one or more attributes that apply to the type.</span></span>

</dd> <dt>

<span data-ttu-id="e133e-119">*tipo de ponteiro*</span><span class="sxs-lookup"><span data-stu-id="e133e-119">*pointer-type*</span></span> 
</dt> <dd>

<span data-ttu-id="e133e-120">Especifica um tipo de ponteiro de MIDL válido.</span><span class="sxs-lookup"><span data-stu-id="e133e-120">Specifies a valid MIDL pointer type.</span></span>

</dd> <dt>

<span data-ttu-id="e133e-121">*Declarador e Declarador-lista*</span><span class="sxs-lookup"><span data-stu-id="e133e-121">*declarator and declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e133e-122">Especifica os declaradores padrão C, como identificadores, declaradores de ponteiro e declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="e133e-122">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="e133e-123">Para obter mais informações, consulte [matriz e Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrizes**](arrays-1.md)e [matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="e133e-123">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="e133e-124">A *lista de declaradores* consiste em um ou mais declaradores, separados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="e133e-124">The *declarator-list* consists of one or more declarators, separated by commas.</span></span> <span data-ttu-id="e133e-125">O identificador de nome de parâmetro no Declarador de função é opcional.</span><span class="sxs-lookup"><span data-stu-id="e133e-125">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="e133e-126">*função-attr-lista*</span><span class="sxs-lookup"><span data-stu-id="e133e-126">*function-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e133e-127">Especifica zero ou mais atributos que se aplicam à função.</span><span class="sxs-lookup"><span data-stu-id="e133e-127">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="e133e-128">Os atributos de função válidos são **\[** [**retorno de chamada**](callback.md) **\]** , **\[** [**local**](local.md) **\]** ; o atributo de ponteiro **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** ou **\[** [**PTR**](ptr.md) **\]** ; e a cadeia de caracteres de atributos de uso **\[** [](string.md) **\]** , **\[** [**ignorar**](ignore.md) **\]** e **\[** [**\_ identificador de contexto**](context-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="e133e-128">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="e133e-129">*especificador de tipo*</span><span class="sxs-lookup"><span data-stu-id="e133e-129">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="e133e-130">Especifica um [ \_ tipo base](midl-base-types.md), [**struct**](struct.md), [**Union**](union.md), tipo de [**Enumeração**](enum.md) ou identificador de tipo.</span><span class="sxs-lookup"><span data-stu-id="e133e-130">Specifies a [base\_type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="e133e-131">Uma especificação de armazenamento opcional pode preceder o *especificador de tipo*.</span><span class="sxs-lookup"><span data-stu-id="e133e-131">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="e133e-132">*declaração de PTR*</span><span class="sxs-lookup"><span data-stu-id="e133e-132">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="e133e-133">Especifica zero ou mais declaradores de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="e133e-133">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="e133e-134">Um Declarador de ponteiro é o mesmo que o Declarador de ponteiro usado em C. Ele é construído a partir do **\*** designador, modificadores, como **distante** e o qualificador **const**.</span><span class="sxs-lookup"><span data-stu-id="e133e-134">A pointer declarator is the same as the pointer declarator used in C. It is constructed from the **\*** designator, modifiers such as **far**, and the qualifier **const**.</span></span>

</dd> <dt>

<span data-ttu-id="e133e-135">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="e133e-135">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e133e-136">Especifica o nome do procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="e133e-136">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="e133e-137">*lista de atributos de parâmetro*</span><span class="sxs-lookup"><span data-stu-id="e133e-137">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="e133e-138">Especifica zero ou mais atributos direcionais, atributos de campo, atributos de uso e atributos de ponteiro apropriados para o tipo de parâmetro especificado.</span><span class="sxs-lookup"><span data-stu-id="e133e-138">Specifies zero or more directional attributes, field attributes, usage attributes, and pointer attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="e133e-139">Separe vários atributos com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="e133e-139">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e133e-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="e133e-140">Remarks</span></span>

<span data-ttu-id="e133e-141">MIDL permite que você declare tipos inteiros, caracteres, cadeias de caracteres e boolianos constantes no corpo da interface do arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="e133e-141">MIDL allows you to declare constant integer, character, string, and Boolean types in the interface body of the IDL file.</span></span> <span data-ttu-id="e133e-142">As declarações de tipo **const** são reproduzidas no arquivo de cabeçalho gerado como **\# definir** diretivas.</span><span class="sxs-lookup"><span data-stu-id="e133e-142">**Const** type declarations are reproduced in the generated header file as **\#define** directives.</span></span>

<span data-ttu-id="e133e-143">Os compiladores de IDL do DCE não dão suporte a expressões constantes.</span><span class="sxs-lookup"><span data-stu-id="e133e-143">DCE IDL compilers do not support constant expressions.</span></span> <span data-ttu-id="e133e-144">Portanto, esse recurso não está disponível quando você usa a opção [**/OSF**](-osf.md) do compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="e133e-144">Therefore, this feature is not available when you use the MIDL compiler [**/osf**](-osf.md) switch.</span></span>

<span data-ttu-id="e133e-145">Uma constante definida anteriormente pode ser usada como o valor atribuído de uma constante subsequente.</span><span class="sxs-lookup"><span data-stu-id="e133e-145">A previously defined constant can be used as the assigned value of a subsequent constant.</span></span> <span data-ttu-id="e133e-146">O valor de uma expressão integral constante é convertido automaticamente no respectivo tipo de inteiro de acordo com as regras de conversão C.</span><span class="sxs-lookup"><span data-stu-id="e133e-146">The value of a constant integral expression is automatically converted to the respective integer type in accordance with C conversion rules.</span></span>

<span data-ttu-id="e133e-147">O valor de uma constante de caractere deve ser um caractere ASCII com aspas simples.</span><span class="sxs-lookup"><span data-stu-id="e133e-147">The value of a character constant must be a single-quoted ASCII character.</span></span> <span data-ttu-id="e133e-148">Quando a constante de caractere é o próprio caractere de aspas simples ('), o caractere de barra invertida ( \) deve preceder o caractere de aspas simples, como em \\ '.</span><span class="sxs-lookup"><span data-stu-id="e133e-148">When the character constant is the single-quote character itself ('), the backslash character (\) must precede the single-quote character, as in \\'.</span></span>

<span data-ttu-id="e133e-149">O valor de uma constante de cadeia de caracteres deve ser uma cadeia de caracteres entre aspas duplas.</span><span class="sxs-lookup"><span data-stu-id="e133e-149">The value of a character-string constant must be a double-quoted string.</span></span> <span data-ttu-id="e133e-150">Dentro de uma cadeia de caracteres, o caractere de barra invertida ( **\\** ) deve preceder um caractere de aspas duplas literal ( **"** ), como em **\\ "**.</span><span class="sxs-lookup"><span data-stu-id="e133e-150">Within a string, the backslash (**\\**) character must precede a literal double-quote character ( **"** ), as in **\\"**.</span></span> <span data-ttu-id="e133e-151">Dentro de uma cadeia de caracteres, o caractere de barra invertida ( **\\** ) representa um caractere de escape.</span><span class="sxs-lookup"><span data-stu-id="e133e-151">Within a string, the backslash character (**\\**) represents an escape character.</span></span> <span data-ttu-id="e133e-152">Constantes de cadeia de caracteres podem consistir de até 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="e133e-152">String constants can consist of up to 255 characters.</span></span>

<span data-ttu-id="e133e-153">O valor **NULL** é o único valor válido para constantes do tipo [**voidÂ \***](void.md).</span><span class="sxs-lookup"><span data-stu-id="e133e-153">The value **NULL** is the only valid value for constants of type [**voidÂ \***](void.md).</span></span> <span data-ttu-id="e133e-154">Todos os atributos associados à Declaração **const** são ignorados.</span><span class="sxs-lookup"><span data-stu-id="e133e-154">Any attributes associated with the **const** declaration are ignored.</span></span>

<span data-ttu-id="e133e-155">O compilador MIDL não verifica erros de intervalo na inicialização **const** .</span><span class="sxs-lookup"><span data-stu-id="e133e-155">The MIDL compiler does not check for range errors in **const** initialization.</span></span> <span data-ttu-id="e133e-156">Por exemplo, quando você especifica "const Short x = 0xFFFFFFFF;", o compilador MIDL não relata um erro e o inicializador é reproduzido no arquivo de cabeçalho gerado.</span><span class="sxs-lookup"><span data-stu-id="e133e-156">For example, when you specify "const short x = 0xFFFFFFFF;" the MIDL compiler does not report an error and the initializer is reproduced in the generated header file.</span></span>

## <a name="examples"></a><span data-ttu-id="e133e-157">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e133e-157">Examples</span></span>

``` syntax
const void *  p1        = NULL; 
const char    my_char1  = 'a'; 
const char    my_char2  = my_char1; 
const wchar_t my_wchar3 = L'a'; 
const wchar_t * pszNote = L"Note"; 
const unsigned short int x = 123; 
 
typedef [string] const char *LPCSTR; 
 
HRESULT GetName([out] wchar_t * const pszName );
```

## <a name="see-also"></a><span data-ttu-id="e133e-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="e133e-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e133e-159">**Storage**</span><span class="sxs-lookup"><span data-stu-id="e133e-159">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="e133e-160">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="e133e-160">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="e133e-161">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="e133e-161">**Boolean**</span></span>](boolean.md)
</dt> <dt>

[<span data-ttu-id="e133e-162">**minuciosa**</span><span class="sxs-lookup"><span data-stu-id="e133e-162">**byte**</span></span>](byte.md)
</dt> <dt>

[<span data-ttu-id="e133e-163">**retorno de chamada**</span><span class="sxs-lookup"><span data-stu-id="e133e-163">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="e133e-164">**char**</span><span class="sxs-lookup"><span data-stu-id="e133e-164">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="e133e-165">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="e133e-165">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="e133e-166">**enumera**</span><span class="sxs-lookup"><span data-stu-id="e133e-166">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="e133e-167">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="e133e-167">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="e133e-168">**ignorar**</span><span class="sxs-lookup"><span data-stu-id="e133e-168">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="e133e-169">**local**</span><span class="sxs-lookup"><span data-stu-id="e133e-169">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="e133e-170">**Longas**</span><span class="sxs-lookup"><span data-stu-id="e133e-170">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="e133e-171">**/osf**</span><span class="sxs-lookup"><span data-stu-id="e133e-171">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="e133e-172">**ptr**</span><span class="sxs-lookup"><span data-stu-id="e133e-172">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="e133e-173">**ref**</span><span class="sxs-lookup"><span data-stu-id="e133e-173">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="e133e-174">**short**</span><span class="sxs-lookup"><span data-stu-id="e133e-174">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="e133e-175">**inteiro**</span><span class="sxs-lookup"><span data-stu-id="e133e-175">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="e133e-176">**menores**</span><span class="sxs-lookup"><span data-stu-id="e133e-176">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="e133e-177">**string**</span><span class="sxs-lookup"><span data-stu-id="e133e-177">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="e133e-178">**struct**</span><span class="sxs-lookup"><span data-stu-id="e133e-178">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="e133e-179">**unida**</span><span class="sxs-lookup"><span data-stu-id="e133e-179">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="e133e-180">**diferente**</span><span class="sxs-lookup"><span data-stu-id="e133e-180">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="e133e-181">**não assinados**</span><span class="sxs-lookup"><span data-stu-id="e133e-181">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="e133e-182">**void**</span><span class="sxs-lookup"><span data-stu-id="e133e-182">**void**</span></span>](void.md)
</dt> <dt>

[<span data-ttu-id="e133e-183">**WCHAR \_ t**</span><span class="sxs-lookup"><span data-stu-id="e133e-183">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 
---
title: atributo const
description: A palavra-chave const modifica o tipo de uma declaração de tipo ou o tipo de um parâmetro de função, impedindo que o valor seja variável.
ms.assetid: 398fab76-93f3-4d5a-9223-1c57c612b2d7
keywords:
- atributo const MIDL
topic_type:
- apiref
api_name:
- const
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7095e29daf18dc111caf37038b06b0beff5245a8
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387055"
---
# <a name="const-attribute"></a><span data-ttu-id="be089-104">atributo const</span><span class="sxs-lookup"><span data-stu-id="be089-104">const attribute</span></span>

<span data-ttu-id="be089-105">A **palavra-chave const** modifica o tipo de uma declaração de tipo ou o tipo de um parâmetro de função, impedindo que o valor seja variável.</span><span class="sxs-lookup"><span data-stu-id="be089-105">The **const** keyword modifies the type of a type declaration or the type of a function parameter, preventing the value from varying.</span></span>

``` syntax
const const-type identifier = const-expression ;

[ typedef [ , type-attribute-list ] ] const const-type declarator-list;

[ typedef [ , type-attribute-list ] ] pointer-type const declarator-list;

[ [ function-attr-list ] ] type-specifier [ ptr-decl ] function-name(
    [ [ parameter-attribute-list ] ] ) const; 

const-type [declarator], [ [ parameter-attribute-list ] ] pointer-type const [declarator], ...);
```

## <a name="parameters"></a><span data-ttu-id="be089-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be089-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be089-107">*const-type*</span><span class="sxs-lookup"><span data-stu-id="be089-107">*const-type*</span></span> 
</dt> <dd>

<span data-ttu-id="be089-108">Especifica um inteiro MIDL válido, caractere, cadeia de caracteres ou tipo booliana.</span><span class="sxs-lookup"><span data-stu-id="be089-108">Specifies a valid MIDL integer, character, string, or Boolean type.</span></span> <span data-ttu-id="be089-109">Os tipos MIDL válidos incluem [**small**](small.md), [**short**](short.md), [**long**](long.md), [**char**](char-idl.md), \**charÂ \** _, _ [*wchar \_ t* \*](wchar-t.md), \**wchar \_ tÂ \**_, _ [*byte* \*](byte.md), \**byteÂ \** _, e [_*voidÂ \**_](void.md).</span><span class="sxs-lookup"><span data-stu-id="be089-109">Valid MIDL types include [**small**](small.md), [**short**](short.md), [**long**](long.md), [**char**](char-idl.md), \**charÂ \**_, [_ *wchar\_t*\*](wchar-t.md), \**wchar\_tÂ \**_, [_ *byte*\*](byte.md), \**byteÂ \** _, and [_*voidÂ \**_](void.md).</span></span> <span data-ttu-id="be089-110">Os tipos de inteiro e de caractere podem ser [_ *assinados* \*](signed.md) [**ou não assinados.**](unsigned.md)</span><span class="sxs-lookup"><span data-stu-id="be089-110">The integer and character types can be [_ *signed*\*](signed.md) or [**unsigned**](unsigned.md).</span></span>

</dd> <dt>

<span data-ttu-id="be089-111">*identifier*</span><span class="sxs-lookup"><span data-stu-id="be089-111">*identifier*</span></span> 
</dt> <dd>

<span data-ttu-id="be089-112">Especifica um identificador MIDL válido.</span><span class="sxs-lookup"><span data-stu-id="be089-112">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="be089-113">Os identificadores MIDL válidos consistem em até 31 caracteres alfanuméricos e/ou sublinhados e devem começar com um caractere alfabético ou sublinhado.</span><span class="sxs-lookup"><span data-stu-id="be089-113">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> <dt>

<span data-ttu-id="be089-114">*const-expression*</span><span class="sxs-lookup"><span data-stu-id="be089-114">*const-expression*</span></span> 
</dt> <dd>

<span data-ttu-id="be089-115">Especifica uma expressão, identificador ou constante numérica ou de caractere apropriada para o tipo especificado: literais inteiros constantes ou expressões de inteiro constante para constantes de inteiro; Expressões boolianas que podem ser computadas na compilação para [**tipos boolianas;**](boolean.md) constantes de caractere único para [**tipos char;**](char-idl.md) e constantes de cadeia de caracteres para tipos **\[** [**de cadeia de**](string.md) **\]** caracteres.</span><span class="sxs-lookup"><span data-stu-id="be089-115">Specifies an expression, identifier, or numeric or character constant appropriate for the specified type: constant integer literals or constant integer expressions for integer constants; Boolean expressions that can be computed at compilation for [**Boolean**](boolean.md) types; single-character constants for [**char**](char-idl.md) types; and string constants for **\[**[**string**](string.md)**\]** types.</span></span> <span data-ttu-id="be089-116">O [ \* *tipo \* voidÂ* _](void.md) pode ser inicializado somente para _\*NULL\*\*.</span><span class="sxs-lookup"><span data-stu-id="be089-116">The [\**voidÂ \** _](void.md) type can be initialized only to _\*NULL\*\*.</span></span>

</dd> <dt>

<span data-ttu-id="be089-117">*type-attribute-list*</span><span class="sxs-lookup"><span data-stu-id="be089-117">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="be089-118">Especifica um ou mais atributos que se aplicam ao tipo.</span><span class="sxs-lookup"><span data-stu-id="be089-118">Specifies one or more attributes that apply to the type.</span></span>

</dd> <dt>

<span data-ttu-id="be089-119">*tipo de ponteiro*</span><span class="sxs-lookup"><span data-stu-id="be089-119">*pointer-type*</span></span> 
</dt> <dd>

<span data-ttu-id="be089-120">Especifica um tipo de ponteiro MIDL válido.</span><span class="sxs-lookup"><span data-stu-id="be089-120">Specifies a valid MIDL pointer type.</span></span>

</dd> <dt>

<span data-ttu-id="be089-121">*declarator e declarator-list*</span><span class="sxs-lookup"><span data-stu-id="be089-121">*declarator and declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="be089-122">Especifica declaradores C padrão, como identificadores, declaradores de ponteiro e declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="be089-122">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="be089-123">Para obter mais informações, [consulte Matriz e Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrizes**](arrays-1.md)e [matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="be089-123">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="be089-124">A *lista de declaradores* consiste em um ou mais declaradores, separados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="be089-124">The *declarator-list* consists of one or more declarators, separated by commas.</span></span> <span data-ttu-id="be089-125">O identificador de nome de parâmetro no declarador de função é opcional.</span><span class="sxs-lookup"><span data-stu-id="be089-125">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="be089-126">*function-attr-list*</span><span class="sxs-lookup"><span data-stu-id="be089-126">*function-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="be089-127">Especifica zero ou mais atributos que se aplicam à função.</span><span class="sxs-lookup"><span data-stu-id="be089-127">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="be089-128">Atributos de função válidos são retorno de chamada , local ; o atributo de ponteiro ref , exclusivo ou ptr ; e a cadeia de caracteres de atributos de uso **\[** [](callback.md) **\]** **\[** [](local.md) **\]** **\[** [](ref.md) **\]** **\[** [](unique.md) **\]** **\[** [](ptr.md) **\]** , **\[** [](string.md) **\]** **\[** [**ignoram**](ignore.md) **\]** e o indicador de **\[** [**\_ contexto**](context-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="be089-128">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="be089-129">*especificador de tipo*</span><span class="sxs-lookup"><span data-stu-id="be089-129">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="be089-130">Especifica um tipo base , [**struct**](struct.md), [**union**](union.md), [**tipo enum**](enum.md) ou identificador de tipo. [ \_](midl-base-types.md)</span><span class="sxs-lookup"><span data-stu-id="be089-130">Specifies a [base\_type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="be089-131">Uma especificação de armazenamento opcional pode *preceder o especificador de tipo*.</span><span class="sxs-lookup"><span data-stu-id="be089-131">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="be089-132">*ptr-decl*</span><span class="sxs-lookup"><span data-stu-id="be089-132">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="be089-133">Especifica zero ou mais declaradores de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="be089-133">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="be089-134">Um declarador de ponteiro é o mesmo que o declarador de ponteiro usado em C. Ele é construído do **\* *designador _ , modificadores*** como _ far e o qualificador **const**.</span><span class="sxs-lookup"><span data-stu-id="be089-134">A pointer declarator is the same as the pointer declarator used in C. It is constructed from the \**\**_ designator, modifiers such as _\* far\*\*, and the qualifier **const**.</span></span>

</dd> <dt>

<span data-ttu-id="be089-135">*function-name*</span><span class="sxs-lookup"><span data-stu-id="be089-135">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="be089-136">Especifica o nome do procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="be089-136">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="be089-137">*parameter-attribute-list*</span><span class="sxs-lookup"><span data-stu-id="be089-137">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="be089-138">Especifica zero ou mais atributos direcionais, atributos de campo, atributos de uso e atributos de ponteiro apropriados para o tipo de parâmetro especificado.</span><span class="sxs-lookup"><span data-stu-id="be089-138">Specifies zero or more directional attributes, field attributes, usage attributes, and pointer attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="be089-139">Separe vários atributos com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="be089-139">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be089-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="be089-140">Remarks</span></span>

<span data-ttu-id="be089-141">MIDL permite declarar inteiro constante, caractere, cadeia de caracteres e tipos boolianas no corpo da interface do arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="be089-141">MIDL allows you to declare constant integer, character, string, and Boolean types in the interface body of the IDL file.</span></span> <span data-ttu-id="be089-142">**As** declarações de tipo Const são reproduzidas no arquivo de header gerado como **\# diretivas de** definição.</span><span class="sxs-lookup"><span data-stu-id="be089-142">**Const** type declarations are reproduced in the generated header file as **\#define** directives.</span></span>

<span data-ttu-id="be089-143">Os compiladores de IDL de DCE não são suportados por expressões constantes.</span><span class="sxs-lookup"><span data-stu-id="be089-143">DCE IDL compilers do not support constant expressions.</span></span> <span data-ttu-id="be089-144">Portanto, esse recurso não está disponível quando você usa a opção [**/osf do**](-osf.md) compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="be089-144">Therefore, this feature is not available when you use the MIDL compiler [**/osf**](-osf.md) switch.</span></span>

<span data-ttu-id="be089-145">Uma constante definida anteriormente pode ser usada como o valor atribuído de uma constante subsequente.</span><span class="sxs-lookup"><span data-stu-id="be089-145">A previously defined constant can be used as the assigned value of a subsequent constant.</span></span> <span data-ttu-id="be089-146">O valor de uma expressão integral constante é convertido automaticamente no respectivo tipo inteiro de acordo com as regras de conversão C.</span><span class="sxs-lookup"><span data-stu-id="be089-146">The value of a constant integral expression is automatically converted to the respective integer type in accordance with C conversion rules.</span></span>

<span data-ttu-id="be089-147">O valor de uma constante de caractere deve ser um caractere ASCII entre aspas simples.</span><span class="sxs-lookup"><span data-stu-id="be089-147">The value of a character constant must be a single-quoted ASCII character.</span></span> <span data-ttu-id="be089-148">Quando a constante de caractere é o próprio caractere de aspas simples ('), o caractere de faixa invertida ( ) deve preceder o caractere de aspas \\ simples, como \\ em '.</span><span class="sxs-lookup"><span data-stu-id="be089-148">When the character constant is the single-quote character itself ('), the backslash character (\\) must precede the single-quote character, as in \\'.</span></span>

<span data-ttu-id="be089-149">O valor de uma constante de cadeia de caracteres deve ser uma cadeia de caracteres entre aspas duplas.</span><span class="sxs-lookup"><span data-stu-id="be089-149">The value of a character-string constant must be a double-quoted string.</span></span> <span data-ttu-id="be089-150">Em uma cadeia de caracteres, o caractere de linha invertida ( ) deve preceder um caractere de aspas duplas literais **\\** ( **"** ), como **\\ em "**.</span><span class="sxs-lookup"><span data-stu-id="be089-150">Within a string, the backslash (**\\**) character must precede a literal double-quote character ( **"** ), as in **\\"**.</span></span> <span data-ttu-id="be089-151">Em uma cadeia de caracteres, o caractere de faixa invertida ( **\\** ) representa um caractere de escape.</span><span class="sxs-lookup"><span data-stu-id="be089-151">Within a string, the backslash character (**\\**) represents an escape character.</span></span> <span data-ttu-id="be089-152">Constantes de cadeia de caracteres podem consistir em até 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="be089-152">String constants can consist of up to 255 characters.</span></span>

<span data-ttu-id="be089-153">O valor **NULL** é o único valor válido para constantes do tipo [ \* *voidÂ \** _](void.md).</span><span class="sxs-lookup"><span data-stu-id="be089-153">The value **NULL** is the only valid value for constants of type [\**voidÂ \** _](void.md).</span></span> <span data-ttu-id="be089-154">Todos os atributos associados à declaração _ *const*\* são ignorados.</span><span class="sxs-lookup"><span data-stu-id="be089-154">Any attributes associated with the _ *const*\* declaration are ignored.</span></span>

<span data-ttu-id="be089-155">O compilador MIDL não verifica se há erros de intervalo na **inicialização const.**</span><span class="sxs-lookup"><span data-stu-id="be089-155">The MIDL compiler does not check for range errors in **const** initialization.</span></span> <span data-ttu-id="be089-156">Por exemplo, quando você especifica "const short x = 0xFFFFFFFF;", o compilador MIDL não relata um erro e o inicializador é reproduzido no arquivo de header gerado.</span><span class="sxs-lookup"><span data-stu-id="be089-156">For example, when you specify "const short x = 0xFFFFFFFF;" the MIDL compiler does not report an error and the initializer is reproduced in the generated header file.</span></span>

## <a name="examples"></a><span data-ttu-id="be089-157">Exemplos</span><span class="sxs-lookup"><span data-stu-id="be089-157">Examples</span></span>

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

## <a name="see-also"></a><span data-ttu-id="be089-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="be089-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be089-159">**Matrizes**</span><span class="sxs-lookup"><span data-stu-id="be089-159">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="be089-160">Tipos base MIDL</span><span class="sxs-lookup"><span data-stu-id="be089-160">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="be089-161">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="be089-161">**Boolean**</span></span>](boolean.md)
</dt> <dt>

[<span data-ttu-id="be089-162">**Byte**</span><span class="sxs-lookup"><span data-stu-id="be089-162">**byte**</span></span>](byte.md)
</dt> <dt>

[<span data-ttu-id="be089-163">**retorno de chamada**</span><span class="sxs-lookup"><span data-stu-id="be089-163">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="be089-164">**Char**</span><span class="sxs-lookup"><span data-stu-id="be089-164">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="be089-165">**alça de \_ contexto**</span><span class="sxs-lookup"><span data-stu-id="be089-165">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="be089-166">**Enum**</span><span class="sxs-lookup"><span data-stu-id="be089-166">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="be089-167">Arquivo IDL (definição de interface)</span><span class="sxs-lookup"><span data-stu-id="be089-167">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="be089-168">**Ignorar**</span><span class="sxs-lookup"><span data-stu-id="be089-168">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="be089-169">**Local**</span><span class="sxs-lookup"><span data-stu-id="be089-169">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="be089-170">**Longas**</span><span class="sxs-lookup"><span data-stu-id="be089-170">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="be089-171">**/osf**</span><span class="sxs-lookup"><span data-stu-id="be089-171">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="be089-172">**ptr**</span><span class="sxs-lookup"><span data-stu-id="be089-172">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="be089-173">**ref**</span><span class="sxs-lookup"><span data-stu-id="be089-173">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="be089-174">**Curto**</span><span class="sxs-lookup"><span data-stu-id="be089-174">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="be089-175">**Assinado**</span><span class="sxs-lookup"><span data-stu-id="be089-175">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="be089-176">**Pequeno**</span><span class="sxs-lookup"><span data-stu-id="be089-176">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="be089-177">**String**</span><span class="sxs-lookup"><span data-stu-id="be089-177">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="be089-178">**Struct**</span><span class="sxs-lookup"><span data-stu-id="be089-178">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="be089-179">**União**</span><span class="sxs-lookup"><span data-stu-id="be089-179">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="be089-180">**unique**</span><span class="sxs-lookup"><span data-stu-id="be089-180">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="be089-181">**Unsigned**</span><span class="sxs-lookup"><span data-stu-id="be089-181">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="be089-182">**Vazio**</span><span class="sxs-lookup"><span data-stu-id="be089-182">**void**</span></span>](void.md)
</dt> <dt>

[<span data-ttu-id="be089-183">**wchar \_ t**</span><span class="sxs-lookup"><span data-stu-id="be089-183">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 
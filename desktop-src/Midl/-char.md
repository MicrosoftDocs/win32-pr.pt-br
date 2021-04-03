---
title: comutador/Char
description: A opção/Char ajuda a garantir que o compilador de MIDL e o compilador C operem juntos corretamente para todos os tipos char e Small.
ms.assetid: 83f204cf-9cd0-42f3-bce7-b8f582e50e67
keywords:
- MIDL do comutador/Char
topic_type:
- apiref
api_name:
- /char
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2254db9d0f4efcd003362e4126c5c295ca532b2f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638636"
---
# <a name="char-switch"></a><span data-ttu-id="4e854-104">comutador/Char</span><span class="sxs-lookup"><span data-stu-id="4e854-104">/char switch</span></span>

<span data-ttu-id="4e854-105">A opção **/Char** ajuda a garantir que o compilador de MIDL e o compilador C operem juntos corretamente para todos os tipos [**Char**](char-idl.md) e [**Small**](small.md) .</span><span class="sxs-lookup"><span data-stu-id="4e854-105">The **/char** switch helps to ensure that the MIDL compiler and C compiler operate together correctly for all [**char**](char-idl.md) and [**small**](small.md) types.</span></span>

``` syntax
midl /char { signed | unsigned | ascii7 }
```

## <a name="switch-options"></a><span data-ttu-id="4e854-106">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="4e854-106">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="signed"></span><span id="SIGNED"></span>

<span data-ttu-id="4e854-107"><span id="signed"></span><span id="SIGNED"></span>assinado \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="4e854-107"><span id="signed"></span><span id="SIGNED"></span>\*\*\*\*signed\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="4e854-108">Especifica que o tipo de compilador C padrão para [**Char**](char-idl.md) é assinado.</span><span class="sxs-lookup"><span data-stu-id="4e854-108">Specifies that the default C-compiler type for [**char**](char-idl.md) is signed.</span></span> <span data-ttu-id="4e854-109">Todas as ocorrências de **Char** não acompanhadas por uma especificação de sinal são geradas como caracteres não assinados.</span><span class="sxs-lookup"><span data-stu-id="4e854-109">All occurrences of **char** not accompanied by a sign specification are generated as unsigned char.</span></span>

</dd> <dt>

<span id="unsigned"></span><span id="UNSIGNED"></span>

<span data-ttu-id="4e854-110"><span id="unsigned"></span><span id="UNSIGNED"></span>Não assinado \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="4e854-110"><span id="unsigned"></span><span id="UNSIGNED"></span>\*\*\*\*unsigned\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="4e854-111">Especifica que o tipo de compilador C padrão para [**Char**](char-idl.md) não é assinado.</span><span class="sxs-lookup"><span data-stu-id="4e854-111">Specifies that the default C-compiler type for [**char**](char-idl.md) is unsigned.</span></span> <span data-ttu-id="4e854-112">Todos os usos de [**pequenos**](small.md) não acompanhados por uma especificação de sinal são gerados como pequenos assinados.</span><span class="sxs-lookup"><span data-stu-id="4e854-112">All uses of [**small**](small.md) not accompanied by a sign specification are generated as signed small.</span></span>

</dd> <dt>

<span id="ascii7"></span><span id="ASCII7"></span>

<span data-ttu-id="4e854-113"><span id="ascii7"></span><span id="ASCII7"></span>ascii7 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="4e854-113"><span id="ascii7"></span><span id="ASCII7"></span>\*\*\*\*ascii7\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="4e854-114">Especifica que todos os valores de [**caracteres**](char-idl.md) devem ser passados para os arquivos gerados sem uma palavra-chave de assinatura específica.</span><span class="sxs-lookup"><span data-stu-id="4e854-114">Specifies that all [**char**](char-idl.md) values are to be passed into the generated files without a specific sign keyword.</span></span> <span data-ttu-id="4e854-115">Todos os usos de [**pequenos**](small.md) não acompanhados por uma especificação de sinal são gerados como **pequenos**.</span><span class="sxs-lookup"><span data-stu-id="4e854-115">All uses of [**small**](small.md) not accompanied by a sign specification are generated as **small**.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e854-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e854-116">Remarks</span></span>

<span data-ttu-id="4e854-117">Por definição, o [**caractere**](char-idl.md) MIDL não é assinado.</span><span class="sxs-lookup"><span data-stu-id="4e854-117">By definition, MIDL [**char**](char-idl.md) is unsigned.</span></span> <span data-ttu-id="4e854-118">"Small" é definido em termos de **Char** ( \# define Small Char) e MIDL [**Small**](small.md) é assinado.</span><span class="sxs-lookup"><span data-stu-id="4e854-118">"Small" is defined in terms of **char** (\#define small char), and MIDL [**small**](small.md) is signed.</span></span>

<span data-ttu-id="4e854-119">A opção **/Char** instrui o compilador MIDL a especificar declarações [**assinadas**](signed.md) explícitas ou [**sem sinal**](unsigned.md) nos arquivos gerados quando a declaração de assinatura do C-compilador estiver em conflito com o padrão MIDL para esse tipo.</span><span class="sxs-lookup"><span data-stu-id="4e854-119">The **/char** switch directs the MIDL compiler to specify explicit [**signed**](signed.md) or [**unsigned**](unsigned.md) declarations in the generated files when the C-compiler sign declaration conflicts with the MIDL default for that type.</span></span>

<span data-ttu-id="4e854-120">Lembre-se de que o compilador MIDL gera os stubs como código-fonte C, que você deve compilar como parte de seus programas de cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="4e854-120">Remember that the MIDL compiler generates the stubs as C source code, which you must compile as part of your client and server programs.</span></span> <span data-ttu-id="4e854-121">Alguns compiladores usam um **caractere assinado** em todos os dados [**Char**](char-idl.md) especificados no código-fonte.</span><span class="sxs-lookup"><span data-stu-id="4e854-121">Some compilers use a **signed char** everywhere [**char**](char-idl.md) data is specified in the source code.</span></span> <span data-ttu-id="4e854-122">O código-fonte do stub que o compilador MIDL gera trata todos os dados **Char** como **caracteres não assinados**.</span><span class="sxs-lookup"><span data-stu-id="4e854-122">The stub source code that the MIDL compiler generates treats all **char** data as **unsigned char**.</span></span> <span data-ttu-id="4e854-123">Se o compilador MIDL simplesmente gerar todos os dados **Char** no arquivo IDL como dados **Char** nos stubs, os compiladores que usam um **caractere assinado** para dados **Char** causarão um conflito no código-fonte do stub.</span><span class="sxs-lookup"><span data-stu-id="4e854-123">If the MIDL compiler simply generated all **char** data in the IDL file as **char** data in the stubs, compilers that use a **signed char** for **char** data would cause a conflict in the stub source code.</span></span>

<span data-ttu-id="4e854-124">A finalidade da opção de linha de comando **/Char** é resolver esses conflitos em potencial.</span><span class="sxs-lookup"><span data-stu-id="4e854-124">The purpose of the **/char** command line switch is to resolve these potential conflicts.</span></span> <span data-ttu-id="4e854-125">Preserva todos os dados especificados como [**Char**](char-idl.md) no arquivo IDL como um **caractere não assinado** no código-fonte do stub.</span><span class="sxs-lookup"><span data-stu-id="4e854-125">It preserves all data specified as [**char**](char-idl.md) in the IDL file as **unsigned char** in the stub source code.</span></span> <span data-ttu-id="4e854-126">Ele também mantém dados [**pequenos**](small.md) como assinados.</span><span class="sxs-lookup"><span data-stu-id="4e854-126">It also maintains [**small**](small.md) data as signed.</span></span>

<span data-ttu-id="4e854-127">A tabela a seguir resume os tipos gerados.</span><span class="sxs-lookup"><span data-stu-id="4e854-127">The following table summarizes the generated types.</span></span>



| <span data-ttu-id="4e854-128">opção MIDL/Char</span><span class="sxs-lookup"><span data-stu-id="4e854-128">midl /char option</span></span>       | <span data-ttu-id="4e854-129">Tipo de caractere gerado</span><span class="sxs-lookup"><span data-stu-id="4e854-129">Generated char type</span></span> | <span data-ttu-id="4e854-130">Tipo pequeno gerado</span><span class="sxs-lookup"><span data-stu-id="4e854-130">Generated small type</span></span> |
|-------------------------|---------------------|----------------------|
| <span data-ttu-id="4e854-131">**/Char de MIDL assinado**</span><span class="sxs-lookup"><span data-stu-id="4e854-131">**midl /char signed**</span></span>   | <span data-ttu-id="4e854-132">**unsigned char**</span><span class="sxs-lookup"><span data-stu-id="4e854-132">**unsigned char**</span></span>   | <span data-ttu-id="4e854-133">**small**</span><span class="sxs-lookup"><span data-stu-id="4e854-133">**small**</span></span>            |
| <span data-ttu-id="4e854-134">**MIDL/Char não assinado**</span><span class="sxs-lookup"><span data-stu-id="4e854-134">**midl /char unsigned**</span></span> | <span data-ttu-id="4e854-135">**char**</span><span class="sxs-lookup"><span data-stu-id="4e854-135">**char**</span></span>            | <span data-ttu-id="4e854-136">**pequeno assinado**</span><span class="sxs-lookup"><span data-stu-id="4e854-136">**signed small**</span></span>     |
| <span data-ttu-id="4e854-137">**/Char MIDL ascii7**</span><span class="sxs-lookup"><span data-stu-id="4e854-137">**midl /char ascii7**</span></span>   | <span data-ttu-id="4e854-138">**char**</span><span class="sxs-lookup"><span data-stu-id="4e854-138">**char**</span></span>            | <span data-ttu-id="4e854-139">**small**</span><span class="sxs-lookup"><span data-stu-id="4e854-139">**small**</span></span>            |



 

<span data-ttu-id="4e854-140">A opção **/Char** signed indica que o caractere do compilador C e os tipos pequenos são assinados.</span><span class="sxs-lookup"><span data-stu-id="4e854-140">The **/char** signed option indicates that the C-compiler char and small types are signed.</span></span> <span data-ttu-id="4e854-141">Para corresponder o padrão MIDL para **Char**, o compilador MIDL deve converter todos os usos de **Char** não acompanhados por uma especificação de sinal para um **Char não assinado**.</span><span class="sxs-lookup"><span data-stu-id="4e854-141">To match the MIDL default for **char**, the MIDL compiler must convert all uses of **char** not accompanied by a sign specification to **unsigned char**.</span></span> <span data-ttu-id="4e854-142">O tipo [**pequeno**](small.md) não é modificado porque o padrão C-Compiler corresponde ao padrão MIDL para **pequeno**.</span><span class="sxs-lookup"><span data-stu-id="4e854-142">The [**small**](small.md) type is not modified because this C-compiler default matches the MIDL default for **small**.</span></span>

<span data-ttu-id="4e854-143">A opção **/Char** não assinado indica que o tipo de [**caractere**](char-idl.md) do compilador C não está assinado.</span><span class="sxs-lookup"><span data-stu-id="4e854-143">The **/char** unsigned option indicates that the C-compiler [**char**](char-idl.md) type is unsigned.</span></span> <span data-ttu-id="4e854-144">O compilador MIDL converte todos os usos de [**pequenos**](small.md) não acompanhados por uma especificação de sinal para uma **assinatura** **pequena**.</span><span class="sxs-lookup"><span data-stu-id="4e854-144">The MIDL compiler converts all uses of [**small**](small.md) not accompanied by a sign specification to **signed** **small**.</span></span>

<span data-ttu-id="4e854-145">A opção ascii7 indica que nenhuma especificação de sinal explícita é adicionada aos tipos [**Char**](char-idl.md) .</span><span class="sxs-lookup"><span data-stu-id="4e854-145">The ascii7 option indicates that no explicit sign specification is added to [**char**](char-idl.md) types.</span></span> <span data-ttu-id="4e854-146">O tipo [**pequeno**](small.md) é gerado como **pequeno**.</span><span class="sxs-lookup"><span data-stu-id="4e854-146">The type [**small**](small.md) is generated as **small**.</span></span>

<span data-ttu-id="4e854-147">Para evitar confusão, você deve usar especificações de assinatura explícitas para tipos [**Char**](char-idl.md) e Small, sempre que possível no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="4e854-147">To avoid confusion, you should use explicit sign specifications for [**char**](char-idl.md) and small types whenever possible in the IDL file.</span></span> <span data-ttu-id="4e854-148">Observe que o uso de tipos de **caracteres** explicitamente assinados em seu arquivo IDL não é suportado pela DCE IDL.</span><span class="sxs-lookup"><span data-stu-id="4e854-148">Note that the use of explicitly signed **char** types in your IDL file is not supported by DCE IDL.</span></span> <span data-ttu-id="4e854-149">Portanto, esse recurso não está disponível quando você compila com a opção MIDL [**/OSF**](-osf.md)</span><span class="sxs-lookup"><span data-stu-id="4e854-149">Therefore, this feature is not available when you compile with the MIDL [**/osf**](-osf.md) switch.</span></span>

<span data-ttu-id="4e854-150">Para obter mais informações relacionadas ao **/Char**, consulte [**Small**](small.md).</span><span class="sxs-lookup"><span data-stu-id="4e854-150">For more information related to **/char**, see [**small**](small.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4e854-151">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4e854-151">Examples</span></span>

<span data-ttu-id="4e854-152">**MIDL/Char assinou filename. idl**</span><span class="sxs-lookup"><span data-stu-id="4e854-152">**midl /char signed filename.idl**</span></span>

<span data-ttu-id="4e854-153">**MIDL/Char filename não assinado. idl**</span><span class="sxs-lookup"><span data-stu-id="4e854-153">**midl /char unsigned filename.idl**</span></span>

<span data-ttu-id="4e854-154">**MIDL/Char ascii7 filename. idl**</span><span class="sxs-lookup"><span data-stu-id="4e854-154">**midl /char ascii7 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="4e854-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e854-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e854-156">**char**</span><span class="sxs-lookup"><span data-stu-id="4e854-156">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="4e854-157">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="4e854-157">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="4e854-158">**/osf**</span><span class="sxs-lookup"><span data-stu-id="4e854-158">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="4e854-159">**menores**</span><span class="sxs-lookup"><span data-stu-id="4e854-159">**small**</span></span>](small.md)
</dt> </dl>

 

 





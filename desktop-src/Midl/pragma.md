---
title: atributo pragma
description: A diretiva \ pragma MIDL \_ Echo instrui o MIDL a emitir a cadeia de caracteres especificada, sem os caracteres de aspas, no arquivo de cabeçalho gerado.
ms.assetid: b8a175d2-ea07-4103-ab45-0de7e477d27a
keywords:
- atributo pragma MIDL
topic_type:
- apiref
api_name:
- pragma
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72f5e1c00c089bc8915adc2d9f3363305c677a96
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103916681"
---
# <a name="pragma-attribute"></a><span data-ttu-id="e5eb3-104">atributo pragma</span><span class="sxs-lookup"><span data-stu-id="e5eb3-104">pragma attribute</span></span>

<span data-ttu-id="e5eb3-105">A \# diretiva **pragma MIDL \_ Echo** instrui o MIDL a emitir a cadeia de caracteres especificada, sem os caracteres de aspas, no arquivo de cabeçalho gerado.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-105">The \#**pragma midl\_echo** directive instructs MIDL to emit the specified string, without the quotation characters, into the generated header file.</span></span>

``` syntax
#pragma midl_echo("string")
#pragma token-sequence
#pragma pack (n)
#pragma pack ( [push] [, id] [, n} )
#pragma pack ( [pop] [, id] [, n} )
```

## <a name="parameters"></a><span data-ttu-id="e5eb3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e5eb3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5eb3-107">*cadeia de caracteres*</span><span class="sxs-lookup"><span data-stu-id="e5eb3-107">*string*</span></span> 
</dt> <dd>

<span data-ttu-id="e5eb3-108">Especifica uma cadeia de caracteres que é inserida no arquivo de cabeçalho gerado.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-108">Specifies a string that is inserted into the generated header file.</span></span> <span data-ttu-id="e5eb3-109">As aspas são removidas durante o processo de inserção.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-109">The quotation marks are removed during the insertion process.</span></span>

</dd> <dt>

<span data-ttu-id="e5eb3-110">*sequência de tokens*</span><span class="sxs-lookup"><span data-stu-id="e5eb3-110">*token-sequence*</span></span> 
</dt> <dd>

<span data-ttu-id="e5eb3-111">Especifica uma sequência de tokens que são inseridos no arquivo de cabeçalho gerado como parte de uma diretiva **\# pragma** sem processamento pelo compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-111">Specifies a sequence of tokens that are inserted into the generated header file as part of a **\#pragma** directive without processing by the MIDL compiler.</span></span>

</dd> <dt>

<span data-ttu-id="e5eb3-112">*n*</span><span class="sxs-lookup"><span data-stu-id="e5eb3-112">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="e5eb3-113">Especifica o tamanho atual do pacote.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-113">Specifies the current pack size.</span></span> <span data-ttu-id="e5eb3-114">Os valores válidos são 1, 2, 4, 8 e 16.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-114">Valid values are 1, 2, 4, 8, and 16.</span></span>

</dd> <dt>

<span data-ttu-id="e5eb3-115">*id*</span><span class="sxs-lookup"><span data-stu-id="e5eb3-115">*id*</span></span> 
</dt> <dd>

<span data-ttu-id="e5eb3-116">Especifica o identificador de usuário.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-116">Specifies the user identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e5eb3-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="e5eb3-117">Remarks</span></span>

<span data-ttu-id="e5eb3-118">As diretivas de pré-processamento c-Language que aparecem no arquivo IDL são processadas pelo pré-processador do compilador C.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-118">C-language preprocessing directives that appear in the IDL file are processed by the C compiler's preprocessor.</span></span> <span data-ttu-id="e5eb3-119">As diretivas de **\# definição** no arquivo IDL estão disponíveis durante a compilação de MIDL, embora não no compilador C.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-119">The **\#define** directives in the IDL file are available during MIDL compilation, although not to the C compiler.</span></span>

<span data-ttu-id="e5eb3-120">Por exemplo, quando o pré-processador encontra a diretiva "definir o \# Windows 4", o pré-processador substitui todas as ocorrências de "Windows" no arquivo IDL por "4".</span><span class="sxs-lookup"><span data-stu-id="e5eb3-120">For example, when the preprocessor encounters the directive "\#define WINDOWS 4", the preprocessor replaces all occurrences of "WINDOWS" in the IDL file with "4".</span></span> <span data-ttu-id="e5eb3-121">O símbolo "WINDOWS" não está disponível em tempo de compilação C.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-121">The symbol "WINDOWS" is not available at C-compile time.</span></span>

<span data-ttu-id="e5eb3-122">Para permitir que as definições de macro do pré-processador C passem pelo compilador MIDL para o compilador C, use a diretiva **\# pragma MIDL \_ Echo** ou [**cpp \_ quote**](cpp-quote.md) .</span><span class="sxs-lookup"><span data-stu-id="e5eb3-122">To allow the C-preprocessor macro definitions to pass through the MIDL compiler to the C compiler, use the **\#pragma midl\_echo** or [**cpp\_quote**](cpp-quote.md) directive.</span></span> <span data-ttu-id="e5eb3-123">Essas diretivas instruem o compilador MIDL a gerar um arquivo de cabeçalho que contém a cadeia de caracteres de parâmetro com as aspas removidas.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-123">These directives instruct the MIDL compiler to generate a header file that contains the parameter string with the quotation marks removed.</span></span> <span data-ttu-id="e5eb3-124">As diretivas **\# pragma MIDL \_ Echo** e **cpp \_ quote** são equivalentes.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-124">The **\#pragma midl\_echo** and **cpp\_quote** directives are equivalent.</span></span>

<span data-ttu-id="e5eb3-125">A diretiva **\# pragma Pack** é usada pelo compilador MIDL para controlar a embalagem de estruturas.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-125">The **\#pragma pack** directive is used by the MIDL compiler to control the packing of structures.</span></span> <span data-ttu-id="e5eb3-126">Ele substitui a opção de linha de comando [**/ZP**](-zp.md) .</span><span class="sxs-lookup"><span data-stu-id="e5eb3-126">It overrides the [**/Zp**](-zp.md) command-line switch.</span></span> <span data-ttu-id="e5eb3-127">A opção Pack (*n*) define o tamanho atual do pacote para um valor específico: 1, 2, 4, 8 ou 16.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-127">The pack (*n*) option sets the current pack size to a specific value: 1, 2, 4, 8, or 16.</span></span> <span data-ttu-id="e5eb3-128">As opções de pacote (push) e de pacote (pop) têm as seguintes características:</span><span class="sxs-lookup"><span data-stu-id="e5eb3-128">The pack (push) and pack (pop) options have the following characteristics:</span></span>

-   <span data-ttu-id="e5eb3-129">O compilador mantém uma pilha de embalagens.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-129">The compiler maintains a packing stack.</span></span> <span data-ttu-id="e5eb3-130">Os elementos da pilha de embalagens incluem um tamanho de pacote e uma *ID* opcional. A pilha é limitada apenas pela memória disponível com o tamanho atual do pacote na parte superior da pilha.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-130">The elements of the packing stack include a pack size and an optional *id*. The stack is limited only by available memory with the current pack size at the top of the stack.</span></span>
-   <span data-ttu-id="e5eb3-131">O pacote (push) resulta no tamanho atual do pacote enviado para a pilha de embalagens.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-131">Pack (push) results in the current pack size pushed onto the packing stack.</span></span> <span data-ttu-id="e5eb3-132">A pilha é limitada pela memória disponível.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-132">The stack is limited by available memory.</span></span>
-   <span data-ttu-id="e5eb3-133">Pack (Push,*n*) é o mesmo que Pack (push) seguido por Pack (*n*).</span><span class="sxs-lookup"><span data-stu-id="e5eb3-133">Pack (push,*n*) is the same as pack (push) followed by pack (*n*).</span></span>
-   <span data-ttu-id="e5eb3-134">Pack (Push, *ID*) também envia por push a *ID* para a pilha de embalagens junto com o tamanho do pacote.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-134">Pack (push, *id*) also pushes *id* onto the packing stack along with the pack size.</span></span>
-   <span data-ttu-id="e5eb3-135">Pack (Push, *ID*, *n*) é o mesmo que Pack (Push, *ID*) seguido por Pack (*n*).</span><span class="sxs-lookup"><span data-stu-id="e5eb3-135">Pack (push, *id*, *n*) is the same as pack (push, *id*) followed by pack (*n*).</span></span>
-   <span data-ttu-id="e5eb3-136">O pacote (pop) resulta na pop-up da pilha de embalagens.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-136">Pack (pop) results in popping the packing stack.</span></span> <span data-ttu-id="e5eb3-137">Pops desequilibrados causam avisos e definem o tamanho atual do pacote como o valor da linha de comando.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-137">Unbalanced pops cause warnings and set the current pack size to the command-line value.</span></span>
-   <span data-ttu-id="e5eb3-138">Se Pack (pop, *ID*, *n*) for especificado, *n* será ignorado.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-138">If pack (pop, *id*, *n*) is specified, then *n* is ignored.</span></span>

<span data-ttu-id="e5eb3-139">O compilador MIDL coloca as cadeias de caracteres especificadas nas diretivas de [**\\ \_ aspas de CPP**](cpp-quote.md) e **pragma** no arquivo de cabeçalho na sequência em que elas são especificadas no arquivo IDL e em relação a outros componentes de interface no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-139">The MIDL compiler places the strings specified in the [**\\cpp\_quote**](cpp-quote.md) and **pragma** directives in the header file in the sequence in which they are specified in the IDL file and relative to other interface components in the IDL file.</span></span> <span data-ttu-id="e5eb3-140">As cadeias de caracteres geralmente devem aparecer na seção interface-corpo do arquivo IDL após todas as operações de [**importação**](import.md) .</span><span class="sxs-lookup"><span data-stu-id="e5eb3-140">The strings should usually appear in the interface-body section of the IDL file after all [**import**](import.md) operations.</span></span>

<span data-ttu-id="e5eb3-141">O compilador MIDL não tenta processar diretivas **\# pragma** que não começam com o prefixo "MIDL" \_ .</span><span class="sxs-lookup"><span data-stu-id="e5eb3-141">The MIDL compiler does not attempt to process **\#pragma** directives that do not start with the prefix "midl\_."</span></span> <span data-ttu-id="e5eb3-142">Outras diretivas **\# pragma** no arquivo IDL são passadas para o arquivo de cabeçalho gerado sem alterações.</span><span class="sxs-lookup"><span data-stu-id="e5eb3-142">Other **\#pragma** directives in the IDL file are passed into the generated header file without changes.</span></span>

## <a name="examples"></a><span data-ttu-id="e5eb3-143">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e5eb3-143">Examples</span></span>

``` syntax
/* IDL file */ 
#pragma midl_echo("#define UNICODE") 
cpp_quote("#define __DELAYED_PREPROCESSING__ 1") 
#pragma hdrstop 
#pragma check_pointer(on) 
 
/* generated header file */ 
#define UNICODE 
#define __DELAYED_PREPROCESSING__ 1 
#pragma hdrstop 
#pragma check_pointer(on)
```

## <a name="see-also"></a><span data-ttu-id="e5eb3-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5eb3-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5eb3-145">**citação de CPP \_**</span><span class="sxs-lookup"><span data-stu-id="e5eb3-145">**cpp\_quote**</span></span>](cpp-quote.md)
</dt> <dt>

[<span data-ttu-id="e5eb3-146">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="e5eb3-146">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="e5eb3-147">**importe**</span><span class="sxs-lookup"><span data-stu-id="e5eb3-147">**import**</span></span>](import.md)
</dt> <dt>

[<span data-ttu-id="e5eb3-148">**/ZP**</span><span class="sxs-lookup"><span data-stu-id="e5eb3-148">**/Zp**</span></span>](-zp.md)
</dt> </dl>

 

 





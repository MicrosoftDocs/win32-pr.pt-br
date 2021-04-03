---
title: Atributo cpp_quote
description: A \_ palavra-chave quote quot instrui o MIDL a emitir a cadeia de caracteres especificada, sem os caracteres de aspas, no arquivo de cabeçalho gerado.
ms.assetid: 0e5a929e-b564-43f7-9270-e79486279834
keywords:
- cpp_quote do atributo MIDL
topic_type:
- apiref
api_name:
- cpp_quote
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5b85f9a909e82395a0a75cf66fb2957c4b03d9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006666"
---
# <a name="cpp_quote-attribute"></a><span data-ttu-id="085fe-104">\_atributo de citação cpp</span><span class="sxs-lookup"><span data-stu-id="085fe-104">cpp\_quote attribute</span></span>

<span data-ttu-id="085fe-105">A palavra-chave **\_ quote quot** instrui o MIDL a emitir a cadeia de caracteres especificada, sem os caracteres de aspas, no arquivo de cabeçalho gerado.</span><span class="sxs-lookup"><span data-stu-id="085fe-105">The **cpp\_quote** keyword instructs MIDL to emit the specified string, without the quote characters, into the generated header file.</span></span>

``` syntax
cpp_quote("string")
```

## <a name="parameters"></a><span data-ttu-id="085fe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="085fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="085fe-107">*cadeia de caracteres*</span><span class="sxs-lookup"><span data-stu-id="085fe-107">*string*</span></span> 
</dt> <dd>

<span data-ttu-id="085fe-108">Especifica uma cadeia de caracteres entre aspas emitida no arquivo de cabeçalho gerado.</span><span class="sxs-lookup"><span data-stu-id="085fe-108">Specifies a quoted string that is emitted in the generated header file.</span></span> <span data-ttu-id="085fe-109">A cadeia de caracteres deve estar entre aspas para evitar a expansão pelo pré-processador de C.</span><span class="sxs-lookup"><span data-stu-id="085fe-109">The string must be quoted to prevent expansion by the C preprocessor.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="085fe-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="085fe-110">Remarks</span></span>

<span data-ttu-id="085fe-111">As diretivas de pré-processamento c-Language que aparecem no arquivo IDL são processadas pelo pré-processador do compilador C.</span><span class="sxs-lookup"><span data-stu-id="085fe-111">C-language preprocessing directives that appear in the IDL file are processed by the C compiler's preprocessor.</span></span> <span data-ttu-id="085fe-112">As diretivas de **\# definição** no arquivo IDL estão disponíveis durante a compilação de MIDL, mas não estão disponíveis para o compilador C.</span><span class="sxs-lookup"><span data-stu-id="085fe-112">The **\#define** directives in the IDL file are available during MIDL compilation but are not available to the C compiler.</span></span>

<span data-ttu-id="085fe-113">Por exemplo, quando o pré-processador encontra a diretiva "definir o \# Windows 4", o pré-processador substitui todas as ocorrências de "Windows" no arquivo IDL por "4".</span><span class="sxs-lookup"><span data-stu-id="085fe-113">For example, when the preprocessor encounters the directive "\#define WINDOWS 4", the preprocessor replaces all occurrences of "WINDOWS" in the IDL file with "4".</span></span> <span data-ttu-id="085fe-114">O símbolo "WINDOWS" não está disponível durante a compilação em linguagem C.</span><span class="sxs-lookup"><span data-stu-id="085fe-114">The symbol "WINDOWS" is not available during C-language compilation.</span></span>

<span data-ttu-id="085fe-115">Para permitir que as definições de macro do pré-processador C passem pelo compilador MIDL para o compilador C, use a diretiva **\# pragma MIDL \_ Echo** ou **cpp \_ quote** .</span><span class="sxs-lookup"><span data-stu-id="085fe-115">To allow the C-preprocessor macro definitions to pass through the MIDL compiler to the C compiler, use the **\#pragma midl\_echo** or **cpp\_quote** directive.</span></span> <span data-ttu-id="085fe-116">Essas diretivas instruem o compilador MIDL a gerar um arquivo de cabeçalho que contém a cadeia de caracteres de parâmetro com as aspas removidas.</span><span class="sxs-lookup"><span data-stu-id="085fe-116">These directives instruct the MIDL compiler to generate a header file that contains the parameter string with the quotation marks removed.</span></span> <span data-ttu-id="085fe-117">As diretivas **\# pragma MIDL \_ Echo** e **cpp \_ quote** são equivalentes.</span><span class="sxs-lookup"><span data-stu-id="085fe-117">The **\#pragma midl\_echo** and **cpp\_quote** directives are equivalent.</span></span>

<span data-ttu-id="085fe-118">O compilador MIDL coloca as cadeias de caracteres especificadas nas diretivas de **\_ aspas de CPP** e [**pragma**](pragma.md) no arquivo de cabeçalho na sequência em que elas são especificadas no arquivo IDL e em relação a outros componentes de interface no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="085fe-118">The MIDL compiler places the strings specified in the **cpp\_quote** and [**pragma**](pragma.md) directives into the header file in the sequence in which they are specified in the IDL file, and relative to other interface components in the IDL file.</span></span> <span data-ttu-id="085fe-119">As cadeias de caracteres normalmente devem aparecer na seção corpo de interface de arquivo IDL após todas as operações de [**importação**](import.md) .</span><span class="sxs-lookup"><span data-stu-id="085fe-119">The strings should usually appear in the IDL file interface body section after all [**import**](import.md) operations.</span></span>

## <a name="examples"></a><span data-ttu-id="085fe-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="085fe-120">Examples</span></span>

``` syntax
cpp_quote("#include \"myfile.h\" ")  
cpp_quote("#define UNICODE")
```

## <a name="see-also"></a><span data-ttu-id="085fe-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="085fe-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="085fe-122">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="085fe-122">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="085fe-123">**importe**</span><span class="sxs-lookup"><span data-stu-id="085fe-123">**import**</span></span>](import.md)
</dt> <dt>

[<span data-ttu-id="085fe-124">**pragma**</span><span class="sxs-lookup"><span data-stu-id="085fe-124">**pragma**</span></span>](pragma.md)
</dt> </dl>

 

 





---
title: Recurso RCDATA
description: Define um recurso de dados brutos para um aplicativo. Os recursos de dados brutos permitem a inclusão de dados binários diretamente no arquivo executável.
ms.assetid: 7535cb06-858b-4726-aaa5-43519f84d0e4
keywords:
- Menus de recursos do RCDATA e outros recursos
topic_type:
- apiref
api_name:
- RCDATA
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44de0e71e3ba744f668535950224129b91bc3653
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103916806"
---
# <a name="rcdata-resource"></a><span data-ttu-id="cf318-105">Recurso RCDATA</span><span class="sxs-lookup"><span data-stu-id="cf318-105">RCDATA resource</span></span>

<span data-ttu-id="cf318-106">Define um recurso de dados brutos para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cf318-106">Defines a raw data resource for an application.</span></span> <span data-ttu-id="cf318-107">Os recursos de dados brutos permitem a inclusão de dados binários diretamente no arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="cf318-107">Raw data resources permit the inclusion of binary data directly in the executable file.</span></span>

``` syntax
nameID RCDATA  [optional-statements] {raw-data  ...}
```

## <a name="parameters"></a><span data-ttu-id="cf318-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cf318-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf318-109"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="cf318-109"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="cf318-110">Nome exclusivo ou um valor inteiro sem sinal de 16 bits que identifica o recurso.</span><span class="sxs-lookup"><span data-stu-id="cf318-110">Unique name or a 16-bit unsigned integer value that identifies the resource.</span></span>

</dd> <dt>

<span data-ttu-id="cf318-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*instruções opcionais*</span><span class="sxs-lookup"><span data-stu-id="cf318-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="cf318-112">Esse parâmetro pode ser zero ou mais das instruções a seguir.</span><span class="sxs-lookup"><span data-stu-id="cf318-112">This parameter can be zero or more of the following statements.</span></span>



| <span data-ttu-id="cf318-113">Instrução</span><span class="sxs-lookup"><span data-stu-id="cf318-113">Statement</span></span>                                                        | <span data-ttu-id="cf318-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf318-114">Description</span></span>                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf318-115">[**Características**](characteristics-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="cf318-115">[**CHARACTERISTICS**](characteristics-statement.md) *dword*</span></span>     | <span data-ttu-id="cf318-116">Informações definidas pelo usuário sobre um recurso que pode ser usado por ferramentas que lêem e gravam arquivos de recursos.</span><span class="sxs-lookup"><span data-stu-id="cf318-116">User-defined information about a resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="cf318-117">Para obter mais informações, consulte [**características**](characteristics-statement.md).</span><span class="sxs-lookup"><span data-stu-id="cf318-117">For more information, see [**CHARACTERISTICS**](characteristics-statement.md).</span></span> |
| <span data-ttu-id="cf318-118">[](language-statement.md) *Idioma* do idioma, *subidioma*</span><span class="sxs-lookup"><span data-stu-id="cf318-118">[**LANGUAGE**](language-statement.md) *language*, *sublanguage*</span></span> | <span data-ttu-id="cf318-119">Idioma do recurso.</span><span class="sxs-lookup"><span data-stu-id="cf318-119">Language for the resource.</span></span> <span data-ttu-id="cf318-120">Para obter mais informações, consulte [**Language**](language-statement.md).</span><span class="sxs-lookup"><span data-stu-id="cf318-120">For more information, see [**LANGUAGE**](language-statement.md).</span></span>                                                                                            |
| <span data-ttu-id="cf318-121">[](version-statement.md) *DWORD* da versão</span><span class="sxs-lookup"><span data-stu-id="cf318-121">[**VERSION**](version-statement.md) *dword*</span></span>                     | <span data-ttu-id="cf318-122">Número de versão definido pelo usuário para o recurso que pode ser usado por ferramentas que lêem e gravam arquivos de recursos.</span><span class="sxs-lookup"><span data-stu-id="cf318-122">User-defined version number for the resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="cf318-123">Para obter mais informações, consulte [**versão**](version-statement.md).</span><span class="sxs-lookup"><span data-stu-id="cf318-123">For more information, see [**VERSION**](version-statement.md).</span></span>              |



 

</dd> <dt>

<span data-ttu-id="cf318-124"><span id="raw-data"></span><span id="RAW-DATA"></span>*dados brutos*</span><span class="sxs-lookup"><span data-stu-id="cf318-124"><span id="raw-data"></span><span id="RAW-DATA"></span>*raw-data*</span></span>
</dt> <dd>

<span data-ttu-id="cf318-125">Dados brutos que consistem em um ou mais números inteiros ou cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="cf318-125">Raw data consisting of one or more integers or strings of characters.</span></span> <span data-ttu-id="cf318-126">Os inteiros podem ser especificados em formato decimal, octal ou hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="cf318-126">Integers can be specified in decimal, octal, or hexadecimal format.</span></span> <span data-ttu-id="cf318-127">Para ser compatível com o Windows de 16 bits, os inteiros são armazenados como valores de **palavra** .</span><span class="sxs-lookup"><span data-stu-id="cf318-127">To be compatible with 16-bit Windows, integers are stored as **WORD** values.</span></span> <span data-ttu-id="cf318-128">Você pode armazenar um inteiro como um valor **DWORD** qualificando o inteiro com o sufixo "L".</span><span class="sxs-lookup"><span data-stu-id="cf318-128">You can store an integer as a **DWORD** value by qualifying the integer with the "L" suffix.</span></span>

<span data-ttu-id="cf318-129">As cadeias de caracteres são colocadas entre aspas.</span><span class="sxs-lookup"><span data-stu-id="cf318-129">Strings are enclosed in quotation marks.</span></span> <span data-ttu-id="cf318-130">O RC não acrescenta automaticamente um caractere nulo de terminação a uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="cf318-130">RC does not automatically append a terminating null character to a string.</span></span> <span data-ttu-id="cf318-131">Cada cadeia de caracteres é uma sequência dos caracteres ANSI especificados, a menos que você o qualifique como uma cadeia de caracteres largos com o prefixo L.</span><span class="sxs-lookup"><span data-stu-id="cf318-131">Each string is a sequence of the specified ANSI characters, unless you qualify it as a wide-character string with the L prefix.</span></span>

<span data-ttu-id="cf318-132">O bloco de dados começa em um limite **DWORD** e o RC não executa nenhum preenchimento ou alinhamento de dados dentro do bloco de *dados brutos* .</span><span class="sxs-lookup"><span data-stu-id="cf318-132">The block of data begins on a **DWORD** boundary and RC performs no padding or alignment of data within the *raw-data* block.</span></span> <span data-ttu-id="cf318-133">É sua responsabilidade garantir o alinhamento adequado dos dados dentro do bloco.</span><span class="sxs-lookup"><span data-stu-id="cf318-133">It is your responsibility to ensure the proper alignment of data within the block.</span></span>

</dd> </dl>

<span data-ttu-id="cf318-134">Alguns atributos também têm suporte para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="cf318-134">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="cf318-135">Para obter mais informações, consulte [atributos de recursos comuns](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="cf318-135">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="cf318-136">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cf318-136">Examples</span></span>

<span data-ttu-id="cf318-137">O exemplo a seguir demonstra o uso da instrução **RCDATA** :</span><span class="sxs-lookup"><span data-stu-id="cf318-137">The following example demonstrates the use of the **RCDATA** statement:</span></span>

``` syntax
resname RCDATA
{
   "Here is an ANSI string\0",    // explicitly null-terminated 
   L"Here is a Unicode string\0", // explicitly null-terminated 
   1024,                          // integer, stored as WORD 
   7L,                            // integer, stored as DWORD 
   0x029a,                        // hex integer 
   0o733,                         // octal integer 
}
```

## <a name="see-also"></a><span data-ttu-id="cf318-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf318-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf318-139">**ACELERADORES**</span><span class="sxs-lookup"><span data-stu-id="cf318-139">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="cf318-140">**CARACTERÍSTICAS**</span><span class="sxs-lookup"><span data-stu-id="cf318-140">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="cf318-141">**LANGUAGE**</span><span class="sxs-lookup"><span data-stu-id="cf318-141">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="cf318-142">**ADICIONARMENU**</span><span class="sxs-lookup"><span data-stu-id="cf318-142">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="cf318-143">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="cf318-143">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="cf318-144">**VERSION**</span><span class="sxs-lookup"><span data-stu-id="cf318-144">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 





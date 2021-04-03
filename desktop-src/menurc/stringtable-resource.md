---
title: Recurso STRINGTABLE
description: Define um ou mais recursos de cadeia de caracteres para um aplicativo. Os recursos de cadeia de caracteres são simplesmente seqüências Unicode ou ASCII terminadas em nulo que podem ser carregadas quando necessário no arquivo executável, usando a função LoadString.
ms.assetid: 5868245d-3445-4792-86f5-253945310d36
keywords:
- Menus de recursos do STRINGTABLE e outros recursos
topic_type:
- apiref
api_name:
- STRINGTABLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 271abd022bdedd3b27e0434e7364542fa51c8987
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084537"
---
# <a name="stringtable-resource"></a><span data-ttu-id="d5b0e-105">Recurso STRINGTABLE</span><span class="sxs-lookup"><span data-stu-id="d5b0e-105">STRINGTABLE resource</span></span>

<span data-ttu-id="d5b0e-106">Define um ou mais recursos de cadeia de caracteres para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d5b0e-106">Defines one or more string resources for an application.</span></span> <span data-ttu-id="d5b0e-107">Os recursos de cadeia de caracteres são simplesmente seqüências Unicode ou ASCII terminadas em nulo que podem ser carregadas quando necessário no arquivo executável, usando a função [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa) .</span><span class="sxs-lookup"><span data-stu-id="d5b0e-107">String resources are simply null-terminated Unicode or ASCII strings that can be loaded when needed from the executable file, using the [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa) function.</span></span>

<span data-ttu-id="d5b0e-108">Há duas maneiras de Formatar uma instrução **STRINGTABLE** :</span><span class="sxs-lookup"><span data-stu-id="d5b0e-108">There are two ways to format a **STRINGTABLE** statement:</span></span>

``` syntax
STRINGTABLE  [optional-statements] {stringID string  ...}
```

<span data-ttu-id="d5b0e-109">\- ou –</span><span class="sxs-lookup"><span data-stu-id="d5b0e-109">\- or -</span></span>

``` syntax
STRINGTABLE
  [optional-statements]
BEGIN
stringID string
. . .
END
```

## <a name="parameters"></a><span data-ttu-id="d5b0e-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5b0e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5b0e-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*instruções opcionais*</span><span class="sxs-lookup"><span data-stu-id="d5b0e-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="d5b0e-112">Esse parâmetro pode ser zero ou mais das instruções a seguir.</span><span class="sxs-lookup"><span data-stu-id="d5b0e-112">This parameter can be zero or more of the following statements.</span></span>



| <span data-ttu-id="d5b0e-113">Instrução</span><span class="sxs-lookup"><span data-stu-id="d5b0e-113">Statement</span></span>                                                        | <span data-ttu-id="d5b0e-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="d5b0e-114">Description</span></span>                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5b0e-115">[**Características**](characteristics-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="d5b0e-115">[**CHARACTERISTICS**](characteristics-statement.md) *dword*</span></span>     | <span data-ttu-id="d5b0e-116">Informações definidas pelo usuário sobre um recurso que pode ser usado por ferramentas que lêem e gravam arquivos de recursos.</span><span class="sxs-lookup"><span data-stu-id="d5b0e-116">User-defined information about a resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="d5b0e-117">Para obter mais informações, consulte [**características**](characteristics-statement.md).</span><span class="sxs-lookup"><span data-stu-id="d5b0e-117">For more information, see [**CHARACTERISTICS**](characteristics-statement.md).</span></span> |
| <span data-ttu-id="d5b0e-118">[](language-statement.md) *Idioma* do idioma, *subidioma*</span><span class="sxs-lookup"><span data-stu-id="d5b0e-118">[**LANGUAGE**](language-statement.md) *language*, *sublanguage*</span></span> | <span data-ttu-id="d5b0e-119">Especifica o idioma do recurso.</span><span class="sxs-lookup"><span data-stu-id="d5b0e-119">Specifies the language for the resource.</span></span> <span data-ttu-id="d5b0e-120">Para obter mais informações, consulte [**Language**](language-statement.md).</span><span class="sxs-lookup"><span data-stu-id="d5b0e-120">For more information, see [**LANGUAGE**](language-statement.md).</span></span>                                                                              |
| <span data-ttu-id="d5b0e-121">[](version-statement.md) *DWORD* da versão</span><span class="sxs-lookup"><span data-stu-id="d5b0e-121">[**VERSION**](version-statement.md) *dword*</span></span>                     | <span data-ttu-id="d5b0e-122">Número de versão definido pelo usuário para o recurso que pode ser usado por ferramentas que lêem e gravam arquivos de recursos.</span><span class="sxs-lookup"><span data-stu-id="d5b0e-122">User-defined version number for the resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="d5b0e-123">Para obter mais informações, consulte [**versão**](version-statement.md).</span><span class="sxs-lookup"><span data-stu-id="d5b0e-123">For more information, see [**VERSION**](version-statement.md).</span></span>              |



 

</dd> <dt>

<span data-ttu-id="d5b0e-124"><span id="stringID"></span><span id="stringid"></span><span id="STRINGID"></span>*stringID*</span><span class="sxs-lookup"><span data-stu-id="d5b0e-124"><span id="stringID"></span><span id="stringid"></span><span id="STRINGID"></span>*stringID*</span></span>
</dt> <dd>

<span data-ttu-id="d5b0e-125">Inteiro de 16 bits sem sinal que identifica o recurso.</span><span class="sxs-lookup"><span data-stu-id="d5b0e-125">Unsigned 16-bit integer that identifies the resource.</span></span>

</dd> <dt>

<span data-ttu-id="d5b0e-126"><span id="string"></span><span id="STRING"></span>*Strings*</span><span class="sxs-lookup"><span data-stu-id="d5b0e-126"><span id="string"></span><span id="STRING"></span>*string*</span></span>
</dt> <dd>

<span data-ttu-id="d5b0e-127">Uma ou mais cadeias de caracteres, entre aspas.</span><span class="sxs-lookup"><span data-stu-id="d5b0e-127">One or more strings, enclosed in quotation marks.</span></span> <span data-ttu-id="d5b0e-128">A cadeia de caracteres não deve ter mais de 4097 caracteres e deve ocupar uma única linha no arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="d5b0e-128">The string must be no longer than 4097 characters and must occupy a single line in the source file.</span></span> <span data-ttu-id="d5b0e-129">Para adicionar um retorno de carro à cadeia de caracteres, use esta sequência de caracteres: \\ 012.</span><span class="sxs-lookup"><span data-stu-id="d5b0e-129">To add a carriage return to the string, use this character sequence: \\012.</span></span> <span data-ttu-id="d5b0e-130">Por exemplo, "linha um \\ 012Line dois" define uma cadeia de caracteres que é exibida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="d5b0e-130">For example, "Line one\\012Line two" defines a string that is displayed as follows:</span></span>

``` syntax
Line one
Line two
```

<span data-ttu-id="d5b0e-131">Para inserir aspas na cadeia de caracteres, use a seguinte sequência: "".</span><span class="sxs-lookup"><span data-stu-id="d5b0e-131">To embed quotes in the string, use the following sequence: "".</span></span> <span data-ttu-id="d5b0e-132">Por exemplo, "" "linha três" "" define uma cadeia de caracteres que é exibida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="d5b0e-132">For example, """Line three""" defines a string that is displayed as follows:</span></span>

``` syntax
"Line three"
```

<span data-ttu-id="d5b0e-133">Para codificar caracteres Unicode, use um "L" seguido dos caracteres Unicode entre aspas.</span><span class="sxs-lookup"><span data-stu-id="d5b0e-133">To encode Unicode characters, use an "L" followed by the Unicode characters enclosed by quotes.</span></span> <span data-ttu-id="d5b0e-134">Consulte a seção de exemplos para obter um exemplo.</span><span class="sxs-lookup"><span data-stu-id="d5b0e-134">See the Examples section for an example.</span></span>

<span data-ttu-id="d5b0e-135">O compilador de recurso também dá suporte a continuaçãos de linha na *cadeia de caracteres*.</span><span class="sxs-lookup"><span data-stu-id="d5b0e-135">The resource compiler also supports line continuations in *string*.</span></span> <span data-ttu-id="d5b0e-136">Consulte a seção de exemplos para obter um exemplo.</span><span class="sxs-lookup"><span data-stu-id="d5b0e-136">See the Examples section for an example.</span></span>

</dd> </dl>

<span data-ttu-id="d5b0e-137">Alguns atributos também têm suporte para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="d5b0e-137">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="d5b0e-138">Para obter mais informações, consulte [atributos de recursos comuns](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="d5b0e-138">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d5b0e-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5b0e-139">Remarks</span></span>

<span data-ttu-id="d5b0e-140">O RC aloca 16 cadeias de caracteres por seção e usa o valor do identificador para determinar qual seção deve conter a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d5b0e-140">RC allocates 16 strings per section and uses the identifier value to determine which section is to contain the string.</span></span> <span data-ttu-id="d5b0e-141">Cadeias de caracteres cujos identificadores diferem apenas nos quatro bits inferiores são colocados na mesma seção.</span><span class="sxs-lookup"><span data-stu-id="d5b0e-141">Strings whose identifiers differ only in the bottom 4 bits are placed in the same section.</span></span> <span data-ttu-id="d5b0e-142">Para obter mais informações, consulte [Q196774](https://support.microsoft.com/kb/196774).</span><span class="sxs-lookup"><span data-stu-id="d5b0e-142">For more information, see [Q196774](https://support.microsoft.com/kb/196774).</span></span>

## <a name="examples"></a><span data-ttu-id="d5b0e-143">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d5b0e-143">Examples</span></span>

<span data-ttu-id="d5b0e-144">O exemplo a seguir demonstra o uso da instrução **STRINGTABLE** para exibir cadeias de caracteres ASCII:</span><span class="sxs-lookup"><span data-stu-id="d5b0e-144">The following example demonstrates the use of the **STRINGTABLE** statement to display ASCII strings:</span></span>

``` syntax
#define IDS_HELLO    1
#define IDS_GOODBYE  2

STRINGTABLE
{
    IDS_HELLO,   "Hello"
    IDS_GOODBYE, "Goodbye"
} 
```

<span data-ttu-id="d5b0e-145">O exemplo a seguir mostra como codificar caracteres Unicode:</span><span class="sxs-lookup"><span data-stu-id="d5b0e-145">The following example shows how to encode Unicode characters:</span></span>

``` syntax
STRINGTABLE
BEGINIDS_CHINESESTRING L"\x5e2e\x52a9"
IDS_RUSSIANSTRING L"\x0421\x043f\x0440\x0430\x0432\x043a\x0430"
IDS_ARABICSTRING L"\x062a\x0639\x0644\x064a\x0645\x0627\x062a"
END
```

<span data-ttu-id="d5b0e-146">O exemplo a seguir mostra cadeias de caracteres com ASCII e Unicode.</span><span class="sxs-lookup"><span data-stu-id="d5b0e-146">The following example shows strings with both ASCII and Unicode.</span></span> <span data-ttu-id="d5b0e-147">Observe que as cadeias de caracteres sem o "L" inicial usam o formato de escape de 2 dígitos:</span><span class="sxs-lookup"><span data-stu-id="d5b0e-147">Note that strings without the initial "L" use the 2-digit escape format:</span></span>

``` syntax
STRINGTABLE
BEGIN
IDS_1 L"5\x00BC-Inch Floppy Disk"
IDS_1a "5\xBC-Inch Floppy Disk"
IDS_2 L"Don't confuse \x2229 (intersection) with \x222A (union)"
IDS_3 "Copyright \xA92001"
IDS_3a L"Copyright \x00a92001"
END
```

<span data-ttu-id="d5b0e-148">O exemplo a seguir mostra como as continuaçãos de linha podem ser usadas:</span><span class="sxs-lookup"><span data-stu-id="d5b0e-148">The following example shows how line continuations can be used:</span></span>

``` syntax
STRINGTABLE
BEGIN
IDS_VERYLONGSTRING "blah blah blah blah blah blah \
blah blah blah blah blah blah \
blah blah blah blah blah blah \
blah blah blah blah blah blah"
END
```

## <a name="see-also"></a><span data-ttu-id="d5b0e-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5b0e-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5b0e-150">**Cadeia de caracteres LoadString**</span><span class="sxs-lookup"><span data-stu-id="d5b0e-150">**LoadString**</span></span>](/windows/win32/api/winuser/nf-winuser-loadstringa)
</dt> <dt>

[<span data-ttu-id="d5b0e-151">**ACELERADORES**</span><span class="sxs-lookup"><span data-stu-id="d5b0e-151">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="d5b0e-152">**CARACTERÍSTICAS**</span><span class="sxs-lookup"><span data-stu-id="d5b0e-152">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="d5b0e-153">**IDIOMA**</span><span class="sxs-lookup"><span data-stu-id="d5b0e-153">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="d5b0e-154">**ADICIONARMENU**</span><span class="sxs-lookup"><span data-stu-id="d5b0e-154">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="d5b0e-155">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="d5b0e-155">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="d5b0e-156">**Versão**</span><span class="sxs-lookup"><span data-stu-id="d5b0e-156">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 
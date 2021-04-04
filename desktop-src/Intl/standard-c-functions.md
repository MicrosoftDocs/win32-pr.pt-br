---
description: As bibliotecas de tempo de execução C padrão contêm versões Unicode UTF-16 (caracteres largos) de funções de cadeia de caracteres que podem ser usadas com as versões Unicode e orientadas a bytes das funções de cadeia de caracteres que podem ser usadas com caracteres de SBCS (conjuntos de caracteres de byte único). O tipo de dados Unicode WCHAR é compatível com o tipo de dados WCHAR \_ t no ANSI C e permite o acesso às funções de cadeia de caracteres Unicode. As versões Unicode das funções começam com as letras &\# 0034; wcs&\# 0034; (ou às vezes &\# 0034; \_ WCS&\# 0034;). O tipo de dados CHAR usado para páginas de código é compatível com o caractere de tipo de dados character no ANSI C, para permitir o acesso às funções de cadeia de caracteres. As versões de caracteres das funções começam com as letras &\# 0034; str&\# 0034;. Também há versões especiais para conjuntos de caracteres de dois bytes (DBCS) que começam com as letras &\# 0034; \_ MBS&\# 0034;.
ms.assetid: a86626c1-7f90-4924-bfdd-384729bd0cc5
title: Funções padrão C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6247b3707f96908ef16d887462ba06573fd8dd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837332"
---
# <a name="standard-c-functions"></a><span data-ttu-id="75727-108">Funções padrão C</span><span class="sxs-lookup"><span data-stu-id="75727-108">Standard C Functions</span></span>

<span data-ttu-id="75727-109">As bibliotecas de tempo de execução C padrão contêm versões Unicode UTF-16 (caracteres largos) de funções de cadeia de caracteres que podem ser usadas com as versões [Unicode](unicode.md) e orientadas a bytes das funções de cadeia de caracteres que podem ser usadas com caracteres de SBCS ( [conjuntos de caracteres de byte único](single-byte-character-sets.md) ).</span><span class="sxs-lookup"><span data-stu-id="75727-109">The standard C runtime libraries contain both Unicode UTF-16 (wide character) versions of string functions that can be used with [Unicode](unicode.md) and byte-oriented versions of string functions that can be used with characters from [single-byte character sets](single-byte-character-sets.md) (SBCSs).</span></span> <span data-ttu-id="75727-110">O tipo de dados Unicode WCHAR é compatível com o tipo de dados WCHAR \_ t no ANSI C e permite o acesso às funções de cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="75727-110">The Unicode data type WCHAR is compatible with the data type wchar\_t in ANSI C, and allows access to the Unicode string functions.</span></span> <span data-ttu-id="75727-111">As versões Unicode das funções começam com as letras "WCS" (ou, às vezes, " \_ WCS").</span><span class="sxs-lookup"><span data-stu-id="75727-111">The Unicode versions of the functions start with the letters "wcs" (or sometimes "\_wcs").</span></span> <span data-ttu-id="75727-112">O tipo de dados CHAR usado para páginas de código é compatível com o caractere de tipo de dados character no ANSI C, para permitir o acesso às funções de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="75727-112">The data type CHAR used for code pages is compatible with the character data type char in ANSI C, to allow access to the character string functions.</span></span> <span data-ttu-id="75727-113">As versões de caracteres das funções começam com as letras "Str".</span><span class="sxs-lookup"><span data-stu-id="75727-113">The character versions of the functions start with the letters "str".</span></span> <span data-ttu-id="75727-114">Também há versões especiais para [conjuntos de caracteres de byte duplo](double-byte-character-sets.md) (DBCS) que começam com as letras " \_ MBS".</span><span class="sxs-lookup"><span data-stu-id="75727-114">There are also special versions for [double-byte character sets](double-byte-character-sets.md) (DBCSs) that start with the letters "\_mbs".</span></span>

<span data-ttu-id="75727-115">As bibliotecas de tempo de execução C padrão incluem funções genéricas para todas as funções de cadeia de caracteres C padrão.</span><span class="sxs-lookup"><span data-stu-id="75727-115">The standard C runtime libraries include generic functions for all standard C string functions.</span></span> <span data-ttu-id="75727-116">Eles começam com " \_ TCS" e são listados no arquivo de cabeçalho TCHAR. h.</span><span class="sxs-lookup"><span data-stu-id="75727-116">They start with "\_tcs" and are listed in the Tchar.h header file.</span></span> <span data-ttu-id="75727-117">Essas funções usam o tipo de dados TCHAR genérico.</span><span class="sxs-lookup"><span data-stu-id="75727-117">These functions use the generic TCHAR data type.</span></span>

<span data-ttu-id="75727-118">Um aplicativo deve adicionar as seguintes linhas para usar as funções genéricas e compilar para Unicode.</span><span class="sxs-lookup"><span data-stu-id="75727-118">An application must add the following lines to use the generic functions and compile for Unicode.</span></span>


```C++
#define _UNICODE

#include <tchar.h>
#include <wchar.h>
```



<span data-ttu-id="75727-119">Observe que os arquivos TCHAR. h e WCHAR. h são necessários e que o sublinhado à esquerda na \_ variável Unicode também é necessário.</span><span class="sxs-lookup"><span data-stu-id="75727-119">Note that both the Tchar.h and Wchar.h files are required, and that the leading underscore on the \_UNICODE variable is also required.</span></span> <span data-ttu-id="75727-120">Esse nomenclatura é específico para a biblioteca C padrão.</span><span class="sxs-lookup"><span data-stu-id="75727-120">This nomenclature is specific to the standard C library.</span></span> <span data-ttu-id="75727-121">O "UNICODE" renderizado sem o sublinhado é para os tempos de execução do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="75727-121">"UNICODE" rendered without the underscore is for the Microsoft Windows runtimes.</span></span>

<span data-ttu-id="75727-122">As funções [wcstombs](/cpp/c-runtime-library/reference/wcstombs-wcstombs-l) e [mbstowcs](/cpp/c-runtime-library/reference/mbstowcs-s-mbstowcs-s-l) podem converter do conjunto de caracteres com suporte da biblioteca C padrão para Unicode e back, com algumas limitações.</span><span class="sxs-lookup"><span data-stu-id="75727-122">The [wcstombs](/cpp/c-runtime-library/reference/wcstombs-wcstombs-l) and [mbstowcs](/cpp/c-runtime-library/reference/mbstowcs-s-mbstowcs-s-l) functions can convert from the character set supported by the standard C library to Unicode and back, with some limitations.</span></span> <span data-ttu-id="75727-123">Para obter mais informações sobre a conversão de cadeias de caracteres de e para Unicode, consulte [conversão entre tipos de cadeia](translation-between-string-types.md).</span><span class="sxs-lookup"><span data-stu-id="75727-123">For more information about translating strings to and from Unicode, see [Translation Between String Types](translation-between-string-types.md).</span></span>

<span data-ttu-id="75727-124">A função [printf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) definida em TCHAR. h dá suporte às mesmas especificações de formato que as funções de impressão strsafe. h, por exemplo, [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa).</span><span class="sxs-lookup"><span data-stu-id="75727-124">The [printf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) function defined in Tchar.h supports the same format specifications as the Strsafe.h print functions, for example [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa).</span></span> <span data-ttu-id="75727-125">Da mesma forma, TCHAR. h define uma função [wprintf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) , na qual a cadeia de caracteres de formato é uma cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="75727-125">Similarly, Tchar.h defines a [wprintf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) function, in which the format string itself is a Unicode string.</span></span>

> [!Caution]  
> <span data-ttu-id="75727-126">A manipulação de buffer insatisfatório é incomplicada em muitos problemas de segurança que envolvem saturações de buffer.</span><span class="sxs-lookup"><span data-stu-id="75727-126">Poor buffer handling is implicated in many security issues that involve buffer overruns.</span></span> <span data-ttu-id="75727-127">Consulte a [referência de strsafe. h](../menurc/strsafe-ovw.md).</span><span class="sxs-lookup"><span data-stu-id="75727-127">See [Strsafe.h Reference](../menurc/strsafe-ovw.md).</span></span> <span data-ttu-id="75727-128">As funções definidas em strsafe. h fornecem processamento adicional para a manipulação de buffer adequada em seu código.</span><span class="sxs-lookup"><span data-stu-id="75727-128">The functions defined in Strsafe.h provide additional processing for proper buffer handling in your code.</span></span> <span data-ttu-id="75727-129">Eles se destinam a substituir suas contrapartes C/C++ internas, bem como implementações específicas do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="75727-129">They are intended to replace their built-in C/C++ counterparts as well as specific Microsoft Windows implementations.</span></span> <span data-ttu-id="75727-130">Para obter mais informações, consulte [Considerações sobre segurança: recursos internacionais](security-considerations--international-features.md).</span><span class="sxs-lookup"><span data-stu-id="75727-130">For more information, see [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="75727-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="75727-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75727-132">Unicode na API do Windows</span><span class="sxs-lookup"><span data-stu-id="75727-132">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> </dl>

 

 

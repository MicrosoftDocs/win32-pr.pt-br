---
description: A sintaxe de consulta avançada (AQS) é a sintaxe de consulta padrão usada pelo Windows Search para consultar o índice e refinar e restringir os parâmetros de pesquisa.
ms.assetid: 76e33903-d063-48c0-9afe-912c3daa8237
title: Usando a sintaxe de consulta avançada programaticamente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8fa69a5a5ccaa37b84a10abd367e5a29656455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105802124"
---
# <a name="using-advanced-query-syntax-programmatically"></a><span data-ttu-id="9ea85-103">Usando a sintaxe de consulta avançada programaticamente</span><span class="sxs-lookup"><span data-stu-id="9ea85-103">Using Advanced Query Syntax Programmatically</span></span>

<span data-ttu-id="9ea85-104">A sintaxe de consulta avançada (AQS) é a sintaxe de consulta padrão usada pelo Windows Search para consultar o índice e refinar e restringir os parâmetros de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="9ea85-104">Advanced Query Syntax (AQS) is the default query syntax used by Windows Search to query the index and to refine and narrow search parameters.</span></span> <span data-ttu-id="9ea85-105">O AQS é empregado por desenvolvedores para criar consultas programaticamente (e por usuários para restringir seus parâmetros de pesquisa).</span><span class="sxs-lookup"><span data-stu-id="9ea85-105">AQS is employed by developers to build queries programmatically (and by users to narrow their search parameters).</span></span> <span data-ttu-id="9ea85-106">O AQS canônico foi introduzido no Windows 7 e deve ser usado no Windows 7 e posterior para gerar programaticamente consultas AQS.</span><span class="sxs-lookup"><span data-stu-id="9ea85-106">Canonical AQS was introduced in Windows 7 and must be used in Windows 7 and later to programmatically generate AQS queries.</span></span>

<span data-ttu-id="9ea85-107">Este tópico é organizado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="9ea85-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="9ea85-108">Sobre a sintaxe de consulta avançada</span><span class="sxs-lookup"><span data-stu-id="9ea85-108">About Advanced Query Syntax</span></span>](#about-advanced-query-syntax)
    -   [<span data-ttu-id="9ea85-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9ea85-109">Examples</span></span>](#examples)
    -   [<span data-ttu-id="9ea85-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9ea85-110">Properties</span></span>](#properties)
-   [<span data-ttu-id="9ea85-111">Uso de palavra-chave em idiomas locais</span><span class="sxs-lookup"><span data-stu-id="9ea85-111">Keyword Use in Local Languages</span></span>](#keyword-use-in-local-languages)
-   [<span data-ttu-id="9ea85-112">Sintaxe de consulta avançada canônica no Windows 7</span><span class="sxs-lookup"><span data-stu-id="9ea85-112">Canonical Advanced Query Syntax in Windows 7</span></span>](#canonical-advanced-query-syntax-in-windows-7)
    -   [<span data-ttu-id="9ea85-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9ea85-113">Examples</span></span>](#examples)
    -   [<span data-ttu-id="9ea85-114">Operadores de consulta</span><span class="sxs-lookup"><span data-stu-id="9ea85-114">Query Operators</span></span>](#query-operators)
    -   [<span data-ttu-id="9ea85-115">Valores de consulta</span><span class="sxs-lookup"><span data-stu-id="9ea85-115">Query Values</span></span>](#query-values)
-   [<span data-ttu-id="9ea85-116">Restrições de escopo</span><span class="sxs-lookup"><span data-stu-id="9ea85-116">Scope Restrictions</span></span>](#scope-restrictions)
-   [<span data-ttu-id="9ea85-117">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="9ea85-117">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="9ea85-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9ea85-118">Related topics</span></span>](#related-topics)

## <a name="about-advanced-query-syntax"></a><span data-ttu-id="9ea85-119">Sobre a sintaxe de consulta avançada</span><span class="sxs-lookup"><span data-stu-id="9ea85-119">About Advanced Query Syntax</span></span>

<span data-ttu-id="9ea85-120">Uma consulta consiste em consultas básicas conectadas com AND, OR e NOT, conforme mostrado na seguinte sintaxe de exemplo:</span><span class="sxs-lookup"><span data-stu-id="9ea85-120">A query consists of basic queries connected with AND, OR, and NOT, as shown in the following example syntax:</span></span>

``` syntax
<query> ::=
     <basic query>
| ( <query> )
| <query> AND <query>  
| <query> <query>    // Same as <query> AND <query>
| <query> OR <query> 
| NOT <query>
```

> [!Note]  
> <span data-ttu-id="9ea85-121">AQS não diferencia maiúsculas de minúsculas, com exceção de AND, OR e NOT, que deve estar em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="9ea85-121">AQS is not case sensitive, with the exception of AND, OR, and NOT, which must be in all uppercase.</span></span>

 

<span data-ttu-id="9ea85-122">Se uma consulta tiver dois ou mais usos de e ou ou, elas serão vinculadas da esquerda para a direita, independentemente de ser e ou ou.</span><span class="sxs-lookup"><span data-stu-id="9ea85-122">If a query has two or more uses of AND or OR, they will bind from left to right, regardless of whether it is AND or OR.</span></span> <span data-ttu-id="9ea85-123">Ou seja, a consulta, "Apple e pêra ou Black", será interpretada como se fosse escrita como "(Apple e pêra) ou Black", e a consulta, "Apple ou pêra e Black", será interpretada como se fosse escrita como "(Apple ou pêra) e Black".</span><span class="sxs-lookup"><span data-stu-id="9ea85-123">That is, the query, "apple AND pear OR plum" will be interpreted as if it were written as "(apple AND pear) OR plum", and the query, "apple OR pear AND plum", will be interpreted as if it were written as "(apple OR pear) AND plum".</span></span> <span data-ttu-id="9ea85-124">Portanto, se um documento contiver a palavra Black, mas nem a Apple, nem a pera, a primeira consulta a retornará, mas a segunda consulta não será.</span><span class="sxs-lookup"><span data-stu-id="9ea85-124">So if a document contains the word plum but neither apple, nor pear, the first query will return it but the second query will not.</span></span> <span data-ttu-id="9ea85-125">Portanto, recomendamos que você use parênteses explícitos para qualquer consulta que combine e e ou para evitar erros ou interpretações indesejadas.</span><span class="sxs-lookup"><span data-stu-id="9ea85-125">Hence, we recommend that you use explicit parentheses for any query that mixes AND and OR to avoid mistakes or misinterpretations.</span></span>

<span data-ttu-id="9ea85-126">Uma consulta básica procura itens que atendam a uma restrição sobre uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="9ea85-126">A basic query searches for items that satisfy a restriction over a property.</span></span> <span data-ttu-id="9ea85-127">A única parte necessária de uma consulta básica é a restrição ou o valor de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="9ea85-127">The only required portion of a basic query is the restriction or search value.</span></span> <span data-ttu-id="9ea85-128">Se você não especificar uma propriedade, o Windows Search pesquisará todas as propriedades.</span><span class="sxs-lookup"><span data-stu-id="9ea85-128">If you do not specify a property, Windows Search searches all properties.</span></span> <span data-ttu-id="9ea85-129"><restr> representa a restrição de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="9ea85-129"><restr> represents the search restriction.</span></span>

<span data-ttu-id="9ea85-130">Os seguintes formulários para uma consulta básica são válidos:</span><span class="sxs-lookup"><span data-stu-id="9ea85-130">The following forms for a basic query are valid:</span></span>

``` syntax
<basic query> ::=
     <prop>:<basic restr>
| <restr>
```

<span data-ttu-id="9ea85-131">Uma propriedade é designada por uma palavra-chave como autor ou tamanho, ou por um nome de propriedade canônica, como [System. DateModified](../properties/props-system-datemodified.md).</span><span class="sxs-lookup"><span data-stu-id="9ea85-131">A property is designated by a keyword such as author or size, or by a canonical property name such as [System.DateModified](../properties/props-system-datemodified.md).</span></span> <span data-ttu-id="9ea85-132">Os formulários válidos para uma propriedade são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="9ea85-132">Valid forms for a property are as follows:</span></span>

``` syntax
<prop> ::= 
     <canonical property name>
| <property label in UI language>
```

<span data-ttu-id="9ea85-133">Um operador indica uma operação como < ou =.</span><span class="sxs-lookup"><span data-stu-id="9ea85-133">An operator indicates an operation such as < or =.</span></span> <span data-ttu-id="9ea85-134">Para obter uma lista de operadores válidos, consulte a seção operadores de consulta mais adiante neste tópico.</span><span class="sxs-lookup"><span data-stu-id="9ea85-134">For a list of valid operators, see the Query Operators section later in this topic.</span></span>

<span data-ttu-id="9ea85-135">Uma restrição básica é uma restrição simples em uma propriedade que pode ser gravada sem parênteses:</span><span class="sxs-lookup"><span data-stu-id="9ea85-135">A basic restriction is a simple restriction on a property that can be written without parentheses:</span></span>

``` syntax
<basic restr> ::=
     <value>
| <op><value>
| NOT <basic restr>
| ( <restr> )
```

<span data-ttu-id="9ea85-136">Uma restrição é um valor de pesquisa, como um valor numérico ou um valor de cadeia de caracteres, opcionalmente com um operador.</span><span class="sxs-lookup"><span data-stu-id="9ea85-136">A restriction is a search value such as a number value or string value, optionally with an operator.</span></span> <span data-ttu-id="9ea85-137">Os formulários válidos para uma restrição são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="9ea85-137">Valid forms for a restriction are as follows:</span></span>

``` syntax
<restr> ::=
    <basic restr>
| <restr> AND <restr>
| <restr> <restr>      // Same as <restr> AND <restr>
| <restr> OR <restr>
```

<span data-ttu-id="9ea85-138">Se você não especificar um operador, o Windows Search escolherá o operador mais apropriado para sua consulta:</span><span class="sxs-lookup"><span data-stu-id="9ea85-138">If you do not specify an operator, Windows Search chooses the most appropriate operator for your query:</span></span>

-   <span data-ttu-id="9ea85-139">Para uma propriedade de cadeia de caracteres, o operador de COP \_ Word \_ STARTSWITH $< é assumido.</span><span class="sxs-lookup"><span data-stu-id="9ea85-139">For a string property, the COP\_WORD\_STARTSWITH $< operator is assumed.</span></span>
-   <span data-ttu-id="9ea85-140">Para todas as outras propriedades, o \_ operador COP equal = é assumido.</span><span class="sxs-lookup"><span data-stu-id="9ea85-140">For all other properties, the COP\_EQUAL = operator is assumed.</span></span>

<span data-ttu-id="9ea85-141">Para o uso programático de AQS, é recomendável que você sempre tenha um operador explícito.</span><span class="sxs-lookup"><span data-stu-id="9ea85-141">For the programmatic use of AQS, we recommend that you always have an explicit operator.</span></span> <span data-ttu-id="9ea85-142">A forma válida para pesquisar um valor ou intervalo de valores simples é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="9ea85-142">The valid form for searching a simple value or value range is as follows:</span></span>

``` syntax
<value> ::=
    <simplevalue>
| <simplevalue> .. <simplevalue>
```

<span data-ttu-id="9ea85-143">Um valor simples pode consistir em qualquer um dos seguintes tipos:</span><span class="sxs-lookup"><span data-stu-id="9ea85-143">A simple value can consist of any of the following types:</span></span>

``` syntax
<simplevalue> ::=
  []         // No value, or a null value
| <word>     // A sequence of characters without whitespace
| <number>   // An integer or a floating point number
| <datetime> // A relative date, or an absolute date and/or time
| <Boolean>
| "..."      // A phrase
| <enumeration range>
```

### <a name="examples"></a><span data-ttu-id="9ea85-144">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9ea85-144">Examples</span></span>

<span data-ttu-id="9ea85-145">Uma consulta que pesquisa um documento que contém a fase "último trimestre", criada por Theresa ou Lee, e que foi salva na pasta mydocs, combina três consultas básicas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="9ea85-145">A query that searches for a document containing the phase "last quarter," authored by Theresa or Lee, and that was saved to the folder MyDocs, combines three basic queries as follows:</span></span>

``` syntax
"last quarter" author:(theresa OR lee) folder:MyDocs
```

<span data-ttu-id="9ea85-146">As três consultas básicas são:</span><span class="sxs-lookup"><span data-stu-id="9ea85-146">The three basic queries are:</span></span>

-   <span data-ttu-id="9ea85-147">"último trimestre"</span><span class="sxs-lookup"><span data-stu-id="9ea85-147">"last quarter"</span></span>
-   <span data-ttu-id="9ea85-148">Autor: (Theresa ou Lee)</span><span class="sxs-lookup"><span data-stu-id="9ea85-148">author:(theresa OR lee)</span></span>
-   <span data-ttu-id="9ea85-149">pasta: mydocs</span><span class="sxs-lookup"><span data-stu-id="9ea85-149">folder:MyDocs</span></span>

<span data-ttu-id="9ea85-150">Uma consulta básica que usa sintaxe canônica é:</span><span class="sxs-lookup"><span data-stu-id="9ea85-150">A basic query that uses canonical syntax is:</span></span>

``` syntax
System.Size:>1kb
```

### <a name="properties"></a><span data-ttu-id="9ea85-151">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9ea85-151">Properties</span></span>

<span data-ttu-id="9ea85-152">As propriedades são referenciadas por uma palavra-chave, que pode ser um nome de propriedade canônica no Windows 7 e posterior.</span><span class="sxs-lookup"><span data-stu-id="9ea85-152">Properties are referred to by a keyword, which can be a canonical property name in Windows 7 and later.</span></span> <span data-ttu-id="9ea85-153">AQS na interface do usuário do Windows pode usar o rótulo em vez do nome da propriedade canônica, como autor, em vez de [System. Author](../properties/props-system-author.md).</span><span class="sxs-lookup"><span data-stu-id="9ea85-153">AQS in the Windows UI can use the label instead of the canonical property name, such as author instead of [System.Author](../properties/props-system-author.md).</span></span> <span data-ttu-id="9ea85-154">No Windows Vista e versões anteriores, era possível usar os rótulos em inglês, independentemente do idioma da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="9ea85-154">In Windows Vista and earlier it was possible to use English labels regardless of the UI language.</span></span> <span data-ttu-id="9ea85-155">No Windows 7 e posterior, o Windows Search reconhece palavras-chave somente no idioma da interface do usuário padrão atual.</span><span class="sxs-lookup"><span data-stu-id="9ea85-155">In Windows 7 and later, Windows Search recognizes keywords in the current default UI language only.</span></span>

### <a name="support-for-custom-properties"></a><span data-ttu-id="9ea85-156">Suporte para propriedades personalizadas</span><span class="sxs-lookup"><span data-stu-id="9ea85-156">Support for Custom Properties</span></span>

<span data-ttu-id="9ea85-157">No Windows Vista e versões anteriores, as propriedades personalizadas não estavam disponíveis em AQS.</span><span class="sxs-lookup"><span data-stu-id="9ea85-157">In Windows Vista and earlier, custom properties were not available in AQS.</span></span> <span data-ttu-id="9ea85-158">No Windows 7 e posterior, o AQS funciona com propriedades personalizadas registradas com o sistema de propriedades.</span><span class="sxs-lookup"><span data-stu-id="9ea85-158">In Windows 7 and later, AQS works with custom properties that are registered with the property system.</span></span> <span data-ttu-id="9ea85-159">Para obter mais informações sobre como criar propriedades personalizadas, consulte [sistema de propriedades](../properties/building-property-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="9ea85-159">For more information on creating custom properties, see [Property System](../properties/building-property-handlers.md).</span></span>

### <a name="datetime-properties-in-windows-8"></a><span data-ttu-id="9ea85-160">Propriedades de DateTime no Windows 8</span><span class="sxs-lookup"><span data-stu-id="9ea85-160">DateTime properties in Windows 8</span></span>

<span data-ttu-id="9ea85-161">A partir do Windows 8, as propriedades de DateTime (como [System. DateModified](../properties/props-system-datemodified.md)) dão suporte ao formato canônico de data e hora especificado por [ISO-8601](https://www.w3.org/TR/NOTE-datetime), incluindo, opcionalmente, o fuso horário UTC.</span><span class="sxs-lookup"><span data-stu-id="9ea85-161">As of Windows 8, DateTime properties (like [System.DateModified](../properties/props-system-datemodified.md)) support the canonical date and time format specified by [ISO-8601](https://www.w3.org/TR/NOTE-datetime), optionally including the UTC time zone.</span></span>

-   <span data-ttu-id="9ea85-162">**Windows 8 e anterior, data e hora sem fuso horário UTC:** *aaaa* - *mm* - *ddThh*:*mm*:*SS*</span><span class="sxs-lookup"><span data-stu-id="9ea85-162">**Windows 8 and earlier, date-time without UTC time zone:** *YYYY*-*MM*-*DDThh*:*mm*:*ss*</span></span>

    <span data-ttu-id="9ea85-163">Esse formato especifica uma hora local, independentemente da localidade do usuário ou do sistema.</span><span class="sxs-lookup"><span data-stu-id="9ea85-163">This format specifies a local time, regardless of the user or system locale.</span></span>

-   <span data-ttu-id="9ea85-164">**Windows 8, data e hora com fuso horário UTC:** *yyyy* - *mm* - *ddThh*:*mm*:*ssTZD*</span><span class="sxs-lookup"><span data-stu-id="9ea85-164">**Windows 8, date-time with UTC time zone:** *YYYY*-*MM*-*DDThh*:*mm*:*ssTZD*</span></span>

    <span data-ttu-id="9ea85-165">Este formato especifica uma hora no fuso horário UTC especificado.</span><span class="sxs-lookup"><span data-stu-id="9ea85-165">This format specifies a time at the specified UTC time zone.</span></span>

## <a name="keyword-use-in-local-languages"></a><span data-ttu-id="9ea85-166">Uso de palavra-chave em idiomas locais</span><span class="sxs-lookup"><span data-stu-id="9ea85-166">Keyword Use in Local Languages</span></span>

<span data-ttu-id="9ea85-167">No Windows 7 e versões posteriores, as palavras-chave mnemônicos funcionam apenas no idioma do sistema, como palavras-chave do alemão somente em um sistema operacional alemão e palavras-chave em inglês apenas em um sistema operacional em inglês.</span><span class="sxs-lookup"><span data-stu-id="9ea85-167">In Windows 7 and later, mnemonic keywords work in the system language only, such as German keywords only on a German operating system, and English keywords only on an English operating system.</span></span> <span data-ttu-id="9ea85-168">[System. Author](../properties/props-system-author.md) é uma palavra-chave canônica, e o valor mnemônico para a propriedade System. Author é autor, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="9ea85-168">[System.Author](../properties/props-system-author.md) is a canonical keyword, and the mnemonic value for the System.Author property is Author, for example.</span></span> <span data-ttu-id="9ea85-169">A introdução de palavras-chave canônicas compensa o fato de que as palavras-chave mnemônicos inglesas não são mais reconhecidas universalmente em todos os sistemas operacionais, independentemente da linguagem, como era o caso no Windows Vista e versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="9ea85-169">The introduction of canonical keywords compensates for the fact that English mnemonic keywords are no longer universally recognized on all operating systems regardless of language, as was the case in Windows Vista and earlier.</span></span>

> [!Note]  
> <span data-ttu-id="9ea85-170">No Windows 7 e posterior, o Windows Search reconhece palavras-chave somente no idioma padrão atual e não em inglês, a menos que o inglês seja o padrão atual.</span><span class="sxs-lookup"><span data-stu-id="9ea85-170">In Windows 7 and later, Windows Search recognizes keywords in the current default language only, and not in English unless English is the current default.</span></span> <span data-ttu-id="9ea85-171">Recomendamos que os desenvolvedores sempre usem a sintaxe canônica para que seu aplicativo não tenha problemas de idioma com palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="9ea85-171">We recommend that developers always use canonical syntax so that their application won't have language problems with keywords.</span></span>

 

## <a name="canonical-advanced-query-syntax-in-windows-7"></a><span data-ttu-id="9ea85-172">Sintaxe de consulta avançada canônica no Windows 7</span><span class="sxs-lookup"><span data-stu-id="9ea85-172">Canonical Advanced Query Syntax in Windows 7</span></span>

<span data-ttu-id="9ea85-173">A sintaxe canônica foi introduzida para palavras-chave no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9ea85-173">Canonical syntax was introduced for keywords in Windows 7.</span></span> <span data-ttu-id="9ea85-174">Um exemplo de uma consulta com uma propriedade canônica é `System.Message.FromAddress:=me@microsoft.com` .</span><span class="sxs-lookup"><span data-stu-id="9ea85-174">An example of a query with a canonical property is `System.Message.FromAddress:=me@microsoft.com`.</span></span> <span data-ttu-id="9ea85-175">Ao codificar consultas em aplicativos em execução no Windows 7 e posterior, você deve usar a sintaxe canônica para gerar consultas AQS programaticamente.</span><span class="sxs-lookup"><span data-stu-id="9ea85-175">When coding queries in applications running on Windows 7 and later, you must use canonical syntax to programmatically generate AQS queries.</span></span> <span data-ttu-id="9ea85-176">Se você não usar a sintaxe canônica e seu aplicativo for implantado em uma localidade ou idioma da interface do usuário diferente do idioma no código do aplicativo, suas consultas não serão interpretadas corretamente.</span><span class="sxs-lookup"><span data-stu-id="9ea85-176">If you do not use canonical syntax and your application is deployed in a locale or UI language different from the language in the application code, your queries will not be interpreted correctly.</span></span>

<span data-ttu-id="9ea85-177">As convenções para a sintaxe de palavra-chave canônica são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="9ea85-177">The conventions for canonical keyword syntax are as follows:</span></span>

-   <span data-ttu-id="9ea85-178">A sintaxe canônica de uma propriedade é seu nome canônico, como `System.Photo.LightSource` .</span><span class="sxs-lookup"><span data-stu-id="9ea85-178">The canonical syntax for a property is its canonical name, such as `System.Photo.LightSource`.</span></span> <span data-ttu-id="9ea85-179">Os nomes canônicos não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="9ea85-179">Canonical names are not case sensitive.</span></span>
-   <span data-ttu-id="9ea85-180">A sintaxe canônica para os operadores boolianos consiste nas palavras-chave AND, OR e NOT, em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="9ea85-180">The canonical syntax for the Boolean operators consists of the keywords AND, OR, and NOT, in all uppercase.</span></span>
-   <span data-ttu-id="9ea85-181">Os operadores <, >, = e assim por diante, não são localizados e, portanto, também fazem parte da sintaxe canônica.</span><span class="sxs-lookup"><span data-stu-id="9ea85-181">The operators <, >, =, and so forth, are not localized and are thus also part of the canonical syntax.</span></span>
-   <span data-ttu-id="9ea85-182">Se uma propriedade `P` tiver valores enumerados ou intervalos chamados N ₁ por meio de NK, a sintaxe canônica para o valor ou o intervalo será o nome canônico de P, seguido pelo caractere \# , seguido de N<sub>I</sub>, conforme ilustrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="9ea85-182">If a property `P` has enumerated values or ranges named N₁ through Nₖ, the canonical syntax for the *I* th value or range is the canonical name for P, followed by the character \#, followed by N<sub>I</sub>, as illustrated in the following example:</span></span>
    -   <span data-ttu-id="9ea85-183">`System.Photo.LightSource#Daylight`, `System.Photo.LightSource#StandardA` e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="9ea85-183">`System.Photo.LightSource#Daylight`, `System.Photo.LightSource#StandardA`, and so forth.</span></span>
-   <span data-ttu-id="9ea85-184">Para um tipo de semântica definido T com valores ou intervalos denominados N ₁ por meio de NK, a sintaxe canônica para o valor ou intervalo *é o nome* canônico para T, seguido pelo caractere \# , seguido de N <sub>I</sub>, conforme ilustrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="9ea85-184">For a defined semantic type T with values or ranges named N₁ through Nₖ, the canonical syntax for the *I* th value or range is the canonical name for T, followed by the character \#, followed by N<sub>I</sub>, as illustrated in the following example:</span></span>
    -   `System.Devices.LaunchDeviceStageFromExplorer:=System.StructuredQueryType.Boolean#True`
-   <span data-ttu-id="9ea85-185">Para valores literais como palavras ou frases, a sintaxe canônica é a mesma que a sintaxe regular.</span><span class="sxs-lookup"><span data-stu-id="9ea85-185">For literal values such as words or phrases, the canonical syntax is the same as the regular syntax.</span></span> <span data-ttu-id="9ea85-186">Exemplos de consultas com valores literais em sintaxe canônica:</span><span class="sxs-lookup"><span data-stu-id="9ea85-186">Examples of queries with literal values in canonical syntax are:</span></span>
    -   `System.Author:sanjay`
    -   `System.Keywords:"Animal"`
    -   `System.FileCount:>100`

> [!Note]  
> <span data-ttu-id="9ea85-187">Não há sintaxe canônica para números no Windows 7 e posterior.</span><span class="sxs-lookup"><span data-stu-id="9ea85-187">There is no canonical syntax for numbers in Windows 7 and later.</span></span> <span data-ttu-id="9ea85-188">Como os formatos de ponto flutuante variam entre as localidades, o uso de uma consulta canônica que envolve uma constante de ponto flutuante não é suportado.</span><span class="sxs-lookup"><span data-stu-id="9ea85-188">Because floating point formats vary among locales, the use of a canonical query that involves a floating point constant is not supported.</span></span> <span data-ttu-id="9ea85-189">As constantes de inteiro, por outro lado, podem ser escritas usando apenas dígitos (sem separadores para milhares) e podem ser usadas com segurança em consultas canônicas no Windows 7 e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="9ea85-189">Integer constants, in contrast, can be written using only digits (no separators for thousands) and can be safely used in canonical queries in Windows 7 and later.</span></span>

 

### <a name="examples"></a><span data-ttu-id="9ea85-190">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9ea85-190">Examples</span></span>

<span data-ttu-id="9ea85-191">A tabela a seguir mostra alguns exemplos de propriedades canônicas e a sintaxe para usá-las.</span><span class="sxs-lookup"><span data-stu-id="9ea85-191">The following table shows some examples of canonical properties and the syntax for using them.</span></span>



| <span data-ttu-id="9ea85-192">Tipo de propriedade canônica</span><span class="sxs-lookup"><span data-stu-id="9ea85-192">Type of canonical property</span></span> | <span data-ttu-id="9ea85-193">Exemplo</span><span class="sxs-lookup"><span data-stu-id="9ea85-193">Example</span></span>                                                                                     | <span data-ttu-id="9ea85-194">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ea85-194">Syntax</span></span>                                                                                                                                                                                                                                                  |
|----------------------------|---------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ea85-195">Valor da cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="9ea85-195">String value</span></span>               | [<span data-ttu-id="9ea85-196">System.Author</span><span class="sxs-lookup"><span data-stu-id="9ea85-196">System.Author</span></span>](../properties/props-system-author.md)<br/>    | <span data-ttu-id="9ea85-197">O valor da cadeia de caracteres é procurado na propriedade autor:</span><span class="sxs-lookup"><span data-stu-id="9ea85-197">The string value is searched for in the author property:</span></span> <br/>`System.Author:Jacobs`                                                                                                                                                              |
| <span data-ttu-id="9ea85-198">Intervalo de enumeração</span><span class="sxs-lookup"><span data-stu-id="9ea85-198">Enumeration range</span></span>          | [<span data-ttu-id="9ea85-199">System. Priority</span><span class="sxs-lookup"><span data-stu-id="9ea85-199">System.Priority</span></span>](../properties/props-system-priority.md)             | <span data-ttu-id="9ea85-200">A propriedade Priority pode ter um intervalo de valores numéricos:</span><span class="sxs-lookup"><span data-stu-id="9ea85-200">The priority property can have a numerical value range:</span></span><br/>`System.Priority:System.Priority#High`                                                                                                                                                |
| <span data-ttu-id="9ea85-201">Boolean</span><span class="sxs-lookup"><span data-stu-id="9ea85-201">Boolean</span></span>                    | [<span data-ttu-id="9ea85-202">System. IsDeleted</span><span class="sxs-lookup"><span data-stu-id="9ea85-202">System.IsDeleted</span></span>](../properties/props-system-isdeleted.md)<br/> | <span data-ttu-id="9ea85-203">Valores Boolianos podem ser usados com qualquer propriedade booleana:</span><span class="sxs-lookup"><span data-stu-id="9ea85-203">Boolean values can be used with any Boolean property:</span></span><br/><span data-ttu-id="9ea85-204">`System.IsDeleted:System.StructuredQueryType.Boolean#True` e `System.IsDeleted:System.StructuredQueryType.Boolean#False`</span><span class="sxs-lookup"><span data-stu-id="9ea85-204">`System.IsDeleted:System.StructuredQueryType.Boolean#True`, and `System.IsDeleted:System.StructuredQueryType.Boolean#False`</span></span>                                                             |
| <span data-ttu-id="9ea85-205">Numérico</span><span class="sxs-lookup"><span data-stu-id="9ea85-205">Numerical</span></span>                  | [<span data-ttu-id="9ea85-206">Sistema. tamanho</span><span class="sxs-lookup"><span data-stu-id="9ea85-206">System.Size</span></span>](../properties/props-system-size.md)<br/>      | <span data-ttu-id="9ea85-207">Não é possível gravar com segurança uma consulta canônica que envolve uma constante de ponto flutuante, pois os formatos de ponto flutuante variam entre as localidades.</span><span class="sxs-lookup"><span data-stu-id="9ea85-207">It is not possible to write safely a canonical query that involves a floating point constant, because floating point formats vary among locales.</span></span> <span data-ttu-id="9ea85-208">Os inteiros devem ser escritos sem separadores para milhares.</span><span class="sxs-lookup"><span data-stu-id="9ea85-208">Integers must be written with no separators for thousands.</span></span> <span data-ttu-id="9ea85-209">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="9ea85-209">For example:</span></span><br/>`System.Size:<12345` |



 

<span data-ttu-id="9ea85-210">Para obter mais informações sobre propriedades canônicas e o sistema de propriedades em geral, consulte [Propriedades do sistema](../properties/props.md).</span><span class="sxs-lookup"><span data-stu-id="9ea85-210">For more information about canonical properties and the property system generally, see [System Properties](../properties/props.md).</span></span> <span data-ttu-id="9ea85-211">Como alternativa, consulte os arquivos de cabeçalho públicos.</span><span class="sxs-lookup"><span data-stu-id="9ea85-211">Alternatively, refer to the public header files.</span></span>

### <a name="query-operators"></a><span data-ttu-id="9ea85-212">Operadores de Consulta</span><span class="sxs-lookup"><span data-stu-id="9ea85-212">Query Operators</span></span>

<span data-ttu-id="9ea85-213">Se uma propriedade, p, tiver vários valores para algum item, uma consulta AQS para p: <restr> retornará o item se <restr> for **verdadeira** para pelo menos um dos valores.</span><span class="sxs-lookup"><span data-stu-id="9ea85-213">If a property, p, has multiple values for some item, an AQS query for p:<restr> returns the item if <restr> is **true** for at least one of the values.</span></span> <span data-ttu-id="9ea85-214">( <restr> representa uma restrição.)</span><span class="sxs-lookup"><span data-stu-id="9ea85-214">(<restr> represents a restriction.)</span></span>

<span data-ttu-id="9ea85-215">A sintaxe listada na tabela a seguir consiste em um operador, símbolo de operador, exemplo e descrição de exemplo.</span><span class="sxs-lookup"><span data-stu-id="9ea85-215">The syntax listed in the following table consists of an operator, operator symbol, example and example description.</span></span> <span data-ttu-id="9ea85-216">O operador e o símbolo podem ser usados em qualquer idioma e incluídos em qualquer consulta.</span><span class="sxs-lookup"><span data-stu-id="9ea85-216">The operator and symbol can be used in any language and included in any query.</span></span> <span data-ttu-id="9ea85-217">Não use os operadores de COP \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9ea85-217">Do not use the COP\_IMPLICIT or COP\_APPLICATION\_SPECIFIC operators.</span></span> <span data-ttu-id="9ea85-218">Alguns dos operadores têm símbolos intercambiáveis.</span><span class="sxs-lookup"><span data-stu-id="9ea85-218">Some of the operators have interchangeable symbols.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9ea85-219">Operador</span><span class="sxs-lookup"><span data-stu-id="9ea85-219">Operator</span></span></th>
<th><span data-ttu-id="9ea85-220">Símbolo</span><span class="sxs-lookup"><span data-stu-id="9ea85-220">Symbol</span></span></th>
<th><span data-ttu-id="9ea85-221">Exemplo</span><span class="sxs-lookup"><span data-stu-id="9ea85-221">Example</span></span></th>
<th><span data-ttu-id="9ea85-222">Descrição</span><span class="sxs-lookup"><span data-stu-id="9ea85-222">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9ea85-223">COP_EQUAL</span><span class="sxs-lookup"><span data-stu-id="9ea85-223">COP_EQUAL</span></span></td>
<td>=<br/></td>
<td><span data-ttu-id="9ea85-224">System. FileExtension: = &quot; . txt&quot;</span><span class="sxs-lookup"><span data-stu-id="9ea85-224">System.FileExtension:=&quot;.txt&quot;</span></span><br/></td>
<td><span data-ttu-id="9ea85-225">O valor é String &quot; <em>. txt</em> &quot; .</span><span class="sxs-lookup"><span data-stu-id="9ea85-225">The value is the string &quot;<em>.txt</em>&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ea85-226">COP_NOTEQUAL</span><span class="sxs-lookup"><span data-stu-id="9ea85-226">COP_NOTEQUAL</span></span></td>
<td><span data-ttu-id="9ea85-227">≠</span><span class="sxs-lookup"><span data-stu-id="9ea85-227">≠</span></span><br/> -<br/> &lt;&gt;<br/> <span data-ttu-id="9ea85-228">NOT</span><span class="sxs-lookup"><span data-stu-id="9ea85-228">NOT</span></span><br/> - -<br/></td>
<td><span data-ttu-id="9ea85-229">System. Kind: imagem ≠</span><span class="sxs-lookup"><span data-stu-id="9ea85-229">System.Kind:≠picture</span></span><br/> <span data-ttu-id="9ea85-230">System. Photo. DateTaken:-[] ¹</span><span class="sxs-lookup"><span data-stu-id="9ea85-230">System.Photo.DateTaken:-[]¹</span></span><br/> <span data-ttu-id="9ea85-231">Sistema. Kind: &lt; &gt; imagem</span><span class="sxs-lookup"><span data-stu-id="9ea85-231">System.Kind:&lt;&gt;picture</span></span><br/> <span data-ttu-id="9ea85-232">Sistema. tipo: não Picture</span><span class="sxs-lookup"><span data-stu-id="9ea85-232">System.Kind:NOT picture</span></span><br/> <span data-ttu-id="9ea85-233">Sistema. Kind:--imagem</span><span class="sxs-lookup"><span data-stu-id="9ea85-233">System.Kind:- -picture</span></span><br/></td>
<td><span data-ttu-id="9ea85-234">A propriedade <a href="/windows/desktop/properties/props-system-kind">System. Kind</a> não é uma imagem.</span><span class="sxs-lookup"><span data-stu-id="9ea85-234">The <a href="/windows/desktop/properties/props-system-kind">System.Kind</a> property is not a picture.</span></span><br/> <span data-ttu-id="9ea85-235">A propriedade <a href="/windows/desktop/properties/props-system-photo-datetaken">System. Photo. DateTaken</a> tem um valor.</span><span class="sxs-lookup"><span data-stu-id="9ea85-235">The <a href="/windows/desktop/properties/props-system-photo-datetaken">System.Photo.DateTaken</a> property has a value.</span></span><br/> <span data-ttu-id="9ea85-236">A propriedade <a href="/windows/desktop/properties/props-system-kind">System. Kind</a> não é uma imagem.</span><span class="sxs-lookup"><span data-stu-id="9ea85-236">The <a href="/windows/desktop/properties/props-system-kind">System.Kind</a> property is not a picture.</span></span> <br/> <span data-ttu-id="9ea85-237">A propriedade <a href="/windows/desktop/properties/props-system-kind">System. Kind</a> não é uma imagem.</span><span class="sxs-lookup"><span data-stu-id="9ea85-237">The <a href="/windows/desktop/properties/props-system-kind">System.Kind</a> property is not a picture.</span></span> <br/> <span data-ttu-id="9ea85-238">Os operadores duplos não aplicados à mesma propriedade não são cancelados. Portanto, System. Kind:--Picture é equivalente a System. Kind:-Picture e System. Kind: não Picture.</span><span class="sxs-lookup"><span data-stu-id="9ea85-238">Double NOT operators applied to the same property do not cancel out. Hence, System.Kind:- -picture is equivalent to System.Kind:-picture and System.Kind:NOT picture.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ea85-239">COP_LESSTHAN</span><span class="sxs-lookup"><span data-stu-id="9ea85-239">COP_LESSTHAN</span></span></td>
<td>&lt;<br/></td>
<td><span data-ttu-id="9ea85-240">System. Size: &lt; 1 KB</span><span class="sxs-lookup"><span data-stu-id="9ea85-240">System.Size:&lt;1kb</span></span><br/></td>
<td><span data-ttu-id="9ea85-241">Esse valor é menor que <em>1 KB</em>.</span><span class="sxs-lookup"><span data-stu-id="9ea85-241">This value is less than <em>1kb</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ea85-242">COP_GREATERTHAN</span><span class="sxs-lookup"><span data-stu-id="9ea85-242">COP_GREATERTHAN</span></span></td>
<td>&gt;<br/></td>
<td><span data-ttu-id="9ea85-243">System. Data: &gt; System. StructuredQueryType. DateTime # hoje</span><span class="sxs-lookup"><span data-stu-id="9ea85-243">System.ItemDate:&gt;System.StructuredQueryType.DateTime#Today</span></span><br/></td>
<td><span data-ttu-id="9ea85-244">Este valor é maior que <em>hoje</em>.</span><span class="sxs-lookup"><span data-stu-id="9ea85-244">This value is greater than <em>today</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ea85-245">COP_LESSTHANOREQUAL</span><span class="sxs-lookup"><span data-stu-id="9ea85-245">COP_LESSTHANOREQUAL</span></span></td>
<td>&lt;=<br/> <span data-ttu-id="9ea85-246">≤</span><span class="sxs-lookup"><span data-stu-id="9ea85-246">≤</span></span><br/></td>
<td><span data-ttu-id="9ea85-247">System. Size: &lt; = 1 KB</span><span class="sxs-lookup"><span data-stu-id="9ea85-247">System.Size:&lt;=1kb</span></span><br/></td>
<td><span data-ttu-id="9ea85-248">Esse valor é menor ou igual a <em>1 KB</em>.</span><span class="sxs-lookup"><span data-stu-id="9ea85-248">This value is less than or equal to <em>1kb</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ea85-249">COP_GREATERTHANOREQUAL</span><span class="sxs-lookup"><span data-stu-id="9ea85-249">COP_GREATERTHANOREQUAL</span></span></td>
<td>&gt;=<br/> <span data-ttu-id="9ea85-250">≥</span><span class="sxs-lookup"><span data-stu-id="9ea85-250">≥</span></span><br/></td>
<td><span data-ttu-id="9ea85-251">System. Size: &gt; = 1 KB</span><span class="sxs-lookup"><span data-stu-id="9ea85-251">System.Size:&gt;=1kb</span></span><br/></td>
<td><span data-ttu-id="9ea85-252">Esse valor é igual a ou maior que <em>1 KB</em>.</span><span class="sxs-lookup"><span data-stu-id="9ea85-252">This value is equal to or greater than <em>1kb</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ea85-253">COP_VALUE_STARTSWITH</span><span class="sxs-lookup"><span data-stu-id="9ea85-253">COP_VALUE_STARTSWITH</span></span></td>
<td>~&lt;<br/></td>
<td><span data-ttu-id="9ea85-254">System. FileName: ~ &lt; &quot; instruções C++&quot;</span><span class="sxs-lookup"><span data-stu-id="9ea85-254">System.FileName:~&lt;&quot;C++ Primer&quot;</span></span><br/></td>
<td><span data-ttu-id="9ea85-255">Localiza os itens em que o nome do arquivo começa com os caracteres de &quot; <em>introdução do C++</em> &quot; .</span><span class="sxs-lookup"><span data-stu-id="9ea85-255">Finds items where the file name begins with the characters &quot;<em>C++ Primer</em>&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ea85-256">COP_VALUE_ENDSWITH</span><span class="sxs-lookup"><span data-stu-id="9ea85-256">COP_VALUE_ENDSWITH</span></span></td>
<td>~&gt;<br/></td>
<td><span data-ttu-id="9ea85-257">System. Photo. CameraModel: ~ &gt; não</span><span class="sxs-lookup"><span data-stu-id="9ea85-257">System.Photo.CameraModel:~&gt;non</span></span><br/></td>
<td><span data-ttu-id="9ea85-258">Localiza itens em que o valor da propriedade termina com os caracteres <em>não</em>.</span><span class="sxs-lookup"><span data-stu-id="9ea85-258">Finds items where the property value ends with the characters <em>non</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ea85-259">COP_VALUE_CONTAINS</span><span class="sxs-lookup"><span data-stu-id="9ea85-259">COP_VALUE_CONTAINS</span></span></td>
<td>~=<br/> ~~<br/></td>
<td><span data-ttu-id="9ea85-260">System. Subject. ~ = round</span><span class="sxs-lookup"><span data-stu-id="9ea85-260">System.Subject.~=round</span></span> <br/> <span data-ttu-id="9ea85-261">System. Search. autosummary: ~ ~ redondo</span><span class="sxs-lookup"><span data-stu-id="9ea85-261">System.Search.Autosummary:~~round</span></span><br/></td>
<td><span data-ttu-id="9ea85-262">Localiza uma mensagem que tem essa cadeia de caracteres no assunto e que corresponderá a &quot; g regras de<em>ida</em> e volta, &quot; por exemplo.</span><span class="sxs-lookup"><span data-stu-id="9ea85-262">Finds a message that has this string in the subject, and will match &quot;g<em>round</em> rules&quot; for example.</span></span><br/> <span data-ttu-id="9ea85-263">Localiza todos os itens com um resumo resumido que contém os caracteres <em>arredondados</em>.</span><span class="sxs-lookup"><span data-stu-id="9ea85-263">Finds all items with an Autosummary that contains the characters <em>round</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ea85-264">COP_VALUE_NOTCONTAINS</span><span class="sxs-lookup"><span data-stu-id="9ea85-264">COP_VALUE_NOTCONTAINS</span></span></td>
<td><span data-ttu-id="9ea85-265">~!</span><span class="sxs-lookup"><span data-stu-id="9ea85-265">~!</span></span><br/></td>
<td><span data-ttu-id="9ea85-266">System. Author: ~! &quot; Sanjay&quot;</span><span class="sxs-lookup"><span data-stu-id="9ea85-266">System.Author:~!&quot;sanjay&quot;</span></span><br/></td>
<td><span data-ttu-id="9ea85-267">Localiza os autores que não têm a sequência de caracteres &quot; <em>Sanjay</em> &quot; neles.</span><span class="sxs-lookup"><span data-stu-id="9ea85-267">Finds authors that do not have the character sequence&quot;<em>sanjay</em>&quot; in them.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ea85-268">COP_DOSWILDCARDS</span><span class="sxs-lookup"><span data-stu-id="9ea85-268">COP_DOSWILDCARDS</span></span></td>
<td>~ <br/></td>
<td><span data-ttu-id="9ea85-269">System. FileName: ~ &quot; MIC? osoft W \* d&quot;</span><span class="sxs-lookup"><span data-stu-id="9ea85-269">System.FileName:~&quot;Mic?osoft W\*d&quot;</span></span><br/></td>
<td><span data-ttu-id="9ea85-270">Localiza os arquivos em que o nome do arquivo começa com o <em>MIC</em>, seguido por algum caractere, seguido por <em>osoft w</em>, seguido de todos os caracteres que terminam com <em>d</em>.</span><span class="sxs-lookup"><span data-stu-id="9ea85-270">Finds files where the file name starts with <em>Mic</em>, followed by some character, followed by <em>osoft w</em>, followed by any characters ending with <em>d</em>.</span></span> <br/> <span data-ttu-id="9ea85-271">O ?</span><span class="sxs-lookup"><span data-stu-id="9ea85-271">The ?</span></span> <span data-ttu-id="9ea85-272">e \* os caracteres não são interpretados literalmente e funcionam como caracteres curinga de estilo DOS:</span><span class="sxs-lookup"><span data-stu-id="9ea85-272">and \* characters are not interpreted literally, and work like DOS-style wildcard characters:</span></span><br/>
<ul>
<li><span data-ttu-id="9ea85-273">?</span><span class="sxs-lookup"><span data-stu-id="9ea85-273">?</span></span> <span data-ttu-id="9ea85-274">corresponde a um caractere arbitrário.</span><span class="sxs-lookup"><span data-stu-id="9ea85-274">matches one arbitrary character.</span></span></li>
<li><span data-ttu-id="9ea85-275">\* corresponde a zero ou mais caracteres arbitrários.</span><span class="sxs-lookup"><span data-stu-id="9ea85-275">\* matches zero or more arbitrary characters.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ea85-276">COP_WORD_EQUAL</span><span class="sxs-lookup"><span data-stu-id="9ea85-276">COP_WORD_EQUAL</span></span></td>
<td>$=<br/> $$<br/></td>
<td><span data-ttu-id="9ea85-277">System. StructuredQuery. virtual. from: $ = &quot; Sanjay Jacobs&quot;</span><span class="sxs-lookup"><span data-stu-id="9ea85-277">System.StructuredQuery.Virtual.From:$=&quot;Sanjay Jacobs&quot;</span></span><br/></td>
<td><span data-ttu-id="9ea85-278">Para o Windows 7 e posterior.</span><span class="sxs-lookup"><span data-stu-id="9ea85-278">For Windows 7 and later.</span></span> <span data-ttu-id="9ea85-279">Localiza a frase &quot; <em>Sanjay Jacobs</em> &quot; em todas as propriedades.</span><span class="sxs-lookup"><span data-stu-id="9ea85-279">Finds the phrase &quot;<em>Sanjay Jacobs</em>&quot; in all From properties.</span></span> <span data-ttu-id="9ea85-280">A palavra <em>Sanjay</em> deve ser seguida da palavra <em>Jacobs</em>.</span><span class="sxs-lookup"><span data-stu-id="9ea85-280">The word <em>Sanjay</em> must be followed by the word <em>Jacobs</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ea85-281">COP_WORD_STARTSWITH</span><span class="sxs-lookup"><span data-stu-id="9ea85-281">COP_WORD_STARTSWITH</span></span></td>
<td>$<<br/></td>
<td><span data-ttu-id="9ea85-282">System. Author: $</span><span class="sxs-lookup"><span data-stu-id="9ea85-282">System.Author:$</span></span><&quot;San&quot; System.Filename:$<&quot;Micro Exe&quot;<br/></td>
<td><span data-ttu-id="9ea85-283">Para o Windows 7 e posterior.</span><span class="sxs-lookup"><span data-stu-id="9ea85-283">For Windows 7 and later.</span></span> <span data-ttu-id="9ea85-284">Localiza qualquer item em que o autor contém uma palavra que começa com os caracteres &quot; <em>San</em> &quot; .</span><span class="sxs-lookup"><span data-stu-id="9ea85-284">Finds any item where Author contains a word starting with the characters &quot;<em>San</em>&quot;.</span></span><br/> <span data-ttu-id="9ea85-285">Localiza qualquer arquivo no qual o nome do arquivo contenha uma palavra começando com <em>micro</em>, seguido por uma palavra que começa com <em>exe</em>.</span><span class="sxs-lookup"><span data-stu-id="9ea85-285">Finds any file in which the file name contains a word starting with <em>micro</em>, followed by a word starting with <em>exe</em>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9ea85-286">¹ colchetes vazios ( \[ \] ) denotam "sem valor".</span><span class="sxs-lookup"><span data-stu-id="9ea85-286">¹ Empty square brackets (\[\]) denote "no value".</span></span>

<span data-ttu-id="9ea85-287">Para propriedades de cadeia de caracteres, a operação padrão é COP \_ Word \_ começa \_ com ou COP \_ Word \_ Equals.</span><span class="sxs-lookup"><span data-stu-id="9ea85-287">For string properties the default operation is either COP\_WORD\_STARTS\_WITH or COP\_WORD\_EQUAL.</span></span>

### <a name="query-values"></a><span data-ttu-id="9ea85-288">Valores de consulta</span><span class="sxs-lookup"><span data-stu-id="9ea85-288">Query Values</span></span>

<span data-ttu-id="9ea85-289">Exemplos úteis de como os valores de consulta podem ser restritos estão listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9ea85-289">Useful examples of how query values can be restricted are listed in the following table.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9ea85-290">Valor/símbolo</span><span class="sxs-lookup"><span data-stu-id="9ea85-290">Value/symbol</span></span></th>
<th><span data-ttu-id="9ea85-291">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9ea85-291">Examples</span></span></th>
<th><span data-ttu-id="9ea85-292">Descrição</span><span class="sxs-lookup"><span data-stu-id="9ea85-292">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9ea85-293">String</span><span class="sxs-lookup"><span data-stu-id="9ea85-293">String</span></span></td>
<td><span data-ttu-id="9ea85-294">auto</span><span class="sxs-lookup"><span data-stu-id="9ea85-294">auto</span></span><br/></td>
<td><span data-ttu-id="9ea85-295">Qualquer sequência de caracteres que possa ser pesquisada.</span><span class="sxs-lookup"><span data-stu-id="9ea85-295">Any sequence of characters that can be searched for.</span></span> <span data-ttu-id="9ea85-296">A cadeia de caracteres não deve conter combinações de espaço em branco ou caracteres que fazem parte da sintaxe.</span><span class="sxs-lookup"><span data-stu-id="9ea85-296">The string must not contain whitespace or character combinations that are part of the syntax.</span></span> <span data-ttu-id="9ea85-297">Este exemplo pesquisa uma palavra que começa com <em>auto</em>.</span><span class="sxs-lookup"><span data-stu-id="9ea85-297">This example searches for a word beginning with <em>auto</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ea85-298">Cadeia de caracteres entre aspas &quot;&quot;</span><span class="sxs-lookup"><span data-stu-id="9ea85-298">Quoted string &quot;&quot;</span></span></td>
<td><span data-ttu-id="9ea85-299">&quot;Conclusões: válidas para &quot; &quot; a &quot; &quot; &quot; &quot; equipe azul&quot;</span><span class="sxs-lookup"><span data-stu-id="9ea85-299">&quot;Conclusions: valid&quot; &quot;The &quot;&quot;blue&quot;&quot; team&quot;</span></span><br/></td>
<td><span data-ttu-id="9ea85-300">Qualquer sequência de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9ea85-300">Any sequence of characters.</span></span> <span data-ttu-id="9ea85-301">A cadeia de caracteres não é interpretada como parte da sintaxe.</span><span class="sxs-lookup"><span data-stu-id="9ea85-301">The string is not interpreted as part of the syntax.</span></span><br/> <span data-ttu-id="9ea85-302">As aspas podem ser incluídas em uma consulta se forem duplicadas.</span><span class="sxs-lookup"><span data-stu-id="9ea85-302">Quotation marks can be included in a query if they are doubled.</span></span> <span data-ttu-id="9ea85-303">Este exemplo pesquisa <em>a &quot; &quot; equipe azul</em>.</span><span class="sxs-lookup"><span data-stu-id="9ea85-303">This example searches for <em>The &quot;blue&quot; team</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ea85-304">Integer</span><span class="sxs-lookup"><span data-stu-id="9ea85-304">Integer</span></span></td>
<td><span data-ttu-id="9ea85-305">5678</span><span class="sxs-lookup"><span data-stu-id="9ea85-305">5678</span></span><br/></td>
<td><span data-ttu-id="9ea85-306">Use apenas dígitos para inteiros.</span><span class="sxs-lookup"><span data-stu-id="9ea85-306">Use only digits for integers.</span></span> <span data-ttu-id="9ea85-307">Não use separadores para milhares.</span><span class="sxs-lookup"><span data-stu-id="9ea85-307">Do not use any separators for thousands.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ea85-308">Número de ponto flutuante</span><span class="sxs-lookup"><span data-stu-id="9ea85-308">Floating point number</span></span></td>
<td><span data-ttu-id="9ea85-309">5678,1234</span><span class="sxs-lookup"><span data-stu-id="9ea85-309">5678.1234</span></span><br/></td>
<td><span data-ttu-id="9ea85-310">Como os formatos de ponto flutuante variam entre as localidades, uma consulta canônica não pode usar uma constante de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="9ea85-310">Because floating point formats vary among locales, a canonical query cannot use a floating point constant.</span></span> <span data-ttu-id="9ea85-311">O uso de sintaxe canônica com números de ponto flutuante não é seguro para localização.</span><span class="sxs-lookup"><span data-stu-id="9ea85-311">The use of canonical syntax with floating point numbers is not localization safe.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ea85-312">Booliano <strong>verdadeiro</strong> / <strong>falso</strong></span><span class="sxs-lookup"><span data-stu-id="9ea85-312">Boolean <strong>true</strong>/<strong>false</strong></span></span></td>
<td><span data-ttu-id="9ea85-313">System. IsRead: = System. StructuredQueryType. Boolean # true</span><span class="sxs-lookup"><span data-stu-id="9ea85-313">System.IsRead:=System.StructuredQueryType.Boolean#True</span></span><br/> <span data-ttu-id="9ea85-314">System. IsEncrypted:-System. StructuredQueryType. Boolean # false</span><span class="sxs-lookup"><span data-stu-id="9ea85-314">System.IsEncrypted:-System.StructuredQueryType.Boolean#False</span></span><br/></td>
<td><span data-ttu-id="9ea85-315">O valor booliano <strong>verdadeiro</strong> .</span><span class="sxs-lookup"><span data-stu-id="9ea85-315">The <strong>TRUE</strong> Boolean value.</span></span><br/> <span data-ttu-id="9ea85-316">O valor booliano <strong>false</strong> .</span><span class="sxs-lookup"><span data-stu-id="9ea85-316">The <strong>FALSE</strong> Boolean value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ea85-317">[]</span><span class="sxs-lookup"><span data-stu-id="9ea85-317">[]</span></span></td>
<td><span data-ttu-id="9ea85-318">System. Keywords: = []</span><span class="sxs-lookup"><span data-stu-id="9ea85-318">System.Keywords:=[]</span></span><br/></td>
<td><span data-ttu-id="9ea85-319">Colchetes vazios denotam que não há nenhum valor.</span><span class="sxs-lookup"><span data-stu-id="9ea85-319">Empty square brackets denote that there is no value.</span></span> <span data-ttu-id="9ea85-320">Este exemplo localiza todos os itens que não foram marcados.</span><span class="sxs-lookup"><span data-stu-id="9ea85-320">This example finds all items that have not been tagged.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ea85-321">Datas absolutas</span><span class="sxs-lookup"><span data-stu-id="9ea85-321">Absolute dates</span></span></td>
<td><span data-ttu-id="9ea85-322">System. @ Date: 1/26/2010</span><span class="sxs-lookup"><span data-stu-id="9ea85-322">System.ItemDate:1/26/2010</span></span><br/> <span data-ttu-id="9ea85-323">SystemDateModified 10/15/2002 19:00</span><span class="sxs-lookup"><span data-stu-id="9ea85-323">SystemDateModified 10/15/2002 19:00</span></span><br/></td>
<td><span data-ttu-id="9ea85-324">Localiza itens com uma data de 26 de janeiro de 2010.</span><span class="sxs-lookup"><span data-stu-id="9ea85-324">Finds items with a date of 26 January 2010.</span></span><br/> <span data-ttu-id="9ea85-325">Localiza itens que foram modificados em 15 de outubro de 2002 entre as horas 19:00:00 e 19:00:59.</span><span class="sxs-lookup"><span data-stu-id="9ea85-325">Finds items that were modified on 15 October 2002 between the hours 19:00:00 and 19:00:59.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9ea85-326">Como os formatos de data (como formatos de ponto flutuante) variam entre as localidades, o uso da sintaxe canônica com datas absolutas não é suportado e não é seguro para localização.</span><span class="sxs-lookup"><span data-stu-id="9ea85-326">Because date formats (like floating point formats) vary among locales, the use of canonical syntax with absolute dates is not supported and is not localization safe.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ea85-327">Datas relativas</span><span class="sxs-lookup"><span data-stu-id="9ea85-327">Relative dates</span></span></td>
<td><span data-ttu-id="9ea85-328">System. Data: System. StructuredQueryType. DateTime # hoje</span><span class="sxs-lookup"><span data-stu-id="9ea85-328">System.ItemDate:System.StructuredQueryType.DateTime#Today</span></span><br/> <span data-ttu-id="9ea85-329">System. DateAcquired: System. StructuredQueryType. DateTime # NextMonth</span><span class="sxs-lookup"><span data-stu-id="9ea85-329">System.DateAcquired:System.StructuredQueryType.DateTime#NextMonth</span></span><br/> <span data-ttu-id="9ea85-330">System. Message. DateReceived: System. StructuredQueryType. DateTime # LastYear</span><span class="sxs-lookup"><span data-stu-id="9ea85-330">System.Message.DateReceived:System.StructuredQueryType.DateTime#LastYear</span></span><br/></td>
<td><span data-ttu-id="9ea85-331">Localiza itens com a data de hoje.</span><span class="sxs-lookup"><span data-stu-id="9ea85-331">Finds items with today's date.</span></span><br/> <span data-ttu-id="9ea85-332">Localiza itens com uma data no próximo mês.</span><span class="sxs-lookup"><span data-stu-id="9ea85-332">Finds items with a date in the next month.</span></span><br/> <span data-ttu-id="9ea85-333">Localiza itens com uma data no último ano.</span><span class="sxs-lookup"><span data-stu-id="9ea85-333">Finds items with a date in the last year.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9ea85-334">Além de Pesquisar datas específicas e intervalos de datas, o AQS reconhece valores de datas relativas (como <em>hoje</em>, <em>amanhã</em>, <em>nextweek</em>, <em>nextmonth</em>) e dia (como <em>terça-feira</em> ou segunda-feira). <em> Quarta-feira</em>) e mês (<em>fevereiro</em>).</span><span class="sxs-lookup"><span data-stu-id="9ea85-334">In addition to searching on specific dates and date ranges, AQS recognizes relative date values (like <em>today</em>, <em>tomorrow</em>, <em>nextweek</em>, <em>nextmonth</em>), and day (like <em>Tuesday</em> or <em>Monday..Wednesday</em>), and month (<em>February</em>).</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ea85-335">..</span><span class="sxs-lookup"><span data-stu-id="9ea85-335">..</span></span></td>
<td><span data-ttu-id="9ea85-336">System. @ Date: 11/05/04.. 11/10/04 sistema. Size: 5 KB.. 10 KB</span><span class="sxs-lookup"><span data-stu-id="9ea85-336">System.ItemDate:11/05/04..11/10/04 System.Size:5kb..10kb</span></span><br/></td>
<td><span data-ttu-id="9ea85-337">Pontos duplos indicam um intervalo de valores.</span><span class="sxs-lookup"><span data-stu-id="9ea85-337">Double periods indicate a value range.</span></span> <span data-ttu-id="9ea85-338">Localiza itens com uma data entre 11/05/04 e 11/10/04, inclusive.</span><span class="sxs-lookup"><span data-stu-id="9ea85-338">Finds items with a date between 11/05/04 and 11/10/04, inclusive.</span></span><br/> <span data-ttu-id="9ea85-339">Localiza itens entre 5 e 10 KB de tamanho.</span><span class="sxs-lookup"><span data-stu-id="9ea85-339">Finds items between 5 and 10kb in size.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="scope-restrictions"></a><span data-ttu-id="9ea85-340">Restrições de escopo</span><span class="sxs-lookup"><span data-stu-id="9ea85-340">Scope Restrictions</span></span>

<span data-ttu-id="9ea85-341">Os usuários podem limitar o escopo de suas pesquisas a locais de pasta ou armazenamentos de dados específicos.</span><span class="sxs-lookup"><span data-stu-id="9ea85-341">Users can limit the scope of their searches to specific folder locations or data stores.</span></span> <span data-ttu-id="9ea85-342">Por exemplo, se você usar várias contas de email e quiser limitar uma consulta ao Microsoft Outlook ou ao Microsoft Outlook Express, poderá usar `System.Search.Store:mapi` ou `System.Search.Store:oe` respectivamente.</span><span class="sxs-lookup"><span data-stu-id="9ea85-342">For example, if you use several email accounts and you want to limit a query to either Microsoft Outlook or Microsoft Outlook Express, you can use `System.Search.Store:mapi` or `System.Search.Store:oe` respectively.</span></span> <span data-ttu-id="9ea85-343">A tabela a seguir mostra alguns exemplos de como restringir uma pesquisa por armazenamento de dados.</span><span class="sxs-lookup"><span data-stu-id="9ea85-343">The following table shows some examples of how to restrict a search by data store.</span></span>



| <span data-ttu-id="9ea85-344">Restringir pesquisa por repositório de dados</span><span class="sxs-lookup"><span data-stu-id="9ea85-344">Restrict search by data store</span></span>  | <span data-ttu-id="9ea85-345">Palavra-chave</span><span class="sxs-lookup"><span data-stu-id="9ea85-345">Keyword</span></span> | <span data-ttu-id="9ea85-346">Exemplo</span><span class="sxs-lookup"><span data-stu-id="9ea85-346">Example</span></span>                                     |
|--------------------------------|---------|---------------------------------------------|
| <span data-ttu-id="9ea85-347">Arquivos</span><span class="sxs-lookup"><span data-stu-id="9ea85-347">Files</span></span>                          | <span data-ttu-id="9ea85-348">arquivo</span><span class="sxs-lookup"><span data-stu-id="9ea85-348">file</span></span>    | <span data-ttu-id="9ea85-349">System. Search. Store: arquivo</span><span class="sxs-lookup"><span data-stu-id="9ea85-349">System.Search.Store:file</span></span>                    |
| <span data-ttu-id="9ea85-350">Outlook</span><span class="sxs-lookup"><span data-stu-id="9ea85-350">Outlook</span></span>                        | <span data-ttu-id="9ea85-351">MAPI</span><span class="sxs-lookup"><span data-stu-id="9ea85-351">mapi</span></span>    | <span data-ttu-id="9ea85-352">System. Search. Store: MAPI</span><span class="sxs-lookup"><span data-stu-id="9ea85-352">System.Search.Store:mapi</span></span>                    |
| <span data-ttu-id="9ea85-353">Outlook Express</span><span class="sxs-lookup"><span data-stu-id="9ea85-353">Outlook Express</span></span>                | <span data-ttu-id="9ea85-354">OE</span><span class="sxs-lookup"><span data-stu-id="9ea85-354">oe</span></span>      | <span data-ttu-id="9ea85-355">System. Search. Store: OE</span><span class="sxs-lookup"><span data-stu-id="9ea85-355">System.Search.Store:oe</span></span>                      |
| <span data-ttu-id="9ea85-356">Arquivos Offline</span><span class="sxs-lookup"><span data-stu-id="9ea85-356">Offline files</span></span>                  | <span data-ttu-id="9ea85-357">CSC</span><span class="sxs-lookup"><span data-stu-id="9ea85-357">csc</span></span>     | <span data-ttu-id="9ea85-358">System. Search. Store: CSC</span><span class="sxs-lookup"><span data-stu-id="9ea85-358">System.Search.Store:csc</span></span>                     |
| <span data-ttu-id="9ea85-359">Pasta específica na unidade local</span><span class="sxs-lookup"><span data-stu-id="9ea85-359">Specific folder on local drive</span></span> | <span data-ttu-id="9ea85-360">folder</span><span class="sxs-lookup"><span data-stu-id="9ea85-360">folder</span></span>  | <span data-ttu-id="9ea85-361">System. ItemFolderNameDisplay: C: " \\ MyFolder"</span><span class="sxs-lookup"><span data-stu-id="9ea85-361">System.ItemFolderNameDisplay:C:"\\MyFolder"</span></span> |



 

## <a name="additional-resources"></a><span data-ttu-id="9ea85-362">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="9ea85-362">Additional Resources</span></span>

-   <span data-ttu-id="9ea85-363">No Windows 7 e posterior, uma opção de menu de atalho pode estar disponível com base no fato de uma condição AQS ser atendida.</span><span class="sxs-lookup"><span data-stu-id="9ea85-363">In Windows 7 and later, a shortcut menu option can be available based on whether an AQS condition is met.</span></span> <span data-ttu-id="9ea85-364">Para obter mais informações, consulte "obtendo comportamento dinâmico para verbos estáticos usando a sintaxe de consulta avançada" em [criando manipuladores de menu de contexto](../shell/context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="9ea85-364">For more information, see "Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax" in [Creating Context Menu Handlers](../shell/context-menu-handlers.md).</span></span>
-   <span data-ttu-id="9ea85-365">As consultas AQS podem ser limitadas a tipos específicos de arquivos, que são conhecidos como tipos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="9ea85-365">AQS queries can be limited to specific types of files, which are known as file kinds.</span></span> <span data-ttu-id="9ea85-366">Para obter mais informações, consulte [tipos de arquivo e associações](../shell/fa-intro.md).</span><span class="sxs-lookup"><span data-stu-id="9ea85-366">For more information, see [File Types and Associations](../shell/fa-intro.md).</span></span> <span data-ttu-id="9ea85-367">Para obter a documentação de referência de propriedade, consulte [System. Kind](../properties/props-system-kind.md)e [System. KindText](../properties/props-system-kindtext.md).</span><span class="sxs-lookup"><span data-stu-id="9ea85-367">For property reference documentation, see [System.Kind](../properties/props-system-kind.md), and [System.KindText](../properties/props-system-kindtext.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ea85-368">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9ea85-368">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ea85-369">Consulta do índice de maneira programática</span><span class="sxs-lookup"><span data-stu-id="9ea85-369">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="9ea85-370">Usando abordagens SQL e AQS para consultar o índice</span><span class="sxs-lookup"><span data-stu-id="9ea85-370">Using SQL and AQS Approaches to Query the Index</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="9ea85-371">Consultando o índice com ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="9ea85-371">Querying the Index with ISearchQueryHelper</span></span>](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[<span data-ttu-id="9ea85-372">Consultando o índice com o protocolo Search-MS</span><span class="sxs-lookup"><span data-stu-id="9ea85-372">Querying the Index with the search-ms Protocol</span></span>](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[<span data-ttu-id="9ea85-373">Consultando o índice com a sintaxe SQL do Windows Search</span><span class="sxs-lookup"><span data-stu-id="9ea85-373">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)
</dt> </dl>

 

 

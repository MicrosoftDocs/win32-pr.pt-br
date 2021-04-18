---
title: Definições de tipo, declarações de construção e importações
description: As definições de tipo, as declarações de construção e as importações podem ocorrer fora do corpo da interface.
ms.assetid: 5d9011ab-bfc4-41f6-bd69-953660191652
keywords:
- MIDL de interfaces, definições de tipo
- interfaces MIDL, declarações de construção
- MIDL de interfaces, importações
- definições de tipo MIDL
- MIDL de declarações de construção
- MIDL de importações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645781f033566ba43dc6e355935ed112d0e8f5f6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105756911"
---
# <a name="type-definitions-construct-declarations-and-imports"></a><span data-ttu-id="bb83a-109">Definições de tipo, declarações de construção e importações</span><span class="sxs-lookup"><span data-stu-id="bb83a-109">Type Definitions, Construct Declarations, and Imports</span></span>

<span data-ttu-id="bb83a-110">As definições de tipo, as declarações de construção e as importações podem ocorrer fora do corpo da interface.</span><span class="sxs-lookup"><span data-stu-id="bb83a-110">Type definitions, construct declarations, and imports can occur outside of the interface body.</span></span> <span data-ttu-id="bb83a-111">Todas as definições do arquivo IDL principal serão exibidas no arquivo de cabeçalho gerado e todos os procedimentos de todas as interfaces no arquivo IDL principal irão gerar rotinas de stub.</span><span class="sxs-lookup"><span data-stu-id="bb83a-111">All definitions from the main IDL file will appear in the generated header file, and all the procedures from all the interfaces in the main IDL file will generate stub routines.</span></span> <span data-ttu-id="bb83a-112">Isso permite que os aplicativos que dão suporte a várias interfaces mesclem arquivos IDL em um único arquivo IDL combinado.</span><span class="sxs-lookup"><span data-stu-id="bb83a-112">This enables applications that support multiple interfaces to merge IDL files into a single, combined IDL file.</span></span>

<span data-ttu-id="bb83a-113">Como resultado, ele requer menos tempo para compilar os arquivos e também permite que MIDL reduza as redundâncias nos stubs gerados.</span><span class="sxs-lookup"><span data-stu-id="bb83a-113">As a result, it requires less time to compile the files and also allows MIDL to reduce redundancies in the generated stubs.</span></span> <span data-ttu-id="bb83a-114">Isso pode melhorar significativamente as interfaces de [**objeto**](object.md) através da capacidade de compartilhar código comum para interfaces base e interfaces derivadas.</span><span class="sxs-lookup"><span data-stu-id="bb83a-114">This can significantly improve [**object**](object.md) interfaces through the ability to share common code for base interfaces and derived interfaces.</span></span> <span data-ttu-id="bb83a-115">Para interfaces que não são de **objeto** , os nomes de procedimento devem ser exclusivos em todas as interfaces.</span><span class="sxs-lookup"><span data-stu-id="bb83a-115">For non- **object** interfaces, the procedure names must be unique across all the interfaces.</span></span> <span data-ttu-id="bb83a-116">Para interfaces de **objeto** , os nomes de procedimento precisam ser exclusivos somente dentro de uma interface.</span><span class="sxs-lookup"><span data-stu-id="bb83a-116">For **object** interfaces, the procedure names need to be unique only within an interface.</span></span> <span data-ttu-id="bb83a-117">Observe que várias interfaces não são permitidas quando você usa a opção [**/OSF**](-osf.md)</span><span class="sxs-lookup"><span data-stu-id="bb83a-117">Note that multiple interfaces are not permitted when you use the [**/osf**](-osf.md) switch.</span></span>

## <a name="declarative-constructs"></a><span data-ttu-id="bb83a-118">Construções declarativas</span><span class="sxs-lookup"><span data-stu-id="bb83a-118">Declarative Constructs</span></span>

<span data-ttu-id="bb83a-119">A sintaxe para construções declarativas no arquivo IDL é semelhante àquela para C. MIDL dá suporte a todas as construções declarativas do Microsoft C/C++, exceto as seguintes:</span><span class="sxs-lookup"><span data-stu-id="bb83a-119">The syntax for declarative constructs in the IDL file is similar to that for C. MIDL supports all Microsoft C/C++ declarative constructs except the following:</span></span>

-   <span data-ttu-id="bb83a-120">Declaradores de estilo mais antigos que permitem que um Declarador seja especificado sem um especificador de tipo, como:</span><span class="sxs-lookup"><span data-stu-id="bb83a-120">Older style declarators that allow a declarator to be specified without a type specifier, such as:</span></span>

    ``` syntax
    x (y) 
    short x (y)
    ```

-   <span data-ttu-id="bb83a-121">Declarações com inicializadores (MIDL aceita apenas declarações que estão em conformidade com a sintaxe MIDL [**const**](const.md) ).</span><span class="sxs-lookup"><span data-stu-id="bb83a-121">Declarations with initializers (MIDL only accepts declarations that conform to the MIDL [**const**](const.md) syntax).</span></span>

<span data-ttu-id="bb83a-122">A palavra-chave [**Import**](import.md) especifica os nomes de um ou mais arquivos IDL a serem importados.</span><span class="sxs-lookup"><span data-stu-id="bb83a-122">The [**import**](import.md) keyword specifies the names of one or more IDL files to import.</span></span> <span data-ttu-id="bb83a-123">A diretiva de importação é semelhante à diretiva C [**include**](include.md) , exceto que apenas os tipos de dados são assimilados no arquivo de importação de IDL.</span><span class="sxs-lookup"><span data-stu-id="bb83a-123">The import directive is similar to the C [**include**](include.md) directive, except that only data types are assimilated into the importing IDL file.</span></span>

## <a name="constant-declaration"></a><span data-ttu-id="bb83a-124">Declaração de constante</span><span class="sxs-lookup"><span data-stu-id="bb83a-124">Constant Declaration</span></span>

<span data-ttu-id="bb83a-125">A declaração de constante especifica as constantes [**booliana**](boolean.md), inteiro, caractere, caractere largo, Cadeia de caracteres e **void \*** .</span><span class="sxs-lookup"><span data-stu-id="bb83a-125">The constant declaration specifies [**Boolean**](boolean.md), integer, character, wide-character, string, and **void \*** constants.</span></span> <span data-ttu-id="bb83a-126">Para obter mais informações, consulte [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="bb83a-126">For more information, see [**const**](const.md).</span></span>

## <a name="general-declaration"></a><span data-ttu-id="bb83a-127">Declaração geral</span><span class="sxs-lookup"><span data-stu-id="bb83a-127">General Declaration</span></span>

<span data-ttu-id="bb83a-128">Uma declaração geral é semelhante à instrução C [**typedef**](typedef.md) com a adição de atributos de tipo IDL.</span><span class="sxs-lookup"><span data-stu-id="bb83a-128">A general declaration is similar to the C [**typedef**](typedef.md) statement with the addition of IDL type attributes.</span></span> <span data-ttu-id="bb83a-129">Exceto no modo [**/OSF**](-osf.md) , o compilador MIDL também permite uma declaração implícita na forma de uma definição de variável.</span><span class="sxs-lookup"><span data-stu-id="bb83a-129">Except in [**/osf**](-osf.md) mode, the MIDL compiler also allows an implicit declaration in the form of a variable definition.</span></span>

## <a name="function-declaration"></a><span data-ttu-id="bb83a-130">Declaração de função</span><span class="sxs-lookup"><span data-stu-id="bb83a-130">Function Declaration</span></span>

<span data-ttu-id="bb83a-131">O Declarador de função é um caso especial da declaração geral.</span><span class="sxs-lookup"><span data-stu-id="bb83a-131">The function declarator is a special case of the general declaration.</span></span> <span data-ttu-id="bb83a-132">Você pode usar atributos IDL para especificar o comportamento do tipo de retorno da função e de cada um dos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="bb83a-132">You can use IDL attributes to specify the behavior of the function return type and each of the parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="bb83a-133">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bb83a-133">Examples</span></span>

``` syntax
[ 
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(3.1), 
    pointer_default(unique) 
] 
interface IdlGrammarExample 
{ 
    import "windows.idl", "other.idl"; 
    const wchar_t * NAME = L"Example Program"; 
    typedef char * PCHAR; 
 
    HRESULT DictCheckSpelling( 
        [in, string] PCHAR   word,     // word to look up 
        [out]        short * isPresent // 0 if not present 
    ); 
}
```

 

 





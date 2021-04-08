---
title: Lidando com as definições em arquivos IDL
description: Esta página descreve por que os símbolos definidos com um \ define desaparecem dos arquivos H gerados pelo compilador de MIDL e o que pode ser feito sobre ele. Esta explicação se aplica a todos os arquivos processados pelo MIDL, como \. idl, \. ACF, arquivos \. h.
ms.assetid: 148dabda-96cc-4f7c-abc7-4bf78ac166ea
keywords:
- MIDL do compilador MIDL, lidando com as definições
- define MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4af77979824c2e76352d6f28bef72161249845d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005474"
---
# <a name="dealing-with-defines-in-idl-files"></a><span data-ttu-id="13033-106">Lidando com as \# definições em arquivos IDL</span><span class="sxs-lookup"><span data-stu-id="13033-106">Dealing with \#defines in IDL Files</span></span>

<span data-ttu-id="13033-107">Esta página descreve por que os símbolos definidos com uma **\# definição** desaparecem dos arquivos H gerados pelo compilador de MIDL e o que pode ser feito sobre ele.</span><span class="sxs-lookup"><span data-stu-id="13033-107">This page describes why symbols defined with a **\#define** disappear from the MIDL compiler generated H files, and what can be done about it.</span></span> <span data-ttu-id="13033-108">Essa explicação se aplica a todos os arquivos processados pelo MIDL, como \* . idl, \* . ACF, \* arquivos. h.</span><span class="sxs-lookup"><span data-stu-id="13033-108">This explanation applies to any files processed by MIDL, such as \*.idl, \*.acf, \*.h files.</span></span>

<span data-ttu-id="13033-109">O desaparecimento de **\# definir** símbolos é resultado de MIDL delegando o pré-processamento de arquivos de entrada para um pré-processador.</span><span class="sxs-lookup"><span data-stu-id="13033-109">The disappearance of **\#define** symbols is a result of MIDL delegating the preprocessing of input files to a preprocessor.</span></span> <span data-ttu-id="13033-110">Por padrão, o pré-processador é um pré-processador de C/C++ do ambiente de compilação.</span><span class="sxs-lookup"><span data-stu-id="13033-110">By default, the preprocessor is a C/C++ preprocessor from the build environment.</span></span> <span data-ttu-id="13033-111">Após o pré-processamento, o MIDL do fluxo de entrada recebe apenas as \# diretivas de pré-processador de linha.</span><span class="sxs-lookup"><span data-stu-id="13033-111">After preprocessing, the input stream MIDL receives has only \#line preprocessor directives.</span></span> <span data-ttu-id="13033-112">Em particular, o pré-processador desverte todas as definições de macro em arquivos de entrada e, portanto, o MIDL não pode detectar sua presença.</span><span class="sxs-lookup"><span data-stu-id="13033-112">In particular, the preprocessor unrolls all macro definitions in input files, and therefore, MIDL cannot detect their presence.</span></span> <span data-ttu-id="13033-113">Consequentemente, quando MIDL Replica definições de tipo de um arquivo de entrada para o arquivo H gerado, as \# Defines não são replicadas.</span><span class="sxs-lookup"><span data-stu-id="13033-113">Consequently, when MIDL replicates type definitions from an input file to the generated H file, the \#defines are not replicated.</span></span> <span data-ttu-id="13033-114">Portanto, não use \# define diretamente em arquivos IDL se eles forem usados posteriormente a partir do arquivo H gerado.</span><span class="sxs-lookup"><span data-stu-id="13033-114">Therefore, do not use \#defines directly in IDL files if they are to be used later from the generated H file.</span></span>

<span data-ttu-id="13033-115">As quatro soluções alternativas a seguir são recomendadas:</span><span class="sxs-lookup"><span data-stu-id="13033-115">The following four workarounds are recommended:</span></span>

-   <span data-ttu-id="13033-116">Use a especificação de Declaração [**const**](const.md) .</span><span class="sxs-lookup"><span data-stu-id="13033-116">Use the [**const**](const.md) declaration specification.</span></span>
-   <span data-ttu-id="13033-117">Use arquivos de cabeçalho separados que são importados ou incluídos no arquivo IDL, e posteriormente incluídos no código-fonte C.</span><span class="sxs-lookup"><span data-stu-id="13033-117">Use separate header files that are imported or included in the IDL file, and later included in the C-source code.</span></span>
-   <span data-ttu-id="13033-118">Use constantes de enumeração no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="13033-118">Use enumeration constants in the IDL file.</span></span>
-   <span data-ttu-id="13033-119">Use [**a \_ cotação de CPP**](cpp-quote.md) para reproduzir **\# definir** no arquivo de cabeçalho gerado.</span><span class="sxs-lookup"><span data-stu-id="13033-119">Use [**cpp\_quote**](cpp-quote.md) to reproduce **\#define** in the generated header file.</span></span>

<span data-ttu-id="13033-120">Você pode reproduzir constantes de manifesto usando a **sintaxe de declaração constante de IDL**.</span><span class="sxs-lookup"><span data-stu-id="13033-120">You can reproduce manifest constants using the **IDL constant-declaration syntax**.</span></span> <span data-ttu-id="13033-121">Observe que [**const**](const.md) na declaração de constante de IDL é diferente da semântica **const** C/C++ e simplesmente introduz uma constante nomeada para uma compilação de IDL.</span><span class="sxs-lookup"><span data-stu-id="13033-121">Note that the [**const**](const.md) in the IDL constant-declaration is different from C/C++ **const** semantics, and simply introduces a named constant for an IDL compilation.</span></span> <span data-ttu-id="13033-122">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="13033-122">For example:</span></span>

``` syntax
const short ARRSIZE = 10
```

<span data-ttu-id="13033-123">Este exemplo especifica que **ARRSIZE** é uma constante com um valor de 10.</span><span class="sxs-lookup"><span data-stu-id="13033-123">This example specifies that **ARRSIZE** is a constant with a value of 10.</span></span> <span data-ttu-id="13033-124">As constantes nomeadas podem ser usadas em declaradores de matriz de IDL e em outros locais onde um programador de C usaria um manifesto definido.</span><span class="sxs-lookup"><span data-stu-id="13033-124">Named constants can be used in IDL array declarators and other places where a C programmer would use a manifest defines.</span></span> <span data-ttu-id="13033-125">Além disso, essa sintaxe resulta na geração da seguinte linha no arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="13033-125">In addition, this syntax results in the following line being generated in the header file:</span></span>

``` syntax
#define ARRSIZE 10
```

<span data-ttu-id="13033-126">Outra maneira de lidar com **\#** instruções de definição é empacotá-las em um arquivo de cabeçalho separado, em um arquivo dedicado para **\#** definir instruções ou em um arquivo que contenha apenas definições de tipo.</span><span class="sxs-lookup"><span data-stu-id="13033-126">Another way to handle **\#** define statements is to package them in a separate header file, either into a file devoted to **\#** define statements or into a file that contains only type definitions.</span></span> <span data-ttu-id="13033-127">Um arquivo que contém apenas diretivas de pré-processador pode ser incluído com segurança pelo arquivo IDL e pelos arquivos de origem C.</span><span class="sxs-lookup"><span data-stu-id="13033-127">A file that contains only preprocessor directives may be safely included both by the IDL file and the C-source files.</span></span> <span data-ttu-id="13033-128">Embora as diretivas não estejam disponíveis no arquivo de cabeçalho gerado pelo compilador MIDL, o programa de origem C pode incluir o arquivo de cabeçalho separado.</span><span class="sxs-lookup"><span data-stu-id="13033-128">Although the directives will not be available in the header file generated by the MIDL compiler, the C-source program can include the separate header file.</span></span> <span data-ttu-id="13033-129">De maneira semelhante, um arquivo de cabeçalho com **\#** instruções de definição e de tipo regular pode ser importado de seu arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="13033-129">In a similar fashion, a header file with **\#** define statements and regular type definitions can be imported from your IDL file.</span></span> <span data-ttu-id="13033-130">Essa abordagem encapsula as **\#** instruções define e typedef usando-as em um arquivo H, de modo que os **\#** símbolos de definição não sejam usados diretamente no arquivo de importação de IDL.</span><span class="sxs-lookup"><span data-stu-id="13033-130">This approach encapsulates the **\#** define and typedef statements by using them in an H file such that the **\#** define symbols are not used in the importing IDL file directly.</span></span> <span data-ttu-id="13033-131">Importar um cabeçalho ou arquivo IDL para outro arquivo IDL impede que as instruções typedef sejam replicadas para o arquivo H gerado pelo MIDL (que está em contraste com as **\#** instruções include).</span><span class="sxs-lookup"><span data-stu-id="13033-131">Importing a header or IDL file to another IDL file prevents the typedef statements from being replicated to the H file generated by MIDL (which is in contrast to **\#** include statements).</span></span> <span data-ttu-id="13033-132">Essa abordagem permite que o arquivo de cabeçalho original seja referenciado com segurança do código C ao longo do arquivo H gerado sem ter um problema com definições duplicadas.</span><span class="sxs-lookup"><span data-stu-id="13033-132">This approach allows the original header file to be safely referenced from the C code along the generated H file without having a problem with duplicated definitions.</span></span>

<span data-ttu-id="13033-133">O uso de constantes de enumeração no arquivo IDL também é eficaz.</span><span class="sxs-lookup"><span data-stu-id="13033-133">Use of enumeration constants in the IDL file is also effective.</span></span> <span data-ttu-id="13033-134">Essas constantes podem ser usadas em expressões constantes em IDL, por exemplo, em declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="13033-134">These constants can be used in constant expressions in IDL, for example, in array declarators.</span></span> <span data-ttu-id="13033-135">As constantes de enumeração não são removidas durante as primeiras fases da compilação MIDL pelo pré-processador do compilador C, portanto, as constantes de enumeração estão disponíveis no arquivo de cabeçalho gerado pelo compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="13033-135">Enumeration constants are not removed during the early phases of MIDL compilation by the C-compiler preprocessor, so enumeration constants are available in the header file generated by the MIDL compiler.</span></span> <span data-ttu-id="13033-136">Considere o seguinte instrução:</span><span class="sxs-lookup"><span data-stu-id="13033-136">Consider the following statement:</span></span>

``` syntax
typedef enum midlworkaround { MAXSTRINGCOUNT = 300 };
```

<span data-ttu-id="13033-137">Essa instrução não será removida durante a compilação MIDL pelo pré-processador C e o typedef será replicado para o arquivo H gerado.</span><span class="sxs-lookup"><span data-stu-id="13033-137">This statement will not be removed during MIDL compilation by the C preprocessor and the typedef will be replicated to the generated H file.</span></span> <span data-ttu-id="13033-138">A constante MAXSTRINGCOUNT está disponível para programas de origem C que incluem o arquivo de cabeçalho gerado pelo compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="13033-138">The constant MAXSTRINGCOUNT is available to C-source programs that include the header file generated by the MIDL compiler.</span></span>

<span data-ttu-id="13033-139">Por fim, a diretiva de [**\_ citação de CPP**](cpp-quote.md) do MIDL pode ser usada para gravar uma cadeia de caracteres arbitrária diretamente no arquivo H gerado.</span><span class="sxs-lookup"><span data-stu-id="13033-139">Finally, the [**cpp\_quote**](cpp-quote.md) directive of MIDL can be used to write out an arbitrary string directly into the generated H file.</span></span> <span data-ttu-id="13033-140">Por exemplo, para obter a constante de manifesto usada anteriormente nesta página com **\_ aspas de CPP**, a instrução a seguir pode ser usada:</span><span class="sxs-lookup"><span data-stu-id="13033-140">For example, to get the manifest constant used previously on this page with **cpp\_quote**, the following statement can be used:</span></span>

``` syntax
cpp_quote ("#define ARRSIZE 10")
```

<span data-ttu-id="13033-141">Essa instrução resulta na geração da seguinte linha no arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="13033-141">This statement results in the following line being generated in the header file:</span></span>

``` syntax
#define ARRSIZE 10
```

 

 





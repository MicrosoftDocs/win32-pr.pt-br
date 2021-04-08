---
description: A biblioteca DbgHelp usa o caminho de pesquisa de símbolo para localizar símbolos de depuração (arquivos. PDB e. dbg). O caminho de pesquisa pode ser composto por um ou mais elementos de caminho separados por ponto e vírgula.
ms.assetid: 3527f589-285b-4cdf-b024-17920971a904
title: Caminhos de símbolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 977772e45c345e1e990dc038fccd852d17d279dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920275"
---
# <a name="symbol-paths"></a><span data-ttu-id="fd111-104">Caminhos de símbolo</span><span class="sxs-lookup"><span data-stu-id="fd111-104">Symbol Paths</span></span>

<span data-ttu-id="fd111-105">A biblioteca DbgHelp usa o caminho de pesquisa de símbolo para localizar símbolos de depuração (arquivos. PDB e. dbg).</span><span class="sxs-lookup"><span data-stu-id="fd111-105">The DbgHelp library uses the symbol search path to locate debug symbols (.pdb and .dbg files).</span></span> <span data-ttu-id="fd111-106">O caminho de pesquisa pode ser composto por um ou mais elementos de caminho separados por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="fd111-106">The search path can be made up of one or more path elements separated by semicolons.</span></span>

## <a name="specifying-search-paths"></a><span data-ttu-id="fd111-107">Especificando caminhos de pesquisa</span><span class="sxs-lookup"><span data-stu-id="fd111-107">Specifying Search Paths</span></span>

<span data-ttu-id="fd111-108">Para especificar onde o manipulador de símbolo pesquisará os diretórios de disco para arquivos de símbolo, chame a função [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) .</span><span class="sxs-lookup"><span data-stu-id="fd111-108">To specify where the symbol handler will search disk directories for symbol files, call the [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) function.</span></span> <span data-ttu-id="fd111-109">Como alternativa, você pode especificar um caminho de pesquisa de símbolo no parâmetro *UserSearchPath* da função [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) .</span><span class="sxs-lookup"><span data-stu-id="fd111-109">Alternatively, you can specify a symbol search path in the *UserSearchPath* parameter of the [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function.</span></span>

<span data-ttu-id="fd111-110">O parâmetro *UserSearchPath* em [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) e o parâmetro *SearchPath* em [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) usam um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um caminho ou uma série de caminhos separados por um ponto-e-vírgula.</span><span class="sxs-lookup"><span data-stu-id="fd111-110">The *UserSearchPath* parameter in [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) and the *SearchPath* parameter in [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) take a pointer to a null-terminated string that specifies a path, or series of paths separated by a semicolon.</span></span> <span data-ttu-id="fd111-111">O manipulador de símbolo usa esses caminhos para pesquisar arquivos de símbolo.</span><span class="sxs-lookup"><span data-stu-id="fd111-111">The symbol handler uses these paths to search for symbol files.</span></span> <span data-ttu-id="fd111-112">Se esse parâmetro for **nulo**, o manipulador de símbolo pesquisará o diretório que contém o módulo para o qual os símbolos estão sendo pesquisados.</span><span class="sxs-lookup"><span data-stu-id="fd111-112">If this parameter is **NULL**, the symbol handler searches the directory that contains the module for which symbols are being searched.</span></span> <span data-ttu-id="fd111-113">Caso contrário, se esse parâmetro for especificado como um valor não **nulo** , o manipulador de símbolo primeiro pesquisará os caminhos definidos pelo aplicativo antes de Pesquisar o diretório do módulo.</span><span class="sxs-lookup"><span data-stu-id="fd111-113">Otherwise, if this parameter is specified as a non-**NULL** value, the symbol handler first searches the paths set by the application before searching the module directory.</span></span> <span data-ttu-id="fd111-114">Se você definir o \_ caminho do símbolo do NT \_ \_ ou a \_ \_ \_ \_ variável de ambiente do caminho do símbolo do NT Alt, o manipulador de símbolos pesquisará os arquivos de símbolo na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="fd111-114">If you set the \_NT\_SYMBOL\_PATH or \_NT\_ALT\_SYMBOL\_PATH environment variable, the symbol handler searches for symbol files in the following order:</span></span>

1. <span data-ttu-id="fd111-115">A \_ \_ variável de ambiente do caminho do símbolo NT \_ .</span><span class="sxs-lookup"><span data-stu-id="fd111-115">The \_NT\_SYMBOL\_PATH environment variable.</span></span>
2. <span data-ttu-id="fd111-116">A \_ \_ variável de ambiente do caminho do símbolo Alt do NT \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="fd111-116">The \_NT\_ALT\_SYMBOL\_PATH environment variable.</span></span>
3. <span data-ttu-id="fd111-117">O diretório que contém o módulo correspondente.</span><span class="sxs-lookup"><span data-stu-id="fd111-117">The directory that contains the corresponding module.</span></span>

<span data-ttu-id="fd111-118">Para recuperar os caminhos de pesquisa, chame a função [**SymGetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsearchpath) .</span><span class="sxs-lookup"><span data-stu-id="fd111-118">To retrieve the search paths, call the [**SymGetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsearchpath) function.</span></span>

<span data-ttu-id="fd111-119">O caminho de pesquisa para arquivos do banco de dados do programa (. pdb) é diferente do caminho para arquivos de depuração (. dbg).</span><span class="sxs-lookup"><span data-stu-id="fd111-119">The search path for program database (.pdb) files is different than the path for debug (.dbg) files.</span></span> <span data-ttu-id="fd111-120">O algoritmo é determinado pela funcionalidade da biblioteca de símbolos.</span><span class="sxs-lookup"><span data-stu-id="fd111-120">The algorithm is determined by the functionality of the symbol library.</span></span> <span data-ttu-id="fd111-121">Por padrão, o Microsoft Visual C/C++ cria símbolos de formato da Microsoft, os retira da imagem e os coloca em um arquivo. pdb separado.</span><span class="sxs-lookup"><span data-stu-id="fd111-121">By default, Microsoft Visual C/C++ creates Microsoft format symbols, strips them from the image, and places them in a separate .pdb file.</span></span> <span data-ttu-id="fd111-122">Normalmente, o arquivo. pdb estará localizado no diretório que contém a imagem executável.</span><span class="sxs-lookup"><span data-stu-id="fd111-122">Typically, the .pdb file will be located in the directory that contains the executable image.</span></span> <span data-ttu-id="fd111-123">O Visual C/C++ incorpora o caminho absoluto para o arquivo. pdb na imagem executável.</span><span class="sxs-lookup"><span data-stu-id="fd111-123">Visual C/C++ embeds the absolute path to the .pdb file in the executable image.</span></span> <span data-ttu-id="fd111-124">Se o manipulador de símbolo não encontrar o arquivo. pdb nesse local ou se o arquivo. pdb foi movido para outro diretório, o manipulador de símbolo localizará o arquivo. pdb usando o caminho de pesquisa descrito para os arquivos. dbg.</span><span class="sxs-lookup"><span data-stu-id="fd111-124">If the symbol handler cannot find the .pdb file in that location or if the .pdb file was moved to another directory, the symbol handler will locate the .pdb file using the search path described for .dbg files.</span></span>

## <a name="path-element-types"></a><span data-ttu-id="fd111-125">Tipos de elemento Path</span><span class="sxs-lookup"><span data-stu-id="fd111-125">Path Element Types</span></span>

<span data-ttu-id="fd111-126">Há três tipos de elementos Path.</span><span class="sxs-lookup"><span data-stu-id="fd111-126">There are three types of path elements.</span></span>

### <a name="standard-path-element"></a><span data-ttu-id="fd111-127">Elemento de caminho padrão</span><span class="sxs-lookup"><span data-stu-id="fd111-127">Standard Path Element</span></span>

<span data-ttu-id="fd111-128">Um elemento Path padrão é pesquisado procurando na raiz do diretório especificado pelo elemento Path.</span><span class="sxs-lookup"><span data-stu-id="fd111-128">A standard path element is searched by looking in the root of the directory specified by the path element.</span></span> <span data-ttu-id="fd111-129">O manipulador de símbolo também procura em um subdiretório de "Symbols" que corresponde à extensão de arquivo do módulo que os símbolos estão sendo procurados.</span><span class="sxs-lookup"><span data-stu-id="fd111-129">The symbol handler also looks in a subdirectory of "symbols" that matches the file extension of the module that symbols are being looked for.</span></span> <span data-ttu-id="fd111-130">Normalmente, é "dll", "exe" ou "sys".</span><span class="sxs-lookup"><span data-stu-id="fd111-130">This is typically "dll", "exe", or "sys".</span></span> <span data-ttu-id="fd111-131">Por fim, ele procura em um subdiretório chamado "Symbols" com um diretório com o mesmo nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="fd111-131">Lastly, it looks in a subdirectory called "symbols" with a directory of the same name as the extension.</span></span> <span data-ttu-id="fd111-132">Por exemplo, se o elemento de caminho do símbolo for "c: \\ Mysymbols" e o arquivo para o qual os símbolos estão sendo pesquisados for "boo.dll", os seguintes diretórios serão pesquisados.</span><span class="sxs-lookup"><span data-stu-id="fd111-132">For example, if the symbol path element is "c:\\mySymbols" and the file that symbols are being searched for is "boo.dll", then the following directories would be searched.</span></span>

- <span data-ttu-id="fd111-133">c: \\ Mysymbols</span><span class="sxs-lookup"><span data-stu-id="fd111-133">c:\\mySymbols</span></span>  
- <span data-ttu-id="fd111-134">c: \\ Mysymbols \\ dll</span><span class="sxs-lookup"><span data-stu-id="fd111-134">c:\\mySymbols\\dll</span></span>  
- <span data-ttu-id="fd111-135">DLL de \\ símbolos c: Mysymbols \\ \\</span><span class="sxs-lookup"><span data-stu-id="fd111-135">c:\\mySymbols\\symbols\\dll</span></span>  

<span data-ttu-id="fd111-136">O manipulador de símbolo usa essa lógica para pesquisar qualquer elemento de caminho que não atenda aos critérios para ser um *servidor de símbolos* ou *cache* (descrito abaixo).</span><span class="sxs-lookup"><span data-stu-id="fd111-136">The symbol handler uses this logic to search any path element that does not meet the criteria to be a *symbol server* or *cache* (described below).</span></span>

### <a name="symbol-server-path-element"></a><span data-ttu-id="fd111-137">Elemento de caminho do servidor Symbol</span><span class="sxs-lookup"><span data-stu-id="fd111-137">Symbol Server Path Element</span></span>

<span data-ttu-id="fd111-138">Um elemento de caminho de *servidor de símbolos* usa uma tecnologia especial que pode localizar um símbolo que seja uma correspondência exata para o módulo em questão.</span><span class="sxs-lookup"><span data-stu-id="fd111-138">A *symbol server* path element uses special technology that can locate a symbol that is an exact match for the module in question.</span></span> <span data-ttu-id="fd111-139">Consulte [usando symsrv](using-symsrv.md) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="fd111-139">See [Using SymSrv](using-symsrv.md) for more details.</span></span>

<span data-ttu-id="fd111-140">O manipulador de símbolos trata um elemento Path como um servidor de símbolos se ele começa com o texto "SRV \* ".</span><span class="sxs-lookup"><span data-stu-id="fd111-140">The symbol handler treats a path element as a symbol server if it begins with the text, "srv\*".</span></span>

> [!Note]  
> <span data-ttu-id="fd111-141">Se o texto "SRV \* " não for especificado, mas o elemento de caminho real for um armazenamento de servidor de símbolos, o manipulador de símbolo atuará como se "SRV \* " fosse especificado.</span><span class="sxs-lookup"><span data-stu-id="fd111-141">If the "srv\*" text is not specified but the actual path element is a symbol server store, then the symbol handler will act as if "srv\*" were specified.</span></span> <span data-ttu-id="fd111-142">O manipulador de símbolos faz essa determinação pesquisando a existência de um arquivo chamado "pingme.txt" no diretório raiz do caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="fd111-142">The symbol handler makes this determination by searching for the existence of a file called "pingme.txt" in the root directory of the specified path.</span></span>

 

### <a name="cache-path-element"></a><span data-ttu-id="fd111-143">Elemento de caminho de cache</span><span class="sxs-lookup"><span data-stu-id="fd111-143">Cache Path Element</span></span>

<span data-ttu-id="fd111-144">Um elemento de caminho de *cache* é uma variação em um elemento de caminho de servidor de símbolo.</span><span class="sxs-lookup"><span data-stu-id="fd111-144">A *cache* path element is a variation on a symbol server path element.</span></span>

<span data-ttu-id="fd111-145">Esse diretório é pesquisado como qualquer outro servidor de símbolos.</span><span class="sxs-lookup"><span data-stu-id="fd111-145">This directory is searched like any other symbol server.</span></span> <span data-ttu-id="fd111-146">No entanto, se o símbolo não for encontrado aqui e for encontrado em um elemento Path mais distante da cadeia do caminho do símbolo, o símbolo será copiado e armazenado no servidor de símbolos especificado neste elemento.</span><span class="sxs-lookup"><span data-stu-id="fd111-146">However, if the symbol is not found here and it is found in a path element farther down the chain of the symbol path, then the symbol will be copied and stored in the symbol server specified in this element.</span></span>

<span data-ttu-id="fd111-147">O manipulador de símbolo trata um elemento Path como um elemento de cache se ele começa com o texto "cache \* ".</span><span class="sxs-lookup"><span data-stu-id="fd111-147">The symbol handler treats a path element as a cache element if it begins with the text, "cache\*".</span></span> <span data-ttu-id="fd111-148">Para especificar um cache em "c: \\ myCache", use um elemento de caminho de símbolo de "cache \* c: \\ myCache".</span><span class="sxs-lookup"><span data-stu-id="fd111-148">To specify a cache in "c:\\myCache", use a symbol path element of "cache\*c:\\myCache".</span></span>

## <a name="example-search-path"></a><span data-ttu-id="fd111-149">Exemplo de caminho de pesquisa</span><span class="sxs-lookup"><span data-stu-id="fd111-149">Example Search Path</span></span>

<span data-ttu-id="fd111-150">Para ver como isso funciona, defina este caminho de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="fd111-150">To see how this works, set this search path.</span></span>

`cache*c:\myCache;srv*\\symbols\symbols`

<!-- 
See example from https://docs.microsoft.com/windows-hardware/drivers/debugger/symbol-path
cache*c:\MySymbols;srv*https://msdl.microsoft.com/download/symbols
-->

<span data-ttu-id="fd111-151">A seguir está uma lista da saída detalhada do manipulador de símbolos ao procurar o ntdll. pdb, usando o caminho de pesquisa listado acima.</span><span class="sxs-lookup"><span data-stu-id="fd111-151">The following is a listing of the symbol handler's verbose output while searching for ntdll.pdb, using the above listed search path.</span></span>

```
DBGHELP: .\ntdll.pdb - file not found
DBGHELP: .\dll\ntdll.pdb - file not found
DBGHELP: .\symbols\dll\ntdll.pdb - file not found
SYMSRV: c:\myCache\ntdll.pdb\0F7FCF88442F4B0E9FB51DC4A754D9DE2\ntdll.pdb not found
SYMSRV: ntdll.pdb from \\symbols\symbols: 10497024 bytes - copied
DBGHELP: c:\myCache\ntdll.pdb\0F7FCF88442F4B0E9FB51DC4A754D9DE2\ntdll.pdb already cached
DBGHELP: ntdll - private symbols & lines
c:\myCache\ntdll.pdb\0F7FCF88442F4B0E9FB51DC4A754D9DE2\ntdll.pdb
```

<span data-ttu-id="fd111-152">As três primeiras linhas da saída mostram o manipulador de símbolo que processa o primeiro elemento Path de `.` .</span><span class="sxs-lookup"><span data-stu-id="fd111-152">The first three lines of output show the symbol handler processing the first path element of `.`.</span></span> <span data-ttu-id="fd111-153">Este é um elemento de caminho padrão.</span><span class="sxs-lookup"><span data-stu-id="fd111-153">This is a standard path element.</span></span>

<span data-ttu-id="fd111-154">A quarta linha mostra o manipulador de símbolo usando o servidor de símbolos para procurar o arquivo no segundo elemento Path, `cache*c:\myCache` que é um elemento de caminho de cache.</span><span class="sxs-lookup"><span data-stu-id="fd111-154">The fourth line shows the symbol handler using the symbol server to look for the file in the second path element of `cache*c:\myCache` which is a cache path element.</span></span>

<span data-ttu-id="fd111-155">A quinta linha mostra que o arquivo está localizado no terceiro elemento Path de `srv*\\symbols\symbols` , que é um elemento Path do servidor Symbol.</span><span class="sxs-lookup"><span data-stu-id="fd111-155">The fifth line shows the file is found in the third path element of `srv*\\symbols\symbols`, which is a symbol server path element.</span></span>

<span data-ttu-id="fd111-156">A sexta linha mostra que o arquivo é copiado para o cache.</span><span class="sxs-lookup"><span data-stu-id="fd111-156">The sixth line shows that the file is copied to the cache.</span></span>

<span data-ttu-id="fd111-157">As duas últimas linhas em que o arquivo é aberto do cache.</span><span class="sxs-lookup"><span data-stu-id="fd111-157">The last two lines that the file is opened from the cache.</span></span>

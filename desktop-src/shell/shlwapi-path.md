---
description: Esta seção descreve as funções de manipulação de caminho do shell do Windows. Os elementos de programação explicados nesta documentação são exportados por Shlwapi.dll e definidos em Shlwapi. h e shlwapi. lib.
title: Funções de manipulação de caminho do Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 31c4afa9-2030-4714-a98b-ed895c9c28a0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8ed0a5e0f2e91a2e647af461ee6679a5542d28b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989081"
---
# <a name="shell-path-handling-functions"></a><span data-ttu-id="7891c-104">Funções de manipulação de caminho do Shell</span><span class="sxs-lookup"><span data-stu-id="7891c-104">Shell Path Handling Functions</span></span>

<span data-ttu-id="7891c-105">Esta seção descreve as funções de manipulação de caminho do shell do Windows.</span><span class="sxs-lookup"><span data-stu-id="7891c-105">This section describes the Windows Shell path handling functions.</span></span> <span data-ttu-id="7891c-106">Os elementos de programação explicados nesta documentação são exportados por Shlwapi.dll e definidos em Shlwapi. h e shlwapi. lib.</span><span class="sxs-lookup"><span data-stu-id="7891c-106">The programming elements explained in this documentation are exported by Shlwapi.dll and defined in Shlwapi.h and Shlwapi.lib.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7891c-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="7891c-107">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7891c-108">Tópico</span><span class="sxs-lookup"><span data-stu-id="7891c-108">Topic</span></span></th>
<th><span data-ttu-id="7891c-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="7891c-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7891c-110"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddbackslasha"><strong>PathAddBackslash</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-110"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddbackslasha"><strong>PathAddBackslash</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-111">Adiciona uma barra invertida ao final de uma cadeia de caracteres para criar a sintaxe correta para um caminho.</span><span class="sxs-lookup"><span data-stu-id="7891c-111">Adds a backslash to the end of a string to create the correct syntax for a path.</span></span> <span data-ttu-id="7891c-112">Se o caminho de origem já tiver uma barra invertida à direita, nenhuma barra invertida será adicionada.</span><span class="sxs-lookup"><span data-stu-id="7891c-112">If the source path already has a trailing backslash, no backslash will be added.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7891c-113">O uso indevido dessa função pode levar a uma saturação do buffer.</span><span class="sxs-lookup"><span data-stu-id="7891c-113">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="7891c-114">Recomendamos o uso da função <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslash"><strong>PathCchAddBackslash</strong></a> ou <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslashex"><strong>PathCchAddBackslashEx</strong></a> mais segura em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="7891c-114">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslash"><strong>PathCchAddBackslash</strong></a> or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslashex"><strong>PathCchAddBackslashEx</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-115"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddextensiona"><strong>PathAddExtension</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-115"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddextensiona"><strong>PathAddExtension</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-116">Adiciona uma extensão de nome de arquivo a uma cadeia de caracteres de caminho.</span><span class="sxs-lookup"><span data-stu-id="7891c-116">Adds a file name extension to a path string.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7891c-117">O uso indevido dessa função pode levar a uma saturação do buffer.</span><span class="sxs-lookup"><span data-stu-id="7891c-117">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="7891c-118">Recomendamos o uso da função <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddextension"><strong>PathCchAddExtension</strong></a> mais segura em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="7891c-118">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddextension"><strong>PathCchAddExtension</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-119"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathappenda"><strong>PathAppend</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-119"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathappenda"><strong>PathAppend</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-120">Anexa um caminho ao final de outro.</span><span class="sxs-lookup"><span data-stu-id="7891c-120">Appends one path to the end of another.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7891c-121">O uso indevido dessa função pode levar a uma saturação do buffer.</span><span class="sxs-lookup"><span data-stu-id="7891c-121">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="7891c-122">Recomendamos o uso da função <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappend"><strong>PathCchAppend</strong></a> ou <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappendex"><strong>PathCchAppendEx</strong></a> mais segura em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="7891c-122">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappend"><strong>PathCchAppend</strong></a> or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappendex"><strong>PathCchAppendEx</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-123"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathbuildroota"><strong>PathBuildRoot</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-123"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathbuildroota"><strong>PathBuildRoot</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-124">Cria um caminho raiz a partir de um determinado número de unidade.</span><span class="sxs-lookup"><span data-stu-id="7891c-124">Creates a root path from a given drive number.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-125"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcanonicalizea"><strong>PathCanonicalize</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-125"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcanonicalizea"><strong>PathCanonicalize</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-126">Simplifica um caminho removendo elementos de navegação, como &quot; . &quot; e &quot; .. &quot; para produzir um caminho direto e bem formado.</span><span class="sxs-lookup"><span data-stu-id="7891c-126">Simplifies a path by removing navigation elements such as &quot;.&quot; and &quot;..&quot; to produce a direct, well-formed path.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-127"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcombinea"><strong>PathCombine</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-127"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcombinea"><strong>PathCombine</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-128">Concatena duas cadeias de caracteres que representam caminhos corretamente formados em um caminho; também concatena qualquer elemento de caminho relativo.</span><span class="sxs-lookup"><span data-stu-id="7891c-128">Concatenates two strings that represent properly formed paths into one path; also concatenates any relative path elements.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7891c-129">O uso indevido dessa função pode levar a uma saturação do buffer.</span><span class="sxs-lookup"><span data-stu-id="7891c-129">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="7891c-130">Recomendamos o uso da função <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombine"><strong>PathCchCombine</strong></a> ou <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombineex"><strong>PathCchCombineEx</strong></a> mais segura em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="7891c-130">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombine"><strong>PathCchCombine</strong></a> or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombineex"><strong>PathCchCombineEx</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-131"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcommonprefixa"><strong>PathCommonPrefix</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-131"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcommonprefixa"><strong>PathCommonPrefix</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-132">Compara dois caminhos para determinar se eles compartilham um prefixo comum.</span><span class="sxs-lookup"><span data-stu-id="7891c-132">Compares two paths to determine if they share a common prefix.</span></span> <span data-ttu-id="7891c-133">Um prefixo é um destes tipos: &quot; C: \\ &quot; , &quot; . &quot; , &quot; .. &quot; , &quot; .. \\ &quot; .</span><span class="sxs-lookup"><span data-stu-id="7891c-133">A prefix is one of these types: &quot;C:\\&quot;, &quot;.&quot;, &quot;..&quot;, &quot;..\\&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-134"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>PathCompactPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-134"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>PathCompactPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-135">Trunca um caminho de arquivo para caber em uma determinada largura de pixel, substituindo os componentes de caminho por reticências.</span><span class="sxs-lookup"><span data-stu-id="7891c-135">Truncates a file path to fit within a given pixel width by replacing path components with ellipses.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-136"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpathexa"><strong>PathCompactPathEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-136"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpathexa"><strong>PathCompactPathEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-137">Trunca um caminho para caber em um determinado número de caracteres, substituindo os componentes de caminho por reticências.</span><span class="sxs-lookup"><span data-stu-id="7891c-137">Truncates a path to fit within a certain number of characters by replacing path components with ellipses.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-138"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurla"><strong>PathCreateFromUrl</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-138"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurla"><strong>PathCreateFromUrl</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-139">Converte uma URL de arquivo em um caminho do Microsoft MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="7891c-139">Converts a file URL to a Microsoft MS-DOS path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-140"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurlalloc"><strong>PathCreateFromUrlAlloc</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-140"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurlalloc"><strong>PathCreateFromUrlAlloc</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-141">Cria um caminho a partir de uma URL de arquivo.</span><span class="sxs-lookup"><span data-stu-id="7891c-141">Creates a path from a file URL.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-142"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfileexistsa"><strong>PathFileExists</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-142"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfileexistsa"><strong>PathFileExists</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-143">Determina se um caminho para um objeto do sistema de arquivos, como um arquivo ou uma pasta, é válido.</span><span class="sxs-lookup"><span data-stu-id="7891c-143">Determines whether a path to a file system object such as a file or folder is valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-144"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindextensiona"><strong>PathFindExtension</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-144"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindextensiona"><strong>PathFindExtension</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-145">Pesquisa um caminho para uma extensão.</span><span class="sxs-lookup"><span data-stu-id="7891c-145">Searches a path for an extension.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-146"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindfilenamea"><strong>PathFindFileName</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-146"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindfilenamea"><strong>PathFindFileName</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-147">Pesquisa um caminho para um nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="7891c-147">Searches a path for a file name.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-148"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindnextcomponenta"><strong>PathFindNextComponent</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-148"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindnextcomponenta"><strong>PathFindNextComponent</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-149">Analisa um caminho e retorna a parte desse caminho que segue a primeira barra invertida.</span><span class="sxs-lookup"><span data-stu-id="7891c-149">Parses a path and returns the portion of that path that follows the first backslash.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-150"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindonpatha"><strong>PathFindOnPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-150"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindonpatha"><strong>PathFindOnPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-151">Procura um arquivo.</span><span class="sxs-lookup"><span data-stu-id="7891c-151">Searches for a file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-152"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindsuffixarraya"><strong>PathFindSuffixArray</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-152"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindsuffixarraya"><strong>PathFindSuffixArray</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-153">Determina se um determinado nome de arquivo tem uma lista de sufixos.</span><span class="sxs-lookup"><span data-stu-id="7891c-153">Determines whether a given file name has one of a list of suffixes.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-154"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetargsa"><strong>PathGetArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-154"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetargsa"><strong>PathGetArgs</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-155">Localiza os argumentos de linha de comando em um determinado caminho.</span><span class="sxs-lookup"><span data-stu-id="7891c-155">Finds the command line arguments within a given path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-156"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetchartypea"><strong>PathGetCharType</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-156"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetchartypea"><strong>PathGetCharType</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-157">Determina o tipo de caractere em relação a um caminho.</span><span class="sxs-lookup"><span data-stu-id="7891c-157">Determines the type of character in relation to a path.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-158"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetdrivenumbera"><strong>PathGetDriveNumber</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-158"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetdrivenumbera"><strong>PathGetDriveNumber</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-159">Pesquisa um caminho para uma letra de unidade dentro do intervalo de ' A ' para ' Z ' e retorna o número da unidade correspondente.</span><span class="sxs-lookup"><span data-stu-id="7891c-159">Searches a path for a drive letter within the range of 'A' to 'Z' and returns the corresponding drive number.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-160"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathiscontenttypea"><strong>PathIsContentType</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-160"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathiscontenttypea"><strong>PathIsContentType</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-161">Determina se o tipo de conteúdo registrado de um arquivo corresponde ao tipo de conteúdo especificado.</span><span class="sxs-lookup"><span data-stu-id="7891c-161">Determines if a file's registered content type matches the specified content type.</span></span> <span data-ttu-id="7891c-162">Essa função obtém o tipo de conteúdo para o tipo de arquivo especificado e compara essa cadeia de caracteres com o <em>pszContentType</em>.</span><span class="sxs-lookup"><span data-stu-id="7891c-162">This function obtains the content type for the specified file type and compares that string with the <em>pszContentType</em>.</span></span> <span data-ttu-id="7891c-163">A comparação não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="7891c-163">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-164"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectorya"><strong>PathIsDirectory</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-164"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectorya"><strong>PathIsDirectory</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-165">Verifica se um caminho é um diretório válido.</span><span class="sxs-lookup"><span data-stu-id="7891c-165">Verifies that a path is a valid directory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-166"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectoryemptya"><strong>PathIsDirectoryEmpty</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-166"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectoryemptya"><strong>PathIsDirectoryEmpty</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-167">Determina se um caminho especificado é um diretório vazio.</span><span class="sxs-lookup"><span data-stu-id="7891c-167">Determines whether a specified path is an empty directory.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-168"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisfilespeca"><strong>PathIsFileSpec</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-168"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisfilespeca"><strong>PathIsFileSpec</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-169">Pesquisa um caminho para qualquer caractere delimitador de caminho (por exemplo, ': ' ou ' \' ).</span><span class="sxs-lookup"><span data-stu-id="7891c-169">Searches a path for any path-delimiting characters (for example, ':' or '\' ).</span></span> <span data-ttu-id="7891c-170">Se não houver nenhum caractere delimitador de caminho presente, o caminho será considerado como um caminho de especificação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="7891c-170">If there are no path-delimiting characters present, the path is considered to be a File Spec path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-171"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathishtmlfilea"><strong>PathIsHTMLFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-171"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathishtmlfilea"><strong>PathIsHTMLFile</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-172">Determina se um arquivo é um arquivo HTML.</span><span class="sxs-lookup"><span data-stu-id="7891c-172">Determines if a file is an HTML file.</span></span> <span data-ttu-id="7891c-173">A determinação é feita com base no tipo de conteúdo registrado para a extensão do arquivo.</span><span class="sxs-lookup"><span data-stu-id="7891c-173">The determination is made based on the content type that is registered for the file's extension.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-174"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathislfnfilespeca"><strong>PathIsLFNFileSpec</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-174"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathislfnfilespeca"><strong>PathIsLFNFileSpec</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-175">Determina se um nome de arquivo está em formato longo.</span><span class="sxs-lookup"><span data-stu-id="7891c-175">Determines whether a file name is in long format.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-176"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisnetworkpatha"><strong>PathIsNetworkPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-176"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisnetworkpatha"><strong>PathIsNetworkPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-177">Determina se uma cadeia de caracteres de caminho representa um recurso de rede.</span><span class="sxs-lookup"><span data-stu-id="7891c-177">Determines whether a path string represents a network resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-178"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisprefixa"><strong>PathIsPrefix</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-178"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisprefixa"><strong>PathIsPrefix</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-179">Pesquisa um caminho para determinar se ele contém um prefixo válido do tipo passado por <em>pszPrefix</em>.</span><span class="sxs-lookup"><span data-stu-id="7891c-179">Searches a path to determine if it contains a valid prefix of the type passed by <em>pszPrefix</em>.</span></span> <span data-ttu-id="7891c-180">Um prefixo é um destes tipos: &quot; C: \\ &quot; , &quot; . &quot; , &quot; .. &quot; , &quot; .. \\ &quot; .</span><span class="sxs-lookup"><span data-stu-id="7891c-180">A prefix is one of these types: &quot;C:\\&quot;, &quot;.&quot;, &quot;..&quot;, &quot;..\\&quot;.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-181"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisrelativea"><strong>PathIsRelative</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-181"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisrelativea"><strong>PathIsRelative</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-182">Pesquisa um caminho e determina se ele é relativo.</span><span class="sxs-lookup"><span data-stu-id="7891c-182">Searches a path and determines if it is relative.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-183"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisroota"><strong>PathIsRoot</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-183"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisroota"><strong>PathIsRoot</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-184">Determina se uma cadeia de caracteres de caminho se refere à raiz de um volume.</span><span class="sxs-lookup"><span data-stu-id="7891c-184">Determines whether a path string refers to the root of a volume.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-185"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissameroota"><strong>PathIsSameRoot</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-185"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissameroota"><strong>PathIsSameRoot</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-186">Compara dois caminhos para determinar se eles têm um componente raiz comum.</span><span class="sxs-lookup"><span data-stu-id="7891c-186">Compares two paths to determine if they have a common root component.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-187"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissystemfoldera"><strong>PathIsSystemFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-187"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissystemfoldera"><strong>PathIsSystemFolder</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-188">Determina se uma pasta existente contém os atributos que o tornam uma pasta do sistema.</span><span class="sxs-lookup"><span data-stu-id="7891c-188">Determines if an existing folder contains the attributes that make it a system folder.</span></span> <span data-ttu-id="7891c-189">Como alternativa, essa função indica se determinados atributos qualificam uma pasta para ser uma pasta do sistema.</span><span class="sxs-lookup"><span data-stu-id="7891c-189">Alternately, this function indicates if certain attributes qualify a folder to be a system folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-190"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisunca"><strong>PathIsUNC</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-190"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisunca"><strong>PathIsUNC</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-191">Determina se uma cadeia de caracteres de caminho é um caminho UNC (Convenção Universal de nomenclatura) válido, em oposição a um caminho com base em uma letra de unidade.</span><span class="sxs-lookup"><span data-stu-id="7891c-191">Determines if a path string is a valid Universal Naming Convention (UNC) path, as opposed to a path based on a drive letter.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-192"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncservera"><strong>PathIsUNCServer</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-192"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncservera"><strong>PathIsUNCServer</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-193">Determina se uma cadeia de caracteres é um UNC válido apenas para um caminho de servidor.</span><span class="sxs-lookup"><span data-stu-id="7891c-193">Determines if a string is a valid UNC for a server path only.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-194"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncserversharea"><strong>PathIsUNCServerShare</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-194"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncserversharea"><strong>PathIsUNCServerShare</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-195">Determina se uma cadeia de caracteres é um caminho de compartilhamento UNC válido, \\ <em>compartilhamento do servidor</em> \ <em></em>.</span><span class="sxs-lookup"><span data-stu-id="7891c-195">Determines if a string is a valid UNC share path, \\<em>server</em>\<em>share</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-196"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisurla"><strong>PathIsURL</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-196"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisurla"><strong>PathIsURL</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-197">Testa uma determinada cadeia de caracteres para determinar se está em conformidade com um formato de URL válido.</span><span class="sxs-lookup"><span data-stu-id="7891c-197">Tests a given string to determine if it conforms to a valid URL format.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-198"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakeprettya"><strong>PathMakePretty</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-198"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakeprettya"><strong>PathMakePretty</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-199">Converte um caminho com maiúsculas e minúsculas em todos os caracteres minúsculos para dar ao caminho uma aparência consistente.</span><span class="sxs-lookup"><span data-stu-id="7891c-199">Converts an all-uppercase path to all lowercase characters to give the path a consistent appearance.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-200"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera"><strong>PathMakeSystemFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-200"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera"><strong>PathMakeSystemFolder</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-201">Dá a uma pasta existente os atributos adequados para se tornarem uma pasta do sistema.</span><span class="sxs-lookup"><span data-stu-id="7891c-201">Gives an existing folder the proper attributes to become a system folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-202"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspeca"><strong>PathMatchSpec</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-202"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspeca"><strong>PathMatchSpec</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-203">Pesquisa uma cadeia de caracteres usando um tipo de correspondência curinga do MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="7891c-203">Searches a string using a MS-DOS wildcard match type.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-204"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspecexa"><strong>PathMatchSpecEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-204"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspecexa"><strong>PathMatchSpecEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-205">Corresponde a um nome de arquivo de um caminho em relação a um ou mais padrões de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="7891c-205">Matches a file name from a path against one or more file name patterns.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-206"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa"><strong>PathParseIconLocation</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-206"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa"><strong>PathParseIconLocation</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-207">Analisa uma cadeia de caracteres de local de arquivo que contém um local de arquivo e um índice de ícone e retorna valores separados.</span><span class="sxs-lookup"><span data-stu-id="7891c-207">Parses a file location string that contains a file location and icon index, and returns separate values.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-208"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathquotespacesa"><strong>PathQuoteSpaces</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-208"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathquotespacesa"><strong>PathQuoteSpaces</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-209">Pesquisa um caminho em busca de espaços.</span><span class="sxs-lookup"><span data-stu-id="7891c-209">Searches a path for spaces.</span></span> <span data-ttu-id="7891c-210">Se forem encontrados espaços, o caminho inteiro será colocado entre aspas.</span><span class="sxs-lookup"><span data-stu-id="7891c-210">If spaces are found, the entire path is enclosed in quotation marks.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-211"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrelativepathtoa"><strong>PathRelativePathTo</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-211"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrelativepathtoa"><strong>PathRelativePathTo</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-212">Cria um caminho relativo de um arquivo ou pasta para outro.</span><span class="sxs-lookup"><span data-stu-id="7891c-212">Creates a relative path from one file or folder to another.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-213"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveargsa"><strong>PathRemoveArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-213"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveargsa"><strong>PathRemoveArgs</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-214">Remove todos os argumentos de um determinado caminho.</span><span class="sxs-lookup"><span data-stu-id="7891c-214">Removes any arguments from a given path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-215"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovebackslasha"><strong>PathRemoveBackslash</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-215"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovebackslasha"><strong>PathRemoveBackslash</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-216">Remove a barra invertida à direita de um determinado caminho.</span><span class="sxs-lookup"><span data-stu-id="7891c-216">Removes the trailing backslash from a given path.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7891c-217">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="7891c-217">This function is deprecated.</span></span> <span data-ttu-id="7891c-218">Recomendamos o uso da função <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslash"><strong>PathCchRemoveBackslash</strong></a> ou <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslashex"><strong>PathCchRemoveBackslashEx</strong></a> em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="7891c-218">We recommend the use of the <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslash"><strong>PathCchRemoveBackslash</strong></a> or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslashex"><strong>PathCchRemoveBackslashEx</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-219"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveblanksa"><strong>PathRemoveBlanks</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-219"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveblanksa"><strong>PathRemoveBlanks</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-220">Remove todos os espaços à esquerda e à direita de uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7891c-220">Removes all leading and trailing spaces from a string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-221"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveextensiona"><strong>PathRemoveExtension</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-221"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveextensiona"><strong>PathRemoveExtension</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-222">Remove a extensão de nome de arquivo de um caminho, se houver uma.</span><span class="sxs-lookup"><span data-stu-id="7891c-222">Removes the file name extension from a path, if one is present.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7891c-223">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="7891c-223">This function is deprecated.</span></span> <span data-ttu-id="7891c-224">Recomendamos o uso do <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremoveextension"><strong>PathCchRemoveExtension</strong></a> em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="7891c-224">We recommend the use of the <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremoveextension"><strong>PathCchRemoveExtension</strong></a> in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-225"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovefilespeca"><strong>PathRemoveFileSpec</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-225"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovefilespeca"><strong>PathRemoveFileSpec</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-226">Remove o nome de arquivo à direita e a barra invertida de um caminho, se estiverem presentes.</span><span class="sxs-lookup"><span data-stu-id="7891c-226">Removes the trailing file name and backslash from a path, if they are present.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7891c-227">Esta função é preterida.</span><span class="sxs-lookup"><span data-stu-id="7891c-227">This function is deprecated.</span></span> <span data-ttu-id="7891c-228">Recomendamos o uso da função <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovefilespec"><strong>PathCchRemoveFileSpec</strong></a> em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="7891c-228">We recommend the use of the <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovefilespec"><strong>PathCchRemoveFileSpec</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-229"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrenameextensiona"><strong>PathRenameExtension</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-229"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrenameextensiona"><strong>PathRenameExtension</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-230">Substitui a extensão de um nome de arquivo por uma nova extensão.</span><span class="sxs-lookup"><span data-stu-id="7891c-230">Replaces the extension of a file name with a new extension.</span></span> <span data-ttu-id="7891c-231">Se o nome do arquivo não contiver uma extensão, a extensão será anexada ao final da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7891c-231">If the file name does not contain an extension, the extension will be attached to the end of the string.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7891c-232">O uso indevido dessa função pode levar a uma saturação do buffer.</span><span class="sxs-lookup"><span data-stu-id="7891c-232">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="7891c-233">Recomendamos o uso da função <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchrenameextension"><strong>PathCchRenameExtension</strong></a> mais segura em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="7891c-233">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchrenameextension"><strong>PathCchRenameExtension</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-234"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsearchandqualifya"><strong>PathSearchAndQualify</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-234"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsearchandqualifya"><strong>PathSearchAndQualify</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-235">Determina se um determinado caminho está formatado corretamente e totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="7891c-235">Determines if a given path is correctly formatted and fully qualified.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-236"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsetdlgitempatha"><strong>PathSetDlgItemPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-236"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsetdlgitempatha"><strong>PathSetDlgItemPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-237">Define o texto de um controle filho em uma janela ou caixa de diálogo, usando <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>PathCompactPath</strong></a> para garantir que o caminho caiba no controle.</span><span class="sxs-lookup"><span data-stu-id="7891c-237">Sets the text of a child control in a window or dialog box, using <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>PathCompactPath</strong></a> to ensure the path fits in the control.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-238"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathskiproota"><strong>PathSkipRoot</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-238"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathskiproota"><strong>PathSkipRoot</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-239">Recupera um ponteiro para o primeiro caractere em um caminho após a letra da unidade ou o servidor UNC/elementos do caminho de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="7891c-239">Retrieves a pointer to the first character in a path following the drive letter or UNC server/share path elements.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-240"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstrippatha"><strong>PathStripPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-240"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstrippatha"><strong>PathStripPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-241">Remove a parte do caminho de um caminho e arquivo totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="7891c-241">Removes the path portion of a fully qualified path and file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-242"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstriptoroota"><strong>PathStripToRoot</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-242"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstriptoroota"><strong>PathStripToRoot</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-243">Remove todos os elementos de arquivo e diretório em um caminho, exceto as informações de raiz.</span><span class="sxs-lookup"><span data-stu-id="7891c-243">Removes all file and directory elements in a path except for the root information.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7891c-244">O uso indevido dessa função pode levar a uma saturação do buffer.</span><span class="sxs-lookup"><span data-stu-id="7891c-244">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="7891c-245">Recomendamos o uso da função <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchstriptoroot"><strong>PathCchStripToRoot</strong></a> mais segura em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="7891c-245">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchstriptoroot"><strong>PathCchStripToRoot</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-246"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathundecoratea"><strong>PathUndecorate</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-246"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathundecoratea"><strong>PathUndecorate</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-247">Remove a decoração de uma cadeia de caracteres de caminho.</span><span class="sxs-lookup"><span data-stu-id="7891c-247">Removes the decoration from a path string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-248"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunexpandenvstringsa"><strong>PathUnExpandEnvStrings</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-248"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunexpandenvstringsa"><strong>PathUnExpandEnvStrings</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-249">Substitui determinados nomes de pasta em um caminho totalmente qualificado com sua cadeia de caracteres de ambiente associada.</span><span class="sxs-lookup"><span data-stu-id="7891c-249">Replaces certain folder names in a fully qualified path with their associated environment string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-250"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunmakesystemfoldera"><strong>PathUnmakeSystemFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-250"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunmakesystemfoldera"><strong>PathUnmakeSystemFolder</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-251">Remove os atributos de uma pasta que o tornam uma pasta do sistema.</span><span class="sxs-lookup"><span data-stu-id="7891c-251">Removes the attributes from a folder that make it a system folder.</span></span> <span data-ttu-id="7891c-252">Essa pasta deve realmente existir no sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="7891c-252">This folder must actually exist in the file system.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-253"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunquotespacesa"><strong>PathUnquoteSpaces</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-253"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunquotespacesa"><strong>PathUnquoteSpaces</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-254">Remove as aspas do início e do fim de um caminho.</span><span class="sxs-lookup"><span data-stu-id="7891c-254">Removes quotes from the beginning and end of a path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-255"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shskipjunction"><strong>SHSkipJunction</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-255"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shskipjunction"><strong>SHSkipJunction</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-256">Verifica um contexto de associação para ver se é seguro associar a um objeto de componente específico.</span><span class="sxs-lookup"><span data-stu-id="7891c-256">Checks a bind context to see if it is safe to bind to a particular component object.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-257"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlapplyschemea"><strong>UrlApplyScheme</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-257"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlapplyschemea"><strong>UrlApplyScheme</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-258">Determina um esquema para uma cadeia de caracteres de URL especificada e retorna uma cadeia de caracteres com um prefixo apropriado.</span><span class="sxs-lookup"><span data-stu-id="7891c-258">Determines a scheme for a specified URL string, and returns a string with an appropriate prefix.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-259"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcanonicalizea"><strong>UrlCanonicalize</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-259"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcanonicalizea"><strong>UrlCanonicalize</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-260">Converte uma cadeia de caracteres de URL em forma canônica.</span><span class="sxs-lookup"><span data-stu-id="7891c-260">Converts a URL string into canonical form.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-261"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcombinea"><strong>UrlCombine</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-261"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcombinea"><strong>UrlCombine</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-262">Quando fornecido com uma URL relativa e sua base, o retorna uma URL na forma canônica.</span><span class="sxs-lookup"><span data-stu-id="7891c-262">When provided with a relative URL and its base, returns a URL in canonical form.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-263"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcomparea"><strong>UrlCompare</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-263"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcomparea"><strong>UrlCompare</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-264">Faz uma comparação que diferencia maiúsculas de minúsculas de duas cadeias de caracteres de URL.</span><span class="sxs-lookup"><span data-stu-id="7891c-264">Makes a case-sensitive comparison of two URL strings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-265"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcreatefrompatha"><strong>UrlCreateFromPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-265"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcreatefrompatha"><strong>UrlCreateFromPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-266">Converte um caminho do MS-DOS em uma URL canônica.</span><span class="sxs-lookup"><span data-stu-id="7891c-266">Converts a MS-DOS path to a canonicalized URL.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-267"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapea"><strong>UrlEscape</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-267"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapea"><strong>UrlEscape</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-268">Converte caracteres ou pares substitutos em uma URL que pode ser alterada durante o transporte pela Internet ( &quot; caracteres não seguros &quot; ) em suas sequências de escape correspondentes.</span><span class="sxs-lookup"><span data-stu-id="7891c-268">Converts characters or surrogate pairs in a URL that might be altered during transport across the Internet (&quot;unsafe&quot; characters) into their corresponding escape sequences.</span></span> <span data-ttu-id="7891c-269">Os pares substitutos são caracteres entre U + 10000 a U + 10FFFF (em UTF-32) ou entre DC00 e DFFF (em UTF-16).</span><span class="sxs-lookup"><span data-stu-id="7891c-269">Surrogate pairs are characters between U+10000 to U+10FFFF (in UTF-32) or between DC00 to DFFF (in UTF-16).</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-270"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapespaces"><strong>UrlEscapeSpaces</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-270"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapespaces"><strong>UrlEscapeSpaces</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-271">Uma macro que converte caracteres de espaço em sua sequência de escape correspondente.</span><span class="sxs-lookup"><span data-stu-id="7891c-271">A macro that converts space characters into their corresponding escape sequence.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-272"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetlocationa"><strong>UrlGetLocation</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-272"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetlocationa"><strong>UrlGetLocation</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-273">Recupera o local de uma URL.</span><span class="sxs-lookup"><span data-stu-id="7891c-273">Retrieves the location from a URL.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-274"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetparta"><strong>UrlGetPart</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-274"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetparta"><strong>UrlGetPart</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-275">Aceita uma cadeia de caracteres de URL e retorna uma parte especificada dessa URL.</span><span class="sxs-lookup"><span data-stu-id="7891c-275">Accepts a URL string and returns a specified part of that URL.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-276"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlhasha"><strong>UrlHash</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-276"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlhasha"><strong>UrlHash</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-277">Aplica hash a uma cadeia de caracteres de URL.</span><span class="sxs-lookup"><span data-stu-id="7891c-277">Hashes a URL string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-278"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisa"><strong>UrlIs</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-278"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisa"><strong>UrlIs</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-279">Testa se uma URL é um tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="7891c-279">Tests whether a URL is a specified type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-280"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisfileurla"><strong>UrlIsFileUrl</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-280"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisfileurla"><strong>UrlIsFileUrl</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-281">Testa uma URL para determinar se é uma URL de arquivo.</span><span class="sxs-lookup"><span data-stu-id="7891c-281">Tests a URL to determine if it is a file URL.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-282"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisnohistorya"><strong>UrlIsNoHistory</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-282"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisnohistorya"><strong>UrlIsNoHistory</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-283">Retorna se uma URL é uma URL que os navegadores normalmente não incluem no histórico de navegação.</span><span class="sxs-lookup"><span data-stu-id="7891c-283">Returns whether a URL is a URL that browsers typically do not include in navigation history.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-284"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisopaquea"><strong>UrlIsOpaque</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-284"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisopaquea"><strong>UrlIsOpaque</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-285">Retorna se uma URL é opaca.</span><span class="sxs-lookup"><span data-stu-id="7891c-285">Returns whether a URL is opaque.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7891c-286"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapea"><strong>UrlUnescape</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-286"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapea"><strong>UrlUnescape</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-287">Converte as sequências de escape de volta em caracteres comuns.</span><span class="sxs-lookup"><span data-stu-id="7891c-287">Converts escape sequences back into ordinary characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7891c-288"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapeinplace"><strong>UrlUnescapeInPlace</strong></a></span><span class="sxs-lookup"><span data-stu-id="7891c-288"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapeinplace"><strong>UrlUnescapeInPlace</strong></a></span></span><br/></td>
<td><span data-ttu-id="7891c-289">Converte as sequências de escape de volta em caracteres comuns e substitui a cadeia de caracteres original.</span><span class="sxs-lookup"><span data-stu-id="7891c-289">Converts escape sequences back into ordinary characters and overwrites the original string.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 





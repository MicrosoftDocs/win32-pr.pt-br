---
description: Esta seção descreve as funções de manipulação de cadeia de caracteres do shell do Windows. Os elementos de programação explicados nesta documentação são exportados por Shlwapi.dll e definidos em Shlwapi. h e shlwapi. lib.
title: Funções de manipulação de cadeia de caracteres do Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: c7329e22-c9bf-4845-bc0a-a155d1bd2005
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4c2e47785db10ba7dc4bbe54e78e3a06be1b152a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922565"
---
# <a name="shell-string-handling-functions"></a><span data-ttu-id="cb730-104">Funções de manipulação de cadeia de caracteres do Shell</span><span class="sxs-lookup"><span data-stu-id="cb730-104">Shell String Handling Functions</span></span>

<span data-ttu-id="cb730-105">Esta seção descreve as funções de manipulação de cadeia de caracteres do shell do Windows.</span><span class="sxs-lookup"><span data-stu-id="cb730-105">This section describes the Windows Shell string handling functions.</span></span> <span data-ttu-id="cb730-106">Os elementos de programação explicados nesta documentação são exportados por Shlwapi.dll e definidos em Shlwapi. h e shlwapi. lib.</span><span class="sxs-lookup"><span data-stu-id="cb730-106">The programming elements explained in this documentation are exported by Shlwapi.dll and defined in Shlwapi.h and Shlwapi.lib.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cb730-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="cb730-107">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cb730-108">Tópico</span><span class="sxs-lookup"><span data-stu-id="cb730-108">Topic</span></span></th>
<th><span data-ttu-id="cb730-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="cb730-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cb730-110"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-chrcmpia"><strong>ChrCmpI</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-110"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-chrcmpia"><strong>ChrCmpI</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-111">Executa uma comparação entre dois caracteres.</span><span class="sxs-lookup"><span data-stu-id="cb730-111">Performs a comparison between two characters.</span></span> <span data-ttu-id="cb730-112">A comparação não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="cb730-112">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb730-113"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-getacceptlanguagesa"><strong>GetAcceptLanguages</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-113"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-getacceptlanguagesa"><strong>GetAcceptLanguages</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-114">Recupera uma cadeia de caracteres usada com sites ao especificar preferências de idioma.</span><span class="sxs-lookup"><span data-stu-id="cb730-114">Retrieves a string used with websites when specifying language preferences.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb730-115"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqna"><strong>IntlStrEqN</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-115"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqna"><strong>IntlStrEqN</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-116">Executa uma comparação que diferencia maiúsculas de minúsculas de um número especificado de caracteres a partir do início de duas cadeias localizadas.</span><span class="sxs-lookup"><span data-stu-id="cb730-116">Performs a case-sensitive comparison of a specified number of characters from the beginning of two localized strings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb730-117"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqnia"><strong>IntlStrEqNI</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-117"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqnia"><strong>IntlStrEqNI</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-118">Executa uma comparação que não diferencia maiúsculas de minúsculas de um número especificado de caracteres a partir do início de duas cadeias localizadas.</span><span class="sxs-lookup"><span data-stu-id="cb730-118">Performs a case-insensitive comparison of a specified number of characters from the beginning of two localized strings.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb730-119"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqworkera"><strong>IntlStrEqWorker</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-119"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqworkera"><strong>IntlStrEqWorker</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-120">Compara um número especificado de caracteres a partir do início de duas cadeias localizadas.</span><span class="sxs-lookup"><span data-stu-id="cb730-120">Compares a specified number of characters from the beginning of two localized strings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb730-121"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-ischarspacea"><strong>IsCharSpace</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-121"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-ischarspacea"><strong>IsCharSpace</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-122">Determina se um caractere representa um espaço.</span><span class="sxs-lookup"><span data-stu-id="cb730-122">Determines whether a character represents a space.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb730-123"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shloadindirectstring"><strong>SHLoadIndirectString</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-123"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shloadindirectstring"><strong>SHLoadIndirectString</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-124">Extrai um recurso de texto especificado quando esse recurso é fornecido na forma de uma cadeia de caracteres indireta (uma cadeia de caracteres que começa com o símbolo ' @ ').</span><span class="sxs-lookup"><span data-stu-id="cb730-124">Extracts a specified text resource when given that resource in the form of an indirect string (a string that begins with the '@' symbol).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb730-125"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa"><strong>SHStrDup</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-125"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa"><strong>SHStrDup</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-126">Faz uma cópia de uma cadeia de caracteres na memória alocada recentemente.</span><span class="sxs-lookup"><span data-stu-id="cb730-126">Makes a copy of a string in newly allocated memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb730-127"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw"><strong>StrCat</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-127"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw"><strong>StrCat</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-128">Acrescenta uma cadeia de caracteres a outra.</span><span class="sxs-lookup"><span data-stu-id="cb730-128">Appends one string to another.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="cb730-129">Não use.</span><span class="sxs-lookup"><span data-stu-id="cb730-129">Do not use.</span></span> <span data-ttu-id="cb730-130">Consulte comentários para funções alternativas.</span><span class="sxs-lookup"><span data-stu-id="cb730-130">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb730-131"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatbuffa"><strong>StrCatBuff</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-131"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatbuffa"><strong>StrCatBuff</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-132">Copia e anexa caracteres de uma cadeia de caracteres ao final de outra.</span><span class="sxs-lookup"><span data-stu-id="cb730-132">Copies and appends characters from one string to the end of another.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="cb730-133">Não use.</span><span class="sxs-lookup"><span data-stu-id="cb730-133">Do not use.</span></span> <span data-ttu-id="cb730-134">Consulte comentários para funções alternativas.</span><span class="sxs-lookup"><span data-stu-id="cb730-134">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb730-135"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatchainw"><strong>StrCatChainW</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-135"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatchainw"><strong>StrCatChainW</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-136">Concatena duas cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="cb730-136">Concatenates two Unicode strings.</span></span> <span data-ttu-id="cb730-137">Usado quando são necessárias concatenações repetidas para o mesmo buffer.</span><span class="sxs-lookup"><span data-stu-id="cb730-137">Used when repeated concatenations to the same buffer are required.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb730-138"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchra"><strong>StrChr</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-138"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchra"><strong>StrChr</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-139">Pesquisa uma cadeia de caracteres para a primeira ocorrência de um caractere que corresponde ao caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="cb730-139">Searches a string for the first occurrence of a character that matches the specified character.</span></span> <span data-ttu-id="cb730-140">A comparação diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="cb730-140">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb730-141"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchria"><strong>StrChrI</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-141"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchria"><strong>StrChrI</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-142">Pesquisa uma cadeia de caracteres para a primeira ocorrência de um caractere que corresponde ao caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="cb730-142">Searches a string for the first occurrence of a character that matches the specified character.</span></span> <span data-ttu-id="cb730-143">A comparação não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="cb730-143">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb730-144"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrniw"><strong>StrChrNIW</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-144"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrniw"><strong>StrChrNIW</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-145">Pesquisa uma cadeia de caracteres para a primeira ocorrência de um caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="cb730-145">Searches a string for the first occurrence of a specified character.</span></span> <span data-ttu-id="cb730-146">A comparação não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="cb730-146">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb730-147"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrnw"><strong>StrChrNW</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-147"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrnw"><strong>StrChrNW</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-148">Pesquisa uma cadeia de caracteres para a primeira ocorrência de um caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="cb730-148">Searches a string for the first occurrence of a specified character.</span></span> <span data-ttu-id="cb730-149">A comparação diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="cb730-149">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb730-150"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpw"><strong>StrCmp</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-150"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpw"><strong>StrCmp</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-151">Compara duas cadeias de caracteres para determinar se elas são iguais.</span><span class="sxs-lookup"><span data-stu-id="cb730-151">Compares two strings to determine if they are the same.</span></span> <span data-ttu-id="cb730-152">A comparação diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="cb730-152">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb730-153"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpca"><strong>StrCmpC</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-153"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpca"><strong>StrCmpC</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-154">Compara Cadeias de caracteres usando regras de agrupamento de tempo de execução C (ASCII).</span><span class="sxs-lookup"><span data-stu-id="cb730-154">Compares strings using C run-time (ASCII) collation rules.</span></span> <span data-ttu-id="cb730-155">A comparação diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="cb730-155">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb730-156"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpiw"><strong>StrCmpI</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-156"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpiw"><strong>StrCmpI</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-157">Compara duas cadeias de caracteres para determinar se elas são iguais.</span><span class="sxs-lookup"><span data-stu-id="cb730-157">Compares two strings to determine if they are the same.</span></span> <span data-ttu-id="cb730-158">A comparação não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="cb730-158">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb730-159"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpica"><strong>StrCmpIC</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-159"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpica"><strong>StrCmpIC</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-160">Compara duas cadeias de caracteres usando regras de agrupamento de tempo de execução C (ASCII).</span><span class="sxs-lookup"><span data-stu-id="cb730-160">Compares two strings using C run-time (ASCII) collation rules.</span></span> <span data-ttu-id="cb730-161">A comparação não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="cb730-161">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb730-162"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmplogicalw"><strong>StrCmpLogicalW</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-162"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmplogicalw"><strong>StrCmpLogicalW</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-163">Compara duas cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="cb730-163">Compares two Unicode strings.</span></span> <span data-ttu-id="cb730-164">Os dígitos nas cadeias de caracteres são considerados como conteúdo numérico em vez de texto.</span><span class="sxs-lookup"><span data-stu-id="cb730-164">Digits in the strings are considered as numerical content rather than text.</span></span> <span data-ttu-id="cb730-165">Esse teste não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="cb730-165">This test is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb730-166"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpna"><strong>StrCmpN</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-166"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpna"><strong>StrCmpN</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-167">Compara um número especificado de caracteres desde o início de duas cadeias para determinar se elas são iguais.</span><span class="sxs-lookup"><span data-stu-id="cb730-167">Compares a specified number of characters from the beginning of two strings to determine if they are the same.</span></span> <span data-ttu-id="cb730-168">A comparação diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="cb730-168">The comparison is case-sensitive.</span></span> <span data-ttu-id="cb730-169">A macro <strong>StrNCmp</strong> difere dessa função somente em nome.</span><span class="sxs-lookup"><span data-stu-id="cb730-169">The <strong>StrNCmp</strong> macro differs from this function in name only.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb730-170"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnca"><strong>StrCmpNC</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-170"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnca"><strong>StrCmpNC</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-171">Compara um número especificado de caracteres desde o início de duas cadeias usando regras de agrupamento em tempo de execução C (ASCII).</span><span class="sxs-lookup"><span data-stu-id="cb730-171">Compares a specified number of characters from the beginning of two strings using C run-time (ASCII) collation rules.</span></span> <span data-ttu-id="cb730-172">A comparação diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="cb730-172">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb730-173"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnia"><strong>StrCmpNI</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-173"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnia"><strong>StrCmpNI</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-174">Compara um número especificado de caracteres desde o início de duas cadeias para determinar se elas são iguais.</span><span class="sxs-lookup"><span data-stu-id="cb730-174">Compares a specified number of characters from the beginning of two strings to determine if they are the same.</span></span> <span data-ttu-id="cb730-175">A comparação não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="cb730-175">The comparison is not case-sensitive.</span></span> <span data-ttu-id="cb730-176">A macro <strong>StrNCmpI</strong> difere dessa função somente em nome.</span><span class="sxs-lookup"><span data-stu-id="cb730-176">The <strong>StrNCmpI</strong> macro differs from this function in name only.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb730-177"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnica"><strong>StrCmpNIC</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-177"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnica"><strong>StrCmpNIC</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-178">Compara um número especificado de caracteres desde o início de duas cadeias usando regras de agrupamento em tempo de execução C (ASCII).</span><span class="sxs-lookup"><span data-stu-id="cb730-178">Compares a specified number of characters from the beginning of two strings using C run-time (ASCII) collation rules.</span></span> <span data-ttu-id="cb730-179">A comparação não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="cb730-179">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb730-180"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw"><strong>StrCpy</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-180"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw"><strong>StrCpy</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-181">Copia uma cadeia de caracteres para outra.</span><span class="sxs-lookup"><span data-stu-id="cb730-181">Copies one string to another.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="cb730-182">Não use.</span><span class="sxs-lookup"><span data-stu-id="cb730-182">Do not use.</span></span> <span data-ttu-id="cb730-183">Consulte comentários para funções alternativas.</span><span class="sxs-lookup"><span data-stu-id="cb730-183">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb730-184"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw"><strong>StrCpy</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-184"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw"><strong>StrCpyN</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-185">Copia um número especificado de caracteres do início de uma cadeia de caracteres para outra.</span><span class="sxs-lookup"><span data-stu-id="cb730-185">Copies a specified number of characters from the beginning of one string to another.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="cb730-186">Não use essa função ou a macro <strong>StrNCpy</strong> .</span><span class="sxs-lookup"><span data-stu-id="cb730-186">Do not use this function or the <strong>StrNCpy</strong> macro.</span></span> <span data-ttu-id="cb730-187">Consulte comentários para funções alternativas.</span><span class="sxs-lookup"><span data-stu-id="cb730-187">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb730-188"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspna"><strong>StrCSpn</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-188"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspna"><strong>StrCSpn</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-189">Pesquisa uma cadeia de caracteres para a primeira ocorrência de qualquer um dos grupos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="cb730-189">Searches a string for the first occurrence of any of a group of characters.</span></span> <span data-ttu-id="cb730-190">O método de pesquisa diferencia maiúsculas de minúsculas e o caractere <strong>nulo</strong> de terminação é incluído na correspondência do padrão de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="cb730-190">The search method is case-sensitive, and the terminating <strong>NULL</strong> character is included within the search pattern match.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb730-191"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspnia"><strong>StrCSpnI</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-191"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspnia"><strong>StrCSpnI</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-192">Pesquisa uma cadeia de caracteres para a primeira ocorrência de qualquer um dos grupos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="cb730-192">Searches a string for the first occurrence of any of a group of characters.</span></span> <span data-ttu-id="cb730-193">O método Search não diferencia maiúsculas de minúsculas e o caractere <strong>nulo</strong> de terminação é incluído na correspondência do padrão de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="cb730-193">The search method is not case-sensitive, and the terminating <strong>NULL</strong> character is included within the search pattern match.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb730-194"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa"><strong>StrDup</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-194"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa"><strong>StrDup</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-195">Duplica uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="cb730-195">Duplicates a string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb730-196"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesize64a"><strong>StrFormatByteSize64</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-196"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesize64a"><strong>StrFormatByteSize64</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-197">Converte um valor numérico em uma cadeia de caracteres que representa o número expresso como um valor de tamanho em bytes, kilobytes, megabytes ou gigabytes, dependendo do tamanho.</span><span class="sxs-lookup"><span data-stu-id="cb730-197">Converts a numeric value into a string that represents the number expressed as a size value in bytes, kilobytes, megabytes, or gigabytes, depending on the size.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb730-198"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-198"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-199">Converte um valor numérico em uma cadeia de caracteres que representa o número expresso como um valor de tamanho em bytes, kilobytes, megabytes ou gigabytes, dependendo do tamanho.</span><span class="sxs-lookup"><span data-stu-id="cb730-199">Converts a numeric value into a string that represents the number expressed as a size value in bytes, kilobytes, megabytes, or gigabytes, depending on the size.</span></span> <span data-ttu-id="cb730-200">Difere de <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> em um tipo de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="cb730-200">Differs from <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> in one parameter type.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb730-201"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizeex"><strong>StrFormatByteSizeEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-201"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizeex"><strong>StrFormatByteSizeEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-202">Converte um valor numérico em uma cadeia de caracteres que representa o número em bytes, kilobytes, megabytes ou gigabytes, dependendo do tamanho.</span><span class="sxs-lookup"><span data-stu-id="cb730-202">Converts a numeric value into a string that represents the number in bytes, kilobytes, megabytes, or gigabytes, depending on the size.</span></span> <span data-ttu-id="cb730-203">Estende <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> oferecendo a opção de arredondar para o dígito exibido mais próximo ou para descartar dígitos não exibidos.</span><span class="sxs-lookup"><span data-stu-id="cb730-203">Extends <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> by offering the option to round to the nearest displayed digit or to discard undisplayed digits.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb730-204"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-204"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-205">Converte um valor numérico em uma cadeia de caracteres que representa o número expresso como um valor de tamanho em bytes, kilobytes, megabytes ou gigabytes, dependendo do tamanho.</span><span class="sxs-lookup"><span data-stu-id="cb730-205">Converts a numeric value into a string that represents the number expressed as a size value in bytes, kilobytes, megabytes, or gigabytes, depending on the size.</span></span> <span data-ttu-id="cb730-206">Difere de <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a> em um tipo de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="cb730-206">Differs from <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a> in one parameter type.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb730-207"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatkbsizea"><strong>StrFormatKBSize</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-207"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatkbsizea"><strong>StrFormatKBSize</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-208">Converte um valor numérico em uma cadeia de caracteres que representa o número expresso como um valor de tamanho em quilobytes.</span><span class="sxs-lookup"><span data-stu-id="cb730-208">Converts a numeric value into a string that represents the number expressed as a size value in kilobytes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb730-209"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strfromtimeintervala"><strong>StrFromTimeInterval</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-209"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strfromtimeintervala"><strong>StrFromTimeInterval</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-210">Converte um intervalo de tempo, especificado em milissegundos, em uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="cb730-210">Converts a time interval, specified in milliseconds, to a string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb730-211"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strisintlequala"><strong>StrIsIntlEqual</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-211"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strisintlequala"><strong>StrIsIntlEqual</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-212">Compara um número especificado de caracteres desde o início de duas cadeias para determinar se elas são iguais.</span><span class="sxs-lookup"><span data-stu-id="cb730-212">Compares a specified number of characters from the beginning of two strings to determine if they are equal.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb730-213"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strncata"><strong>StrNCat</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-213"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strncata"><strong>StrNCat</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-214">Anexa um número especificado de caracteres desde o início de uma cadeia de caracteres até o fim de outro.</span><span class="sxs-lookup"><span data-stu-id="cb730-214">Appends a specified number of characters from the beginning of one string to the end of another.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="cb730-215">Não use essa função ou a macro <strong>StrCatN</strong> .</span><span class="sxs-lookup"><span data-stu-id="cb730-215">Do not use this function or the <strong>StrCatN</strong> macro.</span></span> <span data-ttu-id="cb730-216">Consulte comentários para funções alternativas.</span><span class="sxs-lookup"><span data-stu-id="cb730-216">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb730-217"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strpbrka"><strong>StrPBrk</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-217"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strpbrka"><strong>StrPBrk</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-218">Pesquisa uma cadeia de caracteres para a primeira ocorrência de um caractere contido em um buffer especificado.</span><span class="sxs-lookup"><span data-stu-id="cb730-218">Searches a string for the first occurrence of a character contained in a specified buffer.</span></span> <span data-ttu-id="cb730-219">Essa pesquisa não inclui o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="cb730-219">This search does not include the terminating null character.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb730-220"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchra"><strong>StrRChr</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-220"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchra"><strong>StrRChr</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-221">Pesquisa uma cadeia de caracteres para a última ocorrência de um caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="cb730-221">Searches a string for the last occurrence of a specified character.</span></span> <span data-ttu-id="cb730-222">A comparação diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="cb730-222">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb730-223"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchria"><strong>StrRChrI</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-223"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchria"><strong>StrRChrI</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-224">Pesquisa uma cadeia de caracteres para a última ocorrência de um caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="cb730-224">Searches a string for the last occurrence of a specified character.</span></span> <span data-ttu-id="cb730-225">A comparação não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="cb730-225">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb730-226"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobstr"><strong>StrRetToBSTR</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-226"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobstr"><strong>StrRetToBSTR</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-227">Aceita uma estrutura <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>Strret</strong></a> retornada por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a> que contém ou aponta para uma cadeia de caracteres e retorna essa cadeia de caracteres como um <a href="/previous-versions/windows/desktop/automat/bstr"><strong>BSTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="cb730-227">Accepts a <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> structure returned by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a> that contains or points to a string, and returns that string as a <a href="/previous-versions/windows/desktop/automat/bstr"><strong>BSTR</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb730-228"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa"><strong>StrRetToBuf</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-228"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa"><strong>StrRetToBuf</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-229">Converte uma estrutura <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>Strret</strong></a> retornada por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a> em uma cadeia de caracteres e coloca o resultado em um buffer.</span><span class="sxs-lookup"><span data-stu-id="cb730-229">Converts an <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> structure returned by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a> to a string, and places the result in a buffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb730-230"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra"><strong>StrRetToStr</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-230"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra"><strong>StrRetToStr</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-231">Usa uma estrutura <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>Strret</strong></a> retornada por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a> e retorna um ponteiro para uma cadeia de caracteres alocada que contém o nome de exibição.</span><span class="sxs-lookup"><span data-stu-id="cb730-231">Takes an <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> structure returned by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a> and returns a pointer to an allocated string containing the display name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb730-232"><a href="strrettostrn.md"><strong>StrRetToStrN</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-232"><a href="strrettostrn.md"><strong>StrRetToStrN</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-233">Usa uma estrutura <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>Strret</strong></a> retornada por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a>, converte-a em uma cadeia de caracteres e coloca o resultado em um buffer.</span><span class="sxs-lookup"><span data-stu-id="cb730-233">Takes an <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> structure returned by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a>, converts it to a string, and places the result in a buffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb730-234"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrstria"><strong>StrRStrI</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-234"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrstria"><strong>StrRStrI</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-235">Pesquisa a última ocorrência de uma subcadeia de caracteres especificada em uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="cb730-235">Searches for the last occurrence of a specified substring within a string.</span></span> <span data-ttu-id="cb730-236">A comparação não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="cb730-236">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb730-237"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strspna"><strong>StrSpn</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-237"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strspna"><strong>StrSpn</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-238">Obtém o comprimento de uma subcadeia de caracteres dentro de uma cadeia de caracteres que consiste inteiramente em caracteres contidos em um buffer especificado.</span><span class="sxs-lookup"><span data-stu-id="cb730-238">Obtains the length of a substring within a string that consists entirely of characters contained in a specified buffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb730-239"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstra"><strong>StrStr</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-239"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstra"><strong>StrStr</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-240">Localiza a primeira ocorrência de uma subcadeia de caracteres dentro de uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="cb730-240">Finds the first occurrence of a substring within a string.</span></span> <span data-ttu-id="cb730-241">A comparação diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="cb730-241">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb730-242"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstria"><strong>StrStrI</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-242"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstria"><strong>StrStrI</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-243">Localiza a primeira ocorrência de uma subcadeia de caracteres dentro de uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="cb730-243">Finds the first occurrence of a substring within a string.</span></span> <span data-ttu-id="cb730-244">A comparação não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="cb730-244">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb730-245"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointa"><strong>StrToInt</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-245"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointa"><strong>StrToInt</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-246">Converte uma cadeia de caracteres que representa um valor decimal em um inteiro.</span><span class="sxs-lookup"><span data-stu-id="cb730-246">Converts a string that represents a decimal value to an integer.</span></span> <span data-ttu-id="cb730-247">A macro <strong>StrToLong</strong> é idêntica a essa função.</span><span class="sxs-lookup"><span data-stu-id="cb730-247">The <strong>StrToLong</strong> macro is identical to this function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb730-248"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtoint64exa"><strong>StrToInt64Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-248"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtoint64exa"><strong>StrToInt64Ex</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-249">Converte uma cadeia de caracteres que representa um valor decimal ou hexadecimal em um inteiro de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="cb730-249">Converts a string representing a decimal or hexadecimal value to a 64-bit integer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb730-250"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointexa"><strong>StrToIntEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-250"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointexa"><strong>StrToIntEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-251">Converte uma cadeia de caracteres que representa um número decimal ou hexadecimal em um número inteiro.</span><span class="sxs-lookup"><span data-stu-id="cb730-251">Converts a string representing a decimal or hexadecimal number to an integer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb730-252"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtrima"><strong>Prertrim</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-252"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtrima"><strong>StrTrim</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-253">Remove os caracteres especificados à esquerda e à direita de uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="cb730-253">Removes specified leading and trailing characters from a string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb730-254"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa"><strong>wnsprintf</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-254"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa"><strong>wnsprintf</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-255">Usa uma lista de argumentos de comprimento variável e retorna os valores dos argumentos como uma cadeia de caracteres formatada no estilo <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="cb730-255">Takes a variable-length argument list and returns the values of the arguments as a <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>-style formatted string.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="cb730-256">Não use essa função.</span><span class="sxs-lookup"><span data-stu-id="cb730-256">Do not use this function.</span></span> <span data-ttu-id="cb730-257">Consulte comentários para funções alternativas.</span><span class="sxs-lookup"><span data-stu-id="cb730-257">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb730-258"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa"><strong>wvnsprintf</strong></a></span><span class="sxs-lookup"><span data-stu-id="cb730-258"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa"><strong>wvnsprintf</strong></a></span></span><br/></td>
<td><span data-ttu-id="cb730-259">Usa uma lista de argumentos e retorna os valores dos argumentos como uma cadeia de caracteres formatada no estilo <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="cb730-259">Takes a list of arguments and returns the values of the arguments as a <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>-style formatted string.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="cb730-260">Não use essa função.</span><span class="sxs-lookup"><span data-stu-id="cb730-260">Do not use this function.</span></span> <span data-ttu-id="cb730-261">Consulte comentários para funções alternativas.</span><span class="sxs-lookup"><span data-stu-id="cb730-261">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 

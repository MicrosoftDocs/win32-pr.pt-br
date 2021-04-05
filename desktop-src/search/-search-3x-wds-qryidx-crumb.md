---
description: O argumento de trilha dá suporte a instruções de AQS (sintaxe de consulta avançada completa) e é especialmente útil como meio de controlar o escopo de uma pesquisa.
ms.assetid: b0b974ae-0573-45e4-888e-07138604b62e
title: Argumento de trilha (pesquisa do Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51f36764174e0eecaedee4a9c360bb9d7dabca3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090094"
---
# <a name="crumb-argument-windows-search"></a><span data-ttu-id="6ed02-103">Argumento de trilha (pesquisa do Windows)</span><span class="sxs-lookup"><span data-stu-id="6ed02-103">CRUMB Argument (Windows Search)</span></span>

<span data-ttu-id="6ed02-104">O `crumb` argumento oferece suporte a instruções AQS (sintaxe de consulta avançada completa) e é especialmente útil como meio de controlar o escopo de uma pesquisa.</span><span class="sxs-lookup"><span data-stu-id="6ed02-104">The `crumb` argument supports full Advanced Query Syntax (AQS) statements and is especially useful as a means of controlling the scope of a search.</span></span> <span data-ttu-id="6ed02-105">Além de AQS ements, o `crumb` argumento pode usar um parâmetro especial `location` no Windows Vista e `kind` `store` parâmetros no XP, conforme descrito posteriormente neste tópico.</span><span class="sxs-lookup"><span data-stu-id="6ed02-105">In addition to AQS ements, the `crumb` argument can take a special `location` parameter on Windows Vista and `kind` and `store` parameters on XP, as described later in this topic.</span></span>

<span data-ttu-id="6ed02-106">Este tópico é organizado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="6ed02-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="6ed02-107">Sintaxe de trilha</span><span class="sxs-lookup"><span data-stu-id="6ed02-107">Crumb Syntax</span></span>](#crumb-syntax)
    -   [<span data-ttu-id="6ed02-108">Exemplos gerais</span><span class="sxs-lookup"><span data-stu-id="6ed02-108">General Examples</span></span>](#general-examples)
-   [<span data-ttu-id="6ed02-109">Usando a trilha com o Vista (local)</span><span class="sxs-lookup"><span data-stu-id="6ed02-109">Using crumb with Vista (location)</span></span>](#using-crumb-with-vista-location)
    -   [<span data-ttu-id="6ed02-110">Exemplos do vista</span><span class="sxs-lookup"><span data-stu-id="6ed02-110">Vista Examples</span></span>](#vista-examples)
    -   [<span data-ttu-id="6ed02-111">Constantes para pastas comuns</span><span class="sxs-lookup"><span data-stu-id="6ed02-111">Constants for Common Folders</span></span>](#constants-for-common-folders)
-   [<span data-ttu-id="6ed02-112">Usando a trilha com o Windows XP (tipo e loja)</span><span class="sxs-lookup"><span data-stu-id="6ed02-112">Using crumb with Windows XP (kind and store)</span></span>](#using-crumb-with-windows-xp-kind-and-store)
    -   [<span data-ttu-id="6ed02-113">Exemplos do XP</span><span class="sxs-lookup"><span data-stu-id="6ed02-113">XP Examples</span></span>](#xp-examples)
-   [<span data-ttu-id="6ed02-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6ed02-114">Related topics</span></span>](#related-topics)

 

## <a name="crumb-syntax"></a><span data-ttu-id="6ed02-115">Sintaxe de trilha</span><span class="sxs-lookup"><span data-stu-id="6ed02-115">Crumb Syntax</span></span>

<span data-ttu-id="6ed02-116">A sintaxe de trilha é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="6ed02-116">The crumb syntax is as follows:</span></span>


```
crumb=<column>:<value>[,<label>][,<column>:<value>[,<label>]]& 
```



<span data-ttu-id="6ed02-117">A <column> parte é qualquer propriedade no sistema de propriedades e o</span><span class="sxs-lookup"><span data-stu-id="6ed02-117">The <column> portion is any property in the property system, and the</span></span> <value> <span data-ttu-id="6ed02-118">a parte é um valor válido para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6ed02-118">portion is a valid value for that property.</span></span> <span data-ttu-id="6ed02-119">A <label> parte é um alias opcional para a propriedade que é exibido como uma dica de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="6ed02-119">The <label> portion is an optional alias for the property that displays as a user interface hint.</span></span>

### <a name="general-examples"></a><span data-ttu-id="6ed02-120">Exemplos gerais</span><span class="sxs-lookup"><span data-stu-id="6ed02-120">General Examples</span></span>


```
crumb=System.Author:paolo&
crumb=store:mapi&
crumb=location:c%3a%5cMyVacationPix,Vacation&
```



 

## <a name="using-crumb-with-vista-location"></a><span data-ttu-id="6ed02-121">Usando a trilha com o Vista (local)</span><span class="sxs-lookup"><span data-stu-id="6ed02-121">Using crumb with Vista (location)</span></span>

<span data-ttu-id="6ed02-122">No parâmetro de trilha, o Windows Vista dá suporte ao AQS completo e também à `location` propriedade, que tem uma implementação especial disponível apenas no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6ed02-122">In the crumb parameter, Windows Vista supports full AQS and also the `location` property, which has a special implementation available only on Windows Vista.</span></span> <span data-ttu-id="6ed02-123">Você pode usar uma cadeia de caracteres AQS ou a `location` propriedade dentro de um único parâmetro de trilha, mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="6ed02-123">You can use either an AQS string or the `location` property within a single crumb parameter, but not both.</span></span> <span data-ttu-id="6ed02-124">Se o parâmetro de trilha incluir AQS, todo o restante nesse parâmetro de trilha será ignorado.</span><span class="sxs-lookup"><span data-stu-id="6ed02-124">If the crumb parameter includes AQS, everything else in that crumb parameter is ignored.</span></span>

<span data-ttu-id="6ed02-125">A `location` propriedade permite que você especifique um caminho para pesquisar.</span><span class="sxs-lookup"><span data-stu-id="6ed02-125">The `location` property enables you to specify a path to search.</span></span> <span data-ttu-id="6ed02-126">O Windows Vista pode ignorar o indexador e atravessar o diretório diretamente se o local estiver fora do escopo de rastreamento do indexador.</span><span class="sxs-lookup"><span data-stu-id="6ed02-126">Windows Vista can bypass the Indexer and traverse the directory directly if the location is outside the Indexer's crawl scope.</span></span> <span data-ttu-id="6ed02-127">Consequentemente, essas pesquisas podem ser mais lentas do que as pesquisas que usam o indexador.</span><span class="sxs-lookup"><span data-stu-id="6ed02-127">Consequently, these searches may be slower than searches that use the Indexer.</span></span>

<span data-ttu-id="6ed02-128">Quando você especifica uma `location` propriedade, dois parâmetros adicionais têm suporte e são opcionais:</span><span class="sxs-lookup"><span data-stu-id="6ed02-128">When you specify a `location` property, two additional parameters are supported and optional:</span></span>



| <span data-ttu-id="6ed02-129">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="6ed02-129">Parameter</span></span> | <span data-ttu-id="6ed02-130">Valores</span><span class="sxs-lookup"><span data-stu-id="6ed02-130">Values</span></span>                  | <span data-ttu-id="6ed02-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="6ed02-131">Description</span></span>                                                                                                                                                                       |
|-----------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ed02-132">inclusão</span><span class="sxs-lookup"><span data-stu-id="6ed02-132">inclusion</span></span> | <span data-ttu-id="6ed02-133">incluir, excluir</span><span class="sxs-lookup"><span data-stu-id="6ed02-133">include, exclude</span></span>        | <span data-ttu-id="6ed02-134">Especifica se a consulta deve incluir ou excluir itens desse caminho.</span><span class="sxs-lookup"><span data-stu-id="6ed02-134">Specifies whether the query should include or exclude items from that path.</span></span> <span data-ttu-id="6ed02-135">"Include" é o padrão.</span><span class="sxs-lookup"><span data-stu-id="6ed02-135">"Include" is the default.</span></span> <span data-ttu-id="6ed02-136">O Windows Vista não oferece suporte a exclusões sem inclusões.</span><span class="sxs-lookup"><span data-stu-id="6ed02-136">Windows Vista does not support exclusions without inclusions.</span></span> <span data-ttu-id="6ed02-137">(Veja o exemplo)</span><span class="sxs-lookup"><span data-stu-id="6ed02-137">(See example)</span></span> |
| <span data-ttu-id="6ed02-138">recursão</span><span class="sxs-lookup"><span data-stu-id="6ed02-138">recursion</span></span> | <span data-ttu-id="6ed02-139">recursivo, nonrecursive</span><span class="sxs-lookup"><span data-stu-id="6ed02-139">recursive, nonrecursive</span></span> | <span data-ttu-id="6ed02-140">Especifica se a pesquisa deve recurse todas as subpastas começando com o valor definido no local:</span><span class="sxs-lookup"><span data-stu-id="6ed02-140">Specifies whether the search should recurse all subfolders starting from the value defined in the location:</span></span><value><span data-ttu-id="6ed02-141">.</span><span class="sxs-lookup"><span data-stu-id="6ed02-141">.</span></span> <span data-ttu-id="6ed02-142">"Recursivo" é o padrão.</span><span class="sxs-lookup"><span data-stu-id="6ed02-142">"Recursive" is the default.</span></span>                             |



 

<span data-ttu-id="6ed02-143">Para fazer o escopo de uma pesquisa usando o protocolo Search-MS:, você tem opções diferentes, dependendo do destino do escopo.</span><span class="sxs-lookup"><span data-stu-id="6ed02-143">To scope a search using the search-ms: protocol, you have different options depending on the target of the scope.</span></span>

<span data-ttu-id="6ed02-144">Pasta em um computador local:</span><span class="sxs-lookup"><span data-stu-id="6ed02-144">Folder on a local machine:</span></span>

-   <span data-ttu-id="6ed02-145">Use AQS (trilha = pasta: <caminho codificado de URL>)</span><span class="sxs-lookup"><span data-stu-id="6ed02-145">Use AQS (crumb=folder:<URL-encoded path>)</span></span>
-   <span data-ttu-id="6ed02-146">Usar o argumento de local (trilha = local: <caminho codificado de URL>)</span><span class="sxs-lookup"><span data-stu-id="6ed02-146">Use location argument (crumb=location:<URL-encoded path>)</span></span>

<span data-ttu-id="6ed02-147">Pasta em um computador/rede remota:</span><span class="sxs-lookup"><span data-stu-id="6ed02-147">Folder on a remote machine/network:</span></span>

-   <span data-ttu-id="6ed02-148">Usar o argumento de local (trilha = local: <caminho codificado de URL>)</span><span class="sxs-lookup"><span data-stu-id="6ed02-148">Use location argument (crumb=location:<URL-encoded path>)</span></span>

<span data-ttu-id="6ed02-149">Pasta acessada por meio de um manipulador de protocolo UNC conhecido:</span><span class="sxs-lookup"><span data-stu-id="6ed02-149">Folder accessed via a known UNC protocol handler:</span></span>

-   <span data-ttu-id="6ed02-150">Use AQS (trilha = armazenamento: <UNC protocol handler name> )</span><span class="sxs-lookup"><span data-stu-id="6ed02-150">Use AQS (crumb=store:<UNC protocol handler name>)</span></span>
-   <span data-ttu-id="6ed02-151">Usar o argumento de local (trilha = local: <caminho codificado de URL>)</span><span class="sxs-lookup"><span data-stu-id="6ed02-151">Use location argument (crumb=location:<URL-encoded path>)</span></span>

### <a name="vista-examples"></a><span data-ttu-id="6ed02-152">Exemplos do vista</span><span class="sxs-lookup"><span data-stu-id="6ed02-152">Vista Examples</span></span>


```
search-ms:query=vacation&crumb=location:shell%3aPersonal,include,recursive&

search-ms:crumb=location:c%3a%5cPictures&crumb=location:c%3a%5cPictures%5cDuplicates,,exclude& 

search-ms:crumb=location:c%3a%5cDocuments&crumb=kind:pics&
```



<span data-ttu-id="6ed02-153">O primeiro exemplo executa uma pesquisa por "férias" começando no local shell://Personal (um atalho especial para a pasta meus documentos do usuário), incluindo essa pasta e todas as subpastas.</span><span class="sxs-lookup"><span data-stu-id="6ed02-153">The first example executes a search for "vacation" starting at the shell://Personal location (a special shortcut to the user's My Documents folder), including that folder and all subfolders.</span></span> <span data-ttu-id="6ed02-154">Consulte a tabela abaixo.</span><span class="sxs-lookup"><span data-stu-id="6ed02-154">See table below.</span></span>

<span data-ttu-id="6ed02-155">O segundo exemplo executa uma pesquisa em C: \\ Pictures, mas não em c: \\ imagens \\ duplicatas.</span><span class="sxs-lookup"><span data-stu-id="6ed02-155">The second example executes a search within C:\\Pictures, but not in C:\\Pictures\\Duplicates.</span></span>

<span data-ttu-id="6ed02-156">O terceiro exemplo executa uma pesquisa em C: \\ Documents, limitada a arquivos com a propriedade Kind definida como pics.</span><span class="sxs-lookup"><span data-stu-id="6ed02-156">The third example executes a search within C:\\Documents, limited to files with the kind property set to pics.</span></span>

### <a name="constants-for-common-folders"></a><span data-ttu-id="6ed02-157">Constantes para pastas comuns</span><span class="sxs-lookup"><span data-stu-id="6ed02-157">Constants for Common Folders</span></span>

<span data-ttu-id="6ed02-158">O Windows Vista permite o uso de valores [KNOWNFOLDERID](/previous-versions//bb762584(v=vs.85)) que fornecem uma maneira exclusiva independente do sistema de identificar pastas especiais usadas frequentemente por aplicativos, mas que podem não ter o mesmo nome ou local em um determinado sistema.</span><span class="sxs-lookup"><span data-stu-id="6ed02-158">Windows Vista enables the use of [KNOWNFOLDERID](/previous-versions//bb762584(v=vs.85)) values that provide a unique system-independent way to identify special folders used frequently by applications, but which may not have the same name or location on any given system.</span></span> <span data-ttu-id="6ed02-159">Por exemplo, a pasta do sistema pode ser "C: \\ Windows" em um sistema e "c: \\ WinNT" em outro.</span><span class="sxs-lookup"><span data-stu-id="6ed02-159">For example, the system folder may be "C:\\Windows" on one system and "C:\\Winnt" on another.</span></span> <span data-ttu-id="6ed02-160">Antes do Windows Vista, foram usadas [CSIDLs](/windows/desktop/shell/csidl) .</span><span class="sxs-lookup"><span data-stu-id="6ed02-160">Prior to Windows Vista, [CSIDLs](/windows/desktop/shell/csidl) were used.</span></span>

<span data-ttu-id="6ed02-161">Use esses locais com esta sintaxe:</span><span class="sxs-lookup"><span data-stu-id="6ed02-161">Use these locations with this syntax:</span></span>


```
crumb=location:shell%3a<LocationName>&
```



 

## <a name="using-crumb-with-windows-xp-kind-and-store"></a><span data-ttu-id="6ed02-162">Usando a trilha com o Windows XP (tipo e loja)</span><span class="sxs-lookup"><span data-stu-id="6ed02-162">Using crumb with Windows XP (kind and store)</span></span>

<span data-ttu-id="6ed02-163">Para o Windows Search no Windows XP (WDS 3. x), os termos de AQS "Kind" e "Store" têm uma implementação especial.</span><span class="sxs-lookup"><span data-stu-id="6ed02-163">For Windows Search on Windows XP (WDS 3.x), the AQS terms "kind" and "store" have a special implementation.</span></span> <span data-ttu-id="6ed02-164">Os valores de "Kind" são os mesmos [valores usados no WDS 2. x](../lwef/-search-2x-wds-perceivedtype.md).</span><span class="sxs-lookup"><span data-stu-id="6ed02-164">The "kind" values are the same [values used in WDS 2.x](../lwef/-search-2x-wds-perceivedtype.md).</span></span> <span data-ttu-id="6ed02-165">Os valores de "Store" incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6ed02-165">The "store" values include the following:</span></span>

-   <span data-ttu-id="6ed02-166">MAPI</span><span class="sxs-lookup"><span data-stu-id="6ed02-166">mapi</span></span>
-   <span data-ttu-id="6ed02-167">arquivo</span><span class="sxs-lookup"><span data-stu-id="6ed02-167">file</span></span>
-   <span data-ttu-id="6ed02-168">outlookexpress</span><span class="sxs-lookup"><span data-stu-id="6ed02-168">outlookexpress</span></span>
-   <span data-ttu-id="6ed02-169">any</span><span class="sxs-lookup"><span data-stu-id="6ed02-169">any</span></span>

### <a name="xp-examples"></a><span data-ttu-id="6ed02-170">Exemplos do XP</span><span class="sxs-lookup"><span data-stu-id="6ed02-170">XP Examples</span></span>


```
search-ms:query=from:john&crumb=store:outlookexpress,OE%20Mail&
search-ms:query=from:john&crumb=kind:communications&
```



<span data-ttu-id="6ed02-171">O primeiro exemplo retorna emails do Microsoft Outlook Express de João com o rótulo personalizado "OE Mail".</span><span class="sxs-lookup"><span data-stu-id="6ed02-171">The first example returns Microsoft Outlook Express emails from John with the custom label, "OE Mail".</span></span> <span data-ttu-id="6ed02-172">O segundo exemplo executa uma pesquisa para qualquer comunicação de João.</span><span class="sxs-lookup"><span data-stu-id="6ed02-172">The second example executes a search for any communication from John.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ed02-173">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6ed02-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ed02-174">Introdução com argumentos de Parameter-Value</span><span class="sxs-lookup"><span data-stu-id="6ed02-174">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[<span data-ttu-id="6ed02-175">Argumentos do identificador de localidade</span><span class="sxs-lookup"><span data-stu-id="6ed02-175">Locale Identifier Arguments</span></span>](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[<span data-ttu-id="6ed02-176">Argumento de sintaxe</span><span class="sxs-lookup"><span data-stu-id="6ed02-176">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[<span data-ttu-id="6ed02-177">Argumento STACKEDBY</span><span class="sxs-lookup"><span data-stu-id="6ed02-177">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[<span data-ttu-id="6ed02-178">Argumento de subconsulta</span><span class="sxs-lookup"><span data-stu-id="6ed02-178">SUBQUERY Argument</span></span>](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 

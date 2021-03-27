---
description: 'A pesquisa: protocolo de aplicativo é uma convenção extensível para chamar o aplicativo de pesquisa de desktop no Windows Vista com Service Pack 1 (SP1) e versões posteriores.'
title: Usando o protocolo de pesquisa
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 91a1ec25-f6ab-4377-8478-20bc51a1d5df
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: a9223a2a30cab85f8e1b0dac0d0df2dc4fe8f80c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989070"
---
# <a name="using-the-search-protocol"></a><span data-ttu-id="3b4fd-103">Usando o protocolo de pesquisa</span><span class="sxs-lookup"><span data-stu-id="3b4fd-103">Using the search Protocol</span></span>

<span data-ttu-id="3b4fd-104">A **pesquisa:** [protocolo de aplicativo](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) é uma convenção extensível para chamar o aplicativo de pesquisa de desktop no Windows Vista com Service Pack 1 (SP1) e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-104">The **search:** [application protocol](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) is an extensible convention for calling the desktop search application on Windows Vista with Service Pack 1 (SP1) and later versions.</span></span> <span data-ttu-id="3b4fd-105">O protocolo foi criado no Windows Vista com SP1 (para obter informações, consulte a visão geral do artigo da base [de dados de conhecimento do Windows Vista Desktop Search Changes no Windows Vista Service Pack 1](https://support.microsoft.com/kb/941946)) para fornecer ao Windows uma maneira de determinar e chamar o aplicativo de pesquisa de desktop padrão.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-105">The protocol was created in Windows Vista with SP1 (for information see the Knowledge Base article [Overview of Windows Vista desktop search Changes in Windows Vista Service Pack 1](https://support.microsoft.com/kb/941946)) to give Windows a way to determine and call the default desktop search application.</span></span>

<span data-ttu-id="3b4fd-106">A sintaxe de protocolo fornece vários parâmetros úteis para executar pesquisas de área de trabalho comuns, como termos de pesquisa inseridos pelo usuário ou o local em que a pesquisa foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-106">The protocol syntax provides a number of parameters useful for performing common desktop searches, such as user-entered search terms or the location on which the search was begun.</span></span> <span data-ttu-id="3b4fd-107">Quando os usuários pesquisam de um dos dois pontos de entrada de pesquisa disponíveis (o menu **Iniciar** ou o Windows Explorer), o sistema operacional usa o protocolo de pesquisa para iniciar o aplicativo de pesquisa de área de trabalho padrão.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-107">When users search from one of the two available search entry points (either the **Start** menu or Windows Explorer), the operating system uses the search protocol to launch the default desktop search application.</span></span> <span data-ttu-id="3b4fd-108">Ele faz isso adicionando os termos de pesquisa inseridos pelo usuário à sintaxe do protocolo de pesquisa padrão e passando essas informações para o aplicativo registrado como o aplicativo de pesquisa padrão.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-108">It does this by adding the user-entered search terms to the standard search protocol syntax and passing that information to the application registered as the default search application.</span></span>

<span data-ttu-id="3b4fd-109">Se nenhum outro aplicativo de pesquisa de desktop estiver instalado, uma pesquisa inserida nesses pontos de entrada iniciará o Windows Search Explorer.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-109">If no other desktop search applications are installed, a search entered into these entry points launches the Windows Search Explorer.</span></span> <span data-ttu-id="3b4fd-110">No entanto, desenvolvedores de terceiros podem criar, instalar e registrar seus aplicativos para lidar com o protocolo de pesquisa e para ser o aplicativo de pesquisa padrão.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-110">However, third-party developers can create, install, and register their applications to handle the search protocol and to be the default search application.</span></span> <span data-ttu-id="3b4fd-111">Esses aplicativos precisam dar suporte à sintaxe de protocolo de pesquisa e se registrarem com o recurso de [programas padrão](default-programs.md) para garantir uma experiência tranqüila com o Windows.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-111">Such applications need to support the search protocol syntax and register with the [Default Programs](default-programs.md) feature to ensure a seamless experience with Windows.</span></span>

<span data-ttu-id="3b4fd-112">Se você desenvolver um aplicativo que se destina a usar ou a criar um aplicativo de pesquisa de área de trabalho específico, não deverá depender exclusivamente do protocolo **Search:** .</span><span class="sxs-lookup"><span data-stu-id="3b4fd-112">If you develop an application that is intended to use or build upon a specific desktop search application, you should not depend exclusively on the **search:** protocol.</span></span> <span data-ttu-id="3b4fd-113">Como muitos aplicativos podiam ter a **pesquisa:** protocolo, não há nenhuma garantia de que seu aplicativo de pesquisa de área de trabalho de destino o terá em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-113">Because many applications could own the **search:** protocol, there is no guarantee that your targeted desktop search application will own it at any given time.</span></span> <span data-ttu-id="3b4fd-114">Em vez disso, você deve usar um protocolo de pesquisa particular definido por esse aplicativo de pesquisa de área de trabalho de destino.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-114">Instead, you should use a private search protocol defined by that targeted desktop search application.</span></span> <span data-ttu-id="3b4fd-115">Isso significa que os aplicativos de pesquisa de desktops destinados a ser uma plataforma para aplicativos de terceiros devem dar suporte tanto ao protocolo **Search:** quanto ao seu próprio protocolo de pesquisa proprietário.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-115">This means that desktop search applications intended to be a platform for third-party applications should support both the **search:** protocol and their own proprietary search protocol.</span></span>

> [!Note]  
> <span data-ttu-id="3b4fd-116">A **pesquisa:** protocolo não substitui a pesquisa proprietária [-MS:](../search/-search-3x-wds-qryidx-searchms.md) Protocol.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-116">The **search:** protocol does not replace the proprietary [search-ms:](../search/-search-3x-wds-qryidx-searchms.md) protocol.</span></span> <span data-ttu-id="3b4fd-117">Os aplicativos ainda podem usar o protocolo **Search-MS:** para iniciar o Gerenciador de pesquisa de janelas ou para consultar silenciosamente o indexador do Windows Search.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-117">Applications can still use the **search-ms:** protocol to launch Window Search Explorer or to silently query the Windows Search indexer.</span></span>

 

<span data-ttu-id="3b4fd-118">Este tópico aborda o seguinte:</span><span class="sxs-lookup"><span data-stu-id="3b4fd-118">This topic covers the following:</span></span>

-   [<span data-ttu-id="3b4fd-119">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b4fd-119">Syntax</span></span>](#syntax)
-   [<span data-ttu-id="3b4fd-120">Uso do Windows Vista com SP1 da pesquisa: protocolo</span><span class="sxs-lookup"><span data-stu-id="3b4fd-120">Windows Vista with SP1 use of the search: protocol</span></span>](#windows-vista-with-sp1-use-of-the-search-protocol)
-   [<span data-ttu-id="3b4fd-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3b4fd-121">Examples</span></span>](#examples)
-   [<span data-ttu-id="3b4fd-122">Registrando o aplicativo que manipula o protocolo</span><span class="sxs-lookup"><span data-stu-id="3b4fd-122">Registering the Application that Handles the Protocol</span></span>](#registering-the-application-that-handles-the-protocol)
    -   [<span data-ttu-id="3b4fd-123">Entradas do registro</span><span class="sxs-lookup"><span data-stu-id="3b4fd-123">Registry Entries</span></span>](#registry-entries)
-   [<span data-ttu-id="3b4fd-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3b4fd-124">Related topics</span></span>](#related-topics)

## <a name="syntax"></a><span data-ttu-id="3b4fd-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b4fd-125">Syntax</span></span>

<span data-ttu-id="3b4fd-126">O protocolo de pesquisa usa a seguinte sintaxe padrão codificada por URL:</span><span class="sxs-lookup"><span data-stu-id="3b4fd-126">The search protocol uses the following standard URL-encoded syntax:</span></span>


```C++
search:parameter=value[&parameter=value]&
```



<span data-ttu-id="3b4fd-127">A sintaxe começa identificando o próprio protocolo (**Search:**).</span><span class="sxs-lookup"><span data-stu-id="3b4fd-127">The syntax begins by identifying the protocol itself (**search:**).</span></span> <span data-ttu-id="3b4fd-128">Os pares de parâmetro/valor são argumentos passados para o mecanismo de pesquisa, conforme descrito na tabela a seguir, que mostra todos os parâmetros possíveis para a sintaxe do protocolo de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-128">The parameter/value pairs are arguments passed to the Search engine, as described in the following table, which shows all of the possible parameters for the search protocol syntax.</span></span>



| <span data-ttu-id="3b4fd-129">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="3b4fd-129">Parameter</span></span>                                              | <span data-ttu-id="3b4fd-130">Valor</span><span class="sxs-lookup"><span data-stu-id="3b4fd-130">Value</span></span>                                                         | <span data-ttu-id="3b4fd-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="3b4fd-131">Description</span></span>                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b4fd-132">Consulta</span><span class="sxs-lookup"><span data-stu-id="3b4fd-132">query</span></span>                                                  | <span data-ttu-id="3b4fd-133">Texto codificado por URL</span><span class="sxs-lookup"><span data-stu-id="3b4fd-133">URL-encoded text</span></span>                                              | <span data-ttu-id="3b4fd-134">O texto da consulta inserido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-134">The query text entered by the user.</span></span>                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="3b4fd-135">InputLocale</span><span class="sxs-lookup"><span data-stu-id="3b4fd-135">inputlocale</span></span>](search-protocol-localeidentifiers.md)   | <span data-ttu-id="3b4fd-136">Qualquer LCID (identificador de código de idioma) válido</span><span class="sxs-lookup"><span data-stu-id="3b4fd-136">Any valid language code identifier (LCID)</span></span>                     | <span data-ttu-id="3b4fd-137">O LCID que identifica o idioma de entrada para a consulta.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-137">The LCID that identifies the input language for the query.</span></span>                                                                                                                                                                                                                                     |
| [<span data-ttu-id="3b4fd-138">keywordlocale</span><span class="sxs-lookup"><span data-stu-id="3b4fd-138">keywordlocale</span></span>](search-protocol-localeidentifiers.md) | <span data-ttu-id="3b4fd-139">Qualquer LCID válido</span><span class="sxs-lookup"><span data-stu-id="3b4fd-139">Any valid LCID</span></span>                                                | <span data-ttu-id="3b4fd-140">O LCID que identifica o idioma da versão internacional do indexador.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-140">The LCID that identifies the language of the international version of the Indexer.</span></span> <span data-ttu-id="3b4fd-141">O padrão é 1033 (en-US).</span><span class="sxs-lookup"><span data-stu-id="3b4fd-141">The default is 1033 (en-us).</span></span>                                                                                                                                                                                |
| [<span data-ttu-id="3b4fd-142">estrutural</span><span class="sxs-lookup"><span data-stu-id="3b4fd-142">crumb</span></span>](search-protocol-crumb.md)                     | <span data-ttu-id="3b4fd-143">Instrução AQS</span><span class="sxs-lookup"><span data-stu-id="3b4fd-143">AQS statement</span></span>                                                 | <span data-ttu-id="3b4fd-144">Esse argumento restringe o escopo que está sendo pesquisado.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-144">This argument restricts the scope being searched.</span></span> <span data-ttu-id="3b4fd-145">No Windows Vista, o protocolo de pesquisa dá suporte a AQS completas, bem como a uma implementação especial para um `location` argumento.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-145">In Windows Vista, the search protocol supports full AQS as well as a special implementation for a `location` argument.</span></span> <span data-ttu-id="3b4fd-146">No Windows XP, o protocolo de pesquisa também dá suporte a AQS completas, exceto para uma implementação especial do `kind` e do `store` .</span><span class="sxs-lookup"><span data-stu-id="3b4fd-146">In Windows XP, the search protocol also supports full AQS, except for a special implementation of `kind` and `store`.</span></span> |
| [<span data-ttu-id="3b4fd-147">sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b4fd-147">syntax</span></span>](search-protocol-syntaxargument.md)           | <span data-ttu-id="3b4fd-148">NQS, AQS (não diferencia maiúsculas de minúsculas)</span><span class="sxs-lookup"><span data-stu-id="3b4fd-148">NQS, AQS (not case sensitive)</span></span>                                 | <span data-ttu-id="3b4fd-149">A sintaxe de consulta a ser usada para pesquisar o índice: sintaxe de consulta natural ou sintaxe de consulta avançada (AQS).</span><span class="sxs-lookup"><span data-stu-id="3b4fd-149">The query syntax to use to search the index: either Natural Query Syntax or Advanced Query Syntax (AQS).</span></span> <span data-ttu-id="3b4fd-150">AQS é o padrão e sempre é presumido, analisado e suportado.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-150">AQS is the default and is always assumed parsed and supported.</span></span>                                                                                                                        |
| [<span data-ttu-id="3b4fd-151">stackedby</span><span class="sxs-lookup"><span data-stu-id="3b4fd-151">stackedby</span></span>](search-protocol-stackedby.md)             | <span data-ttu-id="3b4fd-152">Qualquer propriedade válida do sistema de propriedades</span><span class="sxs-lookup"><span data-stu-id="3b4fd-152">Any valid property from the property system</span></span>                   | <span data-ttu-id="3b4fd-153">Uma propriedade que especifica a coluna pela qual os resultados são empilhados.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-153">A property that specifies the column to stack results by.</span></span>                                                                                                                                                                                                                                      |
| [<span data-ttu-id="3b4fd-154">subquery</span><span class="sxs-lookup"><span data-stu-id="3b4fd-154">subquery</span></span>](search-protocol-subquery.md)               | <span data-ttu-id="3b4fd-155">Um caminho totalmente especificado para um arquivo de pesquisa salvo ( \* . Search-MS)</span><span class="sxs-lookup"><span data-stu-id="3b4fd-155">A fully specified path for a Saved Search file (\*.search-ms)</span></span> | <span data-ttu-id="3b4fd-156">Os resultados da subconsulta são usados como a origem da consulta.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-156">The results of the subquery are used as the source for the query.</span></span> <span data-ttu-id="3b4fd-157">Ou seja, os termos de consulta são pesquisados em relação aos resultados da subconsulta.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-157">That is, the query terms are searched for against the results of the subquery.</span></span>                                                                                                                                               |
| <span data-ttu-id="3b4fd-158">displayname</span><span class="sxs-lookup"><span data-stu-id="3b4fd-158">displayname</span></span>                                            | <span data-ttu-id="3b4fd-159">Cadeia de caracteres codificada em URL</span><span class="sxs-lookup"><span data-stu-id="3b4fd-159">URL-encoded string</span></span>                                            | <span data-ttu-id="3b4fd-160">O nome da pesquisa atual.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-160">The name of the current search.</span></span>                                                                                                                                                                                                                                                                |



 

## <a name="windows-vista-with-sp1-use-of-the-search-protocol"></a><span data-ttu-id="3b4fd-161">Uso do Windows Vista com SP1 da pesquisa: protocolo</span><span class="sxs-lookup"><span data-stu-id="3b4fd-161">Windows Vista with SP1 use of the search: protocol</span></span>

<span data-ttu-id="3b4fd-162">O Windows Vista com SP1 tem vários pontos de entrada dos quais ele chama o protocolo **Search:** .</span><span class="sxs-lookup"><span data-stu-id="3b4fd-162">Windows Vista with SP1 has several entry points from which it calls the **search:** protocol.</span></span> <span data-ttu-id="3b4fd-163">Esses pontos de entrada são descritos abaixo, bem como a sintaxe comum associada a cada um.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-163">These entry points are outlined below as well as the common syntax associated with each.</span></span>



| <span data-ttu-id="3b4fd-164">Ponto de entrada de protocolo de pesquisa</span><span class="sxs-lookup"><span data-stu-id="3b4fd-164">Search protocol entry point</span></span> | <span data-ttu-id="3b4fd-165">Localização</span><span class="sxs-lookup"><span data-stu-id="3b4fd-165">Location</span></span>         | <span data-ttu-id="3b4fd-166">Consulta chamada</span><span class="sxs-lookup"><span data-stu-id="3b4fd-166">Query called</span></span>                                                         |
|-----------------------------|------------------|----------------------------------------------------------------------|
| <span data-ttu-id="3b4fd-167">**Pesquisar em qualquer lugar**</span><span class="sxs-lookup"><span data-stu-id="3b4fd-167">**Search Everywhere**</span></span>       | <span data-ttu-id="3b4fd-168">Menu **Iniciar**</span><span class="sxs-lookup"><span data-stu-id="3b4fd-168">**Start** menu</span></span>   | <span data-ttu-id="3b4fd-169">pesquisa: consulta =<*termo de pesquisa*></span><span class="sxs-lookup"><span data-stu-id="3b4fd-169">search:query=<*Search Term*></span></span>                                   |
| <span data-ttu-id="3b4fd-170">**Pesquisar em qualquer lugar**</span><span class="sxs-lookup"><span data-stu-id="3b4fd-170">**Search Everywhere**</span></span>       | <span data-ttu-id="3b4fd-171">Windows Explorer</span><span class="sxs-lookup"><span data-stu-id="3b4fd-171">Windows Explorer</span></span> | <span data-ttu-id="3b4fd-172">pesquisa: consulta =<*termo de pesquisa*>&trilha = local: <*local*></span><span class="sxs-lookup"><span data-stu-id="3b4fd-172">search:query=<*Search Term*>&crumb=location:<*LOCATION*></span></span> |
| <span data-ttu-id="3b4fd-173">Tecla de logotipo do Windows +F</span><span class="sxs-lookup"><span data-stu-id="3b4fd-173">Windows logo key+F</span></span>          | <span data-ttu-id="3b4fd-174">Qualquer lugar</span><span class="sxs-lookup"><span data-stu-id="3b4fd-174">Anywhere</span></span>         | <span data-ttu-id="3b4fd-175">procurando</span><span class="sxs-lookup"><span data-stu-id="3b4fd-175">search:</span></span>                                                              |
| <span data-ttu-id="3b4fd-176">Ctrl+F</span><span class="sxs-lookup"><span data-stu-id="3b4fd-176">CTRL+F</span></span>                      | <span data-ttu-id="3b4fd-177">Windows Explorer</span><span class="sxs-lookup"><span data-stu-id="3b4fd-177">Windows Explorer</span></span> | <span data-ttu-id="3b4fd-178">pesquisa: consulta =<*termo de pesquisa*>&trilha = local: <*local*></span><span class="sxs-lookup"><span data-stu-id="3b4fd-178">search:query=<*Search Term*>&crumb=location:<*LOCATION*></span></span> |
| <span data-ttu-id="3b4fd-179">F3</span><span class="sxs-lookup"><span data-stu-id="3b4fd-179">F3</span></span>                          | <span data-ttu-id="3b4fd-180">Menu **Iniciar**</span><span class="sxs-lookup"><span data-stu-id="3b4fd-180">**Start** menu</span></span>   | <span data-ttu-id="3b4fd-181">procurando</span><span class="sxs-lookup"><span data-stu-id="3b4fd-181">search:</span></span>                                                              |
| <span data-ttu-id="3b4fd-182">F3</span><span class="sxs-lookup"><span data-stu-id="3b4fd-182">F3</span></span>                          | <span data-ttu-id="3b4fd-183">Windows Explorer</span><span class="sxs-lookup"><span data-stu-id="3b4fd-183">Windows Explorer</span></span> | <span data-ttu-id="3b4fd-184">pesquisa: consulta =<*termo de pesquisa*>&trilha = local: <*local*></span><span class="sxs-lookup"><span data-stu-id="3b4fd-184">search:query=<*Search Term*>&crumb=location:<*LOCATION*></span></span> |



 

<span data-ttu-id="3b4fd-185">Os pontos de entrada do protocolo de pesquisa do Windows Vista com SP1 não tiram proveito de todos os parâmetros possíveis no protocolo de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-185">The Windows Vista with SP1 search protocol entry points do not take advantage of all the possible parameters in the search protocol.</span></span> <span data-ttu-id="3b4fd-186">Os aplicativos que se preocupam apenas com a manipulação de chamadas de protocolo de pesquisa do Windows Vista com SP1 podem usar a tabela a seguir como um guia para o mínimo que precisam ser implementados.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-186">Applications that are only concerned with handling search protocol calls from Windows Vista with SP1 can use the following table as a guide to the minimum they need to implement.</span></span>



| <span data-ttu-id="3b4fd-187">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="3b4fd-187">Parameter</span></span>                                              | <span data-ttu-id="3b4fd-188">Usado pelo Windows?</span><span class="sxs-lookup"><span data-stu-id="3b4fd-188">Used by Windows?</span></span> | <span data-ttu-id="3b4fd-189">Como o Windows Vista com SP1 o utiliza ao chamar a pesquisa:</span><span class="sxs-lookup"><span data-stu-id="3b4fd-189">How Windows Vista with SP1 uses it when calling search:</span></span>                                                                                                                                                                                                                     |
|--------------------------------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b4fd-190">Consulta</span><span class="sxs-lookup"><span data-stu-id="3b4fd-190">query</span></span>                                                  | <span data-ttu-id="3b4fd-191">Yes</span><span class="sxs-lookup"><span data-stu-id="3b4fd-191">Yes</span></span>              | <span data-ttu-id="3b4fd-192">O texto da consulta inserido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-192">The query text entered by the user.</span></span>                                                                                                                                                                                                                                         |
| [<span data-ttu-id="3b4fd-193">estrutural</span><span class="sxs-lookup"><span data-stu-id="3b4fd-193">crumb</span></span>](search-protocol-crumb.md)                     | <span data-ttu-id="3b4fd-194">Yes</span><span class="sxs-lookup"><span data-stu-id="3b4fd-194">Yes</span></span>              | <span data-ttu-id="3b4fd-195">a [trilha](search-protocol-crumb.md) usa o `location` argumento para especificar de onde veio a consulta.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-195">[crumb](search-protocol-crumb.md) uses the `location` argument to specify where the query came from.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="3b4fd-196">subquery</span><span class="sxs-lookup"><span data-stu-id="3b4fd-196">subquery</span></span>](search-protocol-subquery.md)               | <span data-ttu-id="3b4fd-197">Yes</span><span class="sxs-lookup"><span data-stu-id="3b4fd-197">Yes</span></span>              | <span data-ttu-id="3b4fd-198">Os resultados do argumento de [subconsulta](search-protocol-subquery.md) são usados como o escopo de itens a serem pesquisados.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-198">The results of the [Subquery](search-protocol-subquery.md) argument are used as the scope of items to search.</span></span> <span data-ttu-id="3b4fd-199">Normalmente, isso seria usado se um usuário estivesse usando um arquivo. Search-MS para pesquisar e, em seguida, chamado de aplicativo de pesquisa de desktop padrão de dentro dessa pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-199">This would typically be used if a user was using a .search-ms file to search and then called the default desktop search application from within that search.</span></span> |
| [<span data-ttu-id="3b4fd-200">InputLocale</span><span class="sxs-lookup"><span data-stu-id="3b4fd-200">inputlocale</span></span>](search-protocol-localeidentifiers.md)   | <span data-ttu-id="3b4fd-201">No</span><span class="sxs-lookup"><span data-stu-id="3b4fd-201">No</span></span>               | <span data-ttu-id="3b4fd-202">Não usado no momento.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-202">Not currently used.</span></span>                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="3b4fd-203">keywordlocale</span><span class="sxs-lookup"><span data-stu-id="3b4fd-203">keywordlocale</span></span>](search-protocol-localeidentifiers.md) | <span data-ttu-id="3b4fd-204">No</span><span class="sxs-lookup"><span data-stu-id="3b4fd-204">No</span></span>               | <span data-ttu-id="3b4fd-205">Não usado no momento.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-205">Not currently used.</span></span>                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="3b4fd-206">sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b4fd-206">syntax</span></span>](search-protocol-syntaxargument.md)           | <span data-ttu-id="3b4fd-207">No</span><span class="sxs-lookup"><span data-stu-id="3b4fd-207">No</span></span>               | <span data-ttu-id="3b4fd-208">Não usado no momento.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-208">Not currently used.</span></span>                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="3b4fd-209">stackedby</span><span class="sxs-lookup"><span data-stu-id="3b4fd-209">stackedby</span></span>](search-protocol-stackedby.md)             | <span data-ttu-id="3b4fd-210">No</span><span class="sxs-lookup"><span data-stu-id="3b4fd-210">No</span></span>               | <span data-ttu-id="3b4fd-211">Não usado no momento.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-211">Not currently used.</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="3b4fd-212">displayname</span><span class="sxs-lookup"><span data-stu-id="3b4fd-212">displayname</span></span>                                            | <span data-ttu-id="3b4fd-213">No</span><span class="sxs-lookup"><span data-stu-id="3b4fd-213">No</span></span>               | <span data-ttu-id="3b4fd-214">Não usado no momento.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-214">Not currently used.</span></span>                                                                                                                                                                                                                                                         |



 

## <a name="examples"></a><span data-ttu-id="3b4fd-215">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3b4fd-215">Examples</span></span>

<span data-ttu-id="3b4fd-216">Se um usuário digitar "Microsoft" no menu **Iniciar** e clicar em **Pesquisar em todos os lugares**, a chamada de protocolo de pesquisa resultante será feita:</span><span class="sxs-lookup"><span data-stu-id="3b4fd-216">If a user enters "Microsoft" in the **Start** menu and clicks **Search Everywhere**, the resulting search protocol call is made:</span></span>


```C++
search:query=microsoft&
```



<span data-ttu-id="3b4fd-217">Se um usuário digitar "Seattle" no Windows Explorer em C: \\ MyFolder e clicar em **Pesquisar em todos os lugares**, a chamada a seguir será feita, usando caracteres de escape para ': ' e ' \\ ':</span><span class="sxs-lookup"><span data-stu-id="3b4fd-217">If a user enters "Seattle" in Windows Explorer within C:\\MyFolder and then clicks **Search Everywhere**, the following call is made, using escape characters for ':' and '\\':</span></span>


```C++
search:query=seattle&crumb=location:C%3A%5CMyFolder
```



## <a name="registering-the-application-that-handles-the-protocol"></a><span data-ttu-id="3b4fd-218">Registrando o aplicativo que manipula o protocolo</span><span class="sxs-lookup"><span data-stu-id="3b4fd-218">Registering the Application that Handles the Protocol</span></span>

<span data-ttu-id="3b4fd-219">Como vários aplicativos podem disputar o protocolo de pesquisa, você deve registrar seu aplicativo com o recurso de [programas padrão](default-programs.md) durante a instalação para permitir que o usuário configure o padrão com mais facilidade.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-219">Because multiple applications can contend for the search protocol, you should register your application with the [Default Programs](default-programs.md) feature during installation to enable the user to configure the default more easily.</span></span> <span data-ttu-id="3b4fd-220">Além dos procedimentos de instalação normalmente praticado no Windows XP, um aplicativo baseado no Windows Vista deve se registrar com o recurso de programas padrão para que o aplicativo e os usuários possam configurar os padrões de forma direta.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-220">In addition to the installation procedures normally practiced under Windows XP, a Windows Vista-based application must register with the Default Programs feature so that the application and users can seamlessly configure defaults.</span></span>

<span data-ttu-id="3b4fd-221">Depois de instalar os arquivos binários necessários no computador do usuário, a rotina de instalação deve concluir estas tarefas gerais:</span><span class="sxs-lookup"><span data-stu-id="3b4fd-221">After installing the necessary binary files on the user's computer, your installation routine should complete these general tasks:</span></span>

1.  <span data-ttu-id="3b4fd-222">Escreva ProgIDs para **o \_ \_ computador local hKey**, conforme descrito abaixo.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-222">Write ProgIDs to **HKEY\_LOCAL\_MACHINE**, as described below.</span></span> <span data-ttu-id="3b4fd-223">Observe que os aplicativos devem criar ProgIDs específicos do aplicativo para o protocolo de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-223">Note that applications must create application-specific ProgIDs for the search protocol.</span></span>
2.  <span data-ttu-id="3b4fd-224">Solicitar Associação de protocolo de pesquisa no nível da máquina.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-224">Claim machine-level search protocol association.</span></span>
3.  <span data-ttu-id="3b4fd-225">Registre o aplicativo com [programas padrão](default-programs.md), conforme explicado em [registrando um aplicativo para uso com programas padrão](default-programs.md), como um Contender para o protocolo de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-225">Register the application with [Default Programs](default-programs.md), as explained in [Registering an Application for Use with Default Programs](default-programs.md), as a contender for the search protocol.</span></span>

### <a name="registry-entries"></a><span data-ttu-id="3b4fd-226">Entradas do Registro</span><span class="sxs-lookup"><span data-stu-id="3b4fd-226">Registry Entries</span></span>

<span data-ttu-id="3b4fd-227">Veja a seguir exemplos das entradas de Registro necessárias para um aplicativo de pesquisa de área de trabalho fictício, pesquisa da contoso.</span><span class="sxs-lookup"><span data-stu-id="3b4fd-227">The following are examples of the required registry entries for a fictional desktop search application, Contoso Search.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            URL Protocol = ""
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            DefaultIcon
               (Default) = %ProgramFiles%\Contoso\Search\contososearch.exe,-7
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Contoso\Search\contososearch.exe %1
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      RegisteredApplications
         Contoso Search = "Software\\Contoso\\Search\\Capabilities"
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         Search
            Capabilities
               ApplicationName = "Contoso Search Test App"
               ApplicationDescription = "Contoso search is a great new desktop search application"
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         Search
            Capabilities
               UrlAssociations
                  search = "contoso-search"
```

## <a name="related-topics"></a><span data-ttu-id="3b4fd-228">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3b4fd-228">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b4fd-229">Sintaxe de consulta avançada</span><span class="sxs-lookup"><span data-stu-id="3b4fd-229">Advanced Query Syntax</span></span>](../search/-search-3x-advancedquerysyntax.md)
</dt> <dt>

[<span data-ttu-id="3b4fd-230">Programas padrão</span><span class="sxs-lookup"><span data-stu-id="3b4fd-230">Default Programs</span></span>](default-programs.md)
</dt> </dl>

 

 

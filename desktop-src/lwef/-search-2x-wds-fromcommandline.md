---
title: Chamando o WDS por meio da linha de comando
description: Você pode iniciar a interface do usuário do Microsoft Windows Desktop Search (WDS) com um filtro, uma loja e uma consulta específicos de outro aplicativo ou uma página da Web que usa o BHO (objeto auxiliar do navegador) usando a sintaxe de linha de comando windowssearch.exe.
ms.assetid: fd62f7c9-08a9-4e05-b0bc-e2215cfff59e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efae7aebc13f578e9c5c32542b451d3600a93a2b
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/19/2020
ms.locfileid: "103640278"
---
# <a name="calling-wds-from-the-command-line"></a><span data-ttu-id="d270d-103">Chamando o WDS por meio da linha de comando</span><span class="sxs-lookup"><span data-stu-id="d270d-103">Calling WDS from the Command Line</span></span>

> [!NOTE]
> <span data-ttu-id="d270d-104">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d270d-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="d270d-105">Em versões posteriores, use o [Windows Search](../search/-search-3x-wds-overview.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="d270d-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="d270d-106">Você pode iniciar a interface do usuário do Microsoft Windows Desktop Search (WDS) com um filtro, uma loja e uma consulta específicos de outro aplicativo ou uma página da Web que usa o BHO (objeto auxiliar do navegador) usando a sintaxe de linha de comando windowssearch.exe.</span><span class="sxs-lookup"><span data-stu-id="d270d-106">You can launch the Microsoft Windows Desktop Search (WDS) user interface with a specific filter, store, and query from another application or a webpage that uses the Browser Helper Object (BHO) by using the windowssearch.exe command line syntax.</span></span> <span data-ttu-id="d270d-107">Ao chamar o WDS na linha de comando, nenhuma informação sobre as ações ou a seleção do usuário na janela do WDS é retornada para o aplicativo de chamada ou para a página da Web.</span><span class="sxs-lookup"><span data-stu-id="d270d-107">When calling WDS from the command line, no information about the user's actions or selection in the WDS window is returned to the calling application or webpage.</span></span>

<span data-ttu-id="d270d-108">O caminho de instalação do WDS é especificado na configuração do registro InstallDir em HKEY_LOCAL_MACHINE \\ software \\ Microsoft \\ Windows Desktop Search.</span><span class="sxs-lookup"><span data-stu-id="d270d-108">The WDS installation path is specified in the InstallDir registry setting under HKEY_LOCAL_MACHINE\\Software\\Microsoft\\Windows Desktop Search.</span></span> <span data-ttu-id="d270d-109">O caminho padrão em que o windowssearch.exe é instalado é arquivos de programas \\ Windows Desktop Search.</span><span class="sxs-lookup"><span data-stu-id="d270d-109">The default path that windowssearch.exe is installed to is Program Files\\Windows Desktop Search.</span></span>

## <a name="command-line-syntax"></a><span data-ttu-id="d270d-110">Sintaxe da linha de comando</span><span class="sxs-lookup"><span data-stu-id="d270d-110">Command Line Syntax</span></span>

<span data-ttu-id="d270d-111">A sintaxe a seguir se aplica à interface de linha de comando do Windows Desktop Search 2. x.</span><span class="sxs-lookup"><span data-stu-id="d270d-111">The following syntax applies to the Windows Desktop Search 2.x command-line interface.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d270d-112">Opções</span><span class="sxs-lookup"><span data-stu-id="d270d-112">Options</span></span></th>
<th><span data-ttu-id="d270d-113">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="d270d-113">Parameter</span></span></th>
<th><span data-ttu-id="d270d-114">Significado</span><span class="sxs-lookup"><span data-stu-id="d270d-114">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d270d-115">/startup</span><span class="sxs-lookup"><span data-stu-id="d270d-115">/startup</span></span></td>

<td><span data-ttu-id="d270d-116">Inicializa o Windows Desktop Search</span><span class="sxs-lookup"><span data-stu-id="d270d-116">Initializes Windows Desktop Search</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d270d-117">/indexnow</span><span class="sxs-lookup"><span data-stu-id="d270d-117">/indexnow</span></span></td>

<td><span data-ttu-id="d270d-118">Desativa o desligamento da indexação e examina novamente todos os locais de índice</span><span class="sxs-lookup"><span data-stu-id="d270d-118">Turns off indexing back-off and rescans all index locations</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d270d-119">/showstatus</span><span class="sxs-lookup"><span data-stu-id="d270d-119">/showstatus</span></span></td>

<td><span data-ttu-id="d270d-120">Mostra a janela de status de indexação</span><span class="sxs-lookup"><span data-stu-id="d270d-120">Shows the indexing status window</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d270d-121">/launchsearchwindow ou/URL</span><span class="sxs-lookup"><span data-stu-id="d270d-121">/launchsearchwindow or /url</span></span></td>

<td><span data-ttu-id="d270d-122">Abre uma janela do WDS com uma consulta vazia</span><span class="sxs-lookup"><span data-stu-id="d270d-122">Opens a WDS window with an empty query</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d270d-123">/url</span><span class="sxs-lookup"><span data-stu-id="d270d-123">/url</span></span></td>
<td><span data-ttu-id="d270d-124">pesquisa: [Store | mostrar | consulta] cadeia de caracteres de consulta</span><span class="sxs-lookup"><span data-stu-id="d270d-124">search:[store|show|query] query string</span></span></td>
<td><span data-ttu-id="d270d-125">Abre uma janela do WDS com uma consulta e um filtro com base nos seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="d270d-125">Opens a WDS window with a query and filter based on the following parameters:</span></span>
<ul>
<li><p><span data-ttu-id="d270d-126">Store-especifica a fonte de dados para consultar: arquivos, Outlook, OutlookExpress.</span><span class="sxs-lookup"><span data-stu-id="d270d-126">store - Specifies the data source to query: files, outlook, outlookexpress.</span></span> <span data-ttu-id="d270d-127">Se não for especificado, todos os repositórios serão pesquisados.</span><span class="sxs-lookup"><span data-stu-id="d270d-127">If not specified all stores will be searched.</span></span> <br/></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="d270d-128">Embora a sintaxe de consulta avançada ofereça suporte à referência do Microsoft Outlook como ' OE ', o parâmetro Store na linha de comando deve ser ' OutlookExpress '.</span><span class="sxs-lookup"><span data-stu-id="d270d-128">While Advanced Query Syntax supports referencing Microsoft Outlook as 'oe', the store parameter on the command line must be 'outlookexpress'.</span></span>
</blockquote>
<p><br/></p></li>
<li><p><span data-ttu-id="d270d-129">Mostrar-especifica qual tipo percebido de resultados deve ser retornado.</span><span class="sxs-lookup"><span data-stu-id="d270d-129">show - Specifies which perceived type of results to return.</span></span> <span data-ttu-id="d270d-130">Consulte <a href="-search-2x-wds-perceivedtype.md">tipos observados</a> para obter uma lista completa de tipos.</span><span class="sxs-lookup"><span data-stu-id="d270d-130">See <a href="-search-2x-wds-perceivedtype.md">Perceived Types</a> for a complete list of types.</span></span> <span data-ttu-id="d270d-131">Se não for especificado, todos os tipos serão retornados.</span><span class="sxs-lookup"><span data-stu-id="d270d-131">If not specified, all types will be returned.</span></span> <br/></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="d270d-132">Há três diferenças entre os valores de tipo percebido e os valores para show.</span><span class="sxs-lookup"><span data-stu-id="d270d-132">There are three differences between the perceived type values and the values for show.</span></span> <span data-ttu-id="d270d-133">Para <code>show</code> , use ' documentos ' em vez de ' Doc ', ' imagens ' em vez de ' pics ' e ' textdocuments ' em vez de ' texto '.</span><span class="sxs-lookup"><span data-stu-id="d270d-133">For <code>show</code>, use 'documents' instead of 'doc', 'pictures' instead of 'pics', and 'textdocuments' instead of 'text'.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="d270d-134">consulta-especifica os critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d270d-134">query - Specifies the search criteria.</span></span> <span data-ttu-id="d270d-135">Esse valor dá suporte a parâmetros de <a href="-search-2x-wds-aqsreference.md">sintaxe de consulta avançada</a> para refinar os resultados.</span><span class="sxs-lookup"><span data-stu-id="d270d-135">This value supports <a href="-search-2x-wds-aqsreference.md">Advanced Query Syntax</a> parameters to refine the results.</span></span> <span data-ttu-id="d270d-136">O parâmetro de consulta deve ser o último parâmetro na URL.</span><span class="sxs-lookup"><span data-stu-id="d270d-136">The query parameter must be the last parameter in the URL.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="example"></a><span data-ttu-id="d270d-137">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d270d-137">Example</span></span>

<span data-ttu-id="d270d-138">Por exemplo, para pesquisar todos os arquivos de imagens que correspondem aos critérios de ' wallpaper ', use o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="d270d-138">For example, to search all files for pictures matching the criteria 'wallpaper' use the following command:</span></span>

`WindowsSearch.exe /url search:store=files&show=pictures&query=wallpaper`

## <a name="related-topics"></a><span data-ttu-id="d270d-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d270d-139">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d270d-140">**Referência**</span><span class="sxs-lookup"><span data-stu-id="d270d-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d270d-141">Sintaxe de consulta avançada</span><span class="sxs-lookup"><span data-stu-id="d270d-141">Advanced Query Syntax</span></span>](-search-2x-wds-aqsreference.md)
</dt> <dt>

[<span data-ttu-id="d270d-142">Tipos observados</span><span class="sxs-lookup"><span data-stu-id="d270d-142">Perceived Types</span></span>](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[<span data-ttu-id="d270d-143">Chamando o WDS de páginas da Web</span><span class="sxs-lookup"><span data-stu-id="d270d-143">Calling WDS from Web Pages</span></span>](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

 






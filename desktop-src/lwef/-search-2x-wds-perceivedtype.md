---
title: Tipos observados (recursos de ambiente herdado do Windows)
description: Percebidotype é uma propriedade que classifica um item no índice.
ms.assetid: 47a5cf55-79f6-48e7-a585-72fc3d7d53d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afaf7d8b827495a94b441e5504762dd53dbe733c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105797581"
---
# <a name="perceived-types-legacy-windows-environment-features"></a><span data-ttu-id="83d12-103">Tipos observados (recursos de ambiente herdado do Windows)</span><span class="sxs-lookup"><span data-stu-id="83d12-103">Perceived Types (Legacy Windows Environment Features)</span></span>

> [!NOTE]
> <span data-ttu-id="83d12-104">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="83d12-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="83d12-105">Em versões posteriores, use o [Windows Search](../search/-search-3x-wds-overview.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="83d12-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="83d12-106">`PerceivedType` é uma propriedade que classifica um item no índice.</span><span class="sxs-lookup"><span data-stu-id="83d12-106">`PerceivedType` is a property that classifies an item in the index.</span></span> <span data-ttu-id="83d12-107">Essa classificação é diferente da classificação "Kind" usada pela sintaxe de [consulta avançada](-search-2x-wds-aqsreference.md) , mas, da mesma forma, permite que os usuários refinam seus resultados de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="83d12-107">This classification is different from the "kind" classification used by the [Advanced Query Syntax](-search-2x-wds-aqsreference.md) but similarly lets users refine their search results.</span></span> <span data-ttu-id="83d12-108">O tipo AQS permite que os usuários limitem sua consulta de pesquisa enquanto a propriedade Percebidatype permite que os usuários filtrem seu conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="83d12-108">The AQS kind lets users limit their search query while the PerceivedType property lets users filter their result set.</span></span>

## <a name="types"></a><span data-ttu-id="83d12-109">Tipos</span><span class="sxs-lookup"><span data-stu-id="83d12-109">Types</span></span>

<span data-ttu-id="83d12-110">Use a propriedade Percebidotype para classificar o tipo de arquivo para que os usuários possam filtrar os resultados da pesquisa por tipo.</span><span class="sxs-lookup"><span data-stu-id="83d12-110">Use the PerceivedType property to classify your file type so that users can filter their search results by type.</span></span> <span data-ttu-id="83d12-111">A saída deve ser uma das seguintes cadeias de caracteres:</span><span class="sxs-lookup"><span data-stu-id="83d12-111">The output must be one of the following strings:</span></span>

-   <span data-ttu-id="83d12-112">contact</span><span class="sxs-lookup"><span data-stu-id="83d12-112">contact</span></span>
-   <span data-ttu-id="83d12-113">comunicações</span><span class="sxs-lookup"><span data-stu-id="83d12-113">communications</span></span>
-   <span data-ttu-id="83d12-114">comunicações/email</span><span class="sxs-lookup"><span data-stu-id="83d12-114">communications/email</span></span>
-   <span data-ttu-id="83d12-115">comunicações/calendário</span><span class="sxs-lookup"><span data-stu-id="83d12-115">communications/calendar</span></span>
-   <span data-ttu-id="83d12-116">comunicações/tarefa</span><span class="sxs-lookup"><span data-stu-id="83d12-116">communications/task</span></span>
-   <span data-ttu-id="83d12-117">comunicações/mensagens instantâneas</span><span class="sxs-lookup"><span data-stu-id="83d12-117">communications/im</span></span>
-   <span data-ttu-id="83d12-118">documento</span><span class="sxs-lookup"><span data-stu-id="83d12-118">document</span></span>
-   <span data-ttu-id="83d12-119">documento/anotação</span><span class="sxs-lookup"><span data-stu-id="83d12-119">document/note</span></span>
-   <span data-ttu-id="83d12-120">documento/texto</span><span class="sxs-lookup"><span data-stu-id="83d12-120">document/text</span></span>
-   <span data-ttu-id="83d12-121">documento/planilha</span><span class="sxs-lookup"><span data-stu-id="83d12-121">document/spreadsheet</span></span>
-   <span data-ttu-id="83d12-122">documento/apresentação</span><span class="sxs-lookup"><span data-stu-id="83d12-122">document/presentation</span></span>
-   <span data-ttu-id="83d12-123">music</span><span class="sxs-lookup"><span data-stu-id="83d12-123">music</span></span>
-   <span data-ttu-id="83d12-124">images</span><span class="sxs-lookup"><span data-stu-id="83d12-124">images</span></span>
-   <span data-ttu-id="83d12-125">imagens/imagem</span><span class="sxs-lookup"><span data-stu-id="83d12-125">images/picture</span></span>
-   <span data-ttu-id="83d12-126">imagens/vídeo</span><span class="sxs-lookup"><span data-stu-id="83d12-126">images/video</span></span>
-   <span data-ttu-id="83d12-127">folder</span><span class="sxs-lookup"><span data-stu-id="83d12-127">folder</span></span>
-   <span data-ttu-id="83d12-128">programa</span><span class="sxs-lookup"><span data-stu-id="83d12-128">program</span></span>

<span data-ttu-id="83d12-129">Por exemplo, quando você deseja criar um suplemento de filtro para um novo tipo de arquivo de imagem, você precisa implementar o seguinte na interface do [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter):</span><span class="sxs-lookup"><span data-stu-id="83d12-129">For example, when you want to create a filter add-in for a new picture file type, you need to implement the following in your [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)interface:</span></span>

-   <span data-ttu-id="83d12-130">**GetChunk** para retornar um FULLPROPSPEC que inclui: D5CDD505-2E9C-101B-9397-08002B2CF9AE/percebidotype</span><span class="sxs-lookup"><span data-stu-id="83d12-130">**GetChunk** to return a FULLPROPSPEC that includes: D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedType</span></span>
-   <span data-ttu-id="83d12-131">**GetValue** para retornar um PROPVARIANT que inclui: VT \_ LPWSTR = "images/Picture"</span><span class="sxs-lookup"><span data-stu-id="83d12-131">**GetValue** to return a PROPVARIANT that includes: VT\_LPWSTR = "images/picture"</span></span>

## <a name="related-topics"></a><span data-ttu-id="83d12-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="83d12-132">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="83d12-133">**Referência**</span><span class="sxs-lookup"><span data-stu-id="83d12-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="83d12-134">Desenvolvendo suplementos do IFilter</span><span class="sxs-lookup"><span data-stu-id="83d12-134">Developing IFilter Add-ins</span></span>](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[<span data-ttu-id="83d12-135">Desenvolvendo manipuladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="83d12-135">Developing Protocol Handlers</span></span>](-search-2x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="83d12-136">Sintaxe de consulta avançada</span><span class="sxs-lookup"><span data-stu-id="83d12-136">Advanced Query Syntax</span></span>](-search-2x-wds-aqsreference.md)
</dt> <dt>

[<span data-ttu-id="83d12-137">Esquematable</span><span class="sxs-lookup"><span data-stu-id="83d12-137">SchemaTable</span></span>](-search-2x-wds-schematable.md)
</dt> </dl>

 

 

---
title: Referência ao índice de recurso do pacote (PRI)
description: Referência ao índice de recurso do pacote (PRI)
ms.assetid: 15f41d83-d729-45e4-a6bb-5f8c6b78293c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef99acafe4fbdadef26c5947145ad734ec44b7bd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117544"
---
# <a name="package-resource-indexing-pri-reference"></a><span data-ttu-id="5baf4-103">Referência ao índice de recurso do pacote (PRI)</span><span class="sxs-lookup"><span data-stu-id="5baf4-103">Package resource indexing (PRI) reference</span></span>

<span data-ttu-id="5baf4-104">Um conjunto de APIs para trabalhar com um indexador de recursos.</span><span class="sxs-lookup"><span data-stu-id="5baf4-104">A set of APIs for working with a resource indexer.</span></span> <span data-ttu-id="5baf4-105">Um indexador de recursos é usado para gerar arquivos de índice de recurso de pacote (PRI) para um aplicativo UWP.</span><span class="sxs-lookup"><span data-stu-id="5baf4-105">A resource indexer is used to generate package resource index (PRI) files for a UWP app.</span></span> <span data-ttu-id="5baf4-106">Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="5baf4-106">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5baf4-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="5baf4-107">In this section</span></span>

<span data-ttu-id="5baf4-108">**Funções**</span><span class="sxs-lookup"><span data-stu-id="5baf4-108">**Functions**</span></span>

-   <span data-ttu-id="5baf4-109">Função [**MrmCreateConfig**](mrmcreateconfig.md)</span><span class="sxs-lookup"><span data-stu-id="5baf4-109">[**MrmCreateConfig**](mrmcreateconfig.md) function</span></span>
-   <span data-ttu-id="5baf4-110">Função [**MrmCreateConfigInMemory**](mrmcreateconfiginmemory.md)</span><span class="sxs-lookup"><span data-stu-id="5baf4-110">[**MrmCreateConfigInMemory**](mrmcreateconfiginmemory.md) function</span></span>
-   <span data-ttu-id="5baf4-111">Função [**MrmCreateResourceFile**](mrmcreateresourcefile.md)</span><span class="sxs-lookup"><span data-stu-id="5baf4-111">[**MrmCreateResourceFile**](mrmcreateresourcefile.md) function</span></span>
-   <span data-ttu-id="5baf4-112">Função [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md)</span><span class="sxs-lookup"><span data-stu-id="5baf4-112">[**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) function</span></span>
-   <span data-ttu-id="5baf4-113">Função [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md)</span><span class="sxs-lookup"><span data-stu-id="5baf4-113">[**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md) function</span></span>
-   <span data-ttu-id="5baf4-114">Função [**MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md)</span><span class="sxs-lookup"><span data-stu-id="5baf4-114">[**MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md) function</span></span>
-   <span data-ttu-id="5baf4-115">Função [**MrmCreateResourceIndexerFromPreviousPriFile**](mrmcreateresourceindexerfrompreviousprifile.md)</span><span class="sxs-lookup"><span data-stu-id="5baf4-115">[**MrmCreateResourceIndexerFromPreviousPriFile**](mrmcreateresourceindexerfrompreviousprifile.md) function</span></span>
-   <span data-ttu-id="5baf4-116">Função [**MrmCreateResourceIndexerFromPreviousSchemaData**](mrmcreateresourceindexerfrompreviousschemadata.md)</span><span class="sxs-lookup"><span data-stu-id="5baf4-116">[**MrmCreateResourceIndexerFromPreviousSchemaData**](mrmcreateresourceindexerfrompreviousschemadata.md) function</span></span>
-   <span data-ttu-id="5baf4-117">Função [**MrmCreateResourceIndexerFromPreviousSchemaFile**](mrmcreateresourceindexerfrompreviousschemafile.md)</span><span class="sxs-lookup"><span data-stu-id="5baf4-117">[**MrmCreateResourceIndexerFromPreviousSchemaFile**](mrmcreateresourceindexerfrompreviousschemafile.md) function</span></span>
-   <span data-ttu-id="5baf4-118">Função [**MrmDestroyIndexerAndMessages**](mrmdestroyindexerandmessages.md)</span><span class="sxs-lookup"><span data-stu-id="5baf4-118">[**MrmDestroyIndexerAndMessages**](mrmdestroyindexerandmessages.md) function</span></span>
-   <span data-ttu-id="5baf4-119">Função [**MrmDumpPriFile**](mrmdumpprifile.md)</span><span class="sxs-lookup"><span data-stu-id="5baf4-119">[**MrmDumpPriFile**](mrmdumpprifile.md) function</span></span>
-   <span data-ttu-id="5baf4-120">Função [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md)</span><span class="sxs-lookup"><span data-stu-id="5baf4-120">[**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md) function</span></span>
-   <span data-ttu-id="5baf4-121">Função [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md)</span><span class="sxs-lookup"><span data-stu-id="5baf4-121">[**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md) function</span></span>
-   <span data-ttu-id="5baf4-122">Função [**MrmFreeMemory**](mrmfreememory.md)</span><span class="sxs-lookup"><span data-stu-id="5baf4-122">[**MrmFreeMemory**](mrmfreememory.md) function</span></span>
-   <span data-ttu-id="5baf4-123">Função [**MrmIndexEmbeddedData**](mrmindexembeddeddata.md)</span><span class="sxs-lookup"><span data-stu-id="5baf4-123">[**MrmIndexEmbeddedData**](mrmindexembeddeddata.md) function</span></span>
-   <span data-ttu-id="5baf4-124">Função [**MrmIndexFile**](mrmindexfile.md)</span><span class="sxs-lookup"><span data-stu-id="5baf4-124">[**MrmIndexFile**](mrmindexfile.md) function</span></span>
-   <span data-ttu-id="5baf4-125">Função [**MrmIndexFileAutoQualifiers**](mrmindexfileautoqualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="5baf4-125">[**MrmIndexFileAutoQualifiers**](mrmindexfileautoqualifiers.md) function</span></span>
-   <span data-ttu-id="5baf4-126">Função [**MrmIndexResourceContainerAutoQualifiers**](mrmindexresourcecontainerautoqualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="5baf4-126">[**MrmIndexResourceContainerAutoQualifiers**](mrmindexresourcecontainerautoqualifiers.md) function</span></span>
-   <span data-ttu-id="5baf4-127">Função [**MrmIndexString**](mrmindexstring.md)</span><span class="sxs-lookup"><span data-stu-id="5baf4-127">[**MrmIndexString**](mrmindexstring.md) function</span></span>
-   <span data-ttu-id="5baf4-128">Função [**MrmPeekResourceIndexerMessages**](mrmpeekresourceindexermessages.md)</span><span class="sxs-lookup"><span data-stu-id="5baf4-128">[**MrmPeekResourceIndexerMessages**](mrmpeekresourceindexermessages.md) function</span></span>

<span data-ttu-id="5baf4-129">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="5baf4-129">**Structures**</span></span>

-   <span data-ttu-id="5baf4-130">Estrutura [**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)</span><span class="sxs-lookup"><span data-stu-id="5baf4-130">[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) structure</span></span>
-   <span data-ttu-id="5baf4-131">Estrutura [**MrmResourceIndexerMessage**](mrmresourceindexermessage.md)</span><span class="sxs-lookup"><span data-stu-id="5baf4-131">[**MrmResourceIndexerMessage**](mrmresourceindexermessage.md) structure</span></span>

<span data-ttu-id="5baf4-132">**Enumerações**</span><span class="sxs-lookup"><span data-stu-id="5baf4-132">**Enumerations**</span></span>

-   <span data-ttu-id="5baf4-133">Enumeração [**MrmDumpType**](mrmdumptype.md)</span><span class="sxs-lookup"><span data-stu-id="5baf4-133">[**MrmDumpType**](mrmdumptype.md) enumeration</span></span>
-   <span data-ttu-id="5baf4-134">Enumeração [**MrmPackagingMode**](mrmpackagingmode.md)</span><span class="sxs-lookup"><span data-stu-id="5baf4-134">[**MrmPackagingMode**](mrmpackagingmode.md) enumeration</span></span>
-   <span data-ttu-id="5baf4-135">Enumeração [**MrmPackagingOptions**](mrmpackagingoptions.md)</span><span class="sxs-lookup"><span data-stu-id="5baf4-135">[**MrmPackagingOptions**](mrmpackagingoptions.md) enumeration</span></span>
-   <span data-ttu-id="5baf4-136">Enumeração [**MrmPlatformVersion**](mrmplatformversion.md)</span><span class="sxs-lookup"><span data-stu-id="5baf4-136">[**MrmPlatformVersion**](mrmplatformversion.md) enumeration</span></span>
-   <span data-ttu-id="5baf4-137">Enumeração [**MrmResourceIndexerMessageSeverity**](mrmresourceindexermessageseverity.md)</span><span class="sxs-lookup"><span data-stu-id="5baf4-137">[**MrmResourceIndexerMessageSeverity**](mrmresourceindexermessageseverity.md) enumeration</span></span>

 

 

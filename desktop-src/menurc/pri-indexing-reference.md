---
title: Referência ao índice de recurso do pacote (PRI)
description: .
ms.assetid: 15f41d83-d729-45e4-a6bb-5f8c6b78293c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b75c0739b4e7673863a21223fbed749c27e65dc4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917306"
---
# <a name="package-resource-indexing-pri-reference"></a><span data-ttu-id="65439-103">Referência ao índice de recurso do pacote (PRI)</span><span class="sxs-lookup"><span data-stu-id="65439-103">Package resource indexing (PRI) reference</span></span>

<span data-ttu-id="65439-104">Um conjunto de APIs para trabalhar com um indexador de recursos.</span><span class="sxs-lookup"><span data-stu-id="65439-104">A set of APIs for working with a resource indexer.</span></span> <span data-ttu-id="65439-105">Um indexador de recursos é usado para gerar arquivos de índice de recurso de pacote (PRI) para um aplicativo UWP.</span><span class="sxs-lookup"><span data-stu-id="65439-105">A resource indexer is used to generate package resource index (PRI) files for a UWP app.</span></span> <span data-ttu-id="65439-106">Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="65439-106">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="65439-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="65439-107">In this section</span></span>

<span data-ttu-id="65439-108">**Funções**</span><span class="sxs-lookup"><span data-stu-id="65439-108">**Functions**</span></span>

-   <span data-ttu-id="65439-109">Função [**MrmCreateConfig**](mrmcreateconfig.md)</span><span class="sxs-lookup"><span data-stu-id="65439-109">[**MrmCreateConfig**](mrmcreateconfig.md) function</span></span>
-   <span data-ttu-id="65439-110">Função [**MrmCreateConfigInMemory**](mrmcreateconfiginmemory.md)</span><span class="sxs-lookup"><span data-stu-id="65439-110">[**MrmCreateConfigInMemory**](mrmcreateconfiginmemory.md) function</span></span>
-   <span data-ttu-id="65439-111">Função [**MrmCreateResourceFile**](mrmcreateresourcefile.md)</span><span class="sxs-lookup"><span data-stu-id="65439-111">[**MrmCreateResourceFile**](mrmcreateresourcefile.md) function</span></span>
-   <span data-ttu-id="65439-112">Função [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md)</span><span class="sxs-lookup"><span data-stu-id="65439-112">[**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) function</span></span>
-   <span data-ttu-id="65439-113">Função [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md)</span><span class="sxs-lookup"><span data-stu-id="65439-113">[**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md) function</span></span>
-   <span data-ttu-id="65439-114">Função [**MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md)</span><span class="sxs-lookup"><span data-stu-id="65439-114">[**MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md) function</span></span>
-   <span data-ttu-id="65439-115">Função [**MrmCreateResourceIndexerFromPreviousPriFile**](mrmcreateresourceindexerfrompreviousprifile.md)</span><span class="sxs-lookup"><span data-stu-id="65439-115">[**MrmCreateResourceIndexerFromPreviousPriFile**](mrmcreateresourceindexerfrompreviousprifile.md) function</span></span>
-   <span data-ttu-id="65439-116">Função [**MrmCreateResourceIndexerFromPreviousSchemaData**](mrmcreateresourceindexerfrompreviousschemadata.md)</span><span class="sxs-lookup"><span data-stu-id="65439-116">[**MrmCreateResourceIndexerFromPreviousSchemaData**](mrmcreateresourceindexerfrompreviousschemadata.md) function</span></span>
-   <span data-ttu-id="65439-117">Função [**MrmCreateResourceIndexerFromPreviousSchemaFile**](mrmcreateresourceindexerfrompreviousschemafile.md)</span><span class="sxs-lookup"><span data-stu-id="65439-117">[**MrmCreateResourceIndexerFromPreviousSchemaFile**](mrmcreateresourceindexerfrompreviousschemafile.md) function</span></span>
-   <span data-ttu-id="65439-118">Função [**MrmDestroyIndexerAndMessages**](mrmdestroyindexerandmessages.md)</span><span class="sxs-lookup"><span data-stu-id="65439-118">[**MrmDestroyIndexerAndMessages**](mrmdestroyindexerandmessages.md) function</span></span>
-   <span data-ttu-id="65439-119">Função [**MrmDumpPriFile**](mrmdumpprifile.md)</span><span class="sxs-lookup"><span data-stu-id="65439-119">[**MrmDumpPriFile**](mrmdumpprifile.md) function</span></span>
-   <span data-ttu-id="65439-120">Função [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md)</span><span class="sxs-lookup"><span data-stu-id="65439-120">[**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md) function</span></span>
-   <span data-ttu-id="65439-121">Função [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md)</span><span class="sxs-lookup"><span data-stu-id="65439-121">[**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md) function</span></span>
-   <span data-ttu-id="65439-122">Função [**MrmFreeMemory**](mrmfreememory.md)</span><span class="sxs-lookup"><span data-stu-id="65439-122">[**MrmFreeMemory**](mrmfreememory.md) function</span></span>
-   <span data-ttu-id="65439-123">Função [**MrmIndexEmbeddedData**](mrmindexembeddeddata.md)</span><span class="sxs-lookup"><span data-stu-id="65439-123">[**MrmIndexEmbeddedData**](mrmindexembeddeddata.md) function</span></span>
-   <span data-ttu-id="65439-124">Função [**MrmIndexFile**](mrmindexfile.md)</span><span class="sxs-lookup"><span data-stu-id="65439-124">[**MrmIndexFile**](mrmindexfile.md) function</span></span>
-   <span data-ttu-id="65439-125">Função [**MrmIndexFileAutoQualifiers**](mrmindexfileautoqualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="65439-125">[**MrmIndexFileAutoQualifiers**](mrmindexfileautoqualifiers.md) function</span></span>
-   <span data-ttu-id="65439-126">Função [**MrmIndexResourceContainerAutoQualifiers**](mrmindexresourcecontainerautoqualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="65439-126">[**MrmIndexResourceContainerAutoQualifiers**](mrmindexresourcecontainerautoqualifiers.md) function</span></span>
-   <span data-ttu-id="65439-127">Função [**MrmIndexString**](mrmindexstring.md)</span><span class="sxs-lookup"><span data-stu-id="65439-127">[**MrmIndexString**](mrmindexstring.md) function</span></span>
-   <span data-ttu-id="65439-128">Função [**MrmPeekResourceIndexerMessages**](mrmpeekresourceindexermessages.md)</span><span class="sxs-lookup"><span data-stu-id="65439-128">[**MrmPeekResourceIndexerMessages**](mrmpeekresourceindexermessages.md) function</span></span>

<span data-ttu-id="65439-129">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="65439-129">**Structures**</span></span>

-   <span data-ttu-id="65439-130">Estrutura [**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)</span><span class="sxs-lookup"><span data-stu-id="65439-130">[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) structure</span></span>
-   <span data-ttu-id="65439-131">Estrutura [**MrmResourceIndexerMessage**](mrmresourceindexermessage.md)</span><span class="sxs-lookup"><span data-stu-id="65439-131">[**MrmResourceIndexerMessage**](mrmresourceindexermessage.md) structure</span></span>

<span data-ttu-id="65439-132">**Enumerações**</span><span class="sxs-lookup"><span data-stu-id="65439-132">**Enumerations**</span></span>

-   <span data-ttu-id="65439-133">Enumeração [**MrmDumpType**](mrmdumptype.md)</span><span class="sxs-lookup"><span data-stu-id="65439-133">[**MrmDumpType**](mrmdumptype.md) enumeration</span></span>
-   <span data-ttu-id="65439-134">Enumeração [**MrmPackagingMode**](mrmpackagingmode.md)</span><span class="sxs-lookup"><span data-stu-id="65439-134">[**MrmPackagingMode**](mrmpackagingmode.md) enumeration</span></span>
-   <span data-ttu-id="65439-135">Enumeração [**MrmPackagingOptions**](mrmpackagingoptions.md)</span><span class="sxs-lookup"><span data-stu-id="65439-135">[**MrmPackagingOptions**](mrmpackagingoptions.md) enumeration</span></span>
-   <span data-ttu-id="65439-136">Enumeração [**MrmPlatformVersion**](mrmplatformversion.md)</span><span class="sxs-lookup"><span data-stu-id="65439-136">[**MrmPlatformVersion**](mrmplatformversion.md) enumeration</span></span>
-   <span data-ttu-id="65439-137">Enumeração [**MrmResourceIndexerMessageSeverity**](mrmresourceindexermessageseverity.md)</span><span class="sxs-lookup"><span data-stu-id="65439-137">[**MrmResourceIndexerMessageSeverity**](mrmresourceindexermessageseverity.md) enumeration</span></span>

 

 
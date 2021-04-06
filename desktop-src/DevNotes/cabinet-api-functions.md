---
description: 'Saiba mais sobre: funções de API de gabinete'
ms.assetid: 43afef50-8fd2-49ec-9fb4-dafd8ebc009e
title: Funções de API de gabinete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327490332d2fe0cb9384eeaaad11215d551f4f0c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826285"
---
# <a name="cabinet-api-functions"></a><span data-ttu-id="f7a8b-103">Funções de API de gabinete</span><span class="sxs-lookup"><span data-stu-id="f7a8b-103">Cabinet API Functions</span></span>

<span data-ttu-id="f7a8b-104">Esta seção descreve as seguintes funções de API de gabinete:</span><span class="sxs-lookup"><span data-stu-id="f7a8b-104">This section describes the following Cabinet API functions:</span></span>

## <a name="fci-functions"></a><span data-ttu-id="f7a8b-105">Funções FCI</span><span class="sxs-lookup"><span data-stu-id="f7a8b-105">FCI Functions</span></span>

<span data-ttu-id="f7a8b-106">A biblioteca FCI (File Compression interface) fornece a capacidade de criar gabinetes (também conhecidos como "arquivos CAB").</span><span class="sxs-lookup"><span data-stu-id="f7a8b-106">The FCI (File Compression Interface) library provides the ability to create cabinets (also known as "CAB files").</span></span> <span data-ttu-id="f7a8b-107">Além disso, a biblioteca fornece compactação para reduzir o tamanho dos dados de arquivo armazenados em gabinetes.</span><span class="sxs-lookup"><span data-stu-id="f7a8b-107">Additionally, the library provides compression to reduce the size of the file data stored in cabinets.</span></span>



| <span data-ttu-id="f7a8b-108">Função</span><span class="sxs-lookup"><span data-stu-id="f7a8b-108">Function</span></span>                                   | <span data-ttu-id="f7a8b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="f7a8b-109">Description</span></span>                                                                                                 |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7a8b-110">**FCIAddFile**</span><span class="sxs-lookup"><span data-stu-id="f7a8b-110">**FCIAddFile**</span></span>](/windows/desktop/api/Fci/nf-fci-fciaddfile)           | <span data-ttu-id="f7a8b-111">Adiciona um arquivo ao gabinete que está sendo construído no momento.</span><span class="sxs-lookup"><span data-stu-id="f7a8b-111">Adds a file to the cabinet currently being contructed.</span></span><br/>                                           |
| [<span data-ttu-id="f7a8b-112">**FCICreate**</span><span class="sxs-lookup"><span data-stu-id="f7a8b-112">**FCICreate**</span></span>](/windows/desktop/api/Fci/nf-fci-fcicreate)             | <span data-ttu-id="f7a8b-113">Cria um contexto de FCI.</span><span class="sxs-lookup"><span data-stu-id="f7a8b-113">Creates an FCI context.</span></span><br/>                                                                          |
| [<span data-ttu-id="f7a8b-114">**FCIDestroy**</span><span class="sxs-lookup"><span data-stu-id="f7a8b-114">**FCIDestroy**</span></span>](/windows/desktop/api/Fci/nf-fci-fcidestroy)           | <span data-ttu-id="f7a8b-115">Exclui um contexto Open FCI, liberando qualquer memória e arquivos temporários associados ao contexto.</span><span class="sxs-lookup"><span data-stu-id="f7a8b-115">Deletes an open FCI context, freeing any memory and temporary files associated with the context.</span></span><br/> |
| [<span data-ttu-id="f7a8b-116">**FCIFlushCabinet**</span><span class="sxs-lookup"><span data-stu-id="f7a8b-116">**FCIFlushCabinet**</span></span>](/windows/desktop/api/Fci/nf-fci-fciflushcabinet) | <span data-ttu-id="f7a8b-117">Conclui o gabinete atual.</span><span class="sxs-lookup"><span data-stu-id="f7a8b-117">Completes the current cabinet.</span></span><br/>                                                                   |
| [<span data-ttu-id="f7a8b-118">**FCIFlushFolder**</span><span class="sxs-lookup"><span data-stu-id="f7a8b-118">**FCIFlushFolder**</span></span>](/windows/desktop/api/Fci/nf-fci-fciflushfolder)   | <span data-ttu-id="f7a8b-119">Força a pasta atual em construção a ser concluída imediatamente.</span><span class="sxs-lookup"><span data-stu-id="f7a8b-119">Forces the current folder under construction to be completed immediately.</span></span><br/>                        |



 

## <a name="fdi-functions"></a><span data-ttu-id="f7a8b-120">Funções FDI</span><span class="sxs-lookup"><span data-stu-id="f7a8b-120">FDI Functions</span></span>

<span data-ttu-id="f7a8b-121">A biblioteca FDI (File descompression interface) fornece a capacidade de extrair arquivos de gabinetes.</span><span class="sxs-lookup"><span data-stu-id="f7a8b-121">The FDI (File Decompression Interface) library provides the ability to extract files from cabinets.</span></span>



| <span data-ttu-id="f7a8b-122">Função</span><span class="sxs-lookup"><span data-stu-id="f7a8b-122">Function</span></span>                                         | <span data-ttu-id="f7a8b-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="f7a8b-123">Description</span></span>                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7a8b-124">**FDICopy**</span><span class="sxs-lookup"><span data-stu-id="f7a8b-124">**FDICopy**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fdicopy)                       | <span data-ttu-id="f7a8b-125">Extrai arquivos de gabinetes.</span><span class="sxs-lookup"><span data-stu-id="f7a8b-125">Extracts files from cabinets.</span></span><br/>                                                          |
| [<span data-ttu-id="f7a8b-126">**FDICreate**</span><span class="sxs-lookup"><span data-stu-id="f7a8b-126">**FDICreate**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fdicreate)                   | <span data-ttu-id="f7a8b-127">Cria um contexto FDI.</span><span class="sxs-lookup"><span data-stu-id="f7a8b-127">Creates an FDI context.</span></span><br/>                                                                |
| [<span data-ttu-id="f7a8b-128">**FDIDestroy**</span><span class="sxs-lookup"><span data-stu-id="f7a8b-128">**FDIDestroy**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fdidestroy)                 | <span data-ttu-id="f7a8b-129">Exclui um contexto FDI aberto.</span><span class="sxs-lookup"><span data-stu-id="f7a8b-129">Deletes an open FDI context.</span></span><br/>                                                           |
| [<span data-ttu-id="f7a8b-130">**FDIIsCabinet**</span><span class="sxs-lookup"><span data-stu-id="f7a8b-130">**FDIIsCabinet**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fdiiscabinet)             | <span data-ttu-id="f7a8b-131">Determina se um arquivo é um gabinete e, se for, retorna informações descritivas.</span><span class="sxs-lookup"><span data-stu-id="f7a8b-131">Determines whether a file is a cabinet and, if it is, returns descriptive information.</span></span><br/> |
| [<span data-ttu-id="f7a8b-132">**FDITruncateCabinet**</span><span class="sxs-lookup"><span data-stu-id="f7a8b-132">**FDITruncateCabinet**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fditruncatecabinet) | <span data-ttu-id="f7a8b-133">Trunca um arquivo de gabinete que começa no número de pasta especificado.</span><span class="sxs-lookup"><span data-stu-id="f7a8b-133">Truncates a cabinet file starting at the specified folder number.</span></span><br/>                      |



 

## <a name="deprecated-functions"></a><span data-ttu-id="f7a8b-134">Funções preteridas</span><span class="sxs-lookup"><span data-stu-id="f7a8b-134">Deprecated Functions</span></span>

-   [<span data-ttu-id="f7a8b-135">**DeleteExtractedFiles**</span><span class="sxs-lookup"><span data-stu-id="f7a8b-135">**DeleteExtractedFiles**</span></span>](deleteextractedfiles.md)
-   [<span data-ttu-id="f7a8b-136">**DllGetVersion**</span><span class="sxs-lookup"><span data-stu-id="f7a8b-136">**DllGetVersion**</span></span>](dllgetversion.md)
-   [<span data-ttu-id="f7a8b-137">**Extração**</span><span class="sxs-lookup"><span data-stu-id="f7a8b-137">**Extract**</span></span>](extract.md)
-   [<span data-ttu-id="f7a8b-138">**GetDllVersion**</span><span class="sxs-lookup"><span data-stu-id="f7a8b-138">**GetDllVersion**</span></span>](getdllversion.md)

## <a name="related-topics"></a><span data-ttu-id="f7a8b-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f7a8b-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7a8b-140">Referência de API de gabinete</span><span class="sxs-lookup"><span data-stu-id="f7a8b-140">Cabinet API Reference</span></span>](cabinet-api-reference.md)
</dt> <dt>

[<span data-ttu-id="f7a8b-141">Usando a API do gabinete</span><span class="sxs-lookup"><span data-stu-id="f7a8b-141">Using the Cabinet API</span></span>](using-the-cabinet-api.md)
</dt> </dl>

 

 





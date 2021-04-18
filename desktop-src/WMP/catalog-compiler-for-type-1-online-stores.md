---
title: Compilador de catálogo para repositórios online do tipo 1
description: Compilador de catálogo para repositórios online do tipo 1
ms.assetid: 49c03d3b-3381-4663-83c8-5bc8fa70f7c3
keywords:
- Armazenamentos online do Windows Media Player, compilador de catálogo
- lojas online, compilador de catálogo
- tipo 1 lojas online, compilador de catálogo
- Armazenamentos online do Windows Media Player, catcomp.exe
- lojas online, catcomp.exe
- Digite 1 lojas online, catcomp.exe
- compilador de catálogo
- catcomp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4c54ffd054c5e72b04ddd32eef12c7fe6b6cc89
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105763364"
---
# <a name="catalog-compiler-for-type-1-online-stores"></a><span data-ttu-id="ba04d-111">Compilador de catálogo para repositórios online do tipo 1</span><span class="sxs-lookup"><span data-stu-id="ba04d-111">Catalog Compiler for Type 1 Online Stores</span></span>

<span data-ttu-id="ba04d-112">O compilador de catálogo (catcomp.exe) é uma ferramenta de linha de comando usada por repositórios online do tipo 1 para compilar o conjunto de arquivos TSV (valores separados por tabulação) que contém os dados do catálogo da loja online em um catálogo compactado que pode ser baixado pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="ba04d-112">The catalog compiler (catcomp.exe) is a command-line tool used by Type 1 online stores to compile the set of tab-separated-value (TSV) files containing the online store's catalog data into a compressed catalog that can be downloaded by Windows Media Player.</span></span> <span data-ttu-id="ba04d-113">O compilador de catálogo também compila arquivos de atualização de catálogo contendo apenas as informações do catálogo que foram alteradas desde a última atualização do catálogo.</span><span class="sxs-lookup"><span data-stu-id="ba04d-113">The catalog compiler also compiles catalog update files containing only the catalog information that has changed since the last catalog update.</span></span>

<span data-ttu-id="ba04d-114">Os arquivos de catálogo compactados ou os arquivos de atualização de catálogo devem ser fornecidos ao Windows Media Player para download na implementação do plug-in da loja online de [IWMPContentPartner:: GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span><span class="sxs-lookup"><span data-stu-id="ba04d-114">The compressed catalog files or catalog update files should be provided to Windows Media Player for download in the online store plug-in's implementation of [IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span></span>

<span data-ttu-id="ba04d-115">Tarefas comuns</span><span class="sxs-lookup"><span data-stu-id="ba04d-115">Common Tasks</span></span>

-   [<span data-ttu-id="ba04d-116">Compilando um catálogo completo de arquivos TSV</span><span class="sxs-lookup"><span data-stu-id="ba04d-116">Compiling a Full Catalog from TSV Files</span></span>](compiling-a-full-catalog-from-tsv-files.md)
-   [<span data-ttu-id="ba04d-117">Compilando uma atualização de catálogo de catálogos completos</span><span class="sxs-lookup"><span data-stu-id="ba04d-117">Compiling a Catalog Update from Full Catalogs</span></span>](compiling-a-catalog-update-from-full-catalogs.md)

<span data-ttu-id="ba04d-118">Tarefas de diagnóstico</span><span class="sxs-lookup"><span data-stu-id="ba04d-118">Diagnostic Tasks</span></span>

-   [<span data-ttu-id="ba04d-119">Exibindo a ajuda</span><span class="sxs-lookup"><span data-stu-id="ba04d-119">Displaying Help</span></span>](displaying-help.md)
-   [<span data-ttu-id="ba04d-120">Recuperando Informações do catálogo</span><span class="sxs-lookup"><span data-stu-id="ba04d-120">Retrieving Catalog Information</span></span>](retrieving-catalog-information.md)
-   [<span data-ttu-id="ba04d-121">Aplicando uma atualização a um catálogo</span><span class="sxs-lookup"><span data-stu-id="ba04d-121">Applying an Update To a Catalog</span></span>](applying-an-update-to-a-catalog.md)

 

 





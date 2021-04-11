---
title: Compilando uma atualização de catálogo de catálogos completos
description: Compilando uma atualização de catálogo de catálogos completos
ms.assetid: 046c0a01-0ad7-41b6-bad5-dcab953a3980
keywords:
- Lojas online do Windows Media Player, compilando catálogos
- lojas online, compilando catálogos
- Digite 1 lojas online, compilando catálogos
- Armazenamentos online do Windows Media Player, atualizações de catálogo
- lojas online, atualizações de catálogo
- Digite 1 lojas online, atualizações de catálogo
- Lojas online do Windows Media Player, catálogos completos
- lojas online, catálogos completos
- Digite 1 lojas online, catálogos completos
- Compilando catálogos
- atualizações do catálogo
- catálogos completos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abaa6d1bc0d3dbc4fefaffe1498be03259716a5e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104293752"
---
# <a name="compiling-a-catalog-update-from-full-catalogs"></a><span data-ttu-id="498f0-115">Compilando uma atualização de catálogo de catálogos completos</span><span class="sxs-lookup"><span data-stu-id="498f0-115">Compiling a Catalog Update from Full Catalogs</span></span>

<span data-ttu-id="498f0-116">Uma atualização de catálogo que contém as alterações entre duas versões de um catálogo compilado pode ser criada usando a sintaxe abaixo, em que *caminho1* é o diretório que contém o primeiro catálogo, o *caminho* 2 é o diretório que contém o segundo catálogo e a depuração pode ser incluída opcionalmente para exibir informações detalhadas de erro na tela.</span><span class="sxs-lookup"><span data-stu-id="498f0-116">A catalog update containing the changes between two versions of a compiled catalog can be created by using the syntax below, where *path1* is the directory containing the first catalog, *path2* is the directory containing the second catalog, and debug can be optionally included to display detailed error information on the screen.</span></span> <span data-ttu-id="498f0-117">Os arquivos de catálogo devem estar em formato descompactado – o nome de arquivo do catálogo compilado seria Catalog. wmdb, em vez de Catalog. wmdb. LZ.</span><span class="sxs-lookup"><span data-stu-id="498f0-117">The catalog files must be in uncompressed form—the file name of the compiled catalog would be catalog.wmdb, rather than catalog.wmdb.lz.</span></span>


```C++
catcomp diff <path1> <path2> [debug]
```



<span data-ttu-id="498f0-118">Por exemplo, se o diretório C: \\ Catalog210 \\ contiver a versão 210 de um catálogo completo compilado e C: \\ Catalog211 \\ contiver a versão 211, o comando a seguir criará um arquivo de diferenças que contém as alterações entre as duas versões:</span><span class="sxs-lookup"><span data-stu-id="498f0-118">For example, if the C:\\Catalog210\\ directory contains version 210 of a full compiled catalog and C:\\Catalog211\\ contains version 211, the following command creates a difference file that contains the changes between the two versions:</span></span>


```C++
catcomp diff C:\Catalog210\ C:\Catalog211\
```



<span data-ttu-id="498f0-119">Para exibir informações detalhadas de erro, você pode adicionar o parâmetro de depuração opcional da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="498f0-119">To display detailed error information, you can add the optional debug parameter as follows:</span></span>


```C++
catcomp diff C:\Catalog210\ C:\Catalog211\ debug
```



<span data-ttu-id="498f0-120">Se a compilação for bem-sucedida, catcomp.exe criará os arquivos de saída listados abaixo e os salvará no diretório que contém o primeiro catálogo.</span><span class="sxs-lookup"><span data-stu-id="498f0-120">If compilation is successful, catcomp.exe creates the output files listed below and saves them in the directory that contains the first catalog.</span></span>



| <span data-ttu-id="498f0-121">Nome do arquivo</span><span class="sxs-lookup"><span data-stu-id="498f0-121">File name</span></span>             | <span data-ttu-id="498f0-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="498f0-122">Description</span></span>                                                                                                                                                                                      |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="498f0-123">Catalog. diff</span><span class="sxs-lookup"><span data-stu-id="498f0-123">catalog.diff</span></span>          | <span data-ttu-id="498f0-124">Arquivo de diferença compilado não compactado.</span><span class="sxs-lookup"><span data-stu-id="498f0-124">Uncompressed compiled difference file.</span></span>                                                                                                                                                           |
| <span data-ttu-id="498f0-125">Catalog. diff. LZ</span><span class="sxs-lookup"><span data-stu-id="498f0-125">catalog.diff.lz</span></span>       | <span data-ttu-id="498f0-126">Versão compactada do arquivo de atualização do catálogo.</span><span class="sxs-lookup"><span data-stu-id="498f0-126">Compressed version of catalog update file.</span></span> <span data-ttu-id="498f0-127">Seu plug-in pode fornecer o local desse arquivo ao Windows Media Player em [IWMPContentPartner:: GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span><span class="sxs-lookup"><span data-stu-id="498f0-127">Your plug-in can give the location of this file to Windows Media Player in [IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span></span> |
| <span data-ttu-id="498f0-128">Catalog. wmdb. Delta</span><span class="sxs-lookup"><span data-stu-id="498f0-128">catalog.wmdb.delta</span></span>    | <span data-ttu-id="498f0-129">Arquivo de saída intermediário.</span><span class="sxs-lookup"><span data-stu-id="498f0-129">Intermediate output file.</span></span> <span data-ttu-id="498f0-130">Não usado pelo Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="498f0-130">Not used by Windows Media Player</span></span>                                                                                                                                       |
| <span data-ttu-id="498f0-131">Catalog. wmdb. Modified</span><span class="sxs-lookup"><span data-stu-id="498f0-131">catalog.wmdb.modified</span></span> | <span data-ttu-id="498f0-132">Arquivo de saída intermediário.</span><span class="sxs-lookup"><span data-stu-id="498f0-132">Intermediate output file.</span></span> <span data-ttu-id="498f0-133">Não usado pelo Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="498f0-133">Not used by Windows Media Player</span></span>                                                                                                                                       |



 

 

 





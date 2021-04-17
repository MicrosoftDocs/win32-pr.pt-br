---
title: Compilando um catálogo completo de arquivos TSV
description: Compilando um catálogo completo de arquivos TSV
ms.assetid: fba80b32-dc78-4c4a-a351-e8786f9a7131
keywords:
- Lojas online do Windows Media Player, compilando catálogos
- lojas online, compilando catálogos
- Digite 1 lojas online, compilando catálogos
- Armazenamentos online do Windows Media Player, arquivos TSV
- lojas online, arquivos TSV
- tipo 1 lojas online, arquivos TSV
- Armazenamentos online do Windows Media Player, catcomp.exe
- lojas online, catcomp.exe
- Digite 1 lojas online, catcomp.exe
- catcomp.exe
- Compilando catálogos
- arquivos de valores separados por tabulação (TSV)
- Arquivos TSV (valores separados por tabulação)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b68af019a5e2302f52f615d5a1dba2180e27cfe5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105770513"
---
# <a name="compiling-a-full-catalog-from-tsv-files"></a><span data-ttu-id="73f92-116">Compilando um catálogo completo de arquivos TSV</span><span class="sxs-lookup"><span data-stu-id="73f92-116">Compiling a Full Catalog from TSV Files</span></span>

<span data-ttu-id="73f92-117">Novos catálogos são criados a partir de um conjunto de arquivos TSV (valores separados por tabulação).</span><span class="sxs-lookup"><span data-stu-id="73f92-117">New catalogs are created from a set of tab-separated-value (TSV) files.</span></span> <span data-ttu-id="73f92-118">Os arquivos devem estar no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="73f92-118">The files must be in Unicode format.</span></span> <span data-ttu-id="73f92-119">Coloque os arquivos TSV necessários listados abaixo em uma pasta (o argumento de caminho de entrada para catcomp.exe) e chame catcomp.exe usando a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="73f92-119">Place the required TSV files listed below into a folder (the input path argument to catcomp.exe), and call catcomp.exe using the following syntax:</span></span>


```C++
catcomp <input path> [version number] [locale ID] [debug]
```



<span data-ttu-id="73f92-120">Se um número de versão não for fornecido, o número de versão será definido como 0.</span><span class="sxs-lookup"><span data-stu-id="73f92-120">If a version number is not provided, the version number will be set to 0.</span></span> <span data-ttu-id="73f92-121">Se nenhuma ID de localidade for fornecida, a localidade do sistema será usada.</span><span class="sxs-lookup"><span data-stu-id="73f92-121">If no locale ID is provided, the system locale is used.</span></span> <span data-ttu-id="73f92-122">Se apenas um argumento opcional numérico for fornecido, supõe-se que seja o número de versão.</span><span class="sxs-lookup"><span data-stu-id="73f92-122">If only one numeric optional argument is provided, it is assumed to be the version number.</span></span> <span data-ttu-id="73f92-123">Se Debug for especificado, a saída para a tela fornecerá informações de diagnóstico mais detalhadas.</span><span class="sxs-lookup"><span data-stu-id="73f92-123">If debug is specified, the output to the screen will provide more detailed diagnostic information.</span></span>

<span data-ttu-id="73f92-124">Por exemplo, o seguinte compilará um catálogo dos arquivos em C: \\ CatalogData \\ 210 e atribuirá ao catálogo um número de versão de 210:</span><span class="sxs-lookup"><span data-stu-id="73f92-124">For example, the following will compile a catalog from the files in C:\\CatalogData\\210 and give the catalog a version number of 210:</span></span>


```C++
catcomp C:\CatalogData\210 210
```



<span data-ttu-id="73f92-125">Para exibir mensagens de erro mais detalhadas, o argumento de depuração opcional pode ser adicionado, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="73f92-125">To display more detailed error messages, the optional debug argument can be added, as follows:</span></span>


```C++
catcomp C:\CatalogData\210 210 debug
```



## <a name="required-tsv-files"></a><span data-ttu-id="73f92-126">Arquivos TSV necessários</span><span class="sxs-lookup"><span data-stu-id="73f92-126">Required TSV Files</span></span>

<span data-ttu-id="73f92-127">Cada um dos arquivos a seguir deve estar presente, mas um arquivo vazio pode ser usado se não houver dados para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="73f92-127">Each of the following files must be present, but an empty file can be used if there is no data for a file.</span></span> <span data-ttu-id="73f92-128">Por exemplo, se o catálogo não contiver canais de rádio, radio.csv poderá ficar vazia.</span><span class="sxs-lookup"><span data-stu-id="73f92-128">For instance, if your catalog contains no radio channels, radio.csv can be empty.</span></span> <span data-ttu-id="73f92-129">Os arquivos devem ser nomeados exatamente como listados.</span><span class="sxs-lookup"><span data-stu-id="73f92-129">The files must be named exactly as listed.</span></span>

[<span data-ttu-id="73f92-130">track.csv</span><span class="sxs-lookup"><span data-stu-id="73f92-130">track.csv</span></span>](track-csv.md)

[<span data-ttu-id="73f92-131">album.csv</span><span class="sxs-lookup"><span data-stu-id="73f92-131">album.csv</span></span>](album-csv.md)

[<span data-ttu-id="73f92-132">artist.csv</span><span class="sxs-lookup"><span data-stu-id="73f92-132">artist.csv</span></span>](artist-csv.md)

[<span data-ttu-id="73f92-133">genre.csv</span><span class="sxs-lookup"><span data-stu-id="73f92-133">genre.csv</span></span>](genre-csv.md)

[<span data-ttu-id="73f92-134">subgenre.csv</span><span class="sxs-lookup"><span data-stu-id="73f92-134">subgenre.csv</span></span>](subgenre-csv.md)

[<span data-ttu-id="73f92-135">list.csv</span><span class="sxs-lookup"><span data-stu-id="73f92-135">list.csv</span></span>](list-csv.md)

[<span data-ttu-id="73f92-136">listitem.csv</span><span class="sxs-lookup"><span data-stu-id="73f92-136">listitem.csv</span></span>](listitem-csv.md)

[<span data-ttu-id="73f92-137">radio.csv</span><span class="sxs-lookup"><span data-stu-id="73f92-137">radio.csv</span></span>](radio-csv.md)

> [!Note]  
> <span data-ttu-id="73f92-138">Embora os nomes de arquivo devam ter extensões. csv, os arquivos não estão no formato CSV (valores separados por vírgula).</span><span class="sxs-lookup"><span data-stu-id="73f92-138">Although the file names must have .csv extensions, the files are not in Comma Separated Values (CSV) format.</span></span> <span data-ttu-id="73f92-139">Os arquivos devem estar no formato TSV (valores separados por tabulação).</span><span class="sxs-lookup"><span data-stu-id="73f92-139">The files must be in Tab Separated Values (TSV) format.</span></span>

 

<span data-ttu-id="73f92-140">Se a compilação for bem-sucedida, catcomp.exe criará três arquivos de saída.</span><span class="sxs-lookup"><span data-stu-id="73f92-140">If compilation is successful, catcomp.exe creates three output files.</span></span>



| <span data-ttu-id="73f92-141">Nome do arquivo</span><span class="sxs-lookup"><span data-stu-id="73f92-141">File name</span></span>                   | <span data-ttu-id="73f92-142">Descrição</span><span class="sxs-lookup"><span data-stu-id="73f92-142">Description</span></span>                                                                                                                                                                         |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73f92-143">Catalog. wmdb</span><span class="sxs-lookup"><span data-stu-id="73f92-143">catalog.wmdb</span></span>                | <span data-ttu-id="73f92-144">Catálogo compilado não compactado.</span><span class="sxs-lookup"><span data-stu-id="73f92-144">Uncompressed compiled catalog.</span></span>                                                                                                                                                      |
| <span data-ttu-id="73f92-145">Catalog. wmdb. LZ</span><span class="sxs-lookup"><span data-stu-id="73f92-145">catalog.wmdb.lz</span></span>             | <span data-ttu-id="73f92-146">Catálogo em formato compactado.</span><span class="sxs-lookup"><span data-stu-id="73f92-146">Catalog in compressed format.</span></span> <span data-ttu-id="73f92-147">Seu plug-in pode fornecer o local desse arquivo ao Windows Media Player em [IWMPContentPartner:: GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span><span class="sxs-lookup"><span data-stu-id="73f92-147">Your plug-in can give the location of this file to Windows Media Player in [IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span></span> |
| <span data-ttu-id="73f92-148">\_words.txt exclusivos compilados \_</span><span class="sxs-lookup"><span data-stu-id="73f92-148">compiled\_unique\_words.txt</span></span> | <span data-ttu-id="73f92-149">Um arquivo de saída intermediário.</span><span class="sxs-lookup"><span data-stu-id="73f92-149">An intermediate output file.</span></span> <span data-ttu-id="73f92-150">Não usado pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="73f92-150">Not used by Windows Media Player.</span></span>                                                                                                                      |



 

 

 





---
title: Aplicando uma atualização a um catálogo
description: Aplicando uma atualização a um catálogo
ms.assetid: 4aedb0d6-36c7-425c-b6d3-e16161cf6828
keywords:
- Lojas online do Windows Media Player, aplicando atualizações aos catálogos
- lojas online, aplicando atualizações aos catálogos
- Digite 1 lojas online, aplicando atualizações aos catálogos
- Armazenamentos online do Windows Media Player, atualizando catálogos
- lojas online, atualizando catálogos
- Digite 1 lojas online, atualizando catálogos
- Armazenamentos online do Windows Media Player, atualizações de catálogo
- lojas online, atualizações de catálogo
- Digite 1 lojas online, atualizações de catálogo
- atualizações do catálogo
- Atualizando catálogos
- aplicando atualizações aos catálogos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d468edb7d09b8804fa924f7c31fc1be45d27c8fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105761490"
---
# <a name="applying-an-update-to-a-catalog"></a><span data-ttu-id="f4cec-115">Aplicando uma atualização a um catálogo</span><span class="sxs-lookup"><span data-stu-id="f4cec-115">Applying an Update To a Catalog</span></span>

> [!Note]  
> <span data-ttu-id="f4cec-116">Isso normalmente não é feito, exceto para fins de diagnóstico, por exemplo, para ajudar a verificar se um arquivo de diferença é válido.</span><span class="sxs-lookup"><span data-stu-id="f4cec-116">This is not normally done except for diagnostic purposes—for instance, to help verify that a difference file is valid.</span></span> <span data-ttu-id="f4cec-117">O catálogo gerado dessa maneira não está em formato compactado e não deve ser passado para o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="f4cec-117">The catalog generated in this way is not in compressed form and should not be passed to Windows Media Player.</span></span>

 

<span data-ttu-id="f4cec-118">Um novo arquivo de catálogo pode ser criado usando a sintaxe abaixo, em que *inputcatalog* é o local do catálogo original e *inputdiff* é o local do arquivo de diferenças a ser aplicado.</span><span class="sxs-lookup"><span data-stu-id="f4cec-118">A new catalog file can be created by using the syntax below, where *inputcatalog* is the location of the original catalog, and *inputdiff* is the location of the difference file to apply.</span></span> <span data-ttu-id="f4cec-119">Os arquivos de catálogo devem estar em formato descompactado.</span><span class="sxs-lookup"><span data-stu-id="f4cec-119">The catalog files must be in uncompressed form.</span></span>


```C++
catcomp applydiff <inputcatalog> <inputdiff>
```



<span data-ttu-id="f4cec-120">Por exemplo, o seguinte cria um novo catálogo de C: \\ Catalog210 \\ Catalog. wmdb e C: \\ Catalog210 \\ Catalog. diff.</span><span class="sxs-lookup"><span data-stu-id="f4cec-120">For example, the following creates a new catalog from C:\\Catalog210\\catalog.wmdb and C:\\Catalog210\\catalog.diff.</span></span>


```C++
catcomp applydiff C:\Catalog210\catalog.wmdb C:\Catalog210\catalog.diff
```



<span data-ttu-id="f4cec-121">Se a compilação for bem-sucedida, catcomp.exe criará os arquivos de saída a seguir.</span><span class="sxs-lookup"><span data-stu-id="f4cec-121">If compilation is successful, catcomp.exe creates the follow output files.</span></span>



| <span data-ttu-id="f4cec-122">Nome do arquivo</span><span class="sxs-lookup"><span data-stu-id="f4cec-122">File name</span></span>        | <span data-ttu-id="f4cec-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="f4cec-123">Description</span></span>       |
|------------------|-------------------|
| <span data-ttu-id="f4cec-124">Catalog. wmdb. New</span><span class="sxs-lookup"><span data-stu-id="f4cec-124">catalog.wmdb.new</span></span> | <span data-ttu-id="f4cec-125">Novo arquivo de catálogo.</span><span class="sxs-lookup"><span data-stu-id="f4cec-125">New catalog file.</span></span> |



 

 

 





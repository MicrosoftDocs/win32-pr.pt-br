---
description: Módulos de mesclagem de vários idiomas, transformações de linguagem e arquivos de gabinete devem ser criados de forma que a ordem dos arquivos corresponda à ordem especificada na tabela de arquivos.
ms.assetid: c6ddf5fc-a7c5-49c1-899b-ff9fdff9c028
title: Ordenando a sequência de arquivos no CAB de um módulo de mesclagem de vários idiomas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01bdd00d8b09c0605b7ddcf656d87d41e3f53776
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172017"
---
# <a name="ordering-the-file-sequence-in-the-cab-of-a-multiple-language-merge-module"></a><span data-ttu-id="78eda-103">Ordenando a sequência de arquivos no CAB de um módulo de mesclagem de vários idiomas</span><span class="sxs-lookup"><span data-stu-id="78eda-103">Ordering the File Sequence in the CAB of a Multiple Language Merge Module</span></span>

<span data-ttu-id="78eda-104">Os módulos de mesclagem de vários idiomas, as transformações de linguagem e os arquivos de gabinete devem ser criados de forma que a ordem dos arquivos no. cab corresponda à ordem de instalação dos arquivos especificados na [tabela de arquivos](file-table.md), mesmo após a aplicação da transformação de idioma.</span><span class="sxs-lookup"><span data-stu-id="78eda-104">Multiple-language merge modules, language transforms, and cabinet files must be authored such that the order of the files in the .cab matches the installation order of files specified in the [File Table](file-table.md), even after the application of the language transform.</span></span> <span data-ttu-id="78eda-105">Se a ordem no módulo e no. cab não corresponder, o módulo de mesclagem não poderá ser usado.</span><span class="sxs-lookup"><span data-stu-id="78eda-105">If the order in the module and in the .cab do not match, the merge module cannot be used.</span></span>

<span data-ttu-id="78eda-106">Atribua a cada arquivo no módulo, um número de sequência exclusivo que seja independente de seu idioma e sempre use esse número de sequência para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="78eda-106">Assign to each file in the module, a unique sequence number that is independent of its language, and then always use that sequence number for the file.</span></span> <span data-ttu-id="78eda-107">Use a mesma sequência ao criar o arquivo de gabinete e criar uma transformação de idioma.</span><span class="sxs-lookup"><span data-stu-id="78eda-107">Use the same sequence when building the cabinet file and authoring a language transform.</span></span>

<span data-ttu-id="78eda-108">Como o instalador instala apenas os arquivos listados na [tabela de arquivos](file-table.md), o uso de uma sequência de arquivos global no gabinete, na [tabela de arquivos](file-table.md)e na transformação de linguagem permite que a ferramenta de mesclagem ignore todos os arquivos extras armazenados no gabinete que não estejam listados na tabela de [arquivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="78eda-108">Because the Installer only installs the files listed in the [File Table](file-table.md), the use of a global file sequence in the cabinet, [File Table](file-table.md), and language transform enables the merge tool to skip any extra files stored in the cabinet that are not listed in the [File Table](file-table.md).</span></span> <span data-ttu-id="78eda-109">Outros arquivos podem existir no gabinete, mas eles não devem estar listados na tabela de [arquivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="78eda-109">Other files may exist in the cabinet, but they must not be listed in the [File Table](file-table.md).</span></span> <span data-ttu-id="78eda-110">Por exemplo, um módulo que instala Code.dll, inglês. dat, alemão. dat e francês. dat pode usar a seguinte ordem de sequência de arquivos global.</span><span class="sxs-lookup"><span data-stu-id="78eda-110">For example, a module installing Code.dll, English.dat, German.dat, and French.dat can use the following global file sequence order.</span></span>



| <span data-ttu-id="78eda-111">Arquivo</span><span class="sxs-lookup"><span data-stu-id="78eda-111">File</span></span>        | <span data-ttu-id="78eda-112">Sequência</span><span class="sxs-lookup"><span data-stu-id="78eda-112">Sequence</span></span> |
|-------------|----------|
| <span data-ttu-id="78eda-113">Code.Dll</span><span class="sxs-lookup"><span data-stu-id="78eda-113">Code.Dll</span></span>    | <span data-ttu-id="78eda-114">1</span><span class="sxs-lookup"><span data-stu-id="78eda-114">1</span></span>        |
| <span data-ttu-id="78eda-115">Inglês. dat</span><span class="sxs-lookup"><span data-stu-id="78eda-115">English.Dat</span></span> | <span data-ttu-id="78eda-116">2</span><span class="sxs-lookup"><span data-stu-id="78eda-116">2</span></span>        |
| <span data-ttu-id="78eda-117">Alemão. dat</span><span class="sxs-lookup"><span data-stu-id="78eda-117">German.Dat</span></span>  | <span data-ttu-id="78eda-118">3</span><span class="sxs-lookup"><span data-stu-id="78eda-118">3</span></span>        |
| <span data-ttu-id="78eda-119">Francês. dat</span><span class="sxs-lookup"><span data-stu-id="78eda-119">French.Dat</span></span>  | <span data-ttu-id="78eda-120">4</span><span class="sxs-lookup"><span data-stu-id="78eda-120">4</span></span>        |



 

<span data-ttu-id="78eda-121">As transformações de linguagem podem ser criadas para modificar a [tabela de arquivos](file-table.md) do módulo para inglês, alemão ou francês.</span><span class="sxs-lookup"><span data-stu-id="78eda-121">Language transforms can then be authored to modify the [File Table](file-table.md) of the module for English, German, or French.</span></span>

<span data-ttu-id="78eda-122">[Tabela de arquivos](file-table.md) (parcial para inglês)</span><span class="sxs-lookup"><span data-stu-id="78eda-122">[File Table](file-table.md) (partial for English)</span></span>



| <span data-ttu-id="78eda-123">Arquivo</span><span class="sxs-lookup"><span data-stu-id="78eda-123">File</span></span>        | <span data-ttu-id="78eda-124">Sequência</span><span class="sxs-lookup"><span data-stu-id="78eda-124">Sequence</span></span> |
|-------------|----------|
| <span data-ttu-id="78eda-125">Code.Dll</span><span class="sxs-lookup"><span data-stu-id="78eda-125">Code.Dll</span></span>    | <span data-ttu-id="78eda-126">1</span><span class="sxs-lookup"><span data-stu-id="78eda-126">1</span></span>        |
| <span data-ttu-id="78eda-127">Inglês. dat</span><span class="sxs-lookup"><span data-stu-id="78eda-127">English.Dat</span></span> | <span data-ttu-id="78eda-128">2</span><span class="sxs-lookup"><span data-stu-id="78eda-128">2</span></span>        |



 

<span data-ttu-id="78eda-129">[Tabela de arquivos](file-table.md) (parcial para alemão)</span><span class="sxs-lookup"><span data-stu-id="78eda-129">[File Table](file-table.md) (partial for German)</span></span>



| <span data-ttu-id="78eda-130">Arquivo</span><span class="sxs-lookup"><span data-stu-id="78eda-130">File</span></span>       | <span data-ttu-id="78eda-131">Sequência</span><span class="sxs-lookup"><span data-stu-id="78eda-131">Sequence</span></span> |
|------------|----------|
| <span data-ttu-id="78eda-132">Code.Dll</span><span class="sxs-lookup"><span data-stu-id="78eda-132">Code.Dll</span></span>   | <span data-ttu-id="78eda-133">1</span><span class="sxs-lookup"><span data-stu-id="78eda-133">1</span></span>        |
| <span data-ttu-id="78eda-134">Alemão. dat</span><span class="sxs-lookup"><span data-stu-id="78eda-134">German.Dat</span></span> | <span data-ttu-id="78eda-135">3</span><span class="sxs-lookup"><span data-stu-id="78eda-135">3</span></span>        |



 

<span data-ttu-id="78eda-136">[Tabela de arquivos](file-table.md) (parcial para francês)</span><span class="sxs-lookup"><span data-stu-id="78eda-136">[File Table](file-table.md) (partial for French)</span></span>



| <span data-ttu-id="78eda-137">Arquivo</span><span class="sxs-lookup"><span data-stu-id="78eda-137">File</span></span>       | <span data-ttu-id="78eda-138">Sequência</span><span class="sxs-lookup"><span data-stu-id="78eda-138">Sequence</span></span> |
|------------|----------|
| <span data-ttu-id="78eda-139">Code.Dll</span><span class="sxs-lookup"><span data-stu-id="78eda-139">Code.Dll</span></span>   | <span data-ttu-id="78eda-140">1</span><span class="sxs-lookup"><span data-stu-id="78eda-140">1</span></span>        |
| <span data-ttu-id="78eda-141">Francês. dat</span><span class="sxs-lookup"><span data-stu-id="78eda-141">French.Dat</span></span> | <span data-ttu-id="78eda-142">4</span><span class="sxs-lookup"><span data-stu-id="78eda-142">4</span></span>        |



 

<span data-ttu-id="78eda-143">Para obter mais informações, consulte [criando uma transformação de idioma para um módulo de mesclagem de vários idiomas](authoring-a-language-transform-for-a-multiple-language-merge-module.md) e [criando tabelas de arquivos de módulo de mesclagem](authoring-merge-module-file-tables.md).</span><span class="sxs-lookup"><span data-stu-id="78eda-143">For more information, see [Authoring a Language Transform for a Multiple Language Merge Module](authoring-a-language-transform-for-a-multiple-language-merge-module.md) and [Authoring Merge Module File Tables](authoring-merge-module-file-tables.md).</span></span>

 

 




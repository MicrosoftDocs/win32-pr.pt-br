---
description: ICE60 valida a tabela de arquivos de um banco de dados Windows Installer.
ms.assetid: 95d9b8b4-0b65-451a-8629-f0b276d6e35d
title: ICE60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e26c6f296fd514f582a699a5f839a7e145169e3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756728"
---
# <a name="ice60"></a><span data-ttu-id="1e1c2-103">ICE60</span><span class="sxs-lookup"><span data-stu-id="1e1c2-103">ICE60</span></span>

<span data-ttu-id="1e1c2-104">ICE60 verifica se os arquivos na [tabela de arquivos](file-table.md) atendem à seguinte condição:</span><span class="sxs-lookup"><span data-stu-id="1e1c2-104">ICE60 checks that files in the [File table](file-table.md) meet the following condition:</span></span>

-   <span data-ttu-id="1e1c2-105">Se o arquivo não for uma fonte e tiver uma versão, ele deverá ter um idioma.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-105">If the file is not a font and has a version, then it must have a language.</span></span>
-   <span data-ttu-id="1e1c2-106">ICE60 verifica se nenhum arquivo com versão está listado na [tabela MsiFileHash](msifilehash-table.md).</span><span class="sxs-lookup"><span data-stu-id="1e1c2-106">ICE60 checks that no versioned files are listed in the [MsiFileHash table](msifilehash-table.md).</span></span>

<span data-ttu-id="1e1c2-107">A falha em corrigir um aviso relatado por ICE60 geralmente leva a um arquivo desinstalado desnecessariamente quando um reparo do produto é feito.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-107">Failure to fix a warning reported by ICE60 generally leads to a file being needlessly reinstalled when a product repair is done.</span></span> <span data-ttu-id="1e1c2-108">Isso acontece porque o arquivo a ser instalado no reparo e o arquivo existente no disco têm a mesma versão (eles são o mesmo arquivo), mas idiomas diferentes.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-108">This happens because the file to be installed in the repair and the existing file on disk have the same version (they are the same file) but different languages.</span></span> <span data-ttu-id="1e1c2-109">A tabela de arquivos lista o idioma como nulo, mas o próprio arquivo tem um valor de idioma no recurso.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-109">The file table lists the language as null, but the file itself has a language value in the resource.</span></span> <span data-ttu-id="1e1c2-110">Com base nas [regras de controle de versão de arquivo](file-versioning-rules.md), o instalador favorece o arquivo a ser instalado e, portanto, é recopiado desnecessariamente.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-110">Based on the [file versioning rules](file-versioning-rules.md), the installer favors the file to be installed, so it is recopied needlessly.</span></span>

## <a name="result"></a><span data-ttu-id="1e1c2-111">Resultado</span><span class="sxs-lookup"><span data-stu-id="1e1c2-111">Result</span></span>

<span data-ttu-id="1e1c2-112">ICE60 lançará um aviso ou um erro se um arquivo na [tabela de arquivos](file-table.md) que não é uma fonte e tiver uma versão não tiver uma linguagem.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-112">ICE60 posts a warning or an error if a file in the [File table](file-table.md) that is not a font and has a version, does not have a language.</span></span>

<span data-ttu-id="1e1c2-113">ICE60 lançará o erro a seguir se um arquivo listado na tabela MsiFileHash tiver controle de versão.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-113">ICE60 posts the following error if a file listed in the MsiFileHash table is versioned.</span></span>

``` syntax
ERROR: "The file [1] is Versioned. It cannot be hashed"
```

## <a name="example"></a><span data-ttu-id="1e1c2-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="1e1c2-114">Example</span></span>

<span data-ttu-id="1e1c2-115">ICE60 relata o seguinte erro e aviso para o exemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-115">ICE60 reports the following error and warning for the example shown.</span></span> <span data-ttu-id="1e1c2-116">(O arquivo B é uma fonte; os outros arquivos não são.)</span><span class="sxs-lookup"><span data-stu-id="1e1c2-116">(File B is a font; the other files are not.)</span></span>

``` syntax
WARNING: The file FileE is not a Font, and its version is not a companion file reference. It should have a language specified in the Language column.
```

<span data-ttu-id="1e1c2-117">O arquivoA tem uma versão e um idioma; Portanto, nenhum aviso ou erro é gerado.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-117">FileA has both a version and a language; therefore no warning or error is generated.</span></span>

<span data-ttu-id="1e1c2-118">FileB tem uma versão, mas não idioma.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-118">FileB has a version but no language.</span></span> <span data-ttu-id="1e1c2-119">No entanto, nenhum aviso ou erro é gerado porque é uma fonte.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-119">No warning or error is generated, however, because it is a font.</span></span>

<span data-ttu-id="1e1c2-120">FileC é uma referência complementar, portanto, não precisa ter um idioma.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-120">FileC is a companion reference, so it does not have to have a language.</span></span> <span data-ttu-id="1e1c2-121">Nenhum aviso ou erro é gerado.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-121">No warning or error is generated.</span></span>

<span data-ttu-id="1e1c2-122">O Arquivado não tem nenhuma versão, portanto, não precisa ter um idioma.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-122">FileD has no version, so it does not need to have a language.</span></span> <span data-ttu-id="1e1c2-123">Nenhum aviso ou erro é gerado.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-123">No warning or error is generated.</span></span>

<span data-ttu-id="1e1c2-124">O arquivo tem uma versão, mas não idioma.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-124">FileE has a version but no language.</span></span> <span data-ttu-id="1e1c2-125">Portanto, um aviso é gerado.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-125">Therefore a warning is generated.</span></span>

<span data-ttu-id="1e1c2-126">Para corrigir esse aviso, adicione um idioma para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-126">To fix this warning, add a language to FileE.</span></span>

<span data-ttu-id="1e1c2-127">Os arquivos devem ter valores de idioma armazenados no recurso de versão sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-127">Files should have language values stored in the version resource whenever possible.</span></span> <span data-ttu-id="1e1c2-128">Se um arquivo for de idioma neutro, use o [LangID](column-data-types.md) 0.</span><span class="sxs-lookup"><span data-stu-id="1e1c2-128">If a file is language neutral, use the [LANGID](column-data-types.md) 0.</span></span>

<span data-ttu-id="1e1c2-129">A [tabela de arquivos](file-table.md) (FileB é uma fonte; os outros arquivos não são.)</span><span class="sxs-lookup"><span data-stu-id="1e1c2-129">[File Table](file-table.md) (FileB is a font; the other files are not.)</span></span>



| <span data-ttu-id="1e1c2-130">Arquivo</span><span class="sxs-lookup"><span data-stu-id="1e1c2-130">File</span></span>  | <span data-ttu-id="1e1c2-131">Versão</span><span class="sxs-lookup"><span data-stu-id="1e1c2-131">Version</span></span> | <span data-ttu-id="1e1c2-132">Idioma</span><span class="sxs-lookup"><span data-stu-id="1e1c2-132">Language</span></span> |
|-------|---------|----------|
| <span data-ttu-id="1e1c2-133">FileA</span><span class="sxs-lookup"><span data-stu-id="1e1c2-133">FileA</span></span> | <span data-ttu-id="1e1c2-134">1.0</span><span class="sxs-lookup"><span data-stu-id="1e1c2-134">1.0</span></span>     | <span data-ttu-id="1e1c2-135">1046</span><span class="sxs-lookup"><span data-stu-id="1e1c2-135">1033</span></span>     |
| <span data-ttu-id="1e1c2-136">FileB</span><span class="sxs-lookup"><span data-stu-id="1e1c2-136">FileB</span></span> | <span data-ttu-id="1e1c2-137">1.0</span><span class="sxs-lookup"><span data-stu-id="1e1c2-137">1.0</span></span>     |          |
| <span data-ttu-id="1e1c2-138">FileC</span><span class="sxs-lookup"><span data-stu-id="1e1c2-138">FileC</span></span> | <span data-ttu-id="1e1c2-139">FileA</span><span class="sxs-lookup"><span data-stu-id="1e1c2-139">FileA</span></span>   |          |
| <span data-ttu-id="1e1c2-140">Arquiva</span><span class="sxs-lookup"><span data-stu-id="1e1c2-140">FileD</span></span> |         |          |
| <span data-ttu-id="1e1c2-141">Arquivo</span><span class="sxs-lookup"><span data-stu-id="1e1c2-141">FileE</span></span> | <span data-ttu-id="1e1c2-142">1.0</span><span class="sxs-lookup"><span data-stu-id="1e1c2-142">1.0</span></span>     |          |



 

[<span data-ttu-id="1e1c2-143">Tabela de fontes</span><span class="sxs-lookup"><span data-stu-id="1e1c2-143">Font Table</span></span>](font-table.md)



| <span data-ttu-id="1e1c2-144">Arquivo</span><span class="sxs-lookup"><span data-stu-id="1e1c2-144">File</span></span>  | <span data-ttu-id="1e1c2-145">FontTitle</span><span class="sxs-lookup"><span data-stu-id="1e1c2-145">FontTitle</span></span>  |
|-------|------------|
| <span data-ttu-id="1e1c2-146">FileB</span><span class="sxs-lookup"><span data-stu-id="1e1c2-146">FileB</span></span> | <span data-ttu-id="1e1c2-147">Título da fonte</span><span class="sxs-lookup"><span data-stu-id="1e1c2-147">Font Title</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="1e1c2-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1e1c2-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e1c2-149">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="1e1c2-149">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




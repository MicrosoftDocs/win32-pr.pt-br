---
description: O ICE35 valida que os componentes que contêm arquivos compactados armazenados em um arquivo de gabinete não estão definidos para execução da origem. Com o Windows Installer 2,0 ou posterior, essa restrição foi removida.
ms.assetid: b4df27e2-9790-4b18-a173-25fa8b0ecd4d
title: ICE35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea6a98079d3c57e0c796332cf0cd5f11045a07b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922019"
---
# <a name="ice35"></a><span data-ttu-id="48b09-104">ICE35</span><span class="sxs-lookup"><span data-stu-id="48b09-104">ICE35</span></span>

<span data-ttu-id="48b09-105">O ICE35 valida que os componentes que contêm arquivos compactados armazenados em um [arquivo de gabinete](cabinet-files.md) não estão definidos para execução da origem.</span><span class="sxs-lookup"><span data-stu-id="48b09-105">ICE35 validates that components containing compressed files stored in a [cabinet file](cabinet-files.md) are not set to run from source.</span></span> <span data-ttu-id="48b09-106">Com o Windows Installer 2,0 ou posterior, essa restrição foi removida.</span><span class="sxs-lookup"><span data-stu-id="48b09-106">With Windows Installer 2.0 or later, this restriction has been removed.</span></span>

<span data-ttu-id="48b09-107">ICE35 consulta a coluna de gabinete da [tabela de mídia](media-table.md) para determinar quais arquivos são compactados e armazenados em um arquivo de gabinete.</span><span class="sxs-lookup"><span data-stu-id="48b09-107">ICE35 queries the Cabinet column of the [Media table](media-table.md) to determine which files are compressed and stored in a cabinet file.</span></span> <span data-ttu-id="48b09-108">Ele consulta a [tabela de arquivos](file-table.md) para determinar quais componentes contêm esses arquivos.</span><span class="sxs-lookup"><span data-stu-id="48b09-108">It queries the [File table](file-table.md) to determine which components contain these files.</span></span> <span data-ttu-id="48b09-109">Por fim, ele verifica a [tabela de componentes](component-table.md) para determinar se os bits de execução da origem estão definidos na coluna atributos.</span><span class="sxs-lookup"><span data-stu-id="48b09-109">Finally, it checks the [Component table](component-table.md) to determine whether the run-from-source bits are set in the Attributes column.</span></span>

## <a name="result"></a><span data-ttu-id="48b09-110">Resultado</span><span class="sxs-lookup"><span data-stu-id="48b09-110">Result</span></span>

<span data-ttu-id="48b09-111">O ICE35 posta uma mensagem de erro se houver um arquivo compactado armazenado em um arquivo de gabinete pertencente a um componente com o conjunto de bits msidbComponentAttributesSourceOnly na coluna atributos da [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="48b09-111">ICE35 posts an error message if there is a compressed file stored in a cabinet file belonging to a component with the msidbComponentAttributesSourceOnly bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="48b09-112">Com o Windows Installer 2,0 ou posterior, isso é alterado de um erro para uma mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="48b09-112">With Windows Installer 2.0 or later, this is changed from an error to a warning message.</span></span> <span data-ttu-id="48b09-113">Um pacote que dá suporte apenas a Windows Installer 2,0 e posteriores tem a \_ Propriedade PID PageCount do fluxo de informações de resumo definida como um valor de pelo menos 200.</span><span class="sxs-lookup"><span data-stu-id="48b09-113">A package that supports only Windows Installer 2.0 and later has the PID\_PAGECOUNT property of the Summary Information Stream set to a value of at least 200.</span></span>

<span data-ttu-id="48b09-114">O ICE35 posta a mensagem de aviso se houver um arquivo compactado armazenado em um arquivo de gabinete pertencente a um componente com o conjunto de bits msidbComponentAttributesOptional na coluna atributos da [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="48b09-114">ICE35 posts warning message if there is a compressed file stored in a cabinet file belonging to a component with the msidbComponentAttributesOptional bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="48b09-115">Esta mensagem de aviso foi removida com Windows Installer 2,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="48b09-115">This warning message has been removed with Windows Installer 2.0 and later.</span></span>

<span data-ttu-id="48b09-116">Se vários arquivos em um componente estiverem em um arquivo de gabinete, o ICE35 relatará erros para cada arquivo que tem a execução do conjunto de bits de origem.</span><span class="sxs-lookup"><span data-stu-id="48b09-116">If multiple files in a component are in a cabinet file, ICE35 reports errors for each file that has the run from source bit set.</span></span>

## <a name="example"></a><span data-ttu-id="48b09-117">Exemplo</span><span class="sxs-lookup"><span data-stu-id="48b09-117">Example</span></span>

<span data-ttu-id="48b09-118">O ICE35 relata os erros e avisos a seguir para o exemplo mostrado usando uma versão anterior à Windows Installer versão 2,0.</span><span class="sxs-lookup"><span data-stu-id="48b09-118">ICE35 reports the following errors and warnings for the example shown using a version earlier than Windows Installer version 2.0.</span></span>



| <span data-ttu-id="48b09-119">Erro de ICE35</span><span class="sxs-lookup"><span data-stu-id="48b09-119">ICE35 Error</span></span>                                                                                                | <span data-ttu-id="48b09-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="48b09-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48b09-121">ERRO: o componente Component3 não pode ser executado somente da origem, porque seu arquivo de membro ' arquivo3 ' está compactado.</span><span class="sxs-lookup"><span data-stu-id="48b09-121">ERROR: Component Component3 cannot be Run From Source only, because its member file 'File3' is compressed.</span></span> | <span data-ttu-id="48b09-122">Há um arquivo compactado armazenado em um arquivo de gabinete e esse arquivo pertence a um componente com o conjunto de bits SourceOnly na coluna atributos da [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="48b09-122">There is a compressed file stored in a cabinet file and this file belongs to a component with the SourceOnly bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="48b09-123">Para corrigir esse erro, altere os 2 bits inferiores do valor de atributos Component2's para "00", ou seja, somente local, ou remova Arquivo4 do arquivo CAB.</span><span class="sxs-lookup"><span data-stu-id="48b09-123">To fix this error change the lower 2 bits of Component2's Attributes value to "00", meaning Local only, or remove File4 from the CAB file.</span></span><br/>                                                                                                                                                                         |
| <span data-ttu-id="48b09-124">ERRO: o componente Component3 não pode ser executado somente da origem, porque seu arquivo de membro ' arquivo3 ' está compactado.</span><span class="sxs-lookup"><span data-stu-id="48b09-124">ERROR: Component Component3 cannot be Run From Source only, because its member file 'File3' is compressed.</span></span> | <span data-ttu-id="48b09-125">Há um arquivo compactado armazenado em um arquivo de gabinete e esse arquivo pertence a um componente com o conjunto de bits SourceOnly na coluna atributos da [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="48b09-125">There is a compressed file stored in a cabinet file and this file belongs to a component with the SourceOnly bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="48b09-126">Como os arquivos em um componente não precisam ter origem na mesma mídia, o ICE35 relata erros para cada arquivo no componente que está em um gabinete.</span><span class="sxs-lookup"><span data-stu-id="48b09-126">Because the files in a component do not all have to originate from the same media, ICE35 reports errors for each file in the component that is in a cabinet.</span></span><br/> <span data-ttu-id="48b09-127">Para corrigir esse erro, altere os 2 bits inferiores do valor de atributos Component2's para "00", ou seja, somente local, ou remova Arquivo4 do arquivo CAB.</span><span class="sxs-lookup"><span data-stu-id="48b09-127">To fix this error change the lower 2 bits of Component2's Attributes value to "00", meaning Local only, or remove File4 from the CAB file.</span></span><br/> |



 

<span data-ttu-id="48b09-128">[Tabela de mídia](media-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="48b09-128">[Media Table](media-table.md) (partial)</span></span>



| <span data-ttu-id="48b09-129">DiskID</span><span class="sxs-lookup"><span data-stu-id="48b09-129">DiskID</span></span> | <span data-ttu-id="48b09-130">LastSequence</span><span class="sxs-lookup"><span data-stu-id="48b09-130">LastSequence</span></span> | <span data-ttu-id="48b09-131">Gabinete</span><span class="sxs-lookup"><span data-stu-id="48b09-131">Cabinet</span></span>   |
|--------|--------------|-----------|
| <span data-ttu-id="48b09-132">1</span><span class="sxs-lookup"><span data-stu-id="48b09-132">1</span></span>      | <span data-ttu-id="48b09-133">2</span><span class="sxs-lookup"><span data-stu-id="48b09-133">2</span></span>            |           |
| <span data-ttu-id="48b09-134">2</span><span class="sxs-lookup"><span data-stu-id="48b09-134">2</span></span>      | <span data-ttu-id="48b09-135">4</span><span class="sxs-lookup"><span data-stu-id="48b09-135">4</span></span>            | <span data-ttu-id="48b09-136">One.cab</span><span class="sxs-lookup"><span data-stu-id="48b09-136">One.cab</span></span>   |
| <span data-ttu-id="48b09-137">3</span><span class="sxs-lookup"><span data-stu-id="48b09-137">3</span></span>      | <span data-ttu-id="48b09-138">5</span><span class="sxs-lookup"><span data-stu-id="48b09-138">5</span></span>            | <span data-ttu-id="48b09-139">\#Two.cab</span><span class="sxs-lookup"><span data-stu-id="48b09-139">\#Two.cab</span></span> |



 

<span data-ttu-id="48b09-140">[Tabela de arquivos](file-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="48b09-140">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="48b09-141">Arquivo</span><span class="sxs-lookup"><span data-stu-id="48b09-141">File</span></span>  | <span data-ttu-id="48b09-142">Componente\_</span><span class="sxs-lookup"><span data-stu-id="48b09-142">Component\_</span></span> | <span data-ttu-id="48b09-143">Sequência</span><span class="sxs-lookup"><span data-stu-id="48b09-143">Sequence</span></span> |
|-------|-------------|----------|
| <span data-ttu-id="48b09-144">Arquivo1</span><span class="sxs-lookup"><span data-stu-id="48b09-144">File1</span></span> | <span data-ttu-id="48b09-145">Component1</span><span class="sxs-lookup"><span data-stu-id="48b09-145">Component1</span></span>  | <span data-ttu-id="48b09-146">1</span><span class="sxs-lookup"><span data-stu-id="48b09-146">1</span></span>        |
| <span data-ttu-id="48b09-147">Arquivo2</span><span class="sxs-lookup"><span data-stu-id="48b09-147">File2</span></span> | <span data-ttu-id="48b09-148">Component2</span><span class="sxs-lookup"><span data-stu-id="48b09-148">Component2</span></span>  | <span data-ttu-id="48b09-149">2</span><span class="sxs-lookup"><span data-stu-id="48b09-149">2</span></span>        |
| <span data-ttu-id="48b09-150">Arquivo3</span><span class="sxs-lookup"><span data-stu-id="48b09-150">File3</span></span> | <span data-ttu-id="48b09-151">Component2</span><span class="sxs-lookup"><span data-stu-id="48b09-151">Component2</span></span>  | <span data-ttu-id="48b09-152">3</span><span class="sxs-lookup"><span data-stu-id="48b09-152">3</span></span>        |
| <span data-ttu-id="48b09-153">Arquivo4</span><span class="sxs-lookup"><span data-stu-id="48b09-153">File4</span></span> | <span data-ttu-id="48b09-154">Component3</span><span class="sxs-lookup"><span data-stu-id="48b09-154">Component3</span></span>  | <span data-ttu-id="48b09-155">4</span><span class="sxs-lookup"><span data-stu-id="48b09-155">4</span></span>        |
| <span data-ttu-id="48b09-156">Arquivo5</span><span class="sxs-lookup"><span data-stu-id="48b09-156">File5</span></span> | <span data-ttu-id="48b09-157">Component3</span><span class="sxs-lookup"><span data-stu-id="48b09-157">Component3</span></span>  | <span data-ttu-id="48b09-158">5</span><span class="sxs-lookup"><span data-stu-id="48b09-158">5</span></span>        |



 

<span data-ttu-id="48b09-159">[Tabela de componentes](component-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="48b09-159">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="48b09-160">Componente</span><span class="sxs-lookup"><span data-stu-id="48b09-160">Component</span></span>  | <span data-ttu-id="48b09-161">Atributos</span><span class="sxs-lookup"><span data-stu-id="48b09-161">Attributes</span></span> |
|------------|------------|
| <span data-ttu-id="48b09-162">Component1</span><span class="sxs-lookup"><span data-stu-id="48b09-162">Component1</span></span> | <span data-ttu-id="48b09-163">0</span><span class="sxs-lookup"><span data-stu-id="48b09-163">0</span></span>          |
| <span data-ttu-id="48b09-164">Component2</span><span class="sxs-lookup"><span data-stu-id="48b09-164">Component2</span></span> | <span data-ttu-id="48b09-165">2</span><span class="sxs-lookup"><span data-stu-id="48b09-165">2</span></span>          |
| <span data-ttu-id="48b09-166">Component3</span><span class="sxs-lookup"><span data-stu-id="48b09-166">Component3</span></span> | <span data-ttu-id="48b09-167">1</span><span class="sxs-lookup"><span data-stu-id="48b09-167">1</span></span>          |



 

<span data-ttu-id="48b09-168">[Tabela de atalho](shortcut-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="48b09-168">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="48b09-169">Atalho</span><span class="sxs-lookup"><span data-stu-id="48b09-169">Shortcut</span></span>  | <span data-ttu-id="48b09-170">ícone\_</span><span class="sxs-lookup"><span data-stu-id="48b09-170">Icon\_</span></span> |
|-----------|--------|
| <span data-ttu-id="48b09-171">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="48b09-171">Shortcut1</span></span> | <span data-ttu-id="48b09-172">Icon2</span><span class="sxs-lookup"><span data-stu-id="48b09-172">Icon2</span></span>  |



 

<span data-ttu-id="48b09-173">Observe que os arquivos também podem ser marcados como compactados usando a propriedade de [**Resumo contagem de palavras**](word-count-summary.md) do [fluxo de informações de resumo](summary-information-stream.md).</span><span class="sxs-lookup"><span data-stu-id="48b09-173">Note that files can also be marked as compressed using the [**Word Count Summary**](word-count-summary.md) Property of the [Summary Information stream](summary-information-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="48b09-174">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="48b09-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48b09-175">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="48b09-175">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 





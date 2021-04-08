---
description: A tabela de diretórios especifica o layout do diretório para o produto. Cada linha da tabela indica um diretório na origem e no destino.
ms.assetid: eaca30cb-fec1-49ca-8b23-5e54c583e3e2
title: Tabela de diretórios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 273445aef67e3f166255321d0ac0ccf1aee37515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922039"
---
# <a name="directory-table"></a><span data-ttu-id="61fa9-104">Tabela de diretórios</span><span class="sxs-lookup"><span data-stu-id="61fa9-104">Directory Table</span></span>

<span data-ttu-id="61fa9-105">A tabela de diretórios especifica o layout do diretório para o produto.</span><span class="sxs-lookup"><span data-stu-id="61fa9-105">The Directory table specifies the directory layout for the product.</span></span> <span data-ttu-id="61fa9-106">Cada linha da tabela indica um diretório na origem e no destino.</span><span class="sxs-lookup"><span data-stu-id="61fa9-106">Each row of the table indicates a directory both at the source and the target.</span></span>

<span data-ttu-id="61fa9-107">A tabela de diretórios tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="61fa9-107">The Directory table has the following columns.</span></span>



| <span data-ttu-id="61fa9-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="61fa9-108">Column</span></span>            | <span data-ttu-id="61fa9-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="61fa9-109">Type</span></span>                         | <span data-ttu-id="61fa9-110">Chave</span><span class="sxs-lookup"><span data-stu-id="61fa9-110">Key</span></span> | <span data-ttu-id="61fa9-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="61fa9-111">Nullable</span></span> |
|-------------------|------------------------------|-----|----------|
| <span data-ttu-id="61fa9-112">Diretório</span><span class="sxs-lookup"><span data-stu-id="61fa9-112">Directory</span></span>         | [<span data-ttu-id="61fa9-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="61fa9-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="61fa9-114">S</span><span class="sxs-lookup"><span data-stu-id="61fa9-114">Y</span></span>   | <span data-ttu-id="61fa9-115">N</span><span class="sxs-lookup"><span data-stu-id="61fa9-115">N</span></span>        |
| <span data-ttu-id="61fa9-116">Pai do diretório \_</span><span class="sxs-lookup"><span data-stu-id="61fa9-116">Directory\_Parent</span></span> | [<span data-ttu-id="61fa9-117">Identificador</span><span class="sxs-lookup"><span data-stu-id="61fa9-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="61fa9-118">N</span><span class="sxs-lookup"><span data-stu-id="61fa9-118">N</span></span>   | <span data-ttu-id="61fa9-119">S</span><span class="sxs-lookup"><span data-stu-id="61fa9-119">Y</span></span>        |
| <span data-ttu-id="61fa9-120">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="61fa9-120">DefaultDir</span></span>        | [<span data-ttu-id="61fa9-121">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="61fa9-121">DefaultDir</span></span>](defaultdir.md) | <span data-ttu-id="61fa9-122">N</span><span class="sxs-lookup"><span data-stu-id="61fa9-122">N</span></span>   | <span data-ttu-id="61fa9-123">N</span><span class="sxs-lookup"><span data-stu-id="61fa9-123">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="61fa9-124">Colunas</span><span class="sxs-lookup"><span data-stu-id="61fa9-124">Columns</span></span>

<dl> <dt>

<span data-ttu-id="61fa9-125"><span id="Directory"></span><span id="directory"></span><span id="DIRECTORY"></span>Active</span><span class="sxs-lookup"><span data-stu-id="61fa9-125"><span id="Directory"></span><span id="directory"></span><span id="DIRECTORY"></span>Directory</span></span>
</dt> <dd>

<span data-ttu-id="61fa9-126">A coluna Directory contém um identificador exclusivo para um diretório ou caminho de diretório.</span><span class="sxs-lookup"><span data-stu-id="61fa9-126">The Directory column contains a unique identifier for a directory or directory path.</span></span> <span data-ttu-id="61fa9-127">Essa coluna pode conter o nome de uma propriedade que é definida como o caminho completo de um diretório de destino.</span><span class="sxs-lookup"><span data-stu-id="61fa9-127">This column can contain the name of a property that is set to the full path of a target directory.</span></span> <span data-ttu-id="61fa9-128">Se essa coluna contiver uma propriedade, o diretório de destino usará o nome especificado na coluna DefaultDir e usará o diretório pai especificado na \_ coluna pai do diretório.</span><span class="sxs-lookup"><span data-stu-id="61fa9-128">If this column contains a property, the target directory takes the name specified in the DefaultDir column and takes the parent directory specified in the Directory\_Parent column.</span></span>

<span data-ttu-id="61fa9-129">O diretório de origem sempre usa o nome especificado na coluna DefaultDir e usa o diretório pai especificado na \_ coluna pai do diretório.</span><span class="sxs-lookup"><span data-stu-id="61fa9-129">The source directory always takes the name specified in the DefaultDir column and takes the parent directory specified in the Directory\_Parent column.</span></span>

<span data-ttu-id="61fa9-130">Se a \_ coluna pai do diretório for nula ou igual ao valor da coluna diretório, a coluna diretório representará um diretório de destino raiz.</span><span class="sxs-lookup"><span data-stu-id="61fa9-130">If the Directory\_Parent column is either null or equal to the value of the Directory column, the Directory column represents a root target directory.</span></span> <span data-ttu-id="61fa9-131">Somente um diretório raiz pode ser especificado na tabela de diretórios.</span><span class="sxs-lookup"><span data-stu-id="61fa9-131">Only one root directory may be specified in the Directory table.</span></span>

</dd> <dt>

<span data-ttu-id="61fa9-132"><span id="Directory_Parent"></span><span id="directory_parent"></span><span id="DIRECTORY_PARENT"></span>Pai do diretório \_</span><span class="sxs-lookup"><span data-stu-id="61fa9-132"><span id="Directory_Parent"></span><span id="directory_parent"></span><span id="DIRECTORY_PARENT"></span>Directory\_Parent</span></span>
</dt> <dd>

<span data-ttu-id="61fa9-133">Esta coluna é uma referência ao diretório pai do diretório.</span><span class="sxs-lookup"><span data-stu-id="61fa9-133">This column is a reference to the directory's parent directory.</span></span> <span data-ttu-id="61fa9-134">Um registro que tem uma \_ coluna pai de diretório igual a NULL ou igual à coluna de diretório representa um diretório raiz.</span><span class="sxs-lookup"><span data-stu-id="61fa9-134">A record that has a Directory\_Parent column equal to null or equal to the Directory column represents a root directory.</span></span> <span data-ttu-id="61fa9-135">O caminho completo do diretório pai é resolvido por referência na \_ coluna pai do diretório é uma chave externa na coluna diretório.</span><span class="sxs-lookup"><span data-stu-id="61fa9-135">The full path of the parent directory is resolved by reference in the Directory\_Parent column is an external key into the Directory column.</span></span> <span data-ttu-id="61fa9-136">Por exemplo, se uma pasta tiver um diretório pai chamado PDIR, o diretório pai de PDIR será fornecido na \_ coluna pai do diretório da linha com PDIR na coluna Directory.</span><span class="sxs-lookup"><span data-stu-id="61fa9-136">For example, if a folder has a parent directory named PDIR, the parent directory of PDIR is given in the Directory\_Parent column of the row with PDIR in the Directory column.</span></span>

</dd> <dt>

<span data-ttu-id="61fa9-137"><span id="DefaultDir"></span><span id="defaultdir"></span><span id="DEFAULTDIR"></span>DefaultDir</span><span class="sxs-lookup"><span data-stu-id="61fa9-137"><span id="DefaultDir"></span><span id="defaultdir"></span><span id="DEFAULTDIR"></span>DefaultDir</span></span>
</dt> <dd>

<span data-ttu-id="61fa9-138">A coluna DefaultDir contém o nome do diretório (localizável) no diretório pai.</span><span class="sxs-lookup"><span data-stu-id="61fa9-138">The DefaultDir column contains the directory's name (localizable)under the parent directory.</span></span> <span data-ttu-id="61fa9-139">Por padrão, esse é o nome dos diretórios de destino e de origem.</span><span class="sxs-lookup"><span data-stu-id="61fa9-139">By default, this is the name of both the target and source directories.</span></span> <span data-ttu-id="61fa9-140">Para especificar nomes de diretórios de origem e de destino diferentes, separe os nomes de origem e de destino com dois-pontos da seguinte maneira: \[ TargetName \] : \[ SourceName \] .</span><span class="sxs-lookup"><span data-stu-id="61fa9-140">To specify different source and target directory names, separate the target and source names with a colon as follows: \[targetname\]:\[sourcename\].</span></span>

<span data-ttu-id="61fa9-141">Se o valor da \_ coluna pai do diretório for nulo ou for igual à coluna do diretório, a coluna DefaultDir especificará o nome de um diretório de origem raiz.</span><span class="sxs-lookup"><span data-stu-id="61fa9-141">If the value of the Directory\_Parent column is null or is equal to the Directory column, the DefaultDir column specifies the name of a root source directory.</span></span>

<span data-ttu-id="61fa9-142">Para um diretório de origem não raiz, um ponto (.) inserido na coluna DefaultDir para o nome do diretório de origem ou o nome do diretório de destino indica que o diretório deve estar localizado em seu diretório pai sem um subdiretório.</span><span class="sxs-lookup"><span data-stu-id="61fa9-142">For a non-root source directory, a period (.) entered in the DefaultDir column for the source directory name or the target directory name indicates the directory should be located in its parent directory without a subdirectory.</span></span>

<span data-ttu-id="61fa9-143">Os nomes de diretório nesta coluna podem ser formatados como pares curtos de nome de arquivo \| .</span><span class="sxs-lookup"><span data-stu-id="61fa9-143">The directory names in this column may be formatted as short filename \| long filename pairs.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="61fa9-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="61fa9-144">Remarks</span></span>

<span data-ttu-id="61fa9-145">Cada registro na tabela representa um diretório nas imagens de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="61fa9-145">Each record in the table represents a directory in both the source and the destination images.</span></span> <span data-ttu-id="61fa9-146">A tabela de diretórios deve especificar um único diretório raiz com um valor de coluna de diretório igual à propriedade [**TARGETDIR**](targetdir.md) .</span><span class="sxs-lookup"><span data-stu-id="61fa9-146">The Directory table must specify a single root directory with a Directory column value equal to the [**TARGETDIR**](targetdir.md) property.</span></span>

<span data-ttu-id="61fa9-147">Para uma [instalação administrativa](administrative-installation.md), instale a imagem administrativa no diretório raiz chamado TARGETDIR e use os nomes de diretório de origem para resolver os diretórios de destino.</span><span class="sxs-lookup"><span data-stu-id="61fa9-147">For an [administrative installation](administrative-installation.md), install the administrative image into the root directory named TARGETDIR and use the source directory names to resolve the target directories.</span></span>

<span data-ttu-id="61fa9-148">Observação o instalador define um número de [Propriedades](properties.md) padrão para caminhos de pasta do sistema.</span><span class="sxs-lookup"><span data-stu-id="61fa9-148">Note the installer sets a number of standard [properties](properties.md) to system folder paths.</span></span> <span data-ttu-id="61fa9-149">Consulte a [referência de propriedade](property-reference.md) para obter uma lista das propriedades definidas como pastas do sistema.</span><span class="sxs-lookup"><span data-stu-id="61fa9-149">See the [Property Reference](property-reference.md) for a list of the properties that are set to system folders.</span></span>

<span data-ttu-id="61fa9-150">A resolução de diretório é executada durante a [ação CostFinalize](costfinalize-action.md) e é feita da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="61fa9-150">Directory resolution is performed during the [CostFinalize action](costfinalize-action.md) and is done as follows:</span></span>

### <a name="root-destination-directory"></a><span data-ttu-id="61fa9-151">Diretório de destino raiz</span><span class="sxs-lookup"><span data-stu-id="61fa9-151">Root Destination Directory</span></span>

<span data-ttu-id="61fa9-152">Pode haver apenas um único diretório de destino raiz.</span><span class="sxs-lookup"><span data-stu-id="61fa9-152">There may only be a single root destination directory.</span></span> <span data-ttu-id="61fa9-153">Para especificar o diretório de destino raiz, defina a coluna Directory como a propriedade [**TARGETDIR**](targetdir.md) e a coluna DefaultDir como a propriedade [**SourceDir**](sourcedir.md) .</span><span class="sxs-lookup"><span data-stu-id="61fa9-153">To specify the root destination directory, set the Directory column to the [**TARGETDIR**](targetdir.md) property and the DefaultDir column to the [**SourceDir**](sourcedir.md) property.</span></span> <span data-ttu-id="61fa9-154">Se a propriedade **TARGETDIR** for definida, o diretório de destino será resolvido para o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="61fa9-154">If the **TARGETDIR** property is defined, the destination directory is resolved to the property's value.</span></span> <span data-ttu-id="61fa9-155">Se a propriedade **TARGETDIR** for indefinida, a propriedade [**ROOTDRIVE**](rootdrive.md) será usada para resolver o caminho.</span><span class="sxs-lookup"><span data-stu-id="61fa9-155">If the **TARGETDIR** property is undefined, the [**ROOTDRIVE**](rootdrive.md) property is used to resolve the path.</span></span>

### <a name="root-source-directory"></a><span data-ttu-id="61fa9-156">Diretório de origem raiz</span><span class="sxs-lookup"><span data-stu-id="61fa9-156">Root Source Directory</span></span>

<span data-ttu-id="61fa9-157">O valor da coluna DefaultDir para a entrada do diretório raiz deve ser definido como a propriedade [**SourceDir**](sourcedir.md) .</span><span class="sxs-lookup"><span data-stu-id="61fa9-157">The value of the DefaultDir column for the root directory entry must be set to the [**SourceDir**](sourcedir.md) property.</span></span>

### <a name="non-root-destination-directories"></a><span data-ttu-id="61fa9-158">Diretórios de destino não raiz</span><span class="sxs-lookup"><span data-stu-id="61fa9-158">Non-root Destination Directories</span></span>

<span data-ttu-id="61fa9-159">O valor do diretório para um diretório não raiz também é interpretado como o nome de uma propriedade que define o local do destino.</span><span class="sxs-lookup"><span data-stu-id="61fa9-159">The Directory value for a non-root directory is also interpreted as the name of a property defining the location of the destination.</span></span> <span data-ttu-id="61fa9-160">Se a propriedade for definida, o diretório de destino será resolvido para o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="61fa9-160">If the property is defined, the destination directory is resolved to the property's value.</span></span> <span data-ttu-id="61fa9-161">Se a propriedade não for definida, o diretório de destino será resolvido para um subdiretório abaixo do diretório de destino resolvido para a \_ entrada pai do diretório.</span><span class="sxs-lookup"><span data-stu-id="61fa9-161">If the property is not defined, the destination directory is resolved to a subdirectory beneath the resolved destination directory for the Directory\_Parent entry.</span></span> <span data-ttu-id="61fa9-162">O valor DefaultDir define o nome do subdiretório.</span><span class="sxs-lookup"><span data-stu-id="61fa9-162">The DefaultDir value defines the name of the subdirectory.</span></span>

### <a name="non-root-source-directories"></a><span data-ttu-id="61fa9-163">Diretórios de origem não raiz</span><span class="sxs-lookup"><span data-stu-id="61fa9-163">Non-root Source Directories</span></span>

<span data-ttu-id="61fa9-164">O diretório de origem para um diretório não raiz é resolvido para um subdiretório do diretório de origem resolvido para a \_ entrada pai do diretório.</span><span class="sxs-lookup"><span data-stu-id="61fa9-164">The source directory for a non-root directory is resolved to a subdirectory of the resolved source directory for the Directory\_Parent entry.</span></span> <span data-ttu-id="61fa9-165">Novamente, o valor DefaultDir define o nome do subdiretório.</span><span class="sxs-lookup"><span data-stu-id="61fa9-165">Again, the DefaultDir value defines the name of the subdirectory.</span></span>

### <a name="short-or-long-file-names"></a><span data-ttu-id="61fa9-166">Nomes de arquivo curtos ou longos</span><span class="sxs-lookup"><span data-stu-id="61fa9-166">Short or Long File Names</span></span>

<span data-ttu-id="61fa9-167">Ao resolver os diretórios de destino, os nomes de arquivo curtos especificados na coluna DefaultDir são usados se a propriedade [**SHORTFILENAMES**](shortfilenames.md) é definida ou o volume no qual o diretório está localizado não dá suporte a nomes de arquivo longos.</span><span class="sxs-lookup"><span data-stu-id="61fa9-167">When resolving destination directories, the short file names specified in the DefaultDir column are used if either the [**SHORTFILENAMES**](shortfilenames.md) property is set or the volume the directory is located on does not support long file names.</span></span> <span data-ttu-id="61fa9-168">Caso contrário, o nome de arquivo longo será usado.</span><span class="sxs-lookup"><span data-stu-id="61fa9-168">Otherwise, the long file name is used.</span></span>

<span data-ttu-id="61fa9-169">Observe que, quando os diretórios são resolvidos durante a ação CostFinalize, as chaves na tabela de diretórios tornam-se [Propriedades](properties.md) definidas como caminhos de diretório.</span><span class="sxs-lookup"><span data-stu-id="61fa9-169">Note that when the directories are resolved during the CostFinalize action, the keys in the Directory table become [properties](properties.md) set to directory paths.</span></span>

[<span data-ttu-id="61fa9-170">Tabela CreateFolder</span><span class="sxs-lookup"><span data-stu-id="61fa9-170">CreateFolder Table</span></span>](createfolder-table.md)

<span data-ttu-id="61fa9-171">Para criar pastas vazias durante uma instalação, consulte a [tabela CreateFolder](createfolder-table.md).</span><span class="sxs-lookup"><span data-stu-id="61fa9-171">For creating empty folders during an installation, see [CreateFolder Table](createfolder-table.md).</span></span>

[<span data-ttu-id="61fa9-172">Usando a tabela de diretórios</span><span class="sxs-lookup"><span data-stu-id="61fa9-172">Using the Directory Table</span></span>](using-the-directory-table.md)

<span data-ttu-id="61fa9-173">Para obter mais informações sobre a tabela de diretórios, incluindo exemplos, consulte [usando a tabela de diretórios](using-the-directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="61fa9-173">For more information about the Directory table, including samples, see [Using the Directory Table](using-the-directory-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="61fa9-174">Validação</span><span class="sxs-lookup"><span data-stu-id="61fa9-174">Validation</span></span>

<dl>

[<span data-ttu-id="61fa9-175">ICE03</span><span class="sxs-lookup"><span data-stu-id="61fa9-175">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="61fa9-176">ICE06</span><span class="sxs-lookup"><span data-stu-id="61fa9-176">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="61fa9-177">ICE07</span><span class="sxs-lookup"><span data-stu-id="61fa9-177">ICE07</span></span>](ice07.md)  
[<span data-ttu-id="61fa9-178">ICE30</span><span class="sxs-lookup"><span data-stu-id="61fa9-178">ICE30</span></span>](ice30.md)  
[<span data-ttu-id="61fa9-179">ICE32</span><span class="sxs-lookup"><span data-stu-id="61fa9-179">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="61fa9-180">ICE38</span><span class="sxs-lookup"><span data-stu-id="61fa9-180">ICE38</span></span>](ice38.md)  
[<span data-ttu-id="61fa9-181">ICE46</span><span class="sxs-lookup"><span data-stu-id="61fa9-181">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="61fa9-182">ICE48</span><span class="sxs-lookup"><span data-stu-id="61fa9-182">ICE48</span></span>](ice48.md)  
[<span data-ttu-id="61fa9-183">ICE56</span><span class="sxs-lookup"><span data-stu-id="61fa9-183">ICE56</span></span>](ice56.md)  
[<span data-ttu-id="61fa9-184">ICE57</span><span class="sxs-lookup"><span data-stu-id="61fa9-184">ICE57</span></span>](ice57.md)  
[<span data-ttu-id="61fa9-185">ICE64</span><span class="sxs-lookup"><span data-stu-id="61fa9-185">ICE64</span></span>](ice64.md)  
[<span data-ttu-id="61fa9-186">ICE88</span><span class="sxs-lookup"><span data-stu-id="61fa9-186">ICE88</span></span>](ice88.md)  
[<span data-ttu-id="61fa9-187">ICE90</span><span class="sxs-lookup"><span data-stu-id="61fa9-187">ICE90</span></span>](ice90.md)  
[<span data-ttu-id="61fa9-188">ICE91</span><span class="sxs-lookup"><span data-stu-id="61fa9-188">ICE91</span></span>](ice91.md)  
[<span data-ttu-id="61fa9-189">ICE99</span><span class="sxs-lookup"><span data-stu-id="61fa9-189">ICE99</span></span>](ice99.md)  
</dl>

 

 




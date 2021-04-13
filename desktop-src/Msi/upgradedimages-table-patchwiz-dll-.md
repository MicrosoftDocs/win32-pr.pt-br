---
description: A tabela UpgradedImages contém informações sobre as imagens atualizadas do produto.
ms.assetid: f4ee2cc8-8a49-4e4a-b8cf-b4ae2bc7e753
title: Tabela UpgradedImages (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48dcecc94786cbe783f21e6e005b645586f2e894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297440"
---
# <a name="upgradedimages-table-patchwizdll"></a><span data-ttu-id="6a308-103">Tabela UpgradedImages (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="6a308-103">UpgradedImages Table (Patchwiz.dll)</span></span>

<span data-ttu-id="6a308-104">A tabela UpgradedImages contém informações sobre as imagens atualizadas do produto.</span><span class="sxs-lookup"><span data-stu-id="6a308-104">The UpgradedImages table contains information about the upgraded images of the product.</span></span> <span data-ttu-id="6a308-105">A imagem atualizada deve ser uma imagem de instalação totalmente descompactada da versão mais recente do produto, por exemplo, uma imagem administrativa ou uma imagem de instalação descompactada de um CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="6a308-105">The upgraded image should be a fully uncompressed setup image of the latest version of the product, for example, an administrative image or an uncompressed setup image from a CD-ROM.</span></span> <span data-ttu-id="6a308-106">Um pacote de patch Windows Installer atualiza uma imagem de destino em uma imagem atualizada.</span><span class="sxs-lookup"><span data-stu-id="6a308-106">A Windows Installer patch package updates a target image into an upgraded image.</span></span> <span data-ttu-id="6a308-107">A tabela UpgradedImages é necessária no banco de dados de criação de patch (arquivo. PCP) e é usada pelo [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="6a308-107">The UpgradedImages table is required in the patch creation database (.pcp file) and is used by [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md).</span></span>

<span data-ttu-id="6a308-108">Uma tabela UpgradedImages contendo pelo menos um registro é necessária em cada banco de dados de criação de patch (arquivo. PCP).</span><span class="sxs-lookup"><span data-stu-id="6a308-108">An UpgradedImages table containing at least one record is required in every patch creation database (.pcp file).</span></span> <span data-ttu-id="6a308-109">Essa tabela é usada pelo [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="6a308-109">This table is used by [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md).</span></span>

<span data-ttu-id="6a308-110">A tabela UpgradedImages tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="6a308-110">The UpgradedImages table has the following columns.</span></span>



| <span data-ttu-id="6a308-111">Coluna</span><span class="sxs-lookup"><span data-stu-id="6a308-111">Column</span></span>       | <span data-ttu-id="6a308-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="6a308-112">Type</span></span> | <span data-ttu-id="6a308-113">Chave</span><span class="sxs-lookup"><span data-stu-id="6a308-113">Key</span></span> | <span data-ttu-id="6a308-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="6a308-114">Nullable</span></span> |
|--------------|------|-----|----------|
| <span data-ttu-id="6a308-115">Atualizado</span><span class="sxs-lookup"><span data-stu-id="6a308-115">Upgraded</span></span>     | <span data-ttu-id="6a308-116">text</span><span class="sxs-lookup"><span data-stu-id="6a308-116">text</span></span> | <span data-ttu-id="6a308-117">S</span><span class="sxs-lookup"><span data-stu-id="6a308-117">Y</span></span>   | <span data-ttu-id="6a308-118">N</span><span class="sxs-lookup"><span data-stu-id="6a308-118">N</span></span>        |
| <span data-ttu-id="6a308-119">MsiPath</span><span class="sxs-lookup"><span data-stu-id="6a308-119">MsiPath</span></span>      | <span data-ttu-id="6a308-120">text</span><span class="sxs-lookup"><span data-stu-id="6a308-120">text</span></span> |     | <span data-ttu-id="6a308-121">N</span><span class="sxs-lookup"><span data-stu-id="6a308-121">N</span></span>        |
| <span data-ttu-id="6a308-122">PatchMsiPath</span><span class="sxs-lookup"><span data-stu-id="6a308-122">PatchMsiPath</span></span> | <span data-ttu-id="6a308-123">text</span><span class="sxs-lookup"><span data-stu-id="6a308-123">text</span></span> |     | <span data-ttu-id="6a308-124">S</span><span class="sxs-lookup"><span data-stu-id="6a308-124">Y</span></span>        |
| <span data-ttu-id="6a308-125">SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="6a308-125">SymbolPaths</span></span>  | <span data-ttu-id="6a308-126">text</span><span class="sxs-lookup"><span data-stu-id="6a308-126">text</span></span> |     | <span data-ttu-id="6a308-127">S</span><span class="sxs-lookup"><span data-stu-id="6a308-127">Y</span></span>        |
| <span data-ttu-id="6a308-128">Família</span><span class="sxs-lookup"><span data-stu-id="6a308-128">Family</span></span>       | <span data-ttu-id="6a308-129">text</span><span class="sxs-lookup"><span data-stu-id="6a308-129">text</span></span> |     | <span data-ttu-id="6a308-130">N</span><span class="sxs-lookup"><span data-stu-id="6a308-130">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="6a308-131">Colunas</span><span class="sxs-lookup"><span data-stu-id="6a308-131">Columns</span></span>

<dl> <dt>

<span data-ttu-id="6a308-132"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Foram</span><span class="sxs-lookup"><span data-stu-id="6a308-132"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Upgraded</span></span>
</dt> <dd>

<span data-ttu-id="6a308-133">O campo atualizado é um identificador arbitrário para conectar as imagens de destino com uma imagem atualizada do produto.</span><span class="sxs-lookup"><span data-stu-id="6a308-133">The Upgraded field is an arbitrary identifier to connect the target images with an upgraded image of the product.</span></span>

</dd> <dt>

<span data-ttu-id="6a308-134"><span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>MsiPath</span><span class="sxs-lookup"><span data-stu-id="6a308-134"><span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>MsiPath</span></span>
</dt> <dd>

<span data-ttu-id="6a308-135">Este campo especifica o caminho completo, incluindo o nome do arquivo, para o local do arquivo. msi para a imagem atualizada.</span><span class="sxs-lookup"><span data-stu-id="6a308-135">This field specifies the full path, including the file name, to the location of the .msi file for the upgraded image.</span></span> <span data-ttu-id="6a308-136">Este é o local dos arquivos de origem para a imagem atualizada.</span><span class="sxs-lookup"><span data-stu-id="6a308-136">This is the location of the source files for the upgraded image.</span></span>

</dd> <dt>

<span data-ttu-id="6a308-137"><span id="PatchMsiPath"></span><span id="patchmsipath"></span><span id="PATCHMSIPATH"></span>PatchMsiPath</span><span class="sxs-lookup"><span data-stu-id="6a308-137"><span id="PatchMsiPath"></span><span id="patchmsipath"></span><span id="PATCHMSIPATH"></span>PatchMsiPath</span></span>
</dt> <dd>

<span data-ttu-id="6a308-138">O patchMsiPath opcional aponta para uma cópia modificada do banco de dados de instalação atualizado que contém a criação adicional específica do processo de instalação do patch.</span><span class="sxs-lookup"><span data-stu-id="6a308-138">The optional patchMsiPath points to a modified copy of the upgraded installation database that contains additional authoring specific to the patch installation process.</span></span> <span data-ttu-id="6a308-139">Por exemplo, caixas de diálogo adicionais ou ações personalizadas condicionadas na propriedade [**patch**](patch.md) .</span><span class="sxs-lookup"><span data-stu-id="6a308-139">For example, additional dialogs or custom actions conditioned on the [**PATCH**](patch.md) property.</span></span>

</dd> <dt>

<span data-ttu-id="6a308-140"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="6a308-140"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span></span>
</dt> <dd>

<span data-ttu-id="6a308-141">Uma lista delimitada por ponto e vírgula de pastas que devem ser pesquisadas para arquivos de símbolo que podem ser usados para otimizar a geração do patch binário.</span><span class="sxs-lookup"><span data-stu-id="6a308-141">A semicolon delimited list of folders that are to be searched for symbol files that may be used to optimize the generation of the binary patch.</span></span> <span data-ttu-id="6a308-142">Observe que os subdiretórios das pastas especificadas neste campo não são pesquisados.</span><span class="sxs-lookup"><span data-stu-id="6a308-142">Note that the subdirectories of folders specified in this field are not searched.</span></span> <span data-ttu-id="6a308-143">Um patch binário otimizado pode ser menor.</span><span class="sxs-lookup"><span data-stu-id="6a308-143">An optimized binary patch may be smaller.</span></span> <span data-ttu-id="6a308-144">Visual C++ deve ser instalado no computador que gera o patch e usado para criar os arquivos de símbolo.</span><span class="sxs-lookup"><span data-stu-id="6a308-144">Visual C++ must be installed on the computer generating the patch and used to create the symbol files.</span></span> <span data-ttu-id="6a308-145">Esse campo é opcional e o instalador cria um patch binário, mesmo se nenhum arquivo de símbolo for especificado ou se os arquivos de símbolo ficarem indisponíveis para Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="6a308-145">This field is optional, and the installer creates a binary patch even if no symbol files are specified or if the symbol files become unavailable to Patchwiz.dll.</span></span>

</dd> <dt>

<span data-ttu-id="6a308-146"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Parentes</span><span class="sxs-lookup"><span data-stu-id="6a308-146"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Family</span></span>
</dt> <dd>

<span data-ttu-id="6a308-147">Chave estrangeira na [tabela ImageFamilies](imagefamilies-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="6a308-147">Foreign key into the [ImageFamilies table](imagefamilies-table-patchwiz-dll-.md).</span></span> <span data-ttu-id="6a308-148">Cada imagem atualizada deve pertencer a apenas uma família.</span><span class="sxs-lookup"><span data-stu-id="6a308-148">Each upgraded image must belong to only one family.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6a308-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a308-149">Remarks</span></span>

<span data-ttu-id="6a308-150">Embora cada imagem atualizada possa ser agrupada em uma família de imagens separada, o agrupamento de imagens atualizadas que compartilham arquivos pode tornar o. msp menor.</span><span class="sxs-lookup"><span data-stu-id="6a308-150">Although each upgraded image can be grouped into a separate image family, grouping upgraded images that share files together may make the .msp smaller.</span></span>

<span data-ttu-id="6a308-151">Esta tabela aceita variáveis de ambiente como caminhos que começam com a versão 4,0 de Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="6a308-151">This table accepts environment variables as paths beginning with version 4.0 of Patchwiz.dll.</span></span>

 

 




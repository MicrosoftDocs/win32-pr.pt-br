---
description: A tabela TargetImages contém informações sobre as imagens de destino do produto. Um pacote de patch Windows Installer atualiza uma imagem de destino em uma imagem atualizada.
ms.assetid: 4681715e-9918-4d7b-8f33-1cca2bb34eb7
title: Tabela TargetImages (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bbb8e7bae92fbc25b217808aaae709f079d65dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837105"
---
# <a name="targetimages-table-patchwizdll"></a><span data-ttu-id="3c69c-104">Tabela TargetImages (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="3c69c-104">TargetImages Table (Patchwiz.dll)</span></span>

<span data-ttu-id="3c69c-105">A tabela TargetImages contém informações sobre as imagens de destino do produto.</span><span class="sxs-lookup"><span data-stu-id="3c69c-105">The TargetImages table contains information about the target images of the product.</span></span> <span data-ttu-id="3c69c-106">Um pacote de patch Windows Installer atualiza uma imagem de destino em uma imagem atualizada.</span><span class="sxs-lookup"><span data-stu-id="3c69c-106">A Windows Installer patch package updates a target image into an upgraded image.</span></span>

<span data-ttu-id="3c69c-107">Uma tabela TargetImages contendo pelo menos um registro é necessária em cada banco de dados de criação de patch (arquivo. PCP).</span><span class="sxs-lookup"><span data-stu-id="3c69c-107">A TargetImages table containing at least one record is required in every patch creation database (.pcp file).</span></span> <span data-ttu-id="3c69c-108">Essa tabela é usada pela função [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="3c69c-108">This table is used by the [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="3c69c-109">A tabela TargetImages tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="3c69c-109">The TargetImages table has the following columns.</span></span>



| <span data-ttu-id="3c69c-110">Coluna</span><span class="sxs-lookup"><span data-stu-id="3c69c-110">Column</span></span>                | <span data-ttu-id="3c69c-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="3c69c-111">Type</span></span>    | <span data-ttu-id="3c69c-112">Chave</span><span class="sxs-lookup"><span data-stu-id="3c69c-112">Key</span></span> | <span data-ttu-id="3c69c-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="3c69c-113">Nullable</span></span> |
|-----------------------|---------|-----|----------|
| <span data-ttu-id="3c69c-114">Destino</span><span class="sxs-lookup"><span data-stu-id="3c69c-114">Target</span></span>                | <span data-ttu-id="3c69c-115">text</span><span class="sxs-lookup"><span data-stu-id="3c69c-115">text</span></span>    | <span data-ttu-id="3c69c-116">S</span><span class="sxs-lookup"><span data-stu-id="3c69c-116">Y</span></span>   | <span data-ttu-id="3c69c-117">N</span><span class="sxs-lookup"><span data-stu-id="3c69c-117">N</span></span>        |
| <span data-ttu-id="3c69c-118">MsiPath</span><span class="sxs-lookup"><span data-stu-id="3c69c-118">MsiPath</span></span>               | <span data-ttu-id="3c69c-119">text</span><span class="sxs-lookup"><span data-stu-id="3c69c-119">text</span></span>    |     | <span data-ttu-id="3c69c-120">N</span><span class="sxs-lookup"><span data-stu-id="3c69c-120">N</span></span>        |
| <span data-ttu-id="3c69c-121">SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="3c69c-121">SymbolPaths</span></span>           | <span data-ttu-id="3c69c-122">text</span><span class="sxs-lookup"><span data-stu-id="3c69c-122">text</span></span>    |     | <span data-ttu-id="3c69c-123">S</span><span class="sxs-lookup"><span data-stu-id="3c69c-123">Y</span></span>        |
| <span data-ttu-id="3c69c-124">Atualizado</span><span class="sxs-lookup"><span data-stu-id="3c69c-124">Upgraded</span></span>              | <span data-ttu-id="3c69c-125">text</span><span class="sxs-lookup"><span data-stu-id="3c69c-125">text</span></span>    |     | <span data-ttu-id="3c69c-126">N</span><span class="sxs-lookup"><span data-stu-id="3c69c-126">N</span></span>        |
| <span data-ttu-id="3c69c-127">Ordem</span><span class="sxs-lookup"><span data-stu-id="3c69c-127">Order</span></span>                 | <span data-ttu-id="3c69c-128">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="3c69c-128">integer</span></span> |     | <span data-ttu-id="3c69c-129">N</span><span class="sxs-lookup"><span data-stu-id="3c69c-129">N</span></span>        |
| <span data-ttu-id="3c69c-130">ProductValidateFlags</span><span class="sxs-lookup"><span data-stu-id="3c69c-130">ProductValidateFlags</span></span>  | <span data-ttu-id="3c69c-131">text</span><span class="sxs-lookup"><span data-stu-id="3c69c-131">text</span></span>    |     | <span data-ttu-id="3c69c-132">S</span><span class="sxs-lookup"><span data-stu-id="3c69c-132">Y</span></span>        |
| <span data-ttu-id="3c69c-133">IgnoreMissingSrcFiles</span><span class="sxs-lookup"><span data-stu-id="3c69c-133">IgnoreMissingSrcFiles</span></span> | <span data-ttu-id="3c69c-134">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="3c69c-134">integer</span></span> |     | <span data-ttu-id="3c69c-135">N</span><span class="sxs-lookup"><span data-stu-id="3c69c-135">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="3c69c-136">Colunas</span><span class="sxs-lookup"><span data-stu-id="3c69c-136">Columns</span></span>

<dl> <dt>

<span data-ttu-id="3c69c-137"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Alvo</span><span class="sxs-lookup"><span data-stu-id="3c69c-137"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Target</span></span>
</dt> <dd>

<span data-ttu-id="3c69c-138">Identificador para uma imagem de destino.</span><span class="sxs-lookup"><span data-stu-id="3c69c-138">Identifier for a target image.</span></span> <span data-ttu-id="3c69c-139">O pacote de patch atualiza a imagem de destino especificada nesta coluna para a imagem atualizada especificada na coluna atualizado.</span><span class="sxs-lookup"><span data-stu-id="3c69c-139">The patch package updates the target image specified in this column to the upgraded image specified in the Upgraded column.</span></span> <span data-ttu-id="3c69c-140">Há uma ou mais imagens de destino para cada imagem atualizada.</span><span class="sxs-lookup"><span data-stu-id="3c69c-140">There are one or more target images for each upgraded image.</span></span> <span data-ttu-id="3c69c-141">A imagem de destino deve ser uma imagem de instalação totalmente descompactada do produto, como uma imagem administrativa ou uma imagem de instalação descompactada em um CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="3c69c-141">The target image must be a fully uncompressed setup image of the product, such as an administrative image or an uncompressed setup image on a CD-ROM.</span></span> <span data-ttu-id="3c69c-142">Observe que a função [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) não gera patches binários para arquivos em gabinetes.</span><span class="sxs-lookup"><span data-stu-id="3c69c-142">Note that the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function does not generate binary patches for files in cabinets.</span></span> <span data-ttu-id="3c69c-143">O valor nesse campo é usado com o valor no campo atualizado para gerar os nomes das transformações que o instalador adiciona ao pacote de patch.</span><span class="sxs-lookup"><span data-stu-id="3c69c-143">The value in this field is used with the value in the Upgraded field to generate the names of the transforms that the installer adds to the patch package.</span></span>

</dd> <dt>

<span data-ttu-id="3c69c-144"><span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>MsiPath</span><span class="sxs-lookup"><span data-stu-id="3c69c-144"><span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>MsiPath</span></span>
</dt> <dd>

<span data-ttu-id="3c69c-145">Este campo especifica o caminho completo, incluindo o nome do arquivo, para o local do arquivo. msi para a imagem de destino.</span><span class="sxs-lookup"><span data-stu-id="3c69c-145">This field specifies the full path, including the file name, to the location of the .msi file for the target image.</span></span> <span data-ttu-id="3c69c-146">Este é o local dos arquivos de origem para a imagem de destino.</span><span class="sxs-lookup"><span data-stu-id="3c69c-146">This is the location of the source files for the target image.</span></span>

</dd> <dt>

<span data-ttu-id="3c69c-147"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="3c69c-147"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span></span>
</dt> <dd>

<span data-ttu-id="3c69c-148">Uma lista delimitada por ponto e vírgula de pastas que devem ser pesquisadas para arquivos de símbolo que podem ser usados para otimizar a geração do patch binário.</span><span class="sxs-lookup"><span data-stu-id="3c69c-148">A semicolon delimited list of folders that are to be searched for symbol files that may be used to optimize the generation of the binary patch.</span></span> <span data-ttu-id="3c69c-149">Observe que os subdiretórios das pastas especificadas neste campo não são pesquisados.</span><span class="sxs-lookup"><span data-stu-id="3c69c-149">Note that the subdirectories of folders specified in this field are not searched.</span></span> <span data-ttu-id="3c69c-150">Um patch binário otimizado pode ser menor.</span><span class="sxs-lookup"><span data-stu-id="3c69c-150">An optimized binary patch may be smaller.</span></span> <span data-ttu-id="3c69c-151">Microsoft Visual C++ deve ser instalado no computador que gera o patch e usado para criar os arquivos de símbolo.</span><span class="sxs-lookup"><span data-stu-id="3c69c-151">Microsoft Visual C++ must be installed on the computer generating the patch and used to create the symbol files.</span></span> <span data-ttu-id="3c69c-152">Esse campo é opcional e o instalador cria um patch binário, mesmo se nenhum arquivo de símbolo for especificado ou se os arquivos de símbolo ficarem indisponíveis para Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="3c69c-152">This field is optional, and the installer creates a binary patch even if no symbol files are specified or if the symbol files become unavailable to Patchwiz.dll.</span></span>

</dd> <dt>

<span data-ttu-id="3c69c-153"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Foram</span><span class="sxs-lookup"><span data-stu-id="3c69c-153"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Upgraded</span></span>
</dt> <dd>

<span data-ttu-id="3c69c-154">Chave estrangeira para a coluna atualizada da [tabela UpgradedImages](upgradedimages-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="3c69c-154">Foreign key to the Upgraded column of the [UpgradedImages table](upgradedimages-table-patchwiz-dll-.md).</span></span> <span data-ttu-id="3c69c-155">A função [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) ignora qualquer imagem atualizada que não seja referenciada por pelo menos um registro da tabela TargetImages.</span><span class="sxs-lookup"><span data-stu-id="3c69c-155">The [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function ignores any upgraded image that is not referenced by at least one record of the TargetImages table.</span></span>

</dd> <dt>

<span data-ttu-id="3c69c-156"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordene</span><span class="sxs-lookup"><span data-stu-id="3c69c-156"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Order</span></span>
</dt> <dd>

<span data-ttu-id="3c69c-157">Ordem relativa da imagem de destino.</span><span class="sxs-lookup"><span data-stu-id="3c69c-157">Relative order of the target image.</span></span> <span data-ttu-id="3c69c-158">Como vários destinos podem ser corrigidos para uma imagem atualizada, o campo ordem fornece um meio de sequenciar as transformações na lista de transformações de patch.</span><span class="sxs-lookup"><span data-stu-id="3c69c-158">Because multiple targets can be patched to an upgraded image, the Order field provides a means to sequence the transforms in the patch transforms list.</span></span> <span data-ttu-id="3c69c-159">Normalmente, o pedido é da imagem mais antiga para a mais nova.</span><span class="sxs-lookup"><span data-stu-id="3c69c-159">Commonly, the order is from oldest to newest image.</span></span>

</dd> <dt>

<span data-ttu-id="3c69c-160"><span id="ProductValidateFlags"></span><span id="productvalidateflags"></span><span id="PRODUCTVALIDATEFLAGS"></span>ProductValidateFlags</span><span class="sxs-lookup"><span data-stu-id="3c69c-160"><span id="ProductValidateFlags"></span><span id="productvalidateflags"></span><span id="PRODUCTVALIDATEFLAGS"></span>ProductValidateFlags</span></span>
</dt> <dd>

<span data-ttu-id="3c69c-161">O campo ProductValidateFlags é usado para especificar a verificação do produto para evitar a aplicação de transformações irrelevantes.</span><span class="sxs-lookup"><span data-stu-id="3c69c-161">The ProductValidateFlags field is used to specify product checking to avoid applying irrelevant transforms.</span></span> <span data-ttu-id="3c69c-162">O valor inserido nesse campo deve ser um inteiro hexadecimal de 8 dígitos e um dos valores válidos para o parâmetro *iValidation* da função [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) .</span><span class="sxs-lookup"><span data-stu-id="3c69c-162">The value entered in this field must be an 8-digit hex integer and one of the valid values for the *iValidation* parameter of the [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) function.</span></span> <span data-ttu-id="3c69c-163">O valor padrão é 0x00000922, que é igual a **MSITRANSFORM \_ validar \_ UPDATEVERSION**  +  **MSITRANSFORM \_ validar \_ NEWEQUALBASEVERSION** MSITRANSFORM  +  **\_ validar \_ UPGRADECODE**  +  **MSITRANSFORM \_ validar \_ produto**.</span><span class="sxs-lookup"><span data-stu-id="3c69c-163">The default value is 0x00000922 which equals **MSITRANSFORM\_VALIDATE\_UPDATEVERSION** + **MSITRANSFORM\_VALIDATE\_NEWEQUALBASEVERSION** + **MSITRANSFORM\_VALIDATE\_UPGRADECODE** + **MSITRANSFORM\_VALIDATE\_PRODUCT**.</span></span>

</dd> <dt>

<span data-ttu-id="3c69c-164"><span id="IgnoreMissingSrcFiles"></span><span id="ignoremissingsrcfiles"></span><span id="IGNOREMISSINGSRCFILES"></span>IgnoreMissingSrcFiles</span><span class="sxs-lookup"><span data-stu-id="3c69c-164"><span id="IgnoreMissingSrcFiles"></span><span id="ignoremissingsrcfiles"></span><span id="IGNOREMISSINGSRCFILES"></span>IgnoreMissingSrcFiles</span></span>
</dt> <dd>

<span data-ttu-id="3c69c-165">Se esse campo for definido como um valor diferente de zero, os arquivos ausentes da imagem de destino serão ignorados pelo instalador e deixados inalterados durante a aplicação de patch.</span><span class="sxs-lookup"><span data-stu-id="3c69c-165">If this field is set to a nonzero value, files missing from the target image are ignored by the installer and left unchanged during patching.</span></span> <span data-ttu-id="3c69c-166">Isso permite que os patches sejam feitos sem a necessidade de toda a imagem; somente os arquivos alterados do produto e do arquivo. msi são necessários.</span><span class="sxs-lookup"><span data-stu-id="3c69c-166">This enables patches to be made without requiring the entire image; only the changed files of the product and the .msi file are required.</span></span> <span data-ttu-id="3c69c-167">Isso pode reduzir o tempo necessário para gerar o patch.</span><span class="sxs-lookup"><span data-stu-id="3c69c-167">This may reduce the time required to generate the patch.</span></span>

> [!Note]  
> <span data-ttu-id="3c69c-168">Não use o valor IgnoreMissingSrcFiles com TrustMsi definido como 1 na [tabela Propriedades](properties-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="3c69c-168">Do not use the IgnoreMissingSrcFiles value with TrustMsi set to 1 in the [Properties Table](properties-table-patchwiz-dll-.md).</span></span>

 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3c69c-169">Comentários</span><span class="sxs-lookup"><span data-stu-id="3c69c-169">Remarks</span></span>

<span data-ttu-id="3c69c-170">Esta tabela aceita variáveis de ambiente como caminhos que começam com a versão 4,0 de Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="3c69c-170">This table accepts environment variables as paths beginning with version 4.0 of Patchwiz.dll.</span></span>

 

 




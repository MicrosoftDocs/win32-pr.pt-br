---
description: A tabela ExternalFiles contém informações sobre arquivos específicos que não fazem parte de uma imagem de destino regular.
ms.assetid: c75591c2-5266-4a99-8104-53815f6550e2
title: Tabela ExternalFiles (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f0002961408be9f43685ef40cd2ccff729e48b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502370"
---
# <a name="externalfiles-table-patchwizdll"></a><span data-ttu-id="64083-103">Tabela ExternalFiles (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="64083-103">ExternalFiles Table (Patchwiz.dll)</span></span>

<span data-ttu-id="64083-104">A tabela ExternalFiles contém informações sobre arquivos específicos que não fazem parte de uma imagem de destino regular.</span><span class="sxs-lookup"><span data-stu-id="64083-104">The ExternalFiles table contains information about specific files that are not part of a regular target image.</span></span> <span data-ttu-id="64083-105">Esses arquivos podem existir em produtos que foram atualizados por outro produto, atualização ou patch.</span><span class="sxs-lookup"><span data-stu-id="64083-105">These files may exist in products that have been updated by another product, upgrade, or patch.</span></span> <span data-ttu-id="64083-106">Essa tabela é opcional no banco de dados de criação de patches (arquivo. PCP) e é usada pela função [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="64083-106">This table is optional in the patch creation database (.pcp file) and is used by the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="64083-107">A tabela ExternalFiles tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="64083-107">The ExternalFiles table has the following columns.</span></span>



| <span data-ttu-id="64083-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="64083-108">Column</span></span>        | <span data-ttu-id="64083-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="64083-109">Type</span></span>    | <span data-ttu-id="64083-110">Chave</span><span class="sxs-lookup"><span data-stu-id="64083-110">Key</span></span> | <span data-ttu-id="64083-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="64083-111">Nullable</span></span> |
|---------------|---------|-----|----------|
| <span data-ttu-id="64083-112">Família</span><span class="sxs-lookup"><span data-stu-id="64083-112">Family</span></span>        | <span data-ttu-id="64083-113">text</span><span class="sxs-lookup"><span data-stu-id="64083-113">text</span></span>    | <span data-ttu-id="64083-114">S</span><span class="sxs-lookup"><span data-stu-id="64083-114">Y</span></span>   | <span data-ttu-id="64083-115">N</span><span class="sxs-lookup"><span data-stu-id="64083-115">N</span></span>        |
| <span data-ttu-id="64083-116">FTK</span><span class="sxs-lookup"><span data-stu-id="64083-116">FTK</span></span>           | <span data-ttu-id="64083-117">text</span><span class="sxs-lookup"><span data-stu-id="64083-117">text</span></span>    | <span data-ttu-id="64083-118">S</span><span class="sxs-lookup"><span data-stu-id="64083-118">Y</span></span>   | <span data-ttu-id="64083-119">N</span><span class="sxs-lookup"><span data-stu-id="64083-119">N</span></span>        |
| <span data-ttu-id="64083-120">FilePath</span><span class="sxs-lookup"><span data-stu-id="64083-120">FilePath</span></span>      | <span data-ttu-id="64083-121">text</span><span class="sxs-lookup"><span data-stu-id="64083-121">text</span></span>    | <span data-ttu-id="64083-122">S</span><span class="sxs-lookup"><span data-stu-id="64083-122">Y</span></span>   | <span data-ttu-id="64083-123">N</span><span class="sxs-lookup"><span data-stu-id="64083-123">N</span></span>        |
| <span data-ttu-id="64083-124">SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="64083-124">SymbolPaths</span></span>   | <span data-ttu-id="64083-125">text</span><span class="sxs-lookup"><span data-stu-id="64083-125">text</span></span>    |     | <span data-ttu-id="64083-126">S</span><span class="sxs-lookup"><span data-stu-id="64083-126">Y</span></span>        |
| <span data-ttu-id="64083-127">IgnoreOffsets</span><span class="sxs-lookup"><span data-stu-id="64083-127">IgnoreOffsets</span></span> | <span data-ttu-id="64083-128">text</span><span class="sxs-lookup"><span data-stu-id="64083-128">text</span></span>    |     | <span data-ttu-id="64083-129">S</span><span class="sxs-lookup"><span data-stu-id="64083-129">Y</span></span>        |
| <span data-ttu-id="64083-130">IgnoreLengths</span><span class="sxs-lookup"><span data-stu-id="64083-130">IgnoreLengths</span></span> | <span data-ttu-id="64083-131">text</span><span class="sxs-lookup"><span data-stu-id="64083-131">text</span></span>    |     | <span data-ttu-id="64083-132">S</span><span class="sxs-lookup"><span data-stu-id="64083-132">Y</span></span>        |
| <span data-ttu-id="64083-133">RetainOffsets</span><span class="sxs-lookup"><span data-stu-id="64083-133">RetainOffsets</span></span> | <span data-ttu-id="64083-134">text</span><span class="sxs-lookup"><span data-stu-id="64083-134">text</span></span>    |     | <span data-ttu-id="64083-135">N</span><span class="sxs-lookup"><span data-stu-id="64083-135">N</span></span>        |
| <span data-ttu-id="64083-136">Ordem</span><span class="sxs-lookup"><span data-stu-id="64083-136">Order</span></span>         | <span data-ttu-id="64083-137">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="64083-137">integer</span></span> |     | <span data-ttu-id="64083-138">S</span><span class="sxs-lookup"><span data-stu-id="64083-138">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="64083-139">Colunas</span><span class="sxs-lookup"><span data-stu-id="64083-139">Columns</span></span>

<dl> <dt>

<span data-ttu-id="64083-140"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Parentes</span><span class="sxs-lookup"><span data-stu-id="64083-140"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Family</span></span>
</dt> <dd>

<span data-ttu-id="64083-141">Chave estrangeira para a coluna família da [tabela ImageFamilies (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="64083-141">Foreign key to the Family column of the [ImageFamilies Table (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="64083-142"><span id="FTK"></span><span id="ftk"></span>FTK</span><span class="sxs-lookup"><span data-stu-id="64083-142"><span id="FTK"></span><span id="ftk"></span>FTK</span></span>
</dt> <dd>

<span data-ttu-id="64083-143">Chave estrangeira na [tabela de arquivos](file-table.md) do arquivo. msi da imagem atualizada.</span><span class="sxs-lookup"><span data-stu-id="64083-143">Foreign key into [File table](file-table.md) of the .msi file of the upgraded image.</span></span>

</dd> <dt>

<span data-ttu-id="64083-144"><span id="FilePath"></span><span id="filepath"></span><span id="FILEPATH"></span>FilePath</span><span class="sxs-lookup"><span data-stu-id="64083-144"><span id="FilePath"></span><span id="filepath"></span><span id="FILEPATH"></span>FilePath</span></span>
</dt> <dd>

<span data-ttu-id="64083-145">Caminho completo do arquivo externo, incluindo o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="64083-145">Full path of the external file including the file name.</span></span> <span data-ttu-id="64083-146">O campo FilePath é usado para localizar o arquivo especificado na coluna FTK.</span><span class="sxs-lookup"><span data-stu-id="64083-146">FilePath field is used to locate the file specified in the FTK column.</span></span>

</dd> <dt>

<span data-ttu-id="64083-147"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="64083-147"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span></span>
</dt> <dd>

<span data-ttu-id="64083-148">O caminho completo pesquisou os arquivos de símbolo do arquivo especificado na coluna FTK.</span><span class="sxs-lookup"><span data-stu-id="64083-148">Full path searched for symbol files of the file specified in the FTK column.</span></span>

</dd> <dt>

<span data-ttu-id="64083-149"><span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets</span><span class="sxs-lookup"><span data-stu-id="64083-149"><span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets</span></span>
</dt> <dd>

<span data-ttu-id="64083-150">O valor nesse campo é uma lista delimitada por vírgulas de números de deslocamento de intervalo para os intervalos a serem ignorados no arquivo externo.</span><span class="sxs-lookup"><span data-stu-id="64083-150">The value in this field is a comma-delimited list of range offset numbers for the ranges to be ignored in the external file.</span></span> <span data-ttu-id="64083-151">A ordem e o número dos intervalos na lista devem corresponder aos itens na coluna IgnoreLengths.</span><span class="sxs-lookup"><span data-stu-id="64083-151">The order and number of the ranges in the list must match the items in the IgnoreLengths column.</span></span> <span data-ttu-id="64083-152">Essa coluna é opcional.</span><span class="sxs-lookup"><span data-stu-id="64083-152">This column is optional.</span></span>

<span data-ttu-id="64083-153">Os valores podem ser decimal ou hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="64083-153">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="64083-154">[Patchwiz.dll](patchwiz-dll.md) tratará o valor como hexadecimal se for prefixado por "0x".</span><span class="sxs-lookup"><span data-stu-id="64083-154">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="64083-155">As colunas são colunas de cadeia de caracteres e Patchwiz.dll converterá os valores em ULONGs.</span><span class="sxs-lookup"><span data-stu-id="64083-155">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="64083-156"><span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths</span><span class="sxs-lookup"><span data-stu-id="64083-156"><span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths</span></span>
</dt> <dd>

<span data-ttu-id="64083-157">O valor nesse campo é uma lista delimitada por vírgulas de comprimentos de intervalo em bytes para que os intervalos sejam ignorados no arquivo externo.</span><span class="sxs-lookup"><span data-stu-id="64083-157">The value in this field is a comma-delimited list of range lengths in bytes for the ranges to be ignored in the external file.</span></span> <span data-ttu-id="64083-158">A ordem e o número dos intervalos na lista devem corresponder aos itens na coluna IgnoreOffsets.</span><span class="sxs-lookup"><span data-stu-id="64083-158">The order and number of the ranges in the list must match the items in the IgnoreOffsets column.</span></span> <span data-ttu-id="64083-159">Essa coluna é opcional.</span><span class="sxs-lookup"><span data-stu-id="64083-159">This column is optional.</span></span>

<span data-ttu-id="64083-160">Os valores podem ser decimal ou hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="64083-160">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="64083-161">[Patchwiz.dll](patchwiz-dll.md) tratará o valor como hexadecimal se for prefixado por "0x".</span><span class="sxs-lookup"><span data-stu-id="64083-161">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="64083-162">As colunas são colunas de cadeia de caracteres e Patchwiz.dll converterá os valores em ULONGs.</span><span class="sxs-lookup"><span data-stu-id="64083-162">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="64083-163"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets</span><span class="sxs-lookup"><span data-stu-id="64083-163"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets</span></span>
</dt> <dd>

<span data-ttu-id="64083-164">O valor nesse campo é uma lista delimitada por vírgulas de números de deslocamento de intervalo para os intervalos a serem retidos no arquivo externo.</span><span class="sxs-lookup"><span data-stu-id="64083-164">The value in this field is a comma-delimited list of range offset numbers for the ranges to be retained in the External file.</span></span> <span data-ttu-id="64083-165">A ordem e o número dos intervalos na lista devem corresponder aos itens na coluna RetainOffsets do registro correspondente na [tabela FamilyFileRanges (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="64083-165">The order and number of the ranges in the list must match the items in the RetainOffsets column of the corresponding record in the [FamilyFileRanges Table (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md).</span></span>

<span data-ttu-id="64083-166">Os valores podem ser decimal ou hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="64083-166">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="64083-167">[Patchwiz.dll](patchwiz-dll.md) tratará o valor como hexadecimal se for prefixado por "0x".</span><span class="sxs-lookup"><span data-stu-id="64083-167">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="64083-168">As colunas são colunas de cadeia de caracteres e Patchwiz.dll converterá os valores em ULONGs.</span><span class="sxs-lookup"><span data-stu-id="64083-168">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="64083-169"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordene</span><span class="sxs-lookup"><span data-stu-id="64083-169"><span id="Order"></span><span id="order"></span><span id="ORDER"></span>Order</span></span>
</dt> <dd>

<span data-ttu-id="64083-170">Se duas ou mais versões forem especificadas para o mesmo arquivo externo, a tabela poderá conter vários registros com valores correspondentes nos campos FTK e Family.</span><span class="sxs-lookup"><span data-stu-id="64083-170">If two or more versions are specified for the same external file, the table may contain multiple records with matching values in the FTK and Family fields.</span></span> <span data-ttu-id="64083-171">Nesse caso, o campo Order pode especificar a ordem dos arquivos externos a serem usados ao criar o patch.</span><span class="sxs-lookup"><span data-stu-id="64083-171">In this case, the Order field may specify the order of external files to use when creating the patch.</span></span> <span data-ttu-id="64083-172">O pedido é do mais antigo para a versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="64083-172">The order is from the oldest to the most recent version.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="64083-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="64083-173">Remarks</span></span>

<span data-ttu-id="64083-174">Esta tabela aceita variáveis de ambiente como caminhos que começam com a versão 4,0 de Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="64083-174">This table accepts environment variables as paths beginning with version 4.0 of Patchwiz.dll.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64083-175">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="64083-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64083-176">Aplicação de patch nas regiões selecionadas de um arquivo</span><span class="sxs-lookup"><span data-stu-id="64083-176">Patching Selected Regions of a File</span></span>](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 




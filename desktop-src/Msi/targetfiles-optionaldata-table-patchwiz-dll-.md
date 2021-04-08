---
description: A \_ tabela TargetFiles OptionalData contém informações sobre arquivos específicos em uma imagem de destino. Essa tabela é opcional no banco de dados de criação de patches (arquivo. PCP) e é usada pela função UiCreatePatchPackageEx.
ms.assetid: 577b1674-1e44-42e1-b011-c0fb561b514c
title: Tabela de TargetFiles_OptionalData (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 859ac2e03f68c28eff5ebf7f5afa2bf53ab69299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922129"
---
# <a name="targetfiles_optionaldata-table-patchwizdll"></a><span data-ttu-id="70718-104">\_Tabela TargetFiles OptionalData (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="70718-104">TargetFiles\_OptionalData Table (Patchwiz.dll)</span></span>

<span data-ttu-id="70718-105">A \_ tabela TargetFiles OptionalData contém informações sobre arquivos específicos em uma imagem de destino.</span><span class="sxs-lookup"><span data-stu-id="70718-105">The TargetFiles\_OptionalData table contains information about specific files in a target image.</span></span> <span data-ttu-id="70718-106">Essa tabela é opcional no banco de dados de criação de patches (arquivo. PCP) e é usada pela função [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="70718-106">This table is optional in the patch creation database (.pcp file) and is used by the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="70718-107">A \_ tabela TargetFiles OptionalData tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="70718-107">The TargetFiles\_OptionalData table has the following columns.</span></span>



| <span data-ttu-id="70718-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="70718-108">Column</span></span>        | <span data-ttu-id="70718-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="70718-109">Type</span></span> | <span data-ttu-id="70718-110">Chave</span><span class="sxs-lookup"><span data-stu-id="70718-110">Key</span></span> | <span data-ttu-id="70718-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="70718-111">Nullable</span></span> |
|---------------|------|-----|----------|
| <span data-ttu-id="70718-112">Destino</span><span class="sxs-lookup"><span data-stu-id="70718-112">Target</span></span>        | <span data-ttu-id="70718-113">text</span><span class="sxs-lookup"><span data-stu-id="70718-113">text</span></span> | <span data-ttu-id="70718-114">S</span><span class="sxs-lookup"><span data-stu-id="70718-114">Y</span></span>   | <span data-ttu-id="70718-115">N</span><span class="sxs-lookup"><span data-stu-id="70718-115">N</span></span>        |
| <span data-ttu-id="70718-116">FTK</span><span class="sxs-lookup"><span data-stu-id="70718-116">FTK</span></span>           | <span data-ttu-id="70718-117">text</span><span class="sxs-lookup"><span data-stu-id="70718-117">text</span></span> | <span data-ttu-id="70718-118">S</span><span class="sxs-lookup"><span data-stu-id="70718-118">Y</span></span>   | <span data-ttu-id="70718-119">N</span><span class="sxs-lookup"><span data-stu-id="70718-119">N</span></span>        |
| <span data-ttu-id="70718-120">SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="70718-120">SymbolPaths</span></span>   | <span data-ttu-id="70718-121">text</span><span class="sxs-lookup"><span data-stu-id="70718-121">text</span></span> |     | <span data-ttu-id="70718-122">S</span><span class="sxs-lookup"><span data-stu-id="70718-122">Y</span></span>        |
| <span data-ttu-id="70718-123">IgnoreOffsets</span><span class="sxs-lookup"><span data-stu-id="70718-123">IgnoreOffsets</span></span> | <span data-ttu-id="70718-124">text</span><span class="sxs-lookup"><span data-stu-id="70718-124">text</span></span> |     | <span data-ttu-id="70718-125">S</span><span class="sxs-lookup"><span data-stu-id="70718-125">Y</span></span>        |
| <span data-ttu-id="70718-126">IgnoreLengths</span><span class="sxs-lookup"><span data-stu-id="70718-126">IgnoreLengths</span></span> | <span data-ttu-id="70718-127">text</span><span class="sxs-lookup"><span data-stu-id="70718-127">text</span></span> |     | <span data-ttu-id="70718-128">S</span><span class="sxs-lookup"><span data-stu-id="70718-128">Y</span></span>        |
| <span data-ttu-id="70718-129">RetainOffsets</span><span class="sxs-lookup"><span data-stu-id="70718-129">RetainOffsets</span></span> | <span data-ttu-id="70718-130">text</span><span class="sxs-lookup"><span data-stu-id="70718-130">text</span></span> |     | <span data-ttu-id="70718-131">S</span><span class="sxs-lookup"><span data-stu-id="70718-131">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="70718-132">Colunas</span><span class="sxs-lookup"><span data-stu-id="70718-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="70718-133"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Alvo</span><span class="sxs-lookup"><span data-stu-id="70718-133"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Target</span></span>
</dt> <dd>

<span data-ttu-id="70718-134">Chave estrangeira para a coluna de destino da [tabela TargetImages (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="70718-134">Foreign key to the Target column of the [TargetImages Table (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="70718-135"><span id="FTK"></span><span id="ftk"></span>FTK</span><span class="sxs-lookup"><span data-stu-id="70718-135"><span id="FTK"></span><span id="ftk"></span>FTK</span></span>
</dt> <dd>

<span data-ttu-id="70718-136">Chave estrangeira na [tabela de arquivos](file-table.md) da imagem de destino.</span><span class="sxs-lookup"><span data-stu-id="70718-136">Foreign key into the [File table](file-table.md) of target image.</span></span>

</dd> <dt>

<span data-ttu-id="70718-137"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="70718-137"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span></span>
</dt> <dd>

<span data-ttu-id="70718-138">O valor nesse campo é adicionado à lista delimitada por ponto-e-vírgula das pastas na coluna SymbolPaths da [tabela TargetImages (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md) quando o patch é gerado e pode ser usado para adicionar arquivos de símbolo para um arquivo específico.</span><span class="sxs-lookup"><span data-stu-id="70718-138">The value in this field is added to the semicolon delimited list of folders in the SymbolPaths column of the [TargetImages Table (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md) when the patch is generated, and can be used to add symbol files for a specific file.</span></span>

</dd> <dt>

<span data-ttu-id="70718-139"><span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets</span><span class="sxs-lookup"><span data-stu-id="70718-139"><span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets</span></span>
</dt> <dd>

<span data-ttu-id="70718-140">O valor nesse campo é uma lista delimitada por vírgulas de números de deslocamento de intervalo para os intervalos a serem ignorados no arquivo de destino.</span><span class="sxs-lookup"><span data-stu-id="70718-140">The value in this field is a comma delimited list of range offset numbers for the ranges to be ignored in the Target file.</span></span> <span data-ttu-id="70718-141">A ordem e o número dos intervalos na lista devem corresponder aos itens na coluna IgnoreLengths.</span><span class="sxs-lookup"><span data-stu-id="70718-141">The order and number of the ranges in the list must match the items in the IgnoreLengths column.</span></span> <span data-ttu-id="70718-142">Essa coluna é opcional.</span><span class="sxs-lookup"><span data-stu-id="70718-142">This column is optional.</span></span>

<span data-ttu-id="70718-143">Os valores podem ser decimal ou hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="70718-143">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="70718-144">[Patchwiz.dll](patchwiz-dll.md) tratará o valor como hexadecimal se for prefixado por "0x".</span><span class="sxs-lookup"><span data-stu-id="70718-144">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="70718-145">As colunas são colunas de cadeia de caracteres e Patchwiz.dll converterá os valores em ULONGs.</span><span class="sxs-lookup"><span data-stu-id="70718-145">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="70718-146"><span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths</span><span class="sxs-lookup"><span data-stu-id="70718-146"><span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths</span></span>
</dt> <dd>

<span data-ttu-id="70718-147">O valor nesse campo é uma lista delimitada por vírgulas de comprimentos de intervalo em bytes para que os intervalos sejam ignorados no arquivo de destino.</span><span class="sxs-lookup"><span data-stu-id="70718-147">The value in this field is a comma delimited list of range lengths in bytes for the ranges to be ignored in the Target file.</span></span> <span data-ttu-id="70718-148">A ordem e o número dos intervalos na lista devem corresponder aos itens na coluna IgnoreOffsets.</span><span class="sxs-lookup"><span data-stu-id="70718-148">The order and number of the ranges in the list must match the items in the IgnoreOffsets column.</span></span> <span data-ttu-id="70718-149">Essa coluna é opcional.</span><span class="sxs-lookup"><span data-stu-id="70718-149">This column is optional.</span></span>

<span data-ttu-id="70718-150">Os valores podem ser decimal ou hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="70718-150">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="70718-151">[Patchwiz.dll](patchwiz-dll.md) tratará o valor como hexadecimal se for prefixado por "0x".</span><span class="sxs-lookup"><span data-stu-id="70718-151">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="70718-152">As colunas são colunas de cadeia de caracteres e Patchwiz.dll converterá os valores em ULONGs.</span><span class="sxs-lookup"><span data-stu-id="70718-152">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="70718-153"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets</span><span class="sxs-lookup"><span data-stu-id="70718-153"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets</span></span>
</dt> <dd>

<span data-ttu-id="70718-154">O valor nesse campo é uma lista delimitada por vírgulas de números de deslocamento de intervalo para os intervalos a serem retidos no arquivo de destino.</span><span class="sxs-lookup"><span data-stu-id="70718-154">The value in this field is a comma delimited list of range offset numbers for the ranges to be retained in the Target file.</span></span> <span data-ttu-id="70718-155">A ordem e o número dos intervalos na lista devem corresponder aos itens na coluna RetainOffsets do registro correspondente na [tabela FamilyFileRanges (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md)</span><span class="sxs-lookup"><span data-stu-id="70718-155">The order and number of the ranges in the list must match the items in the RetainOffsets column of the corresponding record in the [FamilyFileRanges Table (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md)</span></span>

<span data-ttu-id="70718-156">Os valores podem ser decimal ou hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="70718-156">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="70718-157">[Patchwiz.dll](patchwiz-dll.md) tratará o valor como hexadecimal se for prefixado por "0x".</span><span class="sxs-lookup"><span data-stu-id="70718-157">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="70718-158">As colunas são colunas de cadeia de caracteres e Patchwiz.dll converterá os valores em ULONGs.</span><span class="sxs-lookup"><span data-stu-id="70718-158">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="70718-159">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="70718-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70718-160">Aplicação de patch nas regiões selecionadas de um arquivo</span><span class="sxs-lookup"><span data-stu-id="70718-160">Patching Selected Regions of a File</span></span>](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 




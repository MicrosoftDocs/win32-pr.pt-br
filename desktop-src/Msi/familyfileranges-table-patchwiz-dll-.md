---
description: A tabela FamilyFileRanges contém informações sobre arquivos específicos de uma imagem atualizada com intervalos que nunca devem ser substituídos.
ms.assetid: 2e77605a-d909-4a17-977c-18281a96c36c
title: Tabela FamilyFileRanges (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2940d45d82efae3e61842ee0f6b4e46e3f77ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091135"
---
# <a name="familyfileranges-table-patchwizdll"></a><span data-ttu-id="0090a-103">Tabela FamilyFileRanges (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="0090a-103">FamilyFileRanges Table (Patchwiz.dll)</span></span>

<span data-ttu-id="0090a-104">A tabela FamilyFileRanges contém informações sobre arquivos específicos de uma imagem atualizada com intervalos que nunca devem ser substituídos.</span><span class="sxs-lookup"><span data-stu-id="0090a-104">The FamilyFileRanges table contains information about particular files of an upgraded image with ranges that should never be overwritten.</span></span> <span data-ttu-id="0090a-105">Essa tabela é opcional no banco de dados de criação de patches (arquivo. PCP) e é usada pela função [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="0090a-105">This table is optional in the patch creation database (.pcp file) and is used by the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="0090a-106">A tabela FamilyFileRanges tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="0090a-106">The FamilyFileRanges table has the following columns.</span></span>



| <span data-ttu-id="0090a-107">Coluna</span><span class="sxs-lookup"><span data-stu-id="0090a-107">Column</span></span>        | <span data-ttu-id="0090a-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="0090a-108">Type</span></span> | <span data-ttu-id="0090a-109">Chave</span><span class="sxs-lookup"><span data-stu-id="0090a-109">Key</span></span> | <span data-ttu-id="0090a-110">Nullable</span><span class="sxs-lookup"><span data-stu-id="0090a-110">Nullable</span></span> |
|---------------|------|-----|----------|
| <span data-ttu-id="0090a-111">Família</span><span class="sxs-lookup"><span data-stu-id="0090a-111">Family</span></span>        | <span data-ttu-id="0090a-112">text</span><span class="sxs-lookup"><span data-stu-id="0090a-112">text</span></span> | <span data-ttu-id="0090a-113">S</span><span class="sxs-lookup"><span data-stu-id="0090a-113">Y</span></span>   | <span data-ttu-id="0090a-114">N</span><span class="sxs-lookup"><span data-stu-id="0090a-114">N</span></span>        |
| <span data-ttu-id="0090a-115">FTK</span><span class="sxs-lookup"><span data-stu-id="0090a-115">FTK</span></span>           | <span data-ttu-id="0090a-116">text</span><span class="sxs-lookup"><span data-stu-id="0090a-116">text</span></span> | <span data-ttu-id="0090a-117">S</span><span class="sxs-lookup"><span data-stu-id="0090a-117">Y</span></span>   | <span data-ttu-id="0090a-118">N</span><span class="sxs-lookup"><span data-stu-id="0090a-118">N</span></span>        |
| <span data-ttu-id="0090a-119">RetainOffsets</span><span class="sxs-lookup"><span data-stu-id="0090a-119">RetainOffsets</span></span> | <span data-ttu-id="0090a-120">text</span><span class="sxs-lookup"><span data-stu-id="0090a-120">text</span></span> |     | <span data-ttu-id="0090a-121">N</span><span class="sxs-lookup"><span data-stu-id="0090a-121">N</span></span>        |
| <span data-ttu-id="0090a-122">RetainLengths</span><span class="sxs-lookup"><span data-stu-id="0090a-122">RetainLengths</span></span> | <span data-ttu-id="0090a-123">text</span><span class="sxs-lookup"><span data-stu-id="0090a-123">text</span></span> |     | <span data-ttu-id="0090a-124">N</span><span class="sxs-lookup"><span data-stu-id="0090a-124">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="0090a-125">Colunas</span><span class="sxs-lookup"><span data-stu-id="0090a-125">Columns</span></span>

<dl> <dt>

<span data-ttu-id="0090a-126"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Parentes</span><span class="sxs-lookup"><span data-stu-id="0090a-126"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Family</span></span>
</dt> <dd>

<span data-ttu-id="0090a-127">Chave estrangeira para a coluna família da [tabela ImageFamilies (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="0090a-127">Foreign key to the Family column of the [ImageFamilies Table (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="0090a-128"><span id="FTK"></span><span id="ftk"></span>FTK</span><span class="sxs-lookup"><span data-stu-id="0090a-128"><span id="FTK"></span><span id="ftk"></span>FTK</span></span>
</dt> <dd>

<span data-ttu-id="0090a-129">Chave estrangeira nas [tabelas de arquivos](file-table.md) de todas as imagens atualizadas na família de imagens.</span><span class="sxs-lookup"><span data-stu-id="0090a-129">Foreign key into the [File tables](file-table.md) of all the upgraded images in the image family.</span></span>

</dd> <dt>

<span data-ttu-id="0090a-130"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets</span><span class="sxs-lookup"><span data-stu-id="0090a-130"><span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets</span></span>
</dt> <dd>

<span data-ttu-id="0090a-131">O deslocamento dos intervalos que não podem ser substituídos.</span><span class="sxs-lookup"><span data-stu-id="0090a-131">The offset of the ranges that cannot be overwritten.</span></span> <span data-ttu-id="0090a-132">O valor nesse campo é uma lista dos números de deslocamento de intervalo para intervalos que não devem ser substituídos nos arquivos de destino.</span><span class="sxs-lookup"><span data-stu-id="0090a-132">The value in this field is a list of the range offset numbers for ranges that are not to be overwritten in the target files.</span></span> <span data-ttu-id="0090a-133">A ordem e o número dos intervalos na lista devem corresponder aos itens na coluna RetainLengths.</span><span class="sxs-lookup"><span data-stu-id="0090a-133">The order and number of the ranges in the list must match the items in the RetainLengths column.</span></span>

<span data-ttu-id="0090a-134">Os valores podem ser decimal ou hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="0090a-134">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="0090a-135">[Patchwiz.dll](patchwiz-dll.md) tratará o valor como hexadecimal se for prefixado por "0x".</span><span class="sxs-lookup"><span data-stu-id="0090a-135">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="0090a-136">As colunas são colunas de cadeia de caracteres e Patchwiz.dll converterá os valores em ULONGs.</span><span class="sxs-lookup"><span data-stu-id="0090a-136">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> <dt>

<span data-ttu-id="0090a-137"><span id="RetainLengths"></span><span id="retainlengths"></span><span id="RETAINLENGTHS"></span>RetainLengths</span><span class="sxs-lookup"><span data-stu-id="0090a-137"><span id="RetainLengths"></span><span id="retainlengths"></span><span id="RETAINLENGTHS"></span>RetainLengths</span></span>
</dt> <dd>

<span data-ttu-id="0090a-138">O comprimento em bytes dos intervalos que não podem ser substituídos.</span><span class="sxs-lookup"><span data-stu-id="0090a-138">The length in bytes of the ranges that cannot be overwritten.</span></span> <span data-ttu-id="0090a-139">O valor nesse campo é uma lista de números de comprimento de intervalo para os intervalos a serem retidos nos arquivos de destino.</span><span class="sxs-lookup"><span data-stu-id="0090a-139">The value in this field is a list of range length numbers for ranges to retain in target files.</span></span> <span data-ttu-id="0090a-140">A ordem e o número dos intervalos na lista devem corresponder aos itens na coluna RetainOffsets.</span><span class="sxs-lookup"><span data-stu-id="0090a-140">The order and number of the ranges in the list must match the items in the RetainOffsets column.</span></span>

<span data-ttu-id="0090a-141">Os valores podem ser decimal ou hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="0090a-141">The values can be decimal or hexadecimal.</span></span> <span data-ttu-id="0090a-142">[Patchwiz.dll](patchwiz-dll.md) tratará o valor como hexadecimal se for prefixado por "0x".</span><span class="sxs-lookup"><span data-stu-id="0090a-142">[Patchwiz.dll](patchwiz-dll.md) treats the value as hexadecimal if it is prefixed by "0x".</span></span> <span data-ttu-id="0090a-143">As colunas são colunas de cadeia de caracteres e Patchwiz.dll converterá os valores em ULONGs.</span><span class="sxs-lookup"><span data-stu-id="0090a-143">The columns are string columns and Patchwiz.dll will convert the values to ULONGs.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0090a-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="0090a-144">Remarks</span></span>

<span data-ttu-id="0090a-145">Os deslocamentos e comprimentos inseridos em RetainOffsets e RetainLengths não devem especificar intervalos sobrepostos.</span><span class="sxs-lookup"><span data-stu-id="0090a-145">The offsets and lengths entered in RetainOffsets and RetainLengths must not specify overlapping ranges.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0090a-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0090a-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0090a-147">Aplicação de patch nas regiões selecionadas de um arquivo</span><span class="sxs-lookup"><span data-stu-id="0090a-147">Patching Selected Regions of a File</span></span>](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 




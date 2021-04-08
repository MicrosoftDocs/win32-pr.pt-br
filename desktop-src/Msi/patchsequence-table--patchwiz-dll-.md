---
description: A tabela PatchSequence é usada para gerar a tabela MsiPatchSequence em um patch. A tabela requer a versão do PATCHWIZ.DLL que está disponível com Windows Installer&\# 160; 3.0.
ms.assetid: bdeccb3b-57c0-4424-9602-348b8048fd46
title: Tabela PatchSequence (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 382e940d3c0cb6c7be2c8360ab98f2afaf13c799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837303"
---
# <a name="patchsequence-table-patchwizdll"></a><span data-ttu-id="33861-104">Tabela PatchSequence (PATCHWIZ.DLL)</span><span class="sxs-lookup"><span data-stu-id="33861-104">PatchSequence Table (PATCHWIZ.DLL)</span></span>

<span data-ttu-id="33861-105">A tabela PatchSequence é usada para gerar a [tabela MsiPatchSequence](msipatchsequence-table.md) em um patch.</span><span class="sxs-lookup"><span data-stu-id="33861-105">The PatchSequence Table is used to generate the [MsiPatchSequence Table](msipatchsequence-table.md) in a patch.</span></span> <span data-ttu-id="33861-106">A tabela requer a versão do [PATCHWIZ.DLL](patchwiz-dll.md) que está disponível com o Windows Installer 3,0.</span><span class="sxs-lookup"><span data-stu-id="33861-106">The table requires the version of [PATCHWIZ.DLL](patchwiz-dll.md) that is available with Windows Installer 3.0.</span></span>

<span data-ttu-id="33861-107">A tabela a seguir identifica as colunas da tabela PatchSequence.</span><span class="sxs-lookup"><span data-stu-id="33861-107">The following table identifies the columns of the PatchSequence Table.</span></span>



| <span data-ttu-id="33861-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="33861-108">Column</span></span>      | <span data-ttu-id="33861-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="33861-109">Type</span></span>       | <span data-ttu-id="33861-110">Chave</span><span class="sxs-lookup"><span data-stu-id="33861-110">Key</span></span> | <span data-ttu-id="33861-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="33861-111">Nullable</span></span> |
|-------------|------------|-----|----------|
| <span data-ttu-id="33861-112">PatchFamily</span><span class="sxs-lookup"><span data-stu-id="33861-112">PatchFamily</span></span> | <span data-ttu-id="33861-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="33861-113">Identifier</span></span> | <span data-ttu-id="33861-114">S</span><span class="sxs-lookup"><span data-stu-id="33861-114">Y</span></span>   | <span data-ttu-id="33861-115">N</span><span class="sxs-lookup"><span data-stu-id="33861-115">N</span></span>        |
| <span data-ttu-id="33861-116">Destino</span><span class="sxs-lookup"><span data-stu-id="33861-116">Target</span></span>      | <span data-ttu-id="33861-117">Texto</span><span class="sxs-lookup"><span data-stu-id="33861-117">Text</span></span>       | <span data-ttu-id="33861-118">S</span><span class="sxs-lookup"><span data-stu-id="33861-118">Y</span></span>   | <span data-ttu-id="33861-119">S</span><span class="sxs-lookup"><span data-stu-id="33861-119">Y</span></span>        |
| <span data-ttu-id="33861-120">Sequência</span><span class="sxs-lookup"><span data-stu-id="33861-120">Sequence</span></span>    | <span data-ttu-id="33861-121">Versão</span><span class="sxs-lookup"><span data-stu-id="33861-121">Version</span></span>    |     | <span data-ttu-id="33861-122">S</span><span class="sxs-lookup"><span data-stu-id="33861-122">Y</span></span>        |
| <span data-ttu-id="33861-123">Substituir</span><span class="sxs-lookup"><span data-stu-id="33861-123">Supersede</span></span>   | <span data-ttu-id="33861-124">Integer</span><span class="sxs-lookup"><span data-stu-id="33861-124">Integer</span></span>    |     | <span data-ttu-id="33861-125">S</span><span class="sxs-lookup"><span data-stu-id="33861-125">Y</span></span>        |



 

### <a name="columns"></a><span data-ttu-id="33861-126">Colunas</span><span class="sxs-lookup"><span data-stu-id="33861-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="33861-127"><span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily</span><span class="sxs-lookup"><span data-stu-id="33861-127"><span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily</span></span>
</dt> <dd>

<span data-ttu-id="33861-128">O identificador que indica as famílias de sequência às quais esse patch pertence.</span><span class="sxs-lookup"><span data-stu-id="33861-128">The identifier that indicates the sequence families to which this patch belongs.</span></span>

<span data-ttu-id="33861-129">Os valores nas colunas Target e PatchFamily juntas definem a chave primária da tabela.</span><span class="sxs-lookup"><span data-stu-id="33861-129">The values in the Target and PatchFamily columns together define the primary key for the table.</span></span> <span data-ttu-id="33861-130">Um patch que pertence a várias famílias de sequência ou tem sequências diferentes dependendo do código do produto do destino, pode ter uma linha para cada emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="33861-130">A patch that belongs to multiple sequence families, or has different sequences depending on the product code of the target, can have one row for each pairing.</span></span> <span data-ttu-id="33861-131">Esse valor é usado para preencher a coluna PatchFamily da [tabela MsiPatchSequence](msipatchsequence-table.md) que pertence ao patch.</span><span class="sxs-lookup"><span data-stu-id="33861-131">This value is used to populate the PatchFamily column of the [MsiPatchSequence Table](msipatchsequence-table.md) that belongs to the patch.</span></span>

</dd> <dt>

<span data-ttu-id="33861-132"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Alvo</span><span class="sxs-lookup"><span data-stu-id="33861-132"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Target</span></span>
</dt> <dd>

<span data-ttu-id="33861-133">A coluna de destino é usada para filtrar o PatchFamily por código de produto.</span><span class="sxs-lookup"><span data-stu-id="33861-133">The Target column is used to filter the PatchFamily by product code.</span></span>

<span data-ttu-id="33861-134">Um valor nulo nesta coluna indica que esse PatchFamily se aplica a todos os destinos do patch.</span><span class="sxs-lookup"><span data-stu-id="33861-134">A NULL value in this column indicates that this PatchFamily applies to all targets of the patch.</span></span> <span data-ttu-id="33861-135">Se essa coluna contiver uma chave estrangeira para a [tabela TargetImages](targetimages-table-patchwiz-dll-.md), o código do produto da imagem especificada será recuperado e usado para popular o valor do código do produto na linha do novo patch da [tabela MsiPatchSequence](msipatchsequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="33861-135">If this column contains a foreign key to the [TargetImages Table](targetimages-table-patchwiz-dll-.md), the product code of the specified image is retrieved and used to populate the product code value in the new patch's row of the [MsiPatchSequence Table](msipatchsequence-table.md).</span></span> <span data-ttu-id="33861-136">Se essa coluna contiver um GUID, o GUID será usado para preencher o valor do código do produto da linha na tabela MsiPatchSequence.</span><span class="sxs-lookup"><span data-stu-id="33861-136">If this column contains a GUID, the GUID is used to populate the product code value of the row in the MsiPatchSequence Table.</span></span>

</dd> <dt>

<span data-ttu-id="33861-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Ordem</span><span class="sxs-lookup"><span data-stu-id="33861-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="33861-138">O valor na coluna sequence é usado para preencher a coluna sequence da [tabela MsiPatchSequence](msipatchsequence-table.md) do novo arquivo de patch.</span><span class="sxs-lookup"><span data-stu-id="33861-138">The value in the Sequence column is used to populate the Sequence column of the [MsiPatchSequence Table](msipatchsequence-table.md) of the new patch file.</span></span>

<span data-ttu-id="33861-139">Se o valor for NULL, um número de sequência será gerado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="33861-139">If the value is NULL, a sequence number is generated automatically.</span></span>

</dd> <dt>

<span data-ttu-id="33861-140"><span id="Supersede"></span><span id="supersede"></span><span id="SUPERSEDE"></span>Substituir</span><span class="sxs-lookup"><span data-stu-id="33861-140"><span id="Supersede"></span><span id="supersede"></span><span id="SUPERSEDE"></span>Supersede</span></span>
</dt> <dd>

<span data-ttu-id="33861-141">Um valor de **msidbPatchSequenceSupersedeEarlier** ou 1 neste campo indica que esse patch substitui [as pequenas atualizações](small-updates.md) anteriores nas famílias de sequência às quais esse patch pertence.</span><span class="sxs-lookup"><span data-stu-id="33861-141">A value of **msidbPatchSequenceSupersedeEarlier** or 1 in this field indicates that this patch supersedes earlier [small updates](small-updates.md) in the sequence families to which this patch belongs.</span></span>

<span data-ttu-id="33861-142">O valor nessa coluna é usado para definir a coluna atributos da linha do novo patch na [tabela MsiPatchSequence](msipatchsequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="33861-142">The value in this column is used to set the Attributes column of the new patch's row in the [MsiPatchSequence Table](msipatchsequence-table.md) .</span></span>

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="33861-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="33861-143">Remarks</span></span>

<span data-ttu-id="33861-144">Disponível a partir do Windows Installer 3,0.</span><span class="sxs-lookup"><span data-stu-id="33861-144">Available beginning in Windows Installer 3.0.</span></span>

 

 




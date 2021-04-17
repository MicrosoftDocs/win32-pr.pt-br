---
description: A tabela MsiPatchSequence contém todas as informações que o instalador requer para determinar a sequência de aplicação de um patch de atualização pequeno em relação a todos os outros patches.
ms.assetid: ae8319ad-8136-4201-9fcf-ea58ce05f88b
title: Tabela MsiPatchSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e63252b98156a5eac1ebdc5ed5d94c7a42ec93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757115"
---
# <a name="msipatchsequence-table"></a><span data-ttu-id="1f67b-103">Tabela MsiPatchSequence</span><span class="sxs-lookup"><span data-stu-id="1f67b-103">MsiPatchSequence Table</span></span>

<span data-ttu-id="1f67b-104">A tabela MsiPatchSequence contém todas as informações que o instalador requer para determinar a sequência de aplicação de um patch de [atualização pequeno](small-updates.md) em relação a todos os outros patches.</span><span class="sxs-lookup"><span data-stu-id="1f67b-104">The MsiPatchSequence table contains all the information the installer requires to determine the sequence of application of a [small update](small-updates.md) patch relative to all other patches.</span></span> <span data-ttu-id="1f67b-105">A tabela deve estar no banco de dados do arquivo de patch e não em uma transformação no patch.</span><span class="sxs-lookup"><span data-stu-id="1f67b-105">The table must be in the database of the patch file and not in a transform in the patch.</span></span> <span data-ttu-id="1f67b-106">O instalador ignora essa tabela ao aplicar um patch de [atualização importante](major-upgrades.md) .</span><span class="sxs-lookup"><span data-stu-id="1f67b-106">The installer ignores this table when applying a [major upgrade](major-upgrades.md) patch.</span></span> <span data-ttu-id="1f67b-107">Ao aplicar um patch de [atualização secundário](minor-upgrades.md) , o instalador usa apenas essa tabela para identificar patches substituídos que não devem ser sequenciados.</span><span class="sxs-lookup"><span data-stu-id="1f67b-107">When applying a [minor upgrade](minor-upgrades.md) patch, the installer only uses this table to identify superseded patches that must not be sequenced.</span></span>

<span data-ttu-id="1f67b-108">A **tabela MsiPatchSequence** tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="1f67b-108">The **MsiPatchSequence table** has the following columns.</span></span>



| <span data-ttu-id="1f67b-109">Coluna</span><span class="sxs-lookup"><span data-stu-id="1f67b-109">Column</span></span>      | <span data-ttu-id="1f67b-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="1f67b-110">Type</span></span>                         | <span data-ttu-id="1f67b-111">Chave</span><span class="sxs-lookup"><span data-stu-id="1f67b-111">Key</span></span> | <span data-ttu-id="1f67b-112">Nullable</span><span class="sxs-lookup"><span data-stu-id="1f67b-112">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="1f67b-113">PatchFamily</span><span class="sxs-lookup"><span data-stu-id="1f67b-113">PatchFamily</span></span> | [<span data-ttu-id="1f67b-114">Identificador</span><span class="sxs-lookup"><span data-stu-id="1f67b-114">Identifier</span></span>](identifier.md) | <span data-ttu-id="1f67b-115">S</span><span class="sxs-lookup"><span data-stu-id="1f67b-115">Y</span></span>   | <span data-ttu-id="1f67b-116">N</span><span class="sxs-lookup"><span data-stu-id="1f67b-116">N</span></span>        |
| <span data-ttu-id="1f67b-117">ProductCode</span><span class="sxs-lookup"><span data-stu-id="1f67b-117">ProductCode</span></span> | [<span data-ttu-id="1f67b-118">GUID</span><span class="sxs-lookup"><span data-stu-id="1f67b-118">GUID</span></span>](guid.md)             | <span data-ttu-id="1f67b-119">S</span><span class="sxs-lookup"><span data-stu-id="1f67b-119">Y</span></span>   | <span data-ttu-id="1f67b-120">S</span><span class="sxs-lookup"><span data-stu-id="1f67b-120">Y</span></span>        |
| <span data-ttu-id="1f67b-121">Sequência</span><span class="sxs-lookup"><span data-stu-id="1f67b-121">Sequence</span></span>    | [<span data-ttu-id="1f67b-122">Versão</span><span class="sxs-lookup"><span data-stu-id="1f67b-122">Version</span></span>](version.md)       | <span data-ttu-id="1f67b-123">N</span><span class="sxs-lookup"><span data-stu-id="1f67b-123">N</span></span>   | <span data-ttu-id="1f67b-124">N</span><span class="sxs-lookup"><span data-stu-id="1f67b-124">N</span></span>        |
| <span data-ttu-id="1f67b-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="1f67b-125">Attributes</span></span>  | [<span data-ttu-id="1f67b-126">Inteiro</span><span class="sxs-lookup"><span data-stu-id="1f67b-126">Integer</span></span>](integer.md)       | <span data-ttu-id="1f67b-127">N</span><span class="sxs-lookup"><span data-stu-id="1f67b-127">N</span></span>   | <span data-ttu-id="1f67b-128">S</span><span class="sxs-lookup"><span data-stu-id="1f67b-128">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="1f67b-129">Colunas</span><span class="sxs-lookup"><span data-stu-id="1f67b-129">Columns</span></span>

<dl> <dt>

<span data-ttu-id="1f67b-130"><span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily</span><span class="sxs-lookup"><span data-stu-id="1f67b-130"><span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily</span></span>
</dt> <dd>

<span data-ttu-id="1f67b-131">Especifica que o patch é um membro da família de patches denominada neste campo.</span><span class="sxs-lookup"><span data-stu-id="1f67b-131">Specifies that the patch is a member of the patch family named in this field.</span></span> <span data-ttu-id="1f67b-132">Os patches na mesma família de patches que visam a mesma versão do produto são classificados pelos valores na coluna sequência.</span><span class="sxs-lookup"><span data-stu-id="1f67b-132">Patches in the same patch family that target the same product version are sorted by the values in the Sequence column.</span></span> <span data-ttu-id="1f67b-133">Os patches na família de patches são aplicados ao produto de destino na ordem de crescente sequência.</span><span class="sxs-lookup"><span data-stu-id="1f67b-133">The patches within the patch family are applied to the target product in the order of increasing sequence.</span></span> <span data-ttu-id="1f67b-134">O PatchFamily também é usado para determinar quais patches devem ser substituídos.</span><span class="sxs-lookup"><span data-stu-id="1f67b-134">The PatchFamily is also used to determine which patches are to be superseded.</span></span> <span data-ttu-id="1f67b-135">Um patch pode estar listado em várias linhas e pertencer a várias famílias de patches se ele se aplicar a mais de um produto ou incluir várias correções.</span><span class="sxs-lookup"><span data-stu-id="1f67b-135">A patch may be listed in multiple rows and belong to multiple patch families if it applies to more than one product or includes multiple fixes.</span></span>

<span data-ttu-id="1f67b-136">O Windows Installer não interpreta o valor de PatchFamily de nenhuma maneira diferente de comparações para igualdade em relação a outros valores de PatchFamily.</span><span class="sxs-lookup"><span data-stu-id="1f67b-136">The Windows Installer does not interpret the PatchFamily value in any way other than comparisons for equality against other PatchFamily values.</span></span> <span data-ttu-id="1f67b-137">Um valor de PatchFamily deve ser exclusivo dentro do ProductCode direcionado pelo conjunto de patches.</span><span class="sxs-lookup"><span data-stu-id="1f67b-137">A PatchFamily value must be unique within the ProductCode targeted by the set of patches.</span></span> <span data-ttu-id="1f67b-138">Nos cenários de aplicação de patch complexos, o identificador PatchFamily pode precisar ser globalmente exclusivo.</span><span class="sxs-lookup"><span data-stu-id="1f67b-138">In the complex patching scenarios the PatchFamily identifier may need to be globally unique.</span></span>

</dd> <dt>

<span data-ttu-id="1f67b-139"><span id="ProductCode"></span><span id="productcode"></span><span id="PRODUCTCODE"></span>ProductCode</span><span class="sxs-lookup"><span data-stu-id="1f67b-139"><span id="ProductCode"></span><span id="productcode"></span><span id="PRODUCTCODE"></span>ProductCode</span></span>
</dt> <dd>

<span data-ttu-id="1f67b-140">Um valor nesse campo é opcional.</span><span class="sxs-lookup"><span data-stu-id="1f67b-140">A value in this field is optional.</span></span> <span data-ttu-id="1f67b-141">Se um GUID de [código de produto](product-codes.md) for inserido neste campo e o patch estiver sendo aplicado ao produto especificado, o patch será classificado e aplicado como um membro do PatchFamily especificado.</span><span class="sxs-lookup"><span data-stu-id="1f67b-141">If a [product code](product-codes.md) GUID is entered in this field and the patch is being applied to the specified product, the patch is sorted and applied as a member of the specified PatchFamily.</span></span> <span data-ttu-id="1f67b-142">Se um GUID de código do produto for inserido neste campo e o patch não estiver sendo aplicado ao produto especificado pelo ProductCode, essa linha será ignorada.</span><span class="sxs-lookup"><span data-stu-id="1f67b-142">If a product code GUID is entered in this field and the patch is not being applied to the product specified by ProductCode, this row is ignored.</span></span> <span data-ttu-id="1f67b-143">Se o valor em ProductCode for nulo, o patch será classificado e aplicado como um membro de PatchFamily para todos os destinos do patch, independentemente do código do produto.</span><span class="sxs-lookup"><span data-stu-id="1f67b-143">If the value in ProductCode is NULL, the patch is sorted and applied as a member of PatchFamily for all targets of the patch regardless of the product code.</span></span>

<span data-ttu-id="1f67b-144">Um patch pode ter várias linhas no mesmo PatchFamily e um ProductCode diferente para cada produto direcionado ao patch.</span><span class="sxs-lookup"><span data-stu-id="1f67b-144">A patch can have multiple rows in the same PatchFamily and a different ProductCode for each product targeted by the patch.</span></span> <span data-ttu-id="1f67b-145">Uma linha para PatchFamily pode especificar NULL para ProductCode.</span><span class="sxs-lookup"><span data-stu-id="1f67b-145">One row for the PatchFamily can specify NULL for ProductCode.</span></span> <span data-ttu-id="1f67b-146">Se o produto de destino corresponder a uma linha com um ProductCode não nulo, o instalador usará a linha correspondente e ignorará a linha com o ProductCode nulo.</span><span class="sxs-lookup"><span data-stu-id="1f67b-146">If the target product matches a row with a non-NULL ProductCode, the installer uses the matching row and ignores the row with the NULL ProductCode.</span></span> <span data-ttu-id="1f67b-147">Se nenhum dos códigos de produto especificados corresponder ao destino, o patch será classificado e aplicado como membro de PatchFamily para todos os destinos do patch, independentemente do código do produto.</span><span class="sxs-lookup"><span data-stu-id="1f67b-147">If none of the specified product codes match the target, the patch is sorted and applied as a member of PatchFamily for all targets of the patch regardless of the product code.</span></span>

</dd> <dt>

<span data-ttu-id="1f67b-148"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Ordem</span><span class="sxs-lookup"><span data-stu-id="1f67b-148"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="1f67b-149">O valor na coluna sequence especifica a sequência desse patch dentro do PatchFamily especificado.</span><span class="sxs-lookup"><span data-stu-id="1f67b-149">The value in the Sequence column specifies the sequence of this patch within the specified PatchFamily.</span></span> <span data-ttu-id="1f67b-150">O valor em Sequence é expresso no formato de dados de [versão](version.md) .</span><span class="sxs-lookup"><span data-stu-id="1f67b-150">The value in Sequence is expressed in the format of [Version](version.md) data.</span></span> <span data-ttu-id="1f67b-151">O valor contém entre 1 e 4 campos e cada campo tem um intervalo de 0 a 65535.</span><span class="sxs-lookup"><span data-stu-id="1f67b-151">The value contains between 1 and 4 fields and each field has a range of 0 to 65535.</span></span> <span data-ttu-id="1f67b-152">Os membros de PatchFamily são classificados e aplicados ao produto de destino na ordem de valores de sequência crescente.</span><span class="sxs-lookup"><span data-stu-id="1f67b-152">Members of PatchFamily are sorted and applied to the target product in the order of increasing Sequence values.</span></span> <span data-ttu-id="1f67b-153">Por exemplo, os seis valores a seguir estão aumentando: 1, 1,1, 1,2, 2, 1, 2.01.1, 2.01.1.1.</span><span class="sxs-lookup"><span data-stu-id="1f67b-153">For example, the following six values are increasing: 1, 1.1, 1.2, 2.01, 2.01.1, 2.01.1.1.</span></span>

</dd> <dt>

<span data-ttu-id="1f67b-154"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="1f67b-154"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="1f67b-155">A presença do atributo **msidbPatchSequenceSupersedeEarlier** em uma linha indica que o patch de [atualização pequeno](small-updates.md) substitui as atualizações fornecidas por todos os patches com valores de sequência menores no mesmo PatchFamily.</span><span class="sxs-lookup"><span data-stu-id="1f67b-155">The presence of the **msidbPatchSequenceSupersedeEarlier** attribute in a row indicates that the [small update](small-updates.md) patch supersedes the updates provided by all patches with lesser Sequence values in the same PatchFamily.</span></span> <span data-ttu-id="1f67b-156">Esse patch contém todas as correções fornecidas por patches anteriores no PatchFamily especificado.</span><span class="sxs-lookup"><span data-stu-id="1f67b-156">This patch contains all fixes provided by earlier patches in the specified PatchFamily.</span></span> <span data-ttu-id="1f67b-157">Esse atributo não significa que esse patch substitui os patches anteriores em todos os casos porque os patches anteriores podem pertencer a várias famílias de patches.</span><span class="sxs-lookup"><span data-stu-id="1f67b-157">This attribute does not mean that this patch supersedes the earlier patches in all cases because the earlier patches can belong to multiple patch families.</span></span>

<span data-ttu-id="1f67b-158">Um patch de [atualização pequeno](small-updates.md) não pode substituir um patch de atualização [secundária](minor-upgrades.md) ou de [atualização importante](major-upgrades.md) em nenhuma circunstância, mesmo que o **msidbPatchSequenceSupersedeEarlier** esteja definido.</span><span class="sxs-lookup"><span data-stu-id="1f67b-158">A [small update](small-updates.md) patch cannot supersede a [minor upgrade](minor-upgrades.md) or [major upgrade](major-upgrades.md) patch under any circumstances, even if the **msidbPatchSequenceSupersedeEarlier** is set.</span></span> 

| <span data-ttu-id="1f67b-159">Nome</span><span class="sxs-lookup"><span data-stu-id="1f67b-159">Name</span></span>                                   | <span data-ttu-id="1f67b-160">Valor</span><span class="sxs-lookup"><span data-stu-id="1f67b-160">Value</span></span> | <span data-ttu-id="1f67b-161">Significado</span><span class="sxs-lookup"><span data-stu-id="1f67b-161">Meaning</span></span>                                                           |
|----------------------------------------|-------|-------------------------------------------------------------------|
|                                        | <span data-ttu-id="1f67b-162">0x00</span><span class="sxs-lookup"><span data-stu-id="1f67b-162">0x00</span></span>  | <span data-ttu-id="1f67b-163">Indica um valor de sequenciamento simples.</span><span class="sxs-lookup"><span data-stu-id="1f67b-163">Indicates a simple sequencing value.</span></span>                              |
| <span data-ttu-id="1f67b-164">**msidbPatchSequenceSupersedeEarlier**</span><span class="sxs-lookup"><span data-stu-id="1f67b-164">**msidbPatchSequenceSupersedeEarlier**</span></span> | <span data-ttu-id="1f67b-165">0x01</span><span class="sxs-lookup"><span data-stu-id="1f67b-165">0x01</span></span>  | <span data-ttu-id="1f67b-166">Indica um patch que substitui patches anteriores nesta família.</span><span class="sxs-lookup"><span data-stu-id="1f67b-166">Indicates a patch that supersedes earlier patches in this family.</span></span> |



 

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="1f67b-167">Validação</span><span class="sxs-lookup"><span data-stu-id="1f67b-167">Validation</span></span>

<dl>

[<span data-ttu-id="1f67b-168">ICE03</span><span class="sxs-lookup"><span data-stu-id="1f67b-168">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="1f67b-169">ICE06</span><span class="sxs-lookup"><span data-stu-id="1f67b-169">ICE06</span></span>](ice06.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="1f67b-170">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1f67b-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f67b-171">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="1f67b-171">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




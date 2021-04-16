---
description: A tabela PatchMetadata contém informações sobre um patch Windows Installer que é necessário para remover um patch e que é usado por adicionar ou remover programas.
ms.assetid: 09a06de4-0713-4e92-ab29-f34f6c94b677
title: Tabela PatchMetadata (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e2521684714b91d8d172f8eb56bab984ffea87d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747745"
---
# <a name="patchmetadata-table-patchwizdll"></a><span data-ttu-id="813ea-103">Tabela PatchMetadata (PATCHWIZ.DLL)</span><span class="sxs-lookup"><span data-stu-id="813ea-103">PatchMetadata Table (PATCHWIZ.DLL)</span></span>

<span data-ttu-id="813ea-104">A tabela PatchMetadata contém informações sobre um patch Windows Installer que é necessário para remover um patch e que é usado por adicionar ou remover programas.</span><span class="sxs-lookup"><span data-stu-id="813ea-104">The PatchMetadata Table contains information about a Windows Installer patch that is required to remove a patch and that is used by Add/Remove Programs.</span></span> <span data-ttu-id="813ea-105">Todas as propriedades na tabela PatchMetadata são adicionadas à [tabela MsiPatchMetadata](msipatchmetadata-table.md) do arquivo. msp para um patch.</span><span class="sxs-lookup"><span data-stu-id="813ea-105">All the properties in the PatchMetadata Table are added to the [MsiPatchMetadata Table](msipatchmetadata-table.md) of the .msp file for a patch.</span></span>

<span data-ttu-id="813ea-106">A tabela PatchMetadata é necessária em arquivos de propriedades de criação de patch (arquivos. PCP) que têm um MinimumRequiredMsiVersion igual a 300 na [tabela de propriedades](properties-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="813ea-106">The PatchMetadata Table is required in patch creation properties files (.pcp files) that have a MinimumRequiredMsiVersion equal to 300 in the [Properties Table](properties-table-patchwiz-dll-.md).</span></span> <span data-ttu-id="813ea-107">A tabela será opcional se MinimumRequiredMsiVersion não for igual a 300.</span><span class="sxs-lookup"><span data-stu-id="813ea-107">The table is optional if MinimumRequiredMsiVersion is not equal to 300.</span></span>

<span data-ttu-id="813ea-108">A tabela PatchMetadata tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="813ea-108">The PatchMetadata Table has the following columns.</span></span>



| <span data-ttu-id="813ea-109">Coluna</span><span class="sxs-lookup"><span data-stu-id="813ea-109">Column</span></span>   | <span data-ttu-id="813ea-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="813ea-110">Type</span></span> | <span data-ttu-id="813ea-111">Chave</span><span class="sxs-lookup"><span data-stu-id="813ea-111">Key</span></span> | <span data-ttu-id="813ea-112">Nullable</span><span class="sxs-lookup"><span data-stu-id="813ea-112">Nullable</span></span> |
|----------|------|-----|----------|
| <span data-ttu-id="813ea-113">Empresa</span><span class="sxs-lookup"><span data-stu-id="813ea-113">Company</span></span>  | <span data-ttu-id="813ea-114">text</span><span class="sxs-lookup"><span data-stu-id="813ea-114">text</span></span> | <span data-ttu-id="813ea-115">S</span><span class="sxs-lookup"><span data-stu-id="813ea-115">Y</span></span>   | <span data-ttu-id="813ea-116">S</span><span class="sxs-lookup"><span data-stu-id="813ea-116">Y</span></span>        |
| <span data-ttu-id="813ea-117">Propriedade</span><span class="sxs-lookup"><span data-stu-id="813ea-117">Property</span></span> | <span data-ttu-id="813ea-118">text</span><span class="sxs-lookup"><span data-stu-id="813ea-118">text</span></span> | <span data-ttu-id="813ea-119">S</span><span class="sxs-lookup"><span data-stu-id="813ea-119">Y</span></span>   | <span data-ttu-id="813ea-120">N</span><span class="sxs-lookup"><span data-stu-id="813ea-120">N</span></span>        |
| <span data-ttu-id="813ea-121">Valor</span><span class="sxs-lookup"><span data-stu-id="813ea-121">Value</span></span>    | <span data-ttu-id="813ea-122">text</span><span class="sxs-lookup"><span data-stu-id="813ea-122">text</span></span> |     | <span data-ttu-id="813ea-123">S</span><span class="sxs-lookup"><span data-stu-id="813ea-123">Y</span></span>        |



 

### <a name="columns"></a><span data-ttu-id="813ea-124">Colunas</span><span class="sxs-lookup"><span data-stu-id="813ea-124">Columns</span></span>

<dl> <dt>

<span data-ttu-id="813ea-125"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Corporativa</span><span class="sxs-lookup"><span data-stu-id="813ea-125"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Company</span></span>
</dt> <dd>

<span data-ttu-id="813ea-126">O nome da empresa.</span><span class="sxs-lookup"><span data-stu-id="813ea-126">The name of the company.</span></span> <span data-ttu-id="813ea-127">Um campo vazio (um valor nulo) indica que essa linha contém uma das propriedades de metadados padrão.</span><span class="sxs-lookup"><span data-stu-id="813ea-127">An empty field (a Null value) indicates that this row contains one of the standard metadata properties.</span></span> <span data-ttu-id="813ea-128">Uma empresa pode estender o conjunto de propriedades adicionando uma linha à tabela e inserindo um nome de empresa neste campo.</span><span class="sxs-lookup"><span data-stu-id="813ea-128">A company can extend the property set by adding a row to the table, and entering a company name in this field.</span></span>

</dd> <dt>

<span data-ttu-id="813ea-129"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propriedade</span><span class="sxs-lookup"><span data-stu-id="813ea-129"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="813ea-130">O nome de uma propriedade de metadados.</span><span class="sxs-lookup"><span data-stu-id="813ea-130">The name of a metadata property.</span></span> <span data-ttu-id="813ea-131">As propriedades AllowRemoval, ManufacturerName, TargetProductName, MoreInfoURL, DisplayName, Description e Classification são necessárias na tabela PatchMetadata.</span><span class="sxs-lookup"><span data-stu-id="813ea-131">The AllowRemoval, ManufacturerName, TargetProductName, MoreInfoURL, DisplayName, Description, and Classification properties are required in the PatchMetadata Table .</span></span> <span data-ttu-id="813ea-132">Esse campo deve conter uma das propriedades de metadados padrão a seguir se o campo da empresa estiver vazio (um valor nulo).</span><span class="sxs-lookup"><span data-stu-id="813ea-132">This field must contain one of the following standard metadata properties if the Company field is empty (a Null value).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="813ea-133">Propriedade</span><span class="sxs-lookup"><span data-stu-id="813ea-133">Property</span></span></th>
<th><span data-ttu-id="813ea-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="813ea-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="813ea-135">AllowRemoval</span><span class="sxs-lookup"><span data-stu-id="813ea-135">AllowRemoval</span></span></td>
<td><span data-ttu-id="813ea-136">Um valor inteiro que indica se o patch é um <a href="uninstallable-patches.md">patch desinstalável</a>.</span><span class="sxs-lookup"><span data-stu-id="813ea-136">An integer value that indicates whether or not the patch is an <a href="uninstallable-patches.md">Uninstallable Patch</a>.</span></span> <span data-ttu-id="813ea-137">Se o campo de valor contiver um 0 (zero), o patch não poderá ser removido.</span><span class="sxs-lookup"><span data-stu-id="813ea-137">If the Value field contains a 0 (zero), the patch cannot be removed.</span></span> <span data-ttu-id="813ea-138">Se o campo de valor contiver 1 (um), o patch será um patch desinstalável.</span><span class="sxs-lookup"><span data-stu-id="813ea-138">If the Value field contains 1 (one), the patch is an Uninstallable Patch.</span></span> <span data-ttu-id="813ea-139">Essa propriedade é necessária. Essa propriedade é registrada e seu valor pode ser obtido usando a função <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="813ea-139">This property is required.This property is registered and its value can be obtain by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="813ea-140">ManufacturerName</span><span class="sxs-lookup"><span data-stu-id="813ea-140">ManufacturerName</span></span></td>
<td><span data-ttu-id="813ea-141">Um valor de cadeia de caracteres que contém o nome do fabricante do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="813ea-141">A string value that contains the name of the manufacturer of the application.</span></span> <span data-ttu-id="813ea-142">Esta propriedade é necessária.</span><span class="sxs-lookup"><span data-stu-id="813ea-142">This property is required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="813ea-143">MinorUpdateTargetRTM</span><span class="sxs-lookup"><span data-stu-id="813ea-143">MinorUpdateTargetRTM</span></span></td>
<td><span data-ttu-id="813ea-144">Indica que o patch destina-se à versão RTM do produto ou ao patch de atualização principal mais recente.</span><span class="sxs-lookup"><span data-stu-id="813ea-144">Indicates that the patch targets the RTM version of the product or the most recent major upgrade patch.</span></span> <span data-ttu-id="813ea-145">Crie essa propriedade opcional em patches de atualização secundárias que contenham informações de sequenciamento para indicar que o patch remove todos os patches até a versão RTM do produto ou até o patch de atualização principal mais recente.</span><span class="sxs-lookup"><span data-stu-id="813ea-145">Author this optional property in minor upgrade patches that contain sequencing information to indicate that the patch removes of all patches up to the RTM version of the product, or up to the most recent major upgrade patch.</span></span> <span data-ttu-id="813ea-146">Essa propriedade está disponível a partir do Windows Installer 3,1.</span><span class="sxs-lookup"><span data-stu-id="813ea-146">This property is available beginning with Windows Installer 3.1.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="813ea-147">Para exigir que o Windows Installer 3,1 seja instalado para aplicar o patch, defina a propriedade MinimumRequiredMsiVersion como 310 na <a href="properties-table-patchwiz-dll-.md">tabela Properties</a> do arquivo. PCP.</span><span class="sxs-lookup"><span data-stu-id="813ea-147">To require that Windows Installer 3.1 be installed to apply the patch, set the MinimumRequiredMsiVersion property to 310 in the <a href="properties-table-patchwiz-dll-.md">Properties Table</a> of the .pcp file.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="813ea-148">TargetProductName</span><span class="sxs-lookup"><span data-stu-id="813ea-148">TargetProductName</span></span></td>
<td><span data-ttu-id="813ea-149">Um valor de cadeia de caracteres que contém o nome do aplicativo ou conjunto de aplicativos de destino.</span><span class="sxs-lookup"><span data-stu-id="813ea-149">A string value that contains the name of the application or target application suite.</span></span> <span data-ttu-id="813ea-150">Esta propriedade é necessária.</span><span class="sxs-lookup"><span data-stu-id="813ea-150">This property is required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="813ea-151">MoreInfoURL</span><span class="sxs-lookup"><span data-stu-id="813ea-151">MoreInfoURL</span></span></td>
<td><span data-ttu-id="813ea-152">Um valor de cadeia de caracteres que contém uma URL que aponta para informações para esse patch.</span><span class="sxs-lookup"><span data-stu-id="813ea-152">A string value that contains a URL pointing to information for this patch.</span></span> <span data-ttu-id="813ea-153">Essa propriedade necessária é registrada e seu valor pode ser obtido usando a função <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="813ea-153">This required property is registered and its value can be obtained by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span> <span data-ttu-id="813ea-154">A partir do Windows XP com Service Pack 2 (SP2), esse valor pode ser o link de suporte para o patch exibido em Adicionar ou remover programas.</span><span class="sxs-lookup"><span data-stu-id="813ea-154">Beginning with Windows XP with Service Pack 2 (SP2), this value can be the support link for the patch displayed in Add/Remove Programs.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="813ea-155">CreationTimeUTC</span><span class="sxs-lookup"><span data-stu-id="813ea-155">CreationTimeUTC</span></span></td>
<td><span data-ttu-id="813ea-156">Um valor de cadeia de caracteres que contém a hora de criação do arquivo. msp no formato mm-dd-aa HH: MM (mês-dia-ano hora: minuto).</span><span class="sxs-lookup"><span data-stu-id="813ea-156">A string value that contains the creation time of the .msp file in the form mm-dd-yy HH:MM (month-day-year hour:minute).</span></span> <span data-ttu-id="813ea-157">Essa propriedade é opcional.</span><span class="sxs-lookup"><span data-stu-id="813ea-157">This property is optional.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="813ea-158">DisplayName</span><span class="sxs-lookup"><span data-stu-id="813ea-158">DisplayName</span></span></td>
<td><span data-ttu-id="813ea-159">Um valor de cadeia de caracteres que contém o título para o patch que é adequado para exibição pública.</span><span class="sxs-lookup"><span data-stu-id="813ea-159">A string value that contains the title for the patch that is suitable for public display.</span></span> <span data-ttu-id="813ea-160">Esta propriedade é necessária.</span><span class="sxs-lookup"><span data-stu-id="813ea-160">This property is required.</span></span> <span data-ttu-id="813ea-161">Essa propriedade é registrada e seu valor pode ser obtido usando a função <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="813ea-161">This property is registered and its value can be obtain by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span> <span data-ttu-id="813ea-162">A partir do Windows XP com SP2, esse valor é o nome do patch exibido em Adicionar ou remover programas, começando com o Windows XP com SP2.</span><span class="sxs-lookup"><span data-stu-id="813ea-162">Beginning with Windows XP with SP2, this value is the name of the patch displayed in Add/Remove Programs beginning with Windows XP with SP2.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="813ea-163">Descrição</span><span class="sxs-lookup"><span data-stu-id="813ea-163">Description</span></span></td>
<td><span data-ttu-id="813ea-164">Um valor de cadeia de caracteres que contém uma breve descrição do patch.</span><span class="sxs-lookup"><span data-stu-id="813ea-164">A string value that contains a brief description of the patch.</span></span> <span data-ttu-id="813ea-165">Esta propriedade é necessária.</span><span class="sxs-lookup"><span data-stu-id="813ea-165">This property is required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="813ea-166">classificação</span><span class="sxs-lookup"><span data-stu-id="813ea-166">Classification</span></span></td>
<td><span data-ttu-id="813ea-167">Um valor de cadeia de caracteres que contém a categoria arbitrária de atualizações, conforme definido pelo autor do patch.</span><span class="sxs-lookup"><span data-stu-id="813ea-167">A string value that contains the arbitrary category of updates as defined by the author of the patch.</span></span> <span data-ttu-id="813ea-168">Por exemplo, os autores de patch podem especificar que cada patch seja classificado como um hotfix, ROLLUP de segurança, atualização crítica, atualização, Service Pack ou pacote cumulativo de atualizações.</span><span class="sxs-lookup"><span data-stu-id="813ea-168">For example, patch authors can specify that each patch be classified as a Hotfix, Security Rollup, Critical Update, Update, Service Pack, or Update Rollup.</span></span> <span data-ttu-id="813ea-169">Esta propriedade é necessária.</span><span class="sxs-lookup"><span data-stu-id="813ea-169">This property is required.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="813ea-170">OptimizedInstallMode</span><span class="sxs-lookup"><span data-stu-id="813ea-170">OptimizedInstallMode</span></span></td>
<td><span data-ttu-id="813ea-171">Se essa propriedade for definida como 1 (uma) em todos os patches a serem aplicados em uma transação, a aplicação do patch será otimizada, se possível.</span><span class="sxs-lookup"><span data-stu-id="813ea-171">If this property is set to 1 (one) in all the patches to be applied in a transaction, the application of the patch is optimized if possible.</span></span> <span data-ttu-id="813ea-172">Para obter informações, consulte <a href="patch-optimization.md">otimização de patch</a>.</span><span class="sxs-lookup"><span data-stu-id="813ea-172">For information, see <a href="patch-optimization.md">Patch Optimization</a>.</span></span> <span data-ttu-id="813ea-173">Disponível a partir do Windows Installer 3,1.</span><span class="sxs-lookup"><span data-stu-id="813ea-173">Available beginning with Windows Installer 3.1.</span></span></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="813ea-174"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor</span><span class="sxs-lookup"><span data-stu-id="813ea-174"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="813ea-175">Valor da propriedade de metadados.</span><span class="sxs-lookup"><span data-stu-id="813ea-175">Value of the metadata property.</span></span> <span data-ttu-id="813ea-176">Isso nunca pode ser nulo ou uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="813ea-176">This can never be Null or an empty string.</span></span> <span data-ttu-id="813ea-177">Esse valor pode ser localizado.</span><span class="sxs-lookup"><span data-stu-id="813ea-177">This value can be localized.</span></span>

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="813ea-178">Comentários</span><span class="sxs-lookup"><span data-stu-id="813ea-178">Remarks</span></span>

<span data-ttu-id="813ea-179">Disponível a partir do Windows Installer 3,0.</span><span class="sxs-lookup"><span data-stu-id="813ea-179">Available beginning in Windows Installer 3.0.</span></span>

<span data-ttu-id="813ea-180">Todas as propriedades criadas na tabela PatchMetadata são adicionadas à tabela MsiPatchMetadata do arquivo MSP.</span><span class="sxs-lookup"><span data-stu-id="813ea-180">All properties authored into the PatchMetadata Table are added to the MsiPatchMetadata table of the msp file.</span></span> <span data-ttu-id="813ea-181">As propriedades AllowRemoval, MoreInfoURL e DisplayName são registradas e podem ser acessadas por meio do [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa).</span><span class="sxs-lookup"><span data-stu-id="813ea-181">AllowRemoval, MoreInfoURL and DisplayName properties are registered and are accessible through the [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa).</span></span>

 

 





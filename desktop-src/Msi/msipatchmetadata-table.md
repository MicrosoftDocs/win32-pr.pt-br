---
description: A tabela MsiPatchMetadata contém informações sobre um patch Windows Installer necessário para remover o patch e que é usado por adicionar ou remover programas.
ms.assetid: b1c30e16-6c91-451a-8b75-7ddbcefcc092
title: Tabela MsiPatchMetadata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2642661a8f9dc067086926f8e993fc32c95a4a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747753"
---
# <a name="msipatchmetadata-table"></a><span data-ttu-id="c3497-103">Tabela MsiPatchMetadata</span><span class="sxs-lookup"><span data-stu-id="c3497-103">MsiPatchMetadata Table</span></span>

<span data-ttu-id="c3497-104">A tabela MsiPatchMetadata contém informações sobre um patch Windows Installer necessário para remover o patch e que é usado por **Adicionar ou remover programas**.</span><span class="sxs-lookup"><span data-stu-id="c3497-104">The MsiPatchMetadata Table contains information about a Windows Installer patch that is required to remove the patch and that is used by **Add/Remove Programs**.</span></span>

<span data-ttu-id="c3497-105">Os patches instalados sem esta tabela presentes no banco de dados de patch (arquivo. msp) não podem ser removidos e estão faltando algumas informações em **Adicionar ou remover programas**.</span><span class="sxs-lookup"><span data-stu-id="c3497-105">Patches installed without this table present in the patch database (.msp file) cannot be removed, and are missing some information from **Add/Remove Programs**.</span></span> <span data-ttu-id="c3497-106">A tabela deve estar no banco de dados do arquivo de patch e não em uma transformação no patch.</span><span class="sxs-lookup"><span data-stu-id="c3497-106">The table must be in the database of the patch file and not in a transform in the patch.</span></span>

<span data-ttu-id="c3497-107">A tabela MsiPatchMetadata tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3497-107">The MsiPatchMetadata Table has the following columns.</span></span>



| <span data-ttu-id="c3497-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="c3497-108">Column</span></span>   | <span data-ttu-id="c3497-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="c3497-109">Type</span></span>                         | <span data-ttu-id="c3497-110">Chave</span><span class="sxs-lookup"><span data-stu-id="c3497-110">Key</span></span> | <span data-ttu-id="c3497-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="c3497-111">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="c3497-112">Empresa</span><span class="sxs-lookup"><span data-stu-id="c3497-112">Company</span></span>  | [<span data-ttu-id="c3497-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="c3497-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="c3497-114">S</span><span class="sxs-lookup"><span data-stu-id="c3497-114">Y</span></span>   | <span data-ttu-id="c3497-115">S</span><span class="sxs-lookup"><span data-stu-id="c3497-115">Y</span></span>        |
| <span data-ttu-id="c3497-116">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c3497-116">Property</span></span> | [<span data-ttu-id="c3497-117">Identificador</span><span class="sxs-lookup"><span data-stu-id="c3497-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="c3497-118">S</span><span class="sxs-lookup"><span data-stu-id="c3497-118">Y</span></span>   | <span data-ttu-id="c3497-119">N</span><span class="sxs-lookup"><span data-stu-id="c3497-119">N</span></span>        |
| <span data-ttu-id="c3497-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c3497-120">Value</span></span>    | [<span data-ttu-id="c3497-121">Text</span><span class="sxs-lookup"><span data-stu-id="c3497-121">Text</span></span>](text.md)             | <span data-ttu-id="c3497-122">N</span><span class="sxs-lookup"><span data-stu-id="c3497-122">N</span></span>   | <span data-ttu-id="c3497-123">N</span><span class="sxs-lookup"><span data-stu-id="c3497-123">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="c3497-124">Colunas</span><span class="sxs-lookup"><span data-stu-id="c3497-124">Columns</span></span>

<dl> <dt>

<span data-ttu-id="c3497-125"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Corporativa</span><span class="sxs-lookup"><span data-stu-id="c3497-125"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Company</span></span>
</dt> <dd>

<span data-ttu-id="c3497-126">O nome da empresa.</span><span class="sxs-lookup"><span data-stu-id="c3497-126">The name of the company.</span></span> <span data-ttu-id="c3497-127">Um campo vazio (um valor nulo) indica que a linha contém uma das propriedades de metadados padrão do Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c3497-127">An empty field (a Null value) indicates that the row contains one of the standard metadata properties of the Windows Installer.</span></span> <span data-ttu-id="c3497-128">Para obter mais informações, consulte a seção comentários deste tópico.</span><span class="sxs-lookup"><span data-stu-id="c3497-128">For more information, see the Remarks section of this topic.</span></span>

<span data-ttu-id="c3497-129">Ao adicionar uma linha à tabela e inserir um nome de empresa neste campo, você pode adicionar qualquer empresa para estender o conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="c3497-129">By adding a row to the table and entering a company name in this field, you can add any company to extend the property set.</span></span>

</dd> <dt>

<span data-ttu-id="c3497-130"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propriedade</span><span class="sxs-lookup"><span data-stu-id="c3497-130"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="c3497-131">O nome de uma propriedade de metadados.</span><span class="sxs-lookup"><span data-stu-id="c3497-131">The name of a metadata property.</span></span>

</dd> <dt>

<span data-ttu-id="c3497-132"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor</span><span class="sxs-lookup"><span data-stu-id="c3497-132"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="c3497-133">O valor da propriedade de metadados.</span><span class="sxs-lookup"><span data-stu-id="c3497-133">The value of the metadata property.</span></span> <span data-ttu-id="c3497-134">Isso nunca pode ser nulo ou uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="c3497-134">This can never be Null or an empty string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c3497-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3497-135">Remarks</span></span>

<span data-ttu-id="c3497-136">Disponível no Windows Installer 3,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="c3497-136">Available in Windows Installer 3.0 and later.</span></span>

<span data-ttu-id="c3497-137">As linhas na tabela MsiPatchMetadata que contêm um valor nulo no campo CompanyName referem-se a uma das propriedades de metadados de Windows Installer padrão a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3497-137">Rows in the MsiPatchMetadata Table that contain a Null value in the CompanyName field refer to one of the following standard Windows Installer metadata properties.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c3497-138">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c3497-138">Property</span></span></th>
<th><span data-ttu-id="c3497-139">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3497-139">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c3497-140">AllowRemoval</span><span class="sxs-lookup"><span data-stu-id="c3497-140">AllowRemoval</span></span></td>
<td><span data-ttu-id="c3497-141">Indica se o patch é um <a href="uninstallable-patches.md">patch desinstalável</a>ou não.</span><span class="sxs-lookup"><span data-stu-id="c3497-141">Indicates whether or not the patch is an <a href="uninstallable-patches.md">Uninstallable Patch</a>.</span></span> <span data-ttu-id="c3497-142">Se o campo de valor contiver 0 (zero), o patch não poderá ser removido.</span><span class="sxs-lookup"><span data-stu-id="c3497-142">If the value field contains 0 (zero), the patch cannot be removed.</span></span> <span data-ttu-id="c3497-143">Se o campo de valor contiver um (1), o patch será um patch desinstalável. essa propriedade é registrada e seu valor pode ser obtido usando a função <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c3497-143">If the value field contains one (1), the patch is an Uninstallable Patch.This property is registered and its value can be obtain by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c3497-144">ManufacturerName</span><span class="sxs-lookup"><span data-stu-id="c3497-144">ManufacturerName</span></span></td>
<td><span data-ttu-id="c3497-145">Nome do fabricante do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c3497-145">Name of the manufacturer of the application.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c3497-146">MinorUpdateTargetRTM</span><span class="sxs-lookup"><span data-stu-id="c3497-146">MinorUpdateTargetRTM</span></span></td>
<td><span data-ttu-id="c3497-147">Indica que o patch destina-se à versão RTM do produto ou ao patch de atualização principal mais recente.</span><span class="sxs-lookup"><span data-stu-id="c3497-147">Indicates that the patch targets the RTM version of the product or the most recent major upgrade patch.</span></span> <span data-ttu-id="c3497-148">Crie essa propriedade opcional em patches de atualização secundárias que contenham informações de sequenciamento para indicar que o patch remove todos os patches até a versão RTM do produto ou até o patch de atualização principal mais recente.</span><span class="sxs-lookup"><span data-stu-id="c3497-148">Author this optional property in minor upgrade patches that contain sequencing information to indicate that the patch removes of all patches up to the RTM version of the product, or up to the most recent major upgrade patch.</span></span> <span data-ttu-id="c3497-149">Essa propriedade está disponível no Windows Installer 3,1 e posterior.</span><span class="sxs-lookup"><span data-stu-id="c3497-149">This property is available in Windows Installer 3.1 and later.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c3497-150">TargetProductName</span><span class="sxs-lookup"><span data-stu-id="c3497-150">TargetProductName</span></span></td>
<td><span data-ttu-id="c3497-151">Nome do aplicativo ou conjunto de aplicativos de destino.</span><span class="sxs-lookup"><span data-stu-id="c3497-151">Name of the application or target application suite.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c3497-152">MoreInfoURL</span><span class="sxs-lookup"><span data-stu-id="c3497-152">MoreInfoURL</span></span></td>
<td><span data-ttu-id="c3497-153">Uma URL que fornece informações específicas para esse patch.</span><span class="sxs-lookup"><span data-stu-id="c3497-153">A URL that provides information specific to this patch.</span></span> <span data-ttu-id="c3497-154">Essa propriedade é registrada e seu valor pode ser obtido usando a função <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c3497-154">This property is registered and its value can be obtained by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span> <span data-ttu-id="c3497-155">A partir do Windows XP com Service Pack 2 (SP2), esse valor pode ser o link de suporte para o patch exibido em <strong>Adicionar ou remover programas</strong>.</span><span class="sxs-lookup"><span data-stu-id="c3497-155">Beginning with Windows XP with Service Pack 2 (SP2), this value can be the support link for the patch displayed in <strong>Add/Remove Programs</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c3497-156">CreationTimeUTC</span><span class="sxs-lookup"><span data-stu-id="c3497-156">CreationTimeUTC</span></span></td>
<td><span data-ttu-id="c3497-157">Hora de criação do arquivo. msp no formato mm-dd-aa HH: MM (mês-dia-ano hora: minuto).</span><span class="sxs-lookup"><span data-stu-id="c3497-157">Creation time of the .msp file in the form of mm-dd-yy HH:MM (month-day-year hour:minute).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c3497-158">DisplayName</span><span class="sxs-lookup"><span data-stu-id="c3497-158">DisplayName</span></span></td>
<td><span data-ttu-id="c3497-159">Um título para o patch que é OK para a exibição pública.</span><span class="sxs-lookup"><span data-stu-id="c3497-159">A title for the patch that is okay for public display.</span></span> <span data-ttu-id="c3497-160">Essa propriedade é registrada e seu valor pode ser obtido usando a função <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c3497-160">This property is registered, and its value can be obtained by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span> <span data-ttu-id="c3497-161">A partir do Windows XP com SP2, esse valor é o nome do patch exibido em <strong>Adicionar ou remover programas</strong>.</span><span class="sxs-lookup"><span data-stu-id="c3497-161">Beginning with Windows XP with SP2, this value is the name of the patch that is displayed in <strong>Add/Remove Programs</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c3497-162">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3497-162">Description</span></span></td>
<td><span data-ttu-id="c3497-163">Breve descrição do patch.</span><span class="sxs-lookup"><span data-stu-id="c3497-163">Brief description of the patch.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c3497-164">classificação</span><span class="sxs-lookup"><span data-stu-id="c3497-164">Classification</span></span></td>
<td><span data-ttu-id="c3497-165">Um valor de cadeia de caracteres que contém a categoria arbitrária de atualizações, conforme definido pelo autor do patch.</span><span class="sxs-lookup"><span data-stu-id="c3497-165">A string value that contains the arbitrary category of updates as defined by the author of the patch.</span></span> <span data-ttu-id="c3497-166">Por exemplo, os autores de patch podem especificar que cada patch seja classificado como um hotfix, ROLLUP de segurança, atualização crítica, atualização, Service Pack ou pacote cumulativo de atualizações.</span><span class="sxs-lookup"><span data-stu-id="c3497-166">For example, patch authors can specify that each patch be classified as a Hotfix, Security Rollup, Critical Update, Update, Service Pack, or Update Rollup.</span></span> <span data-ttu-id="c3497-167">Esta propriedade é necessária.</span><span class="sxs-lookup"><span data-stu-id="c3497-167">This property is required.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c3497-168">OptimizeCA</span><span class="sxs-lookup"><span data-stu-id="c3497-168">OptimizeCA</span></span></td>
<td><span data-ttu-id="c3497-169">Indica se o Windows Installer deve ignorar ações personalizadas ao aplicar o patch.</span><span class="sxs-lookup"><span data-stu-id="c3497-169">Indicates whether the Windows Installer should skip custom actions when applying the patch.</span></span> <span data-ttu-id="c3497-170">Isso pode reduzir o tempo necessário para aplicar o patch.</span><span class="sxs-lookup"><span data-stu-id="c3497-170">This can reduce the time required to apply the patch.</span></span> <span data-ttu-id="c3497-171">A propriedade OptimizeCA pode ter um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="c3497-171">The OptimizeCA property can have one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="c3497-172">0-não ignore nenhuma ação personalizada.</span><span class="sxs-lookup"><span data-stu-id="c3497-172">0 - Do not skip any custom actions.</span></span></li>
<li><span data-ttu-id="c3497-173">1-ignorar ações personalizadas de atribuição de propriedade e de diretório.</span><span class="sxs-lookup"><span data-stu-id="c3497-173">1 - Skip property and directory assignment custom actions.</span></span> <span data-ttu-id="c3497-174">O <a href="custom-action-type-35.md">tipo de ação personalizada 35</a> e o <a href="custom-action-type-51.md">tipo de ação personalizada 51</a> podem ser ações personalizadas de atribuição de diretório e propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3497-174"><a href="custom-action-type-35.md">Custom Action Type 35</a> and <a href="custom-action-type-51.md">Custom Action Type 51</a> can be property and directory assignment custom actions.</span></span></li>
<li><span data-ttu-id="c3497-175">2-ignorar ações personalizadas imediatas que não se enquadram nas atribuições de propriedade ou de diretório.</span><span class="sxs-lookup"><span data-stu-id="c3497-175">2 - Skip immediate custom actions that do not fall into the property or directory assignments.</span></span> <span data-ttu-id="c3497-176">As ações personalizadas imediatas não incluem a opção msidbCustomActionTypeInScript na coluna Type da <a href="customaction-table.md">tabela CustomAction</a>.</span><span class="sxs-lookup"><span data-stu-id="c3497-176">The immediate custom actions do not include msidbCustomActionTypeInScript option in the Type column of the <a href="customaction-table.md">CustomAction Table</a>.</span></span></li>
<li><span data-ttu-id="c3497-177">4-ignorar ações personalizadas que são executadas no script.</span><span class="sxs-lookup"><span data-stu-id="c3497-177">4 - Skip custom actions that run within the script.</span></span></li>
</ul>
<span data-ttu-id="c3497-178">O valor de OptimizeCA deve ser o mesmo para todos os patches que estão sendo instalados ou nenhuma ação personalizada é ignorada.</span><span class="sxs-lookup"><span data-stu-id="c3497-178">The value of OptimizeCA must be the same for all patches that are being installed or no custom actions are skipped.</span></span> <span data-ttu-id="c3497-179">Por exemplo, se dois patches estiverem sendo instalados e OptimizeCA for definido para os valores 1 e 2, respectivamente, nenhuma ação personalizada será ignorada.</span><span class="sxs-lookup"><span data-stu-id="c3497-179">For example, if two patches are being installed, and OptimizeCA is set to the values 1 and 2 respectively, no custom actions are skipped.</span></span> <br/> <span data-ttu-id="c3497-180">Os valores de OptimizeCA podem ser combinados ao processar vários novos patches.</span><span class="sxs-lookup"><span data-stu-id="c3497-180">The values of OptimizeCA can be combined when processing multiple new patches.</span></span> <span data-ttu-id="c3497-181">Se todos os patches tiverem um (um) incluído nos valores, todas as ações personalizadas de atribuição de propriedades e de diretórios serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="c3497-181">If all patches have a 1 (one) included in the values, then all property and directory assignment custom actions are skipped.</span></span> <span data-ttu-id="c3497-182">Se um patch tiver o valor 3 (três) para a propriedade e um patch tiver o valor 1 (um) para a propriedade, as ações personalizadas de atribuição de diretório e propriedade serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="c3497-182">If one patch has the value 3 (three)for the property, and one patch has the value 1 (one) for the property, the property and directory assignment custom actions are skipped.</span></span> <span data-ttu-id="c3497-183">No entanto, as outras ações personalizadas imediatas são executadas, pois nem todos os patches solicitados são ignorados.</span><span class="sxs-lookup"><span data-stu-id="c3497-183">However, the other immediate custom actions run, because not all of the patches requested are skipped.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c3497-184">OptimizedInstallMode</span><span class="sxs-lookup"><span data-stu-id="c3497-184">OptimizedInstallMode</span></span></td>
<td><span data-ttu-id="c3497-185">Se essa propriedade for definida como 1 (uma) em todos os patches a serem aplicados em uma transação, um aplicativo do patch será otimizado, se possível.</span><span class="sxs-lookup"><span data-stu-id="c3497-185">If this property is set to 1 (one) in all the patches to be applied in a transaction, an application of the patch is optimized if possible.</span></span> <span data-ttu-id="c3497-186">Para obter mais informações, consulte <a href="patch-optimization.md">otimização de patch</a>.</span><span class="sxs-lookup"><span data-stu-id="c3497-186">For more information, see <a href="patch-optimization.md">Patch Optimization</a>.</span></span> <span data-ttu-id="c3497-187">Disponível a partir do Windows Installer 3,1.</span><span class="sxs-lookup"><span data-stu-id="c3497-187">Available beginning with Windows Installer 3.1.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="validation"></a><span data-ttu-id="c3497-188">Validação</span><span class="sxs-lookup"><span data-stu-id="c3497-188">Validation</span></span>

<dl>

[<span data-ttu-id="c3497-189">ICE03</span><span class="sxs-lookup"><span data-stu-id="c3497-189">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="c3497-190">ICE06</span><span class="sxs-lookup"><span data-stu-id="c3497-190">ICE06</span></span>](ice06.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="c3497-191">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c3497-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3497-192">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="c3497-192">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 





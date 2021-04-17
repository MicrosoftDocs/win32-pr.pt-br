---
description: Para reproduzir o pacote de patch de exemplo, você precisa de uma ferramenta de software capaz de criar e editar um pacote de patches Windows Installer.
ms.assetid: 0653d8f6-89b0-4c56-ae51-3c7cb7df2909
title: Criando um arquivo de propriedades de criação de patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2775f8521731b43264df315ae05a874e37dd3ffc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769324"
---
# <a name="creating-a-patch-creation-properties-file"></a><span data-ttu-id="dd183-103">Criando um arquivo de propriedades de criação de patch</span><span class="sxs-lookup"><span data-stu-id="dd183-103">Creating a Patch Creation Properties File</span></span>

<span data-ttu-id="dd183-104">Para reproduzir o pacote de patch de exemplo, você precisa de uma ferramenta de software capaz de criar e editar um pacote de patches Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="dd183-104">To reproduce the sample patch package, you need a software tool capable of creating and editing a Windows Installer patch package.</span></span> <span data-ttu-id="dd183-105">Várias ferramentas de criação de pacotes de patches estão disponíveis de fornecedores de software independentes.</span><span class="sxs-lookup"><span data-stu-id="dd183-105">Several patch package creation tools are available from independent software vendors.</span></span> <span data-ttu-id="dd183-106">O exemplo discutido nas seções a seguir usa um editor de banco de dados Windows Installer chamado Orca para criar um arquivo de propriedades de criação de patch (extensão. PCP).</span><span class="sxs-lookup"><span data-stu-id="dd183-106">The example discussed in the following sections uses a Windows Installer database editor called Orca to author a patch creation properties file (.pcp extension).</span></span> <span data-ttu-id="dd183-107">O arquivo. PCP pode ser usado com os utilitários [Msimsp.exe](msimsp-exe.md) e [Patchwiz.dll](patchwiz-dll.md) para gerar um pacote de patches Windows Installer (extensão. msp).</span><span class="sxs-lookup"><span data-stu-id="dd183-107">The .pcp file may be used with the utilities [Msimsp.exe](msimsp-exe.md) and [Patchwiz.dll](patchwiz-dll.md) to generate a Windows Installer patch package (.msp extension).</span></span> <span data-ttu-id="dd183-108">O orca, Msimsp.exe e Patchwiz.dll são fornecidos nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="dd183-108">Orca, Msimsp.exe, and Patchwiz.dll are provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="dd183-109">Um arquivo de propriedades de criação de patch em branco, template. PCP, também é fornecido com o SDK.</span><span class="sxs-lookup"><span data-stu-id="dd183-109">A blank patch creation properties file, template.pcp, is also provided with the SDK.</span></span> <span data-ttu-id="dd183-110">Faça uma cópia de template. PCP e renomeie essa cópia MNP2000. PCP.</span><span class="sxs-lookup"><span data-stu-id="dd183-110">Make a copy of template.pcp and rename this copy MNP2000.pcp.</span></span> <span data-ttu-id="dd183-111">Use o Orca ou outro editor de banco de dados para inserir os itens a seguir na tabela Properties de MNP2000. PCP.</span><span class="sxs-lookup"><span data-stu-id="dd183-111">Use Orca or another database editor to enter the following data into the Properties table of MNP2000.pcp.</span></span> <span data-ttu-id="dd183-112">A tabela de propriedades contém configurações globais para o pacote de patch.</span><span class="sxs-lookup"><span data-stu-id="dd183-112">The Properties table contains global settings for the patch package.</span></span>

[<span data-ttu-id="dd183-113">Tabela de propriedades</span><span class="sxs-lookup"><span data-stu-id="dd183-113">Properties Table</span></span>](properties-table-patchwiz-dll-.md)



| <span data-ttu-id="dd183-114">Nome</span><span class="sxs-lookup"><span data-stu-id="dd183-114">Name</span></span>                               | <span data-ttu-id="dd183-115">Valor</span><span class="sxs-lookup"><span data-stu-id="dd183-115">Value</span></span>                                  |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="dd183-116">AllowProductCodeMismatches</span><span class="sxs-lookup"><span data-stu-id="dd183-116">AllowProductCodeMismatches</span></span>         | <span data-ttu-id="dd183-117">1</span><span class="sxs-lookup"><span data-stu-id="dd183-117">1</span></span>                                      |
| <span data-ttu-id="dd183-118">AllowProductVersionMajorMismatches</span><span class="sxs-lookup"><span data-stu-id="dd183-118">AllowProductVersionMajorMismatches</span></span> | <span data-ttu-id="dd183-119">1</span><span class="sxs-lookup"><span data-stu-id="dd183-119">1</span></span>                                      |
| <span data-ttu-id="dd183-120">ApiPatchingSymbolFlags</span><span class="sxs-lookup"><span data-stu-id="dd183-120">ApiPatchingSymbolFlags</span></span>             | <span data-ttu-id="dd183-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dd183-121">0x00000000</span></span>                             |
| <span data-ttu-id="dd183-122">DontRemoveTempFolderWhenFinished</span><span class="sxs-lookup"><span data-stu-id="dd183-122">DontRemoveTempFolderWhenFinished</span></span>   | <span data-ttu-id="dd183-123">1</span><span class="sxs-lookup"><span data-stu-id="dd183-123">1</span></span>                                      |
| <span data-ttu-id="dd183-124">IncludeWholeFilesOnly</span><span class="sxs-lookup"><span data-stu-id="dd183-124">IncludeWholeFilesOnly</span></span>              | <span data-ttu-id="dd183-125">0</span><span class="sxs-lookup"><span data-stu-id="dd183-125">0</span></span>                                      |
| <span data-ttu-id="dd183-126">ListOfPatchGUIDsToReplace</span><span class="sxs-lookup"><span data-stu-id="dd183-126">ListOfPatchGUIDsToReplace</span></span>          |                                        |
| <span data-ttu-id="dd183-127">ListOfTargetProductCodes</span><span class="sxs-lookup"><span data-stu-id="dd183-127">ListOfTargetProductCodes</span></span>           | \*                                     |
| <span data-ttu-id="dd183-128">PatchGUID</span><span class="sxs-lookup"><span data-stu-id="dd183-128">PatchGUID</span></span>                          | <span data-ttu-id="dd183-129">{5406B219-A1AC-4BC4-8695-72292C8195AC}</span><span class="sxs-lookup"><span data-stu-id="dd183-129">{5406B219-A1AC-4BC4-8695-72292C8195AC}</span></span> |
| <span data-ttu-id="dd183-130">PatchOutputPath</span><span class="sxs-lookup"><span data-stu-id="dd183-130">PatchOutputPath</span></span>                    | <span data-ttu-id="dd183-131">c: \\ output. msp</span><span class="sxs-lookup"><span data-stu-id="dd183-131">c:\\output.msp</span></span>                         |
| <span data-ttu-id="dd183-132">PatchSourceList</span><span class="sxs-lookup"><span data-stu-id="dd183-132">PatchSourceList</span></span>                    | <span data-ttu-id="dd183-133">PatchSourceList</span><span class="sxs-lookup"><span data-stu-id="dd183-133">PatchSourceList</span></span>                        |



 

<span data-ttu-id="dd183-134">Use o editor de banco de dados do para inserir os itens a seguir na tabela ImageFamilies de MNP2000. PCP.</span><span class="sxs-lookup"><span data-stu-id="dd183-134">Use the database editor to enter the following data into the ImageFamilies table of MNP2000.pcp.</span></span> <span data-ttu-id="dd183-135">A tabela ImageFamilies contém informações a serem adicionadas à [tabela de mídia](media-table.md) durante a aplicação de patch.</span><span class="sxs-lookup"><span data-stu-id="dd183-135">The ImageFamilies table contains information to be added to the [Media table](media-table.md) during patching.</span></span>

[<span data-ttu-id="dd183-136">Tabela ImageFamilies</span><span class="sxs-lookup"><span data-stu-id="dd183-136">ImageFamilies Table</span></span>](imagefamilies-table-patchwiz-dll-.md)



| <span data-ttu-id="dd183-137">Família</span><span class="sxs-lookup"><span data-stu-id="dd183-137">Family</span></span>  | <span data-ttu-id="dd183-138">MediaSrcPropName</span><span class="sxs-lookup"><span data-stu-id="dd183-138">MediaSrcPropName</span></span> | <span data-ttu-id="dd183-139">MediaDiskId</span><span class="sxs-lookup"><span data-stu-id="dd183-139">MediaDiskId</span></span> | <span data-ttu-id="dd183-140">FileSequenceStart</span><span class="sxs-lookup"><span data-stu-id="dd183-140">FileSequenceStart</span></span> | <span data-ttu-id="dd183-141">DiskPrompt</span><span class="sxs-lookup"><span data-stu-id="dd183-141">DiskPrompt</span></span> | <span data-ttu-id="dd183-142">VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="dd183-142">VolumeLabel</span></span> |
|---------|------------------|-------------|-------------------|------------|-------------|
| <span data-ttu-id="dd183-143">MNPapps</span><span class="sxs-lookup"><span data-stu-id="dd183-143">MNPapps</span></span> | <span data-ttu-id="dd183-144">MNPSrcPropName</span><span class="sxs-lookup"><span data-stu-id="dd183-144">MNPSrcPropName</span></span>   | <span data-ttu-id="dd183-145">2</span><span class="sxs-lookup"><span data-stu-id="dd183-145">2</span></span>           | <span data-ttu-id="dd183-146">1000</span><span class="sxs-lookup"><span data-stu-id="dd183-146">1000</span></span>              |            |             |



 

<span data-ttu-id="dd183-147">Insira os dados a seguir na tabela UpgradedImages de MNP2000. PCP.</span><span class="sxs-lookup"><span data-stu-id="dd183-147">Enter the following data into the UpgradedImages table of MNP2000.pcp.</span></span> <span data-ttu-id="dd183-148">A tabela UpgradedImages contém informações sobre a imagem atualizada que você criou no [planejamento de um patch de atualização pequeno](planning-a-small-update-patch.md).</span><span class="sxs-lookup"><span data-stu-id="dd183-148">The UpgradedImages table contains information about the Upgraded image you created in [Planning a Small Update Patch](planning-a-small-update-patch.md).</span></span>

[<span data-ttu-id="dd183-149">Tabela UpgradedImages</span><span class="sxs-lookup"><span data-stu-id="dd183-149">UpgradedImages Table</span></span>](upgradedimages-table-patchwiz-dll-.md)



| <span data-ttu-id="dd183-150">Atualizado</span><span class="sxs-lookup"><span data-stu-id="dd183-150">Upgraded</span></span>   | <span data-ttu-id="dd183-151">MsiPath</span><span class="sxs-lookup"><span data-stu-id="dd183-151">MsiPath</span></span>                                           | <span data-ttu-id="dd183-152">PatchMsiPath</span><span class="sxs-lookup"><span data-stu-id="dd183-152">PatchMsiPath</span></span> | <span data-ttu-id="dd183-153">SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="dd183-153">SymbolPaths</span></span> | <span data-ttu-id="dd183-154">Família</span><span class="sxs-lookup"><span data-stu-id="dd183-154">Family</span></span>  |
|------------|---------------------------------------------------|--------------|-------------|---------|
| <span data-ttu-id="dd183-155">MNP \_ fixo</span><span class="sxs-lookup"><span data-stu-id="dd183-155">MNP\_fixed</span></span> | <span data-ttu-id="dd183-156">C: \\ Observação \_ patch do instalador \\ \\ atualizado \\MNP2000.msi</span><span class="sxs-lookup"><span data-stu-id="dd183-156">C:\\Note\_Installer\\Patch\\Upgraded\\MNP2000.msi</span></span> |              |             | <span data-ttu-id="dd183-157">MNPapps</span><span class="sxs-lookup"><span data-stu-id="dd183-157">MNPapps</span></span> |



 

<span data-ttu-id="dd183-158">Insira os dados a seguir na tabela TargetImages de MNP2000. PCP.</span><span class="sxs-lookup"><span data-stu-id="dd183-158">Enter the following data into the TargetImages table of MNP2000.pcp.</span></span> <span data-ttu-id="dd183-159">A tabela TargetImages contém informações sobre a imagem de destino.</span><span class="sxs-lookup"><span data-stu-id="dd183-159">The TargetImages table contains information about the Target image.</span></span>

[<span data-ttu-id="dd183-160">Tabela TargetImages</span><span class="sxs-lookup"><span data-stu-id="dd183-160">TargetImages Table</span></span>](targetimages-table-patchwiz-dll-.md)



| <span data-ttu-id="dd183-161">Destino</span><span class="sxs-lookup"><span data-stu-id="dd183-161">Target</span></span>     | <span data-ttu-id="dd183-162">MsiPath</span><span class="sxs-lookup"><span data-stu-id="dd183-162">MsiPath</span></span>                                         | <span data-ttu-id="dd183-163">SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="dd183-163">SymbolPaths</span></span> | <span data-ttu-id="dd183-164">Atualizado</span><span class="sxs-lookup"><span data-stu-id="dd183-164">Upgraded</span></span>   | <span data-ttu-id="dd183-165">Ordem</span><span class="sxs-lookup"><span data-stu-id="dd183-165">Order</span></span> | <span data-ttu-id="dd183-166">ProductValidateFlags</span><span class="sxs-lookup"><span data-stu-id="dd183-166">ProductValidateFlags</span></span> | <span data-ttu-id="dd183-167">IgnoreMissingSrcFiles</span><span class="sxs-lookup"><span data-stu-id="dd183-167">IgnoreMissingSrcFiles</span></span> |
|------------|-------------------------------------------------|-------------|------------|-------|----------------------|-----------------------|
| <span data-ttu-id="dd183-168">Erro de MNP \_</span><span class="sxs-lookup"><span data-stu-id="dd183-168">MNP\_error</span></span> | <span data-ttu-id="dd183-169">C: \\ Observação \_ destino do patch do instalador \\ \\ \\MNP2000.msi</span><span class="sxs-lookup"><span data-stu-id="dd183-169">C:\\Note\_Installer\\Patch\\Target\\MNP2000.msi</span></span> |             | <span data-ttu-id="dd183-170">MNP \_ fixo</span><span class="sxs-lookup"><span data-stu-id="dd183-170">MNP\_fixed</span></span> | <span data-ttu-id="dd183-171">1</span><span class="sxs-lookup"><span data-stu-id="dd183-171">1</span></span>     |                      | <span data-ttu-id="dd183-172">0</span><span class="sxs-lookup"><span data-stu-id="dd183-172">0</span></span>                     |



 

<span data-ttu-id="dd183-173">Para o pacote de patch de exemplo, deixe as tabelas a seguir em MNP2000. PCP em branco.</span><span class="sxs-lookup"><span data-stu-id="dd183-173">For the sample patch package, leave the following tables in MNP2000.pcp blank.</span></span>

[<span data-ttu-id="dd183-174">\_Tabela UpgradedFiles OptionalData</span><span class="sxs-lookup"><span data-stu-id="dd183-174">UpgradedFiles\_OptionalData Table</span></span>](upgradedfiles-optionaldata-table-patchwiz-dll-.md)

[<span data-ttu-id="dd183-175">Tabela FamilyFileRanges</span><span class="sxs-lookup"><span data-stu-id="dd183-175">FamilyFileRanges Table</span></span>](familyfileranges-table-patchwiz-dll-.md)

[<span data-ttu-id="dd183-176">\_Tabela TargetFiles OptionalData</span><span class="sxs-lookup"><span data-stu-id="dd183-176">TargetFiles\_OptionalData Table</span></span>](targetfiles-optionaldata-table-patchwiz-dll-.md)

[<span data-ttu-id="dd183-177">Tabela ExternalFiles</span><span class="sxs-lookup"><span data-stu-id="dd183-177">ExternalFiles Table</span></span>](externalfiles-table-patchwiz-dll-.md)

[<span data-ttu-id="dd183-178">Tabela UpgradedFilesToIgnore</span><span class="sxs-lookup"><span data-stu-id="dd183-178">UpgradedFilesToIgnore Table</span></span>](upgradedfilestoignore-table-patchwiz-dll-.md)

[<span data-ttu-id="dd183-179">Continuar</span><span class="sxs-lookup"><span data-stu-id="dd183-179">Continue</span></span>](generating-a-patch-package.md)

 

 




---
description: Para gerar um pacote de patch, é recomendável que você use uma ferramenta de criação de patch, como Msimsp.exe e Patchwiz.dll.
ms.assetid: aca3bbd2-440a-405f-bddc-5f9cc831b811
title: Patchwiz.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6dc1135a9e2c09bb8a96e041f77bae39f0057ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172009"
---
# <a name="patchwizdll"></a><span data-ttu-id="f5e26-103">Patchwiz.dll</span><span class="sxs-lookup"><span data-stu-id="f5e26-103">Patchwiz.dll</span></span>

<span data-ttu-id="f5e26-104">Para gerar um pacote de patch, é recomendável que você use uma ferramenta de criação de patch, como [Msimsp.exe](msimsp-exe.md) e Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="f5e26-104">To generate a patch package, it is recommended that you use a patch creation tool such as [Msimsp.exe](msimsp-exe.md) and Patchwiz.dll.</span></span> <span data-ttu-id="f5e26-105">Patchwiz.dll versão 4,0 é compatível com pacotes e patches que foram criados usando versões anteriores do Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="f5e26-105">Patchwiz.dll version 4.0 is compatible with packages and patches that were authored using earlier versions of the Patchwiz.dll.</span></span> <span data-ttu-id="f5e26-106">A ferramenta de Patchwiz.dll só está disponível nos [componentes SDK do Windows para desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="f5e26-106">The Patchwiz.dll tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="f5e26-107">Patchwiz.dll versão 4,0 tem uma nova função, [UiCreatePatchPackageEx (Patchwiz.dll)](uicreatepatchpackageex--patchwiz-dll-.md), que estende a funcionalidade de [UiCreatePatchPackage (Patchwiz.dll)](uicreatepatchpackage-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="f5e26-107">Patchwiz.dll version 4.0 has one new function, [UiCreatePatchPackageEx (Patchwiz.dll)](uicreatepatchpackageex--patchwiz-dll-.md), that extends the functionality of [UiCreatePatchPackage (Patchwiz.dll)](uicreatepatchpackage-patchwiz-dll-.md).</span></span> <span data-ttu-id="f5e26-108">Essas funções usam um arquivo de propriedades de criação de patch (arquivo. PCP) e geram um [pacote de patch](patch-packages.md)do instalador.</span><span class="sxs-lookup"><span data-stu-id="f5e26-108">These functions take a patch creation properties file (.pcp file) and generate an installer [Patch Package](patch-packages.md).</span></span>

<span data-ttu-id="f5e26-109">O arquivo. PCP é um arquivo de banco de dados binário com o mesmo formato que um banco de dados Windows Installer (arquivo. msi), mas com um esquema de banco de dados diferente.</span><span class="sxs-lookup"><span data-stu-id="f5e26-109">The .pcp file is a binary database file with the same format as a Windows Installer database (.msi file), but with a different database schema.</span></span> <span data-ttu-id="f5e26-110">Portanto, um arquivo. PCP pode ser criado usando as mesmas ferramentas usadas para um banco de dados do instalador.</span><span class="sxs-lookup"><span data-stu-id="f5e26-110">Therefore a .pcp file can be authored by using the same tools used for an installer database.</span></span>

<span data-ttu-id="f5e26-111">Você pode criar um arquivo. PCP usando um editor de tabela, como [Orca.exe](orca-exe.md) para inserir informações no banco de dados. PCP em branco fornecido com o SDK do Windows Installer, template. PCP.</span><span class="sxs-lookup"><span data-stu-id="f5e26-111">You can create a .pcp file by using a table editor such as [Orca.exe](orca-exe.md) to enter information into the blank .pcp database provided with the Windows Installer SDK, Template.pcp.</span></span> <span data-ttu-id="f5e26-112">Para obter mais informações, consulte [um exemplo de aplicação de patch de atualização pequena](a-small-update-patching-example.md).</span><span class="sxs-lookup"><span data-stu-id="f5e26-112">For more information, see [A Small Update Patching Example](a-small-update-patching-example.md).</span></span>

<span data-ttu-id="f5e26-113">As tabelas de banco de dados a seguir são necessárias em todos os arquivos. PCP:</span><span class="sxs-lookup"><span data-stu-id="f5e26-113">The following database tables are required in every .pcp file:</span></span>

-   [<span data-ttu-id="f5e26-114">Tabela de Propriedades (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="f5e26-114">Properties Table (Patchwiz.dll)</span></span>](properties-table-patchwiz-dll-.md)
-   [<span data-ttu-id="f5e26-115">Tabela ImageFamilies (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="f5e26-115">ImageFamilies Table (Patchwiz.dll)</span></span>](imagefamilies-table-patchwiz-dll-.md)
-   [<span data-ttu-id="f5e26-116">Tabela UpgradedImages (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="f5e26-116">UpgradedImages Table (Patchwiz.dll)</span></span>](upgradedimages-table-patchwiz-dll-.md)
-   [<span data-ttu-id="f5e26-117">Tabela TargetImages (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="f5e26-117">TargetImages Table (Patchwiz.dll)</span></span>](targetimages-table-patchwiz-dll-.md)

<span data-ttu-id="f5e26-118">As seguintes tabelas de banco de dados são opcionais:</span><span class="sxs-lookup"><span data-stu-id="f5e26-118">The following database tables are optional:</span></span>

-   [<span data-ttu-id="f5e26-119">\_Tabela UpgradedFiles OptionalData (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="f5e26-119">UpgradedFiles\_OptionalData Table (Patchwiz.dll)</span></span>](upgradedfiles-optionaldata-table-patchwiz-dll-.md)
-   [<span data-ttu-id="f5e26-120">Tabela FamilyFileRanges (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="f5e26-120">FamilyFileRanges Table (Patchwiz.dll)</span></span>](familyfileranges-table-patchwiz-dll-.md)
-   [<span data-ttu-id="f5e26-121">\_Tabela TargetFiles OptionalData (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="f5e26-121">TargetFiles\_OptionalData Table (Patchwiz.dll)</span></span>](targetfiles-optionaldata-table-patchwiz-dll-.md)
-   [<span data-ttu-id="f5e26-122">Tabela ExternalFiles (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="f5e26-122">ExternalFiles Table (Patchwiz.dll)</span></span>](externalfiles-table-patchwiz-dll-.md)
-   [<span data-ttu-id="f5e26-123">Tabela UpgradedFilesToIgnore (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="f5e26-123">UpgradedFilesToIgnore Table (Patchwiz.dll)</span></span>](upgradedfilestoignore-table-patchwiz-dll-.md)

<span data-ttu-id="f5e26-124">A tabela a seguir é necessária em arquivos. PCP que têm um MinimumRequiredMsiVersion igual a 300 na tabela de [Propriedades](properties-table-patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="f5e26-124">The following table is required in .pcp files that have a MinimumRequiredMsiVersion equal to 300 in the [Properties](properties-table-patchwiz-dll-.md) table.</span></span>

-   [<span data-ttu-id="f5e26-125">Tabela PatchMetadata (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="f5e26-125">PatchMetadata Table (Patchwiz.dll)</span></span>](patchmetadata-table--patchwiz-dll-.md)

> [!Note]  
> <span data-ttu-id="f5e26-126">A tabela será opcional se MinimumRequiredMsiVersion não for igual a 300.</span><span class="sxs-lookup"><span data-stu-id="f5e26-126">The table is optional if MinimumRequiredMsiVersion is not equal to 300.</span></span>

 

<span data-ttu-id="f5e26-127">A versão do Patchwiz.dll lançada com Windows Installer 3,0 pode gerar automaticamente informações de sequenciamento de patch e adicioná-las à [tabela MsiPatchSequence](msipatchsequence-table.md) de um novo patch.</span><span class="sxs-lookup"><span data-stu-id="f5e26-127">The version of Patchwiz.dll released with Windows Installer 3.0 can automatically generate patch sequencing information and add it to the [MsiPatchSequence Table](msipatchsequence-table.md) of a new patch.</span></span> <span data-ttu-id="f5e26-128">A [tabela PatchSequence](patchsequence-table--patchwiz-dll-.md) pode ser usada para adicionar manualmente informações de sequenciamento de patch à tabela MsiPatchSequence.</span><span class="sxs-lookup"><span data-stu-id="f5e26-128">The [PatchSequence Table](patchsequence-table--patchwiz-dll-.md) can be used to manually add patch sequencing information the MsiPatchSequence Table.</span></span> <span data-ttu-id="f5e26-129">Para obter mais informações, consulte [gerando informações de sequência de patch](generating-patch-sequence-information---patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="f5e26-129">For more information, see [Generating Patch Sequence Information](generating-patch-sequence-information---patchwiz-dll-.md).</span></span>

<span data-ttu-id="f5e26-130">A partir do Patchwiz.dll versão 2,0, você pode aumentar a velocidade da criação de patch subsequente usando o [cache de informações de patch (Patchwiz.dll)](patch-information-caching-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="f5e26-130">Beginning with Patchwiz.dll version 2.0, you can increase the speed of subsequent patch creation by using [Patch Information Caching (Patchwiz.dll)](patch-information-caching-patchwiz-dll-.md).</span></span>

<span data-ttu-id="f5e26-131">Usar símbolos públicos para seus binários de imagem de destino e de atualização pode reduzir tamanhos de patch binários por aproximadamente uma metade.</span><span class="sxs-lookup"><span data-stu-id="f5e26-131">Using public symbols for your target and upgrade image binaries can reduce binary patch sizes by approximately one half.</span></span> <span data-ttu-id="f5e26-132">Para obter mais informações, consulte [usando símbolos para reduzir o tamanho do patch binário](using-symbols-to-reduce-binary-patch-size.md).</span><span class="sxs-lookup"><span data-stu-id="f5e26-132">For more information, see [Using Symbols to Reduce Binary Patch Size](using-symbols-to-reduce-binary-patch-size.md).</span></span>

<span data-ttu-id="f5e26-133">É possível especificar que determinadas regiões do arquivo de destino sejam substituídas durante a aplicação de patch e que as informações nessas regiões sejam retidas.</span><span class="sxs-lookup"><span data-stu-id="f5e26-133">You can specify that certain regions of the target file be preserved from being overwritten during patching and that the information in those regions be retained.</span></span> <span data-ttu-id="f5e26-134">Para obter mais informações, consulte [aplicação de patch nas regiões selecionadas de um arquivo](patching-selected-regions-of-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="f5e26-134">For more information, see [Patching Selected Regions of a File](patching-selected-regions-of-a-file.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5e26-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f5e26-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5e26-136">Versões, ferramentas e redistribuíveis liberados</span><span class="sxs-lookup"><span data-stu-id="f5e26-136">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 




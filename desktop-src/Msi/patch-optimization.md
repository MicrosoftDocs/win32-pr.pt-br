---
description: Windows Installer pode otimizar a aplicação de patch para reduzir o tempo necessário para aplicar patches aos aplicativos instalados.
ms.assetid: 2bb1c94a-55b6-4aee-b86d-ee9e1f8ed290
title: Otimização de patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86215855bb02314d7eb54c774541b0a2086c7c99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827869"
---
# <a name="patch-optimization"></a><span data-ttu-id="07816-103">Otimização de patch</span><span class="sxs-lookup"><span data-stu-id="07816-103">Patch Optimization</span></span>

<span data-ttu-id="07816-104">Windows Installer pode otimizar a aplicação de patch para reduzir o tempo necessário para aplicar patches aos aplicativos instalados.</span><span class="sxs-lookup"><span data-stu-id="07816-104">Windows Installer can optimize patching to reduce the time that is required to apply patches to installed applications.</span></span>

<span data-ttu-id="07816-105">**Windows Installer 2,0:** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="07816-105">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="07816-106">Para versões do Windows Installer lançadas antes de Windows Installer 3,0, a aplicação de patches executa uma instalação de reparo completa do aplicativo, o que pode levar muito mais tempo.</span><span class="sxs-lookup"><span data-stu-id="07816-106">For versions of Windows Installer released before Windows Installer 3.0, patching runs a complete repair installation of the application, which can take significantly more time.</span></span>

<span data-ttu-id="07816-107">**Windows Installer 3,0 e posterior:** O processo de aplicação de patches altera apenas as partes de um aplicativo que são modificadas por um patch.</span><span class="sxs-lookup"><span data-stu-id="07816-107">**Windows Installer 3.0 and later:** The patching process only changes the parts of an application that are modified by a patch.</span></span>

<span data-ttu-id="07816-108">**Windows Installer 3,1 e posterior:** A partir do Windows Installer 3,1, a otimização de patch requer que todos os patches na transação tenham a propriedade OptimizedInstallMode definida como 1 (um) na [tabela MsiPatchMetadata](msipatchmetadata-table.md).</span><span class="sxs-lookup"><span data-stu-id="07816-108">**Windows Installer 3.1 and later:** Beginning with Windows Installer 3.1, patch optimization requires that all patches in the transaction have the OptimizedInstallMode property set to 1 (one) in the [MsiPatchMetadata Table](msipatchmetadata-table.md).</span></span>

<span data-ttu-id="07816-109">Se um patch modificar apenas as tabelas a seguir, Windows Installer 3,0 ou posterior ignorará as ações associadas a todas as outras tabelas, mesmo se essas ações estiverem listadas nas tabelas de sequência do pacote de instalação do aplicativo original (arquivo. msi).</span><span class="sxs-lookup"><span data-stu-id="07816-109">If a patch only modifies the following tables, Windows Installer 3.0 or later skips the actions that are associated with all the other tables, even if those actions are listed in the sequence tables of the original application installation package (.msi file).</span></span>

-   [<span data-ttu-id="07816-110">AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="07816-110">AdminExecuteSequence</span></span>](adminexecutesequence-table.md)
-   [<span data-ttu-id="07816-111">AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="07816-111">AdminUISequence</span></span>](adminuisequence-table.md)
-   [<span data-ttu-id="07816-112">Condição</span><span class="sxs-lookup"><span data-stu-id="07816-112">Condition</span></span>](condition-table.md)
-   [<span data-ttu-id="07816-113">CustomAction</span><span class="sxs-lookup"><span data-stu-id="07816-113">CustomAction</span></span>](customaction-table.md)
-   [<span data-ttu-id="07816-114">Arquivo</span><span class="sxs-lookup"><span data-stu-id="07816-114">File</span></span>](file-table.md)
-   [<span data-ttu-id="07816-115">FileSFPCatalog</span><span class="sxs-lookup"><span data-stu-id="07816-115">FileSFPCatalog</span></span>](filesfpcatalog-table.md)
-   [<span data-ttu-id="07816-116">InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="07816-116">InstallExecuteSequence</span></span>](installexecutesequence-table.md)
-   [<span data-ttu-id="07816-117">InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="07816-117">InstallUISequence</span></span>](installuisequence-table.md)
-   [<span data-ttu-id="07816-118">Mídia</span><span class="sxs-lookup"><span data-stu-id="07816-118">Media</span></span>](media-table.md)
-   [<span data-ttu-id="07816-119">MoveFile</span><span class="sxs-lookup"><span data-stu-id="07816-119">MoveFile</span></span>](movefile-table.md)
-   [<span data-ttu-id="07816-120">MsiAssembly</span><span class="sxs-lookup"><span data-stu-id="07816-120">MsiAssembly</span></span>](msiassembly-table.md)
-   [<span data-ttu-id="07816-121">MsiDigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="07816-121">MsiDigitalCertificate</span></span>](msidigitalcertificate-table.md)
-   [<span data-ttu-id="07816-122">MsiDigitalSignature</span><span class="sxs-lookup"><span data-stu-id="07816-122">MsiDigitalSignature</span></span>](msidigitalsignature-table.md)
-   [<span data-ttu-id="07816-123">MsiFileHash</span><span class="sxs-lookup"><span data-stu-id="07816-123">MsiFileHash</span></span>](msifilehash-table.md)
-   [<span data-ttu-id="07816-124">MsiPatchHeaders</span><span class="sxs-lookup"><span data-stu-id="07816-124">MsiPatchHeaders</span></span>](msipatchheaders-table.md)
-   [<span data-ttu-id="07816-125">Patch</span><span class="sxs-lookup"><span data-stu-id="07816-125">Patch</span></span>](patch-table.md)
-   [<span data-ttu-id="07816-126">PatchPackage</span><span class="sxs-lookup"><span data-stu-id="07816-126">PatchPackage</span></span>](patchpackage-table.md)
-   [<span data-ttu-id="07816-127">Propriedade</span><span class="sxs-lookup"><span data-stu-id="07816-127">Property</span></span>](property-table.md)
-   [<span data-ttu-id="07816-128">Registro</span><span class="sxs-lookup"><span data-stu-id="07816-128">Registry</span></span>](registry-table.md)
-   [<span data-ttu-id="07816-129">SFPCatalog</span><span class="sxs-lookup"><span data-stu-id="07816-129">SFPCatalog</span></span>](sfpcatalog-table.md)
-   [<span data-ttu-id="07816-130">Importação</span><span class="sxs-lookup"><span data-stu-id="07816-130">TypeLib</span></span>](typelib-table.md)
-   [<span data-ttu-id="07816-131">\_Columns</span><span class="sxs-lookup"><span data-stu-id="07816-131">\_Columns</span></span>](-columns-table.md)
-   [<span data-ttu-id="07816-132">\_Armazenamentos</span><span class="sxs-lookup"><span data-stu-id="07816-132">\_Storages</span></span>](-storages-table.md)
-   [<span data-ttu-id="07816-133">\_Fluxos</span><span class="sxs-lookup"><span data-stu-id="07816-133">\_Streams</span></span>](-streams-table.md)
-   [<span data-ttu-id="07816-134">\_Tabelas</span><span class="sxs-lookup"><span data-stu-id="07816-134">\_Tables</span></span>](-tables-table.md)
-   [<span data-ttu-id="07816-135">\_Tabela de transformview</span><span class="sxs-lookup"><span data-stu-id="07816-135">\_TransformView Table</span></span>](-transformview-table.md)
-   [<span data-ttu-id="07816-136">\_Validação</span><span class="sxs-lookup"><span data-stu-id="07816-136">\_Validation</span></span>](-validation-table.md)

<span data-ttu-id="07816-137">Para desativar a opção de otimização de patch, use a política [DisableFlyWeightPatching](disableflyweightpatching.md) .</span><span class="sxs-lookup"><span data-stu-id="07816-137">To turn off the patch optimization option, use the [DisableFlyWeightPatching](disableflyweightpatching.md) policy.</span></span>

 

 




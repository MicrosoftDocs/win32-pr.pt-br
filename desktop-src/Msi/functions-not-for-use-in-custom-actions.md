---
description: As funções de banco de dados a seguir nunca devem ser chamadas de uma ação personalizada.
ms.assetid: 55fdd82b-9f34-4c2c-a837-8a09f21f568a
title: Funções não para uso em ações personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c77c4714ca65614200cf77d6b207b6eebcaf179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769320"
---
# <a name="functions-not-for-use-in-custom-actions"></a><span data-ttu-id="3aad0-103">Funções não para uso em ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="3aad0-103">Functions Not for Use in Custom Actions</span></span>

<span data-ttu-id="3aad0-104">As [funções de banco de dados](database-functions.md) a seguir nunca devem ser chamadas de uma ação personalizada.</span><span class="sxs-lookup"><span data-stu-id="3aad0-104">The following [Database Functions](database-functions.md) must never be called from a custom action.</span></span>

-   [<span data-ttu-id="3aad0-105">**MsiConfigureProduct**</span><span class="sxs-lookup"><span data-stu-id="3aad0-105">**MsiConfigureProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
-   [<span data-ttu-id="3aad0-106">**MsiConfigureProductEx**</span><span class="sxs-lookup"><span data-stu-id="3aad0-106">**MsiConfigureProductEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)
-   [<span data-ttu-id="3aad0-107">**MsiCreateTransformSummaryInfo**</span><span class="sxs-lookup"><span data-stu-id="3aad0-107">**MsiCreateTransformSummaryInfo**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)
-   [<span data-ttu-id="3aad0-108">**MsiDatabaseApplyTransform**</span><span class="sxs-lookup"><span data-stu-id="3aad0-108">**MsiDatabaseApplyTransform**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)
-   [<span data-ttu-id="3aad0-109">**MsiDatabaseCommit**</span><span class="sxs-lookup"><span data-stu-id="3aad0-109">**MsiDatabaseCommit**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)
-   [<span data-ttu-id="3aad0-110">**MsiDatabaseExport**</span><span class="sxs-lookup"><span data-stu-id="3aad0-110">**MsiDatabaseExport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)
-   [<span data-ttu-id="3aad0-111">**MsiDatabaseGenerateTransform**</span><span class="sxs-lookup"><span data-stu-id="3aad0-111">**MsiDatabaseGenerateTransform**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)
-   [<span data-ttu-id="3aad0-112">**MsiDatabaseImport**</span><span class="sxs-lookup"><span data-stu-id="3aad0-112">**MsiDatabaseImport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)
-   [<span data-ttu-id="3aad0-113">**MsiDatabaseMerge**</span><span class="sxs-lookup"><span data-stu-id="3aad0-113">**MsiDatabaseMerge**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)
-   [<span data-ttu-id="3aad0-114">**MsiEnableLog**</span><span class="sxs-lookup"><span data-stu-id="3aad0-114">**MsiEnableLog**</span></span>](/windows/desktop/api/Msi/nf-msi-msienableloga)
-   [<span data-ttu-id="3aad0-115">**MsiEnableUIPreview**</span><span class="sxs-lookup"><span data-stu-id="3aad0-115">**MsiEnableUIPreview**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)
-   [<span data-ttu-id="3aad0-116">**MsiGetDatabaseState**</span><span class="sxs-lookup"><span data-stu-id="3aad0-116">**MsiGetDatabaseState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)
-   [<span data-ttu-id="3aad0-117">**MsiOpenDatabase**</span><span class="sxs-lookup"><span data-stu-id="3aad0-117">**MsiOpenDatabase**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea)
-   [<span data-ttu-id="3aad0-118">**MsiPreviewBillboard**</span><span class="sxs-lookup"><span data-stu-id="3aad0-118">**MsiPreviewBillboard**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda)
-   [<span data-ttu-id="3aad0-119">**MsiPreviewDialog**</span><span class="sxs-lookup"><span data-stu-id="3aad0-119">**MsiPreviewDialog**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga)
-   [<span data-ttu-id="3aad0-120">**MsiReinstallProduct**</span><span class="sxs-lookup"><span data-stu-id="3aad0-120">**MsiReinstallProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)
-   [<span data-ttu-id="3aad0-121">**MsiSetExternalUI**</span><span class="sxs-lookup"><span data-stu-id="3aad0-121">**MsiSetExternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
-   [<span data-ttu-id="3aad0-122">**MsiSetExternalUIRecord**</span><span class="sxs-lookup"><span data-stu-id="3aad0-122">**MsiSetExternalUIRecord**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord)
-   [<span data-ttu-id="3aad0-123">**MsiSetInternalUI**</span><span class="sxs-lookup"><span data-stu-id="3aad0-123">**MsiSetInternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

<span data-ttu-id="3aad0-124">As [funções do instalador](installer-function-reference.md) a seguir nunca devem ser chamadas de uma ação personalizada.</span><span class="sxs-lookup"><span data-stu-id="3aad0-124">The following [Installer Functions](installer-function-reference.md) must never be called from a custom action.</span></span>

-   [<span data-ttu-id="3aad0-125">**MsiApplyPatch**</span><span class="sxs-lookup"><span data-stu-id="3aad0-125">**MsiApplyPatch**</span></span>](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
-   [<span data-ttu-id="3aad0-126">**MsiCollectUserInfo**</span><span class="sxs-lookup"><span data-stu-id="3aad0-126">**MsiCollectUserInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa)
-   [<span data-ttu-id="3aad0-127">**MsiConfigureFeature**</span><span class="sxs-lookup"><span data-stu-id="3aad0-127">**MsiConfigureFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)
-   [<span data-ttu-id="3aad0-128">**MsiConfigureProduct**</span><span class="sxs-lookup"><span data-stu-id="3aad0-128">**MsiConfigureProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
-   [<span data-ttu-id="3aad0-129">**MsiConfigureProductEx**</span><span class="sxs-lookup"><span data-stu-id="3aad0-129">**MsiConfigureProductEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)
-   [<span data-ttu-id="3aad0-130">**MsiEnableLog**</span><span class="sxs-lookup"><span data-stu-id="3aad0-130">**MsiEnableLog**</span></span>](/windows/desktop/api/Msi/nf-msi-msienableloga)
-   [<span data-ttu-id="3aad0-131">**MsiGetFeatureInfo**</span><span class="sxs-lookup"><span data-stu-id="3aad0-131">**MsiGetFeatureInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa)
-   [<span data-ttu-id="3aad0-132">**MsiGetProductCode**</span><span class="sxs-lookup"><span data-stu-id="3aad0-132">**MsiGetProductCode**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetproductcodea)
-   [<span data-ttu-id="3aad0-133">**MsiGetProductProperty**</span><span class="sxs-lookup"><span data-stu-id="3aad0-133">**MsiGetProductProperty**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya)
-   [<span data-ttu-id="3aad0-134">**MsiInstallMissingComponent**</span><span class="sxs-lookup"><span data-stu-id="3aad0-134">**MsiInstallMissingComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta)
-   [<span data-ttu-id="3aad0-135">**MsiInstallMissingFile**</span><span class="sxs-lookup"><span data-stu-id="3aad0-135">**MsiInstallMissingFile**</span></span>](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)
-   [<span data-ttu-id="3aad0-136">**MsiInstallProduct**</span><span class="sxs-lookup"><span data-stu-id="3aad0-136">**MsiInstallProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)
-   [<span data-ttu-id="3aad0-137">**MsiOpenPackage**</span><span class="sxs-lookup"><span data-stu-id="3aad0-137">**MsiOpenPackage**</span></span>](/windows/desktop/api/Msi/nf-msi-msiopenpackagea)
-   [<span data-ttu-id="3aad0-138">**MsiOpenProduct**</span><span class="sxs-lookup"><span data-stu-id="3aad0-138">**MsiOpenProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiopenproducta)
-   [<span data-ttu-id="3aad0-139">**MsiReinstallFeature**</span><span class="sxs-lookup"><span data-stu-id="3aad0-139">**MsiReinstallFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)
-   [<span data-ttu-id="3aad0-140">**MsiReinstallProduct**</span><span class="sxs-lookup"><span data-stu-id="3aad0-140">**MsiReinstallProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)
-   [<span data-ttu-id="3aad0-141">**MsiSetExternalUI**</span><span class="sxs-lookup"><span data-stu-id="3aad0-141">**MsiSetExternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
-   [<span data-ttu-id="3aad0-142">**MsiSetInternalUI**</span><span class="sxs-lookup"><span data-stu-id="3aad0-142">**MsiSetInternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetinternalui)
-   [<span data-ttu-id="3aad0-143">**MsiUseFeature**</span><span class="sxs-lookup"><span data-stu-id="3aad0-143">**MsiUseFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msiusefeaturea)
-   [<span data-ttu-id="3aad0-144">**MsiUseFeatureEx**</span><span class="sxs-lookup"><span data-stu-id="3aad0-144">**MsiUseFeatureEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiusefeatureexa)
-   [<span data-ttu-id="3aad0-145">**MsiVerifyPackage**</span><span class="sxs-lookup"><span data-stu-id="3aad0-145">**MsiVerifyPackage**</span></span>](/windows/desktop/api/Msi/nf-msi-msiverifypackagea)

<span data-ttu-id="3aad0-146">As [funções do instalador](installer-function-reference.md) a seguir nunca devem ser chamadas de uma ação personalizada se isso iniciar outra instalação.</span><span class="sxs-lookup"><span data-stu-id="3aad0-146">The following [Installer Functions](installer-function-reference.md) must never be called from a custom action if doing so starts another installation.</span></span> <span data-ttu-id="3aad0-147">Eles podem ser chamados de uma ação personalizada que não inicia outra instalação.</span><span class="sxs-lookup"><span data-stu-id="3aad0-147">They may be called from a custom action that does not start another installation.</span></span>

-   [<span data-ttu-id="3aad0-148">**MsiProvideComponent**</span><span class="sxs-lookup"><span data-stu-id="3aad0-148">**MsiProvideComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)
-   [<span data-ttu-id="3aad0-149">**MsiProvideQualifiedComponent**</span><span class="sxs-lookup"><span data-stu-id="3aad0-149">**MsiProvideQualifiedComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)
-   [<span data-ttu-id="3aad0-150">**MsiProvideQualifiedComponentEx**</span><span class="sxs-lookup"><span data-stu-id="3aad0-150">**MsiProvideQualifiedComponentEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa)

<span data-ttu-id="3aad0-151">Uma ação personalizada nunca deve gerar um novo thread que usa funções Windows Installer para alterar o estado do recurso, o estado do componente ou para enviar mensagens de um evento de controle.</span><span class="sxs-lookup"><span data-stu-id="3aad0-151">A custom action should never spawn a new thread that uses Windows Installer functions to change the feature state, component state, or to send messages from a Control Event.</span></span> <span data-ttu-id="3aad0-152">A tentativa de fazer isso faz com que a instalação falhe.</span><span class="sxs-lookup"><span data-stu-id="3aad0-152">Attempting to do this causes the installation to fail.</span></span>

 

 




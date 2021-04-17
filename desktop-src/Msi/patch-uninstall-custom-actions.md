---
description: Você pode usar a opção de desinstalação do patch de ação personalizada para especificar que o instalador execute a ação personalizada somente quando um patch for desinstalado.
ms.assetid: c741aa40-ba4c-459e-936a-19c002620c30
title: Corrigir ações personalizadas de desinstalação de patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90cfffbdb37f1f2fab046b794010a790e9a5212
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783267"
---
# <a name="patch-uninstall-custom-actions"></a><span data-ttu-id="e35f2-103">Corrigir ações personalizadas de desinstalação de patch</span><span class="sxs-lookup"><span data-stu-id="e35f2-103">Patch Uninstall Custom Actions</span></span>

<span data-ttu-id="e35f2-104">Você pode usar a [opção de desinstalação do patch de ação personalizada](custom-action-patch-uninstall-option.md) para especificar que o instalador execute a ação personalizada somente quando um patch for desinstalado.</span><span class="sxs-lookup"><span data-stu-id="e35f2-104">You can use the [Custom Action Patch Uninstall option](custom-action-patch-uninstall-option.md) to specify that the installer run the custom action only when a patch is uninstalled.</span></span>

<span data-ttu-id="e35f2-105">**Windows Installer 4,5 e posterior:** Você pode usar a [opção de desinstalação de patch de ação personalizada](custom-action-patch-uninstall-option.md) para especificar que o instalador só executa a ação personalizada quando um patch é desinstalado.</span><span class="sxs-lookup"><span data-stu-id="e35f2-105">**Windows Installer 4.5 and later:** You can use the [Custom Action Patch Uninstall Option](custom-action-patch-uninstall-option.md) to specify that the installer only run the custom action when a patch is uninstalled.</span></span>

<span data-ttu-id="e35f2-106">\*\*[Windows Installer 4,0 e anteriores](not-supported-in-windows-installer-4-0.md): \* \*</span><span class="sxs-lookup"><span data-stu-id="e35f2-106">\*\*[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):  \*\*</span></span>

<span data-ttu-id="e35f2-107">A [opção de desinstalação de patch de ação personalizada](custom-action-patch-uninstall-option.md) não está disponível.</span><span class="sxs-lookup"><span data-stu-id="e35f2-107">The [Custom Action Patch Uninstall option](custom-action-patch-uninstall-option.md) is not available.</span></span> <span data-ttu-id="e35f2-108">Não há nenhum método para marcar uma [ação personalizada](custom-actions.md) em um pacote de patch a ser executado quando o patch é desinstalado porque o instalador não aplica os pacotes de patch que estão sendo desinstalados.</span><span class="sxs-lookup"><span data-stu-id="e35f2-108">There is no method for marking a [custom action](custom-actions.md) within a patch package to be run when the patch is uninstalled because the installer does not apply the patch packages being uninstalled.</span></span>

<span data-ttu-id="e35f2-109">Para que uma [ação personalizada](custom-actions.md) seja executada quando um patch específico é desinstalado, a ação personalizada deve estar presente no aplicativo original ou estar em um patch para o produto que sempre é aplicado.</span><span class="sxs-lookup"><span data-stu-id="e35f2-109">To have a [custom action](custom-actions.md) run when a particular patch is uninstalled, the custom action must either be present in the original application or be in a patch for the product that is always applied.</span></span>

<span data-ttu-id="e35f2-110">Os desenvolvedores podem usar a propriedade [**MsiPatchRemovalList**](msipatchremovallist.md) para criar um pacote Windows Installer ou patch que executa [ações personalizadas](custom-actions.md) sobre a remoção de um patch.</span><span class="sxs-lookup"><span data-stu-id="e35f2-110">Developers can use the [**MsiPatchRemovalList**](msipatchremovallist.md) property to author a Windows Installer package or patch that performs [custom actions](custom-actions.md) on the removal of a patch.</span></span> <span data-ttu-id="e35f2-111">A ação personalizada pode ser criada no pacote de instalação original, um patch que já foi aplicado ao pacote ou um patch que não é um [patch desinstalável](uninstallable-patches.md).</span><span class="sxs-lookup"><span data-stu-id="e35f2-111">The custom action can be authored into the original installation package, a patch that has already been applied to the package, or a patch that is not an [uninstallable patch](uninstallable-patches.md).</span></span> <span data-ttu-id="e35f2-112">A ação personalizada pode ser condicional na propriedade **MsiPatchRemovalList** nas tabelas de sequência.</span><span class="sxs-lookup"><span data-stu-id="e35f2-112">The custom action can be conditionalized on the **MsiPatchRemovalList** property in the sequence tables.</span></span> <span data-ttu-id="e35f2-113">Consulte [usando propriedades em instruções condicionais](using-properties-in-conditional-statements.md) para obter mais informações sobre a condicionalização de ações.</span><span class="sxs-lookup"><span data-stu-id="e35f2-113">See [Using Properties in Conditional Statements](using-properties-in-conditional-statements.md) for more information about conditionalizing actions.</span></span>

<span data-ttu-id="e35f2-114">A ação personalizada pode obter os GUIDs dos patches que estão sendo removidos do valor da propriedade [**MsiPatchRemovalList**](msipatchremovallist.md) .</span><span class="sxs-lookup"><span data-stu-id="e35f2-114">The custom action can obtain the GUIDs of patches being removed from the value of the [**MsiPatchRemovalList**](msipatchremovallist.md) property.</span></span> <span data-ttu-id="e35f2-115">A ação personalizada pode determinar se o estado de instalação do patch é aplicado, obsoleto ou substituído chamando o [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) ou a propriedade [**patchproperty**](patch-patchproperty.md) do [objeto patch](patch-object.md).</span><span class="sxs-lookup"><span data-stu-id="e35f2-115">The custom action can determine whether the installation state of the patch is applied, obsolete, or superseded by calling the [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) or the [**PatchProperty**](patch-patchproperty.md) property of the [Patch object](patch-object.md).</span></span>

<span data-ttu-id="e35f2-116">Se a ação personalizada exigir metadados especiais do patch, o patch deverá conter uma ação personalizada que grava os metadados em um registro ou local de arquivo quando o patch é aplicado.</span><span class="sxs-lookup"><span data-stu-id="e35f2-116">If the custom action requires special metadata from the patch, the patch should contain a custom action that writes the metadata to a registry or file location when the patch is applied.</span></span> <span data-ttu-id="e35f2-117">A ação personalizada no aplicativo original ou um patch sempre aplicado pode obter as informações necessárias para remover as alterações do patch.</span><span class="sxs-lookup"><span data-stu-id="e35f2-117">The custom action in the original application or a patch that is always applied can obtain the information needed to remove the patch's changes.</span></span>

<span data-ttu-id="e35f2-118">Patches que fazem dificuldade de desfazer corretamente não devem ser marcados como [patches desinstaláveis](uninstallable-patches.md).</span><span class="sxs-lookup"><span data-stu-id="e35f2-118">Patches making changes that are difficult to undo correctly should not be marked as [uninstallable patches](uninstallable-patches.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e35f2-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e35f2-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e35f2-120">Sequenciamento de patch</span><span class="sxs-lookup"><span data-stu-id="e35f2-120">Patch Sequencing</span></span>](sequencing-patches.md)
</dt> <dt>

[<span data-ttu-id="e35f2-121">Removendo patches</span><span class="sxs-lookup"><span data-stu-id="e35f2-121">Removing Patches</span></span>](removing-patches.md)
</dt> <dt>

[<span data-ttu-id="e35f2-122">Patches desinstaláveis</span><span class="sxs-lookup"><span data-stu-id="e35f2-122">Uninstallable Patches</span></span>](uninstallable-patches.md)
</dt> <dt>

[<span data-ttu-id="e35f2-123">Desinstalando patches</span><span class="sxs-lookup"><span data-stu-id="e35f2-123">Uninstalling Patches</span></span>](uninstalling-patches.md)
</dt> <dt>

[<span data-ttu-id="e35f2-124">**MSIPATCHREMOVE**</span><span class="sxs-lookup"><span data-stu-id="e35f2-124">**MSIPATCHREMOVE**</span></span>](msipatchremove.md)
</dt> <dt>

[<span data-ttu-id="e35f2-125">**MsiEnumapplicationsEx**</span><span class="sxs-lookup"><span data-stu-id="e35f2-125">**MsiEnumapplicationsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[<span data-ttu-id="e35f2-126">**MsiGetPatchInfoEx**</span><span class="sxs-lookup"><span data-stu-id="e35f2-126">**MsiGetPatchInfoEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[<span data-ttu-id="e35f2-127">**MsiRemovePatches**</span><span class="sxs-lookup"><span data-stu-id="e35f2-127">**MsiRemovePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 




---
description: Use o sinalizador de opção a seguir para especificar que o instalador execute a ação personalizada somente quando um patch estiver sendo desinstalado. Para definir a opção, adicione o valor nessa tabela ao valor no campo Extended da tabela CustomAction.
ms.assetid: aa4d9e21-5316-42b5-a22e-c7a5becd3cae
title: Opção de desinstalação de patch de ação personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108365876393733f7cc520ae565bb2c5ea7ff3df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752660"
---
# <a name="custom-action-patch-uninstall-option"></a><span data-ttu-id="8b404-104">Opção de desinstalação de patch de ação personalizada</span><span class="sxs-lookup"><span data-stu-id="8b404-104">Custom Action Patch Uninstall Option</span></span>

<span data-ttu-id="8b404-105">Use o sinalizador de opção a seguir para especificar que o instalador execute a ação personalizada somente quando um patch estiver sendo desinstalado.</span><span class="sxs-lookup"><span data-stu-id="8b404-105">Use the following option flag to specify that the installer run the custom action only when a patch is being uninstalled.</span></span> <span data-ttu-id="8b404-106">Para definir a opção, adicione o valor nessa tabela ao valor no campo Extended da [tabela CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="8b404-106">To set the option, add the value in this table to the value in the ExtendedType field of the [CustomAction table](customaction-table.md).</span></span>

<span data-ttu-id="8b404-107">**[Windows Installer 4,0 e anteriores](not-supported-in-windows-installer-4-0.md):** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="8b404-107">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="8b404-108">Essa opção está disponível a partir do Windows Installer 4,5.</span><span class="sxs-lookup"><span data-stu-id="8b404-108">This option is available beginning with Windows Installer 4.5.</span></span>



| <span data-ttu-id="8b404-109">Constante</span><span class="sxs-lookup"><span data-stu-id="8b404-109">Constant</span></span>                                | <span data-ttu-id="8b404-110">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="8b404-110">Hexadecimal</span></span> | <span data-ttu-id="8b404-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="8b404-111">Decimal</span></span> | <span data-ttu-id="8b404-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="8b404-112">Description</span></span>                                                    |
|-----------------------------------------|-------------|---------|----------------------------------------------------------------|
| <span data-ttu-id="8b404-113">**msidbCustomActionTypePatchUninstall**</span><span class="sxs-lookup"><span data-stu-id="8b404-113">**msidbCustomActionTypePatchUninstall**</span></span> | <span data-ttu-id="8b404-114">0x8000</span><span class="sxs-lookup"><span data-stu-id="8b404-114">0x8000</span></span>      | <span data-ttu-id="8b404-115">32768</span><span class="sxs-lookup"><span data-stu-id="8b404-115">32768</span></span>   | <span data-ttu-id="8b404-116">A ação personalizada é executada somente quando um patch está sendo desinstalado.</span><span class="sxs-lookup"><span data-stu-id="8b404-116">The custom action runs only when a patch is being uninstalled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8b404-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b404-117">Remarks</span></span>

<span data-ttu-id="8b404-118">Esse atributo pode ser adicionado a uma ação personalizada por meio de sua criação no pacote de Windows Installer (arquivo. msi).</span><span class="sxs-lookup"><span data-stu-id="8b404-118">This attribute can be added to a custom action by authoring it in the Windows Installer package (.msi file).</span></span> <span data-ttu-id="8b404-119">Uma nova ação personalizada com esse atributo pode ser adicionada por um patch.</span><span class="sxs-lookup"><span data-stu-id="8b404-119">A new custom action with this attribute can be added by a patch.</span></span> <span data-ttu-id="8b404-120">Uma ação personalizada que tenha esse atributo pode ser atualizada por um patch.</span><span class="sxs-lookup"><span data-stu-id="8b404-120">A custom action having this attribute can be updated by a patch.</span></span> <span data-ttu-id="8b404-121">Este atributo não pode ser adicionado ou removido por um patch para uma ação personalizada existente.</span><span class="sxs-lookup"><span data-stu-id="8b404-121">This attribute cannot be added or removed by a patch to an existing custom action.</span></span>

<span data-ttu-id="8b404-122">Se um patch adicionar ou atualizar uma ação personalizada com esse atributo, Windows Installer executará a ação personalizada nova ou atualizada quando o patch for desinstalado.</span><span class="sxs-lookup"><span data-stu-id="8b404-122">If a patch adds or updates a custom action with this attribute, Windows Installer runs the new or updated custom action when the patch is uninstalled.</span></span> <span data-ttu-id="8b404-123">Windows Installer faz com que as atualizações no patch sejam desinstaladas disponíveis para a ação personalizada de desinstalação do patch.</span><span class="sxs-lookup"><span data-stu-id="8b404-123">Windows Installer makes the updates within the patch being uninstalled available to the patch uninstall custom action.</span></span> <span data-ttu-id="8b404-124">O patch deve incluir uma [tabela *<PatchGUID>* MsiTransformView](msitransformview.md) para fornecer essas informações para Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="8b404-124">The patch must include a [MsiTransformView *<PatchGUID>*](msitransformview.md) table to provide this information to Windows Installer.</span></span>

<span data-ttu-id="8b404-125">Quando um pacote que contém uma ação personalizada com o atributo **msidbCustomActionTypePatchUninstall** é instalado usando uma versão do instalador anterior à Windows Installer 4,0, o instalador não chama a ação personalizada quando o patch é desinstalado.</span><span class="sxs-lookup"><span data-stu-id="8b404-125">When a package that contains a custom action with the **msidbCustomActionTypePatchUninstall** attribute is installed using an installer version earlier than Windows Installer 4.0, the installer does not call the custom action when the patch is uninstalled.</span></span> <span data-ttu-id="8b404-126">A instalação pode executar a ação personalizada durante a instalação, o reparo ou a atualização do pacote.</span><span class="sxs-lookup"><span data-stu-id="8b404-126">The install can run the custom action during the installation, repair, or update of the package.</span></span>

<span data-ttu-id="8b404-127">Ações personalizadas com o atributo **msidbCustomActionTypePatchUninstall** devem ser condicionadas usando a propriedade [**MSIPATCHREMOVE**](msipatchremove.md) para impedir que a ação personalizada seja executada durante a instalação, reparo ou atualização usando um sistema com Windows Installer 4,0 ou anterior.</span><span class="sxs-lookup"><span data-stu-id="8b404-127">Custom actions with the **msidbCustomActionTypePatchUninstall** attribute should be conditioned using the [**MSIPATCHREMOVE**](msipatchremove.md) property to prevent the custom action from running when installing, repairing, or updating using a system with Windows Installer 4.0 or earlier.</span></span> <span data-ttu-id="8b404-128">Quando o Windows Installer 4,5 e posterior está instalado, todos os patches no sistema que têm ações personalizadas marcadas com o atributo **msidbCustomActionTypePatchUninstall** executam a ação personalizada durante a desinstalação do patch.</span><span class="sxs-lookup"><span data-stu-id="8b404-128">When Windows Installer 4.5 and later is installed, all the patches on the system having custom actions marked with the **msidbCustomActionTypePatchUninstall** attribute run the custom action during patch uninstallation.</span></span> <span data-ttu-id="8b404-129">Se Windows Installer 4,5 ou posterior for removido do sistema, os patches perderão a funcionalidade de desinstalação do patch de ação personalizada.</span><span class="sxs-lookup"><span data-stu-id="8b404-129">If Windows Installer 4.5 or later is removed from the system, patches lose the custom action patch uninstall functionality.</span></span>

<span data-ttu-id="8b404-130">Para obter informações sobre como executar uma ação personalizada durante a desinstalação de um patch usando uma versão anterior à Windows Installer 4,5, consulte [patches personalizados para desinstalar as ações](patch-uninstall-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="8b404-130">For information about running a custom action during the uninstallation of a patch using a version earlier than Windows Installer 4.5, see [Patch Uninstall Custom Actions](patch-uninstall-custom-actions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b404-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8b404-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b404-132">Opções de execução de In-Script de ação personalizada</span><span class="sxs-lookup"><span data-stu-id="8b404-132">Custom Action In-Script Execution Options</span></span>](custom-action-in-script-execution-options.md)
</dt> <dt>

[<span data-ttu-id="8b404-133">Referência de ação personalizada</span><span class="sxs-lookup"><span data-stu-id="8b404-133">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="8b404-134">Sobre ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="8b404-134">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="8b404-135">Usando ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="8b404-135">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="8b404-136">MsiTransformView *<PatchGUID>*</span><span class="sxs-lookup"><span data-stu-id="8b404-136">MsiTransformView *<PatchGUID>*</span></span>](msitransformview.md)
</dt> </dl>

 

 




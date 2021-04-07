---
description: A interface IUpdateInstaller define as propriedades a seguir.
ms.assetid: 876a2150-40a1-42a3-bc9a-05dec94fccd3
title: Propriedades de IUpdateInstaller
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77df235c49e7b6f27b0f93ec3b0c4def12135065
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827227"
---
# <a name="iupdateinstaller-properties"></a><span data-ttu-id="e2c2e-103">Propriedades de IUpdateInstaller</span><span class="sxs-lookup"><span data-stu-id="e2c2e-103">IUpdateInstaller Properties</span></span>

<span data-ttu-id="e2c2e-104">A interface [**IUpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller) define as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="e2c2e-104">The [**IUpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller) interface defines the following properties.</span></span>



| <span data-ttu-id="e2c2e-105">Propriedade</span><span class="sxs-lookup"><span data-stu-id="e2c2e-105">Property</span></span>                                                                                      | <span data-ttu-id="e2c2e-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="e2c2e-106">Description</span></span>                                                                                                                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2c2e-107">**AllowSourcePrompts**</span><span class="sxs-lookup"><span data-stu-id="e2c2e-107">**AllowSourcePrompts**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_allowsourceprompts)                             | <span data-ttu-id="e2c2e-108">Obtém e define um valor booliano que indica se os prompts de origem devem ser mostrados ao usuário ao instalar as atualizações.</span><span class="sxs-lookup"><span data-stu-id="e2c2e-108">Gets and sets a Boolean value that indicates whether to show source prompts to the user when installing the updates.</span></span>                  |
| [<span data-ttu-id="e2c2e-109">**ClientApplicationID**</span><span class="sxs-lookup"><span data-stu-id="e2c2e-109">**ClientApplicationID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_clientapplicationid)                           | <span data-ttu-id="e2c2e-110">Obtém e define o aplicativo cliente atual.</span><span class="sxs-lookup"><span data-stu-id="e2c2e-110">Gets and sets the current client application.</span></span>                                                                                         |
| [<span data-ttu-id="e2c2e-111">**IsBusy**</span><span class="sxs-lookup"><span data-stu-id="e2c2e-111">**IsBusy**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_isbusy)                                                     | <span data-ttu-id="e2c2e-112">Obtém um valor booliano que indica se uma instalação ou desinstalação está em andamento em um computador em um momento específico.</span><span class="sxs-lookup"><span data-stu-id="e2c2e-112">Gets a Boolean value that indicates whether an installation or uninstallation is in progress on a computer at a specific time.</span></span>        |
| [<span data-ttu-id="e2c2e-113">**Isforced**</span><span class="sxs-lookup"><span data-stu-id="e2c2e-113">**IsForced**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_isforced)                                                 | <span data-ttu-id="e2c2e-114">Obtém ou define um valor booliano que indica se uma atualização deve ser forçada ou desinstalada.</span><span class="sxs-lookup"><span data-stu-id="e2c2e-114">Gets or sets a Boolean value that indicates whether to forcibly install or uninstall an update.</span></span>                                       |
| [<span data-ttu-id="e2c2e-115">**ParentHwnd**</span><span class="sxs-lookup"><span data-stu-id="e2c2e-115">**ParentHwnd**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_parenthwnd)                                             | <span data-ttu-id="e2c2e-116">Obtém e define um identificador para a janela pai que pode conter uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e2c2e-116">Gets and sets a handle to the parent window that can contain a dialog box.</span></span>                                                            |
| [<span data-ttu-id="e2c2e-117">**ParentWindow**</span><span class="sxs-lookup"><span data-stu-id="e2c2e-117">**ParentWindow**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_parentwindow)                                         | <span data-ttu-id="e2c2e-118">Obtém e define a interface que representa a janela pai que pode conter uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e2c2e-118">Gets and sets the interface that represents the parent window that can contain a dialog box.</span></span>                                          |
| [<span data-ttu-id="e2c2e-119">**RebootRequiredBeforeInstallation**</span><span class="sxs-lookup"><span data-stu-id="e2c2e-119">**RebootRequiredBeforeInstallation**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_rebootrequiredbeforeinstallation) | <span data-ttu-id="e2c2e-120">Obtém um valor booliano que indica se uma reinicialização do sistema é necessária antes de instalar ou desinstalar atualizações.</span><span class="sxs-lookup"><span data-stu-id="e2c2e-120">Gets a Boolean value that indicates whether a system restart is required before installing or uninstalling updates.</span></span>                   |
| [<span data-ttu-id="e2c2e-121">**Atualizações**</span><span class="sxs-lookup"><span data-stu-id="e2c2e-121">**Updates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_updates)                                                   | <span data-ttu-id="e2c2e-122">Obtém e define uma interface que contém uma coleção somente leitura das atualizações que são especificadas para instalação ou desinstalação.</span><span class="sxs-lookup"><span data-stu-id="e2c2e-122">Gets and sets an interface that contains a read-only collection of the updates that are specified for installation or uninstallation.</span></span> |



 

 

 




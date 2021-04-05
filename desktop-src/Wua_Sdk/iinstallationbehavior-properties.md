---
description: A interface IInstallationBehavior define as propriedades a seguir.
ms.assetid: abb8e247-44c4-491c-b8ea-9f32d7420c45
title: Propriedades de IInstallationBehavior
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 210f495c19c530a6507ffbd0584f647fc952ae46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920966"
---
# <a name="iinstallationbehavior-properties"></a><span data-ttu-id="12e65-103">Propriedades de IInstallationBehavior</span><span class="sxs-lookup"><span data-stu-id="12e65-103">IInstallationBehavior Properties</span></span>

<span data-ttu-id="12e65-104">A interface [**IInstallationBehavior**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationbehavior) define as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="12e65-104">The [**IInstallationBehavior**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationbehavior) interface defines the following properties.</span></span>



| <span data-ttu-id="12e65-105">Propriedade</span><span class="sxs-lookup"><span data-stu-id="12e65-105">Property</span></span>                                                                                 | <span data-ttu-id="12e65-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="12e65-106">Description</span></span>                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="12e65-107">**CanRequestUserInput**</span><span class="sxs-lookup"><span data-stu-id="12e65-107">**CanRequestUserInput**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_canrequestuserinput)                 | <span data-ttu-id="12e65-108">Obtém um valor booliano thast indica se a instalação ou desinstalação de uma atualização pode solicitar entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="12e65-108">Gets a Boolean value thast indicates whether the installation or uninstallation of an update can prompt for user input.</span></span>                                                        |
| [<span data-ttu-id="12e65-109">**Impacto**</span><span class="sxs-lookup"><span data-stu-id="12e65-109">**Impact**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_impact)                                           | <span data-ttu-id="12e65-110">Obtém uma enumeração [**InstallationImpact**](/windows/win32/api/wuapi/ne-wuapi-installationimpact) que indica como a instalação ou desinstalação da atualização afeta o computador.</span><span class="sxs-lookup"><span data-stu-id="12e65-110">Gets an [**InstallationImpact**](/windows/win32/api/wuapi/ne-wuapi-installationimpact) enumeration that indicates how the installation or uninstallation of the update affects the computer.</span></span>                 |
| [<span data-ttu-id="12e65-111">**RebootBehavior**</span><span class="sxs-lookup"><span data-stu-id="12e65-111">**RebootBehavior**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_rebootbehavior)                           | <span data-ttu-id="12e65-112">Obtém uma enumeração [**InstallationRebootBehavior**](/windows/win32/api/wuapi/ne-wuapi-installationrebootbehavior) que especifica o comportamento de reinicialização que ocorre quando você instala ou desinstala a atualização.</span><span class="sxs-lookup"><span data-stu-id="12e65-112">Gets an [**InstallationRebootBehavior**](/windows/win32/api/wuapi/ne-wuapi-installationrebootbehavior) enumeration that specifies the restart behavior that occurs when you install or uninstall the update.</span></span> |
| [<span data-ttu-id="12e65-113">**RequiresNetworkConnectivity**</span><span class="sxs-lookup"><span data-stu-id="12e65-113">**RequiresNetworkConnectivity**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_requiresnetworkconnectivity) | <span data-ttu-id="12e65-114">Obtém um valor booliano que indica se a instalação ou desinstalação de uma atualização requer conectividade de rede.</span><span class="sxs-lookup"><span data-stu-id="12e65-114">Gets a Boolean value that indicates whether the installation or uninstallation of an update requires network connectivity.</span></span>                                                     |



 

 

 




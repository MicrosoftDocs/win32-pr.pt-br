---
description: A interface IInstallationJob define as propriedades a seguir.
ms.assetid: 74087098-bef0-41f8-8d7b-bbca1d000df8
title: Propriedades de IInstallationJob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b0083acd90b174349c105525676741c762aa05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647298"
---
# <a name="iinstallationjob-properties"></a><span data-ttu-id="ff734-103">Propriedades de IInstallationJob</span><span class="sxs-lookup"><span data-stu-id="ff734-103">IInstallationJob Properties</span></span>

<span data-ttu-id="ff734-104">A interface [**IInstallationJob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) define as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="ff734-104">The [**IInstallationJob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) interface defines the following properties.</span></span>



| <span data-ttu-id="ff734-105">Propriedade</span><span class="sxs-lookup"><span data-stu-id="ff734-105">Property</span></span>                                            | <span data-ttu-id="ff734-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="ff734-106">Description</span></span>                                                                                                                                                                                                                            |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ff734-107">**AsyncState**</span><span class="sxs-lookup"><span data-stu-id="ff734-107">**AsyncState**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_asyncstate)   | <span data-ttu-id="ff734-108">Obtém o objeto de estado específico do chamador que é passado para o método [**IUpdateInstaller. BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) ou [**IUpdateInstaller. BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) .</span><span class="sxs-lookup"><span data-stu-id="ff734-108">Gets the caller-specific state object that is passed to the [**IUpdateInstaller.BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) or [**IUpdateInstaller.BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) method.</span></span>               |
| [<span data-ttu-id="ff734-109">**IsCompleted**</span><span class="sxs-lookup"><span data-stu-id="ff734-109">**IsCompleted**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_iscompleted) | <span data-ttu-id="ff734-110">Obtém um valor que indica se uma chamada para o método [**IUpdateInstaller. BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) ou [**IUpdateInstaller. BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) é completamente processada.</span><span class="sxs-lookup"><span data-stu-id="ff734-110">Gets a value that indicates whether a call to the [**IUpdateInstaller.BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) or [**IUpdateInstaller.BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) method is completely processed.</span></span> |
| [<span data-ttu-id="ff734-111">**Atualizações**</span><span class="sxs-lookup"><span data-stu-id="ff734-111">**Updates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_updates)         | <span data-ttu-id="ff734-112">Obtém uma interface que contém uma coleção somente leitura das atualizações que são especificadas na instalação ou desinstalação.</span><span class="sxs-lookup"><span data-stu-id="ff734-112">Gets an interface that contains a read-only collection of the updates that are specified in the installation or uninstallation.</span></span>                                                                                                        |



 

 

 




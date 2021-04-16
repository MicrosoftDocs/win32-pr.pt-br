---
description: A restauração do sistema monitora e registra automaticamente as principais alterações do sistema no computador de um usuário. Para obter mais informações, consulte restauração do sistema.
ms.assetid: 5fc345ff-8a47-4372-806f-64b8c271fd2d
title: Pontos de restauração do sistema e o Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7fe9bd4b8e22f5aee7e49d3e4c452378f402e7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782323"
---
# <a name="system-restore-points-and-the-windows-installer"></a><span data-ttu-id="7ea5c-104">Pontos de restauração do sistema e o Windows Installer</span><span class="sxs-lookup"><span data-stu-id="7ea5c-104">System Restore Points and the Windows Installer</span></span>

<span data-ttu-id="7ea5c-105">A restauração do sistema monitora e registra automaticamente as principais alterações do sistema no computador de um usuário.</span><span class="sxs-lookup"><span data-stu-id="7ea5c-105">System Restore automatically monitors and records key system changes on a user's computer.</span></span> <span data-ttu-id="7ea5c-106">Para obter mais informações, consulte [restauração do sistema](../sr/system-restore-portal.md).</span><span class="sxs-lookup"><span data-stu-id="7ea5c-106">For more information, see [System Restore](../sr/system-restore-portal.md).</span></span>

<span data-ttu-id="7ea5c-107">Os pontos de restauração do sistema são criados pelo sistema e também são criados por Windows Installer quando o software é instalado ou removido.</span><span class="sxs-lookup"><span data-stu-id="7ea5c-107">System restore points are created by the system and are also created by Windows Installer when software is installed or removed.</span></span>

<span data-ttu-id="7ea5c-108">No Windows XP, o instalador pode criar pontos de verificação durante a primeira instalação de um aplicativo e durante sua remoção.</span><span class="sxs-lookup"><span data-stu-id="7ea5c-108">On Windows XP, the installer may create checkpoints during the first installation of an application, and during its removal.</span></span> <span data-ttu-id="7ea5c-109">O instalador cria somente pontos de verificação nesses casos quando a alteração é executada com pelo menos uma [*interface do usuário básica*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="7ea5c-109">The installer only creates checkpoints in these cases when the change is run with at least a [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="7ea5c-110">As instalações que têm o [nível de interface do usuário](user-interface-levels.md) definido como nenhum geralmente são iniciadas pelo sistema ou por um aplicativo que deve lidar com a criação de um ponto de verificação.</span><span class="sxs-lookup"><span data-stu-id="7ea5c-110">Installations having the [user interface level](user-interface-levels.md) set to None are usually initiated by the system or an application that should handle creating a checkpoint.</span></span> <span data-ttu-id="7ea5c-111">Para obter mais informações, consulte [restauração do sistema](../sr/system-restore-portal.md).</span><span class="sxs-lookup"><span data-stu-id="7ea5c-111">For more information, see [System Restore](../sr/system-restore-portal.md).</span></span>

<span data-ttu-id="7ea5c-112">Em corporações com muitos aplicativos pequenos, os administradores podem optar por desabilitar o ponto de verificação de dentro do instalador para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="7ea5c-112">In corporations with many small applications, administrators may decide to disable checkpointing from within the installer to improve performance.</span></span> <span data-ttu-id="7ea5c-113">Para obter mais informações, consulte [LimitSystemRestoreCheckpointing](limitsystemrestorecheckpointing.md) ou [definindo um ponto de restauração de uma ação personalizada](setting-a-restore-point-from-a-custom-action.md).</span><span class="sxs-lookup"><span data-stu-id="7ea5c-113">For more information, see [LimitSystemRestoreCheckpointing](limitsystemrestorecheckpointing.md) or [Setting a Restore Point from a Custom Action](setting-a-restore-point-from-a-custom-action.md).</span></span>

<span data-ttu-id="7ea5c-114">A partir do Windows Installer 5,0, a propriedade [**MSIFASTINSTALL**](msifastinstall.md) pode ser definida para impedir que uma instalação gere um ponto de restauração do sistema.</span><span class="sxs-lookup"><span data-stu-id="7ea5c-114">Beginning with Windows Installer 5.0, the [**MSIFASTINSTALL**](msifastinstall.md) property can be set to prevent an installation from generating a system restore point.</span></span>

 

 

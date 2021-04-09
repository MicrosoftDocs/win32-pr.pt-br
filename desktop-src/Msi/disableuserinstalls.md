---
description: Essa é uma política de sistema por máquina que pode ser usada quando o administrador desejar apenas aplicativos por máquina instalados.
ms.assetid: 3afa1d89-b76b-4184-b0d7-25cbf6749c7f
title: DisableUserInstalls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5ee8275567c62fc383c0488d6ad3ef8dfc928f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089992"
---
# <a name="disableuserinstalls"></a><span data-ttu-id="07d7e-103">DisableUserInstalls</span><span class="sxs-lookup"><span data-stu-id="07d7e-103">DisableUserInstalls</span></span>

<span data-ttu-id="07d7e-104">Essa é uma [política de sistema](system-policy.md) por máquina que pode ser usada quando o administrador desejar apenas aplicativos por máquina instalados.</span><span class="sxs-lookup"><span data-stu-id="07d7e-104">This is a per-machine [system policy](system-policy.md) that can be used when the administrator only wants per-machine applications installed.</span></span>

<span data-ttu-id="07d7e-105">Se essa política não estiver definida, o instalador pesquisará o registro em busca de aplicativos na seguinte ordem: aplicativos gerenciados registrados como aplicativos por usuário e não gerenciados registrados como por usuário e, por fim, aplicativos registrados como por máquina.</span><span class="sxs-lookup"><span data-stu-id="07d7e-105">If this policy is not set, the installer searches the registry for applications in the following order: managed applications registered as per-user, unmanaged applications registered as per-user, and finally applications registered as per-machine.</span></span>

<span data-ttu-id="07d7e-106">Se essa política for definida como 1, o instalador ignorará todos os aplicativos registrados como por usuário e somente procurará por aplicativos registrados como por computador.</span><span class="sxs-lookup"><span data-stu-id="07d7e-106">If this policy is set to 1, the installer ignores all applications registered as per-user and only searches for applications registered as per-machine.</span></span> <span data-ttu-id="07d7e-107">Chamadas para a interface de programação de aplicativo Windows Installer ou o sistema ignoram aplicativos por usuário.</span><span class="sxs-lookup"><span data-stu-id="07d7e-107">Calls to the Windows Installer application programming interface or system ignore per-user applications.</span></span> <span data-ttu-id="07d7e-108">Uma tentativa de executar uma instalação no [contexto de instalação](installation-context.md) por usuário faz com que o instalador exiba uma mensagem de erro e pare a instalação.</span><span class="sxs-lookup"><span data-stu-id="07d7e-108">An attempt to perform an installation in the per-user [installation context](installation-context.md) causes the installer to display an error message and stops the installation.</span></span> <span data-ttu-id="07d7e-109">Nesse caso, o Windows Installer também impede instalações por usuário de um servidor de terminal.</span><span class="sxs-lookup"><span data-stu-id="07d7e-109">In this case, the Windows Installer also prevents per-user installations from a terminal server.</span></span>

## <a name="registry-key"></a><span data-ttu-id="07d7e-110">Chave do Registro</span><span class="sxs-lookup"><span data-stu-id="07d7e-110">Registry Key</span></span>

<span data-ttu-id="07d7e-111">**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="07d7e-111">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="07d7e-112">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="07d7e-112">Data Type</span></span>

<span data-ttu-id="07d7e-113">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="07d7e-113">**REG\_DWORD**</span></span>

 

 




---
description: Se essa política do sistema for definida como 1, o instalador não armazenará arquivos de reversão durante a instalação e desabilitará a reversão da instalação.
ms.assetid: 01747de6-7478-4403-ba36-8ff1abc2b70f
title: DisableRollback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7f0ce15e618880f021e04adf7d2146a97f6ed65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921062"
---
# <a name="disablerollback"></a><span data-ttu-id="4a4e8-103">DisableRollback</span><span class="sxs-lookup"><span data-stu-id="4a4e8-103">DisableRollback</span></span>

<span data-ttu-id="4a4e8-104">Se essa [política do sistema](system-policy.md) for definida como 1, o instalador não armazenará arquivos de reversão durante a instalação e desabilitará a reversão da instalação.</span><span class="sxs-lookup"><span data-stu-id="4a4e8-104">If this [system policy](system-policy.md) is set to 1, the installer does not store rollback files during installation and disables installation rollback.</span></span> <span data-ttu-id="4a4e8-105">Por padrão, a reversão está habilitada.</span><span class="sxs-lookup"><span data-stu-id="4a4e8-105">By default, rollback is enabled.</span></span> <span data-ttu-id="4a4e8-106">Os administradores são aconselhados a não usar essa política, a menos que seja absolutamente essencial.</span><span class="sxs-lookup"><span data-stu-id="4a4e8-106">Administrators are advised to not use this policy unless it is absolutely essential.</span></span> <span data-ttu-id="4a4e8-107">Para obter mais informações, consulte [Rollback Installation](rollback-installation.md).</span><span class="sxs-lookup"><span data-stu-id="4a4e8-107">For more information, see [Rollback Installation](rollback-installation.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="4a4e8-108">Chave do Registro</span><span class="sxs-lookup"><span data-stu-id="4a4e8-108">Registry Key</span></span>

<span data-ttu-id="4a4e8-109">Para desabilitar a reversão para instalações por usuário, defina **DisableRollback** como 1 na seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="4a4e8-109">To disable rollback for per-user installations, set **DisableRollback** to 1 under the following registry key:</span></span>

<span data-ttu-id="4a4e8-110">**HKEY \_ \_** Políticas de software de usuário atuais \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="4a4e8-110">**HKEY\_CURRENT\_USER**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

<span data-ttu-id="4a4e8-111">Para desabilitar a reversão para instalações por computador, defina **DisableRollback** como 1 na seguinte chave do registro.</span><span class="sxs-lookup"><span data-stu-id="4a4e8-111">To disable rollback for per-computer installations, set **DisableRollback** to 1 under the following registry key.</span></span>

<span data-ttu-id="4a4e8-112">**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="4a4e8-112">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="4a4e8-113">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="4a4e8-113">Data Type</span></span>

<span data-ttu-id="4a4e8-114">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="4a4e8-114">**REG\_DWORD**</span></span>

 

 




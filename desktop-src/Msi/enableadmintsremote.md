---
description: A partir do Windows Server 2008 e do Windows Vista, essa política não tem mais efeito.
ms.assetid: 27a4192e-0574-414d-993e-6c715577f0ba
title: EnableAdminTSRemote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 383339ab5c2a592f3d6ab2cd81b4d6a446780411
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165005"
---
# <a name="enableadmintsremote"></a><span data-ttu-id="0cb3e-103">EnableAdminTSRemote</span><span class="sxs-lookup"><span data-stu-id="0cb3e-103">EnableAdminTSRemote</span></span>

<span data-ttu-id="0cb3e-104">A partir do Windows Server 2008 e do Windows Vista, essa política não tem mais efeito.</span><span class="sxs-lookup"><span data-stu-id="0cb3e-104">Beginning with Windows Server 2008 and Windows Vista, this policy no longer has any effect.</span></span> <span data-ttu-id="0cb3e-105">Um administrador pode executar uma instalação a partir da sessão de console de um servidor de terminal.</span><span class="sxs-lookup"><span data-stu-id="0cb3e-105">An administrator can perform an installation from the console session of a terminal server.</span></span> <span data-ttu-id="0cb3e-106">Um administrador também pode executar uma instalação de uma sessão de cliente do servidor de terminal.</span><span class="sxs-lookup"><span data-stu-id="0cb3e-106">An administrator can also perform an installation from a client session of the terminal server.</span></span>

<span data-ttu-id="0cb3e-107">Para obter mais informações, consulte [serviços de terminal](/windows/desktop/TermServ/terminal-services-portal) no SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="0cb3e-107">For more information, see [Terminal Services](/windows/desktop/TermServ/terminal-services-portal) in the Microsoft Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="0cb3e-108">\* \* Sistemas operacionais anteriores ao Windows Server 2008 e ao Windows Vista: \* \*</span><span class="sxs-lookup"><span data-stu-id="0cb3e-108">\*\*Operating systems earlier than Windows Server 2008 and Windows Vista:  \*\*</span></span>

<span data-ttu-id="0cb3e-109">Definir essa [política de sistema](system-policy.md) por máquina permite que os administradores executem instalações de uma sessão de cliente do servidor de terminal.</span><span class="sxs-lookup"><span data-stu-id="0cb3e-109">Setting this per-machine [system policy](system-policy.md) enables administrators to perform installations from a client session of the terminal server.</span></span> <span data-ttu-id="0cb3e-110">Se essa política não estiver definida, os administradores só poderão executar instalações da sessão de console.</span><span class="sxs-lookup"><span data-stu-id="0cb3e-110">If this policy is not set, administrators can only perform installations from the console session.</span></span> <span data-ttu-id="0cb3e-111">Usuários não administrativos nunca podem executar instalações de uma sessão de cliente.</span><span class="sxs-lookup"><span data-stu-id="0cb3e-111">Nonadministrative users can never perform installations from a client session.</span></span> <span data-ttu-id="0cb3e-112">O valor padrão dessa política permite que somente os administradores executem instalações da sessão do console.</span><span class="sxs-lookup"><span data-stu-id="0cb3e-112">The default value for this policy allows only administrators to perform installations from the console session.</span></span> <span data-ttu-id="0cb3e-113">Os administradores sempre podem fazer [instalações administrativas](administrative-installation.md) de uma sessão de cliente do servidor de terminal ou da sessão de console, independentemente de essa política ser definida.</span><span class="sxs-lookup"><span data-stu-id="0cb3e-113">Administrators can always do [Administrative installations](administrative-installation.md) from a client session of the terminal server, or from the console session, regardless of whether this policy is set.</span></span>

## <a name="registry-key"></a><span data-ttu-id="0cb3e-114">Chave do Registro</span><span class="sxs-lookup"><span data-stu-id="0cb3e-114">Registry Key</span></span>

<span data-ttu-id="0cb3e-115">**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="0cb3e-115">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="0cb3e-116">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="0cb3e-116">Data Type</span></span>

<span data-ttu-id="0cb3e-117">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="0cb3e-117">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="0cb3e-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="0cb3e-118">Remarks</span></span>

<span data-ttu-id="0cb3e-119">Para obter mais informações, consulte também, [usando Windows Installer com um Terminal Server](using-windows-installer-with-a-terminal-server.md).</span><span class="sxs-lookup"><span data-stu-id="0cb3e-119">For more information see also, [Using Windows Installer with a Terminal Server](using-windows-installer-with-a-terminal-server.md).</span></span>

 

 

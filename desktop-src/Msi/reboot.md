---
description: A propriedade reboot suprime determinados prompts para uma reinicialização do sistema.
ms.assetid: d88752cd-f59d-4214-b5b5-ce126500aa4e
title: Reinicializar Propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d94b08a04f3e95d873f6fc233185ce623cafc25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747740"
---
# <a name="reboot-property"></a><span data-ttu-id="522b9-103">Reinicializar Propriedade</span><span class="sxs-lookup"><span data-stu-id="522b9-103">REBOOT property</span></span>

<span data-ttu-id="522b9-104">A propriedade **reboot** suprime determinados prompts para uma reinicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="522b9-104">The **REBOOT** property suppresses certain prompts for a restart of the system.</span></span> <span data-ttu-id="522b9-105">Um administrador normalmente usa essa propriedade com uma série de instalações para instalar vários produtos ao mesmo tempo com apenas uma reinicialização no final.</span><span class="sxs-lookup"><span data-stu-id="522b9-105">An administrator typically uses this property with a series of installations to install several products at the same time with only one restart at the end.</span></span> <span data-ttu-id="522b9-106">Para obter mais informações, consulte [reinicializações do sistema](system-reboots.md).</span><span class="sxs-lookup"><span data-stu-id="522b9-106">For more information, see [System Reboots](system-reboots.md).</span></span>

<span data-ttu-id="522b9-107">As ações [ForceReboot](forcereboot-action.md) e [ScheduleReboot](schedulereboot-action.md) informam o instalador para solicitar que o usuário reinicie o sistema.</span><span class="sxs-lookup"><span data-stu-id="522b9-107">The [ForceReboot](forcereboot-action.md) and [ScheduleReboot](schedulereboot-action.md) actions inform the installer to prompt the user to restart the system.</span></span> <span data-ttu-id="522b9-108">O instalador também pode determinar que uma reinicialização é necessária se houver alguma ação ForceReboot ou ScheduleReboot na sequência.</span><span class="sxs-lookup"><span data-stu-id="522b9-108">The installer can also determine that a restart is necessary whether there are any ForceReboot or ScheduleReboot actions in the sequence.</span></span> <span data-ttu-id="522b9-109">Por exemplo, o instalador solicitará automaticamente uma reinicialização se precisar substituir todos os arquivos em uso durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="522b9-109">For example, the installer automatically prompts for a restart if it needs to replace any files in use during the installation.</span></span>

<span data-ttu-id="522b9-110">Você pode suprimir determinados prompts para reinicializações definindo a propriedade **reboot** da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="522b9-110">You can suppress certain prompts for restarts by setting the **REBOOT** property as follows.</span></span>



| <span data-ttu-id="522b9-111">Valor de reinicialização</span><span class="sxs-lookup"><span data-stu-id="522b9-111">REBOOT value</span></span>   | <span data-ttu-id="522b9-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="522b9-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="522b9-113">Force</span><span class="sxs-lookup"><span data-stu-id="522b9-113">Force</span></span>          | <span data-ttu-id="522b9-114">Sempre solicitar uma reinicialização no final da instalação.</span><span class="sxs-lookup"><span data-stu-id="522b9-114">Always prompt for a restart at the end of the installation.</span></span> <span data-ttu-id="522b9-115">A IU sempre solicita ao usuário uma opção para reiniciar no final.</span><span class="sxs-lookup"><span data-stu-id="522b9-115">The UI always prompts the user with an option to restart at the end.</span></span> <span data-ttu-id="522b9-116">Se não houver nenhuma interface do usuário e essa não for uma [instalação de vários pacotes](multiple-package-installations.md), o sistema será reiniciado automaticamente no final da instalação.</span><span class="sxs-lookup"><span data-stu-id="522b9-116">If there is no user interface, and this is not a [multiple-package installation](multiple-package-installations.md), the system automatically restarts at the end of the installation.</span></span> <span data-ttu-id="522b9-117">Se esta for uma instalação de vários pacotes, não haverá reinicialização automática do sistema e o instalador retornará o \_ erro \_ reinicialização bem-sucedida \_ necessária.</span><span class="sxs-lookup"><span data-stu-id="522b9-117">If this is a multiple-package installation, there is no automatic restart of the system and the installer returns ERROR\_SUCCESS\_REBOOT\_REQUIRED.</span></span> |
| <span data-ttu-id="522b9-118">Suprimir</span><span class="sxs-lookup"><span data-stu-id="522b9-118">Suppress</span></span>       | <span data-ttu-id="522b9-119">Suprimir prompts para uma reinicialização no final da instalação.</span><span class="sxs-lookup"><span data-stu-id="522b9-119">Suppress prompts for a restart at the end of the installation.</span></span> <span data-ttu-id="522b9-120">O instalador ainda solicita ao usuário uma opção para reiniciar durante a instalação sempre que encontrar a [ação ForceReboot](forcereboot-action.md).</span><span class="sxs-lookup"><span data-stu-id="522b9-120">The installer still prompts the user with an option to restart during the installation whenever it encounters the [ForceReboot action](forcereboot-action.md).</span></span> <span data-ttu-id="522b9-121">Se não houver nenhuma interface do usuário, o sistema será reiniciado automaticamente em cada ForceReboot.</span><span class="sxs-lookup"><span data-stu-id="522b9-121">If there is no user interface, the system automatically restarts at each ForceReboot.</span></span> <span data-ttu-id="522b9-122">As reinicializações no final da instalação (por exemplo, causada por uma tentativa de instalar um arquivo em uso) são suprimidas.</span><span class="sxs-lookup"><span data-stu-id="522b9-122">Restarts at the end of the installation (for example, caused by an attempt to install a file in use) are suppressed.</span></span>                                    |
| <span data-ttu-id="522b9-123">ReallySuppress</span><span class="sxs-lookup"><span data-stu-id="522b9-123">ReallySuppress</span></span> | <span data-ttu-id="522b9-124">Suprimir todas as reinicializações e solicitações de reinicialização iniciadas pelo ForceReboot durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="522b9-124">Suppress all restarts and restart prompts initiated by ForceReboot during the installation.</span></span> <span data-ttu-id="522b9-125">Suprimir todas as reinicializações e solicitações de reinicialização no final da instalação.</span><span class="sxs-lookup"><span data-stu-id="522b9-125">Suppress all restarts and restart prompts at the end of the installation.</span></span> <span data-ttu-id="522b9-126">O prompt de reinicialização e a reinicialização em si são suprimidos.</span><span class="sxs-lookup"><span data-stu-id="522b9-126">Both the restart prompt and the restart itself are suppressed.</span></span> <span data-ttu-id="522b9-127">Por exemplo, as reinicializações no final da instalação, causadas por uma tentativa de instalar um arquivo em uso, são suprimidas.</span><span class="sxs-lookup"><span data-stu-id="522b9-127">For example, restarts at the end of the installation, caused by an attempt to install a file in use, are suppressed.</span></span>                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="522b9-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="522b9-128">Remarks</span></span>

<span data-ttu-id="522b9-129">O instalador só avalia o primeiro caractere da propriedade **reboot** .</span><span class="sxs-lookup"><span data-stu-id="522b9-129">The installer only evaluates the first character of the **REBOOT** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="522b9-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="522b9-130">Requirements</span></span>



| <span data-ttu-id="522b9-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="522b9-131">Requirement</span></span> | <span data-ttu-id="522b9-132">Valor</span><span class="sxs-lookup"><span data-stu-id="522b9-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="522b9-133">Versão</span><span class="sxs-lookup"><span data-stu-id="522b9-133">Version</span></span><br/> | <span data-ttu-id="522b9-134">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="522b9-134">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="522b9-135">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="522b9-135">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="522b9-136">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="522b9-136">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="522b9-137">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="522b9-137">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="522b9-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="522b9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="522b9-139">Propriedades</span><span class="sxs-lookup"><span data-stu-id="522b9-139">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="522b9-140">**Propriedade REBOOTPROMPT**</span><span class="sxs-lookup"><span data-stu-id="522b9-140">**REBOOTPROMPT Property**</span></span>](rebootprompt.md)
</dt> <dt>

[<span data-ttu-id="522b9-141">Reinicializações do sistema</span><span class="sxs-lookup"><span data-stu-id="522b9-141">System Reboots</span></span>](system-reboots.md)
</dt> </dl>

 

 





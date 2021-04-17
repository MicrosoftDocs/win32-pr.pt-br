---
description: A ação ForceReboot solicita ao usuário uma reinicialização do sistema durante a instalação.
ms.assetid: e1bcdd59-8cbc-46f7-b908-c8cbc2ea0539
title: Ação ForceReboot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 807bab474f1faacfbc7684797b7a0b7b74f354d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811848"
---
# <a name="forcereboot-action"></a><span data-ttu-id="f2c47-103">Ação ForceReboot</span><span class="sxs-lookup"><span data-stu-id="f2c47-103">ForceReboot Action</span></span>

<span data-ttu-id="f2c47-104">A ação ForceReboot solicita ao usuário uma reinicialização do sistema durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="f2c47-104">The ForceReboot action prompts the user for a restart of the system during the installation.</span></span> <span data-ttu-id="f2c47-105">A ação ForceReboot é diferente da [ação ScheduleReboot](schedulereboot-action.md) , pois a ação ScheduleReboot é usada para agendar uma solicitação para reiniciar no final da instalação.</span><span class="sxs-lookup"><span data-stu-id="f2c47-105">The ForceReboot action is different from the [ScheduleReboot action](schedulereboot-action.md) in that the ScheduleReboot action is used to schedule a prompt to restart at the end of the installation.</span></span>

<span data-ttu-id="f2c47-106">Se a instalação tiver uma interface do usuário, o instalador exibirá uma caixa de diálogo em cada ação ForceReboot que solicita que o usuário reinicie o sistema.</span><span class="sxs-lookup"><span data-stu-id="f2c47-106">If the installation has a user interface, the installer displays a dialog box at each ForceReboot action which prompts the user to restart the system.</span></span> <span data-ttu-id="f2c47-107">O usuário deve responder a esse prompt antes de continuar com a instalação.</span><span class="sxs-lookup"><span data-stu-id="f2c47-107">The user must respond to this prompt before continuing with the installation.</span></span> <span data-ttu-id="f2c47-108">Se a instalação não tiver nenhuma interface do usuário, o sistema será reiniciado automaticamente na ação ForceReboot.</span><span class="sxs-lookup"><span data-stu-id="f2c47-108">If the installation has no user interface, the system automatically restarts at the ForceReboot action.</span></span>

<span data-ttu-id="f2c47-109">Se o instalador determinar que uma reinicialização é necessária, ele solicitará automaticamente que o usuário seja reiniciado no final da instalação, independentemente de haver ou não ações ForceReboot ou ScheduleReboot na sequência.</span><span class="sxs-lookup"><span data-stu-id="f2c47-109">If the installer determines that a restart is necessary, it automatically prompts the user to restart at the end of the installation, whether or not there are any ForceReboot or ScheduleReboot actions in the sequence.</span></span> <span data-ttu-id="f2c47-110">Por exemplo, o instalador solicitará automaticamente uma reinicialização se precisar substituir todos os arquivos usados durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="f2c47-110">For example, the installer automatically prompts for a restart if it needs to replace any files used during the installation.</span></span>

<span data-ttu-id="f2c47-111">Suprimir determinados prompts de reinicialização definindo a propriedade [**reboot**](reboot.md) .</span><span class="sxs-lookup"><span data-stu-id="f2c47-111">Suppress certain restart prompts by setting the [**REBOOT**](reboot.md) property.</span></span>

<span data-ttu-id="f2c47-112">Se o Windows Installer encontrar a ação ForceReboot ou [ScheduleReboot](schedulereboot-action.md) durante uma [instalação de vários pacotes](multiple-package-installations.md), o instalador irá parar e reverter a instalação.</span><span class="sxs-lookup"><span data-stu-id="f2c47-112">If the Windows Installer encounters the ForceReboot or [ScheduleReboot](schedulereboot-action.md) action during a [multiple-package installation](multiple-package-installations.md), the installer will stop and roll back the installation.</span></span> <span data-ttu-id="f2c47-113">Outros pacotes que pertencem à instalação de vários pacotes, que não contêm uma ação ForceReboot ou ScheduleReboot, podem ser instalados.</span><span class="sxs-lookup"><span data-stu-id="f2c47-113">Other packages belonging to the multiple-package installation, that do not contain a ForceReboot or ScheduleReboot action, can be installed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="f2c47-114">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="f2c47-114">Sequence Restrictions</span></span>

<span data-ttu-id="f2c47-115">As ações a seguir geralmente ocorrem juntas como um grupo na sequência de ação.</span><span class="sxs-lookup"><span data-stu-id="f2c47-115">The following actions commonly occur together as a group in the action sequence.</span></span> <span data-ttu-id="f2c47-116">É recomendável que a ação ForceReboot seja agendada para vir após esse grupo.</span><span class="sxs-lookup"><span data-stu-id="f2c47-116">It is recommended that the ForceReboot action be scheduled to come after this group.</span></span> <span data-ttu-id="f2c47-117">Se a ação ForceReboot estiver agendada antes da [ação RegisterProduct](registerproduct-action.md), o instalador novamente exigirá a origem do pacote de instalação após a reinicialização.</span><span class="sxs-lookup"><span data-stu-id="f2c47-117">If the ForceReboot action is scheduled before the [RegisterProduct action](registerproduct-action.md), the installer again requires the source of the installation package after the restart.</span></span> <span data-ttu-id="f2c47-118">Portanto, a sequência preferida para ForceReboot é imediatamente após essa sequência de ação.</span><span class="sxs-lookup"><span data-stu-id="f2c47-118">Therefore, the preferred sequence for ForceReboot is immediately following this action sequence.</span></span>

-   [<span data-ttu-id="f2c47-119">RegisterProduct</span><span class="sxs-lookup"><span data-stu-id="f2c47-119">RegisterProduct</span></span>](registerproduct-action.md)
-   [<span data-ttu-id="f2c47-120">RegisterUser</span><span class="sxs-lookup"><span data-stu-id="f2c47-120">RegisterUser</span></span>](registeruser-action.md)
-   [<span data-ttu-id="f2c47-121">PublishProduct</span><span class="sxs-lookup"><span data-stu-id="f2c47-121">PublishProduct</span></span>](publishproduct-action.md)
-   [<span data-ttu-id="f2c47-122">PublishFeatures</span><span class="sxs-lookup"><span data-stu-id="f2c47-122">PublishFeatures</span></span>](publishfeatures-action.md)
-   [<span data-ttu-id="f2c47-123">Createatalhos</span><span class="sxs-lookup"><span data-stu-id="f2c47-123">CreateShortcuts</span></span>](createshortcuts-action.md)
-   [<span data-ttu-id="f2c47-124">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="f2c47-124">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)
-   [<span data-ttu-id="f2c47-125">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="f2c47-125">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="f2c47-126">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="f2c47-126">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="f2c47-127">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="f2c47-127">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)

<span data-ttu-id="f2c47-128">A ação ForceReboot deve vir entre [InstallInitialize](installinitialize-action.md) e [InstallFinalize](installfinalize-action.md) na sequência de ação da [tabela InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="f2c47-128">The ForceReboot action must come between [InstallInitialize](installinitialize-action.md) and [InstallFinalize](installfinalize-action.md) in the action sequence of the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="f2c47-129">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="f2c47-129">ActionData Messages</span></span>

<span data-ttu-id="f2c47-130">Não há nenhuma mensagem ActionData.</span><span class="sxs-lookup"><span data-stu-id="f2c47-130">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2c47-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="f2c47-131">Remarks</span></span>

<span data-ttu-id="f2c47-132">A ação ForceReboot sempre deve ser usada com uma instrução condicional de modo que o instalador dispare uma reinicialização somente quando necessário.</span><span class="sxs-lookup"><span data-stu-id="f2c47-132">The ForceReboot action must always be used with a conditional statement such that the installer triggers a restart only when necessary.</span></span> <span data-ttu-id="f2c47-133">Por exemplo, uma reinicialização só poderá ser necessária se um determinado arquivo for substituído ou se um componente específico estiver instalado.</span><span class="sxs-lookup"><span data-stu-id="f2c47-133">For example, a restart may only be required if a particular file is replaced or a particular component is installed.</span></span> <span data-ttu-id="f2c47-134">Cada instalação de produto é exclusiva e uma ação personalizada pode ser necessária para determinar se uma reinicialização é necessária.</span><span class="sxs-lookup"><span data-stu-id="f2c47-134">Each product installation is unique and a custom action may be required to determine whether a restart is needed.</span></span> <span data-ttu-id="f2c47-135">A condição na ação ForceReboot normalmente usa a propriedade [**AFTERREBOOT**](afterreboot.md) .</span><span class="sxs-lookup"><span data-stu-id="f2c47-135">The condition on the ForceReboot action commonly makes use of the [**AFTERREBOOT**](afterreboot.md) property.</span></span>

<span data-ttu-id="f2c47-136">ForceReboot executa operações do sistema geradas por quaisquer ações anteriores antes de solicitar uma reinicialização ou reinicialização.</span><span class="sxs-lookup"><span data-stu-id="f2c47-136">ForceReboot runs system operations generated by any previous actions before prompting for a restart or restarting.</span></span> <span data-ttu-id="f2c47-137">Por exemplo, as operações do sistema geradas por [InstallFiles](installfiles-action.md) e [WriteRegistryValues](writeregistryvalues-action.md) são executadas antes de uma reinicialização.</span><span class="sxs-lookup"><span data-stu-id="f2c47-137">For example, the system operations generated by [InstallFiles](installfiles-action.md) and [WriteRegistryValues](writeregistryvalues-action.md) are run before a restart.</span></span>

<span data-ttu-id="f2c47-138">A ação ForceReboot grava uma chave do registro que faz com que o instalador seja iniciado após a reinicialização.</span><span class="sxs-lookup"><span data-stu-id="f2c47-138">The ForceReboot action writes a registry key that causes the installer to start after restarting.</span></span> <span data-ttu-id="f2c47-139">O local dessa chave é **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce**.</span><span class="sxs-lookup"><span data-stu-id="f2c47-139">The location of this key is **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\RunOnce**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2c47-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f2c47-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2c47-141">Reinicializações do sistema</span><span class="sxs-lookup"><span data-stu-id="f2c47-141">System Reboots</span></span>](system-reboots.md)
</dt> </dl>

 

 




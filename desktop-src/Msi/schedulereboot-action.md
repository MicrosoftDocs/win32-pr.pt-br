---
description: Insira a ação ScheduleReboot na sequência de ação para solicitar ao usuário uma reinicialização do sistema no final da instalação. Use a ação ForceReboot para solicitar uma reinicialização durante a instalação.
ms.assetid: 36f24f57-f1f0-4eca-9b6d-1b25fb73fa96
title: Ação ScheduleReboot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460e3f25283c233fac80b25edd91d4bd102de435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828428"
---
# <a name="schedulereboot-action"></a><span data-ttu-id="8a5b7-104">Ação ScheduleReboot</span><span class="sxs-lookup"><span data-stu-id="8a5b7-104">ScheduleReboot Action</span></span>

<span data-ttu-id="8a5b7-105">Insira a ação ScheduleReboot na sequência de ação para solicitar ao usuário uma reinicialização do sistema no final da instalação.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-105">Insert the ScheduleReboot action into the action sequence to prompt the user for a restart of the system at the end of the installation.</span></span> <span data-ttu-id="8a5b7-106">Use a [ação ForceReboot](forcereboot-action.md) para solicitar uma reinicialização durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-106">Use the [ForceReboot action](forcereboot-action.md) to prompt for a restart during installation.</span></span>

<span data-ttu-id="8a5b7-107">Se a instalação tiver uma interface do usuário, o instalador exibirá uma caixa de mensagem e um botão no final da instalação, perguntando se o usuário deseja reiniciar o sistema.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-107">If the installation has a user interface, the installer displays a message box and button at the end of installation asking whether the user wants to restart the system.</span></span> <span data-ttu-id="8a5b7-108">O usuário deve responder a este prompt antes de concluir a instalação.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-108">The user must respond to this prompt before completing installation.</span></span> <span data-ttu-id="8a5b7-109">Se a instalação não tiver nenhuma interface do usuário, o sistema será reiniciado automaticamente no final.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-109">If the installation has no user interface, the system automatically restarts at the end.</span></span>

<span data-ttu-id="8a5b7-110">Se o instalador determinar que uma reinicialização é necessária, ele solicitará automaticamente que o usuário seja reiniciado no final da instalação, independentemente de haver ou não qualquer ação ForceReboot ou ScheduleReboot na sequência.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-110">If the installer determines that a restart is necessary it automatically prompts the user to restart at the end of the installation, whether or not there are any ForceReboot or ScheduleReboot actions in the sequence.</span></span> <span data-ttu-id="8a5b7-111">Por exemplo, o instalador solicitará automaticamente uma reinicialização se precisar substituir todos os arquivos que estão em uso durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-111">For example, the installer automatically prompts for a restart if it needs to replace any files that are in use during installation.</span></span>

<span data-ttu-id="8a5b7-112">Você pode suprimir determinados prompts para reinicializações definindo a propriedade [**reboot**](reboot.md) .</span><span class="sxs-lookup"><span data-stu-id="8a5b7-112">You can suppress certain prompts for restarts by setting the [**REBOOT**](reboot.md) property.</span></span>

<span data-ttu-id="8a5b7-113">Se o Windows Installer encontrar a ação [ForceReboot](forcereboot-action.md) ou ScheduleReboot durante uma [instalação de vários pacotes](multiple-package-installations.md), o instalador irá parar e reverter a instalação.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-113">If the Windows Installer encounters the [ForceReboot](forcereboot-action.md) or ScheduleReboot action during a [multiple-package installation](multiple-package-installations.md), the installer will stop and roll back the installation.</span></span> <span data-ttu-id="8a5b7-114">Outros pacotes que pertencem à instalação de vários pacotes, que não contêm uma ação ForceReboot ou ScheduleReboot, podem ser instalados.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-114">Other packages belonging to the multiple-package installation, that do not contain a ForceReboot or ScheduleReboot action, can be installed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="8a5b7-115">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="8a5b7-115">Sequence Restrictions</span></span>

<span data-ttu-id="8a5b7-116">Não há restrições de sequência.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-116">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="8a5b7-117">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="8a5b7-117">ActionData Messages</span></span>

<span data-ttu-id="8a5b7-118">Não há nenhuma mensagem ActionData.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-118">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a5b7-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a5b7-119">Remarks</span></span>

<span data-ttu-id="8a5b7-120">Por exemplo, essa ação pode ser usada para forçar o instalador a solicitar uma reinicialização depois de instalar os drivers que exigem uma reinicialização.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-120">For example, this action can be used to force the installer to prompt for a restart after installing drivers that require a restart.</span></span> <span data-ttu-id="8a5b7-121">Se o instalador tentar substituir os arquivos que estão em uso, ele solicitará automaticamente que o usuário seja reiniciado mesmo que ScheduleReboot não tenha sido usado.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-121">If the installer attempts to replace files that are in use, it automatically prompts the user to restart even if ScheduleReboot has not been used.</span></span>

<span data-ttu-id="8a5b7-122">A ação ScheduleReboot normalmente é colocada no final da sequência, mas pode ser inserida em qualquer ponto na sequência.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-122">The ScheduleReboot action is typically placed at the end of the sequence, but it can be inserted at any point in the sequence.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a5b7-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8a5b7-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a5b7-124">Reinicializações do sistema</span><span class="sxs-lookup"><span data-stu-id="8a5b7-124">System Reboots</span></span>](system-reboots.md)
</dt> </dl>

 

 




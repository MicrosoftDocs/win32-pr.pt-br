---
description: Notifica o Windows Installer para usar o Gerenciador de reinicialização para desligar todos os aplicativos que têm arquivos em uso e reiniciá-los no final da instalação.
ms.assetid: bfa19cc8-4cf7-42ed-9e94-acaeca8d707a
title: RmShutdownAndRestart ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc91d1de52f516c0728e8d6469fb8cddc2e50cfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751633"
---
# <a name="rmshutdownandrestart-controlevent"></a><span data-ttu-id="17a7e-103">RmShutdownAndRestart ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="17a7e-103">RmShutdownAndRestart ControlEvent</span></span>

<span data-ttu-id="17a7e-104">Esse evento notifica a Windows Installer usar o Gerenciador de [reinicialização](../rstmgr/restart-manager-portal.md) para desligar todos os aplicativos que têm arquivos em uso e reiniciá-los no final da instalação.</span><span class="sxs-lookup"><span data-stu-id="17a7e-104">This event notifies the Windows Installer to use the [Restart Manager](../rstmgr/restart-manager-portal.md) to shutdown all applications that have files in use and to restart them at the end of the installation.</span></span>

<span data-ttu-id="17a7e-105">Esse ControlEvent, não terá efeito se qualquer uma das seguintes opções for verdadeira.</span><span class="sxs-lookup"><span data-stu-id="17a7e-105">This ControlEvent has no effect if any of the following are true.</span></span>

-   <span data-ttu-id="17a7e-106">O sistema operacional que executa a instalação do não é o Windows Vista ou o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="17a7e-106">The operating system running the installation is not Windows Vista or Windows Server 2008.</span></span>
-   <span data-ttu-id="17a7e-107">As interações com o [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) foram desabilitadas pela propriedade [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md) ou pela política [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="17a7e-107">Interactions with the [Restart Manager](../rstmgr/restart-manager-portal.md) have been disabled by the [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md) property or the [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) policy.</span></span>
-   <span data-ttu-id="17a7e-108">Não há sessão do [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) aberta no momento.</span><span class="sxs-lookup"><span data-stu-id="17a7e-108">There is currently no open [Restart Manager](../rstmgr/restart-manager-portal.md) session.</span></span>
-   <span data-ttu-id="17a7e-109">Todas as chamadas do Windows Installer para o [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) retornam uma falha.</span><span class="sxs-lookup"><span data-stu-id="17a7e-109">Any calls from the Windows Installer to the [Restart Manager](../rstmgr/restart-manager-portal.md) returns a failure.</span></span>

## <a name="typical-use"></a><span data-ttu-id="17a7e-110">Usos comum</span><span class="sxs-lookup"><span data-stu-id="17a7e-110">Typical Use</span></span>

<span data-ttu-id="17a7e-111">O evento de controle RMShutdownAndRestart é publicado somente por um controle de [pressão](pushbutton-control.md) na caixa de [diálogo MsiRMFilesInUse](msirmfilesinuse-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="17a7e-111">The RMShutdownAndRestart control event is published only by a [PushButton](pushbutton-control.md) control on the [MsiRMFilesInUse Dialog](msirmfilesinuse-dialog.md) box.</span></span>

 

 

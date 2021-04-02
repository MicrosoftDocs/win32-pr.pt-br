---
description: A caixa de diálogo MsiRMFilesInUse pode ser criada para exibir uma lista de processos que atualmente estão executando arquivos que precisam ser substituídos ou excluídos pela instalação.
ms.assetid: e8d93310-388e-4a08-9bce-04c31c33a665
title: Caixa de diálogo MsiRMFilesInUse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bba73cab51f4b3d8321b15001dbb72c638176b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922742"
---
# <a name="msirmfilesinuse-dialog"></a><span data-ttu-id="c26bc-103">Caixa de diálogo MsiRMFilesInUse</span><span class="sxs-lookup"><span data-stu-id="c26bc-103">MsiRMFilesInUse Dialog</span></span>

<span data-ttu-id="c26bc-104">A caixa de diálogo MsiRMFilesInUse pode ser criada para exibir uma lista de processos que atualmente estão executando arquivos que precisam ser substituídos ou excluídos pela instalação.</span><span class="sxs-lookup"><span data-stu-id="c26bc-104">The MsiRMFilesInUse Dialog box can be authored to display a list of processes that are currently running files that need to be overwritten or deleted by the installation.</span></span> <span data-ttu-id="c26bc-105">O usuário pode selecionar entre opções para "fechar aplicativos automaticamente e reiniciá-los" ou "não fechar aplicativos.</span><span class="sxs-lookup"><span data-stu-id="c26bc-105">The user can select between options to "Automatically close applications and restart them" or "Do not close applications.</span></span> <span data-ttu-id="c26bc-106">(Uma reinicialização será necessária.) " Se o usuário selecionar a opção "fechar aplicativos automaticamente e reiniciá-los", um controle de botão de ação nessa caixa de diálogo poderá ser criado para publicar o evento de controle RMShutdownAndRestart e o [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) poderá fechar os aplicativos e reiniciá-los no final da instalação.</span><span class="sxs-lookup"><span data-stu-id="c26bc-106">(A reboot will be required.)" If the user selects the "Automatically close applications and restart them" option, a push button control on this dialog box can be authored to publish the RMShutdownAndRestart control event and the [Restart Manager](../rstmgr/restart-manager-portal.md) can close the applications and restart them at the end of the installation.</span></span> <span data-ttu-id="c26bc-107">Isso pode eliminar ou reduzir a necessidade de reiniciar o computador.</span><span class="sxs-lookup"><span data-stu-id="c26bc-107">This can eliminate or reduce the need to restart the computer.</span></span> <span data-ttu-id="c26bc-108">Para obter mais informações, consulte [reinicializações do sistema](system-reboots.md).</span><span class="sxs-lookup"><span data-stu-id="c26bc-108">For more information, see [System Reboots](system-reboots.md).</span></span>

<span data-ttu-id="c26bc-109">A caixa de diálogo **MsiRMFilesInUse** será exibida durante uma instalação somente se todas as seguintes opções forem verdadeiras.</span><span class="sxs-lookup"><span data-stu-id="c26bc-109">The **MsiRMFilesInUse** dialog box is displayed during an installation only if all the following are true.</span></span> <span data-ttu-id="c26bc-110">Quando qualquer um desses for falso, o Windows Installer ignorará a caixa de diálogo **MsiRMFilesInUse** .</span><span class="sxs-lookup"><span data-stu-id="c26bc-110">When any of these are false, the Windows Installer ignores the **MsiRMFilesInUse** dialog box.</span></span>

-   <span data-ttu-id="c26bc-111">Uma versão Windows Installer que não seja anterior à versão 4,0 e um sistema operacional que não seja anterior ao Windows Vista ou ao Windows Server 2008 esteja executando a instalação.</span><span class="sxs-lookup"><span data-stu-id="c26bc-111">A Windows Installer version that is not earlier than version 4.0 and an operating system that is not earlier than Windows Vista or Windows Server 2008 is running the installation.</span></span>
-   <span data-ttu-id="c26bc-112">O nível completo da [interface do usuário](user-interface-levels.md) da interface é usado.</span><span class="sxs-lookup"><span data-stu-id="c26bc-112">The Full UI [user interface level](user-interface-levels.md) is used.</span></span>
-   <span data-ttu-id="c26bc-113">As interações com o [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) não foram desabilitadas pela propriedade [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md) ou pela política [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="c26bc-113">Interactions with the [Restart Manager](../rstmgr/restart-manager-portal.md) have not been disabled by the [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md) property or the [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) policy.</span></span>
-   <span data-ttu-id="c26bc-114">A caixa de diálogo **MsiRMFilesInUse** está presente no pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="c26bc-114">The **MsiRMFilesInUse** dialog box is present in the installation package.</span></span>
-   <span data-ttu-id="c26bc-115">Todas as chamadas do Windows Installer para o [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md) são bem-sucedidas.</span><span class="sxs-lookup"><span data-stu-id="c26bc-115">All calls from the Windows Installer to the [Restart Manager](../rstmgr/restart-manager-portal.md) are successful.</span></span>

<span data-ttu-id="c26bc-116">Essa caixa de diálogo será criada conforme exigido pela [ação InstallValidate](installvalidate-action.md).</span><span class="sxs-lookup"><span data-stu-id="c26bc-116">This dialog box will be created as required by the [InstallValidate action](installvalidate-action.md).</span></span>

 

 

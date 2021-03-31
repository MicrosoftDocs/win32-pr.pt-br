---
description: Você pode usar \_ o processo Win32. Create para executar um script ou aplicativo em um computador remoto. No entanto, por motivos de segurança, o processo não pode ser interativo. Quando \_ o processo Win32. Create é chamado no computador local, o processo pode ser interativo.
ms.assetid: 11fea8b1-7d05-4f44-9103-ea804a1d4b38
ms.tgt_platform: multiple
title: Criando processos remotamente usando o WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55e7b97f8f4fdddd608f6ee8c3368bde6ad6e854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662904"
---
# <a name="creating-processes-remotely-using-wmi"></a><span data-ttu-id="c0695-105">Criando processos remotamente usando o WMI</span><span class="sxs-lookup"><span data-stu-id="c0695-105">Creating Processes Remotely using WMI</span></span>

<span data-ttu-id="c0695-106">Você pode usar [**o \_ processo Win32. Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) para executar um script ou aplicativo em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="c0695-106">You can use [**Win32\_Process.Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) to execute a script or application on a remote computer.</span></span> <span data-ttu-id="c0695-107">No entanto, por motivos de segurança, o processo não pode ser interativo.</span><span class="sxs-lookup"><span data-stu-id="c0695-107">However, for security reasons, the process cannot be interactive.</span></span> <span data-ttu-id="c0695-108">Quando **o \_ processo Win32. Create** é chamado no computador local, o processo pode ser interativo.</span><span class="sxs-lookup"><span data-stu-id="c0695-108">When **Win32\_Process.Create** is called on the local computer, the process can be interactive.</span></span>

> [!WARNING]
> <span data-ttu-id="c0695-109">Este tópico descreve o procedimento geral para criar um processo remoto com o WMI.</span><span class="sxs-lookup"><span data-stu-id="c0695-109">This topic describes the general procedure for creating a remote process with WMI.</span></span> <span data-ttu-id="c0695-110">Se você estiver simplesmente procurando executar um script em um sistema remoto, consulte [conectando-se ao WMI remotamente a partir do Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md)ou [conectando-se ao WMI em um computador remoto usando o Windows PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="c0695-110">If you are simply looking to run a script on a remote system, see [Connecting to WMI Remotely Starting with Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md), or [Connecting to WMI on a Remote Computer by Using Windows PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).</span></span> <span data-ttu-id="c0695-111">Para obter mais informações gerais sobre a comunicação remota com o PowerShell, consulte [executando comandos remotos](https://technet.microsoft.com/library/dd819505.aspx).</span><span class="sxs-lookup"><span data-stu-id="c0695-111">For more general information on remoting with PowerShell, see [Running Remote Commands](https://technet.microsoft.com/library/dd819505.aspx).</span></span>

 

<span data-ttu-id="c0695-112">O processo remoto não tem nenhuma interface do usuário, mas está listado no **Gerenciador de tarefas**.</span><span class="sxs-lookup"><span data-stu-id="c0695-112">The remote process has no user interface but it is listed in the **Task Manager**.</span></span> <span data-ttu-id="c0695-113">Um processo criado localmente pode ser executado em qualquer conta se a conta tiver a permissão **Executar método** para o \\ namespace raiz cimv2.</span><span class="sxs-lookup"><span data-stu-id="c0695-113">A process created locally can run under any account if the account has the **Execute Method** permission for the root\\cimv2 namespace.</span></span> <span data-ttu-id="c0695-114">Um processo criado remotamente pode ser executado em qualquer conta se a conta tiver o **método execute** e permissões **habilitar remotas** para raiz \\ cimv2.</span><span class="sxs-lookup"><span data-stu-id="c0695-114">A process created remotely can run under any account if the account has the **Execute Method** and **Remote Enable** permissions for root\\cimv2.</span></span> <span data-ttu-id="c0695-115">As permissões **Executar método** e **habilitar remoto** são definidas no controle WMI no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="c0695-115">The **Execute Method** and **Remote Enable** permissions are set in WMI Control in the Control Panel.</span></span> <span data-ttu-id="c0695-116">Para obter mais informações, consulte [definindo a segurança do namespace com o controle WMI](setting-namespace-security-with-the-wmi-control.md).</span><span class="sxs-lookup"><span data-stu-id="c0695-116">For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>

<span data-ttu-id="c0695-117">Você pode usar o [**Win32 \_ ScheduledJob. Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob) para criar um processo interativo remotamente.</span><span class="sxs-lookup"><span data-stu-id="c0695-117">You can use [**Win32\_ScheduledJob.Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob) to create an interactive process remotely.</span></span> <span data-ttu-id="c0695-118">Mas processos iniciados pelo **Win32 \_ ScheduledJob. Crie** uma execução sob a conta LocalSystem que pode confere muito privilégios.</span><span class="sxs-lookup"><span data-stu-id="c0695-118">But processes started by **Win32\_ScheduledJob.Create** run under the LocalSystem account that can confer too much privilege.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0695-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c0695-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0695-120">Protegendo uma conexão WMI remota</span><span class="sxs-lookup"><span data-stu-id="c0695-120">Securing a Remote WMI Connection</span></span>](securing-a-remote-wmi-connection.md)
</dt> <dt>

[<span data-ttu-id="c0695-121">Conectando-se a um terceiro computador – delegação</span><span class="sxs-lookup"><span data-stu-id="c0695-121">Connecting to a 3rd Computer-Delegation</span></span>](connecting-to-a-3rd-computer-delegation.md)
</dt> </dl>

 

 

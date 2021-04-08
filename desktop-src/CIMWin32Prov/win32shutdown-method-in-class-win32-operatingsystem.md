---
description: Win32Shutdown &\# 8194; O método de classe WMI fornece o conjunto completo de opções de desligamento com suporte dos sistemas operacionais Win32. Isso inclui fazer logoff, desligamento, reinicialização e forçar um logoff, desligamento ou reinicialização.
ms.assetid: 7108570a-81ba-46d5-8b05-de6194f93f18
ms.tgt_platform: multiple
title: Método Win32Shutdown da classe Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Win32Shutdown
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f2cca60c376859438b40ca35be26a99b115634c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826615"
---
# <a name="win32shutdown-method-of-the-win32_operatingsystem-class"></a><span data-ttu-id="a5639-104">Método Win32Shutdown da classe de sistema \_ operacional Win32</span><span class="sxs-lookup"><span data-stu-id="a5639-104">Win32Shutdown method of the Win32\_OperatingSystem class</span></span>

<span data-ttu-id="a5639-105">O método de   [classe WMI](../wmisdk/retrieving-a-class.md) **Win32Shutdown** fornece o conjunto completo de opções de desligamento com suporte dos sistemas operacionais Win32.</span><span class="sxs-lookup"><span data-stu-id="a5639-105">The **Win32Shutdown**   [WMI class](../wmisdk/retrieving-a-class.md) method provides the full set of shutdown options supported by Win32 operating systems.</span></span> <span data-ttu-id="a5639-106">Isso inclui fazer logoff, desligamento, reinicialização e forçar um logoff, desligamento ou reinicialização.</span><span class="sxs-lookup"><span data-stu-id="a5639-106">These include logoff, shutdown, reboot, and forcing a logoff, shutdown, or reboot.</span></span>

<span data-ttu-id="a5639-107">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="a5639-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a5639-108">Para obter mais informações sobre como usar esse método, consulte [chamando um método](../wmisdk/calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="a5639-108">For more information about using this method, see [Calling a Method](../wmisdk/calling-a-method.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a5639-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a5639-109">Syntax</span></span>


```mof
uint32 Win32Shutdown(
  [in] sint32 Flags,
  [in] sint32 Reserved = 
);
```



## <a name="parameters"></a><span data-ttu-id="a5639-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a5639-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5639-111">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="a5639-111">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5639-112">Conjunto de sinalizadores de bitmap para desligar o computador.</span><span class="sxs-lookup"><span data-stu-id="a5639-112">Bitmapped set of flags to shut the computer down.</span></span> <span data-ttu-id="a5639-113">Para forçar um comando, adicione o sinalizador Force (4) ao valor do comando.</span><span class="sxs-lookup"><span data-stu-id="a5639-113">To force a command, add the Force flag (4) to the command value.</span></span> <span data-ttu-id="a5639-114">O uso da força em conjunto com o desligamento ou reinicialização em um computador remoto desliga imediatamente tudo (incluindo WMI, COM e assim por diante) ou reinicia o computador remoto.</span><span class="sxs-lookup"><span data-stu-id="a5639-114">Using Force in conjunction with Shutdown or Reboot on a remote computer immediately shuts down everything (including WMI, COM, and so on), or reboots the remote computer.</span></span> <span data-ttu-id="a5639-115">Isso resulta em um valor de retorno indeterminado.</span><span class="sxs-lookup"><span data-stu-id="a5639-115">This results in an indeterminate return value.</span></span>

<dt>

<span data-ttu-id="a5639-116">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="a5639-116">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="a5639-117">**Logoff – faz** logoff do usuário no computador.</span><span class="sxs-lookup"><span data-stu-id="a5639-117">**Log Off** - Logs the user off the computer.</span></span> <span data-ttu-id="a5639-118">O logoff interrompe todos os processos associados ao contexto de segurança do processo que chamou a função Exit, registra o usuário atual fora do sistema e exibe a caixa de diálogo de logon.</span><span class="sxs-lookup"><span data-stu-id="a5639-118">Logging off stops all processes associated with the security context of the process that called the exit function, logs the current user off the system, and displays the logon dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="a5639-119">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="a5639-119">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="a5639-120">Logoff **forçado (0 + 4)** – registra o usuário no computador imediatamente e não notifica os aplicativos que a sessão de logon está encerrando.</span><span class="sxs-lookup"><span data-stu-id="a5639-120">**Forced Log Off (0 + 4)** - Logs the user off the computer immediately and does not notify applications that the logon session is ending.</span></span> <span data-ttu-id="a5639-121">Isso pode resultar em perda de dados.</span><span class="sxs-lookup"><span data-stu-id="a5639-121">This can result in a loss of data.</span></span>

</dd> <dt>

<span data-ttu-id="a5639-122">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="a5639-122">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="a5639-123">**Desligar** – desliga o computador a um ponto em que é seguro desligar o poder.</span><span class="sxs-lookup"><span data-stu-id="a5639-123">**Shutdown** - Shuts down the computer to a point where it is safe to turn off the power.</span></span> <span data-ttu-id="a5639-124">(Todos os buffers de arquivo são liberados para o disco e todos os processos em execução são interrompidos.) Os usuários veem a mensagem, `It is now safe to turn off your computer.`</span><span class="sxs-lookup"><span data-stu-id="a5639-124">(All file buffers are flushed to disk, and all running processes are stopped.) Users see the message, `It is now safe to turn off your computer.`</span></span>

<span data-ttu-id="a5639-125">Durante o desligamento, o sistema envia uma mensagem para cada aplicativo em execução.</span><span class="sxs-lookup"><span data-stu-id="a5639-125">During shutdown the system sends a message to each running application.</span></span> <span data-ttu-id="a5639-126">Os aplicativos executam qualquer limpeza durante o processamento da mensagem e retornam true para indicar que eles podem ser encerrados.</span><span class="sxs-lookup"><span data-stu-id="a5639-126">The applications perform any cleanup while processing the message and return True to indicate that they can be terminated.</span></span>

</dd> <dt>

<span data-ttu-id="a5639-127">5 (0x5)</span><span class="sxs-lookup"><span data-stu-id="a5639-127">5 (0x5)</span></span>
</dt> <dd>

<span data-ttu-id="a5639-128">**Desligamento forçado (1 + 4)** – desliga o computador a um ponto em que é seguro desligar o poder.</span><span class="sxs-lookup"><span data-stu-id="a5639-128">**Forced Shutdown (1 + 4)** - Shuts down the computer to a point where it is safe to turn off the power.</span></span> <span data-ttu-id="a5639-129">(Todos os buffers de arquivo são liberados para o disco e todos os processos em execução são interrompidos.) Os usuários veem a mensagem,` It is now safe to turn off your computer.`</span><span class="sxs-lookup"><span data-stu-id="a5639-129">(All file buffers are flushed to disk, and all running processes are stopped.) Users see the message,` It is now safe to turn off your computer.`</span></span>

<span data-ttu-id="a5639-130">Quando a abordagem de desligamento forçado é usada, todos os serviços, incluindo WMI, são desligados imediatamente.</span><span class="sxs-lookup"><span data-stu-id="a5639-130">When the forced shutdown approach is used, all services, including WMI, are shut down immediately.</span></span> <span data-ttu-id="a5639-131">Por isso, não será possível receber um valor de retorno se você estiver executando o script em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="a5639-131">Because of this, you will not be able to receive a return value if you are running the script against a remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="a5639-132">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="a5639-132">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="a5639-133">**Reinicializar** – desliga e reinicia o computador.</span><span class="sxs-lookup"><span data-stu-id="a5639-133">**Reboot** - Shuts down and then restarts the computer.</span></span>

</dd> <dt>

<span data-ttu-id="a5639-134">6 (0x6)</span><span class="sxs-lookup"><span data-stu-id="a5639-134">6 (0x6)</span></span>
</dt> <dd>

<span data-ttu-id="a5639-135">**Reinicialização forçada (2 + 4)** – desliga e reinicia o computador.</span><span class="sxs-lookup"><span data-stu-id="a5639-135">**Forced Reboot (2 + 4)** - Shuts down and then restarts the computer.</span></span>

<span data-ttu-id="a5639-136">Quando a abordagem de reinicialização forçada é usada, todos os serviços, incluindo WMI, são desligados imediatamente.</span><span class="sxs-lookup"><span data-stu-id="a5639-136">When the forced reboot approach is used, all services, including WMI, are shut down immediately.</span></span> <span data-ttu-id="a5639-137">Por isso, não será possível receber um valor de retorno se você estiver executando o script em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="a5639-137">Because of this, you will not be able to receive a return value if you are running the script against a remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="a5639-138">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="a5639-138">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="a5639-139">**Desligar – desliga** o computador e desliga a energia (se houver suporte do computador em questão).</span><span class="sxs-lookup"><span data-stu-id="a5639-139">**Power Off** - Shuts down the computer and turns off the power (if supported by the computer in question).</span></span>

</dd> <dt>

<span data-ttu-id="a5639-140">12 (0xC)</span><span class="sxs-lookup"><span data-stu-id="a5639-140">12 (0xC)</span></span>
</dt> <dd>

<span data-ttu-id="a5639-141">Desligamento **forçado (8 + 4)** – desliga o computador e desliga a energia (se houver suporte para o computador em questão).</span><span class="sxs-lookup"><span data-stu-id="a5639-141">**Forced Power Off (8 + 4)** - Shuts down the computer and turns off the power (if supported by the computer in question).</span></span>

<span data-ttu-id="a5639-142">Quando a abordagem de desligamento forçado é usada, todos os serviços, incluindo WMI, são desligados imediatamente.</span><span class="sxs-lookup"><span data-stu-id="a5639-142">When the forced power off approach is used, all services, including WMI, are shut down immediately.</span></span> <span data-ttu-id="a5639-143">Por isso, não será possível receber um valor de retorno se você estiver executando o script em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="a5639-143">Because of this, you will not be able to receive a return value if you are running the script against a remote computer.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a5639-144">*Reservado* \[ para no\]</span><span class="sxs-lookup"><span data-stu-id="a5639-144">*Reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5639-145">Um meio para estender **Win32Shutdown**.</span><span class="sxs-lookup"><span data-stu-id="a5639-145">A means to extend **Win32Shutdown**.</span></span> <span data-ttu-id="a5639-146">Atualmente, o parâmetro *reservado* é ignorado.</span><span class="sxs-lookup"><span data-stu-id="a5639-146">Currently, the *Reserved* parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5639-147">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a5639-147">Return value</span></span>

<span data-ttu-id="a5639-148">Retorna zero (0) para indicar êxito.</span><span class="sxs-lookup"><span data-stu-id="a5639-148">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="a5639-149">Qualquer outro número indica um erro.</span><span class="sxs-lookup"><span data-stu-id="a5639-149">Any other number indicates an error.</span></span> <span data-ttu-id="a5639-150">Para códigos de erro, consulte [**constantes de erro WMI**](../wmisdk/wmi-error-constants.md) ou [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="a5639-150">For error codes, see [**WMI Error Constants**](../wmisdk/wmi-error-constants.md) or [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="a5639-151">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](../debug/system-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a5639-151">For general **HRESULT** values, see [System Error Codes](../debug/system-error-codes.md).</span></span>

<dl> <dt>

<span data-ttu-id="a5639-152">**Êxito** (0)</span><span class="sxs-lookup"><span data-stu-id="a5639-152">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a5639-153">**Outro** (1 a 4294967295)</span><span class="sxs-lookup"><span data-stu-id="a5639-153">**Other** (1–4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="a5639-154">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5639-154">Remarks</span></span>

<span data-ttu-id="a5639-155">Para um gerenciamento mais eficiente de computadores em uma organização, os administradores precisam da capacidade de desligar ou reiniciar remotamente um computador ou fazer logoff remoto de um usuário.</span><span class="sxs-lookup"><span data-stu-id="a5639-155">For more efficient management of computers in an organization, administrators need the ability to remotely shut down or restart a computer, or to remotely log off a user.</span></span> <span data-ttu-id="a5639-156">A capacidade de realizar essas tarefas permite que os administradores instalem software, reconfigurem as configurações do computador, removam computadores da rede e executem outras tarefas sem precisar desligar ou reiniciar manualmente cada computador.</span><span class="sxs-lookup"><span data-stu-id="a5639-156">The ability to carry out these tasks allows administrators to install software, reconfigure computer settings, remove computers from the network, and perform other tasks without having to manually shut down or restart each computer.</span></span>

<span data-ttu-id="a5639-157">Por exemplo, para executar uma atualização de rede, talvez seja necessário desligar todos os computadores em execução em um segmento de rede específico.</span><span class="sxs-lookup"><span data-stu-id="a5639-157">For example, to perform a network upgrade, you might need to shut down all the computers running on a particular network segment.</span></span> <span data-ttu-id="a5639-158">Para forçar uma atualização de Política de Grupo, você precisa registrar os usuários em seus computadores.</span><span class="sxs-lookup"><span data-stu-id="a5639-158">To force a Group Policy upgrade, you need to log users off their computers.</span></span> <span data-ttu-id="a5639-159">Se um vírus de computador estiver presente em qualquer lugar da sua organização, talvez você queira desligar o máximo possível de computadores, antes que o vírus tenha a oportunidade de se espalhar.</span><span class="sxs-lookup"><span data-stu-id="a5639-159">If a computer virus is present anywhere in your organization, you might want to shut down as many computers as possible, before the virus has an opportunity to spread.</span></span> <span data-ttu-id="a5639-160">A capacidade de desligar e reiniciar computadores e fazer logoff de usuários programaticamente em vez de manualmente pode ser um enorme economia de tempo.</span><span class="sxs-lookup"><span data-stu-id="a5639-160">The ability to shut down and restart computers and to log off users programmatically instead of manually can be an enormous time-saver.</span></span>

<span data-ttu-id="a5639-161">O processo de chamada deve ter o privilégio de **\_ \_ nome de desligamento se** .</span><span class="sxs-lookup"><span data-stu-id="a5639-161">The calling process must have the **SE\_SHUTDOWN\_NAME** privilege.</span></span>

<span data-ttu-id="a5639-162">O método [**Win32ShutdownTracker**](win32shutdowntracker-method-in-class-win32-operatingsystem.md) fornece o mesmo conjunto de opções de desligamento com suporte pelo método **Win32Shutdown** no sistema [**\_ operacional Win32**](win32-operatingsystem.md) , mas também permite que você especifique comentários, um motivo para o desligamento ou um tempo limite.</span><span class="sxs-lookup"><span data-stu-id="a5639-162">The [**Win32ShutdownTracker**](win32shutdowntracker-method-in-class-win32-operatingsystem.md) method provides the same set of shutdown options supported by the **Win32Shutdown** method in [**Win32\_OperatingSystem**](win32-operatingsystem.md) but it also allows you to specify comments, a reason for shutdown, or a timeout.</span></span>

<span data-ttu-id="a5639-163">O método Win32Shutdown não tem um parâmetro para bloquear uma estação de trabalho, deixando o usuário conectado.</span><span class="sxs-lookup"><span data-stu-id="a5639-163">The Win32Shutdown method does not have a parameter for locking a workstation, leaving the user logged on.</span></span> <span data-ttu-id="a5639-164">No entanto, as estações de trabalho podem ser bloqueadas na linha de comando usando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="a5639-164">However, workstations can be locked from the command line by using the following command:</span></span>

`% windir %\System32\rundll32.exe user32.dll,LockWorkStation`

## <a name="examples"></a><span data-ttu-id="a5639-165">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a5639-165">Examples</span></span>

<span data-ttu-id="a5639-166">O exemplo do VBScript [fazer logoff, reinicializar ou desligar vários computadores](https://Gallery.TechNet.Microsoft.Com/2e88d504-a4e5-499b-b09a-f90617a6d87d) na galeria do TechNet usa Win32Shutdown para fazer logoff, desligar, reinicializar ou desligar (dependendo da seleção) os computadores listados na matriz de servidores.</span><span class="sxs-lookup"><span data-stu-id="a5639-166">The [Log Out, Reboot, or Shut Down Multiple Computers](https://Gallery.TechNet.Microsoft.Com/2e88d504-a4e5-499b-b09a-f90617a6d87d) VBScript sample on TechNet Gallery uses Win32Shutdown to log off, shut down, reboot, or power off (depending on the selection) the computers listed in the Server array.</span></span>

<span data-ttu-id="a5639-167">O [ComputerManagement.ps1](https://Gallery.TechNet.Microsoft.Com/ef8de213-45b6-4751-8c77-01d1b6623e16) exemplo do PowerShell na galeria do TechNet inclui um método que chama Win32Shutdown em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="a5639-167">The [ComputerManagement.ps1](https://Gallery.TechNet.Microsoft.Com/ef8de213-45b6-4751-8c77-01d1b6623e16) PowerShell sample on TechNet Gallery includes a method that calls Win32Shutdown on a remote computer.</span></span>

<span data-ttu-id="a5639-168">O exemplo do PowerShell a seguir usa o método Win32Shutdown para desligar o computador especificado.</span><span class="sxs-lookup"><span data-stu-id="a5639-168">The following PowerShell example uses the Win32Shutdown method to shut down the specified computer.</span></span>


```PowerShell
$computername= "."
$win32OS = get-wmiobject win32_operatingsystem -computername $computername
$win32OS.psbase.Scope.Options.EnablePrivileges = $true
$win32OS.win32shutdown(8)
```



<span data-ttu-id="a5639-169">O exemplo de código do PowerShell a seguir usa o EnableAllPrivileges do cmdlet Get-WmiObject para atingir os privilégios apropriados.</span><span class="sxs-lookup"><span data-stu-id="a5639-169">The following PowerShell code sample uses the EnableAllPrivileges from get-wmiobject cmdlet to achieve the proper priviliges.</span></span>


```PowerShell
$win32OS = get-wmiobject win32_operatingsystem -computername $computername -EnableAllPrivileges
$win32OS.win32shutdown(8)
```



<span data-ttu-id="a5639-170">O código de exemplo VB.NET a seguir usa o método Shutdown para reinicializar ou fazer logoff de um sistema.</span><span class="sxs-lookup"><span data-stu-id="a5639-170">The following VB.NET sample code uses the Shutdown method to reboot or log off a system.</span></span>


```VB
Dim

testResult AsSingle

Dim WMIServiceObject, ComputerObject AsObject 

'Now get some privileges 

WMIServiceObject = GetObject(
"Winmgmts:{impersonationLevel=impersonate,(Debug,Shutdown)}")
ForEach ComputerObject In WMIServiceObject.InstancesOf("Win32_OperatingSystem") 
    testResult = ComputerObject.Win32Shutdown(2 + 4, 0) 
    'reboot
    'testResult = ComputerObject.Win32Shutdown(0, 0) 'logoff 
    ' testResult = ComputerObject.Win32Shutdown(8 + 4, 0) 'shutdown 

If testResult <> 0 Then 

MsgBox("Sorry, an error has occurred while trying to perform selected operation") 

Else 

'Operation selected in statement above if condition would be carried out 

EndIf 

Next
```



## <a name="requirements"></a><span data-ttu-id="a5639-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5639-171">Requirements</span></span>



| <span data-ttu-id="a5639-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5639-172">Requirement</span></span> | <span data-ttu-id="a5639-173">Valor</span><span class="sxs-lookup"><span data-stu-id="a5639-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5639-174">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5639-174">Minimum supported client</span></span><br/> | <span data-ttu-id="a5639-175">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a5639-175">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a5639-176">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5639-176">Minimum supported server</span></span><br/> | <span data-ttu-id="a5639-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a5639-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a5639-178">Namespace</span><span class="sxs-lookup"><span data-stu-id="a5639-178">Namespace</span></span><br/>                | <span data-ttu-id="a5639-179">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a5639-179">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a5639-180">MOF</span><span class="sxs-lookup"><span data-stu-id="a5639-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a5639-181"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a5639-181"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a5639-182">DLL</span><span class="sxs-lookup"><span data-stu-id="a5639-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5639-183"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5639-183"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5639-184">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5639-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5639-185">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="a5639-185">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="a5639-186">**Sistema \_ operacional Win32**</span><span class="sxs-lookup"><span data-stu-id="a5639-186">**Win32\_OperatingSystem**</span></span>](win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="a5639-187">**Win32ShutdownTracker**</span><span class="sxs-lookup"><span data-stu-id="a5639-187">**Win32ShutdownTracker**</span></span>](win32shutdowntracker-method-in-class-win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="a5639-188">Tarefas do WMI: gerenciamento de desktop</span><span class="sxs-lookup"><span data-stu-id="a5639-188">WMI Tasks: Desktop Management</span></span>](../wmisdk/wmi-tasks--desktop-management.md)
</dt> <dt>

[<span data-ttu-id="a5639-189">Executando operações privilegiadas usando o VBScript</span><span class="sxs-lookup"><span data-stu-id="a5639-189">Executing Privileged Operations Using VBScript</span></span>](../wmisdk/executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

 

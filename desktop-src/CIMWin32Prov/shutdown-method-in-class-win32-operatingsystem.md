---
description: O desligamento&\# 8194; O método de classe WMI descarrega programas e DLLs até que seja seguro desligar o computador.
ms.assetid: 3f069699-810c-49bc-b77e-3fe43acc3dd5
ms.tgt_platform: multiple
title: Método Shutdown da classe Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Shutdown
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: af80442087a0498849388f0da10946b08e282712
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457186"
---
# <a name="shutdown-method-of-the-win32_operatingsystem-class"></a><span data-ttu-id="ca8fc-103">Método Shutdown da classe do sistema \_ operacional Win32</span><span class="sxs-lookup"><span data-stu-id="ca8fc-103">Shutdown method of the Win32\_OperatingSystem class</span></span>

<span data-ttu-id="ca8fc-104">O método **Shutdown** da [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) descarrega programas e DLLs até que seja seguro desligar o computador.</span><span class="sxs-lookup"><span data-stu-id="ca8fc-104">The **Shutdown** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method unloads programs and DLLs until it is safe to turn off the computer.</span></span>

<span data-ttu-id="ca8fc-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="ca8fc-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ca8fc-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ca8fc-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ca8fc-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca8fc-107">Syntax</span></span>


```mof
uint32 Shutdown();
```



## <a name="parameters"></a><span data-ttu-id="ca8fc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca8fc-108">Parameters</span></span>

<span data-ttu-id="ca8fc-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ca8fc-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ca8fc-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ca8fc-110">Return value</span></span>

<span data-ttu-id="ca8fc-111">Retorna zero (0) para indicar êxito.</span><span class="sxs-lookup"><span data-stu-id="ca8fc-111">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="ca8fc-112">Qualquer outro número indica um erro.</span><span class="sxs-lookup"><span data-stu-id="ca8fc-112">Any other number indicates an error.</span></span> <span data-ttu-id="ca8fc-113">Para códigos de erro, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="ca8fc-113">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="ca8fc-114">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="ca8fc-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="ca8fc-115">**Êxito** (0)</span><span class="sxs-lookup"><span data-stu-id="ca8fc-115">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ca8fc-116">**Outro** (1 4294967295)</span><span class="sxs-lookup"><span data-stu-id="ca8fc-116">**Other** (1 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="ca8fc-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca8fc-117">Remarks</span></span>

<span data-ttu-id="ca8fc-118">Ocasionalmente, os computadores precisam ser removidos da rede, talvez para manutenção agendada, porque o computador não está funcionando corretamente ou para concluir um processo de configuração.</span><span class="sxs-lookup"><span data-stu-id="ca8fc-118">Computers occasionally need to be removed from the network, perhaps for scheduled maintenance, because the computer is not functioning correctly, or to complete a configuration process.</span></span> <span data-ttu-id="ca8fc-119">Por exemplo, se um servidor DHCP estiver distribuindo endereços IP errados, talvez você queira desligar o computador até que um técnico de serviço possa ser expedido para corrigir o problema.</span><span class="sxs-lookup"><span data-stu-id="ca8fc-119">For example, if a DHCP server is handing out erroneous IP addresses, you might want to shut the computer down until a service technician can be dispatched to fix the problem.</span></span> <span data-ttu-id="ca8fc-120">Se você suspeitar de que ocorreu uma violação de segurança, talvez seja necessário desligar determinados servidores para garantir que eles não possam ser acessados até que o problema de segurança seja resolvido.</span><span class="sxs-lookup"><span data-stu-id="ca8fc-120">If you suspect that a security breach has occurred, you might need to shut down certain servers to ensure that they cannot be accessed until the security issue has been resolved.</span></span> <span data-ttu-id="ca8fc-121">Algumas operações de configuração (como alterar um nome de computador) exigem que você reinicie o computador antes que a alteração entre em vigor.</span><span class="sxs-lookup"><span data-stu-id="ca8fc-121">Some configuration operations (such as changing a computer name) require you to restart the computer before the change takes effect.</span></span>

<span data-ttu-id="ca8fc-122">Esse método desliga imediatamente o computador, se possível.</span><span class="sxs-lookup"><span data-stu-id="ca8fc-122">This method immediately shuts the computer down, if possible.</span></span> <span data-ttu-id="ca8fc-123">O sistema interrompe todos os processos em execução, libera todos os buffers de arquivo para o disco e desliga o sistema.</span><span class="sxs-lookup"><span data-stu-id="ca8fc-123">The system stops all running processes, flushes all file buffers to the disk, and then powers down the system.</span></span> <span data-ttu-id="ca8fc-124">O processo de chamada deve ter o privilégio de **\_ \_ nome de desligamento se** , conforme descrito no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="ca8fc-124">The calling process must have the **SE\_SHUTDOWN\_NAME** privilege, as described in the following example.</span></span>


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")
```



<span data-ttu-id="ca8fc-125">Para obter mais informações sobre como definir um privilégio, consulte [executando operações privilegiadas](/windows/desktop/WmiSdk/executing-privileged-operations) e [executando operações privilegiadas usando o VBScript](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript).</span><span class="sxs-lookup"><span data-stu-id="ca8fc-125">For more information on setting a privilege, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations) and [Executing Privileged Operations Using VBScript](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript).</span></span> <span data-ttu-id="ca8fc-126">Para obter opções de desligamento adicionais, como um logoff ou um desligamento forçado, consulte o método [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) .</span><span class="sxs-lookup"><span data-stu-id="ca8fc-126">For additional shutdown options, such as a logoff or a forced shutdown, see the [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="ca8fc-127">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ca8fc-127">Examples</span></span>

<span data-ttu-id="ca8fc-128">O código VBScript a seguir desliga o computador local.</span><span class="sxs-lookup"><span data-stu-id="ca8fc-128">The following VBScript code shuts the local computer down.</span></span>

> [!Note]  
> <span data-ttu-id="ca8fc-129">Você deve ter o privilégio de desligamento para invocar com êxito o método de desligamento.</span><span class="sxs-lookup"><span data-stu-id="ca8fc-129">You must have the Shutdown privilege to successfully invoke the Shutdown method.</span></span>

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Shutdown()
next
```



<span data-ttu-id="ca8fc-130">O código Perl a seguir desliga o computador local.</span><span class="sxs-lookup"><span data-stu-id="ca8fc-130">The following Perl code shuts the local computer down.</span></span>

> [!Note]  
> <span data-ttu-id="ca8fc-131">Você deve ter o privilégio de desligamento para invocar com êxito o método de desligamento.</span><span class="sxs-lookup"><span data-stu-id="ca8fc-131">You must have the Shutdown privilege to successfully invoke the Shutdown method.</span></span>

 


```
use strict;
use Win32::OLE;

my $OpSysSet;

eval { $OpSysSet = Win32::OLE->GetObject("winmgmts:{(Shutdown)}//./root/cimv2")->
      ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true"); };

if(!$@ && defined $OpSysSet)
{
 close (STDERR);
 foreach my $OpSys (in $OpSysSet)
 {
  my $RetVal = $OpSys->Shutdown();
  if (!defined $RetVal || $RetVal != 0)
  { 
   print Win32::OLE->LastError, "\n";
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="ca8fc-132">O código VBScript a seguir desliga o computador remoto especificado.</span><span class="sxs-lookup"><span data-stu-id="ca8fc-132">The following VBScript code shuts the specified remote computer down.</span></span> <span data-ttu-id="ca8fc-133">Preencha o *\_ \_ nome do sistema remoto* com o nome do sistema remoto para desligar.</span><span class="sxs-lookup"><span data-stu-id="ca8fc-133">Fill in *REMOTE\_SYSTEM\_NAME* with the name of the remote system to shutdown.</span></span>

> [!Note]  
> <span data-ttu-id="ca8fc-134">Você deve ter o privilégio RemoteShutdown para invocar com êxito o método **Shutdown** .</span><span class="sxs-lookup"><span data-stu-id="ca8fc-134">You must have the RemoteShutdown privilege to successfully invoke the **Shutdown** method.</span></span>

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Debug,RemoteShutdown)}//REMOTE_SYSTEM_NAME/root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Shutdown()
next
```



## <a name="requirements"></a><span data-ttu-id="ca8fc-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca8fc-135">Requirements</span></span>



| <span data-ttu-id="ca8fc-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca8fc-136">Requirement</span></span> | <span data-ttu-id="ca8fc-137">Valor</span><span class="sxs-lookup"><span data-stu-id="ca8fc-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca8fc-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca8fc-138">Minimum supported client</span></span><br/> | <span data-ttu-id="ca8fc-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ca8fc-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ca8fc-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca8fc-140">Minimum supported server</span></span><br/> | <span data-ttu-id="ca8fc-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ca8fc-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ca8fc-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="ca8fc-142">Namespace</span></span><br/>                | <span data-ttu-id="ca8fc-143">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ca8fc-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ca8fc-144">MOF</span><span class="sxs-lookup"><span data-stu-id="ca8fc-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca8fc-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca8fc-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca8fc-146">DLL</span><span class="sxs-lookup"><span data-stu-id="ca8fc-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca8fc-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca8fc-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca8fc-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca8fc-148">See also</span></span>

<dl> <dt>

<span data-ttu-id="ca8fc-149">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ca8fc-149">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ca8fc-150">**Sistema \_ operacional Win32**</span><span class="sxs-lookup"><span data-stu-id="ca8fc-150">**Win32\_OperatingSystem**</span></span>](win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="ca8fc-151">Tarefas do WMI: gerenciamento de desktop</span><span class="sxs-lookup"><span data-stu-id="ca8fc-151">WMI Tasks: Desktop Management</span></span>](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> <dt>

[<span data-ttu-id="ca8fc-152">Executando operações privilegiadas usando o VBScript</span><span class="sxs-lookup"><span data-stu-id="ca8fc-152">Executing Privileged Operations Using VBScript</span></span>](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript)
</dt> </dl>

 


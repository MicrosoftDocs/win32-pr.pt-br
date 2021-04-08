---
description: A reinicialização&\# 8194; O método de classe WMI desliga o sistema de computador e, em seguida, o reinicia.
ms.assetid: 23b70f2a-28ce-4463-9d22-29de52349ab6
ms.tgt_platform: multiple
title: Método reboot da classe Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Reboot
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c4577f708d2f7ec7416ab3455da91b4e35fa079a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920508"
---
# <a name="reboot-method-of-the-win32_operatingsystem-class"></a><span data-ttu-id="012aa-103">Método reboot da classe de sistema \_ operacional Win32</span><span class="sxs-lookup"><span data-stu-id="012aa-103">Reboot method of the Win32\_OperatingSystem class</span></span>

<span data-ttu-id="012aa-104">O método **reinicializar** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) desliga o sistema de computador e, em seguida, o reinicia.</span><span class="sxs-lookup"><span data-stu-id="012aa-104">The **Reboot** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method shuts down the computer system, then restarts it.</span></span>

<span data-ttu-id="012aa-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="012aa-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="012aa-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="012aa-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="012aa-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="012aa-107">Syntax</span></span>


```mof
uint32 Reboot();
```



## <a name="parameters"></a><span data-ttu-id="012aa-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="012aa-108">Parameters</span></span>

<span data-ttu-id="012aa-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="012aa-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="012aa-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="012aa-110">Return value</span></span>

<span data-ttu-id="012aa-111">Retorna zero (0) para indicar êxito.</span><span class="sxs-lookup"><span data-stu-id="012aa-111">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="012aa-112">Qualquer outro número indica um erro.</span><span class="sxs-lookup"><span data-stu-id="012aa-112">Any other number indicates an error.</span></span> <span data-ttu-id="012aa-113">Para códigos de erro, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="012aa-113">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="012aa-114">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="012aa-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="012aa-115">**Êxito** (0)</span><span class="sxs-lookup"><span data-stu-id="012aa-115">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="012aa-116">**Outro** (1 4294967295)</span><span class="sxs-lookup"><span data-stu-id="012aa-116">**Other** (1 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="012aa-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="012aa-117">Remarks</span></span>

<span data-ttu-id="012aa-118">A capacidade de reiniciar programaticamente um computador permite que os administradores executem muitas tarefas de gerenciamento do computador remotamente.</span><span class="sxs-lookup"><span data-stu-id="012aa-118">The ability to programmatically restart a computer allows administrators to perform many computer management tasks remotely.</span></span>

<span data-ttu-id="012aa-119">Por exemplo, se você criar um script para instalar o software ou fazer uma alteração de configuração que exija a reinicialização de um computador, poderá incluir o comando de reinicialização no script e executar a operação inteira remotamente.</span><span class="sxs-lookup"><span data-stu-id="012aa-119">For example, if you create a script to install software or make a configuration change that requires restarting a computer, you can include the restart command in the script and perform the entire operation remotely.</span></span> <span data-ttu-id="012aa-120">O método **reboot** pode ser usado para reiniciar um computador.</span><span class="sxs-lookup"><span data-stu-id="012aa-120">The **Reboot** method can be used to restart a computer.</span></span> <span data-ttu-id="012aa-121">Como o método [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) , o método **reboot** exige que o usuário cujas credenciais de segurança estejam sendo usadas pelo script para ter o privilégio de desligamento.</span><span class="sxs-lookup"><span data-stu-id="012aa-121">Like the [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) method, the **Reboot** method requires the user whose security credentials are being used by the script to possess the Shutdown privilege.</span></span>

## <a name="examples"></a><span data-ttu-id="012aa-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="012aa-122">Examples</span></span>

<span data-ttu-id="012aa-123">O exemplo de código VBScript a seguir invoca o método reboot da classe [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) .</span><span class="sxs-lookup"><span data-stu-id="012aa-123">The following VBScript code sample invokes the Reboot method of the [**Win32\_OperatingSystem**](win32-operatingsystem.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="012aa-124">Você deve ter o privilégio de desligamento para invocar com êxito o método de desligamento.</span><span class="sxs-lookup"><span data-stu-id="012aa-124">You must have the Shutdown privilege to successfully invoke the Shutdown method.</span></span>

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Reboot()
next
```



<span data-ttu-id="012aa-125">O código Perl a seguir invoca o método reboot da classe [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) .</span><span class="sxs-lookup"><span data-stu-id="012aa-125">The following Perl code invokes the Reboot method of the [**Win32\_OperatingSystem**](win32-operatingsystem.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="012aa-126">Você deve ter o privilégio de desligamento para invocar com êxito o método de desligamento.</span><span class="sxs-lookup"><span data-stu-id="012aa-126">You must have the Shutdown privilege to successfully invoke the Shutdown method.</span></span>

 


```
use Win32::OLE;
use strict;
my $OpSysSet;
eval { $OpSysSet = Win32::OLE->GetObject("winmgmts:{(Shutdown)}//./root/cimv2")->
 ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true"); };

if (!$@ && defined $OpSysSet)
{
 close(STDERR);
 foreach my $OpSys (in $OpSysSet)
 {
  my $RetVal = $OpSys->Reboot(); 
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



<span data-ttu-id="012aa-127">O VBScript a seguir invoca o método reboot da classe [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) em um sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="012aa-127">The following VBScript invokes the Reboot method of the [**Win32\_OperatingSystem**](win32-operatingsystem.md) class on a remote system.</span></span> <span data-ttu-id="012aa-128">Preencha \_ \_ o nome do sistema remoto com o nome do sistema remoto para reinicializar.</span><span class="sxs-lookup"><span data-stu-id="012aa-128">Fill in REMOTE\_SYSTEM\_NAME with the name of the remote system to reboot.</span></span>

> [!Note]  
> <span data-ttu-id="012aa-129">Você deve ter o privilégio RemoteShutdown para invocar com êxito o método de reinicialização</span><span class="sxs-lookup"><span data-stu-id="012aa-129">You must have the RemoteShutdown privilege to successfully invoke the Reboot method</span></span>

 


```VB
Set OpSysSet = GetObject("winmgmts:{(RemoteShutdown)}//REMOTE_SYSTEM_NAME/root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Reboot()
next
```



<span data-ttu-id="012aa-130">Ele segue o Perl invoca o método reboot da classe [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) em um sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="012aa-130">he following Perl invokes the Reboot method of the [**Win32\_OperatingSystem**](win32-operatingsystem.md) class on a remote system.</span></span> <span data-ttu-id="012aa-131">Preencha \_ \_ o nome do sistema remoto com o nome do sistema remoto para reinicializar.</span><span class="sxs-lookup"><span data-stu-id="012aa-131">Fill in REMOTE\_SYSTEM\_NAME with the name of the remote system to reboot.</span></span>

> [!Note]  
> <span data-ttu-id="012aa-132">Você deve ter o privilégio RemoteShutdown para invocar com êxito o método de reinicialização.</span><span class="sxs-lookup"><span data-stu-id="012aa-132">You must have the RemoteShutdown privilege to successfully invoke the Reboot method.</span></span>

 


```
use strict;
use Win32::OLE;

use constant REMOTE_SYSTEM_NAME => "MACHINENAME";
use constant USERNAME => "USER";
use constant PASSWORD => "PASSWORD";
use constant NAMESPACE => "root\\cimv2";
use constant wbemPrivilegeRemoteShutdown => 23;
use constant wbemImpersonationLevelImpersonate => 3;
close(STDERR);
my ($locator, $services, $OpSysSet);
eval {
  $locator = Win32::OLE->new('WbemScripting.SWbemLocator');
  $locator->{Security_}->{impersonationlevel} = wbemImpersonationLevelImpersonate;
  $services = $locator->ConnectServer(REMOTE_SYSTEM_NAME, NAMESPACE, USERNAME, PASSWORD);
  $services->{Security_}->{Privileges}->Add(wbemPrivilegeRemoteShutdown);
  $OpSysSet = $services->ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true");
 };

if (!$@ && defined $OpSysSet)
{
 foreach my $OpSys (in $OpSysSet)
 {
  $OpSys->Reboot();
 }
}
else
{
 print Win32::OLE->LastError, "\n";
 exit(1);
}
```



## <a name="requirements"></a><span data-ttu-id="012aa-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="012aa-133">Requirements</span></span>



| <span data-ttu-id="012aa-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="012aa-134">Requirement</span></span> | <span data-ttu-id="012aa-135">Valor</span><span class="sxs-lookup"><span data-stu-id="012aa-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="012aa-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="012aa-136">Minimum supported client</span></span><br/> | <span data-ttu-id="012aa-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="012aa-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="012aa-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="012aa-138">Minimum supported server</span></span><br/> | <span data-ttu-id="012aa-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="012aa-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="012aa-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="012aa-140">Namespace</span></span><br/>                | <span data-ttu-id="012aa-141">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="012aa-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="012aa-142">MOF</span><span class="sxs-lookup"><span data-stu-id="012aa-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="012aa-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="012aa-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="012aa-144">DLL</span><span class="sxs-lookup"><span data-stu-id="012aa-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="012aa-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="012aa-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="012aa-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="012aa-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="012aa-147">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="012aa-147">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="012aa-148">**Sistema \_ operacional Win32**</span><span class="sxs-lookup"><span data-stu-id="012aa-148">**Win32\_OperatingSystem**</span></span>](win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="012aa-149">**\_Método CIM OperatingSystem. Shutdown**</span><span class="sxs-lookup"><span data-stu-id="012aa-149">**CIM\_OperatingSystem.Shutdown method**</span></span>](shutdown-method-in-class-cim-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="012aa-150">Tarefas do WMI: gerenciamento de desktop</span><span class="sxs-lookup"><span data-stu-id="012aa-150">WMI Tasks: Desktop Management</span></span>](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 


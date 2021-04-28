---
description: Método Delete da classe Win32_Service (provedores WMI CIMWin32)-a exclusão&\# 8194; O método de classe WMI exclui um serviço existente.
ms.assetid: aa4e7630-3b19-47dd-acd1-4d1735acb819
ms.tgt_platform: multiple
title: Método Delete da classe Win32_Service (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4031184e23e99fc54237ed0b0b4196fe6c075c5b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089574"
---
# <a name="delete-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="ab762-103">Método Delete da classe Win32_Service (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="ab762-103">Delete method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="ab762-104">O método **excluir** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) exclui um serviço existente.</span><span class="sxs-lookup"><span data-stu-id="ab762-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes an existing service.</span></span>

<span data-ttu-id="ab762-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="ab762-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ab762-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ab762-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ab762-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab762-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="ab762-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab762-108">Parameters</span></span>

<span data-ttu-id="ab762-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ab762-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ab762-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ab762-110">Return value</span></span>

<span data-ttu-id="ab762-111">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="ab762-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="ab762-112">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="ab762-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="ab762-113">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="ab762-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="ab762-114">**0**</span><span class="sxs-lookup"><span data-stu-id="ab762-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="ab762-115">A solicitação foi aceita.</span><span class="sxs-lookup"><span data-stu-id="ab762-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="ab762-116">**1**</span><span class="sxs-lookup"><span data-stu-id="ab762-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="ab762-117">A solicitação não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="ab762-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ab762-118">**2**</span><span class="sxs-lookup"><span data-stu-id="ab762-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="ab762-119">O usuário não tinha o acesso necessário.</span><span class="sxs-lookup"><span data-stu-id="ab762-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="ab762-120">**3**</span><span class="sxs-lookup"><span data-stu-id="ab762-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="ab762-121">O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.</span><span class="sxs-lookup"><span data-stu-id="ab762-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="ab762-122">**4**</span><span class="sxs-lookup"><span data-stu-id="ab762-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="ab762-123">O código de controle pedido não é válido ou é inaceitável para o serviço.</span><span class="sxs-lookup"><span data-stu-id="ab762-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="ab762-124">**5**</span><span class="sxs-lookup"><span data-stu-id="ab762-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="ab762-125">O código de controle solicitado não pode ser enviado ao serviço porque o estado do serviço ([**Win32 \_ BaseService**](win32-baseservice.md).\*\*\*\* A propriedade State) é igual a 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="ab762-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="ab762-126">**6**</span><span class="sxs-lookup"><span data-stu-id="ab762-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="ab762-127">O serviço não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="ab762-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="ab762-128">**7**</span><span class="sxs-lookup"><span data-stu-id="ab762-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="ab762-129">O serviço não respondeu à solicitação de início em um tempo oportuno.</span><span class="sxs-lookup"><span data-stu-id="ab762-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="ab762-130">**8**</span><span class="sxs-lookup"><span data-stu-id="ab762-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="ab762-131">Falha desconhecida ao iniciar o serviço.</span><span class="sxs-lookup"><span data-stu-id="ab762-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="ab762-132">**9**</span><span class="sxs-lookup"><span data-stu-id="ab762-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="ab762-133">O caminho do diretório para o arquivo executável do serviço não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="ab762-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="ab762-134">**10**</span><span class="sxs-lookup"><span data-stu-id="ab762-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="ab762-135">O serviço já está em execução.</span><span class="sxs-lookup"><span data-stu-id="ab762-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="ab762-136">**11**</span><span class="sxs-lookup"><span data-stu-id="ab762-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="ab762-137">O banco de dados para adicionar um serviço novo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="ab762-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="ab762-138">**12**</span><span class="sxs-lookup"><span data-stu-id="ab762-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="ab762-139">Uma dependência da qual esse serviço depende foi removida do sistema.</span><span class="sxs-lookup"><span data-stu-id="ab762-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ab762-140">**13**</span><span class="sxs-lookup"><span data-stu-id="ab762-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="ab762-141">O serviço não localizou o serviço necessário em um serviço dependente.</span><span class="sxs-lookup"><span data-stu-id="ab762-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="ab762-142">**14**</span><span class="sxs-lookup"><span data-stu-id="ab762-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="ab762-143">O serviço foi desabilitado do sistema.</span><span class="sxs-lookup"><span data-stu-id="ab762-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ab762-144">**15**</span><span class="sxs-lookup"><span data-stu-id="ab762-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="ab762-145">O serviço não tem a autenticação correta para ser executado no sistema.</span><span class="sxs-lookup"><span data-stu-id="ab762-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="ab762-146">**16**</span><span class="sxs-lookup"><span data-stu-id="ab762-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="ab762-147">Este serviço está sendo removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="ab762-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ab762-148">**17**</span><span class="sxs-lookup"><span data-stu-id="ab762-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="ab762-149">O serviço não tem nenhum thread de execução.</span><span class="sxs-lookup"><span data-stu-id="ab762-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="ab762-150">**anos**</span><span class="sxs-lookup"><span data-stu-id="ab762-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="ab762-151">O serviço tem dependências circulares quando é iniciado.</span><span class="sxs-lookup"><span data-stu-id="ab762-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="ab762-152">**aprimora**</span><span class="sxs-lookup"><span data-stu-id="ab762-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="ab762-153">Um serviço está sendo executado com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="ab762-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="ab762-154">**20**</span><span class="sxs-lookup"><span data-stu-id="ab762-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="ab762-155">O nome do serviço tem caracteres inválidos.</span><span class="sxs-lookup"><span data-stu-id="ab762-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="ab762-156">**Abril**</span><span class="sxs-lookup"><span data-stu-id="ab762-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="ab762-157">Parâmetros inválidos foram passados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="ab762-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="ab762-158">**22**</span><span class="sxs-lookup"><span data-stu-id="ab762-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="ab762-159">A conta sob a qual este serviço é executado é inválida ou não tem as permissões para executar o serviço.</span><span class="sxs-lookup"><span data-stu-id="ab762-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="ab762-160">**23**</span><span class="sxs-lookup"><span data-stu-id="ab762-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="ab762-161">O serviço existe no banco de dados de serviços disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="ab762-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ab762-162">**24**</span><span class="sxs-lookup"><span data-stu-id="ab762-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="ab762-163">O serviço está pausado atualmente no sistema.</span><span class="sxs-lookup"><span data-stu-id="ab762-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ab762-164">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab762-164">Remarks</span></span>

<span data-ttu-id="ab762-165">À medida que sua organização for alterada, você poderá optar por remover determinados serviços de determinados computadores.</span><span class="sxs-lookup"><span data-stu-id="ab762-165">As your organization changes, you might decide to remove certain services from certain computers.</span></span> <span data-ttu-id="ab762-166">Os serviços internos e de terceiros podem ser removidos usando o WMI, enquanto os serviços do sistema operacional podem ser removidos usando Sysocmgr.exe.</span><span class="sxs-lookup"><span data-stu-id="ab762-166">In-house and third-party services can be removed by using WMI, while operating system services can be removed by using Sysocmgr.exe.</span></span>

<span data-ttu-id="ab762-167">Ao se preparar para remover os serviços, tenha em mente as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="ab762-167">When preparing to remove services, keep the following information in mind:</span></span>

-   <span data-ttu-id="ab762-168">Os serviços devem ser interrompidos antes de serem removidos.</span><span class="sxs-lookup"><span data-stu-id="ab762-168">Services must be stopped before you remove them.</span></span> <span data-ttu-id="ab762-169">Se o serviço estiver em execução quando você emitir o comando delete, o serviço será marcado para exclusão, mas continuará sendo executado até que seja interrompido e todos os identificadores abertos sejam fechados.</span><span class="sxs-lookup"><span data-stu-id="ab762-169">If the service is running when you issue the delete command, the service is marked for deletion, but it continues to run until it stops and all open handles are closed.</span></span>

    <span data-ttu-id="ab762-170">Se o serviço nunca for interrompido, esse serviço nunca será excluído.</span><span class="sxs-lookup"><span data-stu-id="ab762-170">If the service is never stopped, that service will never be deleted.</span></span>

-   <span data-ttu-id="ab762-171">A remoção de um serviço não remove o arquivo executável do serviço.</span><span class="sxs-lookup"><span data-stu-id="ab762-171">Removing a service does not remove the service's executable file.</span></span>

    <span data-ttu-id="ab762-172">A remoção de um serviço usando o WMI exclui as entradas de registro relacionadas em HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services.</span><span class="sxs-lookup"><span data-stu-id="ab762-172">Removing a service by using WMI deletes the related registry entries under HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services.</span></span> <span data-ttu-id="ab762-173">Como resultado, o serviço não é mais instalado e não está disponível por meio do snap-in serviços.</span><span class="sxs-lookup"><span data-stu-id="ab762-173">As a result, the service is no longer installed and is not available through the Services snap-in.</span></span> <span data-ttu-id="ab762-174">No entanto, o WMI não exclui o arquivo executável, o que significa que você pode facilmente reinstalar o serviço.</span><span class="sxs-lookup"><span data-stu-id="ab762-174">However, WMI does not delete the executable file, meaning you could easily reinstall the service.</span></span> <span data-ttu-id="ab762-175">Para excluir o arquivo executável, você deve recuperar o nome do caminho e, em seguida, excluir o arquivo.</span><span class="sxs-lookup"><span data-stu-id="ab762-175">To delete the executable file, you must retrieve the path name and then delete the file.</span></span>

-   <span data-ttu-id="ab762-176">Remover um serviço base do Windows 2000 (por exemplo, DHCP) usando o WMI exclui as entradas do registro para esse serviço, mas não remove o atalho do menu Ferramentas administrativas ou remove o serviço do assistente de componentes do Windows.</span><span class="sxs-lookup"><span data-stu-id="ab762-176">Removing a base Windows 2000 service (for example, DHCP) by using WMI deletes the registry entries for that service but does not remove the shortcut from the Administrative Tools menu or remove the service from the Windows Components Wizard.</span></span> <span data-ttu-id="ab762-177">Isso pode confundir qualquer pessoa que tentar determinar como o computador foi configurado.</span><span class="sxs-lookup"><span data-stu-id="ab762-177">This can confuse anyone trying to determine how the computer has been configured.</span></span>

    <span data-ttu-id="ab762-178">Por exemplo, se você remover o serviço DHCP usando um script WMI, o serviço DHCP não estará mais listado no snap-in serviços.</span><span class="sxs-lookup"><span data-stu-id="ab762-178">For example, if you remove the DHCP service by using a WMI script, the DHCP service is no longer listed in the Services snap-in.</span></span> <span data-ttu-id="ab762-179">No entanto, um atalho não funcional para o console do DHCP permanece no menu Ferramentas administrativas e, se você iniciar o assistente de componentes do Windows, ele indicará que o serviço DHCP está instalado.</span><span class="sxs-lookup"><span data-stu-id="ab762-179">However, a nonfunctioning shortcut to the DHCP console remains in the Administrative Tools menu, and if you start the Windows Component Wizard, it indicates that the DHCP service is installed.</span></span>

    <span data-ttu-id="ab762-180">Por isso, você sempre deve usar Sysocmgr.exe para remover programaticamente os serviços do Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="ab762-180">Because of this, you should always use Sysocmgr.exe to programmatically remove Windows 2000 services.</span></span>

## <a name="examples"></a><span data-ttu-id="ab762-181">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ab762-181">Examples</span></span>

<span data-ttu-id="ab762-182">O exemplo de código VBScript a seguir descreve como excluir um serviço.</span><span class="sxs-lookup"><span data-stu-id="ab762-182">The following VBScript code sample describes how to delete a service.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colListOfServices = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Service WHERE Name = 'DbService'")
For Each objService in colListOfServices
 objService.StopService()
 objService.Delete()
Next
```



<span data-ttu-id="ab762-183">O exemplo de código Perl a seguir descreve como excluir um serviço.</span><span class="sxs-lookup"><span data-stu-id="ab762-183">The following Perl code sample describes how to delete a service.</span></span>


```
use strict;
use Win32::OLE;

my ($Service, $ServiceSet) ;
eval {$ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='MyService'");};
unless($@)
{
 foreach $Service (in $ServiceSet)
 {
  my $RetVal = $Service->Delete();
  if ($RetVal == 0)  
  {
   print "Service deleted \n"; 
  }
  else  
  {
   print "Delete failed: %d", $RetVal;
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="ab762-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab762-184">Requirements</span></span>



| <span data-ttu-id="ab762-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab762-185">Requirement</span></span> | <span data-ttu-id="ab762-186">Valor</span><span class="sxs-lookup"><span data-stu-id="ab762-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab762-187">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab762-187">Minimum supported client</span></span><br/> | <span data-ttu-id="ab762-188">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ab762-188">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ab762-189">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab762-189">Minimum supported server</span></span><br/> | <span data-ttu-id="ab762-190">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab762-190">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ab762-191">Namespace</span><span class="sxs-lookup"><span data-stu-id="ab762-191">Namespace</span></span><br/>                | <span data-ttu-id="ab762-192">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ab762-192">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ab762-193">MOF</span><span class="sxs-lookup"><span data-stu-id="ab762-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab762-194"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ab762-194"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ab762-195">DLL</span><span class="sxs-lookup"><span data-stu-id="ab762-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab762-196"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab762-196"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab762-197">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ab762-197">See also</span></span>

<dl> <dt>

<span data-ttu-id="ab762-198">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ab762-198">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ab762-199">**\_Serviço Win32**</span><span class="sxs-lookup"><span data-stu-id="ab762-199">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="ab762-200">Tarefas do WMI: serviços</span><span class="sxs-lookup"><span data-stu-id="ab762-200">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 


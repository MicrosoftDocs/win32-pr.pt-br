---
title: Método Delete da classe Win32_Service (Serviços de Área de Trabalho Remota)
description: A exclusão \ 8194; O método de classe WMI exclui um serviço existente.
ms.assetid: 0F012D6B-BD29-4AC3-AC7E-78EC02C1FF43
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método Delete
- Método Delete Serviços de Área de Trabalho Remota, classe Win32_Service
- Classe Win32_Service Serviços de Área de Trabalho Remota, método Delete
topic_type:
- apiref
api_name:
- Win32_Service.Delete
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89e2c30ef39d7b36baf62a486477fcf4a7fa2842
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499756"
---
# <a name="delete-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="5509b-106">Método Delete da classe Win32_Service (Serviços de Área de Trabalho Remota)</span><span class="sxs-lookup"><span data-stu-id="5509b-106">Delete method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="5509b-107">O método **excluir** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) exclui um serviço existente.</span><span class="sxs-lookup"><span data-stu-id="5509b-107">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes an existing service.</span></span>

<span data-ttu-id="5509b-108">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="5509b-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5509b-109">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5509b-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5509b-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5509b-110">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="5509b-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5509b-111">Parameters</span></span>

<span data-ttu-id="5509b-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="5509b-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5509b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5509b-113">Return value</span></span>

<span data-ttu-id="5509b-114">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="5509b-114">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="5509b-115">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="5509b-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="5509b-116">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="5509b-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="5509b-117">**0**</span><span class="sxs-lookup"><span data-stu-id="5509b-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="5509b-118">A solicitação foi aceita.</span><span class="sxs-lookup"><span data-stu-id="5509b-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="5509b-119">**1**</span><span class="sxs-lookup"><span data-stu-id="5509b-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="5509b-120">A solicitação não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="5509b-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="5509b-121">**2**</span><span class="sxs-lookup"><span data-stu-id="5509b-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="5509b-122">O usuário não tinha o acesso necessário.</span><span class="sxs-lookup"><span data-stu-id="5509b-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="5509b-123">**3**</span><span class="sxs-lookup"><span data-stu-id="5509b-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="5509b-124">O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.</span><span class="sxs-lookup"><span data-stu-id="5509b-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="5509b-125">**4**</span><span class="sxs-lookup"><span data-stu-id="5509b-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="5509b-126">O código de controle pedido não é válido ou é inaceitável para o serviço.</span><span class="sxs-lookup"><span data-stu-id="5509b-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="5509b-127">**5**</span><span class="sxs-lookup"><span data-stu-id="5509b-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="5509b-128">O código de controle solicitado não pode ser enviado ao serviço porque o estado do serviço ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).\*\*\*\* A propriedade State) é igual a 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="5509b-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="5509b-129">**6**</span><span class="sxs-lookup"><span data-stu-id="5509b-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="5509b-130">O serviço não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="5509b-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="5509b-131">**7**</span><span class="sxs-lookup"><span data-stu-id="5509b-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="5509b-132">O serviço não respondeu à solicitação de início em um tempo oportuno.</span><span class="sxs-lookup"><span data-stu-id="5509b-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="5509b-133">**8**</span><span class="sxs-lookup"><span data-stu-id="5509b-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="5509b-134">Falha desconhecida ao iniciar o serviço.</span><span class="sxs-lookup"><span data-stu-id="5509b-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="5509b-135">**9**</span><span class="sxs-lookup"><span data-stu-id="5509b-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="5509b-136">O caminho do diretório para o arquivo executável do serviço não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="5509b-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="5509b-137">**10**</span><span class="sxs-lookup"><span data-stu-id="5509b-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="5509b-138">O serviço já está em execução.</span><span class="sxs-lookup"><span data-stu-id="5509b-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="5509b-139">**11**</span><span class="sxs-lookup"><span data-stu-id="5509b-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="5509b-140">O banco de dados para adicionar um serviço novo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="5509b-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="5509b-141">**12**</span><span class="sxs-lookup"><span data-stu-id="5509b-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="5509b-142">Uma dependência da qual esse serviço depende foi removida do sistema.</span><span class="sxs-lookup"><span data-stu-id="5509b-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="5509b-143">**13**</span><span class="sxs-lookup"><span data-stu-id="5509b-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="5509b-144">O serviço não localizou o serviço necessário em um serviço dependente.</span><span class="sxs-lookup"><span data-stu-id="5509b-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="5509b-145">**14**</span><span class="sxs-lookup"><span data-stu-id="5509b-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="5509b-146">O serviço foi desabilitado do sistema.</span><span class="sxs-lookup"><span data-stu-id="5509b-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="5509b-147">**15**</span><span class="sxs-lookup"><span data-stu-id="5509b-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="5509b-148">O serviço não tem a autenticação correta para ser executado no sistema.</span><span class="sxs-lookup"><span data-stu-id="5509b-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="5509b-149">**16**</span><span class="sxs-lookup"><span data-stu-id="5509b-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="5509b-150">Este serviço está sendo removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="5509b-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="5509b-151">**17**</span><span class="sxs-lookup"><span data-stu-id="5509b-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="5509b-152">O serviço não tem nenhum thread de execução.</span><span class="sxs-lookup"><span data-stu-id="5509b-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="5509b-153">**anos**</span><span class="sxs-lookup"><span data-stu-id="5509b-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="5509b-154">O serviço tem dependências circulares quando é iniciado.</span><span class="sxs-lookup"><span data-stu-id="5509b-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="5509b-155">**aprimora**</span><span class="sxs-lookup"><span data-stu-id="5509b-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="5509b-156">Um serviço está sendo executado com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="5509b-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="5509b-157">**20**</span><span class="sxs-lookup"><span data-stu-id="5509b-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="5509b-158">O nome do serviço tem caracteres inválidos.</span><span class="sxs-lookup"><span data-stu-id="5509b-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="5509b-159">**Abril**</span><span class="sxs-lookup"><span data-stu-id="5509b-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="5509b-160">Parâmetros inválidos foram passados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="5509b-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="5509b-161">**22**</span><span class="sxs-lookup"><span data-stu-id="5509b-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="5509b-162">A conta sob a qual este serviço é executado é inválida ou não tem as permissões para executar o serviço.</span><span class="sxs-lookup"><span data-stu-id="5509b-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="5509b-163">**23**</span><span class="sxs-lookup"><span data-stu-id="5509b-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="5509b-164">O serviço existe no banco de dados de serviços disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="5509b-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="5509b-165">**24**</span><span class="sxs-lookup"><span data-stu-id="5509b-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="5509b-166">O serviço está pausado atualmente no sistema.</span><span class="sxs-lookup"><span data-stu-id="5509b-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5509b-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="5509b-167">Remarks</span></span>

<span data-ttu-id="5509b-168">À medida que sua organização for alterada, você poderá optar por remover determinados serviços de determinados computadores.</span><span class="sxs-lookup"><span data-stu-id="5509b-168">As your organization changes, you might decide to remove certain services from certain computers.</span></span> <span data-ttu-id="5509b-169">Os serviços internos e de terceiros podem ser removidos usando o WMI, enquanto os serviços do sistema operacional podem ser removidos usando Sysocmgr.exe.</span><span class="sxs-lookup"><span data-stu-id="5509b-169">In-house and third-party services can be removed by using WMI, while operating system services can be removed by using Sysocmgr.exe.</span></span>

<span data-ttu-id="5509b-170">Ao se preparar para remover os serviços, tenha em mente as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="5509b-170">When preparing to remove services, keep the following information in mind:</span></span>

-   <span data-ttu-id="5509b-171">Os serviços devem ser interrompidos antes de serem removidos.</span><span class="sxs-lookup"><span data-stu-id="5509b-171">Services must be stopped before you remove them.</span></span> <span data-ttu-id="5509b-172">Se o serviço estiver em execução quando você emitir o comando delete, o serviço será marcado para exclusão, mas continuará sendo executado até que seja interrompido e todos os identificadores abertos sejam fechados.</span><span class="sxs-lookup"><span data-stu-id="5509b-172">If the service is running when you issue the delete command, the service is marked for deletion, but it continues to run until it stops and all open handles are closed.</span></span>

    <span data-ttu-id="5509b-173">Se o serviço nunca for interrompido, esse serviço nunca será excluído.</span><span class="sxs-lookup"><span data-stu-id="5509b-173">If the service is never stopped, that service will never be deleted.</span></span>

-   <span data-ttu-id="5509b-174">A remoção de um serviço não remove o arquivo executável do serviço.</span><span class="sxs-lookup"><span data-stu-id="5509b-174">Removing a service does not remove the service's executable file.</span></span>

    <span data-ttu-id="5509b-175">A remoção de um serviço usando o WMI exclui as entradas de registro relacionadas em HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services.</span><span class="sxs-lookup"><span data-stu-id="5509b-175">Removing a service by using WMI deletes the related registry entries under HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services.</span></span> <span data-ttu-id="5509b-176">Como resultado, o serviço não é mais instalado e não está disponível por meio do snap-in serviços.</span><span class="sxs-lookup"><span data-stu-id="5509b-176">As a result, the service is no longer installed and is not available through the Services snap-in.</span></span> <span data-ttu-id="5509b-177">No entanto, o WMI não exclui o arquivo executável, o que significa que você pode facilmente reinstalar o serviço.</span><span class="sxs-lookup"><span data-stu-id="5509b-177">However, WMI does not delete the executable file, meaning you could easily reinstall the service.</span></span> <span data-ttu-id="5509b-178">Para excluir o arquivo executável, você deve recuperar o nome do caminho e, em seguida, excluir o arquivo.</span><span class="sxs-lookup"><span data-stu-id="5509b-178">To delete the executable file, you must retrieve the path name and then delete the file.</span></span>

-   <span data-ttu-id="5509b-179">Remover um serviço base do Windows 2000 (por exemplo, DHCP) usando o WMI exclui as entradas do registro para esse serviço, mas não remove o atalho do menu Ferramentas administrativas ou remove o serviço do assistente de componentes do Windows.</span><span class="sxs-lookup"><span data-stu-id="5509b-179">Removing a base Windows 2000 service (for example, DHCP) by using WMI deletes the registry entries for that service but does not remove the shortcut from the Administrative Tools menu or remove the service from the Windows Components Wizard.</span></span> <span data-ttu-id="5509b-180">Isso pode confundir qualquer pessoa que tentar determinar como o computador foi configurado.</span><span class="sxs-lookup"><span data-stu-id="5509b-180">This can confuse anyone trying to determine how the computer has been configured.</span></span>

    <span data-ttu-id="5509b-181">Por exemplo, se você remover o serviço DHCP usando um script WMI, o serviço DHCP não estará mais listado no snap-in serviços.</span><span class="sxs-lookup"><span data-stu-id="5509b-181">For example, if you remove the DHCP service by using a WMI script, the DHCP service is no longer listed in the Services snap-in.</span></span> <span data-ttu-id="5509b-182">No entanto, um atalho não funcional para o console do DHCP permanece no menu Ferramentas administrativas e, se você iniciar o assistente de componentes do Windows, ele indicará que o serviço DHCP está instalado.</span><span class="sxs-lookup"><span data-stu-id="5509b-182">However, a nonfunctioning shortcut to the DHCP console remains in the Administrative Tools menu, and if you start the Windows Component Wizard, it indicates that the DHCP service is installed.</span></span>

    <span data-ttu-id="5509b-183">Por isso, você sempre deve usar Sysocmgr.exe para remover programaticamente os serviços do Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="5509b-183">Because of this, you should always use Sysocmgr.exe to programmatically remove Windows 2000 services.</span></span>

## <a name="examples"></a><span data-ttu-id="5509b-184">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5509b-184">Examples</span></span>

<span data-ttu-id="5509b-185">O exemplo de código VBScript a seguir descreve como excluir um serviço.</span><span class="sxs-lookup"><span data-stu-id="5509b-185">The following VBScript code sample describes how to delete a service.</span></span>


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



<span data-ttu-id="5509b-186">O exemplo de código Perl a seguir descreve como excluir um serviço.</span><span class="sxs-lookup"><span data-stu-id="5509b-186">The following Perl code sample describes how to delete a service.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="5509b-187">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5509b-187">Requirements</span></span>



| <span data-ttu-id="5509b-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="5509b-188">Requirement</span></span> | <span data-ttu-id="5509b-189">Valor</span><span class="sxs-lookup"><span data-stu-id="5509b-189">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5509b-190">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5509b-190">Minimum supported client</span></span><br/> | <span data-ttu-id="5509b-191">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5509b-191">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5509b-192">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5509b-192">Minimum supported server</span></span><br/> | <span data-ttu-id="5509b-193">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5509b-193">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5509b-194">Namespace</span><span class="sxs-lookup"><span data-stu-id="5509b-194">Namespace</span></span><br/>                | <span data-ttu-id="5509b-195">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="5509b-195">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="5509b-196">MOF</span><span class="sxs-lookup"><span data-stu-id="5509b-196">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5509b-197"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5509b-197"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="5509b-198">DLL</span><span class="sxs-lookup"><span data-stu-id="5509b-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5509b-199"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5509b-199"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5509b-200">Confira também</span><span class="sxs-lookup"><span data-stu-id="5509b-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5509b-201">**\_Serviço Win32**</span><span class="sxs-lookup"><span data-stu-id="5509b-201">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="5509b-202">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="5509b-202">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="5509b-203">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="5509b-203">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="5509b-204">Tarefas do WMI: serviços</span><span class="sxs-lookup"><span data-stu-id="5509b-204">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 


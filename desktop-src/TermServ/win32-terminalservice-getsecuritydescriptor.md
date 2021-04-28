---
title: Método GetSecurityDescriptor da classe Win32_Service (Serviços de Área de Trabalho Remota)
description: Método GetSecurityDescriptor da classe Win32_Service (Serviços de Área de Trabalho Remota) – retorna o descritor de segurança que controla o acesso ao serviço.
ms.assetid: 9898091A-5BE2-42A0-BF81-13AB74696ACB
ms.tgt_platform: multiple
keywords:
- Instrumentação de Gerenciamento do Windows de script, segurança
- Instrumentação de Gerenciamento do Windows de segurança, scripts
- Serviços de Área de Trabalho Remota do método GetSecurityDescriptor
- Método GetSecurityDescriptor Serviços de Área de Trabalho Remota, classe Win32_Service
- Classe Win32_Service Serviços de Área de Trabalho Remota, Método GetSecurityDescriptor
topic_type:
- apiref
api_name:
- Win32_Service.GetSecurityDescriptor
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea5b8a9b945048f947aa273e1ccc1f4514469681
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090644"
---
# <a name="getsecuritydescriptor-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="c6dc5-108">Método GetSecurityDescriptor da classe Win32_Service (Serviços de Área de Trabalho Remota)</span><span class="sxs-lookup"><span data-stu-id="c6dc5-108">GetSecurityDescriptor method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="c6dc5-109">O método **GetSecurityDescriptor** retorna o descritor de segurança que controla o acesso ao serviço.</span><span class="sxs-lookup"><span data-stu-id="c6dc5-109">The **GetSecurityDescriptor** method returns the security descriptor that controls access to the service.</span></span> <span data-ttu-id="c6dc5-110">O descritor é retornado como uma instância do [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="c6dc5-110">The descriptor is returned as an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span>

## <a name="syntax"></a><span data-ttu-id="c6dc5-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c6dc5-111">Syntax</span></span>


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="c6dc5-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c6dc5-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6dc5-113">*Descritor* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c6dc5-113">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6dc5-114">O descritor de segurança associado ao serviço.</span><span class="sxs-lookup"><span data-stu-id="c6dc5-114">The security descriptor associated with the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6dc5-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c6dc5-115">Return value</span></span>

<span data-ttu-id="c6dc5-116">Retorna um dos valores listados na lista a seguir ou um valor diferente para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="c6dc5-116">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="c6dc5-117">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="c6dc5-117">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="c6dc5-118">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="c6dc5-118">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="c6dc5-119">**0**</span><span class="sxs-lookup"><span data-stu-id="c6dc5-119">**0**</span></span>
</dt> <dd>

<span data-ttu-id="c6dc5-120">A solicitação foi aceita.</span><span class="sxs-lookup"><span data-stu-id="c6dc5-120">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="c6dc5-121">**1**</span><span class="sxs-lookup"><span data-stu-id="c6dc5-121">**1**</span></span>
</dt> <dd>

<span data-ttu-id="c6dc5-122">A solicitação não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="c6dc5-122">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c6dc5-123">**2**</span><span class="sxs-lookup"><span data-stu-id="c6dc5-123">**2**</span></span>
</dt> <dd>

<span data-ttu-id="c6dc5-124">O usuário não tinha o acesso necessário.</span><span class="sxs-lookup"><span data-stu-id="c6dc5-124">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="c6dc5-125">**3**</span><span class="sxs-lookup"><span data-stu-id="c6dc5-125">**3**</span></span>
</dt> <dd>

<span data-ttu-id="c6dc5-126">O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.</span><span class="sxs-lookup"><span data-stu-id="c6dc5-126">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="c6dc5-127">**4**</span><span class="sxs-lookup"><span data-stu-id="c6dc5-127">**4**</span></span>
</dt> <dd>

<span data-ttu-id="c6dc5-128">O código de controle pedido não é válido ou é inaceitável para o serviço.</span><span class="sxs-lookup"><span data-stu-id="c6dc5-128">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c6dc5-129">**5**</span><span class="sxs-lookup"><span data-stu-id="c6dc5-129">**5**</span></span>
</dt> <dd>

<span data-ttu-id="c6dc5-130">O código de controle solicitado não pode ser enviado ao serviço porque o estado do serviço ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).\*\*\*\* A propriedade State) é igual a 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="c6dc5-130">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="c6dc5-131">**6**</span><span class="sxs-lookup"><span data-stu-id="c6dc5-131">**6**</span></span>
</dt> <dd>

<span data-ttu-id="c6dc5-132">O serviço não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="c6dc5-132">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="c6dc5-133">**7**</span><span class="sxs-lookup"><span data-stu-id="c6dc5-133">**7**</span></span>
</dt> <dd>

<span data-ttu-id="c6dc5-134">O serviço não respondeu à solicitação de início em um tempo oportuno.</span><span class="sxs-lookup"><span data-stu-id="c6dc5-134">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="c6dc5-135">**8**</span><span class="sxs-lookup"><span data-stu-id="c6dc5-135">**8**</span></span>
</dt> <dd>

<span data-ttu-id="c6dc5-136">Falha desconhecida ao iniciar o serviço.</span><span class="sxs-lookup"><span data-stu-id="c6dc5-136">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="c6dc5-137">**9**</span><span class="sxs-lookup"><span data-stu-id="c6dc5-137">**9**</span></span>
</dt> <dd>

<span data-ttu-id="c6dc5-138">O caminho do diretório para o arquivo executável do serviço não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="c6dc5-138">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="c6dc5-139">**10**</span><span class="sxs-lookup"><span data-stu-id="c6dc5-139">**10**</span></span>
</dt> <dd>

<span data-ttu-id="c6dc5-140">O serviço já está em execução.</span><span class="sxs-lookup"><span data-stu-id="c6dc5-140">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="c6dc5-141">**11**</span><span class="sxs-lookup"><span data-stu-id="c6dc5-141">**11**</span></span>
</dt> <dd>

<span data-ttu-id="c6dc5-142">O banco de dados para adicionar um serviço novo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="c6dc5-142">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="c6dc5-143">**12**</span><span class="sxs-lookup"><span data-stu-id="c6dc5-143">**12**</span></span>
</dt> <dd>

<span data-ttu-id="c6dc5-144">Uma dependência da qual esse serviço depende foi removida do sistema.</span><span class="sxs-lookup"><span data-stu-id="c6dc5-144">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c6dc5-145">**13**</span><span class="sxs-lookup"><span data-stu-id="c6dc5-145">**13**</span></span>
</dt> <dd>

<span data-ttu-id="c6dc5-146">O serviço não localizou o serviço necessário em um serviço dependente.</span><span class="sxs-lookup"><span data-stu-id="c6dc5-146">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="c6dc5-147">**14**</span><span class="sxs-lookup"><span data-stu-id="c6dc5-147">**14**</span></span>
</dt> <dd>

<span data-ttu-id="c6dc5-148">O serviço foi desabilitado do sistema.</span><span class="sxs-lookup"><span data-stu-id="c6dc5-148">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c6dc5-149">**15**</span><span class="sxs-lookup"><span data-stu-id="c6dc5-149">**15**</span></span>
</dt> <dd>

<span data-ttu-id="c6dc5-150">O serviço não tem a autenticação correta para ser executado no sistema.</span><span class="sxs-lookup"><span data-stu-id="c6dc5-150">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="c6dc5-151">**16**</span><span class="sxs-lookup"><span data-stu-id="c6dc5-151">**16**</span></span>
</dt> <dd>

<span data-ttu-id="c6dc5-152">Este serviço está sendo removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="c6dc5-152">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c6dc5-153">**17**</span><span class="sxs-lookup"><span data-stu-id="c6dc5-153">**17**</span></span>
</dt> <dd>

<span data-ttu-id="c6dc5-154">O serviço não tem nenhum thread de execução.</span><span class="sxs-lookup"><span data-stu-id="c6dc5-154">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="c6dc5-155">**anos**</span><span class="sxs-lookup"><span data-stu-id="c6dc5-155">**18**</span></span>
</dt> <dd>

<span data-ttu-id="c6dc5-156">O serviço tem dependências circulares quando é iniciado.</span><span class="sxs-lookup"><span data-stu-id="c6dc5-156">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="c6dc5-157">**aprimora**</span><span class="sxs-lookup"><span data-stu-id="c6dc5-157">**19**</span></span>
</dt> <dd>

<span data-ttu-id="c6dc5-158">Um serviço está sendo executado com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="c6dc5-158">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="c6dc5-159">**20**</span><span class="sxs-lookup"><span data-stu-id="c6dc5-159">**20**</span></span>
</dt> <dd>

<span data-ttu-id="c6dc5-160">O nome do serviço tem caracteres inválidos.</span><span class="sxs-lookup"><span data-stu-id="c6dc5-160">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="c6dc5-161">**Abril**</span><span class="sxs-lookup"><span data-stu-id="c6dc5-161">**21**</span></span>
</dt> <dd>

<span data-ttu-id="c6dc5-162">Parâmetros inválidos foram passados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="c6dc5-162">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c6dc5-163">**22**</span><span class="sxs-lookup"><span data-stu-id="c6dc5-163">**22**</span></span>
</dt> <dd>

<span data-ttu-id="c6dc5-164">A conta sob a qual este serviço é executado é inválida ou não tem as permissões para executar o serviço.</span><span class="sxs-lookup"><span data-stu-id="c6dc5-164">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="c6dc5-165">**23**</span><span class="sxs-lookup"><span data-stu-id="c6dc5-165">**23**</span></span>
</dt> <dd>

<span data-ttu-id="c6dc5-166">O serviço existe no banco de dados de serviços disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="c6dc5-166">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c6dc5-167">**24**</span><span class="sxs-lookup"><span data-stu-id="c6dc5-167">**24**</span></span>
</dt> <dd>

<span data-ttu-id="c6dc5-168">O serviço está pausado atualmente no sistema.</span><span class="sxs-lookup"><span data-stu-id="c6dc5-168">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c6dc5-169">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6dc5-169">Remarks</span></span>

<span data-ttu-id="c6dc5-170">A instância do [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa um tipo de dados de [**\_ \_ controle do descritor de segurança**](/windows/desktop/SecAuthZ/security-descriptor-control) e contém uma DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) e uma SACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/s-gly) ) do sistema.</span><span class="sxs-lookup"><span data-stu-id="c6dc5-170">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="c6dc5-171">Para obter mais informações, consulte [listas de controle de acesso](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="c6dc5-171">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="c6dc5-172">Se **SeSecurityPrivilege** não for concedido ou habilitado ao obter um descritor de segurança, somente a DACL será retornada no descritor de segurança retornado.</span><span class="sxs-lookup"><span data-stu-id="c6dc5-172">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="c6dc5-173">Para obter mais informações, consulte [**constantes de privilégio**](/windows/desktop/WmiSdk/privilege-constants) e [executando operações privilegiadas](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="c6dc5-173">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="c6dc5-174">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c6dc5-174">Examples</span></span>

<span data-ttu-id="c6dc5-175">Ao recuperar um descritor de segurança no VBScript, certifique-se de "segurança" e execute como administrador, conforme mostrado no trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="c6dc5-175">When retrieving a security descriptor in VBScript, be sure to "Security" and run as as Admin, as shown in the following code snippet.</span></span> <span data-ttu-id="c6dc5-176">Caso contrário, seu código pode gerar um erro de permissões.</span><span class="sxs-lookup"><span data-stu-id="c6dc5-176">Otherwise, your code may throw a permissions error.</span></span>


```VB
Set objWMIService = GetObject("winmgmts:" _
  & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")
```



<span data-ttu-id="c6dc5-177">Da mesma forma, em VB.NET, certifique-se de definir "EnablePrivileges = true" e executar o aplicativo como administrador.</span><span class="sxs-lookup"><span data-stu-id="c6dc5-177">Similarly, in VB.NET, be sure to set "EnablePrivileges = True" and run the Application as Admin.</span></span>


```VB
Scope = New ManagementScope([String].Format("\\{0}\root\CIMV2", ComputerName), Nothing)
Scope.Options.EnablePrivileges = True
```



## <a name="requirements"></a><span data-ttu-id="c6dc5-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6dc5-178">Requirements</span></span>



| <span data-ttu-id="c6dc5-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6dc5-179">Requirement</span></span> | <span data-ttu-id="c6dc5-180">Valor</span><span class="sxs-lookup"><span data-stu-id="c6dc5-180">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6dc5-181">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c6dc5-181">Minimum supported client</span></span><br/> | <span data-ttu-id="c6dc5-182">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c6dc5-182">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c6dc5-183">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c6dc5-183">Minimum supported server</span></span><br/> | <span data-ttu-id="c6dc5-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c6dc5-184">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c6dc5-185">Namespace</span><span class="sxs-lookup"><span data-stu-id="c6dc5-185">Namespace</span></span><br/>                | <span data-ttu-id="c6dc5-186">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="c6dc5-186">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c6dc5-187">MOF</span><span class="sxs-lookup"><span data-stu-id="c6dc5-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c6dc5-188"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c6dc5-188"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c6dc5-189">DLL</span><span class="sxs-lookup"><span data-stu-id="c6dc5-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6dc5-190"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6dc5-190"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6dc5-191">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c6dc5-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6dc5-192">**\_Serviço Win32**</span><span class="sxs-lookup"><span data-stu-id="c6dc5-192">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="c6dc5-193">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="c6dc5-193">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="c6dc5-194">**Constantes de privilégio**</span><span class="sxs-lookup"><span data-stu-id="c6dc5-194">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="c6dc5-195">Objetos do descritor de segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="c6dc5-195">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="c6dc5-196">Alterando a segurança de acesso em objetos protegíveis</span><span class="sxs-lookup"><span data-stu-id="c6dc5-196">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[<span data-ttu-id="c6dc5-197">Controle de conta de usuário e WMI</span><span class="sxs-lookup"><span data-stu-id="c6dc5-197">User Account Control and WMI</span></span>](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 


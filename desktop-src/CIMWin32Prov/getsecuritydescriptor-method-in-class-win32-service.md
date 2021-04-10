---
description: Retorna o descritor de segurança que controla o acesso ao serviço.
ms.assetid: 99c8346e-e8d6-4f3c-bbdc-437dcf852b2a
ms.tgt_platform: multiple
title: Método GetSecurityDescriptor da classe Win32_Service (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.GetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5bf8dee49893a5a1d3b628e72b0b0746a6215fb0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010155"
---
# <a name="getsecuritydescriptor-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="8378f-103">Método GetSecurityDescriptor da classe Win32_Service (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="8378f-103">GetSecurityDescriptor method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="8378f-104">O método **GetSecurityDescriptor** retorna o descritor de segurança que controla o acesso ao serviço.</span><span class="sxs-lookup"><span data-stu-id="8378f-104">The **GetSecurityDescriptor** method returns the security descriptor that controls access to the service.</span></span> <span data-ttu-id="8378f-105">O descritor é retornado como uma instância do [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="8378f-105">The descriptor is returned as an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span>

## <a name="syntax"></a><span data-ttu-id="8378f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8378f-106">Syntax</span></span>


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="8378f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8378f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8378f-108">*Descritor* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8378f-108">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8378f-109">O descritor de segurança associado ao serviço.</span><span class="sxs-lookup"><span data-stu-id="8378f-109">The security descriptor associated with the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8378f-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8378f-110">Return value</span></span>

<span data-ttu-id="8378f-111">Retorna um dos valores listados na lista a seguir ou um valor diferente para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="8378f-111">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="8378f-112">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="8378f-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="8378f-113">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="8378f-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="8378f-114">**Êxito**</span><span class="sxs-lookup"><span data-stu-id="8378f-114">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="8378f-115">0</span><span class="sxs-lookup"><span data-stu-id="8378f-115">0</span></span>

<span data-ttu-id="8378f-116">A solicitação foi aceita.</span><span class="sxs-lookup"><span data-stu-id="8378f-116">The request was accepted.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8378f-117">1</span><span class="sxs-lookup"><span data-stu-id="8378f-117">1</span></span>

<span data-ttu-id="8378f-118">A solicitação não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="8378f-118">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="8378f-119">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="8378f-119">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="8378f-120">2</span><span class="sxs-lookup"><span data-stu-id="8378f-120">2</span></span>

<span data-ttu-id="8378f-121">O usuário não tinha o acesso necessário.</span><span class="sxs-lookup"><span data-stu-id="8378f-121">The user did not have the necessary access.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8378f-122">3</span><span class="sxs-lookup"><span data-stu-id="8378f-122">3</span></span>

<span data-ttu-id="8378f-123">O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.</span><span class="sxs-lookup"><span data-stu-id="8378f-123">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8378f-124">4</span><span class="sxs-lookup"><span data-stu-id="8378f-124">4</span></span>

<span data-ttu-id="8378f-125">O código de controle pedido não é válido ou é inaceitável para o serviço.</span><span class="sxs-lookup"><span data-stu-id="8378f-125">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8378f-126">5</span><span class="sxs-lookup"><span data-stu-id="8378f-126">5</span></span>

<span data-ttu-id="8378f-127">O código de controle solicitado não pode ser enviado ao serviço porque o estado do serviço ([**Win32 \_ BaseService**](win32-baseservice.md).\*\*\*\* A propriedade State) é igual a 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="8378f-127">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8378f-128">6</span><span class="sxs-lookup"><span data-stu-id="8378f-128">6</span></span>

<span data-ttu-id="8378f-129">O serviço não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="8378f-129">The service has not been started.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8378f-130">7</span><span class="sxs-lookup"><span data-stu-id="8378f-130">7</span></span>

<span data-ttu-id="8378f-131">O serviço não respondeu à solicitação de início em um tempo oportuno.</span><span class="sxs-lookup"><span data-stu-id="8378f-131">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="8378f-132">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="8378f-132">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="8378f-133">8</span><span class="sxs-lookup"><span data-stu-id="8378f-133">8</span></span>

<span data-ttu-id="8378f-134">Falha desconhecida ao iniciar o serviço.</span><span class="sxs-lookup"><span data-stu-id="8378f-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="8378f-135">**Privilégio ausente**</span><span class="sxs-lookup"><span data-stu-id="8378f-135">**Privilege missing**</span></span>
</dt> <dd>

<span data-ttu-id="8378f-136">9</span><span class="sxs-lookup"><span data-stu-id="8378f-136">9</span></span>

<span data-ttu-id="8378f-137">O caminho do diretório para o arquivo executável do serviço não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="8378f-137">The directory path to the service executable file was not found.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8378f-138">10</span><span class="sxs-lookup"><span data-stu-id="8378f-138">10</span></span>

<span data-ttu-id="8378f-139">O serviço já está em execução.</span><span class="sxs-lookup"><span data-stu-id="8378f-139">The service is already running.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8378f-140">11</span><span class="sxs-lookup"><span data-stu-id="8378f-140">11</span></span>

<span data-ttu-id="8378f-141">O banco de dados para adicionar um serviço novo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="8378f-141">The database to add a new service is locked.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8378f-142">12</span><span class="sxs-lookup"><span data-stu-id="8378f-142">12</span></span>

<span data-ttu-id="8378f-143">Uma dependência da qual esse serviço depende foi removida do sistema.</span><span class="sxs-lookup"><span data-stu-id="8378f-143">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8378f-144">13</span><span class="sxs-lookup"><span data-stu-id="8378f-144">13</span></span>

<span data-ttu-id="8378f-145">O serviço não localizou o serviço necessário em um serviço dependente.</span><span class="sxs-lookup"><span data-stu-id="8378f-145">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8378f-146">14</span><span class="sxs-lookup"><span data-stu-id="8378f-146">14</span></span>

<span data-ttu-id="8378f-147">O serviço foi desabilitado do sistema.</span><span class="sxs-lookup"><span data-stu-id="8378f-147">The service has been disabled from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8378f-148">15</span><span class="sxs-lookup"><span data-stu-id="8378f-148">15</span></span>

<span data-ttu-id="8378f-149">O serviço não tem a autenticação correta para ser executado no sistema.</span><span class="sxs-lookup"><span data-stu-id="8378f-149">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8378f-150">16</span><span class="sxs-lookup"><span data-stu-id="8378f-150">16</span></span>

<span data-ttu-id="8378f-151">Este serviço está sendo removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="8378f-151">This service is being removed from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8378f-152">17</span><span class="sxs-lookup"><span data-stu-id="8378f-152">17</span></span>

<span data-ttu-id="8378f-153">O serviço não tem nenhum thread de execução.</span><span class="sxs-lookup"><span data-stu-id="8378f-153">The service has no execution thread.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8378f-154">18</span><span class="sxs-lookup"><span data-stu-id="8378f-154">18</span></span>

<span data-ttu-id="8378f-155">O serviço tem dependências circulares quando é iniciado.</span><span class="sxs-lookup"><span data-stu-id="8378f-155">The service has circular dependencies when it starts.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8378f-156">19</span><span class="sxs-lookup"><span data-stu-id="8378f-156">19</span></span>

<span data-ttu-id="8378f-157">Um serviço está sendo executado com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="8378f-157">A service is running under the same name.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8378f-158">20</span><span class="sxs-lookup"><span data-stu-id="8378f-158">20</span></span>

<span data-ttu-id="8378f-159">O nome do serviço tem caracteres inválidos.</span><span class="sxs-lookup"><span data-stu-id="8378f-159">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="8378f-160">**Parâmetro inválido**</span><span class="sxs-lookup"><span data-stu-id="8378f-160">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="8378f-161">21</span><span class="sxs-lookup"><span data-stu-id="8378f-161">21</span></span>

<span data-ttu-id="8378f-162">Parâmetros inválidos foram passados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="8378f-162">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8378f-163">22</span><span class="sxs-lookup"><span data-stu-id="8378f-163">22</span></span>

<span data-ttu-id="8378f-164">A conta sob a qual este serviço é executado é inválida ou não tem as permissões para executar o serviço.</span><span class="sxs-lookup"><span data-stu-id="8378f-164">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8378f-165">23</span><span class="sxs-lookup"><span data-stu-id="8378f-165">23</span></span>

<span data-ttu-id="8378f-166">O serviço existe no banco de dados de serviços disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="8378f-166">The service exists in the database of services available from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8378f-167">24</span><span class="sxs-lookup"><span data-stu-id="8378f-167">24</span></span>

<span data-ttu-id="8378f-168">O serviço está pausado atualmente no sistema.</span><span class="sxs-lookup"><span data-stu-id="8378f-168">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="8378f-169">**Outras**</span><span class="sxs-lookup"><span data-stu-id="8378f-169">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="8378f-170">22 4294967295</span><span class="sxs-lookup"><span data-stu-id="8378f-170">22 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8378f-171">Comentários</span><span class="sxs-lookup"><span data-stu-id="8378f-171">Remarks</span></span>

<span data-ttu-id="8378f-172">A instância do [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa um tipo de dados de [**\_ \_ controle do descritor de segurança**](/windows/desktop/SecAuthZ/security-descriptor-control) e contém uma DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) e uma SACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/s-gly) ) do sistema.</span><span class="sxs-lookup"><span data-stu-id="8378f-172">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="8378f-173">Para obter mais informações, consulte [listas de controle de acesso](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="8378f-173">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="8378f-174">Se **SeSecurityPrivilege** não for concedido ou habilitado ao obter um descritor de segurança, somente a DACL será retornada no descritor de segurança retornado.</span><span class="sxs-lookup"><span data-stu-id="8378f-174">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="8378f-175">Para obter mais informações, consulte [**constantes de privilégio**](/windows/desktop/WmiSdk/privilege-constants) e [executando operações privilegiadas](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="8378f-175">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="8378f-176">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8378f-176">Examples</span></span>

<span data-ttu-id="8378f-177">Ao recuperar um descritor de segurança no VBScript, certifique-se de "segurança" e execute como administrador, conforme mostrado no trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="8378f-177">When retrieving a security descriptor in VBScript, be sure to "Security" and run as as Admin, as shown in the following code snippet.</span></span> <span data-ttu-id="8378f-178">Caso contrário, seu código pode gerar um erro de permissões.</span><span class="sxs-lookup"><span data-stu-id="8378f-178">Otherwise, your code may throw a permissions error.</span></span>


```VB
Set objWMIService = GetObject("winmgmts:" _
  & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")
```



<span data-ttu-id="8378f-179">Da mesma forma, em VB.NET, certifique-se de definir "EnablePrivileges = true" e executar o aplicativo como administrador.</span><span class="sxs-lookup"><span data-stu-id="8378f-179">Similarly, in VB.NET, be sure to set "EnablePrivileges = True" and run the Application as Admin.</span></span>


```VB
Scope = New ManagementScope([String].Format("\\{0}\root\CIMV2", ComputerName), Nothing)
Scope.Options.EnablePrivileges = True
```



## <a name="requirements"></a><span data-ttu-id="8378f-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8378f-180">Requirements</span></span>



| <span data-ttu-id="8378f-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="8378f-181">Requirement</span></span> | <span data-ttu-id="8378f-182">Valor</span><span class="sxs-lookup"><span data-stu-id="8378f-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8378f-183">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8378f-183">Minimum supported client</span></span><br/> | <span data-ttu-id="8378f-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8378f-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8378f-185">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8378f-185">Minimum supported server</span></span><br/> | <span data-ttu-id="8378f-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8378f-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8378f-187">Namespace</span><span class="sxs-lookup"><span data-stu-id="8378f-187">Namespace</span></span><br/>                | <span data-ttu-id="8378f-188">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8378f-188">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8378f-189">MOF</span><span class="sxs-lookup"><span data-stu-id="8378f-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8378f-190"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8378f-190"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8378f-191">DLL</span><span class="sxs-lookup"><span data-stu-id="8378f-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8378f-192"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8378f-192"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8378f-193">Confira também</span><span class="sxs-lookup"><span data-stu-id="8378f-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8378f-194">**\_Serviço Win32**</span><span class="sxs-lookup"><span data-stu-id="8378f-194">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="8378f-195">**Constantes de privilégio**</span><span class="sxs-lookup"><span data-stu-id="8378f-195">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="8378f-196">Objetos do descritor de segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="8378f-196">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="8378f-197">Alterando a segurança de acesso em objetos protegíveis</span><span class="sxs-lookup"><span data-stu-id="8378f-197">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[<span data-ttu-id="8378f-198">Controle de conta de usuário e WMI</span><span class="sxs-lookup"><span data-stu-id="8378f-198">User Account Control and WMI</span></span>](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 


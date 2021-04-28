---
title: Método SetSecurityDescriptor da classe Win32_Service (Serviços de Área de Trabalho Remota)
description: Método SetSecurityDescriptor da classe Win32_Service (Serviços de Área de Trabalho Remota) – grava uma versão atualizada do descritor de segurança que controla o acesso ao serviço.
ms.assetid: 4F03B798-0912-4A0D-B31E-419662D5849B
ms.tgt_platform: multiple
keywords:
- Instrumentação de Gerenciamento do Windows de script, segurança
- Instrumentação de Gerenciamento do Windows de segurança, scripts
- Serviços de Área de Trabalho Remota do método SetSecurityDescriptor
- Método SetSecurityDescriptor Serviços de Área de Trabalho Remota, classe Win32_Service
- Classe Win32_Service Serviços de Área de Trabalho Remota, método SetSecurityDescriptor
topic_type:
- apiref
api_name:
- Win32_Service.SetSecurityDescriptor
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb2dd7e43041c05b1c294181f8bd01548ed76d87
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114485"
---
# <a name="setsecuritydescriptor-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="2e87a-108">Método SetSecurityDescriptor da classe Win32_Service (Serviços de Área de Trabalho Remota)</span><span class="sxs-lookup"><span data-stu-id="2e87a-108">SetSecurityDescriptor method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="2e87a-109">O método **SetSecurityDescriptor** grava uma versão atualizada do descritor de segurança que controla o acesso ao serviço.</span><span class="sxs-lookup"><span data-stu-id="2e87a-109">The **SetSecurityDescriptor** method writes an updated version of the security descriptor that controls access to the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e87a-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2e87a-110">Syntax</span></span>


```mof
uint32 SetSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="2e87a-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e87a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e87a-112">*Descritor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2e87a-112">*Descriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e87a-113">O descritor de segurança associado ao serviço.</span><span class="sxs-lookup"><span data-stu-id="2e87a-113">The security descriptor associated with the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e87a-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2e87a-114">Return value</span></span>

<span data-ttu-id="2e87a-115">Retorna um dos valores listados na lista a seguir ou um valor diferente para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="2e87a-115">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="2e87a-116">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="2e87a-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="2e87a-117">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="2e87a-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="2e87a-118">**0**</span><span class="sxs-lookup"><span data-stu-id="2e87a-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="2e87a-119">A solicitação foi aceita.</span><span class="sxs-lookup"><span data-stu-id="2e87a-119">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="2e87a-120">**1**</span><span class="sxs-lookup"><span data-stu-id="2e87a-120">**1**</span></span>
</dt> <dd>

<span data-ttu-id="2e87a-121">A solicitação não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="2e87a-121">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="2e87a-122">**2**</span><span class="sxs-lookup"><span data-stu-id="2e87a-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="2e87a-123">O usuário não tinha o acesso necessário.</span><span class="sxs-lookup"><span data-stu-id="2e87a-123">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="2e87a-124">**3**</span><span class="sxs-lookup"><span data-stu-id="2e87a-124">**3**</span></span>
</dt> <dd>

<span data-ttu-id="2e87a-125">O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.</span><span class="sxs-lookup"><span data-stu-id="2e87a-125">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="2e87a-126">**4**</span><span class="sxs-lookup"><span data-stu-id="2e87a-126">**4**</span></span>
</dt> <dd>

<span data-ttu-id="2e87a-127">O código de controle pedido não é válido ou é inaceitável para o serviço.</span><span class="sxs-lookup"><span data-stu-id="2e87a-127">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="2e87a-128">**5**</span><span class="sxs-lookup"><span data-stu-id="2e87a-128">**5**</span></span>
</dt> <dd>

<span data-ttu-id="2e87a-129">O código de controle solicitado não pode ser enviado ao serviço porque o estado do serviço ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).\*\*\*\* A propriedade State) é igual a 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="2e87a-129">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="2e87a-130">**6**</span><span class="sxs-lookup"><span data-stu-id="2e87a-130">**6**</span></span>
</dt> <dd>

<span data-ttu-id="2e87a-131">O serviço não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="2e87a-131">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="2e87a-132">**7**</span><span class="sxs-lookup"><span data-stu-id="2e87a-132">**7**</span></span>
</dt> <dd>

<span data-ttu-id="2e87a-133">O serviço não respondeu à solicitação de início em um tempo oportuno.</span><span class="sxs-lookup"><span data-stu-id="2e87a-133">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="2e87a-134">**8**</span><span class="sxs-lookup"><span data-stu-id="2e87a-134">**8**</span></span>
</dt> <dd>

<span data-ttu-id="2e87a-135">Falha desconhecida ao iniciar o serviço.</span><span class="sxs-lookup"><span data-stu-id="2e87a-135">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="2e87a-136">**9**</span><span class="sxs-lookup"><span data-stu-id="2e87a-136">**9**</span></span>
</dt> <dd>

<span data-ttu-id="2e87a-137">O caminho do diretório para o arquivo executável do serviço não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="2e87a-137">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="2e87a-138">**10**</span><span class="sxs-lookup"><span data-stu-id="2e87a-138">**10**</span></span>
</dt> <dd>

<span data-ttu-id="2e87a-139">O serviço já está em execução.</span><span class="sxs-lookup"><span data-stu-id="2e87a-139">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="2e87a-140">**11**</span><span class="sxs-lookup"><span data-stu-id="2e87a-140">**11**</span></span>
</dt> <dd>

<span data-ttu-id="2e87a-141">O banco de dados para adicionar um serviço novo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="2e87a-141">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="2e87a-142">**12**</span><span class="sxs-lookup"><span data-stu-id="2e87a-142">**12**</span></span>
</dt> <dd>

<span data-ttu-id="2e87a-143">Uma dependência da qual esse serviço depende foi removida do sistema.</span><span class="sxs-lookup"><span data-stu-id="2e87a-143">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="2e87a-144">**13**</span><span class="sxs-lookup"><span data-stu-id="2e87a-144">**13**</span></span>
</dt> <dd>

<span data-ttu-id="2e87a-145">O serviço não localizou o serviço necessário em um serviço dependente.</span><span class="sxs-lookup"><span data-stu-id="2e87a-145">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="2e87a-146">**14**</span><span class="sxs-lookup"><span data-stu-id="2e87a-146">**14**</span></span>
</dt> <dd>

<span data-ttu-id="2e87a-147">O serviço foi desabilitado do sistema.</span><span class="sxs-lookup"><span data-stu-id="2e87a-147">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="2e87a-148">**15**</span><span class="sxs-lookup"><span data-stu-id="2e87a-148">**15**</span></span>
</dt> <dd>

<span data-ttu-id="2e87a-149">O serviço não tem a autenticação correta para ser executado no sistema.</span><span class="sxs-lookup"><span data-stu-id="2e87a-149">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="2e87a-150">**16**</span><span class="sxs-lookup"><span data-stu-id="2e87a-150">**16**</span></span>
</dt> <dd>

<span data-ttu-id="2e87a-151">Este serviço está sendo removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="2e87a-151">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="2e87a-152">**17**</span><span class="sxs-lookup"><span data-stu-id="2e87a-152">**17**</span></span>
</dt> <dd>

<span data-ttu-id="2e87a-153">O serviço não tem nenhum thread de execução.</span><span class="sxs-lookup"><span data-stu-id="2e87a-153">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="2e87a-154">**anos**</span><span class="sxs-lookup"><span data-stu-id="2e87a-154">**18**</span></span>
</dt> <dd>

<span data-ttu-id="2e87a-155">O serviço tem dependências circulares quando é iniciado.</span><span class="sxs-lookup"><span data-stu-id="2e87a-155">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="2e87a-156">**aprimora**</span><span class="sxs-lookup"><span data-stu-id="2e87a-156">**19**</span></span>
</dt> <dd>

<span data-ttu-id="2e87a-157">Um serviço está sendo executado com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="2e87a-157">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="2e87a-158">**20**</span><span class="sxs-lookup"><span data-stu-id="2e87a-158">**20**</span></span>
</dt> <dd>

<span data-ttu-id="2e87a-159">O nome do serviço tem caracteres inválidos.</span><span class="sxs-lookup"><span data-stu-id="2e87a-159">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="2e87a-160">**Abril**</span><span class="sxs-lookup"><span data-stu-id="2e87a-160">**21**</span></span>
</dt> <dd>

<span data-ttu-id="2e87a-161">Parâmetros inválidos foram passados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="2e87a-161">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="2e87a-162">**22**</span><span class="sxs-lookup"><span data-stu-id="2e87a-162">**22**</span></span>
</dt> <dd>

<span data-ttu-id="2e87a-163">A conta sob a qual este serviço é executado é inválida ou não tem as permissões para executar o serviço.</span><span class="sxs-lookup"><span data-stu-id="2e87a-163">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="2e87a-164">**23**</span><span class="sxs-lookup"><span data-stu-id="2e87a-164">**23**</span></span>
</dt> <dd>

<span data-ttu-id="2e87a-165">O serviço existe no banco de dados de serviços disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="2e87a-165">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="2e87a-166">**24**</span><span class="sxs-lookup"><span data-stu-id="2e87a-166">**24**</span></span>
</dt> <dd>

<span data-ttu-id="2e87a-167">O serviço está pausado atualmente no sistema.</span><span class="sxs-lookup"><span data-stu-id="2e87a-167">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e87a-168">Comentários</span><span class="sxs-lookup"><span data-stu-id="2e87a-168">Remarks</span></span>

<span data-ttu-id="2e87a-169">A instância do [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa um tipo de dados de [**\_ \_ controle do descritor de segurança**](/windows/desktop/SecAuthZ/security-descriptor-control) e contém uma DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) e uma SACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/s-gly) ) do sistema.</span><span class="sxs-lookup"><span data-stu-id="2e87a-169">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="2e87a-170">Para obter mais informações, consulte [listas de controle de acesso](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="2e87a-170">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="2e87a-171">Se **SeSecurityPrivilege** não for concedido ou habilitado ao obter um descritor de segurança, somente a DACL será retornada no descritor de segurança retornado.</span><span class="sxs-lookup"><span data-stu-id="2e87a-171">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="2e87a-172">Para obter mais informações, consulte [**constantes de privilégio**](/windows/desktop/WmiSdk/privilege-constants) e [executando operações privilegiadas](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="2e87a-172">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

<span data-ttu-id="2e87a-173">Você pode atualizar a DACL e a SACL na instância [**\_ SecurityDescriptor do Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) ao chamar esse método, mas também pode atualizar apenas a DACL ou apenas a SACL.</span><span class="sxs-lookup"><span data-stu-id="2e87a-173">You can update both the DACL and the SACL in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance when calling this method, but you also can update only the DACL or only the SACL.</span></span>

<span data-ttu-id="2e87a-174">Os valores a seguir [**no \_ \_ controle do descritor de segurança**](/windows/desktop/SecAuthZ/security-descriptor-control) determinam se a DACL, a SACL ou ambas são atualizadas.</span><span class="sxs-lookup"><span data-stu-id="2e87a-174">The following values in [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determine whether the DACL, the SACL, or both are updated.</span></span>

-   <span data-ttu-id="2e87a-175">**\_DACL \_ presente**</span><span class="sxs-lookup"><span data-stu-id="2e87a-175">**SE\_DACL\_PRESENT**</span></span>

    <span data-ttu-id="2e87a-176">Indica que a DACL deve ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="2e87a-176">Indicates that the DACL should be updated.</span></span> <span data-ttu-id="2e87a-177">Se isso não for definido, o WMI preservará o valor original da DACL.</span><span class="sxs-lookup"><span data-stu-id="2e87a-177">If this is not set, then WMI preserves the original value of the DACL.</span></span>

-   <span data-ttu-id="2e87a-178">**\_SACL \_ presente**</span><span class="sxs-lookup"><span data-stu-id="2e87a-178">**SE\_SACL\_PRESENT**</span></span>

    <span data-ttu-id="2e87a-179">Indica que a SACL deve ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="2e87a-179">Indicates that the SACL should be updated.</span></span> <span data-ttu-id="2e87a-180">Se isso não for definido, o WMI preservará o valor original da SACL.</span><span class="sxs-lookup"><span data-stu-id="2e87a-180">If this is not set, then WMI preserves the original value of the SACL.</span></span> <span data-ttu-id="2e87a-181">Para atualizar a SACL, a conta deve ter o privilégio **SeSecurityPrivilege** habilitado.</span><span class="sxs-lookup"><span data-stu-id="2e87a-181">To update the SACL, the account must have the **SeSecurityPrivilege** privilege enabled.</span></span> <span data-ttu-id="2e87a-182">Para scripts, o nome do privilégio é **SeSecurityPrivilege**.</span><span class="sxs-lookup"><span data-stu-id="2e87a-182">For scripting, the privilege name is **SeSecurityPrivilege**.</span></span> <span data-ttu-id="2e87a-183">Para obter mais informações, consulte [**constantes de privilégio**](/windows/desktop/WmiSdk/privilege-constants).</span><span class="sxs-lookup"><span data-stu-id="2e87a-183">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants).</span></span>

<span data-ttu-id="2e87a-184">Se o grupo de confiança e as propriedades de confiança do proprietário não forem **nulas**, eles serão atualizados.</span><span class="sxs-lookup"><span data-stu-id="2e87a-184">If the Group trustee and the Owner trustee properties are not **NULL**, then they are updated.</span></span> <span data-ttu-id="2e87a-185">Caso contrário, o WMI preservará os valores originais.</span><span class="sxs-lookup"><span data-stu-id="2e87a-185">Otherwise, WMI preserves the original values.</span></span> <span data-ttu-id="2e87a-186">Para obter mais informações, consulte [objetos do descritor de segurança do WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span><span class="sxs-lookup"><span data-stu-id="2e87a-186">For more information, see [WMI Security Descriptor Objects](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span></span>

<span data-ttu-id="2e87a-187">Quando uma nova SACL é **nula** em uma chamada desse método, a SACL do descritor de segurança no objeto protegível de destino permanece inalterada.</span><span class="sxs-lookup"><span data-stu-id="2e87a-187">When a new SACL is **NULL** in a call this method, then the security descriptor SACL on the target securable object is left unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e87a-188">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e87a-188">Requirements</span></span>



| <span data-ttu-id="2e87a-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e87a-189">Requirement</span></span> | <span data-ttu-id="2e87a-190">Valor</span><span class="sxs-lookup"><span data-stu-id="2e87a-190">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e87a-191">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e87a-191">Minimum supported client</span></span><br/> | <span data-ttu-id="2e87a-192">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2e87a-192">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2e87a-193">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e87a-193">Minimum supported server</span></span><br/> | <span data-ttu-id="2e87a-194">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e87a-194">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2e87a-195">Namespace</span><span class="sxs-lookup"><span data-stu-id="2e87a-195">Namespace</span></span><br/>                | <span data-ttu-id="2e87a-196">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="2e87a-196">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="2e87a-197">MOF</span><span class="sxs-lookup"><span data-stu-id="2e87a-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e87a-198"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e87a-198"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e87a-199">DLL</span><span class="sxs-lookup"><span data-stu-id="2e87a-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e87a-200"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e87a-200"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e87a-201">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2e87a-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e87a-202">**\_Serviço Win32**</span><span class="sxs-lookup"><span data-stu-id="2e87a-202">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="2e87a-203">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="2e87a-203">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="2e87a-204">**Constantes de privilégio**</span><span class="sxs-lookup"><span data-stu-id="2e87a-204">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="2e87a-205">Objetos do descritor de segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="2e87a-205">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="2e87a-206">Alterando a segurança de acesso em objetos protegíveis</span><span class="sxs-lookup"><span data-stu-id="2e87a-206">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[<span data-ttu-id="2e87a-207">Controle de conta de usuário e WMI</span><span class="sxs-lookup"><span data-stu-id="2e87a-207">User Account Control and WMI</span></span>](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 


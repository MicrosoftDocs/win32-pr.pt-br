---
description: Grava uma versão atualizada do descritor de segurança que controla o acesso ao serviço.
ms.assetid: c1745b69-f355-4b4c-9e58-6a76c230f498
ms.tgt_platform: multiple
title: Método SetSecurityDescriptor da classe Win32_Service (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.SetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 82c08f9c560a1d8e419d9a8f6474f8ea9db4e541
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105769042"
---
# <a name="setsecuritydescriptor-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="95b3f-103">Método SetSecurityDescriptor da classe Win32_Service (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="95b3f-103">SetSecurityDescriptor method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="95b3f-104">O método **SetSecurityDescriptor** grava uma versão atualizada do descritor de segurança que controla o acesso ao serviço.</span><span class="sxs-lookup"><span data-stu-id="95b3f-104">The **SetSecurityDescriptor** method writes an updated version of the security descriptor that controls access to the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="95b3f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="95b3f-105">Syntax</span></span>


```mof
uint32 SetSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="95b3f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="95b3f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95b3f-107">*Descritor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="95b3f-107">*Descriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95b3f-108">O descritor de segurança associado ao serviço.</span><span class="sxs-lookup"><span data-stu-id="95b3f-108">The security descriptor associated with the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95b3f-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="95b3f-109">Return value</span></span>

<span data-ttu-id="95b3f-110">Retorna um dos valores listados na lista a seguir ou um valor diferente para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="95b3f-110">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="95b3f-111">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="95b3f-111">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="95b3f-112">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="95b3f-112">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="95b3f-113">**Êxito**</span><span class="sxs-lookup"><span data-stu-id="95b3f-113">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="95b3f-114">0</span><span class="sxs-lookup"><span data-stu-id="95b3f-114">0</span></span>

<span data-ttu-id="95b3f-115">A solicitação foi aceita.</span><span class="sxs-lookup"><span data-stu-id="95b3f-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="95b3f-116">**1**</span><span class="sxs-lookup"><span data-stu-id="95b3f-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="95b3f-117">A solicitação não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="95b3f-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="95b3f-118">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="95b3f-118">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="95b3f-119">2</span><span class="sxs-lookup"><span data-stu-id="95b3f-119">2</span></span>

<span data-ttu-id="95b3f-120">O usuário não tinha o acesso necessário.</span><span class="sxs-lookup"><span data-stu-id="95b3f-120">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="95b3f-121">**3**</span><span class="sxs-lookup"><span data-stu-id="95b3f-121">**3**</span></span>
</dt> <dd>

<span data-ttu-id="95b3f-122">O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.</span><span class="sxs-lookup"><span data-stu-id="95b3f-122">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="95b3f-123">**4**</span><span class="sxs-lookup"><span data-stu-id="95b3f-123">**4**</span></span>
</dt> <dd>

<span data-ttu-id="95b3f-124">O código de controle pedido não é válido ou é inaceitável para o serviço.</span><span class="sxs-lookup"><span data-stu-id="95b3f-124">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="95b3f-125">**5**</span><span class="sxs-lookup"><span data-stu-id="95b3f-125">**5**</span></span>
</dt> <dd>

<span data-ttu-id="95b3f-126">O código de controle solicitado não pode ser enviado ao serviço porque o estado do serviço ([**Win32 \_ BaseService**](win32-baseservice.md).\*\*\*\* A propriedade State) é igual a 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="95b3f-126">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="95b3f-127">**6**</span><span class="sxs-lookup"><span data-stu-id="95b3f-127">**6**</span></span>
</dt> <dd>

<span data-ttu-id="95b3f-128">O serviço não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="95b3f-128">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="95b3f-129">**7**</span><span class="sxs-lookup"><span data-stu-id="95b3f-129">**7**</span></span>
</dt> <dd>

<span data-ttu-id="95b3f-130">O serviço não respondeu à solicitação de início em um tempo oportuno.</span><span class="sxs-lookup"><span data-stu-id="95b3f-130">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="95b3f-131">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="95b3f-131">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="95b3f-132">8</span><span class="sxs-lookup"><span data-stu-id="95b3f-132">8</span></span>

<span data-ttu-id="95b3f-133">Falha desconhecida ao iniciar o serviço.</span><span class="sxs-lookup"><span data-stu-id="95b3f-133">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="95b3f-134">**Privilégio ausente**</span><span class="sxs-lookup"><span data-stu-id="95b3f-134">**Privilege missing**</span></span>
</dt> <dd>

<span data-ttu-id="95b3f-135">9</span><span class="sxs-lookup"><span data-stu-id="95b3f-135">9</span></span>

<span data-ttu-id="95b3f-136">O caminho do diretório para o arquivo executável do serviço não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="95b3f-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="95b3f-137">**10**</span><span class="sxs-lookup"><span data-stu-id="95b3f-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="95b3f-138">O serviço já está em execução.</span><span class="sxs-lookup"><span data-stu-id="95b3f-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="95b3f-139">**11**</span><span class="sxs-lookup"><span data-stu-id="95b3f-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="95b3f-140">O banco de dados para adicionar um serviço novo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="95b3f-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="95b3f-141">**12**</span><span class="sxs-lookup"><span data-stu-id="95b3f-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="95b3f-142">Uma dependência da qual esse serviço depende foi removida do sistema.</span><span class="sxs-lookup"><span data-stu-id="95b3f-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="95b3f-143">**13**</span><span class="sxs-lookup"><span data-stu-id="95b3f-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="95b3f-144">O serviço não localizou o serviço necessário em um serviço dependente.</span><span class="sxs-lookup"><span data-stu-id="95b3f-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="95b3f-145">**14**</span><span class="sxs-lookup"><span data-stu-id="95b3f-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="95b3f-146">O serviço foi desabilitado do sistema.</span><span class="sxs-lookup"><span data-stu-id="95b3f-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="95b3f-147">**15**</span><span class="sxs-lookup"><span data-stu-id="95b3f-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="95b3f-148">O serviço não tem a autenticação correta para ser executado no sistema.</span><span class="sxs-lookup"><span data-stu-id="95b3f-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="95b3f-149">**16**</span><span class="sxs-lookup"><span data-stu-id="95b3f-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="95b3f-150">Este serviço está sendo removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="95b3f-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="95b3f-151">**17**</span><span class="sxs-lookup"><span data-stu-id="95b3f-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="95b3f-152">O serviço não tem nenhum thread de execução.</span><span class="sxs-lookup"><span data-stu-id="95b3f-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="95b3f-153">**anos**</span><span class="sxs-lookup"><span data-stu-id="95b3f-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="95b3f-154">O serviço tem dependências circulares quando é iniciado.</span><span class="sxs-lookup"><span data-stu-id="95b3f-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="95b3f-155">**aprimora**</span><span class="sxs-lookup"><span data-stu-id="95b3f-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="95b3f-156">Um serviço está sendo executado com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="95b3f-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="95b3f-157">**20**</span><span class="sxs-lookup"><span data-stu-id="95b3f-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="95b3f-158">O nome do serviço tem caracteres inválidos.</span><span class="sxs-lookup"><span data-stu-id="95b3f-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="95b3f-159">**Parâmetro inválido**</span><span class="sxs-lookup"><span data-stu-id="95b3f-159">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="95b3f-160">21</span><span class="sxs-lookup"><span data-stu-id="95b3f-160">21</span></span>

<span data-ttu-id="95b3f-161">Parâmetros inválidos foram passados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="95b3f-161">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="95b3f-162">**22**</span><span class="sxs-lookup"><span data-stu-id="95b3f-162">**22**</span></span>
</dt> <dd>

<span data-ttu-id="95b3f-163">A conta sob a qual este serviço é executado é inválida ou não tem as permissões para executar o serviço.</span><span class="sxs-lookup"><span data-stu-id="95b3f-163">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="95b3f-164">**23**</span><span class="sxs-lookup"><span data-stu-id="95b3f-164">**23**</span></span>
</dt> <dd>

<span data-ttu-id="95b3f-165">O serviço existe no banco de dados de serviços disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="95b3f-165">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="95b3f-166">**24**</span><span class="sxs-lookup"><span data-stu-id="95b3f-166">**24**</span></span>
</dt> <dd>

<span data-ttu-id="95b3f-167">O serviço está pausado atualmente no sistema.</span><span class="sxs-lookup"><span data-stu-id="95b3f-167">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="95b3f-168">**Outras**</span><span class="sxs-lookup"><span data-stu-id="95b3f-168">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="95b3f-169">22 4294967295</span><span class="sxs-lookup"><span data-stu-id="95b3f-169">22 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="95b3f-170">Comentários</span><span class="sxs-lookup"><span data-stu-id="95b3f-170">Remarks</span></span>

<span data-ttu-id="95b3f-171">A instância do [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa um tipo de dados de [**\_ \_ controle do descritor de segurança**](/windows/desktop/SecAuthZ/security-descriptor-control) e contém uma DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) e uma SACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/s-gly) ) do sistema.</span><span class="sxs-lookup"><span data-stu-id="95b3f-171">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="95b3f-172">Para obter mais informações, consulte [listas de controle de acesso](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="95b3f-172">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="95b3f-173">Se **SeSecurityPrivilege** não for concedido ou habilitado ao obter um descritor de segurança, somente a DACL será retornada no descritor de segurança retornado.</span><span class="sxs-lookup"><span data-stu-id="95b3f-173">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="95b3f-174">Para obter mais informações, consulte [**constantes de privilégio**](/windows/desktop/WmiSdk/privilege-constants) e [executando operações privilegiadas](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="95b3f-174">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

<span data-ttu-id="95b3f-175">Você pode atualizar a DACL e a SACL na instância [**\_ SecurityDescriptor do Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) ao chamar esse método, mas também pode atualizar apenas a DACL ou apenas a SACL.</span><span class="sxs-lookup"><span data-stu-id="95b3f-175">You can update both the DACL and the SACL in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance when calling this method, but you also can update only the DACL or only the SACL.</span></span>

<span data-ttu-id="95b3f-176">Os valores a seguir [**no \_ \_ controle do descritor de segurança**](/windows/desktop/SecAuthZ/security-descriptor-control) determinam se a DACL, a SACL ou ambas são atualizadas.</span><span class="sxs-lookup"><span data-stu-id="95b3f-176">The following values in [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determine whether the DACL, the SACL, or both are updated.</span></span>

-   <span data-ttu-id="95b3f-177">**\_DACL \_ presente**</span><span class="sxs-lookup"><span data-stu-id="95b3f-177">**SE\_DACL\_PRESENT**</span></span>

    <span data-ttu-id="95b3f-178">Indica que a DACL deve ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="95b3f-178">Indicates that the DACL should be updated.</span></span> <span data-ttu-id="95b3f-179">Se isso não for definido, o WMI preservará o valor original da DACL.</span><span class="sxs-lookup"><span data-stu-id="95b3f-179">If this is not set, then WMI preserves the original value of the DACL.</span></span>

-   <span data-ttu-id="95b3f-180">**\_SACL \_ presente**</span><span class="sxs-lookup"><span data-stu-id="95b3f-180">**SE\_SACL\_PRESENT**</span></span>

    <span data-ttu-id="95b3f-181">Indica que a SACL deve ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="95b3f-181">Indicates that the SACL should be updated.</span></span> <span data-ttu-id="95b3f-182">Se isso não for definido, o WMI preservará o valor original da SACL.</span><span class="sxs-lookup"><span data-stu-id="95b3f-182">If this is not set, then WMI preserves the original value of the SACL.</span></span> <span data-ttu-id="95b3f-183">Para atualizar a SACL, a conta deve ter o privilégio **SeSecurityPrivilege** habilitado.</span><span class="sxs-lookup"><span data-stu-id="95b3f-183">To update the SACL, the account must have the **SeSecurityPrivilege** privilege enabled.</span></span> <span data-ttu-id="95b3f-184">Para scripts, o nome do privilégio é **SeSecurityPrivilege**.</span><span class="sxs-lookup"><span data-stu-id="95b3f-184">For scripting, the privilege name is **SeSecurityPrivilege**.</span></span> <span data-ttu-id="95b3f-185">Para obter mais informações, consulte [**constantes de privilégio**](/windows/desktop/WmiSdk/privilege-constants).</span><span class="sxs-lookup"><span data-stu-id="95b3f-185">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants).</span></span>

<span data-ttu-id="95b3f-186">Se o grupo de confiança e as propriedades de confiança do proprietário não forem **nulas**, eles serão atualizados.</span><span class="sxs-lookup"><span data-stu-id="95b3f-186">If the Group trustee and the Owner trustee properties are not **NULL**, then they are updated.</span></span> <span data-ttu-id="95b3f-187">Caso contrário, o WMI preservará os valores originais.</span><span class="sxs-lookup"><span data-stu-id="95b3f-187">Otherwise, WMI preserves the original values.</span></span> <span data-ttu-id="95b3f-188">Para obter mais informações, consulte [objetos do descritor de segurança do WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span><span class="sxs-lookup"><span data-stu-id="95b3f-188">For more information, see [WMI Security Descriptor Objects](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span></span>

<span data-ttu-id="95b3f-189">Quando uma nova SACL é **nula** em uma chamada desse método, a SACL do descritor de segurança no objeto protegível de destino permanece inalterada.</span><span class="sxs-lookup"><span data-stu-id="95b3f-189">When a new SACL is **NULL** in a call this method, then the security descriptor SACL on the target securable object is left unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="95b3f-190">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95b3f-190">Requirements</span></span>



| <span data-ttu-id="95b3f-191">Requisito</span><span class="sxs-lookup"><span data-stu-id="95b3f-191">Requirement</span></span> | <span data-ttu-id="95b3f-192">Valor</span><span class="sxs-lookup"><span data-stu-id="95b3f-192">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95b3f-193">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95b3f-193">Minimum supported client</span></span><br/> | <span data-ttu-id="95b3f-194">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="95b3f-194">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="95b3f-195">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95b3f-195">Minimum supported server</span></span><br/> | <span data-ttu-id="95b3f-196">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="95b3f-196">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="95b3f-197">Namespace</span><span class="sxs-lookup"><span data-stu-id="95b3f-197">Namespace</span></span><br/>                | <span data-ttu-id="95b3f-198">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="95b3f-198">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="95b3f-199">MOF</span><span class="sxs-lookup"><span data-stu-id="95b3f-199">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95b3f-200"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="95b3f-200"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="95b3f-201">DLL</span><span class="sxs-lookup"><span data-stu-id="95b3f-201">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95b3f-202"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95b3f-202"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95b3f-203">Confira também</span><span class="sxs-lookup"><span data-stu-id="95b3f-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95b3f-204">**\_Serviço Win32**</span><span class="sxs-lookup"><span data-stu-id="95b3f-204">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="95b3f-205">**Constantes de privilégio**</span><span class="sxs-lookup"><span data-stu-id="95b3f-205">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="95b3f-206">Objetos do descritor de segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="95b3f-206">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="95b3f-207">Alterando a segurança de acesso em objetos protegíveis</span><span class="sxs-lookup"><span data-stu-id="95b3f-207">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[<span data-ttu-id="95b3f-208">Controle de conta de usuário e WMI</span><span class="sxs-lookup"><span data-stu-id="95b3f-208">User Account Control and WMI</span></span>](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 


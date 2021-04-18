---
title: Método ChangeStartMode da classe Win32_Service (Serviços de Área de Trabalho Remota)
description: Modifica o modo de início de um \_ TerminalService Win32.
ms.assetid: 4F4B8CFC-B38C-47C6-A2BA-D498EC2B7F55
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ChangeStartMode
- Método ChangeStartMode Serviços de Área de Trabalho Remota, classe Win32_Service
- Classe Win32_Service Serviços de Área de Trabalho Remota, método ChangeStartMode
topic_type:
- apiref
api_name:
- Win32_Service.ChangeStartMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a46c6b72fbb070dac32b2b6990a217068c77da9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105792594"
---
# <a name="changestartmode-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="31bc8-106">Método ChangeStartMode da classe Win32_Service (Serviços de Área de Trabalho Remota)</span><span class="sxs-lookup"><span data-stu-id="31bc8-106">ChangeStartMode method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="31bc8-107">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeStartMode** modifica o modo de início de [**um \_ TerminalService Win32**](win32-terminalservice.md).</span><span class="sxs-lookup"><span data-stu-id="31bc8-107">The **ChangeStartMode** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies the start mode of a [**Win32\_TerminalService**](win32-terminalservice.md).</span></span>

<span data-ttu-id="31bc8-108">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="31bc8-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="31bc8-109">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="31bc8-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="31bc8-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31bc8-110">Syntax</span></span>


```mof
uint32 ChangeStartMode(
  [in] string StartMode
);
```



## <a name="parameters"></a><span data-ttu-id="31bc8-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31bc8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31bc8-112">*StartMode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="31bc8-112">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31bc8-113">Modo de início do serviço base do Windows.</span><span class="sxs-lookup"><span data-stu-id="31bc8-113">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="31bc8-114"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Inicialização**</span><span class="sxs-lookup"><span data-stu-id="31bc8-114"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot**</span></span>


</dt> <dd>

<span data-ttu-id="31bc8-115">Driver de dispositivo iniciado pelo carregador do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="31bc8-115">Device driver started by the operating system loader.</span></span> <span data-ttu-id="31bc8-116">Esse valor só é válido para serviços do driver.</span><span class="sxs-lookup"><span data-stu-id="31bc8-116">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="31bc8-117"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema**</span><span class="sxs-lookup"><span data-stu-id="31bc8-117"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System**</span></span>


</dt> <dd>

<span data-ttu-id="31bc8-118">Driver de dispositivo iniciado pelo processo de inicialização do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="31bc8-118">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="31bc8-119">Esse valor só é válido para serviços do driver.</span><span class="sxs-lookup"><span data-stu-id="31bc8-119">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="31bc8-120"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automático**</span><span class="sxs-lookup"><span data-stu-id="31bc8-120"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic**</span></span>


</dt> <dd>

<span data-ttu-id="31bc8-121">Serviço a ser iniciado automaticamente pelo Gerenciador de controle de serviço durante a inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="31bc8-121">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="31bc8-122"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual**</span><span class="sxs-lookup"><span data-stu-id="31bc8-122"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual**</span></span>


</dt> <dd>

<span data-ttu-id="31bc8-123">Serviço a ser iniciado pelo Gerenciador de controle de serviço quando um processo chama o método [**StartService**](win32-terminalservice-startservice.md) .</span><span class="sxs-lookup"><span data-stu-id="31bc8-123">Service to be started by the Service Control Manager when a process calls the [**StartService**](win32-terminalservice-startservice.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="31bc8-124"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado**</span><span class="sxs-lookup"><span data-stu-id="31bc8-124"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled**</span></span>


</dt> <dd>

<span data-ttu-id="31bc8-125">Serviço que não pode mais ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="31bc8-125">Service that can no longer be started.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31bc8-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="31bc8-126">Return value</span></span>

<span data-ttu-id="31bc8-127">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="31bc8-127">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="31bc8-128">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="31bc8-128">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="31bc8-129">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="31bc8-129">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="31bc8-130">**0**</span><span class="sxs-lookup"><span data-stu-id="31bc8-130">**0**</span></span>
</dt> <dd>

<span data-ttu-id="31bc8-131">A solicitação foi aceita.</span><span class="sxs-lookup"><span data-stu-id="31bc8-131">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="31bc8-132">**1**</span><span class="sxs-lookup"><span data-stu-id="31bc8-132">**1**</span></span>
</dt> <dd>

<span data-ttu-id="31bc8-133">A solicitação não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="31bc8-133">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="31bc8-134">**2**</span><span class="sxs-lookup"><span data-stu-id="31bc8-134">**2**</span></span>
</dt> <dd>

<span data-ttu-id="31bc8-135">O usuário não tinha o acesso necessário.</span><span class="sxs-lookup"><span data-stu-id="31bc8-135">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="31bc8-136">**3**</span><span class="sxs-lookup"><span data-stu-id="31bc8-136">**3**</span></span>
</dt> <dd>

<span data-ttu-id="31bc8-137">O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.</span><span class="sxs-lookup"><span data-stu-id="31bc8-137">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="31bc8-138">**4**</span><span class="sxs-lookup"><span data-stu-id="31bc8-138">**4**</span></span>
</dt> <dd>

<span data-ttu-id="31bc8-139">O código de controle pedido não é válido ou é inaceitável para o serviço.</span><span class="sxs-lookup"><span data-stu-id="31bc8-139">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="31bc8-140">**5**</span><span class="sxs-lookup"><span data-stu-id="31bc8-140">**5**</span></span>
</dt> <dd>

<span data-ttu-id="31bc8-141">O código de controle solicitado não pode ser enviado ao serviço porque o estado do serviço ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).\*\*\*\* A propriedade State) é igual a 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="31bc8-141">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="31bc8-142">**6**</span><span class="sxs-lookup"><span data-stu-id="31bc8-142">**6**</span></span>
</dt> <dd>

<span data-ttu-id="31bc8-143">O serviço não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="31bc8-143">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="31bc8-144">**7**</span><span class="sxs-lookup"><span data-stu-id="31bc8-144">**7**</span></span>
</dt> <dd>

<span data-ttu-id="31bc8-145">O serviço não respondeu à solicitação de início em um tempo oportuno.</span><span class="sxs-lookup"><span data-stu-id="31bc8-145">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="31bc8-146">**8**</span><span class="sxs-lookup"><span data-stu-id="31bc8-146">**8**</span></span>
</dt> <dd>

<span data-ttu-id="31bc8-147">Falha desconhecida ao iniciar o serviço.</span><span class="sxs-lookup"><span data-stu-id="31bc8-147">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="31bc8-148">**9**</span><span class="sxs-lookup"><span data-stu-id="31bc8-148">**9**</span></span>
</dt> <dd>

<span data-ttu-id="31bc8-149">O caminho do diretório para o arquivo executável do serviço não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="31bc8-149">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="31bc8-150">**10**</span><span class="sxs-lookup"><span data-stu-id="31bc8-150">**10**</span></span>
</dt> <dd>

<span data-ttu-id="31bc8-151">O serviço já está em execução.</span><span class="sxs-lookup"><span data-stu-id="31bc8-151">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="31bc8-152">**11**</span><span class="sxs-lookup"><span data-stu-id="31bc8-152">**11**</span></span>
</dt> <dd>

<span data-ttu-id="31bc8-153">O banco de dados para adicionar um serviço novo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="31bc8-153">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="31bc8-154">**12**</span><span class="sxs-lookup"><span data-stu-id="31bc8-154">**12**</span></span>
</dt> <dd>

<span data-ttu-id="31bc8-155">Uma dependência da qual esse serviço depende foi removida do sistema.</span><span class="sxs-lookup"><span data-stu-id="31bc8-155">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="31bc8-156">**13**</span><span class="sxs-lookup"><span data-stu-id="31bc8-156">**13**</span></span>
</dt> <dd>

<span data-ttu-id="31bc8-157">O serviço não localizou o serviço necessário em um serviço dependente.</span><span class="sxs-lookup"><span data-stu-id="31bc8-157">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="31bc8-158">**14**</span><span class="sxs-lookup"><span data-stu-id="31bc8-158">**14**</span></span>
</dt> <dd>

<span data-ttu-id="31bc8-159">O serviço foi desabilitado do sistema.</span><span class="sxs-lookup"><span data-stu-id="31bc8-159">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="31bc8-160">**15**</span><span class="sxs-lookup"><span data-stu-id="31bc8-160">**15**</span></span>
</dt> <dd>

<span data-ttu-id="31bc8-161">O serviço não tem a autenticação correta para ser executado no sistema.</span><span class="sxs-lookup"><span data-stu-id="31bc8-161">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="31bc8-162">**16**</span><span class="sxs-lookup"><span data-stu-id="31bc8-162">**16**</span></span>
</dt> <dd>

<span data-ttu-id="31bc8-163">Este serviço está sendo removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="31bc8-163">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="31bc8-164">**17**</span><span class="sxs-lookup"><span data-stu-id="31bc8-164">**17**</span></span>
</dt> <dd>

<span data-ttu-id="31bc8-165">O serviço não tem nenhum thread de execução.</span><span class="sxs-lookup"><span data-stu-id="31bc8-165">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="31bc8-166">**anos**</span><span class="sxs-lookup"><span data-stu-id="31bc8-166">**18**</span></span>
</dt> <dd>

<span data-ttu-id="31bc8-167">O serviço tem dependências circulares quando é iniciado.</span><span class="sxs-lookup"><span data-stu-id="31bc8-167">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="31bc8-168">**aprimora**</span><span class="sxs-lookup"><span data-stu-id="31bc8-168">**19**</span></span>
</dt> <dd>

<span data-ttu-id="31bc8-169">Um serviço está sendo executado com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="31bc8-169">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="31bc8-170">**20**</span><span class="sxs-lookup"><span data-stu-id="31bc8-170">**20**</span></span>
</dt> <dd>

<span data-ttu-id="31bc8-171">O nome do serviço tem caracteres inválidos.</span><span class="sxs-lookup"><span data-stu-id="31bc8-171">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="31bc8-172">**Abril**</span><span class="sxs-lookup"><span data-stu-id="31bc8-172">**21**</span></span>
</dt> <dd>

<span data-ttu-id="31bc8-173">Parâmetros inválidos foram passados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="31bc8-173">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="31bc8-174">**22**</span><span class="sxs-lookup"><span data-stu-id="31bc8-174">**22**</span></span>
</dt> <dd>

<span data-ttu-id="31bc8-175">A conta sob a qual este serviço é executado é inválida ou não tem as permissões para executar o serviço.</span><span class="sxs-lookup"><span data-stu-id="31bc8-175">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="31bc8-176">**23**</span><span class="sxs-lookup"><span data-stu-id="31bc8-176">**23**</span></span>
</dt> <dd>

<span data-ttu-id="31bc8-177">O serviço existe no banco de dados de serviços disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="31bc8-177">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="31bc8-178">**24**</span><span class="sxs-lookup"><span data-stu-id="31bc8-178">**24**</span></span>
</dt> <dd>

<span data-ttu-id="31bc8-179">O serviço está pausado atualmente no sistema.</span><span class="sxs-lookup"><span data-stu-id="31bc8-179">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="31bc8-180">Exemplos</span><span class="sxs-lookup"><span data-stu-id="31bc8-180">Examples</span></span>

<span data-ttu-id="31bc8-181">A seguinte [alteração de StartMode de um exemplo do](https://Gallery.TechNet.Microsoft.Com/6d0f06ed-f840-4228-ad2d-e16ebe6a3aed) PowerShell de serviço, extraído da galeria do TechNet, altera o modo de início de um serviço.</span><span class="sxs-lookup"><span data-stu-id="31bc8-181">The following [Change StartMode of a Service](https://Gallery.TechNet.Microsoft.Com/6d0f06ed-f840-4228-ad2d-e16ebe6a3aed) PowerShell sample, pulled from TechNet Gallery, changes the start mode of a service.</span></span>


```PowerShell
$wmi = get-wmiobject -class win32_service -namespace root\cimv2 -computername lisbon | 
where-object { $_.name -eq 'bits' } 
 
$rtn = $wmi.changestartmode("manual") 
if($rtn.returnvalue -eq 0) { "success" } 
ELSE 
  { " $($rtn.returnvalue) was reported" }
```



## <a name="requirements"></a><span data-ttu-id="31bc8-182">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31bc8-182">Requirements</span></span>



| <span data-ttu-id="31bc8-183">Requisito</span><span class="sxs-lookup"><span data-stu-id="31bc8-183">Requirement</span></span> | <span data-ttu-id="31bc8-184">Valor</span><span class="sxs-lookup"><span data-stu-id="31bc8-184">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31bc8-185">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31bc8-185">Minimum supported client</span></span><br/> | <span data-ttu-id="31bc8-186">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31bc8-186">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="31bc8-187">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31bc8-187">Minimum supported server</span></span><br/> | <span data-ttu-id="31bc8-188">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31bc8-188">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="31bc8-189">Namespace</span><span class="sxs-lookup"><span data-stu-id="31bc8-189">Namespace</span></span><br/>                | <span data-ttu-id="31bc8-190">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="31bc8-190">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="31bc8-191">MOF</span><span class="sxs-lookup"><span data-stu-id="31bc8-191">MOF</span></span><br/>                      | <dl> <span data-ttu-id="31bc8-192"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="31bc8-192"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="31bc8-193">DLL</span><span class="sxs-lookup"><span data-stu-id="31bc8-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31bc8-194"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31bc8-194"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31bc8-195">Confira também</span><span class="sxs-lookup"><span data-stu-id="31bc8-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31bc8-196">**\_Serviço Win32**</span><span class="sxs-lookup"><span data-stu-id="31bc8-196">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="31bc8-197">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="31bc8-197">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="31bc8-198">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="31bc8-198">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="31bc8-199">Tarefas do WMI: serviços</span><span class="sxs-lookup"><span data-stu-id="31bc8-199">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 


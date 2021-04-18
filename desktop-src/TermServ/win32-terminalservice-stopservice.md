---
title: Método StopService da classe Win32_Service (Sdoias. h) (serviço de terminal)
description: Coloca o serviço, representado pelo \_ objeto TerminalService do Win32, no estado parado.
ms.assetid: 228711DC-369B-48B6-96EE-DF4026904E26
ms.tgt_platform: multiple
keywords:
- Método StopService Serviços de Área de Trabalho Remota
- Método StopService Serviços de Área de Trabalho Remota, classe Win32_Service
- Classe Win32_Service Serviços de Área de Trabalho Remota, método StopService
topic_type:
- apiref
api_name:
- Win32_Service.StopService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e1b21db330bb9111b96fb244200845cb83b3153
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/26/2021
ms.locfileid: "105778802"
---
# <a name="stopservice-method-of-the-win32_service-class-sdoiash-for-the-terminal-service"></a><span data-ttu-id="9ebe2-106">Método StopService da classe de Win32_Service (Sdoias. h) para o serviço de terminal</span><span class="sxs-lookup"><span data-stu-id="9ebe2-106">StopService method of the Win32_Service class (Sdoias.h) for the Terminal service</span></span>

<span data-ttu-id="9ebe2-107">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **StopService** coloca o serviço, representado pelo [**objeto \_ TerminalService do Win32**](win32-terminalservice.md) , no estado parado.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-107">The **StopService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method places the service, represented by the [**Win32\_TerminalService**](win32-terminalservice.md) object, in the stopped state.</span></span>

<span data-ttu-id="9ebe2-108">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="9ebe2-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9ebe2-109">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="9ebe2-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9ebe2-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9ebe2-110">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="9ebe2-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9ebe2-111">Parameters</span></span>

<span data-ttu-id="9ebe2-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9ebe2-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9ebe2-113">Return value</span></span>

<span data-ttu-id="9ebe2-114">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-114">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="9ebe2-115">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="9ebe2-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="9ebe2-116">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="9ebe2-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="9ebe2-117">**0**</span><span class="sxs-lookup"><span data-stu-id="9ebe2-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="9ebe2-118">A solicitação foi aceita.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="9ebe2-119">**1**</span><span class="sxs-lookup"><span data-stu-id="9ebe2-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="9ebe2-120">A solicitação não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="9ebe2-121">**2**</span><span class="sxs-lookup"><span data-stu-id="9ebe2-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="9ebe2-122">O usuário não tinha o acesso necessário.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="9ebe2-123">**3**</span><span class="sxs-lookup"><span data-stu-id="9ebe2-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="9ebe2-124">O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="9ebe2-125">**4**</span><span class="sxs-lookup"><span data-stu-id="9ebe2-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="9ebe2-126">O código de controle pedido não é válido ou é inaceitável para o serviço.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="9ebe2-127">**5**</span><span class="sxs-lookup"><span data-stu-id="9ebe2-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="9ebe2-128">O código de controle solicitado não pode ser enviado ao serviço porque o estado do serviço ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).\*\*\*\* A propriedade State) é igual a 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="9ebe2-129">**6**</span><span class="sxs-lookup"><span data-stu-id="9ebe2-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="9ebe2-130">O serviço não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="9ebe2-131">**7**</span><span class="sxs-lookup"><span data-stu-id="9ebe2-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="9ebe2-132">O serviço não respondeu à solicitação de início em um tempo oportuno.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="9ebe2-133">**8**</span><span class="sxs-lookup"><span data-stu-id="9ebe2-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="9ebe2-134">Falha desconhecida ao iniciar o serviço.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="9ebe2-135">**9**</span><span class="sxs-lookup"><span data-stu-id="9ebe2-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="9ebe2-136">O caminho do diretório para o arquivo executável do serviço não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="9ebe2-137">**10**</span><span class="sxs-lookup"><span data-stu-id="9ebe2-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="9ebe2-138">O serviço já está em execução.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="9ebe2-139">**11**</span><span class="sxs-lookup"><span data-stu-id="9ebe2-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="9ebe2-140">O banco de dados para adicionar um serviço novo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="9ebe2-141">**12**</span><span class="sxs-lookup"><span data-stu-id="9ebe2-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="9ebe2-142">Uma dependência da qual esse serviço depende foi removida do sistema.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="9ebe2-143">**13**</span><span class="sxs-lookup"><span data-stu-id="9ebe2-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="9ebe2-144">O serviço não localizou o serviço necessário em um serviço dependente.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="9ebe2-145">**14**</span><span class="sxs-lookup"><span data-stu-id="9ebe2-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="9ebe2-146">O serviço foi desabilitado do sistema.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="9ebe2-147">**15**</span><span class="sxs-lookup"><span data-stu-id="9ebe2-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="9ebe2-148">O serviço não tem a autenticação correta para ser executado no sistema.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="9ebe2-149">**16**</span><span class="sxs-lookup"><span data-stu-id="9ebe2-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="9ebe2-150">Este serviço está sendo removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="9ebe2-151">**17**</span><span class="sxs-lookup"><span data-stu-id="9ebe2-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="9ebe2-152">O serviço não tem nenhum thread de execução.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="9ebe2-153">**anos**</span><span class="sxs-lookup"><span data-stu-id="9ebe2-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="9ebe2-154">O serviço tem dependências circulares quando é iniciado.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="9ebe2-155">**aprimora**</span><span class="sxs-lookup"><span data-stu-id="9ebe2-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="9ebe2-156">Um serviço está sendo executado com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="9ebe2-157">**20**</span><span class="sxs-lookup"><span data-stu-id="9ebe2-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="9ebe2-158">O nome do serviço tem caracteres inválidos.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="9ebe2-159">**Abril**</span><span class="sxs-lookup"><span data-stu-id="9ebe2-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="9ebe2-160">Parâmetros inválidos foram passados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="9ebe2-161">**22**</span><span class="sxs-lookup"><span data-stu-id="9ebe2-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="9ebe2-162">A conta sob a qual este serviço é executado é inválida ou não tem as permissões para executar o serviço.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="9ebe2-163">**23**</span><span class="sxs-lookup"><span data-stu-id="9ebe2-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="9ebe2-164">O serviço existe no banco de dados de serviços disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="9ebe2-165">**24**</span><span class="sxs-lookup"><span data-stu-id="9ebe2-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="9ebe2-166">O serviço está pausado atualmente no sistema.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ebe2-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="9ebe2-167">Remarks</span></span>

<span data-ttu-id="9ebe2-168">Depois de determinar quais serviços podem ser interrompidos ou pausados, você pode usar os métodos **StopService** e [**PauseService**](win32-terminalservice-pauseservice.md) para parar e pausar serviços.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-168">After you have determined which services can be stopped or paused, you can use the **StopService** and [**PauseService**](win32-terminalservice-pauseservice.md) methods to stop and pause services.</span></span> <span data-ttu-id="9ebe2-169">A decisão de interromper um serviço em vez de pausá-lo, ou vice-versa, depende de vários fatores, incluindo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="9ebe2-169">The decision to stop a service rather than pause it, or vice versa, depends on several factors, including the following:</span></span>

-   <span data-ttu-id="9ebe2-170">O serviço é capaz de ser pausado?</span><span class="sxs-lookup"><span data-stu-id="9ebe2-170">Is the service capable of being paused?</span></span> <span data-ttu-id="9ebe2-171">Caso contrário, sua única opção é parar o serviço.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-171">If not, your only option is the stop the service.</span></span>
-   <span data-ttu-id="9ebe2-172">Você precisa continuar tratando as solicitações do cliente para qualquer pessoa já conectada ao serviço?</span><span class="sxs-lookup"><span data-stu-id="9ebe2-172">Do you need to continue handling client requests for anyone already connected to the service?</span></span> <span data-ttu-id="9ebe2-173">Nesse caso, pausar um serviço geralmente permite que ele manipule clientes existentes enquanto nega acesso a novos clientes.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-173">If so, pausing a service typically allows it to handle existing clients while denying access to new clients.</span></span> <span data-ttu-id="9ebe2-174">Por outro lado, quando você interrompe um serviço, todos os clientes são imediatamente desconectados.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-174">By contrast, when you stop a service, all clients are immediately disconnected.</span></span>
-   <span data-ttu-id="9ebe2-175">Você precisa reconfigurar um serviço e fazer com que as alterações entrem em vigor imediatamente?</span><span class="sxs-lookup"><span data-stu-id="9ebe2-175">Do you need to reconfigure a service and have the changes take effect immediately?</span></span> <span data-ttu-id="9ebe2-176">Embora as propriedades do serviço possam ser alteradas enquanto um serviço é pausado, a maioria delas não tem efeito até que o serviço seja realmente interrompido e reiniciado.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-176">Although service properties can be changed while a service is paused, most of them do not take effect until the service is actually stopped and restarted.</span></span>

<span data-ttu-id="9ebe2-177">O código de script necessário para interromper um serviço é quase idêntico ao código necessário para pausar o serviço.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-177">The scripting code required to stop a service is almost identical to the code required to pause the service.</span></span>

<span data-ttu-id="9ebe2-178">Se você tentar interromper um serviço que tem serviços dependentes em execução, o método **StopService** falhará com um valor de retorno de 3.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-178">If you attempt to stop a service which has dependent services running, the **StopService** method fails with a return value of 3.</span></span> <span data-ttu-id="9ebe2-179">Os serviços dependentes devem ser interrompidos primeiro.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-179">The dependent services must be stopped first.</span></span>

<span data-ttu-id="9ebe2-180">Se você parar um serviço, verifique imediatamente o [**\_ TerminalService do Win32**](win32-terminalservice.md).\*\*\*\* A propriedade State, pois o valor ainda pode mostrar o serviço como em execução.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-180">If you stop a service, then immediately check the [**Win32\_TerminalService**](win32-terminalservice.md).**State** property, as the value may still show the service as running.</span></span>

## <a name="examples"></a><span data-ttu-id="9ebe2-181">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9ebe2-181">Examples</span></span>

<span data-ttu-id="9ebe2-182">[O set-RemoteService](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) O exemplo do PowerShell define o estado do serviço para máquinas remotas.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-182">[The Set-RemoteService](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) PowerShell sample Sets service state for remote machines.</span></span>

<span data-ttu-id="9ebe2-183">O exemplo de [parar um serviço e seus dependentes](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732) do VBScript interrompe um serviço e todos os serviços dependentes.</span><span class="sxs-lookup"><span data-stu-id="9ebe2-183">The [Stop a Service and Its Dependents](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732) VBScript sample stops a service and all dependent services.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ebe2-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ebe2-184">Requirements</span></span>



| <span data-ttu-id="9ebe2-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ebe2-185">Requirement</span></span> | <span data-ttu-id="9ebe2-186">Valor</span><span class="sxs-lookup"><span data-stu-id="9ebe2-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ebe2-187">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ebe2-187">Minimum supported client</span></span><br/> | <span data-ttu-id="9ebe2-188">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9ebe2-188">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9ebe2-189">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ebe2-189">Minimum supported server</span></span><br/> | <span data-ttu-id="9ebe2-190">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9ebe2-190">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9ebe2-191">Namespace</span><span class="sxs-lookup"><span data-stu-id="9ebe2-191">Namespace</span></span><br/>                | <span data-ttu-id="9ebe2-192">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="9ebe2-192">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="9ebe2-193">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9ebe2-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ebe2-194"><dt>Sdoias. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ebe2-194"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="9ebe2-195">MOF</span><span class="sxs-lookup"><span data-stu-id="9ebe2-195">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ebe2-196"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9ebe2-196"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="9ebe2-197">DLL</span><span class="sxs-lookup"><span data-stu-id="9ebe2-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ebe2-198"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ebe2-198"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ebe2-199">Confira também</span><span class="sxs-lookup"><span data-stu-id="9ebe2-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ebe2-200">**\_Serviço Win32**</span><span class="sxs-lookup"><span data-stu-id="9ebe2-200">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="9ebe2-201">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="9ebe2-201">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="9ebe2-202">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="9ebe2-202">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="9ebe2-203">Tarefas do WMI: serviços</span><span class="sxs-lookup"><span data-stu-id="9ebe2-203">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[<span data-ttu-id="9ebe2-204">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="9ebe2-204">**PauseService**</span></span>](/windows/desktop/CIMWin32Prov/pauseservice-method-in-class-win32-systemdriver)
</dt> </dl>

 


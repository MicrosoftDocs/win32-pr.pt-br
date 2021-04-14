---
title: Método ResumeService da classe Win32_Service (Serviços de Área de Trabalho Remota)
description: Tenta posicionar o serviço referenciado no estado retomado.
ms.assetid: AA020A0A-E69C-44AB-B259-A73460728770
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ResumeService
- Método ResumeService Serviços de Área de Trabalho Remota, classe Win32_Service
- Classe Win32_Service Serviços de Área de Trabalho Remota, método ResumeService
topic_type:
- apiref
api_name:
- Win32_Service.ResumeService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e7b446dea84e4320e9aa8972a88dc4fdd5a6eea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499722"
---
# <a name="resumeservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="f0d91-106">Método ResumeService da classe Win32_Service (Serviços de Área de Trabalho Remota)</span><span class="sxs-lookup"><span data-stu-id="f0d91-106">ResumeService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="f0d91-107">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ResumeService** tenta posicionar o serviço referenciado no estado retomado.</span><span class="sxs-lookup"><span data-stu-id="f0d91-107">The **ResumeService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the referenced service in the resumed state.</span></span>

<span data-ttu-id="f0d91-108">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="f0d91-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f0d91-109">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f0d91-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f0d91-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f0d91-110">Syntax</span></span>


```mof
uint32 ResumeService();
```



## <a name="parameters"></a><span data-ttu-id="f0d91-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0d91-111">Parameters</span></span>

<span data-ttu-id="f0d91-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f0d91-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f0d91-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f0d91-113">Return value</span></span>

<span data-ttu-id="f0d91-114">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="f0d91-114">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="f0d91-115">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="f0d91-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="f0d91-116">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="f0d91-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="f0d91-117">**0**</span><span class="sxs-lookup"><span data-stu-id="f0d91-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="f0d91-118">A solicitação foi aceita.</span><span class="sxs-lookup"><span data-stu-id="f0d91-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="f0d91-119">**1**</span><span class="sxs-lookup"><span data-stu-id="f0d91-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="f0d91-120">A solicitação não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="f0d91-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="f0d91-121">**2**</span><span class="sxs-lookup"><span data-stu-id="f0d91-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="f0d91-122">O usuário não tinha o acesso necessário.</span><span class="sxs-lookup"><span data-stu-id="f0d91-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="f0d91-123">**3**</span><span class="sxs-lookup"><span data-stu-id="f0d91-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="f0d91-124">O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.</span><span class="sxs-lookup"><span data-stu-id="f0d91-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="f0d91-125">**4**</span><span class="sxs-lookup"><span data-stu-id="f0d91-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="f0d91-126">O código de controle pedido não é válido ou é inaceitável para o serviço.</span><span class="sxs-lookup"><span data-stu-id="f0d91-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="f0d91-127">**5**</span><span class="sxs-lookup"><span data-stu-id="f0d91-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="f0d91-128">O código de controle solicitado não pode ser enviado ao serviço porque o estado do serviço ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).\*\*\*\* A propriedade State) é igual a 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="f0d91-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="f0d91-129">**6**</span><span class="sxs-lookup"><span data-stu-id="f0d91-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="f0d91-130">O serviço não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="f0d91-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="f0d91-131">**7**</span><span class="sxs-lookup"><span data-stu-id="f0d91-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="f0d91-132">O serviço não respondeu à solicitação de início em um tempo oportuno.</span><span class="sxs-lookup"><span data-stu-id="f0d91-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="f0d91-133">**8**</span><span class="sxs-lookup"><span data-stu-id="f0d91-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="f0d91-134">Falha desconhecida ao iniciar o serviço.</span><span class="sxs-lookup"><span data-stu-id="f0d91-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="f0d91-135">**9**</span><span class="sxs-lookup"><span data-stu-id="f0d91-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="f0d91-136">O caminho do diretório para o arquivo executável do serviço não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="f0d91-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="f0d91-137">**10**</span><span class="sxs-lookup"><span data-stu-id="f0d91-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="f0d91-138">O serviço já está em execução.</span><span class="sxs-lookup"><span data-stu-id="f0d91-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="f0d91-139">**11**</span><span class="sxs-lookup"><span data-stu-id="f0d91-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="f0d91-140">O banco de dados para adicionar um serviço novo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="f0d91-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="f0d91-141">**12**</span><span class="sxs-lookup"><span data-stu-id="f0d91-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="f0d91-142">Uma dependência da qual esse serviço depende foi removida do sistema.</span><span class="sxs-lookup"><span data-stu-id="f0d91-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="f0d91-143">**13**</span><span class="sxs-lookup"><span data-stu-id="f0d91-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="f0d91-144">O serviço não localizou o serviço necessário em um serviço dependente.</span><span class="sxs-lookup"><span data-stu-id="f0d91-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="f0d91-145">**14**</span><span class="sxs-lookup"><span data-stu-id="f0d91-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="f0d91-146">O serviço foi desabilitado do sistema.</span><span class="sxs-lookup"><span data-stu-id="f0d91-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="f0d91-147">**15**</span><span class="sxs-lookup"><span data-stu-id="f0d91-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="f0d91-148">O serviço não tem a autenticação correta para ser executado no sistema.</span><span class="sxs-lookup"><span data-stu-id="f0d91-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="f0d91-149">**16**</span><span class="sxs-lookup"><span data-stu-id="f0d91-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="f0d91-150">Este serviço está sendo removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="f0d91-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="f0d91-151">**17**</span><span class="sxs-lookup"><span data-stu-id="f0d91-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="f0d91-152">O serviço não tem nenhum thread de execução.</span><span class="sxs-lookup"><span data-stu-id="f0d91-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="f0d91-153">**anos**</span><span class="sxs-lookup"><span data-stu-id="f0d91-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="f0d91-154">O serviço tem dependências circulares quando é iniciado.</span><span class="sxs-lookup"><span data-stu-id="f0d91-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="f0d91-155">**aprimora**</span><span class="sxs-lookup"><span data-stu-id="f0d91-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="f0d91-156">Um serviço está sendo executado com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="f0d91-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="f0d91-157">**20**</span><span class="sxs-lookup"><span data-stu-id="f0d91-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="f0d91-158">O nome do serviço tem caracteres inválidos.</span><span class="sxs-lookup"><span data-stu-id="f0d91-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="f0d91-159">**Abril**</span><span class="sxs-lookup"><span data-stu-id="f0d91-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="f0d91-160">Parâmetros inválidos foram passados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="f0d91-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="f0d91-161">**22**</span><span class="sxs-lookup"><span data-stu-id="f0d91-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="f0d91-162">A conta sob a qual este serviço é executado é inválida ou não tem as permissões para executar o serviço.</span><span class="sxs-lookup"><span data-stu-id="f0d91-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="f0d91-163">**23**</span><span class="sxs-lookup"><span data-stu-id="f0d91-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="f0d91-164">O serviço existe no banco de dados de serviços disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="f0d91-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="f0d91-165">**24**</span><span class="sxs-lookup"><span data-stu-id="f0d91-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="f0d91-166">O serviço está pausado atualmente no sistema.</span><span class="sxs-lookup"><span data-stu-id="f0d91-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f0d91-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0d91-167">Remarks</span></span>

<span data-ttu-id="f0d91-168">Embora possa parecer não ser uma diferença prática entre um serviço que é interrompido e um serviço em pausa, os dois Estados aparecem de forma diferente para o SCM.</span><span class="sxs-lookup"><span data-stu-id="f0d91-168">Although there might appear to be no practical difference between a service that is stopped and a service that is paused, the two states appear differently to the SCM.</span></span> <span data-ttu-id="f0d91-169">Um serviço parado é um serviço que não está em execução e deve passar pelo procedimento de início do serviço inteiro.</span><span class="sxs-lookup"><span data-stu-id="f0d91-169">A stopped service is a service that is not running and must go through the entire service start procedure.</span></span> <span data-ttu-id="f0d91-170">Um serviço em pausa, no entanto, ainda está em execução, mas teve seu funcionamento suspenso.</span><span class="sxs-lookup"><span data-stu-id="f0d91-170">A paused service, however, is still running but has had its functioning is suspended.</span></span> <span data-ttu-id="f0d91-171">Por isso, um serviço em pausa não precisa passar pelo procedimento de início do serviço inteiro, mas precisa de um procedimento diferente para retomar o funcionamento.</span><span class="sxs-lookup"><span data-stu-id="f0d91-171">Because of this, a paused service does not need to go through the entire service start procedure but needs a different procedure to resume functioning.</span></span>

<span data-ttu-id="f0d91-172">Você deve usar o método apropriado para iniciar um serviço que foi interrompido ou para retomar um serviço que tenha sido pausado.</span><span class="sxs-lookup"><span data-stu-id="f0d91-172">You must use the proper method to start a service that has been stopped or to resume a service that has been paused.</span></span> <span data-ttu-id="f0d91-173">Os métodos de [**\_ serviço do Win32**](/windows/desktop/CIMWin32Prov/win32-service) [**StartService**](win32-terminalservice-startservice.md) e **ResumeService** devem ser usados nas seguintes situações:</span><span class="sxs-lookup"><span data-stu-id="f0d91-173">The [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) methods [**StartService**](win32-terminalservice-startservice.md) and **ResumeService** should be used in the following situations:</span></span>

-   <span data-ttu-id="f0d91-174">Se um serviço estiver parado no momento, você deverá usar o método [**StartService**](win32-terminalservice-startservice.md) para reiniciá-lo; **ResumeService** não pode iniciar um serviço que está parado no momento.</span><span class="sxs-lookup"><span data-stu-id="f0d91-174">If a service is currently stopped, you must use the [**StartService**](win32-terminalservice-startservice.md) method to restart it; **ResumeService** cannot start a service that is currently stopped.</span></span>
-   <span data-ttu-id="f0d91-175">Se um serviço estiver em pausa, você deverá usar **ResumeService**.</span><span class="sxs-lookup"><span data-stu-id="f0d91-175">If a service is paused, you must use **ResumeService**.</span></span> <span data-ttu-id="f0d91-176">Se você usar o método [**StartService**](win32-terminalservice-startservice.md) em um serviço em pausa, receberá a mensagem "o serviço já está em execução".</span><span class="sxs-lookup"><span data-stu-id="f0d91-176">If you use the [**StartService**](win32-terminalservice-startservice.md) method on a paused service, you receive the message, "The service is already running."</span></span> <span data-ttu-id="f0d91-177">No entanto, o serviço permanece em pausa até que o código de controle retome o serviço seja enviado a ele.</span><span class="sxs-lookup"><span data-stu-id="f0d91-177">However, the service remains paused until the resume service control code is sent to it.</span></span>

## <a name="examples"></a><span data-ttu-id="f0d91-178">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f0d91-178">Examples</span></span>

<span data-ttu-id="f0d91-179">O exemplo de [retomar os serviços AutoStart que estão em pausa](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) do VBScript reinicia todos os serviços de início automático que foram pausados.</span><span class="sxs-lookup"><span data-stu-id="f0d91-179">The [Resume AutoStart Services that are Paused](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) VBScript sample restarts any auto-start services that have been paused.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0d91-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0d91-180">Requirements</span></span>



| <span data-ttu-id="f0d91-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0d91-181">Requirement</span></span> | <span data-ttu-id="f0d91-182">Valor</span><span class="sxs-lookup"><span data-stu-id="f0d91-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0d91-183">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0d91-183">Minimum supported client</span></span><br/> | <span data-ttu-id="f0d91-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f0d91-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f0d91-185">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0d91-185">Minimum supported server</span></span><br/> | <span data-ttu-id="f0d91-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f0d91-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f0d91-187">Namespace</span><span class="sxs-lookup"><span data-stu-id="f0d91-187">Namespace</span></span><br/>                | <span data-ttu-id="f0d91-188">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="f0d91-188">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f0d91-189">MOF</span><span class="sxs-lookup"><span data-stu-id="f0d91-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0d91-190"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f0d91-190"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f0d91-191">DLL</span><span class="sxs-lookup"><span data-stu-id="f0d91-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0d91-192"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0d91-192"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0d91-193">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0d91-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0d91-194">**\_Serviço Win32**</span><span class="sxs-lookup"><span data-stu-id="f0d91-194">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="f0d91-195">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="f0d91-195">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="f0d91-196">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="f0d91-196">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="f0d91-197">Tarefas do WMI: serviços</span><span class="sxs-lookup"><span data-stu-id="f0d91-197">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 


---
title: Método StartService da classe Win32_Service (Serviços de Área de Trabalho Remota)
description: Método StartService da classe Win32_Service (Serviços de Área de Trabalho Remota) – tenta posicionar o serviço referenciado em seu estado de inicialização.
ms.assetid: 4DA05C48-03A0-4D4B-9E69-0404393C219C
ms.tgt_platform: multiple
keywords:
- Método StartService Serviços de Área de Trabalho Remota
- Método StartService Serviços de Área de Trabalho Remota, classe Win32_Service
- Classe Win32_Service Serviços de Área de Trabalho Remota, método StartService
topic_type:
- apiref
api_name:
- Win32_Service.StartService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce4bd12150223d7cdc1340b7557ba309a1e07da4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084194"
---
# <a name="startservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="a0559-106">Método StartService da classe Win32_Service (Serviços de Área de Trabalho Remota)</span><span class="sxs-lookup"><span data-stu-id="a0559-106">StartService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="a0559-107">O método **StartService** tenta posicionar o serviço referenciado em seu estado de inicialização.</span><span class="sxs-lookup"><span data-stu-id="a0559-107">The **StartService** method attempts to place the referenced service into its startup state.</span></span>

<span data-ttu-id="a0559-108">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="a0559-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a0559-109">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a0559-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a0559-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a0559-110">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="a0559-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a0559-111">Parameters</span></span>

<span data-ttu-id="a0559-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a0559-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a0559-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a0559-113">Return value</span></span>

<span data-ttu-id="a0559-114">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="a0559-114">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="a0559-115">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="a0559-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="a0559-116">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="a0559-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="a0559-117">**0**</span><span class="sxs-lookup"><span data-stu-id="a0559-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="a0559-118">A solicitação foi aceita.</span><span class="sxs-lookup"><span data-stu-id="a0559-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="a0559-119">**1**</span><span class="sxs-lookup"><span data-stu-id="a0559-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="a0559-120">A solicitação não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="a0559-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="a0559-121">**2**</span><span class="sxs-lookup"><span data-stu-id="a0559-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="a0559-122">O usuário não tinha o acesso necessário.</span><span class="sxs-lookup"><span data-stu-id="a0559-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="a0559-123">**3**</span><span class="sxs-lookup"><span data-stu-id="a0559-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="a0559-124">O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.</span><span class="sxs-lookup"><span data-stu-id="a0559-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="a0559-125">**4**</span><span class="sxs-lookup"><span data-stu-id="a0559-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="a0559-126">O código de controle pedido não é válido ou é inaceitável para o serviço.</span><span class="sxs-lookup"><span data-stu-id="a0559-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="a0559-127">**5**</span><span class="sxs-lookup"><span data-stu-id="a0559-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="a0559-128">O código de controle solicitado não pode ser enviado ao serviço porque o estado do serviço ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).\*\*\*\* A propriedade State) é igual a 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="a0559-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="a0559-129">**6**</span><span class="sxs-lookup"><span data-stu-id="a0559-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="a0559-130">O serviço não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="a0559-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="a0559-131">**7**</span><span class="sxs-lookup"><span data-stu-id="a0559-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="a0559-132">O serviço não respondeu à solicitação de início em um tempo oportuno.</span><span class="sxs-lookup"><span data-stu-id="a0559-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="a0559-133">**8**</span><span class="sxs-lookup"><span data-stu-id="a0559-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="a0559-134">Falha desconhecida ao iniciar o serviço.</span><span class="sxs-lookup"><span data-stu-id="a0559-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="a0559-135">**9**</span><span class="sxs-lookup"><span data-stu-id="a0559-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="a0559-136">O caminho do diretório para o arquivo executável do serviço não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="a0559-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="a0559-137">**10**</span><span class="sxs-lookup"><span data-stu-id="a0559-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="a0559-138">O serviço já está em execução.</span><span class="sxs-lookup"><span data-stu-id="a0559-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="a0559-139">**11**</span><span class="sxs-lookup"><span data-stu-id="a0559-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="a0559-140">O banco de dados para adicionar um serviço novo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="a0559-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="a0559-141">**12**</span><span class="sxs-lookup"><span data-stu-id="a0559-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="a0559-142">Uma dependência da qual esse serviço depende foi removida do sistema.</span><span class="sxs-lookup"><span data-stu-id="a0559-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a0559-143">**13**</span><span class="sxs-lookup"><span data-stu-id="a0559-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="a0559-144">O serviço não localizou o serviço necessário em um serviço dependente.</span><span class="sxs-lookup"><span data-stu-id="a0559-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="a0559-145">**14**</span><span class="sxs-lookup"><span data-stu-id="a0559-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="a0559-146">O serviço foi desabilitado do sistema.</span><span class="sxs-lookup"><span data-stu-id="a0559-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a0559-147">**15**</span><span class="sxs-lookup"><span data-stu-id="a0559-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="a0559-148">O serviço não tem a autenticação correta para ser executado no sistema.</span><span class="sxs-lookup"><span data-stu-id="a0559-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="a0559-149">**16**</span><span class="sxs-lookup"><span data-stu-id="a0559-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="a0559-150">Este serviço está sendo removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="a0559-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a0559-151">**17**</span><span class="sxs-lookup"><span data-stu-id="a0559-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="a0559-152">O serviço não tem nenhum thread de execução.</span><span class="sxs-lookup"><span data-stu-id="a0559-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="a0559-153">**anos**</span><span class="sxs-lookup"><span data-stu-id="a0559-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="a0559-154">O serviço tem dependências circulares quando é iniciado.</span><span class="sxs-lookup"><span data-stu-id="a0559-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="a0559-155">**aprimora**</span><span class="sxs-lookup"><span data-stu-id="a0559-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="a0559-156">Um serviço está sendo executado com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="a0559-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="a0559-157">**20**</span><span class="sxs-lookup"><span data-stu-id="a0559-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="a0559-158">O nome do serviço tem caracteres inválidos.</span><span class="sxs-lookup"><span data-stu-id="a0559-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="a0559-159">**Abril**</span><span class="sxs-lookup"><span data-stu-id="a0559-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="a0559-160">Parâmetros inválidos foram passados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="a0559-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="a0559-161">**22**</span><span class="sxs-lookup"><span data-stu-id="a0559-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="a0559-162">A conta sob a qual este serviço é executado é inválida ou não tem as permissões para executar o serviço.</span><span class="sxs-lookup"><span data-stu-id="a0559-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="a0559-163">**23**</span><span class="sxs-lookup"><span data-stu-id="a0559-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="a0559-164">O serviço existe no banco de dados de serviços disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="a0559-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a0559-165">**24**</span><span class="sxs-lookup"><span data-stu-id="a0559-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="a0559-166">O serviço está pausado atualmente no sistema.</span><span class="sxs-lookup"><span data-stu-id="a0559-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a0559-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="a0559-167">Remarks</span></span>

<span data-ttu-id="a0559-168">Embora possa parecer não ser uma diferença prática entre um serviço que é interrompido e um serviço em pausa, os dois Estados aparecem de forma diferente para o SCM.</span><span class="sxs-lookup"><span data-stu-id="a0559-168">Although there might appear to be no practical difference between a service that is stopped and a service that is paused, the two states appear differently to the SCM.</span></span> <span data-ttu-id="a0559-169">Um serviço parado é um serviço que não está em execução e deve passar pelo procedimento de início do serviço inteiro.</span><span class="sxs-lookup"><span data-stu-id="a0559-169">A stopped service is a service that is not running and must go through the entire service start procedure.</span></span> <span data-ttu-id="a0559-170">Um serviço em pausa, no entanto, ainda está em execução, mas teve seu funcionamento suspenso.</span><span class="sxs-lookup"><span data-stu-id="a0559-170">A paused service, however, is still running but has had its functioning is suspended.</span></span> <span data-ttu-id="a0559-171">Por isso, um serviço em pausa não precisa passar pelo procedimento de início do serviço inteiro, mas precisa de um procedimento diferente para retomar o funcionamento.</span><span class="sxs-lookup"><span data-stu-id="a0559-171">Because of this, a paused service does not need to go through the entire service start procedure but needs a different procedure to resume functioning.</span></span>

<span data-ttu-id="a0559-172">Você deve usar o método apropriado para iniciar um serviço que foi interrompido ou para retomar um serviço que tenha sido pausado.</span><span class="sxs-lookup"><span data-stu-id="a0559-172">You must use the proper method to start a service that has been stopped or to resume a service that has been paused.</span></span> <span data-ttu-id="a0559-173">Os métodos de [**\_ serviço do Win32**](/windows/desktop/CIMWin32Prov/win32-service) **StartService** e [**ResumeService**](win32-terminalservice-resumeservice.md) devem ser usados nas seguintes situações:</span><span class="sxs-lookup"><span data-stu-id="a0559-173">The [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) methods **StartService** and [**ResumeService**](win32-terminalservice-resumeservice.md) should be used in the following situations:</span></span>

-   <span data-ttu-id="a0559-174">Se um serviço estiver parado no momento, você deverá usar o método **StartService** para reiniciá-lo; [**ResumeService**](win32-terminalservice-resumeservice.md) não pode iniciar um serviço que está parado no momento.</span><span class="sxs-lookup"><span data-stu-id="a0559-174">If a service is currently stopped, you must use the **StartService** method to restart it; [**ResumeService**](win32-terminalservice-resumeservice.md) cannot start a service that is currently stopped.</span></span>
-   <span data-ttu-id="a0559-175">Se um serviço estiver em pausa, você deverá usar [**ResumeService**](win32-terminalservice-resumeservice.md).</span><span class="sxs-lookup"><span data-stu-id="a0559-175">If a service is paused, you must use [**ResumeService**](win32-terminalservice-resumeservice.md).</span></span> <span data-ttu-id="a0559-176">Se você usar o método **StartService** em um serviço em pausa, receberá a mensagem "o serviço já está em execução".</span><span class="sxs-lookup"><span data-stu-id="a0559-176">If you use the **StartService** method on a paused service, you receive the message, "The service is already running."</span></span> <span data-ttu-id="a0559-177">No entanto, o serviço permanece em pausa até que o código de controle retome o serviço seja enviado a ele.</span><span class="sxs-lookup"><span data-stu-id="a0559-177">However, the service remains paused until the resume service control code is sent to it.</span></span>

<span data-ttu-id="a0559-178">Se você iniciar um serviço interrompido que depende de outro serviço, ambos os serviços serão iniciados.</span><span class="sxs-lookup"><span data-stu-id="a0559-178">If you start a stopped service that depends on another service, then both services are started.</span></span> <span data-ttu-id="a0559-179">Quando um serviço é iniciado com esse método, os serviços dependentes não são iniciados automaticamente.</span><span class="sxs-lookup"><span data-stu-id="a0559-179">When a service is started with this method, any dependent services are not automatically started.</span></span> <span data-ttu-id="a0559-180">Você deve usar a classe de associação [**Win32 \_ DependentService**](/windows/desktop/CIMWin32Prov/win32-dependentservice) e os [ASSOCIADORES de](/windows/desktop/WmiSdk/associators-of-statement) consulta para localizar os dependentes e iniciá-los separadamente.</span><span class="sxs-lookup"><span data-stu-id="a0559-180">You must use the association class [**Win32\_DependentService**](/windows/desktop/CIMWin32Prov/win32-dependentservice) and the [Associators Of](/windows/desktop/WmiSdk/associators-of-statement) query to locate the dependents and start them separately.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0559-181">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0559-181">Requirements</span></span>



| <span data-ttu-id="a0559-182">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0559-182">Requirement</span></span> | <span data-ttu-id="a0559-183">Valor</span><span class="sxs-lookup"><span data-stu-id="a0559-183">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0559-184">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0559-184">Minimum supported client</span></span><br/> | <span data-ttu-id="a0559-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a0559-185">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a0559-186">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0559-186">Minimum supported server</span></span><br/> | <span data-ttu-id="a0559-187">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a0559-187">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a0559-188">Namespace</span><span class="sxs-lookup"><span data-stu-id="a0559-188">Namespace</span></span><br/>                | <span data-ttu-id="a0559-189">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="a0559-189">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="a0559-190">MOF</span><span class="sxs-lookup"><span data-stu-id="a0559-190">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a0559-191"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a0559-191"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a0559-192">DLL</span><span class="sxs-lookup"><span data-stu-id="a0559-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0559-193"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0559-193"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0559-194">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a0559-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0559-195">**\_Serviço Win32**</span><span class="sxs-lookup"><span data-stu-id="a0559-195">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="a0559-196">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="a0559-196">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="a0559-197">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="a0559-197">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="a0559-198">Tarefas do WMI: serviços</span><span class="sxs-lookup"><span data-stu-id="a0559-198">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 


---
title: Método InterrogateService da classe Win32_Service (Serviços de Área de Trabalho Remota)
description: Método InterrogateService da classe Win32_Service (Serviços de Área de Trabalho Remota) – solicita que o serviço referenciado atualize seu estado para o Service Manager.
ms.assetid: 7B572049-416E-4429-BD53-119FF570B2D8
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método InterrogateService
- Método InterrogateService Serviços de Área de Trabalho Remota, classe Win32_Service
- Classe Win32_Service Serviços de Área de Trabalho Remota, método InterrogateService
topic_type:
- apiref
api_name:
- Win32_Service.InterrogateService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 850953b210ea11b9dd1000326d6793e3651ce538
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090654"
---
# <a name="interrogateservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="080c5-106">Método InterrogateService da classe Win32_Service (Serviços de Área de Trabalho Remota)</span><span class="sxs-lookup"><span data-stu-id="080c5-106">InterrogateService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="080c5-107">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **InterrogateService** solicita que o serviço referenciado atualize seu estado para o Service Manager.</span><span class="sxs-lookup"><span data-stu-id="080c5-107">The **InterrogateService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method requests that the referenced service update its state to the service manager.</span></span>

<span data-ttu-id="080c5-108">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="080c5-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="080c5-109">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="080c5-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="080c5-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="080c5-110">Syntax</span></span>


```mof
uint32 InterrogateService();
```



## <a name="parameters"></a><span data-ttu-id="080c5-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="080c5-111">Parameters</span></span>

<span data-ttu-id="080c5-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="080c5-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="080c5-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="080c5-113">Return value</span></span>

<span data-ttu-id="080c5-114">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="080c5-114">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="080c5-115">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="080c5-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="080c5-116">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="080c5-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="080c5-117">**0**</span><span class="sxs-lookup"><span data-stu-id="080c5-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="080c5-118">A solicitação foi aceita.</span><span class="sxs-lookup"><span data-stu-id="080c5-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="080c5-119">**1**</span><span class="sxs-lookup"><span data-stu-id="080c5-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="080c5-120">A solicitação não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="080c5-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="080c5-121">**2**</span><span class="sxs-lookup"><span data-stu-id="080c5-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="080c5-122">O usuário não tinha o acesso necessário.</span><span class="sxs-lookup"><span data-stu-id="080c5-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="080c5-123">**3**</span><span class="sxs-lookup"><span data-stu-id="080c5-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="080c5-124">O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.</span><span class="sxs-lookup"><span data-stu-id="080c5-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="080c5-125">**4**</span><span class="sxs-lookup"><span data-stu-id="080c5-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="080c5-126">O código de controle pedido não é válido ou é inaceitável para o serviço.</span><span class="sxs-lookup"><span data-stu-id="080c5-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="080c5-127">**5**</span><span class="sxs-lookup"><span data-stu-id="080c5-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="080c5-128">O código de controle solicitado não pode ser enviado ao serviço porque o estado do serviço ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).\*\*\*\* A propriedade State) é igual a 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="080c5-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="080c5-129">**6**</span><span class="sxs-lookup"><span data-stu-id="080c5-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="080c5-130">O serviço não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="080c5-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="080c5-131">**7**</span><span class="sxs-lookup"><span data-stu-id="080c5-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="080c5-132">O serviço não respondeu à solicitação de início em um tempo oportuno.</span><span class="sxs-lookup"><span data-stu-id="080c5-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="080c5-133">**8**</span><span class="sxs-lookup"><span data-stu-id="080c5-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="080c5-134">Falha desconhecida ao iniciar o serviço.</span><span class="sxs-lookup"><span data-stu-id="080c5-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="080c5-135">**9**</span><span class="sxs-lookup"><span data-stu-id="080c5-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="080c5-136">O caminho do diretório para o arquivo executável do serviço não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="080c5-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="080c5-137">**10**</span><span class="sxs-lookup"><span data-stu-id="080c5-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="080c5-138">O serviço já está em execução.</span><span class="sxs-lookup"><span data-stu-id="080c5-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="080c5-139">**11**</span><span class="sxs-lookup"><span data-stu-id="080c5-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="080c5-140">O banco de dados para adicionar um serviço novo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="080c5-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="080c5-141">**12**</span><span class="sxs-lookup"><span data-stu-id="080c5-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="080c5-142">Uma dependência da qual esse serviço depende foi removida do sistema.</span><span class="sxs-lookup"><span data-stu-id="080c5-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="080c5-143">**13**</span><span class="sxs-lookup"><span data-stu-id="080c5-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="080c5-144">O serviço não localizou o serviço necessário em um serviço dependente.</span><span class="sxs-lookup"><span data-stu-id="080c5-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="080c5-145">**14**</span><span class="sxs-lookup"><span data-stu-id="080c5-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="080c5-146">O serviço foi desabilitado do sistema.</span><span class="sxs-lookup"><span data-stu-id="080c5-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="080c5-147">**15**</span><span class="sxs-lookup"><span data-stu-id="080c5-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="080c5-148">O serviço não tem a autenticação correta para ser executado no sistema.</span><span class="sxs-lookup"><span data-stu-id="080c5-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="080c5-149">**16**</span><span class="sxs-lookup"><span data-stu-id="080c5-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="080c5-150">Este serviço está sendo removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="080c5-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="080c5-151">**17**</span><span class="sxs-lookup"><span data-stu-id="080c5-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="080c5-152">O serviço não tem nenhum thread de execução.</span><span class="sxs-lookup"><span data-stu-id="080c5-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="080c5-153">**anos**</span><span class="sxs-lookup"><span data-stu-id="080c5-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="080c5-154">O serviço tem dependências circulares quando é iniciado.</span><span class="sxs-lookup"><span data-stu-id="080c5-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="080c5-155">**aprimora**</span><span class="sxs-lookup"><span data-stu-id="080c5-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="080c5-156">Um serviço está sendo executado com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="080c5-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="080c5-157">**20**</span><span class="sxs-lookup"><span data-stu-id="080c5-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="080c5-158">O nome do serviço tem caracteres inválidos.</span><span class="sxs-lookup"><span data-stu-id="080c5-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="080c5-159">**Abril**</span><span class="sxs-lookup"><span data-stu-id="080c5-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="080c5-160">Parâmetros inválidos foram passados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="080c5-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="080c5-161">**22**</span><span class="sxs-lookup"><span data-stu-id="080c5-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="080c5-162">A conta sob a qual este serviço é executado é inválida ou não tem as permissões para executar o serviço.</span><span class="sxs-lookup"><span data-stu-id="080c5-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="080c5-163">**23**</span><span class="sxs-lookup"><span data-stu-id="080c5-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="080c5-164">O serviço existe no banco de dados de serviços disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="080c5-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="080c5-165">**24**</span><span class="sxs-lookup"><span data-stu-id="080c5-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="080c5-166">O serviço está pausado atualmente no sistema.</span><span class="sxs-lookup"><span data-stu-id="080c5-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="080c5-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="080c5-167">Requirements</span></span>



| <span data-ttu-id="080c5-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="080c5-168">Requirement</span></span> | <span data-ttu-id="080c5-169">Valor</span><span class="sxs-lookup"><span data-stu-id="080c5-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="080c5-170">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="080c5-170">Minimum supported client</span></span><br/> | <span data-ttu-id="080c5-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="080c5-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="080c5-172">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="080c5-172">Minimum supported server</span></span><br/> | <span data-ttu-id="080c5-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="080c5-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="080c5-174">Namespace</span><span class="sxs-lookup"><span data-stu-id="080c5-174">Namespace</span></span><br/>                | <span data-ttu-id="080c5-175">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="080c5-175">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="080c5-176">MOF</span><span class="sxs-lookup"><span data-stu-id="080c5-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="080c5-177"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="080c5-177"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="080c5-178">DLL</span><span class="sxs-lookup"><span data-stu-id="080c5-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="080c5-179"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="080c5-179"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="080c5-180">Consulte também</span><span class="sxs-lookup"><span data-stu-id="080c5-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="080c5-181">**\_Serviço Win32**</span><span class="sxs-lookup"><span data-stu-id="080c5-181">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="080c5-182">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="080c5-182">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="080c5-183">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="080c5-183">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="080c5-184">Tarefas do WMI: serviços</span><span class="sxs-lookup"><span data-stu-id="080c5-184">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 


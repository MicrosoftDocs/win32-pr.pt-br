---
description: Solicita que o serviço referenciado atualize seu estado para o Service Manager.
ms.assetid: a4ea8753-1859-4d97-b9ca-47598c7e7654
ms.tgt_platform: multiple
title: Método InterrogateService da classe Win32_Service (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.InterrogateService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7ad1f56afcbe42ced19da823c454291a7b5282d7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089097"
---
# <a name="interrogateservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="3ffde-103">Método InterrogateService da classe Win32_Service (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="3ffde-103">InterrogateService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="3ffde-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **InterrogateService** solicita que o serviço referenciado atualize seu estado para o Service Manager.</span><span class="sxs-lookup"><span data-stu-id="3ffde-104">The **InterrogateService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method requests that the referenced service update its state to the service manager.</span></span>

<span data-ttu-id="3ffde-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="3ffde-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3ffde-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3ffde-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3ffde-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ffde-107">Syntax</span></span>


```mof
uint32 InterrogateService();
```



## <a name="parameters"></a><span data-ttu-id="3ffde-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ffde-108">Parameters</span></span>

<span data-ttu-id="3ffde-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="3ffde-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3ffde-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3ffde-110">Return value</span></span>

<span data-ttu-id="3ffde-111">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="3ffde-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="3ffde-112">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="3ffde-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="3ffde-113">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="3ffde-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="3ffde-114">**0**</span><span class="sxs-lookup"><span data-stu-id="3ffde-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="3ffde-115">A solicitação foi aceita.</span><span class="sxs-lookup"><span data-stu-id="3ffde-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="3ffde-116">**1**</span><span class="sxs-lookup"><span data-stu-id="3ffde-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="3ffde-117">A solicitação não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="3ffde-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="3ffde-118">**2**</span><span class="sxs-lookup"><span data-stu-id="3ffde-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="3ffde-119">O usuário não tinha o acesso necessário.</span><span class="sxs-lookup"><span data-stu-id="3ffde-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="3ffde-120">**3**</span><span class="sxs-lookup"><span data-stu-id="3ffde-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="3ffde-121">O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.</span><span class="sxs-lookup"><span data-stu-id="3ffde-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="3ffde-122">**4**</span><span class="sxs-lookup"><span data-stu-id="3ffde-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="3ffde-123">O código de controle pedido não é válido ou é inaceitável para o serviço.</span><span class="sxs-lookup"><span data-stu-id="3ffde-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="3ffde-124">**5**</span><span class="sxs-lookup"><span data-stu-id="3ffde-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="3ffde-125">O código de controle solicitado não pode ser enviado ao serviço porque o estado do serviço ([**Win32 \_ BaseService**](win32-baseservice.md).\*\*\*\* A propriedade State) é igual a 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="3ffde-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="3ffde-126">**6**</span><span class="sxs-lookup"><span data-stu-id="3ffde-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="3ffde-127">O serviço não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="3ffde-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="3ffde-128">**7**</span><span class="sxs-lookup"><span data-stu-id="3ffde-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="3ffde-129">O serviço não respondeu à solicitação de início em um tempo oportuno.</span><span class="sxs-lookup"><span data-stu-id="3ffde-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="3ffde-130">**8**</span><span class="sxs-lookup"><span data-stu-id="3ffde-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="3ffde-131">Falha desconhecida ao iniciar o serviço.</span><span class="sxs-lookup"><span data-stu-id="3ffde-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="3ffde-132">**9**</span><span class="sxs-lookup"><span data-stu-id="3ffde-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="3ffde-133">O caminho do diretório para o arquivo executável do serviço não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="3ffde-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="3ffde-134">**10**</span><span class="sxs-lookup"><span data-stu-id="3ffde-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="3ffde-135">O serviço já está em execução.</span><span class="sxs-lookup"><span data-stu-id="3ffde-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="3ffde-136">**11**</span><span class="sxs-lookup"><span data-stu-id="3ffde-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="3ffde-137">O banco de dados para adicionar um serviço novo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="3ffde-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="3ffde-138">**12**</span><span class="sxs-lookup"><span data-stu-id="3ffde-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="3ffde-139">Uma dependência da qual esse serviço depende foi removida do sistema.</span><span class="sxs-lookup"><span data-stu-id="3ffde-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3ffde-140">**13**</span><span class="sxs-lookup"><span data-stu-id="3ffde-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="3ffde-141">O serviço não localizou o serviço necessário em um serviço dependente.</span><span class="sxs-lookup"><span data-stu-id="3ffde-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="3ffde-142">**14**</span><span class="sxs-lookup"><span data-stu-id="3ffde-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="3ffde-143">O serviço foi desabilitado do sistema.</span><span class="sxs-lookup"><span data-stu-id="3ffde-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3ffde-144">**15**</span><span class="sxs-lookup"><span data-stu-id="3ffde-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="3ffde-145">O serviço não tem a autenticação correta para ser executado no sistema.</span><span class="sxs-lookup"><span data-stu-id="3ffde-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="3ffde-146">**16**</span><span class="sxs-lookup"><span data-stu-id="3ffde-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="3ffde-147">Este serviço está sendo removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="3ffde-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3ffde-148">**17**</span><span class="sxs-lookup"><span data-stu-id="3ffde-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="3ffde-149">O serviço não tem nenhum thread de execução.</span><span class="sxs-lookup"><span data-stu-id="3ffde-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="3ffde-150">**anos**</span><span class="sxs-lookup"><span data-stu-id="3ffde-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="3ffde-151">O serviço tem dependências circulares quando é iniciado.</span><span class="sxs-lookup"><span data-stu-id="3ffde-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="3ffde-152">**aprimora**</span><span class="sxs-lookup"><span data-stu-id="3ffde-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="3ffde-153">Um serviço está sendo executado com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="3ffde-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="3ffde-154">**20**</span><span class="sxs-lookup"><span data-stu-id="3ffde-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="3ffde-155">O nome do serviço tem caracteres inválidos.</span><span class="sxs-lookup"><span data-stu-id="3ffde-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="3ffde-156">**Abril**</span><span class="sxs-lookup"><span data-stu-id="3ffde-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="3ffde-157">Parâmetros inválidos foram passados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="3ffde-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="3ffde-158">**22**</span><span class="sxs-lookup"><span data-stu-id="3ffde-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="3ffde-159">A conta sob a qual este serviço é executado é inválida ou não tem as permissões para executar o serviço.</span><span class="sxs-lookup"><span data-stu-id="3ffde-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="3ffde-160">**23**</span><span class="sxs-lookup"><span data-stu-id="3ffde-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="3ffde-161">O serviço existe no banco de dados de serviços disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="3ffde-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3ffde-162">**24**</span><span class="sxs-lookup"><span data-stu-id="3ffde-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="3ffde-163">O serviço está pausado atualmente no sistema.</span><span class="sxs-lookup"><span data-stu-id="3ffde-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3ffde-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ffde-164">Requirements</span></span>



| <span data-ttu-id="3ffde-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ffde-165">Requirement</span></span> | <span data-ttu-id="3ffde-166">Valor</span><span class="sxs-lookup"><span data-stu-id="3ffde-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ffde-167">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ffde-167">Minimum supported client</span></span><br/> | <span data-ttu-id="3ffde-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3ffde-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3ffde-169">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ffde-169">Minimum supported server</span></span><br/> | <span data-ttu-id="3ffde-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3ffde-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3ffde-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="3ffde-171">Namespace</span></span><br/>                | <span data-ttu-id="3ffde-172">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3ffde-172">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3ffde-173">MOF</span><span class="sxs-lookup"><span data-stu-id="3ffde-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ffde-174"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3ffde-174"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ffde-175">DLL</span><span class="sxs-lookup"><span data-stu-id="3ffde-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ffde-176"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ffde-176"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ffde-177">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ffde-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ffde-178">**\_Serviço Win32**</span><span class="sxs-lookup"><span data-stu-id="3ffde-178">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

<span data-ttu-id="3ffde-179">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3ffde-179">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3ffde-180">**\_BaseService Win32**</span><span class="sxs-lookup"><span data-stu-id="3ffde-180">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> <dt>

[<span data-ttu-id="3ffde-181">Tarefas do WMI: serviços</span><span class="sxs-lookup"><span data-stu-id="3ffde-181">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 


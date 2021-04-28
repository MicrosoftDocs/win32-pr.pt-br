---
title: Método UserControlService da classe Win32_Service (Serviços de Área de Trabalho Remota)
description: Método UserControlService da classe Win32_Service (Serviços de Área de Trabalho Remota) – tenta enviar um código de controle definido pelo usuário para o serviço referenciado.
ms.assetid: 7B9020C1-2183-4FC4-ABCF-CE34111FF5D3
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método UserControlService
- Método UserControlService Serviços de Área de Trabalho Remota, classe Win32_Service
- Classe Win32_Service Serviços de Área de Trabalho Remota, método UserControlService
topic_type:
- apiref
api_name:
- Win32_Service.UserControlService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e71a33056f596afaf577968a5c725b3f64f79b6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090604"
---
# <a name="usercontrolservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="d0669-106">Método UserControlService da classe Win32_Service (Serviços de Área de Trabalho Remota)</span><span class="sxs-lookup"><span data-stu-id="d0669-106">UserControlService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="d0669-107">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **UserControlService** tenta enviar um código de controle definido pelo usuário para o serviço referenciado.</span><span class="sxs-lookup"><span data-stu-id="d0669-107">The **UserControlService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to send a user-defined control code to the referenced service.</span></span>

<span data-ttu-id="d0669-108">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="d0669-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d0669-109">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d0669-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d0669-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d0669-110">Syntax</span></span>


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a><span data-ttu-id="d0669-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d0669-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0669-112">*ControlCode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d0669-112">*ControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0669-113">Especifica os valores definidos (de 128 a 255) que fornecem comandos de controle específicos para um usuário.</span><span class="sxs-lookup"><span data-stu-id="d0669-113">Specifies defined values (from 128 to 255) that provide control commands specific to a user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0669-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d0669-114">Return value</span></span>

<span data-ttu-id="d0669-115">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="d0669-115">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="d0669-116">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="d0669-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="d0669-117">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="d0669-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="d0669-118">**0**</span><span class="sxs-lookup"><span data-stu-id="d0669-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="d0669-119">A solicitação foi aceita.</span><span class="sxs-lookup"><span data-stu-id="d0669-119">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="d0669-120">**1**</span><span class="sxs-lookup"><span data-stu-id="d0669-120">**1**</span></span>
</dt> <dd>

<span data-ttu-id="d0669-121">A solicitação não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="d0669-121">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="d0669-122">**2**</span><span class="sxs-lookup"><span data-stu-id="d0669-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="d0669-123">O usuário não tinha o acesso necessário.</span><span class="sxs-lookup"><span data-stu-id="d0669-123">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="d0669-124">**3**</span><span class="sxs-lookup"><span data-stu-id="d0669-124">**3**</span></span>
</dt> <dd>

<span data-ttu-id="d0669-125">O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.</span><span class="sxs-lookup"><span data-stu-id="d0669-125">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="d0669-126">**4**</span><span class="sxs-lookup"><span data-stu-id="d0669-126">**4**</span></span>
</dt> <dd>

<span data-ttu-id="d0669-127">O código de controle pedido não é válido ou é inaceitável para o serviço.</span><span class="sxs-lookup"><span data-stu-id="d0669-127">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="d0669-128">**5**</span><span class="sxs-lookup"><span data-stu-id="d0669-128">**5**</span></span>
</dt> <dd>

<span data-ttu-id="d0669-129">O código de controle solicitado não pode ser enviado ao serviço porque o estado do serviço ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).\*\*\*\* A propriedade State) é igual a 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="d0669-129">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="d0669-130">**6**</span><span class="sxs-lookup"><span data-stu-id="d0669-130">**6**</span></span>
</dt> <dd>

<span data-ttu-id="d0669-131">O serviço não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="d0669-131">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="d0669-132">**7**</span><span class="sxs-lookup"><span data-stu-id="d0669-132">**7**</span></span>
</dt> <dd>

<span data-ttu-id="d0669-133">O serviço não respondeu à solicitação de início em um tempo oportuno.</span><span class="sxs-lookup"><span data-stu-id="d0669-133">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="d0669-134">**8**</span><span class="sxs-lookup"><span data-stu-id="d0669-134">**8**</span></span>
</dt> <dd>

<span data-ttu-id="d0669-135">Falha desconhecida ao iniciar o serviço.</span><span class="sxs-lookup"><span data-stu-id="d0669-135">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="d0669-136">**9**</span><span class="sxs-lookup"><span data-stu-id="d0669-136">**9**</span></span>
</dt> <dd>

<span data-ttu-id="d0669-137">O caminho do diretório para o arquivo executável do serviço não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="d0669-137">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="d0669-138">**10**</span><span class="sxs-lookup"><span data-stu-id="d0669-138">**10**</span></span>
</dt> <dd>

<span data-ttu-id="d0669-139">O serviço já está em execução.</span><span class="sxs-lookup"><span data-stu-id="d0669-139">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="d0669-140">**11**</span><span class="sxs-lookup"><span data-stu-id="d0669-140">**11**</span></span>
</dt> <dd>

<span data-ttu-id="d0669-141">O banco de dados para adicionar um serviço novo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="d0669-141">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="d0669-142">**12**</span><span class="sxs-lookup"><span data-stu-id="d0669-142">**12**</span></span>
</dt> <dd>

<span data-ttu-id="d0669-143">Uma dependência da qual esse serviço depende foi removida do sistema.</span><span class="sxs-lookup"><span data-stu-id="d0669-143">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d0669-144">**13**</span><span class="sxs-lookup"><span data-stu-id="d0669-144">**13**</span></span>
</dt> <dd>

<span data-ttu-id="d0669-145">O serviço não localizou o serviço necessário em um serviço dependente.</span><span class="sxs-lookup"><span data-stu-id="d0669-145">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="d0669-146">**14**</span><span class="sxs-lookup"><span data-stu-id="d0669-146">**14**</span></span>
</dt> <dd>

<span data-ttu-id="d0669-147">O serviço foi desabilitado do sistema.</span><span class="sxs-lookup"><span data-stu-id="d0669-147">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d0669-148">**15**</span><span class="sxs-lookup"><span data-stu-id="d0669-148">**15**</span></span>
</dt> <dd>

<span data-ttu-id="d0669-149">O serviço não tem a autenticação correta para ser executado no sistema.</span><span class="sxs-lookup"><span data-stu-id="d0669-149">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="d0669-150">**16**</span><span class="sxs-lookup"><span data-stu-id="d0669-150">**16**</span></span>
</dt> <dd>

<span data-ttu-id="d0669-151">Este serviço está sendo removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="d0669-151">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d0669-152">**17**</span><span class="sxs-lookup"><span data-stu-id="d0669-152">**17**</span></span>
</dt> <dd>

<span data-ttu-id="d0669-153">O serviço não tem nenhum thread de execução.</span><span class="sxs-lookup"><span data-stu-id="d0669-153">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="d0669-154">**anos**</span><span class="sxs-lookup"><span data-stu-id="d0669-154">**18**</span></span>
</dt> <dd>

<span data-ttu-id="d0669-155">O serviço tem dependências circulares quando é iniciado.</span><span class="sxs-lookup"><span data-stu-id="d0669-155">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="d0669-156">**aprimora**</span><span class="sxs-lookup"><span data-stu-id="d0669-156">**19**</span></span>
</dt> <dd>

<span data-ttu-id="d0669-157">Um serviço está sendo executado com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="d0669-157">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="d0669-158">**20**</span><span class="sxs-lookup"><span data-stu-id="d0669-158">**20**</span></span>
</dt> <dd>

<span data-ttu-id="d0669-159">O nome do serviço tem caracteres inválidos.</span><span class="sxs-lookup"><span data-stu-id="d0669-159">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="d0669-160">**Abril**</span><span class="sxs-lookup"><span data-stu-id="d0669-160">**21**</span></span>
</dt> <dd>

<span data-ttu-id="d0669-161">Parâmetros inválidos foram passados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="d0669-161">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="d0669-162">**22**</span><span class="sxs-lookup"><span data-stu-id="d0669-162">**22**</span></span>
</dt> <dd>

<span data-ttu-id="d0669-163">A conta sob a qual este serviço é executado é inválida ou não tem as permissões para executar o serviço.</span><span class="sxs-lookup"><span data-stu-id="d0669-163">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="d0669-164">**23**</span><span class="sxs-lookup"><span data-stu-id="d0669-164">**23**</span></span>
</dt> <dd>

<span data-ttu-id="d0669-165">O serviço existe no banco de dados de serviços disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="d0669-165">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d0669-166">**24**</span><span class="sxs-lookup"><span data-stu-id="d0669-166">**24**</span></span>
</dt> <dd>

<span data-ttu-id="d0669-167">O serviço está pausado atualmente no sistema.</span><span class="sxs-lookup"><span data-stu-id="d0669-167">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d0669-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0669-168">Requirements</span></span>



| <span data-ttu-id="d0669-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0669-169">Requirement</span></span> | <span data-ttu-id="d0669-170">Valor</span><span class="sxs-lookup"><span data-stu-id="d0669-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0669-171">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0669-171">Minimum supported client</span></span><br/> | <span data-ttu-id="d0669-172">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d0669-172">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d0669-173">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0669-173">Minimum supported server</span></span><br/> | <span data-ttu-id="d0669-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d0669-174">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d0669-175">Namespace</span><span class="sxs-lookup"><span data-stu-id="d0669-175">Namespace</span></span><br/>                | <span data-ttu-id="d0669-176">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="d0669-176">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d0669-177">MOF</span><span class="sxs-lookup"><span data-stu-id="d0669-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d0669-178"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d0669-178"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d0669-179">DLL</span><span class="sxs-lookup"><span data-stu-id="d0669-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0669-180"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0669-180"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0669-181">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d0669-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0669-182">**\_Serviço Win32**</span><span class="sxs-lookup"><span data-stu-id="d0669-182">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="d0669-183">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="d0669-183">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="d0669-184">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="d0669-184">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> </dl>

 


---
description: Método UserControlService da classe Win32_Service (provedores WMI CIMWin32) – tenta enviar um código de controle definido pelo usuário para o serviço referenciado.
ms.assetid: a7132c9b-6faf-4182-a5b8-3f2334c1a74b
ms.tgt_platform: multiple
title: Método UserControlService da classe Win32_Service (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.UserControlService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 455128b35c2645c6aa6ea10f64d12dff392fecca
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099995"
---
# <a name="usercontrolservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="5ec77-103">Método UserControlService da classe Win32_Service (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="5ec77-103">UserControlService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="5ec77-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **UserControlService** tenta enviar um código de controle definido pelo usuário para o serviço referenciado.</span><span class="sxs-lookup"><span data-stu-id="5ec77-104">The **UserControlService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to send a user-defined control code to the referenced service.</span></span>

<span data-ttu-id="5ec77-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="5ec77-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5ec77-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5ec77-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5ec77-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5ec77-107">Syntax</span></span>


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a><span data-ttu-id="5ec77-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5ec77-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ec77-109">*ControlCode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5ec77-109">*ControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ec77-110">Especifica os valores definidos (de 128 a 255) que fornecem comandos de controle específicos para um usuário.</span><span class="sxs-lookup"><span data-stu-id="5ec77-110">Specifies defined values (from 128 to 255) that provide control commands specific to a user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ec77-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="5ec77-111">Return value</span></span>

<span data-ttu-id="5ec77-112">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="5ec77-112">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="5ec77-113">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="5ec77-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="5ec77-114">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="5ec77-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="5ec77-115">**0**</span><span class="sxs-lookup"><span data-stu-id="5ec77-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="5ec77-116">A solicitação foi aceita.</span><span class="sxs-lookup"><span data-stu-id="5ec77-116">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="5ec77-117">**1**</span><span class="sxs-lookup"><span data-stu-id="5ec77-117">**1**</span></span>
</dt> <dd>

<span data-ttu-id="5ec77-118">A solicitação não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="5ec77-118">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="5ec77-119">**2**</span><span class="sxs-lookup"><span data-stu-id="5ec77-119">**2**</span></span>
</dt> <dd>

<span data-ttu-id="5ec77-120">O usuário não tinha o acesso necessário.</span><span class="sxs-lookup"><span data-stu-id="5ec77-120">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="5ec77-121">**3**</span><span class="sxs-lookup"><span data-stu-id="5ec77-121">**3**</span></span>
</dt> <dd>

<span data-ttu-id="5ec77-122">O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.</span><span class="sxs-lookup"><span data-stu-id="5ec77-122">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="5ec77-123">**4**</span><span class="sxs-lookup"><span data-stu-id="5ec77-123">**4**</span></span>
</dt> <dd>

<span data-ttu-id="5ec77-124">O código de controle pedido não é válido ou é inaceitável para o serviço.</span><span class="sxs-lookup"><span data-stu-id="5ec77-124">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="5ec77-125">**5**</span><span class="sxs-lookup"><span data-stu-id="5ec77-125">**5**</span></span>
</dt> <dd>

<span data-ttu-id="5ec77-126">O código de controle solicitado não pode ser enviado ao serviço porque o estado do serviço ([**Win32 \_ BaseService**](win32-baseservice.md).\*\*\*\* A propriedade State) é igual a 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="5ec77-126">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="5ec77-127">**6**</span><span class="sxs-lookup"><span data-stu-id="5ec77-127">**6**</span></span>
</dt> <dd>

<span data-ttu-id="5ec77-128">O serviço não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="5ec77-128">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="5ec77-129">**7**</span><span class="sxs-lookup"><span data-stu-id="5ec77-129">**7**</span></span>
</dt> <dd>

<span data-ttu-id="5ec77-130">O serviço não respondeu à solicitação de início em um tempo oportuno.</span><span class="sxs-lookup"><span data-stu-id="5ec77-130">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="5ec77-131">**8**</span><span class="sxs-lookup"><span data-stu-id="5ec77-131">**8**</span></span>
</dt> <dd>

<span data-ttu-id="5ec77-132">Falha desconhecida ao iniciar o serviço.</span><span class="sxs-lookup"><span data-stu-id="5ec77-132">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="5ec77-133">**9**</span><span class="sxs-lookup"><span data-stu-id="5ec77-133">**9**</span></span>
</dt> <dd>

<span data-ttu-id="5ec77-134">O caminho do diretório para o arquivo executável do serviço não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="5ec77-134">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="5ec77-135">**10**</span><span class="sxs-lookup"><span data-stu-id="5ec77-135">**10**</span></span>
</dt> <dd>

<span data-ttu-id="5ec77-136">O serviço já está em execução.</span><span class="sxs-lookup"><span data-stu-id="5ec77-136">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="5ec77-137">**11**</span><span class="sxs-lookup"><span data-stu-id="5ec77-137">**11**</span></span>
</dt> <dd>

<span data-ttu-id="5ec77-138">O banco de dados para adicionar um serviço novo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="5ec77-138">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="5ec77-139">**12**</span><span class="sxs-lookup"><span data-stu-id="5ec77-139">**12**</span></span>
</dt> <dd>

<span data-ttu-id="5ec77-140">Uma dependência da qual esse serviço depende foi removida do sistema.</span><span class="sxs-lookup"><span data-stu-id="5ec77-140">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="5ec77-141">**13**</span><span class="sxs-lookup"><span data-stu-id="5ec77-141">**13**</span></span>
</dt> <dd>

<span data-ttu-id="5ec77-142">O serviço não localizou o serviço necessário em um serviço dependente.</span><span class="sxs-lookup"><span data-stu-id="5ec77-142">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="5ec77-143">**14**</span><span class="sxs-lookup"><span data-stu-id="5ec77-143">**14**</span></span>
</dt> <dd>

<span data-ttu-id="5ec77-144">O serviço foi desabilitado do sistema.</span><span class="sxs-lookup"><span data-stu-id="5ec77-144">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="5ec77-145">**15**</span><span class="sxs-lookup"><span data-stu-id="5ec77-145">**15**</span></span>
</dt> <dd>

<span data-ttu-id="5ec77-146">O serviço não tem a autenticação correta para ser executado no sistema.</span><span class="sxs-lookup"><span data-stu-id="5ec77-146">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="5ec77-147">**16**</span><span class="sxs-lookup"><span data-stu-id="5ec77-147">**16**</span></span>
</dt> <dd>

<span data-ttu-id="5ec77-148">Este serviço está sendo removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="5ec77-148">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="5ec77-149">**17**</span><span class="sxs-lookup"><span data-stu-id="5ec77-149">**17**</span></span>
</dt> <dd>

<span data-ttu-id="5ec77-150">O serviço não tem nenhum thread de execução.</span><span class="sxs-lookup"><span data-stu-id="5ec77-150">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="5ec77-151">**anos**</span><span class="sxs-lookup"><span data-stu-id="5ec77-151">**18**</span></span>
</dt> <dd>

<span data-ttu-id="5ec77-152">O serviço tem dependências circulares quando é iniciado.</span><span class="sxs-lookup"><span data-stu-id="5ec77-152">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="5ec77-153">**aprimora**</span><span class="sxs-lookup"><span data-stu-id="5ec77-153">**19**</span></span>
</dt> <dd>

<span data-ttu-id="5ec77-154">Um serviço está sendo executado com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="5ec77-154">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="5ec77-155">**20**</span><span class="sxs-lookup"><span data-stu-id="5ec77-155">**20**</span></span>
</dt> <dd>

<span data-ttu-id="5ec77-156">O nome do serviço tem caracteres inválidos.</span><span class="sxs-lookup"><span data-stu-id="5ec77-156">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="5ec77-157">**Abril**</span><span class="sxs-lookup"><span data-stu-id="5ec77-157">**21**</span></span>
</dt> <dd>

<span data-ttu-id="5ec77-158">Parâmetros inválidos foram passados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="5ec77-158">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="5ec77-159">**22**</span><span class="sxs-lookup"><span data-stu-id="5ec77-159">**22**</span></span>
</dt> <dd>

<span data-ttu-id="5ec77-160">A conta sob a qual este serviço é executado é inválida ou não tem as permissões para executar o serviço.</span><span class="sxs-lookup"><span data-stu-id="5ec77-160">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="5ec77-161">**23**</span><span class="sxs-lookup"><span data-stu-id="5ec77-161">**23**</span></span>
</dt> <dd>

<span data-ttu-id="5ec77-162">O serviço existe no banco de dados de serviços disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="5ec77-162">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="5ec77-163">**24**</span><span class="sxs-lookup"><span data-stu-id="5ec77-163">**24**</span></span>
</dt> <dd>

<span data-ttu-id="5ec77-164">O serviço está pausado atualmente no sistema.</span><span class="sxs-lookup"><span data-stu-id="5ec77-164">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ec77-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ec77-165">Requirements</span></span>



| <span data-ttu-id="5ec77-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ec77-166">Requirement</span></span> | <span data-ttu-id="5ec77-167">Valor</span><span class="sxs-lookup"><span data-stu-id="5ec77-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ec77-168">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ec77-168">Minimum supported client</span></span><br/> | <span data-ttu-id="5ec77-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5ec77-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5ec77-170">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ec77-170">Minimum supported server</span></span><br/> | <span data-ttu-id="5ec77-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ec77-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5ec77-172">Namespace</span><span class="sxs-lookup"><span data-stu-id="5ec77-172">Namespace</span></span><br/>                | <span data-ttu-id="5ec77-173">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5ec77-173">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5ec77-174">MOF</span><span class="sxs-lookup"><span data-stu-id="5ec77-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ec77-175"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5ec77-175"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ec77-176">DLL</span><span class="sxs-lookup"><span data-stu-id="5ec77-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ec77-177"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ec77-177"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ec77-178">Consulte também</span><span class="sxs-lookup"><span data-stu-id="5ec77-178">See also</span></span>

<dl> <dt>

<span data-ttu-id="5ec77-179">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5ec77-179">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5ec77-180">**\_Serviço Win32**</span><span class="sxs-lookup"><span data-stu-id="5ec77-180">**Win32\_Service**</span></span>](win32-service.md)
</dt> </dl>

 


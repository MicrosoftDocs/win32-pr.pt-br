---
description: Coloca o serviço representado pelo \_ objeto SystemDriver do Win32 no estado parado.
ms.assetid: 0fa8ef44-39eb-448e-8d33-38a5af9a0c13
ms.tgt_platform: multiple
title: Método StopService da classe Win32_SystemDriver (Sdoias. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bb45a414ea9cc7198487dbb61d122722816f4728
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920359"
---
# <a name="stopservice-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="ae1b6-103">Método StopService da classe do \_ SystemDriver Win32</span><span class="sxs-lookup"><span data-stu-id="ae1b6-103">StopService method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="ae1b6-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **StopService** coloca o serviço representado pelo [**objeto \_ systemdrive do Win32**](win32-systemdriver.md) no estado parado.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-104">The **StopService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method places the service represented by the [**Win32\_SystemDriver**](win32-systemdriver.md) object in the stopped state.</span></span>

<span data-ttu-id="ae1b6-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="ae1b6-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ae1b6-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ae1b6-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ae1b6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ae1b6-107">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="ae1b6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ae1b6-108">Parameters</span></span>

<span data-ttu-id="ae1b6-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ae1b6-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ae1b6-110">Return value</span></span>

<span data-ttu-id="ae1b6-111">Retorna um valor de 0 (zero) se o serviço foi interrompido com êxito, 1 (um) se a solicitação não tiver suporte e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-111">Returns a value of 0 (zero) if the service was successfully stopped, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="ae1b6-112">**0**</span><span class="sxs-lookup"><span data-stu-id="ae1b6-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="ae1b6-113">A solicitação foi aceita.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-113">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="ae1b6-114">**1**</span><span class="sxs-lookup"><span data-stu-id="ae1b6-114">**1**</span></span>
</dt> <dd>

<span data-ttu-id="ae1b6-115">A solicitação não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-115">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ae1b6-116">**2**</span><span class="sxs-lookup"><span data-stu-id="ae1b6-116">**2**</span></span>
</dt> <dd>

<span data-ttu-id="ae1b6-117">O usuário não tinha o acesso necessário.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-117">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="ae1b6-118">**3**</span><span class="sxs-lookup"><span data-stu-id="ae1b6-118">**3**</span></span>
</dt> <dd>

<span data-ttu-id="ae1b6-119">O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-119">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="ae1b6-120">**4**</span><span class="sxs-lookup"><span data-stu-id="ae1b6-120">**4**</span></span>
</dt> <dd>

<span data-ttu-id="ae1b6-121">O código de controle pedido não é válido ou é inaceitável para o serviço.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-121">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="ae1b6-122">**5**</span><span class="sxs-lookup"><span data-stu-id="ae1b6-122">**5**</span></span>
</dt> <dd>

<span data-ttu-id="ae1b6-123">O código de controle solicitado não pode ser enviado ao serviço porque o estado do serviço ([**Win32 \_ BaseService**](win32-baseservice.md).\*\*\*\* A propriedade State) é igual a 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-123">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="ae1b6-124">**6**</span><span class="sxs-lookup"><span data-stu-id="ae1b6-124">**6**</span></span>
</dt> <dd>

<span data-ttu-id="ae1b6-125">O serviço não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-125">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="ae1b6-126">**7**</span><span class="sxs-lookup"><span data-stu-id="ae1b6-126">**7**</span></span>
</dt> <dd>

<span data-ttu-id="ae1b6-127">O serviço não respondeu à solicitação de início em um tempo oportuno.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-127">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="ae1b6-128">**8**</span><span class="sxs-lookup"><span data-stu-id="ae1b6-128">**8**</span></span>
</dt> <dd>

<span data-ttu-id="ae1b6-129">Uma falha desconhecida ocorreu na inicialização do serviço.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-129">An unknown failure occurred when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="ae1b6-130">**9**</span><span class="sxs-lookup"><span data-stu-id="ae1b6-130">**9**</span></span>
</dt> <dd>

<span data-ttu-id="ae1b6-131">O caminho do diretório para o arquivo executável do serviço não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-131">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="ae1b6-132">**10**</span><span class="sxs-lookup"><span data-stu-id="ae1b6-132">**10**</span></span>
</dt> <dd>

<span data-ttu-id="ae1b6-133">O serviço já está em execução.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-133">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="ae1b6-134">**11**</span><span class="sxs-lookup"><span data-stu-id="ae1b6-134">**11**</span></span>
</dt> <dd>

<span data-ttu-id="ae1b6-135">O banco de dados para adicionar um serviço novo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-135">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="ae1b6-136">**12**</span><span class="sxs-lookup"><span data-stu-id="ae1b6-136">**12**</span></span>
</dt> <dd>

<span data-ttu-id="ae1b6-137">Uma dependência para a qual esse serviço depende foi removida do sistema.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-137">A dependency for which this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ae1b6-138">**13**</span><span class="sxs-lookup"><span data-stu-id="ae1b6-138">**13**</span></span>
</dt> <dd>

<span data-ttu-id="ae1b6-139">O serviço não localizou o serviço necessário em um serviço dependente.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-139">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="ae1b6-140">**14**</span><span class="sxs-lookup"><span data-stu-id="ae1b6-140">**14**</span></span>
</dt> <dd>

<span data-ttu-id="ae1b6-141">O serviço foi desabilitado do sistema.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-141">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ae1b6-142">**15**</span><span class="sxs-lookup"><span data-stu-id="ae1b6-142">**15**</span></span>
</dt> <dd>

<span data-ttu-id="ae1b6-143">O serviço não tem a autenticação correta para ser executado no sistema.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-143">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="ae1b6-144">**16**</span><span class="sxs-lookup"><span data-stu-id="ae1b6-144">**16**</span></span>
</dt> <dd>

<span data-ttu-id="ae1b6-145">Este serviço está sendo removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-145">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ae1b6-146">**17**</span><span class="sxs-lookup"><span data-stu-id="ae1b6-146">**17**</span></span>
</dt> <dd>

<span data-ttu-id="ae1b6-147">Não há nenhum thread de execução para o serviço.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-147">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="ae1b6-148">**anos**</span><span class="sxs-lookup"><span data-stu-id="ae1b6-148">**18**</span></span>
</dt> <dd>

<span data-ttu-id="ae1b6-149">Há dependências circulares quando o serviço é iniciado.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-149">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="ae1b6-150">**aprimora**</span><span class="sxs-lookup"><span data-stu-id="ae1b6-150">**19**</span></span>
</dt> <dd>

<span data-ttu-id="ae1b6-151">Há um serviço em execução com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-151">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="ae1b6-152">**20**</span><span class="sxs-lookup"><span data-stu-id="ae1b6-152">**20**</span></span>
</dt> <dd>

<span data-ttu-id="ae1b6-153">Há caracteres inválidos no nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-153">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="ae1b6-154">**Abril**</span><span class="sxs-lookup"><span data-stu-id="ae1b6-154">**21**</span></span>
</dt> <dd>

<span data-ttu-id="ae1b6-155">Parâmetros inválidos foram passados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-155">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="ae1b6-156">**22**</span><span class="sxs-lookup"><span data-stu-id="ae1b6-156">**22**</span></span>
</dt> <dd>

<span data-ttu-id="ae1b6-157">A conta na qual esse serviço deve ser executado é inválida ou não tem as permissões para executar o serviço.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-157">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="ae1b6-158">**23**</span><span class="sxs-lookup"><span data-stu-id="ae1b6-158">**23**</span></span>
</dt> <dd>

<span data-ttu-id="ae1b6-159">O serviço existe no banco de dados de serviços disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-159">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ae1b6-160">**24**</span><span class="sxs-lookup"><span data-stu-id="ae1b6-160">**24**</span></span>
</dt> <dd>

<span data-ttu-id="ae1b6-161">O serviço está pausado atualmente no sistema.</span><span class="sxs-lookup"><span data-stu-id="ae1b6-161">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="ae1b6-162">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ae1b6-162">Examples</span></span>

<span data-ttu-id="ae1b6-163">O código do PowerShell a seguir interrompe o serviço "classe de impressora USB da Microsoft".</span><span class="sxs-lookup"><span data-stu-id="ae1b6-163">The following PowerShell code stops the "Microsoft USB Printer class" service.</span></span>


```PowerShell
$usbPrintDriver = Get-WmiObject -query "SELECT * FROM Win32_SystemDriver WHERE Name = 'usbprint'"
$Return = $usbPrintDriver.StopService()
"Stop Service Called. Return value is " + $return.ReturnValue + "."
"To figure out what this means, go look at the docs above this code snippet."
```



## <a name="requirements"></a><span data-ttu-id="ae1b6-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae1b6-164">Requirements</span></span>



| <span data-ttu-id="ae1b6-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae1b6-165">Requirement</span></span> | <span data-ttu-id="ae1b6-166">Valor</span><span class="sxs-lookup"><span data-stu-id="ae1b6-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae1b6-167">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae1b6-167">Minimum supported client</span></span><br/> | <span data-ttu-id="ae1b6-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ae1b6-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ae1b6-169">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae1b6-169">Minimum supported server</span></span><br/> | <span data-ttu-id="ae1b6-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ae1b6-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ae1b6-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="ae1b6-171">Namespace</span></span><br/>                | <span data-ttu-id="ae1b6-172">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ae1b6-172">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ae1b6-173">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ae1b6-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae1b6-174"><dt>Sdoias. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae1b6-174"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="ae1b6-175">MOF</span><span class="sxs-lookup"><span data-stu-id="ae1b6-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae1b6-176"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ae1b6-176"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ae1b6-177">DLL</span><span class="sxs-lookup"><span data-stu-id="ae1b6-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae1b6-178"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae1b6-178"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae1b6-179">Confira também</span><span class="sxs-lookup"><span data-stu-id="ae1b6-179">See also</span></span>

<dl> <dt>

<span data-ttu-id="ae1b6-180">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ae1b6-180">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ae1b6-181">**Systemdrive do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="ae1b6-181">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 


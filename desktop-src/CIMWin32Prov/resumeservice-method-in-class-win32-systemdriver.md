---
description: Tenta posicionar o serviço gerenciado pelo driver do sistema no estado retomado.
ms.assetid: 16bacf06-4236-4d58-9b09-cb86bb73d78a
ms.tgt_platform: multiple
title: Método ResumeService da classe Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.ResumeService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d326fcd0a3bc9801f5e214cdc8740170cf1f1cf8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920216"
---
# <a name="resumeservice-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="94d15-103">Método ResumeService da \_ classe SystemDriver Win32</span><span class="sxs-lookup"><span data-stu-id="94d15-103">ResumeService method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="94d15-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ResumeService** tenta posicionar o serviço gerenciado pelo driver do sistema no estado retomado.</span><span class="sxs-lookup"><span data-stu-id="94d15-104">The **ResumeService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the service managed by the system driver in the resumed state.</span></span>

<span data-ttu-id="94d15-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="94d15-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="94d15-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="94d15-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="94d15-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="94d15-107">Syntax</span></span>


```mof
uint32 ResumeService();
```



## <a name="parameters"></a><span data-ttu-id="94d15-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="94d15-108">Parameters</span></span>

<span data-ttu-id="94d15-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="94d15-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="94d15-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="94d15-110">Return value</span></span>

<span data-ttu-id="94d15-111">Retorna um valor de 0 (zero) se a solicitação **ResumeService** tiver sido aceita, 1 (uma) se a solicitação não tiver suporte e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="94d15-111">Returns a value of 0 (zero) if the **ResumeService** request was accepted, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="94d15-112">**0**</span><span class="sxs-lookup"><span data-stu-id="94d15-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="94d15-113">A solicitação foi aceita.</span><span class="sxs-lookup"><span data-stu-id="94d15-113">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="94d15-114">**1**</span><span class="sxs-lookup"><span data-stu-id="94d15-114">**1**</span></span>
</dt> <dd>

<span data-ttu-id="94d15-115">A solicitação não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="94d15-115">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="94d15-116">**2**</span><span class="sxs-lookup"><span data-stu-id="94d15-116">**2**</span></span>
</dt> <dd>

<span data-ttu-id="94d15-117">O usuário não tinha o acesso necessário.</span><span class="sxs-lookup"><span data-stu-id="94d15-117">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="94d15-118">**3**</span><span class="sxs-lookup"><span data-stu-id="94d15-118">**3**</span></span>
</dt> <dd>

<span data-ttu-id="94d15-119">O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.</span><span class="sxs-lookup"><span data-stu-id="94d15-119">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="94d15-120">**4**</span><span class="sxs-lookup"><span data-stu-id="94d15-120">**4**</span></span>
</dt> <dd>

<span data-ttu-id="94d15-121">O código de controle pedido não é válido ou é inaceitável para o serviço.</span><span class="sxs-lookup"><span data-stu-id="94d15-121">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="94d15-122">**5**</span><span class="sxs-lookup"><span data-stu-id="94d15-122">**5**</span></span>
</dt> <dd>

<span data-ttu-id="94d15-123">O código de controle solicitado não pode ser enviado ao serviço porque o estado do serviço ([**Win32 \_ BaseService**](win32-baseservice.md).\*\*\*\* A propriedade State) é igual a 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="94d15-123">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="94d15-124">**6**</span><span class="sxs-lookup"><span data-stu-id="94d15-124">**6**</span></span>
</dt> <dd>

<span data-ttu-id="94d15-125">O serviço não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="94d15-125">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="94d15-126">**7**</span><span class="sxs-lookup"><span data-stu-id="94d15-126">**7**</span></span>
</dt> <dd>

<span data-ttu-id="94d15-127">O serviço não respondeu à solicitação de início em um tempo oportuno.</span><span class="sxs-lookup"><span data-stu-id="94d15-127">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="94d15-128">**8**</span><span class="sxs-lookup"><span data-stu-id="94d15-128">**8**</span></span>
</dt> <dd>

<span data-ttu-id="94d15-129">Uma falha desconhecida ocorreu na inicialização do serviço.</span><span class="sxs-lookup"><span data-stu-id="94d15-129">An unknown failure occurred when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="94d15-130">**9**</span><span class="sxs-lookup"><span data-stu-id="94d15-130">**9**</span></span>
</dt> <dd>

<span data-ttu-id="94d15-131">O caminho do diretório para o arquivo executável do serviço não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="94d15-131">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="94d15-132">**10**</span><span class="sxs-lookup"><span data-stu-id="94d15-132">**10**</span></span>
</dt> <dd>

<span data-ttu-id="94d15-133">O serviço já está em execução.</span><span class="sxs-lookup"><span data-stu-id="94d15-133">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="94d15-134">**11**</span><span class="sxs-lookup"><span data-stu-id="94d15-134">**11**</span></span>
</dt> <dd>

<span data-ttu-id="94d15-135">O banco de dados para adicionar um serviço novo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="94d15-135">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="94d15-136">**12**</span><span class="sxs-lookup"><span data-stu-id="94d15-136">**12**</span></span>
</dt> <dd>

<span data-ttu-id="94d15-137">Uma dependência para a qual esse serviço depende foi removida do sistema.</span><span class="sxs-lookup"><span data-stu-id="94d15-137">A dependency for which this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="94d15-138">**13**</span><span class="sxs-lookup"><span data-stu-id="94d15-138">**13**</span></span>
</dt> <dd>

<span data-ttu-id="94d15-139">O serviço não localizou o serviço necessário em um serviço dependente.</span><span class="sxs-lookup"><span data-stu-id="94d15-139">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="94d15-140">**14**</span><span class="sxs-lookup"><span data-stu-id="94d15-140">**14**</span></span>
</dt> <dd>

<span data-ttu-id="94d15-141">O serviço foi desabilitado do sistema.</span><span class="sxs-lookup"><span data-stu-id="94d15-141">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="94d15-142">**15**</span><span class="sxs-lookup"><span data-stu-id="94d15-142">**15**</span></span>
</dt> <dd>

<span data-ttu-id="94d15-143">O serviço não tem a autenticação correta para ser executado no sistema.</span><span class="sxs-lookup"><span data-stu-id="94d15-143">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="94d15-144">**16**</span><span class="sxs-lookup"><span data-stu-id="94d15-144">**16**</span></span>
</dt> <dd>

<span data-ttu-id="94d15-145">Este serviço está sendo removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="94d15-145">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="94d15-146">**17**</span><span class="sxs-lookup"><span data-stu-id="94d15-146">**17**</span></span>
</dt> <dd>

<span data-ttu-id="94d15-147">Não há nenhum thread de execução para o serviço.</span><span class="sxs-lookup"><span data-stu-id="94d15-147">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="94d15-148">**anos**</span><span class="sxs-lookup"><span data-stu-id="94d15-148">**18**</span></span>
</dt> <dd>

<span data-ttu-id="94d15-149">Há dependências circulares quando o serviço é iniciado.</span><span class="sxs-lookup"><span data-stu-id="94d15-149">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="94d15-150">**aprimora**</span><span class="sxs-lookup"><span data-stu-id="94d15-150">**19**</span></span>
</dt> <dd>

<span data-ttu-id="94d15-151">Há um serviço em execução com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="94d15-151">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="94d15-152">**20**</span><span class="sxs-lookup"><span data-stu-id="94d15-152">**20**</span></span>
</dt> <dd>

<span data-ttu-id="94d15-153">Há caracteres inválidos no nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="94d15-153">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="94d15-154">**Abril**</span><span class="sxs-lookup"><span data-stu-id="94d15-154">**21**</span></span>
</dt> <dd>

<span data-ttu-id="94d15-155">Parâmetros inválidos foram passados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="94d15-155">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="94d15-156">**22**</span><span class="sxs-lookup"><span data-stu-id="94d15-156">**22**</span></span>
</dt> <dd>

<span data-ttu-id="94d15-157">A conta na qual esse serviço deve ser executado é inválida ou não tem as permissões para executar o serviço.</span><span class="sxs-lookup"><span data-stu-id="94d15-157">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="94d15-158">**23**</span><span class="sxs-lookup"><span data-stu-id="94d15-158">**23**</span></span>
</dt> <dd>

<span data-ttu-id="94d15-159">O serviço existe no banco de dados de serviços disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="94d15-159">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="94d15-160">**24**</span><span class="sxs-lookup"><span data-stu-id="94d15-160">**24**</span></span>
</dt> <dd>

<span data-ttu-id="94d15-161">O serviço está pausado atualmente no sistema.</span><span class="sxs-lookup"><span data-stu-id="94d15-161">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="94d15-162">Exemplos</span><span class="sxs-lookup"><span data-stu-id="94d15-162">Examples</span></span>

<span data-ttu-id="94d15-163">O código do PowerShell a seguir tenta retomar o serviço "classe de impressora USB da Microsoft".</span><span class="sxs-lookup"><span data-stu-id="94d15-163">The following PowerShell code attempts to resume the "Microsoft USB Printer class" service.</span></span>


```PowerShell
$usbPrintDriver = Get-WmiObject -query "SELECT * FROM Win32_SystemDriver WHERE Name = 'usbprint'"
$Return = $usbPrintDriver.ResumeService()
"Resume Service Called. The return value is " + $return.ReturnValue + "."
"To figure out what this means, go look at the docs above this code snippet."
```



## <a name="requirements"></a><span data-ttu-id="94d15-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94d15-164">Requirements</span></span>



| <span data-ttu-id="94d15-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="94d15-165">Requirement</span></span> | <span data-ttu-id="94d15-166">Valor</span><span class="sxs-lookup"><span data-stu-id="94d15-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94d15-167">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94d15-167">Minimum supported client</span></span><br/> | <span data-ttu-id="94d15-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94d15-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="94d15-169">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94d15-169">Minimum supported server</span></span><br/> | <span data-ttu-id="94d15-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94d15-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="94d15-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="94d15-171">Namespace</span></span><br/>                | <span data-ttu-id="94d15-172">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="94d15-172">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="94d15-173">MOF</span><span class="sxs-lookup"><span data-stu-id="94d15-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94d15-174"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="94d15-174"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="94d15-175">DLL</span><span class="sxs-lookup"><span data-stu-id="94d15-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94d15-176"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94d15-176"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94d15-177">Confira também</span><span class="sxs-lookup"><span data-stu-id="94d15-177">See also</span></span>

<dl> <dt>

<span data-ttu-id="94d15-178">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="94d15-178">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="94d15-179">**Systemdrive do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="94d15-179">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 


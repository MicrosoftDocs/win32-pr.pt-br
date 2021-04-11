---
description: Tenta posicionar o serviço gerenciado pelo driver do sistema em seu estado de inicialização.
ms.assetid: 3f9d29aa-b549-4a55-be9c-01fad4932fe6
ms.tgt_platform: multiple
title: Método StartService da classe Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2c189d9b5f24a3ccc803a588abb94337ee65a1da
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164041"
---
# <a name="startservice-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="a7140-103">Método StartService da \_ classe systemdrive do Win32</span><span class="sxs-lookup"><span data-stu-id="a7140-103">StartService method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="a7140-104">O método **StartService** tenta posicionar o serviço gerenciado pelo driver do sistema em seu estado de inicialização.</span><span class="sxs-lookup"><span data-stu-id="a7140-104">The **StartService** method attempts to place the service managed by the system driver into its startup state.</span></span>

<span data-ttu-id="a7140-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="a7140-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a7140-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a7140-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a7140-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a7140-107">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="a7140-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7140-108">Parameters</span></span>

<span data-ttu-id="a7140-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a7140-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a7140-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a7140-110">Return value</span></span>

<span data-ttu-id="a7140-111">Retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a7140-111">Returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a7140-112">**0**</span><span class="sxs-lookup"><span data-stu-id="a7140-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="a7140-113">A solicitação foi aceita.</span><span class="sxs-lookup"><span data-stu-id="a7140-113">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="a7140-114">**1**</span><span class="sxs-lookup"><span data-stu-id="a7140-114">**1**</span></span>
</dt> <dd>

<span data-ttu-id="a7140-115">A solicitação não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="a7140-115">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="a7140-116">**2**</span><span class="sxs-lookup"><span data-stu-id="a7140-116">**2**</span></span>
</dt> <dd>

<span data-ttu-id="a7140-117">O usuário não tinha o acesso necessário.</span><span class="sxs-lookup"><span data-stu-id="a7140-117">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="a7140-118">**3**</span><span class="sxs-lookup"><span data-stu-id="a7140-118">**3**</span></span>
</dt> <dd>

<span data-ttu-id="a7140-119">O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.</span><span class="sxs-lookup"><span data-stu-id="a7140-119">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="a7140-120">**4**</span><span class="sxs-lookup"><span data-stu-id="a7140-120">**4**</span></span>
</dt> <dd>

<span data-ttu-id="a7140-121">O código de controle pedido não é válido ou é inaceitável para o serviço.</span><span class="sxs-lookup"><span data-stu-id="a7140-121">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="a7140-122">**5**</span><span class="sxs-lookup"><span data-stu-id="a7140-122">**5**</span></span>
</dt> <dd>

<span data-ttu-id="a7140-123">O código de controle solicitado não pode ser enviado ao serviço porque o estado do serviço ([**Win32 \_ BaseService**](win32-baseservice.md).\*\*\*\* A propriedade State) é igual a 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="a7140-123">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="a7140-124">**6**</span><span class="sxs-lookup"><span data-stu-id="a7140-124">**6**</span></span>
</dt> <dd>

<span data-ttu-id="a7140-125">O serviço não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="a7140-125">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="a7140-126">**7**</span><span class="sxs-lookup"><span data-stu-id="a7140-126">**7**</span></span>
</dt> <dd>

<span data-ttu-id="a7140-127">O serviço não respondeu à solicitação de início em um tempo oportuno.</span><span class="sxs-lookup"><span data-stu-id="a7140-127">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="a7140-128">**8**</span><span class="sxs-lookup"><span data-stu-id="a7140-128">**8**</span></span>
</dt> <dd>

<span data-ttu-id="a7140-129">Uma falha desconhecida ocorreu na inicialização do serviço.</span><span class="sxs-lookup"><span data-stu-id="a7140-129">An unknown failure occurred when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="a7140-130">**9**</span><span class="sxs-lookup"><span data-stu-id="a7140-130">**9**</span></span>
</dt> <dd>

<span data-ttu-id="a7140-131">O caminho do diretório para o arquivo executável do serviço não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="a7140-131">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="a7140-132">**10**</span><span class="sxs-lookup"><span data-stu-id="a7140-132">**10**</span></span>
</dt> <dd>

<span data-ttu-id="a7140-133">O serviço já está em execução.</span><span class="sxs-lookup"><span data-stu-id="a7140-133">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="a7140-134">**11**</span><span class="sxs-lookup"><span data-stu-id="a7140-134">**11**</span></span>
</dt> <dd>

<span data-ttu-id="a7140-135">O banco de dados para adicionar um serviço novo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="a7140-135">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="a7140-136">**12**</span><span class="sxs-lookup"><span data-stu-id="a7140-136">**12**</span></span>
</dt> <dd>

<span data-ttu-id="a7140-137">Uma dependência para a qual esse serviço depende foi removida do sistema.</span><span class="sxs-lookup"><span data-stu-id="a7140-137">A dependency for which this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a7140-138">**13**</span><span class="sxs-lookup"><span data-stu-id="a7140-138">**13**</span></span>
</dt> <dd>

<span data-ttu-id="a7140-139">O serviço não localizou o serviço necessário em um serviço dependente.</span><span class="sxs-lookup"><span data-stu-id="a7140-139">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="a7140-140">**14**</span><span class="sxs-lookup"><span data-stu-id="a7140-140">**14**</span></span>
</dt> <dd>

<span data-ttu-id="a7140-141">O serviço foi desabilitado do sistema.</span><span class="sxs-lookup"><span data-stu-id="a7140-141">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a7140-142">**15**</span><span class="sxs-lookup"><span data-stu-id="a7140-142">**15**</span></span>
</dt> <dd>

<span data-ttu-id="a7140-143">O serviço não tem a autenticação correta para ser executado no sistema.</span><span class="sxs-lookup"><span data-stu-id="a7140-143">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="a7140-144">**16**</span><span class="sxs-lookup"><span data-stu-id="a7140-144">**16**</span></span>
</dt> <dd>

<span data-ttu-id="a7140-145">Este serviço está sendo removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="a7140-145">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a7140-146">**17**</span><span class="sxs-lookup"><span data-stu-id="a7140-146">**17**</span></span>
</dt> <dd>

<span data-ttu-id="a7140-147">Não há nenhum thread de execução para o serviço.</span><span class="sxs-lookup"><span data-stu-id="a7140-147">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="a7140-148">**anos**</span><span class="sxs-lookup"><span data-stu-id="a7140-148">**18**</span></span>
</dt> <dd>

<span data-ttu-id="a7140-149">Há dependências circulares quando o serviço é iniciado.</span><span class="sxs-lookup"><span data-stu-id="a7140-149">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="a7140-150">**aprimora**</span><span class="sxs-lookup"><span data-stu-id="a7140-150">**19**</span></span>
</dt> <dd>

<span data-ttu-id="a7140-151">Há um serviço em execução com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="a7140-151">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="a7140-152">**20**</span><span class="sxs-lookup"><span data-stu-id="a7140-152">**20**</span></span>
</dt> <dd>

<span data-ttu-id="a7140-153">Há caracteres inválidos no nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="a7140-153">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="a7140-154">**Abril**</span><span class="sxs-lookup"><span data-stu-id="a7140-154">**21**</span></span>
</dt> <dd>

<span data-ttu-id="a7140-155">Parâmetros inválidos foram passados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="a7140-155">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="a7140-156">**22**</span><span class="sxs-lookup"><span data-stu-id="a7140-156">**22**</span></span>
</dt> <dd>

<span data-ttu-id="a7140-157">A conta na qual esse serviço deve ser executado é inválida ou não tem as permissões para executar o serviço.</span><span class="sxs-lookup"><span data-stu-id="a7140-157">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="a7140-158">**23**</span><span class="sxs-lookup"><span data-stu-id="a7140-158">**23**</span></span>
</dt> <dd>

<span data-ttu-id="a7140-159">O serviço existe no banco de dados de serviços disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="a7140-159">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a7140-160">**24**</span><span class="sxs-lookup"><span data-stu-id="a7140-160">**24**</span></span>
</dt> <dd>

<span data-ttu-id="a7140-161">O serviço está pausado atualmente no sistema.</span><span class="sxs-lookup"><span data-stu-id="a7140-161">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="a7140-162">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a7140-162">Examples</span></span>

<span data-ttu-id="a7140-163">O código do PowerShell a seguir inicia o serviço "classe de impressora USB da Microsoft".</span><span class="sxs-lookup"><span data-stu-id="a7140-163">The following PowerShell code starts the "Microsoft USB Printer class" service.</span></span>


```PowerShell
$usbPrintDriver = Get-WmiObject -query "SELECT * FROM Win32_SystemDriver WHERE Name = 'usbprint'"
$Return = $usbPrintDriver.StartService()
"Start Service Called. Return value is " + $return.ReturnValue + "."
"To figure out what this means, go look at the docs above this code snippet."
```



## <a name="requirements"></a><span data-ttu-id="a7140-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7140-164">Requirements</span></span>



| <span data-ttu-id="a7140-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7140-165">Requirement</span></span> | <span data-ttu-id="a7140-166">Valor</span><span class="sxs-lookup"><span data-stu-id="a7140-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7140-167">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a7140-167">Minimum supported client</span></span><br/> | <span data-ttu-id="a7140-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a7140-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a7140-169">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a7140-169">Minimum supported server</span></span><br/> | <span data-ttu-id="a7140-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a7140-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a7140-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="a7140-171">Namespace</span></span><br/>                | <span data-ttu-id="a7140-172">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a7140-172">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a7140-173">MOF</span><span class="sxs-lookup"><span data-stu-id="a7140-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a7140-174"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a7140-174"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a7140-175">DLL</span><span class="sxs-lookup"><span data-stu-id="a7140-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7140-176"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7140-176"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7140-177">Confira também</span><span class="sxs-lookup"><span data-stu-id="a7140-177">See also</span></span>

<dl> <dt>

<span data-ttu-id="a7140-178">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a7140-178">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a7140-179">**Systemdrive do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="a7140-179">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 


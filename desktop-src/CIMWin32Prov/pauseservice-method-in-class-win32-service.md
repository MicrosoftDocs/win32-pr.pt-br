---
description: Método PauseService da classe Win32_Service (provedores WMI CIMWin32) – tenta colocar o serviço no estado pausado.
ms.assetid: 5382457e-7f9c-48a5-9262-b815a1a4a605
ms.tgt_platform: multiple
title: Método PauseService da classe Win32_Service (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.PauseService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7654feea410564137e98861c4c0b5de2b5e7192e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096944"
---
# <a name="pauseservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="3c375-103">Método PauseService da classe Win32_Service (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="3c375-103">PauseService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="3c375-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **PauseService** tenta colocar o serviço no estado pausado.</span><span class="sxs-lookup"><span data-stu-id="3c375-104">The **PauseService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the service in the paused state.</span></span>

<span data-ttu-id="3c375-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="3c375-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3c375-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3c375-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3c375-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3c375-107">Syntax</span></span>


```mof
uint32 PauseService();
```



## <a name="parameters"></a><span data-ttu-id="3c375-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3c375-108">Parameters</span></span>

<span data-ttu-id="3c375-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="3c375-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3c375-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="3c375-110">Return value</span></span>

<span data-ttu-id="3c375-111">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="3c375-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="3c375-112">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="3c375-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="3c375-113">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="3c375-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="3c375-114">**0**</span><span class="sxs-lookup"><span data-stu-id="3c375-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="3c375-115">A solicitação foi aceita.</span><span class="sxs-lookup"><span data-stu-id="3c375-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="3c375-116">**1**</span><span class="sxs-lookup"><span data-stu-id="3c375-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="3c375-117">A solicitação não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="3c375-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="3c375-118">**2**</span><span class="sxs-lookup"><span data-stu-id="3c375-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="3c375-119">O usuário não tinha o acesso necessário.</span><span class="sxs-lookup"><span data-stu-id="3c375-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="3c375-120">**3**</span><span class="sxs-lookup"><span data-stu-id="3c375-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="3c375-121">O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.</span><span class="sxs-lookup"><span data-stu-id="3c375-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="3c375-122">**4**</span><span class="sxs-lookup"><span data-stu-id="3c375-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="3c375-123">O código de controle pedido não é válido ou é inaceitável para o serviço.</span><span class="sxs-lookup"><span data-stu-id="3c375-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="3c375-124">**5**</span><span class="sxs-lookup"><span data-stu-id="3c375-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="3c375-125">O código de controle solicitado não pode ser enviado ao serviço porque o estado do serviço ([**Win32 \_ BaseService**](win32-baseservice.md).\*\*\*\* A propriedade State) é igual a 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="3c375-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="3c375-126">**6**</span><span class="sxs-lookup"><span data-stu-id="3c375-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="3c375-127">O serviço não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="3c375-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="3c375-128">**7**</span><span class="sxs-lookup"><span data-stu-id="3c375-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="3c375-129">O serviço não respondeu à solicitação de início em um tempo oportuno.</span><span class="sxs-lookup"><span data-stu-id="3c375-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="3c375-130">**8**</span><span class="sxs-lookup"><span data-stu-id="3c375-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="3c375-131">Falha desconhecida ao iniciar o serviço.</span><span class="sxs-lookup"><span data-stu-id="3c375-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="3c375-132">**9**</span><span class="sxs-lookup"><span data-stu-id="3c375-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="3c375-133">O caminho do diretório para o arquivo executável do serviço não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="3c375-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="3c375-134">**10**</span><span class="sxs-lookup"><span data-stu-id="3c375-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="3c375-135">O serviço já está em execução.</span><span class="sxs-lookup"><span data-stu-id="3c375-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="3c375-136">**11**</span><span class="sxs-lookup"><span data-stu-id="3c375-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="3c375-137">O banco de dados para adicionar um serviço novo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="3c375-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="3c375-138">**12**</span><span class="sxs-lookup"><span data-stu-id="3c375-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="3c375-139">Uma dependência da qual esse serviço depende foi removida do sistema.</span><span class="sxs-lookup"><span data-stu-id="3c375-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3c375-140">**13**</span><span class="sxs-lookup"><span data-stu-id="3c375-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="3c375-141">O serviço não localizou o serviço necessário em um serviço dependente.</span><span class="sxs-lookup"><span data-stu-id="3c375-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="3c375-142">**14**</span><span class="sxs-lookup"><span data-stu-id="3c375-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="3c375-143">O serviço foi desabilitado do sistema.</span><span class="sxs-lookup"><span data-stu-id="3c375-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3c375-144">**15**</span><span class="sxs-lookup"><span data-stu-id="3c375-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="3c375-145">O serviço não tem a autenticação correta para ser executado no sistema.</span><span class="sxs-lookup"><span data-stu-id="3c375-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="3c375-146">**16**</span><span class="sxs-lookup"><span data-stu-id="3c375-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="3c375-147">Este serviço está sendo removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="3c375-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3c375-148">**17**</span><span class="sxs-lookup"><span data-stu-id="3c375-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="3c375-149">O serviço não tem nenhum thread de execução.</span><span class="sxs-lookup"><span data-stu-id="3c375-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="3c375-150">**anos**</span><span class="sxs-lookup"><span data-stu-id="3c375-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="3c375-151">O serviço tem dependências circulares quando é iniciado.</span><span class="sxs-lookup"><span data-stu-id="3c375-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="3c375-152">**aprimora**</span><span class="sxs-lookup"><span data-stu-id="3c375-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="3c375-153">Um serviço está sendo executado com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="3c375-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="3c375-154">**20**</span><span class="sxs-lookup"><span data-stu-id="3c375-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="3c375-155">O nome do serviço tem caracteres inválidos.</span><span class="sxs-lookup"><span data-stu-id="3c375-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="3c375-156">**Abril**</span><span class="sxs-lookup"><span data-stu-id="3c375-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="3c375-157">Parâmetros inválidos foram passados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="3c375-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="3c375-158">**22**</span><span class="sxs-lookup"><span data-stu-id="3c375-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="3c375-159">A conta sob a qual este serviço é executado é inválida ou não tem as permissões para executar o serviço.</span><span class="sxs-lookup"><span data-stu-id="3c375-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="3c375-160">**23**</span><span class="sxs-lookup"><span data-stu-id="3c375-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="3c375-161">O serviço existe no banco de dados de serviços disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="3c375-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3c375-162">**24**</span><span class="sxs-lookup"><span data-stu-id="3c375-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="3c375-163">O serviço está pausado atualmente no sistema.</span><span class="sxs-lookup"><span data-stu-id="3c375-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3c375-164">Comentários</span><span class="sxs-lookup"><span data-stu-id="3c375-164">Remarks</span></span>

<span data-ttu-id="3c375-165">Depois de determinar quais serviços podem ser interrompidos ou pausados, você pode usar os métodos [**StopService**](stopservice-method-in-class-win32-service.md) e [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md) para parar e pausar serviços.</span><span class="sxs-lookup"><span data-stu-id="3c375-165">After you have determined which services can be stopped or paused, you can use the [**StopService**](stopservice-method-in-class-win32-service.md) and [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md) methods to stop and pause services.</span></span> <span data-ttu-id="3c375-166">A decisão de interromper um serviço em vez de pausá-lo, ou vice-versa, depende de vários fatores, incluindo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="3c375-166">The decision to stop a service rather than pause it, or vice versa, depends on several factors, including the following:</span></span>

-   <span data-ttu-id="3c375-167">O serviço é capaz de ser pausado?</span><span class="sxs-lookup"><span data-stu-id="3c375-167">Is the service capable of being paused?</span></span> <span data-ttu-id="3c375-168">Caso contrário, sua única opção é parar o serviço.</span><span class="sxs-lookup"><span data-stu-id="3c375-168">If not, your only option is the stop the service.</span></span>
-   <span data-ttu-id="3c375-169">Você precisa continuar tratando as solicitações do cliente para qualquer pessoa já conectada ao serviço?</span><span class="sxs-lookup"><span data-stu-id="3c375-169">Do you need to continue handling client requests for anyone already connected to the service?</span></span> <span data-ttu-id="3c375-170">Nesse caso, pausar um serviço geralmente permite que ele manipule clientes existentes enquanto nega acesso a novos clientes.</span><span class="sxs-lookup"><span data-stu-id="3c375-170">If so, pausing a service typically allows it to handle existing clients while denying access to new clients.</span></span> <span data-ttu-id="3c375-171">Por outro lado, quando você interrompe um serviço, todos os clientes são imediatamente desconectados.</span><span class="sxs-lookup"><span data-stu-id="3c375-171">By contrast, when you stop a service, all clients are immediately disconnected.</span></span>
-   <span data-ttu-id="3c375-172">Você precisa reconfigurar um serviço e fazer com que as alterações entrem em vigor imediatamente?</span><span class="sxs-lookup"><span data-stu-id="3c375-172">Do you need to reconfigure a service and have the changes take effect immediately?</span></span> <span data-ttu-id="3c375-173">Embora as propriedades do serviço possam ser alteradas enquanto um serviço é pausado, a maioria delas não tem efeito até que o serviço seja realmente interrompido e reiniciado.</span><span class="sxs-lookup"><span data-stu-id="3c375-173">Although service properties can be changed while a service is paused, most of them do not take effect until the service is actually stopped and restarted.</span></span>

<span data-ttu-id="3c375-174">O código de script necessário para interromper um serviço é quase idêntico ao código necessário para pausar o serviço.</span><span class="sxs-lookup"><span data-stu-id="3c375-174">The scripting code required to stop a service is almost identical to the code required to pause the service.</span></span>

## <a name="examples"></a><span data-ttu-id="3c375-175">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3c375-175">Examples</span></span>

<span data-ttu-id="3c375-176">Os [serviços de pausa em execução em uma conta específica de](https://Gallery.TechNet.Microsoft.Com/12a256dd-39da-4690-b3f0-f0adccaf25f1) exemplo do VBScript pausa todos os serviços em execução na conta de serviço hipotética "netsvc".</span><span class="sxs-lookup"><span data-stu-id="3c375-176">The [Pause Services Running Under a Specific Account](https://Gallery.TechNet.Microsoft.Com/12a256dd-39da-4690-b3f0-f0adccaf25f1) VBScript sample Pauses all services running under the hypothetical service account "Netsvc".</span></span>

<span data-ttu-id="3c375-177">O exemplo de código VBScript a seguir demonstra como pausar um serviço específico de instâncias do [**\_ serviço Win32**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="3c375-177">The following VBScript code sample demonstrates how to pause a specific service from instances of [**Win32\_Service**](win32-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="3c375-178">O serviço deve dar suporte a pausar e já estar em execução.</span><span class="sxs-lookup"><span data-stu-id="3c375-178">The service must support pausing and be running already.</span></span>

 


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='Schedule'")

for each Service in ServiceSet
 SupportsPause = Service.AcceptPause
 if SupportsPause = true then
  RetVal = Service.PauseService()
  if RetVal = 0 then 
   WScript.Echo "Service paused"   
  else
   if RetVal = 1 then 
    WScript.Echo "Pause not supported" 
   else WScript.Echo "An error occurred:" & RetVal
   End If
  End If
 else
  WScript.Echo "Service does not support pause"
 end if
next
```



<span data-ttu-id="3c375-179">O exemplo de código Perl a seguir demonstra como pausar um serviço específico de instâncias do [**\_ serviço Win32**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="3c375-179">The following Perl code sample demonstrates how to pause a specific service from instances of [**Win32\_Service**](win32-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="3c375-180">O serviço deve dar suporte a pausar e já estar em execução.</span><span class="sxs-lookup"><span data-stu-id="3c375-180">The service must support pausing and be running already.</span></span>

 


```
use strict;
use Win32::OLE;

my ($ServiceSet, $SupportsPause, $RetVal);  
eval {$ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\Root\\CIMv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='Schedule'"); };
unless($@)
{
 foreach my $ServiceInst (in $ServiceSet)
 {
  if ($ServiceInst->{AcceptPause})
  {
   $RetVal = $ServiceInst->PauseService();
   if ($RetVal == 0)
   {
    print "\nService paused\n";
   }
   else
   {
    if ($RetVal == 1)
    {
     print "\nPause not supported\n" ;
    }
    else 
    {
     print "\nAn error occurred:", $RetVal, "\n";
    }
   } 
  }
  else
  {
   print "\nService does not support pause\n";
  }
 }
}
else
{
 print STDERR "\n", Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="3c375-181">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c375-181">Requirements</span></span>



| <span data-ttu-id="3c375-182">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c375-182">Requirement</span></span> | <span data-ttu-id="3c375-183">Valor</span><span class="sxs-lookup"><span data-stu-id="3c375-183">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c375-184">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c375-184">Minimum supported client</span></span><br/> | <span data-ttu-id="3c375-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3c375-185">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3c375-186">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c375-186">Minimum supported server</span></span><br/> | <span data-ttu-id="3c375-187">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c375-187">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3c375-188">Namespace</span><span class="sxs-lookup"><span data-stu-id="3c375-188">Namespace</span></span><br/>                | <span data-ttu-id="3c375-189">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="3c375-189">Root\\CIMv2</span></span><br/>                                                                  |
| <span data-ttu-id="3c375-190">MOF</span><span class="sxs-lookup"><span data-stu-id="3c375-190">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c375-191"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3c375-191"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c375-192">DLL</span><span class="sxs-lookup"><span data-stu-id="3c375-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c375-193"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c375-193"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c375-194">Consulte também</span><span class="sxs-lookup"><span data-stu-id="3c375-194">See also</span></span>

<dl> <dt>

<span data-ttu-id="3c375-195">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3c375-195">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3c375-196">**\_Serviço Win32**</span><span class="sxs-lookup"><span data-stu-id="3c375-196">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="3c375-197">Tarefas do WMI: serviços</span><span class="sxs-lookup"><span data-stu-id="3c375-197">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[<span data-ttu-id="3c375-198">**StopService**</span><span class="sxs-lookup"><span data-stu-id="3c375-198">**StopService**</span></span>](stopservice-method-in-class-win32-service.md)
</dt> </dl>

 


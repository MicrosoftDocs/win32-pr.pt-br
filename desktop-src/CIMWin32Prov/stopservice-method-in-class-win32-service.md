---
description: Coloca o serviço, representado pelo objeto de \_ serviço do Win32, no estado parado.
ms.assetid: cc2c71f7-12e6-4ba4-bfb4-f23845d798b5
ms.tgt_platform: multiple
title: Método StopService da classe Win32_Service (Sdoias. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 90d979754a3d6f034c353229dbaa1b1dbaedea79
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756243"
---
# <a name="stopservice-method-of-the-win32_service-class-sdoiash"></a><span data-ttu-id="6eb6a-103">Método StopService da classe Win32_Service (Sdoias. h)</span><span class="sxs-lookup"><span data-stu-id="6eb6a-103">StopService method of the Win32_Service class (Sdoias.h)</span></span>

<span data-ttu-id="6eb6a-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **StopService** coloca o serviço, representado pelo objeto de [**\_ serviço do Win32**](win32-service.md) , no estado parado.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-104">The **StopService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method places the service, represented by the [**Win32\_Service**](win32-service.md) object, in the stopped state.</span></span>

<span data-ttu-id="6eb6a-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="6eb6a-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="6eb6a-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="6eb6a-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="6eb6a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6eb6a-107">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="6eb6a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6eb6a-108">Parameters</span></span>

<span data-ttu-id="6eb6a-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6eb6a-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6eb6a-110">Return value</span></span>

<span data-ttu-id="6eb6a-111">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="6eb6a-112">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="6eb6a-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="6eb6a-113">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="6eb6a-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="6eb6a-114">**0**</span><span class="sxs-lookup"><span data-stu-id="6eb6a-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="6eb6a-115">A solicitação foi aceita.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="6eb6a-116">**1**</span><span class="sxs-lookup"><span data-stu-id="6eb6a-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="6eb6a-117">A solicitação não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="6eb6a-118">**2**</span><span class="sxs-lookup"><span data-stu-id="6eb6a-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="6eb6a-119">O usuário não tinha o acesso necessário.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="6eb6a-120">**3**</span><span class="sxs-lookup"><span data-stu-id="6eb6a-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="6eb6a-121">O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="6eb6a-122">**4**</span><span class="sxs-lookup"><span data-stu-id="6eb6a-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="6eb6a-123">O código de controle pedido não é válido ou é inaceitável para o serviço.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="6eb6a-124">**5**</span><span class="sxs-lookup"><span data-stu-id="6eb6a-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="6eb6a-125">O código de controle solicitado não pode ser enviado ao serviço porque o estado do serviço ([**Win32 \_ BaseService**](win32-baseservice.md).\*\*\*\* A propriedade State) é igual a 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="6eb6a-126">**6**</span><span class="sxs-lookup"><span data-stu-id="6eb6a-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="6eb6a-127">O serviço não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="6eb6a-128">**7**</span><span class="sxs-lookup"><span data-stu-id="6eb6a-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="6eb6a-129">O serviço não respondeu à solicitação de início em um tempo oportuno.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="6eb6a-130">**8**</span><span class="sxs-lookup"><span data-stu-id="6eb6a-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="6eb6a-131">Falha desconhecida ao iniciar o serviço.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="6eb6a-132">**9**</span><span class="sxs-lookup"><span data-stu-id="6eb6a-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="6eb6a-133">O caminho do diretório para o arquivo executável do serviço não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="6eb6a-134">**10**</span><span class="sxs-lookup"><span data-stu-id="6eb6a-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="6eb6a-135">O serviço já está em execução.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="6eb6a-136">**11**</span><span class="sxs-lookup"><span data-stu-id="6eb6a-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="6eb6a-137">O banco de dados para adicionar um serviço novo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="6eb6a-138">**12**</span><span class="sxs-lookup"><span data-stu-id="6eb6a-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="6eb6a-139">Uma dependência da qual esse serviço depende foi removida do sistema.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="6eb6a-140">**13**</span><span class="sxs-lookup"><span data-stu-id="6eb6a-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="6eb6a-141">O serviço não localizou o serviço necessário em um serviço dependente.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="6eb6a-142">**14**</span><span class="sxs-lookup"><span data-stu-id="6eb6a-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="6eb6a-143">O serviço foi desabilitado do sistema.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="6eb6a-144">**15**</span><span class="sxs-lookup"><span data-stu-id="6eb6a-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="6eb6a-145">O serviço não tem a autenticação correta para ser executado no sistema.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="6eb6a-146">**16**</span><span class="sxs-lookup"><span data-stu-id="6eb6a-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="6eb6a-147">Este serviço está sendo removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="6eb6a-148">**17**</span><span class="sxs-lookup"><span data-stu-id="6eb6a-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="6eb6a-149">O serviço não tem nenhum thread de execução.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="6eb6a-150">**anos**</span><span class="sxs-lookup"><span data-stu-id="6eb6a-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="6eb6a-151">O serviço tem dependências circulares quando é iniciado.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="6eb6a-152">**aprimora**</span><span class="sxs-lookup"><span data-stu-id="6eb6a-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="6eb6a-153">Um serviço está sendo executado com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="6eb6a-154">**20**</span><span class="sxs-lookup"><span data-stu-id="6eb6a-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="6eb6a-155">O nome do serviço tem caracteres inválidos.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="6eb6a-156">**Abril**</span><span class="sxs-lookup"><span data-stu-id="6eb6a-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="6eb6a-157">Parâmetros inválidos foram passados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="6eb6a-158">**22**</span><span class="sxs-lookup"><span data-stu-id="6eb6a-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="6eb6a-159">A conta sob a qual este serviço é executado é inválida ou não tem as permissões para executar o serviço.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="6eb6a-160">**23**</span><span class="sxs-lookup"><span data-stu-id="6eb6a-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="6eb6a-161">O serviço existe no banco de dados de serviços disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="6eb6a-162">**24**</span><span class="sxs-lookup"><span data-stu-id="6eb6a-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="6eb6a-163">O serviço está pausado atualmente no sistema.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6eb6a-164">Comentários</span><span class="sxs-lookup"><span data-stu-id="6eb6a-164">Remarks</span></span>

<span data-ttu-id="6eb6a-165">Depois de determinar quais serviços podem ser interrompidos ou pausados, você pode usar os métodos **StopService** e [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md) para parar e pausar serviços.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-165">After you have determined which services can be stopped or paused, you can use the **StopService** and [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md) methods to stop and pause services.</span></span> <span data-ttu-id="6eb6a-166">A decisão de interromper um serviço em vez de pausá-lo, ou vice-versa, depende de vários fatores, incluindo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6eb6a-166">The decision to stop a service rather than pause it, or vice versa, depends on several factors, including the following:</span></span>

-   <span data-ttu-id="6eb6a-167">O serviço é capaz de ser pausado?</span><span class="sxs-lookup"><span data-stu-id="6eb6a-167">Is the service capable of being paused?</span></span> <span data-ttu-id="6eb6a-168">Caso contrário, sua única opção é parar o serviço.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-168">If not, your only option is the stop the service.</span></span>
-   <span data-ttu-id="6eb6a-169">Você precisa continuar tratando as solicitações do cliente para qualquer pessoa já conectada ao serviço?</span><span class="sxs-lookup"><span data-stu-id="6eb6a-169">Do you need to continue handling client requests for anyone already connected to the service?</span></span> <span data-ttu-id="6eb6a-170">Nesse caso, pausar um serviço geralmente permite que ele manipule clientes existentes enquanto nega acesso a novos clientes.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-170">If so, pausing a service typically allows it to handle existing clients while denying access to new clients.</span></span> <span data-ttu-id="6eb6a-171">Por outro lado, quando você interrompe um serviço, todos os clientes são imediatamente desconectados.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-171">By contrast, when you stop a service, all clients are immediately disconnected.</span></span>
-   <span data-ttu-id="6eb6a-172">Você precisa reconfigurar um serviço e fazer com que as alterações entrem em vigor imediatamente?</span><span class="sxs-lookup"><span data-stu-id="6eb6a-172">Do you need to reconfigure a service and have the changes take effect immediately?</span></span> <span data-ttu-id="6eb6a-173">Embora as propriedades do serviço possam ser alteradas enquanto um serviço é pausado, a maioria delas não tem efeito até que o serviço seja realmente interrompido e reiniciado.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-173">Although service properties can be changed while a service is paused, most of them do not take effect until the service is actually stopped and restarted.</span></span>

<span data-ttu-id="6eb6a-174">O código de script necessário para interromper um serviço é quase idêntico ao código necessário para pausar o serviço.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-174">The scripting code required to stop a service is almost identical to the code required to pause the service.</span></span>

<span data-ttu-id="6eb6a-175">Se você tentar interromper um serviço que tem serviços dependentes em execução, o método **StopService** falhará com um valor de retorno de 3.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-175">If you attempt to stop a service which has dependent services running, the **StopService** method fails with a return value of 3.</span></span> <span data-ttu-id="6eb6a-176">Os serviços dependentes devem ser interrompidos primeiro.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-176">The dependent services must be stopped first.</span></span>

<span data-ttu-id="6eb6a-177">Se você parar um serviço, verifique imediatamente o [**\_ serviço Win32**](win32-service.md).\*\*\*\* A propriedade State, pois o valor ainda pode mostrar o serviço como em execução.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-177">If you stop a service, then immediately check the [**Win32\_Service**](win32-service.md).**State** property, as the value may still show the service as running.</span></span>

## <a name="examples"></a><span data-ttu-id="6eb6a-178">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6eb6a-178">Examples</span></span>

<span data-ttu-id="6eb6a-179">[O set-RemoteService](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) O exemplo do PowerShell define o estado do serviço para máquinas remotas.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-179">[The Set-RemoteService](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) PowerShell sample Sets service state for remote machines.</span></span>

<span data-ttu-id="6eb6a-180">O exemplo de [parar um serviço e seus dependentes](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732) do VBScript interrompe um serviço e todos os serviços dependentes.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-180">The [Stop a Service and Its Dependents](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732) VBScript sample stops a service and all dependent services.</span></span>

<span data-ttu-id="6eb6a-181">O exemplo de código VBScript a seguir demonstra como desligar um serviço.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-181">The following VBScript code sample demonstrates how to shut down a service.</span></span>


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='ClipSrv'")

for each Service in ServiceSet
 RetVal = Service.StopService()
 if RetVal = 0 then 
  WScript.Echo "Service stopped" 
 elseif RetVal = 5 then 
  WScript.Echo "Service already stopped" 
 end if
next
```



<span data-ttu-id="6eb6a-182">O exemplo de código Perl a seguir demonstra como desligar um serviço.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-182">The following Perl code sample demonstrates how to shut down a service.</span></span>


```
use strict;
use Win32::OLE;

my $ServiceSet;

eval { $ServiceSet = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='ClipSrv'"); };

if (!$@ && defined $ServiceSet)
{
 foreach my $ServiceInst (in $ServiceSet)
 {
  my $Result = $ServiceInst->StopService();
  if ($Result == 0)
  {
   print "\nService stopped\n";
  }
  elsif ($Result == 5) 
  {
   print "\nService already stopped\n";
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="6eb6a-183">O exemplo de código VBScript a seguir mostra que você não pode interromper o serviço NetDDE até que os serviços dependentes tenham sido interrompidos.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-183">The following VBScript code example shows that you cannot stop the NetDDE service until the dependent services have been stopped.</span></span> <span data-ttu-id="6eb6a-184">Para executar o script, verifique se o serviço NetDDE e seus serviços dependentes estão em execução usando o snap-in do MMC Services. msc ou o comando **net start** .</span><span class="sxs-lookup"><span data-stu-id="6eb6a-184">To run the script, ensure that the NetDDE service and its dependent services are running by using the Services.msc MMC snap-in or the **Net Start** command.</span></span>

<span data-ttu-id="6eb6a-185">A classe [**Win32 \_ DependentService**](win32-dependentservice.md) permite que você localize dependências de serviço por meio [de um associador de](/windows/desktop/WmiSdk/associators-of-statement) consulta.</span><span class="sxs-lookup"><span data-stu-id="6eb6a-185">The [**Win32\_DependentService**](win32-dependentservice.md) class allows you to locate service dependencies through an [Associators Of](/windows/desktop/WmiSdk/associators-of-statement) query.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & _
    strComputer & "\root\cimv2")

Set objNetDDEservice = _
    objWMIService.Get("Win32_Service.Name='NetDDE'")

WScript.Echo "NetDDE service state: " & objNetDDEService.State
WScript.Echo "Stopping NetDDE service"
Return = objNetDDEService.StopService()
WScript.Echo "Return value: " & Return  & _
    "  Service cannot be stopped because " & _
    "dependent services are running"

Set colServiceList = objWMIService.ExecQuery("Associators of " _
    & "{Win32_Service.Name='NetDDE'} Where " _
        & "AssocClass=Win32_DependentService " & _
    "Role=Antecedent" )

For Each objService in colServiceList
   WScript.Echo "Dependent service: " & objService.Name & _
   "   State: " & objService.State
   WScript.Echo "Stopping dependent service " & objService.Name
   objService.StopService()    
Next

Wscript.Sleep 20000
WScript.Echo "Stopping NetDDE service"
Return = objNetDDEService.StopService()
WScript.Echo "Return value: " & Return
```



## <a name="requirements"></a><span data-ttu-id="6eb6a-186">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6eb6a-186">Requirements</span></span>



| <span data-ttu-id="6eb6a-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="6eb6a-187">Requirement</span></span> | <span data-ttu-id="6eb6a-188">Valor</span><span class="sxs-lookup"><span data-stu-id="6eb6a-188">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6eb6a-189">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6eb6a-189">Minimum supported client</span></span><br/> | <span data-ttu-id="6eb6a-190">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6eb6a-190">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6eb6a-191">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6eb6a-191">Minimum supported server</span></span><br/> | <span data-ttu-id="6eb6a-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6eb6a-192">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6eb6a-193">Namespace</span><span class="sxs-lookup"><span data-stu-id="6eb6a-193">Namespace</span></span><br/>                | <span data-ttu-id="6eb6a-194">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6eb6a-194">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6eb6a-195">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6eb6a-195">Header</span></span><br/>                   | <dl> <span data-ttu-id="6eb6a-196"><dt>Sdoias. h</dt></span><span class="sxs-lookup"><span data-stu-id="6eb6a-196"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="6eb6a-197">MOF</span><span class="sxs-lookup"><span data-stu-id="6eb6a-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6eb6a-198"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6eb6a-198"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6eb6a-199">DLL</span><span class="sxs-lookup"><span data-stu-id="6eb6a-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6eb6a-200"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6eb6a-200"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6eb6a-201">Confira também</span><span class="sxs-lookup"><span data-stu-id="6eb6a-201">See also</span></span>

<dl> <dt>

<span data-ttu-id="6eb6a-202">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6eb6a-202">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6eb6a-203">**\_Serviço Win32**</span><span class="sxs-lookup"><span data-stu-id="6eb6a-203">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="6eb6a-204">Tarefas do WMI: serviços</span><span class="sxs-lookup"><span data-stu-id="6eb6a-204">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[<span data-ttu-id="6eb6a-205">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="6eb6a-205">**PauseService**</span></span>](pauseservice-method-in-class-win32-systemdriver.md)
</dt> </dl>

 


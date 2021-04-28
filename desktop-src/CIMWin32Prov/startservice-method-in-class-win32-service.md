---
description: Método StartService da classe Win32_Service (provedores WMI CIMWin32) – tenta posicionar o serviço referenciado em seu estado de inicialização.
ms.assetid: b7a815a2-7bf6-436f-b3b4-de55eeb2de0e
ms.tgt_platform: multiple
title: Método StartService da classe Win32_Service (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a630b9d926ff5377312f1c67630a20816ab38b6c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086154"
---
# <a name="startservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="ae656-103">Método StartService da classe Win32_Service (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="ae656-103">StartService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="ae656-104">O método **StartService** tenta posicionar o serviço referenciado em seu estado de inicialização.</span><span class="sxs-lookup"><span data-stu-id="ae656-104">The **StartService** method attempts to place the referenced service into its startup state.</span></span>

<span data-ttu-id="ae656-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="ae656-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ae656-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ae656-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ae656-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ae656-107">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="ae656-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ae656-108">Parameters</span></span>

<span data-ttu-id="ae656-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ae656-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ae656-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ae656-110">Return value</span></span>

<span data-ttu-id="ae656-111">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="ae656-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="ae656-112">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="ae656-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="ae656-113">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="ae656-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="ae656-114">**0**</span><span class="sxs-lookup"><span data-stu-id="ae656-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="ae656-115">A solicitação foi aceita.</span><span class="sxs-lookup"><span data-stu-id="ae656-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="ae656-116">**1**</span><span class="sxs-lookup"><span data-stu-id="ae656-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="ae656-117">A solicitação não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="ae656-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ae656-118">**2**</span><span class="sxs-lookup"><span data-stu-id="ae656-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="ae656-119">O usuário não tinha o acesso necessário.</span><span class="sxs-lookup"><span data-stu-id="ae656-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="ae656-120">**3**</span><span class="sxs-lookup"><span data-stu-id="ae656-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="ae656-121">O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.</span><span class="sxs-lookup"><span data-stu-id="ae656-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="ae656-122">**4**</span><span class="sxs-lookup"><span data-stu-id="ae656-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="ae656-123">O código de controle pedido não é válido ou é inaceitável para o serviço.</span><span class="sxs-lookup"><span data-stu-id="ae656-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="ae656-124">**5**</span><span class="sxs-lookup"><span data-stu-id="ae656-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="ae656-125">O código de controle solicitado não pode ser enviado ao serviço porque o estado do serviço ([**Win32 \_ BaseService**](win32-baseservice.md).\*\*\*\* A propriedade State) é igual a 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="ae656-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="ae656-126">**6**</span><span class="sxs-lookup"><span data-stu-id="ae656-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="ae656-127">O serviço não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="ae656-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="ae656-128">**7**</span><span class="sxs-lookup"><span data-stu-id="ae656-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="ae656-129">O serviço não respondeu à solicitação de início em um tempo oportuno.</span><span class="sxs-lookup"><span data-stu-id="ae656-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="ae656-130">**8**</span><span class="sxs-lookup"><span data-stu-id="ae656-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="ae656-131">Falha desconhecida ao iniciar o serviço.</span><span class="sxs-lookup"><span data-stu-id="ae656-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="ae656-132">**9**</span><span class="sxs-lookup"><span data-stu-id="ae656-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="ae656-133">O caminho do diretório para o arquivo executável do serviço não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="ae656-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="ae656-134">**10**</span><span class="sxs-lookup"><span data-stu-id="ae656-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="ae656-135">O serviço já está em execução.</span><span class="sxs-lookup"><span data-stu-id="ae656-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="ae656-136">**11**</span><span class="sxs-lookup"><span data-stu-id="ae656-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="ae656-137">O banco de dados para adicionar um serviço novo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="ae656-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="ae656-138">**12**</span><span class="sxs-lookup"><span data-stu-id="ae656-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="ae656-139">Uma dependência da qual esse serviço depende foi removida do sistema.</span><span class="sxs-lookup"><span data-stu-id="ae656-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ae656-140">**13**</span><span class="sxs-lookup"><span data-stu-id="ae656-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="ae656-141">O serviço não localizou o serviço necessário em um serviço dependente.</span><span class="sxs-lookup"><span data-stu-id="ae656-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="ae656-142">**14**</span><span class="sxs-lookup"><span data-stu-id="ae656-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="ae656-143">O serviço foi desabilitado do sistema.</span><span class="sxs-lookup"><span data-stu-id="ae656-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ae656-144">**15**</span><span class="sxs-lookup"><span data-stu-id="ae656-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="ae656-145">O serviço não tem a autenticação correta para ser executado no sistema.</span><span class="sxs-lookup"><span data-stu-id="ae656-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="ae656-146">**16**</span><span class="sxs-lookup"><span data-stu-id="ae656-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="ae656-147">Este serviço está sendo removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="ae656-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ae656-148">**17**</span><span class="sxs-lookup"><span data-stu-id="ae656-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="ae656-149">O serviço não tem nenhum thread de execução.</span><span class="sxs-lookup"><span data-stu-id="ae656-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="ae656-150">**anos**</span><span class="sxs-lookup"><span data-stu-id="ae656-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="ae656-151">O serviço tem dependências circulares quando é iniciado.</span><span class="sxs-lookup"><span data-stu-id="ae656-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="ae656-152">**aprimora**</span><span class="sxs-lookup"><span data-stu-id="ae656-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="ae656-153">Um serviço está sendo executado com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="ae656-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="ae656-154">**20**</span><span class="sxs-lookup"><span data-stu-id="ae656-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="ae656-155">O nome do serviço tem caracteres inválidos.</span><span class="sxs-lookup"><span data-stu-id="ae656-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="ae656-156">**Abril**</span><span class="sxs-lookup"><span data-stu-id="ae656-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="ae656-157">Parâmetros inválidos foram passados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="ae656-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="ae656-158">**22**</span><span class="sxs-lookup"><span data-stu-id="ae656-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="ae656-159">A conta sob a qual este serviço é executado é inválida ou não tem as permissões para executar o serviço.</span><span class="sxs-lookup"><span data-stu-id="ae656-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="ae656-160">**23**</span><span class="sxs-lookup"><span data-stu-id="ae656-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="ae656-161">O serviço existe no banco de dados de serviços disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="ae656-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ae656-162">**24**</span><span class="sxs-lookup"><span data-stu-id="ae656-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="ae656-163">O serviço está pausado atualmente no sistema.</span><span class="sxs-lookup"><span data-stu-id="ae656-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ae656-164">Comentários</span><span class="sxs-lookup"><span data-stu-id="ae656-164">Remarks</span></span>

<span data-ttu-id="ae656-165">Embora possa parecer não ser uma diferença prática entre um serviço que é interrompido e um serviço em pausa, os dois Estados aparecem de forma diferente para o SCM.</span><span class="sxs-lookup"><span data-stu-id="ae656-165">Although there might appear to be no practical difference between a service that is stopped and a service that is paused, the two states appear differently to the SCM.</span></span> <span data-ttu-id="ae656-166">Um serviço parado é um serviço que não está em execução e deve passar pelo procedimento de início do serviço inteiro.</span><span class="sxs-lookup"><span data-stu-id="ae656-166">A stopped service is a service that is not running and must go through the entire service start procedure.</span></span> <span data-ttu-id="ae656-167">Um serviço em pausa, no entanto, ainda está em execução, mas teve seu funcionamento suspenso.</span><span class="sxs-lookup"><span data-stu-id="ae656-167">A paused service, however, is still running but has had its functioning is suspended.</span></span> <span data-ttu-id="ae656-168">Por isso, um serviço em pausa não precisa passar pelo procedimento de início do serviço inteiro, mas precisa de um procedimento diferente para retomar o funcionamento.</span><span class="sxs-lookup"><span data-stu-id="ae656-168">Because of this, a paused service does not need to go through the entire service start procedure but needs a different procedure to resume functioning.</span></span>

<span data-ttu-id="ae656-169">Você deve usar o método apropriado para iniciar um serviço que foi interrompido ou para retomar um serviço que tenha sido pausado.</span><span class="sxs-lookup"><span data-stu-id="ae656-169">You must use the proper method to start a service that has been stopped or to resume a service that has been paused.</span></span> <span data-ttu-id="ae656-170">Os métodos de [**\_ serviço do Win32**](win32-service.md) **StartService** e [**ResumeService**](resumeservice-method-in-class-win32-service.md) devem ser usados nas seguintes situações:</span><span class="sxs-lookup"><span data-stu-id="ae656-170">The [**Win32\_Service**](win32-service.md) methods **StartService** and [**ResumeService**](resumeservice-method-in-class-win32-service.md) should be used in the following situations:</span></span>

-   <span data-ttu-id="ae656-171">Se um serviço estiver parado no momento, você deverá usar o método **StartService** para reiniciá-lo; [**ResumeService**](resumeservice-method-in-class-win32-service.md) não pode iniciar um serviço que está parado no momento.</span><span class="sxs-lookup"><span data-stu-id="ae656-171">If a service is currently stopped, you must use the **StartService** method to restart it; [**ResumeService**](resumeservice-method-in-class-win32-service.md) cannot start a service that is currently stopped.</span></span>
-   <span data-ttu-id="ae656-172">Se um serviço estiver em pausa, você deverá usar [**ResumeService**](resumeservice-method-in-class-win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="ae656-172">If a service is paused, you must use [**ResumeService**](resumeservice-method-in-class-win32-service.md).</span></span> <span data-ttu-id="ae656-173">Se você usar o método **StartService** em um serviço em pausa, receberá a mensagem "o serviço já está em execução".</span><span class="sxs-lookup"><span data-stu-id="ae656-173">If you use the **StartService** method on a paused service, you receive the message, "The service is already running."</span></span> <span data-ttu-id="ae656-174">No entanto, o serviço permanece em pausa até que o código de controle retome o serviço seja enviado a ele.</span><span class="sxs-lookup"><span data-stu-id="ae656-174">However, the service remains paused until the resume service control code is sent to it.</span></span>

<span data-ttu-id="ae656-175">Se você iniciar um serviço interrompido que depende de outro serviço, ambos os serviços serão iniciados.</span><span class="sxs-lookup"><span data-stu-id="ae656-175">If you start a stopped service that depends on another service, then both services are started.</span></span> <span data-ttu-id="ae656-176">Quando um serviço é iniciado com esse método, os serviços dependentes não são iniciados automaticamente.</span><span class="sxs-lookup"><span data-stu-id="ae656-176">When a service is started with this method, any dependent services are not automatically started.</span></span> <span data-ttu-id="ae656-177">Você deve usar a classe de associação [**Win32 \_ DependentService**](win32-dependentservice.md) e os [ASSOCIADORES de](/windows/desktop/WmiSdk/associators-of-statement) consulta para localizar os dependentes e iniciá-los separadamente.</span><span class="sxs-lookup"><span data-stu-id="ae656-177">You must use the association class [**Win32\_DependentService**](win32-dependentservice.md) and the [Associators Of](/windows/desktop/WmiSdk/associators-of-statement) query to locate the dependents and start them separately.</span></span>

## <a name="examples"></a><span data-ttu-id="ae656-178">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ae656-178">Examples</span></span>

<span data-ttu-id="ae656-179">O exemplo [habilitar remotamente](https://Gallery.TechNet.Microsoft.Com/Remotely-Enable-RDP-855c3842) o PowerShell do RDP habilita remotamente o serviço de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="ae656-179">The [Remotely Enable RDP](https://Gallery.TechNet.Microsoft.Com/Remotely-Enable-RDP-855c3842) PowerShell sample remotely enables the Remote Desktop service.</span></span>

<span data-ttu-id="ae656-180">O exemplo de [parar, iniciar, habilitar ou desabilitar](https://Gallery.TechNet.Microsoft.Com/212e68f0-5279-4499-8e9e-6aa1807719c0) o PowerShell de serviço inicia, interrompe, habilita ou desabilita um serviço.</span><span class="sxs-lookup"><span data-stu-id="ae656-180">The [Stop, Start, Enable or Disable Service](https://Gallery.TechNet.Microsoft.Com/212e68f0-5279-4499-8e9e-6aa1807719c0) PowerShell sample starts, stops, enables, or disables a service.</span></span>

<span data-ttu-id="ae656-181">O exemplo de código VBSScript a seguir demonstra como iniciar um serviço específico de instâncias [**do \_ serviço Win32**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="ae656-181">The following VBSScript code sample demonstrates how to start a specific service from instances of [**Win32\_Service**](win32-service.md).</span></span>


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='ClipSrv'")

for each Service in ServiceSet
 RetVal = Service.StartService()
 if RetVal = 0 then WScript.Echo "Service started"
 if RetVal = 10 then WScript.Echo "Service already running"
next
```



<span data-ttu-id="ae656-182">O exemplo de código Perl a seguir demonstra como iniciar um serviço específico de instâncias [**do \_ serviço Win32**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="ae656-182">The following Perl code sample demonstrates how to start a specific service from instances of [**Win32\_Service**](win32-service.md).</span></span>


```
use strict;
use Win32::OLE;

my $ServiceSet;

eval { $ServiceSet = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='ClipSrv'"); };

if(!$@ && defined $ServiceSet)
{
 foreach my $service (in $ServiceSet)
 {
  my $Result = $service->StartService();
  if ($Result == 0) 
  {
   print "\nService started\n";
  }
  elsif ($Result == 10)
  {
   print "\nService already running\n";
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="ae656-183">O exemplo de código VBScript a seguir, NetDDE, depende do serviço NetDDEDSDM.</span><span class="sxs-lookup"><span data-stu-id="ae656-183">The following VBScript code example, NetDDE, is dependent on the NetDDEDSDM service.</span></span> <span data-ttu-id="ae656-184">O script localiza a classe na qual o NetDDE depende e inicia, o que não inicia automaticamente o NetDDE.</span><span class="sxs-lookup"><span data-stu-id="ae656-184">The script locates the class on which NetDDE depends and starts it, which does not automatically start NetDDE.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

' Stop NetDDE if it is running
Set objNetDDEService = objWMIService.Get("Win32_Service.Name='NetDDE'")
Return = objNetDDEService.StopService()

' NetDDE is in the dependent role to another service
Set colServiceList = objWMIService.ExecQuery("Associators of " _
    & "{Win32_Service.Name='NetDDE'} Where " & "AssocClass=Win32_DependentService " & "Role=Dependent" )

' start the service on which NetDDE is dependent
For Each objService in colServiceList
    WScript.Echo "Starting " & objService.Name
    Return = objService.StartService()
    If Return = 0 Then
        WScript.Echo "Parent service " & objService.Name & " started successfully"
    Else
        WScript.Echo "Parent service " & objService.Name & " did not start. Return = " & Return
    End If
Next

' NetDDE is still stopped
Set objNetDDEService = _
    objWMIService.Get("Win32_Service.Name='NetDDE'")
WScript.Echo "Dependent NetDDE service is " & objNetDDEService.State
```



## <a name="requirements"></a><span data-ttu-id="ae656-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae656-185">Requirements</span></span>



| <span data-ttu-id="ae656-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae656-186">Requirement</span></span> | <span data-ttu-id="ae656-187">Valor</span><span class="sxs-lookup"><span data-stu-id="ae656-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae656-188">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae656-188">Minimum supported client</span></span><br/> | <span data-ttu-id="ae656-189">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ae656-189">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ae656-190">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae656-190">Minimum supported server</span></span><br/> | <span data-ttu-id="ae656-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ae656-191">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ae656-192">Namespace</span><span class="sxs-lookup"><span data-stu-id="ae656-192">Namespace</span></span><br/>                | <span data-ttu-id="ae656-193">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ae656-193">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ae656-194">MOF</span><span class="sxs-lookup"><span data-stu-id="ae656-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae656-195"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ae656-195"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ae656-196">DLL</span><span class="sxs-lookup"><span data-stu-id="ae656-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae656-197"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae656-197"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae656-198">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ae656-198">See also</span></span>

<dl> <dt>

<span data-ttu-id="ae656-199">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ae656-199">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ae656-200">**\_Serviço Win32**</span><span class="sxs-lookup"><span data-stu-id="ae656-200">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="ae656-201">Tarefas do WMI: serviços</span><span class="sxs-lookup"><span data-stu-id="ae656-201">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 


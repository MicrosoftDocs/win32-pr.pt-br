---
description: Método ResumeService da classe Win32_Service (provedores WMI CIMWin32) – tenta posicionar o serviço referenciado no estado retomado.
ms.assetid: 3b4228bf-9ff5-44ab-bfe2-f7dd8fb62007
ms.tgt_platform: multiple
title: Método ResumeService da classe Win32_Service (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.ResumeService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 73c21f282577207b63bcfa2d624c59ddfa3c9bcb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090974"
---
# <a name="resumeservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="a4bc6-103">Método ResumeService da classe Win32_Service (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="a4bc6-103">ResumeService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="a4bc6-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ResumeService** tenta posicionar o serviço referenciado no estado retomado.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-104">The **ResumeService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the referenced service in the resumed state.</span></span>

<span data-ttu-id="a4bc6-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="a4bc6-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a4bc6-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a4bc6-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a4bc6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4bc6-107">Syntax</span></span>


```mof
uint32 ResumeService();
```



## <a name="parameters"></a><span data-ttu-id="a4bc6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4bc6-108">Parameters</span></span>

<span data-ttu-id="a4bc6-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a4bc6-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a4bc6-110">Return value</span></span>

<span data-ttu-id="a4bc6-111">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="a4bc6-112">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="a4bc6-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="a4bc6-113">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="a4bc6-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="a4bc6-114">**0**</span><span class="sxs-lookup"><span data-stu-id="a4bc6-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="a4bc6-115">A solicitação foi aceita.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="a4bc6-116">**1**</span><span class="sxs-lookup"><span data-stu-id="a4bc6-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="a4bc6-117">A solicitação não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="a4bc6-118">**2**</span><span class="sxs-lookup"><span data-stu-id="a4bc6-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="a4bc6-119">O usuário não tinha o acesso necessário.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="a4bc6-120">**3**</span><span class="sxs-lookup"><span data-stu-id="a4bc6-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="a4bc6-121">O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="a4bc6-122">**4**</span><span class="sxs-lookup"><span data-stu-id="a4bc6-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="a4bc6-123">O código de controle pedido não é válido ou é inaceitável para o serviço.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="a4bc6-124">**5**</span><span class="sxs-lookup"><span data-stu-id="a4bc6-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="a4bc6-125">O código de controle solicitado não pode ser enviado ao serviço porque o estado do serviço ([**Win32 \_ BaseService**](win32-baseservice.md).\*\*\*\* A propriedade State) é igual a 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="a4bc6-126">**6**</span><span class="sxs-lookup"><span data-stu-id="a4bc6-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="a4bc6-127">O serviço não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="a4bc6-128">**7**</span><span class="sxs-lookup"><span data-stu-id="a4bc6-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="a4bc6-129">O serviço não respondeu à solicitação de início em um tempo oportuno.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="a4bc6-130">**8**</span><span class="sxs-lookup"><span data-stu-id="a4bc6-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="a4bc6-131">Falha desconhecida ao iniciar o serviço.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="a4bc6-132">**9**</span><span class="sxs-lookup"><span data-stu-id="a4bc6-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="a4bc6-133">O caminho do diretório para o arquivo executável do serviço não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="a4bc6-134">**10**</span><span class="sxs-lookup"><span data-stu-id="a4bc6-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="a4bc6-135">O serviço já está em execução.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="a4bc6-136">**11**</span><span class="sxs-lookup"><span data-stu-id="a4bc6-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="a4bc6-137">O banco de dados para adicionar um serviço novo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="a4bc6-138">**12**</span><span class="sxs-lookup"><span data-stu-id="a4bc6-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="a4bc6-139">Uma dependência da qual esse serviço depende foi removida do sistema.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a4bc6-140">**13**</span><span class="sxs-lookup"><span data-stu-id="a4bc6-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="a4bc6-141">O serviço não localizou o serviço necessário em um serviço dependente.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="a4bc6-142">**14**</span><span class="sxs-lookup"><span data-stu-id="a4bc6-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="a4bc6-143">O serviço foi desabilitado do sistema.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a4bc6-144">**15**</span><span class="sxs-lookup"><span data-stu-id="a4bc6-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="a4bc6-145">O serviço não tem a autenticação correta para ser executado no sistema.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="a4bc6-146">**16**</span><span class="sxs-lookup"><span data-stu-id="a4bc6-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="a4bc6-147">Este serviço está sendo removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a4bc6-148">**17**</span><span class="sxs-lookup"><span data-stu-id="a4bc6-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="a4bc6-149">O serviço não tem nenhum thread de execução.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="a4bc6-150">**anos**</span><span class="sxs-lookup"><span data-stu-id="a4bc6-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="a4bc6-151">O serviço tem dependências circulares quando é iniciado.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="a4bc6-152">**aprimora**</span><span class="sxs-lookup"><span data-stu-id="a4bc6-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="a4bc6-153">Um serviço está sendo executado com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="a4bc6-154">**20**</span><span class="sxs-lookup"><span data-stu-id="a4bc6-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="a4bc6-155">O nome do serviço tem caracteres inválidos.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="a4bc6-156">**Abril**</span><span class="sxs-lookup"><span data-stu-id="a4bc6-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="a4bc6-157">Parâmetros inválidos foram passados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="a4bc6-158">**22**</span><span class="sxs-lookup"><span data-stu-id="a4bc6-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="a4bc6-159">A conta sob a qual este serviço é executado é inválida ou não tem as permissões para executar o serviço.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="a4bc6-160">**23**</span><span class="sxs-lookup"><span data-stu-id="a4bc6-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="a4bc6-161">O serviço existe no banco de dados de serviços disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a4bc6-162">**24**</span><span class="sxs-lookup"><span data-stu-id="a4bc6-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="a4bc6-163">O serviço está pausado atualmente no sistema.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a4bc6-164">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4bc6-164">Remarks</span></span>

<span data-ttu-id="a4bc6-165">Embora possa parecer não ser uma diferença prática entre um serviço que é interrompido e um serviço em pausa, os dois Estados aparecem de forma diferente para o SCM.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-165">Although there might appear to be no practical difference between a service that is stopped and a service that is paused, the two states appear differently to the SCM.</span></span> <span data-ttu-id="a4bc6-166">Um serviço parado é um serviço que não está em execução e deve passar pelo procedimento de início do serviço inteiro.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-166">A stopped service is a service that is not running and must go through the entire service start procedure.</span></span> <span data-ttu-id="a4bc6-167">Um serviço em pausa, no entanto, ainda está em execução, mas teve seu funcionamento suspenso.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-167">A paused service, however, is still running but has had its functioning is suspended.</span></span> <span data-ttu-id="a4bc6-168">Por isso, um serviço em pausa não precisa passar pelo procedimento de início do serviço inteiro, mas precisa de um procedimento diferente para retomar o funcionamento.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-168">Because of this, a paused service does not need to go through the entire service start procedure but needs a different procedure to resume functioning.</span></span>

<span data-ttu-id="a4bc6-169">Você deve usar o método apropriado para iniciar um serviço que foi interrompido ou para retomar um serviço que tenha sido pausado.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-169">You must use the proper method to start a service that has been stopped or to resume a service that has been paused.</span></span> <span data-ttu-id="a4bc6-170">Os métodos de [**\_ serviço do Win32**](win32-service.md) [**StartService**](startservice-method-in-class-win32-service.md) e **ResumeService** devem ser usados nas seguintes situações:</span><span class="sxs-lookup"><span data-stu-id="a4bc6-170">The [**Win32\_Service**](win32-service.md) methods [**StartService**](startservice-method-in-class-win32-service.md) and **ResumeService** should be used in the following situations:</span></span>

-   <span data-ttu-id="a4bc6-171">Se um serviço estiver parado no momento, você deverá usar o método [**StartService**](startservice-method-in-class-win32-service.md) para reiniciá-lo; **ResumeService** não pode iniciar um serviço que está parado no momento.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-171">If a service is currently stopped, you must use the [**StartService**](startservice-method-in-class-win32-service.md) method to restart it; **ResumeService** cannot start a service that is currently stopped.</span></span>
-   <span data-ttu-id="a4bc6-172">Se um serviço estiver em pausa, você deverá usar **ResumeService**.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-172">If a service is paused, you must use **ResumeService**.</span></span> <span data-ttu-id="a4bc6-173">Se você usar o método [**StartService**](startservice-method-in-class-win32-service.md) em um serviço em pausa, receberá a mensagem "o serviço já está em execução".</span><span class="sxs-lookup"><span data-stu-id="a4bc6-173">If you use the [**StartService**](startservice-method-in-class-win32-service.md) method on a paused service, you receive the message, "The service is already running."</span></span> <span data-ttu-id="a4bc6-174">No entanto, o serviço permanece em pausa até que o código de controle retome o serviço seja enviado a ele.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-174">However, the service remains paused until the resume service control code is sent to it.</span></span>

## <a name="examples"></a><span data-ttu-id="a4bc6-175">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a4bc6-175">Examples</span></span>

<span data-ttu-id="a4bc6-176">O exemplo de [retomar os serviços AutoStart que estão em pausa](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) do VBScript reinicia todos os serviços de início automático que foram pausados.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-176">The [Resume AutoStart Services that are Paused](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) VBScript sample restarts any auto-start services that have been paused.</span></span>

<span data-ttu-id="a4bc6-177">O exemplo de código VBScript a seguir descreve como retomar um serviço em pausa de instâncias do [**\_ serviço Win32**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="a4bc6-177">The following VBScript code sample describes how to resume a paused service from instances of [**Win32\_Service**](win32-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="a4bc6-178">O serviço deve dar suporte a pausar e já estar em execução.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-178">The service must support pausing and be running already.</span></span>

 


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='Schedule'")

for each Service in ServiceSet
 SupportsPause = Service.AcceptPause
 if SupportsPause = true then
  RetVal = Service.ResumeService()
  if RetVal = 0 then 
   WScript.Echo "Service resumed"   
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



<span data-ttu-id="a4bc6-179">O exemplo de código Perl a seguir descreve como retomar um serviço em pausa de instâncias do [**\_ serviço Win32**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="a4bc6-179">The following Perl code sample describes how to resume a paused service from instances of [**Win32\_Service**](win32-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="a4bc6-180">O serviço deve dar suporte a pausar e já estar em execução.</span><span class="sxs-lookup"><span data-stu-id="a4bc6-180">The service must support pausing and be running already.</span></span>

 


```Perl
use strict;
use Win32::OLE;

my $ServiceSet;

eval { $ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\Root\\CIMv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='Schedule'"); };

if (!$@ && defined $ServiceSet)
{
 foreach my $Service (in $ServiceSet)
 {
  my $SupportsPause = $Service->{AcceptPause};
  if ($SupportsPause)
  {
   my $RetVal = $Service->ResumeService();
   if ($RetVal == 0)
   {
    print "\nService resumed\n";
   }
   else
   {
    if ($RetVal == 1)
    {
     print STDERR "\nPause not supported\n";
    }
    else
    {
     print STDERR "\nAn error occurred: ", $RetVal, "\n";
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
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="a4bc6-181">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4bc6-181">Requirements</span></span>



| <span data-ttu-id="a4bc6-182">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4bc6-182">Requirement</span></span> | <span data-ttu-id="a4bc6-183">Valor</span><span class="sxs-lookup"><span data-stu-id="a4bc6-183">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4bc6-184">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4bc6-184">Minimum supported client</span></span><br/> | <span data-ttu-id="a4bc6-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a4bc6-185">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a4bc6-186">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4bc6-186">Minimum supported server</span></span><br/> | <span data-ttu-id="a4bc6-187">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4bc6-187">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a4bc6-188">Namespace</span><span class="sxs-lookup"><span data-stu-id="a4bc6-188">Namespace</span></span><br/>                | <span data-ttu-id="a4bc6-189">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="a4bc6-189">Root\\CIMv2</span></span><br/>                                                                  |
| <span data-ttu-id="a4bc6-190">MOF</span><span class="sxs-lookup"><span data-stu-id="a4bc6-190">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a4bc6-191"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a4bc6-191"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a4bc6-192">DLL</span><span class="sxs-lookup"><span data-stu-id="a4bc6-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4bc6-193"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4bc6-193"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4bc6-194">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a4bc6-194">See also</span></span>

<dl> <dt>

<span data-ttu-id="a4bc6-195">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a4bc6-195">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a4bc6-196">**\_Serviço Win32**</span><span class="sxs-lookup"><span data-stu-id="a4bc6-196">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="a4bc6-197">Tarefas do WMI: serviços</span><span class="sxs-lookup"><span data-stu-id="a4bc6-197">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 


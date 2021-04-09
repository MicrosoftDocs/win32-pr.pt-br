---
description: Modifica o modo de início de um \_ serviço Win32.
ms.assetid: 4fd6a1eb-d2e0-4172-843d-24ae89c5bfcf
ms.tgt_platform: multiple
title: Método ChangeStartMode da classe Win32_Service (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.ChangeStartMode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 06a4692996354614a685471f98b0243fc1091433
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010177"
---
# <a name="changestartmode-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="ddb71-103">Método ChangeStartMode da classe Win32_Service (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="ddb71-103">ChangeStartMode method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="ddb71-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeStartMode** modifica o modo de início de [**um \_ serviço Win32**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="ddb71-104">The **ChangeStartMode** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies the start mode of a [**Win32\_Service**](win32-service.md).</span></span>

<span data-ttu-id="ddb71-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="ddb71-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ddb71-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ddb71-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ddb71-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ddb71-107">Syntax</span></span>


```mof
uint32 ChangeStartMode(
  [in] string StartMode = Auto Start
);
```



## <a name="parameters"></a><span data-ttu-id="ddb71-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ddb71-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddb71-109">*StartMode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ddb71-109">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddb71-110">Modo de início do serviço base do Windows.</span><span class="sxs-lookup"><span data-stu-id="ddb71-110">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="ddb71-111"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Inicialização inicial** ("inicialização")</span><span class="sxs-lookup"><span data-stu-id="ddb71-111"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="ddb71-112">Driver de dispositivo iniciado pelo carregador do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="ddb71-112">Device driver started by the operating system loader.</span></span> <span data-ttu-id="ddb71-113">Esse valor só é válido para serviços do driver.</span><span class="sxs-lookup"><span data-stu-id="ddb71-113">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="ddb71-114"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema** ("sistema")</span><span class="sxs-lookup"><span data-stu-id="ddb71-114"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="ddb71-115">Driver de dispositivo iniciado pelo processo de inicialização do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="ddb71-115">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="ddb71-116">Esse valor só é válido para serviços do driver.</span><span class="sxs-lookup"><span data-stu-id="ddb71-116">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="ddb71-117"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Início automático** ("automático")</span><span class="sxs-lookup"><span data-stu-id="ddb71-117"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start** ("Automatic")</span></span>


</dt> <dd>

<span data-ttu-id="ddb71-118">Serviço a ser iniciado automaticamente pelo gerenciador de controle de serviço durante a inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="ddb71-118">Service to be started automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="ddb71-119"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Início da demanda** ("manual")</span><span class="sxs-lookup"><span data-stu-id="ddb71-119"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="ddb71-120">Serviço a ser iniciado pelo Gerenciador de controle de serviço quando um processo chama o método [**StartService**](startservice-method-in-class-win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="ddb71-120">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ddb71-121"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("desabilitado")</span><span class="sxs-lookup"><span data-stu-id="ddb71-121"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="ddb71-122">Serviço que não pode mais ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="ddb71-122">Service that can no longer be started.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddb71-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ddb71-123">Return value</span></span>

<span data-ttu-id="ddb71-124">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="ddb71-124">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="ddb71-125">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="ddb71-125">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="ddb71-126">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="ddb71-126">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="ddb71-127">**Êxito**</span><span class="sxs-lookup"><span data-stu-id="ddb71-127">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="ddb71-128">0</span><span class="sxs-lookup"><span data-stu-id="ddb71-128">0</span></span>

<span data-ttu-id="ddb71-129">A solicitação foi aceita.</span><span class="sxs-lookup"><span data-stu-id="ddb71-129">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="ddb71-130">**Sem suporte**</span><span class="sxs-lookup"><span data-stu-id="ddb71-130">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="ddb71-131">1</span><span class="sxs-lookup"><span data-stu-id="ddb71-131">1</span></span>

<span data-ttu-id="ddb71-132">A solicitação não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="ddb71-132">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ddb71-133">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="ddb71-133">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="ddb71-134">2</span><span class="sxs-lookup"><span data-stu-id="ddb71-134">2</span></span>

<span data-ttu-id="ddb71-135">O usuário não tinha o acesso necessário.</span><span class="sxs-lookup"><span data-stu-id="ddb71-135">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="ddb71-136">**Serviços dependentes em execução**</span><span class="sxs-lookup"><span data-stu-id="ddb71-136">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="ddb71-137">3</span><span class="sxs-lookup"><span data-stu-id="ddb71-137">3</span></span>

<span data-ttu-id="ddb71-138">O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.</span><span class="sxs-lookup"><span data-stu-id="ddb71-138">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="ddb71-139">**Controle de serviço inválido**</span><span class="sxs-lookup"><span data-stu-id="ddb71-139">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="ddb71-140">4</span><span class="sxs-lookup"><span data-stu-id="ddb71-140">4</span></span>

<span data-ttu-id="ddb71-141">O código de controle pedido não é válido ou é inaceitável para o serviço.</span><span class="sxs-lookup"><span data-stu-id="ddb71-141">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="ddb71-142">**O serviço não pode aceitar o controle**</span><span class="sxs-lookup"><span data-stu-id="ddb71-142">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="ddb71-143">5</span><span class="sxs-lookup"><span data-stu-id="ddb71-143">5</span></span>

<span data-ttu-id="ddb71-144">O código de controle solicitado não pode ser enviado ao serviço porque o estado do serviço ([**Win32 \_ BaseService**](win32-baseservice.md).\*\*\*\* A propriedade State) é igual a 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="ddb71-144">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="ddb71-145">**Serviço não ativo**</span><span class="sxs-lookup"><span data-stu-id="ddb71-145">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="ddb71-146">6</span><span class="sxs-lookup"><span data-stu-id="ddb71-146">6</span></span>

<span data-ttu-id="ddb71-147">O serviço não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="ddb71-147">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="ddb71-148">**Tempo limite da solicitação de serviço**</span><span class="sxs-lookup"><span data-stu-id="ddb71-148">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="ddb71-149">7</span><span class="sxs-lookup"><span data-stu-id="ddb71-149">7</span></span>

<span data-ttu-id="ddb71-150">O serviço não respondeu à solicitação de início em um tempo oportuno.</span><span class="sxs-lookup"><span data-stu-id="ddb71-150">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="ddb71-151">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="ddb71-151">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="ddb71-152">8</span><span class="sxs-lookup"><span data-stu-id="ddb71-152">8</span></span>

<span data-ttu-id="ddb71-153">Falha desconhecida ao iniciar o serviço.</span><span class="sxs-lookup"><span data-stu-id="ddb71-153">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="ddb71-154">**Caminho não encontrado**</span><span class="sxs-lookup"><span data-stu-id="ddb71-154">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="ddb71-155">9</span><span class="sxs-lookup"><span data-stu-id="ddb71-155">9</span></span>

<span data-ttu-id="ddb71-156">O caminho do diretório para o arquivo executável do serviço não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="ddb71-156">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="ddb71-157">**Serviço já em execução**</span><span class="sxs-lookup"><span data-stu-id="ddb71-157">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="ddb71-158">10</span><span class="sxs-lookup"><span data-stu-id="ddb71-158">10</span></span>

<span data-ttu-id="ddb71-159">O serviço já está em execução.</span><span class="sxs-lookup"><span data-stu-id="ddb71-159">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="ddb71-160">**Banco de dados de serviço bloqueado**</span><span class="sxs-lookup"><span data-stu-id="ddb71-160">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="ddb71-161">11</span><span class="sxs-lookup"><span data-stu-id="ddb71-161">11</span></span>

<span data-ttu-id="ddb71-162">O banco de dados para adicionar um serviço novo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="ddb71-162">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="ddb71-163">**Dependência de serviço excluída**</span><span class="sxs-lookup"><span data-stu-id="ddb71-163">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="ddb71-164">12</span><span class="sxs-lookup"><span data-stu-id="ddb71-164">12</span></span>

<span data-ttu-id="ddb71-165">Uma dependência da qual esse serviço depende foi removida do sistema.</span><span class="sxs-lookup"><span data-stu-id="ddb71-165">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ddb71-166">**Falha na dependência de serviço**</span><span class="sxs-lookup"><span data-stu-id="ddb71-166">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="ddb71-167">13</span><span class="sxs-lookup"><span data-stu-id="ddb71-167">13</span></span>

<span data-ttu-id="ddb71-168">O serviço não localizou o serviço necessário em um serviço dependente.</span><span class="sxs-lookup"><span data-stu-id="ddb71-168">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="ddb71-169">**Serviço desabilitado**</span><span class="sxs-lookup"><span data-stu-id="ddb71-169">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="ddb71-170">14</span><span class="sxs-lookup"><span data-stu-id="ddb71-170">14</span></span>

<span data-ttu-id="ddb71-171">O serviço foi desabilitado do sistema.</span><span class="sxs-lookup"><span data-stu-id="ddb71-171">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ddb71-172">**Falha no logon do serviço**</span><span class="sxs-lookup"><span data-stu-id="ddb71-172">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="ddb71-173">15</span><span class="sxs-lookup"><span data-stu-id="ddb71-173">15</span></span>

<span data-ttu-id="ddb71-174">O serviço não tem a autenticação correta para ser executado no sistema.</span><span class="sxs-lookup"><span data-stu-id="ddb71-174">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="ddb71-175">**Serviço marcado para exclusão**</span><span class="sxs-lookup"><span data-stu-id="ddb71-175">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="ddb71-176">16</span><span class="sxs-lookup"><span data-stu-id="ddb71-176">16</span></span>

<span data-ttu-id="ddb71-177">Este serviço está sendo removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="ddb71-177">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ddb71-178">**Serviço sem thread**</span><span class="sxs-lookup"><span data-stu-id="ddb71-178">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="ddb71-179">17</span><span class="sxs-lookup"><span data-stu-id="ddb71-179">17</span></span>

<span data-ttu-id="ddb71-180">O serviço não tem nenhum thread de execução.</span><span class="sxs-lookup"><span data-stu-id="ddb71-180">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="ddb71-181">**Dependência circular de status**</span><span class="sxs-lookup"><span data-stu-id="ddb71-181">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="ddb71-182">18</span><span class="sxs-lookup"><span data-stu-id="ddb71-182">18</span></span>

<span data-ttu-id="ddb71-183">O serviço tem dependências circulares quando é iniciado.</span><span class="sxs-lookup"><span data-stu-id="ddb71-183">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="ddb71-184">**Nome duplicado de status**</span><span class="sxs-lookup"><span data-stu-id="ddb71-184">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="ddb71-185">19</span><span class="sxs-lookup"><span data-stu-id="ddb71-185">19</span></span>

<span data-ttu-id="ddb71-186">Um serviço está sendo executado com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="ddb71-186">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="ddb71-187">**Nome inválido do status**</span><span class="sxs-lookup"><span data-stu-id="ddb71-187">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="ddb71-188">20</span><span class="sxs-lookup"><span data-stu-id="ddb71-188">20</span></span>

<span data-ttu-id="ddb71-189">O nome do serviço tem caracteres inválidos.</span><span class="sxs-lookup"><span data-stu-id="ddb71-189">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="ddb71-190">**Parâmetro de status inválido**</span><span class="sxs-lookup"><span data-stu-id="ddb71-190">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="ddb71-191">21</span><span class="sxs-lookup"><span data-stu-id="ddb71-191">21</span></span>

<span data-ttu-id="ddb71-192">Parâmetros inválidos foram passados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="ddb71-192">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="ddb71-193">**Conta de serviço inválida de status**</span><span class="sxs-lookup"><span data-stu-id="ddb71-193">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="ddb71-194">22</span><span class="sxs-lookup"><span data-stu-id="ddb71-194">22</span></span>

<span data-ttu-id="ddb71-195">A conta sob a qual este serviço é executado é inválida ou não tem as permissões para executar o serviço.</span><span class="sxs-lookup"><span data-stu-id="ddb71-195">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="ddb71-196">**O serviço de status existe**</span><span class="sxs-lookup"><span data-stu-id="ddb71-196">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="ddb71-197">23</span><span class="sxs-lookup"><span data-stu-id="ddb71-197">23</span></span>

<span data-ttu-id="ddb71-198">O serviço existe no banco de dados de serviços disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="ddb71-198">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ddb71-199">**O serviço já está em pausa**</span><span class="sxs-lookup"><span data-stu-id="ddb71-199">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="ddb71-200">24</span><span class="sxs-lookup"><span data-stu-id="ddb71-200">24</span></span>

<span data-ttu-id="ddb71-201">O serviço está pausado atualmente no sistema.</span><span class="sxs-lookup"><span data-stu-id="ddb71-201">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="ddb71-202">**Outras**</span><span class="sxs-lookup"><span data-stu-id="ddb71-202">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="ddb71-203">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="ddb71-203">25 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="ddb71-204">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ddb71-204">Examples</span></span>

<span data-ttu-id="ddb71-205">A seguinte [alteração de StartMode de um exemplo do](https://Gallery.TechNet.Microsoft.Com/6d0f06ed-f840-4228-ad2d-e16ebe6a3aed) PowerShell de serviço, extraído da galeria do TechNet, altera o modo de início de um serviço.</span><span class="sxs-lookup"><span data-stu-id="ddb71-205">The following [Change StartMode of a Service](https://Gallery.TechNet.Microsoft.Com/6d0f06ed-f840-4228-ad2d-e16ebe6a3aed) PowerShell sample, pulled from TechNet Gallery, changes the start mode of a service.</span></span>


```PowerShell
$wmi = get-wmiobject -class win32_service -namespace root\cimv2 -computername lisbon | 
where-object { $_.name -eq 'bits' } 
 
$rtn = $wmi.changestartmode("manual") 
if($rtn.returnvalue -eq 0) { "success" } 
ELSE 
  { " $($rtn.returnvalue) was reported" }
```



## <a name="requirements"></a><span data-ttu-id="ddb71-206">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ddb71-206">Requirements</span></span>



| <span data-ttu-id="ddb71-207">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddb71-207">Requirement</span></span> | <span data-ttu-id="ddb71-208">Valor</span><span class="sxs-lookup"><span data-stu-id="ddb71-208">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ddb71-209">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ddb71-209">Minimum supported client</span></span><br/> | <span data-ttu-id="ddb71-210">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ddb71-210">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ddb71-211">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ddb71-211">Minimum supported server</span></span><br/> | <span data-ttu-id="ddb71-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ddb71-212">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ddb71-213">Namespace</span><span class="sxs-lookup"><span data-stu-id="ddb71-213">Namespace</span></span><br/>                | <span data-ttu-id="ddb71-214">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ddb71-214">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ddb71-215">MOF</span><span class="sxs-lookup"><span data-stu-id="ddb71-215">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ddb71-216"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ddb71-216"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ddb71-217">DLL</span><span class="sxs-lookup"><span data-stu-id="ddb71-217">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ddb71-218"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ddb71-218"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddb71-219">Confira também</span><span class="sxs-lookup"><span data-stu-id="ddb71-219">See also</span></span>

<dl> <dt>

<span data-ttu-id="ddb71-220">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ddb71-220">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ddb71-221">**\_Serviço Win32**</span><span class="sxs-lookup"><span data-stu-id="ddb71-221">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="ddb71-222">Tarefas do WMI: serviços</span><span class="sxs-lookup"><span data-stu-id="ddb71-222">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 


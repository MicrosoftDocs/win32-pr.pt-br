---
description: Tenta enviar um código de controle definido pelo usuário para um serviço.
ms.assetid: d181dbf8-e1ad-47b2-9e64-4aabc77e64bd
ms.tgt_platform: multiple
title: Método UserControlService da classe Win32_BaseService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.UserControlService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 55647524c8ba561716441976fe6654b933e1900b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826629"
---
# <a name="usercontrolservice-method-of-the-win32_baseservice-class"></a><span data-ttu-id="9fb41-103">Método UserControlService da classe Win32 \_ BaseService</span><span class="sxs-lookup"><span data-stu-id="9fb41-103">UserControlService method of the Win32\_BaseService class</span></span>

<span data-ttu-id="9fb41-104">O método da [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) tenta enviar um código de controle definido pelo usuário para um serviço.</span><span class="sxs-lookup"><span data-stu-id="9fb41-104">The [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to send a user-defined control code to a service.</span></span>

<span data-ttu-id="9fb41-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="9fb41-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9fb41-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="9fb41-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9fb41-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9fb41-107">Syntax</span></span>


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a><span data-ttu-id="9fb41-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9fb41-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fb41-109">*ControlCode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9fb41-109">*ControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fb41-110">Valor que especifica um comando de controle para um serviço.</span><span class="sxs-lookup"><span data-stu-id="9fb41-110">Value that specifies a control command to a service.</span></span> <span data-ttu-id="9fb41-111">Por exemplo, um comando de controle é um comando "Pause" ou "Continue".</span><span class="sxs-lookup"><span data-stu-id="9fb41-111">For example a control command is a "pause" or "continue" command.</span></span> <span data-ttu-id="9fb41-112">O valor pode ser um código predefinido ou um valor e uma ação que o serviço define.</span><span class="sxs-lookup"><span data-stu-id="9fb41-112">The value can be a predefined code, or a value and action that the service defines.</span></span> <span data-ttu-id="9fb41-113">Estes são os códigos de controle predefinidos:</span><span class="sxs-lookup"><span data-stu-id="9fb41-113">The following are the predefined control codes:</span></span>

<dt>

<span id="SERVICE_CONTROL_CONTINUE"></span><span id="service_control_continue"></span>

<span data-ttu-id="9fb41-114"><span id="SERVICE_CONTROL_CONTINUE"></span><span id="service_control_continue"></span>**\_continuação do controle de serviço \_**</span><span class="sxs-lookup"><span data-stu-id="9fb41-114"><span id="SERVICE_CONTROL_CONTINUE"></span><span id="service_control_continue"></span>**SERVICE\_CONTROL\_CONTINUE**</span></span>


</dt> <dd>

<span data-ttu-id="9fb41-115">Notifica um serviço em pausa para retomar.</span><span class="sxs-lookup"><span data-stu-id="9fb41-115">Notifies a paused service to resume.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_INTERROGATE"></span><span id="service_control_interrogate"></span>

<span data-ttu-id="9fb41-116"><span id="SERVICE_CONTROL_INTERROGATE"></span><span id="service_control_interrogate"></span>**\_interrogação de controle de serviço \_**</span><span class="sxs-lookup"><span data-stu-id="9fb41-116"><span id="SERVICE_CONTROL_INTERROGATE"></span><span id="service_control_interrogate"></span>**SERVICE\_CONTROL\_INTERROGATE**</span></span>


</dt> <dd>

<span data-ttu-id="9fb41-117">Notifica um serviço para relatar as informações de status atuais para o Gerenciador de controle de serviço.</span><span class="sxs-lookup"><span data-stu-id="9fb41-117">Notifies a service to report the current status information to the service control manager.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDADD"></span><span id="service_control_netbindadd"></span>

<span data-ttu-id="9fb41-118"><span id="SERVICE_CONTROL_NETBINDADD"></span><span id="service_control_netbindadd"></span>**\_NETBINDADD de controle de serviço \_**</span><span class="sxs-lookup"><span data-stu-id="9fb41-118"><span id="SERVICE_CONTROL_NETBINDADD"></span><span id="service_control_netbindadd"></span>**SERVICE\_CONTROL\_NETBINDADD**</span></span>


</dt> <dd>

<span data-ttu-id="9fb41-119">Notifica um serviço de rede que há um novo componente para associação.</span><span class="sxs-lookup"><span data-stu-id="9fb41-119">Notifies a network service that there is a new component for binding.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDDISABLE"></span><span id="service_control_netbinddisable"></span>

<span data-ttu-id="9fb41-120"><span id="SERVICE_CONTROL_NETBINDDISABLE"></span><span id="service_control_netbinddisable"></span>**\_NETBINDDISABLE de controle de serviço \_**</span><span class="sxs-lookup"><span data-stu-id="9fb41-120"><span id="SERVICE_CONTROL_NETBINDDISABLE"></span><span id="service_control_netbinddisable"></span>**SERVICE\_CONTROL\_NETBINDDISABLE**</span></span>


</dt> <dd>

<span data-ttu-id="9fb41-121">Notifica um serviço de rede que uma de suas associações está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="9fb41-121">Notifies a network service that one of its bindings is disabled.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDENABLE"></span><span id="service_control_netbindenable"></span>

<span data-ttu-id="9fb41-122"><span id="SERVICE_CONTROL_NETBINDENABLE"></span><span id="service_control_netbindenable"></span>**\_NETBINDENABLE de controle de serviço \_**</span><span class="sxs-lookup"><span data-stu-id="9fb41-122"><span id="SERVICE_CONTROL_NETBINDENABLE"></span><span id="service_control_netbindenable"></span>**SERVICE\_CONTROL\_NETBINDENABLE**</span></span>


</dt> <dd>

<span data-ttu-id="9fb41-123">Notifica um serviço de rede de que uma associação desabilitada está habilitada.</span><span class="sxs-lookup"><span data-stu-id="9fb41-123">Notifies a network service that a disabled binding is enabled.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDREMOVE"></span><span id="service_control_netbindremove"></span>

<span data-ttu-id="9fb41-124"><span id="SERVICE_CONTROL_NETBINDREMOVE"></span><span id="service_control_netbindremove"></span>**\_NETBINDREMOVE de controle de serviço \_**</span><span class="sxs-lookup"><span data-stu-id="9fb41-124"><span id="SERVICE_CONTROL_NETBINDREMOVE"></span><span id="service_control_netbindremove"></span>**SERVICE\_CONTROL\_NETBINDREMOVE**</span></span>


</dt> <dd>

<span data-ttu-id="9fb41-125">Notifica um serviço de rede que um componente para associação foi removido.</span><span class="sxs-lookup"><span data-stu-id="9fb41-125">Notifies a network service that a component for binding has been removed.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_PARAMCHANGE"></span><span id="service_control_paramchange"></span>

<span data-ttu-id="9fb41-126"><span id="SERVICE_CONTROL_PARAMCHANGE"></span><span id="service_control_paramchange"></span>**\_PARAMCHANGE de controle de serviço \_**</span><span class="sxs-lookup"><span data-stu-id="9fb41-126"><span id="SERVICE_CONTROL_PARAMCHANGE"></span><span id="service_control_paramchange"></span>**SERVICE\_CONTROL\_PARAMCHANGE**</span></span>


</dt> <dd>

<span data-ttu-id="9fb41-127">Notifica um serviço de que seus parâmetros de inicialização são alterados.</span><span class="sxs-lookup"><span data-stu-id="9fb41-127">Notifies a service that its startup parameters are changed.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_PAUSE"></span><span id="service_control_pause"></span>

<span data-ttu-id="9fb41-128"><span id="SERVICE_CONTROL_PAUSE"></span><span id="service_control_pause"></span>**\_pausa de controle de serviço \_**</span><span class="sxs-lookup"><span data-stu-id="9fb41-128"><span id="SERVICE_CONTROL_PAUSE"></span><span id="service_control_pause"></span>**SERVICE\_CONTROL\_PAUSE**</span></span>


</dt> <dd>

<span data-ttu-id="9fb41-129">Notifica um serviço para pausar.</span><span class="sxs-lookup"><span data-stu-id="9fb41-129">Notifies a service to pause.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_STOP"></span><span id="service_control_stop"></span>

<span data-ttu-id="9fb41-130"><span id="SERVICE_CONTROL_STOP"></span><span id="service_control_stop"></span>**\_parada de controle de serviço \_**</span><span class="sxs-lookup"><span data-stu-id="9fb41-130"><span id="SERVICE_CONTROL_STOP"></span><span id="service_control_stop"></span>**SERVICE\_CONTROL\_STOP**</span></span>


</dt> <dd>

<span data-ttu-id="9fb41-131">Notifica um serviço para parar.</span><span class="sxs-lookup"><span data-stu-id="9fb41-131">Notifies a service to stop.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fb41-132">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9fb41-132">Return value</span></span>

<span data-ttu-id="9fb41-133">Retorna um dos valores listados na lista a seguir ou um valor diferente para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="9fb41-133">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="9fb41-134">**Êxito**</span><span class="sxs-lookup"><span data-stu-id="9fb41-134">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="9fb41-135">0</span><span class="sxs-lookup"><span data-stu-id="9fb41-135">0</span></span>

<span data-ttu-id="9fb41-136">A solicitação é aceita.</span><span class="sxs-lookup"><span data-stu-id="9fb41-136">The request is accepted.</span></span>

</dd> <dt>

<span data-ttu-id="9fb41-137">**Sem suporte**</span><span class="sxs-lookup"><span data-stu-id="9fb41-137">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="9fb41-138">1</span><span class="sxs-lookup"><span data-stu-id="9fb41-138">1</span></span>

<span data-ttu-id="9fb41-139">A solicitação não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="9fb41-139">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="9fb41-140">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="9fb41-140">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="9fb41-141">2</span><span class="sxs-lookup"><span data-stu-id="9fb41-141">2</span></span>

<span data-ttu-id="9fb41-142">O usuário não tem os direitos de acesso necessários.</span><span class="sxs-lookup"><span data-stu-id="9fb41-142">The user does not have the necessary access rights.</span></span>

</dd> <dt>

<span data-ttu-id="9fb41-143">**Serviços dependentes em execução**</span><span class="sxs-lookup"><span data-stu-id="9fb41-143">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="9fb41-144">3</span><span class="sxs-lookup"><span data-stu-id="9fb41-144">3</span></span>

<span data-ttu-id="9fb41-145">O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.</span><span class="sxs-lookup"><span data-stu-id="9fb41-145">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="9fb41-146">**Controle de serviço inválido**</span><span class="sxs-lookup"><span data-stu-id="9fb41-146">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="9fb41-147">4</span><span class="sxs-lookup"><span data-stu-id="9fb41-147">4</span></span>

<span data-ttu-id="9fb41-148">O código de controle pedido não é válido ou é inaceitável para o serviço.</span><span class="sxs-lookup"><span data-stu-id="9fb41-148">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="9fb41-149">**O serviço não pode aceitar o controle**</span><span class="sxs-lookup"><span data-stu-id="9fb41-149">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="9fb41-150">5</span><span class="sxs-lookup"><span data-stu-id="9fb41-150">5</span></span>

<span data-ttu-id="9fb41-151">O código de controle solicitado não pode ser enviado ao serviço porque o estado do serviço ([**Win32 \_ BaseService**](win32-baseservice.md).\*\*\*\* A propriedade State) é igual a 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="9fb41-151">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="9fb41-152">**Serviço não ativo**</span><span class="sxs-lookup"><span data-stu-id="9fb41-152">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="9fb41-153">6</span><span class="sxs-lookup"><span data-stu-id="9fb41-153">6</span></span>

<span data-ttu-id="9fb41-154">O serviço não iniciou.</span><span class="sxs-lookup"><span data-stu-id="9fb41-154">The service has not started.</span></span>

</dd> <dt>

<span data-ttu-id="9fb41-155">**Tempo limite da solicitação de serviço**</span><span class="sxs-lookup"><span data-stu-id="9fb41-155">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="9fb41-156">7</span><span class="sxs-lookup"><span data-stu-id="9fb41-156">7</span></span>

<span data-ttu-id="9fb41-157">O serviço não responde à solicitação de início rapidamente.</span><span class="sxs-lookup"><span data-stu-id="9fb41-157">The service does not respond to the start request quickly.</span></span>

</dd> <dt>

<span data-ttu-id="9fb41-158">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="9fb41-158">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="9fb41-159">8</span><span class="sxs-lookup"><span data-stu-id="9fb41-159">8</span></span>

<span data-ttu-id="9fb41-160">Processo interativo.</span><span class="sxs-lookup"><span data-stu-id="9fb41-160">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="9fb41-161">**Caminho não encontrado**</span><span class="sxs-lookup"><span data-stu-id="9fb41-161">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="9fb41-162">9</span><span class="sxs-lookup"><span data-stu-id="9fb41-162">9</span></span>

<span data-ttu-id="9fb41-163">O caminho do diretório para o arquivo executável do serviço não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="9fb41-163">The directory path to the service executable file is not found.</span></span>

</dd> <dt>

<span data-ttu-id="9fb41-164">**Serviço já em execução**</span><span class="sxs-lookup"><span data-stu-id="9fb41-164">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="9fb41-165">10</span><span class="sxs-lookup"><span data-stu-id="9fb41-165">10</span></span>

<span data-ttu-id="9fb41-166">O serviço já está em execução.</span><span class="sxs-lookup"><span data-stu-id="9fb41-166">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="9fb41-167">**Banco de dados de serviço bloqueado**</span><span class="sxs-lookup"><span data-stu-id="9fb41-167">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="9fb41-168">11</span><span class="sxs-lookup"><span data-stu-id="9fb41-168">11</span></span>

<span data-ttu-id="9fb41-169">O banco de dados para adicionar um serviço novo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="9fb41-169">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="9fb41-170">**Dependência de serviço excluída**</span><span class="sxs-lookup"><span data-stu-id="9fb41-170">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="9fb41-171">12</span><span class="sxs-lookup"><span data-stu-id="9fb41-171">12</span></span>

<span data-ttu-id="9fb41-172">Uma dependência da qual esse serviço depende é removida do sistema.</span><span class="sxs-lookup"><span data-stu-id="9fb41-172">A dependency that this service relies on is removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="9fb41-173">**Falha na dependência de serviço**</span><span class="sxs-lookup"><span data-stu-id="9fb41-173">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="9fb41-174">13</span><span class="sxs-lookup"><span data-stu-id="9fb41-174">13</span></span>

<span data-ttu-id="9fb41-175">O serviço não encontra o serviço necessário de um serviço dependente.</span><span class="sxs-lookup"><span data-stu-id="9fb41-175">The service does not find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="9fb41-176">**Serviço desabilitado**</span><span class="sxs-lookup"><span data-stu-id="9fb41-176">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="9fb41-177">14</span><span class="sxs-lookup"><span data-stu-id="9fb41-177">14</span></span>

<span data-ttu-id="9fb41-178">O serviço está desabilitado no sistema.</span><span class="sxs-lookup"><span data-stu-id="9fb41-178">The service is disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="9fb41-179">**Falha no logon do serviço**</span><span class="sxs-lookup"><span data-stu-id="9fb41-179">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="9fb41-180">15</span><span class="sxs-lookup"><span data-stu-id="9fb41-180">15</span></span>

<span data-ttu-id="9fb41-181">O serviço não tem a autenticação correta para ser executado no sistema.</span><span class="sxs-lookup"><span data-stu-id="9fb41-181">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="9fb41-182">**Serviço marcado para exclusão**</span><span class="sxs-lookup"><span data-stu-id="9fb41-182">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="9fb41-183">16</span><span class="sxs-lookup"><span data-stu-id="9fb41-183">16</span></span>

<span data-ttu-id="9fb41-184">O serviço está sendo removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="9fb41-184">The service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="9fb41-185">**Serviço sem thread**</span><span class="sxs-lookup"><span data-stu-id="9fb41-185">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="9fb41-186">17</span><span class="sxs-lookup"><span data-stu-id="9fb41-186">17</span></span>

<span data-ttu-id="9fb41-187">Não há nenhum thread de execução para o serviço.</span><span class="sxs-lookup"><span data-stu-id="9fb41-187">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="9fb41-188">**Dependência circular de status**</span><span class="sxs-lookup"><span data-stu-id="9fb41-188">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="9fb41-189">18</span><span class="sxs-lookup"><span data-stu-id="9fb41-189">18</span></span>

<span data-ttu-id="9fb41-190">Há dependências circulares quando o serviço é iniciado.</span><span class="sxs-lookup"><span data-stu-id="9fb41-190">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="9fb41-191">**Nome duplicado de status**</span><span class="sxs-lookup"><span data-stu-id="9fb41-191">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="9fb41-192">19</span><span class="sxs-lookup"><span data-stu-id="9fb41-192">19</span></span>

<span data-ttu-id="9fb41-193">Há um serviço em execução com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="9fb41-193">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="9fb41-194">**Nome inválido do status**</span><span class="sxs-lookup"><span data-stu-id="9fb41-194">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="9fb41-195">20</span><span class="sxs-lookup"><span data-stu-id="9fb41-195">20</span></span>

<span data-ttu-id="9fb41-196">Há caracteres inválidos no nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="9fb41-196">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="9fb41-197">**Parâmetro de status inválido**</span><span class="sxs-lookup"><span data-stu-id="9fb41-197">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="9fb41-198">21</span><span class="sxs-lookup"><span data-stu-id="9fb41-198">21</span></span>

<span data-ttu-id="9fb41-199">Parâmetros inválidos foram passados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="9fb41-199">Invalid parameters have passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="9fb41-200">**Conta de serviço inválida de status**</span><span class="sxs-lookup"><span data-stu-id="9fb41-200">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="9fb41-201">22</span><span class="sxs-lookup"><span data-stu-id="9fb41-201">22</span></span>

<span data-ttu-id="9fb41-202">A conta em que esse serviço é executado não é válida ou não tem as permissões para executar o serviço.</span><span class="sxs-lookup"><span data-stu-id="9fb41-202">The account that this service runs under is not valid or does not have the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="9fb41-203">**O serviço de status existe**</span><span class="sxs-lookup"><span data-stu-id="9fb41-203">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="9fb41-204">23</span><span class="sxs-lookup"><span data-stu-id="9fb41-204">23</span></span>

<span data-ttu-id="9fb41-205">O serviço existe no banco de dados de serviços disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="9fb41-205">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="9fb41-206">**O serviço já está em pausa**</span><span class="sxs-lookup"><span data-stu-id="9fb41-206">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="9fb41-207">24</span><span class="sxs-lookup"><span data-stu-id="9fb41-207">24</span></span>

<span data-ttu-id="9fb41-208">O serviço está pausado atualmente no sistema.</span><span class="sxs-lookup"><span data-stu-id="9fb41-208">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="9fb41-209">**Outras**</span><span class="sxs-lookup"><span data-stu-id="9fb41-209">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="9fb41-210">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="9fb41-210">25 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9fb41-211">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fb41-211">Requirements</span></span>



| <span data-ttu-id="9fb41-212">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fb41-212">Requirement</span></span> | <span data-ttu-id="9fb41-213">Valor</span><span class="sxs-lookup"><span data-stu-id="9fb41-213">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9fb41-214">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9fb41-214">Minimum supported client</span></span><br/> | <span data-ttu-id="9fb41-215">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9fb41-215">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9fb41-216">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9fb41-216">Minimum supported server</span></span><br/> | <span data-ttu-id="9fb41-217">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9fb41-217">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9fb41-218">Namespace</span><span class="sxs-lookup"><span data-stu-id="9fb41-218">Namespace</span></span><br/>                | <span data-ttu-id="9fb41-219">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9fb41-219">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9fb41-220">MOF</span><span class="sxs-lookup"><span data-stu-id="9fb41-220">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9fb41-221"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9fb41-221"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9fb41-222">DLL</span><span class="sxs-lookup"><span data-stu-id="9fb41-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fb41-223"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fb41-223"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fb41-224">Confira também</span><span class="sxs-lookup"><span data-stu-id="9fb41-224">See also</span></span>

<dl> <dt>

<span data-ttu-id="9fb41-225">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9fb41-225">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9fb41-226">**\_BaseService Win32**</span><span class="sxs-lookup"><span data-stu-id="9fb41-226">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 


---
description: Modifica o modo de início de um objeto de serviço derivado do Win32 \_ BaseService.
ms.assetid: 33040632-6c04-4084-af09-8e1b8bc29090
ms.tgt_platform: multiple
title: Método ChangeStartMode da classe Win32_BaseService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.ChangeStartMode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9877300a2135b7082677193696cd2d11811ab3dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089167"
---
# <a name="changestartmode-method-of-the-win32_baseservice-class"></a><span data-ttu-id="e9f67-103">Método ChangeStartMode da classe Win32 \_ BaseService</span><span class="sxs-lookup"><span data-stu-id="e9f67-103">ChangeStartMode method of the Win32\_BaseService class</span></span>

<span data-ttu-id="e9f67-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeStartMode** modifica o modo de início de um objeto de serviço derivado de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="e9f67-104">The **ChangeStartMode** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies the start mode of a service object derived from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="e9f67-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="e9f67-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e9f67-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e9f67-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e9f67-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e9f67-107">Syntax</span></span>


```mof
uint32 ChangeStartMode(
  [in] string StartMode = Auto Start
);
```



## <a name="parameters"></a><span data-ttu-id="e9f67-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e9f67-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9f67-109">*StartMode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e9f67-109">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9f67-110">Modo de início do serviço base do Windows.</span><span class="sxs-lookup"><span data-stu-id="e9f67-110">Start mode of the Windows base service.</span></span> <span data-ttu-id="e9f67-111">O padrão é "Automatic".</span><span class="sxs-lookup"><span data-stu-id="e9f67-111">The default is "Automatic".</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="e9f67-112"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Inicialização inicial** ("inicialização")</span><span class="sxs-lookup"><span data-stu-id="e9f67-112"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="e9f67-113">Driver de dispositivo iniciado pelo carregador do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="e9f67-113">Device driver started by the operating system loader.</span></span> <span data-ttu-id="e9f67-114">Esse valor só é válido para serviços do driver.</span><span class="sxs-lookup"><span data-stu-id="e9f67-114">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span data-ttu-id="e9f67-115"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**Início do sistema** ("sistema")</span><span class="sxs-lookup"><span data-stu-id="e9f67-115"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**System Start** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="e9f67-116">Driver de dispositivo iniciado pelo processo de inicialização do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="e9f67-116">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="e9f67-117">Esse valor só é válido para serviços do driver.</span><span class="sxs-lookup"><span data-stu-id="e9f67-117">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="e9f67-118"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Início automático** ("automático")</span><span class="sxs-lookup"><span data-stu-id="e9f67-118"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start** ("Automatic")</span></span>


</dt> <dd>

<span data-ttu-id="e9f67-119">Serviço a ser iniciado automaticamente pelo gerenciador de controle de serviço durante a inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="e9f67-119">Service to be started automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="e9f67-120"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Início da demanda** ("manual")</span><span class="sxs-lookup"><span data-stu-id="e9f67-120"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="e9f67-121">Serviço a ser iniciado pelo Gerenciador de controle de serviço quando um processo chama o método [**StartService**](startservice-method-in-class-win32-baseservice.md) .</span><span class="sxs-lookup"><span data-stu-id="e9f67-121">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-baseservice.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e9f67-122"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("desabilitado")</span><span class="sxs-lookup"><span data-stu-id="e9f67-122"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="e9f67-123">O serviço está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="e9f67-123">Service is disabled.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9f67-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e9f67-124">Return value</span></span>

<span data-ttu-id="e9f67-125">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="e9f67-125">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="e9f67-126">**Êxito**</span><span class="sxs-lookup"><span data-stu-id="e9f67-126">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="e9f67-127">0</span><span class="sxs-lookup"><span data-stu-id="e9f67-127">0</span></span>

<span data-ttu-id="e9f67-128">A solicitação foi aceita.</span><span class="sxs-lookup"><span data-stu-id="e9f67-128">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="e9f67-129">**Sem suporte**</span><span class="sxs-lookup"><span data-stu-id="e9f67-129">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="e9f67-130">1</span><span class="sxs-lookup"><span data-stu-id="e9f67-130">1</span></span>

<span data-ttu-id="e9f67-131">A solicitação não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="e9f67-131">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="e9f67-132">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="e9f67-132">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="e9f67-133">2</span><span class="sxs-lookup"><span data-stu-id="e9f67-133">2</span></span>

<span data-ttu-id="e9f67-134">O usuário não tinha o acesso necessário.</span><span class="sxs-lookup"><span data-stu-id="e9f67-134">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="e9f67-135">**Serviços dependentes em execução**</span><span class="sxs-lookup"><span data-stu-id="e9f67-135">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="e9f67-136">3</span><span class="sxs-lookup"><span data-stu-id="e9f67-136">3</span></span>

<span data-ttu-id="e9f67-137">O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.</span><span class="sxs-lookup"><span data-stu-id="e9f67-137">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="e9f67-138">**Controle de serviço inválido**</span><span class="sxs-lookup"><span data-stu-id="e9f67-138">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="e9f67-139">4</span><span class="sxs-lookup"><span data-stu-id="e9f67-139">4</span></span>

<span data-ttu-id="e9f67-140">O código de controle pedido não é válido ou é inaceitável para o serviço.</span><span class="sxs-lookup"><span data-stu-id="e9f67-140">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="e9f67-141">**O serviço não pode aceitar o controle**</span><span class="sxs-lookup"><span data-stu-id="e9f67-141">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="e9f67-142">5</span><span class="sxs-lookup"><span data-stu-id="e9f67-142">5</span></span>

<span data-ttu-id="e9f67-143">O código de controle solicitado não pode ser enviado ao serviço porque o estado do serviço (Propriedade de [**estado**](win32-baseservice.md) [**\_ BaseService do Win32**](win32-baseservice.md)) é igual a 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="e9f67-143">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md)[**State**](win32-baseservice.md) property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="e9f67-144">**Serviço não ativo**</span><span class="sxs-lookup"><span data-stu-id="e9f67-144">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="e9f67-145">6</span><span class="sxs-lookup"><span data-stu-id="e9f67-145">6</span></span>

<span data-ttu-id="e9f67-146">O serviço não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="e9f67-146">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="e9f67-147">**Tempo limite da solicitação de serviço**</span><span class="sxs-lookup"><span data-stu-id="e9f67-147">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="e9f67-148">7</span><span class="sxs-lookup"><span data-stu-id="e9f67-148">7</span></span>

<span data-ttu-id="e9f67-149">O serviço não respondeu à solicitação de início em um tempo oportuno.</span><span class="sxs-lookup"><span data-stu-id="e9f67-149">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="e9f67-150">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="e9f67-150">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="e9f67-151">8</span><span class="sxs-lookup"><span data-stu-id="e9f67-151">8</span></span>

<span data-ttu-id="e9f67-152">Processo interativo.</span><span class="sxs-lookup"><span data-stu-id="e9f67-152">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="e9f67-153">**Caminho não encontrado**</span><span class="sxs-lookup"><span data-stu-id="e9f67-153">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="e9f67-154">9</span><span class="sxs-lookup"><span data-stu-id="e9f67-154">9</span></span>

<span data-ttu-id="e9f67-155">O caminho do diretório para o arquivo executável do serviço não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="e9f67-155">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="e9f67-156">**Serviço já em execução**</span><span class="sxs-lookup"><span data-stu-id="e9f67-156">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="e9f67-157">10</span><span class="sxs-lookup"><span data-stu-id="e9f67-157">10</span></span>

<span data-ttu-id="e9f67-158">O serviço já está em execução.</span><span class="sxs-lookup"><span data-stu-id="e9f67-158">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="e9f67-159">**Banco de dados de serviço bloqueado**</span><span class="sxs-lookup"><span data-stu-id="e9f67-159">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="e9f67-160">11</span><span class="sxs-lookup"><span data-stu-id="e9f67-160">11</span></span>

<span data-ttu-id="e9f67-161">O banco de dados para adicionar um serviço novo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="e9f67-161">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="e9f67-162">**Dependência de serviço excluída**</span><span class="sxs-lookup"><span data-stu-id="e9f67-162">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="e9f67-163">12</span><span class="sxs-lookup"><span data-stu-id="e9f67-163">12</span></span>

<span data-ttu-id="e9f67-164">Uma dependência da qual esse serviço depende foi removida do sistema.</span><span class="sxs-lookup"><span data-stu-id="e9f67-164">A dependency on which this service relies has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e9f67-165">**Falha na dependência de serviço**</span><span class="sxs-lookup"><span data-stu-id="e9f67-165">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="e9f67-166">13</span><span class="sxs-lookup"><span data-stu-id="e9f67-166">13</span></span>

<span data-ttu-id="e9f67-167">O serviço não localizou o serviço necessário em um serviço dependente.</span><span class="sxs-lookup"><span data-stu-id="e9f67-167">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="e9f67-168">**Serviço desabilitado**</span><span class="sxs-lookup"><span data-stu-id="e9f67-168">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="e9f67-169">14</span><span class="sxs-lookup"><span data-stu-id="e9f67-169">14</span></span>

<span data-ttu-id="e9f67-170">O serviço foi desabilitado do sistema.</span><span class="sxs-lookup"><span data-stu-id="e9f67-170">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e9f67-171">**Falha no logon do serviço**</span><span class="sxs-lookup"><span data-stu-id="e9f67-171">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="e9f67-172">15</span><span class="sxs-lookup"><span data-stu-id="e9f67-172">15</span></span>

<span data-ttu-id="e9f67-173">O serviço não tem a autenticação correta para ser executado no sistema.</span><span class="sxs-lookup"><span data-stu-id="e9f67-173">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="e9f67-174">**Serviço marcado para exclusão**</span><span class="sxs-lookup"><span data-stu-id="e9f67-174">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="e9f67-175">16</span><span class="sxs-lookup"><span data-stu-id="e9f67-175">16</span></span>

<span data-ttu-id="e9f67-176">Este serviço está sendo removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="e9f67-176">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e9f67-177">**Serviço sem thread**</span><span class="sxs-lookup"><span data-stu-id="e9f67-177">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="e9f67-178">17</span><span class="sxs-lookup"><span data-stu-id="e9f67-178">17</span></span>

<span data-ttu-id="e9f67-179">Não há nenhum thread de execução para o serviço.</span><span class="sxs-lookup"><span data-stu-id="e9f67-179">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="e9f67-180">**Dependência circular de status**</span><span class="sxs-lookup"><span data-stu-id="e9f67-180">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="e9f67-181">18</span><span class="sxs-lookup"><span data-stu-id="e9f67-181">18</span></span>

<span data-ttu-id="e9f67-182">Há dependências circulares quando o serviço é iniciado.</span><span class="sxs-lookup"><span data-stu-id="e9f67-182">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="e9f67-183">**Nome duplicado de status**</span><span class="sxs-lookup"><span data-stu-id="e9f67-183">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="e9f67-184">19</span><span class="sxs-lookup"><span data-stu-id="e9f67-184">19</span></span>

<span data-ttu-id="e9f67-185">Há um serviço em execução com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="e9f67-185">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="e9f67-186">**Nome inválido do status**</span><span class="sxs-lookup"><span data-stu-id="e9f67-186">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="e9f67-187">20</span><span class="sxs-lookup"><span data-stu-id="e9f67-187">20</span></span>

<span data-ttu-id="e9f67-188">Há caracteres inválidos no nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="e9f67-188">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="e9f67-189">**Parâmetro de status inválido**</span><span class="sxs-lookup"><span data-stu-id="e9f67-189">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="e9f67-190">21</span><span class="sxs-lookup"><span data-stu-id="e9f67-190">21</span></span>

<span data-ttu-id="e9f67-191">Parâmetros inválidos foram passados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="e9f67-191">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="e9f67-192">**Conta de serviço inválida de status**</span><span class="sxs-lookup"><span data-stu-id="e9f67-192">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="e9f67-193">22</span><span class="sxs-lookup"><span data-stu-id="e9f67-193">22</span></span>

<span data-ttu-id="e9f67-194">A conta na qual esse serviço deve ser executado é inválida ou não tem as permissões para executar o serviço.</span><span class="sxs-lookup"><span data-stu-id="e9f67-194">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="e9f67-195">**O serviço de status existe**</span><span class="sxs-lookup"><span data-stu-id="e9f67-195">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="e9f67-196">23</span><span class="sxs-lookup"><span data-stu-id="e9f67-196">23</span></span>

<span data-ttu-id="e9f67-197">O serviço existe no banco de dados de serviços disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="e9f67-197">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="e9f67-198">**O serviço já está em pausa**</span><span class="sxs-lookup"><span data-stu-id="e9f67-198">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="e9f67-199">24</span><span class="sxs-lookup"><span data-stu-id="e9f67-199">24</span></span>

<span data-ttu-id="e9f67-200">O serviço está pausado atualmente no sistema.</span><span class="sxs-lookup"><span data-stu-id="e9f67-200">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="e9f67-201">**Outras**</span><span class="sxs-lookup"><span data-stu-id="e9f67-201">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="e9f67-202">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="e9f67-202">25 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e9f67-203">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9f67-203">Requirements</span></span>



| <span data-ttu-id="e9f67-204">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9f67-204">Requirement</span></span> | <span data-ttu-id="e9f67-205">Valor</span><span class="sxs-lookup"><span data-stu-id="e9f67-205">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9f67-206">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9f67-206">Minimum supported client</span></span><br/> | <span data-ttu-id="e9f67-207">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e9f67-207">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e9f67-208">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9f67-208">Minimum supported server</span></span><br/> | <span data-ttu-id="e9f67-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9f67-209">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e9f67-210">Namespace</span><span class="sxs-lookup"><span data-stu-id="e9f67-210">Namespace</span></span><br/>                | <span data-ttu-id="e9f67-211">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e9f67-211">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e9f67-212">MOF</span><span class="sxs-lookup"><span data-stu-id="e9f67-212">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9f67-213"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9f67-213"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9f67-214">DLL</span><span class="sxs-lookup"><span data-stu-id="e9f67-214">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9f67-215"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9f67-215"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9f67-216">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9f67-216">See also</span></span>

<dl> <dt>

<span data-ttu-id="e9f67-217">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9f67-217">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e9f67-218">**\_BaseService Win32**</span><span class="sxs-lookup"><span data-stu-id="e9f67-218">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 


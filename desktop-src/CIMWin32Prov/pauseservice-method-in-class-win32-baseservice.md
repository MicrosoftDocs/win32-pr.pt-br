---
description: Tenta colocar o serviço referenciado no estado em pausa.
ms.assetid: 57b8ccdd-056a-4bec-a0f8-ecebcf18039e
ms.tgt_platform: multiple
title: Método PauseService da classe Win32_BaseService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.PauseService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4828b81af5d6d543aaf16a34a08350f09078d623
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762764"
---
# <a name="pauseservice-method-of-the-win32_baseservice-class"></a><span data-ttu-id="def14-103">Método PauseService da classe Win32 \_ BaseService</span><span class="sxs-lookup"><span data-stu-id="def14-103">PauseService method of the Win32\_BaseService class</span></span>

<span data-ttu-id="def14-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **PauseService** tenta colocar o serviço referenciado no estado pausado.</span><span class="sxs-lookup"><span data-stu-id="def14-104">The **PauseService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the referenced service in the paused state.</span></span>

<span data-ttu-id="def14-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="def14-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="def14-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="def14-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="def14-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="def14-107">Syntax</span></span>


```mof
uint32 PauseService();
```



## <a name="parameters"></a><span data-ttu-id="def14-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="def14-108">Parameters</span></span>

<span data-ttu-id="def14-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="def14-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="def14-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="def14-110">Return value</span></span>

<span data-ttu-id="def14-111">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="def14-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="def14-112">**Êxito**</span><span class="sxs-lookup"><span data-stu-id="def14-112">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="def14-113">0</span><span class="sxs-lookup"><span data-stu-id="def14-113">0</span></span>

<span data-ttu-id="def14-114">A solicitação foi aceita.</span><span class="sxs-lookup"><span data-stu-id="def14-114">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="def14-115">**Sem suporte**</span><span class="sxs-lookup"><span data-stu-id="def14-115">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="def14-116">1</span><span class="sxs-lookup"><span data-stu-id="def14-116">1</span></span>

<span data-ttu-id="def14-117">A solicitação não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="def14-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="def14-118">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="def14-118">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="def14-119">2</span><span class="sxs-lookup"><span data-stu-id="def14-119">2</span></span>

<span data-ttu-id="def14-120">O usuário não tinha o acesso necessário.</span><span class="sxs-lookup"><span data-stu-id="def14-120">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="def14-121">**Serviços dependentes em execução**</span><span class="sxs-lookup"><span data-stu-id="def14-121">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="def14-122">3</span><span class="sxs-lookup"><span data-stu-id="def14-122">3</span></span>

<span data-ttu-id="def14-123">O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.</span><span class="sxs-lookup"><span data-stu-id="def14-123">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="def14-124">**Controle de serviço inválido**</span><span class="sxs-lookup"><span data-stu-id="def14-124">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="def14-125">4</span><span class="sxs-lookup"><span data-stu-id="def14-125">4</span></span>

<span data-ttu-id="def14-126">O código de controle pedido não é válido ou é inaceitável para o serviço.</span><span class="sxs-lookup"><span data-stu-id="def14-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="def14-127">**O serviço não pode aceitar o controle**</span><span class="sxs-lookup"><span data-stu-id="def14-127">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="def14-128">5</span><span class="sxs-lookup"><span data-stu-id="def14-128">5</span></span>

<span data-ttu-id="def14-129">O código de controle solicitado não pode ser enviado ao serviço porque o estado do serviço (Propriedade de [**estado**](win32-baseservice.md) [**\_ BaseService do Win32**](win32-baseservice.md)) é igual a 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="def14-129">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md)[**State**](win32-baseservice.md) property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="def14-130">**Serviço não ativo**</span><span class="sxs-lookup"><span data-stu-id="def14-130">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="def14-131">6</span><span class="sxs-lookup"><span data-stu-id="def14-131">6</span></span>

<span data-ttu-id="def14-132">O serviço não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="def14-132">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="def14-133">**Tempo limite da solicitação de serviço**</span><span class="sxs-lookup"><span data-stu-id="def14-133">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="def14-134">7</span><span class="sxs-lookup"><span data-stu-id="def14-134">7</span></span>

<span data-ttu-id="def14-135">O serviço não respondeu à solicitação de início em um tempo oportuno.</span><span class="sxs-lookup"><span data-stu-id="def14-135">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="def14-136">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="def14-136">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="def14-137">8</span><span class="sxs-lookup"><span data-stu-id="def14-137">8</span></span>

<span data-ttu-id="def14-138">Processo interativo.</span><span class="sxs-lookup"><span data-stu-id="def14-138">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="def14-139">**Caminho não encontrado**</span><span class="sxs-lookup"><span data-stu-id="def14-139">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="def14-140">9</span><span class="sxs-lookup"><span data-stu-id="def14-140">9</span></span>

<span data-ttu-id="def14-141">O caminho do diretório para o arquivo executável do serviço não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="def14-141">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="def14-142">**Serviço já em execução**</span><span class="sxs-lookup"><span data-stu-id="def14-142">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="def14-143">10</span><span class="sxs-lookup"><span data-stu-id="def14-143">10</span></span>

<span data-ttu-id="def14-144">O serviço já está em execução.</span><span class="sxs-lookup"><span data-stu-id="def14-144">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="def14-145">**Banco de dados de serviço bloqueado**</span><span class="sxs-lookup"><span data-stu-id="def14-145">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="def14-146">11</span><span class="sxs-lookup"><span data-stu-id="def14-146">11</span></span>

<span data-ttu-id="def14-147">O banco de dados para adicionar um serviço novo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="def14-147">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="def14-148">**Dependência de serviço excluída**</span><span class="sxs-lookup"><span data-stu-id="def14-148">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="def14-149">12</span><span class="sxs-lookup"><span data-stu-id="def14-149">12</span></span>

<span data-ttu-id="def14-150">Uma dependência da qual esse serviço depende foi removida do sistema.</span><span class="sxs-lookup"><span data-stu-id="def14-150">A dependency on which this service relies has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="def14-151">**Falha na dependência de serviço**</span><span class="sxs-lookup"><span data-stu-id="def14-151">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="def14-152">13</span><span class="sxs-lookup"><span data-stu-id="def14-152">13</span></span>

<span data-ttu-id="def14-153">O serviço não localizou o serviço necessário em um serviço dependente.</span><span class="sxs-lookup"><span data-stu-id="def14-153">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="def14-154">**Serviço desabilitado**</span><span class="sxs-lookup"><span data-stu-id="def14-154">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="def14-155">14</span><span class="sxs-lookup"><span data-stu-id="def14-155">14</span></span>

<span data-ttu-id="def14-156">O serviço foi desabilitado do sistema.</span><span class="sxs-lookup"><span data-stu-id="def14-156">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="def14-157">**Falha no logon do serviço**</span><span class="sxs-lookup"><span data-stu-id="def14-157">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="def14-158">15</span><span class="sxs-lookup"><span data-stu-id="def14-158">15</span></span>

<span data-ttu-id="def14-159">O serviço não tem a autenticação correta para ser executado no sistema.</span><span class="sxs-lookup"><span data-stu-id="def14-159">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="def14-160">**Serviço marcado para exclusão**</span><span class="sxs-lookup"><span data-stu-id="def14-160">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="def14-161">16</span><span class="sxs-lookup"><span data-stu-id="def14-161">16</span></span>

<span data-ttu-id="def14-162">Este serviço está sendo removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="def14-162">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="def14-163">**Serviço sem thread**</span><span class="sxs-lookup"><span data-stu-id="def14-163">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="def14-164">17</span><span class="sxs-lookup"><span data-stu-id="def14-164">17</span></span>

<span data-ttu-id="def14-165">Não há nenhum thread de execução para o serviço.</span><span class="sxs-lookup"><span data-stu-id="def14-165">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="def14-166">**Dependência circular de status**</span><span class="sxs-lookup"><span data-stu-id="def14-166">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="def14-167">18</span><span class="sxs-lookup"><span data-stu-id="def14-167">18</span></span>

<span data-ttu-id="def14-168">Há dependências circulares quando o serviço é iniciado.</span><span class="sxs-lookup"><span data-stu-id="def14-168">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="def14-169">**Nome duplicado de status**</span><span class="sxs-lookup"><span data-stu-id="def14-169">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="def14-170">19</span><span class="sxs-lookup"><span data-stu-id="def14-170">19</span></span>

<span data-ttu-id="def14-171">Há um serviço em execução com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="def14-171">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="def14-172">**Nome inválido do status**</span><span class="sxs-lookup"><span data-stu-id="def14-172">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="def14-173">20</span><span class="sxs-lookup"><span data-stu-id="def14-173">20</span></span>

<span data-ttu-id="def14-174">Há caracteres inválidos no nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="def14-174">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="def14-175">**Parâmetro de status inválido**</span><span class="sxs-lookup"><span data-stu-id="def14-175">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="def14-176">21</span><span class="sxs-lookup"><span data-stu-id="def14-176">21</span></span>

<span data-ttu-id="def14-177">Parâmetros inválidos foram passados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="def14-177">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="def14-178">**Conta de serviço inválida de status**</span><span class="sxs-lookup"><span data-stu-id="def14-178">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="def14-179">22</span><span class="sxs-lookup"><span data-stu-id="def14-179">22</span></span>

<span data-ttu-id="def14-180">A conta na qual esse serviço deve ser executado é inválida ou não tem as permissões para executar o serviço.</span><span class="sxs-lookup"><span data-stu-id="def14-180">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="def14-181">**O serviço de status existe**</span><span class="sxs-lookup"><span data-stu-id="def14-181">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="def14-182">23</span><span class="sxs-lookup"><span data-stu-id="def14-182">23</span></span>

<span data-ttu-id="def14-183">O serviço existe no banco de dados de serviços disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="def14-183">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="def14-184">**O serviço já está em pausa**</span><span class="sxs-lookup"><span data-stu-id="def14-184">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="def14-185">24</span><span class="sxs-lookup"><span data-stu-id="def14-185">24</span></span>

<span data-ttu-id="def14-186">O serviço está pausado atualmente no sistema.</span><span class="sxs-lookup"><span data-stu-id="def14-186">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="def14-187">**Outras**</span><span class="sxs-lookup"><span data-stu-id="def14-187">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="def14-188">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="def14-188">25 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="def14-189">Requisitos</span><span class="sxs-lookup"><span data-stu-id="def14-189">Requirements</span></span>



| <span data-ttu-id="def14-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="def14-190">Requirement</span></span> | <span data-ttu-id="def14-191">Valor</span><span class="sxs-lookup"><span data-stu-id="def14-191">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="def14-192">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="def14-192">Minimum supported client</span></span><br/> | <span data-ttu-id="def14-193">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="def14-193">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="def14-194">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="def14-194">Minimum supported server</span></span><br/> | <span data-ttu-id="def14-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="def14-195">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="def14-196">Namespace</span><span class="sxs-lookup"><span data-stu-id="def14-196">Namespace</span></span><br/>                | <span data-ttu-id="def14-197">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="def14-197">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="def14-198">MOF</span><span class="sxs-lookup"><span data-stu-id="def14-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="def14-199"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="def14-199"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="def14-200">DLL</span><span class="sxs-lookup"><span data-stu-id="def14-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="def14-201"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="def14-201"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="def14-202">Confira também</span><span class="sxs-lookup"><span data-stu-id="def14-202">See also</span></span>

<dl> <dt>

<span data-ttu-id="def14-203">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="def14-203">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="def14-204">**\_BaseService Win32**</span><span class="sxs-lookup"><span data-stu-id="def14-204">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 


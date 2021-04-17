---
description: Interrompe o serviço representado pelo objeto derivado do Win32 \_ BaseService.
ms.assetid: 5d6427a6-d233-4db4-9235-c6187b36da5f
ms.tgt_platform: multiple
title: Método StopService da classe Win32_BaseService (Sdoias. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b5b31b854255c6b20253875233bf2e5a44207a5a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750952"
---
# <a name="stopservice-method-of-the-win32_baseservice-class"></a><span data-ttu-id="5f8e5-103">Método StopService da classe Win32 \_ BaseService</span><span class="sxs-lookup"><span data-stu-id="5f8e5-103">StopService method of the Win32\_BaseService class</span></span>

<span data-ttu-id="5f8e5-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **StopService** interrompe o serviço representado pelo objeto derivado do [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="5f8e5-104">The **StopService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method stops the service represented by the object derived from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="5f8e5-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="5f8e5-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5f8e5-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5f8e5-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5f8e5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f8e5-107">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="5f8e5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5f8e5-108">Parameters</span></span>

<span data-ttu-id="5f8e5-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="5f8e5-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5f8e5-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5f8e5-110">Return value</span></span>

<span data-ttu-id="5f8e5-111">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="5f8e5-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="5f8e5-112">**Êxito**</span><span class="sxs-lookup"><span data-stu-id="5f8e5-112">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="5f8e5-113">0</span><span class="sxs-lookup"><span data-stu-id="5f8e5-113">0</span></span>

<span data-ttu-id="5f8e5-114">A solicitação foi aceita.</span><span class="sxs-lookup"><span data-stu-id="5f8e5-114">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="5f8e5-115">**Sem suporte**</span><span class="sxs-lookup"><span data-stu-id="5f8e5-115">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="5f8e5-116">1</span><span class="sxs-lookup"><span data-stu-id="5f8e5-116">1</span></span>

<span data-ttu-id="5f8e5-117">A solicitação não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="5f8e5-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="5f8e5-118">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="5f8e5-118">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="5f8e5-119">2</span><span class="sxs-lookup"><span data-stu-id="5f8e5-119">2</span></span>

<span data-ttu-id="5f8e5-120">O usuário não tinha o acesso necessário.</span><span class="sxs-lookup"><span data-stu-id="5f8e5-120">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="5f8e5-121">**Serviços dependentes em execução**</span><span class="sxs-lookup"><span data-stu-id="5f8e5-121">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="5f8e5-122">3</span><span class="sxs-lookup"><span data-stu-id="5f8e5-122">3</span></span>

<span data-ttu-id="5f8e5-123">O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.</span><span class="sxs-lookup"><span data-stu-id="5f8e5-123">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="5f8e5-124">**Controle de serviço inválido**</span><span class="sxs-lookup"><span data-stu-id="5f8e5-124">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="5f8e5-125">4</span><span class="sxs-lookup"><span data-stu-id="5f8e5-125">4</span></span>

<span data-ttu-id="5f8e5-126">O código de controle pedido não é válido ou é inaceitável para o serviço.</span><span class="sxs-lookup"><span data-stu-id="5f8e5-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="5f8e5-127">**O serviço não pode aceitar o controle**</span><span class="sxs-lookup"><span data-stu-id="5f8e5-127">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="5f8e5-128">5</span><span class="sxs-lookup"><span data-stu-id="5f8e5-128">5</span></span>

<span data-ttu-id="5f8e5-129">O código de controle solicitado não pode ser enviado ao serviço porque o estado do serviço (Propriedade de [**estado**](win32-baseservice.md) [**\_ BaseService do Win32**](win32-baseservice.md)) é igual a 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="5f8e5-129">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md)[**State**](win32-baseservice.md) property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="5f8e5-130">**Serviço não ativo**</span><span class="sxs-lookup"><span data-stu-id="5f8e5-130">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="5f8e5-131">6</span><span class="sxs-lookup"><span data-stu-id="5f8e5-131">6</span></span>

<span data-ttu-id="5f8e5-132">O serviço não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="5f8e5-132">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="5f8e5-133">**Tempo limite da solicitação de serviço**</span><span class="sxs-lookup"><span data-stu-id="5f8e5-133">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="5f8e5-134">7</span><span class="sxs-lookup"><span data-stu-id="5f8e5-134">7</span></span>

<span data-ttu-id="5f8e5-135">O serviço não respondeu à solicitação de início em um tempo oportuno.</span><span class="sxs-lookup"><span data-stu-id="5f8e5-135">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="5f8e5-136">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="5f8e5-136">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="5f8e5-137">8</span><span class="sxs-lookup"><span data-stu-id="5f8e5-137">8</span></span>

<span data-ttu-id="5f8e5-138">Processo interativo.</span><span class="sxs-lookup"><span data-stu-id="5f8e5-138">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="5f8e5-139">**Caminho não encontrado**</span><span class="sxs-lookup"><span data-stu-id="5f8e5-139">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="5f8e5-140">9</span><span class="sxs-lookup"><span data-stu-id="5f8e5-140">9</span></span>

<span data-ttu-id="5f8e5-141">O caminho do diretório para o arquivo executável do serviço não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="5f8e5-141">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="5f8e5-142">**Serviço já em execução**</span><span class="sxs-lookup"><span data-stu-id="5f8e5-142">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="5f8e5-143">10</span><span class="sxs-lookup"><span data-stu-id="5f8e5-143">10</span></span>

<span data-ttu-id="5f8e5-144">O serviço já está em execução.</span><span class="sxs-lookup"><span data-stu-id="5f8e5-144">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="5f8e5-145">**Banco de dados de serviço bloqueado**</span><span class="sxs-lookup"><span data-stu-id="5f8e5-145">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="5f8e5-146">11</span><span class="sxs-lookup"><span data-stu-id="5f8e5-146">11</span></span>

<span data-ttu-id="5f8e5-147">O banco de dados para adicionar um serviço novo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="5f8e5-147">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="5f8e5-148">**Dependência de serviço excluída**</span><span class="sxs-lookup"><span data-stu-id="5f8e5-148">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="5f8e5-149">12</span><span class="sxs-lookup"><span data-stu-id="5f8e5-149">12</span></span>

<span data-ttu-id="5f8e5-150">Uma dependência da qual esse serviço depende foi removida do sistema.</span><span class="sxs-lookup"><span data-stu-id="5f8e5-150">A dependency on which this service relies has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="5f8e5-151">**Falha na dependência de serviço**</span><span class="sxs-lookup"><span data-stu-id="5f8e5-151">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="5f8e5-152">13</span><span class="sxs-lookup"><span data-stu-id="5f8e5-152">13</span></span>

<span data-ttu-id="5f8e5-153">O serviço não pôde localizar o serviço necessário de um serviço dependente.</span><span class="sxs-lookup"><span data-stu-id="5f8e5-153">The service failed to find the service required from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="5f8e5-154">**Serviço desabilitado**</span><span class="sxs-lookup"><span data-stu-id="5f8e5-154">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="5f8e5-155">14</span><span class="sxs-lookup"><span data-stu-id="5f8e5-155">14</span></span>

<span data-ttu-id="5f8e5-156">O serviço foi desabilitado do sistema.</span><span class="sxs-lookup"><span data-stu-id="5f8e5-156">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="5f8e5-157">**Falha no logon do serviço**</span><span class="sxs-lookup"><span data-stu-id="5f8e5-157">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="5f8e5-158">15</span><span class="sxs-lookup"><span data-stu-id="5f8e5-158">15</span></span>

<span data-ttu-id="5f8e5-159">O serviço não tem a autenticação correta para ser executado no sistema.</span><span class="sxs-lookup"><span data-stu-id="5f8e5-159">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="5f8e5-160">**Serviço marcado para exclusão**</span><span class="sxs-lookup"><span data-stu-id="5f8e5-160">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="5f8e5-161">16</span><span class="sxs-lookup"><span data-stu-id="5f8e5-161">16</span></span>

<span data-ttu-id="5f8e5-162">Este serviço está sendo removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="5f8e5-162">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="5f8e5-163">**Serviço sem thread**</span><span class="sxs-lookup"><span data-stu-id="5f8e5-163">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="5f8e5-164">17</span><span class="sxs-lookup"><span data-stu-id="5f8e5-164">17</span></span>

<span data-ttu-id="5f8e5-165">Não há nenhum thread de execução para o serviço.</span><span class="sxs-lookup"><span data-stu-id="5f8e5-165">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="5f8e5-166">**Dependência circular de status**</span><span class="sxs-lookup"><span data-stu-id="5f8e5-166">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="5f8e5-167">18</span><span class="sxs-lookup"><span data-stu-id="5f8e5-167">18</span></span>

<span data-ttu-id="5f8e5-168">Há dependências circulares quando o serviço é iniciado.</span><span class="sxs-lookup"><span data-stu-id="5f8e5-168">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="5f8e5-169">**Nome duplicado de status**</span><span class="sxs-lookup"><span data-stu-id="5f8e5-169">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="5f8e5-170">19</span><span class="sxs-lookup"><span data-stu-id="5f8e5-170">19</span></span>

<span data-ttu-id="5f8e5-171">Há um serviço em execução com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="5f8e5-171">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="5f8e5-172">**Nome inválido do status**</span><span class="sxs-lookup"><span data-stu-id="5f8e5-172">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="5f8e5-173">20</span><span class="sxs-lookup"><span data-stu-id="5f8e5-173">20</span></span>

<span data-ttu-id="5f8e5-174">Há caracteres inválidos no nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="5f8e5-174">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="5f8e5-175">**Parâmetro de status inválido**</span><span class="sxs-lookup"><span data-stu-id="5f8e5-175">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="5f8e5-176">21</span><span class="sxs-lookup"><span data-stu-id="5f8e5-176">21</span></span>

<span data-ttu-id="5f8e5-177">Parâmetros inválidos foram passados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="5f8e5-177">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="5f8e5-178">**Conta de serviço inválida de status**</span><span class="sxs-lookup"><span data-stu-id="5f8e5-178">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="5f8e5-179">22</span><span class="sxs-lookup"><span data-stu-id="5f8e5-179">22</span></span>

<span data-ttu-id="5f8e5-180">A conta na qual esse serviço deve ser executado é inválida ou não tem as permissões para executar o serviço.</span><span class="sxs-lookup"><span data-stu-id="5f8e5-180">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="5f8e5-181">**O serviço de status existe**</span><span class="sxs-lookup"><span data-stu-id="5f8e5-181">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="5f8e5-182">23</span><span class="sxs-lookup"><span data-stu-id="5f8e5-182">23</span></span>

<span data-ttu-id="5f8e5-183">O serviço existe no banco de dados de serviços disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="5f8e5-183">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="5f8e5-184">**O serviço já está em pausa**</span><span class="sxs-lookup"><span data-stu-id="5f8e5-184">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="5f8e5-185">24</span><span class="sxs-lookup"><span data-stu-id="5f8e5-185">24</span></span>

<span data-ttu-id="5f8e5-186">O serviço está pausado atualmente no sistema.</span><span class="sxs-lookup"><span data-stu-id="5f8e5-186">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="5f8e5-187">**Outras**</span><span class="sxs-lookup"><span data-stu-id="5f8e5-187">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="5f8e5-188">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="5f8e5-188">25 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5f8e5-189">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f8e5-189">Requirements</span></span>



| <span data-ttu-id="5f8e5-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f8e5-190">Requirement</span></span> | <span data-ttu-id="5f8e5-191">Valor</span><span class="sxs-lookup"><span data-stu-id="5f8e5-191">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f8e5-192">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f8e5-192">Minimum supported client</span></span><br/> | <span data-ttu-id="5f8e5-193">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5f8e5-193">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5f8e5-194">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f8e5-194">Minimum supported server</span></span><br/> | <span data-ttu-id="5f8e5-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5f8e5-195">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5f8e5-196">Namespace</span><span class="sxs-lookup"><span data-stu-id="5f8e5-196">Namespace</span></span><br/>                | <span data-ttu-id="5f8e5-197">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5f8e5-197">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5f8e5-198">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5f8e5-198">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f8e5-199"><dt>Sdoias. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f8e5-199"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="5f8e5-200">MOF</span><span class="sxs-lookup"><span data-stu-id="5f8e5-200">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5f8e5-201"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5f8e5-201"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5f8e5-202">DLL</span><span class="sxs-lookup"><span data-stu-id="5f8e5-202">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f8e5-203"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f8e5-203"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f8e5-204">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f8e5-204">See also</span></span>

<dl> <dt>

<span data-ttu-id="5f8e5-205">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5f8e5-205">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5f8e5-206">**\_BaseService Win32**</span><span class="sxs-lookup"><span data-stu-id="5f8e5-206">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 


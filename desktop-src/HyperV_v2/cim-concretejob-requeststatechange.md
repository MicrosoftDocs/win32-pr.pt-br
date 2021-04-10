---
description: Solicita que o estado do trabalho seja alterado para o valor especificado no parâmetro Requestedstate. Invocar o método RequestStateChange várias vezes pode fazer com que as solicitações anteriores fossem substituídas ou perdidas.
ms.assetid: 64a9d63e-8af4-4ab1-8343-9a0418b951e2
title: Método RequestStateChange da classe CIM_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6e3efcea0f7ed7d6ecbfef7b543a0e82d90a15b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296475"
---
# <a name="requeststatechange-method-of-the-cim_concretejob-class"></a><span data-ttu-id="5cfb5-104">Método RequestStateChange da \_ classe ConcreteJob do CIM</span><span class="sxs-lookup"><span data-stu-id="5cfb5-104">RequestStateChange method of the CIM\_ConcreteJob class</span></span>

<span data-ttu-id="5cfb5-105">Solicita que o estado do trabalho seja alterado para o valor especificado no parâmetro Requestedstate.</span><span class="sxs-lookup"><span data-stu-id="5cfb5-105">Requests that the state of the job be changed to the value specified in the RequestedState parameter.</span></span> <span data-ttu-id="5cfb5-106">Invocar o método RequestStateChange várias vezes pode fazer com que as solicitações anteriores fossem substituídas ou perdidas.</span><span class="sxs-lookup"><span data-stu-id="5cfb5-106">Invoking the RequestStateChange method multiple times could result in earlier requests being overwritten or lost.</span></span>

<span data-ttu-id="5cfb5-107">Se 0 for retornado, a tarefa será concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="5cfb5-107">If 0 is returned, then the task completed successfully.</span></span> <span data-ttu-id="5cfb5-108">Qualquer outro código de retorno indica uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="5cfb5-108">Any other return code indicates an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cfb5-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5cfb5-109">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="5cfb5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5cfb5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cfb5-111">*Requestedstate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5cfb5-111">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5cfb5-112">O estado para solicitação de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="5cfb5-112">The state to request for a job.</span></span> <span data-ttu-id="5cfb5-113">Os valores possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="5cfb5-113">The possible values are as follows:</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="5cfb5-114"><span id="Start"></span><span id="start"></span><span id="START"></span>**Início** (2)</span><span class="sxs-lookup"><span data-stu-id="5cfb5-114"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5cfb5-115">Altera o estado para ' running '.</span><span class="sxs-lookup"><span data-stu-id="5cfb5-115">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="5cfb5-116"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspender** (3)</span><span class="sxs-lookup"><span data-stu-id="5cfb5-116"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5cfb5-117">Interrompe o trabalho temporariamente.</span><span class="sxs-lookup"><span data-stu-id="5cfb5-117">Stops the job temporarily.</span></span> <span data-ttu-id="5cfb5-118">A intenção é reiniciar subsequentemente o trabalho com ' Start '.</span><span class="sxs-lookup"><span data-stu-id="5cfb5-118">The intention is to subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="5cfb5-119">Pode ser possível inserir o estado ' serviço ' ao ser suspenso.</span><span class="sxs-lookup"><span data-stu-id="5cfb5-119">It might be possible to enter the 'Service' state while suspended.</span></span> <span data-ttu-id="5cfb5-120">(Isso é específico do trabalho.)</span><span class="sxs-lookup"><span data-stu-id="5cfb5-120">(This is job-specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="5cfb5-121"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminar** (4)</span><span class="sxs-lookup"><span data-stu-id="5cfb5-121"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="5cfb5-122">Interrompe o trabalho corretamente, salva os dados, preserva o estado e desliga todos os processos subjacentes de maneira ordenada.</span><span class="sxs-lookup"><span data-stu-id="5cfb5-122">Stops the job cleanly, saves data, preserves the state, and shuts down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="5cfb5-123"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="5cfb5-123"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="5cfb5-124">Encerra o trabalho imediatamente sem nenhum requisito para salvar dados ou preservar o estado.</span><span class="sxs-lookup"><span data-stu-id="5cfb5-124">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5cfb5-125"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Serviço** (6)</span><span class="sxs-lookup"><span data-stu-id="5cfb5-125"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="5cfb5-126">Coloca o trabalho em um estado de serviço específico do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="5cfb5-126">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="5cfb5-127">Pode ser possível reiniciar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="5cfb5-127">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="5cfb5-128"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="5cfb5-128"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="5cfb5-129"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="5cfb5-129"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="5cfb5-130">*TimeoutPeriod* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5cfb5-130">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5cfb5-131">Um período de tempo limite que especifica a quantidade máxima de tempo que o cliente espera que a transição para o novo Estado tenha.</span><span class="sxs-lookup"><span data-stu-id="5cfb5-131">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="5cfb5-132">O formato do intervalo deve ser usado para especificar o período de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="5cfb5-132">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="5cfb5-133">Um valor 0 ou **NULL** indica que o cliente não tem requisitos de tempo para a transição.</span><span class="sxs-lookup"><span data-stu-id="5cfb5-133">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="5cfb5-134">Se essa propriedade não contiver 0 ou **NULL** e a implementação não oferecer suporte a esse parâmetro, um código de retorno 4098 (**uso do parâmetro timeout sem suporte**) deverá ser retornado.</span><span class="sxs-lookup"><span data-stu-id="5cfb5-134">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cfb5-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5cfb5-135">Return value</span></span>

<span data-ttu-id="5cfb5-136">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="5cfb5-136">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="5cfb5-137">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="5cfb5-137">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5cfb5-138">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="5cfb5-138">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5cfb5-139">**Erro desconhecido/não especificado** (2)</span><span class="sxs-lookup"><span data-stu-id="5cfb5-139">**Unknown/Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5cfb5-140">**Não é possível concluir dentro do período de tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="5cfb5-140">**Can NOT complete within Timeout Period** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5cfb5-141">**Com falha** (4)</span><span class="sxs-lookup"><span data-stu-id="5cfb5-141">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5cfb5-142">**Parâmetro inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="5cfb5-142">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="5cfb5-143">**Em uso** (6)</span><span class="sxs-lookup"><span data-stu-id="5cfb5-143">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="5cfb5-144">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="5cfb5-144">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5cfb5-145">**Parâmetros de método verificados-transição iniciada** (4096)</span><span class="sxs-lookup"><span data-stu-id="5cfb5-145">**Method Parameters Checked - Transition Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="5cfb5-146">**Transição de estado inválida** (4097)</span><span class="sxs-lookup"><span data-stu-id="5cfb5-146">**Invalid State Transition** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="5cfb5-147">**Não há suporte para o uso do parâmetro timeout** (4098)</span><span class="sxs-lookup"><span data-stu-id="5cfb5-147">**Use of Timeout Parameter Not Supported** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="5cfb5-148">**Ocupado** (4099)</span><span class="sxs-lookup"><span data-stu-id="5cfb5-148">**Busy** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="5cfb5-149">**Método reservado** (4100.. 32767)</span><span class="sxs-lookup"><span data-stu-id="5cfb5-149">**Method Reserved** (4100..32767)</span></span>
</dt> <dt>

<span data-ttu-id="5cfb5-150">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="5cfb5-150">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="5cfb5-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5cfb5-151">Requirements</span></span>



| <span data-ttu-id="5cfb5-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cfb5-152">Requirement</span></span> | <span data-ttu-id="5cfb5-153">Valor</span><span class="sxs-lookup"><span data-stu-id="5cfb5-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cfb5-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5cfb5-154">Minimum supported client</span></span><br/> | <span data-ttu-id="5cfb5-155">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5cfb5-155">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="5cfb5-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5cfb5-156">Minimum supported server</span></span><br/> | <span data-ttu-id="5cfb5-157">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="5cfb5-157">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="5cfb5-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="5cfb5-158">Namespace</span></span><br/>                | <span data-ttu-id="5cfb5-159">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="5cfb5-159">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5cfb5-160">MOF</span><span class="sxs-lookup"><span data-stu-id="5cfb5-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5cfb5-161"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5cfb5-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5cfb5-162">DLL</span><span class="sxs-lookup"><span data-stu-id="5cfb5-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5cfb5-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5cfb5-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5cfb5-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="5cfb5-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cfb5-165">**\_CONCRETEJOB CIM**</span><span class="sxs-lookup"><span data-stu-id="5cfb5-165">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> </dl>

 

 





---
description: Solicita que o estado do trabalho seja alterado para o estado especificado.
ms.assetid: 5D7D7D20-4BB9-4375-BBBF-7AA64FEE6D13
title: Método RequestStateChange da classe Msvm_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0e7abf5f4bf78ac469e528ab72bb5786130e9cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768501"
---
# <a name="requeststatechange-method-of-the-msvm_concretejob-class"></a><span data-ttu-id="6cfc9-103">Método RequestStateChange da classe Msvm \_ ConcreteJob</span><span class="sxs-lookup"><span data-stu-id="6cfc9-103">RequestStateChange method of the Msvm\_ConcreteJob class</span></span>

<span data-ttu-id="6cfc9-104">Solicita que o estado do trabalho seja alterado para o estado especificado.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-104">Requests that the state of the job be changed to the specified state.</span></span> <span data-ttu-id="6cfc9-105">Invocar o método **RequestStateChange** várias vezes pode fazer com que as solicitações anteriores sejam substituídas ou perdidas.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-105">Invoking the **RequestStateChange** method multiple times can result in earlier requests being overwritten or lost.</span></span> <span data-ttu-id="6cfc9-106">Se 0 for retornado, a tarefa será concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-106">If 0 is returned, then the task completed successfully.</span></span> <span data-ttu-id="6cfc9-107">Qualquer outro código de retorno indica uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-107">Any other return code indicates an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cfc9-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6cfc9-108">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="6cfc9-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6cfc9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cfc9-110">*Requestedstate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6cfc9-110">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cfc9-111">Tipo: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6cfc9-111">Type: **uint16**</span></span>

<span data-ttu-id="6cfc9-112">O novo estado de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-112">The new state of a job.</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="6cfc9-113"><span id="Start"></span><span id="start"></span><span id="START"></span>**Início** (2)</span><span class="sxs-lookup"><span data-stu-id="6cfc9-113"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6cfc9-114">Altera o estado para "em execução".</span><span class="sxs-lookup"><span data-stu-id="6cfc9-114">Changes the state to "Running".</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="6cfc9-115"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspender** (3)</span><span class="sxs-lookup"><span data-stu-id="6cfc9-115"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6cfc9-116">Interrompe o trabalho temporariamente.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-116">Stops the job temporarily.</span></span> <span data-ttu-id="6cfc9-117">A intenção é reiniciar subsequentemente o trabalho com "Start".</span><span class="sxs-lookup"><span data-stu-id="6cfc9-117">The intention is to subsequently restart the job with "Start".</span></span> <span data-ttu-id="6cfc9-118">Pode ser possível inserir o estado "serviço" ao ser suspenso.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-118">It might be possible to enter the "Service" state while suspended.</span></span> <span data-ttu-id="6cfc9-119">(Isso é específico do trabalho.)</span><span class="sxs-lookup"><span data-stu-id="6cfc9-119">(This is job specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="6cfc9-120"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminar** (4)</span><span class="sxs-lookup"><span data-stu-id="6cfc9-120"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6cfc9-121">Interrompe o trabalho corretamente, salvando os dados, preservando o estado e desligando todos os processos subjacentes de maneira ordenada.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-121">Stops the job cleanly, saving data, preserving the state, and shutting down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="6cfc9-122"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="6cfc9-122"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="6cfc9-123">Encerra o trabalho imediatamente sem nenhum requisito para salvar dados ou preservar o estado.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-123">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6cfc9-124"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Serviço** (6)</span><span class="sxs-lookup"><span data-stu-id="6cfc9-124"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="6cfc9-125">Coloca o trabalho em um estado de serviço específico do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-125">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="6cfc9-126">Pode ser possível reiniciar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-126">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="6cfc9-127"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado**</span><span class="sxs-lookup"><span data-stu-id="6cfc9-127"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved**</span></span>


</dt> <dd>

<span data-ttu-id="6cfc9-128">Reservado.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-128">Reserved.</span></span>

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="6cfc9-129"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado**</span><span class="sxs-lookup"><span data-stu-id="6cfc9-129"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved**</span></span>


</dt> <dd>

<span data-ttu-id="6cfc9-130">Reservado.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-130">Reserved.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6cfc9-131">*TimeoutPeriod* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6cfc9-131">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cfc9-132">Tipo: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6cfc9-132">Type: **datetime**</span></span>

<span data-ttu-id="6cfc9-133">Um período de tempo limite que especifica a quantidade máxima de tempo que o cliente espera que a transição para o novo Estado tenha.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-133">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="6cfc9-134">O formato do intervalo deve ser usado para especificar o período de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-134">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="6cfc9-135">Um valor 0 ou **NULL** indica que o cliente não tem requisitos de tempo para a transição.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-135">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="6cfc9-136">Se essa propriedade não contiver 0 ou **NULL** e a implementação não oferecer suporte a esse parâmetro, um código de retorno 4098 (uso do parâmetro timeout sem suporte) deverá ser retornado.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-136">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (Use Of Timeout Parameter Not Supported) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cfc9-137">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6cfc9-137">Return value</span></span>

<span data-ttu-id="6cfc9-138">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6cfc9-138">Type: **uint32**</span></span>

<span data-ttu-id="6cfc9-139">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-139">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="6cfc9-140">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="6cfc9-140">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6cfc9-141">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="6cfc9-141">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6cfc9-142">**Erro desconhecido/não especificado** (2)</span><span class="sxs-lookup"><span data-stu-id="6cfc9-142">**Unknown/Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6cfc9-143">**Não é possível concluir dentro do período de tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="6cfc9-143">**Cannot complete within Timeout Period** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6cfc9-144">**Com falha** (4)</span><span class="sxs-lookup"><span data-stu-id="6cfc9-144">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6cfc9-145">**Parâmetro inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="6cfc9-145">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6cfc9-146">**Em uso** (6)</span><span class="sxs-lookup"><span data-stu-id="6cfc9-146">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="6cfc9-147">**DMTF reservado** (7 4095)</span><span class="sxs-lookup"><span data-stu-id="6cfc9-147">**DMTF Reserved** (7 4095)</span></span>
</dt> <dt>

<span data-ttu-id="6cfc9-148">**Parâmetros de método verificados-transição iniciada** (4096)</span><span class="sxs-lookup"><span data-stu-id="6cfc9-148">**Method Parameters Checked - Transition Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6cfc9-149">**Transição de estado inválida** (4097)</span><span class="sxs-lookup"><span data-stu-id="6cfc9-149">**Invalid State Transition** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="6cfc9-150">**Não há suporte para o uso do parâmetro timeout** (4098)</span><span class="sxs-lookup"><span data-stu-id="6cfc9-150">**Use of Timeout Parameter Not Supported** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="6cfc9-151">**Ocupado** (4099)</span><span class="sxs-lookup"><span data-stu-id="6cfc9-151">**Busy** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="6cfc9-152">**Método reservado** (4100 32767)</span><span class="sxs-lookup"><span data-stu-id="6cfc9-152">**Method Reserved** (4100 32767)</span></span>
</dt> <dt>

<span data-ttu-id="6cfc9-153">**Específico do fornecedor** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="6cfc9-153">**Vendor Specific** (32768 65535)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="6cfc9-154">Comentários</span><span class="sxs-lookup"><span data-stu-id="6cfc9-154">Remarks</span></span>

<span data-ttu-id="6cfc9-155">O acesso à classe [**Msvm \_ ConcreteJob**](msvm-concretejob.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-155">Access to the [**Msvm\_ConcreteJob**](msvm-concretejob.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="6cfc9-156">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="6cfc9-156">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="6cfc9-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6cfc9-157">Requirements</span></span>



| <span data-ttu-id="6cfc9-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cfc9-158">Requirement</span></span> | <span data-ttu-id="6cfc9-159">Valor</span><span class="sxs-lookup"><span data-stu-id="6cfc9-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cfc9-160">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6cfc9-160">Minimum supported client</span></span><br/> | <span data-ttu-id="6cfc9-161">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6cfc9-161">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6cfc9-162">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6cfc9-162">Minimum supported server</span></span><br/> | <span data-ttu-id="6cfc9-163">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6cfc9-163">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6cfc9-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="6cfc9-164">Namespace</span></span><br/>                | <span data-ttu-id="6cfc9-165">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="6cfc9-165">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6cfc9-166">MOF</span><span class="sxs-lookup"><span data-stu-id="6cfc9-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6cfc9-167"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6cfc9-167"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6cfc9-168">DLL</span><span class="sxs-lookup"><span data-stu-id="6cfc9-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6cfc9-169"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6cfc9-169"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6cfc9-170">Confira também</span><span class="sxs-lookup"><span data-stu-id="6cfc9-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cfc9-171">**Msvm \_ ConcreteJob**</span><span class="sxs-lookup"><span data-stu-id="6cfc9-171">**Msvm\_ConcreteJob**</span></span>](msvm-concretejob.md)
</dt> </dl>

 


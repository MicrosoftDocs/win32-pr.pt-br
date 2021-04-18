---
description: Solicita que o estado do trabalho de migração seja alterado para o estado especificado.
ms.assetid: f0be5ea8-7e21-407e-b84d-8bd4ca5a6a2c
title: Método RequestStateChange da classe Msvm_MigrationJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MigrationJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 31011de619780ae36f390ee87038300a3b42fef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778746"
---
# <a name="requeststatechange-method-of-the-msvm_migrationjob-class"></a><span data-ttu-id="9b2d7-103">Método RequestStateChange da classe Msvm \_ MigrationJob</span><span class="sxs-lookup"><span data-stu-id="9b2d7-103">RequestStateChange method of the Msvm\_MigrationJob class</span></span>

<span data-ttu-id="9b2d7-104">Solicita que o estado do trabalho de migração seja alterado para o estado especificado.</span><span class="sxs-lookup"><span data-stu-id="9b2d7-104">Requests that the state of the migration job be changed to the specified state.</span></span> <span data-ttu-id="9b2d7-105">Invocar o método **RequestStateChange** várias vezes pode fazer com que as solicitações anteriores sejam substituídas ou perdidas.</span><span class="sxs-lookup"><span data-stu-id="9b2d7-105">Invoking the **RequestStateChange** method multiple times can result in earlier requests being overwritten or lost.</span></span> <span data-ttu-id="9b2d7-106">Se 0 for retornado, a tarefa será concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="9b2d7-106">If 0 is returned, then the task completed successfully.</span></span> <span data-ttu-id="9b2d7-107">Qualquer outro código de retorno indica uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="9b2d7-107">Any other return code indicates an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b2d7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9b2d7-108">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="9b2d7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9b2d7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b2d7-110">*Requestedstate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9b2d7-110">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b2d7-111">O novo estado de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="9b2d7-111">The new state of a job.</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="9b2d7-112"><span id="Start"></span><span id="start"></span><span id="START"></span>**Início** (2)</span><span class="sxs-lookup"><span data-stu-id="9b2d7-112"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9b2d7-113">Altera o estado para "em execução".</span><span class="sxs-lookup"><span data-stu-id="9b2d7-113">Changes the state to "Running".</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="9b2d7-114"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspender** (3)</span><span class="sxs-lookup"><span data-stu-id="9b2d7-114"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9b2d7-115">Interrompe o trabalho temporariamente.</span><span class="sxs-lookup"><span data-stu-id="9b2d7-115">Stops the job temporarily.</span></span> <span data-ttu-id="9b2d7-116">A intenção é reiniciar subsequentemente o trabalho com "Start".</span><span class="sxs-lookup"><span data-stu-id="9b2d7-116">The intention is to subsequently restart the job with "Start".</span></span> <span data-ttu-id="9b2d7-117">Pode ser possível inserir o estado "serviço" ao ser suspenso.</span><span class="sxs-lookup"><span data-stu-id="9b2d7-117">It might be possible to enter the "Service" state while suspended.</span></span> <span data-ttu-id="9b2d7-118">(Isso é específico do trabalho.)</span><span class="sxs-lookup"><span data-stu-id="9b2d7-118">(This is job specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="9b2d7-119"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminar** (4)</span><span class="sxs-lookup"><span data-stu-id="9b2d7-119"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9b2d7-120">Interrompe o trabalho corretamente, salvando os dados, preservando o estado e desligando todos os processos subjacentes de maneira ordenada.</span><span class="sxs-lookup"><span data-stu-id="9b2d7-120">Stops the job cleanly, saving data, preserving the state, and shutting down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="9b2d7-121"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="9b2d7-121"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="9b2d7-122">Encerra o trabalho imediatamente sem nenhum requisito para salvar dados ou preservar o estado.</span><span class="sxs-lookup"><span data-stu-id="9b2d7-122">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9b2d7-123"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Serviço** (6)</span><span class="sxs-lookup"><span data-stu-id="9b2d7-123"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="9b2d7-124">Coloca o trabalho em um estado de serviço específico do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="9b2d7-124">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="9b2d7-125">Pode ser possível reiniciar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="9b2d7-125">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="9b2d7-126"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado**</span><span class="sxs-lookup"><span data-stu-id="9b2d7-126"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved**</span></span>


</dt> <dd>

<span data-ttu-id="9b2d7-127">Reservado.</span><span class="sxs-lookup"><span data-stu-id="9b2d7-127">Reserved.</span></span>

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="9b2d7-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado**</span><span class="sxs-lookup"><span data-stu-id="9b2d7-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved**</span></span>


</dt> <dd>

<span data-ttu-id="9b2d7-129">Reservado.</span><span class="sxs-lookup"><span data-stu-id="9b2d7-129">Reserved.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="9b2d7-130">*TimeoutPeriod* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9b2d7-130">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b2d7-131">Um período de tempo limite que especifica a quantidade máxima de tempo que o cliente espera que a transição para o novo Estado tenha.</span><span class="sxs-lookup"><span data-stu-id="9b2d7-131">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="9b2d7-132">O formato do intervalo deve ser usado para especificar o período de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="9b2d7-132">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="9b2d7-133">Um valor 0 ou **NULL** indica que o cliente não tem requisitos de tempo para a transição.</span><span class="sxs-lookup"><span data-stu-id="9b2d7-133">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="9b2d7-134">Se essa propriedade não contiver 0 ou **NULL** e a implementação não oferecer suporte a esse parâmetro, um código de retorno 4098 (uso do parâmetro timeout sem suporte) deverá ser retornado.</span><span class="sxs-lookup"><span data-stu-id="9b2d7-134">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (Use Of Timeout Parameter Not Supported) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b2d7-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9b2d7-135">Return value</span></span>

<dl> <dt>

 <span data-ttu-id="9b2d7-136"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="9b2d7-136">(0)</span></span>
</dt> <dt>

 <span data-ttu-id="9b2d7-137">(32768)</span><span class="sxs-lookup"><span data-stu-id="9b2d7-137">(32768)</span></span>
</dt> <dt>

 <span data-ttu-id="9b2d7-138">(32769)</span><span class="sxs-lookup"><span data-stu-id="9b2d7-138">(32769)</span></span>
</dt> <dt>

 <span data-ttu-id="9b2d7-139">(32770)</span><span class="sxs-lookup"><span data-stu-id="9b2d7-139">(32770)</span></span>
</dt> <dt>

 <span data-ttu-id="9b2d7-140">(32771)</span><span class="sxs-lookup"><span data-stu-id="9b2d7-140">(32771)</span></span>
</dt> <dt>

 <span data-ttu-id="9b2d7-141">(32772)</span><span class="sxs-lookup"><span data-stu-id="9b2d7-141">(32772)</span></span>
</dt> <dt>

 <span data-ttu-id="9b2d7-142">(32773)</span><span class="sxs-lookup"><span data-stu-id="9b2d7-142">(32773)</span></span>
</dt> <dt>

 <span data-ttu-id="9b2d7-143">(32774)</span><span class="sxs-lookup"><span data-stu-id="9b2d7-143">(32774)</span></span>
</dt> <dt>

 <span data-ttu-id="9b2d7-144">(32775)</span><span class="sxs-lookup"><span data-stu-id="9b2d7-144">(32775)</span></span>
</dt> <dt>

 <span data-ttu-id="9b2d7-145">(32776)</span><span class="sxs-lookup"><span data-stu-id="9b2d7-145">(32776)</span></span>
</dt> <dt>

 <span data-ttu-id="9b2d7-146">(32777)</span><span class="sxs-lookup"><span data-stu-id="9b2d7-146">(32777)</span></span>
</dt> <dt>

 <span data-ttu-id="9b2d7-147">(32778)</span><span class="sxs-lookup"><span data-stu-id="9b2d7-147">(32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9b2d7-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b2d7-148">Requirements</span></span>



| <span data-ttu-id="9b2d7-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b2d7-149">Requirement</span></span> | <span data-ttu-id="9b2d7-150">Valor</span><span class="sxs-lookup"><span data-stu-id="9b2d7-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b2d7-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9b2d7-151">Minimum supported client</span></span><br/> | <span data-ttu-id="9b2d7-152">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9b2d7-152">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9b2d7-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9b2d7-153">Minimum supported server</span></span><br/> | <span data-ttu-id="9b2d7-154">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9b2d7-154">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9b2d7-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="9b2d7-155">Namespace</span></span><br/>                | <span data-ttu-id="9b2d7-156">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="9b2d7-156">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9b2d7-157">MOF</span><span class="sxs-lookup"><span data-stu-id="9b2d7-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b2d7-158"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9b2d7-158"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b2d7-159">DLL</span><span class="sxs-lookup"><span data-stu-id="9b2d7-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b2d7-160"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9b2d7-160"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9b2d7-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b2d7-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b2d7-162">**Msvm \_ MigrationJob**</span><span class="sxs-lookup"><span data-stu-id="9b2d7-162">**Msvm\_MigrationJob**</span></span>](msvm-migrationjob.md)
</dt> </dl>

 

 





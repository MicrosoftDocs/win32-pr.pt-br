---
description: Solicita uma alteração de estado.
ms.assetid: 53c24e17-2b59-4439-a6d1-e971c189d223
title: Método RequestStateChange da classe Msvm_VirtualSystemReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5612371738915b5e38657eca0773a88e31e3b0d2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105748429"
---
# <a name="requeststatechange-method-of-the-msvm_virtualsystemreferencepointexportjob-class"></a><span data-ttu-id="aeb56-103">Método RequestStateChange da classe Msvm \_ VirtualSystemReferencePointExportJob</span><span class="sxs-lookup"><span data-stu-id="aeb56-103">RequestStateChange method of the Msvm\_VirtualSystemReferencePointExportJob class</span></span>

<span data-ttu-id="aeb56-104">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="aeb56-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="aeb56-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aeb56-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="aeb56-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aeb56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aeb56-107">*Requestedstate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aeb56-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aeb56-108">Altera o estado de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="aeb56-108">Changes the state of a job.</span></span> <span data-ttu-id="aeb56-109">Os valores possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="aeb56-109">The possible values are as follows:</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="aeb56-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Início** (2)</span><span class="sxs-lookup"><span data-stu-id="aeb56-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="aeb56-111">Altera o estado para ' running '.</span><span class="sxs-lookup"><span data-stu-id="aeb56-111">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="aeb56-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspender** (3)</span><span class="sxs-lookup"><span data-stu-id="aeb56-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="aeb56-113">Interrompe o trabalho temporariamente.</span><span class="sxs-lookup"><span data-stu-id="aeb56-113">Stops the job temporarily.</span></span> <span data-ttu-id="aeb56-114">A intenção é reiniciar subsequentemente o trabalho com ' Start '.</span><span class="sxs-lookup"><span data-stu-id="aeb56-114">The intention is to subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="aeb56-115">Pode ser possível inserir o estado ' serviço ' ao ser suspenso.</span><span class="sxs-lookup"><span data-stu-id="aeb56-115">It might be possible to enter the 'Service' state while suspended.</span></span> <span data-ttu-id="aeb56-116">(Isso é específico do trabalho.)</span><span class="sxs-lookup"><span data-stu-id="aeb56-116">(This is job-specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="aeb56-117"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminar** (4)</span><span class="sxs-lookup"><span data-stu-id="aeb56-117"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="aeb56-118">Interrompe o trabalho corretamente, salva os dados, preserva o estado e desliga todos os processos subjacentes de maneira ordenada.</span><span class="sxs-lookup"><span data-stu-id="aeb56-118">Stops the job cleanly, saves data, preserves the state, and shuts down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="aeb56-119"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="aeb56-119"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="aeb56-120">Encerra o trabalho imediatamente sem nenhum requisito para salvar dados ou preservar o estado.</span><span class="sxs-lookup"><span data-stu-id="aeb56-120">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="aeb56-121"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Serviço** (6)</span><span class="sxs-lookup"><span data-stu-id="aeb56-121"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="aeb56-122">Coloca o trabalho em um estado de serviço específico do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="aeb56-122">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="aeb56-123">Pode ser possível reiniciar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="aeb56-123">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="aeb56-124"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="aeb56-124"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="aeb56-125"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="aeb56-125"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="aeb56-126">*TimeoutPeriod* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aeb56-126">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aeb56-127">Um período de tempo limite que especifica a quantidade máxima de tempo que o cliente espera que a transição para o novo Estado tenha.</span><span class="sxs-lookup"><span data-stu-id="aeb56-127">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="aeb56-128">O formato do intervalo deve ser usado para especificar o período de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="aeb56-128">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="aeb56-129">Um valor 0 ou **NULL** indica que o cliente não tem requisitos de tempo para a transição.</span><span class="sxs-lookup"><span data-stu-id="aeb56-129">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="aeb56-130">Se essa propriedade não contiver 0 ou **NULL** e a implementação não oferecer suporte a esse parâmetro, um código de retorno 4098 (**uso do parâmetro timeout sem suporte**) deverá ser retornado.</span><span class="sxs-lookup"><span data-stu-id="aeb56-130">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aeb56-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aeb56-131">Return value</span></span>

<span data-ttu-id="aeb56-132">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="aeb56-132">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

 <span data-ttu-id="aeb56-133"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="aeb56-133">(0)</span></span>
</dt> <dt>

 <span data-ttu-id="aeb56-134">(32768)</span><span class="sxs-lookup"><span data-stu-id="aeb56-134">(32768)</span></span>
</dt> <dt>

 <span data-ttu-id="aeb56-135">(32769)</span><span class="sxs-lookup"><span data-stu-id="aeb56-135">(32769)</span></span>
</dt> <dt>

 <span data-ttu-id="aeb56-136">(32770)</span><span class="sxs-lookup"><span data-stu-id="aeb56-136">(32770)</span></span>
</dt> <dt>

 <span data-ttu-id="aeb56-137">(32771)</span><span class="sxs-lookup"><span data-stu-id="aeb56-137">(32771)</span></span>
</dt> <dt>

 <span data-ttu-id="aeb56-138">(32772)</span><span class="sxs-lookup"><span data-stu-id="aeb56-138">(32772)</span></span>
</dt> <dt>

 <span data-ttu-id="aeb56-139">(32773)</span><span class="sxs-lookup"><span data-stu-id="aeb56-139">(32773)</span></span>
</dt> <dt>

 <span data-ttu-id="aeb56-140">(32774)</span><span class="sxs-lookup"><span data-stu-id="aeb56-140">(32774)</span></span>
</dt> <dt>

 <span data-ttu-id="aeb56-141">(32775)</span><span class="sxs-lookup"><span data-stu-id="aeb56-141">(32775)</span></span>
</dt> <dt>

 <span data-ttu-id="aeb56-142">(32776)</span><span class="sxs-lookup"><span data-stu-id="aeb56-142">(32776)</span></span>
</dt> <dt>

 <span data-ttu-id="aeb56-143">(32777)</span><span class="sxs-lookup"><span data-stu-id="aeb56-143">(32777)</span></span>
</dt> <dt>

 <span data-ttu-id="aeb56-144">(32778)</span><span class="sxs-lookup"><span data-stu-id="aeb56-144">(32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="aeb56-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aeb56-145">Requirements</span></span>



| <span data-ttu-id="aeb56-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="aeb56-146">Requirement</span></span> | <span data-ttu-id="aeb56-147">Valor</span><span class="sxs-lookup"><span data-stu-id="aeb56-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeb56-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aeb56-148">Minimum supported client</span></span><br/> | <span data-ttu-id="aeb56-149">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="aeb56-149">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="aeb56-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aeb56-150">Minimum supported server</span></span><br/> | <span data-ttu-id="aeb56-151">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="aeb56-151">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="aeb56-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="aeb56-152">Namespace</span></span><br/>                | <span data-ttu-id="aeb56-153">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="aeb56-153">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="aeb56-154">MOF</span><span class="sxs-lookup"><span data-stu-id="aeb56-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aeb56-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aeb56-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="aeb56-156">DLL</span><span class="sxs-lookup"><span data-stu-id="aeb56-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aeb56-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="aeb56-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="aeb56-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="aeb56-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aeb56-159">**Msvm \_ VirtualSystemReferencePointExportJob**</span><span class="sxs-lookup"><span data-stu-id="aeb56-159">**Msvm\_VirtualSystemReferencePointExportJob**</span></span>](msvm-virtualsystemreferencepointexportjob.md)
</dt> </dl>

 

 





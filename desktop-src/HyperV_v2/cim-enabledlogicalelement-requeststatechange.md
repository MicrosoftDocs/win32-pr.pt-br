---
description: Solicita que o estado do elemento seja alterado para o valor especificado no parâmetro Requestedstate.
ms.assetid: 6d0061ad-ca14-400a-b813-af920f231eeb
title: Método RequestStateChange da classe CIM_EnabledLogicalElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EnabledLogicalElement.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5b28a2c33b61893be24eacc882b29b5a2be18b14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296808"
---
# <a name="requeststatechange-method-of-the-cim_enabledlogicalelement-class"></a><span data-ttu-id="f08cb-103">Método RequestStateChange da \_ classe EnabledLogicalElement do CIM</span><span class="sxs-lookup"><span data-stu-id="f08cb-103">RequestStateChange method of the CIM\_EnabledLogicalElement class</span></span>

<span data-ttu-id="f08cb-104">Solicita que o estado do elemento seja alterado para o valor especificado no parâmetro Requestedstate.</span><span class="sxs-lookup"><span data-stu-id="f08cb-104">Requests that the state of the element be changed to the value specified in the RequestedState parameter.</span></span> <span data-ttu-id="f08cb-105">Quando a alteração de estado solicitada ocorre, o Enabledstate e o Requestedstate solicitado do elemento serão os mesmos.</span><span class="sxs-lookup"><span data-stu-id="f08cb-105">When the requested state change takes place, the EnabledState and RequestedState of the element will be the same.</span></span> <span data-ttu-id="f08cb-106">Invocar o método RequestStateChange várias vezes pode fazer com que as solicitações anteriores fossem substituídas ou perdidas.</span><span class="sxs-lookup"><span data-stu-id="f08cb-106">Invoking the RequestStateChange method multiple times could result in earlier requests being overwritten or lost.</span></span>

## <a name="syntax"></a><span data-ttu-id="f08cb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f08cb-107">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="f08cb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f08cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f08cb-109">*Requestedstate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f08cb-109">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f08cb-110">O estado solicitado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="f08cb-110">The state requested for the element.</span></span> <span data-ttu-id="f08cb-111">Essas informações serão colocadas na propriedade **requestedstate** da instância se o código de retorno do método **RequestStateChange** for 0 (' concluído sem erro ') ou 4096 (0x1000) (' trabalho iniciado ').</span><span class="sxs-lookup"><span data-stu-id="f08cb-111">This information will be placed into the **RequestedState** property of the instance if the return code of the **RequestStateChange** method is 0 ('Completed with No Error'), or 4096 (0x1000) ('Job Started').</span></span> <span data-ttu-id="f08cb-112">Consulte a descrição das propriedades **enabledstate** e **requestedstate** para obter as explicações detalhadas dos valores **requestedstate** .</span><span class="sxs-lookup"><span data-stu-id="f08cb-112">Refer to the description of the **EnabledState** and **RequestedState** properties for the detailed explanations of the **RequestedState** values.</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="f08cb-113"><span id="Start"></span><span id="start"></span><span id="START"></span>**Início** (2)</span><span class="sxs-lookup"><span data-stu-id="f08cb-113"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f08cb-114">Altera o estado para ' running '.</span><span class="sxs-lookup"><span data-stu-id="f08cb-114">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="f08cb-115"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspender** (3)</span><span class="sxs-lookup"><span data-stu-id="f08cb-115"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f08cb-116">Interrompe o trabalho temporariamente.</span><span class="sxs-lookup"><span data-stu-id="f08cb-116">Stops the job temporarily.</span></span> <span data-ttu-id="f08cb-117">A intenção é reiniciar subsequentemente o trabalho com ' Start '.</span><span class="sxs-lookup"><span data-stu-id="f08cb-117">The intention is to subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="f08cb-118">Pode ser possível inserir o estado ' serviço ' ao ser suspenso.</span><span class="sxs-lookup"><span data-stu-id="f08cb-118">It might be possible to enter the 'Service' state while suspended.</span></span> <span data-ttu-id="f08cb-119">(Isso é específico do trabalho.)</span><span class="sxs-lookup"><span data-stu-id="f08cb-119">(This is job-specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="f08cb-120"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminar** (4)</span><span class="sxs-lookup"><span data-stu-id="f08cb-120"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f08cb-121">Interrompe o trabalho corretamente, salva os dados, preserva o estado e desliga todos os processos subjacentes de maneira ordenada.</span><span class="sxs-lookup"><span data-stu-id="f08cb-121">Stops the job cleanly, saves data, preserves the state, and shuts down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="f08cb-122"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="f08cb-122"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f08cb-123">Encerra o trabalho imediatamente sem nenhum requisito para salvar dados ou preservar o estado.</span><span class="sxs-lookup"><span data-stu-id="f08cb-123">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f08cb-124"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Serviço** (6)</span><span class="sxs-lookup"><span data-stu-id="f08cb-124"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f08cb-125">Coloca o trabalho em um estado de serviço específico do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="f08cb-125">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="f08cb-126">Pode ser possível reiniciar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="f08cb-126">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f08cb-127"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="f08cb-127"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="f08cb-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="f08cb-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="f08cb-129">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="f08cb-129">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f08cb-130">Pode conter uma referência para o [**CIM \_ ConcreteJob**](cim-concretejob.md) criado para acompanhar a transição de estado iniciada pela invocação de método.</span><span class="sxs-lookup"><span data-stu-id="f08cb-130">May contain a reference to the [**CIM\_ConcreteJob**](cim-concretejob.md) created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="f08cb-131">*TimeoutPeriod* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f08cb-131">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f08cb-132">Um período de tempo limite que especifica a quantidade máxima de tempo que o cliente espera que a transição para o novo Estado tenha.</span><span class="sxs-lookup"><span data-stu-id="f08cb-132">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="f08cb-133">O formato do intervalo deve ser usado para especificar o período de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="f08cb-133">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="f08cb-134">Um valor 0 ou **NULL** indica que o cliente não tem requisitos de tempo para a transição.</span><span class="sxs-lookup"><span data-stu-id="f08cb-134">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="f08cb-135">Se essa propriedade não contiver 0 ou **NULL** e a implementação não oferecer suporte a esse parâmetro, um código de retorno 4098 (**uso do parâmetro timeout sem suporte**) deverá ser retornado.</span><span class="sxs-lookup"><span data-stu-id="f08cb-135">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f08cb-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f08cb-136">Return value</span></span>

<span data-ttu-id="f08cb-137">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="f08cb-137">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="f08cb-138">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="f08cb-138">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f08cb-139">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="f08cb-139">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f08cb-140">**Erro desconhecido ou não especificado** (2)</span><span class="sxs-lookup"><span data-stu-id="f08cb-140">**Unknown or Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f08cb-141">**Não é possível concluir dentro do período de tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="f08cb-141">**Cannot complete within Timeout Period** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f08cb-142">**Com falha** (4)</span><span class="sxs-lookup"><span data-stu-id="f08cb-142">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f08cb-143">**Parâmetro inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="f08cb-143">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f08cb-144">**Em uso** (6)</span><span class="sxs-lookup"><span data-stu-id="f08cb-144">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f08cb-145">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="f08cb-145">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f08cb-146">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="f08cb-146">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f08cb-147">**Transição de estado inválida** (4097)</span><span class="sxs-lookup"><span data-stu-id="f08cb-147">**Invalid State Transition** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="f08cb-148">**Não há suporte para o uso do parâmetro timeout** (4098)</span><span class="sxs-lookup"><span data-stu-id="f08cb-148">**Use of Timeout Parameter Not Supported** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="f08cb-149">**Ocupado** (4099)</span><span class="sxs-lookup"><span data-stu-id="f08cb-149">**Busy** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="f08cb-150">**Método reservado** (4100.. 32767)</span><span class="sxs-lookup"><span data-stu-id="f08cb-150">**Method Reserved** (4100..32767)</span></span>
</dt> <dt>

<span data-ttu-id="f08cb-151">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="f08cb-151">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f08cb-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f08cb-152">Requirements</span></span>



| <span data-ttu-id="f08cb-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="f08cb-153">Requirement</span></span> | <span data-ttu-id="f08cb-154">Valor</span><span class="sxs-lookup"><span data-stu-id="f08cb-154">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f08cb-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f08cb-155">Minimum supported client</span></span><br/> | <span data-ttu-id="f08cb-156">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f08cb-156">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="f08cb-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f08cb-157">Minimum supported server</span></span><br/> | <span data-ttu-id="f08cb-158">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f08cb-158">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="f08cb-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="f08cb-159">Namespace</span></span><br/>                | <span data-ttu-id="f08cb-160">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="f08cb-160">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f08cb-161">MOF</span><span class="sxs-lookup"><span data-stu-id="f08cb-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f08cb-162"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f08cb-162"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f08cb-163">DLL</span><span class="sxs-lookup"><span data-stu-id="f08cb-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f08cb-164"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f08cb-164"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f08cb-165">Confira também</span><span class="sxs-lookup"><span data-stu-id="f08cb-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f08cb-166">**\_ENABLEDLOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="f08cb-166">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

 





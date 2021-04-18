---
description: Altera o estado do trabalho.
ms.assetid: 3B11CE45-63E4-43D1-AAF6-02F83C9CBB85
title: 'Método Msvm_CopyFileToGuestJob:: RequestStateChange'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: adf5d866989f3b3518cf53b52e073239e023e3c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105775722"
---
# <a name="msvm_copyfiletoguestjobrequeststatechange-method"></a><span data-ttu-id="ccb6a-103">\_Método Msvm CopyFileToGuestJob:: RequestStateChange</span><span class="sxs-lookup"><span data-stu-id="ccb6a-103">Msvm\_CopyFileToGuestJob::RequestStateChange method</span></span>

<span data-ttu-id="ccb6a-104">Altera o estado do trabalho.</span><span class="sxs-lookup"><span data-stu-id="ccb6a-104">Changes the state of the job.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccb6a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ccb6a-105">Syntax</span></span>


```C++
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="ccb6a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ccb6a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccb6a-107">*Requestedstate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ccb6a-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccb6a-108">O novo estado.</span><span class="sxs-lookup"><span data-stu-id="ccb6a-108">The new state.</span></span> <span data-ttu-id="ccb6a-109">Estes são os valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="ccb6a-109">These are the possible values:</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="ccb6a-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Início** (2)</span><span class="sxs-lookup"><span data-stu-id="ccb6a-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ccb6a-111">Altera o estado para ' running '.</span><span class="sxs-lookup"><span data-stu-id="ccb6a-111">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="ccb6a-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspender** (3)</span><span class="sxs-lookup"><span data-stu-id="ccb6a-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ccb6a-113">Interrompe o trabalho temporariamente.</span><span class="sxs-lookup"><span data-stu-id="ccb6a-113">Stops the job temporarily.</span></span> <span data-ttu-id="ccb6a-114">O cliente pode, então, reiniciar o trabalho posteriormente com ' Start '.</span><span class="sxs-lookup"><span data-stu-id="ccb6a-114">The client can then subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="ccb6a-115">O cliente pode, possivelmente, inserir o estado ' serviço ' enquanto estiver suspenso (isso é específico do trabalho).</span><span class="sxs-lookup"><span data-stu-id="ccb6a-115">The client can possibly enter the 'Service' state while suspended (this is job-specific).</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="ccb6a-116"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminar** (4)</span><span class="sxs-lookup"><span data-stu-id="ccb6a-116"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="ccb6a-117">Interrompe o trabalho corretamente, salvando os dados, preservando o estado e desligando todos os processos subjacentes de maneira ordenada.</span><span class="sxs-lookup"><span data-stu-id="ccb6a-117">Stops the job cleanly, saving data, preserving the state, and shutting down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="ccb6a-118"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="ccb6a-118"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="ccb6a-119">Encerra o trabalho imediatamente sem nenhum requisito para salvar dados ou preservar o estado.</span><span class="sxs-lookup"><span data-stu-id="ccb6a-119">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ccb6a-120"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Serviço** (6)</span><span class="sxs-lookup"><span data-stu-id="ccb6a-120"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="ccb6a-121">Coloca o trabalho em um estado de serviço específico do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="ccb6a-121">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="ccb6a-122">O cliente pode possivelmente reiniciar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="ccb6a-122">The client can possibly restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="ccb6a-123"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="ccb6a-123"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="ccb6a-124"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="ccb6a-124"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="ccb6a-125">*TimeoutPeriod* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ccb6a-125">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccb6a-126">Um período de tempo limite que especifica a quantidade máxima de tempo que o cliente espera que a transição para o novo Estado tenha.</span><span class="sxs-lookup"><span data-stu-id="ccb6a-126">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="ccb6a-127">O formato do intervalo deve ser usado para especificar o período de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="ccb6a-127">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="ccb6a-128">Um valor 0 ou **NULL** indica que o cliente não tem requisitos de tempo para a transição.</span><span class="sxs-lookup"><span data-stu-id="ccb6a-128">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="ccb6a-129">Se essa propriedade não contiver 0 ou **NULL** e a implementação não oferecer suporte a esse parâmetro, um código de retorno 4098 (**uso do parâmetro timeout sem suporte**) deverá ser retornado.</span><span class="sxs-lookup"><span data-stu-id="ccb6a-129">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccb6a-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ccb6a-130">Return value</span></span>

<span data-ttu-id="ccb6a-131">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="ccb6a-131">This method returns one of the following values.</span></span>



| <span data-ttu-id="ccb6a-132">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ccb6a-132">Return code/value</span></span>                                                                                                                                                               | <span data-ttu-id="ccb6a-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="ccb6a-133">Description</span></span>                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ccb6a-134"><dt>**Concluído sem erro**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ccb6a-134"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                   | <span data-ttu-id="ccb6a-135">Êxito.</span><span class="sxs-lookup"><span data-stu-id="ccb6a-135">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="ccb6a-136"><dt>**Uso do parâmetro timeout sem suporte**</dt> <dt>4098</dt></span><span class="sxs-lookup"><span data-stu-id="ccb6a-136"><dt>**Use of Timeout Parameter Not Supported**</dt> <dt>4098</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="ccb6a-137"><dt>32768</dt> <dt>**com falha**</dt></span><span class="sxs-lookup"><span data-stu-id="ccb6a-137"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                |                                                                                    |
| <dl> <span data-ttu-id="ccb6a-138"><dt>**Acesso negado**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="ccb6a-138"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                         | <span data-ttu-id="ccb6a-139">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="ccb6a-139">Access denied.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="ccb6a-140"><dt>**Sem suporte**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="ccb6a-140"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                         |                                                                                    |
| <dl> <span data-ttu-id="ccb6a-141">O <dt>**status é desconhecido**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="ccb6a-141"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                     |                                                                                    |
| <dl> <span data-ttu-id="ccb6a-142"><dt>**Tempo limite**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="ccb6a-142"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                               |                                                                                    |
| <dl> <span data-ttu-id="ccb6a-143"><dt>**Parâmetro inválido**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="ccb6a-143"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                     |                                                                                    |
| <dl> <span data-ttu-id="ccb6a-144">O <dt>**sistema está em uso**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="ccb6a-144"><dt>**System is in use**</dt> <dt>32774</dt></span></span> </dl>                      |                                                                                    |
| <dl> <span data-ttu-id="ccb6a-145"><dt>**Estado inválido para esta operação**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="ccb6a-145"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>      | <span data-ttu-id="ccb6a-146">Não há suporte para o valor especificado no parâmetro *requestedstate* .</span><span class="sxs-lookup"><span data-stu-id="ccb6a-146">The value specified in the *RequestedState* parameter is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="ccb6a-147"><dt>**Tipo de dados incorreto**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="ccb6a-147"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                   |                                                                                    |
| <dl> <span data-ttu-id="ccb6a-148">O <dt>**sistema não está disponível**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="ccb6a-148"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>               |                                                                                    |
| <dl> <span data-ttu-id="ccb6a-149"><dt>**Memória insuficiente**</dt> <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="ccb6a-149"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                         |                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="ccb6a-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccb6a-150">Requirements</span></span>



| <span data-ttu-id="ccb6a-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccb6a-151">Requirement</span></span> | <span data-ttu-id="ccb6a-152">Valor</span><span class="sxs-lookup"><span data-stu-id="ccb6a-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccb6a-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ccb6a-153">Minimum supported client</span></span><br/> | <span data-ttu-id="ccb6a-154">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ccb6a-154">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="ccb6a-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ccb6a-155">Minimum supported server</span></span><br/> | <span data-ttu-id="ccb6a-156">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="ccb6a-156">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ccb6a-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="ccb6a-157">Namespace</span></span><br/>                | <span data-ttu-id="ccb6a-158">\\\\\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="ccb6a-158">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="ccb6a-159">MOF</span><span class="sxs-lookup"><span data-stu-id="ccb6a-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ccb6a-160"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ccb6a-160"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ccb6a-161">DLL</span><span class="sxs-lookup"><span data-stu-id="ccb6a-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccb6a-162"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ccb6a-162"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ccb6a-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="ccb6a-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccb6a-164">**Msvm \_ CopyFileToGuestJob**</span><span class="sxs-lookup"><span data-stu-id="ccb6a-164">**Msvm\_CopyFileToGuestJob**</span></span>](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

 





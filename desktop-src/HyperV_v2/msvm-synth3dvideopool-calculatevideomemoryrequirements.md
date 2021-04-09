---
description: Calcula a quantidade de memória de vídeo necessária para uma máquina virtual do RemoteFX.
ms.assetid: F8C30601-EDA3-47F1-A717-9FE7E9DB8F62
title: Método CalculateVideoMemoryRequirements da classe Msvm_Synth3dVideoPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synth3dVideoPool.CalculateVideoMemoryRequirements
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2a9fd80e777a9d166b896c2ce51d03bd91bbabfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090669"
---
# <a name="calculatevideomemoryrequirements-method-of-the-msvm_synth3dvideopool-class"></a><span data-ttu-id="6ddad-103">Método CalculateVideoMemoryRequirements da \_ classe Synth3dVideoPool Msvm</span><span class="sxs-lookup"><span data-stu-id="6ddad-103">CalculateVideoMemoryRequirements method of the Msvm\_Synth3dVideoPool class</span></span>

<span data-ttu-id="6ddad-104">Calcula a quantidade de memória de vídeo necessária para uma máquina virtual do RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="6ddad-104">Calculates the amount of video memory required for a RemoteFX virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ddad-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6ddad-105">Syntax</span></span>


```mof
uint32 CalculateVideoMemoryRequirements(
  [in]  uint32 monitorResolution,
  [in]  uint32 numberOfMonitors,
  [out] uint64 requiredVideoMemory
);
```



## <a name="parameters"></a><span data-ttu-id="6ddad-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ddad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ddad-107">*monitorResolution* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6ddad-107">*monitorResolution* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ddad-108">A resolução máxima do monitor para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6ddad-108">The maximum monitor resolution for the virtual machine.</span></span> <span data-ttu-id="6ddad-109">Deve ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="6ddad-109">This must be one of the following values.</span></span>



| <span data-ttu-id="6ddad-110">Valor</span><span class="sxs-lookup"><span data-stu-id="6ddad-110">Value</span></span>                                                                        | <span data-ttu-id="6ddad-111">Significado</span><span class="sxs-lookup"><span data-stu-id="6ddad-111">Meaning</span></span>                                           |
|------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="6ddad-112"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6ddad-112"><dt>0</dt></span></span> </dl> | <span data-ttu-id="6ddad-113">A resolução máxima é 1024 768.</span><span class="sxs-lookup"><span data-stu-id="6ddad-113">The maximum resolution is 1024   768.</span></span><br/>  |
| <dl> <span data-ttu-id="6ddad-114"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6ddad-114"><dt>1</dt></span></span> </dl> | <span data-ttu-id="6ddad-115">A resolução máxima é 1280 1024.</span><span class="sxs-lookup"><span data-stu-id="6ddad-115">The maximum resolution is 1280   1024.</span></span><br/> |
| <dl> <span data-ttu-id="6ddad-116"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6ddad-116"><dt>2</dt></span></span> </dl> | <span data-ttu-id="6ddad-117">A resolução máxima é 1600 1200.</span><span class="sxs-lookup"><span data-stu-id="6ddad-117">The maximum resolution is 1600   1200.</span></span><br/> |
| <dl> <span data-ttu-id="6ddad-118"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="6ddad-118"><dt>3</dt></span></span> </dl> | <span data-ttu-id="6ddad-119">A resolução máxima é 1920 1200.</span><span class="sxs-lookup"><span data-stu-id="6ddad-119">The maximum resolution is 1920   1200.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6ddad-120">*numberOfMonitors* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6ddad-120">*numberOfMonitors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ddad-121">O número máximo de monitores para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6ddad-121">The maximum number of monitors for the virtual machine.</span></span> <span data-ttu-id="6ddad-122">O número mínimo de monitores é um e o máximo depende da resolução máxima da tela.</span><span class="sxs-lookup"><span data-stu-id="6ddad-122">The minimum number of monitors is one and the maximum is dependent upon the maximum screen resolution.</span></span> <span data-ttu-id="6ddad-123">A tabela a seguir define o número máximo de monitores permitidos para resoluções diferentes.</span><span class="sxs-lookup"><span data-stu-id="6ddad-123">The following table defines the maximum number of monitors allowed for different resolutions.</span></span>



| <span data-ttu-id="6ddad-124">Resolução</span><span class="sxs-lookup"><span data-stu-id="6ddad-124">Resolution</span></span>             | <span data-ttu-id="6ddad-125">Máximo de monitores</span><span class="sxs-lookup"><span data-stu-id="6ddad-125">Maximum monitors</span></span> |
|------------------------|------------------|
| <span data-ttu-id="6ddad-126">1024 768</span><span class="sxs-lookup"><span data-stu-id="6ddad-126">1024   768</span></span><br/>  | <span data-ttu-id="6ddad-127">4</span><span class="sxs-lookup"><span data-stu-id="6ddad-127">4</span></span><br/>     |
| <span data-ttu-id="6ddad-128">1280 1024</span><span class="sxs-lookup"><span data-stu-id="6ddad-128">1280   1024</span></span><br/> | <span data-ttu-id="6ddad-129">4</span><span class="sxs-lookup"><span data-stu-id="6ddad-129">4</span></span><br/>     |
| <span data-ttu-id="6ddad-130">1600 1200</span><span class="sxs-lookup"><span data-stu-id="6ddad-130">1600   1200</span></span><br/> | <span data-ttu-id="6ddad-131">3</span><span class="sxs-lookup"><span data-stu-id="6ddad-131">3</span></span><br/>     |
| <span data-ttu-id="6ddad-132">1920 1200</span><span class="sxs-lookup"><span data-stu-id="6ddad-132">1920   1200</span></span><br/> | <span data-ttu-id="6ddad-133">2</span><span class="sxs-lookup"><span data-stu-id="6ddad-133">2</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="6ddad-134">*requiredVideoMemory* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6ddad-134">*requiredVideoMemory* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ddad-135">Recebe a quantidade necessária de memória de vídeo, em bytes.</span><span class="sxs-lookup"><span data-stu-id="6ddad-135">Receives the required amount of video memory, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ddad-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6ddad-136">Return value</span></span>

<span data-ttu-id="6ddad-137">Retorna um código de status, que pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="6ddad-137">Returns a status code, which can be one of the following values.</span></span>



| <span data-ttu-id="6ddad-138">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6ddad-138">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="6ddad-139">Descrição</span><span class="sxs-lookup"><span data-stu-id="6ddad-139">Description</span></span>                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="6ddad-140"><dt>**Concluído sem erro**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6ddad-140"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="6ddad-141">Bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6ddad-141">Successful.</span></span><br/>                                |
| <dl> <span data-ttu-id="6ddad-142"><dt>**Parâmetros de método verificados-trabalho iniciado**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="6ddad-142"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="6ddad-143">Trabalho iniciado.</span><span class="sxs-lookup"><span data-stu-id="6ddad-143">Job started.</span></span><br/>                               |
| <dl> <span data-ttu-id="6ddad-144"><dt>32768</dt> <dt>**com falha**</dt></span><span class="sxs-lookup"><span data-stu-id="6ddad-144"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                 | <span data-ttu-id="6ddad-145">Falhou.</span><span class="sxs-lookup"><span data-stu-id="6ddad-145">Failed.</span></span><br/>                                    |
| <dl> <span data-ttu-id="6ddad-146"><dt>**Acesso negado**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="6ddad-146"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                          | <span data-ttu-id="6ddad-147">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="6ddad-147">Access denied.</span></span><br/>                             |
| <dl> <span data-ttu-id="6ddad-148"><dt>**Sem suporte**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="6ddad-148"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                          | <span data-ttu-id="6ddad-149">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="6ddad-149">Not supported.</span></span><br/>                             |
| <dl> <span data-ttu-id="6ddad-150">O <dt>**status é desconhecido**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="6ddad-150"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                      | <span data-ttu-id="6ddad-151">O status é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="6ddad-151">Status is unknown.</span></span><br/>                         |
| <dl> <span data-ttu-id="6ddad-152"><dt>**Tempo limite**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="6ddad-152"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                                | <span data-ttu-id="6ddad-153">Tempo limite.</span><span class="sxs-lookup"><span data-stu-id="6ddad-153">Timeout.</span></span><br/>                                   |
| <dl> <span data-ttu-id="6ddad-154"><dt>**Parâmetro inválido**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="6ddad-154"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                      | <span data-ttu-id="6ddad-155">Um parâmetro não é válido.</span><span class="sxs-lookup"><span data-stu-id="6ddad-155">A parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="6ddad-156">O <dt>**sistema está em uso**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="6ddad-156"><dt>**System is in used**</dt> <dt>32774</dt></span></span> </dl>                      | <span data-ttu-id="6ddad-157">O sistema está em uso.</span><span class="sxs-lookup"><span data-stu-id="6ddad-157">System is in use.</span></span><br/>                          |
| <dl> <span data-ttu-id="6ddad-158"><dt>**Estado inválido para esta operação**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="6ddad-158"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>       | <span data-ttu-id="6ddad-159">O estado não é válido para esta operação.</span><span class="sxs-lookup"><span data-stu-id="6ddad-159">The state is not valid for this operation.</span></span><br/> |
| <dl> <span data-ttu-id="6ddad-160"><dt>**Tipo de dados incorreto**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="6ddad-160"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                    | <span data-ttu-id="6ddad-161">Tipo de dados incorreto.</span><span class="sxs-lookup"><span data-stu-id="6ddad-161">Incorrect data type.</span></span><br/>                       |
| <dl> <span data-ttu-id="6ddad-162">O <dt>**sistema não está disponível**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="6ddad-162"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>                | <span data-ttu-id="6ddad-163">O sistema não está disponível.</span><span class="sxs-lookup"><span data-stu-id="6ddad-163">System is not available.</span></span><br/>                   |
| <dl> <span data-ttu-id="6ddad-164"><dt>**Memória insuficiente**</dt> <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="6ddad-164"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                          | <span data-ttu-id="6ddad-165">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="6ddad-165">Out of memory.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="6ddad-166">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ddad-166">Remarks</span></span>

<span data-ttu-id="6ddad-167">Esse método é normalmente chamado no sistema host para determinar se o host tem memória de vídeo disponível suficiente para hospedar uma máquina virtual do RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="6ddad-167">This method is typically called on the host system to determine if the host has enough available video memory to host a RemoteFX virtual machine.</span></span> <span data-ttu-id="6ddad-168">Para fazer isso, você compara a quantidade de memória de vídeo calculada por esse método com a propriedade [**Msvm \_ PhysicalGPUInfo. AvailableVideoMemory**](msvm-physicalgpuinfo.md) para determinar se o computador host tem memória de vídeo disponível suficiente.</span><span class="sxs-lookup"><span data-stu-id="6ddad-168">To do this, you compare the amount of video memory calculated by this method with the [**Msvm\_PhysicalGPUInfo.AvailableVideoMemory**](msvm-physicalgpuinfo.md) property to determine if the host machine has enough available video memory.</span></span> <span data-ttu-id="6ddad-169">Você pode usar essas informações para determinar se uma máquina virtual pode ser movida para o sistema host.</span><span class="sxs-lookup"><span data-stu-id="6ddad-169">You can use this information to determine if a virtual machine can be moved to the host system.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ddad-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ddad-170">Requirements</span></span>



| <span data-ttu-id="6ddad-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ddad-171">Requirement</span></span> | <span data-ttu-id="6ddad-172">Valor</span><span class="sxs-lookup"><span data-stu-id="6ddad-172">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ddad-173">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ddad-173">Minimum supported client</span></span><br/> | <span data-ttu-id="6ddad-174">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6ddad-174">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6ddad-175">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ddad-175">Minimum supported server</span></span><br/> | <span data-ttu-id="6ddad-176">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6ddad-176">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6ddad-177">Namespace</span><span class="sxs-lookup"><span data-stu-id="6ddad-177">Namespace</span></span><br/>                | <span data-ttu-id="6ddad-178">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="6ddad-178">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6ddad-179">MOF</span><span class="sxs-lookup"><span data-stu-id="6ddad-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ddad-180"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6ddad-180"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ddad-181">DLL</span><span class="sxs-lookup"><span data-stu-id="6ddad-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ddad-182"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6ddad-182"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6ddad-183">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ddad-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ddad-184">**Msvm \_ PhysicalGPUInfo**</span><span class="sxs-lookup"><span data-stu-id="6ddad-184">**Msvm\_PhysicalGPUInfo**</span></span>](msvm-physicalgpuinfo.md)
</dt> <dt>

[<span data-ttu-id="6ddad-185">**Msvm \_ Synth3dVideoPool**</span><span class="sxs-lookup"><span data-stu-id="6ddad-185">**Msvm\_Synth3dVideoPool**</span></span>](msvm-synth3dvideopool.md)
</dt> </dl>

 

 





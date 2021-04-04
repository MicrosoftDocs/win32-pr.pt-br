---
description: Define os dados de configuração da máquina inicial de VMs.
ms.assetid: 0f174d29-ddb2-4a8c-b664-926245573778
title: Método SetInitialMachineConfigurationData da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.SetInitialMachineConfigurationData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 08028358d6bb53406abe15c88e0acd02e748d387
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646819"
---
# <a name="setinitialmachineconfigurationdata-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="0a1af-103">Método SetInitialMachineConfigurationData da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="0a1af-103">SetInitialMachineConfigurationData method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="0a1af-104">Define os dados de configuração inicial da máquina VM.</span><span class="sxs-lookup"><span data-stu-id="0a1af-104">Sets a VM's initial machine configuration data.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a1af-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a1af-105">Syntax</span></span>


```mof
uint32 SetInitialMachineConfigurationData(
  [in]  CIM_ComputerSystem REF TargetSystem,
  [in]  uint8                  ImcData[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="0a1af-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a1af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a1af-107">*TargetSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0a1af-107">*TargetSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a1af-108">Uma referência ao sistema de computador virtual no qual os dados do IMC serão definidos.</span><span class="sxs-lookup"><span data-stu-id="0a1af-108">A reference to the virtual computer system on which the IMC data will be set.</span></span>

</dd> <dt>

<span data-ttu-id="0a1af-109">*Imcdata* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0a1af-109">*ImcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a1af-110">Os dados do IMC a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="0a1af-110">The IMC data to set.</span></span> <span data-ttu-id="0a1af-111">Os primeiros quatro bytes devem ser o comprimento da matriz na ordem big-endian</span><span class="sxs-lookup"><span data-stu-id="0a1af-111">The first four bytes must be the length of the array in big-endian order</span></span>

</dd> <dt>

<span data-ttu-id="0a1af-112">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="0a1af-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a1af-113">Um parâmetro opcional para monitorar o progresso da operação, que é usado se o método não pôde ser executado de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="0a1af-113">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="0a1af-114">Se a operação estiver sendo executada de forma assíncrona, o valor de retorno será 4096.</span><span class="sxs-lookup"><span data-stu-id="0a1af-114">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a1af-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0a1af-115">Return value</span></span>

<span data-ttu-id="0a1af-116">Em caso de sucesso, retorna 0 ou 4096; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="0a1af-116">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="0a1af-117">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="0a1af-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0a1af-118">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="0a1af-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0a1af-119">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="0a1af-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="0a1af-120">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="0a1af-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="0a1af-121">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="0a1af-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="0a1af-122">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="0a1af-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="0a1af-123">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="0a1af-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="0a1af-124">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="0a1af-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="0a1af-125">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="0a1af-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="0a1af-126">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="0a1af-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="0a1af-127">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="0a1af-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="0a1af-128">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="0a1af-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="0a1af-129">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="0a1af-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="0a1af-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a1af-130">Requirements</span></span>



| <span data-ttu-id="0a1af-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a1af-131">Requirement</span></span> | <span data-ttu-id="0a1af-132">Valor</span><span class="sxs-lookup"><span data-stu-id="0a1af-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a1af-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0a1af-133">Minimum supported client</span></span><br/> | <span data-ttu-id="0a1af-134">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0a1af-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="0a1af-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0a1af-135">Minimum supported server</span></span><br/> | <span data-ttu-id="0a1af-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0a1af-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="0a1af-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="0a1af-137">Namespace</span></span><br/>                | <span data-ttu-id="0a1af-138">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="0a1af-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0a1af-139">MOF</span><span class="sxs-lookup"><span data-stu-id="0a1af-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0a1af-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0a1af-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0a1af-141">DLL</span><span class="sxs-lookup"><span data-stu-id="0a1af-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a1af-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0a1af-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0a1af-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a1af-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a1af-144">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="0a1af-144">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 





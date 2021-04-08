---
description: Obtém uma lista de instâncias do Msvm \_ CompatibilityVector que podem ser usadas para verificar a compatibilidade do host de máquinas virtuais (VM).
ms.assetid: 3881D9A0-07C2-4275-925D-F3C3A36B79B4
title: 'Método Msvm_VirtualSystemMigrationService:: GetSystemCompatibilityVectors'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.GetSystemCompatibilityVectors
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8ef8a374d992468247f6dc8f914d7252e7cd2829
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920731"
---
# <a name="msvm_virtualsystemmigrationservicegetsystemcompatibilityvectors-method"></a><span data-ttu-id="61a0d-103">\_Método Msvm VirtualSystemMigrationService:: GetSystemCompatibilityVectors</span><span class="sxs-lookup"><span data-stu-id="61a0d-103">Msvm\_VirtualSystemMigrationService::GetSystemCompatibilityVectors method</span></span>

<span data-ttu-id="61a0d-104">Obtém uma lista de instâncias do [**Msvm \_ CompatibilityVector**](msvm-compatibilityvector.md) que podem ser usadas para verificar a compatibilidade do host de máquinas virtuais (VM).</span><span class="sxs-lookup"><span data-stu-id="61a0d-104">Gets a list of [**Msvm\_CompatibilityVector**](msvm-compatibilityvector.md) instances that can be used to check for virtual machine (VM) to host compatibility.</span></span>

## <a name="syntax"></a><span data-ttu-id="61a0d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61a0d-105">Syntax</span></span>


```C++
uint32 GetSystemCompatibilityVectors(
  [in]  CIM_ComputerSystem   ComputerSystem,
  [out] Msvm_CompatibilityVector CompatibilityVectors[]
);
```



## <a name="parameters"></a><span data-ttu-id="61a0d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="61a0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61a0d-107">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="61a0d-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61a0d-108">Uma referência a uma classe de [**\_ ComputerSystem Msvm**](msvm-computersystem.md) que representa a VM para a qual os vetores de compatibilidade são recuperados.</span><span class="sxs-lookup"><span data-stu-id="61a0d-108">A reference to a [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the VM to retrieve compatibility vectors for.</span></span> <span data-ttu-id="61a0d-109">Se esse parâmetro se referir ao sistema de computador de hospedagem, os dados retornados no parâmetro *CompatibilityVectors* poderão ser usados para determinar se alguma das VMs no sistema de computador de hospedagem pode ser migrada rapidamente para outro sistema de computador de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="61a0d-109">If this parameter refers to the hosting computer system, the data returned in the *CompatibilityVectors* parameter can be used to determine whether any of the VMs on the hosting computer system can be quickly migrated to another hosting computer system.</span></span>

</dd> <dt>

<span data-ttu-id="61a0d-110">*CompatibilityVectors* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="61a0d-110">*CompatibilityVectors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61a0d-111">Uma matriz de instâncias do [**Msvm \_ CompatibilityVector**](msvm-compatibilityvector.md) que contém as informações de compatibilidade para as VMs ou o sistema de computador de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="61a0d-111">An array of [**Msvm\_CompatibilityVector**](msvm-compatibilityvector.md) instances that contain the compatibility info for the VMs or hosting computer system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61a0d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="61a0d-112">Return value</span></span>

<span data-ttu-id="61a0d-113">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="61a0d-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="61a0d-114">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="61a0d-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="61a0d-115">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="61a0d-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="61a0d-116">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="61a0d-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="61a0d-117">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="61a0d-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="61a0d-118">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="61a0d-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="61a0d-119">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="61a0d-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="61a0d-120">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="61a0d-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="61a0d-121">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="61a0d-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="61a0d-122">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="61a0d-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="61a0d-123">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="61a0d-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="61a0d-124">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="61a0d-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="61a0d-125">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="61a0d-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="61a0d-126">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="61a0d-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="61a0d-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="61a0d-127">Remarks</span></span>

<span data-ttu-id="61a0d-128">**GetSystemCompatibilityVectors** Obtém informações de compatibilidade para uma VM (máquina virtual) (quando executado em um sistema de computador VM) ou um host (quando executado em um sistema de computador host).</span><span class="sxs-lookup"><span data-stu-id="61a0d-128">**GetSystemCompatibilityVectors** gets compatibility info for a virtual machine (VM) (when run on a VM computer system) or a host (when run on a host computer system).</span></span> <span data-ttu-id="61a0d-129">As informações de compatibilidade permanecem opacas para o cliente, enquanto as informações fornecem uma maneira de comparar as informações de compatibilidade do host com aquela da VM.</span><span class="sxs-lookup"><span data-stu-id="61a0d-129">The compatibility info remains opaque to the client while the info provides a way to compare the host compatibility info with that of the VM.</span></span>

## <a name="requirements"></a><span data-ttu-id="61a0d-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61a0d-130">Requirements</span></span>



| <span data-ttu-id="61a0d-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="61a0d-131">Requirement</span></span> | <span data-ttu-id="61a0d-132">Valor</span><span class="sxs-lookup"><span data-stu-id="61a0d-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61a0d-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61a0d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="61a0d-134">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="61a0d-134">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="61a0d-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61a0d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="61a0d-136">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="61a0d-136">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="61a0d-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="61a0d-137">Namespace</span></span><br/>                | <span data-ttu-id="61a0d-138">\\\\\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="61a0d-138">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="61a0d-139">MOF</span><span class="sxs-lookup"><span data-stu-id="61a0d-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61a0d-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="61a0d-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="61a0d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="61a0d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61a0d-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="61a0d-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="61a0d-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="61a0d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61a0d-144">**Msvm \_ CompatibilityVector**</span><span class="sxs-lookup"><span data-stu-id="61a0d-144">**Msvm\_CompatibilityVector**</span></span>](msvm-compatibilityvector.md)
</dt> <dt>

[<span data-ttu-id="61a0d-145">**Msvm \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="61a0d-145">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 





---
description: Atualiza o sistema virtual.
ms.assetid: 4b24aac9-b7b9-460f-9227-fd3c1e960191
title: Método UpgradeSystemVersion da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.UpgradeSystemVersion
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4c34b33da14d8718f2c2414de3aea3079672bbb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812931"
---
# <a name="upgradesystemversion-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="589a1-103">Método UpgradeSystemVersion da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="589a1-103">UpgradeSystemVersion method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="589a1-104">Atualiza o sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="589a1-104">Upgrades the virtual system.</span></span>

<span data-ttu-id="589a1-105">Quando aplicado às configurações do sistema de uma configuração de sistema virtual "atual"</span><span class="sxs-lookup"><span data-stu-id="589a1-105">When applied to the system settings of a "current" virtual system configuration</span></span>

## <a name="syntax"></a><span data-ttu-id="589a1-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="589a1-106">Syntax</span></span>


```mof
uint32 UpgradeSystemVersion(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 UpgradeSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="589a1-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="589a1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="589a1-108">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="589a1-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="589a1-109">Uma referência a um [**computador \_ CIM**](cim-computersystem.md) que representa o sistema de máquina virtual a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="589a1-109">A reference to a [**CIM\_ComputerSystem**](cim-computersystem.md) that represents the virtual computer system to be upgraded.</span></span>

</dd> <dt>

<span data-ttu-id="589a1-110">*UpgradeSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="589a1-110">*UpgradeSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="589a1-111">Os dados de configuração de atualização.</span><span class="sxs-lookup"><span data-stu-id="589a1-111">The upgrade setting data.</span></span>

</dd> <dt>

<span data-ttu-id="589a1-112">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="589a1-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="589a1-113">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="589a1-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="589a1-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="589a1-114">Return value</span></span>

<span data-ttu-id="589a1-115">Em caso de sucesso, retorna 0 ou 4096; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="589a1-115">On success, returns a 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="589a1-116">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="589a1-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="589a1-117">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="589a1-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="589a1-118">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="589a1-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="589a1-119">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="589a1-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="589a1-120">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="589a1-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="589a1-121">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="589a1-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="589a1-122">**Parâmetros incompatíveis** (6)</span><span class="sxs-lookup"><span data-stu-id="589a1-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="589a1-123">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="589a1-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="589a1-124">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="589a1-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="589a1-125">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="589a1-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="589a1-126">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="589a1-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="589a1-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="589a1-127">Requirements</span></span>



| <span data-ttu-id="589a1-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="589a1-128">Requirement</span></span> | <span data-ttu-id="589a1-129">Valor</span><span class="sxs-lookup"><span data-stu-id="589a1-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="589a1-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="589a1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="589a1-131">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="589a1-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="589a1-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="589a1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="589a1-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="589a1-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="589a1-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="589a1-134">Namespace</span></span><br/>                | <span data-ttu-id="589a1-135">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="589a1-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="589a1-136">MOF</span><span class="sxs-lookup"><span data-stu-id="589a1-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="589a1-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="589a1-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="589a1-138">DLL</span><span class="sxs-lookup"><span data-stu-id="589a1-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="589a1-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="589a1-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="589a1-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="589a1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="589a1-141">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="589a1-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 


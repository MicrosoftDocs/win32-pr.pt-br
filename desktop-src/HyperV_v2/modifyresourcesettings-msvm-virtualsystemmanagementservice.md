---
description: Modifica as configurações de recursos virtuais.
ms.assetid: 3fb2a65f-9f40-4eb9-99e8-8fe1451427d9
title: Método ModifyResourceSettings da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 872e81926f717671b741a89c9bf954e452803b36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829361"
---
# <a name="modifyresourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="fe0bd-103">Método ModifyResourceSettings da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="fe0bd-103">ModifyResourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="fe0bd-104">Modifica as configurações de recursos virtuais.</span><span class="sxs-lookup"><span data-stu-id="fe0bd-104">Modifies virtual resource settings.</span></span> <span data-ttu-id="fe0bd-105">Quando aplicado a partes de uma configuração de máquina virtual atual, como um efeito colateral, os recursos da máquina virtual ativa podem ser modificados.</span><span class="sxs-lookup"><span data-stu-id="fe0bd-105">When applied to parts of a current virtual machine configuration, as a side effect, the resources of the active virtual machine may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe0bd-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fe0bd-106">Syntax</span></span>


```mof
uint32 ModifyResourceSettings(
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="fe0bd-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe0bd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe0bd-108">*ResourceSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fe0bd-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe0bd-109">Uma matriz de cadeias de caracteres que contém uma instância incorporada de uma classe derivada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), que contém os aspectos modificados dos recursos virtuais existentes.</span><span class="sxs-lookup"><span data-stu-id="fe0bd-109">An array of strings that contain an embedded instance of a class derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), that contain the modified aspects of existing virtual resources.</span></span> <span data-ttu-id="fe0bd-110">A propriedade **InstanceId** de cada instância identifica a configuração de recurso virtual a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="fe0bd-110">The **InstanceID** property of each instance identifies the virtual resource setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="fe0bd-111">*ResultingResourceSettings* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fe0bd-111">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe0bd-112">Uma matriz de referências a instâncias de objetos derivados de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) que representa aspectos virtuais dos recursos virtuais modificados.</span><span class="sxs-lookup"><span data-stu-id="fe0bd-112">An array of references to instances of objects derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) representing virtual aspects of the modified virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="fe0bd-113">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="fe0bd-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe0bd-114">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fe0bd-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe0bd-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fe0bd-115">Return value</span></span>

<span data-ttu-id="fe0bd-116">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="fe0bd-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="fe0bd-117">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="fe0bd-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fe0bd-118">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="fe0bd-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fe0bd-119">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="fe0bd-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fe0bd-120">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="fe0bd-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fe0bd-121">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="fe0bd-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fe0bd-122">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="fe0bd-122">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="fe0bd-123">**Parâmetros incompatíveis** (6)</span><span class="sxs-lookup"><span data-stu-id="fe0bd-123">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="fe0bd-124">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="fe0bd-124">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="fe0bd-125">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="fe0bd-125">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="fe0bd-126">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="fe0bd-126">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="fe0bd-127">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="fe0bd-127">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="fe0bd-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe0bd-128">Requirements</span></span>



| <span data-ttu-id="fe0bd-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe0bd-129">Requirement</span></span> | <span data-ttu-id="fe0bd-130">Valor</span><span class="sxs-lookup"><span data-stu-id="fe0bd-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe0bd-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe0bd-131">Minimum supported client</span></span><br/> | <span data-ttu-id="fe0bd-132">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="fe0bd-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fe0bd-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe0bd-133">Minimum supported server</span></span><br/> | <span data-ttu-id="fe0bd-134">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="fe0bd-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fe0bd-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="fe0bd-135">Namespace</span></span><br/>                | <span data-ttu-id="fe0bd-136">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="fe0bd-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fe0bd-137">MOF</span><span class="sxs-lookup"><span data-stu-id="fe0bd-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fe0bd-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fe0bd-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fe0bd-139">DLL</span><span class="sxs-lookup"><span data-stu-id="fe0bd-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe0bd-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fe0bd-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fe0bd-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe0bd-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe0bd-142">**ModifyVirtualSystemResources (v1)**</span><span class="sxs-lookup"><span data-stu-id="fe0bd-142">**ModifyVirtualSystemResources (V1)**</span></span>](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="fe0bd-143">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="fe0bd-143">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 


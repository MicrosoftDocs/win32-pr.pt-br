---
description: Método ModifyResourceSettings da classe Msvm_VirtualSystemManagementService-modifica as configurações de recurso virtual.
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
ms.openlocfilehash: 09ca0bb9fea02b6acc5599d9f907b1e60fdbd9ec
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119334"
---
# <a name="modifyresourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="09067-103">Método ModifyResourceSettings da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="09067-103">ModifyResourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="09067-104">Modifica as configurações de recursos virtuais.</span><span class="sxs-lookup"><span data-stu-id="09067-104">Modifies virtual resource settings.</span></span> <span data-ttu-id="09067-105">Quando aplicado a partes de uma configuração de máquina virtual atual, como um efeito colateral, os recursos da máquina virtual ativa podem ser modificados.</span><span class="sxs-lookup"><span data-stu-id="09067-105">When applied to parts of a current virtual machine configuration, as a side effect, the resources of the active virtual machine may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="09067-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09067-106">Syntax</span></span>


```mof
uint32 ModifyResourceSettings(
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="09067-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09067-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09067-108">*ResourceSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09067-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09067-109">Uma matriz de cadeias de caracteres que contém uma instância incorporada de uma classe derivada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), que contém os aspectos modificados dos recursos virtuais existentes.</span><span class="sxs-lookup"><span data-stu-id="09067-109">An array of strings that contain an embedded instance of a class derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), that contain the modified aspects of existing virtual resources.</span></span> <span data-ttu-id="09067-110">A propriedade **InstanceId** de cada instância identifica a configuração de recurso virtual a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="09067-110">The **InstanceID** property of each instance identifies the virtual resource setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="09067-111">*ResultingResourceSettings* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="09067-111">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09067-112">Uma matriz de referências a instâncias de objetos derivados de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) que representa aspectos virtuais dos recursos virtuais modificados.</span><span class="sxs-lookup"><span data-stu-id="09067-112">An array of references to instances of objects derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) representing virtual aspects of the modified virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="09067-113">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="09067-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09067-114">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="09067-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09067-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="09067-115">Return value</span></span>

<span data-ttu-id="09067-116">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="09067-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="09067-117">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="09067-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="09067-118">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="09067-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="09067-119">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="09067-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="09067-120">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="09067-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="09067-121">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="09067-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="09067-122">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="09067-122">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="09067-123">**Parâmetros incompatíveis** (6)</span><span class="sxs-lookup"><span data-stu-id="09067-123">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="09067-124">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="09067-124">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="09067-125">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="09067-125">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="09067-126">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="09067-126">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="09067-127">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="09067-127">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="09067-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09067-128">Requirements</span></span>



| <span data-ttu-id="09067-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="09067-129">Requirement</span></span> | <span data-ttu-id="09067-130">Valor</span><span class="sxs-lookup"><span data-stu-id="09067-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09067-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09067-131">Minimum supported client</span></span><br/> | <span data-ttu-id="09067-132">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="09067-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="09067-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09067-133">Minimum supported server</span></span><br/> | <span data-ttu-id="09067-134">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="09067-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="09067-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="09067-135">Namespace</span></span><br/>                | <span data-ttu-id="09067-136">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="09067-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="09067-137">MOF</span><span class="sxs-lookup"><span data-stu-id="09067-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="09067-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="09067-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="09067-139">DLL</span><span class="sxs-lookup"><span data-stu-id="09067-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09067-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="09067-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="09067-141">Consulte também</span><span class="sxs-lookup"><span data-stu-id="09067-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09067-142">**ModifyVirtualSystemResources (v1)**</span><span class="sxs-lookup"><span data-stu-id="09067-142">**ModifyVirtualSystemResources (V1)**</span></span>](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="09067-143">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="09067-143">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 


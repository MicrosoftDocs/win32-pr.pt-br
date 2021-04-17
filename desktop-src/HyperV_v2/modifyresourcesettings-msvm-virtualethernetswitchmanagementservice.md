---
description: Modifica as configurações de recurso para um comutador virtual.
ms.assetid: 1ae2456f-921c-4ea6-b3fb-7065110063fb
title: Método ModifyResourceSettings da classe Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.ModifyResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f40044b20389914281ad4f651019f3e8dc6b6148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759410"
---
# <a name="modifyresourcesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="72c0a-103">Método ModifyResourceSettings da \_ classe VirtualEthernetSwitchManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="72c0a-103">ModifyResourceSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="72c0a-104">Modifica as configurações de recurso para um comutador virtual.</span><span class="sxs-lookup"><span data-stu-id="72c0a-104">Modifies resource settings for a virtual switch.</span></span>

## <a name="syntax"></a><span data-ttu-id="72c0a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="72c0a-105">Syntax</span></span>


```mof
uint32 ModifyResourceSettings(
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="72c0a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="72c0a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72c0a-107">*ResourceSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="72c0a-107">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72c0a-108">Uma matriz de cadeias de caracteres que contém uma instância incorporada de uma classe derivada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), que contém os aspectos modificados dos recursos virtuais existentes.</span><span class="sxs-lookup"><span data-stu-id="72c0a-108">An array of strings that contain an embedded instance of a class derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), that contain the modified aspects of existing virtual resources.</span></span> <span data-ttu-id="72c0a-109">A propriedade **InstanceId** de cada instância identifica a configuração de recurso virtual a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="72c0a-109">The **InstanceID** property of each instance identifies the virtual resource setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="72c0a-110">*ResultingResourceSettings* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="72c0a-110">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="72c0a-111">Uma matriz de referências a instâncias de objetos derivados de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) que representa aspectos virtuais dos recursos virtuais modificados.</span><span class="sxs-lookup"><span data-stu-id="72c0a-111">An array of references to instances of objects derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) representing virtual aspects of the modified virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="72c0a-112">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="72c0a-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="72c0a-113">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="72c0a-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72c0a-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="72c0a-114">Return value</span></span>

<span data-ttu-id="72c0a-115">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="72c0a-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="72c0a-116">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="72c0a-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="72c0a-117">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="72c0a-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="72c0a-118">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="72c0a-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="72c0a-119">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="72c0a-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="72c0a-120">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="72c0a-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="72c0a-121">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="72c0a-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="72c0a-122">**Parâmetros incompatíveis** (6)</span><span class="sxs-lookup"><span data-stu-id="72c0a-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="72c0a-123">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="72c0a-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="72c0a-124">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="72c0a-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="72c0a-125">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="72c0a-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="72c0a-126">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="72c0a-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="72c0a-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72c0a-127">Requirements</span></span>



| <span data-ttu-id="72c0a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="72c0a-128">Requirement</span></span> | <span data-ttu-id="72c0a-129">Valor</span><span class="sxs-lookup"><span data-stu-id="72c0a-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72c0a-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72c0a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="72c0a-131">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="72c0a-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="72c0a-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72c0a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="72c0a-133">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="72c0a-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="72c0a-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="72c0a-134">Namespace</span></span><br/>                | <span data-ttu-id="72c0a-135">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="72c0a-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="72c0a-136">MOF</span><span class="sxs-lookup"><span data-stu-id="72c0a-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72c0a-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="72c0a-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="72c0a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="72c0a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72c0a-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="72c0a-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="72c0a-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="72c0a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72c0a-141">**AddResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="72c0a-141">**AddResourceSettings**</span></span>](addresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="72c0a-142">**RemoveResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="72c0a-142">**RemoveResourceSettings**</span></span>](removeresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="72c0a-143">**Msvm \_ VirtualEthernetSwitchManagementService**</span><span class="sxs-lookup"><span data-stu-id="72c0a-143">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 


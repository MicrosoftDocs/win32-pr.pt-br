---
description: Remove as configurações de recurso virtual de uma configuração de comutador virtual.
ms.assetid: 9992ebcd-8891-42ef-be7e-154f336e37f8
title: Método RemoveResourceSettings da classe Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.RemoveResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9e82117b14ab9975b069e5b340ba9ec504ae65ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010567"
---
# <a name="removeresourcesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="fef39-103">Método RemoveResourceSettings da \_ classe VirtualEthernetSwitchManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="fef39-103">RemoveResourceSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="fef39-104">Remove as configurações de recurso virtual de uma configuração de comutador virtual.</span><span class="sxs-lookup"><span data-stu-id="fef39-104">Removes virtual resource settings from a virtual switch configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="fef39-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fef39-105">Syntax</span></span>


```mof
uint32 RemoveResourceSettings(
  [in]  CIM_ResourceAllocationSettingData REF ResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="fef39-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fef39-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fef39-107">*ResourceSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fef39-107">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fef39-108">Uma matriz de referências a instâncias da classe [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) , em que cada instância representa as configurações de um recurso virtual dentro de uma configuração de comutador virtual que devem ser removidas.</span><span class="sxs-lookup"><span data-stu-id="fef39-108">An array of references to instances of the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class, where each instance represents the settings of a virtual resource within a virtual switch configuration that are to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="fef39-109">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="fef39-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fef39-110">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fef39-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fef39-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fef39-111">Return value</span></span>

<span data-ttu-id="fef39-112">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="fef39-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="fef39-113">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="fef39-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fef39-114">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="fef39-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fef39-115">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="fef39-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fef39-116">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="fef39-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fef39-117">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="fef39-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fef39-118">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="fef39-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="fef39-119">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="fef39-119">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="fef39-120">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="fef39-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="fef39-121">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="fef39-121">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="fef39-122">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="fef39-122">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="fef39-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fef39-123">Requirements</span></span>



| <span data-ttu-id="fef39-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fef39-124">Requirement</span></span> | <span data-ttu-id="fef39-125">Valor</span><span class="sxs-lookup"><span data-stu-id="fef39-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fef39-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fef39-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fef39-127">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="fef39-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fef39-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fef39-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fef39-129">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="fef39-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fef39-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="fef39-130">Namespace</span></span><br/>                | <span data-ttu-id="fef39-131">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="fef39-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fef39-132">MOF</span><span class="sxs-lookup"><span data-stu-id="fef39-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fef39-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fef39-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fef39-134">DLL</span><span class="sxs-lookup"><span data-stu-id="fef39-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fef39-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fef39-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fef39-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="fef39-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fef39-137">**AddResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="fef39-137">**AddResourceSettings**</span></span>](addresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="fef39-138">**ModifyResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="fef39-138">**ModifyResourceSettings**</span></span>](modifyresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="fef39-139">**Msvm \_ VirtualEthernetSwitchManagementService**</span><span class="sxs-lookup"><span data-stu-id="fef39-139">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 


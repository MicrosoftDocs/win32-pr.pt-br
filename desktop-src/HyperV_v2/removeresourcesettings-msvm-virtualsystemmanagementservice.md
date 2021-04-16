---
description: Remove as configurações de recursos virtuais de uma configuração de máquina virtual.
ms.assetid: 74d9a70a-5258-4e4b-8131-b25513d11a4b
title: Método RemoveResourceSettings da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 20a7c9fb10e4f7a6356e47f8c743266095de2042
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768502"
---
# <a name="removeresourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="038dd-103">Método RemoveResourceSettings da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="038dd-103">RemoveResourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="038dd-104">Remove as configurações de recursos virtuais de uma configuração de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="038dd-104">Removes virtual resource settings from a virtual machine configuration.</span></span> <span data-ttu-id="038dd-105">Quando aplicado a partes de uma configuração de máquina virtual atual, a máquina virtual ativa pode ser removida.</span><span class="sxs-lookup"><span data-stu-id="038dd-105">When applied to parts of a current virtual machine configuration, the active virtual machine may be removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="038dd-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="038dd-106">Syntax</span></span>


```mof
uint32 RemoveResourceSettings(
  [in]  CIM_ResourceAllocationSettingData REF ResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="038dd-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="038dd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="038dd-108">*ResourceSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="038dd-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="038dd-109">Uma matriz de referências a instâncias da classe [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) , em que cada instância representa as configurações de um recurso virtual em uma configuração de máquina virtual que devem ser removidas.</span><span class="sxs-lookup"><span data-stu-id="038dd-109">An array of references to instances of the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class, where each instance represents the settings of a virtual resource within a virtual machine configuration that are to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="038dd-110">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="038dd-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="038dd-111">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="038dd-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="038dd-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="038dd-112">Return value</span></span>

<span data-ttu-id="038dd-113">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="038dd-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="038dd-114">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="038dd-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="038dd-115">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="038dd-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="038dd-116">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="038dd-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="038dd-117">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="038dd-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="038dd-118">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="038dd-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="038dd-119">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="038dd-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="038dd-120">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="038dd-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="038dd-121">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="038dd-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="038dd-122">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="038dd-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="038dd-123">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="038dd-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="038dd-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="038dd-124">Requirements</span></span>



| <span data-ttu-id="038dd-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="038dd-125">Requirement</span></span> | <span data-ttu-id="038dd-126">Valor</span><span class="sxs-lookup"><span data-stu-id="038dd-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="038dd-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="038dd-127">Minimum supported client</span></span><br/> | <span data-ttu-id="038dd-128">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="038dd-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="038dd-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="038dd-129">Minimum supported server</span></span><br/> | <span data-ttu-id="038dd-130">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="038dd-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="038dd-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="038dd-131">Namespace</span></span><br/>                | <span data-ttu-id="038dd-132">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="038dd-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="038dd-133">MOF</span><span class="sxs-lookup"><span data-stu-id="038dd-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="038dd-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="038dd-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="038dd-135">DLL</span><span class="sxs-lookup"><span data-stu-id="038dd-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="038dd-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="038dd-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="038dd-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="038dd-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="038dd-138">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="038dd-138">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 


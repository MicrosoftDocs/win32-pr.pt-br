---
description: Define um sistema virtual planejado.
ms.assetid: f129554b-e43e-4c3a-8418-d5d810f4c4b5
title: Método DefinePlannedSystem da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DefinePlannedSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d5e9fa8a49e86850d044216a3d95e3d4dd756fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501373"
---
# <a name="defineplannedsystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="dd1b9-103">Método DefinePlannedSystem da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="dd1b9-103">DefinePlannedSystem method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="dd1b9-104">Define um sistema virtual planejado.</span><span class="sxs-lookup"><span data-stu-id="dd1b9-104">Defines a planned virtual system.</span></span>

<span data-ttu-id="dd1b9-105">A entrada que não está completamente especificada pode ser preenchida com valores padrão.</span><span class="sxs-lookup"><span data-stu-id="dd1b9-105">Input that is not completely specified may be filled out with default values.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd1b9-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dd1b9-106">Syntax</span></span>


```mof
uint32 DefinePlannedSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="dd1b9-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dd1b9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd1b9-108">*SystemSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dd1b9-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd1b9-109">As configurações do sistema para o sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="dd1b9-109">The system settings for the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="dd1b9-110">*ResourceSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dd1b9-110">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd1b9-111">As configurações de recurso para o sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="dd1b9-111">The resource settings for the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="dd1b9-112">*ReferenceConfiguration* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dd1b9-112">*ReferenceConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd1b9-113">Um [**\_ VirtualSystemSettingData CIM**](cim-virtualsystemsettingdata.md) que contém a configuração de referência.</span><span class="sxs-lookup"><span data-stu-id="dd1b9-113">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) containing the reference configuration.</span></span>

</dd> <dt>

<span data-ttu-id="dd1b9-114">*ResultingSystem* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="dd1b9-114">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd1b9-115">Um sistema de sistemas [**CIM \_**](cim-computersystem.md) que contém o System resultante.</span><span class="sxs-lookup"><span data-stu-id="dd1b9-115">A [**CIM\_ComputerSystem**](cim-computersystem.md) containing the resulting system.</span></span>

</dd> <dt>

<span data-ttu-id="dd1b9-116">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="dd1b9-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd1b9-117">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dd1b9-117">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd1b9-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dd1b9-118">Return value</span></span>

<span data-ttu-id="dd1b9-119">Em caso de sucesso, retorna 0 ou 4096; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="dd1b9-119">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="dd1b9-120">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="dd1b9-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dd1b9-121">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="dd1b9-121">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="dd1b9-122">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="dd1b9-122">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dd1b9-123">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="dd1b9-123">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="dd1b9-124">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="dd1b9-124">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="dd1b9-125">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="dd1b9-125">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="dd1b9-126">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="dd1b9-126">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="dd1b9-127">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="dd1b9-127">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="dd1b9-128">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="dd1b9-128">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="dd1b9-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd1b9-129">Requirements</span></span>



| <span data-ttu-id="dd1b9-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd1b9-130">Requirement</span></span> | <span data-ttu-id="dd1b9-131">Valor</span><span class="sxs-lookup"><span data-stu-id="dd1b9-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd1b9-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd1b9-132">Minimum supported client</span></span><br/> | <span data-ttu-id="dd1b9-133">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="dd1b9-133">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="dd1b9-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd1b9-134">Minimum supported server</span></span><br/> | <span data-ttu-id="dd1b9-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="dd1b9-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="dd1b9-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="dd1b9-136">Namespace</span></span><br/>                | <span data-ttu-id="dd1b9-137">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="dd1b9-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="dd1b9-138">MOF</span><span class="sxs-lookup"><span data-stu-id="dd1b9-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd1b9-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dd1b9-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd1b9-140">DLL</span><span class="sxs-lookup"><span data-stu-id="dd1b9-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd1b9-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dd1b9-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dd1b9-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd1b9-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd1b9-143">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="dd1b9-143">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 


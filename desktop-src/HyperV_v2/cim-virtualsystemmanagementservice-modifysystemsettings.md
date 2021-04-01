---
description: Modifica as configurações do sistema virtual.
ms.assetid: 9c3d28f8-9806-411a-866f-d062c6d31818
title: Método ModifySystemSettings da classe CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.ModifySystemSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: da610d03e683b06ad743d1b6d4fe413dc5b31d34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921385"
---
# <a name="modifysystemsettings-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="18e13-103">Método ModifySystemSettings da \_ classe VIRTUALSYSTEMMANAGEMENTSERVICE CIM</span><span class="sxs-lookup"><span data-stu-id="18e13-103">ModifySystemSettings method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="18e13-104">Modifica as configurações do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="18e13-104">Modifies virtual system settings.</span></span>

<span data-ttu-id="18e13-105">Quando aplicado às configurações do sistema de uma configuração de sistema virtual "atual", como um efeito colateral, a instância do sistema virtual pode ser modificada.</span><span class="sxs-lookup"><span data-stu-id="18e13-105">When applied to the system settings of a "current" virtual system configuration, as a side effect the virtual system instance may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="18e13-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="18e13-106">Syntax</span></span>


```mof
uint32 ModifySystemSettings(
  [in]  string              SystemSettings,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="18e13-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18e13-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18e13-108">*SystemSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="18e13-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18e13-109">Cadeia de caracteres que contém uma instância da classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) que é usada para modificar as configurações do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="18e13-109">String containing an instance of class [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) that is used to modify the settings of the virtual system.</span></span> <span data-ttu-id="18e13-110">A instância deve ter uma **InstanceId** válida para identificar a configuração do sistema virtual a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="18e13-110">The instance must have a valid **InstanceID** in order to identify the virtual system setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="18e13-111">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="18e13-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18e13-112">Se a operação for de longa execução, opcionalmente, [**um \_ ConcreteJob CIM**](cim-concretejob.md) que representa o trabalho poderá ser retornado.</span><span class="sxs-lookup"><span data-stu-id="18e13-112">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18e13-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="18e13-113">Return value</span></span>

<span data-ttu-id="18e13-114">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="18e13-114">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="18e13-115">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="18e13-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="18e13-116">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="18e13-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="18e13-117">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="18e13-117">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="18e13-118">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="18e13-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="18e13-119">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="18e13-119">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="18e13-120">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="18e13-120">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="18e13-121">**Parâmetros incompatíveis** (6)</span><span class="sxs-lookup"><span data-stu-id="18e13-121">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="18e13-122">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="18e13-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="18e13-123">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="18e13-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="18e13-124">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="18e13-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="18e13-125">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="18e13-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="18e13-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18e13-126">Requirements</span></span>



| <span data-ttu-id="18e13-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="18e13-127">Requirement</span></span> | <span data-ttu-id="18e13-128">Valor</span><span class="sxs-lookup"><span data-stu-id="18e13-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18e13-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18e13-129">Minimum supported client</span></span><br/> | <span data-ttu-id="18e13-130">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="18e13-130">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="18e13-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18e13-131">Minimum supported server</span></span><br/> | <span data-ttu-id="18e13-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="18e13-132">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="18e13-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="18e13-133">Namespace</span></span><br/>                | <span data-ttu-id="18e13-134">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="18e13-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="18e13-135">MOF</span><span class="sxs-lookup"><span data-stu-id="18e13-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18e13-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="18e13-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="18e13-137">DLL</span><span class="sxs-lookup"><span data-stu-id="18e13-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18e13-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="18e13-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="18e13-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="18e13-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18e13-140">**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="18e13-140">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 





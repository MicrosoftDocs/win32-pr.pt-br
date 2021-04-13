---
description: Move, migra ou realoca um sistema virtual para um sistema de destino.
ms.assetid: 3a0be791-4514-4ce2-b4e8-3735bd6ea1d7
title: Método MigrateVirtualSystemToSystem da classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.MigrateVirtualSystemToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a346596b094b60456af8e2b63865bec1171d99ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296643"
---
# <a name="migratevirtualsystemtosystem-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="40c19-103">Método MigrateVirtualSystemToSystem da \_ classe VirtualSystemMigrationService Msvm</span><span class="sxs-lookup"><span data-stu-id="40c19-103">MigrateVirtualSystemToSystem method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="40c19-104">Move, migra ou realoca um sistema virtual para um sistema de destino.</span><span class="sxs-lookup"><span data-stu-id="40c19-104">Moves, migrates, or relocates a virtual system to a target system.</span></span>

## <a name="syntax"></a><span data-ttu-id="40c19-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="40c19-105">Syntax</span></span>


```mof
uint32 MigrateVirtualSystemToSystem(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  CIM_System         REF DestinationSystem,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] CIM_ComputerSystem REF NewComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="40c19-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="40c19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40c19-107">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="40c19-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40c19-108">Uma referência a uma instância da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) que representa o sistema de computador virtual a ser migrado.</span><span class="sxs-lookup"><span data-stu-id="40c19-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="40c19-109">*DestinationSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="40c19-109">*DestinationSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40c19-110">Uma referência a uma instância da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) que representa o sistema a ser migrado para o.</span><span class="sxs-lookup"><span data-stu-id="40c19-110">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the system to be migrated to.</span></span>

</dd> <dt>

<span data-ttu-id="40c19-111">*MigrationSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="40c19-111">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40c19-112">Uma instância inserida da classe [**Msvm \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) que representa as configurações da operação de migração.</span><span class="sxs-lookup"><span data-stu-id="40c19-112">An embedded instance of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class that represents settings for the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="40c19-113">*NewSystemSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="40c19-113">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40c19-114">Uma instância inserida da classe [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representa as novas propriedades aplicáveis ao sistema virtual depois que ele é migrado.</span><span class="sxs-lookup"><span data-stu-id="40c19-114">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="40c19-115">*NewResourceSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="40c19-115">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40c19-116">Uma matriz de cadeias de caracteres que contém uma instância incorporada da classe [**Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) que representa as novas propriedades aplicáveis aos recursos virtuais do sistema virtual depois que ele é migrado.</span><span class="sxs-lookup"><span data-stu-id="40c19-116">An array of strings that contain an embedded instance of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that represents the new properties applicable to virtual resources of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="40c19-117">*NewComputerSystem* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="40c19-117">*NewComputerSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="40c19-118">Uma referência a uma instância da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) que representa o novo sistema migrado.</span><span class="sxs-lookup"><span data-stu-id="40c19-118">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the new migrated system.</span></span>

</dd> <dt>

<span data-ttu-id="40c19-119">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="40c19-119">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="40c19-120">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="40c19-120">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40c19-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="40c19-121">Return value</span></span>

<span data-ttu-id="40c19-122">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="40c19-122">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="40c19-123">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="40c19-123">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="40c19-124">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="40c19-124">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="40c19-125">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="40c19-125">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="40c19-126">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="40c19-126">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="40c19-127">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="40c19-127">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="40c19-128">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="40c19-128">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="40c19-129">**Parâmetros incompatíveis** (6)</span><span class="sxs-lookup"><span data-stu-id="40c19-129">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="40c19-130">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="40c19-130">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="40c19-131">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="40c19-131">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="40c19-132">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="40c19-132">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="40c19-133">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="40c19-133">**Vendor Specific** (32768..65535 )</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="40c19-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40c19-134">Requirements</span></span>



| <span data-ttu-id="40c19-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="40c19-135">Requirement</span></span> | <span data-ttu-id="40c19-136">Valor</span><span class="sxs-lookup"><span data-stu-id="40c19-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40c19-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40c19-137">Minimum supported client</span></span><br/> | <span data-ttu-id="40c19-138">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="40c19-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="40c19-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40c19-139">Minimum supported server</span></span><br/> | <span data-ttu-id="40c19-140">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="40c19-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="40c19-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="40c19-141">Namespace</span></span><br/>                | <span data-ttu-id="40c19-142">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="40c19-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="40c19-143">MOF</span><span class="sxs-lookup"><span data-stu-id="40c19-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40c19-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="40c19-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="40c19-145">DLL</span><span class="sxs-lookup"><span data-stu-id="40c19-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40c19-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="40c19-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="40c19-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="40c19-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40c19-148">**Msvm \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="40c19-148">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 


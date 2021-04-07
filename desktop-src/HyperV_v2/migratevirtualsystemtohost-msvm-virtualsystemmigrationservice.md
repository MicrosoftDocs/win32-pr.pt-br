---
description: Migra um sistema virtual ou o armazenamento de um sistema virtual para um host de destino especificado por um nome de host.
ms.assetid: 796b043c-5ac9-4c69-9838-0f415be5a63e
title: Método MigrateVirtualSystemToHost da classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.MigrateVirtualSystemToHost
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f46d32f9e1af68cd4256c4eb5adff5c32b8766e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827880"
---
# <a name="migratevirtualsystemtohost-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="09baa-103">Método MigrateVirtualSystemToHost da \_ classe VirtualSystemMigrationService Msvm</span><span class="sxs-lookup"><span data-stu-id="09baa-103">MigrateVirtualSystemToHost method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="09baa-104">Migra um sistema virtual ou o armazenamento de um sistema virtual para um host de destino especificado por um nome de host.</span><span class="sxs-lookup"><span data-stu-id="09baa-104">Migrates a virtual system or the storage of a virtual system to a destination host specified by a hostname.</span></span>

## <a name="syntax"></a><span data-ttu-id="09baa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09baa-105">Syntax</span></span>


```mof
uint32 MigrateVirtualSystemToHost(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 DestinationHost,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="09baa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09baa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09baa-107">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09baa-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09baa-108">Uma referência a uma instância da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) que representa o sistema de computador virtual a ser migrado.</span><span class="sxs-lookup"><span data-stu-id="09baa-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="09baa-109">*DestinationHost* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09baa-109">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09baa-110">O nome do sistema host para a migração.</span><span class="sxs-lookup"><span data-stu-id="09baa-110">The name of the host system for the migration.</span></span> <span data-ttu-id="09baa-111">O formato desse nome é especificado pela propriedade **DestinationHostFormatsSupported** da classe [**Msvm \_ VirtualSystemMigrationCapabilities**](msvm-virtualsystemmigrationcapabilities.md) associada a essa classe.</span><span class="sxs-lookup"><span data-stu-id="09baa-111">The format of this name is specified by the **DestinationHostFormatsSupported** property of the [**Msvm\_VirtualSystemMigrationCapabilities**](msvm-virtualsystemmigrationcapabilities.md) class associated with this class.</span></span>

</dd> <dt>

<span data-ttu-id="09baa-112">*MigrationSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09baa-112">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09baa-113">Uma instância inserida da classe [**Msvm \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) que representa as configurações da operação de migração.</span><span class="sxs-lookup"><span data-stu-id="09baa-113">An embedded instance of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class that represents settings for the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="09baa-114">*NewSystemSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09baa-114">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09baa-115">Uma instância inserida da classe [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representa as novas propriedades aplicáveis ao sistema virtual depois que ele é migrado.</span><span class="sxs-lookup"><span data-stu-id="09baa-115">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="09baa-116">*NewResourceSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09baa-116">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09baa-117">Uma matriz de cadeias de caracteres que contém uma instância incorporada da classe [**Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) que representa as novas propriedades aplicáveis aos recursos virtuais do sistema virtual depois que ele é migrado.</span><span class="sxs-lookup"><span data-stu-id="09baa-117">An array of strings that contain an embedded instance of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that represents the new properties applicable to virtual resources of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="09baa-118">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="09baa-118">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09baa-119">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="09baa-119">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09baa-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="09baa-120">Return value</span></span>

<span data-ttu-id="09baa-121">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="09baa-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="09baa-122">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="09baa-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="09baa-123">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="09baa-123">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="09baa-124">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="09baa-124">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="09baa-125">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="09baa-125">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="09baa-126">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="09baa-126">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="09baa-127">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="09baa-127">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="09baa-128">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="09baa-128">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="09baa-129">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="09baa-129">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="09baa-130">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="09baa-130">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="09baa-131">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="09baa-131">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="09baa-132">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="09baa-132">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="09baa-133">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="09baa-133">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="09baa-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09baa-134">Requirements</span></span>



| <span data-ttu-id="09baa-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="09baa-135">Requirement</span></span> | <span data-ttu-id="09baa-136">Valor</span><span class="sxs-lookup"><span data-stu-id="09baa-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09baa-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09baa-137">Minimum supported client</span></span><br/> | <span data-ttu-id="09baa-138">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="09baa-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="09baa-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09baa-139">Minimum supported server</span></span><br/> | <span data-ttu-id="09baa-140">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="09baa-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="09baa-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="09baa-141">Namespace</span></span><br/>                | <span data-ttu-id="09baa-142">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="09baa-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="09baa-143">MOF</span><span class="sxs-lookup"><span data-stu-id="09baa-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="09baa-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="09baa-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="09baa-145">DLL</span><span class="sxs-lookup"><span data-stu-id="09baa-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09baa-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="09baa-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="09baa-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="09baa-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09baa-148">**Msvm \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="09baa-148">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 


---
description: Determina se o sistema virtual especificado pode ser migrado para um sistema de destino.
ms.assetid: 2E340737-DEE9-4853-ACD8-BEE2A8C69D6D
title: Método CheckVirtualSystemIsMigratableToSystem da classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3e8f294f7e30740e3afab8987c734dbbdbd12acf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785446"
---
# <a name="checkvirtualsystemismigratabletosystem-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="083ec-103">Método CheckVirtualSystemIsMigratableToSystem da \_ classe VirtualSystemMigrationService Msvm</span><span class="sxs-lookup"><span data-stu-id="083ec-103">CheckVirtualSystemIsMigratableToSystem method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="083ec-104">Determina se o sistema virtual especificado pode ser migrado para um sistema de destino.</span><span class="sxs-lookup"><span data-stu-id="083ec-104">Determines whether the specified virtual system can be migrated to a destination system.</span></span>

## <a name="syntax"></a><span data-ttu-id="083ec-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="083ec-105">Syntax</span></span>


```mof
uint32 CheckVirtualSystemIsMigratableToSystem(
  [in]  Msvm_ComputerSystem REF ComputerSystem,
  [in]  Msvm_ComputerSystem REF DestinationSystem,
  [in]  string                  MigrationSettingData,
  [in]  string                  NewSystemSettingData,
  [in]  string                  NewResourceSettingData[],
  [out] boolean                 IsMigratable
);
```



## <a name="parameters"></a><span data-ttu-id="083ec-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="083ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="083ec-107">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="083ec-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="083ec-108">Uma referência a uma instância da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) que representa a máquina virtual para testar a capacidade de migração do.</span><span class="sxs-lookup"><span data-stu-id="083ec-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine to test the migration ability of.</span></span>

</dd> <dt>

<span data-ttu-id="083ec-109">*DestinationSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="083ec-109">*DestinationSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="083ec-110">Uma referência a uma instância da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) que representa a máquina virtual para testar a capacidade de migração para o.</span><span class="sxs-lookup"><span data-stu-id="083ec-110">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine to test the migration ability to.</span></span>

</dd> <dt>

<span data-ttu-id="083ec-111">*MigrationSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="083ec-111">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="083ec-112">Uma instância inserida da classe [**Msvm \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) que representa as configurações da operação de migração.</span><span class="sxs-lookup"><span data-stu-id="083ec-112">An embedded instance of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class that represents settings for the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="083ec-113">*NewSystemSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="083ec-113">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="083ec-114">Uma instância inserida da classe [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representa as novas propriedades aplicáveis ao sistema virtual depois que ele é migrado.</span><span class="sxs-lookup"><span data-stu-id="083ec-114">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="083ec-115">*NewResourceSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="083ec-115">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="083ec-116">Uma matriz de cadeias de caracteres que contém uma instância incorporada da classe [**Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) que representa as novas propriedades aplicáveis aos recursos virtuais do sistema virtual depois que ele é migrado.</span><span class="sxs-lookup"><span data-stu-id="083ec-116">An array of strings that contain an embedded instance of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that represents the new properties applicable to virtual resources of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="083ec-117">*IsMigratable* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="083ec-117">*IsMigratable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="083ec-118">Recebe o resultado da verificação de migração que indica se o sistema virtual pode ser migrado com êxito.</span><span class="sxs-lookup"><span data-stu-id="083ec-118">Receives the migration check result indicating whether the virtual system can be successfully migrated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="083ec-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="083ec-119">Return value</span></span>

<span data-ttu-id="083ec-120">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="083ec-120">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="083ec-121">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="083ec-121">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="083ec-122">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="083ec-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="083ec-123">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="083ec-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="083ec-124">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="083ec-124">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="083ec-125">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="083ec-125">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="083ec-126">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="083ec-126">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="083ec-127">**Parâmetros incompatíveis** (6)</span><span class="sxs-lookup"><span data-stu-id="083ec-127">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="083ec-128">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="083ec-128">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="083ec-129">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="083ec-129">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="083ec-130">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="083ec-130">**Vendor Specific** (32768..65535 )</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="083ec-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="083ec-131">Requirements</span></span>



| <span data-ttu-id="083ec-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="083ec-132">Requirement</span></span> | <span data-ttu-id="083ec-133">Valor</span><span class="sxs-lookup"><span data-stu-id="083ec-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="083ec-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="083ec-134">Minimum supported client</span></span><br/> | <span data-ttu-id="083ec-135">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="083ec-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="083ec-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="083ec-136">Minimum supported server</span></span><br/> | <span data-ttu-id="083ec-137">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="083ec-137">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="083ec-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="083ec-138">Namespace</span></span><br/>                | <span data-ttu-id="083ec-139">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="083ec-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="083ec-140">MOF</span><span class="sxs-lookup"><span data-stu-id="083ec-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="083ec-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="083ec-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="083ec-142">DLL</span><span class="sxs-lookup"><span data-stu-id="083ec-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="083ec-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="083ec-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="083ec-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="083ec-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="083ec-145">**Msvm \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="083ec-145">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 





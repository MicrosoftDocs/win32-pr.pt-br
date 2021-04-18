---
description: Determina se o sistema virtual especificado pode ser migrado para um host de destino especificado por um nome de rede ou endereço IP.
ms.assetid: eacc8448-4683-48df-81b9-8599292944db
title: Método CheckVirtualSystemIsMigratableToHost da classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToHost
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b81f6562f892acbaa5bf7ff7f4f3c772574bd96d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785463"
---
# <a name="checkvirtualsystemismigratabletohost-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="47beb-103">Método CheckVirtualSystemIsMigratableToHost da \_ classe VirtualSystemMigrationService Msvm</span><span class="sxs-lookup"><span data-stu-id="47beb-103">CheckVirtualSystemIsMigratableToHost method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="47beb-104">Determina se o sistema virtual especificado pode ser migrado para um host de destino especificado por um nome de rede ou endereço IP.</span><span class="sxs-lookup"><span data-stu-id="47beb-104">Determines whether the specified virtual system can be migrated to a target host specified by a network name or IP address.</span></span>

## <a name="syntax"></a><span data-ttu-id="47beb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="47beb-105">Syntax</span></span>


```mof
uint32 CheckVirtualSystemIsMigratableToHost(
  [in]  Msvm_ComputerSystem REF ComputerSystem,
  [in]  string                  DestinationHost,
  [in]  string                  MigrationSettingData,
  [in]  string                  NewSystemSettingData,
  [in]  string                  NewResourceSettingData[],
  [out] boolean                 IsMigratable
);
```



## <a name="parameters"></a><span data-ttu-id="47beb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47beb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47beb-107">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="47beb-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47beb-108">Uma referência a uma instância da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) que representa a máquina virtual para testar a capacidade de migração do.</span><span class="sxs-lookup"><span data-stu-id="47beb-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine to test the migration ability of.</span></span>

</dd> <dt>

<span data-ttu-id="47beb-109">*DestinationHost* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="47beb-109">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47beb-110">O nome do sistema host para a migração.</span><span class="sxs-lookup"><span data-stu-id="47beb-110">The name of the host system for the migration.</span></span> <span data-ttu-id="47beb-111">O formato desse nome é especificado pela propriedade **DestinationHostFormatsSupported** da classe [**Msvm \_ VirtualSystemMigrationCapabilities**](msvm-virtualsystemmigrationcapabilities.md) associada a essa classe.</span><span class="sxs-lookup"><span data-stu-id="47beb-111">The format of this name is specified by the **DestinationHostFormatsSupported** property of the [**Msvm\_VirtualSystemMigrationCapabilities**](msvm-virtualsystemmigrationcapabilities.md) class associated with this class.</span></span>

</dd> <dt>

<span data-ttu-id="47beb-112">*MigrationSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="47beb-112">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47beb-113">Uma instância inserida da classe [**Msvm \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) que representa as configurações da operação de migração.</span><span class="sxs-lookup"><span data-stu-id="47beb-113">An embedded instance of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class that represents settings for the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="47beb-114">*NewSystemSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="47beb-114">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47beb-115">Uma instância inserida da classe [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representa as novas propriedades aplicáveis ao sistema virtual depois que ele é migrado.</span><span class="sxs-lookup"><span data-stu-id="47beb-115">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="47beb-116">*NewResourceSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="47beb-116">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47beb-117">Uma matriz de cadeias de caracteres que contém uma instância incorporada da classe [**Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) que representa as novas propriedades aplicáveis aos recursos virtuais do sistema virtual depois que ele é migrado.</span><span class="sxs-lookup"><span data-stu-id="47beb-117">An array of strings that contain an embedded instance of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that represents the new properties applicable to virtual resources of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="47beb-118">*IsMigratable* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="47beb-118">*IsMigratable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47beb-119">Recebe o resultado da verificação de migração que indica se o sistema virtual pode ser migrado com êxito.</span><span class="sxs-lookup"><span data-stu-id="47beb-119">Receives the migration check result indicating whether the virtual system can be successfully migrated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47beb-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="47beb-120">Return value</span></span>

<span data-ttu-id="47beb-121">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="47beb-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="47beb-122">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="47beb-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="47beb-123">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="47beb-123">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="47beb-124">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="47beb-124">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="47beb-125">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="47beb-125">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="47beb-126">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="47beb-126">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="47beb-127">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="47beb-127">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="47beb-128">**Parâmetros incompatíveis** (6)</span><span class="sxs-lookup"><span data-stu-id="47beb-128">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="47beb-129">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="47beb-129">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="47beb-130">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="47beb-130">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="47beb-131">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="47beb-131">**Vendor Specific** (32768..65535 )</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="47beb-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47beb-132">Requirements</span></span>



| <span data-ttu-id="47beb-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="47beb-133">Requirement</span></span> | <span data-ttu-id="47beb-134">Valor</span><span class="sxs-lookup"><span data-stu-id="47beb-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47beb-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47beb-135">Minimum supported client</span></span><br/> | <span data-ttu-id="47beb-136">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="47beb-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="47beb-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47beb-137">Minimum supported server</span></span><br/> | <span data-ttu-id="47beb-138">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="47beb-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="47beb-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="47beb-139">Namespace</span></span><br/>                | <span data-ttu-id="47beb-140">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="47beb-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="47beb-141">MOF</span><span class="sxs-lookup"><span data-stu-id="47beb-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="47beb-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="47beb-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="47beb-143">DLL</span><span class="sxs-lookup"><span data-stu-id="47beb-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47beb-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="47beb-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="47beb-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="47beb-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47beb-146">**Msvm \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="47beb-146">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 





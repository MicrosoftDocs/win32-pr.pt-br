---
description: Determina se o sistema virtual especificado pode ser migrado.
ms.assetid: 1bf1b385-162e-41c9-a408-f7ee755a9646
title: Método CheckVirtualSystemIsMigratable da classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckVirtualSystemIsMigratable
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1aed843f3f0f4c6c30eb6125cdd5859cdba902d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826869"
---
# <a name="checkvirtualsystemismigratable-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="a9ec1-103">Método CheckVirtualSystemIsMigratable da \_ classe VirtualSystemMigrationService Msvm</span><span class="sxs-lookup"><span data-stu-id="a9ec1-103">CheckVirtualSystemIsMigratable method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="a9ec1-104">Determina se o sistema virtual especificado pode ser migrado.</span><span class="sxs-lookup"><span data-stu-id="a9ec1-104">Determines whether the specified virtual system can be migrated.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9ec1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a9ec1-105">Syntax</span></span>


```mof
uint32 CheckVirtualSystemIsMigratable(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 DestinationHost,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a9ec1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a9ec1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9ec1-107">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a9ec1-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9ec1-108">Uma referência a uma instância da classe [**de \_ ComputerSystem do CIM**](cim-computersystem.md) que representa a máquina virtual para testar a capacidade de migração do.</span><span class="sxs-lookup"><span data-stu-id="a9ec1-108">A reference to an instance of the [**CIM\_ComputerSystem**](cim-computersystem.md) class that represents the virtual machine to test the migration ability of.</span></span>

</dd> <dt>

<span data-ttu-id="a9ec1-109">*DestinationHost* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a9ec1-109">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9ec1-110">O nome do sistema host para a migração.</span><span class="sxs-lookup"><span data-stu-id="a9ec1-110">The name of the host system for the migration.</span></span> <span data-ttu-id="a9ec1-111">O formato desse nome é especificado pela propriedade **DestinationHostFormatsSupported** da classe [**Msvm \_ VirtualSystemMigrationCapabilities**](msvm-virtualsystemmigrationcapabilities.md) associada a essa classe.</span><span class="sxs-lookup"><span data-stu-id="a9ec1-111">The format of this name is specified by the **DestinationHostFormatsSupported** property of the [**Msvm\_VirtualSystemMigrationCapabilities**](msvm-virtualsystemmigrationcapabilities.md) class associated with this class.</span></span>

</dd> <dt>

<span data-ttu-id="a9ec1-112">*MigrationSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a9ec1-112">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9ec1-113">Uma instância inserida da classe [**Msvm \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) que representa as configurações da operação de migração.</span><span class="sxs-lookup"><span data-stu-id="a9ec1-113">An embedded instance of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class that represents settings for the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="a9ec1-114">*NewSystemSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a9ec1-114">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9ec1-115">Uma instância inserida da classe [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representa as novas propriedades aplicáveis ao sistema virtual depois que ele é migrado.</span><span class="sxs-lookup"><span data-stu-id="a9ec1-115">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="a9ec1-116">*NewResourceSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a9ec1-116">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9ec1-117">Uma matriz de cadeias de caracteres que contém uma instância incorporada da classe [**Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) que representa as novas propriedades aplicáveis aos recursos virtuais do sistema virtual depois que ele é migrado.</span><span class="sxs-lookup"><span data-stu-id="a9ec1-117">An array of strings that contain an embedded instance of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that represents the new properties applicable to virtual resources of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="a9ec1-118">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="a9ec1-118">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9ec1-119">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a9ec1-119">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9ec1-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a9ec1-120">Return value</span></span>

<span data-ttu-id="a9ec1-121">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a9ec1-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a9ec1-122">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="a9ec1-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a9ec1-123">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="a9ec1-123">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="a9ec1-124">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="a9ec1-124">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="a9ec1-125">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="a9ec1-125">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="a9ec1-126">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="a9ec1-126">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="a9ec1-127">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="a9ec1-127">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="a9ec1-128">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="a9ec1-128">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="a9ec1-129">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="a9ec1-129">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="a9ec1-130">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="a9ec1-130">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="a9ec1-131">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="a9ec1-131">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="a9ec1-132">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="a9ec1-132">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="a9ec1-133">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="a9ec1-133">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a9ec1-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9ec1-134">Requirements</span></span>



| <span data-ttu-id="a9ec1-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9ec1-135">Requirement</span></span> | <span data-ttu-id="a9ec1-136">Valor</span><span class="sxs-lookup"><span data-stu-id="a9ec1-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9ec1-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9ec1-137">Minimum supported client</span></span><br/> | <span data-ttu-id="a9ec1-138">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a9ec1-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a9ec1-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9ec1-139">Minimum supported server</span></span><br/> | <span data-ttu-id="a9ec1-140">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a9ec1-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a9ec1-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="a9ec1-141">Namespace</span></span><br/>                | <span data-ttu-id="a9ec1-142">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="a9ec1-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a9ec1-143">MOF</span><span class="sxs-lookup"><span data-stu-id="a9ec1-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9ec1-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a9ec1-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a9ec1-145">DLL</span><span class="sxs-lookup"><span data-stu-id="a9ec1-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9ec1-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a9ec1-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a9ec1-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9ec1-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9ec1-148">**Msvm \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="a9ec1-148">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 


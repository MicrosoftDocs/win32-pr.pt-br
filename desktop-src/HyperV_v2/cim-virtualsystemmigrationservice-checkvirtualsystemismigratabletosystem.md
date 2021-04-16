---
description: 'Saiba mais sobre: método CheckVirtualSystemIsMigratableToSystem da classe CIM_VirtualSystemMigrationService'
ms.assetid: d3f7c926-804f-4c7c-8964-a8e464155417
title: Método CheckVirtualSystemIsMigratableToSystem da classe CIM_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: be85c51cb507fea3cea14f1706ffa8f67af06c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757421"
---
# <a name="checkvirtualsystemismigratabletosystem-method-of-the-cim_virtualsystemmigrationservice-class"></a><span data-ttu-id="d10ea-103">Método CheckVirtualSystemIsMigratableToSystem da \_ classe VIRTUALSYSTEMMIGRATIONSERVICE CIM</span><span class="sxs-lookup"><span data-stu-id="d10ea-103">CheckVirtualSystemIsMigratableToSystem method of the CIM\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="d10ea-104">Método para executar uma verificação prévia para determinar se um sistema virtual provavelmente será migrado com êxito para um sistema de destino.</span><span class="sxs-lookup"><span data-stu-id="d10ea-104">Method to perform a pre-check to determine whether a virtual system is likely to be successfully migrated to a target system.</span></span> <span data-ttu-id="d10ea-105">Esse método não garante que uma migração subsequente sempre terá sucesso, devido à disponibilidade dinâmica de recursos.</span><span class="sxs-lookup"><span data-stu-id="d10ea-105">This method does not guarantee that a subsequent migration will always succeed, due to dynamic resource availability.</span></span> <span data-ttu-id="d10ea-106">Descrição do código de retorno:</span><span class="sxs-lookup"><span data-stu-id="d10ea-106">Return code description:</span></span>

## <a name="syntax"></a><span data-ttu-id="d10ea-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d10ea-107">Syntax</span></span>


```mof
uint32 CheckVirtualSystemIsMigratableToSystem(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  CIM_System         REF DestinationSystem,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] boolean                IsMigratable
);
```



## <a name="parameters"></a><span data-ttu-id="d10ea-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d10ea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d10ea-109">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d10ea-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d10ea-110">[**CIM \_**](cim-computersystem.md) Instância de ComputerSystem que faz referência ao sistema de computador virtual de origem a ser migrado.</span><span class="sxs-lookup"><span data-stu-id="d10ea-110">[**CIM\_ComputerSystem**](cim-computersystem.md) instance referencing the source virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="d10ea-111">*DestinationSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d10ea-111">*DestinationSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d10ea-112">[**CIM \_**](cim-system.md) Instância do sistema que faz referência ao sistema de destino para o qual migrar o sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="d10ea-112">[**CIM\_System**](cim-system.md) instance referencing the destination system onto which to migrate the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="d10ea-113">*MigrationSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d10ea-113">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d10ea-114">Cadeia de caracteres que contém uma instância inserida da classe [**CIM \_ VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) que representa as configurações de migração aplicáveis à operação de migração.</span><span class="sxs-lookup"><span data-stu-id="d10ea-114">String containing an embedded instance of the [**CIM\_VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) class representing migration settings applicable to the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="d10ea-115">*NewSystemSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d10ea-115">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d10ea-116">Cadeia de caracteres que contém uma instância inserida da classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) que representa as novas propriedades aplicáveis ao sistema virtual depois que ele é migrado.</span><span class="sxs-lookup"><span data-stu-id="d10ea-116">String containing an embedded instance of the [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) class representing new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="d10ea-117">*NewResourceSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d10ea-117">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d10ea-118">Matriz de cadeias de caracteres que contém uma instância incorporada da classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que representa as novas propriedades aplicáveis aos recursos virtuais no escopo do sistema virtual depois que ele é migrado.</span><span class="sxs-lookup"><span data-stu-id="d10ea-118">Array of strings each containing an embedded instance of the [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) class representing new properties applicable to virtual resources in the scope of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="d10ea-119">*IsMigratable* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d10ea-119">*IsMigratable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d10ea-120">O resultado da verificação de migração que indica se o sistema virtual pode ou não ser migrado com êxito.</span><span class="sxs-lookup"><span data-stu-id="d10ea-120">The migration check result indicating whether or not the virtual system can be successfully migrated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d10ea-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d10ea-121">Return value</span></span>

<span data-ttu-id="d10ea-122">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="d10ea-122">Returns a 0 on success; otherwise, returns an error.</span></span>



| <span data-ttu-id="d10ea-123">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d10ea-123">Return code/value</span></span>                                                                                                                                                | <span data-ttu-id="d10ea-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="d10ea-124">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d10ea-125"><dt>**Concluído sem erro**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d10ea-125"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="d10ea-126">Verificação realizada; resultado relatado por meio do valor do \[ parâmetro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="d10ea-126">Check performed; result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="d10ea-127"><dt>**Sem suporte**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d10ea-127"><dt>**Not Supported**</dt> <dt>1</dt></span></span> </dl>              | <span data-ttu-id="d10ea-128">Método sem suporte pela implementação.</span><span class="sxs-lookup"><span data-stu-id="d10ea-128">Method not supported by implementation.</span></span> <span data-ttu-id="d10ea-129">Nenhum resultado relatado pelo valor do \[ parâmetro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="d10ea-129">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="d10ea-130"><dt>**Com falha**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d10ea-130"><dt>**Failed**</dt> <dt>2</dt></span></span> </dl>                     | <span data-ttu-id="d10ea-131">A verificação falhou por razões não especificadas.</span><span class="sxs-lookup"><span data-stu-id="d10ea-131">Check failed for unspecified reasons.</span></span> <span data-ttu-id="d10ea-132">Nenhum resultado relatado pelo valor do \[ parâmetro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="d10ea-132">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="d10ea-133"><dt>**Tempo limite**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d10ea-133"><dt>**Timeout**</dt> <dt>3</dt></span></span> </dl>                    | <span data-ttu-id="d10ea-134">A verificação atingiu o tempo limite. Nenhum resultado relatado pelo valor do \[ parâmetro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="d10ea-134">Check timed out. No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="d10ea-135"><dt>**Parâmetro inválido**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="d10ea-135"><dt>**Invalid Parameter**</dt> <dt>4</dt></span></span> </dl>          | <span data-ttu-id="d10ea-136">Um ou mais parâmetros são formalmente inválidos.</span><span class="sxs-lookup"><span data-stu-id="d10ea-136">One or more parameters are formally invalid.</span></span> <span data-ttu-id="d10ea-137">Por exemplo, o valor do parâmetro *DestinationSystem* não inclui um caminho de objeto válido.</span><span class="sxs-lookup"><span data-stu-id="d10ea-137">For example, the value of the *DestinationSystem* parameter does not comprise a valid object path.</span></span> <span data-ttu-id="d10ea-138">Nenhum resultado relatado pelo valor do \[ parâmetro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="d10ea-138">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                        |
| <dl> <span data-ttu-id="d10ea-139"><dt>**Estado inválido**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="d10ea-139"><dt>**Invalid State**</dt> <dt>5</dt></span></span> </dl>              | <span data-ttu-id="d10ea-140">O sistema virtual de origem, o sistema host de origem ou o sistema host de destino estão em um estado que permite a inicialização da migração de sistema virtual solicitada; Essa pode ser uma condição temporária.</span><span class="sxs-lookup"><span data-stu-id="d10ea-140">The source virtual system, the source host system or the target host system are in a state that does allow initiation of the requested virtual system migration; this may be a temporary condition.</span></span> <span data-ttu-id="d10ea-141">Nenhum resultado relatado pelo valor do \[ parâmetro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="d10ea-141">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="d10ea-142"><dt>**Parâmetros incompatíveis**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="d10ea-142"><dt>**Incompatible Parameters**</dt> <dt>6</dt></span></span> </dl>    | <span data-ttu-id="d10ea-143">Um ou mais parâmetros de entrada são incompatíveis como um conjunto ou em relação ao host de destino.</span><span class="sxs-lookup"><span data-stu-id="d10ea-143">One or more input parameters are incompatible as a set, or with respect to the target host.</span></span> <span data-ttu-id="d10ea-144">Por exemplo, o valor do parâmetro *NewSettingData* contém propriedades que não são suportadas pelo sistema host de destino identificado pelo valor do parâmetro *DestinationSystem* .</span><span class="sxs-lookup"><span data-stu-id="d10ea-144">For example the value of the *NewSettingData* parameter contains properties that are not supported by the target host system identified by the value of the *DestinationSystem* parameter.</span></span> <span data-ttu-id="d10ea-145">Nenhum resultado relatado pelo valor do \[ parâmetro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="d10ea-145">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="d10ea-146"><dt>**DMTF reservado**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="d10ea-146"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>             |                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="d10ea-147"><dt>**Método reservado**</dt> <dt>4097.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="d10ea-147"><dt>**Method Reserved**</dt> <dt>4097..32767</dt></span></span> </dl>  |                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="d10ea-148">32768 <dt>**específicos do fornecedor**</dt> <dt>. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="d10ea-148"><dt>**Vendor Specific**</dt> <dt>32768..65535</dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="d10ea-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d10ea-149">Requirements</span></span>



| <span data-ttu-id="d10ea-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="d10ea-150">Requirement</span></span> | <span data-ttu-id="d10ea-151">Valor</span><span class="sxs-lookup"><span data-stu-id="d10ea-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d10ea-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d10ea-152">Minimum supported client</span></span><br/> | <span data-ttu-id="d10ea-153">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d10ea-153">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="d10ea-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d10ea-154">Minimum supported server</span></span><br/> | <span data-ttu-id="d10ea-155">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d10ea-155">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="d10ea-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="d10ea-156">Namespace</span></span><br/>                | <span data-ttu-id="d10ea-157">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="d10ea-157">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d10ea-158">MOF</span><span class="sxs-lookup"><span data-stu-id="d10ea-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d10ea-159"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d10ea-159"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d10ea-160">DLL</span><span class="sxs-lookup"><span data-stu-id="d10ea-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d10ea-161"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d10ea-161"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d10ea-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="d10ea-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d10ea-163">**\_VIRTUALSYSTEMMIGRATIONSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="d10ea-163">**CIM\_VirtualSystemMigrationService**</span></span>](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 





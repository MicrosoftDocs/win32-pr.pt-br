---
description: Método para mover, migrar ou realocar um sistema virtual para um host de destino especificado por um nome de rede ou endereço IP.
ms.assetid: 09fdc0b2-641c-47f5-b270-e26e3acf7ea5
title: Método MigrateVirtualSystemToHost da classe CIM_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.MigrateVirtualSystemToHost
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d1a90e3adadbb5efc5f9cae3b7710e07c1e05000
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812951"
---
# <a name="migratevirtualsystemtohost-method-of-the-cim_virtualsystemmigrationservice-class"></a><span data-ttu-id="5160a-103">Método MigrateVirtualSystemToHost da \_ classe VIRTUALSYSTEMMIGRATIONSERVICE CIM</span><span class="sxs-lookup"><span data-stu-id="5160a-103">MigrateVirtualSystemToHost method of the CIM\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="5160a-104">Método para mover, migrar ou realocar um sistema virtual para um host de destino especificado por um nome de rede ou endereço IP.</span><span class="sxs-lookup"><span data-stu-id="5160a-104">Method to move, migrate or relocate a virtual system to a target host specified by a network name or IP address.</span></span>

> [!Note]  
> <span data-ttu-id="5160a-105">Esse método destina-se a ser uma solução de transição somente até que a modelagem de suporte a cluster esteja disponível.</span><span class="sxs-lookup"><span data-stu-id="5160a-105">This method is intended as a transitional solution only until modeling of cluster support is available.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="5160a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5160a-106">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="5160a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5160a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5160a-108">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5160a-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5160a-109">Sistema de computador virtual de origem a ser migrado.</span><span class="sxs-lookup"><span data-stu-id="5160a-109">Source virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="5160a-110">*DestinationHost* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5160a-110">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5160a-111">Sistema host de destino para a migração.</span><span class="sxs-lookup"><span data-stu-id="5160a-111">Target host system for the migration.</span></span>

<span data-ttu-id="5160a-112">Formatos aceitáveis para esse parâmetro são transmitidos por meio de valores de elementos da propriedade de matriz **DestinationHostFormatsSupported** \[ \] na instância do [**CIM \_ VirtualSystemMigrationCapabilities**](cim-virtualsystemmigrationcapabilities.md) que está associado por meio da Associação de [**\_ ElementCapabilities do CIM**](cim-elementcapabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="5160a-112">Acceptable formats for this parameter are conveyed through values of elements of the **DestinationHostFormatsSupported**\[ \] array property in the instance of the [**CIM\_VirtualSystemMigrationCapabilities**](cim-virtualsystemmigrationcapabilities.md) that is associated through the [**CIM\_ElementCapabilities**](cim-elementcapabilities.md) association.</span></span>

</dd> <dt>

<span data-ttu-id="5160a-113">*MigrationSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5160a-113">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5160a-114">Cadeia de caracteres que contém uma instância inserida da classe [**CIM \_ VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) que representa as configurações de migração aplicáveis à operação de migração.</span><span class="sxs-lookup"><span data-stu-id="5160a-114">String containing an embedded instance of the [**CIM\_VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) class representing migration settings applicable to the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="5160a-115">*NewSystemSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5160a-115">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5160a-116">Cadeia de caracteres que contém uma instância inserida da classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) que representa as novas propriedades aplicáveis ao sistema virtual depois que ele é migrado.</span><span class="sxs-lookup"><span data-stu-id="5160a-116">String containing an embedded instance of the [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) class representing new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="5160a-117">*NewResourceSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5160a-117">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5160a-118">Matriz de cadeias de caracteres que contém uma instância incorporada da classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que representa as novas propriedades aplicáveis aos recursos virtuais no escopo do sistema virtual depois que ele é migrado.</span><span class="sxs-lookup"><span data-stu-id="5160a-118">Array of strings each containing an embedded instance of the [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) class representing new properties applicable to virtual resources in the scope of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="5160a-119">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="5160a-119">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5160a-120">Se a operação for de longa execução, opcionalmente, [**um \_ ConcreteJob CIM**](cim-concretejob.md) que representa o trabalho poderá ser retornado.</span><span class="sxs-lookup"><span data-stu-id="5160a-120">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5160a-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5160a-121">Return value</span></span>

<span data-ttu-id="5160a-122">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="5160a-122">Returns a 0 on success; otherwise, returns an error.</span></span>



| <span data-ttu-id="5160a-123">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5160a-123">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="5160a-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="5160a-124">Description</span></span>                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5160a-125"><dt>**Concluído sem erro**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5160a-125"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="5160a-126">O sistema virtual foi migrado.</span><span class="sxs-lookup"><span data-stu-id="5160a-126">Virtual system was migrated.</span></span><br/>                                                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="5160a-127"><dt>**Sem suporte**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="5160a-127"><dt>**Not Supported**</dt> <dt>1</dt></span></span> </dl>                              | <span data-ttu-id="5160a-128">Método sem suporte pela implementação.</span><span class="sxs-lookup"><span data-stu-id="5160a-128">Method not supported by implementation.</span></span><br/>                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="5160a-129"><dt>**Com falha**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="5160a-129"><dt>**Failed**</dt> <dt>2</dt></span></span> </dl>                                     | <span data-ttu-id="5160a-130">A migração do sistema virtual falhou por motivos não especificados.</span><span class="sxs-lookup"><span data-stu-id="5160a-130">Virtual system migration failed for unspecified reasons.</span></span><br/>                                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="5160a-131"><dt>**Tempo limite**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="5160a-131"><dt>**Timeout**</dt> <dt>3</dt></span></span> </dl>                                    | <span data-ttu-id="5160a-132">Tempo limite de migração do sistema virtual; o estado do sistema virtual é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="5160a-132">Virtual system migration time out; the virtual system state is unknown.</span></span><br/>                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="5160a-133"><dt>**Parâmetro inválido**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="5160a-133"><dt>**Invalid Parameter**</dt> <dt>4</dt></span></span> </dl>                          | <span data-ttu-id="5160a-134">Um ou mais parâmetros são formalmente inválidos.</span><span class="sxs-lookup"><span data-stu-id="5160a-134">One or more parameters are formally invalid.</span></span> <span data-ttu-id="5160a-135">Por exemplo, o valor do parâmetro *DestinationHost* poderia ter sido especificado em um formato sem suporte.</span><span class="sxs-lookup"><span data-stu-id="5160a-135">For example, the value of the *DestinationHost* parameter could have been specified in an unsupported format.</span></span><br/>                                                                                                                                    |
| <dl> <span data-ttu-id="5160a-136"><dt>**Estado inválido**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="5160a-136"><dt>**Invalid State**</dt> <dt>5</dt></span></span> </dl>                              | <span data-ttu-id="5160a-137">O sistema virtual de origem, o sistema host de origem ou o sistema host de destino estão em um estado que permite a inicialização da migração de sistema virtual solicitada; Essa pode ser uma condição temporária.</span><span class="sxs-lookup"><span data-stu-id="5160a-137">The source virtual system, the source host system or the target host system are in a state that does allow initiation of the requested virtual system migration; this may be a temporary condition.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="5160a-138"><dt>**Parâmetros incompatíveis**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="5160a-138"><dt>**Incompatible Parameters**</dt> <dt>6</dt></span></span> </dl>                    | <span data-ttu-id="5160a-139">Um ou mais parâmetros de entrada são incompatíveis como um conjunto ou em relação ao host de destino.</span><span class="sxs-lookup"><span data-stu-id="5160a-139">One or more input parameters are incompatible as a set, or with respect to the target host.</span></span> <span data-ttu-id="5160a-140">Por exemplo, o valor do parâmetro *MigrationNewSettingData* contém propriedades que não são suportadas pelo sistema host de destino identificado pelo valor do parâmetro *DestinationHost* .</span><span class="sxs-lookup"><span data-stu-id="5160a-140">For example the value of the *MigrationNewSettingData* parameter contains properties that are not supported by the target host system identified by the value of the *DestinationHost* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="5160a-141"><dt>**DMTF reservado**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="5160a-141"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>                             |                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="5160a-142"><dt>**Parâmetros de método verificados-trabalho iniciado**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="5160a-142"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="5160a-143"><dt>**Método reservado**</dt> <dt>4097.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="5160a-143"><dt>**Method Reserved**</dt> <dt>4097..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="5160a-144">32768 <dt>**específicos do fornecedor**</dt> <dt>. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="5160a-144"><dt>**Vendor Specific**</dt> <dt>32768..65535</dt></span></span> </dl>                 |                                                                                                                                                                                                                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="5160a-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5160a-145">Requirements</span></span>



| <span data-ttu-id="5160a-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="5160a-146">Requirement</span></span> | <span data-ttu-id="5160a-147">Valor</span><span class="sxs-lookup"><span data-stu-id="5160a-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5160a-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5160a-148">Minimum supported client</span></span><br/> | <span data-ttu-id="5160a-149">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5160a-149">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="5160a-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5160a-150">Minimum supported server</span></span><br/> | <span data-ttu-id="5160a-151">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="5160a-151">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="5160a-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="5160a-152">Namespace</span></span><br/>                | <span data-ttu-id="5160a-153">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="5160a-153">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5160a-154">MOF</span><span class="sxs-lookup"><span data-stu-id="5160a-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5160a-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5160a-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5160a-156">DLL</span><span class="sxs-lookup"><span data-stu-id="5160a-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5160a-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5160a-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5160a-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="5160a-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5160a-159">**\_VIRTUALSYSTEMMIGRATIONSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="5160a-159">**CIM\_VirtualSystemMigrationService**</span></span>](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 





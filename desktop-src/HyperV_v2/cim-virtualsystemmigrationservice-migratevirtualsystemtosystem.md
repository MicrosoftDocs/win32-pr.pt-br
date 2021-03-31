---
description: Método para mover, migrar ou realocar um sistema virtual para um sistema de destino.
ms.assetid: 210d31f1-093f-4fd5-afd7-5f028b4cb343
title: Método MigrateVirtualSystemToSystem da classe CIM_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.MigrateVirtualSystemToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1459d80785725914cbaa5dda5b81e8d2fabad5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828117"
---
# <a name="migratevirtualsystemtosystem-method-of-the-cim_virtualsystemmigrationservice-class"></a><span data-ttu-id="f413b-103">Método MigrateVirtualSystemToSystem da \_ classe VIRTUALSYSTEMMIGRATIONSERVICE CIM</span><span class="sxs-lookup"><span data-stu-id="f413b-103">MigrateVirtualSystemToSystem method of the CIM\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="f413b-104">Método para mover, migrar ou realocar um sistema virtual para um sistema de destino.</span><span class="sxs-lookup"><span data-stu-id="f413b-104">Method to move, migrate or relocate a virtual system to a target system.</span></span>

<span data-ttu-id="f413b-105">Descrição do código de retorno:</span><span class="sxs-lookup"><span data-stu-id="f413b-105">Return code description:</span></span>

## <a name="syntax"></a><span data-ttu-id="f413b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f413b-106">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="f413b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f413b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f413b-108">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f413b-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f413b-109">Sistema de computador virtual de origem a ser migrado.</span><span class="sxs-lookup"><span data-stu-id="f413b-109">Source virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="f413b-110">*DestinationSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f413b-110">*DestinationSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f413b-111">Sistema host de destino ondepara migrar o sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="f413b-111">Destination host system whereto migrate the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="f413b-112">*MigrationSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f413b-112">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f413b-113">Cadeia de caracteres que contém uma instância inserida da classe [**CIM \_ VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) que representa as configurações de migração aplicáveis à operação de migração.</span><span class="sxs-lookup"><span data-stu-id="f413b-113">String containing an embedded instance of the [**CIM\_VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) class representing migration settings applicable to the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="f413b-114">*NewSystemSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f413b-114">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f413b-115">Cadeia de caracteres que contém uma instância inserida da classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) que representa as novas propriedades aplicáveis ao sistema virtual depois que ele é migrado.</span><span class="sxs-lookup"><span data-stu-id="f413b-115">String containing an embedded instance of the [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) class representing new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="f413b-116">*NewResourceSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f413b-116">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f413b-117">Matriz de cadeias de caracteres que contém uma instância incorporada da classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que representa as novas propriedades aplicáveis aos recursos virtuais no escopo do sistema virtual depois que ele é migrado.</span><span class="sxs-lookup"><span data-stu-id="f413b-117">Array of strings each containing an embedded instance of the [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) class representing new properties applicable to virtual resources in the scope of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="f413b-118">*NewComputerSystem* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f413b-118">*NewComputerSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f413b-119">Referência a uma instância da classe [**de \_ ComputerSystem do CIM**](cim-computersystem.md) que representa o sistema de computador virtual depois que ele foi migrado.</span><span class="sxs-lookup"><span data-stu-id="f413b-119">Reference to an instance of the [**CIM\_ComputerSystem**](cim-computersystem.md) class representing the virtual computer system after it has been migrated.</span></span>

</dd> <dt>

<span data-ttu-id="f413b-120">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="f413b-120">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f413b-121">Se a operação for de longa execução, opcionalmente, [**um \_ ConcreteJob CIM**](cim-concretejob.md) que representa o trabalho poderá ser retornado.</span><span class="sxs-lookup"><span data-stu-id="f413b-121">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f413b-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f413b-122">Return value</span></span>

<span data-ttu-id="f413b-123">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="f413b-123">Returns a 0 on success; otherwise, returns an error.</span></span>



| <span data-ttu-id="f413b-124">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f413b-124">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="f413b-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="f413b-125">Description</span></span>                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f413b-126"><dt>**Concluído sem erro**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f413b-126"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="f413b-127">O sistema virtual foi migrado.</span><span class="sxs-lookup"><span data-stu-id="f413b-127">Virtual system was migrated.</span></span><br/>                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="f413b-128"><dt>**Sem suporte**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f413b-128"><dt>**Not Supported**</dt> <dt>1</dt></span></span> </dl>                              | <span data-ttu-id="f413b-129">Método sem suporte pela implementação.</span><span class="sxs-lookup"><span data-stu-id="f413b-129">Method not supported by implementation.</span></span><br/>                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="f413b-130"><dt>**Com falha**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f413b-130"><dt>**Failed**</dt> <dt>2</dt></span></span> </dl>                                     | <span data-ttu-id="f413b-131">A migração do sistema virtual falhou por motivos não especificados.</span><span class="sxs-lookup"><span data-stu-id="f413b-131">Virtual system migration failed for unspecified reasons.</span></span><br/>                                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="f413b-132"><dt>**Tempo limite**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f413b-132"><dt>**Timeout**</dt> <dt>3</dt></span></span> </dl>                                    | <span data-ttu-id="f413b-133">Tempo limite de migração do sistema virtual; o estado do sistema virtual é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="f413b-133">Virtual system migration time out; the virtual system state is unknown.</span></span><br/>                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="f413b-134"><dt>**Parâmetro inválido**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="f413b-134"><dt>**Invalid Parameter**</dt> <dt>4</dt></span></span> </dl>                          | <span data-ttu-id="f413b-135">Um ou mais parâmetros são formalmente inválidos, por exemplo, o valor do parâmetro do sistema de destino não contém um caminho de objeto válido.</span><span class="sxs-lookup"><span data-stu-id="f413b-135">One or more parameters are formally invalid For example, the value of the Destination System parameter does not contain a valid object path.</span></span><br/>                                                                                                                                                    |
| <dl> <span data-ttu-id="f413b-136"><dt>**Estado inválido**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="f413b-136"><dt>**Invalid State**</dt> <dt>5</dt></span></span> </dl>                              | <span data-ttu-id="f413b-137">O sistema virtual de origem, o sistema host de origem ou o sistema host de destino estão em um estado que permite a inicialização da migração de sistema virtual solicitada; Essa pode ser uma condição temporária.</span><span class="sxs-lookup"><span data-stu-id="f413b-137">The source virtual system, the source host system or the target host system are in a state that does allow initiation of the requested virtual system migration; this may be a temporary condition.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="f413b-138"><dt>**Parâmetros incompatíveis**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="f413b-138"><dt>**Incompatible Parameters**</dt> <dt>6</dt></span></span> </dl>                    | <span data-ttu-id="f413b-139">Um ou mais parâmetros de entrada são incompatíveis como um conjunto ou em relação ao host de destino.</span><span class="sxs-lookup"><span data-stu-id="f413b-139">One or more input parameters are incompatible as a set, or with respect to the target host.</span></span> <span data-ttu-id="f413b-140">Por exemplo, o valor do parâmetro *MigrationNewSettingData* contém propriedades que não são suportadas pelo sistema host de destino identificado pelo valor do parâmetro *DestinationSystem* .</span><span class="sxs-lookup"><span data-stu-id="f413b-140">For example the value of the *MigrationNewSettingData* parameter contains properties that are not supported by the target host system identified by the value of the *DestinationSystem* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="f413b-141"><dt>**DMTF reservado**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="f413b-141"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>                             |                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="f413b-142"><dt>**Parâmetros de método verificados-trabalho iniciado**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="f413b-142"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="f413b-143"><dt>**Método reservado**</dt> <dt>4097.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="f413b-143"><dt>**Method Reserved**</dt> <dt>4097..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="f413b-144">32768 <dt>**específicos do fornecedor**</dt> <dt>. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="f413b-144"><dt>**Vendor Specific**</dt> <dt>32768..65535</dt></span></span> </dl>                 |                                                                                                                                                                                                                                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="f413b-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f413b-145">Requirements</span></span>



| <span data-ttu-id="f413b-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="f413b-146">Requirement</span></span> | <span data-ttu-id="f413b-147">Valor</span><span class="sxs-lookup"><span data-stu-id="f413b-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f413b-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f413b-148">Minimum supported client</span></span><br/> | <span data-ttu-id="f413b-149">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f413b-149">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="f413b-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f413b-150">Minimum supported server</span></span><br/> | <span data-ttu-id="f413b-151">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f413b-151">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="f413b-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="f413b-152">Namespace</span></span><br/>                | <span data-ttu-id="f413b-153">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="f413b-153">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f413b-154">MOF</span><span class="sxs-lookup"><span data-stu-id="f413b-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f413b-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f413b-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f413b-156">DLL</span><span class="sxs-lookup"><span data-stu-id="f413b-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f413b-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f413b-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f413b-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="f413b-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f413b-159">**\_VIRTUALSYSTEMMIGRATIONSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="f413b-159">**CIM\_VirtualSystemMigrationService**</span></span>](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 





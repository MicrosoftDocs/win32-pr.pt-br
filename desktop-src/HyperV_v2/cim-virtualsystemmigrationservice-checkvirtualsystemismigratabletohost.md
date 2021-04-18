---
description: Método para executar uma verificação prévia para determinar se um sistema virtual provavelmente será migrado com êxito para um host de destino especificado por um nome de rede ou endereço IP.
ms.assetid: bfcd4063-30fe-4d18-9df9-7b84a680814c
title: Método CheckVirtualSystemIsMigratableToHost da classe CIM_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToHost
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5769691a792b8f74225b640b0058ad4bd0e27c3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810360"
---
# <a name="checkvirtualsystemismigratabletohost-method-of-the-cim_virtualsystemmigrationservice-class"></a><span data-ttu-id="c1fff-103">Método CheckVirtualSystemIsMigratableToHost da \_ classe VIRTUALSYSTEMMIGRATIONSERVICE CIM</span><span class="sxs-lookup"><span data-stu-id="c1fff-103">CheckVirtualSystemIsMigratableToHost method of the CIM\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="c1fff-104">Método para executar uma verificação prévia para determinar se um sistema virtual provavelmente será migrado com êxito para um host de destino especificado por um nome de rede ou endereço IP.</span><span class="sxs-lookup"><span data-stu-id="c1fff-104">Method to perform a pre-check to determine whether a virtual system is likely to be successfully migrated to a target host specified by a network name or IP address.</span></span> <span data-ttu-id="c1fff-105">Esse método não garante que uma migração subsequente sempre terá sucesso, devido à disponibilidade dinâmica de recursos.</span><span class="sxs-lookup"><span data-stu-id="c1fff-105">This method does not guarantee that a subsequent migration will always succeed, due to dynamic resource availability.</span></span>

<span data-ttu-id="c1fff-106">Descrição do código de retorno:</span><span class="sxs-lookup"><span data-stu-id="c1fff-106">Return code description:</span></span>

<span data-ttu-id="c1fff-107">Observação: esse método destina-se a ser uma solução de transição somente até que a modelagem de suporte a cluster esteja disponível.</span><span class="sxs-lookup"><span data-stu-id="c1fff-107">Note: This method is intended as a transitional solution only until modeling of cluster support is available.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1fff-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c1fff-108">Syntax</span></span>


```mof
uint32 CheckVirtualSystemIsMigratableToHost(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 DestinationHost,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] boolean                IsMigratable
);
```



## <a name="parameters"></a><span data-ttu-id="c1fff-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1fff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1fff-110">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c1fff-110">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1fff-111">Uma referência de [**\_ ComputerSystem de CIM**](cim-computersystem.md) para o sistema de computador virtual de origem a ser migrado.</span><span class="sxs-lookup"><span data-stu-id="c1fff-111">A [**CIM\_ComputerSystem**](cim-computersystem.md) reference to the source virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="c1fff-112">*DestinationHost* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c1fff-112">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1fff-113">Sistema host de destino para a migração.</span><span class="sxs-lookup"><span data-stu-id="c1fff-113">Target host system for the migration.</span></span>

<span data-ttu-id="c1fff-114">Formatos aceitáveis para esse parâmetro são transmitidos por meio de valores de elementos da propriedade de matriz **DestinationHostFormatsSupported** \[ \] na instância do [**CIM \_ VirtualSystemMigrationCapabilities**](cim-virtualsystemmigrationcapabilities.md) que está associado por meio da Associação de [**\_ ElementCapabilities do CIM**](cim-elementcapabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="c1fff-114">Acceptable formats for this parameter are conveyed through values of elements of the **DestinationHostFormatsSupported**\[ \] array property in the instance of the [**CIM\_VirtualSystemMigrationCapabilities**](cim-virtualsystemmigrationcapabilities.md) that is associated through the [**CIM\_ElementCapabilities**](cim-elementcapabilities.md) association.</span></span>

</dd> <dt>

<span data-ttu-id="c1fff-115">*MigrationSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c1fff-115">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1fff-116">Cadeia de caracteres que contém uma instância inserida da classe [**CIM \_ VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) que representa as configurações de migração aplicáveis à operação de migração.</span><span class="sxs-lookup"><span data-stu-id="c1fff-116">String containing an embedded instance of the [**CIM\_VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) class representing migration settings applicable to the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="c1fff-117">*NewSystemSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c1fff-117">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1fff-118">Cadeia de caracteres que contém uma instância inserida da classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) que representa as novas propriedades aplicáveis ao sistema virtual depois que ele é migrado.</span><span class="sxs-lookup"><span data-stu-id="c1fff-118">String containing an embedded instance of the [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) class representing new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="c1fff-119">*NewResourceSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c1fff-119">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1fff-120">Matriz de cadeias de caracteres que contém uma instância incorporada da classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que representa as novas propriedades aplicáveis aos recursos virtuais no escopo do sistema virtual depois que ele é migrado.</span><span class="sxs-lookup"><span data-stu-id="c1fff-120">Array of strings each containing an embedded instance of the [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) class representing new properties applicable to virtual resources in the scope of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="c1fff-121">*IsMigratable* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c1fff-121">*IsMigratable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1fff-122">O resultado da verificação de migração que indica se o sistema virtual pode ou não ser migrado com êxito.</span><span class="sxs-lookup"><span data-stu-id="c1fff-122">The migration check result indicating whether or not the virtual system can be successfully migrated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1fff-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c1fff-123">Return value</span></span>

<span data-ttu-id="c1fff-124">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="c1fff-124">Returns a 0 on success; otherwise, returns an error.</span></span>



| <span data-ttu-id="c1fff-125">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c1fff-125">Return code/value</span></span>                                                                                                                                                | <span data-ttu-id="c1fff-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1fff-126">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c1fff-127"><dt>**Concluído sem erro**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c1fff-127"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="c1fff-128">Verificação realizada; resultado relatado por meio do valor do \[ parâmetro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="c1fff-128">Check performed; result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="c1fff-129"><dt>**Sem suporte**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c1fff-129"><dt>**Not Supported**</dt> <dt>1</dt></span></span> </dl>              | <span data-ttu-id="c1fff-130">Método sem suporte pela implementação.</span><span class="sxs-lookup"><span data-stu-id="c1fff-130">Method not supported by implementation.</span></span> <span data-ttu-id="c1fff-131">Nenhum resultado relatado pelo valor do \[ parâmetro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="c1fff-131">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="c1fff-132"><dt>**Com falha**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c1fff-132"><dt>**Failed**</dt> <dt>2</dt></span></span> </dl>                     | <span data-ttu-id="c1fff-133">A verificação falhou por razões não especificadas.</span><span class="sxs-lookup"><span data-stu-id="c1fff-133">Check failed for unspecified reasons.</span></span> <span data-ttu-id="c1fff-134">Nenhum resultado relatado pelo valor do \[ parâmetro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="c1fff-134">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="c1fff-135"><dt>**Tempo limite**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c1fff-135"><dt>**Timeout**</dt> <dt>3</dt></span></span> </dl>                    | <span data-ttu-id="c1fff-136">A verificação atingiu o tempo limite. Nenhum resultado relatado pelo valor do \[ parâmetro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="c1fff-136">Check timed out. No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="c1fff-137"><dt>**Parâmetro inválido**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="c1fff-137"><dt>**Invalid Parameter**</dt> <dt>4</dt></span></span> </dl>          | <span data-ttu-id="c1fff-138">Um ou mais parâmetros são formalmente inválidos.</span><span class="sxs-lookup"><span data-stu-id="c1fff-138">One or more parameters are formally invalid.</span></span> <span data-ttu-id="c1fff-139">Por exemplo, o valor do parâmetro *DestinationHost* poderia ter sido especificado em um formato sem suporte.</span><span class="sxs-lookup"><span data-stu-id="c1fff-139">For example, the value of the *DestinationHost* parameter could have been specified in an unsupported format.</span></span> <span data-ttu-id="c1fff-140">Nenhum resultado relatado pelo valor do \[ parâmetro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="c1fff-140">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                    |
| <dl> <span data-ttu-id="c1fff-141"><dt>**Estado inválido**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="c1fff-141"><dt>**Invalid State**</dt> <dt>5</dt></span></span> </dl>              | <span data-ttu-id="c1fff-142">O sistema virtual de origem, o sistema host de origem ou o sistema host de destino estão em um estado que permite a inicialização da migração de sistema virtual solicitada; Essa pode ser uma condição temporária.</span><span class="sxs-lookup"><span data-stu-id="c1fff-142">The source virtual system, the source host system or the target host system are in a state that does allow initiation of the requested virtual system migration; this may be a temporary condition.</span></span> <span data-ttu-id="c1fff-143">Nenhum resultado relatado pelo valor do \[ parâmetro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="c1fff-143">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="c1fff-144"><dt>**Parâmetros incompatíveis**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="c1fff-144"><dt>**Incompatible Parameters**</dt> <dt>6</dt></span></span> </dl>    | <span data-ttu-id="c1fff-145">Um ou mais parâmetros de entrada são incompatíveis como um conjunto ou em relação ao host de destino.</span><span class="sxs-lookup"><span data-stu-id="c1fff-145">One or more input parameters are incompatible as a set, or with respect to the target host.</span></span> <span data-ttu-id="c1fff-146">Por exemplo, o valor do parâmetro *MigrationNewSettingData* contém propriedades que não são suportadas pelo sistema host de destino identificado pelo valor do parâmetro *DestinationHost* .</span><span class="sxs-lookup"><span data-stu-id="c1fff-146">For example the value of the *MigrationNewSettingData* parameter contains properties that are not supported by the target host system identified by the value of the *DestinationHost* parameter.</span></span> <span data-ttu-id="c1fff-147">Nenhum resultado relatado pelo valor do \[ parâmetro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="c1fff-147">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="c1fff-148"><dt>**DMTF reservado**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="c1fff-148"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>             |                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="c1fff-149"><dt>**Método reservado**</dt> <dt>4097.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="c1fff-149"><dt>**Method Reserved**</dt> <dt>4097..32767</dt></span></span> </dl>  |                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="c1fff-150">32768 <dt>**específicos do fornecedor**</dt> <dt>. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="c1fff-150"><dt>**Vendor Specific**</dt> <dt>32768..65535</dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="requirements"></a><span data-ttu-id="c1fff-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1fff-151">Requirements</span></span>



| <span data-ttu-id="c1fff-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1fff-152">Requirement</span></span> | <span data-ttu-id="c1fff-153">Valor</span><span class="sxs-lookup"><span data-stu-id="c1fff-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1fff-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1fff-154">Minimum supported client</span></span><br/> | <span data-ttu-id="c1fff-155">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c1fff-155">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="c1fff-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1fff-156">Minimum supported server</span></span><br/> | <span data-ttu-id="c1fff-157">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c1fff-157">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="c1fff-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="c1fff-158">Namespace</span></span><br/>                | <span data-ttu-id="c1fff-159">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="c1fff-159">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c1fff-160">MOF</span><span class="sxs-lookup"><span data-stu-id="c1fff-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1fff-161"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c1fff-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c1fff-162">DLL</span><span class="sxs-lookup"><span data-stu-id="c1fff-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1fff-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c1fff-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c1fff-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1fff-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1fff-165">**\_VIRTUALSYSTEMMIGRATIONSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="c1fff-165">**CIM\_VirtualSystemMigrationService**</span></span>](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 





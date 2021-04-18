---
description: Representa as configurações de uma \_ instância Msvm ResourcePool que não estão relacionadas à alocação.
ms.assetid: 32e0066c-7e14-454c-8aa9-06e093ef8072
title: Classe Msvm_ResourcePoolSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolSettingData
- Msvm_ResourcePoolSettingData.InstanceID
- Msvm_ResourcePoolSettingData.Caption
- Msvm_ResourcePoolSettingData.Description
- Msvm_ResourcePoolSettingData.ElementName
- Msvm_ResourcePoolSettingData.PoolID
- Msvm_ResourcePoolSettingData.ResourceType
- Msvm_ResourcePoolSettingData.OtherResourceType
- Msvm_ResourcePoolSettingData.ResourceSubType
- Msvm_ResourcePoolSettingData.LoadBalancingBehavior
- Msvm_ResourcePoolSettingData.MappingBehavior
- Msvm_ResourcePoolSettingData.MappingOrder
- Msvm_ResourcePoolSettingData.Notes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 37ec7dc6600dbc536ac50a2042e7d53ff8043242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747998"
---
# <a name="msvm_resourcepoolsettingdata-class"></a><span data-ttu-id="ae6fc-103">\_Classe Msvm ResourcePoolSettingData</span><span class="sxs-lookup"><span data-stu-id="ae6fc-103">Msvm\_ResourcePoolSettingData class</span></span>

<span data-ttu-id="ae6fc-104">Representa as configurações de uma instância [**Msvm \_ ResourcePool**](msvm-resourcepool.md) que não estão relacionadas à alocação.</span><span class="sxs-lookup"><span data-stu-id="ae6fc-104">Represents the settings of a [**Msvm\_ResourcePool**](msvm-resourcepool.md) instance that are not allocation related.</span></span>

<span data-ttu-id="ae6fc-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="ae6fc-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae6fc-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ae6fc-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourcePoolSettingData : Msvm_AbstractResourcePoolSettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string PoolID;
  uint16 ResourceType;
  string OtherResourceType;
  string ResourceSubType;
  uint16 LoadBalancingBehavior;
  uint16 MappingBehavior;
  string MappingOrder[];
  string Notes;
};
```

## <a name="members"></a><span data-ttu-id="ae6fc-107">Membros</span><span class="sxs-lookup"><span data-stu-id="ae6fc-107">Members</span></span>

<span data-ttu-id="ae6fc-108">A classe **Msvm \_ ResourcePoolSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ae6fc-108">The **Msvm\_ResourcePoolSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="ae6fc-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ae6fc-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ae6fc-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ae6fc-110">Properties</span></span>

<span data-ttu-id="ae6fc-111">A classe **Msvm \_ ResourcePoolSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ae6fc-111">The **Msvm\_ResourcePoolSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ae6fc-112">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="ae6fc-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6fc-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ae6fc-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae6fc-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae6fc-115">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="ae6fc-115">A short description of the object.</span></span> <span data-ttu-id="ae6fc-116">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ae6fc-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ae6fc-117">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ae6fc-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6fc-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ae6fc-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae6fc-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae6fc-120">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="ae6fc-120">A description of the object.</span></span> <span data-ttu-id="ae6fc-121">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ae6fc-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ae6fc-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ae6fc-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6fc-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ae6fc-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae6fc-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae6fc-125">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="ae6fc-125">A display name for the object.</span></span> <span data-ttu-id="ae6fc-126">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ae6fc-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ae6fc-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ae6fc-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6fc-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ae6fc-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae6fc-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-130">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="ae6fc-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ae6fc-131">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="ae6fc-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ae6fc-132">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ae6fc-132">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ae6fc-133">**LoadBalancingBehavior**</span><span class="sxs-lookup"><span data-stu-id="ae6fc-133">**LoadBalancingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6fc-134">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae6fc-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae6fc-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae6fc-136">Especifica a estratégia de alocação a ser usada pelo pool de recursos para balancear o uso de recursos em seus recursos agregados.</span><span class="sxs-lookup"><span data-stu-id="ae6fc-136">Specifies the allocation strategy to be used by the resource pool to balance resource usage across its aggregated resources.</span></span> <span data-ttu-id="ae6fc-137">Esta propriedade é herdada de [**Msvm \_ AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="ae6fc-137">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

<dl> <dt>

<span data-ttu-id="ae6fc-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-139"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (2)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-139"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-140"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Nenhum** (3)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-140"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-141"><span id="Distributed"></span><span id="distributed"></span><span id="DISTRIBUTED"></span>**Distribuído** (4)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-141"><span id="Distributed"></span><span id="distributed"></span><span id="DISTRIBUTED"></span>**Distributed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-142"><span id="Consolidated_"></span><span id="consolidated_"></span><span id="CONSOLIDATED_"></span>**Consolidado** (5)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-142"><span id="Consolidated_"></span><span id="consolidated_"></span><span id="CONSOLIDATED_"></span>**Consolidated** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ae6fc-143">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="ae6fc-143">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6fc-144">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae6fc-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae6fc-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae6fc-146">Especifica se o pool de recursos pode tentar usar outros recursos de host para satisfazer a solicitação de alocação se os recursos desejados não puderem ser alocados.</span><span class="sxs-lookup"><span data-stu-id="ae6fc-146">Specifies whether the resource pool can attempt to use other host resources to satisfy the allocation request if the desired resources cannot be allocated.</span></span> <span data-ttu-id="ae6fc-147">Esta propriedade é herdada de [**Msvm \_ AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="ae6fc-147">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

<dl> <dt>

<span data-ttu-id="ae6fc-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-149"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (2)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-149"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-150"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (3)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-150"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-151"><span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>**Afinidade flexível** (4)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-151"><span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>**Soft Affinity** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-152"><span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>**Afinidade rígida** (5)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-152"><span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>**Hard Affinity** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-154"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-154"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32767..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ae6fc-155">**MappingOrder**</span><span class="sxs-lookup"><span data-stu-id="ae6fc-155">**MappingOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6fc-156">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ae6fc-156">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae6fc-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae6fc-158">Especifica a ordem na qual os recursos de host disponíveis por meio desse pool serão selecionados ao tentar atender a uma solicitação de alocação e o recurso de host solicitado não estiver disponível ou nenhum recurso de host for especificado.</span><span class="sxs-lookup"><span data-stu-id="ae6fc-158">Specifies the order in which host resources available through this pool will be selected when attempting to satisfy an allocation request, and the requested host resource is not available or no host resource is specified.</span></span> <span data-ttu-id="ae6fc-159">Esta propriedade é herdada de [**Msvm \_ AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="ae6fc-159">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae6fc-160">**Observações**</span><span class="sxs-lookup"><span data-stu-id="ae6fc-160">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6fc-161">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ae6fc-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae6fc-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae6fc-163">Notas fornecidas pelo usuário final que estão relacionadas a esse pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="ae6fc-163">End-user supplied notes that are related to this resource pool.</span></span> <span data-ttu-id="ae6fc-164">Esta propriedade é herdada de [**Msvm \_ AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="ae6fc-164">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae6fc-165">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="ae6fc-165">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6fc-166">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ae6fc-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae6fc-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae6fc-168">Uma cadeia de caracteres que descreve o tipo de recurso quando um valor bem definido não está disponível e **ResourceType** é definido como 0 (outro).</span><span class="sxs-lookup"><span data-stu-id="ae6fc-168">A string that describes the resource type when a well defined value is not available and **ResourceType** is set to 0 (Other).</span></span> <span data-ttu-id="ae6fc-169">Esta propriedade é herdada de [**Msvm \_ AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="ae6fc-169">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae6fc-170">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="ae6fc-170">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6fc-171">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ae6fc-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae6fc-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae6fc-173">Um identificador para o pool.</span><span class="sxs-lookup"><span data-stu-id="ae6fc-173">An identifier for the pool.</span></span> <span data-ttu-id="ae6fc-174">Essa propriedade é usada para fornecer correlação entre salvar e restaurar dados de configuração para o armazenamento persistente subjacente.</span><span class="sxs-lookup"><span data-stu-id="ae6fc-174">This property is used to provide correlation across save and restore of configuration data to underlying persistent storage.</span></span> <span data-ttu-id="ae6fc-175">Esta propriedade é herdada de [**Msvm \_ AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="ae6fc-175">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae6fc-176">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="ae6fc-176">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6fc-177">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ae6fc-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae6fc-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae6fc-179">Uma cadeia de caracteres que descreve um subtipo específico da implementação para este pool.</span><span class="sxs-lookup"><span data-stu-id="ae6fc-179">A string that describes an implementation-specific subtype for this pool.</span></span> <span data-ttu-id="ae6fc-180">Por exemplo, isso pode ser usado para distinguir modelos diferentes do mesmo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="ae6fc-180">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="ae6fc-181">Esta propriedade é herdada de [**Msvm \_ AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="ae6fc-181">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae6fc-182">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="ae6fc-182">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae6fc-183">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae6fc-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ae6fc-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae6fc-185">O tipo de recurso que esse pool de recursos pode alocar.</span><span class="sxs-lookup"><span data-stu-id="ae6fc-185">The type of resource this resource pool can allocate.</span></span> <span data-ttu-id="ae6fc-186">Esta propriedade é herdada de [**Msvm \_ AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="ae6fc-186">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

<dl> <dt>

<span data-ttu-id="ae6fc-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-188"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Sistema de computador** (2)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-188"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-189"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processador** (3)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-189"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-190"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memória** (4)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-190"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-191"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**Controlador IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-191"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-192"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**HBA SCSI paralelo** (6)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-192"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-193"><span id="FC_HBA"></span><span id="fc_hba"></span>**HBA FC** (7)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-193"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-194"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-194"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-195"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-195"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-196"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Adaptador Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-196"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-197"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Outro adaptador de rede** (11)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-197"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-198"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Slot de e/s** (12)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-198"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-199"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Dispositivo de e/s** (13)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-199"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-200"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Unidade de disquete** (14)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-200"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Floppy Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-201"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Unidade de CD** (15)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-201"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-202"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**Unidade de DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-202"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-203"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Unidade de disco** (17)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-203"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Disk Drive** (17)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-204"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Unidade de fita** (18)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-204"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Tape Drive** (18)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-205"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Extensão de armazenamento** (19)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-205"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (19)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-206"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Outro dispositivo de armazenamento** (20)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-206"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other storage device** (20)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-207"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Porta serial** (21)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-207"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (21)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-208"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Porta paralela** (22)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-208"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (22)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-209"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Controlador USB** (23)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-209"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB Controller** (23)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-210"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Controlador de gráficos** (24)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-210"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (24)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-211"><span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**Controlador IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-211"><span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 Controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-212"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unidade particionável** (26)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-212"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-213"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unidade particionável de base** (27)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-213"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-214"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Energia** (28)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-214"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Power** (28)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-215"><span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>**Capacidade de resfriamento** (29)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-215"><span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>**Cooling Capacity** (29)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-216"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Porta do comutador Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-216"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Ethernet Switch Port** (30)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-217"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Disco lógico** (31)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-217"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Logical Disk** (31)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-218"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Volume de armazenamento** (32)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-218"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Storage Volume** (32)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-219"><span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Conexão Ethernet** (33)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-219"><span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet Connection** (33)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-220"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="ae6fc-220"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ae6fc-221"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="ae6fc-221"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..0xFFFF )</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ae6fc-222">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae6fc-222">Requirements</span></span>



| <span data-ttu-id="ae6fc-223">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae6fc-223">Requirement</span></span> | <span data-ttu-id="ae6fc-224">Valor</span><span class="sxs-lookup"><span data-stu-id="ae6fc-224">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae6fc-225">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae6fc-225">Minimum supported client</span></span><br/> | <span data-ttu-id="ae6fc-226">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ae6fc-226">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ae6fc-227">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae6fc-227">Minimum supported server</span></span><br/> | <span data-ttu-id="ae6fc-228">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ae6fc-228">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ae6fc-229">Namespace</span><span class="sxs-lookup"><span data-stu-id="ae6fc-229">Namespace</span></span><br/>                | <span data-ttu-id="ae6fc-230">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="ae6fc-230">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ae6fc-231">MOF</span><span class="sxs-lookup"><span data-stu-id="ae6fc-231">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae6fc-232"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ae6fc-232"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ae6fc-233">DLL</span><span class="sxs-lookup"><span data-stu-id="ae6fc-233">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae6fc-234"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ae6fc-234"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


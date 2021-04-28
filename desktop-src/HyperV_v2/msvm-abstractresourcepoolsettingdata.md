---
description: Classe Msvm_AbstractResourcePoolSettingData – representa as configurações de uma \_ instância Msvm ResourcePool que não estão relacionadas à alocação.
ms.assetid: c5954a92-8942-4b45-aae2-6936328dab1a
title: Classe Msvm_AbstractResourcePoolSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AbstractResourcePoolSettingData
- Msvm_AbstractResourcePoolSettingData.InstanceID
- Msvm_AbstractResourcePoolSettingData.Caption
- Msvm_AbstractResourcePoolSettingData.Description
- Msvm_AbstractResourcePoolSettingData.ElementName
- Msvm_AbstractResourcePoolSettingData.PoolID
- Msvm_AbstractResourcePoolSettingData.ResourceType
- Msvm_AbstractResourcePoolSettingData.OtherResourceType
- Msvm_AbstractResourcePoolSettingData.ResourceSubType
- Msvm_AbstractResourcePoolSettingData.LoadBalancingBehavior
- Msvm_AbstractResourcePoolSettingData.MappingBehavior
- Msvm_AbstractResourcePoolSettingData.MappingOrder
- Msvm_AbstractResourcePoolSettingData.Notes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dca3da14ac74a8d6fab1ba96db98f9e2eccd74ea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112114"
---
# <a name="msvm_abstractresourcepoolsettingdata-class"></a><span data-ttu-id="33106-103">\_Classe Msvm AbstractResourcePoolSettingData</span><span class="sxs-lookup"><span data-stu-id="33106-103">Msvm\_AbstractResourcePoolSettingData class</span></span>

<span data-ttu-id="33106-104">Representa as configurações de uma instância [**Msvm \_ ResourcePool**](msvm-resourcepool.md) que não estão relacionadas à alocação.</span><span class="sxs-lookup"><span data-stu-id="33106-104">Represents the settings of a [**Msvm\_ResourcePool**](msvm-resourcepool.md) instance that are not allocation related.</span></span>

<span data-ttu-id="33106-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="33106-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="33106-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33106-106">Syntax</span></span>

``` syntax
[Abstract, AMENDMENT]
class Msvm_AbstractResourcePoolSettingData : CIM_SettingData
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

## <a name="members"></a><span data-ttu-id="33106-107">Membros</span><span class="sxs-lookup"><span data-stu-id="33106-107">Members</span></span>

<span data-ttu-id="33106-108">A classe **Msvm \_ AbstractResourcePoolSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="33106-108">The **Msvm\_AbstractResourcePoolSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="33106-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="33106-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="33106-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="33106-110">Properties</span></span>

<span data-ttu-id="33106-111">A classe **Msvm \_ AbstractResourcePoolSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="33106-111">The **Msvm\_AbstractResourcePoolSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="33106-112">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="33106-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33106-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="33106-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33106-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33106-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33106-115">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="33106-115">A short description of the object.</span></span> <span data-ttu-id="33106-116">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="33106-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="33106-117">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="33106-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33106-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="33106-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33106-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33106-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33106-120">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="33106-120">A description of the object.</span></span> <span data-ttu-id="33106-121">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="33106-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="33106-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="33106-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33106-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="33106-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33106-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33106-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33106-125">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="33106-125">A display name for the object.</span></span> <span data-ttu-id="33106-126">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="33106-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="33106-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="33106-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33106-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="33106-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33106-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33106-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33106-130">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="33106-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="33106-131">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="33106-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="33106-132">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="33106-132">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="33106-133">**LoadBalancingBehavior**</span><span class="sxs-lookup"><span data-stu-id="33106-133">**LoadBalancingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33106-134">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="33106-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="33106-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33106-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33106-136">Especifica a estratégia de alocação a ser usada pelo pool de recursos para balancear o uso de recursos em seus recursos agregados.</span><span class="sxs-lookup"><span data-stu-id="33106-136">Specifies the allocation strategy to be used by the resource pool to balance resource usage across its aggregated resources.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="33106-137">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="33106-137">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="33106-138">**Sem suporte** (2)</span><span class="sxs-lookup"><span data-stu-id="33106-138">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="33106-139">**Nenhum** (3)</span><span class="sxs-lookup"><span data-stu-id="33106-139">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Distributed"></span><span id="distributed"></span><span id="DISTRIBUTED"></span>

<span data-ttu-id="33106-140">**Distribuído** (4)</span><span class="sxs-lookup"><span data-stu-id="33106-140">**Distributed** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Consolidated"></span><span id="consolidated"></span><span id="CONSOLIDATED"></span>

<span data-ttu-id="33106-141">**Consolidado** (5)</span><span class="sxs-lookup"><span data-stu-id="33106-141">**Consolidated** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="33106-142">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="33106-142">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33106-143">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="33106-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="33106-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33106-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33106-145">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**MappingBehavior**")</span><span class="sxs-lookup"><span data-stu-id="33106-145">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**MappingBehavior**")</span></span>
</dt> </dl>

<span data-ttu-id="33106-146">Especifica se o pool de recursos pode tentar usar outros recursos de host para satisfazer a solicitação de alocação se os recursos desejados não puderem ser alocados.</span><span class="sxs-lookup"><span data-stu-id="33106-146">Specifies whether the resource pool can attempt to use other host resources to satisfy the allocation request if the desired resources cannot be allocated.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="33106-147">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="33106-147">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="33106-148">**Sem suporte** (2)</span><span class="sxs-lookup"><span data-stu-id="33106-148">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="33106-149">**Dedicado** (3)</span><span class="sxs-lookup"><span data-stu-id="33106-149">**Dedicated** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>

<span data-ttu-id="33106-150">**Afinidade flexível** (4)</span><span class="sxs-lookup"><span data-stu-id="33106-150">**Soft Affinity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>

<span data-ttu-id="33106-151">**Afinidade rígida** (5)</span><span class="sxs-lookup"><span data-stu-id="33106-151">**Hard Affinity** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="33106-152">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="33106-152">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="33106-153">**Fornecedor reservado** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="33106-153">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="33106-154">**MappingOrder**</span><span class="sxs-lookup"><span data-stu-id="33106-154">**MappingOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33106-155">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="33106-155">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="33106-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33106-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33106-157">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm \_ ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md).**MappingBehavior**")</span><span class="sxs-lookup"><span data-stu-id="33106-157">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm\_ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md).**MappingBehavior**")</span></span>
</dt> </dl>

<span data-ttu-id="33106-158">Especifica a ordem na qual os recursos de host disponíveis por meio desse pool serão selecionados ao tentar atender a uma solicitação de alocação e o recurso de host solicitado não estiver disponível ou nenhum recurso de host for especificado.</span><span class="sxs-lookup"><span data-stu-id="33106-158">Specifies the order in which host resources available through this pool will be selected when attempting to satisfy an allocation request, and the requested host resource is not available or no host resource is specified.</span></span>

</dd> <dt>

<span data-ttu-id="33106-159">**Observações**</span><span class="sxs-lookup"><span data-stu-id="33106-159">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33106-160">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="33106-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33106-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33106-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33106-162">Notas fornecidas pelo usuário final que estão relacionadas a esse pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="33106-162">End-user supplied notes that are related to this resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="33106-163">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="33106-163">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33106-164">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="33106-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33106-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33106-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33106-166">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourcePool**](cim-resourcepool.md).**OtherResourceType**")</span><span class="sxs-lookup"><span data-stu-id="33106-166">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**OtherResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="33106-167">Uma cadeia de caracteres que descreve o tipo de recurso quando um valor bem definido não está disponível e **ResourceType** é definido como 0 (outro).</span><span class="sxs-lookup"><span data-stu-id="33106-167">A string that describes the resource type when a well defined value is not available and **ResourceType** is set to 0 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="33106-168">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="33106-168">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33106-169">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="33106-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33106-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33106-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33106-171">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourcePool**](cim-resourcepool.md).**Poolid**")</span><span class="sxs-lookup"><span data-stu-id="33106-171">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**PoolID**")</span></span>
</dt> </dl>

<span data-ttu-id="33106-172">Um identificador para o pool.</span><span class="sxs-lookup"><span data-stu-id="33106-172">An identifier for the pool.</span></span> <span data-ttu-id="33106-173">Essa propriedade é usada para fornecer correlação entre salvar e restaurar dados de configuração para o armazenamento persistente subjacente.</span><span class="sxs-lookup"><span data-stu-id="33106-173">This property is used to provide correlation across save and restore of configuration data to underlying persistent storage.</span></span>

</dd> <dt>

<span data-ttu-id="33106-174">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="33106-174">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33106-175">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="33106-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33106-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33106-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33106-177">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourcePool**](cim-resourcepool.md).**ResourceSubType**")</span><span class="sxs-lookup"><span data-stu-id="33106-177">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**ResourceSubType**")</span></span>
</dt> </dl>

<span data-ttu-id="33106-178">Uma cadeia de caracteres que descreve um subtipo específico de implementação para esse pool.</span><span class="sxs-lookup"><span data-stu-id="33106-178">A string that describes an implementation specific sub-type for this pool.</span></span> <span data-ttu-id="33106-179">Por exemplo, isso pode ser usado para distinguir modelos diferentes do mesmo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="33106-179">For example, this may be used to distinguish different models of the same resource type.</span></span>

</dd> <dt>

<span data-ttu-id="33106-180">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="33106-180">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33106-181">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="33106-181">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="33106-182">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33106-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33106-183">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourcePool**](cim-resourcepool.md).**ResourceType**")</span><span class="sxs-lookup"><span data-stu-id="33106-183">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="33106-184">O tipo de recurso que esse pool de recursos pode alocar.</span><span class="sxs-lookup"><span data-stu-id="33106-184">The type of resource this resource pool can allocate.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="33106-185">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="33106-185">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>

<span data-ttu-id="33106-186">**Sistema de computador** (2)</span><span class="sxs-lookup"><span data-stu-id="33106-186">**Computer System** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>

<span data-ttu-id="33106-187">**Processador** (3)</span><span class="sxs-lookup"><span data-stu-id="33106-187">**Processor** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>

<span data-ttu-id="33106-188">**Memória** (4)</span><span class="sxs-lookup"><span data-stu-id="33106-188">**Memory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>

<span data-ttu-id="33106-189">**Controlador IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="33106-189">**IDE Controller** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>

<span data-ttu-id="33106-190">**HBA SCSI paralelo** (6)</span><span class="sxs-lookup"><span data-stu-id="33106-190">**Parallel SCSI HBA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>

<span data-ttu-id="33106-191">**HBA FC** (7)</span><span class="sxs-lookup"><span data-stu-id="33106-191">**FC HBA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>

<span data-ttu-id="33106-192">**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="33106-192">**iSCSI HBA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>

<span data-ttu-id="33106-193">**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="33106-193">**IB HCA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>

<span data-ttu-id="33106-194">**Adaptador Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="33106-194">**Ethernet Adapter** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>

<span data-ttu-id="33106-195">**Outro adaptador de rede** (11)</span><span class="sxs-lookup"><span data-stu-id="33106-195">**Other Network Adapter** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>

<span data-ttu-id="33106-196">**Slot de e/s** (12)</span><span class="sxs-lookup"><span data-stu-id="33106-196">**I/O Slot** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>

<span data-ttu-id="33106-197">**Dispositivo de e/s** (13)</span><span class="sxs-lookup"><span data-stu-id="33106-197">**I/O Device** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>

<span data-ttu-id="33106-198">**Unidade de disquete** (14)</span><span class="sxs-lookup"><span data-stu-id="33106-198">**Floppy Drive** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>

<span data-ttu-id="33106-199">**Unidade de CD** (15)</span><span class="sxs-lookup"><span data-stu-id="33106-199">**CD Drive** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>

<span data-ttu-id="33106-200">**Unidade de DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="33106-200">**DVD drive** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="33106-201">**Unidade de disco** (17)</span><span class="sxs-lookup"><span data-stu-id="33106-201">**Disk Drive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>

<span data-ttu-id="33106-202">**Unidade de fita** (18)</span><span class="sxs-lookup"><span data-stu-id="33106-202">**Tape Drive** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>

<span data-ttu-id="33106-203">**Extensão de armazenamento** (19)</span><span class="sxs-lookup"><span data-stu-id="33106-203">**Storage Extent** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>

<span data-ttu-id="33106-204">**Outro dispositivo de armazenamento** (20)</span><span class="sxs-lookup"><span data-stu-id="33106-204">**Other storage device** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>

<span data-ttu-id="33106-205">**Porta serial** (21)</span><span class="sxs-lookup"><span data-stu-id="33106-205">**Serial port** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

<span data-ttu-id="33106-206">**Porta paralela** (22)</span><span class="sxs-lookup"><span data-stu-id="33106-206">**Parallel port** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>

<span data-ttu-id="33106-207">**Controlador USB** (23)</span><span class="sxs-lookup"><span data-stu-id="33106-207">**USB Controller** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>

<span data-ttu-id="33106-208">**Controlador de gráficos** (24)</span><span class="sxs-lookup"><span data-stu-id="33106-208">**Graphics controller** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>

<span data-ttu-id="33106-209">**Controlador IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="33106-209">**IEEE 1394 Controller** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>

<span data-ttu-id="33106-210">**Unidade particionável** (26)</span><span class="sxs-lookup"><span data-stu-id="33106-210">**Partitionable Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>

<span data-ttu-id="33106-211">**Unidade particionável de base** (27)</span><span class="sxs-lookup"><span data-stu-id="33106-211">**Base Partitionable Unit** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="33106-212">**Energia** (28)</span><span class="sxs-lookup"><span data-stu-id="33106-212">**Power** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>

<span data-ttu-id="33106-213">**Capacidade de resfriamento** (29)</span><span class="sxs-lookup"><span data-stu-id="33106-213">**Cooling Capacity** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>

<span data-ttu-id="33106-214">**Porta do comutador Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="33106-214">**Ethernet Switch Port** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>

<span data-ttu-id="33106-215">**Disco lógico** (31)</span><span class="sxs-lookup"><span data-stu-id="33106-215">**Logical Disk** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>

<span data-ttu-id="33106-216">**Volume de armazenamento** (32)</span><span class="sxs-lookup"><span data-stu-id="33106-216">**Storage Volume** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>

<span data-ttu-id="33106-217">**Conexão Ethernet** (33)</span><span class="sxs-lookup"><span data-stu-id="33106-217">**Ethernet Connection** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="33106-218">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="33106-218">**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="33106-219">**Fornecedor reservado** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="33106-219">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


<span data-ttu-id="33106-220"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="33106-220"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="33106-221">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33106-221">Requirements</span></span>



| <span data-ttu-id="33106-222">Requisito</span><span class="sxs-lookup"><span data-stu-id="33106-222">Requirement</span></span> | <span data-ttu-id="33106-223">Valor</span><span class="sxs-lookup"><span data-stu-id="33106-223">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33106-224">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33106-224">Minimum supported client</span></span><br/> | <span data-ttu-id="33106-225">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="33106-225">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="33106-226">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33106-226">Minimum supported server</span></span><br/> | <span data-ttu-id="33106-227">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="33106-227">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="33106-228">Namespace</span><span class="sxs-lookup"><span data-stu-id="33106-228">Namespace</span></span><br/>                | <span data-ttu-id="33106-229">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="33106-229">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="33106-230">MOF</span><span class="sxs-lookup"><span data-stu-id="33106-230">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33106-231"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="33106-231"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="33106-232">DLL</span><span class="sxs-lookup"><span data-stu-id="33106-232">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33106-233"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="33106-233"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


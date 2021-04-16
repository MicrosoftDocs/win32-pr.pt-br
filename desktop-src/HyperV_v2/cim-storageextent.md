---
description: Descreve os recursos e o gerenciamento de mídia que armazena dados e permite a recuperação dos dados. Essa super classe é usada para representar componentes RAID de software e hardware, ou uma extensão lógica bruta de mídia física.
ms.assetid: 29d105fb-8c34-4824-8679-883aef02a0c9
title: Classe CIM_StorageExtent (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageExtent
- CIM_StorageExtent.DataOrganization
- CIM_StorageExtent.Purpose
- CIM_StorageExtent.Access
- CIM_StorageExtent.ErrorMethodology
- CIM_StorageExtent.BlockSize
- CIM_StorageExtent.NumberOfBlocks
- CIM_StorageExtent.ConsumableBlocks
- CIM_StorageExtent.IsBasedOnUnderlyingRedundancy
- CIM_StorageExtent.SequentialAccess
- CIM_StorageExtent.ExtentStatus
- CIM_StorageExtent.NoSinglePointOfFailure
- CIM_StorageExtent.DataRedundancy
- CIM_StorageExtent.PackageRedundancy
- CIM_StorageExtent.DeltaReservation
- CIM_StorageExtent.Primordial
- CIM_StorageExtent.Name
- CIM_StorageExtent.NameFormat
- CIM_StorageExtent.NameNamespace
- CIM_StorageExtent.OtherNameNamespace
- CIM_StorageExtent.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a3dc1b58dd97582e229497e754d10c3f307eab76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761716"
---
# <a name="cim_storageextent-class-hyper-v-management"></a><span data-ttu-id="7d013-104">Classe CIM_StorageExtent (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="7d013-104">CIM_StorageExtent class (Hyper-V management)</span></span>

<span data-ttu-id="7d013-105">Descreve os recursos e o gerenciamento de mídia que armazena dados e permite a recuperação dos dados.</span><span class="sxs-lookup"><span data-stu-id="7d013-105">Describes the capabilities and management of media that stores data and allows retrieval of the data.</span></span> <span data-ttu-id="7d013-106">Essa super classe é usada para representar componentes RAID de software e hardware, ou uma extensão lógica bruta de mídia física.</span><span class="sxs-lookup"><span data-stu-id="7d013-106">This super class is used to represent software and hardware RAID components, or a raw logical extent of physical media.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d013-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7d013-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.13.0"), UMLPackagePath("CIM::Core::StorageExtent"), AMENDMENT]
class CIM_StorageExtent : CIM_LogicalDevice
{
  uint16  DataOrganization;
  string  Purpose;
  uint16  Access;
  string  ErrorMethodology;
  uint64  BlockSize;
  uint64  NumberOfBlocks;
  uint64  ConsumableBlocks;
  boolean IsBasedOnUnderlyingRedundancy;
  boolean SequentialAccess;
  uint16  ExtentStatus[];
  boolean NoSinglePointOfFailure;
  uint16  DataRedundancy;
  uint16  PackageRedundancy;
  uint8   DeltaReservation;
  boolean Primordial = FALSE;
  string  Name;
  uint16  NameFormat;
  uint16  NameNamespace;
  string  OtherNameNamespace;
  string  OtherNameFormat;
};
```

## <a name="members"></a><span data-ttu-id="7d013-108">Membros</span><span class="sxs-lookup"><span data-stu-id="7d013-108">Members</span></span>

<span data-ttu-id="7d013-109">A classe **CIM \_ StorageExtent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7d013-109">The **CIM\_StorageExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="7d013-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7d013-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7d013-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7d013-111">Properties</span></span>

<span data-ttu-id="7d013-112">A classe **CIM \_ StorageExtent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7d013-112">The **CIM\_StorageExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7d013-113">**Acesso**</span><span class="sxs-lookup"><span data-stu-id="7d013-113">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d013-114">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7d013-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7d013-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7d013-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d013-116">Uma descrição do suporte de leitura/gravação da mídia.</span><span class="sxs-lookup"><span data-stu-id="7d013-116">A description of the read/write support of the media.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7d013-117">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="7d013-117">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="7d013-118">**Legível** (1)</span><span class="sxs-lookup"><span data-stu-id="7d013-118">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="7d013-119">**Gravável** (2)</span><span class="sxs-lookup"><span data-stu-id="7d013-119">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="7d013-120">**Suporte de leitura/gravação** (3)</span><span class="sxs-lookup"><span data-stu-id="7d013-120">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="7d013-121">**Gravar uma vez** (4)</span><span class="sxs-lookup"><span data-stu-id="7d013-121">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7d013-122">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="7d013-122">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d013-123">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7d013-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7d013-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7d013-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d013-125">Qualificadores: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Armazenamento de host DMTF \| 1,4 "," MIB. IETF \| host-REsources-MIB. hrStorageAllocationUnits "," MIF. \|Dispositivos de armazenamento DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="7d013-125">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Host Storage\|001.4", "MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits", "MIF.DMTF\|Storage Devices\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="7d013-126">O tamanho, em bytes, dos blocos que formam a extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7d013-126">The size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="7d013-127">Se forem usados tamanhos de bloco variáveis, essa propriedade deverá especificar o tamanho máximo do bloco.</span><span class="sxs-lookup"><span data-stu-id="7d013-127">If variable block sizes are used, then this property should specify the maximum block size.</span></span> <span data-ttu-id="7d013-128">Se o tamanho do bloco for desconhecido ou se um conceito de bloco não for válido (por exemplo, para **CIM \_ AggregateExtent**, [**\_ memória CIM**](cim-memory.md) ou disco [**CIM \_**](cim-logicaldisk.md)), essa propriedade deverá ser definida como "1" (desconhecido).</span><span class="sxs-lookup"><span data-stu-id="7d013-128">If the block size is unknown or if a block concept is not valid (for example, for **CIM\_AggregateExtent**, [**CIM\_Memory**](cim-memory.md) or [**CIM\_LogicalDisk**](cim-logicaldisk.md)), then this property should be set to "1" (unknow).</span></span>

</dd> <dt>

<span data-ttu-id="7d013-129">**ConsumableBlocks**</span><span class="sxs-lookup"><span data-stu-id="7d013-129">**ConsumableBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d013-130">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7d013-130">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7d013-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7d013-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d013-132">O número máximo de blocos, que estão disponíveis para uso durante a camada **de \_ StorageExtent de CIM** usando a associação de classe [**\_ baseada em CIM**](cim-basedon.md) .</span><span class="sxs-lookup"><span data-stu-id="7d013-132">The maximum number of blocks, that are available for use when layering **CIM\_StorageExtent** using the [**CIM\_BasedOn**](cim-basedon.md) class association.</span></span> <span data-ttu-id="7d013-133">Essa propriedade só tem significado quando a extensão de armazenamento é referenciada na propriedade **Antecedent** em um objeto **\_ baseado em CIM** .</span><span class="sxs-lookup"><span data-stu-id="7d013-133">This property only has meaning when the storage extent is referenced in the **Antecedent** property in a **CIM\_BasedOn** object.</span></span>

</dd> <dt>

<span data-ttu-id="7d013-134">**Dataorganization**</span><span class="sxs-lookup"><span data-stu-id="7d013-134">**DataOrganization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d013-135">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7d013-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7d013-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7d013-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d013-137">O tipo de organização de dados usado pela mídia.</span><span class="sxs-lookup"><span data-stu-id="7d013-137">The type of data organization used by the media.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7d013-138">**Outro** (0)</span><span class="sxs-lookup"><span data-stu-id="7d013-138">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7d013-139">**Desconhecido** (1)</span><span class="sxs-lookup"><span data-stu-id="7d013-139">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Block"></span><span id="fixed_block"></span><span id="FIXED_BLOCK"></span>

<span data-ttu-id="7d013-140">**Bloco fixo** (2)</span><span class="sxs-lookup"><span data-stu-id="7d013-140">**Fixed Block** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Variable_Block"></span><span id="variable_block"></span><span id="VARIABLE_BLOCK"></span>

<span data-ttu-id="7d013-141">**Bloco de variável** (3)</span><span class="sxs-lookup"><span data-stu-id="7d013-141">**Variable Block** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Count_Key_Data"></span><span id="count_key_data"></span><span id="COUNT_KEY_DATA"></span>

<span data-ttu-id="7d013-142">**Dados de chave de contagem** (4)</span><span class="sxs-lookup"><span data-stu-id="7d013-142">**Count Key Data** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7d013-143">**Dataredundância**</span><span class="sxs-lookup"><span data-stu-id="7d013-143">**DataRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d013-144">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7d013-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7d013-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7d013-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d013-146">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**DataRedundancyGoal**","**CIM \_ StorageSetting**.**DataRedundancyMax**","**CIM \_ StorageSetting**.**DataRedundancyMin**")</span><span class="sxs-lookup"><span data-stu-id="7d013-146">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**DataRedundancyGoal**", "**CIM\_StorageSetting**.**DataRedundancyMax**", "**CIM\_StorageSetting**.**DataRedundancyMin**")</span></span>
</dt> </dl>

<span data-ttu-id="7d013-147">O número de cópias completas dos dados atualmente mantidos.</span><span class="sxs-lookup"><span data-stu-id="7d013-147">The number of complete copies of data that are currently maintained.</span></span>

</dd> <dt>

<span data-ttu-id="7d013-148">**DeltaReservation**</span><span class="sxs-lookup"><span data-stu-id="7d013-148">**DeltaReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d013-149">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="7d013-149">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="7d013-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7d013-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d013-151">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("Percentage"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (100), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**DeltaReservationGoal**","**CIM \_ StorageSetting**.**DeltaReservationMax**","**CIM \_ StorageSetting**.**DeltaReservationMin**")</span><span class="sxs-lookup"><span data-stu-id="7d013-151">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Percentage"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (100), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**DeltaReservationGoal**", "**CIM\_StorageSetting**.**DeltaReservationMax**", "**CIM\_StorageSetting**.**DeltaReservationMin**")</span></span>
</dt> </dl>

<span data-ttu-id="7d013-152">O valor atual para reserva de deltas.</span><span class="sxs-lookup"><span data-stu-id="7d013-152">The current value for delta reservation.</span></span> <span data-ttu-id="7d013-153">Essa é uma porcentagem que especifica a quantidade de espaço que deve ser reservada em uma réplica para armazenar em cache as alterações.</span><span class="sxs-lookup"><span data-stu-id="7d013-153">This is a percentage that specifies the amount of space that should be reserved in a replica for caching changes.</span></span>

</dd> <dt>

<span data-ttu-id="7d013-154">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="7d013-154">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d013-155">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7d013-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d013-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7d013-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d013-157">O tipo de detecção de erros e correção com suporte na extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7d013-157">The type of error detection and correction supported by the storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="7d013-158">**ExtentStatus**</span><span class="sxs-lookup"><span data-stu-id="7d013-158">**ExtentStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d013-159">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7d013-159">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7d013-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7d013-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d013-161">Informações de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="7d013-161">Additional status information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7d013-162">**Outro** (0)</span><span class="sxs-lookup"><span data-stu-id="7d013-162">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7d013-163">**Desconhecido** (1)</span><span class="sxs-lookup"><span data-stu-id="7d013-163">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="None_Not_Applicable"></span><span id="none_not_applicable"></span><span id="NONE_NOT_APPLICABLE"></span>

<span data-ttu-id="7d013-164">**Nenhum/não aplicável** (2)</span><span class="sxs-lookup"><span data-stu-id="7d013-164">**None/Not Applicable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Broken"></span><span id="broken"></span><span id="BROKEN"></span>

<span data-ttu-id="7d013-165">**Rompido** (3)</span><span class="sxs-lookup"><span data-stu-id="7d013-165">**Broken** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Data_Lost"></span><span id="data_lost"></span><span id="DATA_LOST"></span>

<span data-ttu-id="7d013-166">**Dados perdidos** (4)</span><span class="sxs-lookup"><span data-stu-id="7d013-166">**Data Lost** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Reconfig"></span><span id="dynamic_reconfig"></span><span id="DYNAMIC_RECONFIG"></span>

<span data-ttu-id="7d013-167">**Reconfiguração dinâmica** (5)</span><span class="sxs-lookup"><span data-stu-id="7d013-167">**Dynamic Reconfig** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Exposed"></span><span id="exposed"></span><span id="EXPOSED"></span>

<span data-ttu-id="7d013-168">**Exposto** (6)</span><span class="sxs-lookup"><span data-stu-id="7d013-168">**Exposed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Fractionally_Exposed"></span><span id="fractionally_exposed"></span><span id="FRACTIONALLY_EXPOSED"></span>

<span data-ttu-id="7d013-169">**Exposto fracionalmente** (7)</span><span class="sxs-lookup"><span data-stu-id="7d013-169">**Fractionally Exposed** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Partially_Exposed"></span><span id="partially_exposed"></span><span id="PARTIALLY_EXPOSED"></span>

<span data-ttu-id="7d013-170">**Parcialmente exposto** (8)</span><span class="sxs-lookup"><span data-stu-id="7d013-170">**Partially Exposed** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Protection_Disabled"></span><span id="protection_disabled"></span><span id="PROTECTION_DISABLED"></span>

<span data-ttu-id="7d013-171">**Proteção desabilitada** (9)</span><span class="sxs-lookup"><span data-stu-id="7d013-171">**Protection Disabled** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Readying"></span><span id="readying"></span><span id="READYING"></span>

<span data-ttu-id="7d013-172">**Pronto** (10)</span><span class="sxs-lookup"><span data-stu-id="7d013-172">**Readying** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Rebuild"></span><span id="rebuild"></span><span id="REBUILD"></span>

<span data-ttu-id="7d013-173">**Recompilação** (11)</span><span class="sxs-lookup"><span data-stu-id="7d013-173">**Rebuild** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Recalculate"></span><span id="recalculate"></span><span id="RECALCULATE"></span>

<span data-ttu-id="7d013-174">**Recalcular** (12)</span><span class="sxs-lookup"><span data-stu-id="7d013-174">**Recalculate** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Spare_in_Use"></span><span id="spare_in_use"></span><span id="SPARE_IN_USE"></span>

<span data-ttu-id="7d013-175">**Reposição em uso** (13)</span><span class="sxs-lookup"><span data-stu-id="7d013-175">**Spare in Use** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Verify_In_Progress"></span><span id="verify_in_progress"></span><span id="VERIFY_IN_PROGRESS"></span>

<span data-ttu-id="7d013-176">**Verificação em andamento** (14)</span><span class="sxs-lookup"><span data-stu-id="7d013-176">**Verify In Progress** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="In-Band_Access_Granted"></span><span id="in-band_access_granted"></span><span id="IN-BAND_ACCESS_GRANTED"></span>

<span data-ttu-id="7d013-177">**Acesso em banda concedido** (15)</span><span class="sxs-lookup"><span data-stu-id="7d013-177">**In-Band Access Granted** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Imported"></span><span id="imported"></span><span id="IMPORTED"></span>

<span data-ttu-id="7d013-178">**Importado** (16)</span><span class="sxs-lookup"><span data-stu-id="7d013-178">**Imported** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Exported"></span><span id="exported"></span><span id="EXPORTED"></span>

<span data-ttu-id="7d013-179">**Exportado** (17)</span><span class="sxs-lookup"><span data-stu-id="7d013-179">**Exported** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="7d013-180">**DMTF reservado** (18.. 32767)</span><span class="sxs-lookup"><span data-stu-id="7d013-180">**DMTF Reserved** (18..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="7d013-181">**Fornecedor reservado** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="7d013-181">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7d013-182">**IsBasedOnUnderlyingRedundancy**</span><span class="sxs-lookup"><span data-stu-id="7d013-182">**IsBasedOnUnderlyingRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d013-183">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="7d013-183">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7d013-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7d013-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d013-185">**true** se as extensões de armazenamento subjacentes forem membros de um [**CIM \_ StorageRedundancyGroup**](/windows/desktop/CIMWin32Prov/cim-storageredundancygroup); caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="7d013-185">**true** if the underlying storage extents are members of a [**CIM\_StorageRedundancyGroup**](/windows/desktop/CIMWin32Prov/cim-storageredundancygroup); otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="7d013-186">**Nome**</span><span class="sxs-lookup"><span data-stu-id="7d013-186">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d013-187">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7d013-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d013-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7d013-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d013-189">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SPC. INCITS-T10 \| VPD 83, \| identificador de associação 0 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ StorageExtent**.**NameFormat**","**CIM \_ StorageExtent**.**NameNamespace**")</span><span class="sxs-lookup"><span data-stu-id="7d013-189">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SPC.INCITS-T10\| VPD 83, Association 0 \| Identifier"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_StorageExtent**.**NameFormat**", "**CIM\_StorageExtent**.**NameNamespace**")</span></span>
</dt> </dl>

<span data-ttu-id="7d013-190">Um identificador exclusivo para a extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7d013-190">A unique identifier for the storage extent.</span></span> <span data-ttu-id="7d013-191">A propriedade **NameFormat** especifica o formato de nomenclatura a ser usado na propriedade **Name** .</span><span class="sxs-lookup"><span data-stu-id="7d013-191">The **NameFormat** property specifies the naming format to use in the **Name** property.</span></span>

</dd> <dt>

<span data-ttu-id="7d013-192">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="7d013-192">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d013-193">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7d013-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7d013-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7d013-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d013-195">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ StorageExtent**.**Name**","**CIM \_ StorageExtent**.**NameNamespace**","**CIM \_ StorageExtent**.**OtherNameFormat**")</span><span class="sxs-lookup"><span data-stu-id="7d013-195">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_StorageExtent**.**Name**", "**CIM\_StorageExtent**.**NameNamespace**", "**CIM\_StorageExtent**.**OtherNameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="7d013-196">O formato de nomenclatura para a propriedade **Name** .</span><span class="sxs-lookup"><span data-stu-id="7d013-196">The naming format for the **Name** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7d013-197">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="7d013-197">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7d013-198">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="7d013-198">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83NAA6"></span><span id="vpd83naa6"></span>

<span data-ttu-id="7d013-199">**VPD83NAA6** (2)</span><span class="sxs-lookup"><span data-stu-id="7d013-199">**VPD83NAA6** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83NAA5"></span><span id="vpd83naa5"></span>

<span data-ttu-id="7d013-200">**VPD83NAA5** (3)</span><span class="sxs-lookup"><span data-stu-id="7d013-200">**VPD83NAA5** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>

<span data-ttu-id="7d013-201">**VPD83Type2** (4)</span><span class="sxs-lookup"><span data-stu-id="7d013-201">**VPD83Type2** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>

<span data-ttu-id="7d013-202">**VPD83Type1** (5)</span><span class="sxs-lookup"><span data-stu-id="7d013-202">**VPD83Type1** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type0"></span><span id="vpd83type0"></span><span id="VPD83TYPE0"></span>

<span data-ttu-id="7d013-203">**VPD83Type0** (6)</span><span class="sxs-lookup"><span data-stu-id="7d013-203">**VPD83Type0** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

<span data-ttu-id="7d013-204">**SNVM** (7)</span><span class="sxs-lookup"><span data-stu-id="7d013-204">**SNVM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>

<span data-ttu-id="7d013-205">**NodeWWN** (8)</span><span class="sxs-lookup"><span data-stu-id="7d013-205">**NodeWWN** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="NAA"></span><span id="naa"></span>

<span data-ttu-id="7d013-206">**Naa** (9)</span><span class="sxs-lookup"><span data-stu-id="7d013-206">**NAA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EUI64"></span><span id="eui64"></span>

<span data-ttu-id="7d013-207">**EUI64** (10)</span><span class="sxs-lookup"><span data-stu-id="7d013-207">**EUI64** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="T10VID"></span><span id="t10vid"></span>

<span data-ttu-id="7d013-208">**T10VID** (11)</span><span class="sxs-lookup"><span data-stu-id="7d013-208">**T10VID** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

<span data-ttu-id="7d013-209">**Nome do dispositivo do so** (12)</span><span class="sxs-lookup"><span data-stu-id="7d013-209">**OS Device Name** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7d013-210">**NameNamespace**</span><span class="sxs-lookup"><span data-stu-id="7d013-210">**NameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d013-211">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7d013-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7d013-212">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7d013-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d013-213">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SPC. INCITS-T10 \| VPD 83, \| identificador de associação 0 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ StorageExtent**.**Name**","**CIM \_ StorageExtent**.**OtherNameNamespace**","**CIM \_ StorageExtent**.**NameFormat**")</span><span class="sxs-lookup"><span data-stu-id="7d013-213">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SPC.INCITS-T10\| VPD 83, Association 0 \| Identifier"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_StorageExtent**.**Name**", "**CIM\_StorageExtent**.**OtherNameNamespace**", "**CIM\_StorageExtent**.**NameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="7d013-214">O namespace da propriedade Name.</span><span class="sxs-lookup"><span data-stu-id="7d013-214">The namespace of the name property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7d013-215">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="7d013-215">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7d013-216">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="7d013-216">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>

<span data-ttu-id="7d013-217">**VPD83Type3** (2)</span><span class="sxs-lookup"><span data-stu-id="7d013-217">**VPD83Type3** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>

<span data-ttu-id="7d013-218">**VPD83Type2** (3)</span><span class="sxs-lookup"><span data-stu-id="7d013-218">**VPD83Type2** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>

<span data-ttu-id="7d013-219">**VPD83Type1** (4)</span><span class="sxs-lookup"><span data-stu-id="7d013-219">**VPD83Type1** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD80"></span><span id="vpd80"></span>

<span data-ttu-id="7d013-220">**VPD80** (5)</span><span class="sxs-lookup"><span data-stu-id="7d013-220">**VPD80** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>

<span data-ttu-id="7d013-221">**NodeWWN** (6)</span><span class="sxs-lookup"><span data-stu-id="7d013-221">**NodeWWN** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

<span data-ttu-id="7d013-222">**SNVM** (7)</span><span class="sxs-lookup"><span data-stu-id="7d013-222">**SNVM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>

<span data-ttu-id="7d013-223">**Namespace de dispositivo do so** (8)</span><span class="sxs-lookup"><span data-stu-id="7d013-223">**OS Device Namespace** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7d013-224">**NoSinglePointOfFailure**</span><span class="sxs-lookup"><span data-stu-id="7d013-224">**NoSinglePointOfFailure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d013-225">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="7d013-225">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7d013-226">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7d013-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d013-227">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**NoSinglePointOfFailure**")</span><span class="sxs-lookup"><span data-stu-id="7d013-227">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**NoSinglePointOfFailure**")</span></span>
</dt> </dl>

<span data-ttu-id="7d013-228">**true** se não houver nenhum ponto único de falha; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="7d013-228">**true** if there are not any single points of failure; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="7d013-229">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="7d013-229">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d013-230">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7d013-230">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7d013-231">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7d013-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d013-232">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Armazenamento de host DMTF \| 1,5 "," MIB. IETF \| host-REsources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="7d013-232">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Host Storage\|001.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="7d013-233">O número total de blocos logicamente contíguos que formam a extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7d013-233">The total number of logically contiguous blocks that form the storage extent.</span></span> <span data-ttu-id="7d013-234">O tamanho total da extensão de armazenamento é calculado multiplicando **BlockSize** por **NumberOfBlocks**.</span><span class="sxs-lookup"><span data-stu-id="7d013-234">The total size of the storage extent is calculated by multiplying **BlockSize** by **NumberOfBlocks**.</span></span> <span data-ttu-id="7d013-235">Se o **BlockSize** for "1", essa propriedade será o tamanho total da extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7d013-235">If the **BlockSize** is "1", this property is the total size of the storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="7d013-236">**OtherNameFormat**</span><span class="sxs-lookup"><span data-stu-id="7d013-236">**OtherNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d013-237">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7d013-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d013-238">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7d013-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d013-239">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ StorageExtent**.**NameFormat**")</span><span class="sxs-lookup"><span data-stu-id="7d013-239">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_StorageExtent**.**NameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="7d013-240">O formato da propriedade **Name** quando a propriedade **NameFormat** é definida como "1" (Other).</span><span class="sxs-lookup"><span data-stu-id="7d013-240">The format of the **Name** property when the **NameFormat** property is set to "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="7d013-241">**OtherNameNamespace**</span><span class="sxs-lookup"><span data-stu-id="7d013-241">**OtherNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d013-242">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7d013-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d013-243">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7d013-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d013-244">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ StorageExtent**.**NameNamespace**")</span><span class="sxs-lookup"><span data-stu-id="7d013-244">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_StorageExtent**.**NameNamespace**")</span></span>
</dt> </dl>

<span data-ttu-id="7d013-245">Uma descrição do namespace da propriedade **Name** quando a propriedade **NameNamespace** é definida como "1" (Other).</span><span class="sxs-lookup"><span data-stu-id="7d013-245">A description of the namespace of the **Name** property when the **NameNamespace** property is set to "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="7d013-246">**PackageRedundancy**</span><span class="sxs-lookup"><span data-stu-id="7d013-246">**PackageRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d013-247">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7d013-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7d013-248">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7d013-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d013-249">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**PackageRedundancyGoal**","**CIM \_ StorageSetting**.**PackageRedundancyMax**","**CIM \_ StorageSetting**.**PackageRedundancyMin**")</span><span class="sxs-lookup"><span data-stu-id="7d013-249">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**PackageRedundancyGoal**", "**CIM\_StorageSetting**.**PackageRedundancyMax**", "**CIM\_StorageSetting**.**PackageRedundancyMin**")</span></span>
</dt> </dl>

<span data-ttu-id="7d013-250">O número atual de pacotes físicos que podem falhar sem perda de dados.</span><span class="sxs-lookup"><span data-stu-id="7d013-250">The current number of physical packages that can fail without data loss.</span></span> <span data-ttu-id="7d013-251">Por exemplo, em um domínio de armazenamento, esse pode ser o número de eixos de disco.</span><span class="sxs-lookup"><span data-stu-id="7d013-251">For example, in a storage domain, this might be the number of disk spindles.</span></span>

</dd> <dt>

<span data-ttu-id="7d013-252">**Primordial**</span><span class="sxs-lookup"><span data-stu-id="7d013-252">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d013-253">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="7d013-253">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7d013-254">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7d013-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d013-255">**true** se a extensão de armazenamento for primordial; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="7d013-255">**true** if the storage extent is primordial; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="7d013-256">**Finalidade**</span><span class="sxs-lookup"><span data-stu-id="7d013-256">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d013-257">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7d013-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d013-258">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7d013-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d013-259">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageDescr ")</span><span class="sxs-lookup"><span data-stu-id="7d013-259">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageDescr")</span></span>
</dt> </dl>

<span data-ttu-id="7d013-260">Uma descrição do uso de mídia.</span><span class="sxs-lookup"><span data-stu-id="7d013-260">A description of the media usage.</span></span>

</dd> <dt>

<span data-ttu-id="7d013-261">**Tenha**</span><span class="sxs-lookup"><span data-stu-id="7d013-261">**SequentialAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d013-262">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="7d013-262">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7d013-263">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7d013-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d013-264">**true** se o armazenamento for acessado sequencialmente por um objeto [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md) ; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="7d013-264">**true** if storage is sequentially accessed by a [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md) object; otherwise, **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7d013-265">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d013-265">Requirements</span></span>



| <span data-ttu-id="7d013-266">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d013-266">Requirement</span></span> | <span data-ttu-id="7d013-267">Valor</span><span class="sxs-lookup"><span data-stu-id="7d013-267">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d013-268">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d013-268">Minimum supported client</span></span><br/> | <span data-ttu-id="7d013-269">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7d013-269">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="7d013-270">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d013-270">Minimum supported server</span></span><br/> | <span data-ttu-id="7d013-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7d013-271">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="7d013-272">Namespace</span><span class="sxs-lookup"><span data-stu-id="7d013-272">Namespace</span></span><br/>                | <span data-ttu-id="7d013-273">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="7d013-273">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7d013-274">MOF</span><span class="sxs-lookup"><span data-stu-id="7d013-274">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d013-275"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7d013-275"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7d013-276">DLL</span><span class="sxs-lookup"><span data-stu-id="7d013-276">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d013-277"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7d013-277"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7d013-278">Confira também</span><span class="sxs-lookup"><span data-stu-id="7d013-278">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d013-279">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="7d013-279">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 


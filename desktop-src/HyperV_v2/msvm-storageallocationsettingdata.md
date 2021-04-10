---
description: Representa as configurações especificamente relacionadas à alocação do armazenamento virtual.
ms.assetid: de6787c0-9998-4f1d-9715-f0dfa0ff70c6
title: Classe Msvm_StorageAllocationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageAllocationSettingData
- Msvm_StorageAllocationSettingData.InstanceID
- Msvm_StorageAllocationSettingData.Caption
- Msvm_StorageAllocationSettingData.Description
- Msvm_StorageAllocationSettingData.ElementName
- Msvm_StorageAllocationSettingData.ResourceType
- Msvm_StorageAllocationSettingData.OtherResourceType
- Msvm_StorageAllocationSettingData.ResourceSubType
- Msvm_StorageAllocationSettingData.PoolID
- Msvm_StorageAllocationSettingData.ConsumerVisibility
- Msvm_StorageAllocationSettingData.HostResource
- Msvm_StorageAllocationSettingData.AllocationUnits
- Msvm_StorageAllocationSettingData.VirtualQuantity
- Msvm_StorageAllocationSettingData.Limit
- Msvm_StorageAllocationSettingData.Weight
- Msvm_StorageAllocationSettingData.StorageQoSPolicyID
- Msvm_StorageAllocationSettingData.AutomaticAllocation
- Msvm_StorageAllocationSettingData.AutomaticDeallocation
- Msvm_StorageAllocationSettingData.Parent
- Msvm_StorageAllocationSettingData.Connection
- Msvm_StorageAllocationSettingData.Address
- Msvm_StorageAllocationSettingData.MappingBehavior
- Msvm_StorageAllocationSettingData.AddressOnParent
- Msvm_StorageAllocationSettingData.VirtualResourceBlockSize
- Msvm_StorageAllocationSettingData.VirtualQuantityUnits
- Msvm_StorageAllocationSettingData.Access
- Msvm_StorageAllocationSettingData.HostResourceBlockSize
- Msvm_StorageAllocationSettingData.Reservation
- Msvm_StorageAllocationSettingData.HostExtentStartingAddress
- Msvm_StorageAllocationSettingData.HostExtentName
- Msvm_StorageAllocationSettingData.HostExtentNameFormat
- Msvm_StorageAllocationSettingData.OtherHostExtentNameFormat
- Msvm_StorageAllocationSettingData.HostExtentNameNamespace
- Msvm_StorageAllocationSettingData.OtherHostExtentNameNamespace
- Msvm_StorageAllocationSettingData.IOPSLimit
- Msvm_StorageAllocationSettingData.IOPSReservation
- Msvm_StorageAllocationSettingData.IOPSAllocationUnits
- Msvm_StorageAllocationSettingData.PersistentReservationsSupported
- Msvm_StorageAllocationSettingData.CachingMode
- Msvm_StorageAllocationSettingData.SnapshotId
- Msvm_StorageAllocationSettingData.IgnoreFlushes
- Msvm_StorageAllocationSettingData.WriteHardeningMethod
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d889c262eee9d827a02547ddbfdff2cb121cb337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170249"
---
# <a name="msvm_storageallocationsettingdata-class"></a><span data-ttu-id="233d6-103">\_Classe Msvm StorageAllocationSettingData</span><span class="sxs-lookup"><span data-stu-id="233d6-103">Msvm\_StorageAllocationSettingData class</span></span>

<span data-ttu-id="233d6-104">Representa as configurações especificamente relacionadas à alocação do armazenamento virtual.</span><span class="sxs-lookup"><span data-stu-id="233d6-104">Represents settings specifically related to the allocation of virtual storage.</span></span>

<span data-ttu-id="233d6-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="233d6-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="233d6-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="233d6-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageAllocationSettingData : CIM_StorageAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Hard Disk Image Default Settings";
  string  Description = "Describes the default settings for the hard disk image resources";
  string  ElementName;
  uint16  ResourceType;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  string  AllocationUnits;
  uint64  VirtualQuantity;
  uint64  Limit = 1;
  uint32  Weight;
  string  StorageQoSPolicyID;
  boolean AutomaticAllocation;
  boolean AutomaticDeallocation;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  uint64  VirtualResourceBlockSize;
  string  VirtualQuantityUnits = "count(fixed size block)";
  uint16  Access;
  uint64  HostResourceBlockSize;
  uint64  Reservation;
  uint64  HostExtentStartingAddress;
  string  HostExtentName;
  uint16  HostExtentNameFormat;
  string  OtherHostExtentNameFormat;
  uint16  HostExtentNameNamespace;
  string  OtherHostExtentNameNamespace;
  uint64  IOPSLimit;
  uint64  IOPSReservation;
  string  IOPSAllocationUnits;
  boolean PersistentReservationsSupported;
  uint16  CachingMode;
  string  SnapshotId = "";
  boolean IgnoreFlushes;
  uint16  WriteHardeningMethod;
};
```

## <a name="members"></a><span data-ttu-id="233d6-107">Membros</span><span class="sxs-lookup"><span data-stu-id="233d6-107">Members</span></span>

<span data-ttu-id="233d6-108">A classe **Msvm \_ StorageAllocationSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="233d6-108">The **Msvm\_StorageAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="233d6-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="233d6-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="233d6-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="233d6-110">Properties</span></span>

<span data-ttu-id="233d6-111">A classe **Msvm \_ StorageAllocationSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="233d6-111">The **Msvm\_StorageAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="233d6-112">**Acesso**</span><span class="sxs-lookup"><span data-stu-id="233d6-112">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-113">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="233d6-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="233d6-115">Especifica o acesso de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="233d6-115">Specifies the storage access.</span></span> <span data-ttu-id="233d6-116">Essa propriedade é herdada do **CIM \_ StorageAllocationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="233d6-116">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

<dl> <dt>

<span data-ttu-id="233d6-117"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="233d6-117"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-118"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Legível** (1)</span><span class="sxs-lookup"><span data-stu-id="233d6-118"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-119"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Gravável** (2)</span><span class="sxs-lookup"><span data-stu-id="233d6-119"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-120"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Suporte de leitura/gravação** (3)</span><span class="sxs-lookup"><span data-stu-id="233d6-120"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="233d6-121">**Endereço**</span><span class="sxs-lookup"><span data-stu-id="233d6-121">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="233d6-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="233d6-124">O endereço do recurso.</span><span class="sxs-lookup"><span data-stu-id="233d6-124">The address of the resource.</span></span> <span data-ttu-id="233d6-125">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="233d6-125">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="233d6-126">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="233d6-126">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="233d6-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="233d6-129">Descreve o endereço deste recurso no contexto do pai.</span><span class="sxs-lookup"><span data-stu-id="233d6-129">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="233d6-130">As propriedades **pai** e **AddressOnParent** são usadas para descrever a relação do controlador, bem como a ordem dos dispositivos em um controlador.</span><span class="sxs-lookup"><span data-stu-id="233d6-130">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="233d6-131">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="233d6-131">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="233d6-132">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="233d6-132">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="233d6-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="233d6-135">As unidades de alocação usadas pelas propriedades **Reservation** e **Limit** .</span><span class="sxs-lookup"><span data-stu-id="233d6-135">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="233d6-136">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="233d6-136">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="233d6-137">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="233d6-137">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-138">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="233d6-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="233d6-140">Indica se o recurso será alocado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="233d6-140">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="233d6-141">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="233d6-141">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="233d6-142">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="233d6-142">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-143">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="233d6-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="233d6-145">Indica se o recurso será desalocado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="233d6-145">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="233d6-146">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="233d6-146">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="233d6-147">**Cachingmode**</span><span class="sxs-lookup"><span data-stu-id="233d6-147">**CachingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-148">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="233d6-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="233d6-150">Indica se e como o cache de arquivo na memória deve ser usado para este VHD.</span><span class="sxs-lookup"><span data-stu-id="233d6-150">Indicates whether and how in-memory file caching should be used for this VHD.</span></span> <span data-ttu-id="233d6-151">A política padrão é definida no campo **DefaultVirtualHardDiskCachingMode** da classe [**Msvm \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="233d6-151">The default policy is set in the **DefaultVirtualHardDiskCachingMode** field of the [**Msvm\_VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="233d6-152">Adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="233d6-152">Added in Windows 10.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="233d6-153">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="233d6-153">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="233d6-154">**Padrão** (2)</span><span class="sxs-lookup"><span data-stu-id="233d6-154">**Default** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Caching"></span><span id="no_caching"></span><span id="NO_CACHING"></span>

<span data-ttu-id="233d6-155">**Sem cache** (3)</span><span class="sxs-lookup"><span data-stu-id="233d6-155">**No Caching** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_Sharable_Parents"></span><span id="cache_sharable_parents"></span><span id="CACHE_SHARABLE_PARENTS"></span>

<span data-ttu-id="233d6-156">**Pais compartilháveis do cache** (4)</span><span class="sxs-lookup"><span data-stu-id="233d6-156">**Cache Sharable Parents** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="233d6-157">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="233d6-157">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-158">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="233d6-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="233d6-160">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="233d6-160">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="233d6-161">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="233d6-161">A short description of the object.</span></span> <span data-ttu-id="233d6-162">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "configurações padrão de imagem de disco rígido".</span><span class="sxs-lookup"><span data-stu-id="233d6-162">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hard Disk Image Default Settings".</span></span>

</dd> <dt>

<span data-ttu-id="233d6-163">**Conexão**</span><span class="sxs-lookup"><span data-stu-id="233d6-163">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-164">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="233d6-164">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="233d6-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="233d6-166">O dispositivo ao qual esse recurso está conectado.</span><span class="sxs-lookup"><span data-stu-id="233d6-166">The device to which this resource is connected.</span></span> <span data-ttu-id="233d6-167">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="233d6-167">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="233d6-168">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="233d6-168">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-169">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="233d6-169">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="233d6-171">A visibilidade do consumidor para o recurso alocado.</span><span class="sxs-lookup"><span data-stu-id="233d6-171">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="233d6-172">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="233d6-172">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<dl> <dt>

<span data-ttu-id="233d6-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="233d6-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-174"><span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span>**Aprovado** (2)</span><span class="sxs-lookup"><span data-stu-id="233d6-174"><span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span>**Passed-Through** (2)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-175"><span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span>**Virtualizado** (3)</span><span class="sxs-lookup"><span data-stu-id="233d6-175"><span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span>**Virtualized** (3)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-176"><span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span>**Não representado** (4)</span><span class="sxs-lookup"><span data-stu-id="233d6-176"><span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span>**Not represented** (4)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="233d6-177">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="233d6-177">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-178">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="233d6-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="233d6-180">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="233d6-180">A description of the object.</span></span> <span data-ttu-id="233d6-181">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "descreve as configurações padrão para os recursos de imagem de disco rígido".</span><span class="sxs-lookup"><span data-stu-id="233d6-181">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Describes the default settings for the hard disk image resources".</span></span>

</dd> <dt>

<span data-ttu-id="233d6-182">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="233d6-182">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-183">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="233d6-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="233d6-185">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="233d6-185">A display name for the object.</span></span> <span data-ttu-id="233d6-186">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="233d6-186">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="233d6-187">**HostExtentName**</span><span class="sxs-lookup"><span data-stu-id="233d6-187">**HostExtentName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-188">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="233d6-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-189">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="233d6-190">Um identificador exclusivo para a extensão do host.</span><span class="sxs-lookup"><span data-stu-id="233d6-190">A unique identifier for the host extent.</span></span> <span data-ttu-id="233d6-191">A extensão de host identificada é usada para a alocação de recursos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="233d6-191">The identified host extent is used for the storage resource allocation.</span></span> <span data-ttu-id="233d6-192">Essa propriedade é herdada do **CIM \_ StorageAllocationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="233d6-192">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="233d6-193">**HostExtentNameFormat**</span><span class="sxs-lookup"><span data-stu-id="233d6-193">**HostExtentNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-194">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="233d6-194">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-195">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="233d6-196">Identifica o formato usado para a propriedade **HostExtentName** .</span><span class="sxs-lookup"><span data-stu-id="233d6-196">Identifies the format that is used for the **HostExtentName** property.</span></span> <span data-ttu-id="233d6-197">Essa propriedade é herdada do **CIM \_ StorageAllocationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="233d6-197">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

<dl> <dt>

<span data-ttu-id="233d6-198"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="233d6-198"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="233d6-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-200"><span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)</span><span class="sxs-lookup"><span data-stu-id="233d6-200"><span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-201"><span id="NAA"></span><span id="naa"></span>**Naa** (9)</span><span class="sxs-lookup"><span data-stu-id="233d6-201"><span id="NAA"></span><span id="naa"></span>**NAA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-202"><span id="EUI64"></span><span id="eui64"></span>**EUI64** (10)</span><span class="sxs-lookup"><span data-stu-id="233d6-202"><span id="EUI64"></span><span id="eui64"></span>**EUI64** (10)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-203"><span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11)</span><span class="sxs-lookup"><span data-stu-id="233d6-203"><span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-204"><span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**Nome do dispositivo do so** (12)</span><span class="sxs-lookup"><span data-stu-id="233d6-204"><span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**OS Device Name** (12)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-205"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="233d6-205"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="233d6-206">)</span><span class="sxs-lookup"><span data-stu-id="233d6-206">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="233d6-207">**HostExtentNameNamespace**</span><span class="sxs-lookup"><span data-stu-id="233d6-207">**HostExtentNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-208">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="233d6-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="233d6-210">Se a extensão do host for um volume SCSI, a origem preferida para nomes de volume SCSI será respostas da página SCSI VPD 83.</span><span class="sxs-lookup"><span data-stu-id="233d6-210">If the host extent is a SCSI volume, then the preferred source for SCSI volume names is SCSI VPD Page 83 responses.</span></span> <span data-ttu-id="233d6-211">Essa propriedade é herdada do **CIM \_ StorageAllocationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="233d6-211">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

<dl> <dt>

<span data-ttu-id="233d6-212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="233d6-212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-213"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="233d6-213"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-214"><span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>**VPD83Type3** (2)</span><span class="sxs-lookup"><span data-stu-id="233d6-214"><span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>**VPD83Type3** (2)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-215"><span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>**VPD83Type2** (3)</span><span class="sxs-lookup"><span data-stu-id="233d6-215"><span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>**VPD83Type2** (3)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-216"><span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>**VPD83Type1** (4)</span><span class="sxs-lookup"><span data-stu-id="233d6-216"><span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>**VPD83Type1** (4)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-217"><span id="VPD80"></span><span id="vpd80"></span>**VPD80** (5)</span><span class="sxs-lookup"><span data-stu-id="233d6-217"><span id="VPD80"></span><span id="vpd80"></span>**VPD80** (5)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-218"><span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>**NodeWWN** (6)</span><span class="sxs-lookup"><span data-stu-id="233d6-218"><span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>**NodeWWN** (6)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-219"><span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)</span><span class="sxs-lookup"><span data-stu-id="233d6-219"><span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-220"><span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>**Namespace de dispositivo do so** (8)</span><span class="sxs-lookup"><span data-stu-id="233d6-220"><span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>**OS Device Namespace** (8)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-221"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="233d6-221"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="233d6-222">)</span><span class="sxs-lookup"><span data-stu-id="233d6-222">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="233d6-223">**HostExtentStartingAddress**</span><span class="sxs-lookup"><span data-stu-id="233d6-223">**HostExtentStartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-224">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="233d6-224">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-225">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="233d6-226">Identifica o endereço inicial na extensão de armazenamento do host, identificado pela propriedade **HostExtentName** , que é usada para a alocação da extensão de armazenamento virtual.</span><span class="sxs-lookup"><span data-stu-id="233d6-226">Identifies the starting address on the host storage extent, identified by the **HostExtentName** property, that is used for the allocation of the virtual storage extent.</span></span> <span data-ttu-id="233d6-227">Um valor **nulo** indica que não há mapeamento direto da extensão de armazenamento virtual para a extensão de armazenamento de host referenciada.</span><span class="sxs-lookup"><span data-stu-id="233d6-227">A **Null** value indicates that there is no direct mapping of the virtual storage extent to the referenced host storage extent.</span></span> <span data-ttu-id="233d6-228">Essa propriedade é herdada do **CIM \_ StorageAllocationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="233d6-228">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="233d6-229">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="233d6-229">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-230">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="233d6-230">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="233d6-231">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="233d6-232">Somente um recurso de host pode ser atribuído a cada dispositivo na máquina virtual, de modo que somente o primeiro elemento dessa matriz pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="233d6-232">Only one host resource can be assigned to each device in the virtual machine, so only the first element of this array can be set.</span></span> <span data-ttu-id="233d6-233">Para dispositivos que dão suporte a esse recurso, defina o primeiro elemento da matriz **HostResource** para conter uma referência ao recurso de host subjacente a ser atribuído.</span><span class="sxs-lookup"><span data-stu-id="233d6-233">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="233d6-234">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="233d6-234">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="233d6-235">Trata-se de uma propriedade somente leitura.</span><span class="sxs-lookup"><span data-stu-id="233d6-235">This is a read-only property.</span></span> <span data-ttu-id="233d6-236">Mas se a propriedade **ResourceType** for 31 (disco lógico) e a propriedade **ResourceSubType** for "Microsoft: Hyper-v: disco rígido virtual", "Microsoft: Hyper-v: disco virtual de CD/DVD" ou "Microsoft: Hyper-v: disquete virtual", a propriedade **HostResource** poderá ser alterada usando o método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="233d6-236">But if the **ResourceType** property is 31 (Logical Disk) and the **ResourceSubType** property is "Microsoft:Hyper-V:Virtual Hard Disk", "Microsoft:Hyper-V:Virtual CD/DVD Disk", or "Microsoft:Hyper-V:Virtual Floppy Disk", the **HostResource** property can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="233d6-237">**HostResourceBlockSize**</span><span class="sxs-lookup"><span data-stu-id="233d6-237">**HostResourceBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-238">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="233d6-238">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-239">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="233d6-240">O tamanho, em bytes, dos blocos que são alocados no host como resultado dessa solicitação de alocação de recursos de armazenamento ou alocação de recursos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="233d6-240">The size, in bytes, of the blocks that are allocated at the host as the result of this storage resource allocation or storage resource allocation request.</span></span> <span data-ttu-id="233d6-241">Se o tamanho do bloco for variável, o tamanho máximo do bloco, em bytes, será especificado.</span><span class="sxs-lookup"><span data-stu-id="233d6-241">If the block size is variable, then the maximum block size, in bytes, will be specified.</span></span> <span data-ttu-id="233d6-242">Se o tamanho do bloco for desconhecido ou se um conceito de bloco não se aplicar, o valor 1 será usado.</span><span class="sxs-lookup"><span data-stu-id="233d6-242">If the block size is unknown or if a block concept does not apply, then the value 1 will be used.</span></span> <span data-ttu-id="233d6-243">Essa propriedade é herdada do **CIM \_ StorageAllocationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="233d6-243">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="233d6-244">**IgnoreFlushes**</span><span class="sxs-lookup"><span data-stu-id="233d6-244">**IgnoreFlushes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-245">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="233d6-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-246">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="233d6-247">Se definido como true, o Hyper-V ignorará a liberação de write-back para essa máquina virtual específica.</span><span class="sxs-lookup"><span data-stu-id="233d6-247">If set to true, Hyper-V will ignore write back flushing for that particular virtual machine.</span></span> <span data-ttu-id="233d6-248">Se definido como false, o Hyper-V continuará a fazer write-back no disco em cada liberação.</span><span class="sxs-lookup"><span data-stu-id="233d6-248">If set to false, Hyper-V will continue to write back to the disk on every flush.</span></span> <span data-ttu-id="233d6-249">A configuração padrão é false.</span><span class="sxs-lookup"><span data-stu-id="233d6-249">The default setting is false.</span></span>

<span data-ttu-id="233d6-250">**Windows 10:** Não há suporte para esse valor até o Windows 10.</span><span class="sxs-lookup"><span data-stu-id="233d6-250">**Windows 10:** This value is not supported until Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="233d6-251">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="233d6-251">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-252">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="233d6-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-253">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-253">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="233d6-254">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="233d6-254">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="233d6-255">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="233d6-255">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="233d6-256">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="233d6-256">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="233d6-257">**IOPSAllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="233d6-257">**IOPSAllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-258">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="233d6-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-259">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="233d6-260">Especifica as unidades de alocação usadas pelas propriedades **IOPSLimit** e **IOPSReservation** .</span><span class="sxs-lookup"><span data-stu-id="233d6-260">Specifies the allocation units used by the **IOPSLimit** and **IOPSReservation** properties.</span></span> <span data-ttu-id="233d6-261">Essa propriedade sempre tem o valor:</span><span class="sxs-lookup"><span data-stu-id="233d6-261">This property always has the value:</span></span>

<span data-ttu-id="233d6-262">"contagem (e/s normalizada)/segundo"</span><span class="sxs-lookup"><span data-stu-id="233d6-262">"count(normalized I/O) / second"</span></span>

<span data-ttu-id="233d6-263">A taxa de transferência é medida em IOPS (operações de e/s normalizadas por segundo) em vez de IOPS brutos.</span><span class="sxs-lookup"><span data-stu-id="233d6-263">Throughput is measured in normalized I/O operations per second (IOPS) instead of raw IOPS.</span></span> <span data-ttu-id="233d6-264">Ao usar IOPS normalizado, cada solicitação de e/s será contabilizada como 1 e/s normalizada se o tamanho da solicitação for menor ou igual a um tamanho de base predefinido (8 KB).</span><span class="sxs-lookup"><span data-stu-id="233d6-264">When using normalized IOPS, each I/O request is accounted for as 1 normalized I/O if the size of the request is less than or equal to a predefined base size (8 KB).</span></span> <span data-ttu-id="233d6-265">As solicitações que são maiores que o tamanho base são contabilizadas como N operações de e/s, em que N é o valor arredondado do tamanho da solicitação dividido pelo tamanho base.</span><span class="sxs-lookup"><span data-stu-id="233d6-265">Requests that are larger than the base size are accounted for as N I/O operations, where N is the rounded-up value of the request size divided by the base size.</span></span> <span data-ttu-id="233d6-266">Por exemplo, se o tamanho base for de 8 KB, uma solicitação de 16 KB será contada como duas operações de e/s normalizadas, uma solicitação de 32 KB como 4 operações de e/s normalizadas e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="233d6-266">For example, if the base size is 8 KB, a 16-KB request is counted as 2 normalized I/O operations, a 32-KB request as 4 normalized I/O operations, and so on.</span></span>

<span data-ttu-id="233d6-267">**Windows 8.1:** Não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="233d6-267">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="233d6-268">**IOPSLimit**</span><span class="sxs-lookup"><span data-stu-id="233d6-268">**IOPSLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-269">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="233d6-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-270">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="233d6-271">Qualificadores: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1000000000)</span><span class="sxs-lookup"><span data-stu-id="233d6-271">Qualifiers: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1000000000)</span></span>
</dt> </dl>

<span data-ttu-id="233d6-272">O número máximo de operações de e/s por segundo (IOPS) que serão atendidas para essa extensão de armazenamento virtual.</span><span class="sxs-lookup"><span data-stu-id="233d6-272">The maximum number of I/O operations per second (IOPS) that will be serviced for this virtual storage extent.</span></span> <span data-ttu-id="233d6-273">Se o valor não for definido ou for zero, não haverá nenhum limite para o número de IOPS que o dispositivo pode emitir.</span><span class="sxs-lookup"><span data-stu-id="233d6-273">If the value isn't defined or is zero, there is no limit to the number of IOPS that the device can issue.</span></span>

> [!Note]  
> <span data-ttu-id="233d6-274">Você pode usar o método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) para modificar o valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="233d6-274">You can use the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class to modify the value of this property.</span></span> <span data-ttu-id="233d6-275">Essa propriedade só é significativa para instâncias **Msvm \_ StorageAllocationSettingData** que solicitam alocações de recursos para máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="233d6-275">This property is meaningful only for **Msvm\_StorageAllocationSettingData** instances that request resource allocations for virtual machines.</span></span> <span data-ttu-id="233d6-276">Ela é ignorada ao alocar recursos a um pool filho.</span><span class="sxs-lookup"><span data-stu-id="233d6-276">It's ignored when allocating resources to a child pool.</span></span>

 

<span data-ttu-id="233d6-277">**Windows 8.1:** Não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="233d6-277">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="233d6-278">**IOPSReservation**</span><span class="sxs-lookup"><span data-stu-id="233d6-278">**IOPSReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-279">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="233d6-279">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-280">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="233d6-281">Qualificadores: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1000000000)</span><span class="sxs-lookup"><span data-stu-id="233d6-281">Qualifiers: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1000000000)</span></span>
</dt> </dl>

<span data-ttu-id="233d6-282">O número mínimo de operações de e/s por segundo (IOPS) que serão atendidas para essa extensão de armazenamento virtual.</span><span class="sxs-lookup"><span data-stu-id="233d6-282">The minimum number of I/O operations per second (IOPS) that will be serviced for this virtual storage extent.</span></span>

<span data-ttu-id="233d6-283">Se **IOPSLimit** e **IOPSReservation** forem definidos, o valor de **IOPSLimit** deverá ser maior ou igual ao valor de **IOPSReservation**.</span><span class="sxs-lookup"><span data-stu-id="233d6-283">If both **IOPSLimit** and **IOPSReservation** are defined, the value of **IOPSLimit** must be greater than or equal to the value of **IOPSReservation**.</span></span>

> [!Note]  
> <span data-ttu-id="233d6-284">Você pode usar o método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) para modificar o valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="233d6-284">You can use the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class to modify the value of this property.</span></span> <span data-ttu-id="233d6-285">Essa propriedade só é significativa para instâncias **Msvm \_ StorageAllocationSettingData** que solicitam alocações de recursos para máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="233d6-285">This property is meaningful only for **Msvm\_StorageAllocationSettingData** instances that request resource allocations for virtual machines.</span></span> <span data-ttu-id="233d6-286">Ela é ignorada ao alocar recursos a um pool filho.</span><span class="sxs-lookup"><span data-stu-id="233d6-286">It's ignored when allocating resources to a child pool.</span></span>

 

<span data-ttu-id="233d6-287">**Windows 8.1:** Não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="233d6-287">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="233d6-288">**Limite**</span><span class="sxs-lookup"><span data-stu-id="233d6-288">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-289">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="233d6-289">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-290">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="233d6-291">O número máximo de blocos que serão concedidos para essa alocação de recurso de armazenamento no host.</span><span class="sxs-lookup"><span data-stu-id="233d6-291">The maximum number of blocks that will be granted for this storage resource allocation at the host.</span></span> <span data-ttu-id="233d6-292">O tamanho do bloco é especificado pela propriedade **HostResourceBlockSize** .</span><span class="sxs-lookup"><span data-stu-id="233d6-292">The block size is specified by the **HostResourceBlockSize** property.</span></span> <span data-ttu-id="233d6-293">Normalmente, o valor dessa propriedade refletiria um tamanho máximo para a extensão de host alocada que corresponde ao tamanho da extensão de armazenamento virtual apresentada ao consumidor.</span><span class="sxs-lookup"><span data-stu-id="233d6-293">Usually the value of this property would reflect a maximum size for the allocated host extent that matches the size of the virtual storage extent presented to the consumer.</span></span> <span data-ttu-id="233d6-294">Um valor menor que isso indicaria uma situação em que uma extensão de armazenamento virtual preenchida de forma grosseira é esperada, em que a taxa de preenchimento é limitada pelo valor da propriedade Limit.</span><span class="sxs-lookup"><span data-stu-id="233d6-294">A value less than that would indicate a situation where a sparsely populated virtual storage extent is expected, where the fill rate is limited by the value of the Limit property.</span></span> <span data-ttu-id="233d6-295">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="233d6-295">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="233d6-296">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="233d6-296">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-297">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="233d6-297">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-298">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="233d6-299">Especifica como esse recurso é mapeado para recursos subjacentes.</span><span class="sxs-lookup"><span data-stu-id="233d6-299">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="233d6-300">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="233d6-300">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="233d6-301">**OtherHostExtentNameFormat**</span><span class="sxs-lookup"><span data-stu-id="233d6-301">**OtherHostExtentNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-302">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="233d6-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-303">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="233d6-304">Uma cadeia de caracteres que descreve o formato da propriedade **HostExtentName** se a propriedade **HostExtentNameFormat** for 1 (Other).</span><span class="sxs-lookup"><span data-stu-id="233d6-304">A string that describes the format of the **HostExtentName** property if the **HostExtentNameFormat** property is 1 (Other).</span></span> <span data-ttu-id="233d6-305">Essa propriedade é herdada do **CIM \_ StorageAllocationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="233d6-305">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="233d6-306">**OtherHostExtentNameNamespace**</span><span class="sxs-lookup"><span data-stu-id="233d6-306">**OtherHostExtentNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-307">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="233d6-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-308">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="233d6-309">Uma cadeia de caracteres que descreve o namespace da propriedade **HostExtentName** se a propriedade **HostExtentNameNamespace** contiver 1 (Other).</span><span class="sxs-lookup"><span data-stu-id="233d6-309">A string that describes the namespace of the **HostExtentName** property if the **HostExtentNameNamespace** property contains 1 (Other).</span></span> <span data-ttu-id="233d6-310">Essa propriedade é herdada do **CIM \_ StorageAllocationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="233d6-310">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="233d6-311">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="233d6-311">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-312">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="233d6-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-313">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="233d6-314">Uma cadeia de caracteres que descreve o tipo de recurso quando um valor bem definido não está disponível e [**ResourceType**](msvm-processorsettingdata.md) tem o valor 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="233d6-314">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1(Other).</span></span> <span data-ttu-id="233d6-315">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="233d6-315">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="233d6-316">**Pai**</span><span class="sxs-lookup"><span data-stu-id="233d6-316">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-317">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="233d6-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-318">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="233d6-319">O pai do recurso.</span><span class="sxs-lookup"><span data-stu-id="233d6-319">The parent of the resource.</span></span> <span data-ttu-id="233d6-320">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="233d6-320">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="233d6-321">**PersistentReservationsSupported**</span><span class="sxs-lookup"><span data-stu-id="233d6-321">**PersistentReservationsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-322">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="233d6-322">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-323">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="233d6-324">Indica se o disco rígido virtual dá suporte a reservas persistentes SCSI-3.</span><span class="sxs-lookup"><span data-stu-id="233d6-324">Indicates whether the virtual hard disk supports SCSI-3 persistent reservations.</span></span>

<span data-ttu-id="233d6-325">**Windows 8.1:** Não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="233d6-325">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="233d6-326">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="233d6-326">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-327">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="233d6-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-328">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="233d6-329">O identificador do pool de recursos do qual esse recurso foi alocado.</span><span class="sxs-lookup"><span data-stu-id="233d6-329">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="233d6-330">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="233d6-330">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="233d6-331">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="233d6-331">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-332">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="233d6-332">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-333">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="233d6-334">Qualificadores: **override** ("reserva"), **ModelCorrespondence** ("CIM \_ StorageAllocationSettingData. HostResourceBlockSize")</span><span class="sxs-lookup"><span data-stu-id="233d6-334">Qualifiers: **Override** ("Reservation"), **ModelCorrespondence** ("CIM\_StorageAllocationSettingData.HostResourceBlockSize")</span></span>
</dt> </dl>

<span data-ttu-id="233d6-335">O número de blocos que têm garantia de disponibilidade para essa alocação de recursos de armazenamento no host.</span><span class="sxs-lookup"><span data-stu-id="233d6-335">The number of blocks that are guaranteed to be available for this storage resource allocation at the host.</span></span> <span data-ttu-id="233d6-336">O tamanho do bloco é especificado pela propriedade **HostResourceBlockSize** .</span><span class="sxs-lookup"><span data-stu-id="233d6-336">The block size is specified by the **HostResourceBlockSize** property.</span></span> <span data-ttu-id="233d6-337">Essa propriedade é herdada do **CIM \_ StorageAllocationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="233d6-337">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="233d6-338">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="233d6-338">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-339">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="233d6-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-340">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="233d6-341">Uma cadeia de caracteres que descreve um subtipo específico da implementação para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="233d6-341">A string that describes an implementation-specific subtype for this resource.</span></span> <span data-ttu-id="233d6-342">Por exemplo, isso pode ser usado para distinguir modelos diferentes do mesmo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="233d6-342">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="233d6-343">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="233d6-343">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="233d6-344">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="233d6-344">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-345">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="233d6-345">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-346">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="233d6-347">O tipo de recurso que essa configuração de alocação representa.</span><span class="sxs-lookup"><span data-stu-id="233d6-347">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="233d6-348">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="233d6-348">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<dl> <dt>

<span data-ttu-id="233d6-349"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="233d6-349"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-350"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Sistema de computador** (2)</span><span class="sxs-lookup"><span data-stu-id="233d6-350"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-351"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processador** (3)</span><span class="sxs-lookup"><span data-stu-id="233d6-351"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-352"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memória** (4)</span><span class="sxs-lookup"><span data-stu-id="233d6-352"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-353"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**Controlador IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="233d6-353"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-354"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**HBA SCSI paralelo** (6)</span><span class="sxs-lookup"><span data-stu-id="233d6-354"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-355"><span id="FC_HBA"></span><span id="fc_hba"></span>**HBA FC** (7)</span><span class="sxs-lookup"><span data-stu-id="233d6-355"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-356"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="233d6-356"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-357"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="233d6-357"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-358"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Adaptador Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="233d6-358"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-359"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Outro adaptador de rede** (11)</span><span class="sxs-lookup"><span data-stu-id="233d6-359"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-360"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Slot de e/s** (12)</span><span class="sxs-lookup"><span data-stu-id="233d6-360"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-361"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Dispositivo de e/s** (13)</span><span class="sxs-lookup"><span data-stu-id="233d6-361"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-362"><span id="Diskette_Drive"></span><span id="diskette_drive"></span><span id="DISKETTE_DRIVE"></span>**Unidade de disquete** (14)</span><span class="sxs-lookup"><span data-stu-id="233d6-362"><span id="Diskette_Drive"></span><span id="diskette_drive"></span><span id="DISKETTE_DRIVE"></span>**Diskette Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-363"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Unidade de CD** (15)</span><span class="sxs-lookup"><span data-stu-id="233d6-363"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-364"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**Unidade de DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="233d6-364"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-365"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Unidade de disco** (17)</span><span class="sxs-lookup"><span data-stu-id="233d6-365"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Disk Drive** (17)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-366"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Unidade de fita** (18)</span><span class="sxs-lookup"><span data-stu-id="233d6-366"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Tape Drive** (18)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-367"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Extensão de armazenamento** (19)</span><span class="sxs-lookup"><span data-stu-id="233d6-367"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (19)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-368"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Outro dispositivo de armazenamento** (20)</span><span class="sxs-lookup"><span data-stu-id="233d6-368"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other Storage Device** (20)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-369"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Porta serial** (21)</span><span class="sxs-lookup"><span data-stu-id="233d6-369"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (21)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-370"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Porta paralela** (22)</span><span class="sxs-lookup"><span data-stu-id="233d6-370"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (22)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-371"><span id="USB_controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Controlador USB** (23)</span><span class="sxs-lookup"><span data-stu-id="233d6-371"><span id="USB_controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB controller** (23)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-372"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Controlador de gráficos** (24)</span><span class="sxs-lookup"><span data-stu-id="233d6-372"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (24)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-373"><span id="IEEE_1394_controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**Controlador IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="233d6-373"><span id="IEEE_1394_controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-374"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unidade particionável** (26)</span><span class="sxs-lookup"><span data-stu-id="233d6-374"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-375"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unidade particionável de base** (27)</span><span class="sxs-lookup"><span data-stu-id="233d6-375"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-376"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Fonte de energia** (28)</span><span class="sxs-lookup"><span data-stu-id="233d6-376"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Power Supply** (28)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-377"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Dispositivo de resfriamento** (29)</span><span class="sxs-lookup"><span data-stu-id="233d6-377"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Cooling Device** (29)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-378"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Porta do comutador Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="233d6-378"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Ethernet Switch Port** (30)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-379"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Disco lógico** (31)</span><span class="sxs-lookup"><span data-stu-id="233d6-379"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Logical Disk** (31)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-380"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Volume de armazenamento** (32)</span><span class="sxs-lookup"><span data-stu-id="233d6-380"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Storage Volume** (32)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-381"><span id="Ethernet_connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Conexão Ethernet** (33)</span><span class="sxs-lookup"><span data-stu-id="233d6-381"><span id="Ethernet_connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet connection** (33)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-382"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (30 32767)</span><span class="sxs-lookup"><span data-stu-id="233d6-382"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (30 32767)</span></span>
</dt> <dt>

<span data-ttu-id="233d6-383"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="233d6-383"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="233d6-384">**SnapshotId**</span><span class="sxs-lookup"><span data-stu-id="233d6-384">**SnapshotId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-385">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="233d6-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-386">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-386">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="233d6-387">Um GUID que representa qual instantâneo dentro do arquivo de conjunto VHD deve ser anexado.</span><span class="sxs-lookup"><span data-stu-id="233d6-387">A GUID representing which snapshot within the VHD Set file is to be attached.</span></span>

> [!Note]  
> <span data-ttu-id="233d6-388">Adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="233d6-388">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="233d6-389">**StorageQoSPolicyID**</span><span class="sxs-lookup"><span data-stu-id="233d6-389">**StorageQoSPolicyID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-390">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="233d6-390">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-391">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="233d6-392">Especifica o identificador exclusivo da política de QoS de armazenamento a ser aplicada a essa extensão de armazenamento virtual.</span><span class="sxs-lookup"><span data-stu-id="233d6-392">Specifies the unique identifier of the Storage QoS Policy to be applied to this virtual storage extent.</span></span>

> [!Note]  
> <span data-ttu-id="233d6-393">Adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="233d6-393">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="233d6-394">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="233d6-394">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-395">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="233d6-395">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-396">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="233d6-397">O número de blocos que são apresentados ao consumidor.</span><span class="sxs-lookup"><span data-stu-id="233d6-397">The number of blocks that are presented to the consumer.</span></span> <span data-ttu-id="233d6-398">O tamanho do bloco é especificado pela propriedade **VirtualResourceBlockSize** .</span><span class="sxs-lookup"><span data-stu-id="233d6-398">The block size is specified by the **VirtualResourceBlockSize** property.</span></span> <span data-ttu-id="233d6-399">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="233d6-399">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="233d6-400">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="233d6-400">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-401">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="233d6-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-402">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="233d6-403">Especifica as unidades usadas pela propriedade **VirtualQuantity** .</span><span class="sxs-lookup"><span data-stu-id="233d6-403">Specifies the units used by the **VirtualQuantity** property.</span></span> <span data-ttu-id="233d6-404">Essa propriedade é herdada do **CIM \_ StorageAllocationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="233d6-404">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>



| <span data-ttu-id="233d6-405">Valor</span><span class="sxs-lookup"><span data-stu-id="233d6-405">Value</span></span>                                                                                                | <span data-ttu-id="233d6-406">Significado</span><span class="sxs-lookup"><span data-stu-id="233d6-406">Meaning</span></span>                                                                                    |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="233d6-407"><dt>"Count (bloco de tamanho fixo)"</dt></span><span class="sxs-lookup"><span data-stu-id="233d6-407"><dt>"count(fixed size block)"</dt></span></span> </dl> | <span data-ttu-id="233d6-408">O tamanho do bloco fixo está contido na propriedade **VirtualResourceBlockSize** .</span><span class="sxs-lookup"><span data-stu-id="233d6-408">The fixed block size is contained in the **VirtualResourceBlockSize** property.</span></span><br/> |
| <dl> <span data-ttu-id="233d6-409"><dt>minuciosa</dt></span><span class="sxs-lookup"><span data-stu-id="233d6-409"><dt>"byte"</dt></span></span> </dl>                    | <span data-ttu-id="233d6-410">A propriedade **VirtualQuantity** é medida em bytes.</span><span class="sxs-lookup"><span data-stu-id="233d6-410">The **VirtualQuantity** property is measured in bytes.</span></span><br/>                          |



 

</dd> <dt>

<span data-ttu-id="233d6-411">**VirtualResourceBlockSize**</span><span class="sxs-lookup"><span data-stu-id="233d6-411">**VirtualResourceBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-412">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="233d6-412">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-413">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="233d6-414">O tamanho, em bytes, dos blocos que são apresentados ao consumidor como resultado dessa solicitação de alocação de recursos de armazenamento ou alocação de recursos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="233d6-414">The size, in bytes, of the blocks that are presented to the consumer as the result of this storage resource allocation or storage resource allocation request.</span></span> <span data-ttu-id="233d6-415">Se o tamanho do bloco for variável, o tamanho máximo do bloco, em bytes, será especificado.</span><span class="sxs-lookup"><span data-stu-id="233d6-415">If the block size is variable, then the maximum block size, in bytes, will be specified.</span></span> <span data-ttu-id="233d6-416">Se o tamanho do bloco for desconhecido ou se um conceito de bloco não se aplicar, o valor 1 será usado.</span><span class="sxs-lookup"><span data-stu-id="233d6-416">If the block size is unknown or if a block concept does not apply, then the value 1 will be used.</span></span> <span data-ttu-id="233d6-417">Essa propriedade é herdada do **CIM \_ StorageAllocationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="233d6-417">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="233d6-418">**Weight**</span><span class="sxs-lookup"><span data-stu-id="233d6-418">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-419">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="233d6-419">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-420">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-420">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="233d6-421">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("peso"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (10000)</span><span class="sxs-lookup"><span data-stu-id="233d6-421">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Weight"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (10000)</span></span>
</dt> </dl>

<span data-ttu-id="233d6-422">Especifica uma prioridade relativa para essa alocação em relação a outras alocações do mesmo pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="233d6-422">Specifies a relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="233d6-423">Essa propriedade não tem nenhuma unidade de medida e só é relevante quando comparada a outras alocações vying para os mesmos recursos de host.</span><span class="sxs-lookup"><span data-stu-id="233d6-423">This property has no unit of measure and is only relevant when compared to other allocations vying for the same host resources.</span></span> <span data-ttu-id="233d6-424">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="233d6-424">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="233d6-425">Intervalo: 1 10000</span><span class="sxs-lookup"><span data-stu-id="233d6-425">Range: 1 10000</span></span>

</dd> <dt>

<span data-ttu-id="233d6-426">**WriteHardeningMethod**</span><span class="sxs-lookup"><span data-stu-id="233d6-426">**WriteHardeningMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="233d6-427">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="233d6-427">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="233d6-428">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="233d6-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="233d6-429">Indica qual método de proteção contra gravação é suportado pelo disco.</span><span class="sxs-lookup"><span data-stu-id="233d6-429">Indicates what write hardening method is supported by the disk.</span></span>

> [!Note]  
> <span data-ttu-id="233d6-430">Essa propriedade foi adicionada no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="233d6-430">This property was added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="233d6-431">**Padrão** (0)</span><span class="sxs-lookup"><span data-stu-id="233d6-431">**Default** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="WriteCacheEnabled"></span><span id="writecacheenabled"></span><span id="WRITECACHEENABLED"></span>

<span data-ttu-id="233d6-432">**WriteCacheEnabled** (1)</span><span class="sxs-lookup"><span data-stu-id="233d6-432">**WriteCacheEnabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="WriteCacheandFUAEnabled"></span><span id="writecacheandfuaenabled"></span><span id="WRITECACHEANDFUAENABLED"></span>

<span data-ttu-id="233d6-433">**WriteCacheandFUAEnabled** (2)</span><span class="sxs-lookup"><span data-stu-id="233d6-433">**WriteCacheandFUAEnabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WriteCacheDisabled"></span><span id="writecachedisabled"></span><span id="WRITECACHEDISABLED"></span>

<span data-ttu-id="233d6-434">**WriteCacheDisabled** (3)</span><span class="sxs-lookup"><span data-stu-id="233d6-434">**WriteCacheDisabled** (3)</span></span>


<span data-ttu-id="233d6-435"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="233d6-435"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="233d6-436">Requisitos</span><span class="sxs-lookup"><span data-stu-id="233d6-436">Requirements</span></span>



| <span data-ttu-id="233d6-437">Requisito</span><span class="sxs-lookup"><span data-stu-id="233d6-437">Requirement</span></span> | <span data-ttu-id="233d6-438">Valor</span><span class="sxs-lookup"><span data-stu-id="233d6-438">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="233d6-439">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="233d6-439">Minimum supported client</span></span><br/> | <span data-ttu-id="233d6-440">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="233d6-440">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="233d6-441">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="233d6-441">Minimum supported server</span></span><br/> | <span data-ttu-id="233d6-442">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="233d6-442">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="233d6-443">Namespace</span><span class="sxs-lookup"><span data-stu-id="233d6-443">Namespace</span></span><br/>                | <span data-ttu-id="233d6-444">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="233d6-444">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="233d6-445">MOF</span><span class="sxs-lookup"><span data-stu-id="233d6-445">MOF</span></span><br/>                      | <dl> <span data-ttu-id="233d6-446"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="233d6-446"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="233d6-447">DLL</span><span class="sxs-lookup"><span data-stu-id="233d6-447">DLL</span></span><br/>                      | <dl> <span data-ttu-id="233d6-448"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="233d6-448"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


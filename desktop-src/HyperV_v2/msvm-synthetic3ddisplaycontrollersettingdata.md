---
description: Representa as configurações de um controlador de vídeo sintético 3D para uma máquina virtual.
ms.assetid: 7162AEED-90CB-41C3-BD44-8B552C00F597
title: Classe Msvm_Synthetic3DDisplayControllerSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DDisplayControllerSettingData
- Msvm_Synthetic3DDisplayControllerSettingData.InstanceID
- Msvm_Synthetic3DDisplayControllerSettingData.Caption
- Msvm_Synthetic3DDisplayControllerSettingData.Description
- Msvm_Synthetic3DDisplayControllerSettingData.ElementName
- Msvm_Synthetic3DDisplayControllerSettingData.ResourceType
- Msvm_Synthetic3DDisplayControllerSettingData.OtherResourceType
- Msvm_Synthetic3DDisplayControllerSettingData.ResourceSubType
- Msvm_Synthetic3DDisplayControllerSettingData.PoolID
- Msvm_Synthetic3DDisplayControllerSettingData.ConsumerVisibility
- Msvm_Synthetic3DDisplayControllerSettingData.HostResource
- Msvm_Synthetic3DDisplayControllerSettingData.AllocationUnits
- Msvm_Synthetic3DDisplayControllerSettingData.VirtualQuantity
- Msvm_Synthetic3DDisplayControllerSettingData.Reservation
- Msvm_Synthetic3DDisplayControllerSettingData.Limit
- Msvm_Synthetic3DDisplayControllerSettingData.Weight
- Msvm_Synthetic3DDisplayControllerSettingData.AutomaticAllocation
- Msvm_Synthetic3DDisplayControllerSettingData.AutomaticDeallocation
- Msvm_Synthetic3DDisplayControllerSettingData.Parent
- Msvm_Synthetic3DDisplayControllerSettingData.Connection
- Msvm_Synthetic3DDisplayControllerSettingData.Address
- Msvm_Synthetic3DDisplayControllerSettingData.MappingBehavior
- Msvm_Synthetic3DDisplayControllerSettingData.AddressOnParent
- Msvm_Synthetic3DDisplayControllerSettingData.VirtualQuantityUnits
- Msvm_Synthetic3DDisplayControllerSettingData.MaximumScreenResolution
- Msvm_Synthetic3DDisplayControllerSettingData.MaximumMonitors
- Msvm_Synthetic3DDisplayControllerSettingData.VRAMSizeBytes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c93bb67cd4a66c4ecc5f6820ff2de7cf3816b2b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778583"
---
# <a name="msvm_synthetic3ddisplaycontrollersettingdata-class"></a><span data-ttu-id="61cba-103">\_Classe Msvm Synthetic3DDisplayControllerSettingData</span><span class="sxs-lookup"><span data-stu-id="61cba-103">Msvm\_Synthetic3DDisplayControllerSettingData class</span></span>

<span data-ttu-id="61cba-104">Representa as configurações de um controlador de vídeo sintético 3D para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="61cba-104">Represents settings for a synthetic 3-D display controller for a virtual machine.</span></span> <span data-ttu-id="61cba-105">Essa classe é usada somente com máquinas virtuais que usam o RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="61cba-105">This class is only used with virtual machines that use RemoteFX.</span></span>

<span data-ttu-id="61cba-106">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="61cba-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="61cba-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61cba-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Synthetic3DDisplayControllerSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "3D Display Controller Default Settings";
  string  Description = "Describes the default settings for the 3D video controller resource pool.";
  string  ElementName;
  uint16  ResourceType = 24;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft:Hyper-V:Synthetic 3D Display Controller";
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits = "count";
  uint64  VirtualQuantity = 1;
  uint64  Reservation = 1;
  uint64  Limit = 1;
  uint32  Weight = 0;
  boolean AutomaticAllocation = True;
  boolean AutomaticDeallocation = True;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  uint8   MaximumScreenResolution;
  uint8   MaximumMonitors;
  uint64  VRAMSizeBytes;
};
```

## <a name="members"></a><span data-ttu-id="61cba-108">Membros</span><span class="sxs-lookup"><span data-stu-id="61cba-108">Members</span></span>

<span data-ttu-id="61cba-109">A classe **Msvm \_ Synthetic3DDisplayControllerSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="61cba-109">The **Msvm\_Synthetic3DDisplayControllerSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="61cba-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="61cba-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="61cba-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="61cba-111">Properties</span></span>

<span data-ttu-id="61cba-112">A classe **Msvm \_ Synthetic3DDisplayControllerSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="61cba-112">The **Msvm\_Synthetic3DDisplayControllerSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="61cba-113">**Endereço**</span><span class="sxs-lookup"><span data-stu-id="61cba-113">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61cba-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="61cba-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61cba-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61cba-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61cba-116">O endereço do recurso.</span><span class="sxs-lookup"><span data-stu-id="61cba-116">The address of the resource.</span></span> <span data-ttu-id="61cba-117">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="61cba-117">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="61cba-118">Essa é uma propriedade somente leitura, mas se a propriedade **ResourceType** for 20 (controlador de gráficos), ela poderá ser alterada usando o método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="61cba-118">This is a read-only property, but if the **ResourceType** property is 20 (Graphics controller), it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="61cba-119">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="61cba-119">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61cba-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="61cba-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61cba-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61cba-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61cba-122">Descreve o endereço deste recurso no contexto do pai.</span><span class="sxs-lookup"><span data-stu-id="61cba-122">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="61cba-123">As propriedades **pai** e **AddressOnParent** são usadas para descrever a relação do controlador, bem como a ordem dos dispositivos em um controlador.</span><span class="sxs-lookup"><span data-stu-id="61cba-123">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="61cba-124">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="61cba-124">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="61cba-125">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="61cba-125">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61cba-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="61cba-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61cba-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61cba-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61cba-128">As unidades de alocação usadas pelas propriedades **Reservation** e **Limit** .</span><span class="sxs-lookup"><span data-stu-id="61cba-128">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="61cba-129">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="61cba-129">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="61cba-130">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="61cba-130">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61cba-131">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="61cba-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="61cba-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61cba-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61cba-133">Indica se o recurso será alocado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="61cba-133">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="61cba-134">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="61cba-134">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="61cba-135">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="61cba-135">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61cba-136">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="61cba-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="61cba-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61cba-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61cba-138">Indica se o recurso será desalocado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="61cba-138">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="61cba-139">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="61cba-139">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="61cba-140">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="61cba-140">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61cba-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="61cba-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61cba-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61cba-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61cba-143">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="61cba-143">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="61cba-144">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="61cba-144">A short description of the object.</span></span> <span data-ttu-id="61cba-145">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="61cba-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="61cba-146">**Conexão**</span><span class="sxs-lookup"><span data-stu-id="61cba-146">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61cba-147">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="61cba-147">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="61cba-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61cba-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61cba-149">O dispositivo ao qual esse recurso está conectado.</span><span class="sxs-lookup"><span data-stu-id="61cba-149">The device to which this resource is connected.</span></span> <span data-ttu-id="61cba-150">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="61cba-150">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="61cba-151">Esta é uma propriedade somente leitura, mas se 1) a propriedade **ResourceType** é 17 (porta serial) ou 2) a propriedade **ResourceType** é 21 (extensão de armazenamento) e a propriedade **ResourceSubType** é "disco rígido virtual da Microsoft", então ela pode ser alterada usando o método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="61cba-151">This is a read-only property, but if either 1) the **ResourceType** property is 17 (Serial port), or 2) the **ResourceType** property is 21 (Storage Extent) and the **ResourceSubType** property is "Microsoft Virtual Hard Disk", then it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="61cba-152">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="61cba-152">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61cba-153">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="61cba-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="61cba-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61cba-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61cba-155">A visibilidade do consumidor para o recurso alocado.</span><span class="sxs-lookup"><span data-stu-id="61cba-155">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="61cba-156">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="61cba-156">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="61cba-157">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="61cba-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61cba-158">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="61cba-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61cba-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61cba-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61cba-160">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="61cba-160">A description of the object.</span></span> <span data-ttu-id="61cba-161">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="61cba-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="61cba-162">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="61cba-162">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61cba-163">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="61cba-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61cba-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61cba-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61cba-165">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="61cba-165">A display name for the object.</span></span> <span data-ttu-id="61cba-166">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="61cba-166">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="61cba-167">A alteração dessa propriedade irá alterar o nome do elemento do derivado do dispositivo lógico associado.</span><span class="sxs-lookup"><span data-stu-id="61cba-167">Changing this property will change the element name of the associated logical device derivative.</span></span>

</dd> <dt>

<span data-ttu-id="61cba-168">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="61cba-168">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61cba-169">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="61cba-169">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="61cba-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61cba-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61cba-171">Somente um recurso de host pode ser atribuído a cada dispositivo na máquina virtual, de modo que somente o primeiro elemento dessa matriz pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="61cba-171">Only one host resource can be assigned to each device in the virtual machine, so only the first element of this array can be set.</span></span> <span data-ttu-id="61cba-172">Para dispositivos que dão suporte a esse recurso, defina o primeiro elemento da matriz **HostResource** para conter uma referência ao recurso de host subjacente que será atribuído.</span><span class="sxs-lookup"><span data-stu-id="61cba-172">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource that is to be assigned.</span></span> <span data-ttu-id="61cba-173">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="61cba-173">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="61cba-174">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="61cba-174">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61cba-175">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="61cba-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61cba-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61cba-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61cba-177">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="61cba-177">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="61cba-178">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="61cba-178">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="61cba-179">**Limite**</span><span class="sxs-lookup"><span data-stu-id="61cba-179">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61cba-180">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="61cba-180">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="61cba-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61cba-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61cba-182">A quantidade máxima de recursos de host correspondentes que podem ser consumidos pela máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="61cba-182">The maximum amount of corresponding host resources that can be consumed by the virtual machine.</span></span> <span data-ttu-id="61cba-183">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="61cba-183">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="61cba-184">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="61cba-184">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61cba-185">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="61cba-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="61cba-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61cba-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61cba-187">Especifica como esse recurso é mapeado para recursos subjacentes.</span><span class="sxs-lookup"><span data-stu-id="61cba-187">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="61cba-188">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="61cba-188">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="61cba-189">**MaximumMonitors**</span><span class="sxs-lookup"><span data-stu-id="61cba-189">**MaximumMonitors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61cba-190">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="61cba-190">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="61cba-191">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="61cba-191">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="61cba-192">O número máximo de monitores disponíveis para o controlador de vídeo 3-D.</span><span class="sxs-lookup"><span data-stu-id="61cba-192">The maximum number of monitors available to the 3-D display controller.</span></span> <span data-ttu-id="61cba-193">O número mínimo de monitores é 1 e o máximo depende da resolução máxima da tela.</span><span class="sxs-lookup"><span data-stu-id="61cba-193">The minimum number of monitors is 1 and the maximum is dependent upon the maximum screen resolution.</span></span> <span data-ttu-id="61cba-194">A tabela a seguir define o número máximo de monitores permitidos para resoluções diferentes.</span><span class="sxs-lookup"><span data-stu-id="61cba-194">The following table defines the maximum number of monitors allowed for different resolutions.</span></span>



| <span data-ttu-id="61cba-195">Resolução</span><span class="sxs-lookup"><span data-stu-id="61cba-195">Resolution</span></span>            | <span data-ttu-id="61cba-196">Máximo de monitores</span><span class="sxs-lookup"><span data-stu-id="61cba-196">Maximum monitors</span></span> |
|-----------------------|------------------|
| <span data-ttu-id="61cba-197">1024 768</span><span class="sxs-lookup"><span data-stu-id="61cba-197">1024  768</span></span><br/>  | <span data-ttu-id="61cba-198">4</span><span class="sxs-lookup"><span data-stu-id="61cba-198">4</span></span><br/>     |
| <span data-ttu-id="61cba-199">1280 1024</span><span class="sxs-lookup"><span data-stu-id="61cba-199">1280  1024</span></span><br/> | <span data-ttu-id="61cba-200">4</span><span class="sxs-lookup"><span data-stu-id="61cba-200">4</span></span><br/>     |
| <span data-ttu-id="61cba-201">1600 1200</span><span class="sxs-lookup"><span data-stu-id="61cba-201">1600  1200</span></span><br/> | <span data-ttu-id="61cba-202">3</span><span class="sxs-lookup"><span data-stu-id="61cba-202">3</span></span><br/>     |
| <span data-ttu-id="61cba-203">1920 1200</span><span class="sxs-lookup"><span data-stu-id="61cba-203">1920  1200</span></span><br/> | <span data-ttu-id="61cba-204">2</span><span class="sxs-lookup"><span data-stu-id="61cba-204">2</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="61cba-205">**MaximumScreenResolution**</span><span class="sxs-lookup"><span data-stu-id="61cba-205">**MaximumScreenResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61cba-206">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="61cba-206">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="61cba-207">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61cba-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61cba-208">Especifica a resolução máxima de tela para o controlador de vídeo 3-D.</span><span class="sxs-lookup"><span data-stu-id="61cba-208">Specifies the maximum screen resolution for the 3-D display controller.</span></span> <span data-ttu-id="61cba-209">Deve ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="61cba-209">This must be one of the following values.</span></span>

<dt>

<span id="1024___768"></span>

<span data-ttu-id="61cba-210"><span id="1024___768"></span>**1024 \* 768** (0)</span><span class="sxs-lookup"><span data-stu-id="61cba-210"><span id="1024___768"></span>**1024 \* 768** (0)</span></span>


</dt> <dd>

<span data-ttu-id="61cba-211">A resolução máxima é 1024 768.</span><span class="sxs-lookup"><span data-stu-id="61cba-211">The maximum resolution is 1024   768.</span></span>

</dd> <dt>

<span id="1280___1024"></span>

<span data-ttu-id="61cba-212"><span id="1280___1024"></span>**1280 \* 1024** (1)</span><span class="sxs-lookup"><span data-stu-id="61cba-212"><span id="1280___1024"></span>**1280 \* 1024** (1)</span></span>


</dt> <dd>

<span data-ttu-id="61cba-213">A resolução máxima é 1280 1024.</span><span class="sxs-lookup"><span data-stu-id="61cba-213">The maximum resolution is 1280   1024.</span></span>

</dd> <dt>

<span id="1600___1200"></span>

<span data-ttu-id="61cba-214"><span id="1600___1200"></span>**1600 \* 1200** (2)</span><span class="sxs-lookup"><span data-stu-id="61cba-214"><span id="1600___1200"></span>**1600 \* 1200** (2)</span></span>


</dt> <dd>

<span data-ttu-id="61cba-215">A resolução máxima é 1600 1200.</span><span class="sxs-lookup"><span data-stu-id="61cba-215">The maximum resolution is 1600   1200.</span></span>

</dd> <dt>

<span id="1920___1200"></span>

<span data-ttu-id="61cba-216"><span id="1920___1200"></span>**1920 \* 1200** (3)</span><span class="sxs-lookup"><span data-stu-id="61cba-216"><span id="1920___1200"></span>**1920 \* 1200** (3)</span></span>


</dt> <dd>

<span data-ttu-id="61cba-217">A resolução máxima é 1920 1200.</span><span class="sxs-lookup"><span data-stu-id="61cba-217">The maximum resolution is 1920   1200.</span></span>

</dd> <dt>

<span id="2560___1600"></span>

<span data-ttu-id="61cba-218"><span id="2560___1600"></span>**2560 \* 1600** (4)</span><span class="sxs-lookup"><span data-stu-id="61cba-218"><span id="2560___1600"></span>**2560 \* 1600** (4)</span></span>


</dt> <dd>

<span data-ttu-id="61cba-219">A resolução máxima é 2650 1600.</span><span class="sxs-lookup"><span data-stu-id="61cba-219">The maximum resolution is 2650   1600.</span></span>

</dd> <dt>

<span id="3840___2160"></span>

<span data-ttu-id="61cba-220"><span id="3840___2160"></span>**3840 \* 2160** (5)</span><span class="sxs-lookup"><span data-stu-id="61cba-220"><span id="3840___2160"></span>**3840 \* 2160** (5)</span></span>


</dt> <dd>

<span data-ttu-id="61cba-221">A resolução máxima é 3840 2160.</span><span class="sxs-lookup"><span data-stu-id="61cba-221">The maximum resolution is 3840   2160.</span></span>

> [!Note]  
> <span data-ttu-id="61cba-222">Adicionado ao Windows 10 e ao Windows Server 2016. msvm \_ synte</span><span class="sxs-lookup"><span data-stu-id="61cba-222">Added in Windows 10 and Windows Server 2016.msvm\_synte</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="61cba-223">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="61cba-223">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61cba-224">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="61cba-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61cba-225">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61cba-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61cba-226">Uma cadeia de caracteres que descreve o tipo de recurso quando um valor bem definido não está disponível e [**ResourceType**](msvm-processorsettingdata.md) tem o valor 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="61cba-226">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1(Other).</span></span> <span data-ttu-id="61cba-227">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="61cba-227">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="61cba-228">**Pai**</span><span class="sxs-lookup"><span data-stu-id="61cba-228">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61cba-229">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="61cba-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61cba-230">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61cba-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61cba-231">O pai do recurso.</span><span class="sxs-lookup"><span data-stu-id="61cba-231">The parent of the resource.</span></span> <span data-ttu-id="61cba-232">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="61cba-232">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="61cba-233">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="61cba-233">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61cba-234">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="61cba-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61cba-235">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61cba-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61cba-236">O identificador do pool de recursos do qual esse recurso foi alocado.</span><span class="sxs-lookup"><span data-stu-id="61cba-236">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="61cba-237">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="61cba-237">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="61cba-238">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="61cba-238">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61cba-239">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="61cba-239">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="61cba-240">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61cba-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61cba-241">A quantidade de recursos de CPU que são reservados para uso pela máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="61cba-241">The amount of CPU resources that are reserved for use by the virtual machine.</span></span> <span data-ttu-id="61cba-242">É garantido que esses recursos estejam disponíveis para consumo pela máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="61cba-242">These resources are guaranteed to be available for consumption by the virtual machine.</span></span> <span data-ttu-id="61cba-243">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="61cba-243">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="61cba-244">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="61cba-244">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61cba-245">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="61cba-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61cba-246">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61cba-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61cba-247">Uma cadeia de caracteres que descreve um subtipo específico de implementação para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="61cba-247">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="61cba-248">Por exemplo, isso pode ser usado para distinguir modelos diferentes do mesmo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="61cba-248">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="61cba-249">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="61cba-249">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="61cba-250">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="61cba-250">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61cba-251">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="61cba-251">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="61cba-252">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61cba-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61cba-253">O tipo de recurso que essa configuração de alocação representa.</span><span class="sxs-lookup"><span data-stu-id="61cba-253">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="61cba-254">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="61cba-254">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="61cba-255">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="61cba-255">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61cba-256">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="61cba-256">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="61cba-257">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61cba-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61cba-258">O número total de núcleos na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="61cba-258">The total number of cores in the virtual machine.</span></span> <span data-ttu-id="61cba-259">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="61cba-259">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="61cba-260">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="61cba-260">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61cba-261">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="61cba-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61cba-262">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61cba-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61cba-263">Especifica a unidade de medida para a propriedade **VirtualQuantity** .</span><span class="sxs-lookup"><span data-stu-id="61cba-263">Specifies the unit of measurement for the **VirtualQuantity** property.</span></span> <span data-ttu-id="61cba-264">O valor dessa propriedade deve ser um valor válido do qualificador de unidades programáticas, conforme definido no anexo C. 1 de DSP0004 V 2.5 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="61cba-264">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="61cba-265">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="61cba-265">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="61cba-266">**VRAMSizeBytes**</span><span class="sxs-lookup"><span data-stu-id="61cba-266">**VRAMSizeBytes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61cba-267">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="61cba-267">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="61cba-268">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="61cba-268">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="61cba-269">O tamanho da memória de vídeo para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="61cba-269">The video memory size for the Virtual Machine.</span></span>

> [!Note]  
> <span data-ttu-id="61cba-270">Adicionado ao Windows 10 e ao Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="61cba-270">Added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>



 <span data-ttu-id="61cba-271">(67108864)</span><span class="sxs-lookup"><span data-stu-id="61cba-271">(67108864)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="61cba-272">(134217728)</span><span class="sxs-lookup"><span data-stu-id="61cba-272">(134217728)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="61cba-273">(268435456)</span><span class="sxs-lookup"><span data-stu-id="61cba-273">(268435456)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="61cba-274">(536870912)</span><span class="sxs-lookup"><span data-stu-id="61cba-274">(536870912)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="61cba-275">(1073741824)</span><span class="sxs-lookup"><span data-stu-id="61cba-275">(1073741824)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="61cba-276">**Weight**</span><span class="sxs-lookup"><span data-stu-id="61cba-276">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61cba-277">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="61cba-277">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="61cba-278">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61cba-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61cba-279">Um inteiro que define o peso para cada processador de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="61cba-279">An integer that defines the weight for each virtual machine processor.</span></span> <span data-ttu-id="61cba-280">Depois que todas as reservas forem atendidas, a capacidade física restante do processador da plataforma de hospedagem será alocada às máquinas virtuais com base em seus pesos relativos.</span><span class="sxs-lookup"><span data-stu-id="61cba-280">After all reserves have been met, the remaining physical processor capacity of the hosting platform will be allocated to virtual machines based on their relative weights.</span></span> <span data-ttu-id="61cba-281">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="61cba-281">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="61cba-282">0</span><span class="sxs-lookup"><span data-stu-id="61cba-282">0</span></span>

<span data-ttu-id="61cba-283">Intervalo: 0 1000</span><span class="sxs-lookup"><span data-stu-id="61cba-283">Range: 0 1000</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="61cba-284">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61cba-284">Requirements</span></span>



| <span data-ttu-id="61cba-285">Requisito</span><span class="sxs-lookup"><span data-stu-id="61cba-285">Requirement</span></span> | <span data-ttu-id="61cba-286">Valor</span><span class="sxs-lookup"><span data-stu-id="61cba-286">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61cba-287">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61cba-287">Minimum supported client</span></span><br/> | <span data-ttu-id="61cba-288">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="61cba-288">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="61cba-289">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61cba-289">Minimum supported server</span></span><br/> | <span data-ttu-id="61cba-290">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="61cba-290">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="61cba-291">Namespace</span><span class="sxs-lookup"><span data-stu-id="61cba-291">Namespace</span></span><br/>                | <span data-ttu-id="61cba-292">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="61cba-292">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="61cba-293">MOF</span><span class="sxs-lookup"><span data-stu-id="61cba-293">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61cba-294"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-294"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="61cba-295">DLL</span><span class="sxs-lookup"><span data-stu-id="61cba-295">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61cba-296"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-296"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

